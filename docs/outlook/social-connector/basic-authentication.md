---
title: Standardauthentifizierung
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 89349d1e-365a-442e-9ba3-2df601d9323c
description: Der Outlook Social Connector (OSC) ruft die ISocialProvider::GetCapabilities-Methode auf, um die Funktionen des OSC-Anbieters für ein soziales Netzwerk zu ermitteln.
ms.openlocfilehash: 7f716df3ef2e82712374ce3d775cdf66eb07e8b3
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33439926"
---
# <a name="basic-authentication"></a>Standardauthentifizierung

Das Outlook Social Connector (OSC) ruft die [ISocialProvider::GetCapabilities-Methode](isocialprovider-getcapabilities.md) auf, um die Funktionen des OSC-Anbieters für ein soziales Netzwerk zu ermitteln. Das OSC verwendet die zurückgegebenen Funktionen, um zu bestimmen, wie ein benutzer Office, der sich bei diesem sozialen Netzwerk anmeldet. Wenn das **useLogonWebAuth-Element**  im zurückgegebenen Funktionen-XML angibt, dass der OSC-Anbieter die Standardauthentifizierung unterstützt, kann das OSC die folgende Aufrufsequenz erstellen, damit sich ein Benutzer bei diesem sozialen Netzwerk anmelden kann: 
  
1. [ISocialProvider::Load](isocialprovider-load.md) – Das Betriebssystem lädt den Anbieter. 
    
2. [ISocialProvider::Version](isocialprovider-version.md) – Das OSC ruft eine Zeichenfolge ab, die die Versionsnummer des OSC-Anbieters darstellt. 
    
3. [ISocialProvider::SocialNetworkName](isocialprovider-socialnetworkname.md) – Das OSC ruft eine Zeichenfolge ab, die den Namen des sozialen Netzwerks darstellt. 
    
4. [ISocialProvider::SocialNetworkGuid](isocialprovider-socialnetworkguid.md) – Das OSC ruft eine unveränderliche GUID ab, die das soziale Netzwerk darstellt. 
    
5. [ISocialProvider::GetCapabilities](isocialprovider-getcapabilities.md) – Das OSC ruft eine Zeichenfolge ab, die die Funktionen des Anbieters darstellt und die der Schemadefinition für das **Capabilities-Element** entspricht. 
    
6. [ISocialProvider::SocialNetworkIcon](isocialprovider-socialnetworkicon.md) – Das OSC ruft ein Bytearray ab, das das Symbol für die Website des sozialen Netzwerks darstellt. 
    
7. [ISocialProvider::GetSession](isocialprovider-getsession.md) – Das OSC ruft eine [ISocialSession-Schnittstelle](isocialsessioniunknown.md) ab. 
    
8. [ISocialSession::Logon](isocialsession-logon.md) – Das Betriebssystem meldet den Benutzer mithilfe des angegebenen Benutzernamens und Kennworts am Standort des sozialen Netzwerks an. 
    
9. [ISocialSession::GetLoggedOnUser](isocialsession-getloggedonuser.md) – Das OSC ruft eine [ISocialProfile-Schnittstelle](isocialprovideriunknown.md) ab, die den angemeldeten Benutzer darstellt. 
    
10. [ISocialSession::GetNetworkIdentifier](isocialsession-getnetworkidentifier.md) – Das OSC ruft eine Zeichenfolge ab, die einen eindeutigen Bezeichner für einen Standort im sozialen Netzwerk darstellt. Der Netzwerkbezeichner kann dem Netzwerknamen entsprechen. 
    
## <a name="see-also"></a>Siehe auch

- [XML für Funktionen](xml-for-capabilities.md)
- [OSC - Typische Aufrufsequenzen](osc-typical-calling-sequences.md)

