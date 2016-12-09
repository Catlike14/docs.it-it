---
title: 'Procedura: Eseguire modifiche di base delle stringhe'
description: 'Procedura: Eseguire modifiche di base delle stringhe'
keywords: .NET, .NET Core
author: stevehoag
ms.date: 07/26/2016
ms.topic: article
ms.prod: .net
ms.technology: dotnet-standard
ms.devlang: dotnet
ms.assetid: 141d5c94-08db-469c-8a33-708c0d3bba42
translationtype: Human Translation
ms.sourcegitcommit: fb00da6505c9edb6a49d2003ae9bcb8e74c11d6c
ms.openlocfilehash: c73aaf1c389ef745ad35987a98242cc75f581e4f

---

# <a name="how-to-perform-basic-string-manipulations"></a>Procedura: Eseguire modifiche di base delle stringhe

Nell'esempio seguente vengono usati alcuni dei metodi descritti nell'argomento [Operazioni di base su stringhe](basic-string-operations.md) per costruire una classe con la quale modificare le stringhe, come può avvenire in un'applicazione reale. Nella classe `MailToData` vengono archiviati il nome e l'indirizzo di un utente in proprietà separate e viene usato un modo per combinare i campi `City`, `State` e `Zip` in una singola stringa da visualizzare all'utente. Questa classe consente anche all'utente di immettere la città, lo stato e il codice postale ZIP (Stati Uniti) sotto forma di singola stringa. L'applicazione automaticamente analizza la singola stringa e immette le informazioni corrette nella proprietà corrispondente.

Per semplicità, in questo esempio viene usata un'applicazione console con un'interfaccia della riga di comando.

## <a name="example"></a>Esempio

```csharp
using System;

class MainClass
{
   static void Main()
   {
      MailToData MyData = new MailToData();

      Console.Write("Enter Your Name: ");
      MyData.Name = Console.ReadLine();
      Console.Write("Enter Your Address: ");
      MyData.Address = Console.ReadLine();
      Console.Write("Enter Your City, State, and ZIP Code separated by spaces: ");
      MyData.CityStateZip = Console.ReadLine();
      Console.WriteLine();

      if (MyData.Validated) {
         Console.WriteLine("Name: {0}", MyData.Name);
         Console.WriteLine("Address: {0}", MyData.Address);
         Console.WriteLine("City: {0}", MyData.City);
         Console.WriteLine("State: {0}", MyData.State);
         Console.WriteLine("Zip: {0}", MyData.Zip);

         Console.WriteLine("\nThe following address will be used:");
         Console.WriteLine(MyData.Address);
         Console.WriteLine(MyData.CityStateZip);
      }
   }
}

public class MailToData
{
   string name = "";
   string address = ""; 
   string citystatezip = "";
   string city = ""; 
   string state = ""; 
   string zip = "";
   bool parseSucceeded = false;

   public string Name
   {
      get{return name;}
      set{name = value;}
   }

   public string Address
   {
      get{return address;}
      set{address = value;}
   }

   public string CityStateZip
   {
      get { 
         return String.Format("{0}, {1} {2}", city, state, zip); 
      }
      set {
         citystatezip = value.Trim();
         ParseCityStateZip();
      }
   }

   public string City
   {
      get{return city;}
      set{city = value;}
   }

   public string State
   {
      get{return state;}
      set{state = value;}
   }

   public string Zip
   {
      get{return zip;}
      set{zip = value;}
   }

   public bool Validated
   {
      get { return parseSucceeded; }
   }

   private void ParseCityStateZip()
   {  
      string msg = "";
      const string msgEnd = "\nYou must enter spaces between city, state, and zip code.\n";

      // Throw a FormatException if the user did not enter the necessary spaces
      // between elements. 
      try
      {
         // City may consist of multiple words, so we'll have to parse the 
         // string from right to left starting with the zip code.
         int zipIndex = citystatezip.LastIndexOf(" ");
         if (zipIndex == -1) { 
            msg = "\nCannot identify a zip code." + msgEnd;
            throw new FormatException(msg);
         }
         zip = citystatezip.Substring(zipIndex + 1);        

         int stateIndex = citystatezip.LastIndexOf(" ", zipIndex - 1);
         if (stateIndex == -1) {  
            msg = "\nCannot identify a state." + msgEnd;
            throw new FormatException(msg);
         }
         state = citystatezip.Substring(stateIndex + 1, zipIndex - stateIndex - 1);        
         state = state.ToUpper();

         city = citystatezip.Substring(0, stateIndex);
         if (city.Length == 0) {
            msg = "\nCannot identify a city." + msgEnd;
            throw new FormatException(msg);
         }
         parseSucceeded = true;
      }
      catch (FormatException ex)
      {
         Console.WriteLine(ex.Message);
      } 
   }

   private string ReturnCityStateZip()
    {
        // Make state uppercase.
        state = state.ToUpper();

        // Put the value of city, state, and zip together in the proper manner.
        string MyCityStateZip = String.Concat(city, ", ", state, " ", zip);

        return MyCityStateZip;
    }
}
```

