---
title: Entwickeln eines Providers mit dem OSC-XML-Schema
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 0872b1b9-c21f-4bba-8cf1-4b010d8d7fb6
description: Das Connector für soziale Netzwerke (OSC)-Anbieter-XML-Schema definiert das Format einer bedeutenden Menge an Informationen, die von einem sozialen Netzwerk über den osc-Anbieter des Netzwerks an den osc übergeben wird.
ms.openlocfilehash: 2346e23beb2de1664ec90263a8f5db5d46c54e6f
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/29/2019
ms.locfileid: "34539255"
---
# <a name="developing-a-provider-with-the-osc-xml-schema"></a><span data-ttu-id="82065-103">Entwickeln eines Providers mit dem OSC-XML-Schema</span><span class="sxs-lookup"><span data-stu-id="82065-103">Developing a provider with the OSC XML schema</span></span>

<span data-ttu-id="82065-104">Das Connector für soziale Netzwerke (OSC)-Anbieter-XML-Schema definiert das Format einer bedeutenden Menge an Informationen, die von einem sozialen Netzwerk über den osc-Anbieter des Netzwerks an den osc übergeben wird.</span><span class="sxs-lookup"><span data-stu-id="82065-104">The Outlook Social Connector (OSC) provider XML schema defines the format of a significant amount of information that is passed from a social network through the network's OSC provider to the OSC.</span></span> <span data-ttu-id="82065-105">Mit dem XML-Schema kann ein osc-Anbieter Funktionen des Anbieters, der Freunde und der Aktivitätsfeed-Elemente im sozialen Netzwerk mithilfe der drei Hauptelemente, **Funktionen**, **Freunde**und **activityFeed**und ihres untergeordneten Elements angeben. Elemente.</span><span class="sxs-lookup"><span data-stu-id="82065-105">The XML schema allows an OSC provider to specify capabilities of the provider, friends, and activity feed items on the social network, by using the three main elements, **capabilities**, **friends**, and **activityFeed**, and their child elements.</span></span> <span data-ttu-id="82065-106">Der osc-Anbieter implementiert Schnittstellen und deren Methoden in der Erweiterbarkeit des osc-Anbieters und gibt XML-Zeichenfolgen als Ausgabeparameter zurück, die dem XML-Schema des osc-Anbieters entsprechen.</span><span class="sxs-lookup"><span data-stu-id="82065-106">The OSC provider implements interfaces and their methods in the OSC provider extensibility, returning XML strings as output parameters that comply with the OSC provider XML schema.</span></span> <span data-ttu-id="82065-107">Der osc ruft diese Methoden auf, um Informationen zu erhalten, die er gemäß Definition des XML-Schemas verstehen kann.</span><span class="sxs-lookup"><span data-stu-id="82065-107">The OSC calls these methods to obtain information that it can understand as defined by the XML schema.</span></span>
  
> [!NOTE]
> <span data-ttu-id="82065-108">OSC-Anbieter Erweiterbarkeit unterstützt das Debuggen `DebugProviders` von Anbietern, `HKEY_CURRENT_USER\Software\Microsoft\Office\Outlook\SocialConnector` indem der Wert des Registrierungsschlüssels auf 1 festgesetzt wird.</span><span class="sxs-lookup"><span data-stu-id="82065-108">OSC provider extensibility supports debugging providers by setting the `DebugProviders` value of the  `HKEY_CURRENT_USER\Software\Microsoft\Office\Outlook\SocialConnector` registry key to 1.</span></span> <span data-ttu-id="82065-109">Wenn Sie das Anbieter Debugging aktivieren, überprüft der osc den Anbieter-XML-Code anhand der Version des osc-XML-Schemas, das Sie im **xmlns** XML-Attribut angeben.</span><span class="sxs-lookup"><span data-stu-id="82065-109">When you turn on provider debugging, the OSC validates the provider XML against the version of the OSC XML schema that you specify in the **xmlns** XML attribute.</span></span> <span data-ttu-id="82065-110">Geben Sie für osc 1,1 und Versionen von OSC seit Outlook Connector für soziale Netzwerke 2013 das **xmlns** -Attribut wie folgt an:`xmlns="http://schemas.microsoft.com/office/outlook/2010/06/socialprovider.xsd"`</span><span class="sxs-lookup"><span data-stu-id="82065-110">For OSC 1.1 and versions of the OSC since Outlook Social Connector 2013, specify the **xmlns** attribute as follows: `xmlns="http://schemas.microsoft.com/office/outlook/2010/06/socialprovider.xsd"`</span></span>
  
