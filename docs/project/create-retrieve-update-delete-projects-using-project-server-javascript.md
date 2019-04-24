---
title: Erstellen, abrufen, aktualisieren und Löschen von Projekten mithilfe von Project Server JavaScript
manager: soliver
ms.date: 08/10/2016
ms.audience: Developer
localization_priority: Normal
ms.assetid: 6b690938-05bc-46a3-a40e-30f081403767
description: Rufen Sie die aktuelle Projectcontext-Instanz ab; Abrufen und durchlaufen der Auflistung der veröffentlichten Projekte auf dem Server; Erstellen, abrufen, Auschecken und Löschen eines Projekts mithilfe des Project Server-JavaScript-Objektmodells; und Ändern der Eigenschaften eines Projekts.
ms.openlocfilehash: 10dac7edfa3e84cebfd0585bc8c4bff1ea22ea44
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32322666"
---
# <a name="create-retrieve-update-and-delete-projects-using-project-server-javascript"></a>Erstellen, abrufen, aktualisieren und Löschen von Projekten mithilfe von Project Server JavaScript

In den Szenarien in diesem Artikel wird gezeigt, wie Sie **** die aktuelle projectcontext-Instanz abrufen. Abrufen und durchlaufen der Auflistung der veröffentlichten Projekte auf dem Server; Erstellen, abrufen, Auschecken und Löschen eines Projekts mithilfe des Project Server-JavaScript-Objektmodells; und Ändern der Eigenschaften eines Projekts. 
  
> [!NOTE]
> Diese Szenarien definieren benutzerdefinierten Code im Markup einer SharePoint-Anwendungsseite, verwenden jedoch nicht die Code-Behind-Datei, die Visual Studio 2012 für die Seite erstellt. 
  
## <a name="prerequisites-for-working-with-project-server-2013-projects-in-the-javascript-object-model"></a>VoraussetZungen für das Arbeiten mit Project Server 2013-Projekten im JavaScript-Objektmodell

Um die in diesem Artikel beschriebenen Szenarien ausführen zu können, müssen Sie die folgenden Produkte installieren und konfigurieren:
  
- SharePoint Server 2013
- Project Server 2013
- Visual Studio 2012
- Office Developer Tools für Visual Studio 2012
    
Sie müssen außerdem über die Berechtigung verfügen, die Erweiterung auf SharePoint Server 2013 bereitzustellen und zu Projekten beizutragen.
  
> [!NOTE]
> Bei diesen Anweisungen wird davon ausgegangen, dass Sie auf dem Computer mit Project Server 2013 entwickeln. 
  
## <a name="create-the-visual-studio-solution"></a>Erstellen der Visual Studio-Lösung
<a name="pj15_CRUDProjectsJSOM_Setup"> </a>

In den folgenden Schritten wird eine Visual Studio 2012-Lösung erstellt, die ein SharePoint-Projekt und eine Anwendungsseite enthält. Die Seite enthält die Logik für das Arbeiten mit Projekten.
  
### <a name="to-create-the-sharepoint-project-in-visual-studio"></a>So erstellen Sie das SharePoint-Projekt in Visual Studio

1. Führen Sie auf dem Computer, auf dem Project Server 2013 ausgeführt wird, Visual Studio 2012 als Administrator aus.
    
2. Klicken Sie in der Menüleiste auf **Datei**, **Neu**, **Projekt**.
    
3. Wählen Sie im Dialogfeld **Neues Projekt** aus der Dropdownliste oben im Dialogfeld die Option **.NET Framework 4.5**. 
    
4. Wählen Sie in der Kategorie **Office/Share** Point-Vorlagen die Option **SharePoint-Lösungen**, und wählen Sie dann die **SharePoint 2013-Projekt** Vorlage aus. 
    
5. Nennen Sie das Projekt ProjectsJSOM, und klicken Sie dann auf die Schaltfläche **OK** . 
    
6. Wählen Sie in das Dialogfeld des **Assistenten zum Anpassen von SharePoint** **als farmlösung bereitstellen**, und wählen Sie dann auf die Schaltfläche **Fertig stellen**. 
    
7. Bearbeiten Sie den Wert der **Website-URL** -Eigenschaft für das **ProjectsJSOM** -Projekt mit der URL der Project Web App-Instanz (Beispiels `https://ServerName/PWA`Weise).
    
