---
title: Ereignisbenachrichtigung in MAPI
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 7b3b625b-6dea-4b12-99a9-152935bdfe39
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 30d4ad5e0fc1ecdc4c8eb06f75d39e38dd481269
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32321396"
---
# <a name="event-notification-in-mapi"></a>Ereignisbenachrichtigung in MAPI

**Gilt für**: Outlook 2013 | Outlook 2016 
  
Ereignisbenachrichtigung ist die Kommunikation von Informationen zwischen zwei MAPI-Objekten. Über eines der Objekte registriert sich ein Client oder Dienstanbieter für die Benachrichtigung über eine Änderung oder einen Fehler, das als Ereignis bezeichnet wird, das im anderen Objekt stattfinden kann. Nach dem Eintreten des Ereignisses wird das erste Objekt über die Änderung oder den Fehler benachrichtigt. Das Objekt, das die Benachrichtigung empfängt, wird als Ratensenke bezeichnet. das für die Benachrichtigung zuständige Objekt wird als Quelle für den Hinweis bezeichnet.
  
Es gibt drei Arten von Empfehlungssenkenobjekten (alle Typen sind standardmäßige MAPI-Objekte):
  
- Raten Sie sink-Objekten.   
- Form advise sink objects.  
- Anzeigen von Ratensenkenobjekten.
    
Advise sink objects are the most common type. Hinweiseken werden in der Regel von Clientanwendungen implementiert, um Adressbuch- und Nachrichtenspeicherbenachrichtigungen zu empfangen und die [IMAPIAdviseSink : IUnknown-Schnittstelle zu](imapiadvisesinkiunknown.md) unterstützen. **IMAPIAdviseSink** enthält eine einzelne Methode, [IMAPIAdviseSink::OnNotify](imapiadvisesink-onnotify.md). Formular- und Ansichtssenken sind seltener. sie werden implementiert, um Benachrichtigungen über Änderungen an benutzerdefinierten Formularen zu erhalten. Formularsenken unterstützen die [IMAPIFormAdviseSink : IUnknown-Schnittstelle](imapiformadvisesinkiunknown.md) und Ansichtssenken unterstützen die [IMAPIViewAdviseSink : IUnknown-Schnittstelle.](imapiviewadvisesinkiunknown.md) Da die meisten Clients standardmäßige Advise Sink-Objekte implementieren, gehen Sie davon aus, dass diskussionen von Benachrichtigungen sich auf Adressbuch- und Nachrichtenspeicherbenachrichtigungen beziehen, anstatt formularbenachrichtigungen. Weitere Informationen zu Formularbenachrichtigungen finden Sie unter [MAPI Forms Notifications](mapi-forms-notifications.md) and [Writing Form Server Code](writing-form-server-code.md).
  
Advise-Quellobjekte werden von Dienstanbietern und von MAPI implementiert. Nicht alle Dienstanbieter unterstützen Ereignisbenachrichtigungen. er ist optional, wird jedoch dringend empfohlen. Nachrichtenspeicher- und Adressbuchanbieter unterstützen in der Regel Objektbenachrichtigungen für mehrere objekte und Tabellenbenachrichtigungen in ihren Inhalten und Hierarchietabellen. Transportanbieter unterstützen Benachrichtigungen nicht direkt; sie sind auf alternative Kommunikationsmethoden mit Clients angewiesen.
  
Im Gegensatz zu Denksen sind Ratenquellenobjekte kein eindeutiger Typ von MAPI-Objekten. Viele MAPI-Objekte, z. B. Nachrichtenspeicher und Tabellen, können die Rolle der Informationsquelle übernehmen. Eine Advise-Quelle ist ein beliebiges MAPI-Objekt, das Folgendes vor sich hat:
  
- Implementiert eine **Advise-Methode** zum Empfangen von Benachrichtigungsregistrierungen. 
    
- Implementiert eine **Unadvise-Methode** zum Empfangen von Benachrichtigungsabsagen. 
    
- Generiert Benachrichtigungen des entsprechenden Typs an die entsprechenden Ratensenkenobjekte, die durch Aufrufen ihrer **IMAPIAdviseSink::OnNotify-Methoden registriert** wurden. 
    
Clients, die Beratende Sink-Objekte implementieren, rufen **Raten** auf, wenn sie sich für eine Benachrichtigung registrieren möchten, in den meisten Fällen die Eintrags-ID des Objekts übergeben, mit dem die Registrierung erfolgen soll, und **unadvise,** wenn sie die Registrierung abbrechen möchten. Clients übergeben einen Parameter an **Advise,** der angibt, welche der verschiedenen Ereignistypen überwacht werden sollen. **Advise** gibt eine Zahl ungleich Null zurück, die eine erfolgreiche Verbindung zwischen der Ratensenke und der Ratenquelle darstellt. 
  
