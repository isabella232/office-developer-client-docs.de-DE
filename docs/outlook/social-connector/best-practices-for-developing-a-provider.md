---
title: Bewährte Methoden für das Entwickeln eines Providers
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 22e3de8a-c4f2-41a4-a5b1-c5b1bf06f724
description: 'Sie sollten die folgenden Methoden bei der Entwicklung eines Outlook Social Connector 2013 (OSC)-Anbieters erfüllen:'
ms.openlocfilehash: a6ee9d54f33bbc855d178aba844a8f65ec92f964
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19795950"
---
# <a name="best-practices-for-developing-a-provider"></a><span data-ttu-id="87142-103">Bewährte Methoden für das Entwickeln eines Providers</span><span class="sxs-lookup"><span data-stu-id="87142-103">Best practices for developing a provider</span></span>

<span data-ttu-id="87142-104">Sie sollten die folgenden Methoden bei der Entwicklung eines Outlook Social Connector 2013 (OSC)-Anbieters erfüllen:</span><span class="sxs-lookup"><span data-stu-id="87142-104">You should adhere to the following practices when you develop an Outlook Social Connector 2013 (OSC) provider:</span></span>
  
- <span data-ttu-id="87142-105">Aus Sicherheitsgründen sollten Rollenanbieter, die Kommunikation über das Internet mit Servern das Protokoll HTTPS (Hypertext Transfer Protocol (HTTP) mit Secure Socket Layer (SSL)) verwenden.</span><span class="sxs-lookup"><span data-stu-id="87142-105">For security reasons, providers that communicate with servers over the Internet should use the HTTPS (Hypertext Transfer Protocol (HTTP) with Secure Socket Layer (SSL)) protocol.</span></span> <span data-ttu-id="87142-106">Anderenfalls besteht ein Risiko dar, ob e-Mail-Adressen, Aktivitäten für soziale Netzwerke und anderer Benutzer Daten abgefangen oder unterwegs verfügbar gemacht werden können.</span><span class="sxs-lookup"><span data-stu-id="87142-106">Otherwise, there is a risk that email addresses, social network activities, and other user data could be intercepted or exposed while in transit.</span></span>
    
- <span data-ttu-id="87142-107">Wenn Sie einen OSC-Anbieter für ein Drittanbieter-soziales Netzwerk entwickeln, muss der Anbieter Vertragsbedingungen für das soziale Netzwerk entsprechen.</span><span class="sxs-lookup"><span data-stu-id="87142-107">If you are developing an OSC provider for a third-party social network, your provider must adhere to the social network's terms of service.</span></span>
    
- <span data-ttu-id="87142-108">Um die Größe des Downloadpakets Anbieter zu minimieren, erstellen Sie den Anbieter mit einem systemeigenen Compiler wie C++ oder ein anderes Programm, das eine COM-Komponente erstellen kann.</span><span class="sxs-lookup"><span data-stu-id="87142-108">To minimize the size of the provider download package, build the provider by using a native compiler such as C++ or any other tool that can build a COM component.</span></span>
    
- <span data-ttu-id="87142-109">Erstellen Sie in Ihren Anbieter einen eindeutigen Benutzer-Agent, der zum Nachverfolgen von Aufrufe durch den Anbieter für soziale Netzwerke in sozialen Netzwerken gesendet wird.</span><span class="sxs-lookup"><span data-stu-id="87142-109">In your provider, create a unique user agent that is sent to the social network to track calls made by the provider to the social network.</span></span>
    
