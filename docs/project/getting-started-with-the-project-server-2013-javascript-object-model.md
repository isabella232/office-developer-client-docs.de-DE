---
title: Erste Schritte mit dem Project Server 2013-JavaScript-Objektmodell
manager: soliver
ms.date: 08/10/2016
ms.audience: Developer
localization_priority: Normal
ms.assetid: 30dc3194-7480-4e7c-b731-4a171d652ee0
description: In Project Server 2013 kann das JavaScript-Objektmodell in Project Online, mobilen und lokalen Entwicklungen verwendet werden. In diesem Thema wird eine kurze Übersicht über das JavaScript-Objektmodell und anschließend das Erstellen einer Anwendungsseite beschrieben, die Projekte mithilfe des JavaScript-Objektmodells abruft und durch diese durch iteriert.
ms.openlocfilehash: ec8a10e987276807dc4648bd8948b2285f76fd37
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32360473"
---
# <a name="getting-started-with-the-project-server-2013-javascript-object-model"></a><span data-ttu-id="166c6-104">Erste Schritte mit dem Project Server 2013-JavaScript-Objektmodell</span><span class="sxs-lookup"><span data-stu-id="166c6-104">Getting started with the Project Server 2013 JavaScript object model</span></span>

<span data-ttu-id="166c6-105">In Project Server 2013 kann das JavaScript-Objektmodell in Project Online, mobilen und lokalen Entwicklungen verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="166c6-105">In Project Server 2013, the JavaScript object model can be used in Project Online, mobile, and on-premise development.</span></span> <span data-ttu-id="166c6-106">In diesem Thema wird eine kurze Übersicht über das JavaScript-Objektmodell und anschließend das Erstellen einer Anwendungsseite beschrieben, die Projekte mithilfe des JavaScript-Objektmodells abruft und durch diese durch iteriert.</span><span class="sxs-lookup"><span data-stu-id="166c6-106">This topic provides a brief overview of the JavaScript object model and then describes how to create an application page that retrieves and iterates through projects by using the JavaScript object model.</span></span>
  
## <a name="using-the-project-server-javascript-object-model"></a><span data-ttu-id="166c6-107">Verwenden des Project Server-JavaScript-Objektmodells</span><span class="sxs-lookup"><span data-stu-id="166c6-107">Using the Project Server JavaScript object model</span></span>
<span data-ttu-id="166c6-108"><a name="pj15_GetStartedJSOM_UseJSOM"> </a></span><span class="sxs-lookup"><span data-stu-id="166c6-108"><a name="pj15_GetStartedJSOM_UseJSOM"> </a></span></span>

