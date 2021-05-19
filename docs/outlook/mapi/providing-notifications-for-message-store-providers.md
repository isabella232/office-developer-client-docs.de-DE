---
title: Bereitstellen von Benachrichtigungen für Store Anbieter
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: c0e1cdba-ceb6-4a3f-8449-79d1a0ad1adf
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: a28e6e6f008517a6b1c2c82dfa391b478963880f
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33419933"
---
# <a name="providing-notifications-for-message-store-providers"></a>Bereitstellen von Benachrichtigungen für Store Anbieter

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Obwohl Benachrichtigungen optional sind, sind sie ein sehr wichtiger Bestandteil eines guten Nachrichtenspeicheranbieters. Clientanwendungen und der MAPI-Spooler sind auf Benachrichtigungen des Nachrichtenspeicheranbieters angewiesen, um eine gute Leistung beim Senden ausgehender Nachrichten oder beim Empfangen eingehender Nachrichten zu erzielen. Clients und der MAPI-Spooler können ohne Benachrichtigungen vom Nachrichtenspeicheranbieter funktionieren, aber sie können Benutzer nicht über Änderungen im Nachrichtenspeicher informieren, ohne sie. In der Regel bedeutet dies, dass Benutzer erst dann sehen können, wenn eine neue Nachricht eingetroffen ist, bis ihr Client als Nächstes den Empfangsordner des Nachrichtenspeichers öffnet.
  
Clients registrieren sich für Benachrichtigungen, indem sie die [IMsgStore::Advise-Methode](imsgstore-advise.md) aufrufen. Der Client übergibt eine [IMAPIAdviseSink : IUnknown-Schnittstelle,](imapiadvisesinkiunknown.md) eine Bitmaske, die angibt, welche Art von Benachrichtigungen der Client empfangen möchte, und eine **EntryID,** die angibt, für welches Objekt im Nachrichtenspeicher die **Advise-Anforderung** gilt. Wenn relevante Ereignisse im Objekt auftreten (z. B. wenn eine neue Nachricht im Empfangsordner im Nachrichtenspeicher eintrifft), sollte der Nachrichtenspeicheranbieter oder das Objekt selbst die [IMAPIAdviseSink::OnNotify-Methode](imapiadvisesink-onnotify.md) für alle **IMAPIAdviseSink-Objekte** aufrufen, die für diesen Ereignistyp registriert wurden. 
  
Auch wenn ihr Nachrichtenspeicheranbieter andere MAPI-Komponenten niemals über Änderungen im Nachrichtenspeicher benachrichtigt, sollte er dennoch **IMsgStore::Advise** implementieren, um MAPI_E_NO_SUPPORT. Dadurch werden andere Komponenten informiert, dass sie keine Benachrichtigungen vom Nachrichtenspeicheranbieter erwarten. 
  
## <a name="see-also"></a>Siehe auch



[Nachrichtenspeicher-Features](message-store-features.md)

