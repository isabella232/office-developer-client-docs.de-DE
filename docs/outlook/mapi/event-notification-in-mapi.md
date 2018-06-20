---
title: Ereignisbenachrichtigung in MAPI
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 7b3b625b-6dea-4b12-99a9-152935bdfe39
description: 'Letzte �nderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 9c1fd58a31481d8666ca931408c16bd73aaba660
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19791656"
---
# <a name="event-notification-in-mapi"></a>Ereignisbenachrichtigung in MAPI

**Betrifft**: Outlook 
  
Benachrichtigung bei ist die Kommunikation des Informationsflusses zwischen zwei MAPI-Objekte. Registriert über eines der Objekte ein Client oder Dienstanbieter für die Benachrichtigung über eine Änderung oder einen Fehler, aufgerufen, ein Ereignis, die in dem anderen Objekt erfolgen kann. Nachdem das Ereignis auftritt, wird das erste Objekt ändern oder Fehler benachrichtigt. Das Objekt, das die Benachrichtigung empfangen, wird den Advise-Empfänger aufgerufen. das Objekt, die verantwortlich für die Benachrichtigung wird die Advise-Quelle bezeichnet.
  
Es gibt drei Typen von Advise Empfängerobjekten (alle Typen sind standard MAPI-Objekte):
  
- Empfehlen Sie Empfängerobjekten.   
- Formular advise-Empfängerobjekten.  
- Ansicht advise-Empfängerobjekten.
    
Informieren Sie die am häufigsten verwendeten Empfängerobjekten sind. Advise-Senken sind in der Regel von Clientanwendungen Adressbuch und Benachrichtigungen über Textnachrichten Store and Support erhalten implementiert die [IMAPIAdviseSink: IUnknown](imapiadvisesinkiunknown.md) Schnittstelle. **IMAPIAdviseSink** enthält eine einzige Methode auf, [IMAPIAdviseSink::OnNotify](imapiadvisesink-onnotify.md). Formular- und darauf hinzuweisen, dass senken seltener sind; Sie werden implementiert Erhalt von Benachrichtigungen zu Änderungen für benutzerdefinierte Formulare. Formular advise-senken Unterstützung der [IMAPIFormAdviseSink: IUnknown](imapiformadvisesinkiunknown.md) senken Support advise-Schnittstelle und Anzeigen der [IMAPIViewAdviseSink: IUnknown](imapiviewadvisesinkiunknown.md) Schnittstelle. Da die meisten Clients Einst advise-Empfängerobjekten, wird davon ausgegangen Sie, dass der Benachrichtigungen an Diskussionen mit Adressbuch und Benachrichtigungen über Textnachrichten Store statt Forms Benachrichtigungen verknüpft sind. Weitere Informationen zu Formularen Benachrichtigungen finden Sie unter [MAPI-Formulare Benachrichtigungen](mapi-forms-notifications.md) und [Schreiben von Formularcode Server](writing-form-server-code.md).
  
Informieren Sie die Objekte implementiert werden, indem Dienstanbieter und MAPI-Quelle. Nicht alle Dienstanbieter unterstützen ereignisbenachrichtigung; Es ist optional, aber dringend empfohlen. Nachrichtenspeicher und Adressbucheinträge Anbieter Benachrichtigungen von Support-Objekt in der Regel für mehrere Objekte und Benachrichtigungen auf ihren Inhalt und Hierarchietabellen Tabelle. Transportanbieter unterstützen Benachrichtigungen nicht direkt. geschäftswichtige alternativer Methoden der Kommunikation mit Clients.
  
Im Gegensatz zu Advise-senken empfehlen Sie, dass die Source-Objekten nicht über einen eindeutigen Objekttyp MAPI sind. Viele MAPI-Objekte, wie Nachrichtenspeicher und Tabellen, dauert die Rolle des Advise-Quelle. Eine Advise-Datenquelle ist jedes MAPI-Objekt mit den folgenden Funktionen:
  
- Implementiert eine **Advise** -Methode, um Registrierungen Benachrichtigung zu erhalten. 
    
- Implementiert eine **Unadvise** -Methode zum absagen Benachrichtigung zu erhalten. 
    
- Generiert Benachrichtigungen des entsprechenden Typs auf die entsprechenden Advise-Empfänger-Objekte, die durch den Aufruf ihrer **IMAPIAdviseSink::OnNotify** Methoden registriert. 
    
Clients, die implementiert werden ausschließlich Empfängerobjekten **Advise** aufrufen, wenn sie möchten, registrieren Sie sich für eine Benachrichtigung, in den meisten Fällen in die Eintrags-ID des Objekts mit der Registrierung erfolgen soll, und **Unadvise** übergeben, wenn sie abbrechen möchten die Registrierung. Clients übergeben Sie einen Parameter an **anweisen** , die verschiedene Typen von Ereignissen gibt an, die sie überwachen möchten. **Advise** gibt eine Zahl ungleich NULL, die eine erfolgreiche Verbindung zwischen der Advise-Empfänger und Advise-Quelle darstellt. 
  
