---
title: Entwickeln einer Project Online-Anwendung mit dem clientseitigen Objektmodell
manager: soliver
ms.date: 11/08/2016
ms.audience: Developer
ms.assetid: 5740d0b2-5d36-40e4-9e83-577cb186359f
description: Dieser Artikel beschreibt die Entwicklung von Microsoft Project Online-Anwendungen für Desktopanwendungen mit dem .NET Framework 4.0. Die in diesem Artikel beschriebene Anwendung ruft Informationen vom hostenden Server ab.
localization_priority: Priority
ms.openlocfilehash: 3d3c2dd5b896c10dab9a0494288f38610cbc99e1
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 01/17/2019
ms.locfileid: "28712939"
---
# <a name="developing-a-project-online-application-using-the-client-side-object-model"></a><span data-ttu-id="42ff8-104">Entwickeln einer Project Online-Anwendung mit dem clientseitigen Objektmodell</span><span class="sxs-lookup"><span data-stu-id="42ff8-104">Developing a Project Online application using the client-side object model</span></span>

<span data-ttu-id="42ff8-105">Dieser Artikel beschreibt die Entwicklung von Microsoft Project Online-Anwendungen für Desktopanwendungen mit dem .NET Framework 4.0.</span><span class="sxs-lookup"><span data-stu-id="42ff8-105">This article describes Microsoft Project Online application development for desktop applications using the .NET Framework 4.0.</span></span> <span data-ttu-id="42ff8-106">Die in diesem Artikel beschriebene Anwendung ruft Informationen vom hostenden Server ab.</span><span class="sxs-lookup"><span data-stu-id="42ff8-106">The application described in this article retrieves information from the hosting server.</span></span> 
  
## <a name="background"></a><span data-ttu-id="42ff8-107">Hintergrund</span><span class="sxs-lookup"><span data-stu-id="42ff8-107">Background</span></span>

<span data-ttu-id="42ff8-108">Microsoft Project kam in den frühen 1990er Jahren als Desktopanwendung auf den Markt.</span><span class="sxs-lookup"><span data-stu-id="42ff8-108">Microsoft Project started as desktop application in the early 1990's.</span></span> <span data-ttu-id="42ff8-109">Heute ist Project viel mehr, wie seine verschiedenen Varianten belegen:</span><span class="sxs-lookup"><span data-stu-id="42ff8-109">Today, Project is much more, as its several varieties attest:</span></span>
  
- <span data-ttu-id="42ff8-110">Die Project Standard-Edition ist eine Desktopanwendung, die als eigenständige Anwendung ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="42ff8-110">Project standard edition is a desktop application that runs as a stand-alone application.</span></span>
    
- <span data-ttu-id="42ff8-111">Die Project Professional-Edition ist eine Desktopanwendung, die in größerem Maßstab mit einem Server interagieren und Daten austauschen kann und die in der Lage ist, die von der Project Standard-Edition bereitgestellte Funktionalität auszuführen.</span><span class="sxs-lookup"><span data-stu-id="42ff8-111">Project professional edition is a desktop application that can interact and share data with a server on a larger scale, as well as perform the functionality found in Project standard edition.</span></span>
    
- <span data-ttu-id="42ff8-112">Project Online ist ein von Microsoft gehosteter Dienst, der Unternehmen eine auf PMO-Ebene angesiedelte Lösung zur Koordinierung und Verwaltung von Projekten, Programmen und Portfolios bietet.</span><span class="sxs-lookup"><span data-stu-id="42ff8-112">Project Online is a Microsoft-hosted service that provides companies with a PMO-level solution to coordinate and manage projects, programs, and portfolios.</span></span> <span data-ttu-id="42ff8-113">Als Angebot, das sich von den Desktop-Editionen unterscheidet, kann Project Online Projektdetails während der gesamten Laufzeit eines Projekts verwalten und nachverfolgen.</span><span class="sxs-lookup"><span data-stu-id="42ff8-113">A different offering than the desktop editions, Project Online can maintain and track project details throughout the life of a project.</span></span> 
    
- <span data-ttu-id="42ff8-114">Project Server ist ein von einem Unternehmen gehosteter Dienst, in dem das Unternehmen den Server verwaltet und schützt, auf dem sich Projekt-, Programm- und Portfolioinformationen befinden.</span><span class="sxs-lookup"><span data-stu-id="42ff8-114">Project Server is an enterprise-hosted service in which the enterprise manages and secures the server containing project, program, and portfolio information.</span></span> <span data-ttu-id="42ff8-115">Project Server bietet, insbesondere durch Schützen des Servers im eigenen Haus, die projekt-, programm- und portfolioorientierten Funktionen von extern gehostetem Project Online mit einer größeren Anpassungsfähigkeit.</span><span class="sxs-lookup"><span data-stu-id="42ff8-115">Project Server, by virtue of securing the server in-house, offers the project, program, and portfolio oriented features of externally-hosted Project Online with a greater capacity for customization.</span></span>
    
<span data-ttu-id="42ff8-116">Project Online hat drei Online-API-Sätze: clientseitiges Objektmodell (CSOM), JavaScript-Objektmodell (JSOM) und Representational State Transfer (REST).</span><span class="sxs-lookup"><span data-stu-id="42ff8-116">Project Online has three online API sets: Client-side Object Model (CSOM), JavaScript Object Model (JSOM), and Representational State Transfer (REST).</span></span> 
  
- <span data-ttu-id="42ff8-117">Die .NET CSOM-Implementierung ist die bevorzugte Schnittstelle bei der Entwicklung von Windows-Anwendungen, die mit Project Online-Mandanten interagieren.</span><span class="sxs-lookup"><span data-stu-id="42ff8-117">The .NET CSOM implementation is the preferred interface when developing Windows applications that interact with Project Online tenants.</span></span> <span data-ttu-id="42ff8-118">Typische Umgebungen für benutzerorientierte Anwendungen sind Windows-Desktops und Microsoft Surface-Geräte.</span><span class="sxs-lookup"><span data-stu-id="42ff8-118">Typical environments for user-centric applications include Windows desktops and Microsoft Surface devices.</span></span> <span data-ttu-id="42ff8-119">Back-End-Anwendung, die mit .NET CSOM geschrieben wurden, können mit anderen Servern für Geschäftslogik und Datenquellen verbunden werden, die sich außerhalb von Project Online befinden.</span><span class="sxs-lookup"><span data-stu-id="42ff8-119">Back-end applications written with .NET CSOM can connect to other servers for business logic and data sources that are external to Project Online.</span></span> <span data-ttu-id="42ff8-120">Abrufanforderungen an Project Online verwenden ein LINQ-ähnliches Abfragesystem, das mehrere Verbesserungen gegenüber den einfachen Abruffunktionen bietet.</span><span class="sxs-lookup"><span data-stu-id="42ff8-120">Retrieval requests to Project Online use a LINQ-like query system that offers several enhancements over basic retrieval functions.</span></span>
    
- <span data-ttu-id="42ff8-121">Die JavaScript-Objektmodell-Schnittstelle (JSOM-Schnittstelle) bietet browserübergreifende Unterstützung für Project Online-Add-Ins. Ein Add-In ist eine Webanwendung, die im Project Online-Mandanten gespeichert ist.</span><span class="sxs-lookup"><span data-stu-id="42ff8-121">The JavaScript Object Model (JSOM) interface provides cross-browser support for Project Online Add-ins. An add-in is a web application that is stored in the Project Online tenant.</span></span> <span data-ttu-id="42ff8-122">Wenn ein Benutzer ein Add-In ausführen möchte, wird der Code für das Add-In heruntergeladen und im Browser auf dem Benutzercomputer ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="42ff8-122">When a user wants to run an add-in, the code for the add-in downloads and runs in the browser on the user machine.</span></span> 
    
- <span data-ttu-id="42ff8-123">Das REST/OData-Modell stellt HTTP-basierte Kommunikation bereit. Diese Schnittstelle wird für Anwendungen in Nicht-Windows-Umgebungen empfohlen.</span><span class="sxs-lookup"><span data-stu-id="42ff8-123">The REST/Odata model provides HTTP-based communication, This interface is recommended for applications in non-Windows environments.</span></span> <span data-ttu-id="42ff8-124">Kommunikationsendpunkte sind die Objekte in der PWA-Website (Project Web Application).</span><span class="sxs-lookup"><span data-stu-id="42ff8-124">Communication endpoints are the objects in the Project Web Application (PWA) site.</span></span> <span data-ttu-id="42ff8-125">Ergebnisse stellen normale HTTP-Statuscodes bereit.</span><span class="sxs-lookup"><span data-stu-id="42ff8-125">Results provide normal HTTP status codes.</span></span>
    
<span data-ttu-id="42ff8-126">Dieser Artikel konzentriert sich auf eine Anwendung, in der die .NET CSOM-Schnittstelle verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="42ff8-126">This article focuses on an application that uses the .NET CSOM interface.</span></span>
  
## <a name="prerequisites"></a><span data-ttu-id="42ff8-127">Voraussetzungen</span><span class="sxs-lookup"><span data-stu-id="42ff8-127">Prerequisites</span></span>

