---
title: Project Server 2013-Architektur und Programmierbarkeit
manager: soliver
ms.date: 09/17/2015
ms.audience: Developer
f1_keywords:
- architecture
- platform
- Project
- Project architecture
- Project programmability
- Project Server architecture
- Project Server programmability
keywords:
- Project 2013, Architektur und Programmierbarkeit, Programmierbarkeit, Project Server,Project 2013, Vorteile für EPM, Architecture und Project Server
localization_priority: Normal
ms.assetid: 9ea3b3c1-fb90-454a-b8e6-abc44fca663d
description: In den Artikeln in diesem Abschnitt wird die Gesamtarchitektur der Enterprise Project Management (EPM)-Lösung beschrieben, die Project Professional 2013, Project Server 2013, Project Web App und SharePoint Server 2013 kombiniert.
ms.openlocfilehash: 44cd5a32b8d3de421ffe3b2d9bf0137146bc4c4e
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33413787"
---
# <a name="project-server-2013-architecture-and-programmability"></a><span data-ttu-id="b6158-104">Project Server 2013-Architektur und Programmierbarkeit</span><span class="sxs-lookup"><span data-stu-id="b6158-104">Project Server 2013 architecture and programmability</span></span>

<span data-ttu-id="b6158-105">In den Artikeln in diesem Abschnitt wird die Gesamtarchitektur der Enterprise Project Management (EPM)-Lösung beschrieben, die Project Professional 2013, Project Server 2013, Project Web App und SharePoint Server 2013 kombiniert.</span><span class="sxs-lookup"><span data-stu-id="b6158-105">The articles in this section describe the overall architecture of the Enterprise Project Management (EPM) solution, which combines Project Professional 2013, Project Server 2013, Project Web App, and SharePoint Server 2013.</span></span>
  
<span data-ttu-id="b6158-106">Project Server 2013 wurde mit .NET Framework 4 erstellt und ist die dritte Hauptversion von Project Server, die eine echte mehrstufige Architektur bietet.</span><span class="sxs-lookup"><span data-stu-id="b6158-106">Project Server 2013 is built with the .NET Framework 4 and is the third major release of Project Server to provide a true multitier architecture.</span></span> <span data-ttu-id="b6158-107">Für den Cloudzugriff implementiert Project Server 2013 ein clientseitiges Objektmodell (CSOM) und einen OData-Dienst für die Berichterstellung, der in Webanwendungen, mobilen Anwendungen und Silverlight-Anwendungen verwendet werden kann.</span><span class="sxs-lookup"><span data-stu-id="b6158-107">For cloud access, Project Server 2013 implements a client-side object model (CSOM) and an OData service for reporting that can be used in web applications, mobile applications, and Silverlight applications.</span></span> <span data-ttu-id="b6158-108">Für lokale Anwendungen können Clients entweder das CSOM oder die Project Server Interface (PSI) verwenden.</span><span class="sxs-lookup"><span data-stu-id="b6158-108">For applications on-premises, clients can use either the CSOM or the Project Server Interface (PSI) services.</span></span> 
  
## <a name="introduction-to-project-server-architecture"></a><span data-ttu-id="b6158-109">Einführung in Project Serverarchitektur</span><span class="sxs-lookup"><span data-stu-id="b6158-109">Introduction to Project Server architecture</span></span>

<span data-ttu-id="b6158-110">In den Themen in diesem Abschnitt wird die Gesamtarchitektur der Enterprise Project Management (EPM)-Lösung beschrieben, die Project Professional 2013, Project Server 2013, Project Web App und SharePoint Server 2013 kombiniert.</span><span class="sxs-lookup"><span data-stu-id="b6158-110">The topics in this section describe the overall architecture of the Enterprise Project Management (EPM) solution, which combines Project Professional 2013, Project Server 2013, Project Web App, and SharePoint Server 2013.</span></span>
  
