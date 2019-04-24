---
title: Bewährte Methoden für die Entwicklung eines Anbieters
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 22e3de8a-c4f2-41a4-a5b1-c5b1bf06f724
description: 'Beachten Sie beim Entwickeln eines Outlook Social Connector 2013 (OSC)-Anbieters die folgenden Methoden:'
ms.openlocfilehash: 6a48a56d8065fb9a176ca6527340c99551cdb52a
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32281237"
---
# <a name="best-practices-for-developing-a-provider"></a><span data-ttu-id="d87b0-103">Bewährte Methoden für die Entwicklung eines Anbieters</span><span class="sxs-lookup"><span data-stu-id="d87b0-103">Best practices for developing a provider</span></span>

<span data-ttu-id="d87b0-104">Beachten Sie beim Entwickeln eines Outlook Social Connector 2013 (OSC)-Anbieters die folgenden Methoden:</span><span class="sxs-lookup"><span data-stu-id="d87b0-104">You should adhere to the following practices when you develop an Outlook Social Connector 2013 (OSC) provider:</span></span>
  
- <span data-ttu-id="d87b0-105">Aus Sicherheitsgründen sollten Anbieter, die mit Servern über das Internet kommunizieren, das HTTPS (Hypertext Transfer Protocol (HTTP) mit Secure Socket Layer (SSL))-Protokoll verwenden.</span><span class="sxs-lookup"><span data-stu-id="d87b0-105">For security reasons, providers that communicate with servers over the Internet should use the HTTPS (Hypertext Transfer Protocol (HTTP) with Secure Socket Layer (SSL)) protocol.</span></span> <span data-ttu-id="d87b0-106">Andernfalls besteht das Risiko, dass e-Mail-Adressen, Aktivitäten für soziale Netzwerke und andere Benutzerdaten während der Übertragung abgefangen oder offen gelegt werden können.</span><span class="sxs-lookup"><span data-stu-id="d87b0-106">Otherwise, there is a risk that email addresses, social network activities, and other user data could be intercepted or exposed while in transit.</span></span>
    
- <span data-ttu-id="d87b0-107">Wenn Sie einen OSC-Anbieter für ein soziales Netzwerk eines Drittanbieters entwickeln, muss Ihr Anbieter die Nutzungsbedingungen für das soziale Netzwerk einhalten.</span><span class="sxs-lookup"><span data-stu-id="d87b0-107">If you are developing an OSC provider for a third-party social network, your provider must adhere to the social network's terms of service.</span></span>
    
- <span data-ttu-id="d87b0-108">Um die Größe des Anbieter-Downloadpakets zu minimieren, erstellen Sie den Anbieter mit einem systemeigenen Compiler wie C++ oder einem anderen Tool, das eine COM-Komponente erstellen kann.</span><span class="sxs-lookup"><span data-stu-id="d87b0-108">To minimize the size of the provider download package, build the provider by using a native compiler such as C++ or any other tool that can build a COM component.</span></span>
    
- <span data-ttu-id="d87b0-109">Erstellen Sie in Ihrem Anbieter einen eindeutigen Benutzer-Agent, der an das soziale Netzwerk gesendet wird, um Anrufe des Anbieters an das soziale Netzwerk nachzuverfolgen.</span><span class="sxs-lookup"><span data-stu-id="d87b0-109">In your provider, create a unique user agent that is sent to the social network to track calls made by the provider to the social network.</span></span>
    
- <span data-ttu-id="d87b0-110">Die [ISocialProvider:: getCapabilities](isocialprovider-getcapabilities.md) -Methode sollte sich nicht darauf verlassen, das soziale Netzwerk über das Internet aufzurufen, um die Funktionen des Anbieters zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="d87b0-110">The [ISocialProvider::GetCapabilities](isocialprovider-getcapabilities.md) method should not rely on calling the social network over the Internet to get the capabilities of the provider.</span></span> <span data-ttu-id="d87b0-111">Beispielsweise können Benutzer Outlook offline starten; Wenn der OSC **getCapabilities** aufruft und keine Netzwerkverbindung besteht, gibt der getCapabilities-Aufruf keine gültigen XML- **Funktionen** zurück. \*\*\*\*</span><span class="sxs-lookup"><span data-stu-id="d87b0-111">For example, users can start Outlook offline; if the OSC calls **GetCapabilities** and there is no network connection, the **GetCapabilities** call will not return valid **capabilities** XML.</span></span> <span data-ttu-id="d87b0-112">Die bewährte Methode besteht darin, XML- **Funktionen** als Ressource in Ihrem Anbieter zu speichern.</span><span class="sxs-lookup"><span data-stu-id="d87b0-112">The best practice is to store **capabilities** XML as a resource in your provider.</span></span> 
    
