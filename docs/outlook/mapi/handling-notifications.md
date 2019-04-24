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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32299387"
---
# <a name="handling-notifications"></a>Behandeln von Benachrichtigungen

**Gilt für**: Outlook 2013 | Outlook 2016 
  
Benachrichtigungen aktivieren Sie ein Objekt, um ein anderes Objekt zu informieren, dass eine Änderung durchlaufen wurde. Der Typ der Änderung wird als Ereignis bezeichnet. MAPI definiert mehrere Ereignisse, für die Benachrichtigungen generiert werden. 
  
Clients registrieren sich in der Regel für ein oder mehrere Ereignisse mit einem oder mehreren Objekten. Diese Objekte werden als Advise sources bezeichnet. Zu den Objekten, die als Advise-Quellen fungieren können, gehört das Session-Objekt unter MAPIs Steuerelement oder ein von einem Dienstanbieter erstelltes Objekt wie eine Nachricht. Das informierte Objekt, das als Advise-Senke bezeichnet wird, enthält entweder eine Implementierung der [IMAPIAdviseSink: IUnknown](imapiadvisesinkiunknown.md) -Schnittstelle oder die [IMAPIViewAdviseSink: IUnknown](imapiviewadvisesinkiunknown.md) -Schnittstelle und befindet sich innerhalb einer Clientanwendung. 
  
Advise-Quellobjekte implementieren Sie eine **Advise** -Methode, die von Clients zum Registrieren von Benachrichtigungen aufgerufen wird, und eine Unadvise-Methode, die zum Abbrechen einer Registrierung aufgerufen wird. **** Einer der zu **Advise** -Parameter ist ein Zeiger auf eine Implementierung von **IMAPIAdviseSink** oder * * IMAPIViewAdviseSink * *. Die Advise-Quelle speichert diesen Zeiger zwischen, sodass er [IMAPIAdviseSink:: OnNotify](imapiadvisesink-onnotify.md) oder eine der Methoden in **IMAPIViewAdviseSink** beim Auftreten einer Änderung aufrufen kann. 
  
Da das Empfangen von Benachrichtigungen es Benutzern ermöglicht, die aktuellsten Informationen anzuzeigen, empfiehlt es sich, dass alle Clients Benachrichtigungen registrieren und behandeln. Sie ist jedoch optional.
  
## <a name="in-this-section"></a>Inhalt dieses Abschnitts

- [Registrieren für eine Benachrichtigung](registering-for-a-notification.md): Beschreibt, wie Sie einen Client für Benachrichtigungen im Rahmen des Initialisierungsprozesses registrieren.
    
- [Abbrechen einer Benachrichtigung](canceling-a-notification.md): Beschreibt, wie ein Abonnement für eine Benachrichtigung abgebrochen wird.
    
- [Behandeln von Nachrichtenspeicher](handling-message-store-notification.md)Benachrichtigungen: Beschreibt, wie Sie sich für Nachrichtenspeicher Benachrichtigungen registrieren.
    
- [Adressbuch Benachrichtigung](handing-address-book-notification.md): Beschreibt, wie Sie sich für Adressbuch Benachrichtigungen registrieren und behandeln.
    
- [Behandlung von Tabellen Benachrichtigungen](handling-table-notification.md): Beschreibt, wie Sie sich in der Hierarchietabelle für Benachrichtigungen registrieren.
    
- [Implementieren eines Advise](implementing-an-advise-sink-object.md)-Senke-Objekts: Beschreibt, wie ein Advise-Senke-Objekt implementiert wird.
    
- [Timing a Notification](timing-a-notification.md): Beschreibt den Zeitpunkt der Client Benachrichtigung durch Dienstanbieter.
    
- Sicherstellen [einer threadsicheren Benachrichtigung](ensuring-a-thread-safe-notification.md): Beschreibt, wie threadsichere Benachrichtigungen mit MAPI sichergestellt werden.
    
- [Erzwingen einer Benachrichtigung](forcing-a-notification.md): Beschreibt, wie eine Benachrichtigung in MAPI erzwungen wird.
    

