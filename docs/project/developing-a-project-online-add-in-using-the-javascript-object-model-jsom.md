---
title: Entwickeln eines Project Online-Add-Ins mithilfe des JavaScript-Objektmodells (JSOM)
manager: soliver
ms.date: 11/08/2016
ms.audience: Developer
localization_priority: Normal
ms.assetid: 4a4b1ad2-de46-421d-a698-53c20c90b93a
description: In diesem Artikel wird die Microsoft Project Online-Add-in-Entwicklung beschrieben, um Ihre Erfahrung mit Project online zu verbessern. Das Entwicklungsprojekt wird als Exemplarische Vorgehensweise implementiert. Das Add-in, das für diesen Artikel verwendet wird, liest und zeigt die Projektnamen und-IDs der veröffentlichten Projekte aus Ihrem Project Online-Konto an und ermöglicht Ihnen das Abrufen von Aufgaben, die einzelnen Projekten zugeordnet sind.
ms.openlocfilehash: 0a472a6300f18aaa65649f44d944445642a59e1a
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32322688"
---
# <a name="developing-a-project-online-add-in-using-the-javascript-object-model-jsom"></a><span data-ttu-id="621c3-105">Entwickeln eines Project Online-Add-Ins mithilfe des JavaScript-Objektmodells (JSOM)</span><span class="sxs-lookup"><span data-stu-id="621c3-105">Developing a Project Online add-in using the JavaScript Object Model (JSOM)</span></span>

<span data-ttu-id="621c3-106">In diesem Artikel wird die Microsoft Project Online-Add-in-Entwicklung beschrieben, um Ihre Erfahrung mit dem Projekt online zu verbessern.</span><span class="sxs-lookup"><span data-stu-id="621c3-106">This article describes Microsoft Project Online Add-in development to enhance your experience with the Project Online.</span></span> <span data-ttu-id="621c3-107">Das Entwicklungsprojekt wird als Exemplarische Vorgehensweise implementiert.</span><span class="sxs-lookup"><span data-stu-id="621c3-107">The development project is implemented as a walkthrough.</span></span> <span data-ttu-id="621c3-108">Das Add-in, das für diesen Artikel verwendet wird, liest und zeigt die Projektnamen und-IDs der veröffentlichten Projekte aus Ihrem Project Online-Konto an und ermöglicht Ihnen das Abrufen von Aufgaben, die einzelnen Projekten zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="621c3-108">The add-in used for this article reads and displays the project names and IDs of the published projects from your Project Online account and allows you to drill down to retrieve tasks associated with individual projects.</span></span>
  
<span data-ttu-id="621c3-109">Zur Laufzeit sieht das Add-in-Listing ähnlich wie in der folgenden Abbildung aus:</span><span class="sxs-lookup"><span data-stu-id="621c3-109">At run time, the add-in listing looks similar to the following illustration:</span></span>
  
<span data-ttu-id="621c3-110">![Screenshot mit einer Liste von JSOM-Projekten und-Aufgaben] (media/766e5914-f048-48f4-9282-291f55e6e90d.png "Screenshot mit einer Liste von JSOM-Projekten und-Aufgaben")</span><span class="sxs-lookup"><span data-stu-id="621c3-110">![Screen shot showing a listing of JSOM projects and tasks](media/766e5914-f048-48f4-9282-291f55e6e90d.png "Screen shot showing a listing of JSOM projects and tasks")</span></span>
  
<span data-ttu-id="621c3-111">Der Schwerpunkt des Beispiels ist die Interaktion mit dem Projekt online, das Abfragen und Festlegen des Kontexts für jede Anforderung vom Dienst.</span><span class="sxs-lookup"><span data-stu-id="621c3-111">The focus of the example is the interaction with the Project Online, making queries and setting the context for each request from the service.</span></span> <span data-ttu-id="621c3-112">Benutzeroberflächenelemente (UI) erhalten nur minimale Aufmerksamkeit.</span><span class="sxs-lookup"><span data-stu-id="621c3-112">User interface (UI) elements receive minimal attention.</span></span> <span data-ttu-id="621c3-113">Stattdessen enthalten die Quellauflistungen Kommentare zur Benutzeroberfläche.</span><span class="sxs-lookup"><span data-stu-id="621c3-113">Instead, the source listings provide comments regarding the UI.</span></span>
  
> [!NOTE]
> <span data-ttu-id="621c3-114">Die Quelldateien für das Beispiel-Add-in, ein Visual Studio-Projekt, sind verfügbar https://github.com/OfficeDev/Project-JSOM-List-Projects-Tasks....unter:.</span><span class="sxs-lookup"><span data-stu-id="621c3-114">The source files for the example add-in, a Visual Studio project, are available at: https://github.com/OfficeDev/Project-JSOM-List-Projects-Tasks.....</span></span> <span data-ttu-id="621c3-115">Halten Sie die Quelldateien als Referenz bereit, während Sie den Artikel lesen, da jeder die andere ergänzt.</span><span class="sxs-lookup"><span data-stu-id="621c3-115">Keep the source files handy as a reference while you read the article, as each complements the other.</span></span> <span data-ttu-id="621c3-116">Die Dateien in der Visual Studio-Projekt erstellen und sind mit minimalen Änderungen ausführbar-ersetzen die URL für Ihren Project Online-Mandanten in den Ordner PWA.</span><span class="sxs-lookup"><span data-stu-id="621c3-116">The files in the Visual Studio project build and are executable with minimal changes—substituting the URL for your Project Online tenant down to the PWA folder.</span></span> 
  
## <a name="background"></a><span data-ttu-id="621c3-117">Hintergrund</span><span class="sxs-lookup"><span data-stu-id="621c3-117">Background</span></span>