<span data-ttu-id="b6158-111">Für den programmgesteuerten Zugriff auf Project Server sollten Sie entweder das CSOM oder die PSI-Dienste mit der Windows Communication Foundation (WCF)-Schnittstelle verwenden.</span><span class="sxs-lookup"><span data-stu-id="b6158-111">For programmatic access to Project Server, you should use either the CSOM or the PSI services with the Windows Communication Foundation (WCF) interface.</span></span> <span data-ttu-id="b6158-112">Die ASMX-Webdienstschnittstelle der PSI ist in Project Server 2013 veraltet, funktioniert aber weiterhin.</span><span class="sxs-lookup"><span data-stu-id="b6158-112">The ASMX web service interface of the PSI is deprecated in Project Server 2013, but still works.</span></span> <span data-ttu-id="b6158-113">Die PSI ermöglicht einen effizienten Zugriff mithilfe von Datasets, und Sie können Handler für serverseitige Ereignisse erstellen.</span><span class="sxs-lookup"><span data-stu-id="b6158-113">The PSI enables efficient access by using datasets and you can create handlers for server-side events.</span></span> <span data-ttu-id="b6158-114">Das CSOM selbst verwendet die PSI, um auf die Project Server-Geschäftsobjektebene zu zugreifen.</span><span class="sxs-lookup"><span data-stu-id="b6158-114">The CSOM itself uses the PSI to access the Project Server business object layer.</span></span> <span data-ttu-id="b6158-115">Statt vier Project Serverdatenbanken verwendet Project Server 2013 eine einzelne Datenbank in der Datenzugriffsebene.</span><span class="sxs-lookup"><span data-stu-id="b6158-115">Instead of four Project Server databases, Project Server 2013 uses a single database in the data access layer.</span></span>
  
<span data-ttu-id="b6158-116">Project Server 2013 integriert sich tief in SharePoint Server 2013.</span><span class="sxs-lookup"><span data-stu-id="b6158-116">Project Server 2013 integrates deeply with SharePoint Server 2013.</span></span> <span data-ttu-id="b6158-117">Der Project-Anwendungsdienst kann anderen websitesammlungen SharePoint in der Farm zugeordnet werden.</span><span class="sxs-lookup"><span data-stu-id="b6158-117">The Project Application Service can be associated with other SharePoint site collections in the farm.</span></span> <span data-ttu-id="b6158-118">Project Server kann mit SharePoint Aufgabenlisten in der Websitesammlung arbeiten und diese melden und auch voll steuern, wo Project Server die Aufgabenlisten als Unternehmensprojekte importiert und verwaltet.</span><span class="sxs-lookup"><span data-stu-id="b6158-118">Project Server can operate with and report on SharePoint task lists in the site collection, and can also get full control where Project Server imports and manages the task lists as enterprise projects.</span></span> <span data-ttu-id="b6158-119">Project Server verwendet auch Version 4 des Windows Workflow Foundation (WF4) und fügt Workflowaktivitäten für Lösungen zur Bedarfsverwaltung hinzu.</span><span class="sxs-lookup"><span data-stu-id="b6158-119">Project Server also uses version 4 of the Windows Workflow Foundation (WF4) and adds workflow activities for Demand Management solutions.</span></span>
  
<span data-ttu-id="b6158-120">Eine Diskussion über die vielen neuen Features, die Project 2013 für Entwickler bietet, und der veralteten Features finden Sie unter [Updates for developers in Project 2013](updates-for-developers-in-project-2013.md).</span><span class="sxs-lookup"><span data-stu-id="b6158-120">For a discussion of the many new features that Project 2013 provides for developers, and of the features that are deprecated, see [Updates for developers in Project 2013](updates-for-developers-in-project-2013.md).</span></span>
  
## <a name="in-this-section"></a><span data-ttu-id="b6158-121">Inhalt dieses Abschnitts</span><span class="sxs-lookup"><span data-stu-id="b6158-121">In this section</span></span>

