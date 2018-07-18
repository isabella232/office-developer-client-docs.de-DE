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
# <a name="forms-based-authentication"></a><span data-ttu-id="9c519-103">Formularbasierte Authentifizierung</span><span class="sxs-lookup"><span data-stu-id="9c519-103">Forms-based authentication</span></span>

<span data-ttu-id="9c519-104">Outlook Social Connector (OSC) die [ISocialProvider::GetCapabilities](isocialprovider-getcapabilities.md) -Methode aufgerufen, um die Funktionen des OSC-Anbieter für soziale Netzwerke bestimmen.</span><span class="sxs-lookup"><span data-stu-id="9c519-104">The Outlook Social Connector (OSC) calls the [ISocialProvider::GetCapabilities](isocialprovider-getcapabilities.md) method to determine the capabilities of the OSC provider for a social network.</span></span> <span data-ttu-id="9c519-105">Die OSC verwendet die zurückgegebenen Funktionen um zu bestimmen, wie einen Office-Benutzer unterstützen, die mit diesem sozialen Netzwerk angemeldet ist.</span><span class="sxs-lookup"><span data-stu-id="9c519-105">The OSC uses the returned capabilities to determine how to support an Office user who is logging on to this social network.</span></span> 

<span data-ttu-id="9c519-106">Wenn das **UseLogonWebAuth** -Element in der zurückgegebenen **Funktionen** XML gibt an, dass der OSC-Anbieter formularbasierte Authentifizierung unterstützt, kann die OSC aufrufende Folgendes zu einem Benutzer ermöglichen, melden Sie sich mit dem sozialen Netzwerk vornehmen:</span><span class="sxs-lookup"><span data-stu-id="9c519-106">If the **useLogonWebAuth** element in the returned **capabilities** XML indicates that the OSC provider supports forms-based authentication, the OSC can make the following calling sequence to allow a user to log on to that social network:</span></span> 
  
1. <span data-ttu-id="9c519-107">[ISocialProvider::Load](isocialprovider-load.md) &ndash; Der OSC lädt den Anbieter.</span><span class="sxs-lookup"><span data-stu-id="9c519-107">[ISocialProvider::Load](isocialprovider-load.md) &ndash; The OSC loads the provider.</span></span> 
    
2. <span data-ttu-id="9c519-108">[ISocialProvider::Version](isocialprovider-version.md) &ndash; Der OSC Ruft eine Zeichenfolge, die die Versionsnummer des Anbieters für diese für soziale Netzwerke darstellt.</span><span class="sxs-lookup"><span data-stu-id="9c519-108">[ISocialProvider::Version](isocialprovider-version.md) &ndash; The OSC gets a string that represents the version number of the provider for this social network.</span></span> 
    
3. <span data-ttu-id="9c519-109">[ISocialProvider::SocialNetworkName](isocialprovider-socialnetworkname.md) &ndash; Der OSC Ruft eine Zeichenfolge, die den Namen für soziale Netzwerke darstellt.</span><span class="sxs-lookup"><span data-stu-id="9c519-109">[ISocialProvider::SocialNetworkName](isocialprovider-socialnetworkname.md) &ndash; The OSC gets a string that represents the social network name.</span></span> 
    
4. <span data-ttu-id="9c519-110">[ISocialProvider::SocialNetworkGuid](isocialprovider-socialnetworkguid.md) &ndash; Der OSC dient zum Abrufen einer unveränderlichen GUID, die für soziale Netzwerke darstellt.</span><span class="sxs-lookup"><span data-stu-id="9c519-110">[ISocialProvider::SocialNetworkGuid](isocialprovider-socialnetworkguid.md) &ndash; The OSC gets an immutable GUID that represents the social network.</span></span> 
    
5. <span data-ttu-id="9c519-111">[ISocialProvider::GetCapabilities](isocialprovider-getcapabilities.md) &ndash; Der OSC Ruft eine Zeichenfolge, die die Funktionen des Providers darstellt, die die Schemadefinition für das **Capabilities** -Element entspricht.</span><span class="sxs-lookup"><span data-stu-id="9c519-111">[ISocialProvider::GetCapabilities](isocialprovider-getcapabilities.md) &ndash; The OSC gets a string that represents the provider's capabilities and that complies with the schema definition for the **capabilities** element.</span></span> 
    
6. <span data-ttu-id="9c519-112">[ISocialProvider::SocialNetworkIcon](isocialprovider-socialnetworkicon.md) &ndash; Der OSC Ruft ein Bytearray, das Symbol für die Website für soziale Netzwerke darstellt.</span><span class="sxs-lookup"><span data-stu-id="9c519-112">[ISocialProvider::SocialNetworkIcon](isocialprovider-socialnetworkicon.md) &ndash; The OSC gets a byte array that represents the icon for the social network site.</span></span> 
    
