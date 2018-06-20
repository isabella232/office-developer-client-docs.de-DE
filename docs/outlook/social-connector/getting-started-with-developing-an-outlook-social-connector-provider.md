---
title: Erste Schritte zur Entwicklung von einem Anbieter Outlook Connector für soziale Netzwerke
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 1c65d2df-86a3-48d5-9fec-a9040f3b878c
description: Verweis auf den Outlook Social Connector (OSC) wird von einem OSC-Anbieter entwickeln mithilfe der Erweiterbarkeit des OSC-Providers beschrieben.
ms.openlocfilehash: 19f5ffe8987d0b19017692ddb8f7888be2140033
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19795948"
---
# <a name="getting-started-with-developing-an-outlook-social-connector-provider"></a><span data-ttu-id="ec6c2-103">Erste Schritte zur Entwicklung von einem Anbieter Outlook Connector für soziale Netzwerke</span><span class="sxs-lookup"><span data-stu-id="ec6c2-103">Getting started with developing an Outlook Social Connector provider</span></span>

<span data-ttu-id="ec6c2-104">Verweis auf den Outlook Social Connector (OSC) wird von einem OSC-Anbieter entwickeln mithilfe der Erweiterbarkeit des OSC-Providers beschrieben.</span><span class="sxs-lookup"><span data-stu-id="ec6c2-104">The Outlook Social Connector (OSC) Provider Reference describes how to develop an OSC provider by using OSC provider extensibility.</span></span> <span data-ttu-id="ec6c2-105">Wenn Sie für die Entwicklung von Lösungen für Outlook nicht vertraut sind, finden Sie unter [Auswählen einer API oder Technologie zur Entwicklung von Outlook-Lösungen](http://msdn.microsoft.com/library/8295da20-e567-4d08-b8e4-5c9b4498edd4%28Office.15%29.aspx) zu den APIs und Technologien, die für Ihre Anforderungen am besten geeignet sind.</span><span class="sxs-lookup"><span data-stu-id="ec6c2-105">If you are new to developing solutions for Outlook, see [Selecting an API or Technology for Developing Outlook Solutions](http://msdn.microsoft.com/library/8295da20-e567-4d08-b8e4-5c9b4498edd4%28Office.15%29.aspx) to identify the APIs and technologies that are most appropriate for your needs.</span></span> 

<span data-ttu-id="ec6c2-106">Dieser Abschnitt bietet eine Übersicht über die OSC, wie ein OSC-Anbieter nützlich, schnell Schritte zum Entwickeln eines Providers, technische Anforderungen, bewährte Methoden für das Entwickeln eines Providers erlernen werden kann und was ist neu in dieser Version.</span><span class="sxs-lookup"><span data-stu-id="ec6c2-106">This section gives an overview of the OSC, how an OSC provider can be useful, quick steps for learning to develop a provider, technical requirements, best practices for developing a provider, and what's new in this release.</span></span> 
  
## <a name="in-this-section"></a><span data-ttu-id="ec6c2-107">Inhalt dieses Abschnitts</span><span class="sxs-lookup"><span data-stu-id="ec6c2-107">In this section</span></span>

- <span data-ttu-id="ec6c2-108">[Neuigkeiten für Anbieter](what-s-new-for-providers.md): vergleicht OSC-features in der vorherigen und der aktuellen Version und beschreibt Elemente der Benutzeroberfläche und XML-Schemaelemente, die hinzugefügt, geändert oder in dieser Version veraltet.</span><span class="sxs-lookup"><span data-stu-id="ec6c2-108">[What's New for Providers](what-s-new-for-providers.md): Compares OSC features in the previous and current release, and describes interface members and XML schema elements that have been added, changed, or deprecated in this release.</span></span> 
    
- <span data-ttu-id="ec6c2-109">[Warum Entwickeln eines Outlook Social Connector Providers](why-develop-an-outlook-social-connector-provider.md): Beschreibt, wie ein OSC-Anbieter für allgemeine soziale Netzwerke Websites und andere interne Netzwerktools hilfreich sein kann.</span><span class="sxs-lookup"><span data-stu-id="ec6c2-109">[Why Develop an Outlook Social Connector Provider](why-develop-an-outlook-social-connector-provider.md): Describes how an OSC provider can be useful for common social network sites and other internal networking tools.</span></span>
    
- <span data-ttu-id="ec6c2-110">[Im Zusammenhang mit Outlook und sozialen Netzwerken der OSC](relating-the-osc-with-outlook-and-social-networks.md): bietet eine Architektur Ansicht der wie die OSC Outlook-Benutzer eine Verbindung mit sozialen Netzwerken herstellt.</span><span class="sxs-lookup"><span data-stu-id="ec6c2-110">[Relating the OSC with Outlook and Social Networks](relating-the-osc-with-outlook-and-social-networks.md): Provides an architectural view of how the OSC connects Outlook users with social networks.</span></span> <span data-ttu-id="ec6c2-111">Definiert auch die Möglichkeit, häufig verwendete Begriffe, wie "sozialen Netzwerken", "Freunde", "nicht-Freunde," und "Kontakte" im weiteren Verlauf dieser Referenz verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="ec6c2-111">Also defines the way that common terms, like "social networks," "friends," "non-friends," and "contacts" are used in the rest of this reference.</span></span>
    
- <span data-ttu-id="ec6c2-112">[Schritte zum Entwickeln ein Providers erlernen](quick-steps-for-learning-to-develop-a-provider.md): enthält eine Zusammenfassung der Schritte, um zu einen OSC-Anbieter zu entwickeln.</span><span class="sxs-lookup"><span data-stu-id="ec6c2-112">[Quick Steps for Learning to Develop a Provider](quick-steps-for-learning-to-develop-a-provider.md): Provides a summary of steps to learn to develop an OSC provider.</span></span>
    
- <span data-ttu-id="ec6c2-113">[Technische Anforderungen](technical-requirements.md): Beschreibt die unterstützten Programmiersprachen, die COM-Sichtbarkeit Anforderungen, die Methode Rückgabetyp Anforderungen und die Details der die OSC-anbietererweiterung DLL.</span><span class="sxs-lookup"><span data-stu-id="ec6c2-113">[Technical Requirements](technical-requirements.md): Describes the supported programming languages, COM visibility requirements, method return type requirements, and details of the OSC provider extensibility DLL.</span></span>
    
- <span data-ttu-id="ec6c2-114">[Bewährte Methoden für das Entwickeln eines Providers](best-practices-for-developing-a-provider.md): enthält eine Liste der bewährten Methoden befolgen beim Entwickeln eines OSC-Providers.</span><span class="sxs-lookup"><span data-stu-id="ec6c2-114">[Best Practices for Developing a Provider](best-practices-for-developing-a-provider.md): Provides a list of best practices to follow while developing an OSC provider.</span></span>
    
## <a name="reference"></a><span data-ttu-id="ec6c2-115">Referenz</span><span class="sxs-lookup"><span data-stu-id="ec6c2-115">Reference</span></span>

- [<span data-ttu-id="ec6c2-116">Referenz zum Outlook Connector Provider für soziale Netzwerke</span><span class="sxs-lookup"><span data-stu-id="ec6c2-116">Outlook Social Connector Provider Reference</span></span>](outlook-social-connector-provider-reference-0.md)
  
## <a name="related-sections"></a><span data-ttu-id="ec6c2-117">Verwandte Abschnitte</span><span class="sxs-lookup"><span data-stu-id="ec6c2-117">Related sections</span></span>

- [<span data-ttu-id="ec6c2-118">Über den OSC-Beispielvorlagen</span><span class="sxs-lookup"><span data-stu-id="ec6c2-118">OSC Sample Templates</span></span>](osc-sample-templates.md)
  
- [<span data-ttu-id="ec6c2-119">OSC - Typische Aufrufsequenzen</span><span class="sxs-lookup"><span data-stu-id="ec6c2-119">OSC Typical Calling Sequences</span></span>](osc-typical-calling-sequences.md)
  
- [<span data-ttu-id="ec6c2-120">Entwickeln eines Providers mit dem OSC-XML-Schema</span><span class="sxs-lookup"><span data-stu-id="ec6c2-120">Developing a Provider with the OSC XML Schema</span></span>](developing-a-provider-with-the-osc-xml-schema.md)
  
- [<span data-ttu-id="ec6c2-121">Debuggen eines Providers</span><span class="sxs-lookup"><span data-stu-id="ec6c2-121">Debugging a Provider</span></span>](debugging-a-provider.md)
  
- [<span data-ttu-id="ec6c2-122">Bereitstellen eines Providers</span><span class="sxs-lookup"><span data-stu-id="ec6c2-122">Deploying a Provider</span></span>](deploying-a-provider.md)
  
- [<span data-ttu-id="ec6c2-123">Vorbereitung der Freigabe eines OSC-Providers</span><span class="sxs-lookup"><span data-stu-id="ec6c2-123">Getting Ready to Release an OSC Provider</span></span>](getting-ready-to-release-an-osc-provider.md)
  
## <a name="see-also"></a><span data-ttu-id="ec6c2-124">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="ec6c2-124">See also</span></span>

- [<span data-ttu-id="ec6c2-125">Microsoft Outlook Connector für soziale Netzwerke 32-bit</span><span class="sxs-lookup"><span data-stu-id="ec6c2-125">Microsoft Outlook Social Connector 32-bit</span></span>](http://www.microsoft.com/downloads/details.aspx?FamilyID=b638cc14-11e5-448a-b5a6-4f553ce81b94)
- [<span data-ttu-id="ec6c2-126">Update für Outlook Connector für soziale Netzwerke (KB983403), 32-Bit-Version</span><span class="sxs-lookup"><span data-stu-id="ec6c2-126">Update for Outlook Social Connector (KB983403), 32-Bit Edition</span></span>](http://www.microsoft.com/downloads/details.aspx?FamilyID=9886faca-f1c5-4579-83e2-c872c7abc61a)
- [<span data-ttu-id="ec6c2-127">Update für Outlook Connector für soziale Netzwerke (KB983403), 64-Bit-Version</span><span class="sxs-lookup"><span data-stu-id="ec6c2-127">Update for Outlook Social Connector (KB983403), 64-bit Edition</span></span>](http://www.microsoft.com/downloads/details.aspx?FamilyID=72a506a7-8a91-4d56-8b27-bf3b3f58fe9a)
- [<span data-ttu-id="ec6c2-128">Outlook Connector für soziale Netzwerke 2013: Anbietervorlagen</span><span class="sxs-lookup"><span data-stu-id="ec6c2-128">Outlook Social Connector 2013: Provider templates</span></span>](http://code.msdn.microsoft.com/Outlook-Social-Connector-73fd8d2c)

