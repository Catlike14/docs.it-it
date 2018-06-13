---
title: Attributo &#39; &lt;attributename&gt; &#39; non può essere applicato più volte
ms.date: 07/20/2015
f1_keywords:
- bc30663
- vbc30663
helpviewer_keywords:
- BC30663
ms.assetid: 3760e7ff-7238-40a1-8676-77d858a64fc0
ms.openlocfilehash: df97a4e391406661db98eb1c958c0e12e45b6c49
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 05/04/2018
ms.locfileid: "33584859"
---
# <a name="attribute-39ltattributenamegt39-cannot-be-applied-multiple-times"></a><span data-ttu-id="8cc24-102">Attributo &#39; &lt;attributename&gt; &#39; non può essere applicato più volte</span><span class="sxs-lookup"><span data-stu-id="8cc24-102">Attribute &#39;&lt;attributename&gt;&#39; cannot be applied multiple times</span></span>
<span data-ttu-id="8cc24-103">L'attributo può essere applicato solo una volta.</span><span class="sxs-lookup"><span data-stu-id="8cc24-103">The attribute can only be applied once.</span></span> <span data-ttu-id="8cc24-104">Il `AttributeUsage` attributo determina se un attributo può essere applicato più volte.</span><span class="sxs-lookup"><span data-stu-id="8cc24-104">The `AttributeUsage` attribute determines whether an attribute can be applied more than once.</span></span>  
  
 <span data-ttu-id="8cc24-105">**ID errore:** BC30663</span><span class="sxs-lookup"><span data-stu-id="8cc24-105">**Error ID:** BC30663</span></span>  
  
## <a name="to-correct-this-error"></a><span data-ttu-id="8cc24-106">Per correggere l'errore</span><span class="sxs-lookup"><span data-stu-id="8cc24-106">To correct this error</span></span>  
  
1.  <span data-ttu-id="8cc24-107">Verificare che l'attributo viene applicato solo una volta.</span><span class="sxs-lookup"><span data-stu-id="8cc24-107">Make sure the attribute is only applied once.</span></span>  
  
2.  <span data-ttu-id="8cc24-108">Se si utilizza attributi personalizzati, è possibile modificare i relativi `AttributeUsage` attributo per consentire più utilizzo dell'attributo, come con l'esempio seguente.</span><span class="sxs-lookup"><span data-stu-id="8cc24-108">If you are using custom attributes you developed, consider changing their `AttributeUsage` attribute to allow multiple attribute usage, as with the following example.</span></span>  
  
```vb  
<AttributeUsage(AllowMultiple := True)>  
```  
  
## <a name="see-also"></a><span data-ttu-id="8cc24-109">Vedere anche</span><span class="sxs-lookup"><span data-stu-id="8cc24-109">See Also</span></span>  
 <xref:System.AttributeUsageAttribute>  
 [<span data-ttu-id="8cc24-110">Creazione di attributi personalizzati</span><span class="sxs-lookup"><span data-stu-id="8cc24-110">Creating Custom Attributes</span></span>](../../../visual-basic/programming-guide/concepts/attributes/creating-custom-attributes.md)  
 [<span data-ttu-id="8cc24-111">AttributeUsage</span><span class="sxs-lookup"><span data-stu-id="8cc24-111">AttributeUsage</span></span>](../../../visual-basic/programming-guide/concepts/attributes/attributeusage.md)
