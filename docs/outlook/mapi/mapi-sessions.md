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
ms.openlocfilehash: a2ab44081c79e72e082687006ab06d0f83b8367e
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2018
ms.locfileid: "22575028"
---
# <a name="mapi-sessions"></a>MAPI-Sitzungen

**Betrifft**: Outlook 2013 | Outlook 2016 
  
Bevor der Clientanwendung aus eine zugrunde liegenden messaging-System aufrufen kann, m�ssen sie eine Sitzung oder bei einer Verbindung mit der MAPI-Subsystems einrichten.
  
Sessions are initiated when a user logs on, a process that accesses a valid profile and validates the messaging system and the message service credentials. Then, the process ensures that all of the profile's message services are correctly configured. The client interface you use determines the logon call. MAPI clients call the [MAPILogonEx](mapilogonex.md) function. 
  
Dienstkonfiguration Nachricht ist eine der interessantesten Teile des Anmeldevorgangs. Das Profil ist die urspr�ngliche Quelle f�r Konfigurationsinformationen. Wenn f�r eine bestimmte Nachrichtendienst nicht vorhanden ist, versucht der Anmeldevorgang den Benutzer auffordern, die sie bereitstellen. Dies ist nicht immer erfolgreich aus zwei Gr�nden: zuerst, den Benutzer aufzufordern, erfordert die Anzeige eines Dialogfelds. Es ist m�glich f�r Clients, um die Anzeige einer Benutzeroberfl�che deaktivieren, indem Sie ein Flag in den Anruf Anmeldung �bergeben. Zweitens kann der Benutzer das Dialogfeld abbrechen, bevor die ben�tigte Informationen hinzugef�gt werden kann.
  
Bei ein Anmeldevorgang einmal fehlschl�gt, wird der Benutzer des Fehlers dar�ber informiert und erhalten die M�glichkeit zum Wiederholen oder Fehlerbedingung zu korrigieren. Auch hier wird eine Benutzeroberfl�che angezeigt, wenn der Client dies zul�sst und der Benutzer aufgefordert wird, geben die Daten nicht vorhanden ist. Wenn diese zweite Versuch nicht erfolgreich ist, wird die MAPI alle-Dienstanbieter in der Nachricht Service f�r die Dauer der Sitzung deaktiviert. Im Grunde ist der gesamte Nachricht-Dienst deaktiviert. Dies bedeutet, dass keines der Dienstanbieter in der Nachrichtendienst arbeiten k�nnen. Dies erfolgt, da, wenn ein Anbieter Fehler bei der Anmeldung, die anderen Anbieter in der Regel auch fehl. Des Anmeldevorgangs kann aufgrund einer ung�ltigen Pfad f�r eine erforderliche Ressource eine inkompatible Version der MAPI, messaging-Server nicht verf�gbar oder besch�digte Daten fehlschlagen. 
  
Clients k�nnen einen von zwei Typen der Sitzungen in den Anruf Anmeldung eingerichtet werden angeben: eine einzelne Sitzung oder einer Freigabesitzung. Einzelne Sitzungen sind VPN-Verbindungen. Es ist eine 1: 1-Beziehung zwischen einer Clientanwendung und die Sitzungen, in denen, die es verwendet wird. Folglich freigeben Clientanwendungen, die eine Sitzung teilen auch ein Profil. Freigabesitzungen einmal hergestellt werden, aber Sie k�nnen von anderen Clientanwendungen, die sie verwenden m�ssen verwendet werden. Das Profil und die Anmeldeinformationen werden nur bei der ersten Anmeldung angegeben. 
  
Clients k�nnen mehrere Male als derselbe Benutzer oder mehrere Benutzer anmelden. MAPI wird dies nicht verhindert. Einige Dienstanbieter, jedoch nicht so flexibel m�glicherweise den Fehlerwert MAPI_E_SESSION_LIMIT f�r nachfolgende Anmeldeversuche zur�ck. -Dienstanbietern mit zugrunde liegenden Hardwareeinschr�nkungen k�nnen es erforderlich sein, einen Grenzwert f�r Videositzung zu erzwingen.
  
Aufrufe der Funktionen zum Einrichten einer Sitzung verf�gen �ber eine Auflistung von Flags und Parameter das Steuerelement, wie die Sitzung erstellt wird. Der Client gibt eine optionale Profilname und ein Fensterhandle, das als �bergeordnetes Fenster f�r alle Dialogfelder fungiert, die angezeigt werden. Die Kennzeichen z�hlen MAPI_NEW_SESSION, mit dem angefordert wird, dass eine neue, einzelne Sitzung (anstelle einer Freigabesitzung) hergestellt werden, und die MAPI_LOGON_UI Benutzer Schnittstelle-Flag. Die Benutzer-Flag-Schnittstelle wird festgelegt, so fordern Sie ein Anmeldedialogfeld an.
  
Die folgende Abbildung zeigt, wie diese verschiedenen Parameter und Flags eine MAPI-Sitzung herzustellen.
  
**Flussdiagramm f�r MAPI-Sitzung**
  
![Flussdiagramm für MAPI-Sitzung] (media/amapi_47.gif "Flussdiagramm für MAPI-Sitzung")
  
For information about handling sessions from within a client application, see [MAPI-Sitzung-Verarbeitung](mapi-session-handling.md)
  
## <a name="see-also"></a>Siehe auch

- [MAPILogonEx](mapilogonex.md)  
- [IMAPISession: IUnknown](imapisessioniunknown.md)
- [MAPI-Sitzung-Verarbeitung](mapi-session-handling.md)  
- [�bersicht �ber die MAPI-Programmierung](mapi-programming-overview.md)

