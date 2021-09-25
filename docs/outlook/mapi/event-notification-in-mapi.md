---
title: Ereignisbenachrichtigung in MAPI
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.localizationpriority: medium
api_type:
- COM
ms.assetid: 7b3b625b-6dea-4b12-99a9-152935bdfe39
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 64605539d04dcbec1eee53ff6d508d1cf5599b08
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59576310"
---
# <a name="event-notification-in-mapi"></a>Ereignisbenachrichtigung in MAPI

**Gilt für**: Outlook 2013 | Outlook 2016 
  
Ereignisbenachrichtigung ist die Kommunikation von Informationen zwischen zwei MAPI-Objekten. Über eines der Objekte registriert sich ein Client oder Dienstanbieter zur Benachrichtigung über eine Änderung oder einen Fehler, die als Ereignis bezeichnet wird, das im anderen Objekt stattfinden kann. Nachdem das Ereignis aufgetreten ist, wird das erste Objekt über die Änderung oder den Fehler benachrichtigt. Das Objekt, das die Benachrichtigung empfängt, wird als Empfehlungssenke bezeichnet. Das für die Benachrichtigung zuständige Objekt wird als Empfehlungsquelle bezeichnet.
  
Es gibt drei Arten von Empfehlungssenkenobjekten (alle Typen sind standardmäßige MAPI-Objekte):
  
- Empfehlen Sie Senkenobjekte.   
- Form advise sink objects.  
- Anzeigen von Empfohlenen Senkenobjekten.
    
Empfehlen Sie Senkenobjekten den am häufigsten verwendeten Typ. Empfehlungssenken werden in der Regel von Clientanwendungen implementiert, um Adressbuch- und Nachrichtenspeicherbenachrichtigungen zu empfangen und die [IMAPIAdviseSink : IUnknown-Schnittstelle](imapiadvisesinkiunknown.md) zu unterstützen. **IMAPIAdviseSink** enthält eine einzelne Methode, [IMAPIAdviseSink::OnNotify](imapiadvisesink-onnotify.md). Formular- und Ansichts-Empfehlungssenken sind weniger häufig; sie werden implementiert, um Benachrichtigungen über Änderungen an benutzerdefinierten Formularen zu erhalten. Formular-Empfehlungssenken unterstützen die [IMAPIFormAdviseSink : IUnknown-Schnittstelle](imapiformadvisesinkiunknown.md) und Ansichts-Empfehlungssenken unterstützen die [IMAPIViewAdviseSink : IUnknown-Schnittstelle.](imapiviewadvisesinkiunknown.md) Da die meisten Clients standardmäßige Empfehlungssenkenobjekte implementieren, wird davon ausgegangen, dass Benachrichtigungen im Zusammenhang mit Adressbuch- und Nachrichtenspeicherbenachrichtigungen statt mit Formularbenachrichtigungen stehen. Weitere Informationen zu Formularbenachrichtigungen finden Sie unter [MAPI Forms Notifications](mapi-forms-notifications.md) and [Writing Form Server Code](writing-form-server-code.md).
  
Empfehlungsquellobjekte werden von Dienstanbietern und mapi implementiert. Nicht alle Dienstanbieter unterstützen Ereignisbenachrichtigungen; es ist optional, wird jedoch dringend empfohlen. Nachrichtenspeicher- und Adressbuchanbieter unterstützen in der Regel Objektbenachrichtigungen für mehrere ihrer Objekte und Tabellenbenachrichtigungen in ihren Inhalten und Hierarchietabellen. Transportanbieter unterstützen Benachrichtigungen nicht direkt; Sie basieren auf alternativen Methoden für die Kommunikation mit Clients.
  
Im Gegensatz zu Empfehlungssenken sind Empfehlungsquellobjekte kein eindeutiger MAPI-Objekttyp. Viele MAPI-Objekte, z. B. Nachrichtenspeicher und Tabellen, können die Rolle der Empfehlungsquelle übernehmen. Eine Empfehlungsquelle ist jedes MAPI-Objekt, das Folgendes ausführt:
  
- Implementiert eine **Advise-Methode** zum Empfangen von Benachrichtigungsregistrierungen. 
    
- Implementiert eine **Unadvise-Methode** zum Empfangen von Benachrichtigungsabsagen. 
    
- Generiert Benachrichtigungen des entsprechenden Typs an die entsprechenden Empfohlenen Senkenobjekte, die registriert wurden, indem ihre **IMAPIAdviseSink::OnNotify-Methoden** aufgerufen werden. 
    
Clients, die Empfehlungssenkenobjekte implementieren, rufen **"Advise"** auf, wenn sie sich für eine Benachrichtigung registrieren möchten. In den meisten Fällen wird der Eintragsbezeichner des Objekts übergeben, mit dem die Registrierung durchgeführt werden soll, und **"Unadvise",** wenn sie die Registrierung abbrechen möchten. Clients übergeben einen Parameter an **Advise,** der angibt, welche der verschiedenen Ereignistypen sie überwachen möchten. **Advise** gibt eine Non-Zero-Nummer zurück, die eine erfolgreiche Verbindung zwischen der Empfehlungssenke und der Empfehlungsquelle darstellt. 
  
