---
title: Unterstützen von Ereignisbenachrichtigungen
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: a1e3e49c-8d1d-4f7e-ba5a-be441f0f10ae
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 83c102c25b17b6769c0c676bbadd874224f75cf6
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/04/2018
ms.locfileid: "25397142"
---
# <a name="supporting-event-notification"></a>Unterstützen von Ereignisbenachrichtigungen

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Da Unterstützung ereignisbenachrichtigung kompliziert sein kann, bietet MAPI drei Support-Objekt-Methoden, mit die die schwierigsten Teile des Prozesses implementiert. Diese Methoden funktionieren als Einheit und ein Anbieter muss alle drei oder keines der Projekte verwenden.
  
Die MAPI-Support-Methoden verwenden Benachrichtigung Schlüssel zum Verwalten der Verbindungen zwischen der Advise-senken und die Objekte, die die Benachrichtigungen generieren. Ein Benachrichtigung Schlüssel ist eine [NOTIFKEY](notifkey.md) -Struktur, die binäre Daten enthält, die ein Objekt über Prozesse identifiziert. Ein Benachrichtigung Schlüssel wird in der Regel aus der langfristige Eintrags-ID des Quellobjekts Advise kopiert. Wenn der Client einen Eintrag Bezeichner im Aufruf **Advise**bereitgestellt hat, können Sie es für die Benachrichtigung-Taste. Wenn der Parameter _LpEntryID_ **Advise** NULL ist, verwenden Sie die Eintrags-ID des äußersten möglichen Container-Objekts, wie die Nachrichtenspeicher. 
  