<span data-ttu-id="42ff8-128">Beginnen Sie mit einem Basissystem unter Windows 10, und fügen Sie die folgenden Elemente hinzu:</span><span class="sxs-lookup"><span data-stu-id="42ff8-128">Start with a base system running Windows 10, and add the following items:</span></span>
  
- <span data-ttu-id="42ff8-129">.NET Framework 4.0 oder höher: Verwenden Sie das vollständige Framework.</span><span class="sxs-lookup"><span data-stu-id="42ff8-129">.Net Framework 4.0 or later -- Use the complete framework.</span></span> <span data-ttu-id="42ff8-130">Die Download-Website ist https://msdn.microsoft.com/vstudio/aa496123.aspx.</span><span class="sxs-lookup"><span data-stu-id="42ff8-130">The download site is https://msdn.microsoft.com/vstudio/aa496123.aspx.</span></span>
    
- <span data-ttu-id="42ff8-131">Visual Studio 2013 oder höher: Es kann jede Edition verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="42ff8-131">Visual Studio 2013 or later -- Any edition is acceptable.</span></span> <span data-ttu-id="42ff8-132">Die Community-Edition von Visual Studio 2015 wurde verwendet, um die Beispielanwendung zu entwickeln.</span><span class="sxs-lookup"><span data-stu-id="42ff8-132">The community edition of Visual Studio 2015 was used to develop the sample application.</span></span> <span data-ttu-id="42ff8-133">Die Community-Edition steht unter https://www.visualstudio.com/en-us/products/visual-studio-community-vs.aspx zur Verfügung.</span><span class="sxs-lookup"><span data-stu-id="42ff8-133">The community edition is available at https://www.visualstudio.com/en-us/products/visual-studio-community-vs.aspx.</span></span>
    
- <span data-ttu-id="42ff8-134">SharePoint Client Components SDK: Project Online und Project Server setzen auf SharePoint und SharePoint-Assemblys auf.</span><span class="sxs-lookup"><span data-stu-id="42ff8-134">SharePoint Client Components SDK -- Project Online and Project Server sit on top of SharePoint, and SharePoint assemblies.</span></span> <span data-ttu-id="42ff8-135">Die SharePoint Client Components sind in den Visual Studio-Editionen Professional und Enterprise enthalten.</span><span class="sxs-lookup"><span data-stu-id="42ff8-135">The SharePoint Client Components are included in Visual Studio Professional and Enterprise editions.</span></span> <span data-ttu-id="42ff8-136">Wenn Sie Visual Studio Community verwenden, ist die neueste Version des Office Developer Tools SDKs auf der folgenden Website verfügbar: https://www.microsoft.com/en-us/download/details.aspx?id=35585.</span><span class="sxs-lookup"><span data-stu-id="42ff8-136">If you use Visual Studio Community edition, the latest version of the Office Developer Tools SDK is available at the following site: https://www.microsoft.com/en-us/download/details.aspx?id=35585.</span></span>
    
- <span data-ttu-id="42ff8-137">Ein Project Online-Konto: Dies ermöglicht den Zugriff auf die hostende Website.</span><span class="sxs-lookup"><span data-stu-id="42ff8-137">A Project Online account -- This provides access to the hosting site.</span></span> <span data-ttu-id="42ff8-138">Weitere Informationen zum Einrichten eines Project Online-Kontos finden Sie unter https://products.office.com/en-us/Project/project-online-portfolio-management.</span><span class="sxs-lookup"><span data-stu-id="42ff8-138">For more information about obtaining a Project Online account, see https://products.office.com/en-us/Project/project-online-portfolio-management.</span></span>
    
- <span data-ttu-id="42ff8-139">Projekte auf der hostenden Website, die mit Informationen ausgefüllt sind</span><span class="sxs-lookup"><span data-stu-id="42ff8-139">Projects on the hosting site that are populated with information</span></span>
    
> [!NOTE]
> <span data-ttu-id="42ff8-140">Das standardmäßige .NET Framework (4.0 oder höher) ist das zu verwendende Framework.</span><span class="sxs-lookup"><span data-stu-id="42ff8-140">The standard .NET Framework (4.0 or later) is the correct framework to use.</span></span> <span data-ttu-id="42ff8-141">Verwenden Sie nicht .NET Framework 4 Client Profile.</span><span class="sxs-lookup"><span data-stu-id="42ff8-141">Do not use the .NET Framework 4 Client Profile.</span></span> 
  
## <a name="develop-the-application"></a><span data-ttu-id="42ff8-142">Entwickeln der Anwendung</span><span class="sxs-lookup"><span data-stu-id="42ff8-142">Develop the application</span></span>

<span data-ttu-id="42ff8-143">Beim Entwickeln einer Desktopanwendung für SharePoint ist das clientseitige Objektmodell (CSOM) für Project die bevorzugte Schnittstelle.</span><span class="sxs-lookup"><span data-stu-id="42ff8-143">In developing a desktop application for SharePoint, the preferred interface is the Project client side object model (CSOM).</span></span> 
  
<span data-ttu-id="42ff8-144">Sie können das vollständige Beispiel aus https://github.com/OfficeDev/Project-CSOM-List-Projects-Tasks herunterladen.</span><span class="sxs-lookup"><span data-stu-id="42ff8-144">You can download the completed sample at https://github.com/OfficeDev/Project-CSOM-List-Projects-Tasks.</span></span>
  
<span data-ttu-id="42ff8-145">Die ersten beiden Themen behandeln grundlegende Aspekte: Erstellen eines Visual Studio-Projekts mit geeigneten Namespaces und Assemblys und Zugreifen auf den hostenden Server.</span><span class="sxs-lookup"><span data-stu-id="42ff8-145">The first two topics cover basic issues: creating a Visual Studio project with appropriate namespaces and assemblies, and accessing the hosting server.</span></span> <span data-ttu-id="42ff8-146">Die übrigen Themen befassen sich mit dem Abrufen von Informationen über das CSOM aus einem und aus vielen Objekten.</span><span class="sxs-lookup"><span data-stu-id="42ff8-146">The remaining topics deal with retrieving information through the CSOM, from one and many objects.</span></span> 
  
<span data-ttu-id="42ff8-147">Das Abrufen von Informationen vom Host ist ein Zwei-Aktionen-Vorgang aus Client-Anwendungen.</span><span class="sxs-lookup"><span data-stu-id="42ff8-147">Retrieving information from the host is a two-action process from client applications.</span></span> <span data-ttu-id="42ff8-148">Als Erstes gibt die Anwendung Abrufanforderungen an und sendet diese an den Server.</span><span class="sxs-lookup"><span data-stu-id="42ff8-148">First, the application specifies and sends one or more retrieval requests to the server.</span></span> <span data-ttu-id="42ff8-149">Als Zweites sendet die Anwendung eine Benachrichtigung an den Server, damit die übermittelten Abfragen ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="42ff8-149">Second, the application issues a notification to the server to execute the submitted queries.</span></span> <span data-ttu-id="42ff8-150">Der Server antwortet, indem er die Abfrageergebnisse an den Client sendet.</span><span class="sxs-lookup"><span data-stu-id="42ff8-150">The server responds by sending the query results to the client.</span></span>
  
### <a name="set-up-the-visual-studio-project"></a><span data-ttu-id="42ff8-151">Einrichten des Visual Studio-Projekts</span><span class="sxs-lookup"><span data-stu-id="42ff8-151">Step 1: Set up the Visual Studio project</span></span>

<span data-ttu-id="42ff8-152">Das Einrichten der Anwendung besteht aus dem Erstellen eines neuen Projekts, dem Verknüpfen der entsprechenden Assemblys und dem Deklarieren der benötigten Namespaces.</span><span class="sxs-lookup"><span data-stu-id="42ff8-152">The application setup consists of creating a new project, linking the appropriate assemblies and declaring the needed namespaces.</span></span> <span data-ttu-id="42ff8-153">Visual Studio bietet verschiedene Typen von Entwicklungsprojekten.</span><span class="sxs-lookup"><span data-stu-id="42ff8-153">Visual Studio presents several types of development projects.</span></span> 
  
#### <a name="select-a-visual-studio-project"></a><span data-ttu-id="42ff8-154">Auswählen eines Visual Studio-Projekts</span><span class="sxs-lookup"><span data-stu-id="42ff8-154">Select a Visual Studio project</span></span>

1. <span data-ttu-id="42ff8-155">Starten Sie Visual Studio, und wählen Sie **Neues Projekt starten** auf der Startseite aus.</span><span class="sxs-lookup"><span data-stu-id="42ff8-155">Launch Visual Studio and select **Start A New Project** on the Start Page.</span></span> 
    
   <span data-ttu-id="42ff8-156">Im Dialogfeld "Neues Projekt" werden verfügbare Anwendungsvorlagen und Datenfelder für die jeweils ausgewählte Vorlage angezeigt.</span><span class="sxs-lookup"><span data-stu-id="42ff8-156">The New Project dialog displays available application templates, and data fields for any selected template.</span></span> 
    
