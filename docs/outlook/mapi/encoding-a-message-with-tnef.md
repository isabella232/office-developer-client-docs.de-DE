---
title: Codieren einer Nachricht mit TNEF
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 6b86d9a9-6876-4885-ae1e-8571b25b85cc
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: cdaa03cfbc0bbd0fcf6a320ecf8fae9f372d5781
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32336701"
---
# <a name="encoding-a-message-with-tnef"></a>Codieren einer Nachricht mit TNEF

**Gilt für**: Outlook 2013 | Outlook 2016 
  
Wenn eine Nachricht übermittelt wird, kann der Transportanbieter eine Datei erstellen, die während der Übertragung verwendet wird, um die Nachricht zu enthalten. Als Nächstes wird eine [IStream-Schnittstelle](https://msdn.microsoft.com/library/aa380034%28VS.85%29.aspx) um die Datei gepackt. Der Transportanbieter verwendet dann [ITnef-Methoden,](itnefiunknown.md) um die Nachrichteneigenschaften in einem markierten Format in den Datenstrom zu schreiben, mit dem die Eigenschaften von den empfangenden Transportanbietern problemlos decodiert werden können. 
  
**So stellen Sie eine gesamte Nachricht in einer einzelnen Datei dar**
  
1. Rufen Sie ein TNEF-Objekt ab, indem Sie ein [IStream-Objekt](https://msdn.microsoft.com/library/aa380034%28VS.85%29.aspx) und eine Nachricht an die [OpenTnefStreamEx-Funktion](opentnefstreamex.md) übergeben. 
    
2. Rufen Sie eine Liste aller definierten Eigenschaften für die Nachricht ab, indem Sie die [IMAPIProp::GetPropList-Methode](imapiprop-getproplist.md) aufrufen. 
    
3. Verwenden [Sie IMAPIProp-Methoden,](imapipropiunknown.md) um alle vom Messagingsystem unterstützten Eigenschaften auszuschließen. Schreiben Sie diese Eigenschaften zu einem geeigneten Zeitpunkt in das Messagingsystem im vom Messagingsystem benötigten Format. 
    
4. Rufen [Sie ITnef::AddProps auf,](itnef-addprops.md) um die verbleibenden Eigenschaften einschließlich aller Anlagen zu codieren. 
    
5. Rufen Sie die [ITnef::Finish-Methode](itnef-finish.md) auf, um die Nachricht in den TNEF-Stream zu codieren, nachdem alle angeforderten Eigenschaften hinzugefügt wurden. 
    
6. Rufen Sie [die ITnef::OpenTaggedBody-Methode](itnef-opentaggedbody.md) auf, um den markierten Nachrichtentext zu erhalten. Dieser markierte Text wird mithilfe von Methoden von der OLE IStream-Schnittstelle in das [Messagingsystem geschrieben.](https://msdn.microsoft.com/library/aa380034%28VS.85%29.aspx) 
    
7. Rufen Sie [die IUnknown::Release-Methode auf,](https://msdn.microsoft.com/library/ms682317%28VS.85%29.aspx) um das **ITnef-Objekt frei** zu geben. 
    
**So verarbeiten Sie eine eingehende TNEF-Nachricht**
  
1. Get a MAPI message object from the MAPI spooler and write message header properties into the new MAPI message.
    
2. Erstellen und initialisieren Sie ein [IStream-Objekt,](https://msdn.microsoft.com/library/aa380034%28VS.85%29.aspx) um die TNEF-Daten aus der eingehenden Nachricht zu enthalten. 
    
3. Übergeben Sie die MAPI-Nachricht und das [IStream-Objekt](https://msdn.microsoft.com/library/aa380034%28VS.85%29.aspx) an die [OpenTnefStreamEx-Funktion.](opentnefstreamex.md) 
    
4. Decodieren Sie die Informationen in den TNEF-Daten, indem Sie die [ITnef::ExtractProps-Methode](itnef-extractprops.md) aufrufen. 
    
   > [!NOTE]
   > Alle von **ExtractProps** decodierten Eigenschaften überschreiben Eigenschaften, die aus dem Umschlag der eingehenden Nachricht decodiert sind. Das heißt, extrahierte TNEF-Eigenschaften überschreiben die vorhandenen Eigenschaften in einer Nachricht. 
  
5. Verarbeiten Sie den markierten Nachrichtentext, indem [Sie ITnef::OpenTaggedBody](itnef-opentaggedbody.md) aufrufen und den Text analysieren, um Anlagenpositionen wiederhergestellt zu werden. 
    
6. Speichern Sie die Nachricht, indem Sie [IMAPIProp::SaveChanges aufrufen.](imapiprop-savechanges.md)
    
7. Geben Sie das TNEF-Objekt frei, indem Sie die [IUnknown::Release-Methode](https://msdn.microsoft.com/library/ms682317%28VS.85%29.aspx) aufrufen. 
    

