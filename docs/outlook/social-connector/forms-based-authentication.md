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
# <a name="forms-based-authentication"></a><span data-ttu-id="5204e-103">Formularbasierte Authentifizierung</span><span class="sxs-lookup"><span data-stu-id="5204e-103">Forms-based authentication</span></span>

<span data-ttu-id="5204e-104">Der Outlook Connector für soziale Netzwerke (OSC) Ruft die [ISocialProvider:: getCapabilities](isocialprovider-getcapabilities.md) -Methode auf, um die Funktionen des osc-Anbieters für ein soziales Netzwerk zu bestimmen.</span><span class="sxs-lookup"><span data-stu-id="5204e-104">The Outlook Social Connector (OSC) calls the [ISocialProvider::GetCapabilities](isocialprovider-getcapabilities.md) method to determine the capabilities of the OSC provider for a social network.</span></span> <span data-ttu-id="5204e-105">OSC verwendet die zurückgegebenen Funktionen, um zu bestimmen, wie ein Office-Benutzer unterstützt wird, der sich an diesem sozialen Netzwerk anmeldet.</span><span class="sxs-lookup"><span data-stu-id="5204e-105">The OSC uses the returned capabilities to determine how to support an Office user who is logging on to this social network.</span></span> 

<span data-ttu-id="5204e-106">Wenn das **useLogonWebAuth** -Element im zurückgegebenen **Capabilities** -XML-Code angibt, dass der osc-Anbieter die formularbasierte Authentifizierung unterstützt, kann osc die folgende Aufrufsequenz ausführen, um einem Benutzer die Anmeldung an diesem sozialen Netzwerk zu ermöglichen:</span><span class="sxs-lookup"><span data-stu-id="5204e-106">If the **useLogonWebAuth** element in the returned **capabilities** XML indicates that the OSC provider supports forms-based authentication, the OSC can make the following calling sequence to allow a user to log on to that social network:</span></span> 
  
1. <span data-ttu-id="5204e-107">[ISocialProvider:: Laden](isocialprovider-load.md) &ndash; Der osc lädt den Anbieter.</span><span class="sxs-lookup"><span data-stu-id="5204e-107">[ISocialProvider::Load](isocialprovider-load.md) &ndash; The OSC loads the provider.</span></span> 
    
2. <span data-ttu-id="5204e-108">[ISocialProvider:: Version](isocialprovider-version.md) &ndash; Osc Ruft eine Zeichenfolge ab, die die Versionsnummer des Anbieters für dieses soziale Netzwerk darstellt.</span><span class="sxs-lookup"><span data-stu-id="5204e-108">[ISocialProvider::Version](isocialprovider-version.md) &ndash; The OSC gets a string that represents the version number of the provider for this social network.</span></span> 
    
3. <span data-ttu-id="5204e-109">[ISocialProvider:: SocialNetworkName](isocialprovider-socialnetworkname.md) &ndash; Osc Ruft eine Zeichenfolge ab, die den Namen des sozialen Netzwerks darstellt.</span><span class="sxs-lookup"><span data-stu-id="5204e-109">[ISocialProvider::SocialNetworkName](isocialprovider-socialnetworkname.md) &ndash; The OSC gets a string that represents the social network name.</span></span> 
    
4. <span data-ttu-id="5204e-110">[ISocialProvider:: SocialNetworkGuid](isocialprovider-socialnetworkguid.md) &ndash; Osc Ruft eine unveränderliche GUID ab, die das soziale Netzwerk darstellt.</span><span class="sxs-lookup"><span data-stu-id="5204e-110">[ISocialProvider::SocialNetworkGuid](isocialprovider-socialnetworkguid.md) &ndash; The OSC gets an immutable GUID that represents the social network.</span></span> 
    
5. <span data-ttu-id="5204e-111">[ISocialProvider:: getCapabilities](isocialprovider-getcapabilities.md) &ndash; Osc Ruft eine Zeichenfolge ab, die die Funktionen des Anbieters darstellt und die der Schema Definition für das **Capabilities** -Element entspricht.</span><span class="sxs-lookup"><span data-stu-id="5204e-111">[ISocialProvider::GetCapabilities](isocialprovider-getcapabilities.md) &ndash; The OSC gets a string that represents the provider's capabilities and that complies with the schema definition for the **capabilities** element.</span></span> 
    
6. <span data-ttu-id="5204e-112">[ISocialProvider:: SocialNetworkIcon](isocialprovider-socialnetworkicon.md) &ndash; Osc Ruft ein Bytearray ab, das das Symbol für die soziale Netzwerk Website darstellt.</span><span class="sxs-lookup"><span data-stu-id="5204e-112">[ISocialProvider::SocialNetworkIcon](isocialprovider-socialnetworkicon.md) &ndash; The OSC gets a byte array that represents the icon for the social network site.</span></span> 
    
