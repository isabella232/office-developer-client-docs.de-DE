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
# <a name="basic-authentication"></a><span data-ttu-id="229e6-103">Standardauthentifizierung</span><span class="sxs-lookup"><span data-stu-id="229e6-103">Basic authentication</span></span>

<span data-ttu-id="229e6-104">Outlook Social Connector (OSC) die [ISocialProvider::GetCapabilities](isocialprovider-getcapabilities.md) -Methode aufgerufen, um die Funktionen des OSC-Anbieter für soziale Netzwerke bestimmen.</span><span class="sxs-lookup"><span data-stu-id="229e6-104">The Outlook Social Connector (OSC) calls the [ISocialProvider::GetCapabilities](isocialprovider-getcapabilities.md) method to determine the capabilities of the OSC provider for a social network.</span></span> <span data-ttu-id="229e6-105">Die OSC verwendet die zurückgegebenen Funktionen um zu bestimmen, wie einen Office-Benutzer unterstützen, die mit diesem sozialen Netzwerk angemeldet ist.</span><span class="sxs-lookup"><span data-stu-id="229e6-105">The OSC uses the returned capabilities to determine how to support an Office user who is logging on to this social network.</span></span> <span data-ttu-id="229e6-106">Wenn das **UseLogonWebAuth** -Element in der zurückgegebenen **Funktionen** XML gibt an, dass der OSC-Anbieter Standardauthentifizierung unterstützt, kann die OSC aufrufende Folgendes zu einem Benutzer ermöglichen, melden Sie sich mit dem sozialen Netzwerk vornehmen:</span><span class="sxs-lookup"><span data-stu-id="229e6-106">If the **useLogonWebAuth** element in the returned **capabilities** XML indicates that the OSC provider supports basic authentication, the OSC can make the following calling sequence to allow a user to log on to that social network:</span></span> 
  
1. <span data-ttu-id="229e6-107">[ISocialProvider::Load](isocialprovider-load.md) – die OSC lädt den Anbieter.</span><span class="sxs-lookup"><span data-stu-id="229e6-107">[ISocialProvider::Load](isocialprovider-load.md) —The OSC loads the provider.</span></span> 
    
2. <span data-ttu-id="229e6-108">[ISocialProvider::Version](isocialprovider-version.md) – die OSC Ruft eine Zeichenfolge, die die Versionsnummer des OSC-Providers darstellt.</span><span class="sxs-lookup"><span data-stu-id="229e6-108">[ISocialProvider::Version](isocialprovider-version.md) —The OSC gets a string that represents the version number of the OSC provider.</span></span> 
    
3. <span data-ttu-id="229e6-109">[ISocialProvider::SocialNetworkName](isocialprovider-socialnetworkname.md) – die OSC Ruft eine Zeichenfolge, die den Namen für soziale Netzwerke darstellt.</span><span class="sxs-lookup"><span data-stu-id="229e6-109">[ISocialProvider::SocialNetworkName](isocialprovider-socialnetworkname.md) —The OSC gets a string that represents the social network name.</span></span> 
    
4. <span data-ttu-id="229e6-110">[ISocialProvider::SocialNetworkGuid](isocialprovider-socialnetworkguid.md) – die OSC dient zum Abrufen einer unveränderlichen GUID, die für soziale Netzwerke darstellt.</span><span class="sxs-lookup"><span data-stu-id="229e6-110">[ISocialProvider::SocialNetworkGuid](isocialprovider-socialnetworkguid.md) —The OSC gets an immutable GUID that represents the social network.</span></span> 
    
5. <span data-ttu-id="229e6-111">[ISocialProvider::GetCapabilities](isocialprovider-getcapabilities.md) – die OSC Ruft eine Zeichenfolge, die die Funktionen des Providers darstellt, die die Schemadefinition für das **Capabilities** -Element entspricht.</span><span class="sxs-lookup"><span data-stu-id="229e6-111">[ISocialProvider::GetCapabilities](isocialprovider-getcapabilities.md) —The OSC gets a string that represents the provider's capabilities and that complies with the schema definition for the **capabilities** element.</span></span> 
    
6. <span data-ttu-id="229e6-112">[ISocialProvider::SocialNetworkIcon](isocialprovider-socialnetworkicon.md) – die OSC Ruft ein Bytearray, das Symbol für die Website für soziale Netzwerke darstellt.</span><span class="sxs-lookup"><span data-stu-id="229e6-112">[ISocialProvider::SocialNetworkIcon](isocialprovider-socialnetworkicon.md) —The OSC gets a byte array that represents the icon for the social network site.</span></span> 
    
7. <span data-ttu-id="229e6-113">[ISocialProvider::GetSession](isocialprovider-getsession.md) – die OSC Ruft eine [ISocialSession](isocialsessioniunknown.md) -Schnittstelle.</span><span class="sxs-lookup"><span data-stu-id="229e6-113">[ISocialProvider::GetSession](isocialprovider-getsession.md) —The OSC gets an [ISocialSession](isocialsessioniunknown.md) interface.</span></span> 
    
8. <span data-ttu-id="229e6-114">[ISocialSession::Logon](isocialsession-logon.md) – die OSC meldet den Benutzer bei der Website für soziale Netzwerke mithilfe der angegebenen Benutzernamen und Kennwort.</span><span class="sxs-lookup"><span data-stu-id="229e6-114">[ISocialSession::Logon](isocialsession-logon.md) —The OSC logs the user on to the social network site by using the specified user name and password.</span></span> 
    
9. <span data-ttu-id="229e6-115">[ISocialSession::GetLoggedOnUser](isocialsession-getloggedonuser.md) – die OSC Ruft eine [ISocialProfile](isocialprovideriunknown.md) -Schnittstelle, die den angemeldeten Benutzer darstellt.</span><span class="sxs-lookup"><span data-stu-id="229e6-115">[ISocialSession::GetLoggedOnUser](isocialsession-getloggedonuser.md) —The OSC gets an [ISocialProfile](isocialprovideriunknown.md) interface that represents the logged-on user.</span></span> 
    
10. <span data-ttu-id="229e6-116">[ISocialSession::GetNetworkIdentifier](isocialsession-getnetworkidentifier.md) – die OSC Ruft eine Zeichenfolge, die einen eindeutigen Bezeichner für eine Website für soziale Netzwerke darstellt.</span><span class="sxs-lookup"><span data-stu-id="229e6-116">[ISocialSession::GetNetworkIdentifier](isocialsession-getnetworkidentifier.md) —The OSC gets a string that represents a unique identifier for a social network site.</span></span> <span data-ttu-id="229e6-117">Die Netzwerk-ID kann den Namen des Netzwerks entsprechen.</span><span class="sxs-lookup"><span data-stu-id="229e6-117">The network identifier can be equivalent to the network name.</span></span> 
    
## <a name="see-also"></a><span data-ttu-id="229e6-118">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="229e6-118">See also</span></span>

- [<span data-ttu-id="229e6-119">XML-Code für Funktionen</span><span class="sxs-lookup"><span data-stu-id="229e6-119">XML for Capabilities</span></span>](xml-for-capabilities.md)
- [<span data-ttu-id="229e6-120">OSC - Typische Aufrufsequenzen</span><span class="sxs-lookup"><span data-stu-id="229e6-120">OSC Typical Calling Sequences</span></span>](osc-typical-calling-sequences.md)

