---
title: Formularbasierte Authentifizierung
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 282b2377-45ba-4f0c-a7d9-830fa3505c93
description: Der Outlook Social Connector (OSC) ruft die ISocialProvider::GetCapabilities-Methode auf, um die Funktionen des OSC-Anbieters für ein soziales Netzwerk zu ermitteln.
ms.openlocfilehash: 420f19a8d7632f2ab9b093eb929ffe879f8a2fc2
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33435530"
---
# <a name="forms-based-authentication"></a>Formularbasierte Authentifizierung

Das Outlook Social Connector (OSC) ruft die [ISocialProvider::GetCapabilities-Methode](isocialprovider-getcapabilities.md) auf, um die Funktionen des OSC-Anbieters für ein soziales Netzwerk zu ermitteln. Das OSC verwendet die zurückgegebenen Funktionen, um zu bestimmen, wie ein benutzer Office, der sich bei diesem sozialen Netzwerk anmeldet. 

Wenn das **useLogonWebAuth-Element**  im zurückgegebenen Funktionen-XML angibt, dass der OSC-Anbieter die formularbasierte Authentifizierung unterstützt, kann die OSC die folgende Aufrufsequenz erstellen, damit sich ein Benutzer bei diesem sozialen Netzwerk anmelden kann: 
  
1. [ISocialProvider::Load](isocialprovider-load.md) &ndash; Das OSC lädt den Anbieter. 
    
2. [ISocialProvider::Version](isocialprovider-version.md) &ndash; Das OSC ruft eine Zeichenfolge ab, die die Versionsnummer des Anbieters für dieses soziale Netzwerk darstellt. 
    
3. [ISocialProvider::SocialNetworkName](isocialprovider-socialnetworkname.md) &ndash; Das OSC ruft eine Zeichenfolge ab, die den Namen des sozialen Netzwerks darstellt. 
    
4. [ISocialProvider::SocialNetworkGuid](isocialprovider-socialnetworkguid.md) &ndash; Das OSC ruft eine unveränderliche GUID ab, die das soziale Netzwerk darstellt. 
    
5. [ISocialProvider::GetCapabilities](isocialprovider-getcapabilities.md) &ndash; Das OSC ruft eine Zeichenfolge ab, die die Funktionen des Anbieters darstellt und der Schemadefinition für das **Capabilities-Element** entspricht. 
    
6. [ISocialProvider::SocialNetworkIcon](isocialprovider-socialnetworkicon.md) &ndash; Das OSC ruft ein Bytearray ab, das das Symbol für den Standort des sozialen Netzwerks darstellt. 
    
7. [ISocialProvider::GetSession](isocialprovider-getsession.md) &ndash; Das OSC ruft eine [ISocialSession-Schnittstelle](isocialsessioniunknown.md) ab. 
    
8. [ISocialSession::LogonWeb](isocialsession-logonweb.md) &ndash; Das OSC initialisiert die Anmeldung am Standort des sozialen Netzwerks über die formularbasierte Authentifizierung. Für diesen anfänglichen Anmeldeaufruf übergibt das OSC **null** für den _connectIn-Parameter._ 
    
9. [ISocialSession::GetLogonUrl](isocialsession-getlogonurl.md) &ndash; Das OSC ruft die URL ab, um dem Benutzer während der Webauthentifizierung ein browserbasiertes Formular anzuzeigen. 
    
10. [ISocialSession::LogonWeb](isocialsession-logonweb.md) &ndash; Das OSC schließt die Anmeldung am Standort für soziale Netzwerke mithilfe der formularbasierten Authentifizierung ab. Das OSC ruft diese Methode ein zweites Mal auf und übertut die URL des Anmeldeformulars an den Anbieter im _connectIn-Parameter._ 
    
11. [ISocialSession::GetLoggedOnUser](isocialsession-getloggedonuser.md) &ndash; Die OSC ruft eine [ISocialProfile-Schnittstelle ab,](isocialprovideriunknown.md) die den angemeldeten Benutzer darstellt. 
    
12. [ISocialSession::GetNetworkIdentifier](isocialsession-getnetworkidentifier.md) &ndash; Das OSC ruft eine Zeichenfolge ab, die einen eindeutigen Bezeichner für einen Standort im sozialen Netzwerk darstellt. Der Netzwerkbezeichner kann dem Netzwerknamen entsprechen. 
    
## <a name="see-also"></a>Siehe auch

- [XML für Funktionen](xml-for-capabilities.md)
- [OSC - Typische Aufrufsequenzen](osc-typical-calling-sequences.md)

