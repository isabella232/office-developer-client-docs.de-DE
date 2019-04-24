---
title: Unterstützende Ereignisbenachrichtigung
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: a1e3e49c-8d1d-4f7e-ba5a-be441f0f10ae
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 83c102c25b17b6769c0c676bbadd874224f75cf6
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32327426"
---
# <a name="supporting-event-notification"></a>Unterstützende Ereignisbenachrichtigung

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Da unterstützende Ereignisbenachrichtigungen kompliziert sein können, stellt MAPI drei Support Objektmethoden bereit, die die schwierigsten Teile des Prozesses implementieren. Diese Methoden funktionieren als Einheit, und ein Anbieter muss alle drei oder keines davon verwenden.
  
Die MAPI-Unterstützungsmethoden verwenden Benachrichtigungs Schlüssel zum Verwalten der Verbindungen zwischen den Advise-Senken und den Objekten, die die Benachrichtigungen generieren. Ein Benachrichtigungs Schlüssel ist eine [NOTIFKEY](notifkey.md) -Struktur, die Binärdaten enthält, die ein Objekt prozessübergreifend kennzeichnen. Ein Benachrichtigungs Schlüssel wird in der Regel aus der langfristigen Eintrags-ID des Advise-Quellobjekts kopiert. Wenn der Client eine Eintrags-ID im Aufruf von **Advise**bereitgestellt hat, können Sie ihn als Benachrichtigungs Schlüssel verwenden. Wenn der _lpEntryID_ -Parameter, der **Advise** lautet, NULL ist, verwenden Sie die Eintrags-ID des äußerst möglichen Containerobjekts, wie etwa der Nachrichtenspeicher. 
  
