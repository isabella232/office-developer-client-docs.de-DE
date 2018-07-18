---
title: Erstellen eines auf SharePoint gehosteten Project Server-Add-Ins
manager: soliver
ms.date: 08/10/2016
ms.audience: Developer
localization_priority: Normal
ms.assetid: bb9c3c00-7121-41e1-9db3-75550d040ba8
description: Die drei Arten von apps, die Sie für Project Online (automatisch gehostet, vom Anbieter gehostet und SharePoint-Hosting) erstellen können, ist die SharePoint-hosted app am einfachsten zu erstellen und bereitstellen.
ms.openlocfilehash: 135a6cd330224041db213e0408735209056d34af
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19796202"
---
# <a name="create-a-sharepoint-hosted-project-server-add-in"></a>Erstellen eines auf SharePoint gehosteten Project Server-Add-Ins

Die drei Arten von apps, die Sie für Project Online (automatisch gehostet, vom Anbieter gehostet und SharePoint-Hosting) erstellen können, ist die SharePoint-hosted app am einfachsten zu erstellen und bereitstellen. Nicht der Fall ist einer SharePoint-hosted app OAuth-Authentifizierung erfordern und nicht Azure verwenden oder Wartung einer lokalen Website für die vom Anbieter gehosteten Ressourcen erfordern. Die **App für SharePoint 2013** -Vorlage in Visual Studio ist eine bequeme Framework für die Entwicklung von apps, die veröffentlicht und in den Office Store verkauft oder mit einem privaten app-Katalog in SharePoint bereitgestellt werden können. 
  
In-Projekt ist Zeitberichte der Prozess, in dem ein Teammitglied die Seite Aufgaben in Project Web App verwenden kann, um den Status einer zugewiesenen Aufgabe, wie die Anzahl der täglichen einer Woche arbeiten für den Vorgang aufgewendeten Arbeitsstunden zu übermitteln. Der Zuordnungsbesitzer (in der Regel der Projektmanager) kann genehmigen oder ablehnen den Status. Wenn der Status genehmigt wird, wird den Zeitplan von Project neu berechnet. Die **QuickStatus** -app zeigt zugewiesene Aufgaben, die der Benutzer kann schnell Prozent abgeschlossen aktualisieren und Status der ausgewählten Zuordnungen zur Genehmigung übermitteln. Obwohl die Seite Aufgaben in Project Web App viel mehr Funktionen verfügt, ist die **QuickStatus** -app ein Beispiel, das eine einfache Benutzeroberfläche bereitstellt. 
  
