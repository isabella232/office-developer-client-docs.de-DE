---
title: Formularbasierte Authentifizierung
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 282b2377-45ba-4f0c-a7d9-830fa3505c93
description: 'Der Outlook Connector für soziale Netzwerke (OSC) Ruft die ISocialProvider:: getCapabilities-Methode auf, um die Funktionen des OSC-Anbieters für ein soziales Netzwerk zu bestimmen.'
ms.openlocfilehash: 420f19a8d7632f2ab9b093eb929ffe879f8a2fc2
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33435530"
---
# <a name="forms-based-authentication"></a>Formularbasierte Authentifizierung

Der Outlook Connector für soziale Netzwerke (OSC) Ruft die [ISocialProvider:: getCapabilities](isocialprovider-getcapabilities.md) -Methode auf, um die Funktionen des osc-Anbieters für ein soziales Netzwerk zu bestimmen. OSC verwendet die zurückgegebenen Funktionen, um zu bestimmen, wie ein Office-Benutzer unterstützt wird, der sich an diesem sozialen Netzwerk anmeldet. 

Wenn das **useLogonWebAuth** -Element im zurückgegebenen **Capabilities** -XML-Code angibt, dass der osc-Anbieter die formularbasierte Authentifizierung unterstützt, kann osc die folgende Aufrufsequenz ausführen, um einem Benutzer die Anmeldung an diesem sozialen Netzwerk zu ermöglichen: 
  
1. [ISocialProvider:: Laden](isocialprovider-load.md) &ndash; Der osc lädt den Anbieter. 
    
2. [ISocialProvider:: Version](isocialprovider-version.md) &ndash; Osc Ruft eine Zeichenfolge ab, die die Versionsnummer des Anbieters für dieses soziale Netzwerk darstellt. 
    
3. [ISocialProvider:: SocialNetworkName](isocialprovider-socialnetworkname.md) &ndash; Osc Ruft eine Zeichenfolge ab, die den Namen des sozialen Netzwerks darstellt. 
    
4. [ISocialProvider:: SocialNetworkGuid](isocialprovider-socialnetworkguid.md) &ndash; Osc Ruft eine unveränderliche GUID ab, die das soziale Netzwerk darstellt. 
    
5. [ISocialProvider:: getCapabilities](isocialprovider-getcapabilities.md) &ndash; Osc Ruft eine Zeichenfolge ab, die die Funktionen des Anbieters darstellt und die der Schema Definition für das **Capabilities** -Element entspricht. 
    
6. [ISocialProvider:: SocialNetworkIcon](isocialprovider-socialnetworkicon.md) &ndash; Osc Ruft ein Bytearray ab, das das Symbol für die soziale Netzwerk Website darstellt. 
    
7. [ISocialProvider:: getSession](isocialprovider-getsession.md) &ndash; Osc Ruft eine [ISocialSession](isocialsessioniunknown.md) -Schnittstelle ab. 
    
8. [ISocialSession:: LogonWeb](isocialsession-logonweb.md) &ndash; Osc initialisiert die Anmeldung beim Netzwerkstandort für soziale Netzwerke durch die formularbasierte Authentifizierung. Bei diesem anfänglichen Anmelde Aufruf übergibt der OSC **null** für den __ Parameter connectin. 
    
9. [ISocialSession:: GetLogonUrl](isocialsession-getlogonurl.md) &ndash; Osc Ruft die URL ab, die dem Benutzer während der Webauthentifizierung ein browserbasiertes Formular angezeigt wird. 
    
10. [ISocialSession:: LogonWeb](isocialsession-logonweb.md) &ndash; Osc vervollständigt die Anmeldung an der Website für soziale Netzwerke mithilfe der formularbasierten Authentifizierung. OSC ruft diese Methode ein zweites Mal auf und übergibt die URL des Anmeldeformulars an den Anbieter im Parameter _connectin_ . 
    
11. [ISocialSession:: GetLoggedOnUser](isocialsession-getloggedonuser.md) &ndash; Osc Ruft eine [ISocialProfile](isocialprovideriunknown.md) -Schnittstelle ab, die den angemeldeten Benutzer darstellt. 
    
12. [ISocialSession:: GetNetworkIdentifier](isocialsession-getnetworkidentifier.md) &ndash; Osc Ruft eine Zeichenfolge ab, die einen eindeutigen Bezeichner für eine soziale Netzwerk Website darstellt. Die Netzwerk-ID kann dem Netzwerknamen entsprechen. 
    
## <a name="see-also"></a>Siehe auch

- [XML für Funktionen](xml-for-capabilities.md)
- [OSC - Typische Aufrufsequenzen](osc-typical-calling-sequences.md)