Um die Supportmethoden zu verwenden, rufen Sie [IMAPISupport:: subscribe](imapisupport-subscribe.md) immer dann auf, wenn ein Client Ihre **Advise** -Methode aufruft, um sich für eine Benachrichtigung zu registrieren. Reservieren Sie eine [NOTIFKEY](notifkey.md) -Struktur, und erstellen Sie einen eindeutigen Benachrichtigungs Schlüssel für Ihr Advise-Quellobjekt. Ein Nachrichtenspeicher Anbieter, der aufgefordert wird, einen Client zu benachrichtigen, wenn eine Nachricht in einen bestimmten Ordner eingeht, erstellt beispielsweise einen Benachrichtigungs Schlüssel für diesen Ordner. Führen Sie einen Zeiger auf die **NOTIFKEY** -Struktur im Aufruf von **subscribe** zusammen mit einem Zeiger auf die Advise-Senke des Clients. **Subscribe** Ruft die [IUnknown:: AddRef](https://msdn.microsoft.com/library/b4316efd-73d4-4995-b898-8025a316ba63%28Office.15%29.aspx) -Methode der Advise-Senke auf, um den Verweiszähler zu erhöhen, und MAPI behält den Zeiger bei, bis die Registrierung abgebrochen wird. 
  
Sie können das NOTIFY_SYNC-Flag zum **abonnieren** anfordern, dass **Notify** sich synchron verhält und nicht zurückgegeben wird, bis alle Aufrufe an die [IMAPIAdviseSink:: OnNotify](imapiadvisesink-onnotify.md) -Methoden der registrierten Advise-Senken vorgenommen wurden. Legen Sie dieses Flag nur für Ihre eigene interne Verwendung fest. Legen Sie ihn nicht fest, wenn Sie auf einen Client- **Advise** -Anruf reagieren. Ereignisbenachrichtigungen zwischen Clients und Anbietern sind immer asynchron. Das heißt, MAPI stellt sicher, dass der Anruf, bei dem ein Ereignis geschieht, an den Client zurückgegeben **** wird, bevor die OnNotify-Aufrufe ausgeführt werden. 
  
Wenn Sie das NOTIFY_SYNC-Flag festlegen, nehmen Sie keine Änderungen an einem der Advise-Senke-Objekte vor, und führen Sie nicht eine von [HrThisThreadAdviseSink](hrthisthreadadvisesink.md) erstellte Wrapper Advise-Senke zum **abonnieren**aus. **HrThisThreadAdviseSink** erstellt eine threadsichere Version einer Advise-Senke, die nur mit asynchroner Benachrichtigung verwendet werden soll. 
  
Wenn eine für synchrone Benachrichtigung registrierte Advise-Senke aus **OnNotify** mit dem CALLBACK_DISCONTINUE-Flagsatz zurückgegeben wird, legt [IMAPISupport:: notify](imapisupport-notify.md) das NOTIFY_CANCELED-Flag fest und gibt ohne Aufrufe von OnNotify zurück. **** 
  
Nachdem **subscribe** zurückgegeben wurde, müssen Sie Ihre Kopie der Advise-Senke des Kunden nicht mehr aufbewahren. Rufen Sie die [IUnknown:: Release](https://msdn.microsoft.com/library/4b494c6f-f0ee-4c35-ae45-ed956f40dc7a%28Office.15%29.aspx) -Methode auf, um Sie zu veröffentlichen. **Subscribe** gibt eine ungleich NULL-Verbindungsnummer zurück, die Sie an den Client zurückgeben sollten. Die Verbindungsnummer stellt die Verbindung zwischen der Advise-Quelle und der Advise-Senke dar. Sie bleibt gültig, bis der Client einen erfolgreichen Aufruf von **Unadvise**durchführt. 
  
Wenn der Client bereit ist, eine Registrierung abzubrechen, ruft er **** ihre Unadvise-Methode auf. Geben Sie die Verbindungsnummer aus **** dem Unadvise-Aufruf an [IMAPISupport:: unsubscribe](imapisupport-unsubscribe.md). **Unsubscribe** Ruft die **IUnknown:: Release** -Methode der Advise-Senke auf. Wie bei **Advise** und **Unadvise**müssen Aufrufe von **subscribe** und **unsubscribe** gekoppelt werden. Sie müssen für jeden Anruf, der zum **abonnieren**vorgenommen wird, einen Aufruf zum **Abmelden** vornehmen. Sie müssen jedoch nicht jedes Mal, wenn Ihre **Advise** -Methode aufgerufen wird, das **Abonnement** aufrufen. Umgekehrt können Sie es zum Einrichten interner Benachrichtigungen aufrufen. 
  
Wenn ein Ereignis eintritt, weisen Sie eine oder [](notification.md) mehrere Benachrichtigungs Strukturen des für das Ereignis geeigneten Typs zu, und rufen [Sie IMAPISupport:: notify](imapisupport-notify.md)auf. **Notify** generiert eine Benachrichtigung für jede registrierte Advise-Senke. Sie sollten alle nicht verwendeten Member der Benachrichtigungsstruktur [](notification.md) auf NULL festlegen. Diese Technik für die Initialisierung **** der Benachrichtigungsstruktur kann Clients helfen, kleinere, schnellere und weniger fehleranfällige OnNotify-Implementierungen zu erstellen. **** 
  
Beachten Sie, dass **** für jedes Ereignis eine separate Benachrichtigungsstruktur erforderlich ist, auch bei mehreren Ereignissen desselben Typs. Wenn beispielsweise drei Clients für Tabellen Benachrichtigungen für eine bestimmte Tabelle registriert sind und fünf Zeilen zur Tabelle hinzugefügt werden, müssen Sie fünf **OBJECT_NOTIFICATION** -Strukturen für Ihren **Notify** -Aufruf erstellen. Eine Batch Benachrichtigung wie diese führt zu einer besseren Leistung als das fünfmalige Aufrufen von **Notify** . Für jeden **Notify** -Anruf ruft MAPI die [IMAPIAdviseSink:: OnNotify](imapiadvisesink-onnotify.md) -Methode jeder registrierten Advise-Senke auf. Wenn es keine registrierten Advise-Senken gibt, ignoriert MAPI den Anruf. 
  
Dienstanbieter, die Batch Benachrichtigungen senden, müssen Sie so sortieren, dass Sie von der ersten Benachrichtigung bis zum letzten interpretiert werden können. Diese Reihenfolge ist insbesondere dann erforderlich, wenn ein Benachrichtigungsbatch eine Reihe von Ereignissen enthält, beispielsweise TABLE_ROW_ADDED mit einem Ereignis, das auf eine frühere Zeile verweist, die in einem anderen Ereignis im gleichen Batch hinzugefügt wurde.
  
## <a name="see-also"></a>Siehe auch



[MAPI-Dienstanbieter](mapi-service-providers.md)

