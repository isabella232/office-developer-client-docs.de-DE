---
title: MAPI-Sitzungen
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.localizationpriority: medium
api_type:
- COM
ms.assetid: c5a7c137-393e-40ff-a2b9-afe02da2435a
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: d4e81b3e3c948d31e1f34e9e6b423ba881302f48
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59595791"
---
# <a name="mapi-sessions"></a>MAPI-Sitzungen

**Gilt für**: Outlook 2013 | Outlook 2016 
  
Bevor der Clientanwendung aus eine zugrunde liegenden messaging-System aufrufen kann, m�ssen sie eine Sitzung oder bei einer Verbindung mit der MAPI-Subsystems einrichten.
  
Sessions are initiated when a user logs on, a process that accesses a valid profile and validates the messaging system and the message service credentials. Then, the process ensures that all of the profile's message services are correctly configured. The client interface you use determines the logon call. MAPI clients call the [MAPILogonEx](mapilogonex.md) function. 
  
Die Konfiguration des Nachrichtendiensts ist einer der wichtigsten Bestandteile des Anmeldevorgangs. Das Profil ist die erste Quelle für Konfigurationsinformationen. Wenn Informationen zu einem bestimmten Nachrichtendienst fehlen, versucht der Anmeldevorgang, den Benutzer aufzufordern, ihn anzugeben. Dies ist aus zwei Gründen nicht immer erfolgreich: Zum einen muss der Benutzer aufgefordert werden, ein Dialogfeld anzuzeigen. Clients können die Anzeige einer Benutzeroberfläche verhindern, indem sie ein Flag an den Anmeldeaufruf übergeben. Zweitens könnte der Benutzer das Dialogfeld abbrechen, bevor die erforderlichen Informationen hinzugefügt werden können.
  
Wenn ein Anmeldevorgang einmal fehlschlägt, wird der Benutzer über den Fehler informiert und erhält die Möglichkeit, die Fehlerbedingung erneut zu versuchen oder zu korrigieren. Erneut wird eine Benutzeroberfläche angezeigt, wenn der Client dies zulässt, und der Benutzer wird aufgefordert, alle fehlenden Daten einzugeben. Wenn dieser zweite Versuch nicht erfolgreich ist, deaktiviert MAPI alle Dienstanbieter im Nachrichtendienst für die Dauer der Sitzung. Tatsächlich ist der gesamte Nachrichtendienst deaktiviert. Dies bedeutet, dass keiner der Dienstanbieter im Nachrichtendienst funktionieren kann. Dies geschieht, da bei einem Anmeldefehler auch die anderen Anbieter fehlschlagen. Der Anmeldevorgang kann aufgrund eines ungültigen Pfads für eine erforderliche Ressource, einer inkompatiblen Version der MAPI, eines nicht verfügbaren Messagingservers oder einer Datenbeschädigung fehlschlagen. 
  
Clients können eine von zwei Arten von Sitzungen angeben, die beim Anmeldeaufruf eingerichtet werden sollen: eine einzelne sitzung oder eine freigegebene Sitzung. Einzelne Sitzungen sind private Verbindungen; zwischen einer Clientanwendung und der verwendeten Sitzung besteht eine 1:1-Beziehung. Folglich teilen sich Clientanwendungen, die eine Sitzung teilen, auch ein Profil. Freigegebene Sitzungen werden einmal eingerichtet, können jedoch von anderen Clientanwendungen verwendet werden, die sie verwenden müssen. Das Profil und die Anmeldeinformationen werden nur bei der ersten Anmeldung angegeben. 
  
Clients können sich mehrmals als derselbe Benutzer oder als mehrere Benutzer anmelden. MapI verhindert dies nicht. Einige Dienstanbieter sind jedoch möglicherweise nicht so flexibel und geben den Fehlerwert MAPI_E_SESSION_LIMIT bei nachfolgenden Anmeldeversuchen zurück. Dienstanbieter mit zugrunde liegenden Hardwareeinschränkungen können erforderlich sein, um ein Sitzungslimit zu erzwingen.
  
Die Funktionsaufrufe zum Einrichten einer Sitzung verfügen über eine Sammlung von Flags und Parametern, die steuern, wie die Sitzung erstellt wird. Der Client gibt einen optionalen Profilnamen und ein Fensterhandle an, das als übergeordnetes Fenster für alle angezeigten Dialogfelder fungiert. Zu den Flags gehören MAPI_NEW_SESSION, die das Erstellen einer neuen, einzelnen Sitzung (anstelle einer freigegebenen Sitzung) und das MAPI_LOGON_UI Benutzeroberflächenkennzeichen anfordern. Das Kennzeichen der Benutzeroberfläche ist so festgelegt, dass ein Anmeldedialogfeld angefordert wird.
  
Die folgende Abbildung zeigt, wie diese verschiedenen Parameter und Flags eine MAPI-Sitzung einrichten.
  
**Flussdiagramm für MAPI-Sitzung**
  
![Flussdiagramm für MAPI-Sitzung](media/amapi_47.gif "Flussdiagramm für MAPI-Sitzung")
  
Informationen zum Behandeln von Sitzungen innerhalb einer Clientanwendung finden Sie unter [MAPI Session Handling](mapi-session-handling.md)
  
## <a name="see-also"></a>Siehe auch

- [MAPILogonEx](mapilogonex.md)  
- [IMAPISession : IUnknown](imapisessioniunknown.md)
- [MAPI-Sitzungsbehandlung](mapi-session-handling.md)  
- [Übersicht über die MAPI-Programmierung](mapi-programming-overview.md)

