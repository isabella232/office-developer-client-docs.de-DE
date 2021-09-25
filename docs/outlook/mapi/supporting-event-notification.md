---
title: Unterstützende Ereignisbenachrichtigung
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.localizationpriority: medium
api_type:
- COM
ms.assetid: a1e3e49c-8d1d-4f7e-ba5a-be441f0f10ae
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 436ebddcf3b6fa9326cc4d3c231d7a94cdefc58a
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59619694"
---
# <a name="supporting-event-notification"></a>Unterstützende Ereignisbenachrichtigung

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Da die Unterstützung von Ereignisbenachrichtigungen kompliziert sein kann, stellt MAPI drei Unterstützungsobjektmethoden bereit, die die kompliziertesten Teile des Prozesses implementieren. Diese Methoden funktionieren als Einheit, und ein Anbieter muss alle drei oder keine davon verwenden.
  
Die MAPI-Unterstützungsmethoden verwenden Benachrichtigungsschlüssel, um die Verbindungen zwischen den Empfehlungssenken und den Objekten zu verwalten, die die Benachrichtigungen generieren. Ein Benachrichtigungsschlüssel ist eine [NOTIFKEY-Struktur,](notifkey.md) die Binärdaten enthält, die ein Objekt prozessübergreifend identifizieren. Ein Benachrichtigungsschlüssel wird in der Regel aus dem langfristigen Eintragsbezeichner des Empfehlungsquellobjekts kopiert. Wenn der Client einen Eintragsbezeichner im Aufruf von **Advise** angegeben hat, können Sie ihn für den Benachrichtigungsschlüssel verwenden. Wenn der  _parameter lpEntryID_ auf **Advise** NULL ist, verwenden Sie den Eintragsbezeichner des äußersten möglichen Containerobjekts, z. B. des Nachrichtenspeichers. 
  
Um die Supportmethoden zu verwenden, rufen [Sie IMAPISupport::Subscribe](imapisupport-subscribe.md) auf, wenn ein Client Ihre **Advise-Methode aufruft,** um sich für eine Benachrichtigung zu registrieren. Weisen Sie eine [NOTIFKEY-Struktur](notifkey.md) zu, und erstellen Sie einen eindeutigen Benachrichtigungsschlüssel für Ihr Empfehlungsquellobjekt. Beispielsweise erstellt ein Nachrichtenspeicheranbieter, der aufgefordert wird, einen Client zu benachrichtigen, wenn eine Nachricht in einem bestimmten Ordner empfangen wird, einen Benachrichtigungsschlüssel für diesen Ordner. Übergeben Sie einen Zeiger an die **NOTIFKEY-Struktur** im **Subscribe-Aufruf** zusammen mit einem Zeiger auf die Empfehlungssenke des Clients. **Subscribe** calls the advise sink's [IUnknown::AddRef](https://msdn.microsoft.com/library/b4316efd-73d4-4995-b898-8025a316ba63%28Office.15%29.aspx) method to increment its reference count and MAPI retains the pointer until the registration is canceled. 
  
Sie können das flag NOTIFY_SYNC an **Subscribe** übergeben, um anzufordern, dass **"Notify"** sich synchron verhält und erst zurückgegeben wird, wenn alle Aufrufe der [IMAPIAdviseSink::OnNotify-Methoden](imapiadvisesink-onnotify.md) registrierter Empfehlungssenken ausgeführt wurden. Legen Sie dieses Kennzeichen nur für Ihre eigene interne Verwendung fest. Legen Sie ihn nicht fest, wenn Sie auf einen **Client-Empfehlungsaufruf** antworten. Ereignisbenachrichtigungen zwischen Clients und Anbietern sind immer asynchron. Das heißt, die MAPI stellt sicher, dass der Anruf, während dem ein Ereignis stattfindet, an den Client zurückgibt, bevor die **OnNotify-Aufrufe** getätigt werden. 
  
Wenn Sie das flag NOTIFY_SYNC festlegen, nehmen Sie keine Änderungen an einem der Advise-Senkenobjekte vor und übergeben Sie keine wrapper-Empfehlungssenke, die von [HrThisThreadAdviseSink](hrthisthreadadvisesink.md) zum **Abonnieren** erstellt wurde. **HrThisThreadAdviseSink** erstellt eine threadsichere Version einer Empfehlungssenke, die nur mit asynchroner Benachrichtigung verwendet werden soll. 
  
