---
title: 'Procedura: utilizzare EdmGen.exe per generare codice a livello oggetti'
ms.date: 03/30/2017
ms.assetid: c44d2ebe-f66f-42cb-9741-4a3f0c2dcffb
ms.openlocfilehash: c15ceec66ad5b1c9ef414c3e57e3b6e49c372e7a
ms.sourcegitcommit: 6eac9a01ff5d70c6d18460324c016a3612c5e268
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/14/2018
ms.locfileid: "45593712"
---
# <a name="how-to-use-edmgenexe-to-generate-object-layer-code"></a>Procedura: utilizzare EdmGen.exe per generare codice a livello oggetti
Questo argomento viene illustrato come usare il [generatore EDM (EdmGen.exe)](../../../../../docs/framework/data/adonet/ef/edm-generator-edmgen-exe.md) strumento per generare codice del livello oggetti in base al file CSDL.  
  
### <a name="to-generate-object-layer-code-for-the-school-model-for-a-visual-basic-project-using-edmgenexe"></a>Per generare il codice del livello oggetti per il modello School per un progetto di Visual Basic usando EdmGen.exe  
  
1.  Creare il database School. Per altre informazioni, vedere [creazione del Database di esempio School](https://msdn.microsoft.com/library/c1bec483-a0ea-4660-aa0b-7b0a8b68fed0).  
  
2.  Generare il modello School o ottenere il file School.csdl. Per altre informazioni, vedere [procedura: usare EdmGen.exe per generare il file di modello e di Mapping](../../../../../docs/framework/data/adonet/ef/how-to-use-edmgen-exe-to-generate-the-model-and-mapping-files.md).  
  
3.  Al prompt dei comandi eseguire il comando seguente senza interruzioni di riga:  
  
    ```  
    "%windir%\Microsoft.NET\Framework\v4.0.30319\edmgen.exe" /mode:EntityClassGeneration   
    /incsdl:.\School.csdl /outobjectlayer:.\School.Objects.vb /language:VB  
    ```  
  
### <a name="to-generate-object-layer-code-for-the-school-model-for-a-c-project-using-edmgenexe"></a>Per generare il codice del livello oggetti per il modello School per un progetto di C# usando EdmGen.exe  
  
1.  Creare il database School. Per altre informazioni, vedere [creazione del Database di esempio School](https://msdn.microsoft.com/library/c1bec483-a0ea-4660-aa0b-7b0a8b68fed0).  
  
2.  Generare il modello School o ottenere il file School.csdl. Per altre informazioni, vedere [procedura: usare EdmGen.exe per generare il file di modello e di Mapping](../../../../../docs/framework/data/adonet/ef/how-to-use-edmgen-exe-to-generate-the-model-and-mapping-files.md).  
  
3.  Al prompt dei comandi eseguire il comando seguente senza interruzioni di riga:  
  
    ```  
    "%windir%\Microsoft.NET\Framework\v4.0.30319\edmgen.exe" /mode:EntityClassGeneration   
    /incsdl:.\School.csdl /outobjectlayer:.\School.Objects.cs /language:CSharp  
    ```  
  
## <a name="see-also"></a>Vedere anche  
 [Modellazione e mapping](../../../../../docs/framework/data/adonet/ef/modeling-and-mapping.md)  
 [Procedura: configurare manualmente un progetto Entity Framework](https://msdn.microsoft.com/library/73f6ae1d-b3b2-4577-aebd-ad5a75954e9e)  
 [Strumenti di ADO.NET Entity Data Model](https://msdn.microsoft.com/library/91076853-0881-421b-837a-f582f36be527)  
 [Procedura: pre-generare viste per migliorare le prestazioni delle Query](https://msdn.microsoft.com/library/b18a9d16-e10b-4043-ba91-b632f85a2579)  
 [Procedura: Usare EdmGen.exe per generare i file di modello e di mapping](../../../../../docs/framework/data/adonet/ef/how-to-use-edmgen-exe-to-generate-the-model-and-mapping-files.md)