2. <span data-ttu-id="42ff8-157">Geben Sie für diese Anwendung die folgenden Elemente an.</span><span class="sxs-lookup"><span data-stu-id="42ff8-157">For this application, specify the following items.</span></span> <span data-ttu-id="42ff8-158">Schlüsselwörter, die auf dem Bildschirm zu finden sind, sind fett ausgezeichnet:</span><span class="sxs-lookup"><span data-stu-id="42ff8-158">Keywords encountered on the screen have a bold attribute:</span></span>
    
   1. <span data-ttu-id="42ff8-159">Wählen Sie aus den installierten Vorlagen im linken Bereich die Vorlage \*\* C# \*\*  =>  **Windows** => **Klassischer Desktop** aus.</span><span class="sxs-lookup"><span data-stu-id="42ff8-159">From the Installed templates in the left pane, select **C#** => **Windows** => **Classic desktop**.</span></span> 
    
   2. <span data-ttu-id="42ff8-160">Wählen Sie oben im zentralen Bereich die Option **.NET Framework 4** aus.</span><span class="sxs-lookup"><span data-stu-id="42ff8-160">At the top of the central pane, select **.NET Framework 4**.</span></span> 
    
   3. <span data-ttu-id="42ff8-161">Wählen Sie aus den Anwendungstypen im zentralen Bereich den Typ **Konsolenanwendung** aus.</span><span class="sxs-lookup"><span data-stu-id="42ff8-161">From the application types in the central pane, choose **Console Application**.</span></span> 
    
   4. <span data-ttu-id="42ff8-162">Geben Sie im unteren Abschnitt einen Namen und Speicherort für das Projekt und einen Projektmappennamen an.</span><span class="sxs-lookup"><span data-stu-id="42ff8-162">In the bottom section, specify a name and location for the project, and a solution name.</span></span> 
    
   5. <span data-ttu-id="42ff8-163">Aktivieren Sie außerdem im unteren Abschnitt das Kontrollkästchen **Projektmappenverzeichnis erstellen**.</span><span class="sxs-lookup"><span data-stu-id="42ff8-163">Also in the bottom section, check the **Create directory for solution** box.</span></span> 
    
3. <span data-ttu-id="42ff8-164">Klicken Sie auf **OK**, um das Ausgangsprojekt zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="42ff8-164">Click **OK** to create the workflow.</span></span> 
    
#### <a name="add-assemblies"></a><span data-ttu-id="42ff8-165">Hinzufügen von Assemblys</span><span class="sxs-lookup"><span data-stu-id="42ff8-165">Add assemblies</span></span>

<span data-ttu-id="42ff8-166">Für die VS-Projektmappe sind die Assembly "ProjectServerClient" aus dem Project 2013 SDK, einige Assemblys aus dem SharePoint SDK und die .NET Framework-Assembly "System.Security" erforderlich.</span><span class="sxs-lookup"><span data-stu-id="42ff8-166">The VS solution needs the ProjectServerClient assembly from the Project 2103 SDK, a couple of assemblies from the SharePoint SDK, and the .NET Framework System.Security assembly.</span></span>
  
1. <span data-ttu-id="42ff8-167">Klicken Sie im Projektmappen-Explorer von VS mit der rechten Maustaste auf den Eintrag "Verweise", und wählen Sie **Verweis hinzufügen...**</span><span class="sxs-lookup"><span data-stu-id="42ff8-167">In the VS Solution Explorer, right-click the References entry, and select **Add Reference…**</span></span> <span data-ttu-id="42ff8-168">im Kontextmenü aus.</span><span class="sxs-lookup"><span data-stu-id="42ff8-168">from the shortcut menu.</span></span> 
    
2. <span data-ttu-id="42ff8-169">Aktivieren Sie den Verweis **Microsoft.ProjectServer.Client.dll**.</span><span class="sxs-lookup"><span data-stu-id="42ff8-169">Check the **Microsoft.ProjectServer.Client.dll**.</span></span> 
    
   <span data-ttu-id="42ff8-170">Klicken Sie ggf. auf die Schaltfläche **Durchsuchen...**</span><span class="sxs-lookup"><span data-stu-id="42ff8-170">If needed, click the **Browse…**</span></span> <span data-ttu-id="42ff8-171">unten im Dialogfeld, und navigieren Sie zum Installationsverzeichnis des Project 2013 SDKs, um die Assembly zu finden.</span><span class="sxs-lookup"><span data-stu-id="42ff8-171">button at the bottom of the dialog and navigate to the Project 2013 SDK installation directory to locate the assembly.</span></span> 
    
3. <span data-ttu-id="42ff8-172">Klicken Sie auf **OK**.</span><span class="sxs-lookup"><span data-stu-id="42ff8-172">Click **OK**.</span></span> 
    
4. <span data-ttu-id="42ff8-173">Fügen Sie den Namespace "ProjectServer.Client" zur CS-Datei hinzu.</span><span class="sxs-lookup"><span data-stu-id="42ff8-173">Add the PrjoctServer Client namespace to the .cs file.</span></span>
    
   ```cs
    using Microsoft.ProjectServer.Client;
   ```

<span data-ttu-id="42ff8-174">Fügen Sie die SharePoint 2013 SDK-Assemblys über die NuGet-Paket-Manager-Konsole hinzu.</span><span class="sxs-lookup"><span data-stu-id="42ff8-174">Add the SharePoint 2013 SDK assemblies using the NuGet Package Manager Console.</span></span> 
  
1. <span data-ttu-id="42ff8-175">Klicken Sie über das VS-Menü "Extras" auf die folgenden Menüs: **Extras =\> NuGet-Paket-Manager =\> Paket-Manager-Konsole**.</span><span class="sxs-lookup"><span data-stu-id="42ff8-175">From the VS Tools menu, click the following menus: **Tools =\> NuGet Package Manager =\> Package Manager Console**.</span></span> 
    
2. <span data-ttu-id="42ff8-176">Geben Sie in der Paket-Manager-Konsole den folgenden Befehl ein, und drücken Sie die \<EINGABETASTE\>:</span><span class="sxs-lookup"><span data-stu-id="42ff8-176">In the Package Manager Console, enter the following command and press \<ENTER\>:</span></span>
    
   ```cs
    Install-Package Microsoft.SharePointOnline.CSOM
   ```

   <span data-ttu-id="42ff8-177">Die **Paket-Manager-Konsole** stellt eine Beschreibung der Befehlsergebnisse bereit, und im Projektmappen-Explorer von VS werden die SharePoint-Assemblys in den Projektverweisen angezeigt.</span><span class="sxs-lookup"><span data-stu-id="42ff8-177">The **Package Manager Console** provides a description of the command results; and, the VS Solution Explorer displays the SharePoint assemblies in the project references.</span></span> 
    
3. <span data-ttu-id="42ff8-178">Fügen Sie die Namespaces zur CS-Datei hinzu:</span><span class="sxs-lookup"><span data-stu-id="42ff8-178">Add the namespaces to the .cs file:</span></span>
    
   ```cs
    using Microsoft.SharePoint.Client;
   ```

<span data-ttu-id="42ff8-179">Die Assembly "System.Security" gehört zu .NET Framework und wurde mit dem Framework installiert.</span><span class="sxs-lookup"><span data-stu-id="42ff8-179">The System.Security assembly is part of .NET Framework and was installed with the framework.</span></span> <span data-ttu-id="42ff8-180">Für die Beispielanwendung ist ein weiterer Namespace erforderlich, der dem hostenden System eine verschlüsselte Zeichenfolge für die Authentifizierung bereitstellt.</span><span class="sxs-lookup"><span data-stu-id="42ff8-180">The sample application needs one more namespace that provides an encrypted string to the hosting system for authentication.</span></span> <span data-ttu-id="42ff8-181">Sobald die Anwendung authentifiziert ist, kann sie auf Projekte auf dem hostenden System zugreifen.</span><span class="sxs-lookup"><span data-stu-id="42ff8-181">Once authenticated, the application can access projects on the hosting system.</span></span> <span data-ttu-id="42ff8-182">Fügen Sie den Namespace "System.Security" wie folgt zur CS-Datei hinzu:</span><span class="sxs-lookup"><span data-stu-id="42ff8-182">Add the System.Security namespace to the .cs file in this way:</span></span>
  
1. <span data-ttu-id="42ff8-183">Klicken Sie im Projektmappen-Explorer von VS mit der rechten Maustaste auf den Eintrag "Verweise", und wählen Sie **Verweis hinzufügen...**</span><span class="sxs-lookup"><span data-stu-id="42ff8-183">In the VS Solution Explorer, right-click the References entry, and select **Add Reference…**</span></span> <span data-ttu-id="42ff8-184">im Kontextmenü aus.</span><span class="sxs-lookup"><span data-stu-id="42ff8-184">from the shortcut menu.</span></span> 
    
2. <span data-ttu-id="42ff8-185">Wählen Sie **Assemblys =\> Framework** im linken Bereich des Dialogfelds für den Verweis-Manager aus, und aktivieren Sie dann **System.Security**.</span><span class="sxs-lookup"><span data-stu-id="42ff8-185">Select **Assemblies =\> Framework** in the left pane of the References Manager dialog, then check **System.Security**.</span></span> 
    
