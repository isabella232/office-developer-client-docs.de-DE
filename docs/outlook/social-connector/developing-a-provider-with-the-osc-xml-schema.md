---
title: Entwickeln eines Providers mit dem OSC-XML-schema
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 0872b1b9-c21f-4bba-8cf1-4b010d8d7fb6
description: Outlook Social Connector (OSC) Provider-XML-Schemas definiert das Format einer beträchtlichen Anzahl von Informationen, die von einem sozialen Netzwerk an die OSC über das Netzwerk OSC-Anbieter übergeben wird.
ms.openlocfilehash: 93df682751146b501a316be62641b8cfd47a74a8
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19795969"
---
# <a name="developing-a-provider-with-the-osc-xml-schema"></a><span data-ttu-id="99f53-103">Entwickeln eines Providers mit dem OSC-XML-schema</span><span class="sxs-lookup"><span data-stu-id="99f53-103">Developing a provider with the OSC XML schema</span></span>

<span data-ttu-id="99f53-104">Outlook Social Connector (OSC) Provider-XML-Schemas definiert das Format einer beträchtlichen Anzahl von Informationen, die von einem sozialen Netzwerk an die OSC über das Netzwerk OSC-Anbieter übergeben wird.</span><span class="sxs-lookup"><span data-stu-id="99f53-104">The Outlook Social Connector (OSC) provider XML schema defines the format of a significant amount of information that is passed from a social network through the network's OSC provider to the OSC.</span></span> <span data-ttu-id="99f53-105">Das XML-Schema ermöglicht einen OSC-Anbieter an Funktionen der Anbieter, Freunde und Elementen im sozialen Netzwerk, mithilfe der drei Hauptelemente, **Funktionen**, **Freunde**, und **ActivityFeed**und ihre untergeordneten Aktivitätsfeed Elemente.</span><span class="sxs-lookup"><span data-stu-id="99f53-105">The XML schema allows an OSC provider to specify capabilities of the provider, friends, and activity feed items on the social network, by using the three main elements, **capabilities**, **friends**, and **activityFeed**, and their child elements.</span></span> <span data-ttu-id="99f53-106">Der OSC-Anbieter implementiert Schnittstellen und deren Methoden in die Erweiterbarkeit des OSC-Providers Rückgabe von XML-Zeichenfolgen als Output-Parameter, die mit dem OSC-Anbieter XML-Schema entsprechen.</span><span class="sxs-lookup"><span data-stu-id="99f53-106">The OSC provider implements interfaces and their methods in the OSC provider extensibility, returning XML strings as output parameters that comply with the OSC provider XML schema.</span></span> <span data-ttu-id="99f53-107">Die OSC ruft diese Methoden zum Abrufen von Informationen, die durch das XML-Schema definierten verarbeitet werden kann.</span><span class="sxs-lookup"><span data-stu-id="99f53-107">The OSC calls these methods to obtain information that it can understand as defined by the XML schema.</span></span>
  
> [!NOTE]
> <span data-ttu-id="99f53-108">Erweiterbarkeit des OSC-Providers debugging Anbieter unterstützt, durch Festlegen der `DebugProviders` Wert der `HKEY_CURRENT_USER\Software\Microsoft\Office\Outlook\SocialConnector` Registrierungsschlüssel auf 1.</span><span class="sxs-lookup"><span data-stu-id="99f53-108">OSC provider extensibility supports debugging providers by setting the `DebugProviders` value of the  `HKEY_CURRENT_USER\Software\Microsoft\Office\Outlook\SocialConnector` registry key to 1.</span></span> <span data-ttu-id="99f53-109">Wenn Sie das Debuggen Anbieter aktivieren, überprüft die OSC den XML-Anbieter für die Version des OSC-XML-Schemas, die Sie im XML- **Xmlns** -Attribut angeben.</span><span class="sxs-lookup"><span data-stu-id="99f53-109">When you turn on provider debugging, the OSC validates the provider XML against the version of the OSC XML schema that you specify in the **xmlns** XML attribute.</span></span> <span data-ttu-id="99f53-110">Geben Sie das **Xmlns** -Attribut OSC 1.1 und die OSC seit Outlook Social Connector 2013-Versionen wie folgt:`xmlns="http://schemas.microsoft.com/office/outlook/2010/06/socialprovider.xsd"`</span><span class="sxs-lookup"><span data-stu-id="99f53-110">For OSC 1.1 and versions of the OSC since Outlook Social Connector 2013, specify the **xmlns** attribute as follows: `xmlns="http://schemas.microsoft.com/office/outlook/2010/06/socialprovider.xsd"`</span></span>
  
