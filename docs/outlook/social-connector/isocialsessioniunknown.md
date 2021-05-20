---
title: ISocialSession IUnknown
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 0fe423d7-b044-479b-89ad-c39620eedd65
description: Stellt eine Verbindung mit einem Standort für soziale Netzwerke dar.
ms.openlocfilehash: c60fab1c27d2f761db28ed06bb45080857630e8d
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33437826"
---
# <a name="isocialsession--iunknown"></a>ISocialSession : IUnknown

Stellt eine Verbindung mit einem Standort für soziale Netzwerke dar.
  
## <a name="members"></a>Elemente

In der folgenden Tabelle sind die Elemente aufgeführt, die auf der **ISocialSession-Schnittstelle verfügbar** sind. 
  
|**Name**|**Membertyp**|**Beschreibung**|
|:-----|:-----|:-----|
|[FindPerson](isocialsession-findperson.md) <br/> |Methode  <br/> |Ruft eine Zeichenfolge ab, die eine oder mehrere Personen darstellt, die mit dem _parameter userID übereinstimmen._  <br/> |
|[FollowPerson](isocialsession-followperson.md) <br/> |Methode  <br/> |Fügt die person hinzu, die durch den  _parameter emailAddress_ als Freund für den angemeldeten Benutzer im sozialen Netzwerk identifiziert wird.  <br/> |
|[GetActivities](isocialsession-getactivities.md) <br/> |Methode  <br/> |Diese Methode ist in osc 1.1 Outlook Social Connector (OSC) veraltet.  <br/> |
|[GetLoggedOnUser](isocialsession-getloggedonuser.md) <br/> |Methode  <br/> |Ruft eine [ISocialProfile-Schnittstelle](isocialprofileisocialperson.md) ab, die den angemeldeten Benutzer darstellt.  <br/> |
|[GetLogonUrl](isocialsession-getlogonurl.md) <br/> |Methode  <br/> |Ruft eine Zeichenfolge ab, die eine URL darstellt, die zum Präsentieren eines browserbasierten Formulars für den Benutzer während der Webauthentifizierung verwendet wird.  <br/> |
|[GetNetworkIdentifier](isocialsession-getnetworkidentifier.md) <br/> |Methode  <br/> |Ruft eine Zeichenfolge ab, die eine eindeutige ID für soziale Netzwerke für eine bestimmte Verbindung mit sozialen Netzwerken darstellt.  <br/> |
|[GetPerson](isocialsession-getperson.md) <br/> |Methode  <br/> |Ruft eine [ISocialPerson-Schnittstelle](isocialpersoniunknown.md) basierend auf dem  _userID-Parameter_ ab.  <br/> |
|[LoggedOnUserID](isocialsession-loggedonuserid.md) <br/> |Eigenschaft  <br/> |Gibt eine Zeichenfolge zurück, die die Benutzer-ID des Benutzers des sozialen Netzwerks darstellt, der derzeit angemeldet ist.  <br/> |
|[LoggedOnUserName](isocialsession-loggedonusername.md) <br/> |Eigenschaft  <br/> |Gibt eine Zeichenfolge zurück, die den Benutzernamen darstellt, der bei der Anmeldung verwendet wird.  <br/> |
|[Logon](isocialsession-logon.md) <br/> |Methode  <br/> |Meldet sich mit dem angegebenen Benutzernamen und Kennwort am Standort des sozialen Netzwerks an.  <br/> |
|[LogonWeb](isocialsession-logonweb.md) <br/> |Methode  <br/> |Meldet sich mithilfe der formularbasierten Authentifizierung am Standort des sozialen Netzwerks an.  <br/> |
|[SiteUrl](isocialsession-siteurl.md) <br/> |Eigenschaft  <br/> |Legt die Website-URL des sozialen Netzwerks fest.  <br/> |
|[UnFollowPerson](isocialsession-unfollowperson.md) <br/> |Methode  <br/> |Entfernt die person, die durch den  _parameter userID_ als Freund im sozialen Netzwerk identifiziert wird.  <br/> |
   
## <a name="remarks"></a>Hinweise

Ein OSC-Anbieter muss diese Schnittstelle implementieren, um mit dem OSC zu kommunizieren.
  
## <a name="see-also"></a>Siehe auch

- [Outlook Schnittstellen für Anbieter für soziale Verbindungen](outlook-social-connector-provider-interfaces.md)

