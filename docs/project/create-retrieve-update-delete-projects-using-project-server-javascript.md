---
title: Erstellen, abrufen, aktualisieren und Löschen von Projekten mit Project Server JavaScript
manager: soliver
ms.date: 08/10/2016
ms.audience: Developer
localization_priority: Normal
ms.assetid: 6b690938-05bc-46a3-a40e-30f081403767
description: Abrufen der aktuellen Instanz ProjectContext; Rufen Sie ab und durchlaufen Sie die Auflistung der veröffentlichten Projekte auf dem Server. Erstellen, abrufen, Auschecken und Löschen eines Projekts mithilfe der Project Server-JavaScript-Objektmodells; und ändern Sie die Eigenschaften des Projekts.
ms.openlocfilehash: 10dac7edfa3e84cebfd0585bc8c4bff1ea22ea44
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/04/2018
ms.locfileid: "25382911"
---
# <a name="create-retrieve-update-and-delete-projects-using-project-server-javascript"></a>Erstellen, abrufen, aktualisieren und Löschen von Projekten mit Project Server JavaScript

Die Szenarien in diesem Artikel wird gezeigt, wie die aktuelle Instanz **ProjectContext** abgerufen; Rufen Sie ab und durchlaufen Sie die Auflistung der veröffentlichten Projekte auf dem Server. Erstellen, abrufen, Auschecken und Löschen eines Projekts mithilfe der Project Server-JavaScript-Objektmodells; und ändern Sie die Eigenschaften des Projekts. 
  
> [!NOTE]
> Diese Szenarien Definieren von benutzerdefiniertem Code im Markup eine SharePoint-Anwendungsseite verwenden jedoch kein Code-Behind-Datei, mit der Visual Studio 2012 erstellt für die Seite. 
  
## <a name="prerequisites-for-working-with-project-server-2013-projects-in-the-javascript-object-model"></a>Voraussetzungen für das Arbeiten mit Project Server 2013-Projekten in der JavaScript-Objektmodell

Um die beschriebenen Szenarien in diesem Artikel durchführen, müssen Sie installieren und konfigurieren die folgenden Produkte:
  
- SharePoint Server 2013
- Project Server 2013
- Visual Studio 2012
- Office Developer Tools für Visual Studio 2012
    
Sie benötigen auch Berechtigungen zum Bereitstellen der Erweiterung zu SharePoint Server 2013 und zur Teilnahme an Projekten.
  
> [!NOTE]
> Diese Anweisungen wird davon ausgegangen, dass Sie auf dem Computer entwickeln, die Project Server 2013 ausgeführt wird. 
  
## <a name="create-the-visual-studio-solution"></a>Erstellen der Visual Studio-Projektmappe
<a name="pj15_CRUDProjectsJSOM_Setup"> </a>

Die folgenden Schritte erstellen Sie eine Visual Studio 2012-Lösung, die ein SharePoint-Projekt und einer Anwendungsseite enthält. Die Seite enthält die Logik für das Arbeiten mit Projekten.
  
### <a name="to-create-the-sharepoint-project-in-visual-studio"></a>Zum Erstellen von SharePoint-Projekt in Visual Studio

1. Führen Sie auf dem Computer, auf der Project Server 2013 ausgeführt wird, Visual Studio 2012 als Administrator.
    
2. Klicken Sie in der Menüleiste auf **Datei**, **Neu**, **Projekt**.
    
3. Wählen Sie im Dialogfeld **Neues Projekt** aus der Dropdownliste oben im Dialogfeld die Option **.NET Framework 4.5**. 
    
4. Wählen Sie in der Kategorie **Office/SharePoint** -Vorlage **SharePoint-Lösungen**, und wählen Sie dann die Vorlage **SharePoint 2013-Projekts** . 
    
5. Nennen Sie das Projekt ProjectsJSOM, und wählen Sie dann auf die Schaltfläche **OK** . 
    
6. Klicken Sie im **Assistenten zum Anpassen von SharePoint**-Dialogfeld Wählen Sie **als Farmlösung bereitstellen**, und wählen Sie dann auf die Schaltfläche **Fertig stellen**. 
    