3. <span data-ttu-id="42ff8-186">Klicken Sie auf **OK**.</span><span class="sxs-lookup"><span data-stu-id="42ff8-186">Click **OK**.</span></span> 
    
4. <span data-ttu-id="42ff8-187">Fügen Sie den Namespace "System.Security" zur CS-Datei hinzu:</span><span class="sxs-lookup"><span data-stu-id="42ff8-187">Add the System.Security namespace to the .cs file:</span></span>
    
   ```cs
    using System.Security;
   ```

<span data-ttu-id="42ff8-188">Der Anfang der CS-Datei sollte die folgenden Namespaces enthalten:</span><span class="sxs-lookup"><span data-stu-id="42ff8-188">The start of the .cs file should contain the following namespaces:</span></span>
  
- <span data-ttu-id="42ff8-189">System</span><span class="sxs-lookup"><span data-stu-id="42ff8-189">System</span></span>
    
- <span data-ttu-id="42ff8-190">System.Collections.Generic</span><span class="sxs-lookup"><span data-stu-id="42ff8-190">System.Collections.Generic</span></span>
    
- <span data-ttu-id="42ff8-191">System.Linq</span><span class="sxs-lookup"><span data-stu-id="42ff8-191">System.Linq</span></span>
    
- <span data-ttu-id="42ff8-192">System.Test</span><span class="sxs-lookup"><span data-stu-id="42ff8-192">System.Test</span></span>
    
- <span data-ttu-id="42ff8-193">Microsoft.ProjectServer.Client</span><span class="sxs-lookup"><span data-stu-id="42ff8-193">Microsoft.ProjectServer.Client</span></span>
    
- <span data-ttu-id="42ff8-194">Microsoft.SharePoint.Client</span><span class="sxs-lookup"><span data-stu-id="42ff8-194">Microsoft.SharePoint.Client</span></span>
    
- <span data-ttu-id="42ff8-195">System.Security</span><span class="sxs-lookup"><span data-stu-id="42ff8-195">System.Security</span></span>
    
### <a name="connect-to-the-host-system"></a><span data-ttu-id="42ff8-196">Verbinden mit dem Hostsystem</span><span class="sxs-lookup"><span data-stu-id="42ff8-196">Connect to the host system</span></span>

<span data-ttu-id="42ff8-197">Project Online ist eine SharePoint-Anwendung, sodass die Verwendung der SharePoint-Authentifizierung der richtige Ansatz ist.</span><span class="sxs-lookup"><span data-stu-id="42ff8-197">Project Online is a SharePoint application, so using SharePoint authentication is the correct approach.</span></span> <span data-ttu-id="42ff8-198">Im folgenden Codefragment wird das Zugreifen auf die gehostete Umgebung vorbereitet.</span><span class="sxs-lookup"><span data-stu-id="42ff8-198">The following code fragment prepares to access the hosted environment.</span></span>
  
```cs
    class Program
    {
        private static ProjectContext projContext;
        static void Main (string[] args)
        {
            using (ProjectContext projContext = new ProjectContext("https://Contoso.sharepoint.com/sites/pwa"))
            {
                SecureString password - new SecureString();
                foreach (char c in "password".ToCharArray()) password.AppendChar(c);
                //Using SharePoint method to load Credentials
                projContext.Credentials = new SharePointOnlineCredentials("sarad@Contoso.onmicrosoft.com", password);

```

<span data-ttu-id="42ff8-199">Die Vorbereitungen für das Zugreifen auf die gehostete Umgebung umfassen die folgenden Schritte:</span><span class="sxs-lookup"><span data-stu-id="42ff8-199">Preparations to access the hosted environment include the following items:</span></span>
  
1. <span data-ttu-id="42ff8-200">Erstellen Sie ein Kontextobjekt für die Projekte: Dieses Objekt ist im folgenden Code aus dem vorherigen Codefragment enthalten.</span><span class="sxs-lookup"><span data-stu-id="42ff8-200">Create a context object for the projects -- this is contained in the following code of the preceding code fragment.</span></span> 
    
   ```cs
    private static ProjectContext projContext;
    
   ```

   <span data-ttu-id="42ff8-201">Der Kontext wird an andere Komponenten vererbt, wodurch es dem System ermöglicht wird, den Kontext des Project-Objektmodells zu verwalten.</span><span class="sxs-lookup"><span data-stu-id="42ff8-201">The context is inherited by other components, allowing the system to manage the context of the Project object model.</span></span>
    
2. <span data-ttu-id="42ff8-202">Geben Sie die Hostwebsite an. Dies erfolgt im folgenden Code aus dem vorherigen Codefragment.</span><span class="sxs-lookup"><span data-stu-id="42ff8-202">Identify the host site -- this is done in the following code from the preceding code fragment.</span></span>
    
   ```cs
    using (ProjectContext projContext = new ProjectContext("https://Contoso.sharepoint.com/sites/pwa"))
   ```

   <span data-ttu-id="42ff8-203">Wenn der Projektkontext instanziiert wird, muss die Anwendung den Stamm der Websitesammlung für Projekte bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="42ff8-203">When instantiating the projects context, the application needs to provide the root of the Projects site collection.</span></span> <span data-ttu-id="42ff8-204">Die Anwendung verwendet eine Teilzeichenfolge der URL des Stamms der Projekte.</span><span class="sxs-lookup"><span data-stu-id="42ff8-204">The application uses a substring of the URL of the root of the Projects.</span></span> <span data-ttu-id="42ff8-205">Ein Momentaufnahme dieser Position ist in der folgenden Abbildung mit einem roten Rechteck hervorgehoben.</span><span class="sxs-lookup"><span data-stu-id="42ff8-205">A snapshot of this location is highlighted with a red rectangle in the following illustration.</span></span> <span data-ttu-id="42ff8-206">Für die Authentifizierung wird die Zeichenfolge ab deren Anfang bis einschließlich der Teilzeichenfolge "pwa" benötigt.</span><span class="sxs-lookup"><span data-stu-id="42ff8-206">The authentication needs the string from its start through the substring "pwa".</span></span> <span data-ttu-id="42ff8-207">Im Codeeintrag wird für die Anwendung die Zeichenfolge "https://XXXXXXXX.sharepoint.com/sites/pwa" verwendet.</span><span class="sxs-lookup"><span data-stu-id="42ff8-207">In the code listing, the application uses the string "https://XXXXXXXX.sharepoint.com/sites/pwa".</span></span>
        
   <span data-ttu-id="42ff8-208">![Momentaufnahme der URL der Websitesammlung für Projekte in einem roten Rahmen ](media/d48c4894-5dba-46b6-886a-3c59bfb83c4d.png "Momentaufnahme der URL der Websitesammlung für Projekte in einem roten Rahmen")</span><span class="sxs-lookup"><span data-stu-id="42ff8-208">![Screen shot of the URL of the Projects site collection within a red border.](media/d48c4894-5dba-46b6-886a-3c59bfb83c4d.png "Screen shot of the URL of the Projects site collection within a red border")</span></span>
  
3. <span data-ttu-id="42ff8-209">Geben Sie das Kennwort in einer sicheren Zeichenfolge an. Dies erfolgt im folgenden Code aus dem vorherigen Codefragment.</span><span class="sxs-lookup"><span data-stu-id="42ff8-209">Place the password in a secure string -- this is done in the following code from the preceding code fragment.</span></span>
    
   ```cs
    SecureString password - new SecureString();
    foreach (char c in "password".ToCharArray()) password.AppendChar(c);
    
   ```

   <span data-ttu-id="42ff8-210">Das Kennwort und das Benutzerkonto sind die Anmeldeinformationen für den Zugriff auf die Hostwebsite.</span><span class="sxs-lookup"><span data-stu-id="42ff8-210">The password and user account are the credentials to access the host site.</span></span> 
    
4. <span data-ttu-id="42ff8-211">Fügen Sie das Benutzerkonto und das Kennwort zur Anmeldeinformationen-Komponente des Kontextobjekts hinzu. Dies erfolgt im folgenden Code aus dem vorherigen Codefragment.</span><span class="sxs-lookup"><span data-stu-id="42ff8-211">Add the user account and password to the credentials portion of the context object -- this is done in the following code from the preceding code fragment.</span></span>
    
   ```cs
    projContext.Credentials = new SharePointOnlineCredentials("sarad@Contoso.onmicrosoft.com", password);
   ```

<span data-ttu-id="42ff8-212">Der instanziierte Projektkontext kann nun verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="42ff8-212">The instantiated project context is ready to use.</span></span>
  
### <a name="list-all-published-projects"></a><span data-ttu-id="42ff8-213">Auflisten aller veröffentlichten Projekte</span><span class="sxs-lookup"><span data-stu-id="42ff8-213">List all published projects</span></span>

