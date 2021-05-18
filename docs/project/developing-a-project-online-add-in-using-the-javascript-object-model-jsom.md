---
title: Entwickeln eines Project Online-Add-Ins mithilfe des JavaScript-Objektmodells (JSOM)
manager: soliver
ms.date: 11/08/2016
ms.audience: Developer
localization_priority: Normal
ms.assetid: 4a4b1ad2-de46-421d-a698-53c20c90b93a
description: In diesem Artikel wird Microsoft Project Online Add-In-Entwicklung beschrieben, um Ihre Erfahrung mit Project Online. Das Entwicklungsprojekt wird als exemplarische Vorgehensweise implementiert. Das für diesen Artikel verwendete Add-In liest und zeigt die Projektnamen und IDs der veröffentlichten Projekte aus Ihrem Project Online-Konto an und ermöglicht es Ihnen, einen Drilldown durchzuführen, um Aufgaben abzurufen, die einzelnen Projekten zugeordnet sind.
ms.openlocfilehash: 0a472a6300f18aaa65649f44d944445642a59e1a
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32322688"
---
# <a name="developing-a-project-online-add-in-using-the-javascript-object-model-jsom"></a>Entwickeln eines Project Online-Add-Ins mithilfe des JavaScript-Objektmodells (JSOM)

In diesem Artikel wird Microsoft Project Online Add-In-Entwicklung beschrieben, um Ihre Erfahrung mit dem Project Online. Das Entwicklungsprojekt wird als exemplarische Vorgehensweise implementiert. Das für diesen Artikel verwendete Add-In liest und zeigt die Projektnamen und IDs der veröffentlichten Projekte aus Ihrem Project Online-Konto an und ermöglicht es Ihnen, einen Drilldown durchzuführen, um Aufgaben abzurufen, die einzelnen Projekten zugeordnet sind.
  
Zur Laufzeit ähnelt der Add-In-Eintrag der folgenden Abbildung:
  
![Screenshot mit einer Auflistung von JSOM-Projekten und]-Aufgaben Screenshot mit einer Auflistung(media/766e5914-f048-48f4-9282-291f55e6e90d.png "von JSOM-Projekten und -Aufgaben")
  
Der Schwerpunkt des Beispiels liegt auf der Interaktion mit Project Online, abfragen und den Kontext für jede Anforderung vom Dienst festlegen. Benutzeroberflächenelemente erhalten minimale Aufmerksamkeit. Stattdessen enthalten die Quellauflistungen Kommentare zur Benutzeroberfläche.
  
> [!NOTE]
> Die Quelldateien für das Beispiel-Add-In, ein Visual Studio Projekt, sind unter verfügbar: https://github.com/OfficeDev/Project-JSOM-List-Projects-Tasks.... . Halten Sie die Quelldateien als Referenz bereit, während Sie den Artikel lesen, da jede die jeweils andere ergänzt. Die Dateien im Visual Studio und sind mit minimalen Änderungen ausführbar. Ersetzen Sie die URL für Ihren Project Online-Mandanten in den PWA Ordner. 
  
## <a name="background"></a>Hintergrund

Project Online ist ein Office 365-Dienst, der Unternehmen eine Projektportfolioverwaltungslösung (PPM) und eine Projektmanagementbürolösung (Project Management Office, PMO) zur Koordination und Verwaltung von Portfolios, Programmen und Projekten bietet. Project Online ist ein anderes Angebot als die Project Desktopeditionen. Dennoch enthält Project Online die Funktionalität zum Verwalten und Nachverfolgen von Projektdetails während der gesamten Lebensdauer eines Projekts. Project Online baut auf SharePoint Online auf.
  
Ein Project Online gehostetes Add-In besteht aus JavaScript- und Ressourcendateien, die mit der Client-Side-Object-Model-API interagieren. Wenn der Benutzer das Add-In besucht, werden JavaScript und Ressourcen im Browser heruntergeladen und ausgeführt. Das Add-In ruft asynchrone Aufrufe an Project Online, um mit dem Dienst zu interagieren, unabhängig davon, ob Daten erstellt, abgerufen, aktualisiert oder gelöscht werden. 
  
