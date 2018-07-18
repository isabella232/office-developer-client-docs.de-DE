---
title: Erstellen, abrufen, aktualisieren und Löschen von Projekten mit Project Server JavaScript
manager: soliver
ms.date: 08/10/2016
ms.audience: Developer
localization_priority: Normal
ms.assetid: 6b690938-05bc-46a3-a40e-30f081403767
description: Abrufen der aktuellen Instanz ProjectContext; Rufen Sie ab und durchlaufen Sie die Auflistung der veröffentlichten Projekte auf dem Server. Erstellen, abrufen, Auschecken und Löschen eines Projekts mithilfe der Project Server-JavaScript-Objektmodells; und ändern Sie die Eigenschaften des Projekts.
ms.openlocfilehash: 966c1298d210cb608001e4ce2b390611a75bdb24
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19796168"
---
# <a name="create-retrieve-update-and-delete-projects-using-project-server-javascript"></a><span data-ttu-id="c57fe-103">Erstellen, abrufen, aktualisieren und Löschen von Projekten mit Project Server JavaScript</span><span class="sxs-lookup"><span data-stu-id="c57fe-103">Create, retrieve, update, and delete projects using Project Server JavaScript</span></span>

<span data-ttu-id="c57fe-104">Die Szenarien in diesem Artikel wird gezeigt, wie die aktuelle Instanz **ProjectContext** abgerufen; Rufen Sie ab und durchlaufen Sie die Auflistung der veröffentlichten Projekte auf dem Server. Erstellen, abrufen, Auschecken und Löschen eines Projekts mithilfe der Project Server-JavaScript-Objektmodells; und ändern Sie die Eigenschaften des Projekts.</span><span class="sxs-lookup"><span data-stu-id="c57fe-104">The scenarios in this article show how to get the current **ProjectContext** instance; retrieve and iterate through the collection of published projects on the server; create, retrieve, check out, and delete a project by using the Project Server JavaScript object model; and change a project's properties.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="c57fe-105">Diese Szenarien Definieren von benutzerdefiniertem Code im Markup eine SharePoint-Anwendungsseite verwenden jedoch kein Code-Behind-Datei, mit der Visual Studio 2012 erstellt für die Seite.</span><span class="sxs-lookup"><span data-stu-id="c57fe-105">These scenarios define custom code in the markup of a SharePoint application page but do not use the code-behind file that Visual Studio 2012 creates for the page.</span></span> 
  
## <a name="prerequisites-for-working-with-project-server-2013-projects-in-the-javascript-object-model"></a><span data-ttu-id="c57fe-106">Voraussetzungen für das Arbeiten mit Project Server 2013-Projekten in der JavaScript-Objektmodell</span><span class="sxs-lookup"><span data-stu-id="c57fe-106">Prerequisites for working with Project Server 2013 projects in the JavaScript object model</span></span>

<span data-ttu-id="c57fe-107">Um die beschriebenen Szenarien in diesem Artikel durchführen, müssen Sie installieren und konfigurieren die folgenden Produkte:</span><span class="sxs-lookup"><span data-stu-id="c57fe-107">To perform the scenarios that are described in this article, you must install and configure the following products:</span></span>
  
- <span data-ttu-id="c57fe-108">SharePoint Server 2013</span><span class="sxs-lookup"><span data-stu-id="c57fe-108">SharePoint Server 2013</span></span>
- <span data-ttu-id="c57fe-109">Project Server 2013</span><span class="sxs-lookup"><span data-stu-id="c57fe-109">Project Server 2013</span></span>
- <span data-ttu-id="c57fe-110">Visual Studio 2012</span><span class="sxs-lookup"><span data-stu-id="c57fe-110">Visual Studio 2012</span></span>
- <span data-ttu-id="c57fe-111">Office Developer Tools für Visual Studio 2012</span><span class="sxs-lookup"><span data-stu-id="c57fe-111">Office Developer Tools for Visual Studio 2012</span></span>
    
<span data-ttu-id="c57fe-112">Sie benötigen auch Berechtigungen zum Bereitstellen der Erweiterung zu SharePoint Server 2013 und zur Teilnahme an Projekten.</span><span class="sxs-lookup"><span data-stu-id="c57fe-112">You must also have permissions to deploy the extension to SharePoint Server 2013 and to contribute to projects.</span></span>
  
> [!NOTE]
> <span data-ttu-id="c57fe-113">Diese Anweisungen wird davon ausgegangen, dass Sie auf dem Computer entwickeln, die Project Server 2013 ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="c57fe-113">These instructions assume that you are developing on the computer that is running Project Server 2013.</span></span> 
  