<span data-ttu-id="42ff8-214">Project Online und ProjectServer verwenden Proxys, um mit dem Server zum Ausführen von Erstell-, Berichts-, Aktualisier- und Löschvorgängen zu kommunizieren.</span><span class="sxs-lookup"><span data-stu-id="42ff8-214">Project Online and ProjectServer use proxies to communicate with the server for create, report, update, and delete (CRUD) operations.</span></span> <span data-ttu-id="42ff8-215">Der Host/Server verarbeitet Anfragen auf effiziente Weise und lässt den Client die folgenden Aktionen in der Kommunikation mit dem Server ausführen:</span><span class="sxs-lookup"><span data-stu-id="42ff8-215">The host/server handles requests in an efficient manner and has the client perform the following actions in communicating with the server:</span></span>
  
1. <span data-ttu-id="42ff8-216">Richten Sie einen Kontext für Kommunikation ein.</span><span class="sxs-lookup"><span data-stu-id="42ff8-216">Establish a context for communication.</span></span> 
    
   <span data-ttu-id="42ff8-217">Der Kontext wird von der Projektesammlung sowie anderen Objekten und Sammlungen (Collections) durch Vererbung verwendet, einschließlich der Aufgabensammlung, der Zuweisungensammlung, des Stufenobjekts und benutzerdefinierter Felder.</span><span class="sxs-lookup"><span data-stu-id="42ff8-217">The context is used by the projects collection, as well as other objects and collections through inheritance, including the tasks collection, assignments collection, the stage object, and custom fields.</span></span> 
    
2. <span data-ttu-id="42ff8-218">Geben Sie mit dem Objektmodell ein Objekt, eine Sammlung oder Daten an, die abgerufen werden sollen.</span><span class="sxs-lookup"><span data-stu-id="42ff8-218">Use the object model to specify an object to retrieve or from which to retrieve data.</span></span>
    
   <span data-ttu-id="42ff8-219">In diesem Schritt wird LINQ als Abfrage oder Methode verwendet.</span><span class="sxs-lookup"><span data-stu-id="42ff8-219">This step uses LINQ as a query or as a method.</span></span> <span data-ttu-id="42ff8-220">Die Spezifikation steuert, was Sie erhalten.</span><span class="sxs-lookup"><span data-stu-id="42ff8-220">The specification controls what you receive.</span></span> <span data-ttu-id="42ff8-221">Dieser Schritt wird häufig als Kern der Load-Methode (Schritt 3) eingebettet.</span><span class="sxs-lookup"><span data-stu-id="42ff8-221">Often, this step is embedded as the body of the Load method (step 3).</span></span> 
    
3. <span data-ttu-id="42ff8-222">Laden Sie die Spezifikation aus dem vorherigen Schritt mit der Load()- oder LoadQuery()-Methode.</span><span class="sxs-lookup"><span data-stu-id="42ff8-222">Load the retrieval specification from the previous step using the Load() or LoadQuery() method.</span></span>
    
   <span data-ttu-id="42ff8-223">Verwenden Sie für das Laden von Sammlungen und Objekten Load().</span><span class="sxs-lookup"><span data-stu-id="42ff8-223">For loading collections and objects, use Load().</span></span> <span data-ttu-id="42ff8-224">Verwenden Sie für Abfragen mit Klauseln wie "where" und "group" LoadQuery().</span><span class="sxs-lookup"><span data-stu-id="42ff8-224">For queries with clauses such as "where" and "group", use LoadQuery().</span></span> 
    
4. <span data-ttu-id="42ff8-225">Führen Sie die Anforderung mit der ExecuteQuery()-Methode aus.</span><span class="sxs-lookup"><span data-stu-id="42ff8-225">Execute the request using the ExecuteQuery() method.</span></span>
    
   <span data-ttu-id="42ff8-226">Die ExecuteQuery()-Methode benachrichtigt den Host, dass die Abfrage oder Abfragen ausgeführt werden können.</span><span class="sxs-lookup"><span data-stu-id="42ff8-226">The ExecuteQuery() method notifies the host that the query or queries are ready to execute.</span></span> <span data-ttu-id="42ff8-227">Sobald der Host die Benachrichtigung erhalten hat, führt er die Abfragen aus und sendet die Ergebnisse an den Client.</span><span class="sxs-lookup"><span data-stu-id="42ff8-227">Once the host receives notification, it executes the queries and sends the results to the client.</span></span> 
    
<span data-ttu-id="42ff8-228">Sobald die Informationen beim Client eingetroffen sind, kann die Anwendung diese verwenden.</span><span class="sxs-lookup"><span data-stu-id="42ff8-228">With the information at the client, the application can use it.</span></span> <span data-ttu-id="42ff8-229">Im folgenden Codefragment werden die veröffentlichten Projekte durchlaufen und werden die ID und der Name für jedes der auf dem Host veröffentlichten Projekte ausgegeben.</span><span class="sxs-lookup"><span data-stu-id="42ff8-229">The following code fragment cycles through the published projects and prints the Id and Name for each published project on the host.</span></span>
  
```cs
// Get the list of projects in Project Web App.
var projects = projContext.Projects;
projContext.Load(projects);
projcontext.ExecuteQuery();
foreach (PublishedProject pubProj in projContext.Projects)
{
    Console.WriteLine("\n{0}. {1}   {2} \t{3} \n", j++, pubProj.Id, pubProj.Name, pubProj.CreatedDate);
}

```

<span data-ttu-id="42ff8-230">Ausgabe:</span><span class="sxs-lookup"><span data-stu-id="42ff8-230">Output</span></span>
  
```cs
Published Project count:2
1. be80a848-b2ef-e511-80f4-00155dc84e01   A second Project     3/21/2016 10:14:40 PM
2. 9d730a1a-60ed-e511-80f6-00155dc87d01   Ent_Proj_1   3/18/2016 11:21:14 PM

```

### <a name="make-a-request"></a><span data-ttu-id="42ff8-231">Stellen einer Anforderung</span><span class="sxs-lookup"><span data-stu-id="42ff8-231">Make a second GET request.</span></span>

<span data-ttu-id="42ff8-232">Über Verwenden der Aktionen aus dem vorherigen Codefragment ruft die Anwendung die Liste der Projekte im angegebenen Konto auf der hostenden Website ab.</span><span class="sxs-lookup"><span data-stu-id="42ff8-232">Using the actions from the previous code fragment, the application retrieves the list of projects in the specified account on the hosting site.</span></span> 
  
1. <span data-ttu-id="42ff8-233">Die Projektkontext wird für die aufzulistenden Projekte angegeben.</span><span class="sxs-lookup"><span data-stu-id="42ff8-233">The ProjectContext is specified for the projects to list.</span></span> 
    
   ```cs
    var projects = projContext.Projects;
   ```

2. <span data-ttu-id="42ff8-234">Geben Sie das abzurufende Element an.</span><span class="sxs-lookup"><span data-stu-id="42ff8-234">Specify the item to retrieve.</span></span> 
    
   ```cs
    projContext.Load(projects);
   ```

   <span data-ttu-id="42ff8-235">Weil nur die Sammlung angegeben ist, ruft der Server die Projektsammlung ab, wobei jedes Projekt mit den Werten für den Standardsatz der Eigenschaften aufgefüllt wird.</span><span class="sxs-lookup"><span data-stu-id="42ff8-235">By only stating the collection, the server retrieves the project collection, populating each project with values for the default set of properties.</span></span> <span data-ttu-id="42ff8-236">Zugreifen auf Eigenschaften, die zum Standardeigenschaftensatz gehören, bringt erfolgreiche Ergebnisse.</span><span class="sxs-lookup"><span data-stu-id="42ff8-236">Accessing properties that are part of the default property set gives successful results.</span></span> <span data-ttu-id="42ff8-237">Zugreifen auf Eigenschaften, die nicht zum Standardeigenschaftensatz gehören, führt zu einer "Nicht initialisiert"-Ausnahme.</span><span class="sxs-lookup"><span data-stu-id="42ff8-237">Accessing properties that are not part of the default set results in a "Not initialized" exception.</span></span>
    
3. <span data-ttu-id="42ff8-238">Laden Sie die Anforderung (projContext.Load).</span><span class="sxs-lookup"><span data-stu-id="42ff8-238">Load the request (projContext.Load).</span></span>
    
   <span data-ttu-id="42ff8-239">Dies gehört zum vorherigen Schritt.</span><span class="sxs-lookup"><span data-stu-id="42ff8-239">This is part of the previous step.</span></span>
    
4. <span data-ttu-id="42ff8-240">Führen Sie die Abfrage aus (ExecuteQuery).</span><span class="sxs-lookup"><span data-stu-id="42ff8-240">Execute the query.</span></span> 
    
   ```cs
    projContext.ExecuteQuery();
   ```

### <a name="retrieve-high-level-project-information"></a><span data-ttu-id="42ff8-241">Abrufen von allgemeinen Projektinformationen</span><span class="sxs-lookup"><span data-stu-id="42ff8-241">Retrieve high-level project information</span></span>

