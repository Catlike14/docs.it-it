---
title: Implementazione di tentativi di chiamata HTTP personalizzati con backoff esponenziale
description: Architettura di Microservizi .NET per le applicazioni nei contenitori .NET | Implementazione di tentativi di chiamata HTTP personalizzati con backoff esponenziale
keywords: Docker, microservizi, ASP.NET, contenitore
author: CESARDELATORRE
ms.author: wiwagn
ms.date: 05/26/2017
ms.prod: .net-core
ms.technology: dotnet-docker
ms.topic: article
ms.openlocfilehash: 4449e5d7e0ca3c81aead26fac653de3ba2187a92
ms.sourcegitcommit: bd1ef61f4bb794b25383d3d72e71041a5ced172e
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 10/18/2017
---
# <a name="implementing-custom-http-call-retries-with-exponential-backoff"></a><span data-ttu-id="b0bc7-104">Implementazione di tentativi di chiamata HTTP personalizzati con backoff esponenziale</span><span class="sxs-lookup"><span data-stu-id="b0bc7-104">Implementing custom HTTP call retries with exponential backoff</span></span>

<span data-ttu-id="b0bc7-105">Per creare microservizi resiliente, è necessario gestire possibili scenari di errore HTTP.</span><span class="sxs-lookup"><span data-stu-id="b0bc7-105">In order to create resilient microservices, you need to handle possible HTTP failure scenarios.</span></span> <span data-ttu-id="b0bc7-106">A tale scopo, è possibile creare la propria implementazione di tentativi con backoff esponenziale.</span><span class="sxs-lookup"><span data-stu-id="b0bc7-106">For that purpose, you could create your own implementation of retries with exponential backoff.</span></span>

<span data-ttu-id="b0bc7-107">Oltre alla gestione di indisponibilità di risorse temporale, il backoff esponenziale deve inoltre prendere in considerazione che il provider di cloud potrebbe limitare la disponibilità di risorse per evitare l'overload di utilizzo.</span><span class="sxs-lookup"><span data-stu-id="b0bc7-107">In addition to handling temporal resource unavailability, the exponential backoff also needs to take into account that the cloud provider might throttle availability of resources to prevent usage overload.</span></span> <span data-ttu-id="b0bc7-108">Ad esempio, molto rapidamente la creazione di un numero eccessivo di richieste di connessione potrebbe essere visualizzata come un Denial of Service ([DoS](https://en.wikipedia.org/wiki/Denial-of-service_attack)) attacco dal provider di cloud.</span><span class="sxs-lookup"><span data-stu-id="b0bc7-108">For example, creating too many connection requests very quickly might be viewed as a Denial of Service ([DoS](https://en.wikipedia.org/wiki/Denial-of-service_attack)) attack by the cloud provider.</span></span> <span data-ttu-id="b0bc7-109">Di conseguenza, è necessario fornire un meccanismo per ridimensionare le richieste di connessione quando è stato rilevato un limite della capacità.</span><span class="sxs-lookup"><span data-stu-id="b0bc7-109">As a result, you need to provide a mechanism to scale back connection requests when a capacity threshold has been encountered.</span></span>

<span data-ttu-id="b0bc7-110">Come un'esplorazione iniziale, è possibile implementare codice personalizzato con una classe di utilità per backoff esponenziale come in [RetryWithExponentialBackoff.cs](https://gist.github.com/CESARDELATORRE/6d7f647b29e55fdc219ee1fd2babb260), più codice simile al seguente (che è disponibile anche su un [repository GitHub ](https://gist.github.com/CESARDELATORRE/d80c6423a1aebaffaf387469f5194f5b)).</span><span class="sxs-lookup"><span data-stu-id="b0bc7-110">As an initial exploration, you could implement your own code with a utility class for exponential backoff as in [RetryWithExponentialBackoff.cs](https://gist.github.com/CESARDELATORRE/6d7f647b29e55fdc219ee1fd2babb260), plus code like the following (which is also available on a [GitHub repo](https://gist.github.com/CESARDELATORRE/d80c6423a1aebaffaf387469f5194f5b)).</span></span>

