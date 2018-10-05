---
title: Eine Nachricht mit TNEF-Codierung
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 6b86d9a9-6876-4885-ae1e-8571b25b85cc
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: cdaa03cfbc0bbd0fcf6a320ecf8fae9f372d5781
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/04/2018
ms.locfileid: "25382526"
---
# <a name="encoding-a-message-with-tnef"></a>Eine Nachricht mit TNEF-Codierung

**Gilt für**: Outlook 2013 | Outlook 2016 
  
Wenn eine Nachricht gesendet wird, kann der Adressbuchhierarchie eine Datei erstellen, die verwendet wird, um die Nachricht während der Übertragung enthalten. Im nächsten Schritt wird die Datei eine [IStream](https://msdn.microsoft.com/library/aa380034%28VS.85%29.aspx) -Schnittstelle umbrochen. Der Adressbuchhierarchie verwendet [ITnef](itnefiunknown.md) Methoden, um die Eigenschaften der Nachricht in das Stream-Objekt in einem markierten Format schreiben, mit dem die Eigenschaften, die von der empfangenden Transport-Anbietern auf einfache Weise decodiert werden können. 
  
**Gesamte Nachricht in einer einzigen Datei darstellen.**
  
1. Abrufen eines TNEF-Objekts, indem Sie ein [IStream](https://msdn.microsoft.com/library/aa380034%28VS.85%29.aspx) -Objekt und eine Nachricht an die Funktion [OpenTnefStreamEx](opentnefstreamex.md) übergeben. 
    
2. Erhalten Sie eine Liste aller definierten Eigenschaften für die Nachricht, durch die [IMAPIProp::GetPropList](imapiprop-getproplist.md) -Methode aufrufen. 
    
3. Verwenden Sie [IMAPIProp](imapipropiunknown.md) Methoden, um alle Eigenschaften von messaging-System unterstützt auszuschließen. Schreiben Sie zu einem geeigneten Zeitpunkt diese Eigenschaften in der messaging-System im Format von messaging-System erforderlich. 
    
4. Rufen Sie [ITnef::AddProps](itnef-addprops.md) , um die übrigen Eigenschaften, einschließlich aller Anlagen zu codieren. 
    
5. Rufen Sie die [ITnef::Finish](itnef-finish.md) -Methode, um die Nachricht in der TNEF-Stream codieren, nachdem alle angeforderten Eigenschaften hinzugefügt werden. 
    
6. Rufen Sie die [ITnef::OpenTaggedBody](itnef-opentaggedbody.md) -Methode, um den markierten Nachrichtentext zu erhalten. Dieser markierte Text wird an die messaging-System mit den Methoden der OLE- [IStream](https://msdn.microsoft.com/library/aa380034%28VS.85%29.aspx) -Schnittstelle geschrieben. 
    
7. Rufen Sie die [IUnknown](https://msdn.microsoft.com/library/ms682317%28VS.85%29.aspx) -Methode, um das Objekt **ITnef** freizugeben. 
    
**An den Prozess eine eingehende TNEF-Nachricht**
  
1. Entnehmen Sie ein MAPI-Message-Objekt die MAPI-Warteschlange und Schreiben Sie Nachrichtenkopf-Eigenschaften in die neue MAPI-Nachricht zu.
    
2. Erstellen Sie und initialisieren Sie [IStream](https://msdn.microsoft.com/library/aa380034%28VS.85%29.aspx) -Objekts, um die TNEF-Daten aus der eingehenden Nachricht enthalten. 
    
3. Übergeben Sie die MAPI-Nachricht und die [IStream](https://msdn.microsoft.com/library/aa380034%28VS.85%29.aspx) -Objekt an die [OpenTnefStreamEx](opentnefstreamex.md) -Funktion. 
    
4. Decodieren Sie die Informationen in die TNEF-Daten durch Aufrufen der Methode [ITnef::ExtractProps](itnef-extractprops.md) . 
    
   > [!NOTE]
   > Nichts **ExtractProps** decodiert werden Eigenschaften, die von der eingehenden Nachricht Umschlag decodiert überschrieben. D. h., überschreibt extrahierte TNEF-Eigenschaften die vorhandenen Eigenschaften in einer Nachricht. 
  
5. Den markierten Nachrichtentext durch Aufrufen von [ITnef::OpenTaggedBody](itnef-opentaggedbody.md) verarbeiten und analysiert den Text, um die Anlage Positionen wiederherstellen. 
    
6. Speichern Sie die Nachricht durch Aufrufen von [IMAPIProp::SaveChanges](imapiprop-savechanges.md).
    
7. Das TNEF-Objekt wird durch Aufrufen der Methode [IUnknown](https://msdn.microsoft.com/library/ms682317%28VS.85%29.aspx) frei. 
    