## <a name="in-this-section"></a><span data-ttu-id="99f53-111">Inhalt dieses Abschnitts</span><span class="sxs-lookup"><span data-stu-id="99f53-111">In this section</span></span>

- <span data-ttu-id="99f53-112">[Synchronisieren von Freunde und Aktivitäten](synchronizing-friends-and-activities.md): Beschreibt die verschiedenen Methoden, OSC-Anbieter Freunde, nicht Freunde und Aktivitäten in einem sozialen Netzwerk synchronisieren können.</span><span class="sxs-lookup"><span data-stu-id="99f53-112">[Synchronizing Friends and Activities](synchronizing-friends-and-activities.md): Describes the various ways that OSC providers can synchronize friends, non-friends, and activities on a social network.</span></span> 
    
- <span data-ttu-id="99f53-113">[OSC-Anbieter-XML-Beispielen](osc-provider-xml-examples.md): enthält XML-Beispielen, die zeigen, wie Funktionen von einem OSC-Anbieter, Freunde und Aktivität angegeben feed Elemente in einem sozialen Netzwerk mit dem OSC-XML-Schema.</span><span class="sxs-lookup"><span data-stu-id="99f53-113">[OSC Provider XML Examples](osc-provider-xml-examples.md): Includes XML examples that show how to specify capabilities of an OSC provider, friends, and activity feed items on a social network by using the OSC XML schema.</span></span>
    
- <span data-ttu-id="99f53-114">[XML-Code für Funktionen](xml-for-capabilities.md): erläutert die - [ISocialProvider::GetCapabilities](isocialprovider-getcapabilities.md) -Methode, die die OSC wird verwendet, um Funktionsinformationen zu, der im **Funktionen** XML, aus der OSC-Anbieter zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="99f53-114">[XML for Capabilities](xml-for-capabilities.md): Explains the - [ISocialProvider::GetCapabilities](isocialprovider-getcapabilities.md) method that the OSC uses to obtain capabilities information, expressed in **capabilities** XML, from the OSC provider.</span></span> <span data-ttu-id="99f53-115">In diesem Abschnitt wird auch die XML-Elemente im XML-Schema von OSC-Anbieter, mit denen einen OSC-Anbieter an seine Funktionalität, einschließlich wie es Benutzer authentifiziert und synchronisiert Freunde und Aktivitäten.</span><span class="sxs-lookup"><span data-stu-id="99f53-115">This section also describes the XML elements in the OSC provider XML schema that allow an OSC provider to specify its functionality, including how it authenticates users and synchronizes friends and activities.</span></span> 
    
- <span data-ttu-id="99f53-116">[XML-Code für Freunde](xml-for-friends.md): enthält Beispiele für die APIs, die die OSC wird verwendet, um Informationen zu Freunde, der im **Freunde** XML, aus der OSC-Anbieter zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="99f53-116">[XML for Friends](xml-for-friends.md): Gives examples of the APIs that the OSC uses to obtain friends' information, expressed in **friends** XML, from the OSC provider.</span></span> <span data-ttu-id="99f53-117">In diesem Abschnitt wird auch die Elemente in der **Freunde** XML.</span><span class="sxs-lookup"><span data-stu-id="99f53-117">This section also describes elements in the **friends** XML.</span></span> 
    