Vor dem Aufrufen von **Advise** können Clients ermitteln, ob ein Nachrichtenspeicheranbieter Benachrichtigungen unterstützt, indem sie überprüfen, ob das flag STORE_NOTIFY_OK in der **Eigenschaft PR_STORE_SUPPORT_MASK** ([PidTagStoreSupportMask](pidtagstoresupportmask-canonical-property.md)) des Nachrichtenspeichers festgelegt ist. Clients können nicht im Voraus bestimmen, ob ein Adressbuchanbieter Benachrichtigungen unterstützt. Clients müssen versuchen, sich zu registrieren, und wenn der Versuch fehlschlägt, können sie davon ausgehen, dass Benachrichtigungen nicht unterstützt werden.
  
Wenn ein Ereignis auftritt, für das ein Client registriert wurde, benachrichtigt die Empfehlungsquelle die Empfehlungssenke, indem sie die [IMAPIAdviseSink::OnNotify-Methode](imapiadvisesink-onnotify.md) mit einer Benachrichtigungsdatenstruktur aufruft, die Informationen über das Ereignis enthält. Die Implementierung von **OnNotify** durch eine Empfehlungssenke kann Aufgaben als Reaktion auf die Benachrichtigung ausführen, z. B. das Aktualisieren von Daten im Arbeitsspeicher oder das Aktualisieren einer Bildschirmanzeige. 
  
Dienstanbieter können die Unterstützung für Benachrichtigungen manuell implementieren oder die Hilfe in drei **IMAPISupport-Methoden** nutzen: [IMAPISupport::Subscribe](imapisupport-subscribe.md), [IMAPISupport::Unsubscribe](imapisupport-unsubscribe.md)und [IMAPISupport::Notify](imapisupport-notify.md). Die **Subscribe-** und **Unsubscribe-Methoden** behandeln die Benachrichtigungsregistrierung und -aufhebung für Anbieter; Die **Notify-Methode** verarbeitet das Senden von Benachrichtigungen, falls zutreffend. 
  
Um die Supportobjektmethoden für die Benachrichtigungsregistrierung zu verwenden, rufen Dienstanbieter [IMAPISupport::Subscribe](imapisupport-subscribe.md) in ihren **Advise-Methoden** auf und übergeben sie, um den Ratgeber-Senkenzeiger zu **abonnieren,** den Clients an **Advise** übergeben. Wenn ein Eintragsbezeichner als Eingabeparameter übergeben wird, um eine Empfehlungsquelle anzugeben, konvertieren Dienstanbieter ihn in einen Binärschlüssel. **Subscribe** erstellt eine eindeutige Verbindungsnummer, und es ist diese Nummer, die Dienstanbieter an Clients zurückgeben. Dienstanbieter können den Verweis auf das "Advise Sink"-Objekt des Clients jederzeit nach Abschluss des **Advise-Aufrufs** freigeben. 
  
Wenn Clients **"Unadvise"** aufrufen, um eine Registrierung abzubrechen, dekrementieren Dienstanbieter entweder die Referenzanzahl auf den Ratschlagzeiger des Clients oder rufen **Unsubscribe** auf, um dies zu tun. 
  
Wenn es an der Zeit ist, eine Benachrichtigung zu generieren, führen Dienstanbieter alle internen Verarbeitungen aus, die sich auf die Benachrichtigung beziehen, und initialisieren eine [NOTIFICATION-Struktur,](notification.md) indem sie alle nicht verwendeten Elemente auf Null festlegen. Diese Technik zum Initialisieren der **NOTIFICATION-Struktur** kann Clients dabei helfen, kleinere, schnellere und weniger fehleranfällige **OnNotify-Implementierungen** zu erstellen. 
  
Die folgende Abbildung zeigt die Kommunikation zwischen "advise sink"-Objekten, "advise source"-Objekten und MAPI. MAPI ist nur beteiligt, wenn die Empfehlungsquelle die **IMAPISupport-Methoden** zur Unterstützung von Benachrichtigungen aufruft. 
  
**Ereignisbenachrichtigungsaufrufe**
  
![Ereignisbenachrichtigungsaufrufe](media/amapi_51.gif "Ereignisbenachrichtigungsaufrufe")
  
Die MFCMAPI **CAdviseSink-Klasse** (unter Verwendung der Dateien AdviseSink.h und AdviseSink.cpp) implementiert das Advise-Senkenobjekt für alle Aufrufe von **"Advise".** Weitere Informationen zu MFCMAPI finden Sie unter [MFCMAPI als Codebeispiel](mfcmapi-as-a-code-sample.md) und [MFCMAPI.](https://go.microsoft.com/fwlink/?LinkId=124154)
  

