---
title: Formularbasierte Authentifizierung
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 282b2377-45ba-4f0c-a7d9-830fa3505c93
description: Outlook Social Connector (OSC) die ISocialProvider::GetCapabilities-Methode aufgerufen, um die Funktionen des OSC-Anbieter für soziale Netzwerke bestimmen.
ms.openlocfilehash: bf6534b72af7db92e02bed74f2028a086b26cbcf
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19795966"
---
# <a name="forms-based-authentication"></a>Formularbasierte Authentifizierung

Outlook Social Connector (OSC) die [ISocialProvider::GetCapabilities](isocialprovider-getcapabilities.md) -Methode aufgerufen, um die Funktionen des OSC-Anbieter für soziale Netzwerke bestimmen. Die OSC verwendet die zurückgegebenen Funktionen um zu bestimmen, wie einen Office-Benutzer unterstützen, die mit diesem sozialen Netzwerk angemeldet ist. 

Wenn das **UseLogonWebAuth** -Element in der zurückgegebenen **Funktionen** XML gibt an, dass der OSC-Anbieter formularbasierte Authentifizierung unterstützt, kann die OSC aufrufende Folgendes zu einem Benutzer ermöglichen, melden Sie sich mit dem sozialen Netzwerk vornehmen: 
  
1. [ISocialProvider::Load](isocialprovider-load.md) &ndash; Der OSC lädt den Anbieter. 
    
2. [ISocialProvider::Version](isocialprovider-version.md) &ndash; Der OSC Ruft eine Zeichenfolge, die die Versionsnummer des Anbieters für diese für soziale Netzwerke darstellt. 
    
3. [ISocialProvider::SocialNetworkName](isocialprovider-socialnetworkname.md) &ndash; Der OSC Ruft eine Zeichenfolge, die den Namen für soziale Netzwerke darstellt. 
    
4. [ISocialProvider::SocialNetworkGuid](isocialprovider-socialnetworkguid.md) &ndash; Der OSC dient zum Abrufen einer unveränderlichen GUID, die für soziale Netzwerke darstellt. 
    
5. [ISocialProvider::GetCapabilities](isocialprovider-getcapabilities.md) &ndash; Der OSC Ruft eine Zeichenfolge, die die Funktionen des Providers darstellt, die die Schemadefinition für das **Capabilities** -Element entspricht. 
    
6. [ISocialProvider::SocialNetworkIcon](isocialprovider-socialnetworkicon.md) &ndash; Der OSC Ruft ein Bytearray, das Symbol für die Website für soziale Netzwerke darstellt. 
    
7. [ISocialProvider::GetSession](isocialprovider-getsession.md) &ndash; Der OSC Ruft eine [ISocialSession](isocialsessioniunknown.md) -Schnittstelle. 
    
8. [ISocialSession::LogonWeb](isocialsession-logonweb.md) &ndash; Der OSC initialisiert Anmelden bei der Website für soziale Netzwerke durch die formularbasierte Authentifizierung. Für diesen ersten Anmeldung Aufruf übergibt die OSC **null** für den Parameter _ConnectIn_ . 
    
9. [ISocialSession::GetLogonUrl](isocialsession-getlogonurl.md) &ndash; Der OSC Ruft die URL zu einem Formular browserbasierte während der Webauthentifizierung für den Benutzer anzuzeigen. 
    
10. [ISocialSession::LogonWeb](isocialsession-logonweb.md) &ndash; Der OSC beendet die Anmeldung bei der Website für soziale Netzwerke mithilfe der formularbasierten Authentifizierung. Die OSC ruft diese Methode ein zweites Mal die URL des Formulars Anmeldung an dem Anbieter in der _ConnectIn_ -Parameter übergeben. 
    
11. [ISocialSession::GetLoggedOnUser](isocialsession-getloggedonuser.md) &ndash; Der OSC Ruft eine [ISocialProfile](isocialprovideriunknown.md) -Schnittstelle, die den angemeldeten Benutzer darstellt. 
    
12. [ISocialSession::GetNetworkIdentifier](isocialsession-getnetworkidentifier.md) &ndash; Der OSC Ruft eine Zeichenfolge, die einen eindeutigen Bezeichner für eine Website für soziale Netzwerke darstellt. Die Netzwerk-ID kann den Namen des Netzwerks entsprechen. 
    
## <a name="see-also"></a>Siehe auch

- [XML-Code für Funktionen](xml-for-capabilities.md)
- [OSC - Typische Aufrufsequenzen](osc-typical-calling-sequences.md)