### <a name="to-create-the-application-page-in-visual-studio"></a>So erstellen Sie die Anwendungsseite in Visual Studio

1. Öffnen Sie im projektMappen- **Explorer**das Kontextmenü für das **ProjectsJSOM** -Projekt, und fügen Sie dann einen zugeordneten SharePoint-Layouts hinzu. 
    
2. Öffnen Sie im Ordner **Layouts** das Kontextmenü für den Ordner **ProjectsJSOM** , und fügen Sie dann eine neue SharePoint-Anwendungsseite mit dem Namen projects. aspx hinzu.
    
3. Öffnen Sie das Kontextmenü für die Seite projects **. aspx** , und wählen Sie **als Startelement festlegen**aus.
    
4. Definieren Sie im Markup für die Seite **projectlist. aspx** die Steuerelemente der Benutzeroberfläche innerhalb der **ASP: Content** -Tags von "Main" wie folgt. 
    
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
   > Diese Steuerelemente können nicht in jedem Szenario verwendet werden. Beispielsweise verwendet das Szenario "Projekte erstellen" nicht die **Textarea** -und **Button** -Steuerelemente. 
  
5. Fügen Sie nach dem schließenden **Span** -Tag wie folgt ein **SharePoint: ScriptLink** -Tag, ein **SharePoint: FormDigest** -Tag und **Script** -Tags hinzu. 
    
   ```HTML
    <SharePoint:ScriptLink id="ScriptLink" name="PS.js" runat="server" ondemand="false" localizable="false" loadafterui="true" />
    <SharePoint:FormDigest id="FormDigest" runat="server" />
    <script type="text/javascript">
        // Replace this comment with the code for your scenario.
    </script>
   ```

   Das **SharePoint: ScriptLink** -Tag verweist auf die Datei "PS. js", die das JavaScript-Objektmodell für Project Server 2013 definiert. Das **SharePoint:FormDigest** -Tag generiert einen Nachrichtenhash für die Sicherheitsüberprüfung bei Bedarf von Operationen, die den Inhalt zu aktualisieren. 
    
