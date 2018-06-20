---
title: Bereitstellen von Benachrichtigungen für Nachrichtenspeicher-Anbieter
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: c0e1cdba-ceb6-4a3f-8449-79d1a0ad1adf
description: 'Letzte �nderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 3abb4ba67ff5f0cf2284fa9286b6968698877b84
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19795333"
---
# <a name="providing-notifications-for-message-store-providers"></a>Bereitstellen von Benachrichtigungen für Nachrichtenspeicher-Anbieter

  
  
**Betrifft**: Outlook 
  
Während Benachrichtigungen optional sind, werden sie ein sehr wichtiger Bestandteil der Anbieter eine gute Nachricht. Clientanwendungen und die MAPI-Warteschlange basieren auf Benachrichtigungen vom Anbieter für die Nachricht an eine gute Leistung beim Senden von ausgehenden Nachrichten oder Empfangen von eingehenden Nachrichten zu erhalten. Clients und die MAPI-Warteschlange können ohne Empfang von Benachrichtigungen aus der Nachricht Informationsdienst funktionieren, aber sie sind nicht in der Lage, Benutzer über Änderungen an den Nachrichtenspeicher, ohne sie zu informieren. Dies bedeutet, die Benutzer werden nicht angezeigt, dass eine neue Nachrichten eingegangen sind, bis deren Clients als Nächstes des Nachrichtenspeicher wird geöffnet wird meistens Ordner.
  
Clients, die durch Aufrufen der Methode [IMsgStore::Advise](imsgstore-advise.md) für Benachrichtigungen registriert werden. Der Client übergibt ein [IMAPIAdviseSink: IUnknown](imapiadvisesinkiunknown.md) Schnittstelle, eine Bitmaske dar, der angibt, welche Art von Benachrichtigungen der Client empfangen, interessiert ist und eine **EntryID** , der angibt, welches Objekt in der Nachricht Speichern der **Advise** Anforderung betrifft. Treten relevanten Ereignisse im-Objekt (beispielsweise, wenn eine neue Nachricht in den Empfangsordner im Nachrichtenspeicher eingeht), sollte die Nachricht Speicheranbieter oder das Objekt selbst die [IMAPIAdviseSink::OnNotify](imapiadvisesink-onnotify.md) -Methode für alle die **aufrufen IMAPIAdviseSink** -Objekten, die für diesen Ereignistyp registriert haben. 
  
Auch wenn Ihre Nachricht speichern benachrichtigt Anbieter nie andere MAPI-Komponenten über Änderungen an der Nachrichtenspeicher weiterhin **IMsgStore::Advise** zum Zurückgeben von MAPI_E_NO_SUPPORT implementiert werden soll. Andere Komponenten nicht zu erwarten, dass Benachrichtigungen aus der Nachricht Anbieter speichern weiß. 
  
## <a name="see-also"></a>Siehe auch



[Nachrichtenspeicher-Features](message-store-features.md)