- <span data-ttu-id="d87b0-113">Ihr OSC-Anbieter kann eine beträchtliche Anzahl von Anrufen an ein soziales Netzwerk generieren.</span><span class="sxs-lookup"><span data-stu-id="d87b0-113">Your OSC provider can generate a significant volume of calls to a social network.</span></span> <span data-ttu-id="d87b0-114">Ziehen Sie in Abhängigkeit von den Nutzungsbedingungen für Ihr soziales Netzwerk das Zwischenspeichern von Freunden in einen Outlook-Ordner in Betracht, um die Anzahl von Anrufen vom OSC zu Ihrem Anbieter zu verringern, und zwar von Ihrem Anbieter zum sozialen Netzwerk.</span><span class="sxs-lookup"><span data-stu-id="d87b0-114">Depending on the terms of service for your social network, consider caching friends to an Outlook folder to reduce the number of calls from the OSC to your provider and, in turn, from your provider to the social network.</span></span>
    
- <span data-ttu-id="d87b0-115">Office 2013 ist sowohl in 32-Bit-als auch in 64-Bit-Versionen verfügbar.</span><span class="sxs-lookup"><span data-stu-id="d87b0-115">Office 2013 is available in both 32-bit and 64-bit versions.</span></span> <span data-ttu-id="d87b0-116">Versionen von Office vor Office 2010 sind nur in einer 32-Bit-Version verfügbar.</span><span class="sxs-lookup"><span data-stu-id="d87b0-116">Versions of Office prior to Office 2010 are available only in a 32-bit version.</span></span> <span data-ttu-id="d87b0-117">Die Standardinstallation von Office 2013 auf 64-Bit-Windows ist 32-Bit.</span><span class="sxs-lookup"><span data-stu-id="d87b0-117">The default installation of Office 2013 on 64-bit Windows is 32-bit.</span></span> <span data-ttu-id="d87b0-118">Wenn Sie die 64-Bit-Version des mit 64-Bit Office 2013 installierten OSC unterstützen möchten, müssen Sie auch eine 64-Bit-Version Ihres Anbieters freigeben.</span><span class="sxs-lookup"><span data-stu-id="d87b0-118">If you intend to support the 64-bit version of the OSC that is installed with 64-bit Office 2013, you must also release a 64-bit version of your provider.</span></span> 
    
## <a name="see-also"></a><span data-ttu-id="d87b0-119">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="d87b0-119">See also</span></span>

- [<span data-ttu-id="d87b0-120">OSC - Typische Aufrufsequenzen</span><span class="sxs-lookup"><span data-stu-id="d87b0-120">OSC Typical Calling Sequences</span></span>](osc-typical-calling-sequences.md)  
- [<span data-ttu-id="d87b0-121">Entwickeln eines Providers mit dem OSC-XML-Schema</span><span class="sxs-lookup"><span data-stu-id="d87b0-121">Developing a Provider with the OSC XML Schema</span></span>](developing-a-provider-with-the-osc-xml-schema.md)  
- [<span data-ttu-id="d87b0-122">Bereitstellen eines Providers</span><span class="sxs-lookup"><span data-stu-id="d87b0-122">Deploying a Provider</span></span>](deploying-a-provider.md)  
- [<span data-ttu-id="d87b0-123">Erste Schritte zum Entwickeln eines Outlook Connector Providers für soziale Netzwerke</span><span class="sxs-lookup"><span data-stu-id="d87b0-123">Getting Started with Developing an Outlook Social Connector Provider</span></span>](getting-started-with-developing-an-outlook-social-connector-provider.md)

