---
title: ISocialSession IUnknown
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 0fe423d7-b044-479b-89ad-c39620eedd65
description: Stellt eine Verbindung zu einem sozialen Netzwerkstandort dar.
ms.openlocfilehash: c60fab1c27d2f761db28ed06bb45080857630e8d
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33437826"
---
# <a name="isocialsession--iunknown"></a>ISocialSession : IUnknown

Stellt eine Verbindung zu einem sozialen Netzwerkstandort dar.
  
## <a name="members"></a>Members

In der folgenden Tabelle sind die Member aufgeführt, die auf der **ISocialSession** -Schnittstelle verfügbar sind. 
  
|**Name**|**Mitgliedstyp**|**Beschreibung**|
|:-----|:-----|:-----|
|[FindPerson](isocialsession-findperson.md) <br/> |Methode  <br/> |Ruft eine Zeichenfolge ab, die eine oder mehrere Personen darstellt, die mit dem Parameter _UserID_ übereinstimmen.  <br/> |
|[FollowPerson](isocialsession-followperson.md) <br/> |Methode  <br/> |Fügt die Person, die vom Parameter " _Email_ " als Freund für den angemeldeten Benutzer im sozialen Netzwerk identifiziert wird, hinzu.  <br/> |
|[GetActivities](isocialsession-getactivities.md) <br/> |Methode  <br/> |Diese Methode ist in Outlook Social Connector (OSC) 1,1 veraltet.  <br/> |
|[GetLoggedOnUser](isocialsession-getloggedonuser.md) <br/> |Methode  <br/> |Ruft eine [ISocialProfile](isocialprofileisocialperson.md) -Schnittstelle ab, die den angemeldeten Benutzer darstellt.  <br/> |
|[GetLogonUrl](isocialsession-getlogonurl.md) <br/> |Methode  <br/> |Ruft eine Zeichenfolge ab, die eine URL darstellt, die zum Anzeigen eines browserbasierten Formulars für den Benutzer während der Webauthentifizierung verwendet wird.  <br/> |
|[GetNetworkIdentifier](isocialsession-getnetworkidentifier.md) <br/> |Methode  <br/> |Ruft eine Zeichenfolge, die eine eindeutige soziale Netzwerk-ID für eine bestimmte soziale Netzwerkverbindung darstellt.  <br/> |
|[GetPerson](isocialsession-getperson.md) <br/> |Methode  <br/> |Ruft eine [ISocialPerson](isocialpersoniunknown.md) -Schnittstelle basierend auf dem Parameter _UserID_ ab.  <br/> |
|[LoggedOnUserID](isocialsession-loggedonuserid.md) <br/> |Eigenschaft  <br/> |Gibt eine Zeichenfolge, die die soziale Netzwerk-Benutzer-ID des derzeit angemeldeten Benutzers darstellt.  <br/> |
|[LoggedOnUserName](isocialsession-loggedonusername.md) <br/> |Eigenschaft  <br/> |Gibt eine Zeichenfolge, die den Benutzernamen darstellt, der bei der Anmeldung verwendet wird.  <br/> |
|[Logon](isocialsession-logon.md) <br/> |Methode  <br/> |Meldet sich mit dem angegebenen Benutzernamen und Kennwort bei der Website für soziale Netzwerke an.  <br/> |
|[LogonWeb](isocialsession-logonweb.md) <br/> |Methode  <br/> |Meldet sich mithilfe der formularbasierten Authentifizierung an der Website für soziale Netzwerke an.  <br/> |
|[SiteUrl](isocialsession-siteurl.md) <br/> |Eigenschaft  <br/> |Legt die URL für die Website für soziale Netzwerke fest.  <br/> |
|[UnFollowPerson](isocialsession-unfollowperson.md) <br/> |Methode  <br/> |Entfernt die Person, die durch den Parameter _UserID_ als Freund im sozialen Netzwerk identifiziert wird.  <br/> |
   
## <a name="remarks"></a>Bemerkungen

Ein OSC-Anbieter muss diese Schnittstelle für die Kommunikation mit dem OSC implementieren.
  
## <a name="see-also"></a>Siehe auch

- [Outlook Social Connector-Anbieterschnittstellen](outlook-social-connector-provider-interfaces.md)

