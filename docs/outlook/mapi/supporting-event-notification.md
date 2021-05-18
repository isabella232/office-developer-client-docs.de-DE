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
  
Da die Unterstützung der Ereignisbenachrichtigung kompliziert sein kann, stellt MAPI drei Unterstützungsobjektmethoden zur Verfügung, die die schwierigsten Teile des Prozesses implementieren. Diese Methoden funktionieren als Einheit, und ein Anbieter muss alle drei oder keine davon verwenden.
  
Die MAPI-Supportmethoden verwenden Benachrichtigungsschlüssel, um die Verbindungen zwischen den Ratensenken und den Objekten zu verwalten, die die Benachrichtigungen generieren. Ein Benachrichtigungsschlüssel ist eine [NOTIFKEY-Struktur,](notifkey.md) die Binärdaten enthält, die ein Objekt prozessübergreifend identifizieren. Ein Benachrichtigungsschlüssel wird in der Regel aus der langfristigen Eintrags-ID des advise-Quellobjekts kopiert. Wenn der Client einen Eintragsbezeichner im Aufruf von **"Advise"** angegeben hat, können Sie ihn für den Benachrichtigungsschlüssel verwenden. Wenn der _zu empfehlende lpEntryID-Parameter_ NULL ist, verwenden Sie die Eintrags-ID des äußerst möglichen Containerobjekts, z. B. des Nachrichtenspeichers.  
  
