---
title: Behandeln von Benachrichtigungen
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.localizationpriority: medium
api_type:
- COM
ms.assetid: 451b71da-a888-4d8f-9814-12f9f846de05
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 1d87b4bc2ee33d4a9590f94af868a2d98ba7c7ac
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59576205"
---
# <a name="handling-notifications"></a>Behandeln von Benachrichtigungen

**Gilt für**: Outlook 2013 | Outlook 2016 
  
Benachrichtigungen ermöglichen es einem Objekt, ein anderes Objekt darüber zu informieren, dass eine Änderung vorgenommen wurde. Der Typ der Änderung wird als Ereignis bezeichnet. MAPI definiert mehrere Ereignisse, für die Benachrichtigungen generiert werden. 
  
Clients registrieren sich in der Regel für ein oder mehrere Ereignisse mit einem oder mehreren Objekten. Diese Objekte werden als Empfehlungsquellen bezeichnet. Objekte, die als Empfehlungsquellen fungieren können, umfassen das Sitzungsobjekt, unter mapi-Kontrolle oder ein von einem Dienstanbieter erstelltes Objekt, z. B. eine Nachricht. Das informierte Objekt, das als Empfehlungssenke bezeichnet wird, enthält entweder eine Implementierung der [IMAPIAdviseSink : IUnknown-Schnittstelle](imapiadvisesinkiunknown.md) oder der [IMAPIViewAdviseSink : IUnknown-Schnittstelle](imapiviewadvisesinkiunknown.md) und befindet sich in einer Clientanwendung. 
  
Advise-Quellobjekte  implementieren eine Advise-Methode, die von Clients aufgerufen wird, um sich für Benachrichtigungen zu registrieren, und eine **Unadvise-Methode,** die aufgerufen wird, um eine Registrierung abzubrechen. Einer der zu **empfehlenden** Parameter ist ein Zeiger auf eine Implementierung von **IMAPIAdviseSink** oder ** IMAPIViewAdviseSink **. Die Empfehlungsquelle speichert diesen Zeiger zwischen, damit [er IMAPIAdviseSink::OnNotify](imapiadvisesink-onnotify.md) oder eine der Methoden in **IMAPIViewAdviseSink** aufrufen kann, wenn eine Änderung auftritt. 
  
Da der Empfang von Benachrichtigungen es Benutzern ermöglicht, die aktuellsten Informationen anzuzeigen, wird empfohlen, dass sich alle Clients für Benachrichtigungen registrieren und diese behandeln. Es ist jedoch optional.
  
## <a name="in-this-section"></a>Inhalt dieses Abschnitts

- [Registrieren für eine Benachrichtigung:](registering-for-a-notification.md)Beschreibt, wie ein Client für Benachrichtigungen als Teil des Initialisierungsprozesses registriert wird.
    
- [Abbrechen einer Benachrichtigung:](canceling-a-notification.md)Beschreibt, wie sie ein Abonnement für eine Benachrichtigung kündigen.
    
- [Behandeln von Nachrichten Store Benachrichtigung:](handling-message-store-notification.md)Beschreibt, wie Sie sich für Nachrichtenspeicherbenachrichtigungen registrieren.
    
- [Handing Address Book Notification](handing-address-book-notification.md): Beschreibt, wie Adressbuchbenachrichtigungen registriert und behandelt werden.
    
- [Behandeln von Tabellenbenachrichtigungen:](handling-table-notification.md)Beschreibt, wie Sie sich für Benachrichtigungen aus der Hierarchietabelle registrieren.
    
- [Implementieren eines Advise Sink-Objekts:](implementing-an-advise-sink-object.md)Beschreibt, wie ein Empfehlungs-Senkenobjekt implementiert wird.
    
- [Timing einer Benachrichtigung:](timing-a-notification.md)Beschreibt den Zeitpunkt der Clientbenachrichtigung durch Dienstanbieter.
    
- [Sicherstellen einer Thread-Safe benachrichtigung:](ensuring-a-thread-safe-notification.md)Beschreibt, wie threadsichere Benachrichtigungen mit MAPI sichergestellt werden.
    
- [Erzwingen einer Benachrichtigung:](forcing-a-notification.md)Beschreibt, wie eine Benachrichtigung in mapi erzwungen wird.
    

