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
  
Wenn eine Nachricht übermittelt wird, kann der Transportanbieter eine Datei erstellen, die die Nachricht während der Übertragung enthält. Als nächstes wird eine [IStream](https://msdn.microsoft.com/library/aa380034%28VS.85%29.aspx) -Schnittstelle um die Datei umbrochen. Der Transportanbieter verwendet dann [ITnef](itnefiunknown.md) -Methoden, um die Nachrichteneigenschaften in den Stream in einem gekennzeichneten Format zu schreiben, mit dem die Eigenschaften problemlos von den empfangenden Transportanbietern dekodiert werden können. 
  
**So stellen Sie eine gesamte Nachricht in einer einzelnen Datei dar**
  
1. Rufen Sie ein TNEF-Objekt ab, indem Sie ein [IStream](https://msdn.microsoft.com/library/aa380034%28VS.85%29.aspx) -Objekt und eine Nachricht an die [OpenTnefStreamEx](opentnefstreamex.md) -Funktion übergeben. 
    
2. Rufen Sie eine Liste aller definierten Eigenschaften für die Nachricht ab, indem Sie die [IMAPIProp::](imapiprop-getproplist.md) getproplist-Methode aufrufen. 
    
3. Verwenden Sie [IMAPIProp](imapipropiunknown.md) -Methoden, um alle vom Messagingsystem unterstützten Eigenschaften auszuschließen. Schreiben Sie diese Eigenschaften zu einem geeigneten Zeitpunkt in dem Format, das vom Messagingsystem benötigt wird, in das Messagingsystem. 
    
4. Rufen Sie [ITnef::](itnef-addprops.md) AddProps auf, um die restlichen Eigenschaften einschließlich aller Anlagen zu codieren. 
    
5. Rufen Sie die [ITnef:: Finish](itnef-finish.md) -Methode auf, um die Nachricht in den TNEF-Stream zu codieren, nachdem alle angeforderten Eigenschaften hinzugefügt wurden. 
    
6. Rufen Sie die [ITnef:: OpenTaggedBody](itnef-opentaggedbody.md) -Methode auf, um den markierten Nachrichtentext abzurufen. Dieser markierte Text wird mithilfe von Methoden der OLE [IStream](https://msdn.microsoft.com/library/aa380034%28VS.85%29.aspx) -Schnittstelle an das Messagingsystem geschrieben. 
    
7. Rufen Sie die [IUnknown:: Release](https://msdn.microsoft.com/library/ms682317%28VS.85%29.aspx) -Methode auf, um das **ITnef** -Objekt freigegeben. 
    
**So verarbeiten Sie eine eingehende TNEF-Nachricht**
  
1. Rufen Sie ein MAPI-Nachrichtenobjekt aus dem MAPI-Spooler ab, und schreiben Sie die Nachrichtenkopf Eigenschaften in die neue MAPI-Nachricht.
    
2. Erstellen und initialisieren Sie ein [IStream](https://msdn.microsoft.com/library/aa380034%28VS.85%29.aspx) -Objekt, das die TNEF-Daten aus der eingehenden Nachricht enthält. 
    
3. Führen Sie die MAPI-Nachricht und das [IStream](https://msdn.microsoft.com/library/aa380034%28VS.85%29.aspx) -Objekt an die [OpenTnefStreamEx](opentnefstreamex.md) -Funktion. 
    
4. DeCodieren Sie die Informationen in den TNEF-Daten, indem Sie die [ITnef:: ExtractProps](itnef-extractprops.md) -Methode aufrufen. 
    
   > [!NOTE]
   > Von **ExtractProps** deCodierte Elemente überschreiben Eigenschaften, die aus dem Umschlag der eingehenden Nachricht dekodiert wurden. Das heißt, extrahierte TNEF-Eigenschaften überschreiben die vorhandenen Eigenschaften in einer Nachricht. 
  
5. Verarbeiten Sie den markierten Nachrichtentext, indem Sie [ITnef:: OpenTaggedBody](itnef-opentaggedbody.md) aufrufen und den Text analysieren, um die Anlagen Positionen wiederherzustellen. 
    
6. Speichern Sie die Nachricht, indem Sie [IMAPIProp:: SaveChanges](imapiprop-savechanges.md)aufrufen.
    
7. Geben Sie das TNEF-Objekt durch Aufrufen der [IUnknown:: Release](https://msdn.microsoft.com/library/ms682317%28VS.85%29.aspx) -Methode frei. 
    