<span data-ttu-id="42ff8-242">Eigenschaften, die keine Standardeigenschaften sind, müssen in der Anforderung an den Server angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="42ff8-242">Properties that are not default properties must be specified in the request to the server.</span></span> <span data-ttu-id="42ff8-243">Im nächsten Codefragment wird der Kontext der Projektesammlung so wie im vorherigen Beispiel geladen.</span><span class="sxs-lookup"><span data-stu-id="42ff8-243">The next code fragment loads the projects collection context as in the previous example.</span></span> <span data-ttu-id="42ff8-244">Anschließend werden in der Spezifikation Nicht-Standardeigenschaften angefordert, die im Ergebnis enthalten sein sollen.</span><span class="sxs-lookup"><span data-stu-id="42ff8-244">Then, the specification requests additional non-default properties to include in the result.</span></span> 
  
```cs
var projects = projContext.Projects;
projContext.Load(projects,
    ps => ps.IncludeWithDefaultProperties(
        p => p.StartDate, p => p.Phase, p => p.Stage));
projContext.ExecuteQuery();

```

<span data-ttu-id="42ff8-245">In der Load-Anweisung wird der Kontext der Projektesammlung angegeben und werden das Startdatum (StartDate), die Phase und die Stufe (Stage) hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="42ff8-245">The load statement specifies the projects collection context, and adds the StartDate, Phase, and Stage to the query result.</span></span> <span data-ttu-id="42ff8-246">Die zusätzlichen Eigenschaften skalar, Objekte oder Sammlungen sein.</span><span class="sxs-lookup"><span data-stu-id="42ff8-246">The additional properties can be scalar, objects, or collections.</span></span> <span data-ttu-id="42ff8-247">Auf skalare Elemente kann direkt zugegriffen werden.</span><span class="sxs-lookup"><span data-stu-id="42ff8-247">Scalar items can be accessed directly.</span></span> <span data-ttu-id="42ff8-248">Objekte und Sammlungen erfordern zusätzliche Verarbeitungsschritte, wie im folgenden Codefragment.</span><span class="sxs-lookup"><span data-stu-id="42ff8-248">Objects and collections require additional processing, as in the following code fragment.</span></span>
  
```cs
// Using the previous definition and Load statement …
projContext.ExecuteQuery();
foreach (PublishedProject pubProj in projContext.Projects)
{
Console.WriteLine("\n\t{0}. \t{1} \n\t{2} \n\t{3} \n", j++, pubProj.Id, pubProj.Name,
    pubProj.CreatedDate);
             // The following statement generates an exception about the object 
             // reference not being set to an instance on the server. 
             // Console.WriteLine("\tCurrent Phase:\t{0}", pubProj.Phase.Name);
             // Phase and Stage are not published with the rest of the data. Need to pull these objects from the server.
             Phase oPhase = pubProj.Phase;
             projContext.Load(oPhase);
             projContext.ExecuteQuery();
             //if-else fails because the else case fails with "Microsoft.SharePoint.Client.ServerObjectNullReferenceException".
             //if (oPhase.ServerObjectIsNull != null)
             //Using try-catch instead
             try
             {
                  Console.WriteLine("\tCurrent Phase:\t{0}", oPhase.Name);
             }
             
             catch
             {
                  Console.WriteLine("\tCurrent Phase:\t Not available");
             }
             
             Stage oStage = pubProj.Stage;
             projContext.Load(oStage);
             projContext.ExecuteQuery();
             //Again, not using if-else combination for the same reason as above.
             try
             {
                  Console.WriteLine("\tCurrent Stage:\t{0}", oStage.Name);
             }
             
             catch
             {
                  Console.WriteLine("\tCurrent Stage:\t Not available");
    }

```

<span data-ttu-id="42ff8-249">Ausgabe für die ersten drei Projekte:</span><span class="sxs-lookup"><span data-stu-id="42ff8-249">Output of the first three projects:</span></span>
  
```cs
Project counts:31
1. Project ID:  957d5fcd-5cbf-e111-9f1e-00155d022681
        Name:           Acquisition Target Analysis
        CreatedDate:            3/22/2016 5:14:34 PM
        Current Phase:  3. Plan
        Current Stage:  6. Plan
2. Project ID:  16905202-5fbf-e111-9f1e-00155d022681
        Name:           Apparel ERP Upgrade
        CreatedDate:            3/22/2016 5:36:40 PM
        Current Phase:  3. Plan
        Current Stage:  6. Plan
3. Project ID:  dce23152-63bf-e111-9f1e-00155d022681
        Name:           Audit Tracking Solution
        CreatedDate:            3/22/2016 5:02:24 PM
        Current Phase:  2. Select
        Current Stage:  4. Select Gate

```

### <a name="retrieve-all-tasks-in-a-project"></a><span data-ttu-id="42ff8-250">Abrufen aller Aufgaben in einem Projekt</span><span class="sxs-lookup"><span data-stu-id="42ff8-250">Retrieve all tasks in a project</span></span>

<span data-ttu-id="42ff8-251">Jedes Projekt hat viele Aufgaben.</span><span class="sxs-lookup"><span data-stu-id="42ff8-251">Each project has many tasks.</span></span> <span data-ttu-id="42ff8-252">Somit besteht das Abrufen der Aufgaben für ein einzelnes Projekt aus folgenden Schritten:</span><span class="sxs-lookup"><span data-stu-id="42ff8-252">So, pulling the tasks for a single project consists of the following:</span></span>
  
1. <span data-ttu-id="42ff8-253">Richten Sie den Kontext der Projektesammlung ein.</span><span class="sxs-lookup"><span data-stu-id="42ff8-253">Establish the context of the projects collection.</span></span>
    
   ```cs
    var projects = projContext.Projects;
   ```

2. <span data-ttu-id="42ff8-254">Rufen Sie die Projektinformationen ab, einschließlich der Aufgabeneigenschaften.</span><span class="sxs-lookup"><span data-stu-id="42ff8-254">Retrieve the project information, including the Task properties.</span></span>
    
   ```cs
    projContext.Load(projects);
    ProjContext.ExecuteQuery();
    foreach (PublishedProject pubProj in projContext.Projects){
    
   ```

    <span data-ttu-id="42ff8-255">Beachten Sie, dass die Anwendung für veröffentlichte Projekte vorgesehen ist.</span><span class="sxs-lookup"><span data-stu-id="42ff8-255">Note that the application is addressing published projects.</span></span> <span data-ttu-id="42ff8-256">Der Kontext für das aktuelle veröffentlichte Projekt ist "pubProj".</span><span class="sxs-lookup"><span data-stu-id="42ff8-256">The context for the current published project is pubProj.</span></span> 
    
3. <span data-ttu-id="42ff8-257">Richten Sie den Kontext für die Aufgabensammlung (Tasks) ein.</span><span class="sxs-lookup"><span data-stu-id="42ff8-257">Establish the context for the Tasks collection.</span></span>
    
   ```cs
    PublishedTaskCollection collTask = pubProj.Tasks;
   ```

   <span data-ttu-id="42ff8-258">Die `pubProj.Tasks`-Eigenschaft verweist auf die Aufgaben des aktuellen veröffentlichten Projekts.</span><span class="sxs-lookup"><span data-stu-id="42ff8-258">The `pubProj.Tasks` property references the tasks of the current published project.</span></span> 
    
4. <span data-ttu-id="42ff8-259">Laden Sie die Spezifikation zum Abrufen der Aufgabensammlung (Task collection), einschließlich der entsprechenden Nicht-Standardeigenschaften.</span><span class="sxs-lookup"><span data-stu-id="42ff8-259">Load the specification to retrieve Task collection, including the appropriate non-default properties.</span></span>
    
   ```cs
    projContext.Load(collTask,
        tsk => tsk.IncludeWithDefaultProperties(
            t => t.Id, t => t.Name, t => t.Start,
            t => t.ScheduledStart, t => t.Completion));
    
   ```

5. <span data-ttu-id="42ff8-260">Führen Sie die Abfrage aus, um die Aufgabensammlung mit den entsprechenden Eigenschaften abzurufen.</span><span class="sxs-lookup"><span data-stu-id="42ff8-260">Execute the query to retrieve the Task collection with the appropriate properties.</span></span>
    
   ```cs
    projContext.ExecuteQuery();
   ```

<span data-ttu-id="42ff8-261">Die Informationen liegen nun lokal vor.</span><span class="sxs-lookup"><span data-stu-id="42ff8-261">The information is now local.</span></span> <span data-ttu-id="42ff8-262">Im folgenden Codefragment wird die veröffentlichte Aufgabensammlung verarbeitet, indem die Informationen in die Konsole geschrieben werden.</span><span class="sxs-lookup"><span data-stu-id="42ff8-262">The following code fragment processes the published tasks collection by writing the information to the console.</span></span>
  
```cs
    Console.WriteLine("Task collection count: {0}", collTask.Count.ToString());
    if (collTask.Count > 0)
    {
        int k = 1;    //Task counter.
        foreach (PublishedTask t in collTask)
        {
            Console.WriteLine("{0}. Id:{1} \tName:{2}", k++, t.Id, t.Name);
            Console.WriteLine("\t ScheduledStart:{0} \tStart:{1} \tCompletion:{2}", k, t.ScheduledStart, t.Start, t.Completion);
        }
    }

```

<span data-ttu-id="42ff8-263">Ausgabe der Aufgaben für ein Projekt:</span><span class="sxs-lookup"><span data-stu-id="42ff8-263">Output of tasks for one project:</span></span>
  
