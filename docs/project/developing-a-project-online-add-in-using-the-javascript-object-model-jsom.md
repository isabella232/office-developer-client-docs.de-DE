---
title: Entwickeln eines Project Online-Add-Ins mithilfe des JavaScript-Objektmodells (JSOM)
manager: soliver
ms.date: 11/08/2016
ms.audience: Developer
ms.localizationpriority: medium
ms.assetid: 4a4b1ad2-de46-421d-a698-53c20c90b93a
description: In diesem Artikel wird Microsoft Project Online Add-In-Entwicklung beschrieben, um Ihre Erfahrung mit Project Online zu verbessern. Das Entwicklungsprojekt wird als exemplarische Vorgehensweise implementiert. Das in diesem Artikel verwendete Add-In liest und zeigt die Projektnamen und IDs der veröffentlichten Projekte aus Ihrem Project Online Konto an und ermöglicht es Ihnen, einen Drilldown zum Abrufen von Aufgaben auszuführen, die einzelnen Projekten zugeordnet sind.
ms.openlocfilehash: b30350a0d78531e304545e551ff61257e52386e8
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59560221"
---
# <a name="developing-a-project-online-add-in-using-the-javascript-object-model-jsom"></a>Entwickeln eines Project Online-Add-Ins mithilfe des JavaScript-Objektmodells (JSOM)

In diesem Artikel wird Microsoft Project Online Add-In-Entwicklung beschrieben, um Ihre Erfahrung mit der Project Online zu verbessern. Das Entwicklungsprojekt wird als exemplarische Vorgehensweise implementiert. Das in diesem Artikel verwendete Add-In liest und zeigt die Projektnamen und IDs der veröffentlichten Projekte aus Ihrem Project Online Konto an und ermöglicht es Ihnen, einen Drilldown zum Abrufen von Aufgaben auszuführen, die einzelnen Projekten zugeordnet sind.
  
Zur Laufzeit sieht der Add-In-Eintrag ähnlich der folgenden Abbildung aus:
  
![Screenshot mit einer Auflistung der JSOM-Projekte und -Aufgaben](media/766e5914-f048-48f4-9282-291f55e6e90d.png "Screenshot mit einer Auflistung der JSOM-Projekte und -Aufgaben")
  
Der Schwerpunkt des Beispiels liegt auf der Interaktion mit dem Project Online, dem Durchführen von Abfragen und dem Festlegen des Kontexts für jede Anforderung vom Dienst. Elemente der Benutzeroberfläche (UI) erhalten minimale Aufmerksamkeit. Stattdessen enthalten die Quelleinträge Kommentare zur Benutzeroberfläche.
  
> [!NOTE]
> Die Quelldateien für das Beispiel-Add-In, ein Visual Studio-Projekt, sind verfügbar unter: https://github.com/OfficeDev/Project-JSOM-List-Projects-Tasks.... . Halten Sie die Quelldateien als Referenz bereit, während Sie den Artikel lesen, da jeder die anderen ergänzt. Die Dateien im Visual Studio Projektbuild und werden mit minimalen Änderungen ausführbar. Dadurch wird die URL für Ihren Project Online Mandanten bis zum PWA Ordners substituiert. 
  
## <a name="background"></a>Hintergrund

Project Online ist ein Office 365 Dienst, der Unternehmen eine Projektportfolioverwaltungslösung (PPM) und eine Projektmanagement-Bürolösung (Project Management Office, PMO) bereitstellt, um Portfolio, Programme und Projekte zu koordinieren und zu verwalten. Project Online unterscheidet sich von den Project Desktopeditionen. Project Online enthält jedoch weiterhin die Funktionalität zum Verwalten und Nachverfolgen von Projektdetails während der gesamten Lebensdauer eines Projekts. Project Online basiert auf SharePoint Online.
  
