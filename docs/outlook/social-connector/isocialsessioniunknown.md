---
title: ISocialSession IUnknown
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 0fe423d7-b044-479b-89ad-c39620eedd65
description: Stellt eine Verbindung mit einer Website für soziale Netzwerke.
ms.openlocfilehash: ee3a8aa72ea187b4c211bc7a49e8a2dbe170adad
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19796004"
---
# <a name="isocialsession--iunknown"></a>ISocialSession : IUnknown

Stellt eine Verbindung mit einer Website für soziale Netzwerke.
  
## <a name="members"></a>Elemente

In der folgenden Tabelle werden die Member, die für die **ISocialSession** -Schnittstelle verfügbar sind. 
  
|**Name**|**Typ des Elements**|**Beschreibung**|
|:-----|:-----|:-----|
|[FindPerson](isocialsession-findperson.md) <br/> |Methode  <br/> |Ruft eine Zeichenfolge, die eine oder mehrere Personen darstellt, die den _Benutzer-ID_ -Parameter entsprechen.  <br/> |
|[FollowPerson](isocialsession-followperson.md) <br/> |Methode  <br/> |Fügt die Person, die durch den Parameter _EmailAddress_ als einen Freund für den angemeldeten Benutzer im sozialen Netzwerk identifiziert.  <br/> |
|[GetActivities](isocialsession-getactivities.md) <br/> |Methode  <br/> |Diese Methode ist in Outlook Social Connector (OSC) 1.1 veraltet.  <br/> |
|[GetLoggedOnUser](isocialsession-getloggedonuser.md) <br/> |Methode  <br/> |Ruft eine [ISocialProfile](isocialprofileisocialperson.md) -Schnittstelle, die den angemeldeten Benutzer darstellt.  <br/> |
|[GetLogonUrl](isocialsession-getlogonurl.md) <br/> |Methode  <br/> |Ruft eine Zeichenfolge, die eine URL darstellt, die für die Darstellung eines Formulars browserbasierte für dem Benutzer während der Webauthentifizierung verwendet wird.  <br/> |
|[GetNetworkIdentifier](isocialsession-getnetworkidentifier.md) <br/> |Methode  <br/> |Ruft eine Zeichenfolge, die einen eindeutigen für soziale Netzwerkbezeichner für eine bestimmte sozialen Netzwerkverbindung darstellt.  <br/> |
|[GetPerson](isocialsession-getperson.md) <br/> |Methode  <br/> |Ruft eine [ISocialPerson](isocialpersoniunknown.md) -Schnittstelle basierend auf dem _UserID_ -Parameter.  <br/> |
|[LoggedOnUserID](isocialsession-loggedonuserid.md) <br/> |Eigenschaft  <br/> |Gibt eine Zeichenfolge, die die sozialen Netzwerk-Benutzer-ID des Benutzers darstellt, der derzeit angemeldet ist.  <br/> |
|[LoggedOnUserName](isocialsession-loggedonusername.md) <br/> |Eigenschaft  <br/> |Gibt eine Zeichenfolge, die den Benutzernamen darstellt, der beim Anmelden verwendet wird.  <br/> |
|[Logon](isocialsession-logon.md) <br/> |Methode  <br/> |Meldet sich bei der Website für soziale Netzwerke mithilfe der angegebenen Benutzernamen und Kennwort.  <br/> |
|[LogonWeb](isocialsession-logonweb.md) <br/> |Methode  <br/> |Meldet sich bei der Website für soziale Netzwerke mithilfe der formularbasierten Authentifizierung.  <br/> |
|[SiteUrl](isocialsession-siteurl.md) <br/> |Eigenschaft  <br/> |Legt die URL der Website für soziale Netzwerke.  <br/> |
|[UnFollowPerson](isocialsession-unfollowperson.md) <br/> |Methode  <br/> |Entfernt die Person, die durch den _Benutzer-ID_ -Parameter als einen Freund im sozialen Netzwerk identifiziert.  <br/> |
   
## <a name="remarks"></a>Bemerkungen

Ein OSC-Anbieter muss diese Schnittstelle für die Kommunikation mit dem OSC implementieren.
  
## <a name="see-also"></a>Siehe auch

- [Outlook Connector für soziale Netzwerke Provider-Schnittstellen](outlook-social-connector-provider-interfaces.md)