```cs
Task collection count: 5
1. Id:256fa850-b2ef-e511-80f6-00155dc87d01      Name:Load software onto computer
         ScheduledStart:2       Start:4/4/2016 8:00:00 AM       Completion:4/4/2016 8:00:00 AM
2. Id:266fa850-b2ef-e511-80f6-00155dc87d01      Name:Locate and load Project Online SDK
         ScheduledStart:3       Start:4/5/2016 8:00:00 AM       Completion:4/5/2016 8:00:00 AM
3. Id:276fa850-b2ef-e511-80f6-00155dc87d01      Name:Locate and load SP SDK
         ScheduledStart:4       Start:4/5/2016 1:00:00 PM       Completion:4/5/2016 1:00:00 PM
4. Id:286fa850-b2ef-e511-80f6-00155dc87d01      Name:Build app that accesses Proj Online
         ScheduledStart:5       Start:4/6/2016 8:00:00 AM       Completion:4/6/2016 8:00:00 AM
5. Id:296fa850-b2ef-e511-80f6-00155dc87d01      Name:Build app that accesses task assignments
         ScheduledStart:6       Start:4/7/2016 8:00:00 AM       Completion:4/7/2016 8:00:00 AM

```

### <a name="access-information-at-multiple-levels"></a><span data-ttu-id="42ff8-264">Zugreifen auf Informationen auf mehreren Ebenen</span><span class="sxs-lookup"><span data-stu-id="42ff8-264">Access information at multiple levels</span></span>

<span data-ttu-id="42ff8-265">Für jede Aufgabe können eine oder mehrere Personen (auch als</span><span class="sxs-lookup"><span data-stu-id="42ff8-265">Each task can have one or more persons (a.k.a.</span></span> <span data-ttu-id="42ff8-266">Ressourcen bezeichnet) an der Erledigung der Aufgabe beteiligt sein.</span><span class="sxs-lookup"><span data-stu-id="42ff8-266">resource) contributing toward its completion.</span></span> <span data-ttu-id="42ff8-267">Die Zuweisungen- (Assignments) und die Ressourcensammlung enthalten diese Informationen für jede Aufgabe.</span><span class="sxs-lookup"><span data-stu-id="42ff8-267">The Assignments and Resources collections contain this information for each task.</span></span> 
  
<span data-ttu-id="42ff8-268">Die Verarbeitung besteht aus den folgenden Schritten:</span><span class="sxs-lookup"><span data-stu-id="42ff8-268">The crawl and content processing architecture consists of the following:</span></span>
  
1. <span data-ttu-id="42ff8-269">Rufen Sie einen Kontext für die Projektaufgabe ab.</span><span class="sxs-lookup"><span data-stu-id="42ff8-269">Obtaining a context for the project task.</span></span>
    
2. <span data-ttu-id="42ff8-270">Erstellen Sie eine Anforderung, und laden Sie die Anforderung für die Zuweisungen, die mit der Aufgabe verknüpft sind.</span><span class="sxs-lookup"><span data-stu-id="42ff8-270">Build a request and load the request for the assignments tied to the task.</span></span> 
    
3. <span data-ttu-id="42ff8-271">Führen Sie die Abfrage für die Zuweisungen aus.</span><span class="sxs-lookup"><span data-stu-id="42ff8-271">Execute the query for the assignments.</span></span>
    
4. <span data-ttu-id="42ff8-272">Erstellen Sie eine Anforderung, und laden Sie die Anforderung für die Ressource, die mit einer einzelnen Zuweisung verknüpft ist.</span><span class="sxs-lookup"><span data-stu-id="42ff8-272">Build a request and load the request for the resource associated with an individual assignment.</span></span> 
    
5. <span data-ttu-id="42ff8-273">Führen Sie die Abfrage für die Ressource aus.</span><span class="sxs-lookup"><span data-stu-id="42ff8-273">Execute the query for the resource.</span></span>
    
> [!NOTE] 
> - <span data-ttu-id="42ff8-274">Die Zuweisungensammlung wird explizit in den Informationen vom Server angefordert, weil sie keine Standardeigenschaft der Aufgabensammlung ist.</span><span class="sxs-lookup"><span data-stu-id="42ff8-274">The Assignments collection is explicitly requested in the information from the server because it is not a default property of the Tasks collection.</span></span> <span data-ttu-id="42ff8-275">Als Sammlung wird anschließend eine Abfrage ausgeführt, um die Sammlung vom Server abzurufen.</span><span class="sxs-lookup"><span data-stu-id="42ff8-275">As a collection, a subsequent query is made to pull the collection from the server.</span></span> 
> - <span data-ttu-id="42ff8-276">Die Ressource ist ein Objekt.</span><span class="sxs-lookup"><span data-stu-id="42ff8-276">The Resource is an object.</span></span> <span data-ttu-id="42ff8-277">Die Abfrage für eine Zuweisung enthält den Namen der Ressource, die mit der Zuweisung verknüpft ist.</span><span class="sxs-lookup"><span data-stu-id="42ff8-277">The query for an assignment includes the resource name associated with the assignment.</span></span>
    
```cs
PublishedTaskCollection collTask = pubProj.Tasks;
    projContext.Load(collTask,
        tsk => tsk.IncludeWithDefaultProperties(
            t => t.Id, t => t.Name, 
            t => t.Assignments));
    projContext.Load(collTask);
    projContext.ExecuteQuery();
    Console.WriteLine("Task collection count: {0}", collTask.Count.ToString());
    if (collTask.Count > 0)
    {
        int k = 1;    //Task counter.
        //Processing task list for current project
        foreach (PublishedTask t in collTask)
        {
            Console.WriteLine("{0}. Id:{1} \tName:{2}", k, t.Id, t.Name);
            k++;
            //Define and retrieve Assignments for current task
            PublishedAssignmentCollection collAssgns = t.Assignments;
            projContext.Load(collAssgns);
            projContext.ExecuteQuery();
            Console.WriteLine("    Assignment collection count: {0}", collAssgns.Count);
            if (collAssgns.Count > 0)
            {
                //Output string for resources assigned to task
                StringBuilder output = new StringBuilder();
                output.AppendFormat("\t Assignments: ");
                foreach (PublishedAssignment a in collAssgns)
                {
                    //Define and retrieve resource name for current assignment 
                    //(an object)
                    projContext.Load(a,
                        b => b.Resource.Name);
                    projContext.ExecuteQuery();
                    output.AppendFormat("{0}, ", a.Resource.Name);
                }
                Console.WriteLine(output);
            }
            else
            {
                Console.WriteLine("\t Assignments: None");
            }
        }
    }   // endif

```

<span data-ttu-id="42ff8-278">Ausgabe für Aufgaben 52, 75 und 76 eines Projekts:</span><span class="sxs-lookup"><span data-stu-id="42ff8-278">Output for tasks 52, 75, and 76 of a project:</span></span>
  
```cs
52. Id:2c729e96-54f0-e511-80c6-000d3a33235f     Name:Develop training materials
    Assignment collection count: 1
         Assignments: Robert Lyon,
75. Id:43729e96-54f0-e511-80c6-000d3a33235f     Name:Determine final deployment strategy
    Assignment collection count: 0
         Assignments: None
76. Id:44729e96-54f0-e511-80c6-000d3a33235f     Name:Develop deployment methodology
    Assignment collection count: 4
         Assignments: Molly Dempsey, Sara Davis, Shammi Mohamed, Zainal Arifin, 

```

### <a name="access-custom-enterprise-level-fields"></a><span data-ttu-id="42ff8-279">Zugreifen auf benutzerdefinierte Felder auf Unternehmensebene</span><span class="sxs-lookup"><span data-stu-id="42ff8-279">Access custom enterprise-level fields</span></span>

<span data-ttu-id="42ff8-280">Für Project Online gibt es benutzerdefinierte Felder.</span><span class="sxs-lookup"><span data-stu-id="42ff8-280">Custom fields exist for Project Online.</span></span> <span data-ttu-id="42ff8-281">Diese Felder sind Felder auf Unternehmensebene, die mit einzelnen Projekten verknüpft werden können.</span><span class="sxs-lookup"><span data-stu-id="42ff8-281">These are enterprise-level fields that can be associated with individual project.</span></span> <span data-ttu-id="42ff8-282">In diesem Abschnitt ist beschrieben, wie auf diese Felder zugegriffen wird.</span><span class="sxs-lookup"><span data-stu-id="42ff8-282">This section describes how to access these fields.</span></span> 
  
<span data-ttu-id="42ff8-283">Benutzerdefinierte Felder sind nicht in den Standardeigenschaften enthalten, die mit einem Projekt verknüpft sind.</span><span class="sxs-lookup"><span data-stu-id="42ff8-283">Custom fields are not included in the default set of properties associated with a project.</span></span> <span data-ttu-id="42ff8-284">Daher müssen sie in der Abrufspezifikation explizit angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="42ff8-284">So, they need explicit identification in the retrieval specification.</span></span> <span data-ttu-id="42ff8-285">Die grundsätzliche Sicht auf den Vorgang besteht aus den folgenden Schritten:</span><span class="sxs-lookup"><span data-stu-id="42ff8-285">The high-level view of the process consists of the following items:</span></span>
  