7. Bearbeiten Sie den Wert der Eigenschaft **Website-URL** für das Projekt **ProjectsJSOM** entsprechend die URL der Project Web App-Instanz (z. B. `https://ServerName/PWA`).
    
### <a name="to-create-the-application-page-in-visual-studio"></a>Zum Erstellen der Anwendungsseite in Visual Studio

1. Im **Projektmappen-Explorer**das Kontextmenü für das Projekt **ProjectsJSOM** öffnen, und fügen Sie eine SharePoint "Layouts" Ordner zugeordnet. 
    
2. Öffnen Sie im Ordner **Layouts** das Kontextmenü für den Ordner **ProjectsJSOM** , und fügen Sie eine neue SharePoint-Anwendungsseite namens ProjectsList.aspx.
    
3. Öffnen Sie das Kontextmenü für die Seite **ProjectsList.aspx** , und wählen Sie **als Startelement festlegen**.
    
4. Definieren Sie Benutzeroberflächen-Steuerelemente in den "Main" **Asp: Content** -Tags im Markup für die Seite **ProjectsList.aspx** wie folgt. 
    
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
   > Diese Steuerelemente können nicht in jedem Szenario verwendet werden. Beispielsweise wird das Szenario "Projekte erstellen" die **Schaltfläche** und **Textarea** -Steuerelemente nicht verwendet. 
  
5. Nach der schließenden **span** markieren, fügen Sie wie folgt ein **SharePoint:ScriptLink** -Tag, ein Tag **SharePoint:FormDigest** und **Script** -Tags hinzu. 
    
   ```HTML
    <SharePoint:ScriptLink id="ScriptLink" name="PS.js" runat="server" ondemand="false" localizable="false" loadafterui="true" />
    <SharePoint:FormDigest id="FormDigest" runat="server" />
    <script type="text/javascript">
        // Replace this comment with the code for your scenario.
    </script>
   ```

   Das Tag **SharePoint:ScriptLink** verweist auf die Datei PS.js, die das JavaScript-Objektmodell für Project Server 2013 definiert. Das **SharePoint:FormDigest** -Tag generiert einen Nachrichtenhash für die sicherheitsüberprüfung bei Bedarf von Operationen, die Server-Inhalte zu aktualisieren. 
    
