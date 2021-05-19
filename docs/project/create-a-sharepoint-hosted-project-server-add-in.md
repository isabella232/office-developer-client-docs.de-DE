---
title: Erstellen eines auf SharePoint gehosteten Project Server-Add-Ins
manager: lindalu
ms.date: 08/10/2016
ms.audience: Developer
localization_priority: Normal
ms.assetid: bb9c3c00-7121-41e1-9db3-75550d040ba8
description: Von den drei Arten von Apps, die Sie für Project Online erstellen können (automatisch gehostet, vom Anbieter gehostet und SharePoint gehostet), ist die von SharePoint gehostete App die einfachste, die sie erstellen und bereitstellen kann.
ms.openlocfilehash: 9b3b41eda40a8419ad72f11bb474acf7acaf81e9
ms.sourcegitcommit: 31b0a7373ff74fe1d6383c30bc67d7675b73d283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/05/2020
ms.locfileid: "41773757"
---
# <a name="create-a-sharepoint-hosted-project-server-add-in"></a>Erstellen eines auf SharePoint gehosteten Project Server-Add-Ins

Von den drei Arten von Apps, die Sie für Project Online erstellen können (automatisch gehostet, vom Anbieter gehostet und SharePoint gehostet), ist die von SharePoint gehostete App die einfachste, die sie erstellen und bereitstellen kann. Eine SharePoint-gehostete App erfordert keine OAuth-Authentifizierung und verwendet weder Azure noch eine lokale Website für die vom Anbieter gehosteten Ressourcen. Die **App für SharePoint 2013-Vorlage** in Visual Studio ist ein praktisches Framework für die Entwicklung von Apps, die im Office Store veröffentlicht und verkauft oder in einem privaten App-Katalog auf SharePoint. 
  
In Project ist statusing ein Prozess, bei dem ein Teammitglied die Seite Aufgaben in Project Web App verwenden kann, um den Status eines zugewiesenen Vorgangs zu übermitteln, z. B. die Anzahl der Arbeitsstunden, die an jedem Tag einer Woche für die Arbeit an der Aufgabe gearbeitet wurden. Der Zuweisungsbesitzer (in der Regel der Projektmanager) kann den Status genehmigen oder ablehnen. Wenn der Status genehmigt wird, Project Den Zeitplan neu berechnen. Die **QuickStatus-App** zeigt zugewiesene Aufgaben an, bei denen der Benutzer den Abgeschlossenen Prozentstand schnell aktualisieren und den Status der ausgewählten Zuordnungen zur Genehmigung übermitteln kann. Obwohl die Seite Aufgaben in Project Web App wesentlich mehr Funktionalität bietet, ist die **QuickStatus-App** ein Beispiel, das eine vereinfachte Benutzeroberfläche bietet. 
  
