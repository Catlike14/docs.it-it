---
title: internal (Riferimenti per C#)
ms.date: 2015-07-20
ms.prod: .net
ms.technology:
- devlang-csharp
ms.topic: article
f1_keywords:
- internal_CSharpKeyword
- internal
dev_langs:
- CSharp
helpviewer_keywords:
- internal keyword [C#]
ms.assetid: 6ee0785c-d7c8-49b8-bb72-0a4dfbcb6461
caps.latest.revision: 23
author: BillWagner
ms.author: wiwagn
translation.priority.ht:
- cs-cz
- de-de
- es-es
- fr-fr
- it-it
- ja-jp
- ko-kr
- pl-pl
- pt-br
- ru-ru
- tr-tr
- zh-cn
- zh-tw
ms.translationtype: HT
ms.sourcegitcommit: 306c608dc7f97594ef6f72ae0f5aaba596c936e1
ms.openlocfilehash: 5674a78e2c317357c31d9e2661a25ce86cbf4f6a
ms.contentlocale: it-it
ms.lasthandoff: 07/28/2017

---
# <a name="internal-c-reference"></a><span data-ttu-id="bf3ee-102">internal (Riferimenti per C#)</span><span class="sxs-lookup"><span data-stu-id="bf3ee-102">internal (C# Reference)</span></span>
<span data-ttu-id="bf3ee-103">La parola chiave `internal` è un [modificatore di accesso](../../../csharp/language-reference/keywords/access-modifiers.md) per tipi e membri dei tipi.</span><span class="sxs-lookup"><span data-stu-id="bf3ee-103">The `internal` keyword is an [access modifier](../../../csharp/language-reference/keywords/access-modifiers.md) for types and type members.</span></span> <span data-ttu-id="bf3ee-104">I tipi o membri interni sono accessibili solo all'interno di file nello stesso assembly, come nell'esempio seguente:</span><span class="sxs-lookup"><span data-stu-id="bf3ee-104">Internal types or members are accessible only within files in the same assembly, as in this example:</span></span>  
  
```  
public class BaseClass   
{  
    // Only accessible within the same assembly  
    internal static int x = 0;  
}  
```  
  
 <span data-ttu-id="bf3ee-105">I tipi o membri con modificatore di accesso `protected internal` sono accessibili dall'assembly corrente o dai tipi che derivano dalla classe che li contiene.</span><span class="sxs-lookup"><span data-stu-id="bf3ee-105">Types or members that have access modifier `protected internal` can be accessed from the current assembly or from types that are derived from the containing class.</span></span>  
  
 <span data-ttu-id="bf3ee-106">Per un confronto di `internal` con altri modificatori di accesso, vedere [Livelli di accessibilità](../../../csharp/language-reference/keywords/accessibility-levels.md) e [Modificatori di accesso](../../../csharp/programming-guide/classes-and-structs/access-modifiers.md).</span><span class="sxs-lookup"><span data-stu-id="bf3ee-106">For a comparison of `internal` with the other access modifiers, see [Accessibility Levels](../../../csharp/language-reference/keywords/accessibility-levels.md) and [Access Modifiers](../../../csharp/programming-guide/classes-and-structs/access-modifiers.md).</span></span>  
  
 <span data-ttu-id="bf3ee-107">Per altre informazioni sugli assembly, vedere [Assembly e Global Assembly Cache](../../../csharp/programming-guide/concepts/assemblies-gac/index.md).</span><span class="sxs-lookup"><span data-stu-id="bf3ee-107">For more information about assemblies, see [Assemblies and the Global Assembly Cache](../../../csharp/programming-guide/concepts/assemblies-gac/index.md).</span></span>  
  
 <span data-ttu-id="bf3ee-108">Un uso comune dell'accesso interno è in fase di sviluppo basato su componenti poiché consente a un gruppo di componenti di collaborare in modo privato senza essere esposti al resto del codice dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="bf3ee-108">A common use of internal access is in component-based development because it enables a group of components to cooperate in a private manner without being exposed to the rest of the application code.</span></span> <span data-ttu-id="bf3ee-109">Ad esempio, un framework per la creazione di interfacce utente grafiche potrebbe indicare le classi `Control` e `Form` che interagiscono usando membri con accesso interno.</span><span class="sxs-lookup"><span data-stu-id="bf3ee-109">For example, a framework for building graphical user interfaces could provide `Control` and `Form` classes that cooperate by using members with internal access.</span></span> <span data-ttu-id="bf3ee-110">Poiché questi membri sono interni, non sono esposti al codice che usa il framework.</span><span class="sxs-lookup"><span data-stu-id="bf3ee-110">Since these members are internal, they are not exposed to code that is using the framework.</span></span>  
  
 <span data-ttu-id="bf3ee-111">Non è corretto fare riferimento a un tipo o a un membro con accesso interno all'esterno dell'assembly in cui è stato definito.</span><span class="sxs-lookup"><span data-stu-id="bf3ee-111">It is an error to reference a type or a member with internal access outside the assembly within which it was defined.</span></span>  
  
## <a name="example"></a><span data-ttu-id="bf3ee-112">Esempio</span><span class="sxs-lookup"><span data-stu-id="bf3ee-112">Example</span></span>  
 <span data-ttu-id="bf3ee-113">Questo esempio contiene due file, `Assembly1.cs` e `Assembly1_a.cs`.</span><span class="sxs-lookup"><span data-stu-id="bf3ee-113">This example contains two files, `Assembly1.cs` and `Assembly1_a.cs`.</span></span> <span data-ttu-id="bf3ee-114">Il primo file contiene una classe di base interna, `BaseClass`.</span><span class="sxs-lookup"><span data-stu-id="bf3ee-114">The first file contains an internal base class, `BaseClass`.</span></span> <span data-ttu-id="bf3ee-115">Nel secondo file, un tentativo di creare un'istanza di `BaseClass` genererà un errore.</span><span class="sxs-lookup"><span data-stu-id="bf3ee-115">In the second file, an attempt to instantiate `BaseClass` will produce an error.</span></span>  
  
```  
// Assembly1.cs  
// Compile with: /target:library  
internal class BaseClass   
{  
   public static int intM = 0;  
}  
```  
  
```  
// Assembly1_a.cs  
// Compile with: /reference:Assembly1.dll  
class TestAccess   
{  
   static void Main()   
   {  
      BaseClass myBase = new BaseClass();   // CS0122  
   }  
}  
```  
  
## <a name="example"></a><span data-ttu-id="bf3ee-116">Esempio</span><span class="sxs-lookup"><span data-stu-id="bf3ee-116">Example</span></span>  
 <span data-ttu-id="bf3ee-117">In questo esempio, usare gli stessi file dell'esempio 1 e modificare il livello di accessibilità di `BaseClass` in `public`.</span><span class="sxs-lookup"><span data-stu-id="bf3ee-117">In this example, use the same files you used in example 1, and change the accessibility level of `BaseClass` to `public`.</span></span> <span data-ttu-id="bf3ee-118">Modificare anche il livello di accessibilità del membro `IntM` in `internal`.</span><span class="sxs-lookup"><span data-stu-id="bf3ee-118">Also change the accessibility level of the member `IntM` to `internal`.</span></span> <span data-ttu-id="bf3ee-119">In questo caso, è possibile creare un'istanza della classe, ma non è possibile accedere al membro interno.</span><span class="sxs-lookup"><span data-stu-id="bf3ee-119">In this case, you can instantiate the class, but you cannot access the internal member.</span></span>  
  
```  
// Assembly2.cs  
// Compile with: /target:library  
public class BaseClass   
{  
   internal static int intM = 0;  
}  
```  
  
```  
// Assembly2_a.cs  
// Compile with: /reference:Assembly1.dll  
public class TestAccess   
{  
   static void Main()   
   {  
      BaseClass myBase = new BaseClass();   // Ok.  
      BaseClass.intM = 444;    // CS0117  
   }  
}  
```  
  
## <a name="c-language-specification"></a><span data-ttu-id="bf3ee-120">Specifiche del linguaggio C#</span><span class="sxs-lookup"><span data-stu-id="bf3ee-120">C# Language Specification</span></span>  
 [!INCLUDE[CSharplangspec](~/includes/csharplangspec-md.md)]  
  
## <a name="see-also"></a><span data-ttu-id="bf3ee-121">Vedere anche</span><span class="sxs-lookup"><span data-stu-id="bf3ee-121">See Also</span></span>  
 <span data-ttu-id="bf3ee-122">[Riferimenti per C#](../../../csharp/language-reference/index.md) </span><span class="sxs-lookup"><span data-stu-id="bf3ee-122">[C# Reference](../../../csharp/language-reference/index.md) </span></span>  
 <span data-ttu-id="bf3ee-123">[Guida per programmatori C#](../../../csharp/programming-guide/index.md) </span><span class="sxs-lookup"><span data-stu-id="bf3ee-123">[C# Programming Guide](../../../csharp/programming-guide/index.md) </span></span>  
 <span data-ttu-id="bf3ee-124">[Parole chiave di C#](../../../csharp/language-reference/keywords/index.md) </span><span class="sxs-lookup"><span data-stu-id="bf3ee-124">[C# Keywords](../../../csharp/language-reference/keywords/index.md) </span></span>  
 <span data-ttu-id="bf3ee-125">[Modificatori di accesso](../../../csharp/language-reference/keywords/access-modifiers.md) </span><span class="sxs-lookup"><span data-stu-id="bf3ee-125">[Access Modifiers](../../../csharp/language-reference/keywords/access-modifiers.md) </span></span>  
 <span data-ttu-id="bf3ee-126">[Livelli di accessibilità](../../../csharp/language-reference/keywords/accessibility-levels.md) </span><span class="sxs-lookup"><span data-stu-id="bf3ee-126">[Accessibility Levels](../../../csharp/language-reference/keywords/accessibility-levels.md) </span></span>  
 <span data-ttu-id="bf3ee-127">[Modificatori](../../../csharp/language-reference/keywords/modifiers.md) </span><span class="sxs-lookup"><span data-stu-id="bf3ee-127">[Modifiers](../../../csharp/language-reference/keywords/modifiers.md) </span></span>  
 <span data-ttu-id="bf3ee-128">[public](../../../csharp/language-reference/keywords/public.md) </span><span class="sxs-lookup"><span data-stu-id="bf3ee-128">[public](../../../csharp/language-reference/keywords/public.md) </span></span>  
 <span data-ttu-id="bf3ee-129">[private](../../../csharp/language-reference/keywords/private.md) </span><span class="sxs-lookup"><span data-stu-id="bf3ee-129">[private](../../../csharp/language-reference/keywords/private.md) </span></span>  
 [<span data-ttu-id="bf3ee-130">protected</span><span class="sxs-lookup"><span data-stu-id="bf3ee-130">protected</span></span>](../../../csharp/language-reference/keywords/protected.md)