Vor dem Aufrufen von **Advise** können Clients ermitteln, ob ein Nachrichtenspeicheranbieter eine Benachrichtigung unterstützt, indem sie überprüfen, ob das STORE_NOTIFY_OK-Flag in der **PR_STORE_SUPPORT_MASK** ([PidTagStoreSupportMask](pidtagstoresupportmask-canonical-property.md))-Eigenschaft des Nachrichtenspeichers festgelegt ist. Clients können nicht im Voraus bestimmen, ob ein Adressbuchanbieter Benachrichtigungen unterstützt. Clients müssen versuchen, sich zu registrieren, und wenn der Versuch fehlschlägt, können sie davon ausgehen, dass Benachrichtigungen nicht unterstützt werden.
  
Wenn ein Ereignis auftritt, für das ein Client registriert wurde, benachrichtigt die Advise-Quelle die Ratensenke, indem sie die [IMAPIAdviseSink::OnNotify-Methode](imapiadvisesink-onnotify.md) mit einer Benachrichtigungsdatenstruktur aufruft, die Informationen über das Ereignis enthält. Die Implementierung von **OnNotify** durch eine Ratensenke kann Aufgaben als Reaktion auf die Benachrichtigung ausführen, z. B. das Aktualisieren von Daten im Arbeitsspeicher oder das Aktualisieren einer Bildschirmanzeige. 
  
Dienstanbieter können die Unterstützung für Benachrichtigungen manuell implementieren oder die Hilfe in drei **IMAPISupport-Methoden** nutzen: [IMAPISupport::Subscribe](imapisupport-subscribe.md), [IMAPISupport::Unsubscribe](imapisupport-unsubscribe.md)und [IMAPISupport::Notify](imapisupport-notify.md). Die **Methoden Subscribe** und **Unsubscribe** behandeln die Registrierung und Deregistrierung von Benachrichtigungen für Anbieter. Die **Notify-Methode** verarbeitet gegebenenfalls das Senden von Benachrichtigungen. 
  
Um die Methoden des Supportobjekts für die Benachrichtigungsregistrierung zu verwenden, rufen Dienstanbieter [IMAPISupport::Subscribe](imapisupport-subscribe.md) in ihren **Advise-Methoden** auf, und übergeben sie an **Subscribe** the advise sink pointer that clients pass to **Advise**. Wenn ein Eintragsbezeichner als Eingabeparameter übergeben wird, um eine Ratgeberquelle anzugeben, konvertieren Dienstanbieter ihn in einen Binärschlüssel. **Subscribe** erstellt eine eindeutige Verbindungsnummer, und es ist diese Nummer, die Dienstanbieter an Clients zurückgeben. Dienstanbieter können den Hinweis-Sink-Objektzeiger des Clients jederzeit nach Abschluss des **Advise-Aufrufs** los. 
  
Wenn Clients **Unadvise** aufrufen, um eine Registrierung abgesagt zu haben, dekrementieren Dienstanbieter entweder die Referenzanzahl für den Hinweissenkenzeiger des Clients, oder rufen **Abbestellen** auf, um dies zu tun. 
  
Wenn es an der Zeit ist, eine Benachrichtigung zu generieren, führen Dienstanbieter eine interne Verarbeitung im Zusammenhang mit der Benachrichtigung durch und initialisieren eine [BENACHRICHTIGUNGsstruktur,](notification.md) indem sie alle nicht verwendeten Member auf Null festlegen. Diese Technik zum Initialisieren der **NOTIFICATION-Struktur** kann Clients dabei helfen, kleinere, schnellere und weniger fehleranfällige **OnNotify-Implementierungen zu** erstellen. 
  
Die folgende Abbildung zeigt die Kommunikation zwischen Ratensenkenobjekten, Beraten von Quellobjekten und MAPI. MAPI ist nur beteiligt, wenn die Quelle "Advise" die **IMAPISupport-Methoden zur** Unterstützung von Benachrichtigungen aufruft. 
  
**Ereignisbenachrichtigungsaufrufe**
  
![Ereignisbenachrichtigungsaufrufe](media/amapi_51.gif "Ereignisbenachrichtigungsaufrufe")
  
Die MFCMAPI **CAdviseSink-Klasse** (unter Verwendung der Dateien AdviseSink.h und AdviseSink.cpp) implementiert das Advise Sink-Objekt für alle Aufrufe von **Advise**. Weitere Informationen zu MFCMAPI finden Sie unter [MFCMAPI als Codebeispiel](mfcmapi-as-a-code-sample.md) und [MFCMAPI](https://go.microsoft.com/fwlink/?LinkId=124154).
  

