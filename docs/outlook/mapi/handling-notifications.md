---
title: Behandeln von Benachrichtigungen
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 451b71da-a888-4d8f-9814-12f9f846de05
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: e261b71a8e94d9db3b1b17168d84798dfe18955d
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33429159"
---
# <a name="handling-notifications"></a>Behandeln von Benachrichtigungen

**Gilt für**: Outlook 2013 | Outlook 2016 
  
Benachrichtigungen ermöglichen es einem Objekt, ein anderes Objekt darüber zu informieren, dass es einer Änderung unterzogen wurde. Der Änderungstyp wird als Ereignis bezeichnet. MAPI definiert mehrere Ereignisse, für die Benachrichtigungen generiert werden. 
  
Clients registrieren sich in der Regel für ein oder mehrere Ereignisse mit einem oder mehreren Objekten. Diese Objekte werden als Ratenquellen bezeichnet. Zu den Objekten, die als Ratgeberquellen fungieren können, gehören das Sitzungsobjekt unter mapI-Steuerelement oder ein von einem Dienstanbieter erstelltes Objekt, z. B. eine Nachricht. Das informierte Objekt, das als "Advise Sink" bezeichnet wird, enthält entweder eine Implementierung der [IMAPIAdviseSink : IUnknown-Schnittstelle](imapiadvisesinkiunknown.md) oder die [IMAPIViewAdviseSink : IUnknown-Schnittstelle](imapiviewadvisesinkiunknown.md) und befindet sich innerhalb einer Clientanwendung. 
  
Advise-Quellobjekte implementieren eine **Advise-Methode,** die von Clients aufgerufen wird, um sich für Benachrichtigungen zu registrieren, und eine **Unadvise-Methode,** die aufgerufen wird, um eine Registrierung abbricht. Einer der zu empfehlenden Parameter **ist** ein Zeiger auf eine Implementierung von **IMAPIAdviseSink** oder ** IMAPIViewAdviseSink **. Die Advise-Quelle speichert diesen Zeiger zwischen, sodass er [IMAPIAdviseSink::OnNotify](imapiadvisesink-onnotify.md) oder eine der Methoden in **IMAPIViewAdviseSink** aufrufen kann, wenn eine Änderung auftritt. 
  
Da benutzer beim Empfangen von Benachrichtigungen die neuesten Informationen anzeigen können, wird empfohlen, dass sich alle Clients für Benachrichtigungen registrieren und diese behandeln. Sie ist jedoch optional.
  
## <a name="in-this-section"></a>Inhalt dieses Abschnitts

- [Registrieren für eine Benachrichtigung](registering-for-a-notification.md): Beschreibt, wie ein Client für Benachrichtigungen als Teil des Initialisierungsprozesses registriert wird.
    
- [Abbrechen einer Benachrichtigung](canceling-a-notification.md): Beschreibt, wie Sie ein Abonnement für eine Benachrichtigung kündigen.
    
- [Handling Message Store Notification](handling-message-store-notification.md): Beschreibt, wie Sie sich für Nachrichtenspeicherbenachrichtigungen registrieren.
    
- [Benachrichtigung über das Handhandbuch:](handing-address-book-notification.md)Beschreibt, wie Adressbuchbenachrichtigungen registriert und behandelt werden.
    
- [Behandeln von Tabellenbenachrichtigungen](handling-table-notification.md): Beschreibt, wie Sie sich für Benachrichtigungen aus der Hierarchietabelle registrieren.
    
- [Implementieren eines Advise Sink-Objekts:](implementing-an-advise-sink-object.md)Beschreibt die Implementierung eines Advise Sink-Objekts.
    
- [Timing a Notification](timing-a-notification.md): Beschreibt den Zeitpunkt der Clientbenachrichtigung durch Dienstanbieter.
    
- [Sicherstellen einer Thread-Safe Benachrichtigung](ensuring-a-thread-safe-notification.md): Beschreibt, wie Sie threadsichere Benachrichtigungen mit MAPI sicherstellen.
    
- [Erzwingen einer Benachrichtigung](forcing-a-notification.md): Beschreibt, wie Sie eine Benachrichtigung in MAPI erzwingen.
    