Um die von Unterstützungsmethoden verwenden, rufen Sie [IMAPISupport::Subscribe](imapisupport-subscribe.md) , wenn ein Client für eine Benachrichtigung registrieren Ihrer **Advise** -Methode aufruft. Ordnen Sie eine Struktur [NOTIFKEY zu](notifkey.md) , und erstellen Sie einen eindeutigen Benachrichtigung Product Key für Ihre Advise-Source-Objekt. Eine Nachricht Speicheranbieter, die aufgefordert wird, einen Client benachrichtigen, wenn eine Nachricht empfangen wird in einen bestimmten Ordner erstellt beispielsweise einen Benachrichtigung Schlüssel für diesen Ordner. Übergeben Sie einen Zeiger auf die Struktur **NOTIFKEY** im Aufruf **Subscribe** sowie einen Zeiger auf des Clients advise-Empfänger. **Subscribe** ruft Advise-Empfänger [IUnknown:: AddRef](https://msdn.microsoft.com/library/b4316efd-73d4-4995-b898-8025a316ba63%28Office.15%29.aspx) -Methode, um die Anzahl der Verweise zu erhöhen und MAPI behält den Zeiger, bis die Registrierung abgebrochen wird. 
  
Können Sie die Kennzeichen NOTIFY_SYNC an übergeben **Subscribe** anfordern, dass **Benachrichtigen** Verhalten synchron und nicht zurückgegeben, bis sie alle Aufrufe der Methoden [IMAPIAdviseSink::OnNotify](imapiadvisesink-onnotify.md) vorgenommen hat registriert advise-Empfänger. Legen Sie dieses Flag nur für die interne Verwendung. Legen Sie sie nicht, wenn Sie einen Client **Advise** -Anruf beantworten. Benachrichtigung bei zwischen Clients und Anbieter ist immer asynchron. MAPI garantiert, dass das heißt, den Anruf, in dem ein Ereignis eintritt an den Client zurückgegeben werden, bevor einer der Aufrufe **OnNotify** vorgenommen werden. 
  
Wenn Sie das NOTIFY_SYNC-Flag festlegen, nehmen Sie keine Änderungen nicht auf eines der Empfängerobjekten anweisen, und übergeben Sie einen Wrapper Advise-Empfänger erstelltes [HrThisThreadAdviseSink](hrthisthreadadvisesink.md) **Abonnieren**nicht. **HrThisThreadAdviseSink** erstellt eine threadsicheren Version einer Advise-Empfänger mit asynchrone Benachrichtigung nur verwendet werden. 
  
Wenn ein Advise-Empfänger, die für die synchrone Benachrichtigung registriert **OnNotify** mit CALLBACK_DISCONTINUE Flag zurückgibt, [IMAPISupport::Notify](imapisupport-notify.md) legt das Flag NOTIFY_CANCELED und ohne Aufrufe von **OnNotify**zurückgegeben. 
  
Nachdem **Subscribe** zurückgegeben wurde, wird nicht mehr muss alle Ihre Kopie des Clients advise-Empfänger. Rufen Sie dessen [IUnknown](https://msdn.microsoft.com/library/4b494c6f-f0ee-4c35-ae45-ed956f40dc7a%28Office.15%29.aspx) -Methode, um es zu lösen. **Subscribe** gibt eine Verbindung ungleich NULL zurück, die an den Client zurückgegeben werden soll. Die Nummer stellt die Verknüpfung zwischen der Advise-Quelle und der Advise-Empfänger. Es bleibt gültig, bis der Client erfolgreich **Unadvise**aufruft. 
  
Wenn der Client eine Registrierung Abbrechen bereit ist, ruft es Ihre **Unadvise** -Methode. Übergeben Sie die Nummer aus dem Aufruf **Unadvise** [IMAPISupport::Unsubscribe](imapisupport-unsubscribe.md). Der Advise-Empfänger **IUnknown** -Methode aufgerufen, **zum Abmelden** . Wie bei **Advise** und **Unadvise**müssen Aufrufe von **Abonnieren** und **kündigen** kombiniert werden. Sie müssen durch Aufrufen von **zum Abmelden** für jeden Aufruf vornehmen, die mit **Subscribe**hergestellt wird. Sie müssen jedoch keinen **Subscribe** rufen Sie jedes Mal, wenn die **Advise** -Methode aufgerufen wird. Im Gegensatz dazu können Sie es für das Einrichten von internen Benachrichtigungen aufrufen. 
  
Wenn ein Ereignis eintritt, reservieren Sie eine oder mehrere [Benachrichtigung](notification.md) Strukturen vom Typ für das Ereignis, und rufen Sie [IMAPISupport::Notify](imapisupport-notify.md). **Benachrichtigen** generiert eine Benachrichtigung für jeden registrierten Advise-Empfänger. Sie sollten alle nicht verwendeten Mitglieder der [Benachrichtigung](notification.md) Struktur auf NULL festgelegt. Dieses Verfahren für die Initialisierung der **Benachrichtigung** Struktur hilft Clients kleiner, schneller und weniger fehleranfällig **OnNotify** Implementierungen zu erstellen. 
  
Beachten Sie, dass eine separate **Benachrichtigung** Struktur für jedes Ereignis, auch für mehrere Ereignisse des gleichen Typs erforderlich ist. Beispielsweise müssen drei Clients für die Tabelle Benachrichtigung für eine bestimmte Tabelle registriert sind, und fünf Zeilen der Tabelle hinzugefügt werden, Sie fünf **OBJECT_NOTIFICATION** Strukturen für Ihren Anruf **Benachrichtigen** erstellen. Eine Benachrichtigung Batch wie dies führt eine bessere Leistung als **Benachrichtigen** fünfmaliges aufrufen. Für jeden Anruf **Benachrichtigen** ruft MAPI die [IMAPIAdviseSink::OnNotify](imapiadvisesink-onnotify.md) -Methode des alle registrierten Advise-Empfänger. Wenn vorhanden sind keine registrierten advise-Empfänger, MAPI ignoriert den Anruf. 
  
Dienstanbieter, die im Batchmodus Benachrichtigungen senden müssen sie bestellen, damit sie auf die letzte aus der ersten Benachrichtigung interpretiert werden können. Diese Reihenfolge ist insbesondere dann erforderlich, wenn ein Batches für die Benachrichtigung über eine Reihe von Ereignissen, wie etwa TABLE_ROW_ADDED mit einem Ereignis enthält, das auf eine vorherige Zeile verweist, die in einem anderen Ereignis in einem Batch hinzugefügt wurde.
  
## <a name="see-also"></a>Siehe auch



[MAPI-Dienstanbieter](mapi-service-providers.md)