Project Online eine weitere Aktion zum Schutz von Informationen, die zu anderen Mandanten gehören, vor dem #A0 durch. Nämlich Project Online eine isolierte Website erstellt, um mit den Anforderungen des Add-Ins zu interagieren. Es wird kein benutzerdefinierter Code auf dem Project Online ausgeführt. 
  
Die Entwicklungseinrichtung für Project Online Add-Ins verwendet den Visual Studio SharePoint Add-In-Projekttyp. Das Add-In ist in JavaScript geschrieben und verwendet das Project JavaScript-Objektmodell (JSOM), um mit dem Project Online interagieren. Das JSOM erbt einen großen Teil seiner Funktionalität von der SharePoint JSOM.
  
> [!NOTE]
> Add-Ins können in der App veröffentlicht und verkauft Office Store oder in einem privaten App-Katalog auf einem SharePoint. Weitere Informationen finden Sie unter [Deploy and publish your Office Add-in](https://docs.microsoft.com/office/dev/add-ins/publish/publish).
> 
> Das in diesem Artikel verwendete #A0 ist ein Beispiel für Entwickler. Es ist nicht für die Verwendung in einer Produktionsumgebung vorgesehen. Der Hauptzweck besteht in einem Beispiel für die Entwicklung von Apps für Project Online. 
  
## <a name="prerequisites"></a>Voraussetzungen

Fügen Sie die folgenden Elemente zu einer unterstützten Windows hinzu:
  
- **.NET Framework 4.0 oder höher**: Vollständige Versionen des Frameworks ab Version 4.0 sind kompatibel. Die Download-Website ist https://msdn.microsoft.com/vstudio/aa496123.aspx.
    
- **Visual Studio 2013 oder höher**:  
    
   - Die professionelle Edition von Visual Studio 2015 ist sofort einsatzbereit und steht unter zur https://www.visualstudio.com/en-us/products/visual-studio-professional-with-msdn-vs.aspx Verfügung.
    
   - Die Community edition von Visual Studio 2015 ist unter https://www.visualstudio.com/en-us/products/visual-studio-community-vs.aspx verfügbar. Diese Edition erfordert die manuelle Installation der Microsoft Office Developer Tools für Visual Studio.
    
   Die Microsoft Office Developer Tools for Visual Studio sind unter https://www.visualstudio.com/en-us/features/office-tools-vs.aspx verfügbar.
    
- **Ein Project Online:** Dies ermöglicht den Zugriff auf den Hostingdienst. Weitere Informationen zum Einrichten eines Project Online-Kontos finden Sie unter https://products.office.com/en-us/Project/project-online-portfolio-management.
    
   Stellen Sie sicher, dass der Add-In-Benutzer über ausreichende Autorisierung für den Zugriff auf einige Projekte im Project Online verfügt. 
    
- **Projekte auf der Hostingwebsite,** die mit Informationen gefüllt sind.
    
> [!NOTE]
> Die Standard-.NET Framework ist das richtige Framework, das verwendet werden soll. Verwenden Sie nicht das ".NET Framework 4-Clientprofil". 
  
### <a name="set-up-the-visual-studio-project"></a>Einrichten des Visual Studio-Projekts

Die Anwendungseinrichtung besteht aus dem Erstellen eines neuen Projekts, dem Verknüpfen der entsprechenden Bibliotheken und dem Deklarieren der erforderlichen Namespaces. Visual Studio bietet verschiedene Typen von Entwicklungsprojekten. Der Abschnitt ist kurz und sehr einfach. Der Wert hat, dass die Informationen an einer Stelle verknurft werden.
  
#### <a name="select-a-visual-studio-project"></a>Auswählen eines Visual Studio-Projekts

Zum Erstellen eines Projekts des entsprechenden Typs für das Add-In müssen Sie die folgenden Schritte ausführen. Schlüsselwörter, die auf dem Bildschirm gefunden werden, haben ein **fett formatiertes** Attribut: 
  
1. Wählen Sie im Menü Datei die Option **Datei**  >    >  **Neu Project**. 
    
2. Wählen Sie im linken Bereich installierte Vorlagen C#  >  **Office/SharePoint**  >  **Web-Add-Ins aus.** 
    
3. Wählen Sie oben im zentralen Bereich **die Option .NET Framework 4** oder höher aus. die aktuelle Version ist 4.6. 
    
4. Wählen Sie in den Anwendungstypen im zentralen Bereich SharePoint **Add-In aus.** 
    
5. Geben Sie im unteren Abschnitt einen Namen und Speicherort für das Projekt und einen Projektmappennamen an. 
    
6. Aktivieren Sie außerdem im unteren Abschnitt das Kontrollkästchen **Projektmappenverzeichnis erstellen**. 
    
7. Klicken Sie auf **OK**, um das Ausgangsprojekt zu erstellen. 
    
Der Visual Studio-Assistent stellt in mehreren Dialogen einige Folgefragen zur Project Online-Einstellungswebsite (in den Dialogen als SharePoint-Einstellungen bezeichnet). Hier sind die Fragen:
  
1. Welche SharePoint möchten Sie zum Debuggen Ihres Add-Ins verwenden? Geben Sie die URL zu Ihrer PWA an, z. B. https://contoso.sharepoint.com/sites/pwa .
    
2. Wie möchten Sie Ihr SharePoint hosten? Wählen Sie [X] **SharePoint gehostet aus.**
    
   Weitere Informationen zu SharePoint Add-Ins, einschließlich Hostingoptionen, finden Sie [unter SharePoint Add-Ins](https://docs.microsoft.com/sharepoint/dev/sp-add-ins/sharepoint-add-ins).
    
3. Klicken Sie auf **Weiter**. 
    
Im zweiten zusätzlichen Dialogfeld werden Sie zum Angeben der SharePoint Onlineversion für das Add-In gefragt: 
  
1. Was ist die früheste Version von SharePoint, die Ihr Add-In als Ziel verwenden soll? Wählen Sie [X] S **harePoint-Online aus.** 
    
2. Klicken Sie auf **Fertig stellen**. 
    
Visual Studio erstellt das Projekt und zugrifft auf Project Online Website. 
  
### <a name="enable-sideloading-on-the-project-online-site"></a>Aktivieren des Querladens auf Project Online Website

Das Querladen ist der Mechanismus zum Testen und Debuggen Project Online Add-Ins. Sie benötigen zwei Skripts für das Querladen: eines zum Aktivieren des Querladens auf Ihrer Project Online-Website und ein weiteres zum Deaktivieren des Querladens, sobald Sie das Testen und Debuggen des Add-Ins abgeschlossen haben.
  
Weitere Informationen zum Einrichten des Querladens finden Sie unter [Enable app SideLoading in your non-developer site collection](https://blogs.msdn.microsoft.com/officeapps/2013/12/10/enable-app-sideloading-in-your-non-developer-site-collection/).
  
> [!NOTE]
> Das Querladen von Apps ist ein Entwickler-/Testfeature. Es ist **nicht für die Produktionsnutzung vorgesehen.** Laden Sie Apps nicht regelmäßig quer, oder halten Sie das Querladen von Apps länger aktiviert, als Sie das Feature aktiv verwenden. 
  
## <a name="add-content-to-the-add-in-project"></a>Hinzufügen von Inhalten zum Add-In-Projekt

Nach dem Erstellen eines Projekts und dem Einrichten des Debugmechanismus umfasst das Hinzufügen von Inhalt zur App die folgenden Aufgaben:
  
- Festlegen des Anwendungsumfangs
    
- Verknüpfen der JSOM-Bibliothek
    
- Hinzufügen von Benutzeroberflächenelementen zum Add-In
    
- Initialisieren und Herstellen einer Verbindung mit Project Online Dienst
    
- Abrufen von Projekten und Details/Eigenschaften
    
- Anzeigen von Projekten
    
- Anzeigen von Aufgaben für Project
    
Das Add-In-Projekt besteht aus vielen Dateien. In diesem Beispiel müssen Sie die folgenden Dateien bearbeiten: 
  
- AppManifest.xml
    
- Default.aspx
    
- App.js
    
- App.css – optional; enthält Formatdefinitionen, die für das Add-In entwickelt wurden
    
Wenn sich der Project Online-Mandant ändert, z. B. von einer Testversion zu einer Abonnementwebsite, können Sie die Projekteigenschaften, einschließlich der Serververbindung und der Website-URL, mithilfe des Eigenschaftenfensters aktualisieren, das über den Befehl Eigenschaftenfenster anzeigen verfügbar   >   ist. 
  
Sie können dem Projekt auch Dateien hinzufügen. Wenn ja, müssen Sie die Elements.xml in derselben Gruppe (Content, Images, Pages oder Scripts) aktualisieren, um die neuen Dateien zu enthalten. Weitere Informationen zu den Projektdateien finden Sie unter [Explore the app manifest structure and the package of a SharePoint Add-in](https://docs.microsoft.com/sharepoint/dev/sp-add-ins/explore-the-app-manifest-structure-and-the-package-of-a-sharepoint-add-in).
  
### <a name="set-application-scope"></a>Festlegen des Anwendungsumfangs

Das Add-In benötigt Bereiche oder Berechtigungsstufen, die definiert sind, bevor der Dienst Informationen in Abfrageergebnissen zurückgibt. Verwenden Sie für dieses Add-In den folgenden Bereich für das Visual Studio Projekt. Diese Änderung wird an der AppManifest.xml auf der Registerkarte Berechtigungen vorgenommen:

|Bereich|Berechtigung|
|:-----|:-----|
|Mehrere Projekte (Project Server)  <br/> |Lesen  <br/> |
   
Speichern Sie die Datei nach dem Festlegen des Anwendungsbereichs. Andernfalls werden keine Daten vom Dienst zurückgegeben. 
  
### <a name="link-the-jsom-library"></a>Verknüpfen der JSOM-Bibliothek

Die Laufzeitbibliotheken Project Online, PS.js und PS.debug.js, werden von Project Online bereitgestellt und sind immer die neueste Version. JavaScript-Add-Ins, die JSOM verwenden, müssen mit einer dieser Bibliotheken verknüpfen. Die Verknüpfungsdefinitionen werden in der Datei "Default.aspx" hinzugefügt. Die Befehle zur Verwendung der PS.js und/oder PS.debug.js sind Teil des Codes in der App.js Datei.
  
Fügen Sie den folgenden Befehl für PS.js oder PS.debug.js im Element hinzu, der `<asp:Content ContentPlaceHolderID="PlaceHolderAdditionalPageHead"` auf "SharePoint:ScriptLink" für sp.js. 
  
```js
<SharePoint:ScriptLink name="PS.js" runat="server" OnDemand="false" LoadAfterUI="true" Localizable="false" />
```

> [!NOTE]
> Das **OnDemand-Attribut** für PS.js oder PS.debug.js auf **false festgelegt.** 
  
### <a name="add-ui-elements-to-the-add-in"></a>Hinzufügen von Benutzeroberflächenelementen zum Add-In

Das Beispiel-Add-In besteht aus einigen Komponenten. Beschreibungen statischer Elemente befinden sich in der Datei "Default.aspx". Dynamische Elementbeschreibungen und Code für alle Komponenten befinden sich in der App.js Datei. Kommentare zu den Komponenten finden Sie in den Quellcodeauflistungen. Hier ist eine Liste der Benutzeroberflächenkomponenten im Add-In:
  
- Titel
    
- Einführungsverbiage
    
- Schaltfläche zum Entfernen von Aufgaben aus der Tabelle
    
- Tabelle, in der die Projekt-ID und der Name sowie die Vorgangsinformationen aufgeführt sind.
    
- Vorgangsschaltfläche (einmal für jedes Projekt geklont), die Vorgangsdaten in die Tabelle importiert.
    
Details zur Benutzeroberfläche, z. B. den Titel und den Kopfzeilenteil der Projekttabelle, finden Sie in der Projektdatei Default.aspx.
  
### <a name="initialize-and-connect-to-the-host-system"></a>Initialisieren und Herstellen einer Verbindung mit dem Hostsystem

Die App.js enthält den JavaScript-Code. Das Add-In lädt PS.js browser und ruft dann die initializePage-Funktion auf. InitializePage ruft einen Kontext für den Project Online ab und startet die loadProjects-Funktion.
  
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

Die loadProjects-Funktion fragt den Dienst nach den Projektnamen und IDs ab. 
  
Die Anwendung ruft den Projektnamen und die Projekt-ID ab. Weitere Informationen zum Projekt sind verfügbar und können durch Ändern der Load-Methode aufgerufen werden, um die abzurufenden Eigenschaften explizit zu identifizieren. Ein Beispiel wird im Code als Kommentar bereitgestellt. 
  
Wenn die Abfrage erfolgreich ist, wird das Add-In fortgesetzt, indem displayProjects aufruft. 
  
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

Die displayProjects-Funktion erstellt eine Tabelle, eine Zeile pro Projekt und eine Schaltfläche, um die Aufgaben für das spezifische Projekt zu zeigen. 
  
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
> Die while-Schleife zugrifft auf die EIGENSCHAFTEN ID und Name. Dies ist etwas anders als das Quellcodeprojekt, das eine Funktion aufruft, die wiederum auf dieselben Eigenschaften zu zugegriffen hat. 
  
### <a name="display-the-tasks-for-a-project"></a>Anzeigen der Vorgänge für ein Projekt

Die Aufgaben sind zwar Teil des Add-Ins, aber nicht Teil des anfänglichen Ladens. Wenn der Benutzer an den Aufgaben interessiert ist, die einem Projekt zugeordnet sind, bewirkt das Klicken auf die Schaltfläche "Aufgaben anzeigen", dass die Aufgaben mithilfe des btnLoadTasks-Ereignishandlers in der Liste angezeigt werden. 
  
Der btnLoadTasks-Ereignishandler mit der entsprechenden Projekt-ID fordert die Aufgaben für das angegebene Projekt vom Server an. Nach dem Abrufen übergibt btnLoadTasks die Aufgabenliste an displayTasks, um die Aufgaben auf dem Bildschirm zu präsentieren.
  
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

Die displayTasks-Funktion zeigt die Vorgänge an, die einem angegebenen Projekt direkt unterhalb des Projekteintrags zugeordnet sind.
  
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
> Die while-Schleife zugrifft auf die Aufgaben-ID und die Nameneigenschaften. Dies ist etwas anders als das Quellcodeprojekt, das eine Funktion aufruft, die wiederum auf dieselben Eigenschaften zu zugegriffen hat. 
  
Es folgt eine Beispielausgabe für die Aufgaben eines einzelnen Projekts.
  
![Screenshot der Ausgabe für eine Projektaufgabe](media/f6500a3f-000b-4f3e-9be6-9a74d0bea15e.png "Screenshot mit der Ausgabe für eine Projektaufgabe")
  
## <a name="see-also"></a>Siehe auch

Dokumentation und Beispiele zu Project Online und Anwendungsentwicklung mit CSOM finden Sie im [Project-Entwicklungsportal](https://developer.microsoft.com/en-us/project).
    


