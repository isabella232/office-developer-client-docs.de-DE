---
title: Entwickeln eines Project Online add-Ins mithilfe der JavaScript-Objektmodell (JSOM)
manager: soliver
ms.date: 11/08/2016
ms.audience: Developer
localization_priority: Normal
ms.assetid: 4a4b1ad2-de46-421d-a698-53c20c90b93a
description: In diesem Artikel wird beschrieben, Microsoft Project Online-Add-in-Entwicklung, um Ihre Erfahrung mit Project Online zu verbessern. Das Entwicklungsprojekt wird als eine exemplarische Vorgehensweise implementiert. Das Add-In für diesen Artikel verwendet liest und zeigt den Projektnamen und die veröffentlichten Projekte von Ihrem Konto Project Online-IDs und ermöglicht es Ihnen, einen Drilldown abrufen Aufgaben im Zusammenhang mit den einzelnen Projekten.
ms.openlocfilehash: ea5c7e3f3d20aa6bf5b6bb77a18eb87d06f549e1
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2018
ms.locfileid: "22572543"
---
# <a name="developing-a-project-online-add-in-using-the-javascript-object-model-jsom"></a><span data-ttu-id="a7631-105">Entwickeln eines Project Online add-Ins mithilfe der JavaScript-Objektmodell (JSOM)</span><span class="sxs-lookup"><span data-stu-id="a7631-105">Developing a Project Online add-in using the JavaScript Object Model (JSOM)</span></span>

<span data-ttu-id="a7631-106">In diesem Artikel wird beschrieben, Microsoft Project Online-Add-in-Entwicklung, um Ihre Erfahrung mit Project Online zu verbessern.</span><span class="sxs-lookup"><span data-stu-id="a7631-106">This article describes Microsoft Project Online Add-in development to enhance your experience with the Project Online.</span></span> <span data-ttu-id="a7631-107">Das Entwicklungsprojekt wird als eine exemplarische Vorgehensweise implementiert.</span><span class="sxs-lookup"><span data-stu-id="a7631-107">The development project is implemented as a walkthrough.</span></span> <span data-ttu-id="a7631-108">Das Add-In für diesen Artikel verwendet liest und zeigt den Projektnamen und die veröffentlichten Projekte von Ihrem Konto Project Online-IDs und ermöglicht es Ihnen, einen Drilldown abrufen Aufgaben im Zusammenhang mit den einzelnen Projekten.</span><span class="sxs-lookup"><span data-stu-id="a7631-108">The add-in used for this article reads and displays the project names and IDs of the published projects from your Project Online account and allows you to drill down to retrieve tasks associated with individual projects.</span></span>
  
<span data-ttu-id="a7631-109">Zur Laufzeit aussieht in der folgenden Abbildung ähnlich die Add-in-Auflistung:</span><span class="sxs-lookup"><span data-stu-id="a7631-109">At run time, the add-in listing looks similar to the following illustration:</span></span>
  
<span data-ttu-id="a7631-110">![Screenshot zeigt eine Liste von JSOM Projekten und Vorgängen] (media/766e5914-f048-48f4-9282-291f55e6e90d.png "Screenshot zeigt eine Liste von JSOM Projekten und Vorgängen")</span><span class="sxs-lookup"><span data-stu-id="a7631-110">![Screen shot showing a listing of JSOM projects and tasks](media/766e5914-f048-48f4-9282-291f55e6e90d.png "Screen shot showing a listing of JSOM projects and tasks")</span></span>
  
<span data-ttu-id="a7631-111">Der Fokus des Beispiels wird die Interaktion mit dem Project Online, Abfragen und Festlegen des Kontexts für jede Anforderung aus dem Dienst.</span><span class="sxs-lookup"><span data-stu-id="a7631-111">The focus of the example is the interaction with the Project Online, making queries and setting the context for each request from the service.</span></span> <span data-ttu-id="a7631-112">Elemente der Benutzeroberfläche (UI) empfangen minimale Aufmerksamkeit.</span><span class="sxs-lookup"><span data-stu-id="a7631-112">User interface (UI) elements receive minimal attention.</span></span> <span data-ttu-id="a7631-113">Stattdessen bieten die Source-Auflistungen Kommentare bezüglich der Benutzeroberfläche.</span><span class="sxs-lookup"><span data-stu-id="a7631-113">Instead, the source listings provide comments regarding the UI.</span></span>
  
> [!NOTE]
> <span data-ttu-id="a7631-114">Die Quelldateien für das Beispiel add-in, ein Visual Studio-Projekt sind verfügbar unter: https://github.com/OfficeDev/Project-JSOM-List-Projects-Tasks.....</span><span class="sxs-lookup"><span data-stu-id="a7631-114">The source files for the example add-in, a Visual Studio project, are available at: https://github.com/OfficeDev/Project-JSOM-List-Projects-Tasks.....</span></span> <span data-ttu-id="a7631-115">Halten Sie die Quelldateien bereit als Referenz beim Lesen des Artikels wie jeden anderen ergänzt.</span><span class="sxs-lookup"><span data-stu-id="a7631-115">Keep the source files handy as a reference while you read the article, as each complements the other.</span></span> <span data-ttu-id="a7631-116">Die Dateien in der Visual Studio project Build und mit minimalen Änderungen ausführbar sind – ersetzen die URL für Ihren Project Online-Mandanten nach unten zu den PWA-Ordner.</span><span class="sxs-lookup"><span data-stu-id="a7631-116">The files in the Visual Studio project build and are executable with minimal changes—substituting the URL for your Project Online tenant down to the PWA folder.</span></span> 
  
## <a name="background"></a><span data-ttu-id="a7631-117">Hintergrund</span><span class="sxs-lookup"><span data-stu-id="a7631-117">Background</span></span>