1. <span data-ttu-id="42ff8-286">Erstellen Sie einen Tunnel zum benutzerdefinierten Feld über dessen allgemeinen Namen.</span><span class="sxs-lookup"><span data-stu-id="42ff8-286">Tunnel to the custom field using its common name.</span></span>
    
2. <span data-ttu-id="42ff8-287">Rufen Sie den internen Namen des benutzerdefinierten Felds ab.</span><span class="sxs-lookup"><span data-stu-id="42ff8-287">Retrieve the internal name of the custom field.</span></span>
    
3. <span data-ttu-id="42ff8-288">Kehren Sie zum globalen Kontext zurück, und fragen Sie das System mit dem internen Namen des benutzerdefinierten Felds ab.</span><span class="sxs-lookup"><span data-stu-id="42ff8-288">Return to the global context and query the system using the internal name of the custom field.</span></span>
    
#### <a name="tunnel-to-the-custom-field-retrieve-its-internal-name-and-used-it-to-query-the-system"></a><span data-ttu-id="42ff8-289">Erstellen eines Tunnels zum benutzerdefinierten Feld, Abrufen dessen internen Namens und Abfragen des Systems mit dem Namen</span><span class="sxs-lookup"><span data-stu-id="42ff8-289">Tunnel to the custom field, retrieve its internal name, and used it to query the system</span></span>

<span data-ttu-id="42ff8-290">In dieser Aufgabe ist ein Abruf angegeben, in dem eine Nicht-Standardeigenschaft mit einem zusätzlichen Detail verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="42ff8-290">This task specifies a retrieval that uses a non-default property with one added detail.</span></span>
  
1. <span data-ttu-id="42ff8-291">Beginnen Sie durch Verwenden Projektekontexts, wie dies am Anfang dieses Artikels beschrieben ist.</span><span class="sxs-lookup"><span data-stu-id="42ff8-291">Begin by using the projects context, as described at the beginning of this article.</span></span>
    
   ```cs
    // Get the list of published projects in Project Web App.
    var projects = projContext.Projects;
    
   ```

2. <span data-ttu-id="42ff8-292">Fügen Sie zwei Elemente zur Abrufanforderung der Projektesammlung hinzu, zusätzlich zu allen anderen Nicht-Standardeigenschaften, die abgerufen werden sollen:</span><span class="sxs-lookup"><span data-stu-id="42ff8-292">Add two items to the projects collection retrieval request in addition to any other non-default properties to retrieve:</span></span>
    
   ```cs
    projContext.Load(projects,
        ps => ps.IncludeWithDefaultProperties(
            p => p.Phase, p => p.Stage,                  // Other nondefault properties
            p => p.IncludeCustomFields,                  // Gets PublishedProject object 
                                                        // that contains custom fields
            p => p.IncludeCustomFields.CustomFields));   // Populates the custom fields
                    projContext.ExecuteQuery();
    
   ```

   <span data-ttu-id="42ff8-293">Die `p => p.IncludeCustomFields`-Klausel kennzeichnet die Notwendigkeit, ein Projektobjekt zu verwenden, das benutzerdefinierte Felder unterstützt.</span><span class="sxs-lookup"><span data-stu-id="42ff8-293">The  `p => p.IncludeCustomFields` clause identifies the need to use a project object that supports custom fields.</span></span> 
    
   <span data-ttu-id="42ff8-294">In der `p => p.IncludeCustomFields.CustomFields`-Klausel wird die Einbeziehung von Daten aus benutzerdefinierten Feldern in das Abfrageergebnis angefordert.</span><span class="sxs-lookup"><span data-stu-id="42ff8-294">The  `p => p.IncludeCustomFields.CustomFields` clause requests the inclusion of custom field data in the query result.</span></span> <span data-ttu-id="42ff8-295">Diese Informationen werden verwendet, nachdem der interne Name des benutzerdefinierten Felds abgerufen wurde.</span><span class="sxs-lookup"><span data-stu-id="42ff8-295">This information is used after the custom field internal name is retrieved.</span></span> 
    
3. <span data-ttu-id="42ff8-296">Laden Sie die Anforderung.</span><span class="sxs-lookup"><span data-stu-id="42ff8-296">Load the request.</span></span>
    
   <span data-ttu-id="42ff8-297">Dies gehört zum vorherigen Schritt.</span><span class="sxs-lookup"><span data-stu-id="42ff8-297">This is part of the previous step.</span></span>
    
4. <span data-ttu-id="42ff8-298">Führen Sie die Abfrage aus.</span><span class="sxs-lookup"><span data-stu-id="42ff8-298">Execute the query.</span></span>
    
   ```cs
    projContext.ExecuteQuery()
   ```

5. <span data-ttu-id="42ff8-299">Mit diesen Informationen erstellen Sie auf dem Client eine Anforderung, um die benutzerdefinierten Felder abzurufen, die mit dem aktuellen Projekt verknüpft sind.</span><span class="sxs-lookup"><span data-stu-id="42ff8-299">With this information on the client, build a request to retrieve the custom fields associated with the current project.</span></span>
    
   ```cs
    foreach (PublishedProject pubProj in projContext.Projects)
    {
        //Console.WriteLine("\n\t{0}. \t{1} \n\t\t{2} \n\t\t{3} \n", 
                j++, pubProj.Id, pubProj.Name, pubProj.CreatedDate);
        CustomFieldCollection collCustF = pubProj.CustomFields;
                        
        projContext.Load(collCustF);
        projContext.ExecuteQuery();
    
   ```

6. <span data-ttu-id="42ff8-300">Suchen Sie das entsprechende benutzerdefinierte Feld, und rufen Sie den internen Namen des Felds ab.</span><span class="sxs-lookup"><span data-stu-id="42ff8-300">Locate the appropriate custom field and retrieve the internal name of the field.</span></span> 
    
   ```cs
        foreach (CustomField oCF in collCustF)
        {
            if (oCF.Name == "Project Health")
            {
                Console.WriteLine("Name: {0}", oCF.Name);
                Console.WriteLine("InternalName: {0}", oCF.InternalName);
    
   ```

   <span data-ttu-id="42ff8-301">Der interne Name des benutzerdefinierten Felds wird abgerufen.</span><span class="sxs-lookup"><span data-stu-id="42ff8-301">The internal name of the custom field is retrieved.</span></span> <span data-ttu-id="42ff8-302">Die grundsätzlichen Schritte 1 und 2 sind jetzt abgeschlossen.</span><span class="sxs-lookup"><span data-stu-id="42ff8-302">High-level items 1 and 2 are now complete.</span></span>
    
7. <span data-ttu-id="42ff8-303">Kehren Sie zum Projektkontext zurück, und rufen Sie den Wert des benutzerdefinierten Felds ab.</span><span class="sxs-lookup"><span data-stu-id="42ff8-303">Return to the project context and retrieve the value of the custom field.</span></span>
    
   ```cs
    Console.WriteLine("Value: {0}", 
        pubProj.IncludeCustomFields.FieldValues[oCF.InternalName]);
    
   ```

   > [!NOTE]
   > <span data-ttu-id="42ff8-304">Der Wert des benutzerdefinierten Felds wird abgerufen, indem der interne Name als Index verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="42ff8-304">The value of the custom field is retrieved using the internal name as an index.</span></span> 
  
<span data-ttu-id="42ff8-305">Die Ausgabe für drei Projekte, bestehend aus Projekt-ID, Projektname, Name des benutzerdefinierten Felds, interner Name des benutzerdefinierten Felds und Wert des benutzerdefinierten Felds.</span><span class="sxs-lookup"><span data-stu-id="42ff8-305">Output of three projects consisting of project ID, project Name, custom field name, custom field internal name, and custom field value.</span></span>
  
```cs
Project counts:31
1. Project ID:  957d5fcd-5cbf-e111-9f1e-00155d022681
        Name:           Acquisition Target Analysis
Name: Project Health
InternalName: Custom_745de6dfcfb4e11195dc00155d02c97f
Value: Green
2. Project ID:  16905202-5fbf-e111-9f1e-00155d022681
        Name:           Apparel ERP Upgrade
Name: Project Health
InternalName: Custom_745de6dfcfb4e11195dc00155d02c97f
Value: Green
3. Project ID:  dce23152-63bf-e111-9f1e-00155d022681
        Name:           Audit Tracking Solution
Name: Project Health
InternalName: Custom_745de6dfcfb4e11195dc00155d02c97f
Value: Red

```

## <a name="see-also"></a><span data-ttu-id="42ff8-306">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="42ff8-306">See also</span></span>

<span data-ttu-id="42ff8-307">Dokumentation und Beispiele zu Project Online und Anwendungsentwicklung mit CSOM finden Sie im [Project-Entwicklungsportal](https://developer.microsoft.com/de-DE/project).</span><span class="sxs-lookup"><span data-stu-id="42ff8-307">For documentation and samples related to Project Online and application development using CSOM, see the [Project Development Portal](https://developer.microsoft.com/de-DE/project).</span></span>
    