## <a name="in-this-section"></a><span data-ttu-id="82065-111">Inhalt dieses Abschnitts</span><span class="sxs-lookup"><span data-stu-id="82065-111">In this section</span></span>

- <span data-ttu-id="82065-112">[Synchronisieren von Freunden und Aktivitäten](synchronizing-friends-and-activities.md): Beschreibt die verschiedenen Möglichkeiten, mit denen osc-Anbieter Freunde, nicht-Freunde und Aktivitäten in einem sozialen Netzwerk synchronisieren können.</span><span class="sxs-lookup"><span data-stu-id="82065-112">[Synchronizing Friends and Activities](synchronizing-friends-and-activities.md): Describes the various ways that OSC providers can synchronize friends, non-friends, and activities on a social network.</span></span> 
    
- <span data-ttu-id="82065-113">[Osc-Anbieter-XML-Beispiele](osc-provider-xml-examples.md): enthält XML-Beispiele, in denen gezeigt wird, wie Funktionen eines osc-Anbieters, von Freunden und von Aktivitätsfeed-Elementen in einem sozialen Netzwerk mithilfe des osc-XML-Schemas angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="82065-113">[OSC Provider XML Examples](osc-provider-xml-examples.md): Includes XML examples that show how to specify capabilities of an OSC provider, friends, and activity feed items on a social network by using the OSC XML schema.</span></span>
    
- <span data-ttu-id="82065-114">[XML für Funktionen](xml-for-capabilities.md): erläutert die- [ISocialProvider:: getCapabilities](isocialprovider-getcapabilities.md) -Methode, mit der die osc-Funktionen Informationen abrufen, die in **Capabilities** XML vom osc-Anbieter ausgedrückt werden.</span><span class="sxs-lookup"><span data-stu-id="82065-114">[XML for Capabilities](xml-for-capabilities.md): Explains the - [ISocialProvider::GetCapabilities](isocialprovider-getcapabilities.md) method that the OSC uses to obtain capabilities information, expressed in **capabilities** XML, from the OSC provider.</span></span> <span data-ttu-id="82065-115">In diesem Abschnitt werden außerdem die XML-Elemente im XML-Schema des osc-Anbieters beschrieben, mit denen ein osc-Anbieter seine Funktionalität angeben kann, einschließlich der Authentifizierung von Benutzern und der Synchronisierung von Freunden und Aktivitäten.</span><span class="sxs-lookup"><span data-stu-id="82065-115">This section also describes the XML elements in the OSC provider XML schema that allow an OSC provider to specify its functionality, including how it authenticates users and synchronizes friends and activities.</span></span> 
    
- <span data-ttu-id="82065-116">[XML für Freunde](xml-for-friends.md): enthält Beispiele der APIs, die die osc verwendet, um Freundes Informationen, ausgedrückt in **friends** XML, vom osc-Anbieter zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="82065-116">[XML for Friends](xml-for-friends.md): Gives examples of the APIs that the OSC uses to obtain friends' information, expressed in **friends** XML, from the OSC provider.</span></span> <span data-ttu-id="82065-117">In diesem Abschnitt werden auch Elemente im **friends** -XML-Code beschrieben.</span><span class="sxs-lookup"><span data-stu-id="82065-117">This section also describes elements in the **friends** XML.</span></span> 
    