6. Ersetzen Sie den Platzhalter Kommentar durch den Code aus einem der folgenden Verfahren:
    
   - [Erstellen von Project Server 2013-Projekten mithilfe des JavaScript-Objektmodells](#pj15_CRUDProjectsJSOM_CreateProjects)
    
   - [Aktualisieren von Project Server 2013-Projekten mithilfe des JavaScript-Objektmodells](#pj15_CRUDProjectsJSOM_UpdateProjects)
    
   - [Löschen von Project Server 2013-Projekten mithilfe des JavaScript-Objektmodells](#pj15_CRUDProjectsJSOM_DeleteProjects)
    
7. Um die Anwendungsseite zu testen, wählen Sie in der Menüleiste die Optionen **Debuggen**, **Debuggen starten**. Wenn Sie aufgefordert werden, die Datei Web. config zu ändern, klicken Sie auf **OK**.
    
## <a name="create-project-server-2013-projects-by-using-the-javascript-object-model"></a>Erstellen von Project Server 2013-Projekten mithilfe des JavaScript-Objektmodells
<a name="pj15_CRUDProjectsJSOM_CreateProjects"> </a>

Das Verfahren in diesem Abschnitt erstellt Projekte mithilfe des JavaScript-Objektmodells. Das Verfahren umfasst die folgenden allgemeinen Schritte:
  
1. Rufen Sie die **** aktuelle projectcontext-Instanz ab. 
    
2. Erstellen Sie ein **ProjectCreationInformation** -Objekt, um die anfänglichen Eigenschaften für das Projekt anzugeben. Geben Sie die erforderliche **Name** -Eigenschaft mithilfe der **ProjectCreationInformation. Set _Name** -Funktion an. 
    
3. Rufen Sie die veröffentlichten Projekte mithilfe der **projectcontext. Get _projects** -Funktion vom Server ab. Die **get_Projects** -Funktion gibt ein **ProjectCollection** -Objekt zurück. 
    
4. Fügen Sie das neue Projekt der Auflistung hinzu, indem Sie die **ProjectCollection. Add** -Funktion verwenden und das **ProjectCreationInformation** -Objekt übergeben. 
    
5. Aktualisieren Sie die Auflistung mithilfe der **ProjectCollection. Update** -Funktion und der **Projectcontext. waitForQueueAsync** -Funktion. Die **Update** -Funktion gibt ein **QueueJob** -Objekt zurück, das Sie an **waitForQueueAsync**. Dieser Aufruf veröffentlicht auch das Projekt.
    
Fügen Sie den folgenden Code zwischen den **Script** -Tags ein, die Sie in der **Visual Studio-Prozedur zur Seite zum Erstellen der Anwendung** hinzugefügt haben. 
  
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

## <a name="update-project-server-2013-projects-by-using-the-javascript-object-model"></a>Aktualisieren von Project Server 2013-Projekten mithilfe des JavaScript-Objektmodells
<a name="pj15_CRUDProjectsJSOM_UpdateProjects"> </a>

Das Verfahren in diesem Abschnitt aktualisiert die **StartDate** -Eigenschaft eines Projekts mithilfe des JavaScript-Objektmodells. Das Verfahren umfasst die folgenden allgemeinen Schritte: 
  
1. Rufen Sie die **** aktuelle projectcontext-Instanz ab. 
    
2. Rufen Sie die veröffentlichten Projekte mithilfe der **projectcontext. Get _projects** -Funktion vom Server ab. Die **get_Projects** -Funktion gibt ein **ProjectCollection** -Objekt zurück. 
    
3. Führen Sie die Anforderung auf dem Server mithilfe der **projectcontext. Laden** -Funktion und der **Projectcontext. executeQueryAsync** -Funktion aus. 
    
4. Ruft ein **"publishedproject"** -Objekt mithilfe der **projectcontext. getById-** Funktion ab. 
    
5. Checken Sie das Zielprojekt mithilfe der **Project. checkOut** -Funktion aus. Die **checkOut** -Funktion gibt die Entwurfsversion des veröffentlichten Projekts zurück. 
    
6. Ändern Sie den Anfangstermin des Projekts mithilfe der **DraftProject. Set _startdate** -Funktion. 
    
7. Veröffentlichen Sie das Projekt mithilfe der **DraftProject. Publish** -Funktion und der **Projectcontext. waitForQueueAsync** -Funktion. Die **Publish** -Funktion gibt ein **QueueJob** -Objekt zurück, das Sie an **waitForQueueAsync**.
    
Fügen Sie den folgenden Code zwischen den **Script** -Tags ein, die Sie in der **Visual Studio-Prozedur zur Seite zum Erstellen der Anwendung** hinzugefügt haben. 
  
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

## <a name="delete-project-server-2013-projects-by-using-the-javascript-object-model"></a>Löschen von Project Server 2013-Projekten mithilfe des JavaScript-Objektmodells
<a name="pj15_CRUDProjectsJSOM_DeleteProjects"> </a>

Mit dem Verfahren in diesem Abschnitt wird ein Projekt mithilfe des JavaScript-Objektmodells gelöscht. Das Verfahren umfasst die folgenden allgemeinen Schritte:
  
1. Rufen Sie die **** aktuelle projectcontext-Instanz ab. 
    
2. Rufen Sie die veröffentlichten Projekte mithilfe der **projectcontext. Get _projects** -Funktion vom Server ab. Die **get_Projects** -Funktion gibt ein **ProjectCollection** -Objekt zurück. 
    
3. Führen Sie die Anforderung auf dem Server mithilfe der **projectcontext. Laden** -Funktion und der **Projectcontext. executeQueryAsync** -Funktion aus. 
    
4. Ruft ein **"publishedproject"** -Objekt mithilfe der **ProjectCollection. getById** -Funktion ab. 
    
5. Löschen Sie das Projekt, indem Sie es an die **ProjectCollection. Remove** -Funktion übergeben. 
    
6. Aktualisieren Sie die Auflistung mithilfe der **ProjectCollection. Update** -Funktion und der **Projectcontext. waitForQueueAsync** -Funktion. Die **Update** -Funktion gibt ein **QueueJob** -Objekt zurück, das Sie an **waitForQueueAsync**.
    
Fügen Sie den folgenden Code zwischen den **Script** -Tags ein, die Sie in der **Visual Studio-Prozedur zur Seite zum Erstellen der Anwendung** hinzugefügt haben. 
  
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

<a name="pj15_CRUDProjectsJSOM_AR"> </a>

## <a name="see-also"></a>Siehe auch

- [Project-Programmieraufgaben](project-programming-tasks.md)
- [Clientseitiges Objektmodell (CSOM) für Project 2013](client-side-object-model-csom-for-project-2013.md)
    

