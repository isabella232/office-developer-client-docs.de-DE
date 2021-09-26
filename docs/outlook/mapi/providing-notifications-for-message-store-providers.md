---
title: Bereitstellen von Benachrichtigungen für Nachrichtenanbieter Store
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.localizationpriority: medium
api_type:
- COM
ms.assetid: c0e1cdba-ceb6-4a3f-8449-79d1a0ad1adf
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: aaa51d12ee6959d4ec8f75c84ce0cf4124922300
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59624376"
---
# <a name="providing-notifications-for-message-store-providers"></a>Bereitstellen von Benachrichtigungen für Nachrichtenanbieter Store

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Obwohl Benachrichtigungen optional sind, sind sie ein sehr wichtiger Bestandteil eines guten Nachrichtenspeicheranbieters. Clientanwendungen und der MAPI-Spooler verwenden Benachrichtigungen vom Nachrichtenspeicheranbieter, um eine gute Leistung beim Senden ausgehender Nachrichten oder beim Empfangen eingehender Nachrichten zu erzielen. Clients und der MAPI-Spooler können funktionieren, ohne Benachrichtigungen vom Nachrichtenspeicheranbieter zu erhalten, aber sie können die Benutzer nicht über Änderungen im Nachrichtenspeicher informieren. In der Regel bedeutet dies, dass Benutzer nicht sehen können, dass eine neue Nachricht angekommen ist, bis ihr Client den Empfangsordner des Nachrichtenspeichers das nächste Mal öffnet.
  
Clients registrieren sich für Benachrichtigungen, indem sie die [IMsgStore::Advise-Methode](imsgstore-advise.md) aufrufen. Der Client übergibt eine [IMAPIAdviseSink : IUnknown-Schnittstelle,](imapiadvisesinkiunknown.md) eine Bitmaske, die angibt, welche Art von Benachrichtigungen der Client empfangen möchte, und eine **EntryID,** die angibt, für welches Objekt im Nachrichtenspeicher die **Empfehlungsanforderung** gilt. Wenn relevante Ereignisse im Objekt auftreten (z. B. wenn eine neue Nachricht im Empfangsordner im Nachrichtenspeicher eintrifft), sollte der Nachrichtenspeicheranbieter oder das Objekt selbst die [IMAPIAdviseSink::OnNotify-Methode](imapiadvisesink-onnotify.md) für alle **IMAPIAdviseSink-Objekte** aufrufen, die für diesen Ereignistyp registriert wurden. 
  
Auch wenn Ihr Nachrichtenspeicheranbieter andere MAPI-Komponenten nie über Änderungen im Nachrichtenspeicher benachrichtigt, sollte er **dennoch IMsgStore::Advise** implementieren, um MAPI_E_NO_SUPPORT zurückzugeben. Dadurch werden andere Komponenten informiert, die keine Benachrichtigungen vom Nachrichtenspeicheranbieter erwarten. 
  
## <a name="see-also"></a>Siehe auch



[Nachrichtenspeicher-Features](message-store-features.md)