<span data-ttu-id="621c3-118">Project Online ist ein Office 365-Dienst, der Unternehmen eine Projektportfolio Verwaltung (PPM) und Projektmanagement Office (PMO) bietet, um Portfolios, Programme und Projekte zu koordinieren und zu verwalten.</span><span class="sxs-lookup"><span data-stu-id="621c3-118">Project Online is a Office 365 service that provides companies with a project portfolio management (PPM) and project management office (PMO) solution to coordinate and manage portfolios, programs, and projects.</span></span> <span data-ttu-id="621c3-119">Project Online ist ein anderes Angebot als die Project Desktop-Editionen; Project Online enthält jedoch weiterhin die Funktionalität, um Projektdetails während der gesamten Lebensdauer eines Projekts zu verwalten und nachzuverfolgen.</span><span class="sxs-lookup"><span data-stu-id="621c3-119">Project Online is a different offering than the Project desktop editions; yet, Project Online still contains the functionality to maintain and track project details throughout the life of a project.</span></span> <span data-ttu-id="621c3-120">Project Online basiert auf SharePoint Online.</span><span class="sxs-lookup"><span data-stu-id="621c3-120">Project Online is built on SharePoint Online.</span></span>
  
<span data-ttu-id="621c3-121">Ein gehostetes Project Online-Add-in besteht aus JavaScript-und Ressourcendateien, die mit der Client seitigen Objektmodell-API interagieren.</span><span class="sxs-lookup"><span data-stu-id="621c3-121">A Project Online hosted add-in consists of JavaScript and resource files that interact with the Client-Side-Object-Model API.</span></span> <span data-ttu-id="621c3-122">Wenn der Benutzer das Add-in besucht, werden JavaScript und Ressourcen im Browser heruntergeladen und ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="621c3-122">When the user visits the add-in, the JavaScript and resources are downloaded and executed within the browser.</span></span> <span data-ttu-id="621c3-123">Das Add-in führt asynchrone Aufrufe von Project Online aus, um mit dem Dienst zu interagieren, sei es das Erstellen, abrufen, aktualisieren oder Löschen von Daten.</span><span class="sxs-lookup"><span data-stu-id="621c3-123">The add-In makes asynchronous calls to Project Online to interact with the service, whether creating, retrieving, updating, or deleting data.</span></span> 
  
<span data-ttu-id="621c3-124">Project Online führt eine weitere Aktion aus, um Informationen zu schützen, die anderen Mandanten des Add-ins gehören. in Project Online wird nämlich eine isolierte Website erstellt, die mit den Anforderungen des Add-ins interagiert.</span><span class="sxs-lookup"><span data-stu-id="621c3-124">Project Online performs one more action to protect information that belongs to other tenants from the add-in; namely, Project Online creates an isolated site to interact with the requests from the add-in.</span></span> <span data-ttu-id="621c3-125">Auf dem Project Online-Host wird kein benutzerdefinierter Code ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="621c3-125">No custom code runs on the Project Online host.</span></span> 
  
<span data-ttu-id="621c3-126">Das Entwicklungs Setup für Project Online-Add-Ins verwendet den Projekttyp Visual Studio SharePoint-Add-in.</span><span class="sxs-lookup"><span data-stu-id="621c3-126">The development setup for Project Online add-ins uses the Visual Studio SharePoint Add-in project type.</span></span> <span data-ttu-id="621c3-127">Das Add-in ist in JavaScript geschrieben und verwendet das Project-JavaScript-Objektmodell (JSOM) für die Interaktion mit dem Project Online-Dienst.</span><span class="sxs-lookup"><span data-stu-id="621c3-127">The add-in is written in JavaScript, and uses the Project JavaScript object model (JSOM) to interact with the Project Online service.</span></span> <span data-ttu-id="621c3-128">Der JSOM erbt einen Großteil seiner Funktionalität von der SharePoint-JSOM.</span><span class="sxs-lookup"><span data-stu-id="621c3-128">The JSOM inherits much of its functionality from the SharePoint JSOM.</span></span>
  
