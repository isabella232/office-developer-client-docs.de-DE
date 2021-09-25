---
title: Erste Schritte mit dem JavaScript-Objektmodell Project Server 2013
manager: soliver
ms.date: 08/10/2016
ms.audience: Developer
ms.localizationpriority: medium
ms.assetid: 30dc3194-7480-4e7c-b731-4a171d652ee0
description: In Project Server 2013 kann das JavaScript-Objektmodell in Project Online, mobilen und lokalen Entwicklung verwendet werden. Dieses Thema enthält eine kurze Übersicht über das JavaScript-Objektmodell und beschreibt dann, wie Sie eine Anwendungsseite erstellen, die Projekte mithilfe des JavaScript-Objektmodells abruft und durchläuft.
ms.openlocfilehash: 5c667b736eb98829cbad538abdab1613b4cd7946
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59616145"
---
# <a name="getting-started-with-the-project-server-2013-javascript-object-model"></a>Erste Schritte mit dem JavaScript-Objektmodell Project Server 2013

In Project Server 2013 kann das JavaScript-Objektmodell in Project Online, mobilen und lokalen Entwicklung verwendet werden. Dieses Thema enthält eine kurze Übersicht über das JavaScript-Objektmodell und beschreibt dann, wie Sie eine Anwendungsseite erstellen, die Projekte mithilfe des JavaScript-Objektmodells abruft und durchläuft.
  
## <a name="using-the-project-server-javascript-object-model"></a>Verwenden des JavaScript-Objektmodells für Project Server
<a name="pj15_GetStartedJSOM_UseJSOM"> </a>

