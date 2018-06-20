---
title: Standardauthentifizierung
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 89349d1e-365a-442e-9ba3-2df601d9323c
description: Outlook Social Connector (OSC) die ISocialProvider::GetCapabilities-Methode aufgerufen, um die Funktionen des OSC-Anbieter für soziale Netzwerke bestimmen.
ms.openlocfilehash: 8287133445a4e8fa928f6b7724ab41ca9b58baf9
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19795978"
---
# <a name="basic-authentication"></a>Standardauthentifizierung

Outlook Social Connector (OSC) die [ISocialProvider::GetCapabilities](isocialprovider-getcapabilities.md) -Methode aufgerufen, um die Funktionen des OSC-Anbieter für soziale Netzwerke bestimmen. Die OSC verwendet die zurückgegebenen Funktionen um zu bestimmen, wie einen Office-Benutzer unterstützen, die mit diesem sozialen Netzwerk angemeldet ist. Wenn das **UseLogonWebAuth** -Element in der zurückgegebenen **Funktionen** XML gibt an, dass der OSC-Anbieter Standardauthentifizierung unterstützt, kann die OSC aufrufende Folgendes zu einem Benutzer ermöglichen, melden Sie sich mit dem sozialen Netzwerk vornehmen: 
  
1. [ISocialProvider::Load](isocialprovider-load.md) – die OSC lädt den Anbieter. 
    
2. [ISocialProvider::Version](isocialprovider-version.md) – die OSC Ruft eine Zeichenfolge, die die Versionsnummer des OSC-Providers darstellt. 
    
3. [ISocialProvider::SocialNetworkName](isocialprovider-socialnetworkname.md) – die OSC Ruft eine Zeichenfolge, die den Namen für soziale Netzwerke darstellt. 
    
4. [ISocialProvider::SocialNetworkGuid](isocialprovider-socialnetworkguid.md) – die OSC dient zum Abrufen einer unveränderlichen GUID, die für soziale Netzwerke darstellt. 
    
5. [ISocialProvider::GetCapabilities](isocialprovider-getcapabilities.md) – die OSC Ruft eine Zeichenfolge, die die Funktionen des Providers darstellt, die die Schemadefinition für das **Capabilities** -Element entspricht. 
    
6. [ISocialProvider::SocialNetworkIcon](isocialprovider-socialnetworkicon.md) – die OSC Ruft ein Bytearray, das Symbol für die Website für soziale Netzwerke darstellt. 
    
7. [ISocialProvider::GetSession](isocialprovider-getsession.md) – die OSC Ruft eine [ISocialSession](isocialsessioniunknown.md) -Schnittstelle. 
    
8. [ISocialSession::Logon](isocialsession-logon.md) – die OSC meldet den Benutzer bei der Website für soziale Netzwerke mithilfe der angegebenen Benutzernamen und Kennwort. 
    
9. [ISocialSession::GetLoggedOnUser](isocialsession-getloggedonuser.md) – die OSC Ruft eine [ISocialProfile](isocialprovideriunknown.md) -Schnittstelle, die den angemeldeten Benutzer darstellt. 
    
10. [ISocialSession::GetNetworkIdentifier](isocialsession-getnetworkidentifier.md) – die OSC Ruft eine Zeichenfolge, die einen eindeutigen Bezeichner für eine Website für soziale Netzwerke darstellt. Die Netzwerk-ID kann den Namen des Netzwerks entsprechen. 
    
## <a name="see-also"></a>Siehe auch

- [XML-Code für Funktionen](xml-for-capabilities.md)
- [OSC - Typische Aufrufsequenzen](osc-typical-calling-sequences.md)

