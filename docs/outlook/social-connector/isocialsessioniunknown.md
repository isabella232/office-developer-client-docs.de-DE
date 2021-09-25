---
title: ISocialSession IUnknown
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
ms.assetid: 0fe423d7-b044-479b-89ad-c39620eedd65
description: Stellt eine Verbindung mit einem Standort für soziale Netzwerke dar.
ms.openlocfilehash: 7efe8922f7f4dfa3c9cf06a910266c0d3bf2cdda
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59629067"
---
# <a name="isocialsession--iunknown"></a>ISocialSession : IUnknown

Stellt eine Verbindung mit einem Standort für soziale Netzwerke dar.
  
## <a name="members"></a>Members

In der folgenden Tabelle sind die Elemente aufgeführt, die auf der **ISocialSession-Schnittstelle** verfügbar sind. 
  
|**Name**|**Membertyp**|**Beschreibung**|
|:-----|:-----|:-----|
|[FindPerson](isocialsession-findperson.md) <br/> |Methode  <br/> |Ruft eine Zeichenfolge ab, die eine oder mehrere Personen darstellt, die dem  _parameter userID_ entsprechen.  <br/> |
|[FollowPerson](isocialsession-followperson.md) <br/> |Methode  <br/> |Fügt die vom parameter  _emailAddress identifizierte_ Person als Freund für den angemeldeten Benutzer im sozialen Netzwerk hinzu.  <br/> |
|[GetActivities](isocialsession-getactivities.md) <br/> |Methode  <br/> |Diese Methode ist in Outlook Connector für soziale Netzwerke (OSC) 1.1 veraltet.  <br/> |
|[GetLoggedOnUser](isocialsession-getloggedonuser.md) <br/> |Methode  <br/> |Ruft eine [ISocialProfile-Schnittstelle](isocialprofileisocialperson.md) ab, die den angemeldeten Benutzer darstellt.  <br/> |
|[GetLogonUrl](isocialsession-getlogonurl.md) <br/> |Methode  <br/> |Ruft eine Zeichenfolge ab, die eine URL darstellt, die für die Darstellung eines browserbasierten Formulars für den Benutzer während der Webauthentifizierung verwendet wird.  <br/> |
|[GetNetworkIdentifier](isocialsession-getnetworkidentifier.md) <br/> |Methode  <br/> |Ruft eine Zeichenfolge ab, die einen eindeutigen Bezeichner für ein soziales Netzwerk für eine bestimmte Verbindung mit einem sozialen Netzwerk darstellt.  <br/> |
|[GetPerson](isocialsession-getperson.md) <br/> |Methode  <br/> |Ruft eine [ISocialPerson-Schnittstelle](isocialpersoniunknown.md) basierend auf dem  _userID-Parameter_ ab.  <br/> |
|[LoggedOnUserID](isocialsession-loggedonuserid.md) <br/> |Eigenschaft  <br/> |Gibt eine Zeichenfolge zurück, die die Benutzer-ID des Aktuell angemeldeten Benutzers im sozialen Netzwerk darstellt.  <br/> |
|[LoggedOnUserName](isocialsession-loggedonusername.md) <br/> |Eigenschaft  <br/> |Gibt eine Zeichenfolge zurück, die den Benutzernamen darstellt, der bei der Anmeldung verwendet wird.  <br/> |
|[Logon](isocialsession-logon.md) <br/> |Methode  <br/> |Meldet sich mithilfe des angegebenen Benutzernamens und Kennworts am Standort des sozialen Netzwerks an.  <br/> |
|[LogonWeb](isocialsession-logonweb.md) <br/> |Methode  <br/> |Meldet sich mithilfe der formularbasierten Authentifizierung am Standort des sozialen Netzwerks an.  <br/> |
|[SiteUrl](isocialsession-siteurl.md) <br/> |Eigenschaft  <br/> |Legt die URL des Standorts für das soziale Netzwerk fest.  <br/> |
|[UnFollowPerson](isocialsession-unfollowperson.md) <br/> |Methode  <br/> |Entfernt die Person, die vom  _Parameter userID_ als Freund im sozialen Netzwerk identifiziert wird.  <br/> |
   
## <a name="remarks"></a>Bemerkungen

Ein OSC-Anbieter muss diese Schnittstelle für die Kommunikation mit dem OSC implementieren.
  
## <a name="see-also"></a>Siehe auch

- [Outlook Anbieterschnittstellen für Connector für soziale Netzwerke](outlook-social-connector-provider-interfaces.md)

