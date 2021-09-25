---
title: Erstellen eines auf SharePoint gehosteten Project Server-Add-Ins
manager: lindalu
ms.date: 08/10/2016
ms.audience: Developer
ms.localizationpriority: medium
ms.assetid: bb9c3c00-7121-41e1-9db3-75550d040ba8
description: Von den drei Arten von Apps, die Sie für Project Online erstellen können (automatisch gehostet, vom Anbieter gehostet und SharePoint gehostet), ist die SharePoint gehostete App am einfachsten zu erstellen und bereitzustellen.
ms.openlocfilehash: 2afa297fe61f026977277356b8ad63dbf86992ef
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59560270"
---
# <a name="create-a-sharepoint-hosted-project-server-add-in"></a>Erstellen eines auf SharePoint gehosteten Project Server-Add-Ins

Von den drei Arten von Apps, die Sie für Project Online erstellen können (automatisch gehostet, vom Anbieter gehostet und SharePoint gehostet), ist die SharePoint gehostete App am einfachsten zu erstellen und bereitzustellen. Eine SharePoint-gehostete App erfordert keine OAuth-Authentifizierung und verwendet weder Azure noch die Wartung einer lokalen Website für die vom Anbieter gehosteten Ressourcen. Die Vorlage **"App für SharePoint 2013"** in Visual Studio ist ein praktisches Framework für die Entwicklung von Apps, die im Office Store veröffentlicht und verkauft oder in einem privaten App-Katalog auf SharePoint bereitgestellt werden können. 
  
In Project ist Statuserfassung ein Prozess, bei dem ein Teammitglied die Seite "Aufgaben" in Project Web App verwenden kann, um den Status einer zugewiesenen Aufgabe zu übermitteln, z. B. die Anzahl der Arbeitsstunden pro Tag einer Woche, die an der Aufgabe gearbeitet wurde. Der Zuweisungsbesitzer (in der Regel der Projektmanager) kann den Status genehmigen oder ablehnen. Wenn der Status genehmigt wird, berechnet Project den Zeitplan neu. Die **QuickStatus-App** zeigt zugewiesene Aufgaben an, bei denen der Benutzer den Prozentsatz der abgeschlossenen Aufgaben schnell aktualisieren und den Status der ausgewählten Aufgaben zur Genehmigung übermitteln kann. Obwohl die Seite "Aufgaben" in Project Web App über viel mehr Funktionalität verfügt, ist die **QuickStatus-App** ein Beispiel, das eine vereinfachte Benutzeroberfläche bereitstellt. 
  
