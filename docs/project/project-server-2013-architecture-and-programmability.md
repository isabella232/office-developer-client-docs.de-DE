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
- Project 2013, Architektur und Programmierbarkeit, Programmierbarkeit, Project Server, Project 2013, Vorteile für EPM, Architecture und Project Server
localization_priority: Normal
ms.assetid: 9ea3b3c1-fb90-454a-b8e6-abc44fca663d
description: In den Artikeln in diesem Abschnitt wird die Gesamtarchitektur der Enterprise Project Management-Lösung (EPM) beschrieben, die Project Professional 2013, Project Server 2013, Project Web App und SharePoint Server 2013 kombiniert.
ms.openlocfilehash: 44cd5a32b8d3de421ffe3b2d9bf0137146bc4c4e
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32301470"
---
# <a name="project-server-2013-architecture-and-programmability"></a><span data-ttu-id="0289a-104">Project Server 2013-Architektur und Programmierbarkeit</span><span class="sxs-lookup"><span data-stu-id="0289a-104">Project Server 2013 architecture and programmability</span></span>

<span data-ttu-id="0289a-105">In den Artikeln in diesem Abschnitt wird die Gesamtarchitektur der Enterprise Project Management-Lösung (EPM) beschrieben, die Project Professional 2013, Project Server 2013, Project Web App und SharePoint Server 2013 kombiniert.</span><span class="sxs-lookup"><span data-stu-id="0289a-105">The articles in this section describe the overall architecture of the Enterprise Project Management (EPM) solution, which combines Project Professional 2013, Project Server 2013, Project Web App, and SharePoint Server 2013.</span></span>
  
<span data-ttu-id="0289a-106">Project Server 2013 wurde mit .NET Framework 4 erstellt und ist die dritte Hauptversion von Project Server, um eine echte mehrstufige Architektur bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="0289a-106">Project Server 2013 is built with the .NET Framework 4 and is the third major release of Project Server to provide a true multitier architecture.</span></span> <span data-ttu-id="0289a-107">Für den Cloud-Zugriff implementiert Project Server 2013 ein clientseitiges Objektmodell (CSOM) und einen OData-Dienst für Berichte, die in Webanwendungen, mobilen Anwendungen und Silverlight-Anwendungen verwendet werden können.</span><span class="sxs-lookup"><span data-stu-id="0289a-107">For cloud access, Project Server 2013 implements a client-side object model (CSOM) and an OData service for reporting that can be used in web applications, mobile applications, and Silverlight applications.</span></span> <span data-ttu-id="0289a-108">Für lokale Anwendungen können Clients entweder die CSOM oder die PSI-Dienste (Project Server Interface) verwenden.</span><span class="sxs-lookup"><span data-stu-id="0289a-108">For applications on-premises, clients can use either the CSOM or the Project Server Interface (PSI) services.</span></span> 
  
## <a name="introduction-to-project-server-architecture"></a><span data-ttu-id="0289a-109">Einführung in die Project Server-Architektur</span><span class="sxs-lookup"><span data-stu-id="0289a-109">Introduction to Project Server architecture</span></span>

<span data-ttu-id="0289a-110">Die Themen in diesem Abschnitt beschreiben die Gesamtarchitektur der Enterprise Project Management (EPM)-Lösung, die Project Professional 2013, Project Server 2013, Project Web App und SharePoint Server 2013 kombiniert.</span><span class="sxs-lookup"><span data-stu-id="0289a-110">The topics in this section describe the overall architecture of the Enterprise Project Management (EPM) solution, which combines Project Professional 2013, Project Server 2013, Project Web App, and SharePoint Server 2013.</span></span>
  
<span data-ttu-id="0289a-111">Für den programmgesteuerten Zugriff auf Project Server sollten Sie entweder die CSOM oder die PSI-Dienste mit der Windows Communication Foundation (WCF)-Schnittstelle verwenden.</span><span class="sxs-lookup"><span data-stu-id="0289a-111">For programmatic access to Project Server, you should use either the CSOM or the PSI services with the Windows Communication Foundation (WCF) interface.</span></span> <span data-ttu-id="0289a-112">Die ASMX-Webdienst-Schnittstelle der PSI ist in Project Server 2013 veraltet, funktioniert aber immer noch.</span><span class="sxs-lookup"><span data-stu-id="0289a-112">The ASMX web service interface of the PSI is deprecated in Project Server 2013, but still works.</span></span> <span data-ttu-id="0289a-113">Das PSI ermöglicht den effizienten Zugriff mithilfe von Datasets und Sie können Handler für serverseitige Ereignisse erstellen.</span><span class="sxs-lookup"><span data-stu-id="0289a-113">The PSI enables efficient access by using datasets and you can create handlers for server-side events.</span></span> <span data-ttu-id="0289a-114">Der CSOM selbst verwendet die PSI für den Zugriff auf die Project Server-Geschäftsobjektebene.</span><span class="sxs-lookup"><span data-stu-id="0289a-114">The CSOM itself uses the PSI to access the Project Server business object layer.</span></span> <span data-ttu-id="0289a-115">Anstelle von vier Project Server-Datenbanken verwendet Project Server 2013 eine einzelne Datenbank in der Datenzugriffsschicht.</span><span class="sxs-lookup"><span data-stu-id="0289a-115">Instead of four Project Server databases, Project Server 2013 uses a single database in the data access layer.</span></span>
  
