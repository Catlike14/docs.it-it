---
title: Oggetto My.Response
ms.date: 07/20/2015
f1_keywords:
- My.MyWebExtension.Response
- My.Response
helpviewer_keywords:
- My.Response object
ms.assetid: 626359bc-3165-40b4-bfaf-2c610e26eb5b
ms.openlocfilehash: 0a907d74112586e7b88c5a0a6f40080455454d7f
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 05/04/2018
---
# <a name="myresponse-object"></a>Oggetto My.Response
Ottiene il <xref:System.Web.HttpResponse> oggetto associato di <xref:System.Web.UI.Page>. Questo oggetto consente di inviare dati di risposta HTTP a un client e contiene informazioni su tale risposta.  
  
## <a name="remarks"></a>Note  
 Il `My.Response` oggetto contiene l'oggetto corrente <xref:System.Web.HttpResponse> oggetto associato alla pagina.  
  
 Il `My.Response` oggetto è disponibile solo per [!INCLUDE[vstecasp](~/includes/vstecasp-md.md)] applicazioni.  
  
## <a name="example"></a>Esempio  
 Nell'esempio seguente ottiene la raccolta di intestazione dal `My.Request` oggetto e viene utilizzato il `My.Response` oggetto da scrivere la pagina ASP.NET.  
  
 [!code-vb[VbVbalrMyWeb#1](../../../visual-basic/language-reference/objects/codesnippet/VisualBasic/my-response-object_1.aspx)]  
  
## <a name="see-also"></a>Vedere anche  
 <xref:System.Web.HttpResponse>  
 [Oggetto My.Request](../../../visual-basic/language-reference/objects/my-request-object.md)