7. <span data-ttu-id="5204e-113">[ISocialProvider:: getSession](isocialprovider-getsession.md) &ndash; Osc Ruft eine [ISocialSession](isocialsessioniunknown.md) -Schnittstelle ab.</span><span class="sxs-lookup"><span data-stu-id="5204e-113">[ISocialProvider::GetSession](isocialprovider-getsession.md) &ndash; The OSC gets an [ISocialSession](isocialsessioniunknown.md) interface.</span></span> 
    
8. <span data-ttu-id="5204e-114">[ISocialSession:: LogonWeb](isocialsession-logonweb.md) &ndash; Osc initialisiert die Anmeldung beim Netzwerkstandort für soziale Netzwerke durch die formularbasierte Authentifizierung.</span><span class="sxs-lookup"><span data-stu-id="5204e-114">[ISocialSession::LogonWeb](isocialsession-logonweb.md) &ndash; The OSC initializes logging on to the social network site by forms-based authentication.</span></span> <span data-ttu-id="5204e-115">Bei diesem anfänglichen Anmelde Aufruf übergibt der OSC **null** für den __ Parameter connectin.</span><span class="sxs-lookup"><span data-stu-id="5204e-115">For this initial logon call, the OSC passes **null** for the  _connectIn_ parameter.</span></span> 
    
9. <span data-ttu-id="5204e-116">[ISocialSession:: GetLogonUrl](isocialsession-getlogonurl.md) &ndash; Osc Ruft die URL ab, die dem Benutzer während der Webauthentifizierung ein browserbasiertes Formular angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="5204e-116">[ISocialSession::GetLogonUrl](isocialsession-getlogonurl.md) &ndash; The OSC gets the URL to display a browser-based form to the user during web authentication.</span></span> 
    
10. <span data-ttu-id="5204e-117">[ISocialSession:: LogonWeb](isocialsession-logonweb.md) &ndash; Osc vervollständigt die Anmeldung an der Website für soziale Netzwerke mithilfe der formularbasierten Authentifizierung.</span><span class="sxs-lookup"><span data-stu-id="5204e-117">[ISocialSession::LogonWeb](isocialsession-logonweb.md) &ndash; The OSC completes the logon to the social network site by using forms-based authentication.</span></span> <span data-ttu-id="5204e-118">OSC ruft diese Methode ein zweites Mal auf und übergibt die URL des Anmeldeformulars an den Anbieter im Parameter _connectin_ .</span><span class="sxs-lookup"><span data-stu-id="5204e-118">The OSC calls this method a second time, passing the URL of the logon form to the provider in the  _connectIn_ parameter.</span></span> 
    
11. <span data-ttu-id="5204e-119">[ISocialSession:: GetLoggedOnUser](isocialsession-getloggedonuser.md) &ndash; Osc Ruft eine [ISocialProfile](isocialprovideriunknown.md) -Schnittstelle ab, die den angemeldeten Benutzer darstellt.</span><span class="sxs-lookup"><span data-stu-id="5204e-119">[ISocialSession::GetLoggedOnUser](isocialsession-getloggedonuser.md) &ndash; The OSC gets an [ISocialProfile](isocialprovideriunknown.md) interface that represents the logged-on user.</span></span> 
    
12. <span data-ttu-id="5204e-120">[ISocialSession:: GetNetworkIdentifier](isocialsession-getnetworkidentifier.md) &ndash; Osc Ruft eine Zeichenfolge ab, die einen eindeutigen Bezeichner für eine soziale Netzwerk Website darstellt.</span><span class="sxs-lookup"><span data-stu-id="5204e-120">[ISocialSession::GetNetworkIdentifier](isocialsession-getnetworkidentifier.md) &ndash; The OSC gets a string that represents a unique identifier for a social network site.</span></span> <span data-ttu-id="5204e-121">Die Netzwerk-ID kann dem Netzwerknamen entsprechen.</span><span class="sxs-lookup"><span data-stu-id="5204e-121">The network identifier can be equivalent to the network name.</span></span> 
    
## <a name="see-also"></a><span data-ttu-id="5204e-122">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="5204e-122">See also</span></span>

- [<span data-ttu-id="5204e-123">XML für Funktionen</span><span class="sxs-lookup"><span data-stu-id="5204e-123">XML for Capabilities</span></span>](xml-for-capabilities.md)
- [<span data-ttu-id="5204e-124">OSC - Typische Aufrufsequenzen</span><span class="sxs-lookup"><span data-stu-id="5204e-124">OSC Typical Calling Sequences</span></span>](osc-typical-calling-sequences.md)

