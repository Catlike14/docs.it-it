---
title: Controllo di serializzazione e deserializzazione con SerializationBinder
ms.date: 03/30/2017
ms.assetid: ba8dcecf-acc7-467c-939d-021bbac797d4
ms.openlocfilehash: 3252413606f4aaf45a825d8d0a6f4af8763ef6be
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 05/04/2018
ms.locfileid: "33488917"
---
# <a name="controlling-serialization-and-deserialization-with-serializationbinder"></a>Controllo di serializzazione e deserializzazione con SerializationBinder
Durante la serializzazione un formattatore trasmette le informazioni necessarie per la creazione di un'istanza di un oggetto di tipo e versione corretti. Tali informazioni comprendono in genere il nome completo del tipo e il nome dell'assembly dell'oggetto. Per impostazione predefinita, la deserializzazione usa queste informazioni per creare un'istanza di un oggetto identico. Per alcuni utenti potrebbe essere necessario controllare la classe da serializzare e deserializzare, in quanto la classe originale potrebbe non esistere sul computer che esegue la deserializzazione o si è spostata tra gli assembly oppure su server e client sono necessarie versioni diverse della classe. Per altre informazioni, vedere [utilizzo di serializzazione dello strumento di associazione](../../../../docs/framework/wcf/samples/usage-of-serialization-binder.md).  
  
> [!WARNING]
>  Questa funzionalità è disponibile solo se si usa <xref:System.Runtime.Serialization.Formatters.Binary.BinaryFormatter> o <xref:System.Runtime.Serialization.NetDataContractSerializer>.  
  
## <a name="using-serializationbinder"></a>Uso di SerializationBinder  
 <xref:System.Runtime.Serialization.SerializationBinder> è una classe astratta usata per controllare i tipi effettivi usati durante la serializzazione e la deserializzazione. Per controllare i tipi usati durante la serializzazione e la deserializzazione, derivare una classe da <xref:System.Runtime.Serialization.SerializationBinder> ed eseguire l'override dei metodi <xref:System.Runtime.Serialization.SerializationBinder.BindToName(System.Type,System.String@,System.String@)> e <xref:System.Runtime.Serialization.SerializationBinder.BindToType(System.String,System.String)>. Il metodo <xref:System.Runtime.Serialization.SerializationBinder.BindToName(System.Type,System.String@,System.String@)> usa un elemento <xref:System.Type> e restituisce un nome tipo e assembly. Il metodo <xref:System.Runtime.Serialization.SerializationBinder.BindToType(System.String,System.String)> usa un nome tipo e assembly e restituisce un elemento <xref:System.Type>.  
  
## <a name="see-also"></a>Vedere anche  
 [Serializzazione e deserializzazione](../../../../docs/framework/wcf/feature-details/serialization-and-deserialization.md)  
 [Uso del gestore di associazione della serializzazione](../../../../docs/framework/wcf/samples/usage-of-serialization-binder.md)
