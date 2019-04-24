---
title: Erste Schritte beim Entwickeln eines Outlook Social Connector-Anbieters
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 1c65d2df-86a3-48d5-9fec-a9040f3b878c
description: In der Referenz zur Outlook Social Connector (OSC) wird beschrieben, wie Sie einen OSC-Anbieter mithilfe der OSC-Anbieter Erweiterbarkeit entwickeln.
ms.openlocfilehash: 24f8eabe33103f53e848f055b72fd402bc5dd89a
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32327160"
---
# <a name="getting-started-with-developing-an-outlook-social-connector-provider"></a><span data-ttu-id="17ad5-103">Erste Schritte beim Entwickeln eines Outlook Social Connector-Anbieters</span><span class="sxs-lookup"><span data-stu-id="17ad5-103">Getting started with developing an Outlook Social Connector provider</span></span>

<span data-ttu-id="17ad5-104">In der Referenz zur Outlook Social Connector (OSC) wird beschrieben, wie Sie einen OSC-Anbieter mithilfe der OSC-Anbieter Erweiterbarkeit entwickeln.</span><span class="sxs-lookup"><span data-stu-id="17ad5-104">The Outlook Social Connector (OSC) Provider Reference describes how to develop an OSC provider by using OSC provider extensibility.</span></span> <span data-ttu-id="17ad5-105">Wenn Sie gerade erst mit dem Entwickeln von Lösungen für Outlook begonnen haben, finden Sie im Artikel [Selecting an API or Technology for Developing Outlook Solutions](https://msdn.microsoft.com/library/8295da20-e567-4d08-b8e4-5c9b4498edd4%28Office.15%29.aspx) weitere Informationen zu den APIs und Technologien, die am besten zu Ihren Anforderungen passen.</span><span class="sxs-lookup"><span data-stu-id="17ad5-105">If you are new to developing solutions for Outlook, see [Selecting an API or Technology for Developing Outlook Solutions](https://msdn.microsoft.com/library/8295da20-e567-4d08-b8e4-5c9b4498edd4%28Office.15%29.aspx) to identify the APIs and technologies that are most appropriate for your needs.</span></span> 

<span data-ttu-id="17ad5-106">Dieser Abschnitt enthält eine Übersicht über den OSC, wie ein OSC-Anbieter nützlich sein kann, schnelle Schritte zum Entwickeln eines Anbieters, technische Anforderungen, bewährte Methoden für die Entwicklung eines Anbieters und Neuerungen in dieser Release.</span><span class="sxs-lookup"><span data-stu-id="17ad5-106">This section gives an overview of the OSC, how an OSC provider can be useful, quick steps for learning to develop a provider, technical requirements, best practices for developing a provider, and what's new in this release.</span></span> 
  
## <a name="in-this-section"></a><span data-ttu-id="17ad5-107">Inhalt dieses Abschnitts</span><span class="sxs-lookup"><span data-stu-id="17ad5-107">In this section</span></span>

- <span data-ttu-id="17ad5-108">Neuigkeiten [für Anbieter](what-s-new-for-providers.md): vergleicht osc-Features in der vorherigen und aktuellen Version und beschreibt SCHNITTSTELLENMEMBER und XML-Schemaelemente, die in dieser Version hinzugefügt, geändert oder veraltet sind.</span><span class="sxs-lookup"><span data-stu-id="17ad5-108">[What's New for Providers](what-s-new-for-providers.md): Compares OSC features in the previous and current release, and describes interface members and XML schema elements that have been added, changed, or deprecated in this release.</span></span> 
    
- <span data-ttu-id="17ad5-109">[Gründe für die Entwicklung eines Outlook Social Connector](why-develop-an-outlook-social-connector-provider.md)-Anbieters: Beschreibt, wie ein osc-Anbieter für allgemeine soziale Netzwerk Websites und andere interne Netzwerktools nützlich sein kann.</span><span class="sxs-lookup"><span data-stu-id="17ad5-109">[Why Develop an Outlook Social Connector Provider](why-develop-an-outlook-social-connector-provider.md): Describes how an OSC provider can be useful for common social network sites and other internal networking tools.</span></span>
    
- <span data-ttu-id="17ad5-110">[Zusammenhang mit dem osc mit Outlook und sozialen Netzwerken](relating-the-osc-with-outlook-and-social-networks.md): bietet eine Architektur Ansicht, wie der osc Outlook-Benutzer mit sozialen Netzwerken verbindet.</span><span class="sxs-lookup"><span data-stu-id="17ad5-110">[Relating the OSC with Outlook and Social Networks](relating-the-osc-with-outlook-and-social-networks.md): Provides an architectural view of how the OSC connects Outlook users with social networks.</span></span> <span data-ttu-id="17ad5-111">Definiert auch die Art und Weise, wie allgemeine Ausdrücke wie "soziale Netzwerke", "Freunde", "nicht-Freunde" und "Kontakte" im Rest dieser Referenz verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="17ad5-111">Also defines the way that common terms, like "social networks," "friends," "non-friends," and "contacts" are used in the rest of this reference.</span></span>
    
- <span data-ttu-id="17ad5-112">[Schnelle Schritte zum Entwickeln eines Anbieters](quick-steps-for-learning-to-develop-a-provider.md): enthält eine Zusammenfassung der Schritte zum Entwickeln eines osc-Anbieters.</span><span class="sxs-lookup"><span data-stu-id="17ad5-112">[Quick Steps for Learning to Develop a Provider](quick-steps-for-learning-to-develop-a-provider.md): Provides a summary of steps to learn to develop an OSC provider.</span></span>
    
- <span data-ttu-id="17ad5-113">[Technische Anforderungen](technical-requirements.md): Beschreibung der unterstützten Programmiersprachen, Anforderungen an die com-Sichtbarkeits Anforderungen, Methodenrückgabe Typen und Details zur osc-Erweiterungs-DLL.</span><span class="sxs-lookup"><span data-stu-id="17ad5-113">[Technical Requirements](technical-requirements.md): Describes the supported programming languages, COM visibility requirements, method return type requirements, and details of the OSC provider extensibility DLL.</span></span>
    
- <span data-ttu-id="17ad5-114">[Bewährte Methoden für die Entwicklung eines Anbieters](best-practices-for-developing-a-provider.md): enthält eine Liste der bewährten Methoden beim Entwickeln eines osc-Anbieters.</span><span class="sxs-lookup"><span data-stu-id="17ad5-114">[Best Practices for Developing a Provider](best-practices-for-developing-a-provider.md): Provides a list of best practices to follow while developing an OSC provider.</span></span>
    
## <a name="reference"></a><span data-ttu-id="17ad5-115">Referenz</span><span class="sxs-lookup"><span data-stu-id="17ad5-115">Reference</span></span>

- [<span data-ttu-id="17ad5-116">Referenz zum Outlook Connector Provider für soziale Netzwerke</span><span class="sxs-lookup"><span data-stu-id="17ad5-116">Outlook Social Connector Provider Reference</span></span>](outlook-social-connector-provider-reference-0.md)
  
## <a name="related-sections"></a><span data-ttu-id="17ad5-117">Verwandte Abschnitte</span><span class="sxs-lookup"><span data-stu-id="17ad5-117">Related sections</span></span>

- [<span data-ttu-id="17ad5-118">Über den OSC-Beispielvorlagen</span><span class="sxs-lookup"><span data-stu-id="17ad5-118">OSC Sample Templates</span></span>](osc-sample-templates.md)
  
- [<span data-ttu-id="17ad5-119">OSC - Typische Aufrufsequenzen</span><span class="sxs-lookup"><span data-stu-id="17ad5-119">OSC Typical Calling Sequences</span></span>](osc-typical-calling-sequences.md)
  
- [<span data-ttu-id="17ad5-120">Entwickeln eines Providers mit dem OSC-XML-Schema</span><span class="sxs-lookup"><span data-stu-id="17ad5-120">Developing a Provider with the OSC XML Schema</span></span>](developing-a-provider-with-the-osc-xml-schema.md)
  
- [<span data-ttu-id="17ad5-121">Debuggen eines Providers</span><span class="sxs-lookup"><span data-stu-id="17ad5-121">Debugging a Provider</span></span>](debugging-a-provider.md)
  
- [<span data-ttu-id="17ad5-122">Bereitstellen eines Providers</span><span class="sxs-lookup"><span data-stu-id="17ad5-122">Deploying a Provider</span></span>](deploying-a-provider.md)
  
- [<span data-ttu-id="17ad5-123">Vorbereitung der Freigabe eines OSC-Providers</span><span class="sxs-lookup"><span data-stu-id="17ad5-123">Getting Ready to Release an OSC Provider</span></span>](getting-ready-to-release-an-osc-provider.md)
  
## <a name="see-also"></a><span data-ttu-id="17ad5-124">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="17ad5-124">See also</span></span>

- [<span data-ttu-id="17ad5-125">Microsoft Outlook Connector für soziale Netzwerke 32-Bit</span><span class="sxs-lookup"><span data-stu-id="17ad5-125">Microsoft Outlook Social Connector 32-bit</span></span>](https://www.microsoft.com/downloads/details.aspx?FamilyID=b638cc14-11e5-448a-b5a6-4f553ce81b94)
- [<span data-ttu-id="17ad5-126">Update für Outlook Connector für soziale Netzwerke (KB983403), 32-Bit-Edition</span><span class="sxs-lookup"><span data-stu-id="17ad5-126">Update for Outlook Social Connector (KB983403), 32-Bit Edition</span></span>](https://www.microsoft.com/downloads/details.aspx?FamilyID=9886faca-f1c5-4579-83e2-c872c7abc61a)
- [<span data-ttu-id="17ad5-127">Update für Outlook Connector für soziale Netzwerke (KB983403), 64-Bit-Edition</span><span class="sxs-lookup"><span data-stu-id="17ad5-127">Update for Outlook Social Connector (KB983403), 64-bit Edition</span></span>](https://www.microsoft.com/downloads/details.aspx?FamilyID=72a506a7-8a91-4d56-8b27-bf3b3f58fe9a)
- [<span data-ttu-id="17ad5-128">Outlook Connector für soziale Netzwerke 2013: Anbietervorlagen</span><span class="sxs-lookup"><span data-stu-id="17ad5-128">Outlook Social Connector 2013: Provider templates</span></span>](https://code.msdn.microsoft.com/Outlook-Social-Connector-73fd8d2c)

