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
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33435873"
---
# <a name="mapi-sessions"></a>MAPI-Sitzungen

**Gilt für**: Outlook 2013 | Outlook 2016 
  
Bevor der Clientanwendung aus eine zugrunde liegenden messaging-System aufrufen kann, m�ssen sie eine Sitzung oder bei einer Verbindung mit der MAPI-Subsystems einrichten.
  
Sessions are initiated when a user logs on, a process that accesses a valid profile and validates the messaging system and the message service credentials. Then, the process ensures that all of the profile's message services are correctly configured. The client interface you use determines the logon call. MAPI clients call the [MAPILogonEx](mapilogonex.md) function. 
  
Die Konfiguration des Nachrichtendienstes ist einer der wichtigsten Bestandteile des Anmeldevorgangs. Das Profil ist die erste Quelle für Konfigurationsinformationen. Wenn Informationen für einen bestimmten Nachrichtendienst fehlen, versucht der Anmeldeprozess, den Benutzer zur Bereitstellung aufzufordern. Dies ist aus zwei Gründen nicht immer erfolgreich: Erstens erfordert die Aufforderung des Benutzers die Anzeige eines Dialogfelds. Es ist möglich, dass Clients die Anzeige einer Benutzeroberfläche nicht zulassen, indem sie ein Flag an den Anmeldeaufruf übergeben. Zweitens kann der Benutzer das Dialogfeld abbrechen, bevor die erforderlichen Informationen hinzugefügt werden können.
  
Wenn ein Anmeldevorgang einmal fehlschlägt, wird der Benutzer über den Fehler informiert und erhält die Möglichkeit, die Fehlerbedingung erneut zu versuchen oder zu korrigieren. Erneut wird eine Benutzeroberfläche angezeigt, wenn der Client dies zulässt, und der Benutzer wird aufgefordert, die fehlenden Daten einzugeben. Wenn dieser zweite Versuch fehlschlägt, deaktiviert MAPI alle Dienstanbieter im Nachrichtendienst für die Dauer der Sitzung. Tatsächlich ist der gesamte Nachrichtendienst deaktiviert. Dies bedeutet, dass keiner der Dienstanbieter im Nachrichtendienst funktionieren kann. Dies geschieht, da bei einem Fehler bei der Anmeldung eines Anbieters in der Regel auch die anderen Anbieter ausfallen. Der Anmeldeprozess kann aufgrund eines ungültigen Pfads für eine erforderliche Ressource, einer inkompatiblen MAPI-Version, eines nicht verfügbaren Messagingservers oder einer Datenbeschädigung fehlschlagen. 
  
Clients können eine von zwei Arten von Sitzungen angeben, die im Anmeldeaufruf eingerichtet werden sollen: eine einzelne Sitzung oder eine freigegebene Sitzung. Einzelne Sitzungen sind private Verbindungen; Zwischen einer Clientanwendung und der von ihr verwendeten Sitzung besteht eine 1:1-Beziehung. Infolgedessen teilen Clientanwendungen, die eine Sitzung gemeinsam nutzen, auch ein Profil. Freigegebene Sitzungen werden einmal eingerichtet, können jedoch von anderen Clientanwendungen verwendet werden, die sie verwenden müssen. Das Profil und die Anmeldeinformationen werden nur mit der ersten Anmeldung angegeben. 
  
Clients können sich mehrmals als derselbe Benutzer oder als mehrere Benutzer anmelden. MAPI verhindert dies nicht. Einige Dienstanbieter sind jedoch möglicherweise nicht so flexibel, da der Fehlerwert MAPI_E_SESSION_LIMIT bei nachfolgenden Anmeldeversuchen zurückgegeben wird. Dienstanbieter mit zugrunde liegenden Hardwareeinschränkungen können erforderlich sein, um ein Sitzungslimit zu erzwingen.
  
Die Funktionsaufrufe zum Einrichten einer Sitzung verfügen über eine Sammlung von Flags und Parametern, die steuern, wie die Sitzung erstellt wird. Der Client gibt einen optionalen Profilnamen und ein Fensterhandle an, das als übergeordnetes Fenster für alle angezeigten Dialogfelder fungiert. Die Flags enthalten MAPI_NEW_SESSION, die die Einrichtung einer neuen, individuellen Sitzung (anstelle einer freigegebenen Sitzung) und das MAPI_LOGON_UI-Benutzeroberflächenflagfordert. Das Benutzeroberflächenflag wird so festgelegt, dass ein Anmeldedialogfeld anfordert.
  
Die folgende Abbildung zeigt, wie diese verschiedenen Parameter und Flags eine MAPI-Sitzung einrichten.
  
**Flussdiagramm für MAPI-Sitzung**
  
![MAPI-Sitzungsflussdiagramm](media/amapi_47.gif "MAPI-Sitzungsflussdiagramm")
  
Informationen zum Behandeln von Sitzungen innerhalb einer Clientanwendung finden Sie unter [MAPI Session Handling](mapi-session-handling.md)
  
## <a name="see-also"></a>Siehe auch

- [MAPILogonEx](mapilogonex.md)  
- [IMAPISession : IUnknown](imapisessioniunknown.md)
- [MAPI-Sitzungsbehandlung](mapi-session-handling.md)  
- [Übersicht über die MAPI-Programmierung](mapi-programming-overview.md)

