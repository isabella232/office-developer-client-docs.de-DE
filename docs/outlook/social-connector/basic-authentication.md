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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32281220"
---
# <a name="basic-authentication"></a><span data-ttu-id="97231-103">Standardauthentifizierung</span><span class="sxs-lookup"><span data-stu-id="97231-103">Basic authentication</span></span>

<span data-ttu-id="97231-104">Der Outlook Connector für soziale Netzwerke (OSC) Ruft die [ISocialProvider:: getCapabilities](isocialprovider-getcapabilities.md) -Methode auf, um die Funktionen des osc-Anbieters für ein soziales Netzwerk zu bestimmen.</span><span class="sxs-lookup"><span data-stu-id="97231-104">The Outlook Social Connector (OSC) calls the [ISocialProvider::GetCapabilities](isocialprovider-getcapabilities.md) method to determine the capabilities of the OSC provider for a social network.</span></span> <span data-ttu-id="97231-105">OSC verwendet die zurückgegebenen Funktionen, um zu bestimmen, wie ein Office-Benutzer unterstützt wird, der sich an diesem sozialen Netzwerk anmeldet.</span><span class="sxs-lookup"><span data-stu-id="97231-105">The OSC uses the returned capabilities to determine how to support an Office user who is logging on to this social network.</span></span> <span data-ttu-id="97231-106">Wenn das **useLogonWebAuth** -Element im zurückgegebenen **Capabilities** -XML-Code angibt, dass der osc-Anbieter die Standardauthentifizierung unterstützt, kann osc die folgende Aufrufsequenz ausführen, um einem Benutzer die Anmeldung an diesem sozialen Netzwerk zu ermöglichen:</span><span class="sxs-lookup"><span data-stu-id="97231-106">If the **useLogonWebAuth** element in the returned **capabilities** XML indicates that the OSC provider supports basic authentication, the OSC can make the following calling sequence to allow a user to log on to that social network:</span></span> 
  
1. <span data-ttu-id="97231-107">[ISocialProvider:: Load](isocialprovider-load.md) – der osc lädt den Anbieter.</span><span class="sxs-lookup"><span data-stu-id="97231-107">[ISocialProvider::Load](isocialprovider-load.md) —The OSC loads the provider.</span></span> 
    
2. <span data-ttu-id="97231-108">[ISocialProvider:: Version](isocialprovider-version.md) – osc Ruft eine Zeichenfolge ab, die die Versionsnummer des osc-Anbieters darstellt.</span><span class="sxs-lookup"><span data-stu-id="97231-108">[ISocialProvider::Version](isocialprovider-version.md) —The OSC gets a string that represents the version number of the OSC provider.</span></span> 
    
3. <span data-ttu-id="97231-109">[ISocialProvider:: SocialNetworkName](isocialprovider-socialnetworkname.md) – osc Ruft eine Zeichenfolge ab, die den Namen des sozialen Netzwerks darstellt.</span><span class="sxs-lookup"><span data-stu-id="97231-109">[ISocialProvider::SocialNetworkName](isocialprovider-socialnetworkname.md) —The OSC gets a string that represents the social network name.</span></span> 
    
4. <span data-ttu-id="97231-110">[ISocialProvider:: SocialNetworkGuid](isocialprovider-socialnetworkguid.md) – osc Ruft eine unveränderliche GUID ab, die das soziale Netzwerk darstellt.</span><span class="sxs-lookup"><span data-stu-id="97231-110">[ISocialProvider::SocialNetworkGuid](isocialprovider-socialnetworkguid.md) —The OSC gets an immutable GUID that represents the social network.</span></span> 
    
5. <span data-ttu-id="97231-111">[ISocialProvider:: getCapabilities](isocialprovider-getcapabilities.md) – osc Ruft eine Zeichenfolge ab, die die Funktionen des Anbieters darstellt und die der Schema Definition für das **Capabilities** -Element entspricht.</span><span class="sxs-lookup"><span data-stu-id="97231-111">[ISocialProvider::GetCapabilities](isocialprovider-getcapabilities.md) —The OSC gets a string that represents the provider's capabilities and that complies with the schema definition for the **capabilities** element.</span></span> 
    
6. <span data-ttu-id="97231-112">[ISocialProvider:: SocialNetworkIcon](isocialprovider-socialnetworkicon.md) – osc Ruft ein Bytearray ab, das das Symbol für die soziale Netzwerk Website darstellt.</span><span class="sxs-lookup"><span data-stu-id="97231-112">[ISocialProvider::SocialNetworkIcon](isocialprovider-socialnetworkicon.md) —The OSC gets a byte array that represents the icon for the social network site.</span></span> 
    
7. <span data-ttu-id="97231-113">[ISocialProvider:: getSession](isocialprovider-getsession.md) – der osc Ruft eine [ISocialSession](isocialsessioniunknown.md) -Schnittstelle ab.</span><span class="sxs-lookup"><span data-stu-id="97231-113">[ISocialProvider::GetSession](isocialprovider-getsession.md) —The OSC gets an [ISocialSession](isocialsessioniunknown.md) interface.</span></span> 
    
8. <span data-ttu-id="97231-114">[ISocialSession:: Anmeldung](isocialsession-logon.md) -osc meldet den Benutzer mithilfe des angegebenen Benutzernamens und Kennworts an der Website für soziale Netzwerke an.</span><span class="sxs-lookup"><span data-stu-id="97231-114">[ISocialSession::Logon](isocialsession-logon.md) —The OSC logs the user on to the social network site by using the specified user name and password.</span></span> 
    
9. <span data-ttu-id="97231-115">[ISocialSession:: GetLoggedOnUser](isocialsession-getloggedonuser.md) – osc Ruft eine [ISocialProfile](isocialprovideriunknown.md) -Schnittstelle ab, die den angemeldeten Benutzer darstellt.</span><span class="sxs-lookup"><span data-stu-id="97231-115">[ISocialSession::GetLoggedOnUser](isocialsession-getloggedonuser.md) —The OSC gets an [ISocialProfile](isocialprovideriunknown.md) interface that represents the logged-on user.</span></span> 
    
10. <span data-ttu-id="97231-116">[ISocialSession:: GetNetworkIdentifier](isocialsession-getnetworkidentifier.md) – osc Ruft eine Zeichenfolge ab, die einen eindeutigen Bezeichner für eine soziale Netzwerk Website darstellt.</span><span class="sxs-lookup"><span data-stu-id="97231-116">[ISocialSession::GetNetworkIdentifier](isocialsession-getnetworkidentifier.md) —The OSC gets a string that represents a unique identifier for a social network site.</span></span> <span data-ttu-id="97231-117">Die Netzwerk-ID kann dem Netzwerknamen entsprechen.</span><span class="sxs-lookup"><span data-stu-id="97231-117">The network identifier can be equivalent to the network name.</span></span> 
    
## <a name="see-also"></a><span data-ttu-id="97231-118">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="97231-118">See also</span></span>

- [<span data-ttu-id="97231-119">XML für Funktionen</span><span class="sxs-lookup"><span data-stu-id="97231-119">XML for Capabilities</span></span>](xml-for-capabilities.md)
- [<span data-ttu-id="97231-120">OSC - Typische Aufrufsequenzen</span><span class="sxs-lookup"><span data-stu-id="97231-120">OSC Typical Calling Sequences</span></span>](osc-typical-calling-sequences.md)