<span data-ttu-id="a7631-118">Project Online ist ein Office 365-Dienst, der bietet Unternehmen eine Project Portfoliomanagement (PPM) und Project Management (PMO) Office-Lösung zu koordinieren und Verwalten von Portfolios, Programmen und Projekten.</span><span class="sxs-lookup"><span data-stu-id="a7631-118">Project Online is a Office 365 service that provides companies with a project portfolio management (PPM) and project management office (PMO) solution to coordinate and manage portfolios, programs, and projects.</span></span> <span data-ttu-id="a7631-119">Project Online ist eine unterschiedliche besser als die Project-desktop-Versionen. noch enthält Project Online noch die Funktionalität zum Verwalten und Nachverfolgen von Projektdetails im Lebenszyklus eines Projekts.</span><span class="sxs-lookup"><span data-stu-id="a7631-119">Project Online is a different offering than the Project desktop editions; yet, Project Online still contains the functionality to maintain and track project details throughout the life of a project.</span></span> <span data-ttu-id="a7631-120">Project Online baut auf SharePoint Online.</span><span class="sxs-lookup"><span data-stu-id="a7631-120">Project Online is built on SharePoint Online.</span></span>
  
<span data-ttu-id="a7631-121">Ein Project Online gehostet Add-in besteht aus JavaScript und Ressource-Dateien, die mit der Client-Side-Objektmodell-API interagieren.</span><span class="sxs-lookup"><span data-stu-id="a7631-121">A Project Online hosted add-in consists of JavaScript and resource files that interact with the Client-Side-Object-Model API.</span></span> <span data-ttu-id="a7631-122">Wenn der Benutzer das Add-in besucht, werden die JavaScript und Ressourcen heruntergeladen und im Browser ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="a7631-122">When the user visits the add-in, the JavaScript and resources are downloaded and executed within the browser.</span></span> <span data-ttu-id="a7631-123">Das Add-In wird asynchroner Aufrufe für Project Online mit dem Dienst interagieren, ob erstellen, abrufen, aktualisieren und Löschen von Daten.</span><span class="sxs-lookup"><span data-stu-id="a7631-123">The add-In makes asynchronous calls to Project Online to interact with the service, whether creating, retrieving, updating, or deleting data.</span></span> 
  
<span data-ttu-id="a7631-124">Project Online führt eine weitere Aktion zum Schutz von Informationen, die über das Add-in zu anderen Mandanten gehört. Project Online erstellt nämlich eine isolierte Website zur Interaktion mit den Anforderungen von das Add-in.</span><span class="sxs-lookup"><span data-stu-id="a7631-124">Project Online performs one more action to protect information that belongs to other tenants from the add-in; namely, Project Online creates an isolated site to interact with the requests from the add-in.</span></span> <span data-ttu-id="a7631-125">Kein benutzerdefinierter Code ausgeführt wird, auf dem Project Online-Host.</span><span class="sxs-lookup"><span data-stu-id="a7631-125">No custom code runs on the Project Online host.</span></span> 
  
<span data-ttu-id="a7631-126">Die Einrichtung der Entwicklung für Project Online-add-ins verwendet den Projekttyp Visual Studio SharePoint-Add-in.</span><span class="sxs-lookup"><span data-stu-id="a7631-126">The development setup for Project Online add-ins uses the Visual Studio SharePoint Add-in project type.</span></span> <span data-ttu-id="a7631-127">Das Add-In wird in JavaScript geschrieben, und das Projekt JavaScript-Objektmodell (JSOM) für die Interaktion mit dem Project Online-Dienst verwendet.</span><span class="sxs-lookup"><span data-stu-id="a7631-127">The add-in is written in JavaScript, and uses the Project JavaScript object model (JSOM) to interact with the Project Online service.</span></span> <span data-ttu-id="a7631-128">Die JSOM erbt Großteil der Funktionalität von der SharePoint JSOM.</span><span class="sxs-lookup"><span data-stu-id="a7631-128">The JSOM inherits much of its functionality from the SharePoint JSOM.</span></span>
  
