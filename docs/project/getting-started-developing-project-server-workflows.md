---
title: Erste Schritte beim Entwickeln von Project Server-Workflows
manager: soliver
ms.date: 08/10/2016
ms.audience: Developer
localization_priority: Normal
ms.assetid: 735bbb04-a8c1-46c0-a346-42050f0ac9b1
description: Die Anforderungsverwaltungsprozesse in Project Server 2013 umfassen Workflows, mit deren Hilfe Sie Projektvorschläge und Portfolioanalysen verwalten können. Dieser Abschnitt enthält Artikel mit Informationen zum Erstellen von Workflows für Project Server.
ms.openlocfilehash: 0a09022e63528f50ee4f0c8bd69bd6c34c5d8753
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32344471"
---
# <a name="getting-started-developing-project-server-workflows"></a><span data-ttu-id="c6cc9-104">Erste Schritte beim Entwickeln von Project Server-Workflows</span><span class="sxs-lookup"><span data-stu-id="c6cc9-104">Getting started developing Project Server workflows</span></span>

<span data-ttu-id="c6cc9-105">Die Anforderungsverwaltungsprozesse in Project Server 2013 umfassen Workflows, mit deren Hilfe Sie Projektvorschläge und Portfolioanalysen verwalten können.</span><span class="sxs-lookup"><span data-stu-id="c6cc9-105">Demand management processes in Project Server 2013 include workflows that help you manage project proposals and portfolio analyses.</span></span> <span data-ttu-id="c6cc9-106">Dieser Abschnitt enthält Artikel mit Informationen zum Erstellen von Workflows für Project Server.</span><span class="sxs-lookup"><span data-stu-id="c6cc9-106">This section includes articles that show how to create workflows for Project Server.</span></span>
  
<span data-ttu-id="c6cc9-107">Project Server 2013-Workflows verwenden die SharePoint Server 2013-Workflowplattform, die auf Version 4 von Windows Workflow Foundation (WF4) baut.</span><span class="sxs-lookup"><span data-stu-id="c6cc9-107">Project Server 2013 workflows use the SharePoint Server 2013 workflow platform, which is built on version 4 of Windows Workflow Foundation (WF4).</span></span> <span data-ttu-id="c6cc9-108">WF4-basierte Workflows sind deklarativ, was bedeutet, dass das Workflowentwurfstool Workflowphasen, Aktionen, Bedingungen und andere Elemente im XAML-Code speichert, der zur Laufzeit interpretiert wird.</span><span class="sxs-lookup"><span data-stu-id="c6cc9-108">WF4-based workflows are declarative, which means that the workflow design tool saves workflow stages, actions, conditions, and other elements to XAML code, which is interpreted at run-time.</span></span> <span data-ttu-id="c6cc9-109">Sie können entweder SharePoint Designer 2013 oder Visual Studio 2012 verwenden, um deklarative Workflows zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="c6cc9-109">You can use either SharePoint Designer 2013 or Visual Studio 2012 to create declarative workflows.</span></span> <span data-ttu-id="c6cc9-110">Für einen Workflow ist Workflow-Manager Client 1.0-Ausführungsmodul erforderlich, das sich auf einem lokalen Server für lokale Lösungen oder auf einem Remoteserver für Project Online befinden kann.</span><span class="sxs-lookup"><span data-stu-id="c6cc9-110">A workflow requires the Workflow Manager Client 1.0 execution engine, which can be on a local server for on-premises solutions or on a remote server for Project Online solutions.</span></span>
  
