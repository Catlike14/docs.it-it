---
title: 'Procedura: utilizzare un Pool di Thread (Visual Basic)'
ms.date: 07/20/2015
ms.assetid: 90a0bb24-39f8-41f5-a217-b52a7d4fed0b
ms.openlocfilehash: a61defc2e40662d7fdadb40693e757fa559adb6a
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 05/04/2018
---
# <a name="how-to-use-a-thread-pool-visual-basic"></a>Procedura: utilizzare un Pool di Thread (Visual Basic)
La *creazione di un pool di thread* è una forma di multithreading che prevede l'aggiunta di attività a una coda e l'avvio automatico di tali attività nel corso della creazione dei thread. Per ulteriori informazioni, vedere [(Visual Basic) il pool di Thread](../../../../visual-basic/programming-guide/concepts/threading/thread-pooling.md).  
  
 Nell'esempio seguente viene usato il pool di thread di .NET Framework per calcolare il risultato della sequenza di `Fibonacci` relativa a 10 numeri compresi tra 20 e 40. Ogni risultato di `Fibonacci` viene rappresentato dalla classe `Fibonacci`, che fornisce un metodo denominato `ThreadPoolCallback` per l'esecuzione del calcolo. Viene creato un oggetto che rappresenta ogni valore `Fibonacci`, il metodo `ThreadPoolCallback` viene passato a <xref:System.Threading.ThreadPool.QueueUserWorkItem%2A>, che assegna un thread disponibile del pool per eseguire il metodo.  
  
 Poiché a ogni oggetto `Fibonacci` viene assegnato un valore semi-casuale da calcolare e poiché ogni thread è in competizione con gli altri per ottenere il tempo del processore, non è possibile prevedere quanto tempo richiederà il calcolo di tutti e 10 i risultati. Per questo motivo a ogni oggetto `Fibonacci` viene passata un'istanza della classe <xref:System.Threading.ManualResetEvent> durante la costruzione. Dopo aver completato il calcolo, ogni oggetto segnala l'oggetto evento specificato. In questo modo il thread primario può bloccare l'esecuzione con `Fibonacci` finché tutti e dieci gli oggetti <xref:System.Threading.WaitHandle.WaitAll%2A> non hanno calcolato un risultato. Il metodo `Main` visualizza quindi ogni risultato `Fibonacci`.  
  
## <a name="example"></a>Esempio  
  
```vb  
Imports System.Threading  
  
Module Module1  
  
    Public Class Fibonacci  
        Private _n As Integer  
        Private _fibOfN  
        Private _doneEvent As ManualResetEvent  
  
        Public ReadOnly Property N() As Integer  
            Get  
                Return _n  
            End Get  
        End Property  
  
        Public ReadOnly Property FibOfN() As Integer  
            Get  
                Return _fibOfN  
            End Get  
        End Property  
  
        Sub New(ByVal n As Integer, ByVal doneEvent As ManualResetEvent)  
            _n = n  
            _doneEvent = doneEvent  
        End Sub  
  
        ' Wrapper method for use with the thread pool.  
        Public Sub ThreadPoolCallBack(ByVal threadContext As Object)  
            Dim threadIndex As Integer = CType(threadContext, Integer)  
            Console.WriteLine("thread {0} started...", threadIndex)  
            _fibOfN = Calculate(_n)  
            Console.WriteLine("thread {0} result calculated...", threadIndex)  
            _doneEvent.Set()  
        End Sub  
  
        Public Function Calculate(ByVal n As Integer) As Integer  
            If n <= 1 Then  
                Return n  
            End If  
            Return Calculate(n - 1) + Calculate(n - 2)  
        End Function  
  
    End Class  
  
    <MTAThread()>   
    Sub Main()  
        Const FibonacciCalculations As Integer = 9 ' 0 to 9  
  
        ' One event is used for each Fibonacci object  
        Dim doneEvents(FibonacciCalculations) As ManualResetEvent  
        Dim fibArray(FibonacciCalculations) As Fibonacci  
        Dim r As New Random()  
  
        ' Configure and start threads using ThreadPool.  
        Console.WriteLine("launching {0} tasks...", FibonacciCalculations)  
  
        For i As Integer = 0 To FibonacciCalculations  
            doneEvents(i) = New ManualResetEvent(False)  
            Dim f = New Fibonacci(r.Next(20, 40), doneEvents(i))  
            fibArray(i) = f  
            ThreadPool.QueueUserWorkItem(AddressOf f.ThreadPoolCallBack, i)  
        Next  
  
        ' Wait for all threads in pool to calculate.  
        WaitHandle.WaitAll(doneEvents)  
        Console.WriteLine("All calculations are complete.")  
  
        ' Display the results.  
        For i As Integer = 0 To FibonacciCalculations  
            Dim f As Fibonacci = fibArray(i)  
            Console.WriteLine("Fibonacci({0}) = {1}", f.N, f.FibOfN)  
        Next  
    End Sub  
  
End Module  
```  
  
 Di seguito viene riportato un esempio dell'output.  
  
```  
launching 10 tasks...  
thread 0 started...  
thread 1 started...  
thread 1 result calculated...  
thread 2 started...  
thread 2 result calculated...  
thread 3 started...  
thread 3 result calculated...  
thread 4 started...  
thread 0 result calculated...  
thread 5 started...  
thread 5 result calculated...  
thread 6 started...  
thread 4 result calculated...  
thread 7 started...  
thread 6 result calculated...  
thread 8 started...  
thread 8 result calculated...  
thread 9 started...  
thread 9 result calculated...  
thread 7 result calculated...  
All calculations are complete.  
Fibonacci(38) = 39088169  
Fibonacci(29) = 514229  
Fibonacci(25) = 75025  
Fibonacci(22) = 17711  
Fibonacci(38) = 39088169  
Fibonacci(29) = 514229  
Fibonacci(29) = 514229  
Fibonacci(38) = 39088169  
Fibonacci(21) = 10946  
Fibonacci(27) = 196418  
```  
  
## <a name="see-also"></a>Vedere anche  
 <xref:System.Threading.Mutex>  
 <xref:System.Threading.WaitHandle.WaitAll%2A>  
 <xref:System.Threading.ManualResetEvent>  
 <xref:System.Threading.EventWaitHandle.Set%2A>  
 <xref:System.Threading.ThreadPool>  
 <xref:System.Threading.ThreadPool.QueueUserWorkItem%2A>  
 <xref:System.Threading.ManualResetEvent>  
 <xref:System.Threading.Monitor>  
 [Creazione di pool di thread (Visual Basic)](../../../../visual-basic/programming-guide/concepts/threading/thread-pooling.md)  
 [Threading (Visual Basic)](../../../../visual-basic/programming-guide/concepts/threading/index.md)  
 [Sicurezza](../../../../standard/security/index.md)