Die **QuickStatus-App** ist ein Beispiel für Entwickler. Es ist nicht für die Verwendung in einer Produktionsumgebung vorgesehen. Der hauptzweck ist es, ein Beispiel für die App-Entwicklung für Project Online zu zeigen, nicht um eine voll funktionsfähige Status-App zu erstellen. Einen besseren Ansatz für die Statusanzeige finden Sie in der Empfehlung unter [Nächste Schritte](#pj15_StatusingApp_NextSteps).
  
Allgemeine Informationen zum Status finden Sie unter [Vorgangsfortschritt](https://support.office.com/article/Find-information-about-Project-Server-2013-8b08a414-15a7-4076-b2db-c90d0214ea7f?ui=en-US&rs=en-US&ad=US#BKMK_TaskProgress). Weitere Informationen zum Entwickeln von Add-Ins für SharePoint und Project Server finden Sie unter [SharePoint Add-Ins](https://msdn.microsoft.com/library/jj163230.aspx).

<a name="pj15_StatusingApp_Prerequisites"> </a>

## <a name="prerequisites-for-creating-an-app-for-project-server-2013"></a>Voraussetzungen für das Erstellen einer App für Project Server 2013

Um relativ einfache Apps zu entwickeln, die auf Project Online oder in einer lokalen Installation von Project Server 2013 bereitgestellt werden können, können Sie die Napa verwenden, die eine Onlineentwicklungsumgebung bereitstellen. Für komplexere Apps, das Ändern des Project Web App-Menübands und ein einfacheres Debuggen während der Entwicklung können Sie Visual Studio 2012 oder Visual Studio 2013. Bei einer lokalen Installation können Sie z. B. die Drafts-Datentabellen manuell auf Änderungen in der Project überprüfen. In diesem Artikel wird gezeigt, wie Sie die App-Entwicklung mit Visual Studio.
  
Die Entwicklung Project Server-Apps mit Visual Studio erfordert Folgendes:
  
- Stellen Sie sicher, dass Sie die neuesten Service Packs und Windows-Updates auf dem lokalen Entwicklungscomputer installiert haben. Als Betriebssystem kann Windows 7, Windows 8, Windows Server 2008 oder Windows Server 2012 verwendet werden.
    
- Sie müssen einen Computer mit SharePoint Server 2013 und Project Server 2013 installiert haben, auf dem der Computer für die App-Isolation und das Querladen von Apps konfiguriert ist. Das Querladen ermöglicht Visual Studio, die App vorübergehend zum Debuggen zu installieren. Sie können eine lokale Installation von SharePoint server Project verwenden. Weitere Informationen finden Sie unter Einrichten einer lokalen Entwicklungsumgebung [für Apps für SharePoint](https://msdn.microsoft.com/library/fp179923%28Office.15%29.aspx).
    
   > [!NOTE]
   > Konfigurieren Sie für eine lokale Installation eine isolierte App-Domäne,  *bevor*  Sie einen Unternehmens-App-Katalog erstellen. 
  
- Der Entwicklungscomputer kann ein Remotecomputer sein, auf dem Office Entwicklertools für Visual Studio 2012 installiert sind. Stellen Sie sicher, dass Sie die neueste Version installiert haben. weitere Informationen *finden* Sie im Abschnitt [Extras](https://msdn.microsoft.com/office/apps/fp123627.aspx)der Apps für Office und SharePoint Downloads .
    
- Stellen Sie sicher, Project Web App-Instanz, die Sie für die Entwicklung und tests verwenden, im Browser verfügbar ist.
    
Informationen zur Verwendung der Onlinetools finden Sie unter Einrichten einer Umgebung für die Entwicklung von Apps [für SharePoint auf Office 365](https://msdn.microsoft.com/library/fp161179.aspx). Eine exemplarische Vorgehensweise zum Erstellen einer einfachen App für Project Server, die die Onlinetools verwendet, finden Sie in der EPMSource-Blogreihe Erstellen Ihrer ersten Project [Server-App.](https://epmsource.com/2012/11/20/building-your-first-project-server-app-part-zerothe-introduction/)

<a name="pj15_StatusingApp_UsingVisualStudio"> </a>

## <a name="using-visual-studio-to-create-a-project-server-app"></a>Verwenden Visual Studio zum Erstellen einer Project Server-App

Office Developer Tools for Visual Studio 2012 enthält eine Vorlage für SharePoint Apps, die mit Project Server 2013 verwendet werden können. Wenn Sie eine App-Lösung erstellen, enthält die Lösung die folgenden Dateien für Ihren benutzerdefinierten Code:
  
- **AppManifest.xml** enthält Einstellungen für den App-Titel, den Berechtigungsanforderungsbereich und andere Eigenschaften. Prozedur 1 enthält Schritte zum Festlegen der Eigenschaften mithilfe des Manifest-Designers. 
    
- **Default.aspx** im Ordner Seiten ist die Hauptseite der App. In Prozedur 2 wird gezeigt, wie Sie HTML5-Inhalte für die **QuickStatus-App** hinzufügen. 
    
- **App.js** im Ordner Skripts ist die primäre Datei für den benutzerdefinierten JavaScript-Code. In Prozedur 3 wird der JavaScript-Code für die **QuickStatus-App** erläutert. 
    
   Wenn Sie kommerzielle Steuerelemente wie ein jQuery-basiertes Raster oder eine Datumsauswahl hinzufügen, können Sie Verweise auf zusätzliche JavaScript-Dateien in der Datei Default.aspx hinzufügen.
    
- **App.css** im Ordner Inhalt ist die primäre Datei für benutzerdefinierte CSS3-Formatvorlagen. Prozedur 2 und Prozedur 3 enthalten Informationen zu Cascading Stylesheets (CSS)-Formatvorlagen für die **QuickStatus-App.** Sie können Verweise auf zusätzliche CSS-Dateien in der Datei "Default.aspx" hinzufügen. 
    
- **AppIcon.png** im Ordner Bilder ist das 96 x 96-Symbol, das die App im Office Store oder im App-Katalog anzeigt. 
    
Zum Ändern des Project Web App-Menübands können Sie eine benutzerdefinierte Menübandaktion hinzufügen. Der Beispielcode für den [Abschnitt QuickStatus-App](#pj15_StatusingApp_Example) enthält den vollständigen Code für die geänderten Dateien Default.aspx, App.js, App.css, Elements.xml und AppManifest.xml Dateien. 
  
### <a name="procedure-1-to-create-an-app-project-in-visual-studio"></a>Vorgehensweise 1: So erstellen Sie ein App-Projekt in Visual Studio

1. Führen Visual Studio 2012 als Administrator aus, und wählen Sie dann auf der Startseite **Project** Neue Option aus. 
    
2. Erweitern Sie **im Dialogfeld Project** die Knoten **Vorlagen**, **Visual C#** und **Office/SharePoint,** und wählen Sie **dann Apps aus.** Verwenden Sie die **Standardeinstellung .NET Framework 4.5** in der Dropdownliste Zielframework am oberen Rand des Mittelbereichs, und wählen Sie dann **App für SharePoint 2013** aus (siehe Abbildung 1). 
    
3. Geben Sie **im Feld Name** QuickStatus ein, navigieren Sie zu dem Speicherort, an dem Sie die App speichern möchten, und wählen Sie dann OK **aus.**
    
   **Abbildung 1. Erstellen einer Project Server-App in Visual Studio**

   ![Erstellen einer Project Server-App in Visual Studio](media/pj15_CreateStatusingApp_NewProject.gif "Erstellen einer Project Server-App in Visual Studio")
  
4. Füllen Sie **im Dialogfeld Neue App für SharePoint** die folgenden drei Felder aus: 
    
   - Geben Sie im oberen Textfeld den Namen ein, den die App in der Project anzeigen soll. Geben Sie beispielsweise Quick Status Update ein.
    
   - Geben Sie für die Website, die zum Debuggen verwendet werden soll, die URL der Project Web App-Instanz ein. Geben Sie beispielsweise `https://ServerName/ProjectServerName` ein (ersetzen _Sie ServerName_ und _ProjectServerName_ durch Eigene Werte), und wählen Sie dann **Überprüfen aus.** Wenn alles gut geht, zeigt Visual Studio **Verbindung erfolgreich an.** Wenn Sie eine Fehlermeldung erhalten, stellen Sie sicher, dass die Project Web App-URL korrekt ist und dass der Project Server-Computer für die App-Isolation und das Querladen von Apps konfiguriert ist. Weitere Informationen finden Sie im Abschnitt Voraussetzungen für das Erstellen einer [App für Project Server 2013.](#pj15_StatusingApp_Prerequisites) 
    
   - Wählen Sie **in der Dropdownliste** How do you want to host your app for SharePoint die Option SharePoint gehostet **aus.**
    
   > [!CAUTION]
   > Wenn Sie den standardmäßigen vom Anbieter gehosteten Projekttyp aus Versehen auswählen, erstellt Visual Studio zwei Projekte in der Projektmappe: ein **QuickStatus-Projekt** und ein **QuickStatusWeb-Projekt.**  Wenn zwei Projekte zu sehen sind, löschen Sie diese Lösung, und starten Sie erneut. 
  
5. Wählen **Sie OK** aus, um die **QuickStatus-Lösung,** **das QuickStatus-Projekt** und die Standarddateien zu erstellen. 
    
6. Öffnen Sie die Manifest-Designer-Ansicht (doppelklicken Sie z. B. auf die AppManifest.xml Datei). Auf der **Registerkarte Allgemein** sollte im Textfeld **Titel** der App-Name angezeigt werden, den Sie in Schritt 4 eingeben. Wählen Sie **die Registerkarte** Berechtigungen aus, um die folgenden Berechtigungsanforderungen für die App hinzuzufügen (siehe Abbildung 2): 
    
   - Wählen Sie in der ersten Zeile der **Liste Berechtigungsanforderungen** in der Spalte **Bereich** in der Dropdownliste **Statusing** aus. Wählen Sie **in der Spalte** Berechtigung die Option **SubmitStatus aus.**
    
   - Fügen Sie eine Zeile hinzu, in der **Scope** mehrere **Projekte** und die **Berechtigung Read** **ist.**
    
   **Abbildung 2. Festlegen des Berechtigungsbereichs für eine Status-App**

   ![Festlegen des Berechtigungsumfangs für eine Statuserfassungs-App](media/pj15_CreateStatusingApp_PermissionScope.gif "Festlegen des Berechtigungsumfangs für eine Statuserfassungs-App")
  
Die **QuickStatus-App** ermöglicht es einem Project Web App-Benutzer, Zuordnungen für den Benutzer aus mehreren Projekten zu lesen, den abgeschlossenen Zuordnungsprozentl zu ändern und das Update zu übermitteln. Die anderen Berechtigungsanforderungsbereiche, die in der Dropdownliste in Abbildung 2 angezeigt werden, sind für diese App nicht erforderlich. Die Berechtigungsanforderungsbereiche sind die Berechtigungen, die die App im Auftrag des Benutzers anfordert. Wenn der Benutzer nicht über diese Berechtigungen in Project Web App verfügt, wird die App nicht ausgeführt. Eine App kann über mehrere Berechtigungsanforderungsbereiche verfügen, einschließlich derer für andere SharePoint Berechtigungen, sollte jedoch nur über das für die App-Funktionalität erforderliche Minimum verfügen. Im Folgenden finden Sie die Berechtigungsanforderungsbereiche, die sich auf Project Server bezogen haben: 

- **Enterprise Ressourcen**: Ressourcen-Manager-Berechtigungen zum Lesen oder Schreiben von Informationen zu anderen Project Web App-Benutzern.
    
- **Mehrere Projekte**: Lese- oder Schreibzugriff auf mehrere Projekte, bei denen der Benutzer über die angeforderten Berechtigungen verfügt.
    
- **Project Server**: Erfordert, dass der App-Benutzer über Administratorberechtigungen für Project Web App verfügt.
    
- **Reporting**: Read the **ProjectData** OData service for Project Web App (requires only log on permission for Project Web App). 
    
- **Single Project**: Lese- oder Schreibzugriff auf ein Projekt, in dem der Benutzer über die angeforderten Berechtigungen verfügt.
    
- **Statusing**: Übermitteln von Aktualisierungen für den Status von Zuordnungen, z. B. Arbeitsstunden, Prozent abgeschlossene und neue Zuordnungen.
    
- **Workflow**: Wenn der Benutzer über die Berechtigung zum Ausführen Project Serverworkflows verfügt, wird die App mit erhöhten Berechtigungen für den Workflow ausgeführt.
    
Weitere Informationen zu Berechtigungsanforderungsbereich für Project Server 2013 finden Sie im Abschnitt *Project-Apps* unter [Updates for developers in Project 2013](updates-for-developers-in-project-2013.md) und [App permissions in SharePoint 2013](https://msdn.microsoft.com/library/fp142383.aspx).


<a name="pj15_StatusingApp_HTML"> </a>

### <a name="creating-the-html-content-for-the-quickstatus-app"></a>Erstellen des HTML-Inhalts für die QuickStatus-App

Bevor Sie mit dem Codieren der HTML-Inhalte beginnen, entwerfen Sie die Benutzeroberfläche und die Benutzeroberfläche für die QuickStatus-App (Abbildung 3 zeigt ein Beispiel für die abgeschlossene Seite). Ein Entwurf kann auch eine Gliederung der JavaScript-Funktionen enthalten, die mit dem HTML-Code interagieren. Allgemeine Informationen finden Sie unter [UX design for apps in SharePoint 2013](https://msdn.microsoft.com/library/fp179934.aspx).
  
**Abbildung 3. Design der QuickStatus-App-Seite**

![Design der QuickStatus-App-Seite](media/pj15_CreateStatusingApp_AfterRefresh.gif "Design der QuickStatus-App-Seite")
  
Die App zeigt den Anzeigenamen oben an, der der Wert des **Title-Elements** in AppManifest.xml. 
  
Standardmäßig verwendet die Seite HTML5. Nachfolgend finden Sie die Standard-HTML-Elemente für die hauptbenutzeroberflächenobjekte, die die **QuickStatus-App** im Textkörper der Seite enthält: 
  
- Ein **Formularelement** enthält alle anderen Benutzeroberflächenelemente. 
    
- Ein **Fieldset-Element** erstellt einen Container und einen Rahmen für die Zuordnungstabelle. Das untergeordnete **Legendenelement** enthält eine Bezeichnung für den Container. 
    
- Ein **Tabellenelement** enthält eine Beschriftung und nur eine Tabellenkopfzeile. JavaScript-Funktionen ändern die Tabellenbeschriftung und fügen Zeilen für die Zuordnungen hinzu. 
    
   > [!NOTE]
   > Zum einfachen Hinzufügen von Auslagerungen und Sortierungen würde eine Produktions-App wahrscheinlich ein kommerzielles jQuery-basiertes Rastersteuerelement anstelle einer Tabelle verwenden. 
  
   Die Tabelle enthält Spalten für den Projektnamen, den Vorgangsnamen mit einem Kontrollkästchen, die aktuelle Arbeit, den Abgeschlossenen Prozentbetrag, die verbleibende Arbeit und den Zuordnungsendtermin. JavaScript-Funktionen erstellen das Kontrollkästchen und das Texteingabefeld für den Prozentbereich, der für jeden Vorgang abgeschlossen ist.
    
- Ein **Eingabeelement** für ein Textfeld legt für alle ausgewählten Zuordnungen den vollständigen Prozentbereich fest. 
    
- Ein **Schaltflächenelement** übermittelt die Statusänderungen. 
    
- Ein **Schaltflächenelement** aktualisiert die Seite. 
    
- Ein **Schaltflächenelement** beendet die App und kehrt zur Seite Aufgaben in Project Web App zurück. 
    
Das untere Textfeld und  die Schaltflächenelemente befinden sich innerhalb von div-Elementen, sodass CSS die Position und Darstellung der Benutzeroberflächenobjekte problemlos verwalten kann. Eine JavaScript-Funktion fügt am unteren Rand der Seite einen Absatz hinzu, der Ergebnisse für den Erfolg oder Fehler der Statusaktualisierung enthält. 
  
### <a name="procedure-2-to-create-the-html-content"></a>Vorgehensweise 2: So erstellen Sie den HTML-Inhalt

1. Öffnen Visual Studio die Datei "Default.aspx".
    
   Die Datei enthält zwei **asp:Content-Elemente:** Das Element mit dem Attribut wird innerhalb der Seitenkopfzeile hinzugefügt, und das Element mit dem Attribut wird innerhalb des  `ContentPlaceHolderID="PlaceHolderAdditionalPageHead"`  `ContentPlaceHolderID="PlaceHolderMain"` **Seitentextelements** platziert. 
    
2. Fügen Sie im Steuerelement für die Seitenkopfzeile einen Verweis auf die PS.js auf dem `<asp:Content ContentPlaceHolderID="PlaceHolderAdditionalPageHead" runat="server">` Servercomputer Project hinzu. Zum Testen und Debuggen können Sie PS.debug.js. 
    
   ```HTML
     <script type="text/javascript" src="/_layouts/15/ps.debug.js"></script>
   ```

   Die App-Infrastruktur verwendet das `/_layouts/15/` virtuelle Verzeichnis für SharePoint in IIS. Die physische Datei ist  `%ProgramFiles%\Common Files\Microsoft Shared\Web Server Extensions\15\TEMPLATE\LAYOUTS\PS.debug.js` .
    
   > [!NOTE]
   > Entfernen Sie vor der Bereitstellung der App für die Produktionsnutzung aus den  `.debug` Skriptverweisen, um die Leistung zu verbessern. 
  
3. Löschen Sie im Steuerelement für den Seitentext das generierte div-Element, und fügen Sie dann den `<asp:Content ContentPlaceHolderID="PlaceHolderMain" runat="server">` HTML-Code  für die Benutzeroberflächenobjekte hinzu. Das **Tabellenelement** enthält nur eine Kopfzeile. Die **Spalte Vorgangsname** enthält ein Eingabesteuerelement des Kontrollkästchens. Text für das **Caption-Element** wird durch den **onGetUserNameSuccess-Rückruf** für die **getUserInfo-Funktion** in der App.js ersetzt. 
    
    ```HTML
    <form>
        <fieldset>
        <legend>Select assigned tasks</legend>
        <table id="assignmentsTable">
            <caption id="tableCaption">Replace caption</caption>
            <thead>
            <tr id="headerRow">
                <th>Project name</th>
                <th><input type="checkbox" id="headercheckbox" checked="checked" />Task name</th>
                <th>Actual work</th>
                <th>% complete</th>
                <th>Remaining work</th>
                <th>Due date</th>
            </tr>
            </thead>
        </table>
        </fieldset>
        <div id="inputPercentComplete" >
        Set percent complete for all selected assignments, or leave this
        <br /> field blank and set percent complete for individual assignments: 
        <input type="text" name="percentComplete" id="pctComplete" size="4"  maxlength="4" />
        </div>
        <div id="submitResult">
        <p><button id="btnSubmitUpdate" type="button" class="bottomButtons" ></button></p>
        <p id="message"></p>
        </div>
        <div id="refreshPage">
        <p><button id="btnRefresh" type="button" class="bottomButtons" >Refresh</button></p>
        </div>
        <div id="exitPage">
        <p><button id="btnExit" type="button" class="bottomButtons" >Exit</button></p>
        </div>
    </form>
    ```

4. Fügen Sie in der Datei App.css CSS-Code für die Position und Darstellung der Benutzeroberflächenelemente hinzu. Den vollständigen CSS-Code der **QuickStatus-App** finden Sie im Abschnitt [Beispielcode für die QuickStatus-App.](#pj15_StatusingApp_Example) 
    
Prozedur 3 fügt die JavaScript-Funktionen hinzu, um die Zuordnungen zu lesen und die Tabellenzeilen zu erstellen sowie den Abgeschlossenen Zuordnungsprozentsatz zu ändern und zu aktualisieren. Die eigentlichen Schritte sind iterativer bei der Entwicklung einer App, in der Sie abwechselnd einen Teil des HTML-Codes erstellen, verwandte Formatvorlagen und JavaScript-Funktionen hinzufügen und testen, mehr HTML-Code ändern oder hinzufügen und dann den Prozess wiederholen.

<a name="pj15_StatusingApp_JavaScript"> </a>

### <a name="creating-the-javascript-functions-for-the-quickstatus-app"></a>Erstellen der JavaScript-Funktionen für die QuickStatus-App

Die Visual Studio-Vorlage für eine SharePoint-App enthält die App.js-Datei, die den Standard initialisierungscode enthält, der den SharePoint-Clientkontext abgibt und grundlegende Get- und Set-Aktionen für die App-Seite veranschaulicht. Der JavaScript-Namespace für SharePoint clientseitige SP.js ist **SP**. Da eine Project Server-App die PS.js verwendet, verwendet  die App den PS-Namespace, um den Clientkontext zu erhalten und auf das JSOM für Project Server zugreift. 
  
JavaScript-Funktionen in der **QuickStatus-App** umfassen Folgendes: 
  
- Der **dokumentbereite** Ereignishandler wird ausgeführt, wenn das Dokumentobjektmodell (DOCUMENT Object Model, DOM) instanziiert wird. Der  ready-Ereignishandler führt die folgenden vier Schritte aus: 
    
    1. Initialisiert die **globale ProjContext-Variable** mit dem Clientkontext für Project Server JSOM und **die globale pwaWeb-Variable.** 
        
    2. Ruft die **getUserInfo-Funktion** auf, um die **globale ProjUser-Variable** zu initialisieren. 
        
    3. Ruft die **getAssignments-Funktion** auf, die angegebene Zuweisungsdaten für den Benutzer ab ruft. 
        
    4. Binds click event handlers to the table header check box, and to the check boxes in each row of the table. Die Click-Ereignishandler verwalten das aktivierte **Attribut** der Kontrollkästchen, wenn der Benutzer ein Kontrollkästchen in der Tabelle auswählt oder auswählt. 
    
- Wenn die **getAssignments-Funktion** erfolgreich ist, ruft sie die **onGetAssignmentsSuccess-Funktion** auf. Diese Funktion fügt für jede Zuordnung eine Zeile in die Tabelle ein, initialisiert die HTML-Steuerelemente in jeder Zeile und initialisiert dann die Eigenschaften der unteren Schaltfläche. 
    
- Der **onClick-Ereignishandler** für die **Schaltfläche Update** ruft die **updateAssignments-Funktion** auf. Diese Funktion ruft den vollständigen Prozentwert ab, der auf jede ausgewählte Zuordnung angewendet wird. oder wenn das vollständige Textfeld Prozent leer ist, ruft die Funktion den Prozent abgeschlossen jeder ausgewählten Zuordnung in der Tabelle ab. Die **updateAssignments-Funktion** speichert und übermittelt dann die Statusupdates und schreibt eine Meldung über die Ergebnisse an den unteren Rand der Seite. 
    
### <a name="procedure-3-to-create-the-javascript-functions"></a>Verfahren 3. So erstellen Sie die JavaScript-Funktionen

1. Öffnen Visual Studio die Datei App.js, und löschen Sie dann alle Inhalte in der Datei.
    
2. Fügen Sie die globalen Variablen und den **dokumentbereiten Ereignishandler** hinzu. Auf **das Dokumentobjekt** wird mithilfe einer jQuery-Funktion zugegriffen. 
    
   Das Kontrollkästchen Click-Ereignishandler für die Tabellenkopfzeile legt den aktivierten Status der Zeilenkontrollkästchen fest. Wenn alle Zeilenkontrollkästchen aktiviert sind oder alle aktiviert sind, wird der aktivierte Status des Kopfzeilenkontrollkästchens durch den Click-Ereignishandler für die Zeilen aktiviert. Die Click-Ereignishandler legen auch die Ergebnismeldung am unteren Rand der Seite auf eine leere Zeichenfolge fest.
    
   ```js
    var projContext;
    var pwaWeb;
    var projUser;
    // This code runs when the DOM is ready and creates a ProjectContext object.
    // The ProjectContext object is required to use the JSOM for Project Server.
    $(document).ready(function () {
        projContext = PS.ProjectContext.get_current();
        pwaWeb = projContext.get_web();
        getUserInfo();
        getAssignments();
        // Bind a click event handler to the table header check box, which sets the row check boxes
        // to the checked state of the header check box, and sets the results message to an empty string.
        $('#headercheckbox').live('click', function (event) {
            $('input:checkbox:not(#headercheckbox)').attr('checked', this.checked);
            $get("message").innerText = "";
        });
        // Bind a click event handler to the row check boxes. If any row check box is cleared, clear
        // the header check box. If all of the row check boxes are selected, select the header check box.
        $('input:checkbox:not(#headercheckbox)').live('click', function (event) {
            var isChecked = true;
            $('input:checkbox:not(#headercheckbox)').each(function () {
                if (this.checked == false) isChecked = false;
                $get("message").innerText = "";
            });
            $("#headercheckbox").attr('checked', isChecked);
        });
    });
   ```

3. Fügen Sie **die getUserInfo-Funktion** hinzu, die **onGetUserNameSuccess** aufruft, wenn die Abfrage erfolgreich ist. Die **onGetUserNameSuccess-Funktion** ersetzt den  Inhalt des Beschriftungsab absatzes durch eine Tabellenbeschriftung, die den Benutzernamen enthält. 
    
   ```js
        // Get information about the current user.
        function getUserInfo() {
            projUser = pwaWeb.get_currentUser();
            projContext.load(projUser);
            projContext.executeQueryAsync(onGetUserNameSuccess,
                // Anonymous function to execute if getUserInfo fails.
                function (sender, args) {
                    alert('Failed to get user name. Error: ' + args.get_message());
            });
        } 
        // This function is executed if the getUserInfo call is successful.
        function onGetUserNameSuccess() {
            var prefaceInfo = 'Assignments for ' + projUser.get_title();
            $('#tableCaption').text(prefaceInfo);
        }
   ```

4. Fügen Sie **die getAssignments-Funktion** hinzu, die **onGetAssignmentsSuccess aufruft** (siehe Schritt 5), wenn die Zuweisungsabfrage erfolgreich ist. Die **Option Include** schränkt die Abfrage so ein, dass nur die angegebenen Felder zurückgegeben werden. 
    
   ```js
    // Get the collection of assignments for the current user.
    function getAssignments() {
        assignments = PS.EnterpriseResource.getSelf(projContext).get_assignments();
        // Register the request that you want to run on the server. The optional "Include" parameter 
        // requests only the specified properties for each assignment in the collection.
        projContext.load(assignments,
            'Include(Project, Name, ActualWork, ActualWorkMilliseconds, PercentComplete, RemainingWork, Finish, Task)');
        // Run the request on the server.
        projContext.executeQueryAsync(onGetAssignmentsSuccess,
            // Anonymous function to execute if getAssignments fails.
            function (sender, args) {
                alert('Failed to get assignments. Error: ' + args.get_message());
            });
    }
   ```

5. Fügen Sie **die onGetAssignmentsSuccess-Funktion** hinzu, die der Tabelle eine Zeile für jede Zuordnung hinzufügt. Die **prevProjName-Variable** wird verwendet, um zu bestimmen, ob eine Zeile für ein anderes Projekt gilt. Wenn ja, wird der Projektname in fett formatierter Schriftart angezeigt. Andern falls nicht, wird der Projektname auf eine leere Zeichenfolge festgelegt. 
    
   > [!NOTE]
   > Das JSOM enthält keine **TimeSpan-Eigenschaften,** die das CSOM enthält, z. B. **ActualWorkTimeSpan**. Stattdessen verwendet das JSOM Eigenschaften für die Anzahl von Millisekunden, z. [B. ps. StatusAssignment.actualWorkMilliseconds-Eigenschaft.](https://msdn.microsoft.com/library/736bce1e-f734-0efe-6c5f-e0e891ab00ef%28Office.15%29.aspx) Die Methode zum Erhalten dieser Eigenschaft **ist \_ actualWorkMilliseconds**, die einen ganzzahligen Wert zurückgibt. > Die **get_actualWork-Methode** gibt eine Zeichenfolge wie "3h" zurück. Sie können einen der Werte in der **QuickStatus-App** verwenden, ihn jedoch anders anzeigen. Die Zuordnungsabfrage enthält beide Eigenschaften, sodass Sie den Wert während des Debuggens testen können. Wenn Sie die **actualWork-Variable** entfernen, können Sie auch die **ActualWork-Eigenschaft** in der Zuweisungsabfrage entfernen. 
  
   Schließlich initialisiert **die onGetAssignmentsSuccess-Funktion** die Schaltfläche **Update** und die **Schaltfläche Aktualisieren** mit Click-Ereignishandlern. Der Textwert der Schaltfläche **Aktualisieren** kann auch im HTML-Code festgelegt werden. 
    
   ```js
        // Get the enumerator, iterate through the assignment collection, 
        // and add each assignment to the table.
        function onGetAssignmentsSuccess(sender, args) {
            if (assignments.get_count() > 0) {
                var assignmentsEnumerator = assignments.getEnumerator();
                var projName = "";
                var prevProjName = "3D2A8045-4920-4B31-B3E7-9D0C5195FC70"; // Any unique name.
                var taskNum = 0;
                var chkTask = "";
                var txtPctComplete = "";
                // Constants for creating input controls in the table.
                var INPUTCHK = '<input type="checkbox" class="chkTask" checked="checked" id="chk';
                var LBLCHK = '<label for="chk';
                var INPUTTXT = '<input type="text" size="4"  maxlength="4" class="txtPctComplete" id="txt';
                while (assignmentsEnumerator.moveNext()) {
                    var statusAssignment = assignmentsEnumerator.get_current();
                    projName = statusAssignment.get_project().get_name();
                    // Get an integer, such as 3600000.
                    var actualWorkMilliseconds = statusAssignment.get_actualWorkMilliseconds(); 
                    // Get a string, such as "1h". Not used here.
                    var actualWork = statusAssignment.get_actualWork();
                    if (projName === prevProjName) {
                        projName = "";
                    }
                    prevProjName = statusAssignment.get_project().get_name();
                    // Create a row for the assignment information.
                    var row = assignmentsTable.insertRow();
                    taskNum++;
                    // Create an HTML string with a check box and task name label, for example:
                    // <input type="checkbox" class="chkTask" checked="checked" id="chk1" /> <label for="chk1">Task 1</label>
                    chkTask = INPUTCHK + taskNum + '" /> ' + LBLCHK + taskNum + '">' 
                        + statusAssignment.get_name() + '</label>';
                    txtPctComplete = INPUTTXT + taskNum + '" />';
                    // Insert cells for the assignment properties.
                    row.insertCell().innerHTML = '<strong>' + projName + '</strong>';
                    row.insertCell().innerHTML = chkTask;
                    row.insertCell().innerText = actualWorkMilliseconds / 3600000 + 'h';
                    row.insertCell().innerHTML = txtPctComplete;
                    row.insertCell().innerText = statusAssignment.get_remainingWork();
                    row.insertCell().innerText = statusAssignment.get_finish();
                    // Initialize the percent complete cell.
                    $get("txt" + taskNum).innerText = statusAssignment.get_percentComplete() + '%'
                }
            }
            else {
                $('p#message').attr('style', 'color: #0f3fdb');     // Blue text.
                $get("message").innerText = projUser.get_title() + ' has no assignments'
            }
            // Initialize the button properties.
            $get("btnSubmitUpdate").onclick = function() { updateAssignments(); };
            $get("btnSubmitUpdate").innerText = 'Update';
            $get('btnRefresh').onclick = function () { window.location.reload(true); };
            $get('btnExit').onclick = function () { exitToPwa(); };
        }
   ```

6. Fügen Sie **den updateAssignments-Click-Ereignishandler** für die Schaltfläche **Aktualisieren** hinzu. Wenn der Benutzer einen Wert für den abgeschlossenen Prozentwert eines Vorgangs ändert oder einen Wert im Textfeld **percentComplete** hinzufügt, kann der Wert in mehreren Formaten eingegeben werden, z. B. "60", "60 %" oder "60 %". Die **getNumericValue-Methode** gibt den numerischen Wert des Eingabetexts zurück. 
    
   > [!NOTE]
   > In einer App, die für die Produktionsnutzung konzipiert ist, sollten Eingabewerte für numerische Informationen die Feldüberprüfung und zusätzliche Fehlerüberprüfung umfassen. 
  
   Das **UpdateAssignments-Beispiel** enthält einige grundlegende Fehlerüberprüfungen  und zeigt Informationen im Nachrichtenab absatz am unteren Rand der Seite an– grün, wenn die Aktualisierungsabfrage erfolgreich ist, und rot, wenn ein Eingabefehler auftritt oder die Aktualisierungsabfrage nicht erfolgreich ist. 
    
   Vor der Verwendung der **submitAllStatusUpdates-Methode** muss die App die Updates auf dem Server mithilfe der **PS speichern. StatusAssignmentCollection.update-Methode.** 
    
   ```js
        // Update all checked assignments. If the bottom percent complete field is blank,
        // use the value in the % complete field of each selected row in the table.
        function updateAssignments() {
            // Get percent complete from the bottom text box.
            var pctCompleteMain = getNumericValue($('#pctComplete').val()).trim();
            var pctComplete = pctCompleteMain;
            var assignmentsEnumerator = assignments.getEnumerator();
            var taskNum = 0;
            var taskRow = "";
            var indexPercent = "";
            var doSubmit = true;
            while (assignmentsEnumerator.moveNext()) {
                var pctCompleteRow = "";
                taskRow = "chk" + ++taskNum;
                if ($get(taskRow).checked) {
                    var statusAssignment = assignmentsEnumerator.get_current();
                    if (pctCompleteMain === "") {
                        // Get percent complete from the text box field in the table row.
                        pctCompleteRow = getNumericValue($('#txt' + taskNum).val());
                        pctComplete = pctCompleteRow;
                    }
                    // If both percent complete fields are empty, show an error.
                    if (pctCompleteMain === "" && pctCompleteRow === "") {
                        $('p#message').attr('style', 'color: #e11500');     // Red text.
                        $get("message").innerHTML =
                            '<b>Error:</b> Both <i>Percent complete</i> fields are empty, in row '
                            + taskNum
                            + ' and in the bottom textbox.<br/>One of those fields must have a valid percent.'
                            + '<p>Please refresh the page and try again.</p>';
                        doSubmit = false;
                        taskNum = 0;
                        break;
                    }
                    if (doSubmit) statusAssignment.set_percentComplete(pctComplete);
                }
            } 
            // Save and submit the assignment updates.
            if (doSubmit) {
                assignments.update();
                assignments.submitAllStatusUpdates();
                projContext.executeQueryAsync(function (source, args) {
                    $('p#message').attr('style', 'color: #0faa0d');     // Green text.
                    $get("message").innerText = 'Assignments have been updated.';
                }, function (source, args) {
                    $('p#message').attr('style', 'color: #e11500');     // Red text.
                    $get("message").innerText = 'Error updating assignments: ' + args.get_message();
                });
            }
        }
        // Get the numeric part for percent complete, from a string. For example, with "20 %", return "20".
        function getNumericValue(pctComplete) {
            pctComplete = pctComplete.trim();
            pctComplete = pctComplete.replace(/ /g, "");    // Remove interior spaces.
            indexPercent = pctComplete.indexOf('%', 0);
            if (indexPercent > -1) pctComplete = pctComplete.substring(0, indexPercent);
            return pctComplete;
        }
   ```

7. Fügen Sie **die exitToPwa-Funktion** hinzu, die den **SPHostUrl-Abfragezeichenfolgenparameter** für die URL der Host-Project Web App-Website verwendet. Um zur Seite Aufgaben zurück zu navigieren, fügen Sie  `"/Tasks.aspx"` die URL an. Die variable **spHostUrl** wird beispielsweise auf  `https://ServerName/ProjectServerName/Tasks.aspx` festgelegt.
    
   Die **getQueryStringParameter-Funktion** teilt die URL der **QuickStatus-Seite** auf, um den angegebenen Parameter in den URL-Optionen zu extrahieren und zurückzukehren. Im Folgenden finden Sie ein Beispiel für das **Dokument. URL-Wert** für das **QuickStatus-Dokument** (alle in einer Zeile): 
    
   ```HTML
    https://app-ef98082fa37e3c.servername.officeapps.selfhost.corp.microsoft.com/pwa/
        QuickStatus/Pages/Default.aspx
        ?SPHostUrl=https%3A%2F%2Fsphvm%2D85178%2Fpwa
        &SPLanguage=en%2DUS
        &SPClientTag=1
        &SPProductNumber=15%2E0%2E4420%2E1022
        &SPAppWebUrl=https%3A%2F%2Fapp%2Def98082fa37e3c%2Eservername
            %2Eofficeapps%2Eselfhost%2Ecorp%2Emicrosoft%2Ecom%2Fpwa%2FQuickStatus
   ```

   Für die vorherige URL gibt **die GetQueryStringParameter-Funktion** den **SPHostUrl-Abfragezeichenfolgenwert** zurück,  `https://ServerName/pwa` . 
    
   ```js
        // Exit the QuickStatus page and go back to the Tasks page in Project Web App.
        function exitToPwa() {
            // Get the SharePoint host URL, which is the top page of PWA, and add the Tasks page.
            var spHostUrl = decodeURIComponent(getQueryStringParameter('SPHostUrl'))
                            + "/Tasks.aspx";
            // Set the top window for the QuickStatus IFrame to the Tasks page.
            window.top.location.href = spHostUrl;
        }
        // Get a specified query string parameter from the {StandardTokens} URL option string.
        function getQueryStringParameter(urlParameterKey) {
            var docUrl = document.URL;
            var params = docUrl.split('?')[1].split('&');
            for (var i = 0; i < params.length; i++) {
                var theParam = params[i].split('=');
                if (theParam[0] == urlParameterKey)
                    return decodeURIComponent(theParam[1]);
            }
        }
   ```

Wenn Sie die **QuickStatus-App** zu diesem Zeitpunkt veröffentlichen und Project Web App hinzufügen, kann die App auf der Seite Websiteinhalte ausgeführt werden, für Benutzer ist sie jedoch nicht einfach verfügbar. Damit Benutzer die App finden und ausführen können, können Sie dem Menüband auf der Seite Aufgaben eine Schaltfläche hinzufügen. In Prozedur 4 wird gezeigt, wie Sie eine benutzerdefinierte Menübandaktion hinzufügen. 

<a name="pj15_StatusingApp_ribbon"> </a>

### <a name="adding-a-ribbon-custom-action"></a>Hinzufügen einer benutzerdefinierten Menübandaktion

Menübandregisterkarten, Gruppen und Steuerelemente für Project Web App werden in der pwaribbon.xml-Datei angegeben, die im Verzeichnis auf dem Computer installiert ist, auf dem `[Program Files]\Common Files\Microsoft Shared\Web Server Extensions\15\TEMPLATE\FEATURES\PWARibbon\listtemplates` Project Server ausgeführt wird. Um benutzerdefinierte Aktionen für das Menüband Project Web App zu entwerfen, enthält der Project 2013 SDK-Download eine Kopie pwaribbon.xml. 
  
Project Web App verwendet unterschiedliche Menübanddefinitionen für die Seite Aufgaben, je nachdem, ob die Project Web App-Instanz den Modus für einmalige Eingaben verwendet, mit dem Benutzer Werte für die Arbeitszeittabelle und den Aufgabenstatus eingeben können. Wenn Sie über Administratorberechtigungen für Project Web App verfügen, wählen Sie zum Bestimmen des Eintragsmodus **PWA Einstellungen** im Dropdownmenü Einstellungen in der oberen rechten Ecke der Seite aus. Wählen Sie PWA Einstellungen Seite Arbeitszeittabelle Einstellungen und Standardwerte aus, und sehen  Sie sich dann das Kontrollkästchen Einzelner **Eintragsmodus** am unteren Rand der Seite an. 
  
Wenn der Einzeleingabemodus deaktiviert ist, wird das Menüband auf der Seite Aufgaben durch den Bereich Meine Arbeit in der pwaribbon.xml: 
  
```XML
   <!-- REGION My Work Ribbon-->
   <CustomAction
      Id="Ribbon.ContextualTabs.MyWork"
      . . .
```

Wenn der Modus für einen einzelnen Eintrag aktiviert ist, wird das Seitenband Aufgaben durch den Bereich Gebundener Modus in der pwaribbon.xml: 
  
```XML
   <!-- REGION Tied Mode Ribbon-->
   <CustomAction
      Id="Ribbon.ContextualTabs.TiedMode"
      . . .
```

Obwohl die Gruppen und Steuerelemente in den einzelnen Regionen ähnlich aussehen, kann ein Steuerelement für den gebundenen Modus eine andere Funktion als das gleiche Steuerelement für den nicht gebundenen Modus aufrufen. In Prozedur 4 wird gezeigt, wie Sie ein Schaltflächensteuerelement für die **QuickStatus-App** hinzufügen, wenn der Modus für den einzelnen Eintrag deaktiviert ist (das Kontrollkästchen Einzelner **Eintragsmodus** ist deaktiviert). 
  
> [!NOTE]
> Allgemeine Informationen zum Hinzufügen benutzerdefinierter Aktionen zu einem Menüband oder zu einem Menü in einer SharePoint-Anwendung finden Sie unter [Create custom actions to deploy with apps for SharePoint](https://msdn.microsoft.com/library/jj163954.aspx). 
  
### <a name="procedure-4-to-add-a-ribbon-custom-action-to-the-tasks-page"></a>Prozedur 4. So fügen Sie der Seite Aufgaben eine benutzerdefinierte Menübandaktion hinzu

1. Untersuchen Sie das Menüband auf der Seite Aufgaben in Project Web App. Wählen Sie auf **dem** Menüband die Registerkarte AUFGABEN aus, und planen Sie, wie sie geändert werden soll. Es gibt sieben Gruppen, z. **B. Submit**, **Tasks** und **Period**. Die **Gruppe** Übermitteln verfügt über zwei Steuerelemente, eine **Schaltfläche Speichern** und ein Dropdownmenü Status senden.  Sie können ein Steuerelement an einem beliebigen Ort in einer Gruppe hinzufügen, eine Gruppe mit einem neuen Steuerelement an einem beliebigen Speicherort auf der Registerkarte AUFGABEN hinzufügen oder eine weitere Menübandregisterkarte mit benutzerdefinierten Gruppen und Steuerelementen hinzufügen.  In diesem Beispiel fügen wir der  Gruppe Übermitteln eine dritte Schaltfläche hinzu, in der die Schaltfläche die URL der **QuickStatus-App** aufruft. 
    
2. Klicken Sie **im** Bereich Projektmappen-Explorer in Visual Studio mit der rechten Maustaste auf das **Projekt QuickStatus,** und fügen Sie dann ein neues Element hinzu. Wählen Sie im Dialogfeld **Neues Element** hinzufügen die Option **Benutzerdefinierte Menübandaktion** aus (siehe Abbildung 4). Nennen Sie beispielsweise die benutzerdefinierte Aktion RibbonQuickStatusAction, und wählen Sie dann **Hinzufügen aus.**
    
   **Abbildung 4. Hinzufügen einer benutzerdefinierten Menübandaktion**

   ![Hinzufügen einer benutzerdefinierten Menübandaktion](media/pj15_CreateStatusingApp_AddRibbonCustomAction.gif "Hinzufügen einer benutzerdefinierten Menübandaktion")
  
3. Lassen Sie auf  der ersten Seite des Assistenten Benutzerdefinierte Aktion für Menüband erstellen die Option **Hostweb** ausgewählt, **wählen** Sie in der Dropdownliste keine für den benutzerdefinierten Aktionsbereich aus, und wählen Sie dann **Weiter** aus (siehe Abbildung 5). Die Elemente in den Dropdownlisten sind relevant für SharePoint, nicht für Project Server. Wir ersetzen den Großteil der generierten XML für die benutzerdefinierte Aktion, sodass sie auf Project angewendet wird. 
    
   **Abbildung 5. Angeben von Eigenschaften für die benutzerdefinierte Menübandaktion**

   ![Festlegen von Eigenschaften für die benutzerdefinierte Menübandaktion](media/pj15_CreateStatusingApp_RibbonCustomAction2.gif "Festlegen von Eigenschaften für die benutzerdefinierte Menübandaktion")
  
4. Lassen Sie auf  der nächsten Seite des Assistenten Benutzerdefinierte Aktion für Menüband erstellen alle Standardwerte für die Einstellungen, und wählen Sie dann **Fertig** stellen aus (siehe Abbildung 6). Visual Studio erstellt den **Ordner RibbonQuickStatusAction,** der eine Elements.xml enthält. 
    
   **Abbildung 6. Angeben der Einstellungen für ein Schaltflächensteuerelement**

   ![Festlegen der Einstellungen für ein Schaltflächensteuerelement](media/pj15_CreateStatusingApp_RibbonCustomAction3.gif "Festlegen der Einstellungen für ein Schaltflächensteuerelement")
  
5. Ändern Sie den standardmäßig generierten Code in der Elements.xml für die benutzerdefinierte Menübandaktion. Im Folgenden finden Sie den standardmäßigen XML-Code:
    
   ```XML
    <?xml version="1.0" encoding="utf-8"?>
    <Elements xmlns="http://schemas.microsoft.com/sharepoint/">
        <CustomAction Id="21ea3aaf-79e5-4aac-9479-8eef14b4d9df.RibbonQuickStatusAction"
                    Location="CommandUI.Ribbon"
                    Sequence="10001"
                    Title="Invoke &apos;RibbonQuickStatusAction&apos; action">
        <CommandUIExtension>
            <!-- 
            Update the UI definitions below with the controls and the command actions
            that you want to enable for the custom action.
            -->
            <CommandUIDefinitions>
            <CommandUIDefinition Location="Ribbon.ListItem.Actions.Controls._children">
                <Button Id="Ribbon.ListItem.Actions.RibbonQuickStatusActionButton"
                        Alt="Request RibbonQuickStatusAction"
                        Sequence="100"
                        Command="Invoke_RibbonQuickStatusActionButtonRequest"
                        LabelText="Request RibbonQuickStatusAction"
                        TemplateAlias="o1"
                        Image32by32="_layouts/15/images/placeholder32x32.png"
                        Image16by16="_layouts/15/images/placeholder16x16.png" />
            </CommandUIDefinition>
            </CommandUIDefinitions>
            <CommandUIHandlers>
            <CommandUIHandler Command="Invoke_RibbonQuickStatusActionButtonRequest"
                                CommandAction="~appWebUrl/Pages/Default.aspx"/>
            </CommandUIHandlers>
        </CommandUIExtension >
        </CustomAction>
    </Elements>
   ```

   1. Löschen Sie **im CustomAction-Element** das **Sequence-Attribut** und das **Title-Attribut.** 
    
   2. Um der Gruppe  Übermitteln ein Steuerelement hinzuzufügen, suchen Sie die erste Gruppe in der Auflistung in der pwaribbon.xml-Datei, die das Element ist, das `Ribbon.ContextualTabs.MyWork.Home.Groups` beginnt, `<Group Id="Ribbon.ContextualTabs.MyWork.Home.Page" Command="PageGroup" Sequence="10" Title="$Resources:pwafeatures,PAGE_PDP_CM_SUBMIT"` . Um der Gruppe Übermitteln  ein untergeordnetes Steuerelement hinzuzufügen, zeigt der folgende Code das richtige **Location-Attribut** des **CommandUIDefinition-Elements** in Elements.xml Datei: 
    
      ```XML
        <CommandUIDefinitions>
          <CommandUIDefinition Location="Ribbon.ContextualTabs.MyWork.Home.Page.Controls._children">
             . . .
          </CommandUIDefinition>
        </CommandUIDefinitions>
      ```

   3. Ändern Sie die Attributwerte des **untergeordneten Button-Elements** wie folgt: 
    
       ```XML
            <Button Id="Ribbon.ContextualTabs.MyWork.Home.Page.QuickStatus"
                    Alt="Quick Status app"
                    Sequence="30"
                    Command="Invoke_QuickStatus"
                    LabelText="Quick Status"
                    TemplateAlias="o1"
                    Image16by16="_layouts/15/1033/images/ps16x16.png" 
                    Image16by16Left="-80"
                    Image16by16Top="-144"
                    Image32by32="_layouts/15/1033/images/ps32x32.png" 
                    Image32by32Left="-32"
                    Image32by32Top="-288" 
                    ToolTipTitle="QuickStatus"
                    ToolTipDescription="Run the QuickStatus app" />
       ```

       - Damit die Schaltfläche zum dritten Steuerelement in der Gruppe wird, kann das **Sequence-Attribut** eine beliebige Zahl höher sein als der Wert des vorhandenen  `Sequence="20"` Send **Status-Steuerelements** (ein **FlyoutAnchor-Element** in pwaribbon.xml). Standardmäßig sind die Sequenznummern von Gruppen und Steuerelementen , wodurch  `10, 20, 30, …` Elemente in Zwischenpositionen eingefügt werden können.
    
       - Das **Command-Attribut** gibt den Befehl an, der im **CommandUIHandler-Element** ausgeführt werden soll (siehe den folgenden Schritt 5.d). Sie können den Befehlsnamen vereinfachen, um es dem nächsten Entwickler zu erleichtern. Beispielsweise ist  `Command="Invoke_QuickStatus"` das Lesen einfacher als  `Command="Invoke_RibbonQuickStatusActionButtonRequest"` .
    
       - Die Bildattribute geben das 16 x 16-Pixel-Symbol und das 32 x 32-Pixel-Symbol für das Schaltflächensteuerelement an. Gibt in der Elements.xml-Datei  `Image32by32="_layouts/15/images/placeholder32x32.png"` einen orangefarbenen Punkt an. Sie können Symbole aus den Bildzuordnungsdateien (ps16x16.png und ps32x32.png) extrahieren, die im Verzeichnis auf dem Computer installiert sind, auf dem `[Program Files]\Common Files\Microsoft Shared\Web Server Extensions\15\TEMPLATE\LAYOUTS\1033\IMAGES` Project Server ausgeführt wird. Beispielsweise befindet sich das Symbol mit 32 x 32 Pixeln in der zweiten Spalte mit Symbolen von links und der zehnten Zeile unten am oberen Rand der ps32x32.png-Bildkarte (der obere Rand des Symbols liegt hinter dem Ende der neunten Zeile; 9 Zeilen x 32 Pixel/Zeile = 288 Pixel). 
    
       - Fügen Sie zum Anzeigen einer QuickInfo für das Schaltflächensteuerelement das **ToolTipTitle-Attribut** und das **ToolTipDescription-Attribut** hinzu. 
    
    4. Ändern Sie die Attribute des **CommandUIHandler-Elements.** Stellen Sie beispielsweise sicher, dass das **Command-Attribut** dem **Command-Attributwert** für das **Button-Element** entspricht. Für das **CommandAction-Attribut** `~appWebUrl` ist ein Platzhalter für die URL der **QuickStatus-Webseite.** Wenn die Menübandschaltfläche die **QuickStatus-App** aufruft, wird das **{StandardTokens}-Token** durch #A0 ersetzt, die **SPHostUrl,** **SPLanguage,** **SPClientTag,** **SPProductNumber** und **SPAppWebUrl enthalten.**
    
        ```XML
            <CommandUIHandlers>
                <CommandUIHandler Command="Invoke_QuickStatus"
                                  CommandAction="~appWebUrl/Pages/Default.aspx?{StandardTokens}"/>
            </CommandUIHandlers>
        ```

6. Öffnen Sie im Projektmappen-Explorer den **Feature1.feature-Designer,** und  verschieben Sie das  **RibbonQuickStatusAction-Element** aus dem Bereich Elemente im Projektmappenbereich in die Elemente im **Featurebereich.** Wenn Sie dann den **Package.package-Designer** öffnen, befindet sich das **RibbonQuickStatusAction-Element** im Bereich Elemente **im Bereich** Paket. 
    
Während Sie die App entwickeln und eine Menübandschaltfläche hinzufügen, testen Sie normalerweise die App und legen haltepunkte im JavaScript-Code für das Debuggen. Wenn Sie **F5** drücken, um das Debuggen zu starten, kompiliert Visual Studio die App, stellt sie auf der Website zur Verfügung, die in der **Website-URL-Eigenschaft** des **QuickStatus-Projekts** angegeben ist, und zeigt eine Seite an, die fragt, ob Sie der App vertrauen. Wenn Sie fortfahren und die **QuickStatus-App** beenden, kehrt sie zur Seite Aufgaben in Project Web App zurück. 

> [!NOTE]
> Abbildung 7 zeigt, dass die **Schaltfläche Schnellstatus** auf der Registerkarte **AUFGABEN** des Menübands deaktiviert ist. Nach vielen Debugbereitstellungen mit Visual Studio können benutzerdefinierte Menübandsteuerelemente blockiert werden, wenn Sie die veröffentlichte App weiterhin auf demselben Testserver debuggen oder bereitstellen. Um die Schaltfläche zu aktivieren, löschen Sie das **RibbonQuickStatusAction-Element** in Visual Studio, und erstellen Sie dann eine neue Menübandaktion mit einem anderen Namen und einer anderen ID. Wenn das Problem damit nicht gelöst wird, versuchen Sie, die App aus der Project Web App-Testinstanz zu entfernen, und erstellen Sie die App dann mit einer anderen App-ID neu. 
  
**Abbildung 7. Anzeigen der QuickInfo der deaktivierten Schaltfläche "Schnellstatus"**

![Anzeigen der QuickInfo der deaktivierten Schaltfläche](media/pj15_CreateStatusingApp_ButtonToolTipDisabled.gif "Anzeigen der QuickInfo der deaktivierten Schaltfläche")
  
In Verfahren 5 wird gezeigt, wie Sie die **QuickStatus-App** bereitstellen und installieren. In Verfahren 6 werden einige zusätzliche Schritte zum Testen der App nach der Installation gezeigt. 

<a name="pj15_StatusingApp_Deploying"> </a>

## <a name="deploying-the-quickstatus-app"></a>Bereitstellen der QuickStatus-App

Es gibt mehrere Möglichkeiten zum Bereitstellen einer App in SharePoint Webanwendung, z. B. Project Web App. Welche Bereitstellung Sie verwenden, hängt davon ab, ob Sie die App in einem privaten SharePoint-Katalog oder im öffentlichen Office Store veröffentlichen möchten und ob SharePoint lokal installiert ist oder ein Online-Mandanzunternehmen ist. In Verfahren 5 wird gezeigt, wie Die **QuickStatus-App** in einer lokalen Installation in einem privaten App-Katalog bereitgestellt wird. Weitere Informationen finden Sie unter [Installieren und Verwalten von Apps für SharePoint 2013](https://technet.microsoft.com/library/fp161232.aspx) und Veröffentlichen von Apps für [SharePoint](https://msdn.microsoft.com/library/jj164070.aspx)
  
> [!NOTE]
> Das Hinzufügen einer App zu einem SharePoint erfordert SharePoint Administratorberechtigungen. 
  
### <a name="procedure-5-to-deploy-the-quickstatus-app"></a>Prozedur 5. So stellen Sie die QuickStatus-App zur Bereitstellung

1. Speichern Visual Studio Alle Dateien, und klicken Sie dann im Projektmappen-Explorer  mit der rechten Maustaste auf das **Projekt QuickStatus,** und wählen Sie **Veröffentlichen aus.**
    
2. Da die **QuickStatus-App** SharePoint gehostet wird, gibt es nur sehr wenige Optionen für die Veröffentlichung (siehe Abbildung 8). Wählen Sie **im Dialogfeld Apps für Office und SharePoint** veröffentlichen die Option Fertig stellen **aus.**
    
   **Abbildung 8. Veröffentlichen der QuickStatus-App**

   ![Verwenden des Assistenten zum Veröffentlichen](media/pj15_CreateStatusingApp_PublishWizard.gif "Verwenden des Assistenten zum Veröffentlichen")
  
3. Kopieren Sie QuickStatus.app Datei aus dem Verzeichnis in ein bequemes Verzeichnis auf dem lokalen Computer (oder auf den SharePoint für eine lokale `~\QuickStatus\bin\Debug\app.publish\1.0.0.0` Installation). 
    
4. Wählen SharePoint In der Zentraladministration **apps** in der Schnellstart-Option aus, und wählen Sie **dann App-Katalog verwalten aus.**
    
5. Wenn kein App-Katalog vorhanden ist, erstellen Sie eine Websitesammlung für den App-Katalog, indem Sie den Abschnitt Konfigurieren der *App-Katalogwebsite* für eine Webanwendung unter Verwalten des App-Katalogs [in SharePoint 2013](https://technet.microsoft.com/library/fp161234.aspx)folgen.
    
   Wenn ein App-Katalog vorhanden ist, navigieren Sie zur Website-URL auf der Seite App-Katalog verwalten. In den folgenden Schritten ist beispielsweise die Website für den App-Katalog  `https://ServerName/sites/TestApps` .
    
6. Wählen Sie auf der Seite App-Katalog die Option **Apps for SharePoint** in der Schnellstartseite aus. Wählen Sie auf der Seite Apps SharePoint auf der Registerkarte **DATEIEN** des Menübands die Option **Hochladen Dokument aus.**
    
7. Suchen Sie **im** Dialogfeld Dokument hinzufügen nach der QuickStatus.app, fügen Sie Kommentare für die Version hinzu, und wählen Sie dann **OK aus.**
    
8. Wenn Sie eine App hinzufügen, können Sie auch lokale Informationen für die App-Beschreibung, das Symbol und andere Informationen hinzufügen. Fügen Sie **im Dialogfeld Apps for SharePoint - QuickStatus.app** die Informationen hinzu, die Sie für die App in der SharePoint anzeigen möchten. Fügen Sie beispielsweise die folgenden Informationen hinzu: 
    
   1. **Feld Kurze Beschreibung:** Geben Sie Schnellstatus-Test-App ein.
    
   2. **Beschreibungsfeld:** Geben Sie Test app to update percent complete for tasks in multiple projects ein.
    
   3. **Symbol-URL-Felder:** Fügen Sie den Websiteressourcen für den App-Katalog ein 96 x 96-Pixel-Bild für das App-Symbol hinzu. Navigieren Sie beispielsweise zu , wählen Sie im Dropdownmenü Einstellungen Websiteinhalte aus, wählen Sie `https://ServerName/sites/TestApps` **Websiteressourcen**  aus, und fügen Sie dann das quickStatusApp.png hinzu.  Klicken Sie mit der rechten Maustaste auf das **quickStatusApp-Element,** wählen Sie **Eigenschaften** aus, und kopieren Sie dann den **Wert Address (URL)** im **Dialogfeld** Eigenschaften. Kopieren Sie beispielsweise , und fügen Sie den Wert dann in das  `https://ServerName/sites/TestApps/SiteAssets/QuickStatusApp.png` Feld **Symbol-URL-Webadresse** ein. Geben Sie eine Beschreibung für das Symbol ein, z. B. (wie in Abbildung 9), geben Sie QuickStatus-App-Symbol ein. Testen Sie, ob die URL gültig ist.
    
      **Abbildung 9. Hinzufügen einer Symbol-URL für die QuickStatus-App**

      ![Festlegen von Eigenschaften für die App in SharePoint](media/pj15_CreateStatusingApp_AddAppToSharePointSettings.gif "Festlegen von Eigenschaften für die App in SharePoint")
  
   4. **Kategoriefeld:** Wählen Sie eine vorhandene Kategorie aus, oder geben Sie Einen eigenen Wert an. Geben Sie beispielsweise Statusing ein.
    
      > [!NOTE]
      > Eine Kategorie namens **Statusing** dient nur zu Testzwecken. Eine typische Kategorie für Project Server-Apps ist **Project Management**. 
  
   5. **Publisher:** Geben Sie den Namen des Herausgebers ein. Geben Sie in diesem Beispiel Project SDK ein.
    
   6. **Feld Aktiviert:** Aktivieren Sie das Kontrollkästchen Aktiviert, um die App für Project für die Installation sichtbar **zu** machen. 
    
   7. Zusätzliche Felder sind optional. Sie können beispielsweise eine Support-URL und mehrere Hilfebilder für die Seite "App-Details" hinzufügen. In Abbildung 9 enthalten die Felder **Bild-URL 1** die URL für einen Screenshot der App und eine Beschreibung des Screenshots. 
    
   8. Wählen Sie **im SharePoint - QuickStatus.app** Dialogfeld Speichern **aus.** In Abbildung 9 wird das Element Quick **Status Update** in der Bibliothek Apps für SharePoint zur Bearbeitung ausgecheckt.  Auf der Registerkarte **BEARBEITEN** des Dialogfeldbands würden Sie also Einchecken auswählen, um den Vorgang zu vervollständigen (siehe Abbildung 10). 
    
      **Abbildung 10. Die QuickStatus-App wird der Bibliothek Apps for SharePoint hinzugefügt.**

      ![Die QuickStatus-App wird SharePoint hinzugefügt](media/pj15_CreateStatusingApp_AddAppToSharePoint.gif "Die QuickStatus-App wird SharePoint hinzugefügt")
  
9. Wählen Project Web App im Dropdownmenü **Einstellungen** Hinzufügen **einer App aus.** Wählen Sie auf der Seite Ihre Apps auf der Schnellstartleiste **Aus Ihrer** Organisation aus, und wählen Sie dann **App-Details** für die **App Für schnelles Statusupdate** aus. Abbildung 11 zeigt die Detailseite mit dem App-Symbol, dem Screenshot und anderen Informationen, die Sie im vorherigen Schritt hinzugefügt haben. 
    
   **Abbildung 11. Verwenden der Detailseite "Quick Status Update" in Project Web App**

   ![Hinzufügen der QuickStatus-App zu Project Web App](media/pj15_CreateStatusingApp_AddAppToPWA.gif "Hinzufügen der QuickStatus-App zu Project Web App")
  
10. Wählen Sie auf der Seite Quick Status Update Details die Option **ADD IT aus.** Project Web App zeigt ein Dialogfeld an, in dem die Vorgänge aufgeführt sind, die die QuickStatus-App ausführen kann (siehe Abbildung 12). Die Liste der Vorgänge wird von den **AppPermissionRequest-Elementen** in der AppManifest.xml abgeleitet. 
    
    **Abbildung 12. Überprüfen, ob Sie der Schnellstatus-App vertrauen**

    ![Überprüfen des Vertrauens gegenüber der QuickStatus-App](media/pj15_CreateStatusingApp_AddAppToPWA2Trust.gif "Überprüfen des Vertrauens gegenüber der QuickStatus-App")
  
11. Wählen Sie **im Dialogfeld Schnellstatusaktualisierung** vertrauen die Option **Vertrauen aus.** Die App wird der Seite Project Web App-Websiteinhalte hinzugefügt (siehe Abbildung 13).
    
    **Abbildung 13. Anzeigen der Schnellstatus-App auf der Seite Websiteinhalte**

    ![Anzeigen der QuickStatus-App in den Websiteinhalten](media/pj15_CreateStatusingApp_AddAppToPWA3.gif "Anzeigen der QuickStatus-App in den Websiteinhalten")
  
Auf der Seite Websiteinhalte können Sie das Symbol Für **schnelles Statusupdate** auswählen, um die App ausführen zu können.

> [!NOTE]
> Für zusätzliche Befehle, die Informationen zur App bereitstellen, wählen Sie  auf der Seite Websiteinhalte den Bereich aus, der den Namen des Schnellstatusupdates und die Auslassungspunkte (...) enthält. Sie können die Seite Informationen für die App überprüfen, die Seite App-Details anzeigen, die Informationen zu App-Fehlern enthält, die Seite app-Berechtigungen überprüfen oder die App aus Project Web App entfernen. 
  
Auf der Seite Aufgaben in Project Web App (siehe Abbildung 14) sollte die Schaltfläche **QuickStatus** im Menüband aktiviert sein. Wenn die **Schaltfläche Schnellstatus** deaktiviert ist, führen Sie die in der Anmerkung für Abbildung 7 beschriebenen Aktionen aus. 

**Abbildung 14. Starten der QuickStatus-App über die Registerkarte TASKS**

![Starten der QuickStatus-App von der Registerkarte "TASKS"](media/pj15_CreateStatusingApp_TasksRibbon.gif "Starten der QuickStatus-App von der Registerkarte &quot;TASKS&quot;")
  
In Prozedur 6 werden einige Tests gezeigt, die mit der QuickStatus-App durchgeführt werden sollen.

<a name="pj15_StatusingApp_Testing"> </a>

## <a name="testing-the-quickstatus-app"></a>Testen der QuickStatus-App

Jeder Vorgang, den ein Benutzer in der **QuickStatus-App** ausprobieren kann, sollte auf einer Testinstallation von Project Server getestet werden, bevor die App auf einem Produktionsserver oder in einem Produktions mandanten von Project Online. Mit einer Testinstallation können Sie Zuordnungen für Benutzer ändern und löschen, ohne dass sich dies auf die tatsächlichen Projekte ausdingt. Tests sollten auch mehrere Benutzer mit unterschiedlichen Berechtigungssätzen umfassen, z. B. Administrator, Projektmanager und Teammitglied. Bei gründlichen Tests können Änderungen aufgedeckt werden, die in der App vorgenommen werden sollten, die bei Tests während der Entwicklung nicht offensichtlich waren. Prozedur 6 listet mehrere Tests für die **QuickStatus-App** auf, enthält jedoch keine umfassende Reihe von Tests. 
  
### <a name="procedure-6-to-test-the-quickstatus-app"></a>Verfahren 6. So testen Sie die QuickStatus-App

1. Führen Sie **die QuickStatus-App** aus, in der der Benutzer keine Zuweisungen hat. Die App sollte am unteren Rand der Seite eine blaue Meldung anzeigen, z. B. Benutzername **hat keine Zuweisungen**.
    
   Wählen **Sie Aktualisieren** aus, und die Nachrichtenänderungen zu grünen **Zuordnungen wurden aktualisiert.**
    
   > [!NOTE]
   > Das Verhalten der App sollte so geändert werden, dass die Schaltfläche **Aktualisieren** deaktiviert ist, wenn keine Zuweisungen verfügbar sind. 
  
2. Führen Sie die App aus, in der der Benutzer mehrere Zuordnungen in verschiedenen Projekten hat und einige Zuordnungen nicht abgeschlossen sind. Beachten Sie die Darstellung der App, und führen Sie aktionen wie folgt aus (siehe Abbildung 15):
    
   1. Die **onGetAssignmentsSuccess-Funktion** erstellt eine Zeile in der Tabelle für jede Zuordnung für den aktuellen Benutzer. Der Projektname wird nur einmal in fett formatierter Schriftart für die erste Zuordnung in jedem Projekt angezeigt. 
    
   2. Aktivieren Sie das  Kontrollkästchen in der Spaltenüberschrift Vorgangsname. Der Ereignishandler für den Tabellenkopfklicken gibt alle anderen Kontrollkästchen in den Vorgangszeilen frei. 
    
   3. Wählen Sie alle Vorgänge aus. Der Click-Ereignishandler für jede Zeile bestimmt, ob alle Zeilen ausgewählt sind, und wählt in diesem Fall die Spaltenüberschrift **Vorgangsname** aus. 
    
   4. Löschen Sie alle Kontrollkästchen erneut, und wählen Sie dann eine Zuordnung mit verbleibender Arbeit aus. In Abbildung 15 wird beispielsweise gezeigt, dass für die oberste Aufgabe T1 20 % verbleibende Arbeit übrig bleibt.
    
   5. Geben Sie **im Textfeld Prozent vollständig** festlegen 80 ein, und wählen Sie dann Aktualisieren **aus.** Unten auf der Seite sollte eine grüne Meldung angezeigt werden, **Zuordnungen wurden aktualisiert.**
    
      **Abbildung 15. Aktualisieren einer Zuordnung in der QuickStatus-App**

      ![Aktualisieren einer Zuweisung in der QuickStatus-App](media/pj15_CreateStatusingApp_Testing1Update.gif "Aktualisieren einer Zuweisung in der QuickStatus-App")
  
3. Wählen **Sie Aktualisieren** aus (siehe Abbildung 16). Alle Aufgaben werden erneut ausgewählt, und die oberste Aufgabe zeigt 80 % abgeschlossen an. 
    
      **Abbildung 16. Aktualisieren der Seite "Quick Status Update"**

      ![Aktualisieren der QuickStatus-Seite](media/pj15_CreateStatusingApp_Testing2Refresh.gif "Aktualisieren der QuickStatus-Seite")
  
4. Löschen Sie alle Kontrollkästchen, und wählen Sie dann einen anderen Vorgang aus. Wählen Sie z. B. **Neue Aufgabe aus PWA**. Lassen Sie das Textfeld Prozent **vollständig festlegen** leer, löschen Sie den gesamten Text in der Spalte **% abgeschlossen** für die ausgewählte Aufgabe, und wählen Sie dann **Aktualisieren aus.** Da beide Textfelder leer sind, zeigt die App eine rote Fehlermeldung an (siehe Abbildung 17).
    
      **Abbildung 17. Testen der Fehlermeldung**

      ![Testen der Fehlermeldung](media/pj15_CreateStatusingApp_Testing3Error.gif "Testen der Fehlermeldung")
  
5. Aktualisieren Sie den vorherigen Vorgang auf 80 % abgeschlossen, und wählen Sie dann **Beenden aus.** Die **exitToPwa-Funktion** ändert den Speicherort des Browserfensters in die Seite Aufgaben in der SharePoint Hostanwendung (d. h., die URL wird in https://ServerName/pwa/Tasks.aspx) geändert. Abbildung 18 zeigt, dass der **T1-Vorgang** und der neue Vorgang aus **PWA** jeweils 80 % abgeschlossen sind. 
    
      **Abbildung 18. Überprüfen der Aktualisierung der Aufgaben in Project Web App**

      ![Überprüfen der aktualisierten Aufgaben in Project Web App](media/pj15_CreateStatusingApp_TasksUpdatedInPWA.gif "Überprüfen der aktualisierten Aufgaben in Project Web App")
  
6. Bevor der aktualisierte Status in Project Professional 2013 angezeigt wird, müssen die Änderungen zur Genehmigung übermittelt und dann vom Projektmanager genehmigt werden.
    
Tests zeigen verschiedene andere Änderungen an, die in der **QuickStatus-App** vorgenommen werden sollten, um die Benutzerfreundlichkeit zu verbessern. Beispiel:

- Es sollten zusätzliche Fehlerüberprüfungen und Überprüfungen von Textfeldwerten durchgeführt werden. Derzeit kann ein Benutzer einen nicht numerischen oder einen negativen Wert für abgeschlossenen Prozentwert eingeben, was zu einer unfreundlichen Fehlermeldung führt. Bei einem negativen Wert lautet die Fehlermeldung beispielsweise Fehleraktualisierungszuweisungen: **PJClientCallableException: StatusingSetDataValueInvalid**.
    
- Die Fehlermeldung für leere Textfelder könnte das Projekt und den Vorgang zusätzlich zur Zeilennummer auflisten.
    
- Die Erfolgsmeldung könnte eine Liste der aktualisierten Aufgaben enthalten. oder wenn die **updateAssignments-Funktion** erfolgreich ist, kann sie eine automatische Seitenaktualisierung durchführen und aktualisierte Aufgaben oder Prozentsätze in einer anderen Farbe und fett formatierten Schriftart anzeigen. 
    
- Um eine sehr große Tabelle zu vermeiden, sollte die Zuordnungstabelle auf Vorgänge beschränkt sein, die weniger als 100 % abgeschlossen sind. Oder fügen Sie eine Option zum Anzeigen aller Vorgänge hinzu. Dieses Problem kann auch mithilfe eines jQuery-basierten Rasters anstelle einer Tabelle gelöst werden, in der Sie problemlos Filterung und Rasterauslagerung implementieren können.
    
- Da  die **QuickStatus-App** den Status nicht übermittelt, wäre das Symbol **Schnellstatus** auf der  Registerkarte AUFGABEN des Menübands logischer das erste Symbol in der Gruppe Aufgaben und nicht das letzte Symbol in der Gruppe Absenden.  
    
- Da die **onGetAssignmentsSuccess-Funktion** den **BtnSubmitUpdate-Schaltflächentext** initialisiert, die anderen Textwerte der Schaltflächen jedoch in HTML initialisiert werden, bleibt die Seite während der Ausgeführten der **getAssignments-Funktion** in einem teilweise initialisierten Zustand. Schaltflächen auf der Seite würden konsistenter angezeigt, wenn alle Textwerte in HTML initialisiert würden. 
    
Am wichtigsten ist, dass der von der **QuickStatus-App** verwendete Ansatz, bei dem die Prozent für Zuordnungen vollständig geändert wird, in einer Produktions-App überarbeitet werden sollte. Weitere Informationen finden Sie im [Abschnitt Nächste](#pj15_StatusingApp_NextSteps) Schritte. 

<a name="pj15_StatusingApp_Example"> </a>

## <a name="example-code-for-the-quickstatus-app"></a>Beispielcode für die QuickStatus-App

### <a name="defaultaspx-file"></a>Datei "Default.aspx"

Der folgende Code befindet sich in `Pages\Default.aspx` der Datei des **QuickStatus-Projekts:** 
  
```HTML
    <%-- The following lines are ASP.NET directives needed when using SharePoint components --%>
    <%@ Page Inherits="Microsoft.SharePoint.WebPartPages.WebPartPage, Microsoft.SharePoint, Version=15.0.0.0, 
    Culture=neutral, PublicKeyToken=71e9bce111e9429c" MasterPageFile="~masterurl/default.master" Language="C#" %>
    <%@ Register TagPrefix="Utilities" Namespace="Microsoft.SharePoint.Utilities" Assembly="Microsoft.SharePoint, Version=15.0.0.0, 
    Culture=neutral, PublicKeyToken=71e9bce111e9429c" %>
    <%@ Register TagPrefix="WebPartPages" Namespace="Microsoft.SharePoint.WebPartPages" Assembly="Microsoft.SharePoint, Version=15.0.0.0, 
    Culture=neutral, PublicKeyToken=71e9bce111e9429c" %>
    <%@ Register TagPrefix="SharePoint" Namespace="Microsoft.SharePoint.WebControls" Assembly="Microsoft.SharePoint, Version=15.0.0.0, 
    Culture=neutral, PublicKeyToken=71e9bce111e9429c" %>
    <%-- The markup and script in the following Content element will be placed in the <head> of the page.
        For production deployment, change the .debug.js JavaScript references to .js. --%>
    <asp:Content ContentPlaceHolderID="PlaceHolderAdditionalPageHead" runat="server">
    <script type="text/javascript" src="../Scripts/jquery-1.7.1.min.js"></script>
    <script type="text/javascript" src="/_layouts/15/sp.runtime.debug.js"></script>
    <script type="text/javascript" src="/_layouts/15/sp.debug.js"></script>
    <script type="text/javascript" src="/_layouts/15/ps.debug.js"></script>
    <!-- CSS styles -->
    <link rel="Stylesheet" type="text/css" href="../Content/App.css" />
    <!-- Add your JavaScript to the following file -->
    <script type="text/javascript" src="../Scripts/App.js"></script>
    </asp:Content>
    <%-- The markup and script in the following Content element will be placed in the <body> of the page --%>
    <asp:Content ContentPlaceHolderID="PlaceHolderMain" runat="server">
    <form>
        <fieldset>
        <legend>Select assigned tasks</legend>
        <table id="assignmentsTable">
            <caption id="tableCaption">Replace caption</caption>
            <thead>
            <tr id="headerRow">
                <th>Project name</th>
                <th><input type="checkbox" id="headercheckbox" checked="checked" />Task name</th>
                <th>Actual work</th>
                <th>% complete</th>
                <th>Remaining work</th>
                <th>Due date</th>
            </tr>
            </thead>
        </table>
        </fieldset>
        <div id="inputPercentComplete" >
        Set percent complete for all selected assignments, or leave this
        <br /> field blank and set percent complete for individual assignments: 
        <input type="text" name="percentComplete" id="pctComplete" size="4"  maxlength="4" />
        </div>
        <div id="submitResult">
        <p><button id="btnSubmitUpdate" type="button" class="bottomButtons" ></button></p>
        <p id="message"></p>
        </div>
        <div id="refreshPage">
        <p><button id="btnRefresh" type="button" class="bottomButtons" >Refresh</button></p>
        </div>
    <div id="exitPage">
        <p><button id="btnExit" type="button" class="bottomButtons" >Exit</button></p>
    </div>
    </form>
    </asp:Content>
```

<br/>

### <a name="appjs-file"></a>App.js-Datei

Der folgende Code befindet sich in `Scripts\App.js` der Datei des **QuickStatus-Projekts:** 
  
```js
    var projContext;
    var pwaWeb;
    var projUser;
    // This code runs when the DOM is ready and creates a ProjectContext object.
    // The ProjectContext object is required to use the JSOM for Project Server.
    $(document).ready(function () {
        projContext = PS.ProjectContext.get_current();
        pwaWeb = projContext.get_web();
        getUserInfo();
        getAssignments();
        // Bind a click event handler to the table header check box, which sets the row check boxes
        // to the selected state of the header check box, and sets the results message to an empty string.
        $('#headercheckbox').live('click', function (event) {
            $('input:checkbox:not(#headercheckbox)').attr('checked', this.checked);
            $get("message").innerText = "";
        });
        // Bind a click event handler to the row check boxes. If any row check box is cleared, clear
        // the header check box. If all of the row check boxes are selected, select the header check box.
        $('input:checkbox:not(#headercheckbox)').live('click', function (event) {
            var isChecked = true;
            $('input:checkbox:not(#headercheckbox)').each(function () {
                if (this.checked == false) isChecked = false;
                $get("message").innerText = "";
            });
            $("#headercheckbox").attr('checked', isChecked);
        });
    });
    // Get information about the current user.
    function getUserInfo() {
        projUser = pwaWeb.get_currentUser();
        projContext.load(projUser);
        projContext.executeQueryAsync(onGetUserNameSuccess,
            // Anonymous function to execute if getUserInfo fails.
            function (sender, args) {
                alert('Failed to get user name. Error: ' + args.get_message());
        });
    }
    // This function is executed if the getUserInfo call is successful.
    // Replace the contents of the 'caption' paragraph with the project user name.
    function onGetUserNameSuccess() {
        var prefaceInfo = 'Assignments for ' + projUser.get_title();
        $('#tableCaption').text(prefaceInfo);
    }
    // Get the collection of assignments for the current user.
    function getAssignments() {
        assignments = PS.EnterpriseResource.getSelf(projContext).get_assignments();
        // Register the request that you want to run on the server. The optional "Include" parameter 
        // requests only the specified properties for each assignment in the collection.
        projContext.load(assignments,
            'Include(Project, Name, ActualWork, ActualWorkMilliseconds, PercentComplete, RemainingWork, Finish, Task)');
        // Run the request on the server.
        projContext.executeQueryAsync(onGetAssignmentsSuccess,
            // Anonymous function to execute if getAssignments fails.
            function (sender, args) {
                alert('Failed to get assignments. Error: ' + args.get_message());
            });
    }
    // Get the enumerator, iterate through the assignment collection, 
    // and add each assignment to the table.
    function onGetAssignmentsSuccess(sender, args) {
        if (assignments.get_count() > 0) {
            var assignmentsEnumerator = assignments.getEnumerator();
            var projName = "";
            var prevProjName = "3D2A8045-4920-4B31-B3E7-9D0C5195FC70"; // Any unique name.
            var taskNum = 0;
            var chkTask = "";
            var txtPctComplete = "";
            // Constants for creating input controls in the table.
            var INPUTCHK = '<input type="checkbox" class="chkTask" checked="checked" id="chk';
            var LBLCHK = '<label for="chk';
            var INPUTTXT = '<input type="text" size="4"  maxlength="4" class="txtPctComplete" id="txt';
            while (assignmentsEnumerator.moveNext()) {
                var statusAssignment = assignmentsEnumerator.get_current();
                projName = statusAssignment.get_project().get_name();
                // Get an integer value for the number of milliseconds of actual work, such as 3600000.
                var actualWorkMilliseconds = statusAssignment.get_actualWorkMilliseconds();
                // Get a string value for the assignment actual work, such as "1h". Not used here.
                var actualWork = statusAssignment.get_actualWork();                         
                if (projName === prevProjName) {
                    projName = "";
                }
                prevProjName = statusAssignment.get_project().get_name();
                // Create a row for the assignment information.
                var row = assignmentsTable.insertRow();
                taskNum++;
                // Create an HTML string with a check box and task name label, for example:
                //     <input type="checkbox" class="chkTask" checked="checked" id="chk1" /> 
                //     <label for="chk1">Task 1</label>
                chkTask = INPUTCHK + taskNum + '" /> ' + LBLCHK + taskNum + '">'
                    + statusAssignment.get_name() + '</label>';
                txtPctComplete = INPUTTXT + taskNum + '" />';
                // Insert cells for the assignment properties.
                row.insertCell().innerHTML = '<strong>' + projName + '</strong>';
                row.insertCell().innerHTML = chkTask;
                row.insertCell().innerText = actualWorkMilliseconds / 3600000 + 'h';
                row.insertCell().innerHTML = txtPctComplete;
                row.insertCell().innerText = statusAssignment.get_remainingWork();
                row.insertCell().innerText = statusAssignment.get_finish();
                // Initialize the percent complete cell.
                $get("txt" + taskNum).innerText = statusAssignment.get_percentComplete() + '%'
            }
        }
        else {
            $('p#message').attr('style', 'color: #0f3fdb');     // Blue text.
            $get("message").innerText = projUser.get_title() + ' has no assignments'
        }
        // Initialize the button properties.
        $get("btnSubmitUpdate").onclick = function() { updateAssignments(); };
        $get("btnSubmitUpdate").innerText = 'Update';
        $get('btnRefresh').onclick = function () { window.location.reload(true); };
        $get('btnExit').onclick = function () { exitToPwa(); };
    }
    // Update all selected assignments. If the bottom percent complete field is blank,
    // use the value in the % complete field of each selected row in the table.
    function updateAssignments() {
        // Get percent complete from the bottom text box.
        var pctCompleteMain = getNumericValue($('#pctComplete').val()).trim();
        var pctComplete = pctCompleteMain;
        var assignmentsEnumerator = assignments.getEnumerator();
        var taskNum = 0;
        var taskRow = "";
        var indexPercent = "";
        var doSubmit = true;
        while (assignmentsEnumerator.moveNext()) {
            var pctCompleteRow = "";
            taskRow = "chk" + ++taskNum;
            if ($get(taskRow).checked) {
                var statusAssignment = assignmentsEnumerator.get_current();
                if (pctCompleteMain === "") {
                    // Get percent complete from the text box field in the table row.
                    pctCompleteRow = getNumericValue($('#txt' + taskNum).val());
                    pctComplete = pctCompleteRow;
                }
                // If both percent complete fields are empty, show an error.
                if (pctCompleteMain === "" && pctCompleteRow === "") {
                    $('p#message').attr('style', 'color: #e11500');     // Red text.
                    $get("message").innerHTML =
                        '<b>Error:</b> Both <i>Percent complete</i> fields are empty, in row '
                        + taskNum
                        + ' and in the bottom textbox.<br/>One of those fields must have a valid percent.'
                        + '<p>Please refresh the page and try again.</p>';
                    doSubmit = false;
                    taskNum = 0;
                    break;
                }
                if (doSubmit) statusAssignment.set_percentComplete(pctComplete);
            }
        } 
        // Save and submit the assignment updates.
        if (doSubmit) {
            assignments.update();
            assignments.submitAllStatusUpdates();
            projContext.executeQueryAsync(function (source, args) {
                $('p#message').attr('style', 'color: #0faa0d');     // Green text.
                $get("message").innerText = 'Assignments have been updated.';
            }, function (source, args) {
                $('p#message').attr('style', 'color: #e11500');     // Red text.
                $get("message").innerText = 'Error updating assignments: ' + args.get_message();
            });
        }
    }
    // Get the numeric part for percent complete, from a string. 
    // For example, with "20 %", return "20".
    function getNumericValue(pctComplete) {
        pctComplete = pctComplete.trim();
        pctComplete = pctComplete.replace(/ /g, "");    // Remove interior spaces.
        indexPercent = pctComplete.indexOf('%', 0);
        if (indexPercent > -1) pctComplete = pctComplete.substring(0, indexPercent);
        return pctComplete;
    }
    // Exit the QuickStatus page and go back to the Tasks page in Project Web App.
    function exitToPwa() {
        // Get the SharePoint host URL, which is the top page of PWA, and add the Tasks page.
        var spHostUrl = decodeURIComponent(getQueryStringParameter('SPHostUrl'))
                        + "/Tasks.aspx";
        // Set the top window for the QuickStatus IFrame to the Tasks page.
        window.top.location.href = spHostUrl;
    }
    // Get a specified query string parameter from the {StandardTokens} URL option string.
    function getQueryStringParameter(urlParameterKey) {
        var docUrl = document.URL;
        var params = docUrl.split('?')[1].split('&');
        for (var i = 0; i < params.length; i++) {
            var theParam = params[i].split('=');
            if (theParam[0] == urlParameterKey)
                return decodeURIComponent(theParam[1]);
        }
    }
```

<br/>

### <a name="appcss-file"></a>App.css-Datei

Der folgende CSS-Code befindet sich in `Content\App.css` der Datei des **QuickStatus-Projekts:** 
  
```css
    /* Custom styles for the QuickStatus app. */
    /*============= Table elements ========================================*/
    table {
        width: 90%;
    }
    caption {
        font-size: 16px;
        padding-bottom: 5px;
        font-weight: bold;
        color: gray;
    }
    table th {
        background-color: gray;
        color: white;
    }
    table td, th {
        width: auto;
        text-align: left;
        padding: 2px;
        border: solid 1px whitesmoke;
        color: gray;
    }
    /*=== Class for check boxes added to rows 
    */
    .chkTask {
        width: 12px;
        height: 12px;
        color: gray;
    }
    /*========== DIV id for the Percent Complete text box ================*/
    #inputPercentComplete {
        position: fixed;
        top: auto;
        height: auto;
        padding-top: 20px;
        margin-left: 30px;
    }
    /*========== DIV id for the Submit Result button ====================*/
    #submitResult {
        position: fixed;
        top: auto;
        height: auto;
        padding-top: 60px;
    }
    /*========== DIV id for the Refresh Page button ====================*/
    #refreshPage {
        position: fixed;
        top: auto;
        height: auto;
        padding-top: 60px;
        margin-left: 120px;
    }
    /*========== DIV id for the Exit Page button ====================*/
    #exitPage {
        position: fixed;
        top: auto;
        height: auto;
        padding-top: 60px;
        margin-left: 240px;
    }
    /*========== Class for the buttons at the bottom of the page =======*/
    .bottomButtons {
        color: gray;
        font-weight: bold; 
        font-size: 12px; 
        border-color: darkgreen;
        border-width: thin;
    }
```

<br/>

### <a name="elementsxml-file-for-the-ribbon"></a>Elements.xml für das Menüband

Die folgende XML-Definition für die hinzugefügte Schaltfläche auf der Registerkarte **TASKS** im Menüband befindet sich in der Datei `RibbonQuickStatusAction\Elements.xml` des **QuickStatus-Projekts:** 
  
```XML
    <?xml version="1.0" encoding="utf-8"?>
    <Elements xmlns="http://schemas.microsoft.com/sharepoint/">
    <CustomAction Id="21ea3aaf-79e5-4aac-9479-8eef14b4d9df.RibbonQuickStatusAction"
                    Location="CommandUI.Ribbon">
        <CommandUIExtension>
        <!-- 
        Add a button that invokes the QuickStatus app. The Quick Status button is displayed as  
        the third control in the Page group (the group title is "Submit").
        -->
        <CommandUIDefinitions>
            <CommandUIDefinition Location="Ribbon.ContextualTabs.MyWork.Home.Page.Controls._children">
            <Button Id="Ribbon.ContextualTabs.MyWork.Home.Page.QuickStatus"
                    Alt="Quick Status app"
                    Sequence="30"
                    Command="Invokae_QuickStatus"
                    LabelText="Quick Status"
                    TemplateAlias="o1"
                    Image16by16="_layouts/15/1033/images/ps16x16.png" 
                    Image16by16Left="-80"
                    Image16by16Top="-144"
                    Image32by32="_layouts/15/1033/images/ps32x32.png" 
                    Image32by32Left="-32"
                    Image32by32Top="-288" 
                    ToolTipTitle="Quick Status"
                    ToolTipDescription="Run the QuickStatus app" />
            </CommandUIDefinition>
        </CommandUIDefinitions>
        <CommandUIHandlers>
            <CommandUIHandler Command="Invoke_QuickStatus"
                            CommandAction="~appWebUrl/Pages/Default.aspx?{StandardTokens}"/>
        </CommandUIHandlers>
        </CommandUIExtension >
    </CustomAction>
    </Elements>
```

<br/>

### <a name="appmanifestxml-file"></a>Die Datei "AppManifest.xml"

Im Folgenden finden Sie die XML für das App-Manifest des **QuickStatus-Projekts,** das die beiden Berechtigungsanforderungsbereiche enthält, die zum Aktualisieren des Zuweisungsstatus des App-Benutzers in mehreren Projekten erforderlich sind: 
  
```XML
    <?xml version="1.0" encoding="utf-8" ?>
    <!--Created:cb85b80c-f585-40ff-8bfc-12ff4d0e34a9-->
    <App xmlns="http://schemas.microsoft.com/sharepoint/2012/app/manifest"
        Name="QuickStatus"
        ProductID="{bbc497e7-1221-4d7b-a0ae-141a99546008}"
        Version="1.0.0.0"
        SharePointMinVersion="15.0.0.0"
    >
    <Properties>
        <Title>Quick Status Update</Title>
        <StartPage>~appWebUrl/Pages/Default.aspx?{StandardTokens}</StartPage>
    </Properties>
    <AppPrincipal>
        <Internal />
    </AppPrincipal>
    <AppPermissionRequests>
        <AppPermissionRequest Scope="https://sharepoint/projectserver/statusing" Right="SubmitStatus" />
        <AppPermissionRequest Scope="https://sharepoint/projectserver/projects" Right="Read" />
    </AppPermissionRequests>
    </App>
```

<br/>

### <a name="appiconpng-file"></a>AppIcon.png-Datei

Die vollständige Visual Studio für die **QuickStatus-App** enthält eine benutzerdefinierte AppIcon.png Datei. Die Lösung wird im Download des Project 2013 SDK enthalten sein. 

<a name="pj15_StatusingApp_NextSteps"> </a>

## <a name="next-steps"></a>Nächste Schritte

Die **QuickStatus-App** ist ein relativ einfaches Beispiel für das Schreiben von Apps, die auf Project Server 2013 und Project Online. Im [Abschnitt Testen der QuickStatus-App](#pj15_StatusingApp_Testing) werden mehrere Verbesserungen aufgeführt, die für eine bessere Benutzerfreundlichkeit vorgenommen werden können. Die **QuickStatus-App** verwendet JavaScript-Funktionen, um den Zuweisungsstatus für Project Web App zu aktualisieren. Das Ändern des abgeschlossenen Zuordnungsprozentes ist jedoch keine empfohlene Projektverwaltungspraxis. Ein weiterer Ansatz wäre das Aktualisieren des tatsächlichen Startdatums und der verbleibenden Dauer der zugewiesenen Vorgänge. Eine Diskussion der Probleme finden Sie unter [Update Better](https://www.mpug.com/articles/update-better) im MPUG-Newsletter. 

<a name="pj15_StatusingApp_AdditionalResources"> </a>

## <a name="see-also"></a>Siehe auch

- [Project Serverprogrammierungsaufgaben](project-programming-tasks.md)
- [SharePoint-Add-Ins](https://msdn.microsoft.com/library/jj163230.aspx)
- [Verwalten von Vorgangsaktualisierungen in Project Web App](https://technet.microsoft.com/library/hh767481%28v=office.14%29.aspx)
- [Erstellen benutzerdefinierter Aktionen zur Bereitstellung mit SharePoint-Add-Ins](https://msdn.microsoft.com/library/jj163954.aspx)
    