Die Verwendung des JavaScript-Objektmodells ist eine hervorragende Möglichkeit zum Erstellen einer App, die clientseitig ausgeführt wird (im Gegensatz zu verwaltetem Clientcode, der remote ausgeführt werden muss). Apps können das JavaScript-Objektmodell verwenden, um Objekte abzurufen oder zu ändern, indem asynchrone Aufrufe an den Server gesendet werden. Apps, die das JavaScript-Objektmodell verwenden, werden in der Regel als benutzerdefinierte SharePoint-Add-Ins, Anwendungsseiten und Webparts bereitgestellt. Weitere Informationen finden Sie unter "Typen von SharePoint Komponenten, die in einer App für SharePoint enthalten sein können" in [Hostwebsites, Add-In-Webs und SharePoint Komponenten in SharePoint 2013.](https://msdn.microsoft.com/library/b791cdf5-8aa2-47fa-bc4c-aee437354759%28Office.15%29.aspx)
  
Das JavaScript-Objektmodell implementiert die Hauptfunktionalität von Project Server 2013, aber das JavaScript-Objektmodell und das Serverobjektmodell haben keine 1:1-Parität. Der Einstiegspunkt für das JavaScript-Objektmodell ist das **ProjectContext-Objekt,** das den Clientkontext für Project Server 2013 darstellt und Zugriff auf Serverinhalte und -funktionen bietet. Das JavaScript-Objektmodell für Project Server 2013 ist in der PS.js-Datei definiert, die sich im Standardpfad `%ProgramFiles%\Common Files\Microsoft Shared\Web Server Extensions\15\TEMPLATE\LAYOUTS` auf dem Anwendungsserver befindet. Project Server 2013 installiert auch die PS.Debug.js-Datei am selben Speicherort. PS.Debug.js ist eine nicht verwaltete Version von PS.js, die IntelliSense-Informationen bereitstellt. 
  
Das JavaScript-Objektmodell ermöglicht die Formularauthentifizierung, und alle Anforderungen werden als aktueller Benutzer authentifiziert. Weitere Informationen zur Sicherheit und anderen Überlegungen zum Entwerfen von benutzerdefinierten Apps und Lösungen finden Sie unter [Authentifizierung, Autorisierung und Sicherheit in SharePoint 2013,](https://msdn.microsoft.com/library/8734790c-eb75-4d78-9604-7cc23b33b693%28Office.15%29.aspx)wichtige Aspekte der SharePoint Architektur [und Entwicklungslandschaft von Add-Ins](https://msdn.microsoft.com/library/ae96572b-8f06-4fd3-854f-fc312f7f2d88%28Office.15%29.aspx)und [SharePoint-Add-Ins im Vergleich zu SharePoint Lösungen.](https://msdn.microsoft.com/library/0e9efadb-aaf2-4c0d-afd5-d6cf25c4e7a8%28Office.15%29.aspx)
  
> [!NOTE]
> Um remote auf Daten von einem SharePoint Standort aus zuzugreifen, bietet SharePoint 2013 eine domänenübergreifende Bibliothek, mit der Sie clientseitige domänenübergreifende Aufrufe tätigen können. Weitere Informationen finden Sie unter [Access SharePoint 2013-Daten von Add-Ins mithilfe der domänenübergreifenden Bibliothek.](https://msdn.microsoft.com/library/bc37ff5c-1285-40af-98ae-01286696242d%28Office.15%29.aspx) 
  
Viele Konzepte und Prozesse für die Verwendung des JavaScript-Objektmodells für Project Server 2013 ähneln denen in verwandten Clientobjektmodellen. Weitere Informationen zum verwalteten Clientobjektmodell Project Server 2013 finden Sie unter **Microsoft.ProjectServer.Client.** Weitere Informationen zum SharePoint 2013JavaScript-Objektmodell und zum verwalteten Clientobjektmodell finden Sie unter [Ausführen grundlegender Vorgänge mit JavaScript-Bibliothekscode in SharePoint 2013](https://msdn.microsoft.com/library/29089af8-dbc0-49b7-a1a0-9e311f49c826%28Office.15%29.aspx) und Abschließen grundlegender Vorgänge mit SharePoint [2013-Clientbibliothekscode.](https://msdn.microsoft.com/library/5a69c9e3-73bf-4ed5-bc19-182056bdb394%28Office.15%29.aspx)
  
## <a name="walkthrough-creating-an-application-page-that-retrieves-and-iterates-through-projects"></a>Exemplarische Vorgehensweise: Erstellen einer Anwendungsseite, die Projekte abruft und durchläuft
<a name="pj15_GetStartedJSOM_UseJSOM"> </a>

Erfahren Sie, wie Sie eine Anwendungsseite erstellen, die die ID, den Namen und das Erstellungsdatum jedes veröffentlichten Projekts auf einer Website anzeigt.
  
### <a name="prerequisites-for-creating-an-application-page-that-retrieves-and-iterates-through-projects"></a>Voraussetzungen für das Erstellen einer Anwendungsseite, die Projekte abruft und durchläuft
<a name="pj15_GetStartedJSOM_Prereqs"> </a>

Um die in diesem Thema beschriebene Anwendungsseite zu entwickeln, müssen Sie die folgenden Produkte installieren und konfigurieren:
  
- SharePoint Server 2013
- Project Server 2013 mit mindestens einem veröffentlichten Projekt
- Visual Studio 2012
- Office Developer Tools für Visual Studio 2012
    
Sie müssen auch über Berechtigungen zum Bereitstellen der Erweiterung auf SharePoint Server 2013 und zum Abrufen von Projekten verfügen.
  
> [!NOTE]
> Bei diesen Anweisungen wird davon ausgegangen, dass Sie die Entwicklung auf dem Computer durchführen, auf dem Project Server 2013 ausgeführt wird. 
  
### <a name="creating-the-application-page-in-visual-studio-2012"></a>Erstellen der Anwendungsseite in Visual Studio 2012
<a name="pj15_GetStartedJSOM_CreateVS"> </a>

Mit den folgenden Schritten werden ein SharePoint Projekt und eine Anwendungsseite erstellt, die eine Tabelle und eine Beschriftung enthält. In der Tabelle werden Informationen zu den Projekten angezeigt, und auf der Beschriftung werden Fehlermeldungen angezeigt.
  
1. Führen Sie auf dem Computer, auf dem Project Server 2013 ausgeführt wird, Visual Studio 2012 als Administrator aus.
    
2. Erstellen Sie wie folgt ein leeres SharePoint 2013-Projekt:
    
    1. Wählen Sie im Dialogfeld **Neues Projekt** in der Dropdownliste oben im Dialogfeld **.NET Framework 4.5** aus. 
        
    2. Wählen Sie in der Liste der Vorlagenkategorien die **kategorie Office SharePoint** und dann die Vorlage **SharePoint 2013 Project** aus. 
        
    3. Benennen Sie das Projekt "GetProjectsJSOM", und klicken Sie dann auf die Schaltfläche **"OK".** 
        
    4. Wählen Sie im Dialogfeld **SharePoint Anpassungs-Assistent** die Option **"Als Farmlösung bereitstellen"** und dann die Schaltfläche **"OK"** aus. 
    
3. Bearbeiten Sie im Projektmappen-Explorer den Wert der **Website-URL-Eigenschaft** für das **ProjectsJSOM-Projekt** so, dass er der URL der Project Web App-Instanz entspricht (z. B. `https://ServerName/PWA` ).
    
4. Öffnen Sie das Kontextmenü für das **GetProjectsJSOM-Projekt,** und fügen Sie dann einen SharePoint zugeordneten Ordner "Layouts" hinzu. 
    
5. Öffnen Sie im Ordner **"Layouts"** das Kontextmenü für den Ordner **"GetProjectsJSOM",** und fügen Sie dann eine neue SharePoint Anwendungsseite namens ProjectsList.aspx hinzu.
    
   > [!NOTE]
   > In diesem Beispiel wird nicht die CodeBehind-Datei verwendet, die Visual Studio 2012 für die Anwendungsseite erstellt. 
  
6. Öffnen Sie das Kontextmenü für die Seite **ProjectsList.aspx,** und wählen Sie **"Als Startelement festlegen"** aus.
    
7. Definieren Sie im Markup für die Seite **ProjectsList.aspx** wie folgt eine Tabelle und einen Nachrichtenplatzhalter innerhalb der **asp:Content-Tags** vom Typ "Main". 
    
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

### <a name="retrieving-the-projects-collection"></a>Abrufen der Projects-Auflistung
<a name="pj15_GetStartedJSOM_RetrieveProjs"> </a>

Mit den folgenden Schritten wird die Projektsammlung abgerufen und initialisiert.
  
1. Fügen Sie nach dem schließenden **div-Tag** wie folgt ein **SharePoint:ScriptLink-Tag** hinzu, das auf die PS.js Datei verweist. 
    
   ```HTML
    <SharePoint:ScriptLink name="PS.js" runat="server" ondemand="false" localizable="false" loadafterui="true" />
   ```

2. Fügen Sie unterhalb des **SharePoint:ScriptLink-Tags** Wie folgt **Skripttags** hinzu. 
    
   ```HTML
    <script type="text/javascript">
        // Paste the remaining code snippets here, in the order that they are presented.
    </script>
   ```

3. Deklarieren Sie wie folgt eine globale Variable zum Speichern der Projektsammlung.
    
   ```js
   var projects;
   ```

4. Rufen Sie den **SP auf. SOD.executeOrDelayUntilScriptLoaded-Methode,** um sicherzustellen, dass die PS.js-Datei geladen wird, bevor der benutzerdefinierte Code ausgeführt wird. 
    
   ```js
   SP.SOD.executeOrDelayUntilScriptLoaded(GetProjects, "PS.js");
   ```

5. Fügen Sie wie folgt eine Funktion hinzu, die eine Verbindung mit dem aktuellen Kontext herstellt und die Projektsammlung abruft.
    
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

   Einige Clientobjekte, die Sie über den Kontext abrufen, enthalten keine Daten, bis sie initialisiert wurden. d. h., Sie können erst auf die Eigenschaftswerte des Objekts zugreifen, wenn das Objekt initialisiert wurde. Darüber hinaus müssen Sie für Eigenschaften vom Typ **ValueObject** die Eigenschaft explizit anfordern, bevor Sie auf ihren Wert zugreifen können. (Wenn Sie versuchen, auf eine Eigenschaft zuzugreifen, bevor sie initialisiert wird, erhalten Sie eine **PropertyOrFieldNotInitializedException-Ausnahme.)** 
    
   Zum Initialisieren eines Objekts rufen Sie die **Load-Methode** (oder die **loadQuery-Methode)** und dann die **executeQueryAsync-Methode** auf. 
    
   - Durch Aufrufen der **Load-Funktion** oder der **loadQuery-Funktion** wird eine Anforderung registriert, die auf dem Server ausgeführt werden soll. Sie übergeben einen Parameter, der das abzurufende Objekt darstellt. Wenn Sie mit einer **ValueObject-Eigenschaft** arbeiten, fordern Sie auch die Eigenschaft im Parameter an. 
    
   - Durch Aufrufen der **executeQueryAsync-Funktion** wird die Abfrageanforderung asynchron an den Server gesendet. Sie übergeben eine Erfolgsrückruffunktion und eine Fehlerrückruffunktion, die aufgerufen werden soll, wenn die Serverantwort empfangen wird. 
    
   Um den Netzwerkdatenverkehr zu reduzieren, fordern Sie nur die Eigenschaften an, mit denen Sie arbeiten möchten, wenn Sie die **Ladefunktion** aufrufen. Wenn Sie mit mehreren Objekten arbeiten, gruppieren Sie außerdem mehrere Aufrufe der **Ladefunktion,** bevor Sie die **executeQueryAsync-Funktion** aufrufen, wenn dies möglich ist. 
    
### <a name="iterating-through-the-projects-collection"></a>Durchlaufen der Projektsammlung
<a name="pj15_GetStartedJSOM_IterateProjs"> </a>

Die folgenden Schritte durchlaufen die Projektsammlung (wenn der Serveraufruf erfolgreich war) oder rendern eine Fehlermeldung (wenn der Aufruf fehlschlägt).
  
1. Fügen Sie wie folgt eine Erfolgsrückruffunktion hinzu, die die Projektsammlung durchläuft.
    
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

2. Fügen Sie wie folgt eine Fehlerrückruffunktion hinzu, die eine Fehlermeldung rendert.
    
    ```js
    function onQueryFailed(sender, args) {
        $get("spanMessage").innerText = 'Request failed: ' + args.get_message();
    }
    ```

3. Um die Anwendungsseite zu testen, wählen Sie in der Menüleiste die Optionen **Debuggen**, **Debuggen starten**. Wenn Sie aufgefordert werden, die web.config Datei zu ändern, wählen Sie **OK** aus.

<a name="pj15_GetStartedJSOM_CompleteExample"> </a>

## <a name="complete-code-example"></a>Vollständiges Codebeispiel

Es folgt der vollständige Code aus der Datei ProjectsList.aspx.
  
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

<a name="pj15_GetStartedJSOM_AR"> </a>

## <a name="see-also"></a>Siehe auch

- [Erstellen, Abrufen, Aktualisieren und Löschen von Projekten mithilfe des Project Server JavaScript-Objektmodells](create-retrieve-update-delete-projects-using-project-server-javascript.md)  
- [Clientseitiges Objektmodell (CSOM) für Project 2013](client-side-object-model-csom-for-project-2013.md)
- [Erste Schritte mit dem Project Server-CSOM und .NET](getting-started-with-the-project-server-csom-and-net.md)
    