6. Ersetzen Sie den Kommentar Platzhalter durch den Code aus einem der folgenden Verfahren aus:
    
   - [Erstellen von Project Server 2013-Projekten mithilfe des JavaScript-Objektmodells](#pj15_CRUDProjectsJSOM_CreateProjects)
    
   - [Aktualisieren von Project Server 2013-Projekte mithilfe des JavaScript-Objektmodells](#pj15_CRUDProjectsJSOM_UpdateProjects)
    
   - [Löschen von Project Server 2013-Projekten mithilfe des JavaScript-Objektmodells](#pj15_CRUDProjectsJSOM_DeleteProjects)
    
7. Wählen Sie zum Testen der Anwendungsseite in der Menüleiste **Debuggen**, **Debuggen starten**aus. Wenn Sie aufgefordert werden, ändern Sie die Datei "Web.config", und wählen Sie **OK**.
    
## <a name="create-project-server-2013-projects-by-using-the-javascript-object-model"></a>Erstellen von Project Server 2013-Projekten mithilfe des JavaScript-Objektmodells
<a name="pj15_CRUDProjectsJSOM_CreateProjects"> </a>

Das Verfahren in diesem Abschnitt werden Projekte mithilfe des JavaScript-Objektmodells erstellt. Das Verfahren umfasst die folgenden allgemeinen Schritte:
  
1. Rufen Sie die aktuelle Instanz **ProjectContext** . 
    
2. Erstellen Sie ein **ProjectCreationInformation** -Objekt, um die anfängliche Eigenschaften für Ihr Projekt angeben. Geben Sie die erforderlichen **Name** -Eigenschaft mithilfe der **ProjectCreationInformation.set_name** -Funktion. 
    
3. Die veröffentlichten Projekte mithilfe der Funktion **ProjectContext.get_projects** vom Server ab. Die **Get_projects** -Funktion gibt ein **ProjectCollection** -Objekt zurück. 
    
4. Fügen Sie das neue Projekt zur Auflistung hinzu, indem Sie mithilfe der **ProjectCollection.add** -Funktion und im **ProjectCreationInformation** -Objekt übergeben. 
    
5. Aktualisieren Sie die Auflistung mithilfe der **ProjectCollection.update** und die **ProjectContext.waitForQueueAsync** -Funktion. Die **update** -Funktion gibt ein **QueueJob** -Objekt, das Sie an **WaitForQueueAsync**übergeben. Dieses Anrufs veröffentlicht auch das Projekt.
    
Fügen Sie den folgenden Code zwischen den **Script** -Tags, die Sie im Verfahren **zum Erstellen der Anwendungsseite in Visual Studio** hinzugefügt. 
  
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

## <a name="update-project-server-2013-projects-by-using-the-javascript-object-model"></a>Aktualisieren von Project Server 2013-Projekte mithilfe des JavaScript-Objektmodells
<a name="pj15_CRUDProjectsJSOM_UpdateProjects"> </a>

Das Verfahren in diesem Abschnitt werden die **StartDate** -Eigenschaft eines Projekts mithilfe des JavaScript-Objektmodells aktualisiert. Das Verfahren umfasst die folgenden allgemeinen Schritte: 
  
1. Rufen Sie die aktuelle Instanz **ProjectContext** . 
    
2. Die veröffentlichten Projekte mithilfe der Funktion **ProjectContext.get_projects** vom Server ab. Die **Get_projects** -Funktion gibt ein **ProjectCollection** -Objekt zurück. 
    
3. Führen Sie die Anforderung auf dem Server mithilfe der **ProjectContext.load** und die **ProjectContext.executeQueryAsync** -Funktion. 
    
4. Rufen Sie ein **PublishedProject** -Objekt mithilfe der Funktion **ProjectContext.getById ab** . 
    
5. Das Zielprojekt mithilfe der Funktion **Project.checkOut** auszuchecken. Die **CheckOut** -Funktion gibt die Entwurfsversion der veröffentlichten Projekt zurück. 
    
6. Ändern Sie mithilfe der Funktion **DraftProject.set_startDate** Anfangstermin des Projekts. 
    
7. Veröffentlichen Sie das Projekt mithilfe der **DraftProject.publish** und die **ProjectContext.waitForQueueAsync** -Funktion. Die **Veröffentlichen** -Funktion gibt ein **QueueJob** -Objekt, das Sie an **WaitForQueueAsync**übergeben.
    
Fügen Sie den folgenden Code zwischen den **Script** -Tags, die Sie im Verfahren **zum Erstellen der Anwendungsseite in Visual Studio** hinzugefügt. 
  
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

Das Verfahren in diesem Abschnitt Löscht ein Projekt mithilfe des JavaScript-Objektmodells. Das Verfahren umfasst die folgenden allgemeinen Schritte:
  
1. Rufen Sie die aktuelle Instanz **ProjectContext** . 
    
2. Die veröffentlichten Projekte mithilfe der Funktion **ProjectContext.get_projects** vom Server ab. Die **Get_projects** -Funktion gibt ein **ProjectCollection** -Objekt zurück. 
    
3. Führen Sie die Anforderung auf dem Server mithilfe der **ProjectContext.load** und die **ProjectContext.executeQueryAsync** -Funktion. 
    
4. Rufen Sie ein **PublishedProject** -Objekt mithilfe der Funktion **ProjectCollection.getById ab** . 
    
5. Löschen Sie das Projekt, indem Sie es an die Funktion **ProjectCollection.remove** übergeben. 
    
6. Aktualisieren Sie die Auflistung mithilfe der **ProjectCollection.update** und die **ProjectContext.waitForQueueAsync** -Funktion. Die **update** -Funktion gibt ein **QueueJob** -Objekt, das Sie an **WaitForQueueAsync**übergeben.
    
Fügen Sie den folgenden Code zwischen den **Script** -Tags, die Sie im Verfahren **zum Erstellen der Anwendungsseite in Visual Studio** hinzugefügt. 
  
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
    

