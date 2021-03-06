---
title: '&lt;include&gt; (Guida per programmatori C#)'
ms.date: 07/20/2015
f1_keywords:
- include
- <include>
helpviewer_keywords:
- <include> C# XML tag
- include C# XML tag
ms.assetid: a8a70302-6196-4643-bd09-ef33f411f18f
ms.openlocfilehash: 854c8b61fa8164bccfc9451f2f163dab4a56388f
ms.sourcegitcommit: fb78d8abbdb87144a3872cf154930157090dd933
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 10/01/2018
ms.locfileid: "47192992"
---
# <a name="ltincludegt-c-programming-guide"></a>&lt;include&gt; (Guida per programmatori C#)
## <a name="syntax"></a>Sintassi  
  
```xml  
<include file='filename' path='tagpath[@name="id"]' />  
```  
  
#### <a name="parameters"></a>Parametri  
 `filename`  
 Nome del file XML che contiene la documentazione. Il nome file può essere qualificato con un percorso relativo al file del codice sorgente. Racchiudere `filename` tra virgolette singole (' ').  
  
 `tagpath`  
 Percorso dei tag di `filename` che porta al `name` del tag. Racchiudere il percorso tra virgolette singole (' ').  
  
 `name`  
 Identificatore del nome contenuto nel tag che precede i commenti. `name` ha sempre un `id`.  
  
 `id`  
 ID del tag che precede i commenti. Racchiudere l'ID tra virgolette doppie (" ").  
  
## <a name="remarks"></a>Note  
 Il tag \<include> consente di fare riferimento ai commenti di un altro file per la descrizione dei tipi e dei membri del codice sorgente, eliminando la necessità di inserire i commenti relativi alla documentazione direttamente nel file del codice sorgente. Inserendo la documentazione in un file separato, è possibile applicare alla documentazione il controllo del codice sorgente separatamente dal codice sorgente. Una persona, ad esempio, può avere il file di codice sorgente estratto e un'altra il file della documentazione estratto.  
  
 Il tag \<include> usa la sintassi XML XPath. Per informazioni sulla personalizzazione dell'utilizzo di \<include>, consultare la documentazione relativa a XPath.  
  
## <a name="example"></a>Esempio  
 In questo esempio vengono presi in considerazione più file. Di seguito è riportato il primo file, che usa \<include>:  
  
 [!code-csharp[csProgGuideDocComments#5](../../../csharp/programming-guide/xmldoc/codesnippet/CSharp/include_1.cs)]  
  
 Il secondo file, xml_include_tag.doc, contiene i commenti alla documentazione seguenti:  
  
```xml  
<MyDocs>  
  
<MyMembers name="test">  
<summary>  
The summary for this type.  
</summary>  
</MyMembers>  
  
<MyMembers name="test2">  
<summary>  
The summary for this other type.  
</summary>  
</MyMembers>  
  
</MyDocs>  
```  
  
## <a name="program-output"></a>Output di programma  
 L'output seguente viene generato quando si compilano le classi Test e Test2 con la riga di comando seguente: `/doc:DocFileName.xml.`. In Visual Studio, è possibile specificare l'opzione dei commenti XML alla documentazione nel riquadro Compilazione di Creazione progetti. Se il compilatore C# rileva il tag \<include>, la ricerca dei commenti alla documentazione verrà eseguita nel file xml_include_tag.doc anziché nel file di origine corrente. Il compilatore genera quindi il file DocFileName.xml, che verrà usato dagli strumenti della documentazione come [Sandcastle](https://github.com/EWSoftware/SHFB) per realizzare la documentazione finale.  
  
```xml  
<?xml version="1.0"?>   
<doc>   
    <assembly>   
        <name>xml_include_tag</name>   
    </assembly>   
    <members>   
        <member name="T:Test">   
            <summary>   
The summary for this type.   
</summary>   
        </member>   
        <member name="T:Test2">   
            <summary>   
The summary for this other type.   
</summary>   
        </member>   
    </members>   
</doc>   
```  
  
## <a name="see-also"></a>Vedere anche

- [Guida per programmatori C#](../../../csharp/programming-guide/index.md)  
- [Tag consigliati per i commenti relativi alla documentazione](../../../csharp/programming-guide/xmldoc/recommended-tags-for-documentation-comments.md)
