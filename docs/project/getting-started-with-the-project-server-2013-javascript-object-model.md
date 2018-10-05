---
title: Erste Schritte mit dem Project Server 2013 JavaScript-Objektmodell
manager: soliver
ms.date: 08/10/2016
ms.audience: Developer
localization_priority: Normal
ms.assetid: 30dc3194-7480-4e7c-b731-4a171d652ee0
description: In Project Server 2013 kann bei der Entwicklung für Project Online Mobil und am Standort das JavaScript-Objektmodell verwendet werden. Dieses Thema bietet eine kurze Übersicht über das JavaScript-Objektmodell und Erstellen einer Anwendungsseite, die abgerufen und durchlaufen und Projekte mithilfe des JavaScript-Objektmodells beschrieben.
ms.openlocfilehash: ec8a10e987276807dc4648bd8948b2285f76fd37
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/04/2018
ms.locfileid: "25388210"
---
# <a name="getting-started-with-the-project-server-2013-javascript-object-model"></a>Erste Schritte mit dem Project Server 2013 JavaScript-Objektmodell

In Project Server 2013 kann bei der Entwicklung für Project Online Mobil und am Standort das JavaScript-Objektmodell verwendet werden. Dieses Thema bietet eine kurze Übersicht über das JavaScript-Objektmodell und Erstellen einer Anwendungsseite, die abgerufen und durchlaufen und Projekte mithilfe des JavaScript-Objektmodells beschrieben.
  
## <a name="using-the-project-server-javascript-object-model"></a>Verwenden des Project Server-JavaScript-Objektmodells
<a name="pj15_GetStartedJSOM_UseJSOM"> </a>

