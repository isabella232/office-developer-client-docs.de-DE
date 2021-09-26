---
title: Codieren einer Nachricht mit TNEF
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.localizationpriority: medium
api_type:
- COM
ms.assetid: 6b86d9a9-6876-4885-ae1e-8571b25b85cc
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 1d45a79b9b0817e760d53327da5c5e5ef82a67e6
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59630950"
---
# <a name="encoding-a-message-with-tnef"></a>Codieren einer Nachricht mit TNEF

**Gilt für**: Outlook 2013 | Outlook 2016 
  
Wenn eine Nachricht gesendet wird, kann der Transportanbieter eine Datei erstellen, die verwendet wird, um die Nachricht während der Übertragung zu enthalten. Als Nächstes wird eine [IStream-Schnittstelle](https://msdn.microsoft.com/library/aa380034%28VS.85%29.aspx) um die Datei gepackt. Der Transportanbieter verwendet dann [ITnef-Methoden,](itnefiunknown.md) um die Nachrichteneigenschaften in einem markierten Format in den Datenstrom zu schreiben, mit dem die Eigenschaften von den empfangenden Transportanbietern einfach decodiert werden können. 
  
**So stellen Sie eine gesamte Nachricht in einer einzelnen Datei dar**
  
1. Rufen Sie ein TNEF-Objekt ab, indem Sie ein [IStream-Objekt](https://msdn.microsoft.com/library/aa380034%28VS.85%29.aspx) und eine Nachricht an die [OpenTnefStreamEx-Funktion](opentnefstreamex.md) übergeben. 
    
2. Rufen Sie eine Liste aller definierten Eigenschaften für die Nachricht ab, indem Sie die [IMAPIProp::GetPropList-Methode](imapiprop-getproplist.md) aufrufen. 
    
3. Verwenden Sie [IMAPIProp-Methoden,](imapipropiunknown.md) um alle vom Messagingsystem unterstützten Eigenschaften auszuschließen. Schreiben Sie diese Eigenschaften zu einem geeigneten Zeitpunkt in das Messagingsystem in dem vom Messagingsystem erforderlichen Format. 
    
4. Rufen Sie [ITnef::AddProps](itnef-addprops.md) auf, um die verbleibenden Eigenschaften einschließlich aller Anlagen zu codieren. 
    
5. Rufen Sie die [ITnef::Finish-Methode](itnef-finish.md) auf, um die Nachricht im TNEF-Stream zu codieren, nachdem alle angeforderten Eigenschaften hinzugefügt wurden. 
    
6. Rufen Sie die [ITnef::OpenTaggedBody-Methode](itnef-opentaggedbody.md) auf, um den markierten Nachrichtentext abzurufen. Dieser markierte Text wird mithilfe von Methoden der [OLE-IStream-Schnittstelle](https://msdn.microsoft.com/library/aa380034%28VS.85%29.aspx) in das Messagingsystem geschrieben. 
    
7. Rufen Sie die [IUnknown::Release-Methode](https://msdn.microsoft.com/library/ms682317%28VS.85%29.aspx) auf, um das **ITnef-Objekt** freizugeben. 
    
**So verarbeiten Sie eine eingehende TNEF-Nachricht**
  
1. Rufen Sie ein MAPI-Nachrichtenobjekt aus dem MAPI-Spooler ab, und schreiben Sie Nachrichtenkopfeigenschaften in die neue MAPI-Nachricht.
    
2. Erstellen und Initialisieren eines [IStream-Objekts,](https://msdn.microsoft.com/library/aa380034%28VS.85%29.aspx) das die TNEF-Daten aus der eingehenden Nachricht enthält. 
    
3. Übergeben Sie die MAPI-Nachricht und das [IStream-Objekt](https://msdn.microsoft.com/library/aa380034%28VS.85%29.aspx) an die [OpenTnefStreamEx-Funktion.](opentnefstreamex.md) 
    
4. Decodieren Sie die Informationen in den TNEF-Daten, indem Sie die [ITnef::ExtractProps-Methode](itnef-extractprops.md) aufrufen. 
    
   > [!NOTE]
   > Alle von **ExtractProps** decodierten Eigenschaften werden vom Umschlag der eingehenden Nachricht decodiert. Das heißt, extrahierte TNEF-Eigenschaften überschreiben die vorhandenen Eigenschaften in einer Nachricht. 
  
5. Verarbeiten Sie den markierten Nachrichtentext durch Aufrufen von [ITnef::OpenTaggedBody,](itnef-opentaggedbody.md) und analysieren Sie den Text, um Anlagenpositionen wiederherzustellen. 
    
6. Speichern Sie die Nachricht, indem Sie [IMAPIProp::SaveChanges](imapiprop-savechanges.md)aufrufen.
    
7. Geben Sie das TNEF-Objekt frei, indem Sie die [IUnknown::Release-Methode](https://msdn.microsoft.com/library/ms682317%28VS.85%29.aspx) aufrufen. 
    