<span data-ttu-id="0289a-116">Project Server 2013 ist in SharePoint Server 2013 integriert.</span><span class="sxs-lookup"><span data-stu-id="0289a-116">Project Server 2013 integrates deeply with SharePoint Server 2013.</span></span> <span data-ttu-id="0289a-117">Der Project-Anwendungsdienst kann anderen SharePoint-Websitesammlungen in der Farm zugeordnet werden.</span><span class="sxs-lookup"><span data-stu-id="0289a-117">The Project Application Service can be associated with other SharePoint site collections in the farm.</span></span> <span data-ttu-id="0289a-118">Project Server kann mit SharePoint-Aufgabenlisten in der Websitesammlung arbeiten und Berichte dazu und kann auch vollständige Kontrolle darüber erhalten, wo Project Server die Aufgabenlisten als Enterprise-Projekte importiert und verwaltet.</span><span class="sxs-lookup"><span data-stu-id="0289a-118">Project Server can operate with and report on SharePoint task lists in the site collection, and can also get full control where Project Server imports and manages the task lists as enterprise projects.</span></span> <span data-ttu-id="0289a-119">Project Server verwendet außerdem Version 4 des Windows Workflow Foundation (WF4) und fügt Workflow Aktivitäten für Bedarfs Verwaltungslösungen hinzu.</span><span class="sxs-lookup"><span data-stu-id="0289a-119">Project Server also uses version 4 of the Windows Workflow Foundation (WF4) and adds workflow activities for Demand Management solutions.</span></span>
  
<span data-ttu-id="0289a-120">Eine Erläuterung der vielen neuen Features von Project 2013 für Entwickler und der Features, die veraltet sind, finden Sie unter [Updates für Entwickler in project 2013](updates-for-developers-in-project-2013.md).</span><span class="sxs-lookup"><span data-stu-id="0289a-120">For a discussion of the many new features that Project 2013 provides for developers, and of the features that are deprecated, see [Updates for developers in Project 2013](updates-for-developers-in-project-2013.md).</span></span>
  
## <a name="in-this-section"></a><span data-ttu-id="0289a-121">Inhalt dieses Abschnitts</span><span class="sxs-lookup"><span data-stu-id="0289a-121">In this section</span></span>

<span data-ttu-id="0289a-122">In der [Architektur von Project Server 2013](project-server-2013-architecture.md) werden die wichtigsten Teile der Project 2013-Plattform beschrieben, einschließlich der Clients und Server.</span><span class="sxs-lookup"><span data-stu-id="0289a-122">[Project Server 2013 architecture](project-server-2013-architecture.md) describes the major parts of the Project 2013 platform, including the clients and servers.</span></span> 
  
<span data-ttu-id="0289a-123">[Project Server-Programmierbarkeit](project-server-programmability.md) erläutert die wichtigsten Erweiterbarkeitsfeatures von project Server 2013, die Anpassung von Project Web App und das Aktualisieren von Anwendungen, die für frühere Project Server-Versionen erstellt wurden.</span><span class="sxs-lookup"><span data-stu-id="0289a-123">[Project Server programmability](project-server-programmability.md) discusses the main extensibility features of Project Server 2013, customization of Project Web App, and upgrading applications that are built for previous Project Server versions.</span></span> 
  
<span data-ttu-id="0289a-124">[Was die PSI tut und was nicht](what-the-psi-does-and-does-not-do.md) , beschreibt Szenarios, in denen das PSI verwendet werden kann, und listet Dinge auf, die das PSI nicht kann.</span><span class="sxs-lookup"><span data-stu-id="0289a-124">[What the PSI does and does not do](what-the-psi-does-and-does-not-do.md) describes scenarios where the PSI can be used and lists things that the PSI cannot do.</span></span> 
  
<span data-ttu-id="0289a-125">[Was das CSOM tut und was nicht](what-the-csom-does-and-does-not-do.md) , beschreibt Szenarios, in denen die CSOM verwendet werden kann, und listet die Dinge auf, die das CSOM nicht ausführen kann.</span><span class="sxs-lookup"><span data-stu-id="0289a-125">[What the CSOM does and does not do](what-the-csom-does-and-does-not-do.md) describes scenarios where the CSOM can be used and lists things that the CSOM cannot do.</span></span> 
  
### <a name="topics-not-covered"></a><span data-ttu-id="0289a-126">Themen werden nicht behandelt</span><span class="sxs-lookup"><span data-stu-id="0289a-126">Topics not covered</span></span>

<span data-ttu-id="0289a-127">Die Artikel im Abschnitt *Architektur und Programmierbarkeit* dokumentieren nicht die Features der Project-Desktop Clients (project Standard 2013 und project Professional 2013) oder Project Web App.</span><span class="sxs-lookup"><span data-stu-id="0289a-127">The articles in the  *Architecture and programmability*  section do not document features of the Project desktop clients (Project Standard 2013 and Project Professional 2013) or Project Web App.</span></span> 
  
<span data-ttu-id="0289a-128">Visual Basic for Applications (VBA)-Hilfe ist im Visual Basic-Editor in Project Standard und Project Professional verfügbar.</span><span class="sxs-lookup"><span data-stu-id="0289a-128">Visual Basic for Applications (VBA) help is available in the Visual Basic editor within Project Standard and Project Professional.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="0289a-129">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="0289a-129">See also</span></span>
<span data-ttu-id="0289a-130"><a name="bk_addresources"> </a></span><span class="sxs-lookup"><span data-stu-id="0289a-130"></span></span>

- [<span data-ttu-id="0289a-131">Updates für Entwickler in Project 2013</span><span class="sxs-lookup"><span data-stu-id="0289a-131">Updates for developers in Project 2013</span></span>](updates-for-developers-in-project-2013.md)
    
- [<span data-ttu-id="0289a-132">Erste Schritte beim Entwickeln von Project Server-Workflows</span><span class="sxs-lookup"><span data-stu-id="0289a-132">Getting started developing Project Server workflows</span></span>](getting-started-developing-project-server-workflows.md)
    