- <span data-ttu-id="87142-110">Die Methode [ISocialProvider::GetCapabilities](isocialprovider-getcapabilities.md) sollten nicht zum Aufrufen von sozialen Netzwerk über das Internet zum Abrufen der Funktionalität des Anbieters verlassen.</span><span class="sxs-lookup"><span data-stu-id="87142-110">The [ISocialProvider::GetCapabilities](isocialprovider-getcapabilities.md) method should not rely on calling the social network over the Internet to get the capabilities of the provider.</span></span> <span data-ttu-id="87142-111">Beispielsweise können Benutzer offline Starten von Outlook; Wenn die OSC- **GetCapabilities Anrufe** , und es keine Verbindung zum Netzwerk wird, wird der Anruf **GetCapabilities** keine gültige **Funktionen** XML zurück.</span><span class="sxs-lookup"><span data-stu-id="87142-111">For example, users can start Outlook offline; if the OSC calls **GetCapabilities** and there is no network connection, the **GetCapabilities** call will not return valid **capabilities** XML.</span></span> <span data-ttu-id="87142-112">Bewährt hat sich zum Speichern von **Funktionen** XML als Ressource in Ihrem Anbieter.</span><span class="sxs-lookup"><span data-stu-id="87142-112">The best practice is to store **capabilities** XML as a resource in your provider.</span></span> 
    
- <span data-ttu-id="87142-113">Ihre OSC-Anbieter kann Anrufe mit einem sozialen Netzwerk umfangreichem generieren.</span><span class="sxs-lookup"><span data-stu-id="87142-113">Your OSC provider can generate a significant volume of calls to a social network.</span></span> <span data-ttu-id="87142-114">Erwägen Sie je nach der rechtlichen Hinweise für das soziale Netzwerk Zwischenspeichern Freunde zu einem Outlook-Ordner, um die Anzahl der Anrufe von der OSC an Ihren Anbieter und wiederum von Ihrem Anbieter in sozialen Netzwerken reduziert.</span><span class="sxs-lookup"><span data-stu-id="87142-114">Depending on the terms of service for your social network, consider caching friends to an Outlook folder to reduce the number of calls from the OSC to your provider and, in turn, from your provider to the social network.</span></span>
    
- <span data-ttu-id="87142-115">Office 2013 ist in 32-Bit- und 64-Bit-Versionen verfügbar.</span><span class="sxs-lookup"><span data-stu-id="87142-115">Office 2013 is available in both 32-bit and 64-bit versions.</span></span> <span data-ttu-id="87142-116">Office prior to Office 2010-Versionen stehen nur in einer 32-Bit-Version zur Verfügung.</span><span class="sxs-lookup"><span data-stu-id="87142-116">Versions of Office prior to Office 2010 are available only in a 32-bit version.</span></span> <span data-ttu-id="87142-117">Die Standardinstallation von Office 2013 64-Bit-Version von Windows ist 32-Bit.</span><span class="sxs-lookup"><span data-stu-id="87142-117">The default installation of Office 2013 on 64-bit Windows is 32-bit.</span></span> <span data-ttu-id="87142-118">Wenn Sie beabsichtigen, die 64-Bit-Version von der OSC zu unterstützen, die mit Office 2013 64-Bit-Version installiert ist, müssen Sie auch eine 64-Bit-Version des Anbieters freigeben.</span><span class="sxs-lookup"><span data-stu-id="87142-118">If you intend to support the 64-bit version of the OSC that is installed with 64-bit Office 2013, you must also release a 64-bit version of your provider.</span></span> 
    
## <a name="see-also"></a><span data-ttu-id="87142-119">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="87142-119">See also</span></span>

- [<span data-ttu-id="87142-120">OSC - Typische Aufrufsequenzen</span><span class="sxs-lookup"><span data-stu-id="87142-120">OSC Typical Calling Sequences</span></span>](osc-typical-calling-sequences.md)  
- [<span data-ttu-id="87142-121">Entwickeln eines Providers mit dem OSC-XML-Schema</span><span class="sxs-lookup"><span data-stu-id="87142-121">Developing a Provider with the OSC XML Schema</span></span>](developing-a-provider-with-the-osc-xml-schema.md)  
- [<span data-ttu-id="87142-122">Bereitstellen eines Providers</span><span class="sxs-lookup"><span data-stu-id="87142-122">Deploying a Provider</span></span>](deploying-a-provider.md)  
- [<span data-ttu-id="87142-123">Erste Schritte zum Entwickeln eines Outlook Connector Providers für soziale Netzwerke</span><span class="sxs-lookup"><span data-stu-id="87142-123">Getting Started with Developing an Outlook Social Connector Provider</span></span>](getting-started-with-developing-an-outlook-social-connector-provider.md)