Vor dem Aufruf von **anweisen**, können Clients bestimmen, ob eine Nachricht Speicheranbieter Benachrichtigung Mobilgeräts unterstützt, die das Flag STORE_NOTIFY_OK in den Nachrichtenspeicher **PR_STORE_SUPPORT_MASK** ([PidTagStoreSupportMask](pidtagstoresupportmask-canonical-property.md)) festgelegt ist -Eigenschaft. Besteht keine Möglichkeit für Clients, um feststellen, ob ein Adressbuchanbieter Benachrichtigungen unterstützt. Clients müssen versuchen, registrieren, und wenn der Versuch ein Fehler auftritt, sie können davon ausgegangen, dass Benachrichtigungen nicht unterstützt werden.
  
Tritt ein Ereignis für die Clientidentität registriert hat, benachrichtigt die Advise-Quelle Advise-Empfänger, indem er seine [IMAPIAdviseSink::OnNotify](imapiadvisesink-onnotify.md) -Methode mit einer Benachrichtigung-Datenstruktur Informationen über das Ereignis enthält. Implementierung von **OnNotify** Advise-Empfänger kann als Antwort auf die Benachrichtigung, wie das Aktualisieren von Daten im Arbeitsspeicher oder Aktualisieren einer Bildschirmanzeige Aufgaben ausführen. 
  
Dienstanbieter implementieren die Unterstützung für Benachrichtigungen manuell oder der Hilfe in drei **IMAPISupport** Methoden nutzen können: [IMAPISupport::Subscribe](imapisupport-subscribe.md), [IMAPISupport::Unsubscribe](imapisupport-unsubscribe.md)und [IMAPISupport::Notify ](imapisupport-notify.md). Die Methoden **Abonnieren** und **kündigen** benachrichtigungsregistrierung behandeln und für Anbieter für die Registrierung aufgehoben; die Methode **Benachrichtigen** verarbeitet sendende Benachrichtigungen bei Bedarf. 
  
Für die Verwendung der Methoden des Support-Objekts für benachrichtigungsregistrierung-Dienstanbieter [IMAPISupport::Subscribe](imapisupport-subscribe.md) in ihren **Advise** -Methoden aufrufen und übergeben Sie **Abonnieren** den Advise-Empfängerzeiger, den Clients an **Advise**übergeben. Wenn eine Eintrags-ID als Eingabeparameter an einer Datenquelle Advise übergeben wird, von Dienstanbietern zu einem binären Schlüssel konvertieren. **Subscribe** erstellt eine eindeutige Verbindung Reihe, und diese Nummer, die an die Clients Dienstanbieter zurückgeben kann. Dienstanbieter können des Clients freigeben advise-Empfängerzeiger jederzeit nach Abschluss der **Advise** -Anruf. 
  
Wenn Clients **Unadvise** Abbrechen eine Registrierung Dienstanbieter aufrufen entweder die verweiszählung auf des Clients verringern advise-Empfängerzeiger, oder rufen Sie **kündigen** , um diesen Vorgang auszuführen. 
  
Wenn eine Benachrichtigung generiert wird, führen Sie Dienstanbieter interne Verarbeitung, bezieht sich auf die Benachrichtigung, die eine [Benachrichtigung](notification.md) Struktur initialisiert, indem Sie alle nicht verwendeten Member auf 0 (null) festlegen. Dieses Verfahren für die Initialisierung der **Benachrichtigung** Struktur hilft Clients kleiner, schneller und weniger fehleranfällig **OnNotify** Implementierungen zu erstellen. 
  
Die folgende Abbildung zeigt der Kommunikation zwischen Empfängerobjekten darauf hinzuweisen, advise-Source-Objekten und MAPI. MAPI ist beteiligt, nur, wenn die Advise-Quelle die **IMAPISupport** -Methoden für die Benachrichtigung Unterstützung aufruft. 
  
**Ereignisbenachrichtigungsaufrufe**
  
![Ereignisbenachrichtigungsaufrufe] (media/amapi_51.gif "Ereignisbenachrichtigungsaufrufe")
  
(Bei Verwendung der AdviseSink.h und AdviseSink.cpp-Dateien) MFCMAPI (engl.) **CAdviseSink** -Klasse implementiert das Advise-Empfängerobjekt für alle Anrufe **Advise**. Weitere Informationen zu MFCMAPI (engl.) finden Sie unter [MFCMAPI (engl.) als ein Codebeispiel](mfcmapi-as-a-code-sample.md) und [MFCMAPI (engl.)](http://go.microsoft.com/fwlink/?LinkId=124154).
  