Um die Supportmethoden zu verwenden, rufen Sie [IMAPISupport::Subscribe](imapisupport-subscribe.md) auf, wenn ein Client Ihre **Advise-Methode** aufruft, um sich für eine Benachrichtigung zu registrieren. Weisen Sie eine [NOTIFKEY-Struktur](notifkey.md) zu, und erstellen Sie einen eindeutigen Benachrichtigungsschlüssel für Ihr Advise-Quellobjekt. Beispielsweise erstellt ein Nachrichtenspeicheranbieter, der aufgefordert wird, einen Client zu benachrichtigen, wenn eine Nachricht in einem bestimmten Ordner empfangen wird, einen Benachrichtigungsschlüssel für diesen Ordner. Übergeben Sie einen Zeiger auf die **NOTIFKEY-Struktur** im Aufruf von **Subscribe** zusammen mit einem Zeiger auf die Ratensenke des Clients. **Subscribe** ruft die [IUnknown::AddRef-Methode](https://msdn.microsoft.com/library/b4316efd-73d4-4995-b898-8025a316ba63%28Office.15%29.aspx) der Hinweissenke auf, um die Referenzanzahl zu erhöhen, und MAPI behält den Zeiger bei, bis die Registrierung abgebrochen wird. 
  
Sie können das NOTIFY_SYNC-Flag an **Subscribe** übergeben, um an die Anforderung zu senden, dass **Notify** synchron verhält, und erst dann zurückgeben, wenn alle Aufrufe der [IMAPIAdviseSink::OnNotify-Methoden](imapiadvisesink-onnotify.md) registrierter Hinweissenken ausgeführt wurden. Legen Sie dieses Flag nur für Ihre eigene interne Verwendung ein. Legen Sie sie nicht auf, wenn Sie auf einen Kundenanruf **mit Raten** antworten. Die Ereignisbenachrichtigung zwischen Clients und Anbietern ist immer asynchron. Das heißt, MAPI garantiert, dass der Aufruf, während dem ein Ereignis eintritt, an den Client zurückzukehren, bevor die **OnNotify-Aufrufe** ausgeführt werden. 
  
Wenn Sie das NOTIFY_SYNC-Flag festlegen, nehmen Sie keine Änderungen an den Objekten der advise sink vor, und übergeben Sie keine wrapper -Hinweissenke, die von [HrThisThreadAdviseSink](hrthisthreadadvisesink.md) für **Subscribe** erstellt wurde. **HrThisThreadAdviseSink** erstellt eine threadsichere Version einer Ratensenke, die nur mit asynchroner Benachrichtigung verwendet werden soll. 
  
Wenn eine für synchrone Benachrichtigungen registrierte Hinweissenke von **OnNotify** mit dem CALLBACK_DISCONTINUE-Flagsatz zurückgibt, legt [IMAPISupport::Notify](imapisupport-notify.md) das flag NOTIFY_CANCELED fest und gibt zurück, ohne **OnNotify** zu aufrufen. 
  
Nachdem **Subscribe** zurückgegeben wurde, müssen Sie ihre Kopie der Kunden-Ratensenke nicht mehr halten. Rufen Sie die [IUnknown::Release-Methode auf, um](https://msdn.microsoft.com/library/4b494c6f-f0ee-4c35-ae45-ed956f40dc7a%28Office.15%29.aspx) sie frei zu geben. **Subscribe** gibt eine Verbindungsnummer ungleich Null zurück, die Sie an den Client zurückgeben sollten. Die Verbindungsnummer stellt den Link zwischen der Quelle "Advise" und der "Advise"-Senke dar. Er bleibt gültig, bis der Client **unadvise erfolgreich aufruft.** 
  
Wenn der Client bereit ist, eine Registrierung abbricht, ruft er Ihre **Unadvise-Methode** auf. Übergeben Sie die Verbindungsnummer aus dem **Unadvise-Aufruf** an [IMAPISupport::Unsubscribe](imapisupport-unsubscribe.md). **Unsubscribe** ruft die **IUnknown::Release-Methode der** Ratensenke auf. Wie bei **Advise** und **Unadvise** müssen Anrufe zum **Abonnieren** und **Abmelden** gekoppelt werden. Sie müssen für jeden **Anruf,** der zum Abonnieren erfolgt, einen Aufruf zum Abmelden **von machen.** Sie müssen jedoch nicht jedes Mal **Abonnieren** aufrufen, wenn Ihre **Advise-Methode** aufgerufen wird. Umgekehrt können Sie es zum Einrichten interner Benachrichtigungen aufrufen. 
  
Wenn ein Ereignis auftritt, weisen Sie mindestens eine [BENACHRICHTIGUNGsstruktur](notification.md) des für das Ereignis geeigneten Typs zu, und rufen [Sie IMAPISupport::Notify auf.](imapisupport-notify.md) **Notify** generiert eine Benachrichtigung für jede registrierte Hinweissenke. Sie sollten alle nicht verwendeten Elemente der [NOTIFICATION-Struktur](notification.md) auf Null festlegen. Diese Technik zum Initialisieren der **NOTIFICATION-Struktur** kann Clients dabei helfen, kleinere, schnellere und weniger fehleranfällige **OnNotify-Implementierungen zu** erstellen. 
  
Beachten **Sie,** dass für jedes Ereignis eine separate NOTIFICATION-Struktur erforderlich ist, auch für mehrere Ereignisse desselben Typs. Wenn beispielsweise drei Clients für tabellenbenachrichtigungen in einer bestimmten Tabelle registriert sind und  der Tabelle fünf Zeilen hinzugefügt werden, müssen Sie fünf OBJECT_NOTIFICATION für Ihren Notify-Aufruf **erstellen.** Eine Batchbenachrichtigung wie diese führt zu einer besseren Leistung als das Fünffache des Aufrufs **von Notify.** Für jeden **Notify-Aufruf** ruft MAPI die [IMAPIAdviseSink::OnNotify-Methode](imapiadvisesink-onnotify.md) jeder registrierten Ratensenke auf. Wenn es keine registrierten Ratensenken gibt, ignoriert MAPI den Anruf. 
  
Dienstanbieter, die Batchbenachrichtigungen senden, müssen diese so bestellen, dass sie von der ersten bis zur letzten Benachrichtigung interpretiert werden können. Diese Reihenfolge ist besonders erforderlich, wenn ein Benachrichtigungsbatch eine Reihe von Ereignissen enthält, z. B. TABLE_ROW_ADDED mit einem Ereignis, das auf eine vorherige Zeile verweist, die in einem anderen Ereignis im gleichen Batch hinzugefügt wurde.
  
## <a name="see-also"></a>Siehe auch



[MAPI-Dienstanbieter](mapi-service-providers.md)

