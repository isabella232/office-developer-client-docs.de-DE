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
# <a name="developing-a-project-online-add-in-using-the-javascript-object-model-jsom"></a>Entwickeln eines Project Online add-Ins mithilfe der JavaScript-Objektmodell (JSOM)

In diesem Artikel wird beschrieben, Microsoft Project Online-Add-in-Entwicklung, um Ihre Erfahrung mit Project Online zu verbessern. Das Entwicklungsprojekt wird als eine exemplarische Vorgehensweise implementiert. Das Add-In für diesen Artikel verwendet liest und zeigt den Projektnamen und die veröffentlichten Projekte von Ihrem Konto Project Online-IDs und ermöglicht es Ihnen, einen Drilldown abrufen Aufgaben im Zusammenhang mit den einzelnen Projekten.
  
Zur Laufzeit aussieht in der folgenden Abbildung ähnlich die Add-in-Auflistung:
  
![Screenshot zeigt eine Liste von JSOM Projekten und Vorgängen] (media/766e5914-f048-48f4-9282-291f55e6e90d.png "Screenshot zeigt eine Liste von JSOM Projekten und Vorgängen")
  
Der Fokus des Beispiels wird die Interaktion mit dem Project Online, Abfragen und Festlegen des Kontexts für jede Anforderung aus dem Dienst. Elemente der Benutzeroberfläche (UI) empfangen minimale Aufmerksamkeit. Stattdessen bieten die Source-Auflistungen Kommentare bezüglich der Benutzeroberfläche.
  
> [!NOTE]
> Die Quelldateien für das Beispiel add-in, ein Visual Studio-Projekt sind verfügbar unter: https://github.com/OfficeDev/Project-JSOM-List-Projects-Tasks..... Halten Sie die Quelldateien bereit als Referenz beim Lesen des Artikels wie jeden anderen ergänzt. Die Dateien in der Visual Studio project Build und mit minimalen Änderungen ausführbar sind – ersetzen die URL für Ihren Project Online-Mandanten nach unten zu den PWA-Ordner. 
  
## <a name="background"></a>Hintergrund

Project Online ist ein Office 365-Dienst, der bietet Unternehmen eine Project Portfoliomanagement (PPM) und Project Management (PMO) Office-Lösung zu koordinieren und Verwalten von Portfolios, Programmen und Projekten. Project Online ist eine unterschiedliche besser als die Project-desktop-Versionen. noch enthält Project Online noch die Funktionalität zum Verwalten und Nachverfolgen von Projektdetails im Lebenszyklus eines Projekts. Project Online baut auf SharePoint Online.
  
Ein Project Online gehostet Add-in besteht aus JavaScript und Ressource-Dateien, die mit der Client-Side-Objektmodell-API interagieren. Wenn der Benutzer das Add-in besucht, werden die JavaScript und Ressourcen heruntergeladen und im Browser ausgeführt. Das Add-In wird asynchroner Aufrufe für Project Online mit dem Dienst interagieren, ob erstellen, abrufen, aktualisieren und Löschen von Daten. 
  
Project Online führt eine weitere Aktion zum Schutz von Informationen, die über das Add-in zu anderen Mandanten gehört. Project Online erstellt nämlich eine isolierte Website zur Interaktion mit den Anforderungen von das Add-in. Kein benutzerdefinierter Code ausgeführt wird, auf dem Project Online-Host. 
  
Die Einrichtung der Entwicklung für Project Online-add-ins verwendet den Projekttyp Visual Studio SharePoint-Add-in. Das Add-In wird in JavaScript geschrieben, und das Projekt JavaScript-Objektmodell (JSOM) für die Interaktion mit dem Project Online-Dienst verwendet. Die JSOM erbt Großteil der Funktionalität von der SharePoint JSOM.
  
