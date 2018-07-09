---
title: Project-Clientprogrammierung
manager: soliver
ms.date: 08/10/2016
ms.audience: Developer
f1_keywords:
- object model
- Project object model
- Project VBA
- VBA
keywords:
- VBA, Object Model, Project, Programmierbarkeit, project-Programmierung, Project VBA, Visual Basic für Applikationen, Project-Objektmodell, VBA, Objekt Objektmodell, VBA, Visual Basic für Applikationen
localization_priority: Normal
ms.assetid: 0ad49ff6-8dff-4379-a52c-d292c53c2bc0
description: Die Project 2013-desktop-Clientanwendungen – Project Standard 2013 und Project Professional 2013 – angepasst und mithilfe von VBA Makros schreiben erweitert werden kann. Visual Studio 2012 können zum Anpassen der Menüband-Benutzeroberfläche und Erstellen komplexer-add-ins Office-Add-ins ermöglicht eine neue Erweiterbarkeit modellieren für Aufgabenbereichen in Project, die auf einer gemeinsamen Plattform für Office 2013 integriert sind. Project Standard 2013 und Project Professional 2013 können allgemeine Office-Add-ins ausführen und Verwenden des Task Pane-add-ins, die speziell für das Projekt für die Integration von SharePoint, andere Websites und Webanwendungen und externe Daten entwickelt werden.
ms.openlocfilehash: e8604b4d479d0c64f8d45ad2363d7391d57408ed
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19796302"
---
# <a name="project-client-programming"></a><span data-ttu-id="2d371-106">Project-Clientprogrammierung</span><span class="sxs-lookup"><span data-stu-id="2d371-106">Project client programming</span></span>

<span data-ttu-id="2d371-107">Die Project 2013-desktop-Clientanwendungen – Project Standard 2013 und Project Professional 2013 – angepasst und mithilfe von VBA Makros schreiben erweitert werden kann.</span><span class="sxs-lookup"><span data-stu-id="2d371-107">The Project 2013 desktop client applications—Project Standard 2013 and Project Professional 2013—can be customized and extended by using VBA to write macros.</span></span> <span data-ttu-id="2d371-108">Visual Studio 2012 können zum Anpassen der Menüband-Benutzeroberfläche und Erstellen komplexer-add-ins Office-Add-ins ermöglicht eine neue Erweiterbarkeit modellieren für Aufgabenbereichen in Project, die auf einer gemeinsamen Plattform für Office 2013 integriert sind.</span><span class="sxs-lookup"><span data-stu-id="2d371-108">You can use Visual Studio 2012 to customize the ribbon user interface and create complex add-ins. Office Add-ins enables a new extensibility model for task panes in Project that are built on a common Office 2013 platform.</span></span> <span data-ttu-id="2d371-109">Project Standard 2013 und Project Professional 2013 können allgemeine Office-Add-ins ausführen und Verwenden des Task Pane-add-ins, die speziell für das Projekt für die Integration von SharePoint, andere Websites und Webanwendungen und externe Daten entwickelt werden.</span><span class="sxs-lookup"><span data-stu-id="2d371-109">Project Standard 2013 and Project Professional 2013 can run general Office Add-ins and use task pane add-ins that are developed specifically for Project to integrate with SharePoint, other websites and web applications, and external data.</span></span>
  
 <span data-ttu-id="2d371-110">**Verschieben in Visual Studio** VBA ist hilfreich für das Aufzeichnen von Makros und Entwickeln von Lösungen relativ einfach Automatisierung.</span><span class="sxs-lookup"><span data-stu-id="2d371-110">**Moving to Visual Studio** VBA is useful for recording macros and developing relatively simple automation solutions.</span></span> <span data-ttu-id="2d371-111">Informationen zum Entwickeln von Task Pane-add-ins sollten-add-ins und weitere komplexe, sichere, skalierbare, und auf einfache Weise bereitgestellter Lösungen für die Verwendung von Visual Studio 2012.</span><span class="sxs-lookup"><span data-stu-id="2d371-111">To develop task pane add-ins, add-ins, and more complex, secure, scalable, and easily deployed solutions, we recommend that you use Visual Studio 2012.</span></span> <span data-ttu-id="2d371-112">Microsoft .NET Framework 4.0 und die primäre Interopassembly für Project 2013 bieten viele Vorteile für das Entwickeln und Bereitstellen von Lösungen, die Automatisierung und Integration von Project 2013-desktop-Clients.</span><span class="sxs-lookup"><span data-stu-id="2d371-112">The Microsoft .NET Framework 4.0 and the Project 2013 primary interop assembly provide many advantages for developing and deploying solutions that automate and integrate the Project 2013 desktop clients.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="2d371-113">Visual Studio 2010 können Sie das um Projekt-add-ins zu entwickeln. Visual Studio 2012 enthält jedoch Vorlagen und Erweiterungen, die Office-Add-ins Clients erstellen sollen.</span><span class="sxs-lookup"><span data-stu-id="2d371-113">You can use Visual Studio 2010 to develop Project add-ins. However, Visual Studio 2012 includes templates and extensions that are designed to create Office Add-ins clients.</span></span> 
  