Wenn eine für synchrone Benachrichtigung registrierte Empfehlungssenke von **OnNotify** mit dem festgelegten CALLBACK_DISCONTINUE Flag zurückgegeben wird, legt [IMAPISupport::Notify](imapisupport-notify.md) das NOTIFY_CANCELED Flag fest und gibt es zurück, ohne **OnNotify** auf den Namen zu verweisen. 
  
Nachdem **Subscribe** zurückgegeben wurde, müssen Sie ihre Kopie der Empfehlungssenke des Clients nicht mehr aufbewahren. Rufen Sie die [IUnknown::Release-Methode](https://msdn.microsoft.com/library/4b494c6f-f0ee-4c35-ae45-ed956f40dc7a%28Office.15%29.aspx) auf, um sie freizugeben. **Subscribe** gibt eine Nonzero-Verbindungsnummer zurück, die Sie an den Client zurückgeben sollten. Die Verbindungsnummer stellt die Verknüpfung zwischen der Empfehlungsquelle und der Empfehlungssenke dar. Sie bleibt gültig, bis der Client **unadvise erfolgreich aufruft.** 
  
Wenn der Client bereit ist, eine Registrierung abzubrechen, wird ihre **Unadvise-Methode** aufgerufen. Übergeben Sie die Verbindungsnummer aus dem **Unadvise-Aufruf** an [IMAPISupport::Unsubscribe](imapisupport-unsubscribe.md). **Unsubscribe** calls the advise sink's **IUnknown::Release** method. Wie **bei "Rat"** und **"Unadvise"** müssen Aufrufe zum **Abonnieren** und **Kündigen** gekoppelt werden. Sie müssen einen Aufruf zum **Kündigen des Abonnements** für jeden Anruf tätigen, der zum **Abonnieren** getätigt wird. Sie müssen **Subscribe** jedoch nicht jedes Mal aufrufen, wenn Ihre **Advise-Methode** aufgerufen wird. Im Gegensatz dazu können Sie sie zum Einrichten interner Benachrichtigungen aufrufen. 
  
Wenn ein Ereignis auftritt, weisen Sie eine oder mehrere [NOTIFICATION-Strukturen](notification.md) des für das Ereignis geeigneten Typs zu, und rufen Sie [IMAPISupport::Notify](imapisupport-notify.md)auf. **Notify** generiert eine Benachrichtigung für jede registrierte Empfehlungssenke. Sie sollten alle nicht verwendeten Elemente der [NOTIFICATION-Struktur](notification.md) auf Null festlegen. Diese Technik zum Initialisieren der **NOTIFICATION-Struktur** kann Clients dabei helfen, kleinere, schnellere und weniger fehleranfällige **OnNotify-Implementierungen** zu erstellen. 
  
Beachten Sie, dass für jedes Ereignis eine separate **NOTIFICATION-Struktur** erforderlich ist, auch für mehrere Ereignisse desselben Typs. Wenn beispielsweise drei Clients für tabellenbenachrichtigungen in einer bestimmten Tabelle registriert sind und fünf Zeilen zur Tabelle hinzugefügt werden, müssen Sie fünf **OBJECT_NOTIFICATION** Strukturen für Ihren **Notify-Aufruf** erstellen. Eine solche Batchbenachrichtigung führt zu einer besseren Leistung als das fünffache Aufrufen von **"Benachrichtigen".** Für jeden **Notify-Aufruf** ruft MAPI die [IMAPIAdviseSink::OnNotify-Methode](imapiadvisesink-onnotify.md) jeder registrierten Empfehlungssenke auf. Wenn keine registrierten Empfehlungssenken vorhanden sind, ignoriert MAPI den Aufruf. 
  
Dienstanbieter, die Benachrichtigungen im Batch senden, müssen sie so anordnen, dass sie von der ersten Benachrichtigung bis zur letzten interpretiert werden können. Diese Sortierung ist besonders erforderlich, wenn ein Benachrichtigungsbatch eine Reihe von Ereignissen enthält, z. B. TABLE_ROW_ADDED mit einem Ereignis, das auf eine vorherige Zeile verweist, die in einem anderen Ereignis im gleichen Batch hinzugefügt wurde.
  
## <a name="see-also"></a>Siehe auch



[MAPI-Dienstanbieter](mapi-service-providers.md)