<span data-ttu-id="c6cc9-111">Sie können SharePoint Designer 2013 verwenden, um relativ einfache deklarative Workflows zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="c6cc9-111">You can use SharePoint Designer 2013 to create relatively simple declarative workflows.</span></span> <span data-ttu-id="c6cc9-112">Für komplexe Workflows und Workflowvorlagen, die wiederverwendet werden können, können Sie Visual Studio 2012 verwenden, um Workflows für Project Web App zu entwickeln und zu debuggen.</span><span class="sxs-lookup"><span data-stu-id="c6cc9-112">For complex workflows, and workflow templates that can be reused, you can use Visual Studio 2012 to develop and debug workflows for Project Web App.</span></span> <span data-ttu-id="c6cc9-113">Weitere Informationen finden Sie unter [Creating Project Workflows using Visual Studio 2012](https://blogs.msdn.com/b/project_programmability/archive/2012/11/07/creating-project-workflows-using-visual-studio-2012.aspx).</span><span class="sxs-lookup"><span data-stu-id="c6cc9-113">For more information, see [Creating Project Workflows using Visual Studio 2012](https://blogs.msdn.com/b/project_programmability/archive/2012/11/07/creating-project-workflows-using-visual-studio-2012.aspx).</span></span>
  
> [!IMPORTANT]
> <span data-ttu-id="c6cc9-114">Verwenden Sie eine Testinstallation von Project Server, nicht eine Produktionsinstallation, um Workflows zu entwickeln und zu testen.</span><span class="sxs-lookup"><span data-stu-id="c6cc9-114">Use a test installation of Project Server, not a production installation, to develop and test workflows.</span></span> <span data-ttu-id="c6cc9-115">Workflows, die für Vorabversionen von Project Server 2013 entwickelt wurden, müssen für die Releaseversion getestet und möglicherweise erneut erstellt und erneut zur Verfügung gestellt werden.</span><span class="sxs-lookup"><span data-stu-id="c6cc9-115">Workflows that are developed for pre-release versions of Project Server 2013 must be tested for the release version, and may have to be created again and redeployed.</span></span> 
  
## <a name="in-this-section"></a><span data-ttu-id="c6cc9-116">Inhalt dieses Abschnitts</span><span class="sxs-lookup"><span data-stu-id="c6cc9-116">In this section</span></span>

[<span data-ttu-id="c6cc9-117">Erstellen eines Project Serverworkflows für die Bedarfsverwaltung</span><span class="sxs-lookup"><span data-stu-id="c6cc9-117">Create a Project Server workflow for Demand Management</span></span>](create-a-project-server-workflow-for-demand-management.md)
  
## <a name="see-also"></a><span data-ttu-id="c6cc9-118">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="c6cc9-118">See also</span></span>



[<span data-ttu-id="c6cc9-119">Massenaktualisierung benutzerdefinierter Felder und Erstellen von Projektwebsites aus Project Online Workflow</span><span class="sxs-lookup"><span data-stu-id="c6cc9-119">Bulk update custom fields and create project sites from a Project Online workflow</span></span>](bulk-update-custom-fields-and-create-project-sites-from-workflow-in-project.md)


[<span data-ttu-id="c6cc9-120">Entwickeln von Workflows in SharePoint Designer 2013 und Visio 2013</span><span class="sxs-lookup"><span data-stu-id="c6cc9-120">Workflow development in SharePoint Designer 2013 and Visio 2013</span></span>](https://msdn.microsoft.com/library/jj163272%28office.15%29.aspx)
  
[<span data-ttu-id="c6cc9-121">Neuerungen in Workflows für SharePoint 2013</span><span class="sxs-lookup"><span data-stu-id="c6cc9-121">What's new in workflows for SharePoint 2013</span></span>](https://msdn.microsoft.com/library/jj163177.aspx)
  
[<span data-ttu-id="c6cc9-122">Entwickeln von SharePoint 2013-Workflows mit Visual Studio</span><span class="sxs-lookup"><span data-stu-id="c6cc9-122">Develop SharePoint 2013 workflows using Visual Studio</span></span>](https://msdn.microsoft.com/library/jj163199.aspx)
  
[<span data-ttu-id="c6cc9-123">Erstellen Project Workflows mit Visual Studio 2012</span><span class="sxs-lookup"><span data-stu-id="c6cc9-123">Creating Project Workflows using Visual Studio 2012</span></span>](https://blogs.msdn.com/b/project_programmability/archive/2012/11/07/creating-project-workflows-using-visual-studio-2012.aspx)
  
[<span data-ttu-id="c6cc9-124">Windows Workflow Foundation </span><span class="sxs-lookup"><span data-stu-id="c6cc9-124">Windows Workflow Foundation</span></span>](https://msdn.microsoft.com/library/dd489441.aspx)
  
[<span data-ttu-id="c6cc9-125">Einführung eines Entwicklers in Windows Workflow Foundation (WF) in .NET 4</span><span class="sxs-lookup"><span data-stu-id="c6cc9-125">A developer's introduction to Windows Workflow Foundation (WF) in .NET 4</span></span>](https://msdn.microsoft.com/library/ee342461.aspx)
  
[<span data-ttu-id="c6cc9-126">Hitchhiker es Guide to Demand Management (Whitepaper)</span><span class="sxs-lookup"><span data-stu-id="c6cc9-126">Hitchhiker's guide to demand management (white paper)</span></span>](https://msdn.microsoft.com/library/ff973112.aspx)

