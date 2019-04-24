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
  
Ereignisbenachrichtigung ist die Kommunikation zwischen zwei MAPI-Objekten. Durch eines der Objekte registriert ein Client-oder Dienstanbieter die Benachrichtigung über eine Änderung oder einen Fehler, die als Ereignis bezeichnet wird, die im anderen Objekt erfolgen kann. Nachdem das Ereignis eintritt, wird das erste Objekt über die Änderung oder den Fehler benachrichtigt. Das Objekt, das die Benachrichtigung empfängt, wird als Advise-Senke bezeichnet. das für die Benachrichtigung zuständige Objekt wird als Advise-Quelle bezeichnet.
  
Es gibt drei Typen von Advise-Senke-Objekten (alle Typen sind Standard-MAPI-Objekte):
  
- Advise-Objekte.   
- Formular Advise Sink-Objekte.  
- View Advise-Senke-Objekte.
    
Advise-Senke-Objekte sind der häufigste Typ. Advise-Senken werden in der Regel von Clientanwendungen implementiert, um Benachrichtigungen über Adressbuch-und Nachrichtenspeicher zu erhalten und die [IMAPIAdviseSink: IUnknown](imapiadvisesinkiunknown.md) -Schnittstelle zu unterstützen. **IMAPIAdviseSink** enthält eine einzelne Methode, [IMAPIAdviseSink:: OnNotify](imapiadvisesink-onnotify.md). Formular-und Ansichts-Advise-Senken sind seltener; Sie werden implementiert, um Benachrichtigungen zu Änderungen an benutzerdefinierten Formularen zu erhalten. Form Advise-Senken unterstützen die [IMAPIFormAdviseSink: IUnknown](imapiformadvisesinkiunknown.md) -Schnittstelle und View Advise-Senken unterstützen die [IMAPIViewAdviseSink: IUnknown](imapiviewadvisesinkiunknown.md) -Schnittstelle. Da die meisten Clients standardmäßige Advise-Objekt Objekte implementieren, gehen Sie davon aus, dass sich die Diskussionen über Benachrichtigungen auf Adressbuch-und Nachrichtenspeicher Benachrichtigungen beziehen, statt auf Formular Benachrichtigungen. Weitere Informationen zu Formular Benachrichtigungen finden Sie unter [MAPI](mapi-forms-notifications.md) -Formular Benachrichtigungen und [Schreiben von Formular Server Code](writing-form-server-code.md).
  
Advise-Quellobjekte werden von Dienstanbietern und von MAPI implementiert. Nicht alle Dienstanbieter unterstützen Ereignisbenachrichtigungen; Sie ist optional, wird jedoch dringend empfohlen. Nachrichtenspeicher-und Adressbuchanbieter unterstützen in der Regelobjekt Benachrichtigungen für mehrere Objekte und Tabellen Benachrichtigungen in ihren Inhalts-und Hierarchietabellen. Transport Anbieter unterstützen keine Benachrichtigungen direkt; Sie setzen auf Alternative Kommunikationsmethoden mit Clients.
  
Im Gegensatz zu Advise-Senken sind Quellobjekte kein eindeutiger MAPI-Objekttyp. Viele MAPI-Objekte, wie Nachrichtenspeicher und Tabellen, können die Rolle der Advise-Quelle übernehmen. Eine Advise-Quelle ist ein MAPI-Objekt, das folgende Aktionen ausführt:
  
- Implementiert eine **Advise** -Methode, um Benachrichtigungs Registrierungen zu erhalten. 
    
- Implementiert eine **Unadvise** -Methode, um Benachrichtigungs Abbruch zu erhalten. 
    
- Generiert Benachrichtigungen des entsprechenden Typs für die entsprechenden Advise-Empfängerobjekte, die sich registriert haben, indem **Sie Ihre IMAPIAdviseSink:: OnNotify** -Methoden aufrufen. 
    
Clients, die Advise-Senke-Objekte implementieren, rufen **Advise** auf, wenn Sie sich für eine Benachrichtigung registrieren möchten, in den meisten Fällen übergeben Sie die Eintrags-ID **** des Objekts, mit dem die Registrierung erfolgen soll, und deaktivieren Sie, wenn Sie den Registrierung. Clients übergeben einen Parameter, **** der angibt, welche der verschiedenen Ereignistypen überwacht werden sollen. **Advise** gibt eine Zahl ungleich NULL zurück, die eine erfolgreiche Verbindung zwischen der Advise-Senke und der Advise-Quelle darstellt. 
  