> [!NOTE]
> <span data-ttu-id="621c3-129">Add-Ins können im Office Store veröffentlicht und verkauft oder in einem privaten App-Katalog auf SharePoint bereitgestellt werden.</span><span class="sxs-lookup"><span data-stu-id="621c3-129">Add-ins can be published and sold in the Office Store or deployed to a private app catalog on SharePoint.</span></span> <span data-ttu-id="621c3-130">Weitere Informationen finden Sie unter [bereitstellen und Veröffentlichen Ihres Office-Add-ins](https://docs.microsoft.com/office/dev/add-ins/publish/publish).</span><span class="sxs-lookup"><span data-stu-id="621c3-130">For more information, see [Deploy and publish your Office Add-in](https://docs.microsoft.com/office/dev/add-ins/publish/publish).</span></span>
> 
> <span data-ttu-id="621c3-131">Das in diesem Artikel verwendete Add-in ist ein Beispiel für Entwickler; Es ist nicht für die Verwendung in einer Produktionsumgebung vorgesehen.</span><span class="sxs-lookup"><span data-stu-id="621c3-131">The add-in used in this article is a sample for developers; it is not intended for use in a production environment.</span></span> <span data-ttu-id="621c3-132">Der Hauptzweck besteht darin, ein Beispiel für die APP-Entwicklung für Project online zu zeigen.</span><span class="sxs-lookup"><span data-stu-id="621c3-132">The primary purpose is to show an example of app development for Project Online.</span></span> 
  
## <a name="prerequisites"></a><span data-ttu-id="621c3-133">Voraussetzungen</span><span class="sxs-lookup"><span data-stu-id="621c3-133">Prerequisites</span></span>

<span data-ttu-id="621c3-134">Fügen Sie der unterstützten Windows-Umgebung die folgenden Elemente hinzu:</span><span class="sxs-lookup"><span data-stu-id="621c3-134">Add the following items to a supported Windows environment:</span></span>
  
- <span data-ttu-id="621c3-135">**.NET framework 4,0 oder höher**: vollständige Versionen des Frameworks ab Version 4,0 sind kompatibel.</span><span class="sxs-lookup"><span data-stu-id="621c3-135">**.NET Framework 4.0 or later**: Complete versions of the framework from version 4.0 are compatible.</span></span> <span data-ttu-id="621c3-136">Die Download-Website ist https://msdn.microsoft.com/vstudio/aa496123.aspx.</span><span class="sxs-lookup"><span data-stu-id="621c3-136">The download site is https://msdn.microsoft.com/vstudio/aa496123.aspx.</span></span>
    
- <span data-ttu-id="621c3-137">**Visual Studio 2013 oder höher**:</span><span class="sxs-lookup"><span data-stu-id="621c3-137">**Visual Studio 2013 or later**:</span></span>  
    
   - <span data-ttu-id="621c3-138">Die Professional Edition von Visual Studio 2015 ist Soforteinsatz bereit und ist verfügbar unter https://www.visualstudio.com/en-us/products/visual-studio-professional-with-msdn-vs.aspx.</span><span class="sxs-lookup"><span data-stu-id="621c3-138">The professional edition of Visual Studio 2015 is ready to go out-of-the box and is available at https://www.visualstudio.com/en-us/products/visual-studio-professional-with-msdn-vs.aspx.</span></span>
    
   - <span data-ttu-id="621c3-139">Die Community-Edition von Visual Studio 2015 ist verfügbar https://www.visualstudio.com/en-us/products/visual-studio-community-vs.aspxunter.</span><span class="sxs-lookup"><span data-stu-id="621c3-139">The community edition of Visual Studio 2015 is available at https://www.visualstudio.com/en-us/products/visual-studio-community-vs.aspx.</span></span> <span data-ttu-id="621c3-140">Diese Edition erfordert die manuelle Installation der Microsoft Office Developer Tools für Visual Studio.</span><span class="sxs-lookup"><span data-stu-id="621c3-140">This edition requires manual installation of the Microsoft Office Developer Tools for Visual Studio.</span></span>
    
   <span data-ttu-id="621c3-141">Die Microsoft Office Developer Tools für Visual Studio sind verfügbar unter https://www.visualstudio.com/en-us/features/office-tools-vs.aspx.</span><span class="sxs-lookup"><span data-stu-id="621c3-141">The Microsoft Office Developer Tools for Visual Studio are available at https://www.visualstudio.com/en-us/features/office-tools-vs.aspx.</span></span>
    
- <span data-ttu-id="621c3-142">**Ein Project Online-Konto**: Dadurch wird der Zugriff auf den Hostdienst ermöglicht.</span><span class="sxs-lookup"><span data-stu-id="621c3-142">**A Project Online account**: This provides access to the hosting service.</span></span> <span data-ttu-id="621c3-143">Weitere Informationen zum Einrichten eines Project Online-Kontos finden Sie unter https://products.office.com/en-us/Project/project-online-portfolio-management.</span><span class="sxs-lookup"><span data-stu-id="621c3-143">For more information about obtaining a Project Online account, see https://products.office.com/en-us/Project/project-online-portfolio-management.</span></span>
    
   <span data-ttu-id="621c3-144">Stellen Sie sicher, dass der Add-in-Benutzer über ausreichende Autorisierung für den Zugriff auf einige Projekte im Project Online-Mandanten verfügt.</span><span class="sxs-lookup"><span data-stu-id="621c3-144">Ensure that the add-in user has sufficient authorization to access some projects in the Project Online tenant.</span></span> 
    
- <span data-ttu-id="621c3-145">**Projekte auf der Hostwebsite** , die mit Informationen aufgefüllt werden.</span><span class="sxs-lookup"><span data-stu-id="621c3-145">**Projects on the hosting site** that are populated with information.</span></span>
    
> [!NOTE]
> <span data-ttu-id="621c3-146">Das standardmäßige .NET Framework ist das richtige Framework für die Verwendung.</span><span class="sxs-lookup"><span data-stu-id="621c3-146">The standard .NET Framework is the correct framework to use.</span></span> <span data-ttu-id="621c3-147">Verwenden Sie nicht das ".NET Framework 4-Client Profil".</span><span class="sxs-lookup"><span data-stu-id="621c3-147">Do not use the ".NET Framework 4 Client Profile".</span></span> 
  
### <a name="set-up-the-visual-studio-project"></a><span data-ttu-id="621c3-148">Einrichten des Visual Studio-Projekts</span><span class="sxs-lookup"><span data-stu-id="621c3-148">Set up the Visual Studio project</span></span>

<span data-ttu-id="621c3-149">Das Anwendungssetup umfasst das Erstellen eines neuen Projekts, das Verknüpfen der entsprechenden Bibliotheken und das Deklarieren der benötigten Namespaces.</span><span class="sxs-lookup"><span data-stu-id="621c3-149">The application setup consists of creating a new project, linking the appropriate libraries and declaring the needed namespaces.</span></span> <span data-ttu-id="621c3-150">Visual Studio bietet verschiedene Typen von Entwicklungsprojekten.</span><span class="sxs-lookup"><span data-stu-id="621c3-150">Visual Studio presents several types of development projects.</span></span> <span data-ttu-id="621c3-151">Der Abschnitt ist kurz und sehr einfach.</span><span class="sxs-lookup"><span data-stu-id="621c3-151">The section is brief and very basic.</span></span> <span data-ttu-id="621c3-152">Der Wert besteht darin, dass die Informationen an einem Ort verschmolzen werden.</span><span class="sxs-lookup"><span data-stu-id="621c3-152">The value is having the information is coalesced in one place.</span></span>
  
#### <a name="select-a-visual-studio-project"></a><span data-ttu-id="621c3-153">Auswählen eines Visual Studio-Projekts</span><span class="sxs-lookup"><span data-stu-id="621c3-153">Select a Visual Studio project</span></span>

<span data-ttu-id="621c3-154">Führen Sie die folgenden Schritte aus, um ein Projekt vom geeigneten Typ für das Add-in zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="621c3-154">To create a project of the appropriate type for the add-in, you must do the following steps.</span></span> <span data-ttu-id="621c3-155">Auf dem Bildschirm aufgetretene Schlüsselwörter weisen ein **Bold** -Attribut auf:</span><span class="sxs-lookup"><span data-stu-id="621c3-155">Keywords encountered on the screen have a **bold** attribute:</span></span> 
  
1. <span data-ttu-id="621c3-156">Wählen Sie im Menü Datei die Option **Datei** > **Neues** > **Projekt**aus.</span><span class="sxs-lookup"><span data-stu-id="621c3-156">From the File menu, choose **File** > **New** > **Project**.</span></span> 
    
2. <span data-ttu-id="621c3-157">Wählen Sie im linken Bereich unter installierte Vorlagen die Option **C#** > -**Office/SharePoint** > -**Web-Add-ins**aus.</span><span class="sxs-lookup"><span data-stu-id="621c3-157">From the Installed templates in the left pane, select **C#** > **Office/SharePoint** > **Web Add-ins**.</span></span> 
    
3. <span data-ttu-id="621c3-158">Wählen Sie oben im zentralen Bereich **.NET Framework 4** oder höher aus. die aktuelle Version ist 4,6.</span><span class="sxs-lookup"><span data-stu-id="621c3-158">At the top of the central pane, select **.NET Framework 4** or later; the current version is 4.6.</span></span> 
    
4. <span data-ttu-id="621c3-159">Wählen Sie in den Anwendungstypen im zentralen Bereich **SharePoint-Add-in**aus.</span><span class="sxs-lookup"><span data-stu-id="621c3-159">From the application types in the central pane, choose **SharePoint Add-in**.</span></span> 
    
5. <span data-ttu-id="621c3-160">Geben Sie im unteren Abschnitt einen Namen und Speicherort für das Projekt und einen Projektmappennamen an.</span><span class="sxs-lookup"><span data-stu-id="621c3-160">In the bottom section, specify a name and location for the project, and a solution name.</span></span> 
    
6. <span data-ttu-id="621c3-161">Aktivieren Sie außerdem im unteren Abschnitt das Kontrollkästchen **Projektmappenverzeichnis erstellen**.</span><span class="sxs-lookup"><span data-stu-id="621c3-161">Also in the bottom section, check the **Create directory for solution** box.</span></span> 
    
7. <span data-ttu-id="621c3-162">Klicken Sie auf **OK**, um das Ausgangsprojekt zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="621c3-162">Click **OK** to create the initial project.</span></span> 
    
<span data-ttu-id="621c3-163">Der Visual Studio-Assistent stellt in einigen folgenden Dialogfeldern einige weitere Fragen zur Project Online-einstellungswebsite (die als SharePoint-Einstellungen in den Dialogfeldern bezeichnet werden) bereit.</span><span class="sxs-lookup"><span data-stu-id="621c3-163">The Visual Studio Wizard asks a few follow-up questions about the Project Online settings site (called SharePoint settings in the dialogs) in a couple of dialogs that follow.</span></span> <span data-ttu-id="621c3-164">Hier sind die Fragen:</span><span class="sxs-lookup"><span data-stu-id="621c3-164">Here are the questions:</span></span>
  
1. <span data-ttu-id="621c3-165">Welche SharePoint-Website soll für das Debuggen des Add-Ins verwendet werden?</span><span class="sxs-lookup"><span data-stu-id="621c3-165">What SharePoint site do you want to use for debugging your add-in?</span></span> <span data-ttu-id="621c3-166">Geben Sie die URL ihrer PWA-Website an, https://contoso.sharepoint.com/sites/pwabeispielsweise.</span><span class="sxs-lookup"><span data-stu-id="621c3-166">Specify the URL to your PWA site, such as https://contoso.sharepoint.com/sites/pwa.</span></span>
    
2. <span data-ttu-id="621c3-167">Wie soll Ihr SharePoint-Add-in gehostet werden?</span><span class="sxs-lookup"><span data-stu-id="621c3-167">How do you want to host your SharePoint Add-in?</span></span> <span data-ttu-id="621c3-168">Wählen Sie [X] von **SharePoint gehostet**.</span><span class="sxs-lookup"><span data-stu-id="621c3-168">Choose [X] **SharePoint-hosted**.</span></span>
    
   <span data-ttu-id="621c3-169">Weitere Informationen zu SharePoint-Add-Ins, einschließlich Hosting-Optionen, finden Sie unter [SharePoint-Add-ins](https://docs.microsoft.com/sharepoint/dev/sp-add-ins/sharepoint-add-ins).</span><span class="sxs-lookup"><span data-stu-id="621c3-169">For more information about SharePoint Add-ins, including hosting options, see [SharePoint Add-ins](https://docs.microsoft.com/sharepoint/dev/sp-add-ins/sharepoint-add-ins).</span></span>
    
3. <span data-ttu-id="621c3-170">Klicken Sie auf **Weiter**.</span><span class="sxs-lookup"><span data-stu-id="621c3-170">Click **Next**.</span></span> 
    
<span data-ttu-id="621c3-171">Im zweiten zusätzlichen Dialogfeld werden Sie aufgefordert, die SharePoint Online-Version für das Add-in anzugeben:</span><span class="sxs-lookup"><span data-stu-id="621c3-171">The second additional dialog asks you to specify the SharePoint Online version for the add-in:</span></span> 
  
1. <span data-ttu-id="621c3-172">Was ist die früheste Version von SharePoint, die das Add-in als Ziel haben soll?</span><span class="sxs-lookup"><span data-stu-id="621c3-172">What's the earliest version of SharePoint that you want your add-in to target?</span></span> <span data-ttu-id="621c3-173">Wählen Sie [X] S **harePoint-Online**aus.</span><span class="sxs-lookup"><span data-stu-id="621c3-173">Choose [X] S **harePoint-Online**.</span></span> 
    
2. <span data-ttu-id="621c3-174">Klicken Sie auf **Fertig stellen**.</span><span class="sxs-lookup"><span data-stu-id="621c3-174">Click **Finish**.</span></span> 
    
<span data-ttu-id="621c3-175">Visual Studio erstellt das Projekt und greift auf die Project Online-Website zu.</span><span class="sxs-lookup"><span data-stu-id="621c3-175">Visual Studio creates the project and accesses the Project Online site.</span></span> 
  
### <a name="enable-sideloading-on-the-project-online-site"></a><span data-ttu-id="621c3-176">Aktivieren von querladen auf der Project Online-Website</span><span class="sxs-lookup"><span data-stu-id="621c3-176">Enable sideloading on the Project Online site</span></span>

<span data-ttu-id="621c3-177">Querladen ist der Mechanismus zum Testen und Debuggen von Project Online-Add-Ins. Sie benötigen zwei Skripts für querladen: eine, um querladen auf Ihrer Project Online-Website zu aktivieren, und eine andere, um querladen zu deaktivieren, nachdem Sie das Testen und Debuggen des Add-Ins abgeschlossen haben.</span><span class="sxs-lookup"><span data-stu-id="621c3-177">Sideloading is the mechanism for testing and debugging Project Online add-ins. You need two scripts for sideloading: one to enable sideloading on your Project Online site and another to disable sideloading once you finish testing and debugging the add-in.</span></span>
  
<span data-ttu-id="621c3-178">Weitere Informationen zum Einrichten von querladen finden Sie unter [enable App querladen in your Non-Developer Site Collection](https://blogs.msdn.microsoft.com/officeapps/2013/12/10/enable-app-sideloading-in-your-non-developer-site-collection/).</span><span class="sxs-lookup"><span data-stu-id="621c3-178">For more information about setting up sideloading, see [Enable app SideLoading in your non-developer site collection](https://blogs.msdn.microsoft.com/officeapps/2013/12/10/enable-app-sideloading-in-your-non-developer-site-collection/).</span></span>
  
> [!NOTE]
> <span data-ttu-id="621c3-179">Querladen-Apps ist eine Entwickler/Test-Funktion.</span><span class="sxs-lookup"><span data-stu-id="621c3-179">Sideloading apps is a developer/test feature.</span></span> <span data-ttu-id="621c3-180">Es ist **nicht für die Verwendung in der Produktion vorgesehen**.</span><span class="sxs-lookup"><span data-stu-id="621c3-180">It is **not intended for production use**.</span></span> <span data-ttu-id="621c3-181">Querladen Sie apps nicht regelmäßig, oder halten Sie App querladen länger aktiviert, als Sie das Feature aktiv verwenden.</span><span class="sxs-lookup"><span data-stu-id="621c3-181">Do not sideload apps regularly, or keep app sideloading enabled for longer than you are actively using the feature.</span></span> 
  
## <a name="add-content-to-the-add-in-project"></a><span data-ttu-id="621c3-182">Hinzufügen von Inhalt zum Add-in-Projekt</span><span class="sxs-lookup"><span data-stu-id="621c3-182">Add content to the add-in project</span></span>

<span data-ttu-id="621c3-183">Nach dem Erstellen eines Projekts und dem Einrichten des Debugging-Mechanismus umfasst das Hinzufügen von Inhalt zur APP die folgenden Aufgaben:</span><span class="sxs-lookup"><span data-stu-id="621c3-183">After creating a project and setting up the debugging mechanism, adding content to the app includes the following tasks:</span></span>
  
- <span data-ttu-id="621c3-184">Festlegen des Anwendungsbereichs</span><span class="sxs-lookup"><span data-stu-id="621c3-184">Setting the application scope</span></span>
    
- <span data-ttu-id="621c3-185">Verknüpfen der JSOM-Bibliothek</span><span class="sxs-lookup"><span data-stu-id="621c3-185">Linking the JSOM library</span></span>
    
- <span data-ttu-id="621c3-186">Hinzufügen von Benutzeroberflächenelementen zum Add-in</span><span class="sxs-lookup"><span data-stu-id="621c3-186">Adding UI Elements to the add-in</span></span>
    
- <span data-ttu-id="621c3-187">Initialisieren und Herstellen einer Verbindung mit dem Project Online-Dienst</span><span class="sxs-lookup"><span data-stu-id="621c3-187">Initializing and connecting to the Project Online service</span></span>
    
- <span data-ttu-id="621c3-188">Abrufen von Projekten und Details/Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="621c3-188">Retrieving projects and details/properties</span></span>
    
- <span data-ttu-id="621c3-189">Anzeigen von Projekten</span><span class="sxs-lookup"><span data-stu-id="621c3-189">Displaying projects</span></span>
    
- <span data-ttu-id="621c3-190">Anzeigen von Aufgaben für ein Projekt</span><span class="sxs-lookup"><span data-stu-id="621c3-190">Displaying tasks for a Project</span></span>
    
<span data-ttu-id="621c3-191">Das Add-in-Projekt besteht aus zahlreichen Dateien.</span><span class="sxs-lookup"><span data-stu-id="621c3-191">The add-in project consists of many files.</span></span> <span data-ttu-id="621c3-192">In diesem Beispiel müssen Sie die folgenden Dateien bearbeiten:</span><span class="sxs-lookup"><span data-stu-id="621c3-192">In this example, you'll need to edit the following files:</span></span> 
  
- <span data-ttu-id="621c3-193">Datei AppManifest. XML</span><span class="sxs-lookup"><span data-stu-id="621c3-193">AppManifest.xml</span></span>
    
- <span data-ttu-id="621c3-194">Default. aspx</span><span class="sxs-lookup"><span data-stu-id="621c3-194">Default.aspx</span></span>
    
- <span data-ttu-id="621c3-195">App. js</span><span class="sxs-lookup"><span data-stu-id="621c3-195">App.js</span></span>
    
- <span data-ttu-id="621c3-196">App. CSS – optional; enthält Formatvorlagendefinitionen für das Add-in</span><span class="sxs-lookup"><span data-stu-id="621c3-196">App.css - optional; contains style definitions developed for the add-in</span></span>
    
<span data-ttu-id="621c3-197">Wenn sich der Project Online-Mandant ändert, wie beispielsweise das Wechseln von einer Testversion zu einer Abonnement Website, können Sie die Projekteigenschaften einschließlich der Server Verbindung und der Website-URL mithilfe des Eigenschaftenfensters, das über die **Ansichts** > Eigenschaften verfügbar ist, aktualisieren.\*\* Fenster\*\* Befehl.</span><span class="sxs-lookup"><span data-stu-id="621c3-197">If the Project Online tenant changes, such as moving from a trial to a subscription site, you can update the project properties, including the Server Connection and Site URL, using the Properties Window available through the **View** > **Properties Window** command.</span></span> 
  
<span data-ttu-id="621c3-198">Sie können dem Projekt auch Dateien hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="621c3-198">You can also add files to the project.</span></span> <span data-ttu-id="621c3-199">Wenn dies der Fall ist, müssen Sie die Datei "Elements. xml" in derselben Gruppe (Inhalt, Bilder, Seiten oder Skripts) so aktualisieren, dass Sie die neuen Dateien enthält.</span><span class="sxs-lookup"><span data-stu-id="621c3-199">If so, you'll need to update the Elements.xml file located in the same group (Content, Images, Pages, or Scripts) to include the new files.</span></span> <span data-ttu-id="621c3-200">Weitere Informationen zu den Projektdateien finden Sie unter [erkunden der APP-Manifeststruktur und des Pakets eines SharePoint-Add-ins](https://docs.microsoft.com/sharepoint/dev/sp-add-ins/explore-the-app-manifest-structure-and-the-package-of-a-sharepoint-add-in).</span><span class="sxs-lookup"><span data-stu-id="621c3-200">For more information about the project files, see [Explore the app manifest structure and the package of a SharePoint Add-in](https://docs.microsoft.com/sharepoint/dev/sp-add-ins/explore-the-app-manifest-structure-and-the-package-of-a-sharepoint-add-in).</span></span>
  
### <a name="set-application-scope"></a><span data-ttu-id="621c3-201">Festlegen des Anwendungsbereichs</span><span class="sxs-lookup"><span data-stu-id="621c3-201">Set application scope</span></span>

<span data-ttu-id="621c3-202">Das Add-in benötigt Bereichs-oder Berechtigungsstufen, die definiert werden, bevor der Dienstinformationen in Abfrageergebnissen zurückgibt.</span><span class="sxs-lookup"><span data-stu-id="621c3-202">The add-in needs scope or permission levels defined before the service returns information in query results.</span></span> <span data-ttu-id="621c3-203">Verwenden Sie für dieses Add-in den folgenden Bereich für das Visual Studio-Projekt.</span><span class="sxs-lookup"><span data-stu-id="621c3-203">For this add-in, use the following scope to the Visual Studio project.</span></span> <span data-ttu-id="621c3-204">Diese Änderung wird in der Datei Datei AppManifest. XML auf der Registerkarte Berechtigungen vorgenommen:</span><span class="sxs-lookup"><span data-stu-id="621c3-204">This change is made to the AppManifest.xml file in the Permissions tab:</span></span>

|<span data-ttu-id="621c3-205">Bereich</span><span class="sxs-lookup"><span data-stu-id="621c3-205">Scope</span></span>|<span data-ttu-id="621c3-206">Berechtigung</span><span class="sxs-lookup"><span data-stu-id="621c3-206">Permission</span></span>|
|:-----|:-----|
|<span data-ttu-id="621c3-207">Mehrere Projekte (Project Server)</span><span class="sxs-lookup"><span data-stu-id="621c3-207">Multiple Projects (Project Server)</span></span>  <br/> |<span data-ttu-id="621c3-208">Lesen</span><span class="sxs-lookup"><span data-stu-id="621c3-208">Read</span></span>  <br/> |
   
<span data-ttu-id="621c3-209">Speichern Sie die Datei, nachdem Sie den Anwendungsbereich festgelegt haben.</span><span class="sxs-lookup"><span data-stu-id="621c3-209">Save the file after setting the application scope.</span></span> <span data-ttu-id="621c3-210">Andernfalls werden vom Dienst keine Daten zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="621c3-210">Otherwise, no data will be returned from the service.</span></span> 
  
### <a name="link-the-jsom-library"></a><span data-ttu-id="621c3-211">Verknüpfen der JSOM-Bibliothek</span><span class="sxs-lookup"><span data-stu-id="621c3-211">Link the JSOM library</span></span>

<span data-ttu-id="621c3-212">Die Laufzeit-Project Online-Bibliotheken, PS. js und PS. Debug. js, werden von Project Online bereitgestellt und sind immer die neueste Version.</span><span class="sxs-lookup"><span data-stu-id="621c3-212">The runtime Project Online libraries, PS.js and PS.debug.js, are provided by Project Online and are always the most recent version.</span></span> <span data-ttu-id="621c3-213">JavaScript-Add-Ins, die JSOM verwenden, müssen mit einer dieser Bibliotheken verknüpft sein.</span><span class="sxs-lookup"><span data-stu-id="621c3-213">JavaScript add-ins that use JSOM must link with one of these libraries.</span></span> <span data-ttu-id="621c3-214">Die Verknüpfungs Definitionen werden in der Datei "default. aspx" hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="621c3-214">The linking definitions are added in the Default.aspx file.</span></span> <span data-ttu-id="621c3-215">Die Befehle zur Verwendung von PS. js und/oder PS. Debug. js sind Teil des Codes in der Datei "App. js".</span><span class="sxs-lookup"><span data-stu-id="621c3-215">The commands to use the PS.js and/or PS.debug.js are part of the code located in the App.js file.</span></span>
  
<span data-ttu-id="621c3-216">Fügen Sie den folgenden Befehl für die Definition PS. js oder PS. Debug. js `<asp:Content ContentPlaceHolderID="PlaceHolderAdditionalPageHead"` im Element nach dem "SharePoint: ScriptLink" für SP. js hinzu.</span><span class="sxs-lookup"><span data-stu-id="621c3-216">Add the following command for PS.js or PS.debug.js definition in the  `<asp:Content ContentPlaceHolderID="PlaceHolderAdditionalPageHead"` element following the "SharePoint:ScriptLink" for sp.js.</span></span> 
  
```js
<SharePoint:ScriptLink name="PS.js" runat="server" OnDemand="false" LoadAfterUI="true" Localizable="false" />
```

> [!NOTE]
> <span data-ttu-id="621c3-217">Das **OnDemand** -Attribut für PS. js oder PS. Debug. js ist auf **false**festgelegt.</span><span class="sxs-lookup"><span data-stu-id="621c3-217">The **OnDemand** attribute for PS.js or PS.debug.js set to **false**.</span></span> 
  
### <a name="add-ui-elements-to-the-add-in"></a><span data-ttu-id="621c3-218">Hinzufügen von Benutzeroberflächenelementen zum Add-in</span><span class="sxs-lookup"><span data-stu-id="621c3-218">Add UI elements to the add-in</span></span>

<span data-ttu-id="621c3-219">Das Beispiel-Add-in besteht aus einigen Komponenten.</span><span class="sxs-lookup"><span data-stu-id="621c3-219">The example add-in consists of a few components.</span></span> <span data-ttu-id="621c3-220">Beschreibungen statischer Elemente befinden sich in der Datei default. aspx.</span><span class="sxs-lookup"><span data-stu-id="621c3-220">Static element descriptions are located in the Default.aspx file.</span></span> <span data-ttu-id="621c3-221">Dynamische Elementbeschreibungen und Code für alle Komponenten befinden sich in der Datei "App. js".</span><span class="sxs-lookup"><span data-stu-id="621c3-221">Dynamic element descriptions and code for all components are located in the App.js file.</span></span> <span data-ttu-id="621c3-222">Kommentare zu den Komponenten finden Sie in den Quell Codeauflistungen.</span><span class="sxs-lookup"><span data-stu-id="621c3-222">For comments regarding the components, refer to the source code listings.</span></span> <span data-ttu-id="621c3-223">Es folgt eine Liste der Benutzeroberflächenkomponenten im Add-in:</span><span class="sxs-lookup"><span data-stu-id="621c3-223">Here is a list of the UI components in the add-in:</span></span>
  
- <span data-ttu-id="621c3-224">Position</span><span class="sxs-lookup"><span data-stu-id="621c3-224">Title</span></span>
    
- <span data-ttu-id="621c3-225">Einführung in Wortschwall</span><span class="sxs-lookup"><span data-stu-id="621c3-225">Introductory verbiage</span></span>
    
- <span data-ttu-id="621c3-226">Schaltfläche zum Entfernen von Aufgaben aus der Tabelle</span><span class="sxs-lookup"><span data-stu-id="621c3-226">Button to remove tasks from the table</span></span>
    
- <span data-ttu-id="621c3-227">Tabelle, in der die Projekt-ID und der Name sowie die Vorgangsinformationen aufgeführt sind.</span><span class="sxs-lookup"><span data-stu-id="621c3-227">Table that lists the project ID and name, and the task information.</span></span>
    
- <span data-ttu-id="621c3-228">Aufgabenschaltfläche (für jedes Projekt einmal geklont), die Aufgabendaten in die Tabelle importiert.</span><span class="sxs-lookup"><span data-stu-id="621c3-228">Tasks Button (cloned once for each project) that imports task data into the table.</span></span>
    
<span data-ttu-id="621c3-229">Details zur Benutzeroberfläche, wie Titel und Kopfzeilen Bereich der Project-Tabelle, finden Sie in der Project-Standarddatei.</span><span class="sxs-lookup"><span data-stu-id="621c3-229">For details of the user interface, such as the title and the header portion of the project table, see the Default.aspx project file.</span></span>
  
### <a name="initialize-and-connect-to-the-host-system"></a><span data-ttu-id="621c3-230">Initialisieren und Herstellen einer Verbindung mit dem Hostsystem</span><span class="sxs-lookup"><span data-stu-id="621c3-230">Initialize and connect to the host system</span></span>

<span data-ttu-id="621c3-231">Die Datei app. js enthält den JavaScript-Code.</span><span class="sxs-lookup"><span data-stu-id="621c3-231">The App.js file contains the JavaScript code.</span></span> <span data-ttu-id="621c3-232">Das Add-in lädt PS. js im Browser und ruft dann die initializePage-Funktion auf.</span><span class="sxs-lookup"><span data-stu-id="621c3-232">The add-in loads PS.js in the browser, and then calls the initializePage function.</span></span> <span data-ttu-id="621c3-233">InitializePage Ruft einen Kontext zum Project Online-Endpunkt ab und startet die loadProjects-Funktion.</span><span class="sxs-lookup"><span data-stu-id="621c3-233">InitializePage retrieves a context to the Project Online endpoint and starts the loadProjects function.</span></span>
  
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

### <a name="retrieve-the-projects"></a><span data-ttu-id="621c3-234">Abrufen der Projekte</span><span class="sxs-lookup"><span data-stu-id="621c3-234">Retrieve the projects</span></span>

<span data-ttu-id="621c3-235">Die loadProjects-Funktion fragt den Dienst nach den Projektnamen und-IDs ab.</span><span class="sxs-lookup"><span data-stu-id="621c3-235">The loadProjects function queries the service for the project names and IDs.</span></span> 
  
<span data-ttu-id="621c3-236">Die Anwendung ruft den Projektnamen und die Projekt-ID ab. Weitere Informationen zum Projekt stehen zur Verfügung, und Sie können durch Ändern der Lademethode darauf zugreifen, um explizit die abzurufenden Eigenschaften zu identifizieren.</span><span class="sxs-lookup"><span data-stu-id="621c3-236">The application retrieves the project name and project Id. Other information about the project is available and can be accessed by modifying the load method to identify explicitly the properties to retrieve.</span></span> <span data-ttu-id="621c3-237">Ein Beispiel wird im Code als Kommentar angegeben.</span><span class="sxs-lookup"><span data-stu-id="621c3-237">An example is provided in the code as a comment.</span></span> 
  
<span data-ttu-id="621c3-238">Wenn die Abfrage erfolgreich ist, wird das Add-in weiterhin durch Aufrufen von displayProjects.</span><span class="sxs-lookup"><span data-stu-id="621c3-238">If the query succeeds, the add-in continues by calling displayProjects.</span></span> 
  
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

### <a name="display-the-projects"></a><span data-ttu-id="621c3-239">Anzeigen der Projekte</span><span class="sxs-lookup"><span data-stu-id="621c3-239">Display the projects</span></span>

<span data-ttu-id="621c3-240">Die displayProjects-Funktion erstellt eine Tabelle, eine Zeile pro Projekt und eine Schaltfläche, um die Aufgaben für das jeweilige Projekt anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="621c3-240">The displayProjects function creates a table, one row per project, and a button to show the tasks for the specific project.</span></span> 
  
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
> <span data-ttu-id="621c3-241">Die while-Schleife greift auf die Eigenschaften ID und Name zu.</span><span class="sxs-lookup"><span data-stu-id="621c3-241">The while loop accesses the ID and name properties.</span></span> <span data-ttu-id="621c3-242">Dies unterscheidet sich geringfügig vom Quellcodeprojekt, das eine Funktion aufruft, die wiederum auf dieselben Eigenschaften zugreift.</span><span class="sxs-lookup"><span data-stu-id="621c3-242">This is slightly different than the source code project that calls a function that, in turn, accesses the same properties.</span></span> 
  
### <a name="display-the-tasks-for-a-project"></a><span data-ttu-id="621c3-243">Anzeigen der Aufgaben für ein Projekt</span><span class="sxs-lookup"><span data-stu-id="621c3-243">Display the tasks for a project</span></span>

<span data-ttu-id="621c3-244">Die Aufgaben, während ein Teil des Add-Ins nicht Teil des anfänglichen Ladens ist.</span><span class="sxs-lookup"><span data-stu-id="621c3-244">The tasks, while part of the add-in, are not part of the initial loading.</span></span> <span data-ttu-id="621c3-245">Wenn der Benutzer an den mit einem Projekt verknüpften Vorgängen interessiert ist, werden durch Klicken auf die Schaltfläche Aufgaben anzeigen in der Liste mithilfe des btnLoadTasks-Ereignishandlers angezeigt.</span><span class="sxs-lookup"><span data-stu-id="621c3-245">If the user is interested in the tasks associated with a project, clicking the "Show Tasks" button causes the tasks to display in the list using the btnLoadTasks event handler.</span></span> 
  
<span data-ttu-id="621c3-246">Der btnLoadTasks-Ereignishandler mit der entsprechenden Projekt-ID fordert die Aufgaben für das angegebene Projekt vom Server an.</span><span class="sxs-lookup"><span data-stu-id="621c3-246">The btnLoadTasks event handler, with the appropriate project ID, requests the tasks for the specified project from the server.</span></span> <span data-ttu-id="621c3-247">Nach dem Abrufen übergibt btnLoadTasks die Aufgabenliste an Display Tasks, um die Aufgaben auf dem Bildschirm darzustellen.</span><span class="sxs-lookup"><span data-stu-id="621c3-247">Once retrieved, btnLoadTasks passes the task list to displayTasks to present the tasks onscreen.</span></span>
  
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

<span data-ttu-id="621c3-248">Mit der Display Tasks-Funktion werden die Aufgaben angezeigt, die einem angegebenen Projekt unmittelbar unterhalb des Projekteintrags zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="621c3-248">The displayTasks function displays the tasks associated with a specified project immediately beneath the project entry.</span></span>
  
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
> <span data-ttu-id="621c3-249">Die while-Schleife greift auf die Eigenschaften Vorgangs-ID und Name zu.</span><span class="sxs-lookup"><span data-stu-id="621c3-249">The while loop accesses the task ID and name properties.</span></span> <span data-ttu-id="621c3-250">Dies unterscheidet sich geringfügig vom Quellcodeprojekt, das eine Funktion aufruft, die wiederum auf dieselben Eigenschaften zugreift.</span><span class="sxs-lookup"><span data-stu-id="621c3-250">This is slightly different than the source code project that calls a function that, in turn, accesses the same properties.</span></span> 
  
<span data-ttu-id="621c3-251">Die Beispielausgabe für die Aufgaben eines einzelnen Projekts folgt.</span><span class="sxs-lookup"><span data-stu-id="621c3-251">Sample output for the tasks of a single project follows.</span></span>
  
<span data-ttu-id="621c3-252">![Screenshot mit der Ausgabe für eine Projektaufgabe] (media/f6500a3f-000b-4f3e-9be6-9a74d0bea15e.png "Screenshot mit der Ausgabe für eine Projektaufgabe")</span><span class="sxs-lookup"><span data-stu-id="621c3-252">![Screen shot showing the output for a project task](media/f6500a3f-000b-4f3e-9be6-9a74d0bea15e.png "Screen shot showing the output for a project task")</span></span>
  
## <a name="see-also"></a><span data-ttu-id="621c3-253">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="621c3-253">See also</span></span>

<span data-ttu-id="621c3-254">Dokumentation und Beispiele zu Project Online und Anwendungsentwicklung mit CSOM finden Sie im [Project-Entwicklungsportal](https://developer.microsoft.com/en-us/project).</span><span class="sxs-lookup"><span data-stu-id="621c3-254">For documentation and samples related to Project Online and application development using CSOM, see the [Project Development Portal](https://developer.microsoft.com/en-us/project).</span></span>
    