```csharp
public sealed class RetryWithExponentialBackoff
{
    private readonly int maxRetries, delayMilliseconds, maxDelayMilliseconds;

    public RetryWithExponentialBackoff(int maxRetries = 50,
        int delayMilliseconds = 200,
        int maxDelayMilliseconds = 2000)
    {
        this.maxRetries = maxRetries;
        this.delayMilliseconds = delayMilliseconds;
        this.maxDelayMilliseconds = maxDelayMilliseconds;
    }

    public async Task RunAsync(Func<Task> func)
    {
        ExponentialBackoff backoff = new ExponentialBackoff(this.maxRetries,
            this.delayMilliseconds,
            this.maxDelayMilliseconds);
        retry:
        try
        {
            await func();
        }
        catch (Exception ex) when (ex is TimeoutException ||
            ex is System.Net.Http.HttpRequestException)
        {
            Debug.WriteLine("Exception raised is: " +
                ex.GetType().ToString() +
                " –Message: " + ex.Message +
                " -- Inner Message: " +
                ex.InnerException.Message);
            await backoff.Delay();
            goto retry;
        }
    }
}

public struct ExponentialBackoff
{
    private readonly int m_maxRetries, m_delayMilliseconds, m_maxDelayMilliseconds;
    private int m_retries, m_pow;

    public ExponentialBackoff(int maxRetries, int delayMilliseconds,
        int maxDelayMilliseconds)
    {
        m_maxRetries = maxRetries;
        m_delayMilliseconds = delayMilliseconds;
        m_maxDelayMilliseconds = maxDelayMilliseconds;
        m_retries = 0;
        m_pow = 1;
    }

    public Task Delay()
    {
        if (m_retries == m_maxRetries)
        {
            throw new TimeoutException("Max retry attempts exceeded.");
        }
        ++m_retries;
        if (m_retries < 31)
        {
            m_pow = m_pow << 1; // m_pow = Pow(2, m_retries - 1)
        }
        int delay = Math.Min(m_delayMilliseconds * (m_pow - 1) / 2,
            m_maxDelayMilliseconds);
        return Task.Delay(delay);
    }
}
```

<span data-ttu-id="b0bc7-111">Con questo codice in un client C\# applicazione (anche una C, un'applicazione MVC ASP.NET o un'altra API Web client microservizio\# Xamarin applicazione) è semplice.</span><span class="sxs-lookup"><span data-stu-id="b0bc7-111">Using this code in a client C\# application (another Web API client microservice, an ASP.NET MVC application, or even a C\# Xamarin application) is straightforward.</span></span> <span data-ttu-id="b0bc7-112">Nell'esempio seguente, mediante la classe HttpClient.</span><span class="sxs-lookup"><span data-stu-id="b0bc7-112">The following example shows how, using the HttpClient class.</span></span>

```csharp
public async Task<Catalog> GetCatalogItems(int page,int take, int? brand, int? type)
{
    _apiClient = new HttpClient();
    var itemsQs = $"items?pageIndex={page}&pageSize={take}";
    var filterQs = "";
    var catalogUrl = $"{_remoteServiceBaseUrl}items{filterQs}?pageIndex={page}&pageSize={take}";
    var dataString = "";
    //
    // Using HttpClient with Retry and Exponential Backoff
    //
    var retry = new RetryWithExponentialBackoff();
    await retry.RunAsync(async () =>
    {
        // work with HttpClient call
        dataString = await _apiClient.GetStringAsync(catalogUrl);
    });
    return JsonConvert.DeserializeObject<Catalog>(dataString);
}
```

<span data-ttu-id="b0bc7-113">Tuttavia, questo codice è adatto solo come un modello di prova.</span><span class="sxs-lookup"><span data-stu-id="b0bc7-113">However, this code is suitable only as a proof of concept.</span></span> <span data-ttu-id="b0bc7-114">L'argomento successivo viene illustrato come utilizzare più sofisticate e sperimentate le librerie.</span><span class="sxs-lookup"><span data-stu-id="b0bc7-114">The next topic explains how to use more sophisticated and proven libraries.</span></span>


>[!div class="step-by-step"]
<span data-ttu-id="b0bc7-115">[Precedente] [Avanti] (implement-http-call-retries-exponential-backoff-polly.md) (implement-resilient-entity-framework-core-sql-connections.md)</span><span class="sxs-lookup"><span data-stu-id="b0bc7-115">[Previous] (implement-resilient-entity-framework-core-sql-connections.md) [Next] (implement-http-call-retries-exponential-backoff-polly.md)</span></span>