<span data-ttu-id="b6158-122">[Project Server 2013-Architektur](project-server-2013-architecture.md) beschreibt die wichtigsten Teile der Project 2013-Plattform, einschließlich der Clients und Server.</span><span class="sxs-lookup"><span data-stu-id="b6158-122">[Project Server 2013 architecture](project-server-2013-architecture.md) describes the major parts of the Project 2013 platform, including the clients and servers.</span></span> 
  
<span data-ttu-id="b6158-123">[Project Server-Programmierbarkeit](project-server-programmability.md) behandelt die wichtigsten Erweiterbarkeitsfeatures von Project Server 2013, die Anpassung von Project Web App und das Upgrade von Anwendungen, die für frühere Project Server-Versionen erstellt wurden.</span><span class="sxs-lookup"><span data-stu-id="b6158-123">[Project Server programmability](project-server-programmability.md) discusses the main extensibility features of Project Server 2013, customization of Project Web App, and upgrading applications that are built for previous Project Server versions.</span></span> 
  
<span data-ttu-id="b6158-124">[Was die PSI tut und](what-the-psi-does-and-does-not-do.md) nicht, beschreibt Szenarien, in denen die PSI verwendet werden kann, und listet Dinge auf, die die PSI nicht tun kann.</span><span class="sxs-lookup"><span data-stu-id="b6158-124">[What the PSI does and does not do](what-the-psi-does-and-does-not-do.md) describes scenarios where the PSI can be used and lists things that the PSI cannot do.</span></span> 
  
<span data-ttu-id="b6158-125">[Was das CSOM](what-the-csom-does-and-does-not-do.md) tut und nicht, beschreibt Szenarien, in denen das CSOM verwendet werden kann, und listet Dinge auf, die das CSOM nicht tun kann.</span><span class="sxs-lookup"><span data-stu-id="b6158-125">[What the CSOM does and does not do](what-the-csom-does-and-does-not-do.md) describes scenarios where the CSOM can be used and lists things that the CSOM cannot do.</span></span> 
  
### <a name="topics-not-covered"></a><span data-ttu-id="b6158-126">Themen, die nicht behandelt werden</span><span class="sxs-lookup"><span data-stu-id="b6158-126">Topics not covered</span></span>

<span data-ttu-id="b6158-127">Die Artikel im Abschnitt *Architektur* und Programmierbarkeit dokumentieren keine Features der Project-Desktopclients (Project Standard 2013 und Project Professional 2013) oder Project Web App.</span><span class="sxs-lookup"><span data-stu-id="b6158-127">The articles in the  *Architecture and programmability*  section do not document features of the Project desktop clients (Project Standard 2013 and Project Professional 2013) or Project Web App.</span></span> 
  
<span data-ttu-id="b6158-128">Visual Basic for Applications (VBA)-Hilfe ist im editor Visual Basic innerhalb von Project Standard und Project Professional.</span><span class="sxs-lookup"><span data-stu-id="b6158-128">Visual Basic for Applications (VBA) help is available in the Visual Basic editor within Project Standard and Project Professional.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="b6158-129">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="b6158-129">See also</span></span>
<span data-ttu-id="b6158-130"><a name="bk_addresources"> </a></span><span class="sxs-lookup"><span data-stu-id="b6158-130"><a name="bk_addresources"> </a></span></span>

- [<span data-ttu-id="b6158-131">Updates für Entwickler in Project 2013</span><span class="sxs-lookup"><span data-stu-id="b6158-131">Updates for developers in Project 2013</span></span>](updates-for-developers-in-project-2013.md)
    
- [<span data-ttu-id="b6158-132">Erste Schritte beim Entwickeln von Project Server-Workflows</span><span class="sxs-lookup"><span data-stu-id="b6158-132">Getting started developing Project Server workflows</span></span>](getting-started-developing-project-server-workflows.md)
    