## <a name="create-the-visual-studio-solution"></a><span data-ttu-id="c57fe-114">Erstellen der Visual Studio-Projektmappe</span><span class="sxs-lookup"><span data-stu-id="c57fe-114">Create the Visual Studio solution</span></span>
<span data-ttu-id="c57fe-115"><a name="pj15_CRUDProjectsJSOM_Setup"> </a></span><span class="sxs-lookup"><span data-stu-id="c57fe-115"></span></span>

<span data-ttu-id="c57fe-116">Die folgenden Schritte erstellen Sie eine Visual Studio 2012-Lösung, die ein SharePoint-Projekt und einer Anwendungsseite enthält.</span><span class="sxs-lookup"><span data-stu-id="c57fe-116">The following steps create a Visual Studio 2012 solution that contains a SharePoint project and an application page.</span></span> <span data-ttu-id="c57fe-117">Die Seite enthält die Logik für das Arbeiten mit Projekten.</span><span class="sxs-lookup"><span data-stu-id="c57fe-117">The page contains the logic for working with projects.</span></span>
  
### <a name="to-create-the-sharepoint-project-in-visual-studio"></a><span data-ttu-id="c57fe-118">Zum Erstellen von SharePoint-Projekt in Visual Studio</span><span class="sxs-lookup"><span data-stu-id="c57fe-118">To create the SharePoint project in Visual Studio</span></span>

1. <span data-ttu-id="c57fe-119">Führen Sie auf dem Computer, auf der Project Server 2013 ausgeführt wird, Visual Studio 2012 als Administrator.</span><span class="sxs-lookup"><span data-stu-id="c57fe-119">On the computer that is running Project Server 2013, run Visual Studio 2012 as an administrator.</span></span>
    
2. <span data-ttu-id="c57fe-120">Klicken Sie in der Menüleiste auf **Datei**, **Neu**, **Projekt**.</span><span class="sxs-lookup"><span data-stu-id="c57fe-120">On the menu bar, choose **File**, **New**, **Project**.</span></span>
    
3. <span data-ttu-id="c57fe-121">Wählen Sie im Dialogfeld **Neues Projekt** aus der Dropdownliste oben im Dialogfeld die Option **.NET Framework 4.5**.</span><span class="sxs-lookup"><span data-stu-id="c57fe-121">In the **New Project** dialog box, choose **.NET Framework 4.5** from the drop-down list at the top of the dialog box.</span></span> 
    
4. <span data-ttu-id="c57fe-122">Wählen Sie in der Kategorie **Office/SharePoint** -Vorlage **SharePoint-Lösungen**, und wählen Sie dann die Vorlage **SharePoint 2013-Projekts** .</span><span class="sxs-lookup"><span data-stu-id="c57fe-122">In the **Office/SharePoint** template category, choose **SharePoint Solutions**, and then choose the **SharePoint 2013 Project** template.</span></span> 
    
5. <span data-ttu-id="c57fe-123">Nennen Sie das Projekt ProjectsJSOM, und wählen Sie dann auf die Schaltfläche **OK** .</span><span class="sxs-lookup"><span data-stu-id="c57fe-123">Name the project ProjectsJSOM, and then choose the **OK** button.</span></span> 
    
6. <span data-ttu-id="c57fe-124">Klicken Sie im **Assistenten zum Anpassen von SharePoint**-Dialogfeld Wählen Sie **als Farmlösung bereitstellen**, und wählen Sie dann auf die Schaltfläche **Fertig stellen**.</span><span class="sxs-lookup"><span data-stu-id="c57fe-124">In the **SharePoint Customization Wizard** dialog box, choose **Deploy as a farm solution**, and then choose the **Finish** button.</span></span> 
    
7. <span data-ttu-id="c57fe-125">Bearbeiten Sie den Wert der Eigenschaft **Website-URL** für das Projekt **ProjectsJSOM** entsprechend die URL der Project Web App-Instanz (z. B. `http://ServerName/PWA`).</span><span class="sxs-lookup"><span data-stu-id="c57fe-125">Edit the value of the **Site URL** property for the **ProjectsJSOM** project to match the URL of the Project Web App instance (for example,  `http://ServerName/PWA`).</span></span>
    
### <a name="to-create-the-application-page-in-visual-studio"></a><span data-ttu-id="c57fe-126">Zum Erstellen der Anwendungsseite in Visual Studio</span><span class="sxs-lookup"><span data-stu-id="c57fe-126">To create the application page in Visual Studio</span></span>

