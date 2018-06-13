---
title: 'Procedura: personalizzare i feed con il provider di reflection (WCF Data Services)'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- WCF Data Services, customizing
- WCF Data Services, customizing feeds
ms.assetid: 00c23dcf-9bb8-459a-a012-6c4d9bcad7e9
ms.openlocfilehash: 984a4aac43689be0ec80e7f6c289e8d5229e9e1b
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 05/04/2018
ms.locfileid: "33358008"
---
# <a name="how-to-customize-feeds-with-the-reflection-provider-wcf-data-services"></a><span data-ttu-id="e7322-102">Procedura: personalizzare i feed con il provider di reflection (WCF Data Services)</span><span class="sxs-lookup"><span data-stu-id="e7322-102">How to: Customize Feeds with the Reflection Provider (WCF Data Services)</span></span>
[!INCLUDE[ssAstoria](../../../../includes/ssastoria-md.md)]<span data-ttu-id="e7322-103"> consente di personalizzare la serializzazione Atom in una risposta del servizio dati in modo che venga eseguito il mapping delle proprietà di un'entità agli elementi inutilizzati definiti nel protocollo AtomPub.</span><span class="sxs-lookup"><span data-stu-id="e7322-103"> enables you to customize the Atom serialization in a data service response so that properties of an entity may be mapped to unused elements that are defined in the AtomPub protocol.</span></span> <span data-ttu-id="e7322-104">In questo argomento viene illustrato come definire attributi di mapping per i tipi di entità in un modello di dati definito tramite il provider di reflection.</span><span class="sxs-lookup"><span data-stu-id="e7322-104">This topic shows how to define mapping attributes for the entity types in a data model that is defined by using the reflection provider.</span></span> <span data-ttu-id="e7322-105">Per ulteriori informazioni, vedere [personalizzazione Feed](../../../../docs/framework/data/wcf/feed-customization-wcf-data-services.md).</span><span class="sxs-lookup"><span data-stu-id="e7322-105">For more information, see [Feed Customization](../../../../docs/framework/data/wcf/feed-customization-wcf-data-services.md).</span></span>  
  
 <span data-ttu-id="e7322-106">Il modello di dati per questo esempio viene definito nell'argomento [procedura: creare un servizio dati tramite il Provider di Reflection](../../../../docs/framework/data/wcf/create-a-data-service-using-rp-wcf-data-services.md)</span><span class="sxs-lookup"><span data-stu-id="e7322-106">The data model for this example is defined in the topic [How to: Create a Data Service Using the Reflection Provider](../../../../docs/framework/data/wcf/create-a-data-service-using-rp-wcf-data-services.md)</span></span>  
  
## <a name="example"></a><span data-ttu-id="e7322-107">Esempio</span><span class="sxs-lookup"><span data-stu-id="e7322-107">Example</span></span>  
 <span data-ttu-id="e7322-108">Nell'esempio seguente viene eseguito il mapping di entrambe le proprietà del tipo di `Order` agli elementi Atom esistenti.</span><span class="sxs-lookup"><span data-stu-id="e7322-108">In the following example, both properties of the `Order` type are mapped to existing Atom elements.</span></span> <span data-ttu-id="e7322-109">Viene eseguito il mapping della proprietà `Product` del tipo di `Item` a un attributo di feed personalizzato in uno spazio dei nomi separato.</span><span class="sxs-lookup"><span data-stu-id="e7322-109">The `Product` property of the `Item` type is mapped to a custom feed attribute in a separate namespace.</span></span>  
  
 [!code-csharp[Astoria Custom Feeds#CustomIQueryableFeeds](../../../../samples/snippets/csharp/VS_Snippets_Misc/astoria custom feeds/cs/orderitems.svc.cs#customiqueryablefeeds)]
 [!code-vb[Astoria Custom Feeds#CustomIQueryableFeeds](../../../../samples/snippets/visualbasic/VS_Snippets_Misc/astoria custom feeds/vb/orderitems.svc.vb#customiqueryablefeeds)]  
  
## <a name="example"></a><span data-ttu-id="e7322-110">Esempio</span><span class="sxs-lookup"><span data-stu-id="e7322-110">Example</span></span>  
 <span data-ttu-id="e7322-111">Nell'esempio precedente per l'URI `http://myservice/OrderItems.svc/Orders(0)?$expand=Items` viene restituito il risultato seguente.</span><span class="sxs-lookup"><span data-stu-id="e7322-111">The previous example returns the following result for the URI `http://myservice/OrderItems.svc/Orders(0)?$expand=Items`.</span></span>  
  
 [!code-xml[Astoria Custom Feeds#IQueryableFeedResultInline](../../../../samples/snippets/xml/VS_Snippets_Misc/astoria custom feeds/xml/iqueryablefeedresultinline.xml#iqueryablefeedresultinline)]  
  
## <a name="see-also"></a><span data-ttu-id="e7322-112">Vedere anche</span><span class="sxs-lookup"><span data-stu-id="e7322-112">See Also</span></span>  
 [<span data-ttu-id="e7322-113">Provider di reflection</span><span class="sxs-lookup"><span data-stu-id="e7322-113">Reflection Provider</span></span>](../../../../docs/framework/data/wcf/reflection-provider-wcf-data-services.md)
