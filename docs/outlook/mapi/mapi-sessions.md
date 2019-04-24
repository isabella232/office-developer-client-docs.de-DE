---
title: MAPI-Sitzungen
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: c5a7c137-393e-40ff-a2b9-afe02da2435a
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 3dd55d8ee3cb2751fb27184f0069ae831e2164ee
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32319583"
---
# <a name="mapi-sessions"></a>MAPI-Sitzungen

**Gilt für**: Outlook 2013 | Outlook 2016 
  
Bevor der Clientanwendung aus eine zugrunde liegenden messaging-System aufrufen kann, m�ssen sie eine Sitzung oder bei einer Verbindung mit der MAPI-Subsystems einrichten.
  
Sessions are initiated when a user logs on, a process that accesses a valid profile and validates the messaging system and the message service credentials. Then, the process ensures that all of the profile's message services are correctly configured. The client interface you use determines the logon call. MAPI clients call the [MAPILogonEx](mapilogonex.md) function. 
  
Die Nachrichtendienst Konfiguration ist einer der wichtigsten Teile des Anmeldevorgangs. Das Profil ist die erste Quelle für Konfigurationsinformationen. Wenn Informationen für einen bestimmten Nachrichtendienst fehlen, versucht der Anmeldeprozess, den Benutzer aufzufordern, ihn bereitzustellen. Dies ist aus zwei Gründen nicht immer erfolgreich: Erstens erfordert die Bestätigung des Benutzers, dass ein Dialogfeld angezeigt wird. Clients können die Anzeige einer Benutzeroberfläche nicht zulassen, indem Sie eine Kennzeichnung an den Anmelde Anruf übergeben. Zweitens könnte der Benutzer das Dialogfeld abbrechen, bevor die benötigten Informationen hinzugefügt werden können.
  
Wenn ein Anmeldevorgang einmal fehlschlägt, wird der Benutzer über den Fehler informiert und hat die Möglichkeit, den Fehler zu wiederholen oder zu korrigieren. Erneut wird eine Benutzeroberfläche angezeigt, wenn der Client dies zulässt, und der Benutzer wird aufgefordert, alle fehlenden Daten einzugeben. Wenn dieser zweite Versuch nicht erfolgreich ist, deaktiviert MAPI alle Dienstanbieter im Nachrichtendienst für die Dauer der Sitzung. Der gesamte Nachrichtendienst ist tatsächlich deaktiviert. Dies führt dazu, dass keiner der Dienstanbieter im Nachrichtendienst funktionieren kann. Der Grund dafür ist, dass bei einem Ausfall eines Anbieters bei der Anmeldung die anderen Anbieter in der Regel auch fehlschlagen. Der Anmeldeprozess kann aufgrund eines ungültigen Pfads für eine erforderliche Ressource, einer inkompatiblen MAPI-Version, eines nicht verfügbaren Messaging Servers oder einer Datenbeschädigung fehlschlagen. 
  
Clients können einen von zwei Sitzungstypen angeben, die im Anmelde Anruf festgelegt werden sollen: eine einzelne Sitzung oder eine freigegebene Sitzung. Einzelne Sitzungen sind private Verbindungen; zwischen einer Clientanwendung und der verwendeten Sitzung besteht eine 1:1-Beziehung. Clientanwendungen, die eine Sitzung gemeinsam nutzen, können daher auch ein Profil verwenden. FreigeGebene Sitzungen werden einmalig eingerichtet, können jedoch von anderen Clientanwendungen verwendet werden, die Sie verwenden müssen. Das Profil und die Anmeldeinformationen werden nur bei der erstmaligen Anmeldung angegeben. 
  
Clients können sich mehrmals als derselbe Benutzer oder mehrere Benutzer anmelden. Dies wird durch MAPI nicht verhindert. Einige Dienstanbieter sind jedoch möglicherweise nicht so flexibel, und der Fehlerwert MAPI_E_SESSION_LIMIT wird bei nachfolgenden Anmeldeversuchen zurückgegeben. Dienstanbieter mit zugrunde liegenden Hardwareeinschränkungen können zum Erzwingen eines Sitzungslimits erforderlich sein.
  
Die Funktionsaufrufe zum Einrichten einer Sitzung haben eine Auflistung von Flags und Parametern, die Steuern, wie die Sitzung erstellt wird. Der Client gibt einen optionalen Profilnamen und ein Fensterhandle an, das als übergeordnetes Fenster für alle angezeigten Dialogfelder fungiert. Zu den Flags gehört MAPI_NEW_SESSION, das eine neue, einzelne Sitzung (anstelle einer freigegebenen Sitzung) und das MAPI_LOGON_UI-Benutzeroberflächen Kennzeichen anfordert. Das Benutzeroberflächen Kennzeichen ist so festgelegt, dass ein Anmeldedialogfeld angefordert wird.
  
In der folgenden Abbildung wird gezeigt, wie diese verschiedenen Parameter und Flags eine MAPI-Sitzung herstellen.
  
**Flussdiagramm für MAPI-Sitzung**
  
![MAPI-Sitzungs Flussdiagramm] (media/amapi_47.gif "MAPI-Sitzungs Flussdiagramm")
  
Informationen zur Behandlung von Sitzungen innerhalb einer Clientanwendung finden Sie unter [MAPI-Sitzungs Verarbeitung](mapi-session-handling.md)
  
## <a name="see-also"></a>Siehe auch

- [MAPILogonEx](mapilogonex.md)  
- [IMAPISession : IUnknown](imapisessioniunknown.md)
- [MAPI-Sitzungs Verarbeitung](mapi-session-handling.md)  
- [�bersicht �ber die MAPI-Programmierung](mapi-programming-overview.md)

