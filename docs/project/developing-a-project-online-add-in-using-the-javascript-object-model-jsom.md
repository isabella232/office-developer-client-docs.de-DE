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
# <a name="developing-a-project-online-add-in-using-the-javascript-object-model-jsom"></a>Entwickeln eines Project Online-Add-Ins mithilfe des JavaScript-Objektmodells (JSOM)

In diesem Artikel wird die Microsoft Project Online-Add-in-Entwicklung beschrieben, um Ihre Erfahrung mit dem Projekt online zu verbessern. Das Entwicklungsprojekt wird als Exemplarische Vorgehensweise implementiert. Das Add-in, das für diesen Artikel verwendet wird, liest und zeigt die Projektnamen und-IDs der veröffentlichten Projekte aus Ihrem Project Online-Konto an und ermöglicht Ihnen das Abrufen von Aufgaben, die einzelnen Projekten zugeordnet sind.
  
Zur Laufzeit sieht das Add-in-Listing ähnlich wie in der folgenden Abbildung aus:
  
![Screenshot mit einer Liste von JSOM-Projekten und-Aufgaben] (media/766e5914-f048-48f4-9282-291f55e6e90d.png "Screenshot mit einer Liste von JSOM-Projekten und-Aufgaben")
  
Der Schwerpunkt des Beispiels ist die Interaktion mit dem Projekt online, das Abfragen und Festlegen des Kontexts für jede Anforderung vom Dienst. Benutzeroberflächenelemente (UI) erhalten nur minimale Aufmerksamkeit. Stattdessen enthalten die Quellauflistungen Kommentare zur Benutzeroberfläche.
  
> [!NOTE]
> Die Quelldateien für das Beispiel-Add-in, ein Visual Studio-Projekt, sind verfügbar https://github.com/OfficeDev/Project-JSOM-List-Projects-Tasks....unter:. Halten Sie die Quelldateien als Referenz bereit, während Sie den Artikel lesen, da jeder die andere ergänzt. Die Dateien in der Visual Studio-Projekt erstellen und sind mit minimalen Änderungen ausführbar-ersetzen die URL für Ihren Project Online-Mandanten in den Ordner PWA. 
  
## <a name="background"></a>Hintergrund

Project Online ist ein Office 365-Dienst, der Unternehmen eine Projektportfolio Verwaltung (PPM) und Projektmanagement Office (PMO) bietet, um Portfolios, Programme und Projekte zu koordinieren und zu verwalten. Project Online ist ein anderes Angebot als die Project Desktop-Editionen; Project Online enthält jedoch weiterhin die Funktionalität, um Projektdetails während der gesamten Lebensdauer eines Projekts zu verwalten und nachzuverfolgen. Project Online basiert auf SharePoint Online.
  
Ein gehostetes Project Online-Add-in besteht aus JavaScript-und Ressourcendateien, die mit der Client seitigen Objektmodell-API interagieren. Wenn der Benutzer das Add-in besucht, werden JavaScript und Ressourcen im Browser heruntergeladen und ausgeführt. Das Add-in führt asynchrone Aufrufe von Project Online aus, um mit dem Dienst zu interagieren, sei es das Erstellen, abrufen, aktualisieren oder Löschen von Daten. 
  
Project Online führt eine weitere Aktion aus, um Informationen zu schützen, die anderen Mandanten des Add-ins gehören. in Project Online wird nämlich eine isolierte Website erstellt, die mit den Anforderungen des Add-ins interagiert. Auf dem Project Online-Host wird kein benutzerdefinierter Code ausgeführt. 
  
Das Entwicklungs Setup für Project Online-Add-Ins verwendet den Projekttyp Visual Studio SharePoint-Add-in. Das Add-in ist in JavaScript geschrieben und verwendet das Project-JavaScript-Objektmodell (JSOM) für die Interaktion mit dem Project Online-Dienst. Der JSOM erbt einen Großteil seiner Funktionalität von der SharePoint-JSOM.
  
