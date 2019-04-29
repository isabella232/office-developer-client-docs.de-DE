---
title: Standardauthentifizierung
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 89349d1e-365a-442e-9ba3-2df601d9323c
description: 'Der Outlook Connector für soziale Netzwerke (OSC) Ruft die ISocialProvider:: getCapabilities-Methode auf, um die Funktionen des OSC-Anbieters für ein soziales Netzwerk zu bestimmen.'
ms.openlocfilehash: 7f716df3ef2e82712374ce3d775cdf66eb07e8b3
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33439926"
---
# <a name="basic-authentication"></a>Standardauthentifizierung

Der Outlook Connector für soziale Netzwerke (OSC) Ruft die [ISocialProvider:: getCapabilities](isocialprovider-getcapabilities.md) -Methode auf, um die Funktionen des osc-Anbieters für ein soziales Netzwerk zu bestimmen. OSC verwendet die zurückgegebenen Funktionen, um zu bestimmen, wie ein Office-Benutzer unterstützt wird, der sich an diesem sozialen Netzwerk anmeldet. Wenn das **useLogonWebAuth** -Element im zurückgegebenen **Capabilities** -XML-Code angibt, dass der osc-Anbieter die Standardauthentifizierung unterstützt, kann osc die folgende Aufrufsequenz ausführen, um einem Benutzer die Anmeldung an diesem sozialen Netzwerk zu ermöglichen: 
  
1. [ISocialProvider:: Load](isocialprovider-load.md) – der osc lädt den Anbieter. 
    
2. [ISocialProvider:: Version](isocialprovider-version.md) – osc Ruft eine Zeichenfolge ab, die die Versionsnummer des osc-Anbieters darstellt. 
    
3. [ISocialProvider:: SocialNetworkName](isocialprovider-socialnetworkname.md) – osc Ruft eine Zeichenfolge ab, die den Namen des sozialen Netzwerks darstellt. 
    
4. [ISocialProvider:: SocialNetworkGuid](isocialprovider-socialnetworkguid.md) – osc Ruft eine unveränderliche GUID ab, die das soziale Netzwerk darstellt. 
    
5. [ISocialProvider:: getCapabilities](isocialprovider-getcapabilities.md) – osc Ruft eine Zeichenfolge ab, die die Funktionen des Anbieters darstellt und die der Schema Definition für das **Capabilities** -Element entspricht. 
    
6. [ISocialProvider:: SocialNetworkIcon](isocialprovider-socialnetworkicon.md) – osc Ruft ein Bytearray ab, das das Symbol für die soziale Netzwerk Website darstellt. 
    
7. [ISocialProvider:: getSession](isocialprovider-getsession.md) – der osc Ruft eine [ISocialSession](isocialsessioniunknown.md) -Schnittstelle ab. 
    
8. [ISocialSession:: Anmeldung](isocialsession-logon.md) -osc meldet den Benutzer mithilfe des angegebenen Benutzernamens und Kennworts an der Website für soziale Netzwerke an. 
    
9. [ISocialSession:: GetLoggedOnUser](isocialsession-getloggedonuser.md) – osc Ruft eine [ISocialProfile](isocialprovideriunknown.md) -Schnittstelle ab, die den angemeldeten Benutzer darstellt. 
    
10. [ISocialSession:: GetNetworkIdentifier](isocialsession-getnetworkidentifier.md) – osc Ruft eine Zeichenfolge ab, die einen eindeutigen Bezeichner für eine soziale Netzwerk Website darstellt. Die Netzwerk-ID kann dem Netzwerknamen entsprechen. 
    
## <a name="see-also"></a>Siehe auch

- [XML für Funktionen](xml-for-capabilities.md)
- [OSC - Typische Aufrufsequenzen](osc-typical-calling-sequences.md)

