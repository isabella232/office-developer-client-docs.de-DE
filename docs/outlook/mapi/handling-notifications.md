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
ms.openlocfilehash: 4c19e88ac1cfb29a9841ec78516410e23b3e5403
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2018
ms.locfileid: "22567580"
---
# <a name="handling-notifications"></a>Behandeln von Benachrichtigungen

**Betrifft**: Outlook 2013 | Outlook 2016 
  
Benachrichtigungen aktivieren, ein Objekt zu einem anderen zu informieren, dass es eine Änderung unterzogen wurde-Objekt. Die Art der Änderung wird als ein Ereignis bezeichnet. MAPI definiert mehrere Ereignisse, die für die Benachrichtigung generiert werden. 
  
Clients registrieren Sie sich in der Regel für eine oder mehrere Ereignisse mit einem oder mehreren Objekten. Diese Objekte werden als bezeichnet advise-Quellen. Objekte, die act can as advise-Quellen sind das Session-Objekt unter des MAPI-Steuerelement oder ein Objekt von einem Dienstanbieter, wie eine Nachricht erstellt wurde. Das informierte-Objekt genannt der Advise-Empfänger enthält, entweder eine Implementierung von der [IMAPIAdviseSink: IUnknown](imapiadvisesinkiunknown.md) Schnittstelle oder die [IMAPIViewAdviseSink: IUnknown](imapiviewadvisesinkiunknown.md) -Schnittstelle und ist innerhalb von einer Clientanwendung aus. 
  
Advise-Source-Objekten Implementieren einer **Advise** -Methode, die von Clients für Benachrichtigungen registriert aufgerufen wird, und eine **Unadvise** -Methode, die aufgerufen wird, um eine Registrierung abzubrechen. Einer der Parameter zu **Advise** ist ein Zeiger auf eine Implementierung der **IMAPIAdviseSink** oder ** IMAPIViewAdviseSink **. Die Quelle der Advise speichert diese Zeiger, damit sie aufrufen kann [IMAPIAdviseSink::OnNotify](imapiadvisesink-onnotify.md) oder eine der Methoden in **IMAPIViewAdviseSink** bei einer Änderung wird. 
  
Da Benutzern das Anzeigen der aktuellsten Informationen empfangen von Benachrichtigungen ermöglicht werden, wird empfohlen, dass alle Clients für registrieren und Behandeln von Benachrichtigungen. Es ist jedoch optional.
  
## <a name="in-this-section"></a>Inhalt dieses Abschnitts

- [Registrieren für eine Benachrichtigung](registering-for-a-notification.md): Beschreibt, wie einen Client für Benachrichtigungen als Teil der Initialisierungsprozess zu registrieren.
    
- [Stornieren einer Benachrichtigungs](canceling-a-notification.md): Beschreibt, wie Sie ein Abonnement für eine Benachrichtigung abzubrechen.
    
- [Benachrichtigung bei Nachrichten speichern behandeln](handling-message-store-notification.md): Beschreibt, wie für Benachrichtigungen über Textnachrichten Store registrieren.
    
- [Zuzuteilen Address Book Benachrichtigung](handing-address-book-notification.md): Beschreibt, wie Sie für registrieren und Address Book Benachrichtigungen zu behandeln.
    
- [Behandeln von Tabelle Benachrichtigung](handling-table-notification.md): Beschreibt, wie für Benachrichtigungen aus der Hierarchietabelle registrieren.
    
- [Implementieren einer Advise-Empfängerobjekt](implementing-an-advise-sink-object.md): Implementieren einer Advise-Empfängerobjekt beschrieben.
    
- [Eine Benachrichtigung Anzeigedauer](timing-a-notification.md): den Zeitpunkt der Benachrichtigung durch den Client von Dienstanbietern beschreibt.
    
- [Sicherstellen, dass eine Benachrichtigung threadsicheren](ensuring-a-thread-safe-notification.md): Beschreibt, wie Sie threadsicheren Benachrichtigung mit MAPI sicherzustellen.
    
- [Erzwingen Sie eine Benachrichtigung](forcing-a-notification.md): Beschreibt, wie Sie eine Benachrichtigung in MAPI zu erzwingen.
    