Die **QuickStatus** -app ist ein Beispiel für Entwickler. Es ist nicht für die Verwendung in einer produktionsumgebung vorgesehen. Der primäre Zweck ist ein Beispiel für app-Entwicklung für Project Online, nicht für eine voll funktionsfähige statuserfassungs-app erstellen angezeigt. Eine bessere Ansatz für Zeitberichte finden Sie unter der Empfehlung in den [nächsten Schritten](#pj15_StatusingApp_NextSteps).
  
Allgemeine Informationen zu Zeitberichte finden Sie unter [Vorgang in Arbeit](https://support.office.com/article/Find-information-about-Project-Server-2013-8b08a414-15a7-4076-b2db-c90d0214ea7f?ui=en-US&rs=en-US&ad=US#BKMK_TaskProgress). Weitere Informationen zum Entwickeln von Add-Ins für SharePoint und Project Server finden Sie unter [SharePoint-Add-ins](http://msdn.microsoft.com/en-us/library/jj163230.aspx).

<a name="pj15_StatusingApp_Prerequisites"> </a>

## <a name="prerequisites-for-creating-an-app-for-project-server-2013"></a>Erforderliche Komponenten für das Erstellen einer app für Project Server 2013

Informationen zum Entwickeln von apps relativ einfach, die mit Project Online oder einer lokalen Installation von Project Server 2013 bereitgestellt werden können, können Sie die Napa verwenden, die eine online-Entwicklung-Umgebung bereitstellen. Für komplexere apps können Project Web App-Multifunktionsleiste und einfacher Debuggen während der Entwicklung, ändern Sie Visual Studio 2012 oder Visual Studio 2013 verwenden. Beispielsweise können Sie mit einer lokalen Installation manuell die Datentabellen Entwürfe, damit die Änderungen in der Project Server-Datenbank überprüfen. In diesem Artikel veranschaulicht, wie app-Entwicklung mit Visual Studio ausführen.
  
Entwicklung von apps mit Visual Studio Project Server ist Folgendes erforderlich:
  
- Stellen Sie sicher, dass Sie die neuesten Servicepacks und Windows-Updates auf Ihrem lokalen Entwicklungscomputer installiert haben. Das Betriebssystem kann Windows 7, Windows 8, Windows Server 2008 oder Windows Server 2012 sein.
    
- Sie müssen einen Computer verfügen, auf dem SharePoint Server 2013 und Project Server 2013 installiert, in der Computer für eine app-Isolation und Sideloading Apps konfiguriert ist. Sideloading kann Visual Studio die app für das debugging vorübergehend zu installieren. Sie können eine lokale Installation von SharePoint und Project Server verwenden. Weitere Informationen finden Sie unter [Einrichten einer lokalen Entwicklungsumgebung für apps für SharePoint](http://msdn.microsoft.com/en-us/library/fp179923%28Office.15%29.aspx).
    
   > [!NOTE]
   > Konfigurieren Sie für eine lokale Installation einer isolierten app Domäne *vor* einen unternehmenseigenen app-Katalog zu erstellen. 
  
- Dem Entwicklungscomputer kann auf einem Remotecomputer sein, der Office Developer Tools für Visual Studio 2012 installiert hat. Stellen Sie sicher, dass Sie die aktuellste Version installiert haben; finden Sie im Abschnitt *Tools* den [Downloads für Apps für Office und SharePoint](http://msdn.microsoft.com/en-us/office/apps/fp123627.aspx).
    
- Stellen Sie sicher, dass die Project Web App-Instanz Sie für die Entwicklung verwenden und Tests in den Browser zugänglich ist.
    
Informationen zur Verwendung der online-Tools finden Sie unter [Einrichten einer Umgebung für die Entwicklung von apps für SharePoint in Office 365](http://msdn.microsoft.com/en-us/library/fp161179.aspx). Eine exemplarische Vorgehensweise zur Erstellung einer einfachen app für Project Server, die online-Tools verwendet, werden soll, finden Sie unter EPMSource-Blog-Reihe [Erstellen Ihrer ersten app für Project Server](http://epmsource.com/2012/11/20/building-your-first-project-server-app-part-zerothe-introduction/).

<a name="pj15_StatusingApp_UsingVisualStudio"> </a>

## <a name="using-visual-studio-to-create-a-project-server-app"></a>Verwenden von Visual Studio zum Erstellen einer Project Server-app

Office Developer Tools für Visual Studio 2012 enthält eine Vorlage für SharePoint-apps, die mit Project Server 2013 verwendet werden können. Wenn Sie eine app-Lösung erstellen, enthält die Lösung für den benutzerdefinierten Code die folgenden Dateien:
  
- **AppManifest.xml** umfassen Einstellungen für die app-Titel, berechtigungsanforderungsbereich und andere Eigenschaften. Schritt 1 enthält die Schritte zum Festlegen der Eigenschaften mithilfe des Manifest-Designers. 
    
- **"Default.aspx"** im Ordner Seiten ist die Hauptseite der app. Verfahren 2 zeigt, wie HTML5 Inhalte für die **QuickStatus** -app hinzufügen. 
    
- **App.js** in den Ordner Scripts ist die primäre Datei für den benutzerdefinierten JavaScript-Code. Schritt 3 wird den JavaScript-Code für die **QuickStatus** -app erläutert. 
    
   Wenn Sie kommerziellen Steuerelemente wie zum Beispiel ein jQuery-basierte Raster- oder Datumsauswahl hinzufügen, können Sie Verweise auf zusätzliche JavaScript-Dateien in der Datei "default.aspx" hinzufügen.
    
- **"App.CSS"** im Ordner "Content" ist die primäre Datei für benutzerdefinierte CSS3 Formatvorlagen. Schritt 2 und 3 Verfahren enthalten Informationen zu cascading Stylesheets (CSS)-Formate für die **QuickStatus** -app. Sie können die Verweise auf zusätzliche CSS-Dateien in der Datei "default.aspx" hinzufügen. 
    
- **AppIcon.png** im Ordner Images ist das 96 x 96-Symbol, das die app im Office Store oder den app-Katalog wird angezeigt. 
    
Um die Project Web App-Multifunktionsleiste ändern, können Sie eine benutzerdefinierte Aktion hinzufügen. Der [Beispielcode für die QuickStatus-app](#pj15_StatusingApp_Example) -Abschnitt enthält den vollständigen Code für die geänderten Dateien Default.aspx, App.js, "App.CSS", "Elements.xml" und "AppManifest.xml". 
  
### <a name="procedure-1-to-create-an-app-project-in-visual-studio"></a>Schritt 1. Zum Erstellen eines app-Projekts in Visual Studio

1. Führen Sie Visual Studio 2012 als Administrator, und wählen Sie dann auf der Startseite **Neues Projekt** aus. 
    
2. Klicken Sie im Dialogfeld **Neues Projekt** erweitern Sie die **Vorlagen**, **Visual C#-** und **Office/SharePoint** -Knoten zu, und wählen Sie dann **Apps**aus. Verwenden Sie die Standardeinstellung **.NET Framework 4.5** in der Ziel-Framework Dropdown-Liste am oberen Rand der mittleren Bereich, und wählen Sie dann **App für SharePoint 2013** (siehe Abbildung 1). 
    
3. Im Feld **Name** Geben Sie QuickStatus, navigieren Sie zum Speicherort, in dem Sie die app zu speichern, und wählen Sie dann **OK**möchten.
    
   **Abbildung 1. Erstellen einer Project Server-app in Visual Studio**

   ![Erstellen einer Project Server-app in Visual Studio] (media/pj15_CreateStatusingApp_NewProject.gif "Erstellen einer Project Server-app in Visual Studio")
  
4. Füllen Sie im Dialogfeld **neue app für SharePoint** die nachfolgend beschriebenen drei Felder aus: 
    
   - Geben Sie den Namen, den Sie die app in Project Web App anzeigen möchten, klicken Sie im oberen Textfeld. Geben Sie zum Beispiel schnell Status aktualisieren.
    
   - Geben Sie für die Website für das debugging verwendet werden soll die URL der Project Web App-Instanz. Geben Sie zum Beispiel `https://ServerName/ProjectServerName` (ersetzen Sie _ServerName_ und _ProjectServerName_ durch eigene Werte), und klicken Sie auf **Überprüfen**. Wenn alles gut geht, zeigt Visual Studio **Verbindung wurde erfolgreich hergestellt**. Wenn Sie eine Fehlermeldung erhalten, stellen Sie sicher, dass die Project Web App-URL korrekt ist und der Project Server-Computer für app-Isolation und Sideloading von apps konfiguriert ist. Weitere Informationen finden Sie im Abschnitt [Voraussetzungen für das Erstellen einer Apps für Project Server 2013](#pj15_StatusingApp_Prerequisites) . 
    
   - Wählen Sie in der Dropdownliste **Wie soll Ihre app für SharePoint gehostet** **SharePoint gehostet**.
    
   > [!CAUTION]
   > Wenn Sie versehentlich von der standardmäßige **vom Anbieter gehosteten** Projekttyp auswählen, erstellt Visual Studio zwei Projekte in der Lösung: ein **QuickStatus** -Projekt und ein **QuickStatusWeb** -Projekt. Wenn Sie zwei Projekte angezeigt wird, dieser Lösung löschen und erneut starten. 
  
5. Wählen Sie **OK** zum Erstellen der **QuickStatus** -Lösung, die **QuickStatus** -Projekt und die Standard-Dateien. 
    
6. Öffnen Sie die Manifest-Designer-Ansicht (beispielsweise Doppelklicken auf die Datei AppManifest.xml-Datei). Auf der Registerkarte **Allgemein** sollte das Textfeld **Titel** den Namen der app anzeigen, den Sie in Schritt 4 eingegeben haben. Wählen Sie die Registerkarte **Berechtigungen** die folgenden berechtigungsanforderungen für die app hinzufügen (siehe Abbildung 2): 
    
   - Wählen Sie in der ersten Zeile der **berechtigungsanforderungen** -Liste in der Spalte **Bereich** **Zeitberichte** in der Dropdown-Liste. Wählen Sie in der Spalte **Berechtigung** **SubmitStatus**.
    
   - Hinzufügen einer Zeile, wobei der **Bereich** umfasst **Mehrere Projekte** und die **Berechtigung** **Lesen**.
    
   **Abbildung 2. Festlegen des berechtigungsumfangs für eine statuserfassungs-app**

   ![Festlegen des berechtigungsumfangs für eine statuserfassungs-app] (media/pj15_CreateStatusingApp_PermissionScope.gif "Festlegen des berechtigungsumfangs für eine statuserfassungs-app")
  
Die **QuickStatus** -app kann ein Project Web App-Benutzer Zuordnungen für diesen Benutzer aus mehreren Projekten lesen, ändern die Zuordnung prozentual abgeschlossen und die Aktualisierung senden. Die anderen berechtigungsanforderungsbereiche in der Dropdown-Liste in Abbildung 2 dargestellt sind nicht erforderlich für diese app. Die berechtigungsanforderungsbereiche sind die Berechtigungen, die die app im Auftrag des Benutzers anfordert. Wenn der Benutzer nicht über diese Berechtigungen in Project Web App verfügt, wird die app nicht ausgeführt. Eine app kann über mehrere berechtigungsanforderungsbereiche, einschließlich derer, für andere SharePoint-Berechtigungen, jedoch sollte nur das Minimum für die app-Funktionalität. Dies sind die berechtigungsanforderungsbereiche, die im Zusammenhang mit Project Server: 

- **Enterprise-Ressourcen**: Berechtigungen für Ressourcen-Manager, zum Lesen oder Schreiben von Informationen über andere Project Web App-Benutzer.
    
- **Mehrere Projekte**: Lese- oder Schreibzugriff mehr als ein Projekt, in dem der Benutzer die angeforderten Berechtigungen verfügt.
    
- **Project Server**: bewirkt, dass die app-Benutzer benötigen Administratorberechtigungen für Project Web App.
    
- **Reporting**: Lesen Sie den **ProjectData** OData-Dienst für Project Web App (erfordert nur anmelden Berechtigung für Project Web App). 
    
- **Einzelnes Projekt**: Lese- oder Schreibzugriff auf ein Projekt, in dem der Benutzer die angeforderten Berechtigungen verfügt.
    
- **Statusing**: Updates für den Status der Zuordnungen, wie Zeiten gearbeitet, Prozent abgeschlossen und neue Zuordnungen zu übermitteln.
    
- **Workflow**: Wenn der Benutzer die Berechtigung zum Ausführen von Project Server-Workflows verfügt, klicken Sie dann die app ausgeführt wird, mit erhöhten Berechtigungen für den Workflow.
    
Weitere Informationen zu berechtigungsanforderungsbereiche für Project Server 2013 finden Sie im Abschnitt *Project-apps* in [Updates für Entwickler in Project 2013](updates-for-developers-in-project-2013.md) und [App-Berechtigungen in SharePoint 2013](http://msdn.microsoft.com/library/fp142383.aspx).


<a name="pj15_StatusingApp_HTML"> </a>

### <a name="creating-the-html-content-for-the-quickstatus-app"></a>Erstellen von HTML-Inhalten für die QuickStatus-app

Bevor Sie beginnen, Codieren des HTML-Inhalts, Entwerfen der Benutzeroberfläche und die Benutzeroberfläche für die QuickStatus-app (Abbildung 3 zeigt ein Beispiel für die fertige Seite). Ein Entwurf kann auch einen Überblick über die JavaScript-Funktionen enthalten, die mit den HTML-Code interagieren. Allgemeine Informationen finden Sie unter [UX-Design für apps in SharePoint 2013](http://msdn.microsoft.com/library/fp179934.aspx).
  
**Abbildung 3. Design der QuickStatus-app-Seite**

![Design der QuickStatus-app-Seite] (media/pj15_CreateStatusingApp_AfterRefresh.gif "Design der QuickStatus-app-Seite")
  
Die app wird der Anzeigename im oberen Bereich, der der Wert des **Title** -Elements in der Datei AppManifest.xml ist. 
  
Standardmäßig wird die Seite HTML5 verwendet. Es folgen die standardmäßigen HTML-Elemente für die Benutzeroberfläche Hauptobjekte, die die **QuickStatus** -app im Textkörper der Seite enthält: 
  
- Ein **Form** -Element enthält alle anderen Elemente der Benutzeroberfläche. 
    
- Ein Element **Feldgruppe** erstellt einen Container und einen Rahmen für die Tabelle der Zuordnungen. das untergeordnete **Legend** -Element enthält eine Beschriftung für den Container. 
    
- Ein **Table** -Element enthält eine Beschriftung und nur eine Kopfzeile. JavaScript-Funktionen ändern Sie die Tabellenüberschrift und Zeilen für die Zuordnungen hinzufügen. 
    
   > [!NOTE]
   > Zum paging und Sortierung auf einfache Weise hinzufügen verwenden eine app Produktion ein kommerziellen jQuery-basierten Rastersteuerelements anstelle einer Tabelle wahrscheinlich. 
  
   Die Tabelle enthält Spalten für den Projektnamen, Vorgangsname mit einem Kontrollkästchen, aktuelle Arbeit, Prozent abgeschlossen, verbleibende Arbeit und den Endtermin für der Zuordnung. JavaScript-Funktionen erstellen das Kontrollkästchen und der Texteingabefeld für den Prozentsatz der einzelnen Aufgaben abgeschlossen.
    
- Ein **input** -Element für ein Textfeld legt % abgeschlossen für alle ausgewählten Zuordnungen fest. 
    
- Ein **Button** -Element sendet der Status geändert wird. 
    
- Ein **Button** -Element wird die Seite aktualisiert. 
    
- Ein **Button** -Element die app beendet und auf der Seite Vorgänge in Project Web App zurückgegeben. 
    
Die unteren Text-Feld und die Schaltfläche Elemente sind in **Div** -Elemente, sodass CSS auf einfache Weise die Position und die Darstellung der UI-Objekte verwalten können. Eine JavaScript-Funktion hinzugefügt einen Absatz am unteren Rand der Seite, die Ergebnisse für den Erfolg enthält, oder das Fehlschlagen des Updates Status. 
  
### <a name="procedure-2-to-create-the-html-content"></a>Schritt 2. Den HTML-Code Inhalt erstellen

1. Öffnen Sie in Visual Studio die Datei "default.aspx".
    
   Die Datei enthält zwei **Asp: Content** Elemente: das Element mit der `ContentPlaceHolderID="PlaceHolderAdditionalPageHead"` -Attribut innerhalb der Seitenkopf und dem Element hinzugefügt wird die `ContentPlaceHolderID="PlaceHolderMain"` Attribut wird innerhalb der Seite **Body** -Element eingefügt. 
    
2. In der `<asp:Content ContentPlaceHolderID="PlaceHolderAdditionalPageHead" runat="server">` für die Kopfzeile der Seite steuern, fügen Sie einen Verweis auf die Datei PS.js auf dem Project Server-Computer. Zum Testen und Debuggen, können Sie PS.debug.js verwenden. 
    
   ```HTML
     <script type="text/javascript" src="/_layouts/15/ps.debug.js"></script>
   ```

   Die app-Infrastruktur verwendet die `/_layouts/15/` virtuellen Verzeichnisses für die SharePoint-Website in IIS. Ist die physische Datei `%ProgramFiles%\Common Files\Microsoft Shared\Web Server Extensions\15\TEMPLATE\LAYOUTS\PS.debug.js`.
    
   > [!NOTE]
   > Entfernen Sie vor der Bereitstellung der app für den Produktiveinsatz `.debug` aus der Skriptverweise zum Verbessern der Leistung. 
  
3. In der `<asp:Content ContentPlaceHolderID="PlaceHolderMain" runat="server">` für den Textkörper der Seite steuern, löschen das generierten **Div** -Element, und fügen Sie den HTML-Code für die UI-Objekte. Das **Table** -Element enthält nur eine Kopfzeile. Die **Vorgangsname** Spalte enthält ein Kontrollkästchen Eingabesteuerelement. Text der **Caption** -Elements wird durch den **OnGetUserNameSuccess** Rückruf für die **GetUserInfo** -Funktion in der Datei App.js ersetzt. 
    
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

4. Fügen Sie in der Datei "App.CSS" CSS-Code für die Position und die Darstellung der Benutzeroberflächenelemente. Der vollständige CSS-Code der **QuickStatus** -app finden Sie im [Beispielcode für die QuickStatus-app](#pj15_StatusingApp_Example) -Abschnitt. 
    
Schritt 3 fügt die JavaScript-Funktionen, um die Zuordnungen lesen und Erstellen von Zeilen der Tabelle und zu ändern und aktualisieren die Zuordnung prozentual abgeschlossen. Die tatsächlichen Schritte werden bei der Entwicklung von einer app mehr iterative Alternativ erstellen Sie einige der HTML-Code, hinzufügen und Testen von verwandten Formatvorlagen und JavaScript-Funktionen, ändern oder Hinzufügen weiterer HTML-Code und wiederholen Sie dieses Verfahren.

<a name="pj15_StatusingApp_JavaScript"> </a>

### <a name="creating-the-javascript-functions-for-the-quickstatus-app"></a>Erstellen die JavaScript-Funktionen für die QuickStatus-app

Visual Studio-Vorlage für eine SharePoint-app umfasst die App.js-Datei, die Code für die Initialisierung enthält, die im Kontext der SharePoint-Client ruft und veranschaulicht grundlegende abrufen und Festlegen von Aktionen für die appseite. Der JavaScript-Namespace für die SharePoint-Client-seitigen SP.js Bibliothek ist **SP**. Da eine Project Server-app die PS.js-Bibliothek verwendet, wird die app **PS** -Namespace für den Clientkontext abzurufen und den Zugriff des JSOM für Project Server. 
  
Die folgenden: JavaScript-Funktionen in der **QuickStatus** -app 
  
- Der Dokument **bereit** -Ereignishandler ausgeführt, wenn das Dokumentobjektmodell (DOM) instanziiert wird. Der **bereit** Ereignishandler führt die folgenden vier Schritte aus: 
    
    1. Initialisiert die **ProjContext** globale Variable mit dem Clientkontext für die Project Server-JSOM und die globale Variable **PwaWeb** . 
        
    2. Ruft die **GetUserInfo** -Funktion, um die **ProjUser** globale Variable zu initialisieren. 
        
    3. Ruft die **GetAssignments** -Funktion, welche ruft Zuordnungsdaten für den Benutzer angegeben. 
        
    4. Bindet klicken Sie auf Ereignishandler, um das Kontrollkästchen Kopfzeile Tabelle und die Kontrollkästchen in jeder Zeile der Tabelle. Die Click-Ereignishandler verwalten das Attribut **checked** Kontrollkästchen, wenn der Benutzer aktiviert oder deaktiviert die Kontrollkästchen in der Tabelle alle. 
    
- Wenn die Funktion **GetAssignments** erfolgreich ist, ruft es die **OnGetAssignmentsSuccess** -Funktion. Dass die Funktion eine Zeile in der Tabelle für jede Zuweisung fügt initialisiert die HTML-Steuerelemente in jeder Zeile, und klicken Sie dann die unteren Schaltflächeneigenschaften. 
    
- Der **OnClick** -Ereignishandler für die Schaltfläche **Aktualisieren** Ruft die **UpdateAssignments** -Funktion. Zu jeder ausgewählten Zuordnung ist, dass die Funktion dient zum Abrufen des Prozentwertes angewendet. Wenn das Feld Prozent abgeschlossen leer ist, die Funktion ruft ab oder den Prozentsatz der einzelnen ausgewählten Zuordnung abgeschlossen in der Tabelle. Die Funktion **UpdateAssignments** klicken Sie dann speichert und sendet die Statusupdates und schreibt eine Nachricht zu den Ergebnissen am unteren Rand der Seite. 
    
### <a name="procedure-3-to-create-the-javascript-functions"></a>Schritt 3. Erstellen Sie die JavaScript-Funktionen

1. Klicken Sie in Visual Studio öffnen Sie die Datei App.js, und löschen Sie alle Inhalte in der Datei.
    
2. Fügen Sie die globalen Variablen und der Dokument-Ereignishandler **bereit** . Das **Document** -Objekt erfolgt über eine jQuery-Funktion. 
    
   Click-Ereignishandler für das Kontrollkästchen Kopfzeile Tabelle wird die Kontrollkästchen Zeile des aktivierten Zustands. Alle Kontrollkästchen der Zeile ausgewählt sind oder alle deaktiviert sind, wird Click-Ereignishandler für die Kontrollkästchen Zeile des aktivierten Zustands das Kontrollkästchen Kopfzeile. Die Click-Ereignishandler werden auch die Ergebnisse Nachricht am unteren Rand der Seite, um eine leere Zeichenfolge festgelegt.
    
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

3. Fügen Sie die **GetUserInfo** -Funktion, die **OnGetUserNameSuccess** aufruft, wenn die Abfrage erfolgreich ist. Die Funktion **OnGetUserNameSuccess** ersetzt den Inhalt des Absatzes **Beschriftung** durch eine Tabellenüberschrift, die den Benutzernamen enthält. 
    
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

4. Fügen Sie die **GetAssignments** -Funktion, die **OnGetAssignmentsSuccess** aufruft (siehe Schritt 5), wenn die Zuordnung Abfrage erfolgreich ist. Die Option **einbeziehen** beschränkt die Abfrage aus, um nur die angegebenen Felder zurückgeben. 
    
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

5. Fügen Sie die **OnGetAssignmentsSuccess** -Funktion, die in der Tabelle eine Zeile für jede Zuweisung hinzufügt. Die Variable **PrevProjName** wird verwendet, um zu bestimmen, ob eine Zeile für ein anderes Projekt ist. In diesem Fall wird der Projektnamen fett dargestellt; Wenn dies nicht der Fall ist, wird der Projektname ist eine leere Zeichenfolge festgelegt. 
    
   > [!NOTE]
   > Die JSOM enthält keinen **TimeSpan** -Eigenschaften, die das CSOM, wie beispielsweise **ActualWorkTimeSpan enthält**. Stattdessen verwendet die JSOM Eigenschaften für die Anzahl der Millisekunden, wie die folgenden [ StatusAssignment.actualWorkMilliseconds](http://msdn.microsoft.com/library/736bce1e-f734-0efe-6c5f-e0e891ab00ef%28Office.15%29.aspx) Eigenschaft. Die Methode zum Abrufen dieser Eigenschaft ist **abrufen\_ActualWorkMilliseconds**, die einen ganzzahligen Wert zurückgibt. > Die **Get_actualWork** -Methode gibt eine Zeichenfolge wie "3 h" zurück. Sie können einen der Werte in der **QuickStatus** -app verwenden, jedoch anders angezeigt. Die Zuordnungen Abfrage enthält beide Eigenschaften, damit Sie den Wert während des Debuggens testen können. Wenn Sie die Variable **ActualWork** entfernen, können Sie auch die **ActualWork** -Eigenschaft in der Abfrage Zuordnungen entfernen. 
  
   Schließlich die Funktion **OnGetAssignmentsSuccess** initialisiert die Schaltfläche **Aktualisieren** , und die Schaltfläche **Aktualisieren** mit click-Ereignishandler. Der Textwert der Schaltfläche **Aktualisieren** kann auch in der HTML-Code festgelegt werden. 
    
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

6. Hinzufügen der **UpdateAssignments** klicken Sie auf Ereignishandler für die Schaltfläche **Aktualisieren** . Wenn der Benutzer einen Wert für prozentuale Fertigstellung eines Vorgangs ändert oder einen Wert in das Textfeld **PercentComplete fügt** , kann der Wert in verschiedenen Formaten wie "60", "60 %" oder "60 %" eingegeben werden. Die **GetNumericValue** -Methode gibt den numerischen Wert des eingegebenen Texts. 
    
   > [!NOTE]
   > Verwenden Sie eine app, die für die Produktion entwickelt wurde, Eingabewerte für numerische Informationen sollte Feld Validierung und fehlerüberprüfung zusätzliche enthalten. 
  
   Das Beispiel **UpdateAssignments** umfasst einige grundlegende fehlerüberprüfung und zeigt Informationen in der **Nachricht** Absatz am unteren Rand der Seite – Grün, wenn die Update-Abfrage erfolgreich ist und Rot liegt ein Eingabefehler oder die Update-Abfrage ist nicht erfolgreich. 
    
   Bevor Sie die **SubmitAllStatusUpdates** -Methode verwenden, muss die app die Updates auf dem Server Speichern mithilfe der folgenden ** StatusAssignmentCollection.update** Methode. 
    
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

7. Fügen Sie die **ExitToPwa** -Funktion, die dem **SPHostUrl** Abfragezeichenfolgen-Parameter für die URL der Hostwebsite Project Web App verwendet. Um wieder auf der Seite Aufgaben zu navigieren, append `"/Tasks.aspx"` an die URL. Beispielsweise würde die Variable **SpHostUrl** festgelegt werden, auf `https://ServerName/ProjectServerName/Tasks.aspx`.
    
   Die Funktion **GetQueryStringParameter** teilt die URL der **QuickStatus** -Seite, um extrahieren und den angegebenen Parameter in der URL-Optionen zurückgegeben. Es folgt ein Beispiel für das Dokument **. URL** Wert für die **QuickStatus** -Dokument (alle in einer einzigen Zeile): 
    
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

   Für die vorherige URL, die **GetQueryStringParameter** -Funktion gibt den Zeichenfolgenwert **SPHostUrl** Abfrage `https://ServerName/pwa`. 
    
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

Wenn Sie die **QuickStatus** -app zu diesem Zeitpunkt veröffentlichen und Hinzufügen der Kontaktobjekte zu Project Web App, die app von der Seite Websiteinhalte ausgeführt werden kann, aber es ist nicht auf einfache Weise für Benutzer verfügbar. Mit denen Benutzer suchen und die app ausführen, können Sie eine Schaltfläche auf dem Menüband auf der Seite Aufgaben dafür hinzufügen. Schritt 4 zeigt, wie eine benutzerdefinierte Aktion hinzufügen. 

<a name="pj15_StatusingApp_ribbon"> </a>

### <a name="adding-a-ribbon-custom-action"></a>Hinzufügen einer benutzerdefinierten Menübandaktion

Menüband-Registerkarten, Gruppen und Steuerelemente für Project Web App werden angegeben, in der Datei pwaribbon.xml, in dem installiert ist die `[Program Files]\Common Files\Microsoft Shared\Web Server Extensions\15\TEMPLATE\FEATURES\PWARibbon\listtemplates` Verzeichnis auf dem Computer mit Project Server. Der Project 2013-SDK-Download enthält eine Kopie der pwaribbon.xml Design benutzerdefinierte Aktionen für die Project Web App-Multifunktionsleiste erleichtern. 
  
Project Web App verwendet andere Multifunktionsleiste Definitionen für die Seite Aufgaben, je nachdem, ob die Project Web App-Instanz einfacher Eingabemodus verwendet, die Benutzer Werte für sowohl die Arbeitszeittabellen und Vorgangsstatus eingeben können. Wenn Sie über Administratorberechtigungen für Project Web App verfügen, um den Eintrag Modus ermitteln wählen Sie **PWA-Einstellungen** in einem Dropdown-Einstellungsmenü auf der oberen rechten Ecke der Seite. Wählen Sie **Einstellungen und Standardwerte in der**auf der Seite PWA-Einstellungen, und betrachten Sie dann das Kontrollkästchen **Einfacher Eingabemodus** am unteren Rand der Seite. 
  
Wenn einfacher Eingabemodus deaktiviert ist, wird auf das Menüband auf der Seite Aufgaben nach der Region Meine Arbeit in pwaribbon.xml definiert: 
  
```XML
   <!-- REGION My Work Ribbon-->
   <CustomAction
      Id="Ribbon.ContextualTabs.MyWork"
      . . .
```

Wenn einfacher Eingabemodus aktiviert ist, wird das Menüband Aufgaben Seite durch die Region gebunden-Modus in pwaribbon.xml definiert: 
  
```XML
   <!-- REGION Tied Mode Ribbon-->
   <CustomAction
      Id="Ribbon.ContextualTabs.TiedMode"
      . . .
```

Obwohl die Gruppen und Steuerelementen in jeder Region ähnlich aussehen, kann ein Steuerelement für die verknüpften Modus eine andere Funktion als selben Steuerelement für den Modus nicht gebunden aufrufen. Schritt 4 zeigt, wie ein Button-Steuerelement für die **QuickStatus** -app hinzufügen, wenn einfacher Eingabemodus deaktiviert ist (das Kontrollkästchen **Einfacher Eingabemodus** ist klar). 
  
> [!NOTE]
> Allgemeine Informationen zum Hinzufügen von benutzerdefinierten Aktionen auf ein Menüband oder ein Menü in einer SharePoint-Anwendung finden Sie unter [Erstellen benutzerdefinierter Aktionen zur Bereitstellung mit apps für SharePoint](http://msdn.microsoft.com/en-us/library/jj163954.aspx). 
  
### <a name="procedure-4-to-add-a-ribbon-custom-action-to-the-tasks-page"></a>Schritt 4. So fügen Sie eine benutzerdefinierte Aktion auf der Seite Vorgänge hinzu

1. Überprüfen Sie auf das Menüband auf der Seite Aufgaben in Project Web App. Wählen Sie die Registerkarte **Vorgänge** auf dem Menüband und Planen Sie, wie es zu ändern. Es gibt sieben Gruppen, wie **Submit**, **Aufgaben**und **Zeitraum**an. Die Gruppe **Senden** verfügt über zwei Steuerelemente, die eine Schaltfläche **Speichern** und ein Dropdownmenü **Status senden** . Sie können ein Steuerelement an einer beliebigen Stelle in einer Gruppe hinzufügen, fügen eine Gruppe mit einem neuen Steuerelement an einer beliebigen Position auf der Registerkarte **TASKS** oder Hinzufügen einer anderen Registerkarte für Menüband, die benutzerdefinierte Gruppen und Steuerelemente verfügt. In diesem Beispiel fügen wir der Gruppe **Senden** , wobei die Schaltfläche für die URL der **QuickStatus** -app Ruft die eine dritte Schaltfläche hinzu. 
    
2. Klicken Sie im **Projektmappen-Explorer** in Visual Studio mit der rechten Maustaste in des **QuickStatus** -Projekts, und klicken Sie dann ein neues Element hinzufügen. Wählen Sie im Dialogfeld **Neues Element hinzufügen** die **Benutzerdefinierte Menübandaktion** (siehe Abbildung 4). Angenommen, nennen Sie die benutzerdefinierte Aktion RibbonQuickStatusAction, und wählen Sie dann **Hinzufügen**.
    
   **Abbildung 4. Hinzufügen einer benutzerdefinierten Menübandaktion**

   ![Hinzufügen einer benutzerdefinierten Menübandaktion] (media/pj15_CreateStatusingApp_AddRibbonCustomAction.gif "Hinzufügen einer benutzerdefinierten Menübandaktion")
  
3. Lassen Sie auf der ersten Seite des Assistenten **Für Menüband benutzerdefinierte Aktion erstellen** , die **Host-Web** -Option ausgewählt, wählen Sie **keine** aus in der Dropdown-Liste für den Bereich der benutzerdefinierten Aktion und wählen Sie dann auf **Weiter** (siehe Abbildung 5). Die Elemente in der Dropdown-Listen sind relevant für SharePoint, nicht für Project Server. Wir ersetzt die meisten der generierten XML-Code für die benutzerdefinierte Aktion, damit sie auf Project Server angewendet wird. 
    
   **Abbildung 5. Angeben von Eigenschaften für die benutzerdefinierte Menübandaktion**

   ![Angeben von Eigenschaften für die benutzerdefinierte Menübandaktion] (media/pj15_CreateStatusingApp_RibbonCustomAction2.gif "Angeben von Eigenschaften für die benutzerdefinierte Menübandaktion")
  
4. Lassen Sie auf der nächsten Seite des Assistenten für **Benutzerdefinierte Aktion für Menüband erstellen** , die Standardwerte für die Einstellungen, und wählen Sie dann auf **Fertig stellen** (siehe Abbildung 6). Visual Studio erstellt den **RibbonQuickStatusAction** -Ordner, der eine Elements.xml-Datei enthält. 
    
   **Abbildung 6. Angeben der Einstellungen für ein Button-Steuerelement**

   ![Angeben der Einstellungen für ein Button-Steuerelement] (media/pj15_CreateStatusingApp_RibbonCustomAction3.gif "Angeben der Einstellungen für ein Button-Steuerelement")
  
5. Ändern Sie den generierten Standardcode in der Datei Elements.xml für die benutzerdefinierte Menübandaktion. Es folgt der Standard-XML-Code:
    
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

   1. Löschen Sie im **CustomAction** -Elements **Sequence** -Attribut und das **Title** -Attribut. 
    
   2. Um der Gruppe **Senden** ein Steuerelement hinzuzufügen, suchen Sie nach der ersten Gruppe in der `Ribbon.ContextualTabs.MyWork.Home.Groups` Auflistung in der Datei pwaribbon.xml, das das Element, beginnt, `<Group Id="Ribbon.ContextualTabs.MyWork.Home.Page" Command="PageGroup" Sequence="10" Title="$Resources:pwafeatures,PAGE_PDP_CM_SUBMIT"`. Der folgende Code zeigt das richtige **Location** -Attribut des **CommandUIDefinition** -Element, um der Gruppe **Senden** ein untergeordnetes Steuerelement hinzugefügt haben, in der Datei "Elements.xml": 
    
      ```XML
        <CommandUIDefinitions>
          <CommandUIDefinition Location="Ribbon.ContextualTabs.MyWork.Home.Page.Controls._children">
             . . .
          </CommandUIDefinition>
        </CommandUIDefinitions>
      ```

   3. Ändern Sie die Attributwerte des untergeordneten **Button** -Element wie folgt: 
    
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

       - Damit der Schaltfläche das dritte Steuerelement in der Gruppe, **Sequence** -Attribut kann eine beliebige Anzahl höher ist als entsprechen den `Sequence="20"` Wert des vorhandenen **Status senden** -Steuerelements (bei dem es sich um ein **FlyoutAnchor** -Element in pwaribbon.xml handelt). Standardmäßig werden die Zahlen Sequenz von Gruppen und Steuerelementen `10, 20, 30, …`, wodurch Elemente in intermediate Positionen eingefügt werden soll.
    
       - Das **Command** -Attribut gibt den Befehl zum Ausführen im **CommandUIHandler** -Element (Siehe den folgenden Schritt 5.d). Sie können den Namen des Befehls für den nächsten Entwickler vereinfachen vereinfachen. Beispielsweise `Command="Invoke_QuickStatus"` ist einfacher zu lesen als `Command="Invoke_RibbonQuickStatusActionButtonRequest"`.
    
       - Die Attribute von Bildern Geben Sie das Symbol 16 x 16 Pixeln und 32 x 32 Pixel Symbol für das Button-Steuerelement. In der Standarddatei "Elements.xml" `Image32by32="_layouts/15/images/placeholder32x32.png"` gibt eine orange Punkt. Extrahieren Sie Symbole aus der Zuordnung Bilddateien (ps16x16.png und ps32x32.png), die in installiert sind die `[Program Files]\Common Files\Microsoft Shared\Web Server Extensions\15\TEMPLATE\LAYOUTS\1033\IMAGES` Verzeichnis auf dem Computer mit Project Server. Das Symbol 32 x 32 Pixel ist beispielsweise in der zweiten Spalte der Symbole von links und die zehnte Zeile nach unten vom oberen Rand der Imagemap ps32x32.png (im oberen Bereich des Symbols wird nach dem Ende der neunte Zeile; 9 Zeilen X 32 Pixel/Zeile = 288 Pixel). 
    
       - Um für das Button-Steuerelement eine QuickInfo anzuzeigen, fügen Sie das Attribut **ToolTipTitle** und **ToolTipDescription** -Attribut hinzu. 
    
    4. Ändern Sie die Attribute des **CommandUIHandler** -Elements. Angenommen, stellen Sie sicher, dass das **Command** -Attribut den **Befehl** Attributwert für das **Button** -Element übereinstimmt. Für das Attribut **CommandAction** `~appWebUrl` ist ein Platzhalter für die URL der Webseite **QuickStatus** . Wenn die Menübandschaltfläche die **QuickStatus** -app aufruft, von wird das Token **{StandardTokens}** durch URL-Optionen ersetzt, die **SPHostUrl**, **SPLanguage**, **SPClientTag**, **SPProductNumber**und **SPAppWebUrl enthalten **.
    
        ```XML
            <CommandUIHandlers>
                <CommandUIHandler Command="Invoke_QuickStatus"
                                  CommandAction="~appWebUrl/Pages/Default.aspx?{StandardTokens}"/>
            </CommandUIHandlers>
        ```

6. Klicken Sie im **Projektmappen-Explorer**öffnen Sie den Designer **Feature1.feature** und verschieben Sie **RibbonQuickStatusAction** Element aus dem Bereich der **Elemente in der Lösung** in den Bereich der **Elemente in der Funktion** zu. Wenn Sie dann den **Package.package** -Designer zu öffnen, wird das **RibbonQuickStatusAction** -Element im Bereich **Elemente im Paket** . 
    
Beim Entwickeln der app und eine Menübandschaltfläche hinzufügen, Testen der app, normalerweise an und legen Sie Haltepunkte in der JavaScript-Code für das debugging. Beim Drücken Sie **F5** , um mit dem Debuggen beginnen, Visual Studio kompiliert die app, die Website, die in der **Website-URL** -Eigenschaft des Projekts **QuickStatus** angegeben ist, und zeigt eine Seite mit der Aufforderung, ob Sie die app vertrauen bereitgestellt. Wenn Sie fortfahren, und Sie dann die **QuickStatus** -app beenden, wird auf der Seite Vorgänge in Project Web App zurückgegeben. 

> [!NOTE]
> Abbildung 7 zeigt, dass die Schaltfläche **Schnelles Status** auf der Registerkarte **Vorgänge** des Menübands deaktiviert ist. Nach vielen Bereitstellungen mit Visual Studio debuggen, können benutzerdefinierte Menüband-Steuerelementen blockiert werden, wenn Sie weiterhin Debuggen oder die veröffentlichte Anwendung auf dem gleichen Testserver bereitstellen. Zum Aktivieren der Schaltfläche Löschen Sie des Elements **RibbonQuickStatusAction** in Visual Studio, und erstellen Sie eine neue Menübandaktion, die über einen anderen Namen und die ID verfügt. Wenn das Problem nicht, entfernen Sie die app aus der Project Web App-Testinstanz und dann neu erstellen der app mit einer anderen app-ID. 
  
**Abbildung 7. Anzeigen der QuickInfo der deaktivierten Schaltfläche schnell Status**

![Anzeigen der QuickInfo der deaktivierten Schaltfläche] (media/pj15_CreateStatusingApp_ButtonToolTipDisabled.gif "Anzeigen der QuickInfo der deaktivierten Schaltfläche")
  
Schritt 5 zeigt, wie bereitstellen und Installieren der **QuickStatus** -app. Schritt 6 zeigt einige zusätzliche Schritte in der app testen, nachdem Sie es installiert haben. 

<a name="pj15_StatusingApp_Deploying"> </a>

## <a name="deploying-the-quickstatus-app"></a>Bereitstellen der QuickStatus-app

Sie haben verschiedene Möglichkeiten für die Bereitstellung einer app auf einer SharePoint-Web-Anwendung wie Project Web App. Die Bereitstellung, die Sie verwenden, hängt davon, ob Sie die app mit einem privaten SharePoint-Katalog oder auf den öffentlichen Office Store veröffentlichen möchten, und gibt an, ob SharePoint installiert ist: lokal oder einer online-Instanz ist. Schritt 5 veranschaulicht, wie die **QuickStatus** -app für eine lokale Installation in einem privaten app-Katalog bereitzustellen. Weitere Informationen finden Sie unter [Installieren und Verwalten von apps für SharePoint 2013](http://technet.microsoft.com/library/fp161232.aspx) und [Veröffentlichen von apps für SharePoint](http://msdn.microsoft.com/library/jj164070.aspx)
  
> [!NOTE]
> Hinzufügen einer app zu einer SharePoint-Katalog erfordert Administratorberechtigungen für SharePoint. 
  
### <a name="procedure-5-to-deploy-the-quickstatus-app"></a>5-Prozedur. Zum Bereitstellen der QuickStatus-app

1. In Visual Studio speichern Sie alle Dateien, und klicken Sie dann mit der rechten Maustaste im **Projektmappen-Explorer** des Projekts **QuickStatus** und auf **Veröffentlichen**.
    
2. Da die **QuickStatus** -app in SharePoint gehostet ist, sind sehr wenige Optionen zum Veröffentlichen (siehe Abbildung 8). Wählen Sie im Dialogfeld **Veröffentlichen von apps für Office und SharePoint** **Fertig stellen**.
    
   **Abbildung 8. Veröffentlichen der QuickStatus-app**

   ![Mit dem Assistenten zum Veröffentlichen] (media/pj15_CreateStatusingApp_PublishWizard.gif "Mit dem Assistenten zum Veröffentlichen")
  
3. Kopieren Sie die Datei QuickStatus.app aus der `~\QuickStatus\bin\Debug\app.publish\1.0.0.0` Verzeichnis in einem geeigneten Verzeichnis auf dem lokalen Computer (oder auf dem SharePoint-Computer für eine lokale Installation). 
    
4. Wählen Sie in der SharePoint-Zentraladministration **Apps** in der Schnellstartleiste, und wählen Sie dann auf **App-Katalog verwalten**.
    
5. Wenn ein app-Katalog nicht vorhanden ist, erstellen Sie eine Websitesammlung für die app-Katalog gemäß Abschnitt *Konfigurieren der App-Katalogwebsite für eine Webanwendung* in [der App-Katalog in SharePoint 2013 verwalten](http://technet.microsoft.com/library/fp161234.aspx).
    
   Wenn ein app-Katalog vorhanden ist, navigieren Sie zu der Website-URL auf der Seite App-Katalog verwalten. In den folgenden Schritten wird das app-Katalogwebsite `http://ServerName/sites/TestApps`.
    
6. Wählen Sie auf der appseite-Katalog **Apps für SharePoint** in der Schnellstartleiste. Wählen Sie auf der SharePoint-Seite, auf der Registerkarte **Dateien** des Menübands, Apps für **Dokument hochladen**.
    
7. Klicken Sie im Dialogfeld **Hinzufügen eines Dokuments** nach der Datei QuickStatus.app suchen Sie, fügen Sie Kommentare für die Version und wählen Sie dann auf **OK**.
    
8. Wenn Sie eine app hinzufügen, können Sie auch lokale Informationen für die app-Beschreibung, Symbol und andere Informationen hinzufügen. Fügen Sie die Informationen, die Sie für die app in der SharePoint-Websitesammlung anzeigen möchten, klicken Sie im Dialogfeld **Apps für SharePoint - QuickStatus.app** . Fügen Sie beispielsweise die folgende Informationen ein: 
    
   1. **Kurze Beschreibung** dar: Typ Quick Status Test-app.
    
   2. Feld **Beschreibung** : Geben Sie Test-app abgeschlossenen Prozentsatz für Vorgänge in mehreren Projekten zu aktualisieren.
    
   3. **Symbol-URL** -Felder: ein Bild 96 x 96 Pixel, für das app-Symbol auf der Website-Objekten für die app-Katalog hinzufügen. Navigieren Sie beispielsweise zum `http://ServerName/sites/TestApps`, wählen Sie im Dropdown-Menü **Einstellungen** **auf Websiteinhalte** , wählen Sie **Website-Objekten**, und fügen Sie das Bild quickStatusApp.png. Mit der rechten Maustaste in des **QuickStatusApp** -Elements, wählen Sie **Eigenschaften**, und kopieren Sie im Dialogfeld **Eigenschaften** den Wert des **Felds Webadresse (URL)** . Kopieren Sie beispielsweise `http://ServerName/sites/TestApps/SiteAssets/QuickStatusApp.png`, und fügen Sie den Wert im Feld Adresse Web **Symbol-URL** . Geben Sie eine Beschreibung für das Symbol, beispielsweise (wie in Abbildung 9), geben Sie QuickStatus-app-Symbol. Testen Sie, dass die URL gültig ist.
    
      **Abbildung 9. Hinzufügen einer Symbol-URL für die QuickStatus-app**

      ![Festlegen von Eigenschaften in SharePoint für die app] (media/pj15_CreateStatusingApp_AddAppToSharePointSettings.gif "Festlegen von Eigenschaften in SharePoint für die app")
  
   4. Feld **Kategorie** : Wählen Sie eine vorhandene Kategorie aus, oder geben Sie Ihren eigenen Wert. Geben Sie zum Beispiel Zeitberichte.
    
      > [!NOTE]
      > Eine Kategorie mit dem Namen **Statusing** ist nur für Testzwecke. Eine typische Kategorie für Project Server-apps ist **Enterprise Project Management**. 
  
   5. **Den Namen des Herausgebers** dar: Geben Sie den Namen des Herausgebers. Geben Sie in diesem Beispiel Project-SDK.
    
   6. Feld **aktiviert** : Wenn Sie die app für Project Web App-Websiteadministratoren für die Installation sichtbar ist, aktivieren Sie das Kontrollkästchen **aktiviert** . 
    
   7. Zusätzliche Felder sind optional. Beispielsweise können Sie eine Support-URL und mehrere Hilfe Bilder für die app-Detailseite hinzufügen. In Abbildung 9 umfassen die **Bild-URL-1** -Felder die URL für ein Screenshot der app und eine Beschreibung des Screenshots. 
    
   8. Wählen Sie im Dialogfeld **Apps für SharePoint - QuickStatus.app** **Speichern**aus. In Abbildung 9 das **Schnelle Status Update** -Element in der Apps für SharePoint-Bibliothek zur Bearbeitung, ausgechecktes usw. der Registerkarte **Bearbeiten** im Dialogfeld Feld Menüband, würden Sie **Einchecken** bis zum Abschluss der auswählen (siehe Abbildung 10). 
    
      **Abbildung 10. Die QuickStatus-app wird die Apps für SharePoint-Bibliothek hinzugefügt.**

      ![Die QuickStatus-app wird SharePoint hinzugefügt] (media/pj15_CreateStatusingApp_AddAppToSharePoint.gif "Die QuickStatus-app wird SharePoint hinzugefügt")
  
9. Wählen Sie in Project Web App im im Dropdown-Menü **Einstellungen** **app hinzufügen**aus. Auf der Seite Ihre Apps in der Schnellstartleiste auswählen **Aus Ihrer Organisation**, und wählen Sie dann **App-Details** für die **Schnelle Statusbericht** app. Abbildung 11 zeigt die Detailseite mit der app-Symbol, Screenshot und andere Informationen, die Sie im vorherigen Schritt hinzugefügt haben. 
    
   **Abbildung 11. Verwenden der Detailseite für schnelles Status aktualisieren in Project Web App**

   ![Hinzufügen der QuickStatus-app zu Project Web App] (media/pj15_CreateStatusingApp_AddAppToPWA.gif "Hinzufügen der QuickStatus-app zu Project Web App")
  
10. Wählen Sie auf der Detailseite für schnelles Statusbericht **Hinzufügen**. Project Web App zeigt ein Dialogfeld, in der die Vorgänge, die die QuickStatus-app ausführen können aufgelistet (siehe Abbildung 12). Die Liste der Vorgänge wird von der **AppPermissionRequest** -Elemente in der Datei AppManifest.XML abgeleitet. 
    
    **Abbildung 12. Sicherstellen, dass Sie die app schnell Status vertrauen**

    ![Verifizieren der Vertrauensstellung für die QuickStatus-app] (media/pj15_CreateStatusingApp_AddAppToPWA2Trust.gif "Verifizieren der Vertrauensstellung für die QuickStatus-app")
  
11. Wählen Sie im Dialogfeld **Vertrauen Sie schnell Statusbericht** **Vertrauensstellung ihn**aus. Die app wird auf der Seite Project Web App-Websiteinhalt hinzugefügt (siehe Abbildung 13).
    
    **Abbildung 13. Anzeigen der app schnell Status auf der Seite Websiteinhalte**

    ![Anzeigen der QuickStatus-app in Websiteinhalten] (media/pj15_CreateStatusingApp_AddAppToPWA3.gif "Anzeigen der QuickStatus-app in Websiteinhalten")
  
Wählen Sie auf der Seite Websiteinhalte das Symbol **Quick Status aktualisieren** , um die app auszuführen.

> [!NOTE]
> Weitere Befehle, die Informationen über die app auf der Seite Websiteinhalte bereitstellen, wählen Sie die Region, die den Namen des **Quick Status Update** und den drei Punkten (...) enthält. Sie können überprüfen Sie die Seite Info für die app, die App-Details-Seite, die Informationen zu app-Fehler enthält, anzeigen, lesen Sie die Seite der app-Berechtigungen oder entfernen die app aus Project Web App. 
  
Auf der Seite Aufgaben in Project Web App (siehe Abbildung 14), auf dem Menüband auf die Schaltfläche **QuickStatus** aktiviert werden soll. Wenn die Schaltfläche **Schnelles Status** deaktiviert ist, versuchen Sie es in die Notiz für Abbildung 7 beschriebenen Aktionen. 

**Abbildung 14. Starten der QuickStatus-app auf der Registerkarte TASKS**

![Starten der QuickStatus-app auf der Registerkarte TASKS] (media/pj15_CreateStatusingApp_TasksRibbon.gif "Starten der QuickStatus-app auf der Registerkarte TASKS")
  
Schritt 6 zeigt einige Tests, mit der QuickStatus-app herzustellen.

<a name="pj15_StatusingApp_Testing"> </a>

## <a name="testing-the-quickstatus-app"></a>Testen der QuickStatus-app

Jeder Operation, die versuchen, ein Benutzer in der **QuickStatus** -app sollte in einer Testinstallation von Project Server vor der Bereitstellung von der app auf einem Produktionsserver oder auf einen produktionsmandanten von Project Online getestet werden soll. Eine Testinstallation können Sie ändern und Löschen von Zuordnungen für Benutzer ohne tatsächliche Projekte. Tests sollten auch mehrere Benutzer umfassen, die über verschiedene Sätze von Berechtigungen, beispielsweise Administrator, Projektmanager und Teammitglied verfügen. Umfassende Tests kann Änderungen, die in der app erfolgen soll aufdecken, die nicht offensichtlich während der Entwicklung des Tests wurden. Schritt 6 zeigt mehrere Tests für die **QuickStatus** -app, umfasst aber keine vollständige Reihe von Tests aus. 
  
### <a name="procedure-6-to-test-the-quickstatus-app"></a>Schritt 6. So testen Sie die QuickStatus-app

1. Führen Sie die **QuickStatus** -app, in dem der Benutzer hat keine Zuordnungen. Die app sollte eine blaue Nachricht am unteren Rand der Seite, beispielsweise **Benutzername hat keine Zuordnungen**angezeigt wird.
    
   Wählen Sie **Update**, und die Meldung Änderungen an eine grüne **Zuordnungen aktualisiert wurden**.
    
   > [!NOTE]
   > Das Verhalten der app sollte nur geändert werden, damit die Schaltfläche **Aktualisieren** deaktiviert ist, wenn es keine Aufgaben sind. 
  
2. Führen Sie die Anwendung, in denen der Benutzer hat mehrere Zuordnungen in mehreren verschiedenen Projekten und einige Aufgaben sind nicht vollständig. Beachten Sie die Darstellung der app und Aktionen Sie wie folgt (siehe Abbildung 15):
    
   1. Die Funktion **OnGetAssignmentsSuccess** erstellt eine Zeile in der Tabelle für jede Zuordnung für den aktuellen Benutzer. Der Namen des Projekts zeigt nur einmal fett, für die erste Zuordnung im jeweiligen Projekt. 
    
   2. Deaktivieren Sie das Kontrollkästchen in der Spaltenüberschrift **Vorgangsname** . Tabelle, klicken Sie auf Ereignis-Handler löscht alle die anderen Kontrollkästchen Felder in den Aufgabenzeilen. 
    
   3. Wählen Sie alle Tasks aus. Click-Ereignishandler wählt für jede Zeile bestimmt, ob alle Zeilen ausgewählt sind, und wenn dies der Fall ist, die Spaltenüberschrift **Vorgangsname** . 
    
   4. Deaktivieren Sie die Kontrollkästchen aller erneut, und wählen Sie dann eine Zuordnung, die verbleibende Arbeit zugewiesen wurde. Abbildung 15 zeigt beispielsweise dem oberen Vorgang T1 20 % verbleibende Arbeit abgeschlossen hat.
    
   5. Geben Sie in das Textfeld **Prozent abgeschlossen festlegen** 80 ein, und wählen Sie **Aktualisieren**. Eine grüne Nachricht, **Zuordnungen aktualisiert wurden**sollte den unteren Rand der Seite angezeigt werden.
    
      **Abbildung 15. Aktualisieren einer Zuweisung in der QuickStatus-app**

      ![Aktualisieren einer Zuweisung in der QuickStatus-app] (media/pj15_CreateStatusingApp_Testing1Update.gif "Aktualisieren einer Zuweisung in der QuickStatus-app")
  
3. Wählen Sie **Aktualisieren** (siehe Abbildung 16). Alle Aufgaben erneut aktiviert sind, und die obere Aufgabe veranschaulicht 80 % abgeschlossen. 
    
      **Abbildung 16. Aktualisieren Sie die Seite schnell Statusbericht**

      ![Aktualisieren der QuickStatus-Seite] (media/pj15_CreateStatusingApp_Testing2Refresh.gif "Aktualisieren der QuickStatus-Seite")
  
4. Deaktivieren Sie alle Kontrollkästchen, und wählen Sie dann aus einer anderen Aufgabe. Wählen Sie zum Beispiel **neue Aufgabe aus Project Web Access**. Lassen Sie das Feld **% abgeschlossen festgelegt** leer, löschen Sie alle Textabschnitte in der Spalte **% abgeschlossen** für den ausgewählten Vorgang und wählen Sie **Aktualisieren**. Da beide Textfelder leer sind, zeigt die app einen roten Fehler angezeigt (siehe Abbildung 17).
    
      **Abbildung 17. Testen der Fehlermeldung**

      ![Testen der Fehlermeldung] (media/pj15_CreateStatusingApp_Testing3Error.gif "Testen der Fehlermeldung")
  
5. Aktualisieren der vorherigen Aufgabe auf 80 % abgeschlossen, und wählen Sie dann auf **Beenden**. Die Funktion **ExitToPwa** ändert die Position des Browser-Fensters auf der Seite Vorgänge in der SharePoint-Host-Anwendung (d. h., ändert sich die URL in https://ServerName/pwa/Tasks.aspx). Abbildung 18 zeigt, dass die Aufgabe **T1** und die **neue Aufgabe aus Project Web Access** -Aufgabe 80 % abgeschlossen angezeigt. 
    
      **Abbildung 18. Überprüfen der Aufgaben in Project Web App aktualisiert werden**

      ![Überprüfen der aktualisierten Aufgaben in Project Web App] (media/pj15_CreateStatusingApp_TasksUpdatedInPWA.gif "Überprüfen der aktualisierten Aufgaben in Project Web App")
  
6. Bevor der aktualisierte Status in Project Professional 2013 angezeigt wird, müssen die Änderungen zur Genehmigung vorgelegt und von der Projektmanager genehmigt werden.
    
Testen, werden weitere Änderungen, die in der **QuickStatus** -app für verbesserte Nutzbarkeit hergestellt werden soll. Beispiel:

- Zusätzliche Fehler überprüft und Validierung von Text im Feld Werte sollte vorhanden sein. Derzeit kann ein Benutzer eingeben, ein nicht-numerische Wert oder einen negativen Wert für Prozent abgeschlossen ist, führt zu einer Fehlermeldung ungeeignete. Mit einem negativen Wert, wird die Fehlermeldung **Fehler beim Aktualisieren der Zuordnungen: PJClientCallableException: StatusingSetDataValueInvalid**.
    
- Die Fehlermeldung für leere Textfelder konnte das Projekt und die Aufgabe neben die Nummer der Tabellenzeile aufgelistet.
    
- Die Erfolgsmeldung an konnte eine Liste der Aufgaben aktualisiert enthalten. oder wenn die Funktion **UpdateAssignments** erfolgreich ist, konnte eine Seite Automatische Aktualisierung ausführen und aktualisierten Aufgaben oder Prozentsätze in eine andere Farbe und fett anzeigen. 
    
- Um eine sehr umfangreiche Tabelle zu vermeiden, sollten die Tabelle der Zuordnungen auf Aufgaben beschränkt werden, die weniger als 100 % abgeschlossen sind. Auch eine Option, um alle Vorgänge hinzufügen. Dieses Problem kann auch mithilfe eines Rasters jQuery-basierte anstelle einer Tabelle, wobei können Sie auf einfache Weise filtern und Raster implementieren gelöst werden paging.
    
- Da die **QuickStatus** -app nicht Status sendet, wäre das **Schnelle** Statussymbol auf der Registerkarte **Vorgänge** des Menübands mehr logisch nicht das erste Symbol in der Gruppe **Vorgänge** , sondern das letzte Symbol in der Gruppe **Senden** . 
    
- Da die **OnGetAssignmentsSuccess** -Funktion den Text der Schaltfläche **BtnSubmitUpdate** initialisiert, aber die Schaltfläche Textwerte werden in HTML initialisiert, wird die Seite in einem teilweise initialisierten Zustand während der **GetAssignments** beibehalten. Funktion ausgeführt wird. Schaltflächen auf der Seite scheint konsistenter, wenn die Textwerte in HTML initialisiert wurden. 
    
Vor allem sollte der Ansatz, den der **QuickStatus** -app verwendet, wobei Prozent geändert für Zuordnungen, abschließen überarbeitet werden in einer app Produktion. Weitere Informationen finden Sie im Abschnitt [Weitere Schritte](#pj15_StatusingApp_NextSteps) . 

<a name="pj15_StatusingApp_Example"> </a>

## <a name="example-code-for-the-quickstatus-app"></a>Beispielcode für die QuickStatus-app

### <a name="defaultaspx-file"></a>Datei "default.aspx"

Der folgende Code ist der `Pages\Default.aspx` Datei des Projekts **QuickStatus** : 
  
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

Der folgende Code ist der `Scripts\App.js` Datei des Projekts **QuickStatus** : 
  
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

### <a name="appcss-file"></a>Datei "App.CSS"

Der folgenden CSS-Code befindet sich in der `Content\App.css` Datei des Projekts **QuickStatus** : 
  
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

### <a name="elementsxml-file-for-the-ribbon"></a>Datei "Elements.xml" für das Menüband

Die folgende XML-Definition für die hinzugefügte Schaltfläche auf der Registerkarte **Aufgaben** auf dem Menüband befindet sich in der `RibbonQuickStatusAction\Elements.xml` Datei des Projekts **QuickStatus** : 
  
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

Nachfolgend sehen Sie das XML für das app-Manifest des **QuickStatus** -Projekts, das zwei berechtigungsanforderungsbereiche enthält, die zum Aktualisieren des app-Benutzers Status einer Aufgabe in mehreren Projekten erforderlich sind: 
  
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
        <AppPermissionRequest Scope="http://sharepoint/projectserver/statusing" Right="SubmitStatus" />
        <AppPermissionRequest Scope="http://sharepoint/projectserver/projects" Right="Read" />
    </AppPermissionRequests>
    </App>
```

<br/>

### <a name="appiconpng-file"></a>AppIcon.png-Datei

Die vollständige Visual Studio-Lösung für die **QuickStatus** -app umfasst eine benutzerdefinierte AppIcon.png-Datei. Die Lösung eingeschlossen werden in den Project 2013-SDK-Download. 

<a name="pj15_StatusingApp_NextSteps"> </a>

## <a name="next-steps"></a>Nächste Schritte

Die **QuickStatus** -app ist ein relativ einfaches Beispiel dafür, wie Sie apps zu schreiben, die auf Project Server 2013 und Project Online installiert werden kann. [Testen der QuickStatus-app](#pj15_StatusingApp_Testing) im Abschnitt enthält mehrere Verbesserungen, die für eine bessere Verwendbarkeit hergestellt werden können. Die **QuickStatus** -app verwendet JavaScript-Funktionen zum Status einer Aufgabe für Project Web App zu aktualisieren. Aber ändern die Zuordnung prozentual abgeschlossen ist keine empfohlene Project Management Vorgehensweise. Ein weiterer Ansatz wäre das tatsächliche Startdatum und die verbleibende Dauer der zugewiesenen Aufgaben zu aktualisieren. Eine Erläuterung der Probleme finden Sie unter [Update besser](http://www.mpug.com/articles/update-better) in den MPUG Newsletter an. 

<a name="pj15_StatusingApp_AdditionalResources"> </a>

## <a name="see-also"></a>Siehe auch

- [Project Server-Programmieraufgaben](project-programming-tasks.md)
- [SharePoint-Add-Ins](http://msdn.microsoft.com/library/jj163230.aspx)
- [Verwalten von vorgangsaktualisierungen in Project Web App](https://technet.microsoft.com/en-us/library/hh767481%28v=office.14%29.aspx)
- [Gewusst wie: Erstellen benutzerdefinierter Aktionen zur Bereitstellung mit Add-Ins für SharePoint](http://msdn.microsoft.com/library/jj163954.aspx)
    