Mit dem JavaScript-Objektmodell ist eine hervorragende Möglichkeit zum eine app zu erstellen, die mithilfe der clientseitigen (im Gegensatz zu verwalteten Clientcode der Remote ausgeführt werden muss) ausführt. Apps können das JavaScript-Objektmodell zum Abrufen oder Ändern von Objekten durch Senden von asynchronen Aufrufen an den Server. Apps, die das JavaScript-Objektmodell verwenden, werden in der Regel als benutzerdefinierte SharePoint-Add-ins, Anwendungsseiten und Webparts bereitgestellt. Weitere Informationen finden Sie unter "Arten von SharePoint-Komponenten, die in einer app für SharePoint werden können" in [hostwebs, Add-in - Webs und SharePoint-Komponenten in SharePoint 2013](https://msdn.microsoft.com/library/b791cdf5-8aa2-47fa-bc4c-aee437354759%28Office.15%29.aspx).
  
Das JavaScript-Objektmodell implementiert die wichtigste Funktionen von Project Server 2013, aber das JavaScript-Objektmodell und das Serverobjektmodell keine 1: 1-Parität. Der Einstiegspunkt für das JavaScript-Objektmodell ist das **ProjectContext** -Objekt, das stellt des Clientkontexts für Project Server 2013 und bietet Zugriff auf Serverinhalt und die Funktionalität. Das JavaScript-Objektmodell für Project Server 2013 ist in der Datei PS.js, die sich im Standardpfad befindet definiert `%ProgramFiles%\Common Files\Microsoft Shared\Web Server Extensions\15\TEMPLATE\LAYOUTS` auf dem Anwendungsserver. Projektserver 2013 werden auch die folgenden installiert. Debug.js-Datei am selben Speicherort. FOLGENDEN Debug.js ist eine unminified Version des PS.js, die IntelliSense-Informationen enthält. 
  
Das JavaScript-Objektmodell ermöglicht die Formularauthentifizierung und alle Anfragen werden wie des aktuellen Benutzers authentifiziert. Weitere Informationen zu Sicherheit und anderen Aspekten für benutzerdefinierte apps entwerfen und Lösungen finden Sie unter [Authentifizierung, Autorisierung und Sicherheit in SharePoint 2013](https://msdn.microsoft.com/library/8734790c-eb75-4d78-9604-7cc23b33b693%28Office.15%29.aspx), [wichtige Aspekte der SharePoint-Add-in-Architektur und Entwicklung Querformat](https://msdn.microsoft.com/library/ae96572b-8f06-4fd3-854f-fc312f7f2d88%28Office.15%29.aspx), und [SharePoint-Add-ins mit SharePoint-Lösungen verglichen](https://msdn.microsoft.com/library/0e9efadb-aaf2-4c0d-afd5-d6cf25c4e7a8%28Office.15%29.aspx).
  
> [!NOTE]
> Zugriff auf Daten aus einer SharePoint-Website Remote, bietet SharePoint 2013 eine Cross-Domain-Bibliothek, die Sie mithilfe der clientseitigen Cross-Domain-Anrufe tätigen kann. Weitere Informationen finden Sie unter [Zugriff auf SharePoint 2013-Daten von add-ins mithilfe der domänenübergreifenden Bibliothek](https://msdn.microsoft.com/library/bc37ff5c-1285-40af-98ae-01286696242d%28Office.15%29.aspx). 
  
Viele Konzepte und Prozesse für die Verwendung des JavaScript-Objektmodells für Project Server 2013 ähneln in zugehörigen Client-Objektmodellen. Weitere Informationen zum Objektmodell für Project Server 2013 verwaltete Client finden Sie unter **Microsoft.ProjectServer.Client**. Weitere Informationen zu den SharePoint 2013JavaScript-Objektmodell und verwalteten Clientobjektmodell finden Sie unter [Ausführen grundlegender Vorgänge mit JavaScript-Bibliothekscode in SharePoint 2013](https://msdn.microsoft.com/library/29089af8-dbc0-49b7-a1a0-9e311f49c826%28Office.15%29.aspx) und [vollständige grundlegender Vorgänge unter Verwendung SharePoint 2013-Clients Bibliothekscode](https://msdn.microsoft.com/library/5a69c9e3-73bf-4ed5-bc19-182056bdb394%28Office.15%29.aspx).
  
## <a name="walkthrough-creating-an-application-page-that-retrieves-and-iterates-through-projects"></a>Exemplarische Vorgehensweise: Erstellen einer Anwendungsseite, die abgerufen und durchlaufen und Projekte
<a name="pj15_GetStartedJSOM_UseJSOM"> </a>

Informationen Sie zum Erstellen einer Anwendungsseite, die die ID, Name und Erstellungsdatum der einzelnen veröffentlichten Projekte in einer Website anzeigt.
  
### <a name="prerequisites-for-creating-an-application-page-that-retrieves-and-iterates-through-projects"></a>Voraussetzungen für das Erstellen einer Anwendungsseite, die abgerufen und durchlaufen und Projekte
<a name="pj15_GetStartedJSOM_Prereqs"> </a>

Um die Anwendungsseite zu entwickeln, die in diesem Thema beschrieben wird, müssen Sie installieren und konfigurieren die folgenden Produkte:
  
- SharePoint Server 2013
- Project Server 2013 mit mindestens ein veröffentlichtes Projekt
- Visual Studio 2012
- Office Developer Tools für Visual Studio 2012
    
Sie benötigen auch über die Berechtigungen zum Bereitstellen der Erweiterungs für SharePoint Server 2013 und zum Abrufen von Projekten.
  
> [!NOTE]
> Diese Anweisungen wird davon ausgegangen, dass Sie auf dem Computer entwickeln, die Project Server 2013 ausgeführt wird. 
  
### <a name="creating-the-application-page-in-visual-studio-2012"></a>Erstellen der Anwendungsseite in Visual Studio 2012
<a name="pj15_GetStartedJSOM_CreateVS"> </a>

Die folgenden Schritte erstellen Sie ein SharePoint-Projekt und einer Anwendungsseite, die eine Tabelle und eine Beschriftung enthält. Die Tabelle enthält Informationen zu den Projekten und die Beschriftung für Fehlermeldungen angezeigt.
  
1. Führen Sie auf dem Computer, auf der Project Server 2013 ausgeführt wird, Visual Studio 2012 als Administrator.
    
2. Erstellen Sie ein leeres SharePoint 2013-Projekt wie folgt:
    
    1. Wählen Sie im Dialogfeld **Neues Projekt** aus der Dropdownliste oben im Dialogfeld die Option **.NET Framework 4.5**. 
        
    2. Wählen Sie in der Liste der Kategorien die Kategorie **Office SharePoint** , und wählen Sie dann die Vorlage **SharePoint 2013-Projekts** . 
        
    3. Nennen Sie das Projekt GetProjectsJSOM, und wählen Sie dann auf die Schaltfläche **OK** . 
        
    4. Wählen Sie in das Dialogfeld des **Assistenten zum Anpassen von SharePoint** **als farmlösung bereitstellen**, und wählen Sie dann auf die Schaltfläche **OK** . 
    
3. Bearbeiten Sie im Projektmappen-Explorer den Wert der Eigenschaft **Website-URL** für das Projekt **ProjectsJSOM** entsprechend die URL der Project Web App-Instanz (z. B. `https://ServerName/PWA`).
    
4. Öffnen Sie das Kontextmenü für das **GetProjectsJSOM** -Projekt, und fügen Sie eine SharePoint "Layouts" Ordner zugeordnet. 
    
5. Öffnen Sie im Ordner **Layouts** das Kontextmenü für den Ordner **GetProjectsJSOM** , und fügen Sie eine neue SharePoint-Anwendungsseite namens ProjectsList.aspx.
    
   > [!NOTE]
   > In diesem Beispiel wird die CodeBehind-Datei, die Visual Studio 2012 erstellt für die Anwendungsseite nicht verwendet. 
  
6. Öffnen Sie das Kontextmenü für die Seite **ProjectsList.aspx** , und wählen Sie **als Startelement festlegen**.
    
7. Definieren Sie im Markup für die Seite **ProjectsList.aspx** eine Tabelle und eine Nachricht Platzhalter in den "Main" **Asp: Content** -Tags wie folgt. 
    
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

Die folgenden Schritte abrufen und initialisieren die Projects-Auflistung.
  
1. Nach dem schließenden **Div** markieren, fügen Sie einen **SharePoint:ScriptLink** -Tag, das die Datei PS.js wie folgt verweist. 
    
   ```HTML
    <SharePoint:ScriptLink name="PS.js" runat="server" ondemand="false" localizable="false" loadafterui="true" />
   ```

2. Fügen Sie unterhalb des Tags **SharePoint:ScriptLink** **Script** -Tags, wie folgt hinzu. 
    
   ```HTML
    <script type="text/javascript">
        // Paste the remaining code snippets here, in the order that they are presented.
    </script>
   ```

3. Deklarieren Sie eine globale Variable zum Speichern von wie folgt der Projects-Auflistung.
    
   ```js
   var projects;
   ```

4. Rufen Sie die **SP. SOD.executeOrDelayUntilScriptLoaded** -Methode, um sicherzustellen, dass die PS.js-Datei geladen wird, bevor der benutzerdefinierte Code ausgeführt wird. 
    
   ```js
   SP.SOD.executeOrDelayUntilScriptLoaded(GetProjects, "PS.js");
   ```

5. Fügen Sie eine Funktion, die eine Verbindung mit dem aktuellen Kontext und ruft die Projects-Auflistung, wie folgt hinzu.
    
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

   Einige Clientobjekte, die Sie durch den Kontext abrufen enthalten keine Daten, bis sie initialisiert werden. Sie können nicht d. h., die Eigenschaftswerte des Objekts zugreifen, bis das Objekt initialisiert wird. Darüber hinaus müssen für Eigenschaften vom Typ **ValueObject**, Sie explizit die Eigenschaft anfordern, bevor Sie seinen Wert zugreifen können. (Wenn Sie versuchen, eine Eigenschaft zugegriffen werden, bevor es initialisiert wird, erhalten Sie eine Ausnahme **PropertyOrFieldNotInitializedException** .) 
    
   Um ein Objekt zu initialisieren, rufen Sie die **load** -Methode (oder der **"loadquery"** -Methode), und klicken Sie dann die **ExecuteQueryAsync** -Methode. 
    
   - Die Funktion **Laden** oder die Funktion **"loadquery"-Methode** aufrufen registriert eine Anforderung, die auf dem Server ausgeführt werden soll. Sie übergeben Sie einen Parameter, der das Objekt darstellt, das Sie abrufen möchten. Wenn Sie mit einer Eigenschaft **ValueObject** arbeiten, fordern Sie auch die Eigenschaft im Parameter. 
    
   - Aufrufen der **ExecuteQueryAsync** -Funktion sendet die abfrageanforderung asynchron an den Server. Sie übergeben Sie eine Rückruffunktion Erfolg und eine Fehler-Callback-Funktion, die aufgerufen werden, wenn die Antwort vom Server empfangen wird. 
    
   Fordern Sie an, um den Netzwerkverkehr zu reduzieren, nur die Eigenschaften, die das Arbeiten mit beim Aufruf der Funktion **geladen** werden sollen. Wenn Sie mit mehreren Objekten arbeiten, gruppieren Sie mehrere Anrufe an die Funktion **geladen werden** darüber hinaus, bevor Sie die **ExecuteQueryAsync** -Funktion aufrufen, wenn es möglich ist. 
    
### <a name="iterating-through-the-projects-collection"></a>Durchlaufen der Projects-Auflistung
<a name="pj15_GetStartedJSOM_IterateProjs"> </a>

Die folgenden Schritte aus der Projects-Auflistung durchlaufen, (falls der Server-Aufruf erfolgreich ist) oder eine Fehlermeldung (wenn der Aufruf fehlschlägt) zu rendern.
  
1. Fügen Sie eine Erfolg Callback-Funktion, die wie folgt die Projects-Auflistung durchläuft.
    
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

2. Fügen Sie eine Fehler-Callback-Funktion, die eine Fehlermeldung wie folgt gerendert wird.
    
    ```js
    function onQueryFailed(sender, args) {
        $get("spanMessage").innerText = 'Request failed: ' + args.get_message();
    }
    ```

3. Wählen Sie zum Testen der Anwendungsseite in der Menüleiste **Debuggen**, **Debuggen starten**aus. Wenn Sie aufgefordert werden, ändern Sie die Datei "Web.config", und wählen Sie **OK**.

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

- [Erstellen, abrufen, aktualisieren und Löschen von Projekten mit dem Project Server-JavaScript-Objektmodell](create-retrieve-update-delete-projects-using-project-server-javascript.md)  
- [Clientseitiges Objektmodell (CSOM) für Project 2013](client-side-object-model-csom-for-project-2013.md)
- [Erste Schritte mit dem Project Server-CSOM und .NET](getting-started-with-the-project-server-csom-and-net.md)
    

