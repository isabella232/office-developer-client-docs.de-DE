---
title: Erste Schritte mit der Entwicklung eines Outlook Social Connector-Anbieters
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 1c65d2df-86a3-48d5-9fec-a9040f3b878c
description: Die Outlook Social Connector (OSC)-Anbieterreferenz beschreibt die Entwicklung eines OSC-Anbieters mithilfe der Erweiterbarkeit des OSC-Anbieters.
ms.openlocfilehash: 24f8eabe33103f53e848f055b72fd402bc5dd89a
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32327160"
---
# <a name="getting-started-with-developing-an-outlook-social-connector-provider"></a><span data-ttu-id="36250-103">Erste Schritte mit der Entwicklung eines Outlook Social Connector-Anbieters</span><span class="sxs-lookup"><span data-stu-id="36250-103">Getting started with developing an Outlook Social Connector provider</span></span>

<span data-ttu-id="36250-104">Die Outlook Social Connector (OSC)-Anbieterreferenz beschreibt die Entwicklung eines OSC-Anbieters mithilfe der Erweiterbarkeit des OSC-Anbieters.</span><span class="sxs-lookup"><span data-stu-id="36250-104">The Outlook Social Connector (OSC) Provider Reference describes how to develop an OSC provider by using OSC provider extensibility.</span></span> <span data-ttu-id="36250-105">Wenn Sie gerade erst mit dem Entwickeln von Lösungen für Outlook begonnen haben, finden Sie im Artikel [Selecting an API or Technology for Developing Outlook Solutions](https://msdn.microsoft.com/library/8295da20-e567-4d08-b8e4-5c9b4498edd4%28Office.15%29.aspx) weitere Informationen zu den APIs und Technologien, die am besten zu Ihren Anforderungen passen.</span><span class="sxs-lookup"><span data-stu-id="36250-105">If you are new to developing solutions for Outlook, see [Selecting an API or Technology for Developing Outlook Solutions](https://msdn.microsoft.com/library/8295da20-e567-4d08-b8e4-5c9b4498edd4%28Office.15%29.aspx) to identify the APIs and technologies that are most appropriate for your needs.</span></span> 

<span data-ttu-id="36250-106">Dieser Abschnitt enthält eine Übersicht über die OSC, wie ein OSC-Anbieter nützlich sein kann, schnelle Schritte zum Entwickeln eines Anbieters, technische Anforderungen, bewährte Methoden für die Entwicklung eines Anbieters und was in dieser Version neu ist.</span><span class="sxs-lookup"><span data-stu-id="36250-106">This section gives an overview of the OSC, how an OSC provider can be useful, quick steps for learning to develop a provider, technical requirements, best practices for developing a provider, and what's new in this release.</span></span> 
  
## <a name="in-this-section"></a><span data-ttu-id="36250-107">Inhalt dieses Abschnitts</span><span class="sxs-lookup"><span data-stu-id="36250-107">In this section</span></span>

- <span data-ttu-id="36250-108">[Neues für](what-s-new-for-providers.md)Anbieter: Vergleicht DIE OSC-Features in der vorherigen und aktuellen Version und beschreibt Benutzeroberflächenelemente und XML-Schemaelemente, die in dieser Version hinzugefügt, geändert oder veraltet sind.</span><span class="sxs-lookup"><span data-stu-id="36250-108">[What's New for Providers](what-s-new-for-providers.md): Compares OSC features in the previous and current release, and describes interface members and XML schema elements that have been added, changed, or deprecated in this release.</span></span> 
    
- <span data-ttu-id="36250-109">[Why Develop an Outlook Social Connector Provider](why-develop-an-outlook-social-connector-provider.md): Beschreibt, wie ein OSC-Anbieter für gemeinsame Websites für soziale Netzwerke und andere interne Netzwerktools nützlich sein kann.</span><span class="sxs-lookup"><span data-stu-id="36250-109">[Why Develop an Outlook Social Connector Provider](why-develop-an-outlook-social-connector-provider.md): Describes how an OSC provider can be useful for common social network sites and other internal networking tools.</span></span>
    
- <span data-ttu-id="36250-110">[In Bezug auf das OSC mit Outlook und sozialen](relating-the-osc-with-outlook-and-social-networks.md)Netzwerken: Bietet eine Architekturansicht, wie das OSC Outlook-Benutzer mit sozialen Netzwerken verbindet.</span><span class="sxs-lookup"><span data-stu-id="36250-110">[Relating the OSC with Outlook and Social Networks](relating-the-osc-with-outlook-and-social-networks.md): Provides an architectural view of how the OSC connects Outlook users with social networks.</span></span> <span data-ttu-id="36250-111">Außerdem wird definiert, wie allgemeine Begriffe wie "soziale Netzwerke", "Freunde", "Nicht-Freunde" und "Kontakte" im Rest dieses Verweises verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="36250-111">Also defines the way that common terms, like "social networks," "friends," "non-friends," and "contacts" are used in the rest of this reference.</span></span>
    
- <span data-ttu-id="36250-112">[Quick Steps for Learning to Develop a Provider](quick-steps-for-learning-to-develop-a-provider.md): Enthält eine Zusammenfassung der Schritte zum Entwickeln eines OSC-Anbieters.</span><span class="sxs-lookup"><span data-stu-id="36250-112">[Quick Steps for Learning to Develop a Provider](quick-steps-for-learning-to-develop-a-provider.md): Provides a summary of steps to learn to develop an OSC provider.</span></span>
    
- <span data-ttu-id="36250-113">[Technische Anforderungen](technical-requirements.md): Beschreibt die unterstützten Programmiersprachen, ANFORDERUNGEN für die COM-Sichtbarkeit, Anforderungen an methodenrücksenkungstypen und Details der ERWEITERBARKEITS-DLL des OSC-Anbieters.</span><span class="sxs-lookup"><span data-stu-id="36250-113">[Technical Requirements](technical-requirements.md): Describes the supported programming languages, COM visibility requirements, method return type requirements, and details of the OSC provider extensibility DLL.</span></span>
    
- <span data-ttu-id="36250-114">[Bewährte Methoden für die Entwicklung eines Anbieters:](best-practices-for-developing-a-provider.md)Enthält eine Liste der bewährten Methoden, die bei der Entwicklung eines OSC-Anbieters zu befolgen sind.</span><span class="sxs-lookup"><span data-stu-id="36250-114">[Best Practices for Developing a Provider](best-practices-for-developing-a-provider.md): Provides a list of best practices to follow while developing an OSC provider.</span></span>
    
## <a name="reference"></a><span data-ttu-id="36250-115">Referenz</span><span class="sxs-lookup"><span data-stu-id="36250-115">Reference</span></span>

- [<span data-ttu-id="36250-116">Referenz zum Outlook Connector Provider für soziale Netzwerke</span><span class="sxs-lookup"><span data-stu-id="36250-116">Outlook Social Connector Provider Reference</span></span>](outlook-social-connector-provider-reference-0.md)
  
## <a name="related-sections"></a><span data-ttu-id="36250-117">Verwandte Abschnitte</span><span class="sxs-lookup"><span data-stu-id="36250-117">Related sections</span></span>

- [<span data-ttu-id="36250-118">Über den OSC-Beispielvorlagen</span><span class="sxs-lookup"><span data-stu-id="36250-118">OSC Sample Templates</span></span>](osc-sample-templates.md)
  
- [<span data-ttu-id="36250-119">OSC - Typische Aufrufsequenzen</span><span class="sxs-lookup"><span data-stu-id="36250-119">OSC Typical Calling Sequences</span></span>](osc-typical-calling-sequences.md)
  
- [<span data-ttu-id="36250-120">Entwickeln eines Providers mit dem OSC-XML-Schema</span><span class="sxs-lookup"><span data-stu-id="36250-120">Developing a Provider with the OSC XML Schema</span></span>](developing-a-provider-with-the-osc-xml-schema.md)
  
- [<span data-ttu-id="36250-121">Debuggen eines Providers</span><span class="sxs-lookup"><span data-stu-id="36250-121">Debugging a Provider</span></span>](debugging-a-provider.md)
  
- [<span data-ttu-id="36250-122">Bereitstellen eines Providers</span><span class="sxs-lookup"><span data-stu-id="36250-122">Deploying a Provider</span></span>](deploying-a-provider.md)
  
- [<span data-ttu-id="36250-123">Vorbereitung der Freigabe eines OSC-Providers</span><span class="sxs-lookup"><span data-stu-id="36250-123">Getting Ready to Release an OSC Provider</span></span>](getting-ready-to-release-an-osc-provider.md)
  
## <a name="see-also"></a><span data-ttu-id="36250-124">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="36250-124">See also</span></span>

- [<span data-ttu-id="36250-125">Microsoft Outlook Social Connector 32-Bit</span><span class="sxs-lookup"><span data-stu-id="36250-125">Microsoft Outlook Social Connector 32-bit</span></span>](https://www.microsoft.com/downloads/details.aspx?FamilyID=b638cc14-11e5-448a-b5a6-4f553ce81b94)
- [<span data-ttu-id="36250-126">Update für Outlook Social Connector (KB983403), 32-Bit Edition</span><span class="sxs-lookup"><span data-stu-id="36250-126">Update for Outlook Social Connector (KB983403), 32-Bit Edition</span></span>](https://www.microsoft.com/downloads/details.aspx?FamilyID=9886faca-f1c5-4579-83e2-c872c7abc61a)
- [<span data-ttu-id="36250-127">Update für Outlook Social Connector (KB983403), 64-Bit-Edition</span><span class="sxs-lookup"><span data-stu-id="36250-127">Update for Outlook Social Connector (KB983403), 64-bit Edition</span></span>](https://www.microsoft.com/downloads/details.aspx?FamilyID=72a506a7-8a91-4d56-8b27-bf3b3f58fe9a)
- [<span data-ttu-id="36250-128">Outlook Social Connector 2013: Anbietervorlagen</span><span class="sxs-lookup"><span data-stu-id="36250-128">Outlook Social Connector 2013: Provider templates</span></span>](https://code.msdn.microsoft.com/Outlook-Social-Connector-73fd8d2c)