- <span data-ttu-id="99f53-118">[XML-Code für Aktivitäten](xml-for-activities.md): enthält Beispiele für die APIs, die die OSC wird verwendet, um Aktivitätsinformationen zu, der im **ActivityFeed** XML, aus der OSC-Anbieter zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="99f53-118">[XML for Activities](xml-for-activities.md): Gives examples of the APIs that the OSC uses to obtain activities information, expressed in **activityFeed** XML, from the OSC provider.</span></span> <span data-ttu-id="99f53-119">In diesem Abschnitt wird auch die XML-Elemente im XML-Schema von OSC-Anbieter, mit die einen OSC-Anbieter eine Aktivitätsfeed angeben können.</span><span class="sxs-lookup"><span data-stu-id="99f53-119">This section also describes the XML elements in the OSC provider XML schema that allow an OSC provider to specify an activity feed.</span></span> <span data-ttu-id="99f53-120">Ein Aktivitätsfeed umfasst das Netzwerk, in dem die Aktivitäts--Elemente stammt Feed, Details der einzelnen Elemente Aktivitätsfeed (z. B. Besitzer, eingeben und Veröffentlichungsdatum der Aktivität), und die Vorlage aus, um die Aktivität anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="99f53-120">An activity feed includes the network where the activity feed items originated, details of each activity feed item (such as owner, type, and publish date of the activity), and the template to display the activity.</span></span> 
    
## <a name="reference"></a><span data-ttu-id="99f53-121">Referenz</span><span class="sxs-lookup"><span data-stu-id="99f53-121">Reference</span></span>

- [<span data-ttu-id="99f53-122">Referenz zum Outlook Connector Provider für soziale Netzwerke</span><span class="sxs-lookup"><span data-stu-id="99f53-122">Outlook Social Connector Provider Reference</span></span>](outlook-social-connector-provider-reference-0.md)
  
## <a name="related-sections"></a><span data-ttu-id="99f53-123">Verwandte Abschnitte</span><span class="sxs-lookup"><span data-stu-id="99f53-123">Related sections</span></span>

- [<span data-ttu-id="99f53-124">Erste Schritte zum Entwickeln eines Outlook Connector Providers für soziale Netzwerke</span><span class="sxs-lookup"><span data-stu-id="99f53-124">Getting Started with Developing an Outlook Social Connector Provider</span></span>](getting-started-with-developing-an-outlook-social-connector-provider.md)
  
- [<span data-ttu-id="99f53-125">Über den OSC-Beispielvorlagen</span><span class="sxs-lookup"><span data-stu-id="99f53-125">OSC Sample Templates</span></span>](osc-sample-templates.md)
  
- [<span data-ttu-id="99f53-126">OSC - Typische Aufrufsequenzen</span><span class="sxs-lookup"><span data-stu-id="99f53-126">OSC Typical Calling Sequences</span></span>](osc-typical-calling-sequences.md)
  
- [<span data-ttu-id="99f53-127">Debuggen eines Providers</span><span class="sxs-lookup"><span data-stu-id="99f53-127">Debugging a Provider</span></span>](debugging-a-provider.md)
  
- [<span data-ttu-id="99f53-128">Bereitstellen eines Providers</span><span class="sxs-lookup"><span data-stu-id="99f53-128">Deploying a Provider</span></span>](deploying-a-provider.md)
  
- [<span data-ttu-id="99f53-129">Bewährte Methoden für das Entwickeln eines Providers</span><span class="sxs-lookup"><span data-stu-id="99f53-129">Best Practices for Developing a Provider</span></span>](best-practices-for-developing-a-provider.md)
  
## <a name="see-also"></a><span data-ttu-id="99f53-130">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="99f53-130">See also</span></span>

- [<span data-ttu-id="99f53-131">Debuggen eines Providers</span><span class="sxs-lookup"><span data-stu-id="99f53-131">Debugging a Provider</span></span>](debugging-a-provider.md)