> [!NOTE]
> <span data-ttu-id="a7631-129">-Add-ins können veröffentlicht und in den Office Store verkauft oder mit einem privaten app-Katalog in SharePoint bereitgestellt werden.</span><span class="sxs-lookup"><span data-stu-id="a7631-129">Add-ins can be published and sold in the Office Store or deployed to a private app catalog on SharePoint.</span></span> <span data-ttu-id="a7631-130">Weitere Informationen finden Sie unter [Bereitstellen und veröffentlichen Sie Ihre Office-Add-in](https://docs.microsoft.com/en-us/office/dev/add-ins/publish/publish).</span><span class="sxs-lookup"><span data-stu-id="a7631-130">For more information, see [Deploy and publish your Office Add-in](https://docs.microsoft.com/en-us/office/dev/add-ins/publish/publish).</span></span>
> 
> <span data-ttu-id="a7631-131">Das Add-in, das in diesem Artikel verwendeten ist ein Beispiel für Entwickler. Es ist nicht für die Verwendung in einer produktionsumgebung vorgesehen.</span><span class="sxs-lookup"><span data-stu-id="a7631-131">The add-in used in this article is a sample for developers; it is not intended for use in a production environment.</span></span> <span data-ttu-id="a7631-132">Der primäre Zweck ist ein Beispiel für app-Entwicklung für Project Online angezeigt.</span><span class="sxs-lookup"><span data-stu-id="a7631-132">The primary purpose is to show an example of app development for Project Online.</span></span> 
  
## <a name="prerequisites"></a><span data-ttu-id="a7631-133">Voraussetzungen</span><span class="sxs-lookup"><span data-stu-id="a7631-133">Prerequisites</span></span>

<span data-ttu-id="a7631-134">Fügen Sie die folgenden Elemente zu einer unterstützten Windows-Umgebung:</span><span class="sxs-lookup"><span data-stu-id="a7631-134">Add the following items to a supported Windows environment:</span></span>
  
- <span data-ttu-id="a7631-135">**.NET Framework 4.0 oder höher**: vollständige Framework Version 4.0-Versionen kompatibel sind.</span><span class="sxs-lookup"><span data-stu-id="a7631-135">**.NET Framework 4.0 or later**: Complete versions of the framework from version 4.0 are compatible.</span></span> <span data-ttu-id="a7631-136">Die Download-Website ist https://msdn.microsoft.com/en-us/vstudio/aa496123.aspx.</span><span class="sxs-lookup"><span data-stu-id="a7631-136">The download site is https://msdn.microsoft.com/en-us/vstudio/aa496123.aspx.</span></span>
    
- <span data-ttu-id="a7631-137">**Visual Studio 2013 oder höher**:</span><span class="sxs-lookup"><span data-stu-id="a7631-137">**Visual Studio 2013 or later**:</span></span>  
    
   - <span data-ttu-id="a7631-138">Die professional Edition von Visual Studio 2015 ist bereit zur ausgehend von der im Feld wechseln und finden Sie unter https://www.visualstudio.com/en-us/products/visual-studio-professional-with-msdn-vs.aspx.</span><span class="sxs-lookup"><span data-stu-id="a7631-138">The professional edition of Visual Studio 2015 is ready to go out-of-the box and is available at https://www.visualstudio.com/en-us/products/visual-studio-professional-with-msdn-vs.aspx.</span></span>
    
   - <span data-ttu-id="a7631-139">Die Community-Edition von Visual Studio 2015 steht unter https://www.visualstudio.com/en-us/products/visual-studio-community-vs.aspx.</span><span class="sxs-lookup"><span data-stu-id="a7631-139">The community edition of Visual Studio 2015 is available at https://www.visualstudio.com/en-us/products/visual-studio-community-vs.aspx.</span></span> <span data-ttu-id="a7631-140">Diese Edition erfordert die manuelle Installation von Microsoft Office Developer Tools für Visual Studio.</span><span class="sxs-lookup"><span data-stu-id="a7631-140">This edition requires manual installation of the Microsoft Office Developer Tools for Visual Studio.</span></span>
    
   <span data-ttu-id="a7631-141">Die Microsoft Office Developer Tools für Visual Studio stehen unter https://www.visualstudio.com/en-us/features/office-tools-vs.aspx.</span><span class="sxs-lookup"><span data-stu-id="a7631-141">The Microsoft Office Developer Tools for Visual Studio are available at https://www.visualstudio.com/en-us/features/office-tools-vs.aspx.</span></span>
    
- <span data-ttu-id="a7631-142">**Eine Project Online-Konto**: Dies ermöglicht den Zugriff auf die hosting-Dienst.</span><span class="sxs-lookup"><span data-stu-id="a7631-142">**A Project Online account**: This provides access to the hosting service.</span></span> <span data-ttu-id="a7631-143">Weitere Informationen dazu, wie Sie ein Konto mit Project Online erhalten, finden Sie unter https://products.office.com/en-us/Project/project-online-portfolio-management.</span><span class="sxs-lookup"><span data-stu-id="a7631-143">For more information about obtaining a Project Online account, see https://products.office.com/en-us/Project/project-online-portfolio-management.</span></span>
    
   <span data-ttu-id="a7631-144">Stellen Sie sicher, dass der Add-in-Benutzer über die erforderlichen Berechtigungen auf einige Projekte in Project Online-Mandanten zuzugreifen.</span><span class="sxs-lookup"><span data-stu-id="a7631-144">Ensure that the add-in user has sufficient authorization to access some projects in the Project Online tenant.</span></span> 
    
- <span data-ttu-id="a7631-145">**Projekte auf der hosting-Website** , die mit Daten aufgefüllt werden.</span><span class="sxs-lookup"><span data-stu-id="a7631-145">**Projects on the hosting site** that are populated with information.</span></span>
    
> [!NOTE]
> <span data-ttu-id="a7631-146">Der Standard ist .NET Framework die richtige Framework verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="a7631-146">The standard .NET Framework is the correct framework to use.</span></span> <span data-ttu-id="a7631-147">Verwenden Sie ".NET Framework 4 Client Profile" nicht.</span><span class="sxs-lookup"><span data-stu-id="a7631-147">Do not use the ".NET Framework 4 Client Profile".</span></span> 
  
### <a name="set-up-the-visual-studio-project"></a><span data-ttu-id="a7631-148">Einrichten des Visual Studio-Projekts</span><span class="sxs-lookup"><span data-stu-id="a7631-148">Set up the Visual Studio project</span></span>

<span data-ttu-id="a7631-149">Erstellen eines neuen Projekts, verknüpfen die entsprechenden Bibliotheken und deklarieren die erforderlichen Namespaces besteht der Installation der Anwendung aus.</span><span class="sxs-lookup"><span data-stu-id="a7631-149">The application setup consists of creating a new project, linking the appropriate libraries and declaring the needed namespaces.</span></span> <span data-ttu-id="a7631-150">Visual Studio stellt verschiedene Arten von Entwicklungsprojekten.</span><span class="sxs-lookup"><span data-stu-id="a7631-150">Visual Studio presents several types of development projects.</span></span> <span data-ttu-id="a7631-151">Der Abschnitt ist kurz und elementare.</span><span class="sxs-lookup"><span data-stu-id="a7631-151">The section is brief and very basic.</span></span> <span data-ttu-id="a7631-152">Der Wert die Informationen Servercomputer ist an einem Ort gemischt zusammengefügt.</span><span class="sxs-lookup"><span data-stu-id="a7631-152">The value is having the information is coalesced in one place.</span></span>
  
#### <a name="select-a-visual-studio-project"></a><span data-ttu-id="a7631-153">Wählen Sie ein Visual Studio-Projekt</span><span class="sxs-lookup"><span data-stu-id="a7631-153">Select a Visual Studio project</span></span>

<span data-ttu-id="a7631-154">Wenn Sie ein Projekt des entsprechenden Typs für das Add-in erstellen, müssen Sie die folgenden Schritte durchführen.</span><span class="sxs-lookup"><span data-stu-id="a7631-154">To create a project of the appropriate type for the add-in, you must do the following steps.</span></span> <span data-ttu-id="a7631-155">Schlüsselwörter aufgetreten ist, auf dem Bildschirm aufweisen eine **Fett** Attribut:</span><span class="sxs-lookup"><span data-stu-id="a7631-155">Keywords encountered on the screen have a **bold** attribute:</span></span> 
  
1. <span data-ttu-id="a7631-156">Wählen Sie im Menü Datei die Option **Datei** > **New** > **Projekt**.</span><span class="sxs-lookup"><span data-stu-id="a7631-156">From the File menu, choose **File** > **New** > **Project**.</span></span> 
    
2. <span data-ttu-id="a7631-157">Wählen Sie im linken Bereich die installierte Vorlagen ein **C#-** > **Office/SharePoint** > **Web-Add-ins**.</span><span class="sxs-lookup"><span data-stu-id="a7631-157">From the Installed templates in the left pane, select **C#** > **Office/SharePoint** > **Web Add-ins**.</span></span> 
    
3. <span data-ttu-id="a7631-158">Wählen Sie am oberen Rand der mittleren Bereich, **.NET Framework 4** oder höher; die aktuelle Version ist 4.6.</span><span class="sxs-lookup"><span data-stu-id="a7631-158">At the top of the central pane, select **.NET Framework 4** or later; the current version is 4.6.</span></span> 
    
4. <span data-ttu-id="a7631-159">Wählen Sie im mittleren Bereich Anwendungstypen **SharePoint-Add-in**.</span><span class="sxs-lookup"><span data-stu-id="a7631-159">From the application types in the central pane, choose **SharePoint Add-in**.</span></span> 
    
5. <span data-ttu-id="a7631-160">Geben Sie im unteren Bereich einen Namen und Speicherort für das Projekt, und einen Lösungsnamen.</span><span class="sxs-lookup"><span data-stu-id="a7631-160">In the bottom section, specify a name and location for the project, and a solution name.</span></span> 
    
6. <span data-ttu-id="a7631-161">Auch im unteren Bereich das Kontrollkästchen Sie **Projektmappenverzeichnis erstellen** .</span><span class="sxs-lookup"><span data-stu-id="a7631-161">Also in the bottom section, check the **Create directory for solution** box.</span></span> 
    
7. <span data-ttu-id="a7631-162">Klicken Sie auf **OK** , um das ursprüngliche Projekt zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="a7631-162">Click **OK** to create the initial project.</span></span> 
    
<span data-ttu-id="a7631-163">Visual Studio-Assistenten stellt ein paar weitere Fragen zur Project Online Einstellungen-Website (gewählte SharePoint-Einstellungen in den Dialogfeldern) in eine Reihe von Dialogfeldern, die folgen.</span><span class="sxs-lookup"><span data-stu-id="a7631-163">The Visual Studio Wizard asks a few follow-up questions about the Project Online settings site (called SharePoint settings in the dialogs) in a couple of dialogs that follow.</span></span> <span data-ttu-id="a7631-164">Es folgen die Fragen:</span><span class="sxs-lookup"><span data-stu-id="a7631-164">Here are the questions:</span></span>
  
1. <span data-ttu-id="a7631-165">Welche SharePoint-Website möchten Sie für das debugging Ihrer-add-in?</span><span class="sxs-lookup"><span data-stu-id="a7631-165">What SharePoint site do you want to use for debugging your add-in?</span></span> <span data-ttu-id="a7631-166">Geben Sie die URL der PWA-Website wie https://contoso.sharepoint.com/sites/pwa.</span><span class="sxs-lookup"><span data-stu-id="a7631-166">Specify the URL to your PWA site, such as https://contoso.sharepoint.com/sites/pwa.</span></span>
    
2. <span data-ttu-id="a7631-167">Wie möchten Sie Ihre SharePoint-Add-Ins hosten?</span><span class="sxs-lookup"><span data-stu-id="a7631-167">How do you want to host your SharePoint Add-in?</span></span> <span data-ttu-id="a7631-168">Wählen Sie [X] **SharePoint gehostet**.</span><span class="sxs-lookup"><span data-stu-id="a7631-168">Choose [X] **SharePoint-hosted**.</span></span>
    
   <span data-ttu-id="a7631-169">Weitere Informationen zu SharePoint-Add-ins einschließlich hosting-Optionen finden Sie unter [SharePoint-Add-ins](https://docs.microsoft.com/en-us/sharepoint/dev/sp-add-ins/sharepoint-add-ins).</span><span class="sxs-lookup"><span data-stu-id="a7631-169">For more information about SharePoint Add-ins, including hosting options, see [SharePoint Add-ins](https://docs.microsoft.com/en-us/sharepoint/dev/sp-add-ins/sharepoint-add-ins).</span></span>
    
3. <span data-ttu-id="a7631-170">Klicken Sie auf **Weiter**.</span><span class="sxs-lookup"><span data-stu-id="a7631-170">Click **Next**.</span></span> 
    
<span data-ttu-id="a7631-171">Das zweite zusätzliche Dialogfeld aufgefordert, geben Sie die SharePoint Online-Version für das Add-in:</span><span class="sxs-lookup"><span data-stu-id="a7631-171">The second additional dialog asks you to specify the SharePoint Online version for the add-in:</span></span> 
  
1. <span data-ttu-id="a7631-172">Was ist die erste Version von SharePoint, die Ihr Add-in zum Ziel soll?</span><span class="sxs-lookup"><span data-stu-id="a7631-172">What's the earliest version of SharePoint that you want your add-in to target?</span></span> <span data-ttu-id="a7631-173">Wählen Sie [X] S **HarePoint Online**.</span><span class="sxs-lookup"><span data-stu-id="a7631-173">Choose [X] S **harePoint-Online**.</span></span> 
    
2. <span data-ttu-id="a7631-174">Klicken Sie auf **Fertig stellen**.</span><span class="sxs-lookup"><span data-stu-id="a7631-174">Click **Finish**.</span></span> 
    
<span data-ttu-id="a7631-175">Visual Studio erstellt das Projekt und greift auf die Project Online-Website.</span><span class="sxs-lookup"><span data-stu-id="a7631-175">Visual Studio creates the project and accesses the Project Online site.</span></span> 
  
### <a name="enable-sideloading-on-the-project-online-site"></a><span data-ttu-id="a7631-176">Aktivieren Sie auf der Website Project Online sideloading</span><span class="sxs-lookup"><span data-stu-id="a7631-176">Enable sideloading on the Project Online site</span></span>

<span data-ttu-id="a7631-177">Sideloading ist der Mechanismus zum Testen und Debuggen Project Online-add-ins. Benötigen Sie zwei Skripts für Sideloading: eine Sideloading auf Ihre Project Online-Website und eine andere Sideloading zu deaktivieren, sobald Sie fertig sind, testen und Debuggen das Add-in zu aktivieren.</span><span class="sxs-lookup"><span data-stu-id="a7631-177">Sideloading is the mechanism for testing and debugging Project Online add-ins. You need two scripts for sideloading: one to enable sideloading on your Project Online site and another to disable sideloading once you finish testing and debugging the add-in.</span></span>
  
<span data-ttu-id="a7631-178">Weitere Informationen zum Einrichten von Sideloading finden Sie unter [app in Ihrer Websitesammlung Nichtentwickler SideLoading aktivieren](https://blogs.msdn.microsoft.com/officeapps/2013/12/10/enable-app-sideloading-in-your-non-developer-site-collection/).</span><span class="sxs-lookup"><span data-stu-id="a7631-178">For more information about setting up sideloading, see [Enable app SideLoading in your non-developer site collection](https://blogs.msdn.microsoft.com/officeapps/2013/12/10/enable-app-sideloading-in-your-non-developer-site-collection/).</span></span>
  
> [!NOTE]
> <span data-ttu-id="a7631-179">Sideloading apps ist ein Entwickler/Test-Feature.</span><span class="sxs-lookup"><span data-stu-id="a7631-179">Sideloading apps is a developer/test feature.</span></span> <span data-ttu-id="a7631-180">Es ist **nicht für die Verwendung in der Produktion vorgesehenen**.</span><span class="sxs-lookup"><span data-stu-id="a7631-180">It is **not intended for production use**.</span></span> <span data-ttu-id="a7631-181">Führen Sie nicht Sideload apps regelmäßig aus, oder behalten Sie app-Sideloading für mehr als Sie das Feature aktiv verwenden aktiviert.</span><span class="sxs-lookup"><span data-stu-id="a7631-181">Do not sideload apps regularly, or keep app sideloading enabled for longer than you are actively using the feature.</span></span> 
  
## <a name="add-content-to-the-add-in-project"></a><span data-ttu-id="a7631-182">Hinzufügen von Inhalt zum Projekt-Add-in</span><span class="sxs-lookup"><span data-stu-id="a7631-182">Add content to the add-in project</span></span>

<span data-ttu-id="a7631-183">Nach dem Erstellen eines Projekts und Einrichten des debugging-Mechanismus, umfasst Hinzufügen von Inhalt für die app die folgenden Aufgaben aus:</span><span class="sxs-lookup"><span data-stu-id="a7631-183">After creating a project and setting up the debugging mechanism, adding content to the app includes the following tasks:</span></span>
  
- <span data-ttu-id="a7631-184">Festlegen des Anwendungsbereichs</span><span class="sxs-lookup"><span data-stu-id="a7631-184">Setting the application scope</span></span>
    
- <span data-ttu-id="a7631-185">Verknüpfen der JSOM-Bibliothek</span><span class="sxs-lookup"><span data-stu-id="a7631-185">Linking the JSOM library</span></span>
    
- <span data-ttu-id="a7631-186">Hinzufügen von UI-Elemente für das Add-in</span><span class="sxs-lookup"><span data-stu-id="a7631-186">Adding UI Elements to the add-in</span></span>
    
- <span data-ttu-id="a7631-187">Initialisieren und beim Verbinden mit dem Project Online-Dienst</span><span class="sxs-lookup"><span data-stu-id="a7631-187">Initializing and connecting to the Project Online service</span></span>
    
- <span data-ttu-id="a7631-188">Abrufen von Projekten und Details-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="a7631-188">Retrieving projects and details/properties</span></span>
    
- <span data-ttu-id="a7631-189">Anzeigen von Projekten</span><span class="sxs-lookup"><span data-stu-id="a7631-189">Displaying projects</span></span>
    
- <span data-ttu-id="a7631-190">Anzeigen von Aufgaben für ein Projekt</span><span class="sxs-lookup"><span data-stu-id="a7631-190">Displaying tasks for a Project</span></span>
    
<span data-ttu-id="a7631-191">Das Add-In-Projekt umfasst viele Dateien.</span><span class="sxs-lookup"><span data-stu-id="a7631-191">The add-in project consists of many files.</span></span> <span data-ttu-id="a7631-192">In diesem Beispiel benötigen Sie die folgenden Dateien zu bearbeiten:</span><span class="sxs-lookup"><span data-stu-id="a7631-192">In this example, you'll need to edit the following files:</span></span> 
  
- <span data-ttu-id="a7631-193">AppManifest.xml</span><span class="sxs-lookup"><span data-stu-id="a7631-193">AppManifest.xml</span></span>
    
- <span data-ttu-id="a7631-194">"Default.aspx"</span><span class="sxs-lookup"><span data-stu-id="a7631-194">Default.aspx</span></span>
    
- <span data-ttu-id="a7631-195">App.js</span><span class="sxs-lookup"><span data-stu-id="a7631-195">App.js</span></span>
    
- <span data-ttu-id="a7631-196">"App.CSS" - optional; enthält Formatvorlagendefinitionen, die für das Add-in entwickelt</span><span class="sxs-lookup"><span data-stu-id="a7631-196">App.css - optional; contains style definitions developed for the add-in</span></span>
    
<span data-ttu-id="a7631-197">Wenn der Mandant Project Online ändert wie das Wechseln von einer Testversion zu einer Abonnement-Website können Sie die Projekteigenschaften, einschließlich der Server-Verbindung und die URL der Website aktualisieren, im Eigenschaftenfenster die **Ansicht**zur Verfügung > **Eigenschaften Fenster** Befehl.</span><span class="sxs-lookup"><span data-stu-id="a7631-197">If the Project Online tenant changes, such as moving from a trial to a subscription site, you can update the project properties, including the Server Connection and Site URL, using the Properties Window available through the **View** > **Properties Window** command.</span></span> 
  
<span data-ttu-id="a7631-198">Sie können auch Dateien zum Projekt hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="a7631-198">You can also add files to the project.</span></span> <span data-ttu-id="a7631-199">Ist dies der Fall ist, müssen Sie die Datei "Elements.xml" befindet sich in der gleichen Gruppe (Inhalt, Bilder, Seiten oder Skripts) umfassen die neuen Dateien zu aktualisieren.</span><span class="sxs-lookup"><span data-stu-id="a7631-199">If so, you'll need to update the Elements.xml file located in the same group (Content, Images, Pages, or Scripts) to include the new files.</span></span> <span data-ttu-id="a7631-200">Weitere Informationen zu den Projektdateien finden Sie unter [Untersuchen der app-manifest-Struktur und des Pakets über ein SharePoint-Add-in](https://docs.microsoft.com/en-us/sharepoint/dev/sp-add-ins/explore-the-app-manifest-structure-and-the-package-of-a-sharepoint-add-in).</span><span class="sxs-lookup"><span data-stu-id="a7631-200">For more information about the project files, see [Explore the app manifest structure and the package of a SharePoint Add-in](https://docs.microsoft.com/en-us/sharepoint/dev/sp-add-ins/explore-the-app-manifest-structure-and-the-package-of-a-sharepoint-add-in).</span></span>
  
### <a name="set-application-scope"></a><span data-ttu-id="a7631-201">Set-Anwendungsbereich</span><span class="sxs-lookup"><span data-stu-id="a7631-201">Set application scope</span></span>

<span data-ttu-id="a7631-202">Das Add-in benötigt Bereichs oder Berechtigung Ebenen definiert werden, bevor der Dienst Informationen in Abfrageergebnissen zurückgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="a7631-202">The add-in needs scope or permission levels defined before the service returns information in query results.</span></span> <span data-ttu-id="a7631-203">Verwenden Sie für dieses Add-in den folgenden Bereich für die Visual Studio-Projekt.</span><span class="sxs-lookup"><span data-stu-id="a7631-203">For this add-in, use the following scope to the Visual Studio project.</span></span> <span data-ttu-id="a7631-204">Diese Änderung wird auf der Registerkarte Berechtigungen die Datei AppManifest.XML vorgenommen:</span><span class="sxs-lookup"><span data-stu-id="a7631-204">This change is made to the AppManifest.xml file in the Permissions tab:</span></span>

|<span data-ttu-id="a7631-205">Umfang</span><span class="sxs-lookup"><span data-stu-id="a7631-205">Scope</span></span>|<span data-ttu-id="a7631-206">Berechtigung</span><span class="sxs-lookup"><span data-stu-id="a7631-206">Permission</span></span>|
|:-----|:-----|
|<span data-ttu-id="a7631-207">Mehrere Projekte (Projektserver)</span><span class="sxs-lookup"><span data-stu-id="a7631-207">Multiple Projects (Project Server)</span></span>  <br/> |<span data-ttu-id="a7631-208">Lesen</span><span class="sxs-lookup"><span data-stu-id="a7631-208">Read</span></span>  <br/> |
   
<span data-ttu-id="a7631-209">Speichern Sie die Datei nach dem Festlegen des Gültigkeitsbereichs der Anwendung.</span><span class="sxs-lookup"><span data-stu-id="a7631-209">Save the file after setting the application scope.</span></span> <span data-ttu-id="a7631-210">Andernfalls werden keine Daten aus dem Dienst zurückgegeben werden.</span><span class="sxs-lookup"><span data-stu-id="a7631-210">Otherwise, no data will be returned from the service.</span></span> 
  
### <a name="link-the-jsom-library"></a><span data-ttu-id="a7631-211">Verknüpfen der JSOM-Bibliothek</span><span class="sxs-lookup"><span data-stu-id="a7631-211">Link the JSOM library</span></span>

<span data-ttu-id="a7631-212">Die Laufzeit Project Online Bibliotheken, PS.js und PS.debug.js, werden von Project Online bereitgestellt und sind immer die aktuellste Version.</span><span class="sxs-lookup"><span data-stu-id="a7631-212">The runtime Project Online libraries, PS.js and PS.debug.js, are provided by Project Online and are always the most recent version.</span></span> <span data-ttu-id="a7631-213">JavaScript-add-ins, die JSOM verwenden, müssen mit einer dieser Bibliotheken verknüpfen.</span><span class="sxs-lookup"><span data-stu-id="a7631-213">JavaScript add-ins that use JSOM must link with one of these libraries.</span></span> <span data-ttu-id="a7631-214">Die Verknüpfung Definitionen sind in der Datei "default.aspx" hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="a7631-214">The linking definitions are added in the Default.aspx file.</span></span> <span data-ttu-id="a7631-215">Die Befehle, um die PS.js und/oder PS.debug.js zu verwenden sind Teil des Codes befindet sich in der Datei App.js.</span><span class="sxs-lookup"><span data-stu-id="a7631-215">The commands to use the PS.js and/or PS.debug.js are part of the code located in the App.js file.</span></span>
  
<span data-ttu-id="a7631-216">Fügen Sie den folgenden Befehl für die PS.js oder PS.debug.js in der `<asp:Content ContentPlaceHolderID="PlaceHolderAdditionalPageHead"` Element folgt "SharePoint:ScriptLink" für sp.js.</span><span class="sxs-lookup"><span data-stu-id="a7631-216">Add the following command for PS.js or PS.debug.js definition in the  `<asp:Content ContentPlaceHolderID="PlaceHolderAdditionalPageHead"` element following the "SharePoint:ScriptLink" for sp.js.</span></span> 
  
```js
<SharePoint:ScriptLink name="PS.js" runat="server" OnDemand="false" LoadAfterUI="true" Localizable="false" />
```

> [!NOTE]
> <span data-ttu-id="a7631-217">Das Attribut **OnDemand** für PS.js oder PS.debug.js festlegen auf **false festgelegt**.</span><span class="sxs-lookup"><span data-stu-id="a7631-217">The **OnDemand** attribute for PS.js or PS.debug.js set to **false**.</span></span> 
  
### <a name="add-ui-elements-to-the-add-in"></a><span data-ttu-id="a7631-218">Hinzufügen von UI-Elemente für das Add-in</span><span class="sxs-lookup"><span data-stu-id="a7631-218">Add UI elements to the add-in</span></span>

<span data-ttu-id="a7631-219">Das Beispiel-add-in umfasst einige Komponenten.</span><span class="sxs-lookup"><span data-stu-id="a7631-219">The example add-in consists of a few components.</span></span> <span data-ttu-id="a7631-220">Statische elementbeschreibungen befinden sich in der Datei Default.aspx.</span><span class="sxs-lookup"><span data-stu-id="a7631-220">Static element descriptions are located in the Default.aspx file.</span></span> <span data-ttu-id="a7631-221">Dynamische elementbeschreibungen und Code für alle Komponenten befinden sich in der Datei App.js.</span><span class="sxs-lookup"><span data-stu-id="a7631-221">Dynamic element descriptions and code for all components are located in the App.js file.</span></span> <span data-ttu-id="a7631-222">Kommentare zu den Komponenten finden Sie in der Quelle Codebeispiele.</span><span class="sxs-lookup"><span data-stu-id="a7631-222">For comments regarding the components, refer to the source code listings.</span></span> <span data-ttu-id="a7631-223">Es folgt eine Liste der Komponenten der Benutzeroberfläche in das Add-in:</span><span class="sxs-lookup"><span data-stu-id="a7631-223">Here is a list of the UI components in the add-in:</span></span>
  
- <span data-ttu-id="a7631-224">Titel</span><span class="sxs-lookup"><span data-stu-id="a7631-224">Title</span></span>
    
- <span data-ttu-id="a7631-225">Einführende Textpassagen</span><span class="sxs-lookup"><span data-stu-id="a7631-225">Introductory verbiage</span></span>
    
- <span data-ttu-id="a7631-226">Schaltfläche, um Aufgaben aus der Tabelle entfernen</span><span class="sxs-lookup"><span data-stu-id="a7631-226">Button to remove tasks from the table</span></span>
    
- <span data-ttu-id="a7631-227">Tabelle, die die Projekt-ID und Name und die Informationen zum Vorgang aufgeführt sind.</span><span class="sxs-lookup"><span data-stu-id="a7631-227">Table that lists the project ID and name, and the task information.</span></span>
    
- <span data-ttu-id="a7631-228">Aufgaben Schaltfläche (einmal für jedes Projekt geklont), die in der Tabelle Vorgangsdaten importiert.</span><span class="sxs-lookup"><span data-stu-id="a7631-228">Tasks Button (cloned once for each project) that imports task data into the table.</span></span>
    
<span data-ttu-id="a7631-229">Details der Benutzeroberfläche, wie den Titel und den Header Teil der Projekttabelle finden Sie die Datei "default.aspx" Projekt.</span><span class="sxs-lookup"><span data-stu-id="a7631-229">For details of the user interface, such as the title and the header portion of the project table, see the Default.aspx project file.</span></span>
  
### <a name="initialize-and-connect-to-the-host-system"></a><span data-ttu-id="a7631-230">Initialisieren und eine Verbindung mit dem Host-system</span><span class="sxs-lookup"><span data-stu-id="a7631-230">Initialize and connect to the host system</span></span>

<span data-ttu-id="a7631-231">Die Datei App.js enthält den JavaScript-Code.</span><span class="sxs-lookup"><span data-stu-id="a7631-231">The App.js file contains the JavaScript code.</span></span> <span data-ttu-id="a7631-232">Das Add-In lädt PS.js im Browser und ruft dann die Funktion InitializePage.</span><span class="sxs-lookup"><span data-stu-id="a7631-232">The add-in loads PS.js in the browser, and then calls the initializePage function.</span></span> <span data-ttu-id="a7631-233">InitializePage Ruft einen Kontext an den Endpunkt Project Online und startet die LoadProjects-Funktion.</span><span class="sxs-lookup"><span data-stu-id="a7631-233">InitializePage retrieves a context to the Project Online endpoint and starts the loadProjects function.</span></span>
  
```js
    'use strict';
    SP.SOD.executeOrDelayUntilScriptLoaded(initializePage, "PS.js");
    //Project PWA Context and published projects in PWA
    var projContext;
    var projects;
    function initializePage() {
        //Get the Project context for this web
        projContext = PS.ProjectContext.get_current();
        loadProjects();
    }
    //General CSOM failure event handler
    //Invoked when ExecuteQueryAsync returns unsuccessfully
    function onRequestFailed(sender, args) {
        alert("Failed to execute: " + args.get_message());
        return;
    };

```

### <a name="retrieve-the-projects"></a><span data-ttu-id="a7631-234">Abrufen der Projekte</span><span class="sxs-lookup"><span data-stu-id="a7631-234">Retrieve the projects</span></span>

<span data-ttu-id="a7631-235">Die Funktion LoadProjects fragt den Dienst für den Projektnamen und IDs.</span><span class="sxs-lookup"><span data-stu-id="a7631-235">The loadProjects function queries the service for the project names and IDs.</span></span> 
  
<span data-ttu-id="a7631-236">Die Anwendung ruft den Projektnamen und die Project-Id. Weitere Informationen über das Projekt ist verfügbar und durch Ändern der Load-Methode, um die Eigenschaften zum Abrufen explizit ermitteln zugegriffen werden kann.</span><span class="sxs-lookup"><span data-stu-id="a7631-236">The application retrieves the project name and project Id. Other information about the project is available and can be accessed by modifying the load method to identify explicitly the properties to retrieve.</span></span> <span data-ttu-id="a7631-237">Ein Beispiel wird im Code als Kommentar bereitgestellt.</span><span class="sxs-lookup"><span data-stu-id="a7631-237">An example is provided in the code as a comment.</span></span> 
  
<span data-ttu-id="a7631-238">Wenn die Abfrage erfolgreich ist, wird das Add-in durch Aufrufen von DisplayProjects fortgesetzt.</span><span class="sxs-lookup"><span data-stu-id="a7631-238">If the query succeeds, the add-in continues by calling displayProjects.</span></span> 
  
```js
    //Query CSOM and get the list of projects in PWA
    function loadProjects() {
        projects = projContext.get_projects();
    //Request to server - identifies what to retrieve
        projContext.load(projects, 'Include(Name, Id)');
        //Notice to server to execute query
        projContext.executeQueryAsync(displayProjects, onRequestFailed);
        // Syntax for requesting more fields to pull down from server
        // projContext.load(projects, 'Include(Name, Description, StartDate, 
        // Id, IsCheckedOut)');
    }

```

### <a name="display-the-projects"></a><span data-ttu-id="a7631-239">Anzeigen der Projekte</span><span class="sxs-lookup"><span data-stu-id="a7631-239">Display the projects</span></span>

<span data-ttu-id="a7631-240">Die Funktion DisplayProjects erstellt eine Tabelle, eine Zeile pro Projekt und eine Schaltfläche, um die Vorgänge für bestimmte Projekte angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="a7631-240">The displayProjects function creates a table, one row per project, and a button to show the tasks for the specific project.</span></span> 
  
```js
    //Display the projects with names and ids in a table
    function displayProjects() {
        //Current published project and ID
        var p, projId;
        //Project table rows to publish collectively
        var pTable = []; 
        var pEnum = projects.getEnumerator();
        //Build a 3-column table, with one project per row.
        while (pEnum.moveNext()) {
            p = pEnum.get_current();
        
            //Items used in getting information for table rows:
            //Current published project object, and ID and name
            // var project = p;
            // var projId = p.get_id();
            // var projName = p.get_name();
        
            //Continue processing/working with project object as needed.
        }
    }

```

> [!NOTE]
> <span data-ttu-id="a7631-241">Die While-Schleife greift auf die ID und Name-Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="a7631-241">The while loop accesses the ID and name properties.</span></span> <span data-ttu-id="a7631-242">Dies ist geringfügig Quellcodeprojekt an, das eine Funktion aufruft, die wiederum die gleichen Eigenschaften zugreift.</span><span class="sxs-lookup"><span data-stu-id="a7631-242">This is slightly different than the source code project that calls a function that, in turn, accesses the same properties.</span></span> 
  
### <a name="display-the-tasks-for-a-project"></a><span data-ttu-id="a7631-243">Die Aufgaben für ein Projekt anzeigen</span><span class="sxs-lookup"><span data-stu-id="a7631-243">Display the tasks for a project</span></span>

<span data-ttu-id="a7631-244">Die Aufgaben beim Teil des Add-Ins, sind nicht Teil der anfänglichen laden.</span><span class="sxs-lookup"><span data-stu-id="a7631-244">The tasks, while part of the add-in, are not part of the initial loading.</span></span> <span data-ttu-id="a7631-245">Wenn der Benutzer die Aufgaben im Zusammenhang mit einem Projekt interessiert ist, wird durch Klicken auf die Schaltfläche "Aufgaben anzeigen" die Aufgaben in der Liste mit dem BtnLoadTasks-Ereignishandler anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="a7631-245">If the user is interested in the tasks associated with a project, clicking the "Show Tasks" button causes the tasks to display in the list using the btnLoadTasks event handler.</span></span> 
  
<span data-ttu-id="a7631-246">Im BtnLoadTasks-Ereignishandler mit der entsprechenden Project-ID, fordert die Aufgaben für das angegebene Projekt vom Server.</span><span class="sxs-lookup"><span data-stu-id="a7631-246">The btnLoadTasks event handler, with the appropriate project ID, requests the tasks for the specified project from the server.</span></span> <span data-ttu-id="a7631-247">Nachdem abgerufen, übergibt BtnLoadTasks die Aufgabenliste an DisplayTasks, die auf dem Bildschirm Aufgaben durchzuführen.</span><span class="sxs-lookup"><span data-stu-id="a7631-247">Once retrieved, btnLoadTasks passes the task list to displayTasks to present the tasks onscreen.</span></span>
  
```js
    //Query CSOM and get the list of tasks for a specific project
    function btnLoadTasks(pid) {
        //Event handler for the "Show tasks" buttons. 
        //
        //The project ID is the sole argument and is used to get the appropriate task 
        //info from the service.
        //The project ID is also the button name, and is used to identify where to place
        //the task information in the table.
        //
        //Project ID to pass to the event handler
        var projId = pid;
        //
        //Get the project reference
        var pProj = projects.getById(projId);
        //
        //Get the tasks collection reference associated with the project.
        var tasks = pProj.get_tasks();
        //
        projContext.load(tasks, 'Include(Id, Name, Start, ScheduledStart, Completion)');
        //
        //If the query succeeds, displayTasks presents the tasks to the user.
        projContext.executeQueryAsync(function () { displayTasks(tasks, projId) }, onRequestFailed);
    }

```

<span data-ttu-id="a7631-248">Die Funktion DisplayTasks zeigt Aufgaben im Zusammenhang mit ein angegebenes Projekt unmittelbar unterhalb des Eintrags Projekt.</span><span class="sxs-lookup"><span data-stu-id="a7631-248">The displayTasks function displays the tasks associated with a specified project immediately beneath the project entry.</span></span>
  
```js
    //Insert tasks for the specified project immediately underneath the project entry 
    //in the table.
    function displayTasks(tasks, projId) {
        //selected project ID
        var pId = projId;
        //individual task
        var t;
        //Task table rows to publish collectively
        var tTable = [];
        var tEnum = tasks.getEnumerator();
        //Build table one task per row.
        while (tEnum.moveNext()) {
            t = tEnum.get_current();
            //
            //Items used in getting information for table rows:
            //Current task object, and ID and name
            // var task = t;
            // var taskId = t.get_id();
            // var taskName = t.get_name();
            
            //Continue processing/working with task object as needed.
        }
    }

```

> [!NOTE]
> <span data-ttu-id="a7631-249">Die While-Schleife greift auf die Vorgangs-ID und Name-Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="a7631-249">The while loop accesses the task ID and name properties.</span></span> <span data-ttu-id="a7631-250">Dies ist geringfügig Quellcodeprojekt an, das eine Funktion aufruft, die wiederum die gleichen Eigenschaften zugreift.</span><span class="sxs-lookup"><span data-stu-id="a7631-250">This is slightly different than the source code project that calls a function that, in turn, accesses the same properties.</span></span> 
  
<span data-ttu-id="a7631-251">Beispielausgabe für die Aufgaben eines einzelnen Projekts folgt.</span><span class="sxs-lookup"><span data-stu-id="a7631-251">Sample output for the tasks of a single project follows.</span></span>
  
<span data-ttu-id="a7631-252">![Screenshot zeigt die Ausgabe für eine Projektaufgabe] (media/f6500a3f-000b-4f3e-9be6-9a74d0bea15e.png "Screenshot zeigt die Ausgabe für eine Projektaufgabe")</span><span class="sxs-lookup"><span data-stu-id="a7631-252">![Screen shot showing the output for a project task](media/f6500a3f-000b-4f3e-9be6-9a74d0bea15e.png "Screen shot showing the output for a project task")</span></span>
  
## <a name="see-also"></a><span data-ttu-id="a7631-253">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="a7631-253">See also</span></span>

<span data-ttu-id="a7631-254">Dokumentation und Beispiele im Zusammenhang mit Project Online und die Anwendungsentwicklung mithilfe von CSOM finden Sie im [Projekt Development Portal](https://developer.microsoft.com/en-us/project).</span><span class="sxs-lookup"><span data-stu-id="a7631-254">For documentation and samples related to Project Online and application development using CSOM, see the [Project Development Portal](https://developer.microsoft.com/en-us/project).</span></span>
    