1. <span data-ttu-id="c57fe-127">Im **Projektmappen-Explorer**das Kontextmenü für das Projekt **ProjectsJSOM** öffnen, und fügen Sie eine SharePoint "Layouts" Ordner zugeordnet.</span><span class="sxs-lookup"><span data-stu-id="c57fe-127">In **Solution Explorer**, open the shortcut menu for the **ProjectsJSOM** project, and then add a SharePoint "Layouts" mapped folder.</span></span> 
    
2. <span data-ttu-id="c57fe-128">Öffnen Sie im Ordner **Layouts** das Kontextmenü für den Ordner **ProjectsJSOM** , und fügen Sie eine neue SharePoint-Anwendungsseite namens ProjectsList.aspx.</span><span class="sxs-lookup"><span data-stu-id="c57fe-128">In the **Layouts** folder, open the shortcut menu for the **ProjectsJSOM** folder, and then add a new SharePoint application page named ProjectsList.aspx.</span></span>
    
3. <span data-ttu-id="c57fe-129">Öffnen Sie das Kontextmenü für die Seite **ProjectsList.aspx** , und wählen Sie **als Startelement festlegen**.</span><span class="sxs-lookup"><span data-stu-id="c57fe-129">Open the shortcut menu for the **ProjectsList.aspx** page and choose **Set as Startup Item**.</span></span>
    
4. <span data-ttu-id="c57fe-130">Definieren Sie Benutzeroberflächen-Steuerelemente in den "Main" **Asp: Content** -Tags im Markup für die Seite **ProjectsList.aspx** wie folgt.</span><span class="sxs-lookup"><span data-stu-id="c57fe-130">In the markup for the **ProjectsList.aspx** page, define user interface controls inside the "Main" **asp:Content** tags, as follows.</span></span> 
    
   ```HTML
    <table width="100%" id="tblProjects">
        <tr id="headerRow">
            <th width="25%" align="left">Name</th>
            <th width="25%" align="left">Description</th>
            <th width="25%" align="left">Start Date</th>
            <th width="25%" align="left">ID</th>
        </tr>
    </table>
    <textarea id="txtGuid" rows="1" cols="35">Paste the project GUID here.</textarea>
    <button id="btnSend" type="button"></button><br />
    <span id="spanMessage" style="color: #FF0000;"></span>
   ```

   > [!NOTE]
   > <span data-ttu-id="c57fe-131">Diese Steuerelemente können nicht in jedem Szenario verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="c57fe-131">These controls may not be used in every scenario.</span></span> <span data-ttu-id="c57fe-132">Beispielsweise wird das Szenario "Projekte erstellen" die **Schaltfläche** und **Textarea** -Steuerelemente nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="c57fe-132">For example, the "Create projects" scenario does not use the **textarea** and **button** controls.</span></span> 
  
5. <span data-ttu-id="c57fe-133">Nach der schließenden **span** markieren, fügen Sie wie folgt ein **SharePoint:ScriptLink** -Tag, ein Tag **SharePoint:FormDigest** und **Script** -Tags hinzu.</span><span class="sxs-lookup"><span data-stu-id="c57fe-133">After the closing **span** tag, add a **SharePoint:ScriptLink** tag, a **SharePoint:FormDigest** tag, and **script** tags, as follows.</span></span> 
    
   ```HTML
    <SharePoint:ScriptLink id="ScriptLink" name="PS.js" runat="server" ondemand="false" localizable="false" loadafterui="true" />
    <SharePoint:FormDigest id="FormDigest" runat="server" />
    <script type="text/javascript">
        // Replace this comment with the code for your scenario.
    </script>
   ```

   <span data-ttu-id="c57fe-134">Das Tag **SharePoint:ScriptLink** verweist auf die Datei PS.js, die das JavaScript-Objektmodell für Project Server 2013 definiert.</span><span class="sxs-lookup"><span data-stu-id="c57fe-134">The **SharePoint:ScriptLink** tag references the PS.js file, which defines the JavaScript object model for Project Server 2013.</span></span> <span data-ttu-id="c57fe-135">Das **SharePoint:FormDigest** -Tag generiert einen Nachrichtenhash für die sicherheitsüberprüfung bei Bedarf von Operationen, die Server-Inhalte zu aktualisieren.</span><span class="sxs-lookup"><span data-stu-id="c57fe-135">The **SharePoint:FormDigest** tag generates a message digest for security validation when required by operations that update server content.</span></span> 
    
