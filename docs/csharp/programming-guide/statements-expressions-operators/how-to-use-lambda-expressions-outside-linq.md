---
title: 'Procedura: utilizzare espressioni lambda al di fuori di LINQ (Guida per programmatori C#)'
ms.date: 07/20/2015
ms.prod: .net
ms.technology: devlang-csharp
ms.topic: article
helpviewer_keywords: lambda expressions [C#], outside LINQ
ms.assetid: 2b519274-6ee4-4455-ab2e-aed67dbfd07c
caps.latest.revision: "12"
author: BillWagner
ms.author: wiwagn
ms.openlocfilehash: c99f6bc7c9db1f0e2341c31ec5bf60217723d4e3
ms.sourcegitcommit: 4f3fef493080a43e70e951223894768d36ce430a
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 11/21/2017
---
# <a name="how-to-use-lambda-expressions-outside-linq-c-programming-guide"></a><span data-ttu-id="4696b-102">Procedura: utilizzare espressioni lambda al di fuori di LINQ (Guida per programmatori C#)</span><span class="sxs-lookup"><span data-stu-id="4696b-102">How to: Use Lambda Expressions Outside LINQ (C# Programming Guide)</span></span>
<span data-ttu-id="4696b-103">Le espressioni lambda non sono limitate alle query [!INCLUDE[vbteclinq](~/includes/vbteclinq-md.md)].</span><span class="sxs-lookup"><span data-stu-id="4696b-103">Lambda expressions are not limited to [!INCLUDE[vbteclinq](~/includes/vbteclinq-md.md)] queries.</span></span> <span data-ttu-id="4696b-104">È possibile usarle dove è previsto un valore delegate, ovvero dove può essere usato un metodo anonimo.</span><span class="sxs-lookup"><span data-stu-id="4696b-104">You can use them anywhere a delegate value is expected, that is, wherever an anonymous method can be used.</span></span> <span data-ttu-id="4696b-105">Nell'esempio seguente viene illustrato come usare un'espressione lambda in un gestore eventi Windows Forms.</span><span class="sxs-lookup"><span data-stu-id="4696b-105">The following example shows how to use a lambda expression in a Windows Forms event handler.</span></span> <span data-ttu-id="4696b-106">Si noti che i tipi degli input (<xref:System.Object> e <xref:System.Windows.Forms.MouseEventArgs>) vengono derivati tramite inferenza dal compilatore e non devono essere forniti in modo esplicito nei parametri di input dell'espressione lambda.</span><span class="sxs-lookup"><span data-stu-id="4696b-106">Notice that the types of the inputs (<xref:System.Object> and <xref:System.Windows.Forms.MouseEventArgs>) are inferred by the compiler and do not have to be explicitly given in the lambda input parameters.</span></span>  
  
## <a name="example"></a><span data-ttu-id="4696b-107">Esempio</span><span class="sxs-lookup"><span data-stu-id="4696b-107">Example</span></span>  
  
```  
public partial class Form1 : Form  
{  
    public Form1()  
    {  
        InitializeComponent();  
        // Use a lambda expression to define an event handler.  
       this.Click += (s, e) => { MessageBox.Show(((MouseEventArgs)e).Location.ToString());};  
    }  
}  
```  
  
## <a name="see-also"></a><span data-ttu-id="4696b-108">Vedere anche</span><span class="sxs-lookup"><span data-stu-id="4696b-108">See Also</span></span>  
 [<span data-ttu-id="4696b-109">Espressioni lambda</span><span class="sxs-lookup"><span data-stu-id="4696b-109">Lambda Expressions</span></span>](../../../csharp/programming-guide/statements-expressions-operators/lambda-expressions.md)  
 [<span data-ttu-id="4696b-110">Metodi anonimi</span><span class="sxs-lookup"><span data-stu-id="4696b-110">Anonymous Methods</span></span>](../../../csharp/programming-guide/statements-expressions-operators/anonymous-methods.md)  
 [<span data-ttu-id="4696b-111">LINQ (Language-Integrated Query)</span><span class="sxs-lookup"><span data-stu-id="4696b-111">LINQ (Language-Integrated Query)</span></span>](http://msdn.microsoft.com/library/a73c4aec-5d15-4e98-b962-1274021ea93d)
