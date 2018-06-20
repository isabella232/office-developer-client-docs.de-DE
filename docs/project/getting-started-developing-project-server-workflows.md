---
title: Erste Schritte beim Entwickeln von Project Server-workflows
manager: soliver
ms.date: 08/10/2016
ms.audience: Developer
localization_priority: Normal
ms.assetid: 735bbb04-a8c1-46c0-a346-42050f0ac9b1
description: Bei Bedarf, dass Verwaltungsprozesse in Project Server 2013 Workflows enthalten, die Ihnen helfen Verwalten von Projektvorschlägen und Portfolioanalysen. Dieser Abschnitt enthält Artikel, die zeigen, wie Sie zum Erstellen von Workflows für Project Server.
ms.openlocfilehash: 275f61b7992423a5e10a7ba90b8c76433290343e
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19796163"
---
# <a name="getting-started-developing-project-server-workflows"></a><span data-ttu-id="66787-104">Erste Schritte beim Entwickeln von Project Server-workflows</span><span class="sxs-lookup"><span data-stu-id="66787-104">Getting started developing Project Server workflows</span></span>

<span data-ttu-id="66787-105">Bei Bedarf, dass Verwaltungsprozesse in Project Server 2013 Workflows enthalten, die Ihnen helfen Verwalten von Projektvorschlägen und Portfolioanalysen.</span><span class="sxs-lookup"><span data-stu-id="66787-105">Demand management processes in Project Server 2013 include workflows that help you manage project proposals and portfolio analyses.</span></span> <span data-ttu-id="66787-106">Dieser Abschnitt enthält Artikel, die zeigen, wie Sie zum Erstellen von Workflows für Project Server.</span><span class="sxs-lookup"><span data-stu-id="66787-106">This section includes articles that show how to create workflows for Project Server.</span></span>
  
<span data-ttu-id="66787-107">Project Server 2013-Workflows mithilfe die SharePoint Server 2013-Workflow-Plattform, die auf Windows Workflow Foundation (WF4), Version 4 erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="66787-107">Project Server 2013 workflows use the SharePoint Server 2013 workflow platform, which is built on version 4 of Windows Workflow Foundation (WF4).</span></span> <span data-ttu-id="66787-108">WF4 basierenden Workflows sind deklarative, was bedeutet, dass das Workflow-Entwurfstool Workflowstufen, Aktionen, Bedingungen und andere Elemente in XAML-Code speichert, die zur Laufzeit interpretiert wird.</span><span class="sxs-lookup"><span data-stu-id="66787-108">WF4-based workflows are declarative, which means that the workflow design tool saves workflow stages, actions, conditions, and other elements to XAML code, which is interpreted at run-time.</span></span> <span data-ttu-id="66787-109">SharePoint Designer 2013 oder Visual Studio 2012 können Sie um deklarative Workflows zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="66787-109">You can use either SharePoint Designer 2013 or Visual Studio 2012 to create declarative workflows.</span></span> <span data-ttu-id="66787-110">Ein Workflow muss das Workflow-Manager-Client 1.0-Ausführungsmodul, der auf einem lokalen Server für lokale Lösungen oder auf einem Remoteserver für Project Online Solutions sein kann.</span><span class="sxs-lookup"><span data-stu-id="66787-110">A workflow requires the Workflow Manager Client 1.0 execution engine, which can be on a local server for on-premises solutions or on a remote server for Project Online solutions.</span></span>
  
