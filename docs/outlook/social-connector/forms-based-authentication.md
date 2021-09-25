---
title: Formularbasierte Authentifizierung
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
ms.localizationpriority: medium
ms.assetid: 282b2377-45ba-4f0c-a7d9-830fa3505c93
description: Der Outlook Connector für soziale Netzwerke (OSC) ruft die ISocialProvider::GetCapabilities-Methode auf, um die Funktionen des OSC-Anbieters für ein soziales Netzwerk zu ermitteln.
ms.openlocfilehash: da424c773b7860c27bc5bf6609b6b26508212e72
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59563267"
---
# <a name="forms-based-authentication"></a>Formularbasierte Authentifizierung

Der Outlook Connector für soziale Netzwerke (OSC) ruft die [ISocialProvider::GetCapabilities-Methode](isocialprovider-getcapabilities.md) auf, um die Funktionen des OSC-Anbieters für ein soziales Netzwerk zu ermitteln. Der OSC verwendet die zurückgegebenen Funktionen, um zu bestimmen, wie ein Office Benutzer unterstützt wird, der sich bei diesem sozialen Netzwerk anmeldet. 

Wenn das **useLogonWebAuth-Element** in den zurückgegebenen **Funktionen** angibt, dass der OSC-Anbieter die formularbasierte Authentifizierung unterstützt, kann osc die folgende Aufrufsequenz erstellen, damit sich ein Benutzer bei diesem sozialen Netzwerk anmelden kann: 
  
1. [ISocialProvider::Load](isocialprovider-load.md) &ndash; Der OSC lädt den Anbieter. 
    
2. [ISocialProvider::Version](isocialprovider-version.md) &ndash; Der OSC ruft eine Zeichenfolge ab, die die Versionsnummer des Anbieters für dieses soziale Netzwerk darstellt. 
    
3. [ISocialProvider::SocialNetworkName](isocialprovider-socialnetworkname.md) &ndash; Der OSC ruft eine Zeichenfolge ab, die den Namen des sozialen Netzwerks darstellt. 
    
4. [ISocialProvider::SocialNetworkGuid](isocialprovider-socialnetworkguid.md) &ndash; Der OSC ruft eine unveränderliche GUID ab, die das soziale Netzwerk darstellt. 
    
5. [ISocialProvider::GetCapabilities](isocialprovider-getcapabilities.md) &ndash; Der OSC ruft eine Zeichenfolge ab, die die Funktionen des Anbieters darstellt und der Schemadefinition für das **Capabilities-Element** entspricht. 
    
6. [ISocialProvider::SocialNetworkIcon](isocialprovider-socialnetworkicon.md) &ndash; Der OSC ruft ein Bytearray ab, das das Symbol für den Standort des sozialen Netzwerks darstellt. 
    
7. [ISocialProvider::GetSession](isocialprovider-getsession.md) &ndash; Osc ruft eine [ISocialSession-Schnittstelle](isocialsessioniunknown.md) ab. 
    
8. [ISocialSession::LogonWeb](isocialsession-logonweb.md) &ndash; Der OSC initialisiert die Anmeldung an der Website für soziale Netzwerke durch formularbasierte Authentifizierung. Für diesen anfänglichen Anmeldeaufruf übergibt osc **null** für den _connectIn-Parameter._ 
    
9. [ISocialSession::GetLogonUrl](isocialsession-getlogonurl.md) &ndash; Der OSC ruft die URL zum Anzeigen eines browserbasierten Formulars für den Benutzer während der Webauthentifizierung ab. 
    
10. [ISocialSession::LogonWeb](isocialsession-logonweb.md) &ndash; Der OSC schließt die Anmeldung bei der Website des sozialen Netzwerks mithilfe der formularbasierten Authentifizierung ab. Der OSC ruft diese Methode ein zweites Mal auf und übergibt die URL des Anmeldeformulars an den Anbieter im _parameter "connectIn"._ 
    
11. [ISocialSession::GetLoggedOnUser](isocialsession-getloggedonuser.md) &ndash; Der OSC ruft eine [ISocialProfile-Schnittstelle](isocialprovideriunknown.md) ab, die den angemeldeten Benutzer darstellt. 
    
12. [ISocialSession::GetNetworkIdentifier](isocialsession-getnetworkidentifier.md) &ndash; Der OSC ruft eine Zeichenfolge ab, die einen eindeutigen Bezeichner für einen Standort in sozialen Netzwerken darstellt. Der Netzwerkbezeichner kann dem Netzwerknamen entsprechen. 
    
## <a name="see-also"></a>Siehe auch

- [XML für Funktionen](xml-for-capabilities.md)
- [OSC - Typische Aufrufsequenzen](osc-typical-calling-sequences.md)