Ein Project Online gehosteten Add-In besteht aus JavaScript- und Ressourcendateien, die mit der clientseitigen Objektmodell-API interagieren. Wenn der Benutzer das Add-In besucht, werden JavaScript und Ressourcen im Browser heruntergeladen und ausgeführt. Das Add-In führt asynchrone Aufrufe an Project Online aus, um mit dem Dienst zu interagieren, unabhängig davon, ob Daten erstellt, abgerufen, aktualisiert oder gelöscht werden. 
  
Project Online führt eine weitere Aktion aus, um Informationen, die zu anderen Mandanten gehören, vor dem Add-In zu schützen. nämlich erstellt Project Online eine isolierte Website, um mit den Anforderungen des Add-Ins zu interagieren. Auf dem Project Online Host wird kein benutzerdefinierter Code ausgeführt. 
  
Das Entwicklungssetup für Project Online-Add-Ins verwendet den Visual Studio SharePoint Add-In-Projekttyp. Das Add-In ist in JavaScript geschrieben und verwendet das Project JavaScript-Objektmodell (JSOM), um mit dem Project Online Dienst zu interagieren. Das JSOM erbt einen Großteil seiner Funktionalität vom SharePoint JSOM.
  
> [!NOTE]
> Add-Ins können im Office Store veröffentlicht und verkauft oder in einem privaten App-Katalog auf SharePoint bereitgestellt werden. Weitere Informationen finden Sie unter [Bereitstellen und Veröffentlichen Ihres Office-Add-Ins.](https://docs.microsoft.com/office/dev/add-ins/publish/publish)
> 
> Das in diesem Artikel verwendete Add-In ist ein Beispiel für Entwickler. sie ist nicht für die Verwendung in einer Produktionsumgebung vorgesehen. Der Hauptzweck besteht darin, ein Beispiel für die App-Entwicklung für Project Online zu zeigen. 
  
## <a name="prerequisites"></a>Voraussetzungen

Fügen Sie die folgenden Elemente zu einer unterstützten Windows Umgebung hinzu:
  
- **.NET Framework 4.0 oder höher:** Vollständige Versionen des Frameworks ab Version 4.0 sind kompatibel. Die Download-Website ist https://msdn.microsoft.com/vstudio/aa496123.aspx.
    
- **Visual Studio 2013 oder höher:**  
    
   - Die Professional Edition von Visual Studio 2015 ist sofort einsatzbereit und steht unter https://www.visualstudio.com/en-us/products/visual-studio-professional-with-msdn-vs.aspx zur Verfügung.
    
   - Die Community-Edition von Visual Studio 2015 finden Sie unter https://www.visualstudio.com/en-us/products/visual-studio-community-vs.aspx . Diese Edition erfordert die manuelle Installation der Microsoft Office Developer Tools für Visual Studio.
    
   Die Microsoft Office Developer Tools für Visual Studio finden Sie unter https://www.visualstudio.com/en-us/features/office-tools-vs.aspx .
    
- **Ein Project Online Konto:** Dies ermöglicht den Zugriff auf den Hostingdienst. Weitere Informationen zum Einrichten eines Project Online-Kontos finden Sie unter https://products.office.com/en-us/Project/project-online-portfolio-management.
    
   Stellen Sie sicher, dass der Add-In-Benutzer über ausreichende Autorisierung für den Zugriff auf einige Projekte im Project Online Mandanten verfügt. 
    
- **Projekte auf der Hostingwebsite,** die mit Informationen aufgefüllt werden.
    
> [!NOTE]
> Die standard .NET Framework ist das richtige Framework. Verwenden Sie nicht das ".NET Framework 4-Clientprofil". 
  
### <a name="set-up-the-visual-studio-project"></a>Einrichten des Visual Studio-Projekts

Das Anwendungssetup besteht aus dem Erstellen eines neuen Projekts, dem Verknüpfen der entsprechenden Bibliotheken und dem Deklarieren der erforderlichen Namespaces. Visual Studio bietet verschiedene Typen von Entwicklungsprojekten. Der Abschnitt ist kurz und sehr einfach. Bei dem Wert werden die Informationen an einer zentralen Stelle zusammengef?nigt.
  
#### <a name="select-a-visual-studio-project"></a>Auswählen eines Visual Studio-Projekts

Um ein Projekt mit dem entsprechenden Typ für das Add-In zu erstellen, müssen Sie die folgenden Schritte ausführen. Schlüsselwörter, die auf dem Bildschirm auftreten, weisen ein **fett formatiertes** Attribut auf: 
  
1. Wählen Sie im Menü "Datei" die Option  >  **"Datei neu**  >  **Project"** aus. 
    
2. Wählen Sie in den installierten Vorlagen im linken Bereich C#-Office/SharePoint  >    >  **Web-Add-Ins aus.** 
    
3. Wählen Sie oben im zentralen Bereich **.NET Framework 4** oder höher aus. Die aktuelle Version ist 4.6. 
    
4. Wählen Sie in den Anwendungstypen im zentralen Bereich **SharePoint Add-In** aus. 
    
5. Geben Sie im unteren Abschnitt einen Namen und Speicherort für das Projekt und einen Projektmappennamen an. 
    
6. Aktivieren Sie außerdem im unteren Abschnitt das Kontrollkästchen **Projektmappenverzeichnis erstellen**. 
    
7. Klicken Sie auf **OK**, um das Ausgangsprojekt zu erstellen. 
    
Der Visual Studio-Assistent stellt einige Nachverfolgungsfragen zur Website für Project Online Einstellungen (SharePoint Einstellungen in den Dialogfeldern genannt) in einigen nachfolgenden Dialogfeldern. Hier sind die Fragen:
  
1. Welche SharePoint Website möchten Sie zum Debuggen Ihres Add-Ins verwenden? Geben Sie die URL zu Ihrer PWA Website an, https://contoso.sharepoint.com/sites/pwa z. B. .
    
2. Wie möchten Sie Ihr SharePoint-Add-In hosten? Wählen Sie [X] **SharePoint gehostet.**
    
   Weitere Informationen zu SharePoint-Add-Ins, einschließlich Hostingoptionen, finden Sie unter [SharePoint Add-Ins.](https://docs.microsoft.com/sharepoint/dev/sp-add-ins/sharepoint-add-ins)
    
3. Klicken Sie auf **Weiter**. 
    
Im zweiten zusätzlichen Dialogfeld werden Sie aufgefordert, die SharePoint Onlineversion für das Add-In anzugeben: 
  
1. Was ist die früheste Version von SharePoint, auf die Ihr Add-In ausgerichtet werden soll? Choose [X] S **harePoint-Online**. 
    
2. Klicken Sie auf **Fertig stellen**. 
    
Visual Studio erstellt das Projekt und greift auf die Project Online Website zu. 
  
### <a name="enable-sideloading-on-the-project-online-site"></a>Aktivieren des Querladens auf der Project Online Website

Querladen ist der Mechanismus zum Testen und Debuggen Project Online-Add-Ins. Sie benötigen zwei Skripts für das Querladen: eines zum Aktivieren des Querladens auf Ihrer Project Online Website und ein weiteres zum Deaktivieren des Querladens, sobald Sie das Testen und Debuggen des Add-Ins abgeschlossen haben.
  
Weitere Informationen zum Einrichten des Querladens finden Sie unter Aktivieren des [Querladens von Apps in Ihrer Websitesammlung,](https://blogs.msdn.microsoft.com/officeapps/2013/12/10/enable-app-sideloading-in-your-non-developer-site-collection/)die keine Entwickler ist.
  
> [!NOTE]
> Das Querladen von Apps ist ein Entwickler-/Testfeature. Es ist **nicht für die Verwendung in der Produktion vorgesehen.** Laden Sie Apps nicht regelmäßig quer, oder lassen Sie das Querladen von Apps länger aktiviert, als Sie das Feature aktiv verwenden. 
  
## <a name="add-content-to-the-add-in-project"></a>Hinzufügen von Inhalten zum Add-In-Projekt

Nach dem Erstellen eines Projekts und dem Einrichten des Debugmechanismus umfasst das Hinzufügen von Inhalten zur App die folgenden Aufgaben:
  
- Festlegen des Anwendungsbereichs
    
- Verknüpfen der JSOM-Bibliothek
    
- Hinzufügen von UI-Elementen zum Add-In
    
- Initialisieren und Herstellen einer Verbindung mit dem Project Online-Dienst
    
- Abrufen von Projekten und Details/Eigenschaften
    
- Anzeigen von Projekten
    
- Anzeigen von Aufgaben für eine Project
    
Das Add-In-Projekt besteht aus vielen Dateien. In diesem Beispiel müssen Sie die folgenden Dateien bearbeiten: 
  
- AppManifest.xml
    
- Default.aspx
    
- App.js
    
- App.css – optional; enthält Formatvorlagendefinitionen, die für das Add-In entwickelt wurden
    
Wenn sich der Project Online-Mandant ändert, z. B. von einer Testversion zu einer Abonnementwebsite wechseln, können Sie die Projekteigenschaften, einschließlich der Serververbindung und der Website-URL, mithilfe des Eigenschaftenfensters aktualisieren, das über den Befehl  >  **Eigenschaftenfenster** anzeigen verfügbar ist. 
  
Sie können dem Projekt auch Dateien hinzufügen. Wenn dies der Fall ist, müssen Sie die Elements.xml Datei aktualisieren, die sich in derselben Gruppe (Inhalt, Bilder, Seiten oder Skripts) befindet, um die neuen Dateien einzuschließen. Weitere Informationen zu den Projektdateien finden Sie unter [Untersuchen der App-Manifeststruktur und des Pakets eines SharePoint-Add-Ins.](https://docs.microsoft.com/sharepoint/dev/sp-add-ins/explore-the-app-manifest-structure-and-the-package-of-a-sharepoint-add-in)
  
### <a name="set-application-scope"></a>Festlegen des Anwendungsbereichs

Das Add-In benötigt Bereiche oder Berechtigungsstufen, die definiert werden, bevor der Dienst Informationen in Abfrageergebnissen zurückgibt. Verwenden Sie für dieses Add-In den folgenden Bereich für das Visual Studio Projekt. Diese Änderung wird an der datei AppManifest.xml auf der Registerkarte "Berechtigungen" vorgenommen:

|Umfang|Berechtigung|
|:-----|:-----|
|Mehrere Projekte (Project Server)  <br/> |Lesen  <br/> |
   
Speichern Sie die Datei nach dem Festlegen des Anwendungsbereichs. Andernfalls werden keine Daten vom Dienst zurückgegeben. 
  
### <a name="link-the-jsom-library"></a>Verknüpfen der JSOM-Bibliothek

Die Laufzeitbibliotheken Project Online, PS.js und PS.debug.js, werden von Project Online bereitgestellt und sind immer die neueste Version. JavaScript-Add-Ins, die JSOM verwenden, müssen mit einer dieser Bibliotheken verknüpft sein. Die Verknüpfungsdefinitionen werden in der Datei Default.aspx hinzugefügt. Die Befehle zum Verwenden der PS.js und/oder PS.debug.js sind Teil des Codes, der sich in der App.js-Datei befindet.
  
Fügen Sie den folgenden Befehl für PS.js oder PS.debug.js Definition im `<asp:Content ContentPlaceHolderID="PlaceHolderAdditionalPageHead"` Element hinzu, das auf "SharePoint:ScriptLink" für sp.js folgt. 
  
```js
<SharePoint:ScriptLink name="PS.js" runat="server" OnDemand="false" LoadAfterUI="true" Localizable="false" />
```

> [!NOTE]
> Das **OnDemand** -Attribut für PS.js oder PS.debug.js auf **"false"** festgelegt. 
  
### <a name="add-ui-elements-to-the-add-in"></a>Hinzufügen von UI-Elementen zum Add-In

Das Beispiel-Add-In besteht aus einigen Komponenten. Beschreibungen statischer Elemente befinden sich in der Datei Default.aspx. Beschreibungen dynamischer Elemente und Code für alle Komponenten befinden sich in der App.js Datei. Kommentare zu den Komponenten finden Sie in den Quellcodeauflistungen. Hier ist eine Liste der Benutzeroberflächenkomponenten im Add-In:
  
- Titel
    
- Einführendes Wort
    
- Schaltfläche zum Entfernen von Aufgaben aus der Tabelle
    
- Tabelle, die die Projekt-ID und den Projektnamen sowie die Vorgangsinformationen auflistet.
    
- Aufgabenschaltfläche (einmal für jedes Projekt geklont), die Vorgangsdaten in die Tabelle importiert.
    
Ausführliche Informationen zur Benutzeroberfläche, z. B. den Titel und den Headerteil der Projekttabelle, finden Sie in der Projektdatei "Default.aspx".
  
### <a name="initialize-and-connect-to-the-host-system"></a>Initialisieren und Herstellen einer Verbindung mit dem Hostsystem

Die App.js-Datei enthält den JavaScript-Code. Das Add-In lädt PS.js im Browser und ruft dann die InitializePage-Funktion auf. InitializePage ruft einen Kontext zum Project Online Endpunkt ab und startet die loadProjects-Funktion.
  
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

Die LoadProjects-Funktion fragt den Dienst nach den Projektnamen und IDs ab. 
  
Die Anwendung ruft den Projektnamen und die Projekt-ID ab. Weitere Informationen zum Projekt sind verfügbar und können durch Ändern der Lademethode aufgerufen werden, um explizit die abzurufenden Eigenschaften zu identifizieren. Ein Beispiel wird im Code als Kommentar bereitgestellt. 
  
Wenn die Abfrage erfolgreich ist, wird das Add-In fortgesetzt, indem displayProjects aufgerufen wird. 
  
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

Die displayProjects-Funktion erstellt eine Tabelle, eine Zeile pro Projekt und eine Schaltfläche zum Anzeigen der Aufgaben für das jeweilige Projekt. 
  
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
> Die While-Schleife greift auf die ID- und Namenseigenschaften zu. Dies unterscheidet sich geringfügig vom Quellcodeprojekt, das eine Funktion aufruft, die wiederum auf dieselben Eigenschaften zugreift. 
  
### <a name="display-the-tasks-for-a-project"></a>Anzeigen der Aufgaben für ein Projekt

Die Aufgaben sind zwar Teil des Add-Ins, sind aber nicht Teil des anfänglichen Ladens. Wenn der Benutzer an den mit einem Projekt verknüpften Aufgaben interessiert ist, bewirkt das Klicken auf die Schaltfläche "Aufgaben anzeigen", dass die Aufgaben mithilfe des btnLoadTasks-Ereignishandlers in der Liste angezeigt werden. 
  
Der btnLoadTasks-Ereignishandler mit der entsprechenden Projekt-ID fordert die Aufgaben für das angegebene Projekt vom Server an. Nach dem Abrufen übergibt btnLoadTasks die Aufgabenliste an displayTasks, um die Aufgaben auf dem Bildschirm darzustellen.
  
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
> Die While-Schleife greift auf die Eigenschaften der Aufgaben-ID und des Namens zu. Dies unterscheidet sich geringfügig vom Quellcodeprojekt, das eine Funktion aufruft, die wiederum auf dieselben Eigenschaften zugreift. 
  
Es folgt eine Beispielausgabe für die Aufgaben eines einzelnen Projekts.
  
![Screenshot mit der Ausgabe einer Projektaufgabe](media/f6500a3f-000b-4f3e-9be6-9a74d0bea15e.png "Screenshot mit der Ausgabe einer Projektaufgabe")
  
## <a name="see-also"></a>Siehe auch

Dokumentation und Beispiele zu Project Online und Anwendungsentwicklung mit CSOM finden Sie im [Project-Entwicklungsportal](https://developer.microsoft.com/en-us/project).
    