Vor dem Aufrufen von **Advise**können Clients ermitteln, ob ein Nachrichtenspeicher Anbieter eine Benachrichtigung unterstützt, indem Sie überprüfen, dass das STORE_NOTIFY_OK-Flag im **PR_STORE_SUPPORT_MASK** des Nachrichtenspeichers ([PidTagStoreSupportMask](pidtagstoresupportmask-canonical-property.md)) festgelegt ist. Eigenschaft. Es gibt keine Möglichkeit für Clients, vorab zu bestimmen, ob ein Adressbuchanbieter Benachrichtigungen unterstützt. Clients müssen sich registrieren, und wenn der Versuch fehlschlägt, können Sie davon ausgehen, dass Benachrichtigungen nicht unterstützt werden.
  
Tritt ein Ereignis ein, für das ein Client registriert wurde, benachrichtigt die Advise-Quelle die Advise-Senke, indem [Sie die IMAPIAdviseSink:: OnNotify](imapiadvisesink-onnotify.md) -Methode mit einer Benachrichtigungsdatenstruktur aufruft, die Informationen über das Ereignis enthält. Die Implementierung von onNotify durch **** eine Advise-Senke kann Aufgaben als Reaktion auf die Benachrichtigung ausführen, beispielsweise das Aktualisieren von Daten im Arbeitsspeicher oder das Aktualisieren einer Bildschirmanzeige. 
  
Dienstanbieter können die Unterstützung für Benachrichtigungen manuell implementieren oder die Hilfe in drei **IMAPISupport** -Methoden nutzen: [IMAPISupport:: subscribe](imapisupport-subscribe.md), [IMAPISupport:: unsubscribe](imapisupport-unsubscribe.md)und [IMAPISupport:: notify ](imapisupport-notify.md). Die **subscribe** - **** und die Unsubscribe-Methode behandeln die Benachrichtigungs Registrierung und-Deregistrierung für Anbieter. die **Notify** -Methode verarbeitet bei Bedarf das Senden von Benachrichtigungen. 
  
Um die Support-Objektmethoden für die Benachrichtigungs Registrierung zu verwenden, rufen Dienstanbieter [IMAPISupport:: subscribe](imapisupport-subscribe.md) in Ihren **Advise** -Methoden auf und geben den Advise-Senke-Zeiger an, den die Clients an **Advise**übermitteln. **** Wenn eine Eintrags-ID als Eingabeparameter übergeben wird, um eine Advise-Quelle anzugeben, werden Sie von Dienstanbietern in einen Binär Schlüssel konvertiert. **Subscribe** erstellt eine eindeutige Verbindungsnummer, und diese Nummer wird von Dienstanbietern an Clients zurückgegeben. Dienstanbieter können den Objektzeiger des Advise-Objekts des Clients jederzeit freigeben, nachdem der **Advise** -Aufruf abgeschlossen wurde. 
  
Wenn Clients **Unadvise** aufrufen, um eine Registrierung abzubrechen, verringern die Dienstanbieter entweder den Verweiszähler auf den Zeiger der Advise-Senke des Clients oder rufen das **Abonnement** ab, um dasselbe zu tun. 
  
Wenn es Zeit ist, eine Benachrichtigung zu generieren, führen Dienstanbieter jede interne Verarbeitung aus, die sich auf die Benachrichtigung [](notification.md) bezieht, und Initialisiert eine Benachrichtigungsstruktur, indem alle nicht verwendeten Member auf NULL festgelegt werden. Diese Technik für die Initialisierung **** der Benachrichtigungsstruktur kann Clients helfen, kleinere, schnellere und weniger fehleranfällige OnNotify-Implementierungen zu erstellen. **** 
  
Die folgende Abbildung zeigt die Kommunikation zwischen den Advise-Senke-Objekten, Advise-Quellobjekten und MAPI. MAPI ist nur dann beteiligt, wenn die Advise-Quelle die **IMAPISupport** -Methoden für die Benachrichtigungsunterstützung aufruft. 
  
**Ereignisbenachrichtigungsaufrufe**
  
![Ereignis Benachrichtigungsaufrufe] (media/amapi_51.gif "Ereignis Benachrichtigungsaufrufe")
  
Die MFCMAPI- **CAdviseSink** -Klasse (mit den Dateien AdviseSink. h und AdviseSink. cpp) implementiert das Advise-Senke-Objekt für alle Aufrufe von **Advise**. Weitere Informationen zu MFCMAPI finden Sie unter [MfcMapi als Code Beispiel](mfcmapi-as-a-code-sample.md) und [MfcMapi](https://go.microsoft.com/fwlink/?LinkId=124154).
  