Die **QuickStatus-App** ist ein Beispiel für Entwickler. sie ist nicht für die Verwendung in einer Produktionsumgebung vorgesehen. Der Hauptzweck besteht darin, ein Beispiel für die App-Entwicklung für Project Online zu zeigen, nicht um eine voll funktionsfähige Statuserfassungs-App zu erstellen. Einen besseren Ansatz zur Statuserfassung finden Sie in der Empfehlung in den [nächsten Schritten.](#pj15_StatusingApp_NextSteps)
  
Allgemeine Informationen zum Status finden Sie unter [Vorgangsfortschritt.](https://support.office.com/article/Find-information-about-Project-Server-2013-8b08a414-15a7-4076-b2db-c90d0214ea7f?ui=en-US&rs=en-US&ad=US#BKMK_TaskProgress) Weitere Informationen zum Entwickeln von Add-Ins für SharePoint und Project Server finden Sie unter [SharePoint Add-Ins.](https://msdn.microsoft.com/library/jj163230.aspx)

<a name="pj15_StatusingApp_Prerequisites"> </a>

## <a name="prerequisites-for-creating-an-app-for-project-server-2013"></a>Voraussetzungen für die Erstellung einer App für Project Server 2013

Um relativ einfache Apps zu entwickeln, die für Project Online oder für eine lokale Installation von Project Server 2013 bereitgestellt werden können, können Sie die Napa verwenden, die eine Onlineentwicklungsumgebung bereitstellt. Für komplexere Apps, das Ändern des Project Web App-Menübands und das einfachere Debuggen während der Entwicklung können Sie Visual Studio 2012 oder Visual Studio 2013 verwenden. Bei einer lokalen Installation können Sie beispielsweise die Entwurfsdatentabellen manuell auf Änderungen in der Project Serverdatenbank überprüfen. In diesem Artikel erfahren Sie, wie Sie die App-Entwicklung mit Visual Studio durchführen.
  
Die Entwicklung von Project Server-Apps mit Visual Studio erfordert Folgendes:
  
- Stellen Sie sicher, dass Sie die neuesten Service Packs und Windows-Updates auf dem lokalen Entwicklungscomputer installiert haben. Als Betriebssystem kann Windows 7, Windows 8, Windows Server 2008 oder Windows Server 2012 verwendet werden.
    
- Sie müssen über einen Computer verfügen, auf dem SharePoint Server 2013 und Project Server 2013 installiert ist, auf dem der Computer für die App-Isolation und das Querladen von Apps konfiguriert ist. Durch das Querladen können Visual Studio die App vorübergehend zum Debuggen installieren. Sie können eine lokale Installation von SharePoint und Project Server verwenden. Weitere Informationen finden Sie unter [Einrichten einer lokalen Entwicklungsumgebung für Apps für SharePoint.](https://msdn.microsoft.com/library/fp179923%28Office.15%29.aspx)
    
   > [!NOTE]
   > Konfigurieren Sie für eine lokale Installation eine isolierte App-Domäne,  *bevor*  Sie einen Unternehmens-App-Katalog erstellen. 
  
- Der Entwicklungscomputer kann ein Remotecomputer sein, auf dem Office Developer Tools für Visual Studio 2012 installiert ist. Stellen Sie sicher, dass Sie die neueste Version installiert haben. weitere Informationen finden Sie im Abschnitt *"Extras"* der [Downloads für Apps für Office und SharePoint.](https://msdn.microsoft.com/office/apps/fp123627.aspx)
    
- Stellen Sie sicher, dass im Browser auf die Project Web App-Instanz zugegriffen werden kann, die Sie für Entwicklung und Tests verwenden werden.
    
Informationen zur Verwendung der Onlinetools finden Sie unter [Einrichten einer Umgebung zum Entwickeln von Apps für SharePoint auf Office 365.](https://msdn.microsoft.com/library/fp161179.aspx) Eine exemplarische Vorgehensweise zum Erstellen einer einfachen App für Project Server, die die Onlinetools verwendet, finden Sie in der EPMSource-Blogreihe ["Building your first Project Server app".](https://epmsource.com/2012/11/20/building-your-first-project-server-app-part-zerothe-introduction/)

<a name="pj15_StatusingApp_UsingVisualStudio"> </a>

## <a name="using-visual-studio-to-create-a-project-server-app"></a>Verwenden von Visual Studio zum Erstellen einer Project Server-App

Office Entwicklertools für Visual Studio 2012 enthalten eine Vorlage für SharePoint Apps, die mit Project Server 2013 verwendet werden können. Wenn Sie eine App-Lösung erstellen, enthält die Lösung die folgenden Dateien für Ihren benutzerdefinierten Code:
  
- **AppManifest.xml** enthält Einstellungen für den App-Titel, den Berechtigungsanforderungsbereich und andere Eigenschaften. Prozedur 1 enthält Schritte zum Festlegen der Eigenschaften mithilfe des Manifest-Designers. 
    
- **Default.aspx** im Ordner "Pages" ist die Hauptseite der App. In Prozedur 2 wird gezeigt, wie HTML5-Inhalte für die **QuickStatus-App** hinzugefügt werden. 
    
- **App.js** im Ordner "Skripts" ist die primäre Datei für den benutzerdefinierten JavaScript-Code. In Prozedur 3 wird der JavaScript-Code für die **QuickStatus-App** erläutert. 
    
   Wenn Sie kommerzielle Steuerelemente wie ein jQuery-basiertes Raster oder eine Datumsauswahl hinzufügen, können Sie Verweise auf zusätzliche JavaScript-Dateien in der Datei "Default.aspx" hinzufügen.
    
- **"App.css"** im Ordner "Inhalt" ist die primäre Datei für benutzerdefinierte CSS3-Formatvorlagen. Prozedur 2 und Prozedur 3 enthalten Informationen zu CSS-Formatvorlagen (Cascading Stylesheets) für die **QuickStatus-App.** Sie können Verweise auf zusätzliche CSS-Dateien in der Datei "Default.aspx" hinzufügen. 
    
- **AppIcon.png** im Ordner "Bilder" ist das 96 x 96-Symbol, das die App im Office Store oder im App-Katalog anzeigt. 
    
Zum Ändern des Project Web App-Menübands können Sie eine benutzerdefinierte Menübandaktion hinzufügen. Der [Beispielcode für den QuickStatus-App-Abschnitt](#pj15_StatusingApp_Example) enthält den vollständigen Code für die geänderten Dateien Default.aspx, App.js, App.css, Elements.xml und AppManifest.xml. 
  
### <a name="procedure-1-to-create-an-app-project-in-visual-studio"></a>Vorgehensweise 1: So erstellen Sie ein App-Projekt in Visual Studio

1. Führen Sie Visual Studio 2012 als Administrator aus, und wählen Sie dann neue **Project** auf der Startseite aus. 
    
2. Erweitern Sie im Dialogfeld **Neue Project** die Knoten **Vorlagen,** **Visual C#** und **Office/SharePoint,** und wählen Sie dann **Apps** aus. Verwenden Sie die **Standardeinstellung .NET Framework 4.5** in der Dropdownliste des Zielframeworks oben im mittleren Bereich, und wählen Sie dann **App für SharePoint 2013** aus (siehe Abbildung 1). 
    
3. Geben Sie im **Feld "Name"** quickStatus ein, navigieren Sie zu dem Speicherort, an dem Sie die App speichern möchten, und klicken Sie dann auf **"OK".**
    
   **Abbildung 1. Erstellen einer Project Server-App in Visual Studio**

   ![Erstellen einer Project Server-App in Visual Studio](media/pj15_CreateStatusingApp_NewProject.gif "Erstellen einer Project Server-App in Visual Studio")
  
4. Füllen Sie im Dialogfeld **"Neue App für SharePoint"** die folgenden drei Felder aus: 
    
   - Geben Sie im oberen Textfeld den Namen ein, den die App in Project Web App anzeigen soll. Geben Sie z. B. quick Status Update ein.
    
   - Geben Sie für die Website, die für das Debuggen verwendet werden soll, die URL der Project Web App-Instanz ein. Geben Sie z. B. `https://ServerName/ProjectServerName` ServerName und ProjectServerName durch Ihre eigenen Werte ein, und wählen Sie dann **Überprüfen** aus.   Wenn alles gut läuft, zeigt Visual Studio **eine erfolgreiche Verbindung** an. Wenn eine Fehlermeldung angezeigt wird, stellen Sie sicher, dass die Project Web App-URL korrekt ist und dass der Project Servercomputer für die App-Isolierung und das Querladen von Apps konfiguriert ist. Weitere Informationen finden Sie im Abschnitt "Voraussetzungen für das [Erstellen einer App für Project Server 2013".](#pj15_StatusingApp_Prerequisites) 
    
   - Wählen Sie in der Dropdownliste "Gew how **do you want to host your app for SharePoint"** SharePoint **gehosteten** aus.
    
   > [!CAUTION]
   > Wenn Sie versehentlich den standardmäßigen vom **Anbieter gehosteten** Projekttyp auswählen, erstellt Visual Studio zwei Projekte in der Projektmappe: ein **QuickStatus-Projekt** und ein **QuickStatusWeb-Projekt.** Wenn zwei Projekte angezeigt werden, löschen Sie diese Lösung, und starten Sie erneut. 
  
5. Wählen Sie **"OK"** aus, um die **QuickStatus-Lösung,** das **QuickStatus-Projekt** und die Standarddateien zu erstellen. 
    
6. Öffnen Sie die Manifest-Designer-Ansicht (doppelklicken Sie beispielsweise auf die datei AppManifest.xml). Auf der Registerkarte **"Allgemein"** sollte im Textfeld **"Titel"** der App-Name angezeigt werden, den Sie in Schritt 4 eingegeben haben. Wählen Sie die Registerkarte **"Berechtigungen",** um die folgenden Berechtigungsanforderungen für die App hinzuzufügen (siehe Abbildung 2): 
    
   - In the first row of the **Permission requests** list, in the **Scope** column, choose **Statusing** in the drop-down list. Klicken Sie in der Spalte **"Berechtigung"** auf **"SubmitStatus".**
    
   - Fügen Sie eine Zeile hinzu, in der der **Bereich** **mehrere Projekte** und die **Berechtigung** **lesegeschützt** ist.
    
   **Abbildung 2. Festlegen des Berechtigungsbereichs für eine Statuserfassungs-App**

   ![Festlegen des Berechtigungsumfangs für eine Statuserfassungs-App](media/pj15_CreateStatusingApp_PermissionScope.gif "Festlegen des Berechtigungsumfangs für eine Statuserfassungs-App")
  
Die **QuickStatus-App** ermöglicht es einem Project Web App-Benutzer, Zuordnungen für diesen Benutzer aus mehreren Projekten zu lesen, die Zuordnung in Prozent zu ändern und die Aktualisierung zu übermitteln. Die anderen Berechtigungsanforderungsbereiche in der Dropdownliste in Abbildung 2 sind für diese App nicht erforderlich. Die Berechtigungsanforderungsbereiche sind die Berechtigungen, die die App im Namen des Benutzers anfordert. Wenn der Benutzer nicht über diese Berechtigungen in Project Web App verfügt, wird die App nicht ausgeführt. Eine App kann mehrere Berechtigungsanforderungsbereiche haben, einschließlich der bereiche für andere SharePoint Berechtigungen, sollte jedoch nur das für die App-Funktionalität erforderliche Minimum aufweisen. Es folgen die Berechtigungsanforderungsbereiche, die sich auf Project Server beziehen: 

- **Enterprise Ressourcen:** Ressourcen-Manager-Berechtigungen zum Lesen oder Schreiben von Informationen zu anderen Project Web App-Benutzern.
    
- **Mehrere Projekte:** Lese- oder Schreibzugriff auf mehrere Projekte, bei denen der Benutzer über die angeforderten Berechtigungen verfügt.
    
- **Project Server:** Erfordert, dass der App-Benutzer über Administratorberechtigungen für Project Web App verfügt.
    
- **Reporting:** Read the **ProjectData** OData service for Project Web App (requires only log on permission for Project Web App). 
    
- **Einzelne Project:** Lese- oder Schreibzugriff auf ein Projekt, bei dem der Benutzer über die angeforderten Berechtigungen verfügt.
    
- **Statuserfassung:** Übermitteln von Updates für den Status von Zuordnungen, z. B. Arbeitszeiten, abgeschlossene Prozent und neue Zuordnungen.
    
- **Workflow:** Wenn der Benutzer über die Berechtigung zum Ausführen Project Serverworkflows verfügt, wird die App mit erhöhten Berechtigungen für den Workflow ausgeführt.
    
Weitere Informationen zu Berechtigungsanforderungsbereichen für Project Server 2013 finden Sie im Abschnitt *Project Apps* unter [Updates für Entwickler in Project 2013](updates-for-developers-in-project-2013.md) und [App-Berechtigungen in SharePoint 2013.](https://msdn.microsoft.com/library/fp142383.aspx)


<a name="pj15_StatusingApp_HTML"> </a>

### <a name="creating-the-html-content-for-the-quickstatus-app"></a>Erstellen des HTML-Inhalts für die QuickStatus-App

Bevor Sie mit dem Codieren des HTML-Inhalts beginnen, entwerfen Sie die Benutzeroberfläche und die Benutzeroberfläche für die QuickStatus-App (Abbildung 3 zeigt ein Beispiel für die abgeschlossene Seite). Ein Entwurf kann auch eine Gliederung der JavaScript-Funktionen enthalten, die mit dem HTML-Code interagieren. Allgemeine Informationen finden Sie [unter UX-Design für Apps in SharePoint 2013.](https://msdn.microsoft.com/library/fp179934.aspx)
  
**Abbildung 3. Entwurf der QuickStatus-App-Seite**

![Design der QuickStatus-App-Seite](media/pj15_CreateStatusingApp_AfterRefresh.gif "Design der QuickStatus-App-Seite")
  
Die App zeigt den Anzeigenamen oben an, d. h. den Wert des **Title-Elements** in AppManifest.xml. 
  
Standardmäßig verwendet die Seite HTML5. Es folgen die standardmäßigen HTML-Elemente für die hauptbenutzeroberflächenobjekte, die die **QuickStatus-App** im Textkörper der Seite enthält: 
  
- Ein **Formularelement** enthält alle anderen UI-Elemente. 
    
- Ein **Fieldset-Element** erstellt einen Container und Rahmen für das Zuordnungsverzeichnis. Das untergeordnete **Legendenelement** stellt eine Bezeichnung für den Container bereit. 
    
- Ein **Tabellenelement** enthält eine Beschriftung und nur eine Tabellenkopfzeile. JavaScript-Funktionen ändern die Tabellenbeschriftung und fügen Zeilen für die Zuweisungen hinzu. 
    
   > [!NOTE]
   > Zum einfachen Hinzufügen von Paging und Sortieren würde eine Produktions-App wahrscheinlich ein kommerzielles jQuery-basiertes Rastersteuerelement anstelle einer Tabelle verwenden. 
  
   Die Tabelle enthält Spalten für den Projektnamen, den Vorgangsnamen mit einem Kontrollkästchen, die aktuelle Arbeit, den Prozentsatz der abgeschlossenen Arbeit, die verbleibende Arbeit und den Endtermin der Zuordnung. JavaScript-Funktionen erstellen das Kontrollkästchen und das Texteingabefeld für den Prozentsatz der abgeschlossenen Aufgaben.
    
- Ein **Eingabeelement** für ein Textfeld legt den Prozentsatz der abgeschlossenen Arbeit für alle ausgewählten Zuordnungen fest. 
    
- Ein **Schaltflächenelement** sendet die Statusänderungen. 
    
- Ein **Schaltflächenelement** aktualisiert die Seite. 
    
- Ein **Schaltflächenelement** beendet die App und kehrt zur Seite "Aufgaben" in Project Web App zurück. 
    
Das untere Textfeld und  die Schaltflächenelemente befinden sich in div-Elementen, sodass CSS die Position und Darstellung der UI-Objekte problemlos verwalten kann. Eine JavaScript-Funktion fügt am unteren Rand der Seite einen Absatz hinzu, der Ergebnisse für Erfolg oder Fehler der Statusaktualisierung enthält. 
  
### <a name="procedure-2-to-create-the-html-content"></a>Vorgehensweise 2: So erstellen Sie den HTML-Inhalt

1. Öffnen Sie in Visual Studio die Datei "Default.aspx".
    
   Die Datei enthält zwei **asp:Content-Elemente:** Das Element mit dem  `ContentPlaceHolderID="PlaceHolderAdditionalPageHead"` Attribut wird innerhalb des Seitenheaders hinzugefügt, und das Element mit dem Attribut wird innerhalb des  `ContentPlaceHolderID="PlaceHolderMain"` **Seitentextelements** platziert. 
    
2. Fügen Sie im `<asp:Content ContentPlaceHolderID="PlaceHolderAdditionalPageHead" runat="server">` Steuerelement für die Kopfzeile der Seite einen Verweis auf die PS.js-Datei auf dem Project Servercomputer hinzu. Zum Testen und Debuggen können Sie PS.debug.js verwenden. 
    
   ```HTML
     <script type="text/javascript" src="/_layouts/15/ps.debug.js"></script>
   ```

   Die App-Infrastruktur verwendet das `/_layouts/15/` virtuelle Verzeichnis für die SharePoint-Website in IIS. Die physische Datei ist  `%ProgramFiles%\Common Files\Microsoft Shared\Web Server Extensions\15\TEMPLATE\LAYOUTS\PS.debug.js` .
    
   > [!NOTE]
   > Entfernen Sie vor der Bereitstellung der App für die Produktionsverwendung  `.debug` die Skriptverweise, um die Leistung zu verbessern. 
  
3. Löschen Sie im  `<asp:Content ContentPlaceHolderID="PlaceHolderMain" runat="server">` Steuerelement für den Seitentext das generierte **div-Element,** und fügen Sie dann den HTML-Code für die UI-Objekte hinzu. Das **Tabellenelement** enthält nur eine Kopfzeile. Die Spalte **"Vorgangsname"** enthält ein Kontrollkästchen-Eingabesteuerelement. Text für das **Caption-Element** wird durch den **onGetUserNameSuccess-Rückruf** für die **getUserInfo-Funktion** in der App.js-Datei ersetzt. 
    
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

4. Fügen Sie in der Datei "App.css" CSS-Code für die Position und Darstellung der UI-Elemente hinzu. Den vollständigen CSS-Code der **QuickStatus-App** finden Sie im [Beispielcode für den Abschnitt "QuickStatus-App".](#pj15_StatusingApp_Example) 
    
In Prozedur 3 werden die JavaScript-Funktionen hinzugefügt, um die Zuordnungen zu lesen und die Tabellenzeilen zu erstellen sowie um den Prozentsatz der abgeschlossenen Zuordnung zu ändern und zu aktualisieren. Die tatsächlichen Schritte sind iterativer bei der Entwicklung einer App, in der Sie alternativ einen Teil des HTML-Codes erstellen, verwandte Formatvorlagen und JavaScript-Funktionen hinzufügen und testen, mehr HTML-Code ändern oder hinzufügen und dann den Prozess wiederholen.

<a name="pj15_StatusingApp_JavaScript"> </a>

### <a name="creating-the-javascript-functions-for-the-quickstatus-app"></a>Erstellen der JavaScript-Funktionen für die QuickStatus-App

Die Visual Studio Vorlage für eine SharePoint App enthält die App.js-Datei, die Standardinitialisierungscode enthält, der den SharePoint Clientkontext abruft und grundlegende Get- und Set-Aktionen für die App-Seite veranschaulicht. Der JavaScript-Namespace für die SharePoint clientseitige SP.js Bibliothek ist **SP.** Da eine Project Server-App die PS.js Bibliothek verwendet, verwendet die App den **PS-Namespace,** um den Clientkontext abzurufen und auf das JSOM für Project Server zuzugreifen. 
  
JavaScript-Funktionen in der **QuickStatus-App** umfassen Folgendes: 
  
- Der Ereignishandler für **dokumentbereite** Dokumente wird ausgeführt, wenn das Dokumentobjektmodell (DOM) instanziiert wird. Der  ready-Ereignishandler führt die folgenden vier Schritte aus: 
    
    1. Initialisiert die globale **ProjContext-Variable** mit dem Clientkontext für das Project Server JSOM und die globale **Variable pwaWeb.** 
        
    2. Ruft die **getUserInfo-Funktion** auf, um die **globale ProjUser-Variable** zu initialisieren. 
        
    3. Ruft die **getAssignments-Funktion auf,** die angegebene Zuweisungsdaten für den Benutzer abruft. 
        
    4. Bindet Click-Ereignishandler an das Tabellenkopf-Kontrollkästchen und an die Kontrollkästchen in jeder Zeile der Tabelle. Die Click-Ereignishandler verwalten das **aktivierte** Attribut der Kontrollkästchen, wenn der Benutzer ein Kontrollkästchen in der Tabelle auswählt oder deaktiviert. 
    
- Wenn die **getAssignments-Funktion** erfolgreich ist, wird die **onGetAssignmentsSuccess-Funktion** aufgerufen. Diese Funktion fügt für jede Zuordnung eine Zeile in die Tabelle ein, initialisiert die HTML-Steuerelemente in jeder Zeile und initialisiert dann die Eigenschaften der unteren Schaltfläche. 
    
- Der onClick-Ereignishandler für die Schaltfläche **"Update"** ruft die **UpdateAssignments-Funktion** **auf.** Diese Funktion ruft den Prozentwert ab, der auf jede ausgewählte Zuordnung angewendet wird. oder wenn das Textfeld "Prozent abgeschlossen" leer ist, ruft die Funktion den Prozentsatz der abgeschlossenen Arbeit aller ausgewählten Zuordnungen in der Tabelle ab. Die **updateAssignments-Funktion** speichert und sendet dann die Statusaktualisierungen und schreibt eine Meldung zu den Ergebnissen am ende der Seite. 
    
### <a name="procedure-3-to-create-the-javascript-functions"></a>Prozedur 3. So erstellen Sie die JavaScript-Funktionen

1. Öffnen Sie in Visual Studio die App.js Datei, und löschen Sie dann den gesamten Inhalt der Datei.
    
2. Fügen Sie die globalen  Variablen und den ereignisbereiten Ereignishandler für das Dokument hinzu. Der Zugriff auf das **Dokumentobjekt** erfolgt mithilfe einer jQuery-Funktion. 
    
   Der Click-Ereignishandler für das Kontrollkästchen "Tabellenkopfzeile" legt den Kontrollkästchenstatus der Zeilen fest. Wenn alle Zeilenkontrollkästchen aktiviert oder alle deaktiviert sind, legt der Click-Ereignishandler für die Zeilenkontrollkästchen den aktivierten Status des Kopfzeilenkontrollkästchens fest. Die Click-Ereignishandler legen auch die Ergebnismeldung am unteren Rand der Seite auf eine leere Zeichenfolge fest.
    
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

3. Fügen Sie die **getUserInfo-Funktion** hinzu, die **onGetUserNameSuccess aufruft,** wenn die Abfrage erfolgreich ist. Die **onGetUserNameSuccess-Funktion** ersetzt den Inhalt des **Beschriftungsabsätze** durch eine Tabellenbeschriftung, die den Benutzernamen enthält. 
    
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

4. Fügen Sie die **getAssignments-Funktion** hinzu, die **onGetAssignmentsSuccess aufruft** (siehe Schritt 5), wenn die Zuordnungsabfrage erfolgreich ist. Mit **der Option "Einschließen"** wird die Abfrage so beschränkt, dass nur die angegebenen Felder zurückgegeben werden. 
    
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

5. Fügen Sie die **onGetAssignmentsSuccess-Funktion** hinzu, die der Tabelle eine Zeile für jede Zuordnung hinzufügt. Die **Variable prevProjName** wird verwendet, um zu bestimmen, ob sich eine Zeile für ein anderes Projekt befindet. Wenn ja, wird der Projektname fett formatiert angezeigt. Ist dies nicht der Typ, wird der Projektname auf eine leere Zeichenfolge festgelegt. 
    
   > [!NOTE]
   > Das JSOM enthält keine **TimeSpan-Eigenschaften,** die das CSOM enthält, z. **B. ActualWorkTimeSpan**. Stattdessen verwendet jsom Eigenschaften für die Anzahl von Millisekunden, [z. B. die PS. StatusAssignment.actualWorkMilliseconds-Eigenschaft.](https://msdn.microsoft.com/library/736bce1e-f734-0efe-6c5f-e0e891ab00ef%28Office.15%29.aspx) The method to get that property is **get \_ actualWorkMilliseconds**, which returns an integer value. > Die **get_actualWork-Methode** gibt eine Zeichenfolge wie "3h" zurück. Sie können einen der beiden Werte in der **QuickStatus-App** verwenden, ihn jedoch anders anzeigen. Die Zuordnungsabfrage enthält beide Eigenschaften, sodass Sie den Wert während des Debuggens testen können. Wenn Sie die **actualWork-Variable** entfernen, können Sie auch die **ActualWork-Eigenschaft** in der Zuordnungsabfrage entfernen. 
  
   Schließlich initialisiert die **onGetAssignmentsSuccess-Funktion** die Schaltfläche **"Aktualisieren"** und die Schaltfläche **"Aktualisieren"** mit Klickereignishandlern. Der Textwert der Schaltfläche **"Aktualisieren"** könnte auch im HTML-Code festgelegt werden. 
    
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

6. Fügen Sie den **UpdateAssignments-Click-Ereignishandler** für die Schaltfläche **"Aktualisieren"** hinzu. Wenn der Benutzer einen Wert für den Prozentsatz der abgeschlossenen Arbeit eines Vorgangs ändert oder einen Wert im Textfeld **"percentComplete"** hinzufügt, kann der Wert in mehrere Formate eingegeben werden, z. B. "60", "60%" oder "60 %". Die **methode getNumericValue** gibt den numerischen Wert des Eingabetexts zurück. 
    
   > [!NOTE]
   > In einer app, die für die Verwendung in der Produktion entwickelt wurde, sollten Eingabewerte für numerische Informationen Feldüberprüfung und zusätzliche Fehlerüberprüfung enthalten. 
  
   Das **UpdateAssignments-Beispiel** enthält einige grundlegende Fehlerüberprüfungen und zeigt Informationen im **Meldungsabsätzen** am unteren Rand der Seite an – grün, wenn die Aktualisierungsabfrage erfolgreich ist, und Rot, wenn ein Eingabefehler auftritt oder die Aktualisierungsabfrage nicht erfolgreich ist. 
    
   Vor der Verwendung der **submitAllStatusUpdates-Methode** muss die App die Updates mithilfe des PS auf dem Server **speichern. StatusAssignmentCollection.update-Methode.** 
    
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

7. Fügen Sie die **exitToPwa-Funktion** hinzu, die den Parameter der **SPHostUrl-Abfragezeichenfolge** für die URL des Hosts Project Web App-Website verwendet. Um zur Seite "Aufgaben" zurückzukehren, fügen Sie  `"/Tasks.aspx"` die URL an. Beispielsweise würde die **spHostUrl-Variable** auf festgelegt  `https://ServerName/ProjectServerName/Tasks.aspx` werden.
    
   Die **GetQueryStringParameter-Funktion** teilt die URL der **QuickStatus-Seite,** um den angegebenen Parameter in den URL-Optionen zu extrahieren und zurückzugeben. Nachfolgend sehen Sie ein Beispiel für das **Dokument. URL-Wert** für das **QuickStatus-Dokument** (alle in einer Zeile): 
    
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

   Für die vorherige URL gibt die **getQueryStringParameter-Funktion** den **SPHostUrl-Abfragezeichenfolgenwert**  `https://ServerName/pwa` zurück. 
    
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

Wenn Sie die **QuickStatus-App** zu diesem Zeitpunkt veröffentlichen und Project Web App hinzufügen, kann die App über die Seite "Websiteinhalte" ausgeführt werden, ist jedoch nicht einfach für Benutzer verfügbar. Um Benutzern zu helfen, die App zu finden und auszuführen, können Sie dem Menüband auf der Seite "Aufgaben" eine Entsprechende Schaltfläche hinzufügen. In Prozedur 4 wird das Hinzufügen einer benutzerdefinierten Menübandaktion veranschaulicht. 

<a name="pj15_StatusingApp_ribbon"> </a>

### <a name="adding-a-ribbon-custom-action"></a>Hinzufügen einer benutzerdefinierten Menübandaktion

Menübandregisterkarten, Gruppen und Steuerelemente für Project Web App werden in der pwaribbon.xml Datei angegeben, die im Verzeichnis auf dem Computer installiert ist, `[Program Files]\Common Files\Microsoft Shared\Web Server Extensions\15\TEMPLATE\FEATURES\PWARibbon\listtemplates` auf dem Project Server ausgeführt wird. Um benutzerdefinierte Aktionen für das menüband Project Web App zu entwerfen, enthält der Project 2013 SDK-Download eine Kopie der pwaribbon.xml. 
  
Project Web App verwendet unterschiedliche Menübanddefinitionen für die Aufgabenseite, je nachdem, ob die Project Web App-Instanz den Einzeleingabemodus verwendet, mit dem Benutzer Werte für die Arbeitszeittabelle und den Aufgabenstatus eingeben können. Wenn Sie über Administratorberechtigungen für Project Web App verfügen, wählen Sie **PWA Einstellungen** im Dropdown-Einstellungsmenü in der oberen rechten Ecke der Seite aus, um den Eintragsmodus zu bestimmen. On the PWA Einstellungen page, choose **Timesheet Einstellungen and Defaults,** and then look at the **Single Entry Mode** check box at the bottom of the page. 
  
Wenn der Einzeleintragsmodus deaktiviert ist, wird das Menüband auf der Seite "Aufgaben" durch den Bereich "Meine Arbeit" in pwaribbon.xml definiert: 
  
```XML
   <!-- REGION My Work Ribbon-->
   <CustomAction
      Id="Ribbon.ContextualTabs.MyWork"
      . . .
```

Wenn der Einzeleintragsmodus aktiviert ist, wird das Menüband der Seite "Aufgaben" durch den Bereich "Gebundener Modus" in pwaribbon.xml definiert: 
  
```XML
   <!-- REGION Tied Mode Ribbon-->
   <CustomAction
      Id="Ribbon.ContextualTabs.TiedMode"
      . . .
```

Obwohl die Gruppen und Steuerelemente in den einzelnen Regionen ähnlich aussehen, kann ein Steuerelement für den gebundenen Modus eine andere Funktion als dasselbe Steuerelement für den nicht gebundenen Modus aufrufen. In Prozedur 4 wird gezeigt, wie Sie ein Schaltflächensteuerelement für die **QuickStatus-App** hinzufügen, wenn der Einzeleintragsmodus deaktiviert ist (das Kontrollkästchen für den **einzeleintragsmodus** ist deaktiviert). 
  
> [!NOTE]
> Allgemeine Informationen zum Hinzufügen von benutzerdefinierten Aktionen zu einem Menüband oder zu einem Menü in einer SharePoint Anwendung finden Sie unter [Erstellen benutzerdefinierter Aktionen zum Bereitstellen mit Apps für SharePoint.](https://msdn.microsoft.com/library/jj163954.aspx) 
  
### <a name="procedure-4-to-add-a-ribbon-custom-action-to-the-tasks-page"></a>Prozedur 4. So fügen Sie der Seite "Aufgaben" eine benutzerdefinierte Menübandaktion hinzu

1. Überprüfen Sie das Menüband auf der Seite "Aufgaben" in Project Web App. Wählen Sie die Registerkarte **"AUFGABEN"** im Menüband aus, und planen Sie, wie sie geändert werden soll. Es gibt sieben Gruppen, z. **B. "Submit",** **"Tasks"** und **"Period".** Die Gruppe **"Absenden"** verfügt über zwei Steuerelemente, eine Schaltfläche **"Speichern"** und ein Dropdownmenü **"Sendestatus".** Sie können ein Steuerelement an einer beliebigen Stelle in einer Gruppe hinzufügen, eine Gruppe mit einem neuen Steuerelement an einer beliebigen Stelle auf der Registerkarte **AUFGABEN** hinzufügen oder eine weitere Registerkarte des Menübands hinzufügen, die benutzerdefinierte Gruppen und Steuerelemente enthält. In diesem Beispiel fügen wir der Gruppe **"Absenden"** eine dritte Schaltfläche hinzu, in der die Schaltfläche die URL der **QuickStatus-App** aufruft. 
    
2. Klicken Sie im **Projektmappen-Explorer-Bereich** in Visual Studio mit der rechten Maustaste auf das **QuickStatus-Projekt,** und fügen Sie dann ein neues Element hinzu. Wählen Sie im Dialogfeld **"Neues Element hinzufügen"** die **benutzerdefinierte Menübandaktion** aus (siehe Abbildung 4). Benennen Sie beispielsweise die benutzerdefinierte Aktion "RibbonQuickStatusAction", und wählen Sie dann **"Hinzufügen"** aus.
    
   **Abbildung 4. Hinzufügen einer benutzerdefinierten Menübandaktion**

   ![Hinzufügen einer benutzerdefinierten Menübandaktion](media/pj15_CreateStatusingApp_AddRibbonCustomAction.gif "Hinzufügen einer benutzerdefinierten Menübandaktion")
  
3. Lassen Sie auf der ersten Seite des Assistenten zum Erstellen einer **benutzerdefinierten Aktion für das Menüband** die **Hostweboption** ausgewählt, wählen Sie in der Dropdownliste für den benutzerdefinierten Aktionsbereich **"None"** und dann **"Weiter"** aus (siehe Abbildung 5). Die Elemente in den Dropdownlisten sind für SharePoint relevant, nicht für Project Server. Wir ersetzen den größten Teil des generierten XML für die benutzerdefinierte Aktion, sodass sie auf Project Server angewendet wird. 
    
   **Abbildung 5. Angeben von Eigenschaften für die benutzerdefinierte Menübandaktion**

   ![Festlegen von Eigenschaften für die benutzerdefinierte Menübandaktion](media/pj15_CreateStatusingApp_RibbonCustomAction2.gif "Festlegen von Eigenschaften für die benutzerdefinierte Menübandaktion")
  
4. Lassen Sie auf der nächsten Seite des Assistenten zum Erstellen einer **benutzerdefinierten Aktion für das Menüband** alle Standardwerte für die Einstellungen, und wählen Sie dann **Fertig stellen** aus (siehe Abbildung 6). Visual Studio erstellt den Ordner **"RibbonQuickStatusAction",** der eine Elements.xml Datei enthält. 
    
   **Abbildung 6. Angeben der Einstellungen für ein Schaltflächensteuerelement**

   ![Festlegen der Einstellungen für ein Schaltflächensteuerelement](media/pj15_CreateStatusingApp_RibbonCustomAction3.gif "Festlegen der Einstellungen für ein Schaltflächensteuerelement")
  
5. Ändern Sie den standardmäßig generierten Code in der Elements.xml-Datei für die benutzerdefinierte Menübandaktion. Es folgt der Standard-XML-Code:
    
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

   1. Löschen Sie im **CustomAction-Element** das **Sequence-Attribut** und das **Title-Attribut.** 
    
   2. Um der **Submit-Gruppe** ein Steuerelement hinzuzufügen, suchen Sie die erste Gruppe in der  `Ribbon.ContextualTabs.MyWork.Home.Groups` Auflistung in der pwaribbon.xml-Datei, bei der es sich um das Element handelt, das  `<Group Id="Ribbon.ContextualTabs.MyWork.Home.Page" Command="PageGroup" Sequence="10" Title="$Resources:pwafeatures,PAGE_PDP_CM_SUBMIT"` beginnt. Um der **Submit-Gruppe** ein untergeordnetes Steuerelement hinzuzufügen, zeigt der folgende Code das richtige **Location-Attribut** des **CommandUIDefinition-Elements** in der Elements.xml Datei: 
    
      ```XML
        <CommandUIDefinitions>
          <CommandUIDefinition Location="Ribbon.ContextualTabs.MyWork.Home.Page.Controls._children">
             . . .
          </CommandUIDefinition>
        </CommandUIDefinitions>
      ```

   3. Ändern Sie die Attributwerte des untergeordneten **Button-Elements** wie folgt: 
    
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

       - Um die Schaltfläche zum dritten Steuerelement in der Gruppe zu machen, kann das **Sequence-Attribut** eine beliebige Zahl höher sein als der  `Sequence="20"` Wert des vorhandenen Send **Status-Steuerelements** (bei dem es sich um ein **FlyoutAnchor-Element** in pwaribbon.xml handelt). Üblicherweise sind die Sequenznummern von Gruppen und Steuerelementen  `10, 20, 30, …` , wodurch Elemente in Zwischenpositionen eingefügt werden können.
    
       - Das **Command-Attribut** gibt den Befehl an, der im **CommandUIHandler-Element** ausgeführt werden soll (siehe folgenden Schritt 5.d). Sie können den Befehlsnamen vereinfachen, um ihn für den nächsten Entwickler zu vereinfachen. Beispielsweise  `Command="Invoke_QuickStatus"` ist einfacher zu lesen als  `Command="Invoke_RibbonQuickStatusActionButtonRequest"` .
    
       - Die Bildattribute geben das Symbol mit 16 x 16 Pixeln und das Symbol mit 32 x 32 Pixeln für das Schaltflächensteuerelement an. Gibt in der Standarddatei Elements.xml  `Image32by32="_layouts/15/images/placeholder32x32.png"` einen orangefarbenen Punkt an. Sie können Symbole aus den Imagemapdateien (ps16x16.png und ps32x32.png) extrahieren, die im `[Program Files]\Common Files\Microsoft Shared\Web Server Extensions\15\TEMPLATE\LAYOUTS\1033\IMAGES` Verzeichnis auf dem Computer installiert sind, auf dem Project Server ausgeführt wird. Beispielsweise befindet sich das Symbol mit 32 x 32 Pixeln in der zweiten Spalte der Symbole links und in der zehnten Zeile vom oberen Rand der ps32x32.png Bildzuordnung nach unten (der obere Rand des Symbols befindet sich nach dem Ende der neunten Zeile; 9 Zeilen x 32 Pixel/Zeile = 288 Pixel). 
    
       - Um eine QuickInfo für das Schaltflächensteuerelement anzuzeigen, fügen Sie das **ToolTipTitle-Attribut** und das **ToolTipDescription-Attribut** hinzu. 
    
    4. Ändern Sie die Attribute des **CommandUIHandler-Elements.** Stellen Sie beispielsweise sicher, dass das **Command-Attribut** mit dem **Command-Attributwert** für das **Button-Element** übereinstimmt. Für das **CommandAction-Attribut** `~appWebUrl` ist ein Platzhalter für die URL der **QuickStatus-Webseite.** Wenn die Menübandschaltfläche die **QuickStatus-App** aufruft, wird das **{StandardTokens}-Token** durch URL-Optionen ersetzt, die **SPHostUrl,** **SPLanguage,** **SPClientTag,** **SPProductNumber** und **SPAppWebUrl** enthalten.
    
        ```XML
            <CommandUIHandlers>
                <CommandUIHandler Command="Invoke_QuickStatus"
                                  CommandAction="~appWebUrl/Pages/Default.aspx?{StandardTokens}"/>
            </CommandUIHandlers>
        ```

6. Öffnen Sie im **Projektmappen-Explorer** den **Feature1.feature-Designer,** und verschieben Sie das **RibbonQuickStatusAction-Element** aus den **Elementen im Lösungsbereich** in die **Elemente im Featurebereich.** Wenn Sie dann den **Package.package-Designer** öffnen, befindet sich das **RibbonQuickStatusAction-Element** in den **Elementen im Paketbereich.** 
    
Während Sie die App entwickeln und eine Menübandschaltfläche hinzufügen, testen Sie normalerweise die App und legen Haltepunkte im JavaScript-Code für das Debuggen fest. Wenn Sie **F5** drücken, um mit dem Debuggen zu beginnen, kompiliert Visual Studio die App, stellt sie auf der Website bereit, die in der **Website-URL-Eigenschaft** des **QuickStatus-Projekts** angegeben ist, und zeigt eine Seite an, auf der Sie gefragt werden, ob Sie der App vertrauen. Wenn Sie fortfahren und dann die **QuickStatus-App** beenden, wird sie zur Seite "Aufgaben" in Project Web App zurück. 

> [!NOTE]
> Abbildung 7 zeigt, dass die Schaltfläche **"Schnellstatus"** auf der Registerkarte **"AUFGABEN"** des Menübands deaktiviert ist. Nach vielen Debugbereitstellungen mit Visual Studio können benutzerdefinierte Menübandsteuerelemente blockiert werden, wenn Sie mit dem Debuggen oder Bereitstellen der veröffentlichten App auf demselben Testserver fortfahren. Um die Schaltfläche zu aktivieren, löschen Sie das **RibbonQuickStatusAction-Element** in Visual Studio, und erstellen Sie dann eine neue Menübandaktion mit einem anderen Namen und einer anderen ID. Wenn das Problem dadurch nicht behoben wird, versuchen Sie, die App aus der Project Web App-Testinstanz zu entfernen, und erstellen Sie die App dann mit einer anderen App-ID neu. 
  
**Abbildung 7. Anzeigen der QuickInfo der deaktivierten Schaltfläche "Schnellstatus"**

![Anzeigen der QuickInfo der deaktivierten Schaltfläche](media/pj15_CreateStatusingApp_ButtonToolTipDisabled.gif "Anzeigen der QuickInfo der deaktivierten Schaltfläche")
  
In Verfahren 5 wird gezeigt, wie die **QuickStatus-App** bereitgestellt und installiert wird. Verfahren 6 zeigt einige zusätzliche Schritte beim Testen der App nach der Installation. 

<a name="pj15_StatusingApp_Deploying"> </a>

## <a name="deploying-the-quickstatus-app"></a>Bereitstellen der QuickStatus-App

Es gibt verschiedene Möglichkeiten, eine App in einer SharePoint Webanwendung bereitzustellen, z. B. Project Web App. Welche Bereitstellung Sie verwenden, hängt davon ab, ob Sie die App in einem privaten SharePoint Katalog oder im öffentlichen Office Store veröffentlichen möchten und ob SharePoint lokal installiert ist oder ein Onlinemandant ist. In Verfahren 5 wird gezeigt, wie die **QuickStatus-App** in einer lokalen Installation in einem privaten App-Katalog bereitgestellt wird. Weitere Informationen finden Sie unter [Installieren und Verwalten von Apps für SharePoint 2013](https://technet.microsoft.com/library/fp161232.aspx) und Veröffentlichen von Apps für [SharePoint](https://msdn.microsoft.com/library/jj164070.aspx)
  
> [!NOTE]
> Das Hinzufügen einer App zu einem SharePoint Katalog erfordert SharePoint Administratorberechtigungen. 
  
### <a name="procedure-5-to-deploy-the-quickstatus-app"></a>Prozedur 5. So stellen Sie die QuickStatus-App bereit

1. Speichern Sie in Visual Studio alle Dateien, klicken Sie dann im **Projektmappen-Explorer** mit der rechten Maustaste auf das **QuickStatus-Projekt,** und wählen Sie **"Veröffentlichen"** aus.
    
2. Da die **QuickStatus-App** SharePoint gehostet wird, gibt es nur sehr wenige Optionen für die Veröffentlichung (siehe Abbildung 8). Wählen Sie im Dialogfeld **"Apps für Office veröffentlichen" und im** Dialogfeld SharePoint die Option **"Fertig stellen"** aus.
    
   **Abbildung 8. Veröffentlichen der QuickStatus-App**

   ![Verwenden des Assistenten zum Veröffentlichen](media/pj15_CreateStatusingApp_PublishWizard.gif "Verwenden des Assistenten zum Veröffentlichen")
  
3. Kopieren Sie die QuickStatus.app Datei aus dem `~\QuickStatus\bin\Debug\app.publish\1.0.0.0` Verzeichnis in ein praktisches Verzeichnis auf dem lokalen Computer (oder auf den SharePoint Computer für eine lokale Installation). 
    
4. Wählen Sie in SharePoint Zentraladministration im Schnellstart die Option **"Apps"** und dann **"App-Katalog verwalten"** aus.
    
5. Wenn kein App-Katalog vorhanden ist, erstellen Sie eine Websitesammlung für den App-Katalog, indem Sie den Abschnitt *"Konfigurieren der App-Katalogwebsite für eine Webanwendung"* im Abschnitt ["Verwalten des App-Katalogs" in SharePoint 2013](https://technet.microsoft.com/library/fp161234.aspx)befolgen.
    
   Wenn ein App-Katalog vorhanden ist, navigieren Sie zur Website-URL auf der Seite "App-Katalog verwalten". In den folgenden Schritten lautet beispielsweise die App-Katalogwebsite  `https://ServerName/sites/TestApps` .
    
6. Wählen Sie auf der Seite "App-Katalog" in der Schnellstartleiste **"Apps für SharePoint"** aus. On the Apps for SharePoint page, on the **FILES** tab of the ribbon, choose **Hochladen Document**.
    
7. Navigieren Sie im Dialogfeld **"Dokument hinzufügen"** nach der QuickStatus.app Datei, fügen Sie Kommentare für die Version hinzu, und klicken Sie dann auf **"OK".**
    
8. Wenn Sie eine App hinzufügen, können Sie auch lokale Informationen für die App-Beschreibung, das Symbol und andere Informationen hinzufügen. Fügen Sie im Dialogfeld **"Apps für SharePoint – QuickStatus.app"** die Informationen hinzu, die Sie für die App in der SharePoint Websitesammlung anzeigen möchten. Fügen Sie beispielsweise die folgenden Informationen hinzu: 
    
   1. **Kurzbeschreibungsfeld:** Geben Sie die Schnellstatus-Test-App ein.
    
   2. **Beschreibungsfeld:** Geben Sie "Test"-App ein, um den Prozentsatz der abgeschlossenen Aufgaben in mehreren Projekten zu aktualisieren.
    
   3. **Symbol-URL-Felder:** Fügen Sie den Websiteressourcen für den App-Katalog ein Bild mit 96 x 96 Pixeln für das App-Symbol hinzu. Navigieren Sie beispielsweise im `https://ServerName/sites/TestApps` Dropdownmenü **Einstellungen** zu **"Websiteinhalte",** wählen Sie **"Websiteobjekte"** aus, und fügen Sie dann das quickStatusApp.png Bild hinzu. Klicken Sie mit der rechten Maustaste auf das **QuickStatusApp-Element,** wählen Sie **"Eigenschaften"** aus, und kopieren Sie dann den **Url-Wert im** Dialogfeld **"Eigenschaften".** Kopieren Sie z.  `https://ServerName/sites/TestApps/SiteAssets/QuickStatusApp.png` B. den Wert, und fügen Sie ihn in das Webadressfeld der **Symbol-URL** ein. Geben Sie eine Beschreibung für das Symbol ein, z. B. (wie in Abbildung 9 dargestellt), und geben Sie das QuickStatus-App-Symbol ein. Testen Sie, dass die URL gültig ist.
    
      **Abbildung 9. Hinzufügen einer Symbol-URL für die QuickStatus-App**

      ![Festlegen von Eigenschaften für die App in SharePoint](media/pj15_CreateStatusingApp_AddAppToSharePointSettings.gif "Festlegen von Eigenschaften für die App in SharePoint")
  
   4. **Kategoriefeld:** Wählen Sie eine vorhandene Kategorie aus, oder geben Sie Ihren eigenen Wert an. Geben Sie z. B. "Statusing" ein.
    
      > [!NOTE]
      > Eine Kategorie mit dem Namen **Statusing** dient nur zu Testzwecken. Eine typische Kategorie für Project Server-Apps ist **Project-Verwaltung.** 
  
   5. **Publisher Namensfeld:** Geben Sie den Namen des Herausgebers ein. Geben Sie in diesem Beispiel Project SDK ein.
    
   6. **Aktiviertes** Feld: Aktivieren Sie das Kontrollkästchen **"Aktiviert",** um die App für Project Websiteadministratoren der Web App für die Installation sichtbar zu machen. 
    
   7. Zusätzliche Felder sind optional. Sie können z. B. eine Support-URL und mehrere Hilfebilder für die Seite "App-Details" hinzufügen. In Abbildung 9 enthalten die Felder **"Bild-URL 1"** die URL für einen Screenshot der App und eine Beschreibung des Screenshots. 
    
   8. Wählen Sie im Dialogfeld **"Apps für SharePoint – QuickStatus.app"** die Option **"Speichern"** aus. In Abbildung 9 ist das **Element "Schnellstatusaktualisierung"** in der Bibliothek "Apps für SharePoint" zur Bearbeitung ausgecheckt. Auf der Registerkarte **"BEARBEITEN"** des Dialogfeld-Menübands würden Sie also **"Einchecken"** auswählen, um den Vorgang abzuschließen (siehe Abbildung 10). 
    
      **Abbildung 10. Die QuickStatus-App wird der Bibliothek "Apps für SharePoint" hinzugefügt.**

      ![Die QuickStatus-App wird SharePoint hinzugefügt](media/pj15_CreateStatusingApp_AddAppToSharePoint.gif "Die QuickStatus-App wird SharePoint hinzugefügt")
  
9. Wählen Sie in Project Web App im Dropdownmenü **Einstellungen** die Option **"App hinzufügen"** aus. Wählen Sie auf der Seite "Ihre Apps" in der Schnellstartleiste **"Aus Ihrer Organisation" und** dann **"App-Details"** für die **Schnellstatusaktualisierungs-App** aus. Abbildung 11 zeigt die Detailseite mit dem App-Symbol, dem Screenshot und anderen Informationen, die Sie im vorherigen Schritt hinzugefügt haben. 
    
   **Abbildung 11. Verwenden der Seite "Details zum Schnellstatusupdate" in Project Web App**

   ![Hinzufügen der QuickStatus-App zu Project Web App](media/pj15_CreateStatusingApp_AddAppToPWA.gif "Hinzufügen der QuickStatus-App zu Project Web App")
  
10. On the Quick Status Update details page, choose **ADD IT**. Project Web App zeigt ein Dialogfeld mit den Vorgängen an, die die QuickStatus-App ausführen kann (siehe Abbildung 12). Die Liste der Vorgänge wird von den **AppPermissionRequest-Elementen** in der datei AppManifest.xml abgeleitet. 
    
    **Abbildung 12. Überprüfen, ob Sie der Schnellstatus-App vertrauen**

    ![Überprüfen des Vertrauens gegenüber der QuickStatus-App](media/pj15_CreateStatusingApp_AddAppToPWA2Trust.gif "Überprüfen des Vertrauens gegenüber der QuickStatus-App")
  
11. Wählen Sie im Dialogfeld **"Schnellstatusaktualisierung vertrauen"** die Option **"Vertrauen"** aus. Die App wird der Seite Project Web App Site Contents hinzugefügt (siehe Abbildung 13).
    
    **Abbildung 13. Anzeigen der Schnellstatus-App auf der Seite "Websiteinhalte"**

    ![Anzeigen der QuickStatus-App in den Websiteinhalten](media/pj15_CreateStatusingApp_AddAppToPWA3.gif "Anzeigen der QuickStatus-App in den Websiteinhalten")
  
Auf der Seite "Websiteinhalte" können Sie das Symbol **"Schnellstatusaktualisierung"** auswählen, um die App auszuführen.

> [!NOTE]
> Für zusätzliche Befehle, die Informationen über die App bereitstellen, wählen Sie auf der Seite "Websiteinhalte" den Bereich aus, der den Namen der **Schnellstatusaktualisierung** und die Auslassungspunkte (...) enthält. Sie können die Seite "Info" für die App überprüfen, die Seite "App-Details" anzeigen, die Informationen zu App-Fehlern enthält, die App-Berechtigungsseite überprüfen oder die App aus Project Web App entfernen. 
  
Auf der Seite "Aufgaben" in Project Web App (siehe Abbildung 14) sollte die Schaltfläche **"QuickStatus"** auf dem Menüband aktiviert sein. Wenn die Schaltfläche **"Schnellstatus"** deaktiviert ist, versuchen Sie es mit den in der Notiz für Abbildung 7 beschriebenen Aktionen. 

**Abbildung 14. Starten der QuickStatus-App über die Registerkarte "AUFGABEN"**

![Starten der QuickStatus-App von der Registerkarte "TASKS"](media/pj15_CreateStatusingApp_TasksRibbon.gif "Starten der QuickStatus-App von der Registerkarte &quot;TASKS&quot;")
  
In Prozedur 6 werden einige Tests gezeigt, die mit der QuickStatus-App durchgeführt werden müssen.

<a name="pj15_StatusingApp_Testing"> </a>

## <a name="testing-the-quickstatus-app"></a>Testen der QuickStatus-App

Jeder Vorgang, den ein Benutzer in der **QuickStatus-App** ausprobieren kann, sollte auf einer Testinstallation von Project Server getestet werden, bevor die App auf einem Produktionsserver oder einem Produktionsmandanten von Project Online bereitgestellt wird. Mit einer Testinstallation können Sie Zuordnungen für Benutzer ändern und löschen, ohne dass sich dies auf tatsächliche Projekte auswirkt. Die Tests sollten auch mehrere Benutzer umfassen, die über unterschiedliche Berechtigungssätze verfügen, z. B. Administrator, Projektmanager und Teammitglieder. Durch sorgfältige Tests können Änderungen gefunden werden, die in der App vorgenommen werden sollten, die beim Testen während der Entwicklung nicht erkennbar waren. In Verfahren 6 sind mehrere Tests für die **QuickStatus-App** aufgeführt, jedoch keine vollständige Reihe von Tests. 
  
### <a name="procedure-6-to-test-the-quickstatus-app"></a>Prozedur 6. So testen Sie die QuickStatus-App

1. Führen Sie die **QuickStatus-App** aus, bei der der Benutzer keine Zuweisungen hat. Die App sollte unten auf der Seite eine blaue Meldung anzeigen, z. B. weist der **Benutzername keine Zuweisungen auf.**
    
   Wählen Sie **"Aktualisieren"** aus, und die Meldungsänderungen in eine grüne **Zuordnung wurden aktualisiert.**
    
   > [!NOTE]
   > Das App-Verhalten sollte so geändert werden, dass die Schaltfläche **"Aktualisieren"** deaktiviert ist, wenn keine Zuweisungen vorhanden sind. 
  
2. Führen Sie die App aus, in der der Benutzer mehrere Aufgaben in mehreren verschiedenen Projekten hat und einige Zuordnungen nicht abgeschlossen sind. Beachten Sie die Darstellung der App und führen Sie Aktionen wie folgt aus (siehe Abbildung 15):
    
   1. Die **OnGetAssignmentsSuccess-Funktion** erstellt eine Zeile in der Tabelle für jede Zuordnung für den aktuellen Benutzer. Der Projektname wird nur einmal in fetter Schrift für die erste Zuordnung in jedem Projekt angezeigt. 
    
   2. Deaktivieren Sie das Kontrollkästchen in der Spaltenüberschrift **Vorgangsname.** Der Tabellenkopf-Click-Ereignishandler löscht alle anderen Kontrollkästchen in den Aufgabenzeilen. 
    
   3. Wählen Sie alle Aufgaben aus. Der Click-Ereignishandler für jede Zeile bestimmt, ob alle Zeilen ausgewählt sind, und wählt ggf. die Spaltenüberschrift **"Vorgangsname"** aus. 
    
   4. Deaktivieren Sie erneut alle Kontrollkästchen, und wählen Sie dann eine Zuordnung mit verbleibender Arbeit aus. Abbildung 15 zeigt beispielsweise, dass für den obersten Vorgang T1 noch 20 % verbleibende Arbeit zu erledigen ist.
    
   5. Geben Sie im Textfeld **"Prozent abgeschlossen"** den Wert 80 ein, und wählen Sie dann **"Aktualisieren"** aus. Am unteren Rand der Seite sollte eine grüne Meldung angezeigt **werden, Zuordnungen wurden aktualisiert.**
    
      **Abbildung 15. Aktualisieren einer Zuweisung in der QuickStatus-App**

      ![Aktualisieren einer Zuweisung in der QuickStatus-App](media/pj15_CreateStatusingApp_Testing1Update.gif "Aktualisieren einer Zuweisung in der QuickStatus-App")
  
3. Wählen Sie **"Aktualisieren"** aus (siehe Abbildung 16). Alle Vorgänge werden erneut ausgewählt, und der oberste Vorgang zeigt 80 % abgeschlossen an. 
    
      **Abbildung 16. Aktualisieren der Seite "Schnellstatusaktualisierung"**

      ![Aktualisieren der QuickStatus-Seite](media/pj15_CreateStatusingApp_Testing2Refresh.gif "Aktualisieren der QuickStatus-Seite")
  
4. Deaktivieren Sie alle Kontrollkästchen, und wählen Sie dann eine andere Aufgabe aus. Wählen Sie z. **B. "Neue Aufgabe" aus PWA aus.** Lassen Sie das Textfeld **"Prozent abgeschlossen"** leer, löschen Sie den gesamten Text in der Spalte **"% abgeschlossen"** für den ausgewählten Vorgang, und wählen Sie dann **"Aktualisieren"** aus. Da beide Textfelder leer sind, zeigt die App eine rote Fehlermeldung an (siehe Abbildung 17).
    
      **Abbildung 17. Testen der Fehlermeldung**

      ![Testen der Fehlermeldung](media/pj15_CreateStatusingApp_Testing3Error.gif "Testen der Fehlermeldung")
  
5. Aktualisieren Sie die vorherige Aufgabe auf 80 %, und wählen Sie dann **"Beenden" aus.** Die **exitToPwa-Funktion** ändert den Speicherort des Browserfensters zur Seite "Aufgaben" in der SharePoint Hostanwendung (d. h. die URL ändert sich in https://ServerName/pwa/Tasks.aspx) . Abbildung 18 zeigt, dass der **T1-Vorgang** und der **neue Vorgang aus PWA** Vorgang jeweils 80 % abgeschlossen angezeigt werden. 
    
      **Abbildung 18. Überprüfen, ob die Aufgaben in Project Web App aktualisiert werden**

      ![Überprüfen der aktualisierten Aufgaben in Project Web App](media/pj15_CreateStatusingApp_TasksUpdatedInPWA.gif "Überprüfen der aktualisierten Aufgaben in Project Web App")
  
6. Bevor der aktualisierte Status in Project Professional 2013 angezeigt wird, müssen die Änderungen zur Genehmigung übermittelt und dann vom Projektmanager genehmigt werden.
    
Beim Testen werden mehrere weitere Änderungen in der **QuickStatus-App** angezeigt, um die Benutzerfreundlichkeit zu verbessern. Beispiel:

- Es sollten zusätzliche Fehlerüberprüfungen und Überprüfungen von Textfeldwerten durchgeführt werden. Derzeit kann ein Benutzer einen nicht numerischen Wert oder einen negativen Wert für "Percent Complete" eingeben, was zu einer unfreundlichen Fehlermeldung führt. Bei einem negativen Wert lautet die Fehlermeldung beispielsweise Fehler beim Aktualisieren von **Zuordnungen: PJClientCallableException: StatusingSetDataValueInvalid**.
    
- Die Fehlermeldung für leere Textfelder könnte das Projekt und den Vorgang zusätzlich zur Zeilennummer auflisten.
    
- Die Erfolgsmeldung kann eine Liste der aktualisierten Aufgaben enthalten. oder wenn die **UpdateAssignments-Funktion** erfolgreich ist, kann sie eine automatische Seitenaktualisierung ausführen und aktualisierte Aufgaben oder Prozentsätze in einer anderen Farbe und fett formatiert anzeigen. 
    
- Um eine sehr große Tabelle zu vermeiden, sollte die Tabelle der Zuordnungen auf Vorgänge beschränkt sein, die zu weniger als 100 % abgeschlossen sind. Oder fügen Sie eine Option zum Anzeigen aller Aufgaben hinzu. Dieses Problem kann auch mithilfe eines jQuery-basierten Rasters anstelle einer Tabelle behoben werden, in dem Sie problemlos Filterung und Raster paging implementieren können.
    
- Da die **QuickStatus-App** keinen Status übermittelt, ist das **Symbol "Schnellstatus"** auf der Registerkarte **"AUFGABEN"** des Menübands logischer das erste Symbol in der Gruppe **"Aufgaben"** und nicht das letzte Symbol in der Gruppe **"Absenden".** 
    
- Da die **onGetAssignmentsSuccess-Funktion** den **BtnSubmitUpdate-Schaltflächentext** initialisiert, aber die anderen Schaltflächentextwerte in HTML initialisiert werden, befindet sich die Seite in einem teilweise initialisierten Zustand, während die **Funktion getAssignments** ausgeführt wird. Schaltflächen auf der Seite würden konsistenter erscheinen, wenn die Textwerte alle in HTML initialisiert würden. 
    
Am wichtigsten ist, dass der Ansatz, den die **QuickStatus-App** verwendet, bei der sie sich in Prozent für Zuordnungen ändert, in einer Produktions-App überarbeitet werden sollte. Weitere Informationen finden Sie im Abschnitt ["Nächste Schritte".](#pj15_StatusingApp_NextSteps) 

<a name="pj15_StatusingApp_Example"> </a>

## <a name="example-code-for-the-quickstatus-app"></a>Beispielcode für die QuickStatus-App

### <a name="defaultaspx-file"></a>Default.aspx-Datei

Der folgende Code befindet sich in der `Pages\Default.aspx` Datei des **QuickStatus-Projekts:** 
  
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

### <a name="appjs-file"></a>App.js Datei

Der folgende Code befindet sich in der `Scripts\App.js` Datei des **QuickStatus-Projekts:** 
  
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

Der folgende CSS-Code befindet sich in der `Content\App.css` Datei des **QuickStatus-Projekts:** 
  
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

### <a name="elementsxml-file-for-the-ribbon"></a>Elements.xml-Datei für das Menüband

Die folgende XML-Definition für die hinzugefügte Schaltfläche auf der Registerkarte **TASKS** im Menüband befindet sich in der `RibbonQuickStatusAction\Elements.xml` Datei des **QuickStatus-Projekts:** 
  
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

Es folgt der XML-Code für das App-Manifest des **QuickStatus-Projekts,** das die beiden Berechtigungsanforderungsbereiche enthält, die zum Aktualisieren des Zuweisungsstatus des App-Benutzers in mehreren Projekten erforderlich sind: 
  
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

### <a name="appiconpng-file"></a>AppIcon.png Datei

Die vollständige Visual Studio-Lösung für die **QuickStatus-App** enthält eine benutzerdefinierte AppIcon.png Datei. Die Lösung wird im Project 2013 SDK-Download enthalten sein. 

<a name="pj15_StatusingApp_NextSteps"> </a>

## <a name="next-steps"></a>Nächste Schritte

Die **QuickStatus-App** ist ein relativ einfaches Beispiel für das Schreiben von Apps, die auf Project Server 2013 und Project Online installiert werden können. Im Abschnitt ["Testen der QuickStatus-App"](#pj15_StatusingApp_Testing) sind mehrere Verbesserungen aufgeführt, die für eine bessere Benutzerfreundlichkeit vorgenommen werden können. Die **QuickStatus-App** verwendet JavaScript-Funktionen, um den Zuweisungsstatus für Project Web App zu aktualisieren. Das Ändern des Prozentsatzes abgeschlossener Zuordnungen ist jedoch keine empfohlene Projektmanagement-Methode. Ein weiterer Ansatz besteht darin, den tatsächlichen Anfangstermin und die verbleibende Dauer der zugewiesenen Vorgänge zu aktualisieren. Eine Erläuterung der Probleme finden Sie unter ["Update Better"](https://www.mpug.com/articles/update-better) im MPUG-Newsletter. 

<a name="pj15_StatusingApp_AdditionalResources"> </a>

## <a name="see-also"></a>Siehe auch

- [Project Serverprogrammierungsaufgaben](project-programming-tasks.md)
- [SharePoint-Add-Ins](https://msdn.microsoft.com/library/jj163230.aspx)
- [Verwalten von Vorgangsaktualisierungen in Project Web App](https://technet.microsoft.com/library/hh767481%28v=office.14%29.aspx)
- [Erstellen benutzerdefinierter Aktionen zur Bereitstellung mit SharePoint-Add-Ins](https://msdn.microsoft.com/library/jj163954.aspx)
    