```vb
Class MainClass
   Public Shared Sub Main()
      Dim MyData As New MailToData()

      Console.Write("Enter Your Name: ")
      MyData.Name = Console.ReadLine()
      Console.Write("Enter Your Address: ")
      MyData.Address = Console.ReadLine()
      Console.Write("Enter Your City, State, and ZIP Code separated by spaces: ")
      MyData.CityStateZip = Console.ReadLine()
      Console.WriteLine()

      If MyData.Validated Then
         Console.WriteLine("Name: {0}", MyData.Name)
         Console.WriteLine("Address: {0}", MyData.Address)
         Console.WriteLine("City: {0}", MyData.City)
         Console.WriteLine("State: {0}", MyData.State)
         Console.WriteLine("ZIP Code: {0}", MyData.Zip)

         Console.WriteLine("The following address will be used:")
         Console.WriteLine(MyData.Address)
         Console.WriteLine(MyData.CityStateZip)
      End If
   End Sub
End Class

Public Class MailToData
   Private strName As String = ""
   Private strAddress As String = ""
   Private strCityStateZip As String = ""
   Private strCity As String = ""
   Private strState As String = ""
   Private strZip As String = ""
   Private parseSucceeded As Boolean = False

   Public Property Name() As String
      Get
         Return strName
      End Get
      Set
         strName = value
      End Set
   End Property 

   Public Property Address() As String
      Get
         Return strAddress
      End Get
      Set
         strAddress = value
      End Set
   End Property 

   Public Property CityStateZip() As String
      Get
         Return String.Format("{0}, {1} {2}", strCity, strState, strZip)
      End Get
      Set
         strCityStateZip = value.Trim()
         ParseCityStateZip()
      End Set
   End Property

   Public Property City() As String
      Get
         Return strCity
      End Get
      Set
         strCity = value
      End Set
   End Property 

   Public Property State() As String
      Get
         Return strState
      End Get
      Set
         strState = value
      End Set
   End Property 

   Public Property Zip() As String
      Get
         Return strZip
      End Get
      Set
         strZip = value
      End Set
   End Property

   Public ReadOnly Property Validated As Boolean
      Get
         Return parseSucceeded 
      End Get
   End Property 

   Private Sub ParseCityStateZip()
      Dim msg As String = Nothing
      Const msgEnd As String = vbCrLf + 
                               "You must enter spaces between city, state, and zip code." +
                               vbCrLf

      ' Throw a FormatException if the user did not enter the necessary spaces
      ' between elements. 
      Try
         ' City may consist of multiple words, so we'll have to parse the 
         ' string from right to left starting with the zip code.
         Dim zipIndex As Integer = strCityStateZip.LastIndexOf(" ")
         If zipIndex = -1 Then 
            msg = vbCrLf + "Cannot identify a zip code." + msgEnd
            Throw New FormatException(msg)
         End If
         strZip = strCityStateZip.Substring(zipIndex + 1)        

         Dim stateIndex As Integer = strCityStateZip.LastIndexOf(" ", zipIndex - 1)
         If stateIndex = -1 Then  
            msg = vbCrLf + "Cannot identify a state." + msgEnd
            Throw New FormatException(msg)
         End If
         strState = strCityStateZip.Substring(stateIndex + 1, zipIndex - stateIndex - 1)        
         strState = strState.ToUpper()

         strCity = strCityStateZip.Substring(0, stateIndex)
         If strCity.Length = 0 Then
            msg = vbCrLf + "Cannot identify a city." + msgEnd
            Throw New FormatException(msg)
         End If
         parseSucceeded = True
      Catch ex As FormatException
         Console.WriteLine(ex.Message)  
      End Try
   End Sub
End Class
```

Dopo aver eseguito il codice precedente, all'utente viene chiesto di immettere nome e indirizzo. L'applicazione inserisce le informazioni nelle proprietà corrette e visualizza le informazioni all'utente, creando una singola stringa che contiene la città, lo stato e il codice postale ZIP (Stati Uniti).

## <a name="see-also"></a>Vedere anche

[Operazioni di base su stringhe](basic-string-operations.md)



<!--HONumber=Nov16_HO3-->


