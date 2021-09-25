---
title: Standardauthentifizierung
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
ms.localizationpriority: medium
ms.assetid: 89349d1e-365a-442e-9ba3-2df601d9323c
description: Der Outlook Connector für soziale Netzwerke (OSC) ruft die ISocialProvider::GetCapabilities-Methode auf, um die Funktionen des OSC-Anbieters für ein soziales Netzwerk zu ermitteln.
ms.openlocfilehash: 803fe6ae37bb408f8e3082e184317c4d19831906
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59616257"
---
# <a name="basic-authentication"></a>Standardauthentifizierung

Der Outlook Connector für soziale Netzwerke (OSC) ruft die [ISocialProvider::GetCapabilities-Methode](isocialprovider-getcapabilities.md) auf, um die Funktionen des OSC-Anbieters für ein soziales Netzwerk zu ermitteln. Der OSC verwendet die zurückgegebenen Funktionen, um zu bestimmen, wie ein Office Benutzer unterstützt wird, der sich bei diesem sozialen Netzwerk anmeldet. Wenn das **useLogonWebAuth-Element** in den zurückgegebenen **Funktionen** angibt, dass der OSC-Anbieter die Standardauthentifizierung unterstützt, kann osc die folgende Aufrufsequenz vornehmen, damit sich ein Benutzer bei diesem sozialen Netzwerk anmelden kann: 
  
1. [ISocialProvider::Load](isocialprovider-load.md) -Der OSC lädt den Anbieter. 
    
2. [ISocialProvider::Version](isocialprovider-version.md) - Der OSC ruft eine Zeichenfolge ab, die die Versionsnummer des OSC-Anbieters darstellt. 
    
3. [ISocialProvider::SocialNetworkName](isocialprovider-socialnetworkname.md) -Der OSC ruft eine Zeichenfolge ab, die den Namen des sozialen Netzwerks darstellt. 
    
4. [ISocialProvider::SocialNetworkGuid](isocialprovider-socialnetworkguid.md) -Der OSC erhält eine unveränderliche GUID, die das soziale Netzwerk darstellt. 
    
5. [ISocialProvider::GetCapabilities](isocialprovider-getcapabilities.md) -Der OSC ruft eine Zeichenfolge ab, die die Funktionen des Anbieters darstellt und der Schemadefinition für das **Capabilities-Element** entspricht. 
    
6. [ISocialProvider::SocialNetworkIcon](isocialprovider-socialnetworkicon.md) -Der OSC ruft ein Bytearray ab, das das Symbol für die Website des sozialen Netzwerks darstellt. 
    
7. [ISocialProvider::GetSession](isocialprovider-getsession.md) -Der OSC ruft eine [ISocialSession-Schnittstelle](isocialsessioniunknown.md) ab. 
    
8. [ISocialSession::Logon](isocialsession-logon.md) -Der OSC protokolliert den Benutzer mithilfe des angegebenen Benutzernamens und Kennworts am Standort des sozialen Netzwerks. 
    
9. [ISocialSession::GetLoggedOnUser](isocialsession-getloggedonuser.md) - Der OSC ruft eine [ISocialProfile-Schnittstelle](isocialprovideriunknown.md) ab, die den angemeldeten Benutzer darstellt. 
    
10. [ISocialSession::GetNetworkIdentifier](isocialsession-getnetworkidentifier.md) -Der OSC ruft eine Zeichenfolge ab, die einen eindeutigen Bezeichner für eine Website in sozialen Netzwerken darstellt. Der Netzwerkbezeichner kann dem Netzwerknamen entsprechen. 
    
## <a name="see-also"></a>Siehe auch

- [XML für Funktionen](xml-for-capabilities.md)
- [OSC - Typische Aufrufsequenzen](osc-typical-calling-sequences.md)

