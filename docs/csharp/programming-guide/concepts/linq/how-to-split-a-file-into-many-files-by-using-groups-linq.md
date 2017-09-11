---
title: 'Procedura: Suddividere un file in molti file usando i gruppi (LINQ) (C#)'
ms.custom: 
ms.date: 2015-07-20
ms.prod: .net
ms.reviewer: 
ms.suite: 
ms.technology:
- devlang-csharp
ms.topic: article
dev_langs:
- CSharp
ms.assetid: 8179b91c-d778-4e57-884f-77fe5a8e4e40
caps.latest.revision: 3
author: BillWagner
ms.author: wiwagn
translation.priority.mt:
- cs-cz
- pl-pl
- pt-br
- tr-tr
ms.translationtype: HT
ms.sourcegitcommit: 306c608dc7f97594ef6f72ae0f5aaba596c936e1
ms.openlocfilehash: f49cd82b0e6fecc2e4459dbe31656db0aa5f42ee
ms.contentlocale: it-it
ms.lasthandoff: 07/28/2017

---
# <a name="how-to-split-a-file-into-many-files-by-using-groups-linq-c"></a><span data-ttu-id="9427c-102">Procedura: Suddividere un file in molti file usando i gruppi (LINQ) (C#)</span><span class="sxs-lookup"><span data-stu-id="9427c-102">How to: Split a File Into Many Files by Using Groups (LINQ) (C#)</span></span>
<span data-ttu-id="9427c-103">Questo esempio illustra un modo per unire il contenuto di due file e creare quindi un set di nuovi file in cui i dati sono organizzati in modo diverso.</span><span class="sxs-lookup"><span data-stu-id="9427c-103">This example shows one way to merge the contents of two files and then create a set of new files that organize the data in a new way.</span></span>  
  
### <a name="to-create-the-data-files"></a><span data-ttu-id="9427c-104">Per creare i file di dati</span><span class="sxs-lookup"><span data-stu-id="9427c-104">To create the data files</span></span>  
  
1.  <span data-ttu-id="9427c-105">Copiare i nomi seguenti in un file di testo denominato names1.txt e salvarlo nella cartella del progetto:</span><span class="sxs-lookup"><span data-stu-id="9427c-105">Copy these names into a text file that is named names1.txt and save it in your project folder:</span></span>  
  
    ```  
    Bankov, Peter  
    Holm, Michael  
    Garcia, Hugo  
    Potra, Cristina  
    Noriega, Fabricio  
    Aw, Kam Foo  
    Beebe, Ann  
    Toyoshima, Tim  
    Guy, Wey Yuan  
    Garcia, Debra  
    ```  
  
2.  <span data-ttu-id="9427c-106">Copiare i nomi seguenti in un file di testo denominato names2.txt e salvarlo nella cartella del progetto. Si noti che i due file hanno alcuni nomi in comune.</span><span class="sxs-lookup"><span data-stu-id="9427c-106">Copy these names into a text file that is named names2.txt and save it in your project folder: Note that the two files have some names in common.</span></span>  
  
    ```  
    Liu, Jinghao  
    Bankov, Peter  
    Holm, Michael  
    Garcia, Hugo  
    Beebe, Ann  
    Gilchrist, Beth  
    Myrcha, Jacek  
    Giakoumakis, Leo  
    McLin, Nkenge  
    El Yassir, Mehdi  
    ```  
  
## <a name="example"></a><span data-ttu-id="9427c-107">Esempio</span><span class="sxs-lookup"><span data-stu-id="9427c-107">Example</span></span>  
  
```csharp  
class SplitWithGroups  
{  
    static void Main()  
    {  
        string[] fileA = System.IO.File.ReadAllLines(@"../../../names1.txt");  
        string[] fileB = System.IO.File.ReadAllLines(@"../../../names2.txt");  
  
        // Concatenate and remove duplicate names based on  
        // default string comparer  
        var mergeQuery = fileA.Union(fileB);  
  
        // Group the names by the first letter in the last name.  
        var groupQuery = from name in mergeQuery  
                         let n = name.Split(',')  
                         group name by n[0][0] into g  
                         orderby g.Key  
                         select g;  
  
        // Create a new file for each group that was created  
        // Note that nested foreach loops are required to access  
        // individual items with each group.  
        foreach (var g in groupQuery)  
        {  
            // Create the new file name.  
            string fileName = @"../../../testFile_" + g.Key + ".txt";  
  
            // Output to display.  
            Console.WriteLine(g.Key);  
  
            // Write file.  
            using (System.IO.StreamWriter sw = new System.IO.StreamWriter(fileName))  
            {  
                foreach (var item in g)  
                {  
                    sw.WriteLine(item);  
                    // Output to console for example purposes.  
                    Console.WriteLine("   {0}", item);  
                }  
            }  
        }  
        // Keep console window open in debug mode.  
        Console.WriteLine("Files have been written. Press any key to exit");  
        Console.ReadKey();  
    }  
}  
/* Output:   
    A  
       Aw, Kam Foo  
    B  
       Bankov, Peter  
       Beebe, Ann  
    E  
       El Yassir, Mehdi  
    G  
       Garcia, Hugo  
       Guy, Wey Yuan  
       Garcia, Debra  
       Gilchrist, Beth  
       Giakoumakis, Leo  
    H  
       Holm, Michael  
    L  
       Liu, Jinghao  
    M  
       Myrcha, Jacek  
       McLin, Nkenge  
    N  
       Noriega, Fabricio  
    P  
       Potra, Cristina  
    T  
       Toyoshima, Tim  
 */  
```  
  
 <span data-ttu-id="9427c-108">Il programma scrive un file separato per ogni gruppo nella stessa cartella dei file di dati.</span><span class="sxs-lookup"><span data-stu-id="9427c-108">The program writes a separate file for each group in the same folder as the data files.</span></span>  
  
## <a name="compiling-the-code"></a><span data-ttu-id="9427c-109">Compilazione del codice</span><span class="sxs-lookup"><span data-stu-id="9427c-109">Compiling the Code</span></span>  
 <span data-ttu-id="9427c-110">Creare un progetto che usi .NET Framework versione 3.5 o successiva con un riferimento a System.Core.dll e alle direttive `using` per gli spazi dei nomi System.Linq e System.IO.</span><span class="sxs-lookup"><span data-stu-id="9427c-110">Create a project that targets the .NET Framework  version 3.5 or higher, with a reference to System.Core.dll and `using` directives for the System.Linq and System.IO namespaces.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="9427c-111">Vedere anche</span><span class="sxs-lookup"><span data-stu-id="9427c-111">See Also</span></span>  
 <span data-ttu-id="9427c-112">[LINQ e stringhe (C#)](../../../../csharp/programming-guide/concepts/linq/linq-and-strings.md) </span><span class="sxs-lookup"><span data-stu-id="9427c-112">[LINQ and Strings (C#)](../../../../csharp/programming-guide/concepts/linq/linq-and-strings.md) </span></span>  
 [<span data-ttu-id="9427c-113">Directory di file e LINQ (C#)</span><span class="sxs-lookup"><span data-stu-id="9427c-113">LINQ and File Directories (C#)</span></span>](../../../../csharp/programming-guide/concepts/linq/linq-and-file-directories.md)