<span data-ttu-id="166c6-109">Die Verwendung des JavaScript-Objektmodells ist eine hervorragende Möglichkeit, eine App zu erstellen, die clientseitig ausgeführt wird (im Gegensatz zu verwalteten Clientcode, der remote ausgeführt werden muss).</span><span class="sxs-lookup"><span data-stu-id="166c6-109">Using the JavaScript object model is a great way to create an app that runs client-side (as opposed to managed client code which needs to run remotely).</span></span> <span data-ttu-id="166c6-110">Apps können das JavaScript-Objektmodell verwenden, um Objekte abzurufen oder zu ändern, indem asynchrone Aufrufe an den Server gesendet werden.</span><span class="sxs-lookup"><span data-stu-id="166c6-110">Apps can use the JavaScript object model to retrieve or change objects by sending asynchronous calls to the server.</span></span> <span data-ttu-id="166c6-111">Apps, die das JavaScript-Objektmodell verwenden, werden in der Regel als benutzerdefinierte SharePoint-Add-Ins, Anwendungsseiten und Webparts.</span><span class="sxs-lookup"><span data-stu-id="166c6-111">Apps that use the JavaScript object model are typically deployed as custom SharePoint Add-ins, application pages, and Web Parts.</span></span> <span data-ttu-id="166c6-112">Weitere Informationen finden Sie unter "Typen von SharePoint-Komponenten, die in einer App für SharePoint enthalten sein können" in [Hostwebs, Add-In-Webs und SharePoint-Komponenten in SharePoint 2013](https://msdn.microsoft.com/library/b791cdf5-8aa2-47fa-bc4c-aee437354759%28Office.15%29.aspx).</span><span class="sxs-lookup"><span data-stu-id="166c6-112">For more information, see "Types of SharePoint components that can be in an app for SharePoint" in [Host webs, add-in webs, and SharePoint components in SharePoint 2013](https://msdn.microsoft.com/library/b791cdf5-8aa2-47fa-bc4c-aee437354759%28Office.15%29.aspx).</span></span>
  
<span data-ttu-id="166c6-113">Das JavaScript-Objektmodell implementiert die Hauptfunktionalität von Project Server 2013, aber das JavaScript-Objektmodell und das Serverobjektmodell haben keine 1:1-Parität.</span><span class="sxs-lookup"><span data-stu-id="166c6-113">The JavaScript object model implements the main functionality of Project Server 2013, but the JavaScript object model and the server object model do not have one-to-one parity.</span></span> <span data-ttu-id="166c6-114">Der Einstiegspunkt zum JavaScript-Objektmodell ist das **ProjectContext-Objekt,** das den Clientkontext für Project Server 2013 darstellt und Zugriff auf Serverinhalte und -funktionen bietet.</span><span class="sxs-lookup"><span data-stu-id="166c6-114">The entry point to the JavaScript object model is the **ProjectContext** object, which represents the client context for Project Server 2013 and provides access to server content and functionality.</span></span> <span data-ttu-id="166c6-115">Das JavaScript-Objektmodell für Project Server 2013 ist in der PS.js-Datei definiert, die sich im Standardpfad auf dem  `%ProgramFiles%\Common Files\Microsoft Shared\Web Server Extensions\15\TEMPLATE\LAYOUTS` Anwendungsserver befindet.</span><span class="sxs-lookup"><span data-stu-id="166c6-115">The JavaScript object model for Project Server 2013 is defined in the PS.js file, which is located in the default path  `%ProgramFiles%\Common Files\Microsoft Shared\Web Server Extensions\15\TEMPLATE\LAYOUTS` on the application server.</span></span> <span data-ttu-id="166c6-116">Project Server 2013 installiert die datei PS.Debug.js am gleichen Speicherort.</span><span class="sxs-lookup"><span data-stu-id="166c6-116">Project Server 2013 also installs the PS.Debug.js file in the same location.</span></span> <span data-ttu-id="166c6-117">PS.Debug.js ist eine nicht verifizierte Version von PS.js, die IntelliSense enthält.</span><span class="sxs-lookup"><span data-stu-id="166c6-117">PS.Debug.js is an unminified version of PS.js that provides IntelliSense information.</span></span> 
  
<span data-ttu-id="166c6-118">Das JavaScript-Objektmodell ermöglicht die Formularauthentifizierung, und alle Anforderungen werden als aktueller Benutzer authentifiziert.</span><span class="sxs-lookup"><span data-stu-id="166c6-118">The JavaScript object model allows Forms authentication, and all requests are authenticated as the current user.</span></span> <span data-ttu-id="166c6-119">Weitere Informationen zu Sicherheit und anderen Überlegungen zum Entwerfen benutzerdefinierter Apps und Lösungen finden Sie unter Authentifizierung, Autorisierung und Sicherheit [in SharePoint 2013](https://msdn.microsoft.com/library/8734790c-eb75-4d78-9604-7cc23b33b693%28Office.15%29.aspx), Wichtige Aspekte der Architektur und Entwicklungslandschaft von [SharePoint-Add-Ins](https://msdn.microsoft.com/library/ae96572b-8f06-4fd3-854f-fc312f7f2d88%28Office.15%29.aspx)und [SharePoint-Add-Ins](https://msdn.microsoft.com/library/0e9efadb-aaf2-4c0d-afd5-d6cf25c4e7a8%28Office.15%29.aspx)im Vergleich zu SharePoint-Lösungen .</span><span class="sxs-lookup"><span data-stu-id="166c6-119">For more information about security and other considerations for designing custom apps and solutions, see [Authentication, authorization, and security in SharePoint 2013](https://msdn.microsoft.com/library/8734790c-eb75-4d78-9604-7cc23b33b693%28Office.15%29.aspx), [Important aspects of the SharePoint Add-in architecture and development landscape](https://msdn.microsoft.com/library/ae96572b-8f06-4fd3-854f-fc312f7f2d88%28Office.15%29.aspx), and [SharePoint Add-ins compared with SharePoint solutions](https://msdn.microsoft.com/library/0e9efadb-aaf2-4c0d-afd5-d6cf25c4e7a8%28Office.15%29.aspx).</span></span>
  
> [!NOTE]
> <span data-ttu-id="166c6-120">Für den Remotezugriff auf Daten von einer SharePoint-Website bietet SharePoint 2013 eine domänenübergreifende Bibliothek, mit der Sie clientseitige domänenübergreifende Anrufe ausführen können.</span><span class="sxs-lookup"><span data-stu-id="166c6-120">To access data from a SharePoint site remotely, SharePoint 2013 provides a cross-domain library that enables you to make client-side cross-domain calls.</span></span> <span data-ttu-id="166c6-121">Weitere Informationen finden Sie unter [Access SharePoint 2013 data from add-ins using the cross-domain library](https://msdn.microsoft.com/library/bc37ff5c-1285-40af-98ae-01286696242d%28Office.15%29.aspx).</span><span class="sxs-lookup"><span data-stu-id="166c6-121">For more information, see [Access SharePoint 2013 data from add-ins using the cross-domain library](https://msdn.microsoft.com/library/bc37ff5c-1285-40af-98ae-01286696242d%28Office.15%29.aspx).</span></span> 
  
<span data-ttu-id="166c6-122">Viele Konzepte und Prozesse für die Verwendung des JavaScript-Objektmodells für Project Server 2013 ähneln denen in verwandten Clientobjektmodellen.</span><span class="sxs-lookup"><span data-stu-id="166c6-122">Many concepts and processes for using the JavaScript object model for Project Server 2013 resemble those in related client object models.</span></span> <span data-ttu-id="166c6-123">Weitere Informationen zum verwalteten Clientobjektmodell von Project Server 2013 finden Sie unter **Microsoft.ProjectServer.Client**.</span><span class="sxs-lookup"><span data-stu-id="166c6-123">For more information about the Project Server 2013 managed client object model, see **Microsoft.ProjectServer.Client**.</span></span> <span data-ttu-id="166c6-124">Weitere Informationen zum SharePoint 2013JavaScript-Objektmodell und zum verwalteten Clientobjektmodell finden Sie unter [Complete basic operations using JavaScript library code in SharePoint 2013](https://msdn.microsoft.com/library/29089af8-dbc0-49b7-a1a0-9e311f49c826%28Office.15%29.aspx) und Complete basic operations using [SharePoint 2013 client library code](https://msdn.microsoft.com/library/5a69c9e3-73bf-4ed5-bc19-182056bdb394%28Office.15%29.aspx).</span><span class="sxs-lookup"><span data-stu-id="166c6-124">For more information about the SharePoint 2013JavaScript object model and managed client object model, see [Complete basic operations using JavaScript library code in SharePoint 2013](https://msdn.microsoft.com/library/29089af8-dbc0-49b7-a1a0-9e311f49c826%28Office.15%29.aspx) and [Complete basic operations using SharePoint 2013 client library code](https://msdn.microsoft.com/library/5a69c9e3-73bf-4ed5-bc19-182056bdb394%28Office.15%29.aspx).</span></span>
  
## <a name="walkthrough-creating-an-application-page-that-retrieves-and-iterates-through-projects"></a><span data-ttu-id="166c6-125">Exemplarische Vorgehensweise: Erstellen einer Anwendungsseite, die Projekte abruft und durch iteriert</span><span class="sxs-lookup"><span data-stu-id="166c6-125">Walkthrough: Creating an application page that retrieves and iterates through projects</span></span>
<span data-ttu-id="166c6-126"><a name="pj15_GetStartedJSOM_UseJSOM"> </a></span><span class="sxs-lookup"><span data-stu-id="166c6-126"><a name="pj15_GetStartedJSOM_UseJSOM"> </a></span></span>

<span data-ttu-id="166c6-127">Erfahren Sie, wie Sie eine Anwendungsseite erstellen, die die ID, den Namen und das Erstellungsdatum jedes veröffentlichten Projekts auf einer Website anzeigt.</span><span class="sxs-lookup"><span data-stu-id="166c6-127">Learn how to create an application page that displays the ID, name, and created date of each published project in a site.</span></span>
  
### <a name="prerequisites-for-creating-an-application-page-that-retrieves-and-iterates-through-projects"></a><span data-ttu-id="166c6-128">Voraussetzungen für das Erstellen einer Anwendungsseite, die Projekte abruft und durch iteriert</span><span class="sxs-lookup"><span data-stu-id="166c6-128">Prerequisites for creating an application page that retrieves and iterates through projects</span></span>
<span data-ttu-id="166c6-129"><a name="pj15_GetStartedJSOM_Prereqs"> </a></span><span class="sxs-lookup"><span data-stu-id="166c6-129"><a name="pj15_GetStartedJSOM_Prereqs"> </a></span></span>

<span data-ttu-id="166c6-130">Um die in diesem Thema beschriebene Anwendungsseite zu entwickeln, müssen Sie die folgenden Produkte installieren und konfigurieren:</span><span class="sxs-lookup"><span data-stu-id="166c6-130">To develop the application page that is described in this topic, you must install and configure the following products:</span></span>
  
- <span data-ttu-id="166c6-131">SharePoint Server 2013</span><span class="sxs-lookup"><span data-stu-id="166c6-131">SharePoint Server 2013</span></span>
- <span data-ttu-id="166c6-132">Project Server 2013 mit mindestens einem veröffentlichten Projekt</span><span class="sxs-lookup"><span data-stu-id="166c6-132">Project Server 2013 with at least one published project</span></span>
- <span data-ttu-id="166c6-133">Visual Studio 2012</span><span class="sxs-lookup"><span data-stu-id="166c6-133">Visual Studio 2012</span></span>
- <span data-ttu-id="166c6-134">Office Developer Tools für Visual Studio 2012</span><span class="sxs-lookup"><span data-stu-id="166c6-134">Office Developer Tools for Visual Studio 2012</span></span>
    
<span data-ttu-id="166c6-135">Sie müssen auch über Berechtigungen zum Bereitstellen der Erweiterung in SharePoint Server 2013 und zum Abrufen von Projekten verfügen.</span><span class="sxs-lookup"><span data-stu-id="166c6-135">You must also have permissions to deploy the extension to SharePoint Server 2013 and to retrieve projects.</span></span>
  
> [!NOTE]
> <span data-ttu-id="166c6-136">In diesen Anweisungen wird davon ausgegangen, dass Sie auf dem Computer mit Project Server 2013 entwickeln.</span><span class="sxs-lookup"><span data-stu-id="166c6-136">These instructions assume that you are developing on the computer that is running Project Server 2013.</span></span> 
  
### <a name="creating-the-application-page-in-visual-studio-2012"></a><span data-ttu-id="166c6-137">Erstellen der Anwendungsseite in Visual Studio 2012</span><span class="sxs-lookup"><span data-stu-id="166c6-137">Creating the application page in Visual Studio 2012</span></span>
<span data-ttu-id="166c6-138"><a name="pj15_GetStartedJSOM_CreateVS"> </a></span><span class="sxs-lookup"><span data-stu-id="166c6-138"><a name="pj15_GetStartedJSOM_CreateVS"> </a></span></span>

<span data-ttu-id="166c6-139">In den folgenden Schritten werden ein SharePoint-Projekt und eine Anwendungsseite erstellt, die eine Tabelle und Bezeichnung enthält.</span><span class="sxs-lookup"><span data-stu-id="166c6-139">The following steps create a SharePoint project and an application page that contains a table and label.</span></span> <span data-ttu-id="166c6-140">In der Tabelle werden Informationen zu den Projekten angezeigt, und die Bezeichnung zeigt Fehlermeldungen an.</span><span class="sxs-lookup"><span data-stu-id="166c6-140">The table displays information about the projects and the label displays error messages.</span></span>
  
1. <span data-ttu-id="166c6-141">Führen Sie auf dem Computer, auf dem Project Server 2013 ausgeführt wird, Visual Studio 2012 als Administrator aus.</span><span class="sxs-lookup"><span data-stu-id="166c6-141">On the computer that is running Project Server 2013, run Visual Studio 2012 as an administrator.</span></span>
    
2. <span data-ttu-id="166c6-142">Erstellen Sie wie folgt ein leeres SharePoint 2013-Projekt:</span><span class="sxs-lookup"><span data-stu-id="166c6-142">Create an empty SharePoint 2013 project, as follows:</span></span>
    
    1. <span data-ttu-id="166c6-143">Wählen Sie im Dialogfeld **Neues Projekt** in der Dropdownliste oben im Dialogfeld **.NET Framework 4.5** aus.</span><span class="sxs-lookup"><span data-stu-id="166c6-143">In the **New Project** dialog box, choose **.NET Framework 4.5** from the drop-down list at the top of the dialog box.</span></span> 
        
    2. <span data-ttu-id="166c6-144">Wählen Sie in der Liste der Vorlagenkategorien die **Kategorie Office SharePoint** aus, und wählen Sie dann die **SharePoint 2013-Projektvorlage** aus.</span><span class="sxs-lookup"><span data-stu-id="166c6-144">In the list of template categories, choose the **Office SharePoint** category, and then choose the **SharePoint 2013 Project** template.</span></span> 
        
    3. <span data-ttu-id="166c6-145">Nennen Sie das Projekt GetProjectsJSOM, und wählen Sie dann die **Schaltfläche OK** aus.</span><span class="sxs-lookup"><span data-stu-id="166c6-145">Name the project GetProjectsJSOM, and then choose the **OK** button.</span></span> 
        
    4. <span data-ttu-id="166c6-146">Wählen Sie **im Dialogfeld SharePoint-Anpassungs-Assistent** die Option **Als** Farmlösung bereitstellen aus, und klicken Sie dann auf die **Schaltfläche OK.**</span><span class="sxs-lookup"><span data-stu-id="166c6-146">In the **SharePoint Customization Wizard** dialog box, choose **Deploy as a farm solution**, and then choose the **OK** button.</span></span> 
    
3. <span data-ttu-id="166c6-147">Bearbeiten Sie im Projektmappen-Explorer den Wert der **Site URL-Eigenschaft** für das **ProjectsJSOM-Projekt,** um mit der URL der Project Web App-Instanz (z. B. ) zu  `https://ServerName/PWA` übereinstimmen.</span><span class="sxs-lookup"><span data-stu-id="166c6-147">In Solution Explorer, edit the value of the **Site URL** property for the **ProjectsJSOM** project to match the URL of the Project Web App instance (for example,  `https://ServerName/PWA`).</span></span>
    
4. <span data-ttu-id="166c6-148">Öffnen Sie das Kontextmenü für das **GetProjectsJSOM-Projekt,** und fügen Sie dann einen zugeordneten SharePoint-Ordner "Layouts" hinzu.</span><span class="sxs-lookup"><span data-stu-id="166c6-148">Open the shortcut menu for the **GetProjectsJSOM** project, and then add a SharePoint "Layouts" mapped folder.</span></span> 
    
5. <span data-ttu-id="166c6-149">Öffnen Sie im Ordner **Layouts** das Kontextmenü für den Ordner **GetProjectsJSOM,** und fügen Sie dann eine neue SharePoint-Anwendungsseite namens ProjectsList.aspx hinzu.</span><span class="sxs-lookup"><span data-stu-id="166c6-149">In the **Layouts** folder, open the shortcut menu for the **GetProjectsJSOM** folder, and then add a new SharePoint application page named ProjectsList.aspx.</span></span>
    
   > [!NOTE]
   > <span data-ttu-id="166c6-150">In diesem Beispiel wird nicht die Code-Behind-Datei verwendet, die Visual Studio 2012 für die Anwendungsseite erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="166c6-150">This example does not use the code-behind file that Visual Studio 2012 creates for the application page.</span></span> 
  
6. <span data-ttu-id="166c6-151">Öffnen Sie das Kontextmenü für die **Seite ProjectsList.aspx,** und wählen **Sie Als Startelement festlegen aus.**</span><span class="sxs-lookup"><span data-stu-id="166c6-151">Open the shortcut menu for the **ProjectsList.aspx** page and choose **Set as Startup Item**.</span></span>
    
7. <span data-ttu-id="166c6-152">Definieren Sie im Markup für die **ProjectsList.aspx-Seite** eine Tabelle und einen Nachrichtenplatzhalter innerhalb der "Main"-asp:Content-Tags wie folgt. </span><span class="sxs-lookup"><span data-stu-id="166c6-152">In the markup for the **ProjectsList.aspx** page, define a table and a message placeholder inside the "Main" **asp:Content** tags, as follows.</span></span> 
    
    ```HTML
    <table width="100%" id="tblProjects">
        <tr id="headerRow">
            <th width="25%" align="left">Project name</th>
            <th width="25%" align="left">Created date</th>
            <th width="50%" align="left">Project ID</th>
        </tr>
    </table>
    <div id="divMessage">
        <br/>
        <span id="spanMessage" style="color: #FF0000;"></span>
    </div>
    ```

### <a name="retrieving-the-projects-collection"></a><span data-ttu-id="166c6-153">Abrufen der Projektsammlung</span><span class="sxs-lookup"><span data-stu-id="166c6-153">Retrieving the projects collection</span></span>
<span data-ttu-id="166c6-154"><a name="pj15_GetStartedJSOM_RetrieveProjs"> </a></span><span class="sxs-lookup"><span data-stu-id="166c6-154"><a name="pj15_GetStartedJSOM_RetrieveProjs"> </a></span></span>

<span data-ttu-id="166c6-155">In den folgenden Schritten wird die Projektsammlung abgerufen und initialisiert.</span><span class="sxs-lookup"><span data-stu-id="166c6-155">The following steps retrieve and initialize the projects collection.</span></span>
  
1. <span data-ttu-id="166c6-156">Fügen Sie nach dem schließenden **div-Tag** ein **SharePoint:ScriptLink-Tag** hinzu, das auf die PS.js wie folgt verweist.</span><span class="sxs-lookup"><span data-stu-id="166c6-156">After the closing **div** tag, add a **SharePoint:ScriptLink** tag that references the PS.js file, as follows.</span></span> 
    
   ```HTML
    <SharePoint:ScriptLink name="PS.js" runat="server" ondemand="false" localizable="false" loadafterui="true" />
   ```

2. <span data-ttu-id="166c6-157">Fügen Sie **unter dem SharePoint:ScriptLink-Tag** **skripttags** wie folgt hinzu.</span><span class="sxs-lookup"><span data-stu-id="166c6-157">Below the **SharePoint:ScriptLink** tag, add **script** tags, as follows.</span></span> 
    
   ```HTML
    <script type="text/javascript">
        // Paste the remaining code snippets here, in the order that they are presented.
    </script>
   ```

3. <span data-ttu-id="166c6-158">Deklarieren Sie eine globale Variable, um die Projects-Auflistung wie folgt zu speichern.</span><span class="sxs-lookup"><span data-stu-id="166c6-158">Declare a global variable to store the projects collection, as follows.</span></span>
    
   ```js
   var projects;
   ```

4. <span data-ttu-id="166c6-159">Rufen Sie **dieSP.SOD.executeOrDelayUntilScriptLoaded-Methode** auf, um sicherzustellen, dass die PS.js geladen wird, bevor Der benutzerdefinierte Code ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="166c6-159">Call the **SP.SOD.executeOrDelayUntilScriptLoaded** method to ensure that the PS.js file is loaded before your custom code runs.</span></span> 
    
   ```js
   SP.SOD.executeOrDelayUntilScriptLoaded(GetProjects, "PS.js");
   ```

5. <span data-ttu-id="166c6-160">Fügen Sie eine Funktion hinzu, die eine Verbindung mit dem aktuellen Kontext herstellt und die Projects-Auflistung wie folgt abruft.</span><span class="sxs-lookup"><span data-stu-id="166c6-160">Add a function that connects to the current context and retrieves the projects collection, as follows.</span></span>
    
   ```js
    function GetProjects() {
        // Initialize the current client context.
        var projContext = PS.ProjectContext.get_current();
        // Get the projects collection.
        projects = projContext.get_projects();
        // Register the request that you want to run on the server.
        // This call includes an optional "Include" parameter to request only the
        // Name, CreatedDate, and Id properties of the projects in the collection.
        projContext.load(projects, 'Include(Name, CreatedDate, Id)');
        // Run the request on the server.
        projContext.executeQueryAsync(onQuerySucceeded, onQueryFailed);
    }
   ```

   <span data-ttu-id="166c6-161">Einige Clientobjekte, die Sie über den Kontext abrufen, enthalten keine Daten, bis sie initialisiert wurden. Das heißt, Sie können erst auf die Eigenschaftswerte des Objekts zugreifen, wenn das Objekt initialisiert wurde.</span><span class="sxs-lookup"><span data-stu-id="166c6-161">Some client objects that you retrieve through the context contain no data until they are initialized; that is, you cannot access the property values of the object until the object is initialized.</span></span> <span data-ttu-id="166c6-162">Darüber hinaus müssen Sie für Eigenschaften vom Typ **ValueObject** die Eigenschaft explizit anfordern, bevor Sie auf ihren Wert zugreifen können.</span><span class="sxs-lookup"><span data-stu-id="166c6-162">Moreover, for properties of type **ValueObject**, you must explicitly request the property before you can access its value.</span></span> <span data-ttu-id="166c6-163">(Wenn Sie versuchen, auf eine Eigenschaft zu zugreifen, bevor sie initialisiert wird, erhalten Sie eine **PropertyOrFieldNotInitializedException-Ausnahme.)**</span><span class="sxs-lookup"><span data-stu-id="166c6-163">(If you try to access a property before it is initialized, you receive a **PropertyOrFieldNotInitializedException** exception.)</span></span> 
    
   <span data-ttu-id="166c6-164">Zum Initialisieren eines Objekts rufen Sie die **load-Methode** (oder **die loadQuery-Methode)** und dann die **executeQueryAsync-Methode** auf.</span><span class="sxs-lookup"><span data-stu-id="166c6-164">To initialize an object, you call the **load** method (or the **loadQuery** method) and then the **executeQueryAsync** method.</span></span> 
    
   - <span data-ttu-id="166c6-165">Durch aufrufen **der Load-Funktion** oder **der loadQuery-Funktion** wird eine Anforderung registriert, die Sie auf dem Server ausführen möchten.</span><span class="sxs-lookup"><span data-stu-id="166c6-165">Calling the **load** function or the **loadQuery** function registers a request that you want to run on the server.</span></span> <span data-ttu-id="166c6-166">Sie übergeben einen Parameter, der das abzurufende Objekt darstellt.</span><span class="sxs-lookup"><span data-stu-id="166c6-166">You pass in a parameter that represents the object that you want to retrieve.</span></span> <span data-ttu-id="166c6-167">Wenn Sie mit einer **ValueObject-Eigenschaft** arbeiten, fordern Sie auch die Eigenschaft im Parameter an.</span><span class="sxs-lookup"><span data-stu-id="166c6-167">If you are working with a **ValueObject** property, then you also request the property in the parameter.</span></span> 
    
   - <span data-ttu-id="166c6-168">Durch Aufrufen **der executeQueryAsync-Funktion** wird die Abfrageanforderung asynchron an den Server gesendet.</span><span class="sxs-lookup"><span data-stu-id="166c6-168">Calling the **executeQueryAsync** function sends the query request to the server asynchronously.</span></span> <span data-ttu-id="166c6-169">Sie übergeben eine erfolgreiche Rückruffunktion und eine Fehlerrückruffunktion zum Aufrufen, wenn die Serverantwort empfangen wird.</span><span class="sxs-lookup"><span data-stu-id="166c6-169">You pass in a success callback function and a failure callback function to invoke when the server response is received.</span></span> 
    
   <span data-ttu-id="166c6-170">Um den Netzwerkdatenverkehr zu reduzieren, fordern Sie beim Aufrufen der Ladefunktion nur die Eigenschaften an, mit denen Sie **arbeiten** möchten.</span><span class="sxs-lookup"><span data-stu-id="166c6-170">To reduce network traffic, request only the properties that you want to work with when you call the **load** function.</span></span> <span data-ttu-id="166c6-171">Wenn Sie mit mehreren Objekten arbeiten, gruppieren  Sie außerdem mehrere Aufrufe der Load-Funktion, bevor Sie die **executeQueryAsync-Funktion** aufrufen, wenn dies möglich ist.</span><span class="sxs-lookup"><span data-stu-id="166c6-171">In addition, if you are working with multiple objects, group multiple calls to the **load** function before you call the **executeQueryAsync** function when it is possible.</span></span> 
    
### <a name="iterating-through-the-projects-collection"></a><span data-ttu-id="166c6-172">Iterieren der Projektsammlung</span><span class="sxs-lookup"><span data-stu-id="166c6-172">Iterating through the projects collection</span></span>
<span data-ttu-id="166c6-173"><a name="pj15_GetStartedJSOM_IterateProjs"> </a></span><span class="sxs-lookup"><span data-stu-id="166c6-173"><a name="pj15_GetStartedJSOM_IterateProjs"> </a></span></span>

<span data-ttu-id="166c6-174">Führen Sie die folgenden Schritte durch die Projects-Auflistung durch (wenn der Serveraufruf erfolgreich ist) oder rendern Sie eine Fehlermeldung (wenn der Aufruf fehlschlägt).</span><span class="sxs-lookup"><span data-stu-id="166c6-174">The following steps iterate through the projects collection (if the server call is successful) or render an error message (if the call fails).</span></span>
  
1. <span data-ttu-id="166c6-175">Fügen Sie wie folgt eine erfolgreiche Rückruffunktion hinzu, die die Projects-Auflistung durchfärstet.</span><span class="sxs-lookup"><span data-stu-id="166c6-175">Add a success callback function that iterates through the projects collection, as follows.</span></span>
    
   ```js
    function onQuerySucceeded(sender, args) {
        // Get the enumerator and iterate through the collection.
        var projectEnumerator = projects.getEnumerator();
        while (projectEnumerator.moveNext()) {
            var project = projectEnumerator.get_current();
            // Create the row for the project's information.
            var row = tblProjects.insertRow();
            // Insert cells for the Id, Name, and CreatedDate properties.
            row.insertCell().innerText = project.get_name();
            row.insertCell().innerText = project.get_createdDate();
            row.insertCell().innerText = project.get_id();
        }
    }
   ```

2. <span data-ttu-id="166c6-176">Fügen Sie eine Fehlerrückruffunktion hinzu, die eine Fehlermeldung wie folgt rendert.</span><span class="sxs-lookup"><span data-stu-id="166c6-176">Add a failure callback function that renders an error message, as follows.</span></span>
    
    ```js
    function onQueryFailed(sender, args) {
        $get("spanMessage").innerText = 'Request failed: ' + args.get_message();
    }
    ```

3. <span data-ttu-id="166c6-177">Um die Anwendungsseite zu testen, wählen Sie in der Menüleiste die Optionen **Debuggen**, **Debuggen starten**.</span><span class="sxs-lookup"><span data-stu-id="166c6-177">To test the application page, on the menu bar, choose **Debug**, **Start Debugging**.</span></span> <span data-ttu-id="166c6-178">Wenn Sie aufgefordert werden, die Datei web.config zu ändern, wählen Sie **OK aus.**</span><span class="sxs-lookup"><span data-stu-id="166c6-178">If you are prompted to modify the web.config file, choose **OK**.</span></span>

<span data-ttu-id="166c6-179"><a name="pj15_GetStartedJSOM_CompleteExample"> </a></span><span class="sxs-lookup"><span data-stu-id="166c6-179"><a name="pj15_GetStartedJSOM_CompleteExample"> </a></span></span>

## <a name="complete-code-example"></a><span data-ttu-id="166c6-180">Vollständiges Codebeispiel</span><span class="sxs-lookup"><span data-stu-id="166c6-180">Complete code example</span></span>

<span data-ttu-id="166c6-181">Nachfolgend finden Sie den vollständigen Code aus der Datei ProjectsList.aspx.</span><span class="sxs-lookup"><span data-stu-id="166c6-181">Following is the complete code from the ProjectsList.aspx file.</span></span>
  
```js
<%@ Assembly Name="$SharePoint.Project.AssemblyFullName$" %>
<%@ Import Namespace="Microsoft.SharePoint.ApplicationPages" %>
<%@ Register Tagprefix="SharePoint" Namespace="Microsoft.SharePoint.WebControls" Assembly="Microsoft.SharePoint, Version=15.0.0.0, Culture=neutral, PublicKeyToken=71e9bce111e9429c" %>
<%@ Register Tagprefix="Utilities" Namespace="Microsoft.SharePoint.Utilities" Assembly="Microsoft.SharePoint, Version=15.0.0.0, Culture=neutral, PublicKeyToken=71e9bce111e9429c" %>
<%@ Register Tagprefix="asp" Namespace="System.Web.UI" Assembly="System.Web.Extensions, Version=3.5.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35" %>
<%@ Import Namespace="Microsoft.SharePoint" %>
<%@ Assembly Name="Microsoft.Web.CommandUI, Version=15.0.0.0, Culture=neutral, PublicKeyToken=71e9bce111e9429c" %>
<%@ Page Language="C#" AutoEventWireup="true" CodeBehind="ProjectsList.aspx.cs" Inherits="GetProjectsJSOM.Layouts.GetProjectsJSOM.ProjectsList" DynamicMasterPageFile="~masterurl/default.master" %>
<asp:Content ID="PageHead" ContentPlaceHolderID="PlaceHolderAdditionalPageHead" runat="server">
</asp:Content>
<asp:Content ID="Main" ContentPlaceHolderID="PlaceHolderMain" runat="server">
    <table width="100%" id="tblProjects">
    <tr id="headerRow">
        <th width="25%" align="left">Project name</th>
        <th width="25%" align="left">Created date</th>
        <th width="50%" align="left">Project ID</th>
    </tr>
</table>
<div id="divMessage">
    <br/>
    <span id="spanMessage" style="color: #FF0000;"></span>
</div>
<SharePoint:ScriptLink name="PS.js" runat="server" ondemand="false" localizable="false" loadafterui="true" />
<script type="text/javascript">
    // Declare a variable to store the published projects that exist
    // in the current context.
    var projects;
    // Ensure that the PS.js file is loaded before your custom code runs.
    SP.SOD.executeOrDelayUntilScriptLoaded(GetProjects, "PS.js");
    // Get the projects collection.
    function GetProjects() {
        // Initialize the current client context.
        var projContext = PS.ProjectContext.get_current();
        // Get the projects collection.
        projects = projContext.get_projects();
        // Register the request that you want to run on the server.
        // This call includes an optional "Include" parameter to request only the
        // Name, CreatedDate, and Id properties of the projects in the collection.
        projContext.load(projects, 'Include(Name, CreatedDate, Id)');
        // Run the request on the server.
        projContext.executeQueryAsync(onQuerySucceeded, onQueryFailed);
    }
    function onQuerySucceeded(sender, args) {
        // Get the enumerator and iterate through the collection.
        var projectEnumerator = projects.getEnumerator();
        while (projectEnumerator.moveNext()) {
            var project = projectEnumerator.get_current();
            // Create the row for the project's information.
            var row = tblProjects.insertRow();
            // Insert cells for the Id, Name, and CreatedDate properties.
            row.insertCell().innerText = project.get_name();
            row.insertCell().innerText = project.get_createdDate();
            row.insertCell().innerText = project.get_id();
        }
    }
    function onQueryFailed(sender, args) {
        $get("spanMessage").innerText = 'Request failed: ' + args.get_message();
    }
</script>
</asp:Content>
<asp:Content ID="PageTitle" ContentPlaceHolderID="PlaceHolderPageTitle" runat="server">
Application Page
</asp:Content>
<asp:Content ID="PageTitleInTitleArea" ContentPlaceHolderID="PlaceHolderPageTitleInTitleArea" runat="server" >
My Application Page
</asp:Content>

```

<span data-ttu-id="166c6-182"><a name="pj15_GetStartedJSOM_AR"> </a></span><span class="sxs-lookup"><span data-stu-id="166c6-182"><a name="pj15_GetStartedJSOM_AR"> </a></span></span>

## <a name="see-also"></a><span data-ttu-id="166c6-183">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="166c6-183">See also</span></span>

- [<span data-ttu-id="166c6-184">Erstellen, Abrufen, Aktualisieren und Löschen von Projekten mithilfe des Project Server-JavaScript-Objektmodells</span><span class="sxs-lookup"><span data-stu-id="166c6-184">Create, retrieve, update, and delete projects by using the Project Server JavaScript object model</span></span>](create-retrieve-update-delete-projects-using-project-server-javascript.md)  
- [<span data-ttu-id="166c6-185">Clientseitiges Objektmodell (CSOM) für Project 2013</span><span class="sxs-lookup"><span data-stu-id="166c6-185">Client-side object model (CSOM) for Project 2013</span></span>](client-side-object-model-csom-for-project-2013.md)
- [<span data-ttu-id="166c6-186">Erste Schritte mit dem Project Server-CSOM und .NET</span><span class="sxs-lookup"><span data-stu-id="166c6-186">Getting started with the Project Server CSOM and .NET</span></span>](getting-started-with-the-project-server-csom-and-net.md)
    

