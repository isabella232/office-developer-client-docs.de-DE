---
title: Bereitstellen von Benachrichtigungen für Nachrichtenspeicher Anbieter
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: c0e1cdba-ceb6-4a3f-8449-79d1a0ad1adf
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: a28e6e6f008517a6b1c2c82dfa391b478963880f
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32328469"
---
# <a name="providing-notifications-for-message-store-providers"></a>Bereitstellen von Benachrichtigungen für Nachrichtenspeicher Anbieter

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Während Benachrichtigungen optional sind, sind Sie ein sehr wichtiger Teil eines guten Nachrichtenspeicher Anbieters. Client Anwendungen und der MAPI-Spooler verwenden Benachrichtigungen des Nachrichtenspeicher Anbieters, um beim Übermitteln ausgehender Nachrichten oder empfangen von eingehenden Nachrichten eine gute Leistung zu erzielen. Clients und der MAPI-Spooler können ohne Benachrichtigung des Nachrichtenspeicher Anbieters funktionieren, Sie können jedoch keine Benutzer über Änderungen im Nachrichtenspeicher informieren. In der Regel ist dies der Fall, dass Benutzer nicht erkennen können, dass eine neue Nachricht eingegangen ist, bis Ihr Client als nächstes den Empfangsordner des Nachrichtenspeichers öffnet.
  
Clients registrieren sich für Benachrichtigungen, indem Sie die [IMsgStore:: Advise](imsgstore-advise.md) -Methode aufrufen. Der Client übergibt eine [IMAPIAdviseSink: IUnknown](imapiadvisesinkiunknown.md) -Schnittstelle, eine Bitmaske, die angibt, welche Art von Benachrichtigungen der Client erhalten soll, **** und ein Eintrags-Nr., der angibt, welches Objekt im Nachrichtenspeicher die **Advise** Request gilt für. Wenn im Objekt relevante Ereignisse auftreten (beispielsweise, wenn eine neue Nachricht im empfangenden Ordner im Nachrichtenspeicher eingeht), sollte der Nachrichtenspeicher Anbieter oder das Objekt selbst die [IMAPIAdviseSink:: OnNotify](imapiadvisesink-onnotify.md) -Methode für alle ** IMAPIAdviseSink** -Objekte, die für diesen Ereignistyp registriert sind. 
  
Auch wenn der Nachrichtenspeicher Anbieter keine anderen MAPI-Komponenten von Änderungen im Nachrichtenspeicher benachrichtigt, sollte er weiterhin **IMsgStore:: Advise** implementieren, um MAPI_E_NO_SUPPORT zurückzugeben. Dadurch werden andere Komponenten informiert, dass keine Benachrichtigungen vom Nachrichtenspeicher Anbieter erwartet werden. 
  
## <a name="see-also"></a>Siehe auch



[Nachrichtenspeicher-Features](message-store-features.md)