7. <span data-ttu-id="9c519-113">[ISocialProvider::GetSession](isocialprovider-getsession.md) &ndash; Der OSC Ruft eine [ISocialSession](isocialsessioniunknown.md) -Schnittstelle.</span><span class="sxs-lookup"><span data-stu-id="9c519-113">[ISocialProvider::GetSession](isocialprovider-getsession.md) &ndash; The OSC gets an [ISocialSession](isocialsessioniunknown.md) interface.</span></span> 
    
8. <span data-ttu-id="9c519-114">[ISocialSession::LogonWeb](isocialsession-logonweb.md) &ndash; Der OSC initialisiert Anmelden bei der Website für soziale Netzwerke durch die formularbasierte Authentifizierung.</span><span class="sxs-lookup"><span data-stu-id="9c519-114">[ISocialSession::LogonWeb](isocialsession-logonweb.md) &ndash; The OSC initializes logging on to the social network site by forms-based authentication.</span></span> <span data-ttu-id="9c519-115">Für diesen ersten Anmeldung Aufruf übergibt die OSC **null** für den Parameter _ConnectIn_ .</span><span class="sxs-lookup"><span data-stu-id="9c519-115">For this initial logon call, the OSC passes **null** for the  _connectIn_ parameter.</span></span> 
    
9. <span data-ttu-id="9c519-116">[ISocialSession::GetLogonUrl](isocialsession-getlogonurl.md) &ndash; Der OSC Ruft die URL zu einem Formular browserbasierte während der Webauthentifizierung für den Benutzer anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="9c519-116">[ISocialSession::GetLogonUrl](isocialsession-getlogonurl.md) &ndash; The OSC gets the URL to display a browser-based form to the user during web authentication.</span></span> 
    
10. <span data-ttu-id="9c519-117">[ISocialSession::LogonWeb](isocialsession-logonweb.md) &ndash; Der OSC beendet die Anmeldung bei der Website für soziale Netzwerke mithilfe der formularbasierten Authentifizierung.</span><span class="sxs-lookup"><span data-stu-id="9c519-117">[ISocialSession::LogonWeb](isocialsession-logonweb.md) &ndash; The OSC completes the logon to the social network site by using forms-based authentication.</span></span> <span data-ttu-id="9c519-118">Die OSC ruft diese Methode ein zweites Mal die URL des Formulars Anmeldung an dem Anbieter in der _ConnectIn_ -Parameter übergeben.</span><span class="sxs-lookup"><span data-stu-id="9c519-118">The OSC calls this method a second time, passing the URL of the logon form to the provider in the  _connectIn_ parameter.</span></span> 
    
11. <span data-ttu-id="9c519-119">[ISocialSession::GetLoggedOnUser](isocialsession-getloggedonuser.md) &ndash; Der OSC Ruft eine [ISocialProfile](isocialprovideriunknown.md) -Schnittstelle, die den angemeldeten Benutzer darstellt.</span><span class="sxs-lookup"><span data-stu-id="9c519-119">[ISocialSession::GetLoggedOnUser](isocialsession-getloggedonuser.md) &ndash; The OSC gets an [ISocialProfile](isocialprovideriunknown.md) interface that represents the logged-on user.</span></span> 
    
12. <span data-ttu-id="9c519-120">[ISocialSession::GetNetworkIdentifier](isocialsession-getnetworkidentifier.md) &ndash; Der OSC Ruft eine Zeichenfolge, die einen eindeutigen Bezeichner für eine Website für soziale Netzwerke darstellt.</span><span class="sxs-lookup"><span data-stu-id="9c519-120">[ISocialSession::GetNetworkIdentifier](isocialsession-getnetworkidentifier.md) &ndash; The OSC gets a string that represents a unique identifier for a social network site.</span></span> <span data-ttu-id="9c519-121">Die Netzwerk-ID kann den Namen des Netzwerks entsprechen.</span><span class="sxs-lookup"><span data-stu-id="9c519-121">The network identifier can be equivalent to the network name.</span></span> 
    
## <a name="see-also"></a><span data-ttu-id="9c519-122">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="9c519-122">See also</span></span>

- [<span data-ttu-id="9c519-123">XML-Code für Funktionen</span><span class="sxs-lookup"><span data-stu-id="9c519-123">XML for Capabilities</span></span>](xml-for-capabilities.md)
- [<span data-ttu-id="9c519-124">OSC - Typische Aufrufsequenzen</span><span class="sxs-lookup"><span data-stu-id="9c519-124">OSC Typical Calling Sequences</span></span>](osc-typical-calling-sequences.md)