<span data-ttu-id="66787-111">SharePoint Designer 2013 können Sie um deklarative Workflows relativ einfach zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="66787-111">You can use SharePoint Designer 2013 to create relatively simple declarative workflows.</span></span> <span data-ttu-id="66787-112">Für komplexe Workflows und Workflowvorlagen, die wiederverwendet werden können, können Sie Visual Studio 2012 verwenden, entwickeln und Debuggen von Workflows für Project Web App.</span><span class="sxs-lookup"><span data-stu-id="66787-112">For complex workflows, and workflow templates that can be reused, you can use Visual Studio 2012 to develop and debug workflows for Project Web App.</span></span> <span data-ttu-id="66787-113">Weitere Informationen finden Sie unter [Erstellen von Project-Workflows mithilfe von Visual Studio 2012](http://blogs.msdn.com/b/project_programmability/archive/2012/11/07/creating-project-workflows-using-visual-studio-2012.aspx).</span><span class="sxs-lookup"><span data-stu-id="66787-113">For more information, see [Creating Project Workflows using Visual Studio 2012](http://blogs.msdn.com/b/project_programmability/archive/2012/11/07/creating-project-workflows-using-visual-studio-2012.aspx).</span></span>
  
> [!IMPORTANT]
> <span data-ttu-id="66787-114">Verwenden Sie eine Testinstallation von Project Server, eine produktive-Installation, entwickeln und Testen des Workflows.</span><span class="sxs-lookup"><span data-stu-id="66787-114">Use a test installation of Project Server, not a production installation, to develop and test workflows.</span></span> <span data-ttu-id="66787-115">Workflows, die für Vorabversionen von Project Server 2013 entwickelt werden für die endgültige Produktversion getestet werden müssen, und weist möglicherweise neu erstellt und erneut bereitgestellt werden.</span><span class="sxs-lookup"><span data-stu-id="66787-115">Workflows that are developed for pre-release versions of Project Server 2013 must be tested for the release version, and may have to be created again and redeployed.</span></span> 
  
## <a name="in-this-section"></a><span data-ttu-id="66787-116">Inhalt dieses Abschnitts</span><span class="sxs-lookup"><span data-stu-id="66787-116">In this section</span></span>

[<span data-ttu-id="66787-117">Erstellen eines Project Server-Workflows für das Bedarfsmanagement</span><span class="sxs-lookup"><span data-stu-id="66787-117">Create a Project Server workflow for Demand Management</span></span>](create-a-project-server-workflow-for-demand-management.md)
  
## <a name="see-also"></a><span data-ttu-id="66787-118">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="66787-118">See also</span></span>



[<span data-ttu-id="66787-119">Massen-Update für benutzerdefinierte Felder und Erstellen von Projektwebsites in Project Online-workflow</span><span class="sxs-lookup"><span data-stu-id="66787-119">Bulk update custom fields and create project sites from a Project Online workflow</span></span>](bulk-update-custom-fields-and-create-project-sites-from-workflow-in-project.md)


[<span data-ttu-id="66787-120">Workflowentwicklung in SharePoint Designer 2013 und Visio 2013</span><span class="sxs-lookup"><span data-stu-id="66787-120">Workflow development in SharePoint Designer 2013 and Visio 2013</span></span>](http://msdn.microsoft.com/en-us/library/jj163272%28office.15%29.aspx)
  
[<span data-ttu-id="66787-121">Neuerungen in Workflows für SharePoint 2013</span><span class="sxs-lookup"><span data-stu-id="66787-121">What's new in workflows for SharePoint 2013</span></span>](http://msdn.microsoft.com/en-us/library/jj163177.aspx)
  
[<span data-ttu-id="66787-122">Entwickeln von SharePoint 2013-Workflows mit Visual Studio</span><span class="sxs-lookup"><span data-stu-id="66787-122">Develop SharePoint 2013 workflows using Visual Studio</span></span>](http://msdn.microsoft.com/en-us/library/jj163199.aspx)
  
[<span data-ttu-id="66787-123">Erstellen von Project-Workflows mit Visual Studio 2012</span><span class="sxs-lookup"><span data-stu-id="66787-123">Creating Project Workflows using Visual Studio 2012</span></span>](http://blogs.msdn.com/b/project_programmability/archive/2012/11/07/creating-project-workflows-using-visual-studio-2012.aspx)
  
[<span data-ttu-id="66787-124">Windows Workflow Foundation</span><span class="sxs-lookup"><span data-stu-id="66787-124">Windows Workflow Foundation</span></span>](http://msdn.microsoft.com/en-us/library/dd489441.aspx)
  
[<span data-ttu-id="66787-125">Einführung in die ein Entwickler zu Windows Workflow Foundation (WF) in .NET 4</span><span class="sxs-lookup"><span data-stu-id="66787-125">A developer's introduction to Windows Workflow Foundation (WF) in .NET 4</span></span>](http://msdn.microsoft.com/en-us/library/ee342461.aspx)
  
[<span data-ttu-id="66787-126">Implementierung des projektbedarfsmanagements projektbedarfsmanagement (Whitepaper)</span><span class="sxs-lookup"><span data-stu-id="66787-126">Hitchhiker's guide to demand management (white paper)</span></span>](http://msdn.microsoft.com/en-us/library/ff973112.aspx)