- <span data-ttu-id="82065-118">[XML for Activities](xml-for-activities.md): enthält Beispiele der APIs, die die osc zum Abrufen von Aktivitätsinformationen verwendet, ausgedrückt in **activityFeed** XML, vom osc-Anbieter.</span><span class="sxs-lookup"><span data-stu-id="82065-118">[XML for Activities](xml-for-activities.md): Gives examples of the APIs that the OSC uses to obtain activities information, expressed in **activityFeed** XML, from the OSC provider.</span></span> <span data-ttu-id="82065-119">In diesem Abschnitt werden außerdem die XML-Elemente im XML-Schema des osc-Anbieters beschrieben, mit denen ein osc-Anbieter einen Aktivitätsfeed angeben kann.</span><span class="sxs-lookup"><span data-stu-id="82065-119">This section also describes the XML elements in the OSC provider XML schema that allow an OSC provider to specify an activity feed.</span></span> <span data-ttu-id="82065-120">Ein Aktivitätsfeed umfasst das Netzwerk, in dem die Aktivitätsfeed-Elemente stammen, Details zu den einzelnen Aktivitätsfeed-Elementen (wie Besitzer, Typ und Veröffentlichungsdatum der Aktivität) und die Vorlage zum Anzeigen der Aktivität.</span><span class="sxs-lookup"><span data-stu-id="82065-120">An activity feed includes the network where the activity feed items originated, details of each activity feed item (such as owner, type, and publish date of the activity), and the template to display the activity.</span></span> 
    
## <a name="reference"></a><span data-ttu-id="82065-121">Referenz</span><span class="sxs-lookup"><span data-stu-id="82065-121">Reference</span></span>

- [<span data-ttu-id="82065-122">Referenz zum Outlook Connector Provider für soziale Netzwerke</span><span class="sxs-lookup"><span data-stu-id="82065-122">Outlook Social Connector Provider Reference</span></span>](outlook-social-connector-provider-reference-0.md)
  
## <a name="related-sections"></a><span data-ttu-id="82065-123">Verwandte Abschnitte</span><span class="sxs-lookup"><span data-stu-id="82065-123">Related sections</span></span>

- [<span data-ttu-id="82065-124">Erste Schritte zum Entwickeln eines Outlook Connector Providers für soziale Netzwerke</span><span class="sxs-lookup"><span data-stu-id="82065-124">Getting Started with Developing an Outlook Social Connector Provider</span></span>](getting-started-with-developing-an-outlook-social-connector-provider.md)
  
- [<span data-ttu-id="82065-125">Über den OSC-Beispielvorlagen</span><span class="sxs-lookup"><span data-stu-id="82065-125">OSC Sample Templates</span></span>](osc-sample-templates.md)
  
- [<span data-ttu-id="82065-126">OSC - Typische Aufrufsequenzen</span><span class="sxs-lookup"><span data-stu-id="82065-126">OSC Typical Calling Sequences</span></span>](osc-typical-calling-sequences.md)
  
- [<span data-ttu-id="82065-127">Debuggen eines Providers</span><span class="sxs-lookup"><span data-stu-id="82065-127">Debugging a Provider</span></span>](debugging-a-provider.md)
  
- [<span data-ttu-id="82065-128">Bereitstellen eines Providers</span><span class="sxs-lookup"><span data-stu-id="82065-128">Deploying a Provider</span></span>](deploying-a-provider.md)
  
- [<span data-ttu-id="82065-129">Bewährte Methoden für die Entwicklung eines Anbieters</span><span class="sxs-lookup"><span data-stu-id="82065-129">Best Practices for Developing a Provider</span></span>](best-practices-for-developing-a-provider.md)
  
## <a name="see-also"></a><span data-ttu-id="82065-130">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="82065-130">See also</span></span>

- [<span data-ttu-id="82065-131">Debuggen eines Providers</span><span class="sxs-lookup"><span data-stu-id="82065-131">Debugging a Provider</span></span>](debugging-a-provider.md)