<span data-ttu-id="2d371-114">Das **MSProject** -Objektmodell für VBA in Project 2013 ist im Wesentlichen identisch mit **Microsoft.Office.Interop.MSProject** -Objektmodell für verwalteten Code-Lösungen mit Office Developer Tools für Visual Studio 2013 (auch bekannt als VSTO).</span><span class="sxs-lookup"><span data-stu-id="2d371-114">The **MSProject** object model for VBA in Project 2013 is essentially the same as the **Microsoft.Office.Interop.MSProject** object model for managed-code solutions with Office Developer Tools for Visual Studio 2013 (also known as VSTO).</span></span> <span data-ttu-id="2d371-115">Visual Studio 2012 enthält Vorlagen für die Entwicklung von auf Anwendungsebene-add-ins für Project 2010 und Project 2013 (Project Standard oder Project Professional-Versionen).</span><span class="sxs-lookup"><span data-stu-id="2d371-115">Visual Studio 2012 includes templates for developing application-level add-ins for Project 2010 and for Project 2013 (either the Project Standard or Project Professional versions).</span></span> <span data-ttu-id="2d371-116">Entwickeln, testen und Bereitstellen von erweiterten Integration-Lösungen, die mit dem Project-desktop-Client und andere Office 2013-Anwendungen und Integration mit SharePoint-Websites, Listen, VSTO und Office Developer Tools für Visual Studio 2012 zu vereinfachen und Workflows.</span><span class="sxs-lookup"><span data-stu-id="2d371-116">VSTO and Office Developer Tools for Visual Studio 2012 simplify developing, testing, and deploying advanced integration solutions that can use the Project desktop client and other Office 2013 applications, and integrate with SharePoint sites, lists, and workflows.</span></span> 
  
<span data-ttu-id="2d371-117">Task Pane-add-ins und andere add-ins für Office und SharePoint im Office Store verkauft werden (siehe [http://office.microsoft.com/store/](http://office.microsoft.com/en-us/store/)) für die Verwendung mit Project Online und lokale Installationen.</span><span class="sxs-lookup"><span data-stu-id="2d371-117">Task pane add-ins and other add-ins for Office and SharePoint can be sold in the Office Store (see [http://office.microsoft.com/store/](http://office.microsoft.com/en-us/store/)) for use with both Project Online and on-premises installations.</span></span> <span data-ttu-id="2d371-118">VBA-Makros und VSTO-add-ins können nicht im Office Store verteilt werden sollen; Sie dienen zur lokalen Verwendung mit Project Standard und Project Professional.</span><span class="sxs-lookup"><span data-stu-id="2d371-118">VBA macros and VSTO add-ins cannot be distributed in the Office Store; they are designed for local use with Project Standard and Project Professional.</span></span> <span data-ttu-id="2d371-119">Sie können VBA-Makros innerhalb eines Projekts verteilen. MPP-Datei, in der Datei Global.MPT auf Ihrem Computer zu installieren, oder in der Enterprise-global-Projektvorlage in Project Server 2013 zu verteilen.</span><span class="sxs-lookup"><span data-stu-id="2d371-119">You can distribute VBA macros within a project .MPP file, install them in the Global.MPT file on your computer, or distribute them in the enterprise global template in Project Server 2013.</span></span> <span data-ttu-id="2d371-120">VSTO-add-ins können sicherer über [ClickOnce](http://msdn.microsoft.com/de-de/library/t71a733d.aspx) -Bereitstellung verteilt werden, wodurch einfache Updates.</span><span class="sxs-lookup"><span data-stu-id="2d371-120">VSTO add-ins can be distributed more securely through [ClickOnce](http://msdn.microsoft.com/de-de/library/t71a733d.aspx) deployment, which enables easy updates.</span></span> 
  
## <a name="reference"></a><span data-ttu-id="2d371-121">Referenz</span><span class="sxs-lookup"><span data-stu-id="2d371-121">Reference</span></span>

<span data-ttu-id="2d371-122">[Project-VBA-Entwicklerreferenz (engl.)](http://msdn.microsoft.com/de-de/library/ee861523%28office.15%29.aspx) Enthält einführende und VBA-Hilfe-Artikel.</span><span class="sxs-lookup"><span data-stu-id="2d371-122">[Project VBA developer reference](http://msdn.microsoft.com/de-de/library/ee861523%28office.15%29.aspx) Contains introductory and VBA Help articles.</span></span> 
  
## <a name="related-sections"></a><span data-ttu-id="2d371-123">Verwandte Abschnitte</span><span class="sxs-lookup"><span data-stu-id="2d371-123">Related sections</span></span>

<span data-ttu-id="2d371-124">[Project Server 2013-Architektur](project-server-2013-architecture.md) Zeigt, wie die Project-Clients mit Project Server interagieren.</span><span class="sxs-lookup"><span data-stu-id="2d371-124">[Project Server 2013 architecture](project-server-2013-architecture.md) Shows how the Project clients interact with Project Server.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="2d371-125">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="2d371-125">See also</span></span>



[<span data-ttu-id="2d371-126">Project für Entwickler</span><span class="sxs-lookup"><span data-stu-id="2d371-126">Project for developers</span></span>](http://msdn.microsoft.com/de-de/office/aa905469)
  
[<span data-ttu-id="2d371-127">Office Developercenter</span><span class="sxs-lookup"><span data-stu-id="2d371-127">Office developer center</span></span>](https://dev.office.com)
  
[<span data-ttu-id="2d371-128">Visual Studio Developer center</span><span class="sxs-lookup"><span data-stu-id="2d371-128">Visual Studio developer center</span></span>](http://msdn.microsoft.com/en-us/vstudio/aa718325.aspx)
  
[<span data-ttu-id="2d371-129">ClickOnce-Sicherheit und Bereitstellung</span><span class="sxs-lookup"><span data-stu-id="2d371-129">ClickOnce Security and Deployment</span></span>](http://msdn.microsoft.com/de-de/library/t71a733d.aspx)
  
[<span data-ttu-id="2d371-130">Verfügbare Felder</span><span class="sxs-lookup"><span data-stu-id="2d371-130">Available fields reference</span></span>](http://office.microsoft.com/en-us/project-help/available-fields-reference-HA102749299.aspx?CTT=1)