> [!NOTE]
> -Add-ins können veröffentlicht und in den Office Store verkauft oder mit einem privaten app-Katalog in SharePoint bereitgestellt werden. Weitere Informationen finden Sie unter [Bereitstellen und veröffentlichen Sie Ihre Office-Add-in](https://docs.microsoft.com/en-us/office/dev/add-ins/publish/publish).
> 
> Das Add-in, das in diesem Artikel verwendeten ist ein Beispiel für Entwickler. Es ist nicht für die Verwendung in einer produktionsumgebung vorgesehen. Der primäre Zweck ist ein Beispiel für app-Entwicklung für Project Online angezeigt. 
  
## <a name="prerequisites"></a>Voraussetzungen

Fügen Sie die folgenden Elemente zu einer unterstützten Windows-Umgebung:
  
- **.NET Framework 4.0 oder höher**: vollständige Framework Version 4.0-Versionen kompatibel sind. Die Download-Website ist https://msdn.microsoft.com/en-us/vstudio/aa496123.aspx.
    
- **Visual Studio 2013 oder höher**:  
    
   - Die professional Edition von Visual Studio 2015 ist bereit zur ausgehend von der im Feld wechseln und finden Sie unter https://www.visualstudio.com/en-us/products/visual-studio-professional-with-msdn-vs.aspx.
    
   - Die Community-Edition von Visual Studio 2015 steht unter https://www.visualstudio.com/en-us/products/visual-studio-community-vs.aspx. Diese Edition erfordert die manuelle Installation von Microsoft Office Developer Tools für Visual Studio.
    
   Die Microsoft Office Developer Tools für Visual Studio stehen unter https://www.visualstudio.com/en-us/features/office-tools-vs.aspx.
    
- **Eine Project Online-Konto**: Dies ermöglicht den Zugriff auf die hosting-Dienst. Weitere Informationen dazu, wie Sie ein Konto mit Project Online erhalten, finden Sie unter https://products.office.com/en-us/Project/project-online-portfolio-management.
    
   Stellen Sie sicher, dass der Add-in-Benutzer über die erforderlichen Berechtigungen auf einige Projekte in Project Online-Mandanten zuzugreifen. 
    
- **Projekte auf der hosting-Website** , die mit Daten aufgefüllt werden.
    
> [!NOTE]
> Der Standard ist .NET Framework die richtige Framework verwendet werden. Verwenden Sie ".NET Framework 4 Client Profile" nicht. 
  
### <a name="set-up-the-visual-studio-project"></a>Einrichten des Visual Studio-Projekts

Erstellen eines neuen Projekts, verknüpfen die entsprechenden Bibliotheken und deklarieren die erforderlichen Namespaces besteht der Installation der Anwendung aus. Visual Studio stellt verschiedene Arten von Entwicklungsprojekten. Der Abschnitt ist kurz und elementare. Der Wert die Informationen Servercomputer ist an einem Ort gemischt zusammengefügt.
  
#### <a name="select-a-visual-studio-project"></a>Wählen Sie ein Visual Studio-Projekt

Wenn Sie ein Projekt des entsprechenden Typs für das Add-in erstellen, müssen Sie die folgenden Schritte durchführen. Schlüsselwörter aufgetreten ist, auf dem Bildschirm aufweisen eine **Fett** Attribut: 
  
1. Wählen Sie im Menü Datei die Option **Datei** > **New** > **Projekt**. 
    
2. Wählen Sie im linken Bereich die installierte Vorlagen ein **C#-** > **Office/SharePoint** > **Web-Add-ins**. 
    
3. Wählen Sie am oberen Rand der mittleren Bereich, **.NET Framework 4** oder höher; die aktuelle Version ist 4.6. 
    
4. Wählen Sie im mittleren Bereich Anwendungstypen **SharePoint-Add-in**. 
    
5. Geben Sie im unteren Bereich einen Namen und Speicherort für das Projekt, und einen Lösungsnamen. 
    
6. Auch im unteren Bereich das Kontrollkästchen Sie **Projektmappenverzeichnis erstellen** . 
    
7. Klicken Sie auf **OK** , um das ursprüngliche Projekt zu erstellen. 
    
Visual Studio-Assistenten stellt ein paar weitere Fragen zur Project Online Einstellungen-Website (gewählte SharePoint-Einstellungen in den Dialogfeldern) in eine Reihe von Dialogfeldern, die folgen. Es folgen die Fragen:
  
1. Welche SharePoint-Website möchten Sie für das debugging Ihrer-add-in? Geben Sie die URL der PWA-Website wie https://contoso.sharepoint.com/sites/pwa.
    
2. Wie möchten Sie Ihre SharePoint-Add-Ins hosten? Wählen Sie [X] **SharePoint gehostet**.
    
   Weitere Informationen zu SharePoint-Add-ins einschließlich hosting-Optionen finden Sie unter [SharePoint-Add-ins](https://docs.microsoft.com/en-us/sharepoint/dev/sp-add-ins/sharepoint-add-ins).
    
3. Klicken Sie auf **Weiter**. 
    
Das zweite zusätzliche Dialogfeld aufgefordert, geben Sie die SharePoint Online-Version für das Add-in: 
  
1. Was ist die erste Version von SharePoint, die Ihr Add-in zum Ziel soll? Wählen Sie [X] S **HarePoint Online**. 
    
2. Klicken Sie auf **Fertig stellen**. 
    
Visual Studio erstellt das Projekt und greift auf die Project Online-Website. 
  
### <a name="enable-sideloading-on-the-project-online-site"></a>Aktivieren Sie auf der Website Project Online sideloading

Sideloading ist der Mechanismus zum Testen und Debuggen Project Online-add-ins. Benötigen Sie zwei Skripts für Sideloading: eine Sideloading auf Ihre Project Online-Website und eine andere Sideloading zu deaktivieren, sobald Sie fertig sind, testen und Debuggen das Add-in zu aktivieren.
  
Weitere Informationen zum Einrichten von Sideloading finden Sie unter [app in Ihrer Websitesammlung Nichtentwickler SideLoading aktivieren](https://blogs.msdn.microsoft.com/officeapps/2013/12/10/enable-app-sideloading-in-your-non-developer-site-collection/).
  
> [!NOTE]
> Sideloading apps ist ein Entwickler/Test-Feature. Es ist **nicht für die Verwendung in der Produktion vorgesehenen**. Führen Sie nicht Sideload apps regelmäßig aus, oder behalten Sie app-Sideloading für mehr als Sie das Feature aktiv verwenden aktiviert. 
  
## <a name="add-content-to-the-add-in-project"></a>Hinzufügen von Inhalt zum Projekt-Add-in

Nach dem Erstellen eines Projekts und Einrichten des debugging-Mechanismus, umfasst Hinzufügen von Inhalt für die app die folgenden Aufgaben aus:
  
- Festlegen des Anwendungsbereichs
    
- Verknüpfen der JSOM-Bibliothek
    
- Hinzufügen von UI-Elemente für das Add-in
    
- Initialisieren und beim Verbinden mit dem Project Online-Dienst
    
- Abrufen von Projekten und Details-Eigenschaften
    
- Anzeigen von Projekten
    
- Anzeigen von Aufgaben für ein Projekt
    
Das Add-In-Projekt umfasst viele Dateien. In diesem Beispiel benötigen Sie die folgenden Dateien zu bearbeiten: 
  
- AppManifest.xml
    
- "Default.aspx"
    
- App.js
    
- "App.CSS" - optional; enthält Formatvorlagendefinitionen, die für das Add-in entwickelt
    
Wenn der Mandant Project Online ändert wie das Wechseln von einer Testversion zu einer Abonnement-Website können Sie die Projekteigenschaften, einschließlich der Server-Verbindung und die URL der Website aktualisieren, im Eigenschaftenfenster die **Ansicht**zur Verfügung > **Eigenschaften Fenster** Befehl. 
  
Sie können auch Dateien zum Projekt hinzufügen. Ist dies der Fall ist, müssen Sie die Datei "Elements.xml" befindet sich in der gleichen Gruppe (Inhalt, Bilder, Seiten oder Skripts) umfassen die neuen Dateien zu aktualisieren. Weitere Informationen zu den Projektdateien finden Sie unter [Untersuchen der app-manifest-Struktur und des Pakets über ein SharePoint-Add-in](https://docs.microsoft.com/en-us/sharepoint/dev/sp-add-ins/explore-the-app-manifest-structure-and-the-package-of-a-sharepoint-add-in).
  
### <a name="set-application-scope"></a>Set-Anwendungsbereich

Das Add-in benötigt Bereichs oder Berechtigung Ebenen definiert werden, bevor der Dienst Informationen in Abfrageergebnissen zurückgegeben wird. Verwenden Sie für dieses Add-in den folgenden Bereich für die Visual Studio-Projekt. Diese Änderung wird auf der Registerkarte Berechtigungen die Datei AppManifest.XML vorgenommen:

|Umfang|Berechtigung|
|:-----|:-----|
|Mehrere Projekte (Projektserver)  <br/> |Lesen  <br/> |
   
Speichern Sie die Datei nach dem Festlegen des Gültigkeitsbereichs der Anwendung. Andernfalls werden keine Daten aus dem Dienst zurückgegeben werden. 
  
### <a name="link-the-jsom-library"></a>Verknüpfen der JSOM-Bibliothek

Die Laufzeit Project Online Bibliotheken, PS.js und PS.debug.js, werden von Project Online bereitgestellt und sind immer die aktuellste Version. JavaScript-add-ins, die JSOM verwenden, müssen mit einer dieser Bibliotheken verknüpfen. Die Verknüpfung Definitionen sind in der Datei "default.aspx" hinzugefügt. Die Befehle, um die PS.js und/oder PS.debug.js zu verwenden sind Teil des Codes befindet sich in der Datei App.js.
  
Fügen Sie den folgenden Befehl für die PS.js oder PS.debug.js in der `<asp:Content ContentPlaceHolderID="PlaceHolderAdditionalPageHead"` Element folgt "SharePoint:ScriptLink" für sp.js. 
  
```js
<SharePoint:ScriptLink name="PS.js" runat="server" OnDemand="false" LoadAfterUI="true" Localizable="false" />
```

> [!NOTE]
> Das Attribut **OnDemand** für PS.js oder PS.debug.js festlegen auf **false festgelegt**. 
  
### <a name="add-ui-elements-to-the-add-in"></a>Hinzufügen von UI-Elemente für das Add-in

Das Beispiel-add-in umfasst einige Komponenten. Statische elementbeschreibungen befinden sich in der Datei Default.aspx. Dynamische elementbeschreibungen und Code für alle Komponenten befinden sich in der Datei App.js. Kommentare zu den Komponenten finden Sie in der Quelle Codebeispiele. Es folgt eine Liste der Komponenten der Benutzeroberfläche in das Add-in:
  
- Titel
    
- Einführende Textpassagen
    
- Schaltfläche, um Aufgaben aus der Tabelle entfernen
    
- Tabelle, die die Projekt-ID und Name und die Informationen zum Vorgang aufgeführt sind.
    
- Aufgaben Schaltfläche (einmal für jedes Projekt geklont), die in der Tabelle Vorgangsdaten importiert.
    
Details der Benutzeroberfläche, wie den Titel und den Header Teil der Projekttabelle finden Sie die Datei "default.aspx" Projekt.
  
### <a name="initialize-and-connect-to-the-host-system"></a>Initialisieren und eine Verbindung mit dem Host-system

Die Datei App.js enthält den JavaScript-Code. Das Add-In lädt PS.js im Browser und ruft dann die Funktion InitializePage. InitializePage Ruft einen Kontext an den Endpunkt Project Online und startet die LoadProjects-Funktion.
  
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

Die Funktion LoadProjects fragt den Dienst für den Projektnamen und IDs. 
  
Die Anwendung ruft den Projektnamen und die Project-Id. Weitere Informationen über das Projekt ist verfügbar und durch Ändern der Load-Methode, um die Eigenschaften zum Abrufen explizit ermitteln zugegriffen werden kann. Ein Beispiel wird im Code als Kommentar bereitgestellt. 
  
Wenn die Abfrage erfolgreich ist, wird das Add-in durch Aufrufen von DisplayProjects fortgesetzt. 
  
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

Die Funktion DisplayProjects erstellt eine Tabelle, eine Zeile pro Projekt und eine Schaltfläche, um die Vorgänge für bestimmte Projekte angezeigt werden. 
  
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
> Die While-Schleife greift auf die ID und Name-Eigenschaft. Dies ist geringfügig Quellcodeprojekt an, das eine Funktion aufruft, die wiederum die gleichen Eigenschaften zugreift. 
  
### <a name="display-the-tasks-for-a-project"></a>Die Aufgaben für ein Projekt anzeigen

Die Aufgaben beim Teil des Add-Ins, sind nicht Teil der anfänglichen laden. Wenn der Benutzer die Aufgaben im Zusammenhang mit einem Projekt interessiert ist, wird durch Klicken auf die Schaltfläche "Aufgaben anzeigen" die Aufgaben in der Liste mit dem BtnLoadTasks-Ereignishandler anzuzeigen. 
  
Im BtnLoadTasks-Ereignishandler mit der entsprechenden Project-ID, fordert die Aufgaben für das angegebene Projekt vom Server. Nachdem abgerufen, übergibt BtnLoadTasks die Aufgabenliste an DisplayTasks, die auf dem Bildschirm Aufgaben durchzuführen.
  
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

Die Funktion DisplayTasks zeigt Aufgaben im Zusammenhang mit ein angegebenes Projekt unmittelbar unterhalb des Eintrags Projekt.
  
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
> Die While-Schleife greift auf die Vorgangs-ID und Name-Eigenschaft. Dies ist geringfügig Quellcodeprojekt an, das eine Funktion aufruft, die wiederum die gleichen Eigenschaften zugreift. 
  
Beispielausgabe für die Aufgaben eines einzelnen Projekts folgt.
  
![Screenshot zeigt die Ausgabe für eine Projektaufgabe] (media/f6500a3f-000b-4f3e-9be6-9a74d0bea15e.png "Screenshot zeigt die Ausgabe für eine Projektaufgabe")
  
## <a name="see-also"></a>Siehe auch

Dokumentation und Beispiele im Zusammenhang mit Project Online und die Anwendungsentwicklung mithilfe von CSOM finden Sie im [Projekt Development Portal](https://developer.microsoft.com/en-us/project).
    