6. <span data-ttu-id="c57fe-136">Ersetzen Sie den Kommentar Platzhalter durch den Code aus einem der folgenden Verfahren aus:</span><span class="sxs-lookup"><span data-stu-id="c57fe-136">Replace the placeholder comment with the code from one of the following procedures:</span></span>
    
   - [<span data-ttu-id="c57fe-137">Erstellen von Project Server 2013-Projekten mithilfe des JavaScript-Objektmodells</span><span class="sxs-lookup"><span data-stu-id="c57fe-137">Create Project Server 2013 projects by using the JavaScript object model</span></span>](#pj15_CRUDProjectsJSOM_CreateProjects)
    
   - [<span data-ttu-id="c57fe-138">Aktualisieren von Project Server 2013-Projekte mithilfe des JavaScript-Objektmodells</span><span class="sxs-lookup"><span data-stu-id="c57fe-138">Update Project Server 2013 projects by using the JavaScript object model</span></span>](#pj15_CRUDProjectsJSOM_UpdateProjects)
    
   - [<span data-ttu-id="c57fe-139">Löschen von Project Server 2013-Projekten mithilfe des JavaScript-Objektmodells</span><span class="sxs-lookup"><span data-stu-id="c57fe-139">Delete Project Server 2013 projects by using the JavaScript object model</span></span>](#pj15_CRUDProjectsJSOM_DeleteProjects)
    
7. <span data-ttu-id="c57fe-140">Wählen Sie zum Testen der Anwendungsseite in der Menüleiste **Debuggen**, **Debuggen starten**aus.</span><span class="sxs-lookup"><span data-stu-id="c57fe-140">To test the application page, on the menu bar, choose **Debug**, **Start Debugging**.</span></span> <span data-ttu-id="c57fe-141">Wenn Sie aufgefordert werden, ändern Sie die Datei "Web.config", und wählen Sie **OK**.</span><span class="sxs-lookup"><span data-stu-id="c57fe-141">If you are prompted to modify the web.config file, choose **OK**.</span></span>
    
## <a name="create-project-server-2013-projects-by-using-the-javascript-object-model"></a><span data-ttu-id="c57fe-142">Erstellen von Project Server 2013-Projekten mithilfe des JavaScript-Objektmodells</span><span class="sxs-lookup"><span data-stu-id="c57fe-142">Create Project Server 2013 projects by using the JavaScript object model</span></span>
<span data-ttu-id="c57fe-143"><a name="pj15_CRUDProjectsJSOM_CreateProjects"> </a></span><span class="sxs-lookup"><span data-stu-id="c57fe-143"></span></span>

<span data-ttu-id="c57fe-144">Das Verfahren in diesem Abschnitt werden Projekte mithilfe des JavaScript-Objektmodells erstellt.</span><span class="sxs-lookup"><span data-stu-id="c57fe-144">The procedure in this section creates projects by using the JavaScript object model.</span></span> <span data-ttu-id="c57fe-145">Das Verfahren umfasst die folgenden allgemeinen Schritte:</span><span class="sxs-lookup"><span data-stu-id="c57fe-145">The procedure includes the following high-level steps:</span></span>
  
1. <span data-ttu-id="c57fe-146">Rufen Sie die aktuelle Instanz **ProjectContext** .</span><span class="sxs-lookup"><span data-stu-id="c57fe-146">Get the current **ProjectContext** instance.</span></span> 
    
2. <span data-ttu-id="c57fe-147">Erstellen Sie ein **ProjectCreationInformation** -Objekt, um die anfängliche Eigenschaften für Ihr Projekt angeben.</span><span class="sxs-lookup"><span data-stu-id="c57fe-147">Create a **ProjectCreationInformation** object to specify initial properties for your project.</span></span> <span data-ttu-id="c57fe-148">Geben Sie die erforderlichen **Name** -Eigenschaft mithilfe der **ProjectCreationInformation.set_name** -Funktion.</span><span class="sxs-lookup"><span data-stu-id="c57fe-148">Specify the required **name** property by using the **ProjectCreationInformation.set_name** function.</span></span> 
    
3. <span data-ttu-id="c57fe-149">Die veröffentlichten Projekte mithilfe der Funktion **ProjectContext.get_projects** vom Server ab.</span><span class="sxs-lookup"><span data-stu-id="c57fe-149">Retrieve the published projects from the server by using the **ProjectContext.get_projects** function.</span></span> <span data-ttu-id="c57fe-150">Die **Get_projects** -Funktion gibt ein **ProjectCollection** -Objekt zurück.</span><span class="sxs-lookup"><span data-stu-id="c57fe-150">The **get_projects** function returns a **ProjectCollection** object.</span></span> 
    
4. <span data-ttu-id="c57fe-151">Fügen Sie das neue Projekt zur Auflistung hinzu, indem Sie mithilfe der **ProjectCollection.add** -Funktion und im **ProjectCreationInformation** -Objekt übergeben.</span><span class="sxs-lookup"><span data-stu-id="c57fe-151">Add the new project to the collection by using the **ProjectCollection.add** function and passing in the **ProjectCreationInformation** object.</span></span> 
    
5. <span data-ttu-id="c57fe-152">Aktualisieren Sie die Auflistung mithilfe der **ProjectCollection.update** und die **ProjectContext.waitForQueueAsync** -Funktion.</span><span class="sxs-lookup"><span data-stu-id="c57fe-152">Update the collection by using the **ProjectCollection.update** function and the **ProjectContext.waitForQueueAsync** function.</span></span> <span data-ttu-id="c57fe-153">Die **update** -Funktion gibt ein **QueueJob** -Objekt, das Sie an **WaitForQueueAsync**übergeben.</span><span class="sxs-lookup"><span data-stu-id="c57fe-153">The **update** function returns a **QueueJob** object that you pass to **waitForQueueAsync**.</span></span> <span data-ttu-id="c57fe-154">Dieses Anrufs veröffentlicht auch das Projekt.</span><span class="sxs-lookup"><span data-stu-id="c57fe-154">This call also publishes the project.</span></span>
    
<span data-ttu-id="c57fe-155">Fügen Sie den folgenden Code zwischen den **Script** -Tags, die Sie im Verfahren **zum Erstellen der Anwendungsseite in Visual Studio** hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="c57fe-155">Paste the following code between the **script** tags that you added in the **To create the application page in Visual Studio** procedure.</span></span> 
  
```js
    // Declare a global variable to store the project collection.
    var projects;
    // Ensure that the PS.js file is loaded before your custom code runs.
    SP.SOD.executeOrDelayUntilScriptLoaded(CreateProject, "PS.js");
    // Add a project the projects collection.
    function CreateProject() {
        
        // Initialize the current client context.
        var projContext = PS.ProjectContext.get_current();
        // Initialize a ProjectCreationInformation object and specify properties
        // for the new project.
        // The Name property is required and must be unique.
        var creationInfo = new PS.ProjectCreationInformation();
        creationInfo.set_name("Test Project 1");
        // Specify optional properties for the new project.
        // If not specified, the Start property uses the current date and the
        // EnterpriseProjectTypeId property uses the default EPT.
        creationInfo.set_description("Created through the JSOM.");
        creationInfo.set_start("2013-10-01 09:00:00.000");
        // Get the projects collection.
        projects = projContext.get_projects();
        // Add the new project to the projects collection.
        projects.add(creationInfo);
        // Add a second project to use in the deleting projects procedure.
        creationInfo.set_name("Test Project 2");
        projects.add(creationInfo);
        // Submit the request to update the collection on the server
        var updateJob = projects.update();
        projContext.waitForQueueAsync(updateJob, 10, GetProjects);
    }
    // Get the projects collection.
    function GetProjects(response) {
        // This call demonstrates that you can get the context from the 
        // ProjectCollection object.
        var projContext = projects.get_context();
        // Register the request for information that you want to run on the server.
        // This call includes an optional "Include" parameter to request only the Name, Description,
        // StartDate, and Id properties of the projects in the collection.
        projContext.load(projects, 'Include(Name, Description, StartDate, Id)');
        // Run the request on the server.
        projContext.executeQueryAsync(IterateThroughProjects, QueryFailed);
    }
    // Iterate through the projects collection.
    function IterateThroughProjects(response) {
        // Get the enumerator and iterate through the collection.
        var enumerator = projects.getEnumerator();
        while (enumerator.moveNext()) {
            var project = enumerator.get_current();
            // Create and populate a row with the values for the project's Name, Description,
            // StartDate, and Id properties.
            var row = tblProjects.insertRow();
            row.insertCell().innerText = project.get_name();
            row.insertCell().innerText = project.get_description();
            row.insertCell().innerText = project.get_startDate();
            row.insertCell().innerText = project.get_id();
        }
        // This scenario does not use the textarea or button controls.
        $get("txtGuid").disabled = true;
        $get("btnSend").disabled = true;
    }
    function QueryFailed(sender, args) {
        $get("spanMessage").innerText = 'Request failed: ' + args.get_message();
    }
```

## <a name="update-project-server-2013-projects-by-using-the-javascript-object-model"></a><span data-ttu-id="c57fe-156">Aktualisieren von Project Server 2013-Projekte mithilfe des JavaScript-Objektmodells</span><span class="sxs-lookup"><span data-stu-id="c57fe-156">Update Project Server 2013 projects by using the JavaScript object model</span></span>
<span data-ttu-id="c57fe-157"><a name="pj15_CRUDProjectsJSOM_UpdateProjects"> </a></span><span class="sxs-lookup"><span data-stu-id="c57fe-157"></span></span>

<span data-ttu-id="c57fe-158">Das Verfahren in diesem Abschnitt werden die **StartDate** -Eigenschaft eines Projekts mithilfe des JavaScript-Objektmodells aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="c57fe-158">The procedure in this section updates the **startDate** property of a project by using the JavaScript object model.</span></span> <span data-ttu-id="c57fe-159">Das Verfahren umfasst die folgenden allgemeinen Schritte:</span><span class="sxs-lookup"><span data-stu-id="c57fe-159">The procedure includes the following high-level steps:</span></span> 
  
1. <span data-ttu-id="c57fe-160">Rufen Sie die aktuelle Instanz **ProjectContext** .</span><span class="sxs-lookup"><span data-stu-id="c57fe-160">Get the current **ProjectContext** instance.</span></span> 
    
2. <span data-ttu-id="c57fe-161">Die veröffentlichten Projekte mithilfe der Funktion **ProjectContext.get_projects** vom Server ab.</span><span class="sxs-lookup"><span data-stu-id="c57fe-161">Retrieve the published projects from the server by using the **ProjectContext.get_projects** function.</span></span> <span data-ttu-id="c57fe-162">Die **Get_projects** -Funktion gibt ein **ProjectCollection** -Objekt zurück.</span><span class="sxs-lookup"><span data-stu-id="c57fe-162">The **get_projects** function returns a **ProjectCollection** object.</span></span> 
    
3. <span data-ttu-id="c57fe-163">Führen Sie die Anforderung auf dem Server mithilfe der **ProjectContext.load** und die **ProjectContext.executeQueryAsync** -Funktion.</span><span class="sxs-lookup"><span data-stu-id="c57fe-163">Run the request on the server by using the **ProjectContext.load** function and the **ProjectContext.executeQueryAsync** function.</span></span> 
    
4. <span data-ttu-id="c57fe-164">Rufen Sie ein **PublishedProject** -Objekt mithilfe der Funktion **ProjectContext.getById ab** .</span><span class="sxs-lookup"><span data-stu-id="c57fe-164">Retrieve a **PublishedProject** object by using the **ProjectContext.getById** function.</span></span> 
    
5. <span data-ttu-id="c57fe-165">Das Zielprojekt mithilfe der Funktion **Project.checkOut** auszuchecken.</span><span class="sxs-lookup"><span data-stu-id="c57fe-165">Check out the target project by using the **Project.checkOut** function.</span></span> <span data-ttu-id="c57fe-166">Die **CheckOut** -Funktion gibt die Entwurfsversion der veröffentlichten Projekt zurück.</span><span class="sxs-lookup"><span data-stu-id="c57fe-166">The **checkOut** function returns the draft version of the published project.</span></span> 
    
6. <span data-ttu-id="c57fe-167">Ändern Sie mithilfe der Funktion **DraftProject.set_startDate** Anfangstermin des Projekts.</span><span class="sxs-lookup"><span data-stu-id="c57fe-167">Change the project's start date by using the **DraftProject.set_startDate** function.</span></span> 
    
7. <span data-ttu-id="c57fe-168">Veröffentlichen Sie das Projekt mithilfe der **DraftProject.publish** und die **ProjectContext.waitForQueueAsync** -Funktion.</span><span class="sxs-lookup"><span data-stu-id="c57fe-168">Publish the project by using the **DraftProject.publish** function and the **ProjectContext.waitForQueueAsync** function.</span></span> <span data-ttu-id="c57fe-169">Die **Veröffentlichen** -Funktion gibt ein **QueueJob** -Objekt, das Sie an **WaitForQueueAsync**übergeben.</span><span class="sxs-lookup"><span data-stu-id="c57fe-169">The **publish** function returns a **QueueJob** object that you pass to **waitForQueueAsync**.</span></span>
    
<span data-ttu-id="c57fe-170">Fügen Sie den folgenden Code zwischen den **Script** -Tags, die Sie im Verfahren **zum Erstellen der Anwendungsseite in Visual Studio** hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="c57fe-170">Paste the following code between the **script** tags that you added in the **To create the application page in Visual Studio** procedure.</span></span> 
  
```js
    // Declare global variables.
    var projContext;
    var projects;
    // Ensure that the PS.js file is loaded before your custom code runs.
    SP.SOD.executeOrDelayUntilScriptLoaded(GetProjects, "PS.js");
    // Get the projects collection.
    function GetProjects() {
        // Initialize the current client context.
        projContext = PS.ProjectContext.get_current();
        // Get the projects collection.
        projects = projContext.get_projects();
        // Register the request for information that you want to run on the server.
        // This call includes an optional "Include" parameter to request only the Name, Description,
        // StartDate, and Id properties of the projects in the collection.
        projContext.load(projects, 'Include(Name, Description, StartDate, Id)');
        // Run the request on the server.
        projContext.executeQueryAsync(IterateThroughProjects, QueryFailed);
    }
    // Iterate through the projects collection.
    function IterateThroughProjects(response) {
        // Get the enumerator and iterate through the collection.
        var enumerator = projects.getEnumerator();
        while (enumerator.moveNext()) {
            var project = enumerator.get_current();
            // Create and populate a row with the values for the project's Name, Description,
            // StartDate, and Id properties.
            var row = tblProjects.insertRow();
            row.insertCell().innerText = project.get_name();
            row.insertCell().innerText = project.get_description();
            row.insertCell().innerText = project.get_startDate();
            row.insertCell().innerText = project.get_id();
        }
        // Initialize button properties.
        $get("btnSend").onclick = function () { ChangeProject(); };
        $get("btnSend").innerText = "Update";
    }
    // Change the project's start date.
    function ChangeProject() {
        // Get the identifier of the target project.
        var targetGuid = $get("txtGuid").innerText;
        // Get the target project and then check it out. The checkOut function
        // returns the draft version of the project.
        var project = projects.getById(targetGuid);
        var draftProject = project.checkOut();
        // Set the new property value and then publish the project.
        // Specify "true" to also check the project in.
        draftProject.set_startDate("2013-12-31 09:00:00.000");
        var publishJob = draftProject.publish(true);
        // Register the job that you want to run on the server and specify the
        // timeout duration and callback function.
        projContext.waitForQueueAsync(publishJob, 10, QueueJobSent);
    }
    // Print the JobState return code, which gives the status of the queue job.
    function QueueJobSent(response) {
        $get("spanMessage").innerText = 'JobState = ' + response + '. Wait a few seconds, then refresh the page to see your changes.';
    }
    function QueryFailed(sender, args) {
        $get("spanMessage").innerText = 'Request failed: ' + args.get_message();
    }
```

## <a name="delete-project-server-2013-projects-by-using-the-javascript-object-model"></a><span data-ttu-id="c57fe-171">Löschen von Project Server 2013-Projekten mithilfe des JavaScript-Objektmodells</span><span class="sxs-lookup"><span data-stu-id="c57fe-171">Delete Project Server 2013 projects by using the JavaScript object model</span></span>
<span data-ttu-id="c57fe-172"><a name="pj15_CRUDProjectsJSOM_DeleteProjects"> </a></span><span class="sxs-lookup"><span data-stu-id="c57fe-172"></span></span>

<span data-ttu-id="c57fe-173">Das Verfahren in diesem Abschnitt Löscht ein Projekt mithilfe des JavaScript-Objektmodells.</span><span class="sxs-lookup"><span data-stu-id="c57fe-173">The procedure in this section deletes a project by using the JavaScript object model.</span></span> <span data-ttu-id="c57fe-174">Das Verfahren umfasst die folgenden allgemeinen Schritte:</span><span class="sxs-lookup"><span data-stu-id="c57fe-174">The procedure includes the following high-level steps:</span></span>
  
1. <span data-ttu-id="c57fe-175">Rufen Sie die aktuelle Instanz **ProjectContext** .</span><span class="sxs-lookup"><span data-stu-id="c57fe-175">Get the current **ProjectContext** instance.</span></span> 
    
2. <span data-ttu-id="c57fe-176">Die veröffentlichten Projekte mithilfe der Funktion **ProjectContext.get_projects** vom Server ab.</span><span class="sxs-lookup"><span data-stu-id="c57fe-176">Retrieve the published projects from the server by using the **ProjectContext.get_projects** function.</span></span> <span data-ttu-id="c57fe-177">Die **Get_projects** -Funktion gibt ein **ProjectCollection** -Objekt zurück.</span><span class="sxs-lookup"><span data-stu-id="c57fe-177">The **get_projects** function returns a **ProjectCollection** object.</span></span> 
    
3. <span data-ttu-id="c57fe-178">Führen Sie die Anforderung auf dem Server mithilfe der **ProjectContext.load** und die **ProjectContext.executeQueryAsync** -Funktion.</span><span class="sxs-lookup"><span data-stu-id="c57fe-178">Run the request on the server by using the **ProjectContext.load** function and the **ProjectContext.executeQueryAsync** function.</span></span> 
    
4. <span data-ttu-id="c57fe-179">Rufen Sie ein **PublishedProject** -Objekt mithilfe der Funktion **ProjectCollection.getById ab** .</span><span class="sxs-lookup"><span data-stu-id="c57fe-179">Retrieve a **PublishedProject** object by using the **ProjectCollection.getById** function.</span></span> 
    
5. <span data-ttu-id="c57fe-180">Löschen Sie das Projekt, indem Sie es an die Funktion **ProjectCollection.remove** übergeben.</span><span class="sxs-lookup"><span data-stu-id="c57fe-180">Delete the project by passing it to the **ProjectCollection.remove** function.</span></span> 
    
6. <span data-ttu-id="c57fe-181">Aktualisieren Sie die Auflistung mithilfe der **ProjectCollection.update** und die **ProjectContext.waitForQueueAsync** -Funktion.</span><span class="sxs-lookup"><span data-stu-id="c57fe-181">Update the collection by using the **ProjectCollection.update** function and the **ProjectContext.waitForQueueAsync** function.</span></span> <span data-ttu-id="c57fe-182">Die **update** -Funktion gibt ein **QueueJob** -Objekt, das Sie an **WaitForQueueAsync**übergeben.</span><span class="sxs-lookup"><span data-stu-id="c57fe-182">The **update** function returns a **QueueJob** object that you pass to **waitForQueueAsync**.</span></span>
    
<span data-ttu-id="c57fe-183">Fügen Sie den folgenden Code zwischen den **Script** -Tags, die Sie im Verfahren **zum Erstellen der Anwendungsseite in Visual Studio** hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="c57fe-183">Paste the following code between the **script** tags that you added in the **To create the application page in Visual Studio** procedure.</span></span> 
  
```js
    // Declare global variables.
    var projContext;
    var projects;
    // Ensure that the PS.js file is loaded before your custom code runs.
    SP.SOD.executeOrDelayUntilScriptLoaded(GetProjects, "PS.js");
    // Get the projects collection.
    function GetProjects() {
        // Initialize the current client context.
        projContext = PS.ProjectContext.get_current();
        // Get the projects collection.
        projects = projContext.get_projects();
        // Register the request for information that you want to run on the server.
        // This call includes an optional "Include" parameter to request only the Name, Description,
        // StartDate, and Id properties of the projects in the collection.
        projContext.load(projects, 'Include(Name, Description, StartDate, Id)');
        // Run the request on the server.
        projContext.executeQueryAsync(IterateThroughProjects, QueryFailed);
    }
    // Iterate through the projects collection.
    function IterateThroughProjects(response) {
        // Get the enumerator and iterate through the collection.
        var enumerator = projects.getEnumerator();
        while (enumerator.moveNext()) {
            var project = enumerator.get_current();
            // Create and populate a row with the values for the project's Name, Description,
            // StartDate, and Id properties.
            var row = tblProjects.insertRow();
            row.insertCell().innerText = project.get_name();
            row.insertCell().innerText = project.get_description();
            row.insertCell().innerText = project.get_startDate();
            row.insertCell().innerText = project.get_id();
        }
        // Initialize button properties.
        $get("btnSend").onclick = function () { DeleteProject(); };
        $get("btnSend").innerText = "Delete";
    }
    // Delete the project.
    function DeleteProject() {
        // Get the identifier of the target project.
        var targetGuid = $get("txtGuid").innerText;
        // Get the target project and then remove it from the collection.
        var project = projects.getById(targetGuid);
        projects.remove(project);
        var removeJob = projects.update();
        // Register the job that you want to run on the server and specify the
        // timeout duration and callback function.
        projContext.waitForQueueAsync(removeJob, 10, QueueJobSent);
    }
    // Print the JobState return code, which gives the status of the queue job.
    function QueueJobSent(response) {
        $get("spanMessage").innerText = 'JobState = ' + response + '. Wait a few seconds, then refresh the page to see your changes.';
    }
    function QueryFailed(sender, args) {
        $get("spanMessage").innerText = 'Request failed: ' + args.get_message();
    }
```

<span data-ttu-id="c57fe-184"><a name="pj15_CRUDProjectsJSOM_AR"> </a></span><span class="sxs-lookup"><span data-stu-id="c57fe-184"></span></span>

## <a name="see-also"></a><span data-ttu-id="c57fe-185">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="c57fe-185">See also</span></span>

- [<span data-ttu-id="c57fe-186">Project-Programmieraufgaben</span><span class="sxs-lookup"><span data-stu-id="c57fe-186">Project programming tasks</span></span>](project-programming-tasks.md)
- [<span data-ttu-id="c57fe-187">Clientseitiges Objektmodell (CSOM) für Project 2013</span><span class="sxs-lookup"><span data-stu-id="c57fe-187">Client-side object model (CSOM) for Project 2013</span></span>](client-side-object-model-csom-for-project-2013.md)
    