> [!NOTE]
> Add-Ins können im Office Store veröffentlicht und verkauft oder in einem privaten App-Katalog auf SharePoint bereitgestellt werden. Weitere Informationen finden Sie unter [bereitstellen und Veröffentlichen Ihres Office-Add-ins](https://docs.microsoft.com/office/dev/add-ins/publish/publish).
> 
> Das in diesem Artikel verwendete Add-in ist ein Beispiel für Entwickler; Es ist nicht für die Verwendung in einer Produktionsumgebung vorgesehen. Der Hauptzweck besteht darin, ein Beispiel für die APP-Entwicklung für Project online zu zeigen. 
  
## <a name="prerequisites"></a>Voraussetzungen

Fügen Sie der unterstützten Windows-Umgebung die folgenden Elemente hinzu:
  
- **.NET framework 4,0 oder höher**: vollständige Versionen des Frameworks ab Version 4,0 sind kompatibel. Die Download-Website ist https://msdn.microsoft.com/vstudio/aa496123.aspx.
    
- **Visual Studio 2013 oder höher**:  
    
   - Die Professional Edition von Visual Studio 2015 ist Soforteinsatz bereit und ist verfügbar unter https://www.visualstudio.com/en-us/products/visual-studio-professional-with-msdn-vs.aspx.
    
   - Die Community-Edition von Visual Studio 2015 ist verfügbar https://www.visualstudio.com/en-us/products/visual-studio-community-vs.aspxunter. Diese Edition erfordert die manuelle Installation der Microsoft Office Developer Tools für Visual Studio.
    
   Die Microsoft Office Developer Tools für Visual Studio sind verfügbar unter https://www.visualstudio.com/en-us/features/office-tools-vs.aspx.
    
- **Ein Project Online-Konto**: Dadurch wird der Zugriff auf den Hostdienst ermöglicht. Weitere Informationen zum Einrichten eines Project Online-Kontos finden Sie unter https://products.office.com/en-us/Project/project-online-portfolio-management.
    
   Stellen Sie sicher, dass der Add-in-Benutzer über ausreichende Autorisierung für den Zugriff auf einige Projekte im Project Online-Mandanten verfügt. 
    
- **Projekte auf der Hostwebsite** , die mit Informationen aufgefüllt werden.
    
> [!NOTE]
> Das standardmäßige .NET Framework ist das richtige Framework für die Verwendung. Verwenden Sie nicht das ".NET Framework 4-Client Profil". 
  
### <a name="set-up-the-visual-studio-project"></a>Einrichten des Visual Studio-Projekts

Das Anwendungssetup umfasst das Erstellen eines neuen Projekts, das Verknüpfen der entsprechenden Bibliotheken und das Deklarieren der benötigten Namespaces. Visual Studio bietet verschiedene Typen von Entwicklungsprojekten. Der Abschnitt ist kurz und sehr einfach. Der Wert besteht darin, dass die Informationen an einem Ort verschmolzen werden.
  
#### <a name="select-a-visual-studio-project"></a>Auswählen eines Visual Studio-Projekts

Führen Sie die folgenden Schritte aus, um ein Projekt vom geeigneten Typ für das Add-in zu erstellen. Auf dem Bildschirm aufgetretene Schlüsselwörter weisen ein **Bold** -Attribut auf: 
  
1. Wählen Sie im Menü Datei die Option **Datei** > **Neues** > **Projekt**aus. 
    
2. Wählen Sie im linken Bereich unter installierte Vorlagen die Option **C#** > -**Office/SharePoint** > -**Web-Add-ins**aus. 
    
3. Wählen Sie oben im zentralen Bereich **.NET Framework 4** oder höher aus. die aktuelle Version ist 4,6. 
    
4. Wählen Sie in den Anwendungstypen im zentralen Bereich **SharePoint-Add-in**aus. 
    
5. Geben Sie im unteren Abschnitt einen Namen und Speicherort für das Projekt und einen Projektmappennamen an. 
    
6. Aktivieren Sie außerdem im unteren Abschnitt das Kontrollkästchen **Projektmappenverzeichnis erstellen**. 
    
7. Klicken Sie auf **OK**, um das Ausgangsprojekt zu erstellen. 
    
Der Visual Studio-Assistent stellt in einigen folgenden Dialogfeldern einige weitere Fragen zur Project Online-einstellungswebsite (die als SharePoint-Einstellungen in den Dialogfeldern bezeichnet werden) bereit. Hier sind die Fragen:
  
1. Welche SharePoint-Website soll für das Debuggen des Add-Ins verwendet werden? Geben Sie die URL ihrer PWA-Website an, https://contoso.sharepoint.com/sites/pwabeispielsweise.
    
2. Wie soll Ihr SharePoint-Add-in gehostet werden? Wählen Sie [X] von **SharePoint gehostet**.
    
   Weitere Informationen zu SharePoint-Add-Ins, einschließlich Hosting-Optionen, finden Sie unter [SharePoint-Add-ins](https://docs.microsoft.com/sharepoint/dev/sp-add-ins/sharepoint-add-ins).
    
3. Klicken Sie auf **Weiter**. 
    
Im zweiten zusätzlichen Dialogfeld werden Sie aufgefordert, die SharePoint Online-Version für das Add-in anzugeben: 
  
1. Was ist die früheste Version von SharePoint, die das Add-in als Ziel haben soll? Wählen Sie [X] S **harePoint-Online**aus. 
    
2. Klicken Sie auf **Fertig stellen**. 
    
Visual Studio erstellt das Projekt und greift auf die Project Online-Website zu. 
  
### <a name="enable-sideloading-on-the-project-online-site"></a>Aktivieren von querladen auf der Project Online-Website

Querladen ist der Mechanismus zum Testen und Debuggen von Project Online-Add-Ins. Sie benötigen zwei Skripts für querladen: eine, um querladen auf Ihrer Project Online-Website zu aktivieren, und eine andere, um querladen zu deaktivieren, nachdem Sie das Testen und Debuggen des Add-Ins abgeschlossen haben.
  
Weitere Informationen zum Einrichten von querladen finden Sie unter [enable App querladen in your Non-Developer Site Collection](https://blogs.msdn.microsoft.com/officeapps/2013/12/10/enable-app-sideloading-in-your-non-developer-site-collection/).
  
> [!NOTE]
> Querladen-Apps ist eine Entwickler/Test-Funktion. Es ist **nicht für die Verwendung in der Produktion vorgesehen**. Querladen Sie apps nicht regelmäßig, oder halten Sie App querladen länger aktiviert, als Sie das Feature aktiv verwenden. 
  
## <a name="add-content-to-the-add-in-project"></a>Hinzufügen von Inhalt zum Add-in-Projekt

Nach dem Erstellen eines Projekts und dem Einrichten des Debugging-Mechanismus umfasst das Hinzufügen von Inhalt zur APP die folgenden Aufgaben:
  
- Festlegen des Anwendungsbereichs
    
- Verknüpfen der JSOM-Bibliothek
    
- Hinzufügen von Benutzeroberflächenelementen zum Add-in
    
- Initialisieren und Herstellen einer Verbindung mit dem Project Online-Dienst
    
- Abrufen von Projekten und Details/Eigenschaften
    
- Anzeigen von Projekten
    
- Anzeigen von Aufgaben für ein Projekt
    
Das Add-in-Projekt besteht aus zahlreichen Dateien. In diesem Beispiel müssen Sie die folgenden Dateien bearbeiten: 
  
- Datei AppManifest. XML
    
- Default. aspx
    
- App. js
    
- App. CSS – optional; enthält Formatvorlagendefinitionen für das Add-in
    
Wenn sich der Project Online-Mandant ändert, wie beispielsweise das Wechseln von einer Testversion zu einer Abonnement Website, können Sie die Projekteigenschaften einschließlich der Server Verbindung und der Website-URL mithilfe des Eigenschaftenfensters, das über die **Ansichts** > Eigenschaften verfügbar ist, aktualisieren.** Fenster** Befehl. 
  
Sie können dem Projekt auch Dateien hinzufügen. Wenn dies der Fall ist, müssen Sie die Datei "Elements. xml" in derselben Gruppe (Inhalt, Bilder, Seiten oder Skripts) so aktualisieren, dass Sie die neuen Dateien enthält. Weitere Informationen zu den Projektdateien finden Sie unter [erkunden der APP-Manifeststruktur und des Pakets eines SharePoint-Add-ins](https://docs.microsoft.com/sharepoint/dev/sp-add-ins/explore-the-app-manifest-structure-and-the-package-of-a-sharepoint-add-in).
  
### <a name="set-application-scope"></a>Festlegen des Anwendungsbereichs

Das Add-in benötigt Bereichs-oder Berechtigungsstufen, die definiert werden, bevor der Dienstinformationen in Abfrageergebnissen zurückgibt. Verwenden Sie für dieses Add-in den folgenden Bereich für das Visual Studio-Projekt. Diese Änderung wird in der Datei Datei AppManifest. XML auf der Registerkarte Berechtigungen vorgenommen:

|Bereich|Berechtigung|
|:-----|:-----|
|Mehrere Projekte (Project Server)  <br/> |Lesen  <br/> |
   
Speichern Sie die Datei, nachdem Sie den Anwendungsbereich festgelegt haben. Andernfalls werden vom Dienst keine Daten zurückgegeben. 
  
### <a name="link-the-jsom-library"></a>Verknüpfen der JSOM-Bibliothek

Die Laufzeit-Project Online-Bibliotheken, PS. js und PS. Debug. js, werden von Project Online bereitgestellt und sind immer die neueste Version. JavaScript-Add-Ins, die JSOM verwenden, müssen mit einer dieser Bibliotheken verknüpft sein. Die Verknüpfungs Definitionen werden in der Datei "default. aspx" hinzugefügt. Die Befehle zur Verwendung von PS. js und/oder PS. Debug. js sind Teil des Codes in der Datei "App. js".
  
Fügen Sie den folgenden Befehl für die Definition PS. js oder PS. Debug. js `<asp:Content ContentPlaceHolderID="PlaceHolderAdditionalPageHead"` im Element nach dem "SharePoint: ScriptLink" für SP. js hinzu. 
  
```js
<SharePoint:ScriptLink name="PS.js" runat="server" OnDemand="false" LoadAfterUI="true" Localizable="false" />
```

> [!NOTE]
> Das **OnDemand** -Attribut für PS. js oder PS. Debug. js ist auf **false**festgelegt. 
  
### <a name="add-ui-elements-to-the-add-in"></a>Hinzufügen von Benutzeroberflächenelementen zum Add-in

Das Beispiel-Add-in besteht aus einigen Komponenten. Beschreibungen statischer Elemente befinden sich in der Datei default. aspx. Dynamische Elementbeschreibungen und Code für alle Komponenten befinden sich in der Datei "App. js". Kommentare zu den Komponenten finden Sie in den Quell Codeauflistungen. Es folgt eine Liste der Benutzeroberflächenkomponenten im Add-in:
  
- Position
    
- Einführung in Wortschwall
    
- Schaltfläche zum Entfernen von Aufgaben aus der Tabelle
    
- Tabelle, in der die Projekt-ID und der Name sowie die Vorgangsinformationen aufgeführt sind.
    
- Aufgabenschaltfläche (für jedes Projekt einmal geklont), die Aufgabendaten in die Tabelle importiert.
    
Details zur Benutzeroberfläche, wie Titel und Kopfzeilen Bereich der Project-Tabelle, finden Sie in der Project-Standarddatei.
  
### <a name="initialize-and-connect-to-the-host-system"></a>Initialisieren und Herstellen einer Verbindung mit dem Hostsystem

Die Datei app. js enthält den JavaScript-Code. Das Add-in lädt PS. js im Browser und ruft dann die initializePage-Funktion auf. InitializePage Ruft einen Kontext zum Project Online-Endpunkt ab und startet die loadProjects-Funktion.
  
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

### <a name="retrieve-the-projects"></a>Abrufen der Projekte

Die loadProjects-Funktion fragt den Dienst nach den Projektnamen und-IDs ab. 
  
Die Anwendung ruft den Projektnamen und die Projekt-ID ab. Weitere Informationen zum Projekt stehen zur Verfügung, und Sie können durch Ändern der Lademethode darauf zugreifen, um explizit die abzurufenden Eigenschaften zu identifizieren. Ein Beispiel wird im Code als Kommentar angegeben. 
  
Wenn die Abfrage erfolgreich ist, wird das Add-in weiterhin durch Aufrufen von displayProjects. 
  
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

### <a name="display-the-projects"></a>Anzeigen der Projekte

Die displayProjects-Funktion erstellt eine Tabelle, eine Zeile pro Projekt und eine Schaltfläche, um die Aufgaben für das jeweilige Projekt anzuzeigen. 
  
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
> Die while-Schleife greift auf die Eigenschaften ID und Name zu. Dies unterscheidet sich geringfügig vom Quellcodeprojekt, das eine Funktion aufruft, die wiederum auf dieselben Eigenschaften zugreift. 
  
### <a name="display-the-tasks-for-a-project"></a>Anzeigen der Aufgaben für ein Projekt

Die Aufgaben, während ein Teil des Add-Ins nicht Teil des anfänglichen Ladens ist. Wenn der Benutzer an den mit einem Projekt verknüpften Vorgängen interessiert ist, werden durch Klicken auf die Schaltfläche Aufgaben anzeigen in der Liste mithilfe des btnLoadTasks-Ereignishandlers angezeigt. 
  
Der btnLoadTasks-Ereignishandler mit der entsprechenden Projekt-ID fordert die Aufgaben für das angegebene Projekt vom Server an. Nach dem Abrufen übergibt btnLoadTasks die Aufgabenliste an Display Tasks, um die Aufgaben auf dem Bildschirm darzustellen.
  
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

Mit der Display Tasks-Funktion werden die Aufgaben angezeigt, die einem angegebenen Projekt unmittelbar unterhalb des Projekteintrags zugeordnet sind.
  
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
> Die while-Schleife greift auf die Eigenschaften Vorgangs-ID und Name zu. Dies unterscheidet sich geringfügig vom Quellcodeprojekt, das eine Funktion aufruft, die wiederum auf dieselben Eigenschaften zugreift. 
  
Die Beispielausgabe für die Aufgaben eines einzelnen Projekts folgt.
  
![Screenshot mit der Ausgabe für eine Projektaufgabe] (media/f6500a3f-000b-4f3e-9be6-9a74d0bea15e.png "Screenshot mit der Ausgabe für eine Projektaufgabe")
  
## <a name="see-also"></a>Siehe auch

Dokumentation und Beispiele zu Project Online und Anwendungsentwicklung mit CSOM finden Sie im [Project-Entwicklungsportal](https://developer.microsoft.com/en-us/project).
    


