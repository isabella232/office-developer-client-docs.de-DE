---
title: Erstellen eines auf SharePoint gehosteten Project Server-Add-Ins
manager: lindalu
ms.date: 08/10/2016
ms.audience: Developer
localization_priority: Normal
ms.assetid: bb9c3c00-7121-41e1-9db3-75550d040ba8
description: Von den drei Arten von apps, die Sie für Project online erstellen können (automatisch gehostete, vom Anbieter gehostete und in SharePoint gehostete), ist die in SharePoint gehostete App am einfachsten zu erstellen und bereitzustellen.
ms.openlocfilehash: 9b3b41eda40a8419ad72f11bb474acf7acaf81e9
ms.sourcegitcommit: 31b0a7373ff74fe1d6383c30bc67d7675b73d283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/05/2020
ms.locfileid: "41773757"
---
# <a name="create-a-sharepoint-hosted-project-server-add-in"></a>Erstellen eines auf SharePoint gehosteten Project Server-Add-Ins

Von den drei Arten von apps, die Sie für Project online erstellen können (automatisch gehostete, vom Anbieter gehostete und in SharePoint gehostete), ist die in SharePoint gehostete App am einfachsten zu erstellen und bereitzustellen. Eine in SharePoint gehostete App erfordert keine OAuth-Authentifizierung und verwendet kein Azure oder erfordert die Wartung eines lokalen Standorts für vom Anbieter gehostete Ressourcen. Die **App für SharePoint 2013** Vorlage in Visual Studio ist ein praktisches Framework für die Entwicklung von apps, die im Office Store veröffentlicht und verkauft oder in einem privaten App-Katalog auf SharePoint bereitgestellt werden können. 
  
In Project ist Statusing ein Prozess, bei dem ein Teammitglied die Seite Vorgänge in Project Web App verwenden kann, um den Status einer zugewiesenen Aufgabe zu übermitteln, beispielsweise die Anzahl der Arbeitsstunden, die an jedem Tag in einer Woche für die Arbeit an der Aufgabe aufgewendet wurden. Der Zuordnungsbesitzer (in der Regel der Projektmanager) kann den Status genehmigen oder ablehnen. Wenn der Status genehmigt ist, berechnet Project den Zeitplan neu. In der **Quick Status** -App werden zugewiesene Vorgänge angezeigt, in denen der Benutzer den abgeschlossenen Prozentsatz der ausgewählten Zuweisungen schnell aktualisieren und den Status der Genehmigung übermitteln kann. Obwohl die Seite Aufgaben in Project Web App wesentlich mehr Funktionen aufweist, ist die **Quick Status** -App ein Beispiel, das eine vereinfachte Benutzeroberfläche bereitstellt. 
  
Die **Quick Status** -APP ist ein Beispiel für Entwickler; Sie ist nicht für die Verwendung in einer Produktionsumgebung vorgesehen. Der Hauptzweck besteht darin, ein Beispiel für die APP-Entwicklung für Project online zu zeigen, nicht um eine voll funktionsfähige Status-APP zu erstellen. Einen besseren Ansatz bei der Statusverwaltung finden Sie in der Empfehlung in den [nächsten Schritten](#pj15_StatusingApp_NextSteps).
  
Allgemeine Informationen zum Statusing finden Sie unter [Aufgabenfortschritt](https://support.office.com/article/Find-information-about-Project-Server-2013-8b08a414-15a7-4076-b2db-c90d0214ea7f?ui=en-US&rs=en-US&ad=US#BKMK_TaskProgress). Weitere Informationen zum Entwickeln von Add-Ins für SharePoint und Project Server finden Sie unter [SharePoint-Add-ins](https://msdn.microsoft.com/library/jj163230.aspx).

<a name="pj15_StatusingApp_Prerequisites"> </a>

## <a name="prerequisites-for-creating-an-app-for-project-server-2013"></a>Voraussetzungen für das Erstellen einer APP für Project Server 2013

Um relativ einfache apps zu entwickeln, die für Project Online oder für eine lokale Installation von Project Server 2013 bereitgestellt werden können, können Sie das Napa verwenden, das eine Online Entwicklungsumgebung bereitstellt. Für komplexere apps, das Ändern des Project Web App Menübands und das einfachere Debuggen während der Entwicklung können Sie Visual Studio 2012 oder Visual Studio 2013 verwenden. Bei einer lokalen Installation können Sie beispielsweise die Entwurfsdaten Tabellen für Änderungen in der Project Server-Datenbank manuell überprüfen. In diesem Artikel erfahren Sie, wie Sie die APP-Entwicklung mit Visual Studio durchführen.
  
Die Entwicklung von Project Server-apps mit Visual Studio erfordert Folgendes:
  
- Stellen Sie sicher, dass Sie die neuesten Service Packs und Windows-Updates auf dem lokalen Entwicklungscomputer installiert haben. Als Betriebssystem kann Windows 7, Windows 8, Windows Server 2008 oder Windows Server 2012 verwendet werden.
    
- Sie müssen über einen Computer verfügen, auf dem SharePoint Server 2013 und Project Server 2013 installiert ist, in dem der Computer für die APP-Isolierung und Sideloading von apps konfiguriert ist. Sideloading ermöglicht Visual Studio die vorübergehende Installation der APP für das Debugging. Sie können eine lokale Installation von SharePoint und Project Server verwenden. Weitere Informationen finden Sie unter [Einrichten einer lokalen Entwicklungsumgebung für Apps für SharePoint](https://msdn.microsoft.com/library/fp179923%28Office.15%29.aspx).
    
   > [!NOTE]
   > Konfigurieren Sie für eine lokale Installation eine isolierte App-Domäne *vor dem* Erstellen eines Unternehmens-App-Katalogs. 
  
- Der Entwicklungscomputer kann ein Remotecomputer sein, auf dem Office Developer Tools für Visual Studio 2012 installiert ist. Stellen Sie sicher, dass Sie die neueste Version installiert haben; Weitere Informationen finden Sie im Abschnitt *Tools* der [Downloads Apps für Office und SharePoint](https://msdn.microsoft.com/office/apps/fp123627.aspx).
    
- Stellen Sie sicher, dass im Browser auf die Project Web App Instanz zugegriffen werden kann, die Sie für die Entwicklung und das Testen verwenden.
    
Informationen zur Verwendung der Online Tools finden Sie unter [Einrichten einer Umgebung für die Entwicklung von Apps für SharePoint auf Office 365](https://msdn.microsoft.com/library/fp161179.aspx). Eine exemplarische Vorgehensweise zum Erstellen einer einfachen App für Project Server, die die Online Tools verwendet, finden Sie in der EPMSource-Blog Reihe unter [Erstellen Ihrer ersten Project Server-App](https://epmsource.com/2012/11/20/building-your-first-project-server-app-part-zerothe-introduction/).

<a name="pj15_StatusingApp_UsingVisualStudio"> </a>

## <a name="using-visual-studio-to-create-a-project-server-app"></a>Erstellen einer Project Server-App mithilfe Visual Studio

Office Developer Tools für Visual Studio 2012 enthält eine Vorlage für SharePoint-apps, die mit Project Server 2013 verwendet werden kann. Wenn Sie eine APP-Lösung erstellen, enthält die Lösung die folgenden Dateien für Ihren benutzerdefinierten Code:
  
- **AppManifest. XML** enthält Einstellungen für den APP-Titel, den Berechtigungs Anforderungsbereich und andere Eigenschaften. Prozedur 1 enthält Schritte zum Festlegen der Eigenschaften mithilfe des Manifest-Designers. 
    
- " **Default. aspx** " im Ordner "Pages" ist die Hauptseite der app. In Prozedur 2 wird das Hinzufügen von HTML5-Inhalten für die **Quick Status** -App gezeigt. 
    
- " **App. js** " im Ordner "Skripts" ist die primäre Datei für den benutzerdefinierten JavaScript-Code. In Prozedur 3 wird der JavaScript-Code für die **Quick Status** -App erläutert. 
    
   Wenn Sie kommerzielle Steuerelemente wie ein auf jQuery basierendes Raster oder eine Datumsauswahl hinzufügen, können Sie Verweise auf zusätzliche JavaScript-Dateien in der Datei "default. aspx" hinzufügen.
    
- " **App. CSS** " im Inhaltsordner ist die primäre Datei für benutzerdefinierte CSS3-Formatvorlagen. In Prozedur 2 und Prozedur 3 werden Informationen zu CSS-Formatvorlagen (Cascading Stylesheets) für die **Quick Status** -app hinzugefügt. Sie können Verweise auf zusätzliche CSS-Dateien in der Datei "default. aspx" hinzufügen. 
    
- **AppIcon. png** im Ordner Images ist das Symbol 96 x 96, das die APP im Office Store oder im App-Katalog anzeigt. 
    
Zum Ändern des Project Web App Menübands können Sie eine benutzerdefinierte menübandaktion hinzufügen. Der [Beispielcode für den Quick Status-App](#pj15_StatusingApp_Example) -Abschnitt enthält den vollständigen Code für die Dateien "default. aspx", "App. js", "App. CSS", "Elements. xml" und "AppManifest. xml". 
  
### <a name="procedure-1-to-create-an-app-project-in-visual-studio"></a>Prozedur 1. So erstellen Sie ein App-Projekt in Visual Studio

1. Führen Sie Visual Studio 2012 als Administrator aus, und wählen Sie dann auf der Start Seite **Neues Projekt** aus. 
    
2. Erweitern Sie im Dialogfeld **Neues Projekt** den Knoten **Vorlagen**, **Visual C#** und **Office/SharePoint** , und wählen Sie dann **apps**aus. Verwenden Sie die Standard **.NET Framework 4.5** in der Dropdownliste Ziel Framework oben im mittleren Bereich, und wählen Sie dann **App für SharePoint 2013** aus (siehe Abbildung 1). 
    
3. Geben Sie im Feld **Name den Namen** Quick Status ein, navigieren Sie zu dem Speicherort, an dem Sie die APP speichern möchten, und wählen Sie dann **OK**aus.
    
   **Abbildung 1. Erstellen einer Project Server-app in Visual Studio**

   ![Erstellen einer Project Server-App in Visual Studio](media/pj15_CreateStatusingApp_NewProject.gif "Erstellen einer Project Server-App in Visual Studio")
  
4. Geben Sie im Dialogfeld **neue APP für SharePoint** die folgenden drei Felder ein: 
    
   - Geben Sie in das Textfeld oben den Namen ein, den die app in Project Web App anzeigen soll. Geben Sie beispielsweise Quick Status Update ein.
    
   - Geben Sie die URL der Project Web App-Instanz ein, damit die Website für das Debugging verwendet werden kann. Geben `https://ServerName/ProjectServerName` Sie beispielsweise (Ersetzen von _Servername_ und _ProjectServerName_ durch eigene Werte) ein, und wählen Sie dann **validieren**aus. Wenn alles gut geht, zeigt Visual Studio die **Verbindung erfolgreich**. Wenn Sie eine Fehlermeldung erhalten, stellen Sie sicher, dass die Project Web App-URL richtig ist und dass der Project Server-Computer für die APP-Isolierung und Sideloading von apps konfiguriert ist. Weitere Informationen finden Sie unter [Voraussetzungen für das Erstellen einer APP für Project Server 2013](#pj15_StatusingApp_Prerequisites) Abschnitt. 
    
   - Wählen Sie in der Dropdownliste **wie soll Ihre APP für SharePoint** gehostet werden die Option **SharePoint-** Hosted aus.
    
   > [!CAUTION]
   > Wenn Sie den vom **Anbieter gehosteten** Standardprojekttyp versehentlich auswählen, erstellt Visual Studio zwei Projekte in der Projektmappe: ein **Quick Status** -Projekt und ein **QuickStatusWeb** -Projekt. Wenn zwei Projekte angezeigt werden, löschen Sie die Lösung, und starten Sie Sie erneut. 
  
5. Wählen Sie **OK** aus, um die **Quick Status** -Lösung, das **Quick Status** -Projekt und die Standarddateien zu erstellen. 
    
6. Öffnen Sie die Manifest-Designer-Ansicht (Doppelklicken Sie beispielsweise auf die Datei AppManifest. Xml). Auf der Registerkarte **Allgemein** sollte im Textfeld **Titel** der App-Name angezeigt werden, den Sie in Schritt 4 eingegeben haben. Wählen Sie die Registerkarte **Berechtigungen** aus, um die folgenden Berechtigungsanforderungen für die APP hinzuzufügen (siehe Abbildung 2): 
    
   - Wählen Sie in der ersten Zeile der Liste **Berechtigungsanforderungen** in der Spalte **Bereich** die Option **Statusing** in der Dropdownliste aus. Wählen Sie in der Spalte **Berechtigung** die Option **SubmitStatus**aus.
    
   - Fügen Sie eine Zeile hinzu, bei der der **Bereich** **mehrere Projekte** ist und die **Berechtigung** **gelesen**wird.
    
   **Abbildung 2. Festlegen des Berechtigungs Bereichs für eine Statusing-App**

   ![Festlegen des Berechtigungsumfangs für eine Statuserfassungs-App](media/pj15_CreateStatusingApp_PermissionScope.gif "Festlegen des Berechtigungsumfangs für eine Statuserfassungs-App")
  
Mit der **Quick Status** -App kann ein Project Web App-Benutzerzuweisungen für diesen Benutzer aus mehreren Projekten lesen, die Zuweisung "Prozent abgeschlossen" ändern und das Update übermitteln. Die anderen Berechtigungs Anforderungsbereiche, die in der Dropdownliste in Abbildung 2 angezeigt werden, sind für diese APP nicht erforderlich. Die Berechtigungs Anforderungsbereiche sind die Berechtigungen, die die APP im Namen des Benutzers anfordert. Wenn der Benutzer nicht über diese Berechtigungen in Project Web App verfügt, wird die APP nicht ausgeführt. Eine APP kann mehrere Berechtigungs Anforderungsbereiche haben, einschließlich derer für andere SharePoint-Berechtigungen, aber nur die für die APP-Funktionalität erforderlichen Mindestanforderungen haben. Im folgenden sind die Berechtigungs Anforderungsbereiche im Zusammenhang mit Project Server aufgeführt: 

- **Enterprise-Ressourcen**: Ressourcen-Manager-Berechtigungen zum Lesen oder Schreiben von Informationen zu anderen Project Web App Benutzern.
    
- **Mehrere Projekte**: Lesen oder schreiben in mehreren Projekten, bei denen der Benutzer über die erforderlichen Berechtigungen verfügt.
    
- **Project Server**: erfordert, dass der App-Benutzer über Administratorberechtigungen für Project Web App verfügt.
    
- **Berichterstellung**: Lesen Sie den **ProjectData** OData-Dienst für Project Web App (erfordert nur die Berechtigung Anmelden für Project Web App). 
    
- **Einzelnes Projekt**: Lesen oder schreiben in einem Projekt, in dem der Benutzer über die erforderlichen Berechtigungen verfügt.
    
- **Statusing**: Übermitteln von Updates für den Status von Zuordnungen, wie gearbeitete Zeiten, abgeschlossenen Prozentsatz und neue Zuordnungen.
    
- **Workflow**: Wenn der Benutzer über die Berechtigung zum Ausführen von Project Server-Workflows verfügt, wird die APP dann mit erhöhten Berechtigungen für den Workflow ausgeführt.
    
Weitere Informationen zu Berechtigungs Anforderungsbereichen für Project Server 2013 finden Sie im Abschnitt *Projekt apps* unter [Updates für Entwickler in Project 2013](updates-for-developers-in-project-2013.md) und [App-Berechtigungen in SharePoint 2013](https://msdn.microsoft.com/library/fp142383.aspx).


<a name="pj15_StatusingApp_HTML"> </a>

### <a name="creating-the-html-content-for-the-quickstatus-app"></a>Erstellen des HTML-Inhalts für die Quick Status-App

Bevor Sie mit dem Codieren des HTML-Inhalts beginnen, entwerfen Sie die Benutzeroberfläche und die Benutzererfahrung für die Quick Status-app (Abbildung 3 zeigt ein Beispiel für die abgeschlossene Seite). Ein Entwurf kann auch eine Übersicht über die JavaScript-Funktionen enthalten, die mit dem HTML-Code interagieren. Allgemeine Informationen finden Sie unter [UX-Design für apps in SharePoint 2013](https://msdn.microsoft.com/library/fp179934.aspx).
  
**Abbildung 3. Entwurf der Quick Status-App-Seite**

![Design der QuickStatus-App-Seite](media/pj15_CreateStatusingApp_AfterRefresh.gif "Design der QuickStatus-App-Seite")
  
Die APP zeigt den Anzeigenamen oben an, bei dem es sich um den Wert des **Title** -Elements in AppManifest. XML handelt. 
  
Standardmäßig verwendet die Seite HTML5. Im folgenden finden Sie die standardmäßigen HTML-Elemente für die wichtigsten UI-Objekte, die die **Quick Status** -App im Textkörper der Seite enthält: 
  
- Ein **Form** -Element enthält alle anderen Benutzeroberflächenelemente. 
    
- Ein **FIELDSET** -Element erstellt einen Container und einen Rahmen für die Zuordnungstabelle; das untergeordnete **Legend** -Element stellt eine Bezeichnung für den Container bereit. 
    
- Ein **Table** -Element enthält eine Beschriftung und nur eine Tabellenkopfzeile. JavaScript-Funktionen ändern die Tabellenüberschrift und fügen Zeilen für die Zuordnungen hinzu. 
    
   > [!NOTE]
   > Um einfach Paging und Sortieren hinzuzufügen, würde eine Produktions-App wahrscheinlich ein kommerzielles jQuery-basiertes Grid-Steuerelement anstelle einer Tabelle verwenden. 
  
   Die Tabelle enthält Spalten für den Projektnamen, den Vorgangsnamen mit einem Kontrollkästchen, die aktuelle Arbeit, den abgeschlossenen Prozentsatz, die verbleibende Arbeit und den Endtermin der Zuordnung. JavaScript-Funktionen erstellen Sie das Kontrollkästchen und das Texteingabefeld für den abgeschlossenen Prozentsatz der einzelnen Vorgänge.
    
- Ein **Input** -Element für ein Textfeld legt den abgeschlossenen Prozentsatz für alle ausgewählten Zuordnungen fest. 
    
- Ein **Button** -Element sendet die Statusänderungen. 
    
- Ein **Button** -Element aktualisiert die Seite. 
    
- Ein **Button** -Element beendet die APP und kehrt zur Seite Aufgaben in Project Web App zurück. 
    
Das untere Textfeld und die Schaltflächenelemente befinden sich in **div** -Elementen, sodass CSS die Position und das Aussehen der UI-Objekte leicht verwalten kann. Eine JavaScript-Funktion fügt am unteren Rand der Seite einen Absatz hinzu, der Ergebnisse zum Erfolg oder Misserfolg der Statusaktualisierung enthält. 
  
### <a name="procedure-2-to-create-the-html-content"></a>Verfahren 2. So erstellen Sie den HTML-Inhalt

1. Öffnen Sie in Visual Studio die Datei default. aspx.
    
   Die Datei enthält zwei **ASP: Content** -Elemente: das Element mit `ContentPlaceHolderID="PlaceHolderAdditionalPageHead"` dem-Attribut wird innerhalb der Seitenkopfzeile hinzugefügt, und `ContentPlaceHolderID="PlaceHolderMain"` das Element mit dem-Attribut wird innerhalb des Seiten **Text** Elements eingefügt. 
    
2. Fügen Sie `<asp:Content ContentPlaceHolderID="PlaceHolderAdditionalPageHead" runat="server">` im Steuerelement für die Seitenkopfzeile einen Verweis auf die Datei PS. js auf dem Project Server-Computer hinzu. Zum Testen und Debuggen können Sie PS. Debug. js verwenden. 
    
   ```HTML
     <script type="text/javascript" src="/_layouts/15/ps.debug.js"></script>
   ```

   Die APP-Infrastruktur verwendet `/_layouts/15/` das virtuelle Verzeichnis für die SharePoint-Website in IIS. Die physische Datei ist `%ProgramFiles%\Common Files\Microsoft Shared\Web Server Extensions\15\TEMPLATE\LAYOUTS\PS.debug.js`.
    
   > [!NOTE]
   > Bevor Sie die APP für Produktionszwecke bereitstellen, `.debug` entfernen Sie aus den Skriptverweisen, um die Leistung zu verbessern. 
  
3. Löschen Sie `<asp:Content ContentPlaceHolderID="PlaceHolderMain" runat="server">` im Steuerelement für den Seiten Text das generierte **div** -Element, und fügen Sie dann den HTML-Code für die UI-Objekte hinzu. Das **Table** -Element enthält nur eine Überschriftenzeile. Die **Vorgangsnamen** Spalte enthält ein Kontrollkästchen-Eingabesteuerelement. Text für das **Caption** -Element wird durch den **onGetUserNameSuccess** -Rückruf für die **getUserInfo** -Funktion in der Datei app. js ersetzt. 
    
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

4. Fügen Sie in der Datei app. CSS CSS-Code für die Position und die Darstellung der Benutzeroberflächenelemente hinzu. Den vollständigen CSS-Code der **Quick Status** -App finden Sie im [Beispielcode für den Quick Status-App](#pj15_StatusingApp_Example) -Abschnitt. 
    
In Prozedur 3 werden die JavaScript-Funktionen hinzugefügt, um die Zuordnungen zu lesen und die Tabellenzeilen zu erstellen sowie die Zuordnung abgeschlossener Prozentsatz zu ändern und zu aktualisieren. Die tatsächlichen Schritte sind iterativer bei der Entwicklung einer APP, bei der Sie alternativ einen Teil des HTML-Codes erstellen, Verwandte Formatvorlagen und JavaScript-Funktionen hinzufügen und testen, HTML-Code ändern oder hinzufügen und dann den Vorgang wiederholen.

<a name="pj15_StatusingApp_JavaScript"> </a>

### <a name="creating-the-javascript-functions-for-the-quickstatus-app"></a>Erstellen der JavaScript-Funktionen für die Quick Status-App

Die Visual Studio Vorlage für eine SharePoint-app enthält die Datei app. js, die den Standard Initialisierungscode enthält, der den SharePoint-Clientkontext abruft und grundlegende Get-und Sets-Aktionen für die APP-Seite demonstriert. Der JavaScript-Namespace für die SharePoint-clientseitige SP. js-Bibliothek ist **SP**. Da eine Project Server-APP die PS. js-Bibliothek verwendet, verwendet die APP den **PS** -Namespace, um den Clientkontext abzurufen und auf das JSOM für Project Server zuzugreifen. 
  
JavaScript-Funktionen in der **Quick Status** -APP umfassen Folgendes: 
  
- Der Dokument **fertige** Ereignishandler wird ausgeführt, wenn das Dokumentobjektmodell (DOM) instanziiert wird. Der **fertige** Ereignishandler führt die folgenden vier Schritte aus: 
    
    1. Initialisiert die globale Variable **projcontext** mit dem Clientkontext für die Project Server-JSOM und die globale **pwaWeb** -Variable. 
        
    2. Ruft die **getUserInfo** -Funktion auf, um die globale **projUser** -Variable zu initialisieren. 
        
    3. Ruft die **getassignings** -Funktion auf, die angegebene Zuordnungsdaten für den Benutzer abruft. 
        
    4. Bindet Klickereignishandler an das Tabellenkopf Kontrollkästchen und die Kontrollkästchen in jeder Zeile der Tabelle. Die Click-Ereignishandler verwalten das **checked** -Attribut der Kontrollkästchen, wenn der Benutzer ein Kontrollkästchen in der Tabelle aktiviert oder deaktiviert. 
    
- Wenn die **getassignings** -Funktion erfolgreich ist, wird die **onGetAssignmentsSuccess** -Funktion aufgerufen. Diese Funktion fügt für jede Zuweisung eine Zeile in die Tabelle ein, initialisiert die HTML-Steuerelemente in jeder Zeile und initialisiert dann die unteren Schaltflächeneigenschaften. 
    
- Der **OnClick** -Ereignishandler für die Schaltfläche **Aktualisieren** Ruft die **updateAssignments** -Funktion auf. Diese Funktion Ruft den vollständigen Prozentwert ab, der auf die einzelnen ausgewählten Zuordnungen angewendet wird. oder wenn das Textfeld Prozent abgeschlossen leer ist, ruft die Funktion den abgeschlossenen Prozentsatz jeder ausgewählten Zuordnung in der Tabelle ab. Die **updateAssignments** -Funktion speichert und übermittelt die Statusaktualisierungen und schreibt eine Meldung zu den Ergebnissen an den unteren Rand der Seite. 
    
### <a name="procedure-3-to-create-the-javascript-functions"></a>Verfahren 3. So erstellen Sie die JavaScript-Funktionen

1. Öffnen Sie in Visual Studio die Datei app. js, und löschen Sie dann alle Inhalte in der Datei.
    
2. Fügen Sie die globalen Variablen und den Dokument **Ready** -Ereignishandler hinzu. Auf das **Document** -Objekt wird mithilfe einer jQuery-Funktion zugegriffen. 
    
   Durch das Kontrollkästchen Ereignishandler für das Tabellenkopf Feld klicken wird der Aktivierungsstatus der Zeilenkontrollkästchen festgelegt. Wenn alle Zeilenkontrollkästchen aktiviert oder alle deaktiviert sind, wird durch die Kontrollkästchen Ereignishandler für die Zeile Aktivieren der Aktivierungsstatus des Headers aktiviert. Die Click-Ereignishandler legen auch die Ergebnismeldung am unteren Rand der Seite auf eine leere Zeichenfolge fest.
    
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

3. Fügen Sie die **getUserInfo** -Funktion hinzu, die **onGetUserNameSuccess** aufruft, wenn die Abfrage erfolgreich ist. Die **onGetUserNameSuccess** -Funktion ersetzt den Inhalt des Absatzes **Caption** durch eine Tabellenbeschriftung, die den Benutzernamen enthält. 
    
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

4. Fügen Sie die **getassignings** -Funktion hinzu, die **onGetAssignmentsSuccess** (siehe Schritt 5) aufruft, wenn die Zuordnungs Abfrage erfolgreich ist. Die Option **include** schränkt die Abfrage so ein, dass nur die angegebenen Felder zurückgegeben werden. 
    
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

5. Fügen Sie die **onGetAssignmentsSuccess** -Funktion hinzu, wodurch der Tabelle eine Zeile für jede Zuordnung hinzugefügt wird. Die **prevProjName** -Variable wird verwendet, um zu bestimmen, ob eine Zeile für ein anderes Projekt ist. Wenn dies der Fall ist, wird der Projektname in einer fett formatierten Schriftart angezeigt. Wenn dies nicht der Fall ist, wird der Projektname auf eine leere Zeichenfolge festgelegt. 
    
   > [!NOTE]
   > Das JSOM enthält keine **TimeSpan** -Eigenschaften, die die CSOM umfasst, beispielsweise **ActualWorkTimeSpan**. Stattdessen verwendet der JSOM-Eigenschaft für die Anzahl der Millisekunden, wie die [PS. StatusAssignment. actualWorkMilliseconds](https://msdn.microsoft.com/library/736bce1e-f734-0efe-6c5f-e0e891ab00ef%28Office.15%29.aspx) -Eigenschaft. Die Methode zum Abrufen dieser Eigenschaft ist **get\_actualWorkMilliseconds**, die einen ganzzahligen Wert zurückgibt. > die **get_actualWork** -Methode eine Zeichenfolge wie "3H" zurückgibt. Sie können entweder den Wert in der **Quick Status** -App verwenden, ihn jedoch anders anzeigen. Die Zuweisungs Abfrage enthält beide Eigenschaften, sodass Sie den Wert während des Debuggings testen können. Wenn Sie die **aktuelle** Arbeits Variable entfernen, können Sie die Eigenschaft " **actualy** " auch in der Zuordnungs Abfrage entfernen. 
  
   Schließlich initialisiert die **onGetAssignmentsSuccess** -Funktion die Schaltfläche **Aktualisieren** und die Schaltfläche **Aktualisieren** mit Klick-Ereignishandlern. Der Textwert der Schaltfläche **Aktualisieren** kann auch im HTML-Code festgelegt werden. 
    
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

6. Fügen Sie den **updateAssignments** -Click-Ereignishandler für die Schaltfläche **Aktualisieren** hinzu. Wenn der Benutzer einen Wert für den abgeschlossenen Prozentsatz einer Aufgabe ändert oder einen Wert in das Textfeld **PercentComplete** hinzufügt, kann der Wert in verschiedenen Formaten wie "60", "60%" oder "60%" eingegeben werden. Die **GetNumericValue** -Methode gibt den numerischen Wert des Eingabe Texts zurück. 
    
   > [!NOTE]
   > In einer APP, die für die Verwendung in der Produktion entwickelt wurde, sollten Eingabewerte für numerische Informationen die Feldüberprüfung und zusätzliche Fehlerüberprüfung umfassen. 
  
   Das **updateAssignments** -Beispiel enthält einige grundlegende Fehlerüberprüfung und zeigt Informationen im **Nachrichten** Absatz am unteren Rand der Seite an: grün, wenn die Aktualisierungsabfrage erfolgreich ist, und rot, wenn ein Eingabefehler vorliegt oder die Aktualisierungsabfrage nicht erfolgreich ausgeführt wird. 
    
   Bevor Sie die **submitAllStatusUpdates** -Methode verwenden, muss die APP die Updates auf dem Server mithilfe der **PS speichern. StatusAssignmentCollection. Update** -Methode. 
    
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

7. Fügen Sie die **exitToPwa** -Funktion hinzu, die den **SPHostUrl** -Abfragezeichenfolgenparameter für die URL der Host Project Web App-Website verwendet. Um zur Seite Aufgaben zurückzukehren, `"/Tasks.aspx"` fügen Sie die URL an. Beispielsweise wäre die **spHostUrl** -Variable auf `https://ServerName/ProjectServerName/Tasks.aspx`festgelegt.
    
   Die **getquerystringparameter** -Funktion teilt die URL der **Quick Status** -Seite, um den angegebenen Parameter in den URL-Optionen zu extrahieren und zurückzugeben. Im folgenden finden Sie ein Beispiel für das **Dokument. URL** -Wert für das **Quick Status** -Dokument (alle in einer Reihe): 
    
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

   Für die vorherige URL gibt die **getquerystringparameter** -Funktion den **SPHostUrl** - `https://ServerName/pwa`Abfragezeichenfolgenwert zurück. 
    
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

Wenn Sie die **Quick Status** -APP zu diesem Zeitpunkt veröffentlichen und Project Web App hinzufügen, kann die APP auf der Seite Websiteinhalte ausgeführt werden, Sie ist jedoch für Benutzer nicht leicht verfügbar. Um Benutzer beim Suchen und Ausführen der APP zu unterstützen, können Sie der Multifunktionsleiste auf der Seite "Vorgänge" eine Schaltfläche hinzufügen. In Prozedur 4 wird gezeigt, wie eine benutzerdefinierte menübandaktion hinzugefügt wird. 

<a name="pj15_StatusingApp_ribbon"> </a>

### <a name="adding-a-ribbon-custom-action"></a>Hinzufügen einer benutzerdefinierten Menübandaktion

Menübandregisterkarten, Gruppen und Steuerelemente für Project Web App werden in der Datei pwaribbon. XML angegeben, die im `[Program Files]\Common Files\Microsoft Shared\Web Server Extensions\15\TEMPLATE\FEATURES\PWARibbon\listtemplates` Verzeichnis auf dem Computer installiert ist, auf dem Project Server ausführt. Zum Entwerfen von benutzerdefinierten Aktionen für das Project Web App Menüband enthält der Project 2013 SDK-Download eine Kopie von pwaribbon. Xml. 
  
Project Web App verwendet unterschiedliche Menü Band Definitionen für die Seite "Vorgänge", je nachdem, ob die Project Web App-Instanz einen einzelnen Eingabemodus verwendet, mit dem Benutzer Werte für die Arbeitszeittabelle und den Vorgangsstatus eingeben können. Wenn Sie über Administratorrechte für Project Web App verfügen, wählen Sie im Menü Dropdown-Einstellungen in der oberen rechten Ecke der Seite die Option **PWA-Einstellungen** aus, um den Eingabemodus zu ermitteln. Wählen Sie auf der Seite PWA-Einstellungen die Option **Arbeitszeittabellen Einstellungen und Standardwerte**aus, und sehen Sie sich dann das Kontrollkästchen **einzelner Eingabemodus** am unteren Rand der Seite an. 
  
Wenn der einzeleingabe Modus deaktiviert ist, wird das Menüband auf der Seite "Vorgänge" in pwaribbon. XML durch den Bereich "meine Arbeit" definiert: 
  
```XML
   <!-- REGION My Work Ribbon-->
   <CustomAction
      Id="Ribbon.ContextualTabs.MyWork"
      . . .
```

Wenn der einzeleingabe Modus aktiviert ist, wird das Menüband für die Aufgabenseite durch den Bereich "gebundener Modus" in pwaribbon. XML definiert: 
  
```XML
   <!-- REGION Tied Mode Ribbon-->
   <CustomAction
      Id="Ribbon.ContextualTabs.TiedMode"
      . . .
```

Obwohl die Gruppen und Steuerelemente in jeder Region ähnlich aussehen, kann ein Steuerelement für den gebundenen Modus eine andere Funktion als das gleiche Steuerelement für den nicht gebundenen Modus aufrufen. In Verfahren 4 wird gezeigt, wie ein Schaltflächen-Steuerelement für die **Quick Status** -app hinzugefügt wird, wenn der einzeleingabe Modus deaktiviert ist (das Kontrollkästchen **Einzel Eintrags Modus** ist deaktiviert). 
  
> [!NOTE]
> Allgemeine Informationen zum Hinzufügen von benutzerdefinierten Aktionen zu einem Menüband oder zu einem Menü in einer SharePoint-Anwendung finden Sie unter [Erstellen benutzerdefinierter Aktionen zur Bereitstellung mit Apps für SharePoint](https://msdn.microsoft.com/library/jj163954.aspx). 
  
### <a name="procedure-4-to-add-a-ribbon-custom-action-to-the-tasks-page"></a>Prozedur 4. So fügen Sie der Seite "Vorgänge" eine benutzerdefinierte menübandaktion hinzu

1. Überprüfen Sie das Menüband auf der Seite Vorgänge in Project Web App. Wählen Sie im Menüband die Registerkarte **Tasks** aus, und planen Sie, wie Sie geändert werden soll. Es gibt sieben Gruppen, beispielsweise **Submit**, **Tasks**und **Period**. Die **Submit** -Gruppe verfügt über zwei Steuerelemente, eine Schaltfläche **Speichern** und das Dropdownmenü **Sende Status** . Sie können ein Steuerelement an einer beliebigen Position in einer Gruppe hinzufügen, eine Gruppe mit einem neuen Steuerelement an einer beliebigen Position auf der Registerkarte **Aufgaben** hinzufügen oder eine weitere menübandregisterkarte mit benutzerdefinierten Gruppen und Steuerelementen hinzufügen. In diesem Beispiel wird der **Submit** -Gruppe eine dritte Schaltfläche hinzugefügt, wobei die Schaltfläche die URL der **Quick Status** -App aufruft. 
    
2. Klicken Sie im Bereich **Projektmappen-Explorer** in Visual Studio mit der rechten Maustaste auf das **Quick Status** -Projekt, und fügen Sie dann ein neues Element hinzu. Wählen Sie im Dialogfeld **Neues Element hinzufügen** die Option **benutzerdefinierte menübandaktion** aus (siehe Abbildung 4). Nennen Sie beispielsweise die benutzerdefinierte Aktion RibbonQuickStatusAction, und wählen Sie dann **Hinzufügen**aus.
    
   **Abbildung 4. Hinzufügen einer benutzerdefinierten menübandaktion**

   ![Hinzufügen einer benutzerdefinierten Menübandaktion](media/pj15_CreateStatusingApp_AddRibbonCustomAction.gif "Hinzufügen einer benutzerdefinierten Menübandaktion")
  
3. Lassen Sie auf der ersten Seite des Assistenten zum **Erstellen einer benutzerdefinierten Aktion für Menüband** die Option **Host-Webdienste** ausgewählt, wählen Sie in der Dropdownliste für den Bereich benutzerdefinierter Aktionen die Option **keine** aus, und klicken Sie dann auf **weiter** (siehe Abbildung 5). Die Elemente in den Dropdownlisten sind für SharePoint relevant, nicht für Project Server. Wir ersetzen den Großteil des generierten XML-Code für die benutzerdefinierte Aktion so, dass Sie auf Project Server angewendet wird. 
    
   **Abbildung 5. Angeben von Eigenschaften für die benutzerdefinierte menübandaktion**

   ![Festlegen von Eigenschaften für die benutzerdefinierte Menübandaktion](media/pj15_CreateStatusingApp_RibbonCustomAction2.gif "Festlegen von Eigenschaften für die benutzerdefinierte Menübandaktion")
  
4. Belassen Sie auf der nächsten Seite des Assistenten zum **Erstellen einer benutzerdefinierten Aktion für Menüband** alle Standardwerte für die Einstellungen, und wählen Sie dann **Fertig stellen** aus (siehe Abbildung 6). Visual Studio erstellt den **RibbonQuickStatusAction** -Ordner, der eine Datei "Elements. xml" enthält. 
    
   **Abbildung 6. Angeben der Einstellungen für ein Schaltflächen-Steuerelement**

   ![Festlegen der Einstellungen für ein Schaltflächensteuerelement](media/pj15_CreateStatusingApp_RibbonCustomAction3.gif "Festlegen der Einstellungen für ein Schaltflächensteuerelement")
  
5. Ändern Sie den standardmäßig generierten Code in der Datei "Elements. xml" für die benutzerdefinierte menübandaktion. Im folgenden finden Sie den standardmäßigen XML-Code:
    
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

   1. Löschen Sie im **Custom** -Element das **Sequence** -Attribut und das **Title** -Attribut. 
    
   2. Wenn Sie der **Submit** -Gruppe ein Steuerelement hinzufügen möchten, suchen Sie `Ribbon.ContextualTabs.MyWork.Home.Groups` die erste Gruppe in der Auflistung in der pwaribbon. XML-Datei, die `<Group Id="Ribbon.ContextualTabs.MyWork.Home.Page" Command="PageGroup" Sequence="10" Title="$Resources:pwafeatures,PAGE_PDP_CM_SUBMIT"`das Element darstellt, das beginnt. Um der **Submit** -Gruppe ein untergeordnetes Steuerelement hinzuzufügen, zeigt der folgende Code das richtige **Location** -Attribut des **CommandUIDefinition** -Elements in der Datei "Elements. xml": 
    
      ```XML
        <CommandUIDefinitions>
          <CommandUIDefinition Location="Ribbon.ContextualTabs.MyWork.Home.Page.Controls._children">
             . . .
          </CommandUIDefinition>
        </CommandUIDefinitions>
      ```

   3. Ändern Sie die Attributwerte des untergeordneten **Schaltflächen** Elements wie folgt: 
    
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

       - Damit die Schaltfläche das dritte Steuerelement in der Gruppe ist, kann das **Sequence** -Attribut eine beliebige Zahl `Sequence="20"` höher sein als der Wert des vorhandenen **Sende Status** Steuerelements (bei dem es sich um ein **FlyoutAnchor** -Element in pwaribbon. XML handelt). Gemäß der Konvention sind `10, 20, 30, …`die Sequenznummern von Gruppen und Steuerelementen, mit denen Elemente in zwischen Positionen eingefügt werden können.
    
       - Das **Command** -Attribut gibt den Befehl an, der im **commanduihandler-** -Element ausgeführt werden soll (siehe den folgenden Schritt 5. d). Sie können den Befehlsnamen vereinfachen, damit er für den nächsten Entwickler einfacher wird. Beispielsweise `Command="Invoke_QuickStatus"` ist einfacher zu lesen als `Command="Invoke_RibbonQuickStatusActionButtonRequest"`.
    
       - Die Bildattribute geben das 16 x 16-Pixel-Symbol und das 32 x 32-Pixel-Symbol für das Schaltflächen-Steuerelement an. `Image32by32="_layouts/15/images/placeholder32x32.png"` Gibt in der Datei Default Elements. XML einen orangefarbenen Punkt an. Sie können Symbole aus den Bild Zuordnungsdateien (ps16x16. png und ps32x32. png) extrahieren, die im `[Program Files]\Common Files\Microsoft Shared\Web Server Extensions\15\TEMPLATE\LAYOUTS\1033\IMAGES` Verzeichnis auf dem Computer installiert sind, auf dem Project Server läuft. Beispielsweise befindet sich das 32 x 32-Pixel-Symbol in der zweiten Spalte mit Symbolen von Links und der zehnten Zeile nach unten vom oberen Rand der ps32x32. png-ImageMap (der obere Rand des Symbols befindet sich nach dem Ende der neunten Zeile; 9 Zeilen x 32 Pixel/Zeile = 288 Pixel). 
    
       - Zum Anzeigen einer QuickInfo für das Schaltflächen-Steuerelement fügen Sie das **ToolTipTitle** -Attribut und das **ToolTipDescription** -Attribut hinzu. 
    
    4. Ändern Sie die Attribute des **commanduihandler-** -Elements. Stellen Sie beispielsweise sicher, dass das **Command** -Attribut mit dem Wert des **Command** -Attributs für das **Button** -Element übereinstimmt. Für das **Command** - `~appWebUrl` Attribut ist ein Platzhalter für die URL der **Quick Status** -Webseite. Wenn die **Quick Status** -App auf der menübandschaltfläche aufgerufen wird, wird das Token **{Standard Tokens}** durch URL-Optionen ersetzt, die **SPHostUrl**, die **Sprache**, **SPClientTag**, **SPProductNumber**und **SPAppWebUrl**einschließen.
    
        ```XML
            <CommandUIHandlers>
                <CommandUIHandler Command="Invoke_QuickStatus"
                                  CommandAction="~appWebUrl/Pages/Default.aspx?{StandardTokens}"/>
            </CommandUIHandlers>
        ```

6. Öffnen Sie im **Projektmappen-Explorer**den **Feature1. Feature** -Designer, und legen Sie das **RibbonQuickStatusAction** -Element aus den **Elementen im Lösungs** Bereich auf die **Elemente im Featurebereich** . Wenn Sie dann den **Paket-** Designer öffnen, befindet sich das **RibbonQuickStatusAction** -Element in den **Elementen im Paket** Bereich. 
    
Wenn Sie die APP entwickeln und eine menübandschaltfläche hinzufügen, testen Sie die APP normalerweise und legen Haltepunkte im JavaScript-Code für das Debugging fest. Wenn Sie **F5** drücken, um das Debuggen zu starten, kompiliert Visual Studio die APP, stellt Sie auf der Website bereit, die in der Eigenschaft **Website-URL** des **Quick Status** -Projekts angegeben ist, und zeigt eine Seite an, die fragt, ob Sie der APP Vertrauen. Wenn Sie den Vorgang fortsetzen und dann die **Quick Status** -App beenden, wird die Seite "Aufgaben" in Project Web App zurückgegeben. 

> [!NOTE]
> Abbildung 7 zeigt, dass die Schaltfläche " **schnell Status** " auf der Registerkarte " **Aufgaben** " des Menübands deaktiviert ist. Nach vielen Debug-Bereitstellungen mit Visual Studio können benutzerdefinierte menübandsteuerelemente blockiert werden, wenn Sie die veröffentlichte App weiterhin auf demselben Testserver Debuggen oder bereitstellen. Zum Aktivieren der Schaltfläche Löschen Sie das **RibbonQuickStatusAction** -Element in Visual Studio und erstellen dann eine neue menübandaktion mit einem anderen Namen und einer anderen ID. Wenn das Problem dadurch nicht behoben wird, versuchen Sie, die APP aus der Project Web App Testinstanz zu entfernen und die APP dann mit einer anderen APP-ID neu zu erstellen. 
  
**Abbildung 7. Anzeigen der QuickInfo der deaktivierten Schaltfläche "schnell Status"**

![Anzeigen der QuickInfo der deaktivierten Schaltfläche](media/pj15_CreateStatusingApp_ButtonToolTipDisabled.gif "Anzeigen der QuickInfo der deaktivierten Schaltfläche")
  
In Verfahren 5 wird gezeigt, wie Sie die **Quick Status** -App bereitstellen und installieren. In Prozedur 6 werden einige zusätzliche Schritte zum Testen der APP gezeigt, nachdem Sie Sie installiert haben. 

<a name="pj15_StatusingApp_Deploying"> </a>

## <a name="deploying-the-quickstatus-app"></a>Bereitstellen der Quick Status-App

Es gibt verschiedene Möglichkeiten, eine app in einer SharePoint-Webanwendung wie Project Web App bereitzustellen. Welche Bereitstellung Sie verwenden, hängt davon ab, ob die app in einem privaten SharePoint-Katalog oder im öffentlichen Office Store veröffentlicht werden soll und ob SharePoint lokal installiert ist oder ein Online-Mandant ist. In Verfahren 5 wird gezeigt, wie die **Quick Status** -app in einer lokalen Installation in einem privaten App-Katalog bereitgestellt wird. Weitere Informationen finden Sie unter [Installieren und Verwalten von Apps für SharePoint 2013](https://technet.microsoft.com/library/fp161232.aspx) und [Veröffentlichen von Apps für SharePoint](https://msdn.microsoft.com/library/jj164070.aspx)
  
> [!NOTE]
> Zum Hinzufügen einer APP zu einem SharePoint-Katalog sind SharePoint-Administratorberechtigungen erforderlich. 
  
### <a name="procedure-5-to-deploy-the-quickstatus-app"></a>Prozedur 5. So stellen Sie die Quick Status-App bereit

1. Speichern Sie in Visual Studio alle Dateien, und klicken Sie dann im **Projektmappen-Explorer** mit der rechten Maustaste auf das **Quick Status** -Projekt, und wählen Sie **veröffentlichen**aus.
    
2. Da die **Quick Status** -app in SharePoint gehostet wird, gibt es nur sehr wenige Optionen für die Veröffentlichung (siehe Abbildung 8). Wählen Sie im Dialogfeld **Apps für Office und SharePoint veröffentlichen** die Option **Fertig stellen**aus.
    
   **Abbildung 8. Veröffentlichen der Quick Status-App**

   ![Verwenden des Assistenten zum Veröffentlichen](media/pj15_CreateStatusingApp_PublishWizard.gif "Verwenden des Assistenten zum Veröffentlichen")
  
3. Kopieren Sie die Datei Quick Status. app aus `~\QuickStatus\bin\Debug\app.publish\1.0.0.0` dem Verzeichnis in ein bequemes Verzeichnis auf dem lokalen Computer (oder auf den SharePoint-Computer für eine lokale Installation). 
    
4. Klicken Sie in der SharePoint-zentral Administration auf der Schnellstartleiste auf **apps** , und wählen Sie dann **App-Katalog verwalten**aus.
    
5. Wenn kein App-Katalog vorhanden ist, erstellen Sie eine Websitesammlung für den App-Katalog, indem Sie im Abschnitt Verwalten des App-Katalogs [in SharePoint 2013](https://technet.microsoft.com/library/fp161234.aspx)auf die *App-katalogwebsite für eine Webanwendung konfigurieren* folgen.
    
   Wenn ein App-Katalog vorhanden ist, navigieren Sie auf der Seite App-Katalog verwalten zur Website-URL. In den folgenden Schritten ist `https://ServerName/sites/TestApps`beispielsweise die APP-katalogwebsite.
    
6. Klicken Sie auf der Seite App-Katalog auf der Schnellstartleiste auf **Apps für SharePoint** . Wählen Sie auf der Seite Apps für SharePoint im Menüband auf der Registerkarte **Dateien** die Option **Dokument hochladen**aus.
    
7. Suchen Sie im Dialogfeld **Dokument hinzufügen** nach der Quick Status. app-Datei, fügen Sie Kommentare zur Version hinzu, und wählen Sie dann **OK**aus.
    
8. Wenn Sie eine APP hinzufügen, können Sie auch lokale Informationen für die APP-Beschreibung, das Symbol und andere Informationen hinzufügen. Fügen Sie im Dialogfeld **Apps für SharePoint-Quick Status. app** die Informationen hinzu, die Sie für die app in der SharePoint-Websitesammlung anzeigen möchten. Fügen Sie beispielsweise die folgenden Informationen hinzu: 
    
   1. **Kurzes Beschreibungs** Feld: Geben Sie Quick Status Test App ein.
    
   2. **Beschreibungs** Feld: Geben Sie Test-App ein, um den abgeschlossenen Prozentsatz für Vorgänge in mehreren Projekten zu aktualisieren.
    
   3. **Symbol-URL** -Felder: Fügen Sie ein 96 x 96-Pixel Bild für das App-Symbol zu den Websiteobjekten für den App-Katalog hinzu. Navigieren Sie beispielsweise zu `https://ServerName/sites/TestApps`, wählen Sie im Dropdownmenü **Einstellungen** die Option **Websiteinhalte** aus, wählen Sie **Website Objekte**aus, und fügen Sie dann das Bild quickStatusApp. png hinzu. Klicken Sie mit der rechten Maustaste auf das **quickStatusApp** -Element, wählen Sie **Eigenschaften**aus, und kopieren Sie dann den Wert **Address (URL)** im Dialogfeld **Eigenschaften** . Kopieren `https://ServerName/sites/TestApps/SiteAssets/QuickStatusApp.png`Sie beispielsweise den Wert in das Feld **Symbol-URL** -Webadresse, und fügen Sie ihn ein. Geben Sie eine Beschreibung für das Symbol ein, beispielsweise (siehe Abbildung 9), geben Sie Quick Status App-Symbol ein. Testen Sie, ob die URL gültig ist.
    
      **Abbildung 9. Hinzufügen einer Symbol-URL für die Quick Status-App**

      ![Festlegen von Eigenschaften für die App in SharePoint](media/pj15_CreateStatusingApp_AddAppToSharePointSettings.gif "Festlegen von Eigenschaften für die App in SharePoint")
  
   4. **Category** -Feld: Wählen Sie eine vorhandene Kategorie aus, oder geben Sie einen eigenen Wert an. Geben Sie beispielsweise Statusing ein.
    
      > [!NOTE]
      > Eine Kategorie mit dem Namen **Statusing** dient nur zu Testzwecken. Eine typische Kategorie für Project Server-Apps ist **Projekt Management**. 
  
   5. Feld **Herausgebername** : Geben Sie den Namen des Herausgebers ein. Geben Sie in diesem Beispiel Project SDK ein.
    
   6. Feld **Enabled** : Aktivieren Sie das Kontrollkästchen **aktiviert** , um die APP für Project Web App Websiteadministratoren für die Installation sichtbar zu machen. 
    
   7. Zusätzliche Felder sind optional. Sie können beispielsweise eine Support-URL und mehrere Hilfe Bilder für die Seite mit den App-Details hinzufügen. In Abbildung 9 enthalten die Felder **Bild-URL 1** die URL für einen Screenshot der APP und eine Beschreibung des Screenshot. 
    
   8. Wählen Sie im Dialogfeld **Apps für SharePoint-Quick Status. app** die Option **Speichern**aus. In Abbildung 9 ist das Element **Quick Status Update** in der Bibliothek Apps für SharePoint zur Bearbeitung ausgecheckt, daher würden Sie auf der Registerkarte **Bearbeiten** des Dialogfeld-Menübands **Einchecken** auswählen, um den Vorgang abzuschließen (siehe Abbildung 10). 
    
      **Abbildung 10. Die Quick Status-APP wird der Apps für SharePoint-Bibliothek hinzugefügt.**

      ![Die QuickStatus-App wird SharePoint hinzugefügt](media/pj15_CreateStatusingApp_AddAppToSharePoint.gif "Die QuickStatus-App wird SharePoint hinzugefügt")
  
9. Wählen Sie in Project Web App im Dropdownmenü **Einstellungen** die Option **app hinzufügen**aus. Wählen Sie auf der Seite Ihre apps auf der Schnellstartleiste in **Ihrer Organisation aus**, und wählen Sie dann **App-Details** für die **schnell Status Update** -App aus. Abbildung 11 zeigt die Detailseite mit dem App-Symbol, Screenshot und anderen Informationen, die Sie im vorherigen Schritt hinzugefügt haben. 
    
   **Abbildung 11. Verwenden der Seite Details zum schnell Status Update in Project Web App**

   ![Hinzufügen der QuickStatus-App zu Project Web App](media/pj15_CreateStatusingApp_AddAppToPWA.gif "Hinzufügen der QuickStatus-App zu Project Web App")
  
10. Wählen Sie auf der Seite Quick Status Update Details die Option **Hinzufügen**aus. Project Web App zeigt ein Dialogfeld an, in dem die Vorgänge aufgelistet sind, die die Quick Status-app ausführen kann (siehe Abbildung 12). Die Liste der Vorgänge wird von den **AppPermissionRequest** -Elementen in der Datei AppManifest. XML abgeleitet. 
    
    **Abbildung 12. Überprüfen, ob Sie der schnell Status-App Vertrauen**

    ![Überprüfen des Vertrauens gegenüber der QuickStatus-App](media/pj15_CreateStatusingApp_AddAppToPWA2Trust.gif "Überprüfen des Vertrauens gegenüber der QuickStatus-App")
  
11. Wählen Sie im Dialogfeld **schnell Status Aktualisierung ausführen** **vertrauenswürdig aus**. Die APP wird der Seite Project Web App Websiteinhalt hinzugefügt (siehe Abbildung 13).
    
    **Abbildung 13. Anzeigen der schnell Status-App auf der Seite "Websiteinhalte"**

    ![Anzeigen der QuickStatus-App in den Websiteinhalten](media/pj15_CreateStatusingApp_AddAppToPWA3.gif "Anzeigen der QuickStatus-App in den Websiteinhalten")
  
Auf der Seite Websiteinhalte können Sie das Symbol **Quick Status Update** auswählen, um die APP auszuführen.

> [!NOTE]
> Für zusätzliche Befehle, die Informationen über die APP bereitstellen, wählen Sie auf der Seite Websiteinhalte den Bereich aus, der den **schnell Status Update** Namen und die Auslassungspunkte (...) enthält. Sie können die Seite Info für die APP lesen, die Seite App-Details anzeigen, die Informationen zu app-Fehlern enthält, die Seite App-Berechtigungen überprüfen oder die APP aus Project Web App entfernen. 
  
Auf der Seite Aufgaben in Project Web App (siehe Abbildung 14) sollte die Schaltfläche **Quick Status** auf dem Menüband aktiviert sein. Wenn die Schaltfläche " **schnell Status** " deaktiviert ist, versuchen Sie die im Hinweis für Abbildung 7 beschriebenen Aktionen. 

**Abbildung 14. Starten der Quick Status-App auf der Registerkarte "Aufgaben"**

![Starten der QuickStatus-App von der Registerkarte "TASKS"](media/pj15_CreateStatusingApp_TasksRibbon.gif "Starten der QuickStatus-App von der Registerkarte "TASKS"")
  
In Prozedur 6 sind einige Tests aufgeführt, die mit der Quick Status-App vorgenommen werden müssen.

<a name="pj15_StatusingApp_Testing"> </a>

## <a name="testing-the-quickstatus-app"></a>Testen der Quick Status-App

Jeder Vorgang, den ein Benutzer in der **Quick Status** -App möglicherweise ausprobieren sollte, sollte vor der Bereitstellung der APP auf einem Produktions Server oder einem Produktions Mandanten von Project online auf einer Testinstallation von Project Server getestet werden. Mit einer Testinstallation können Sie Zuordnungen für Benutzer ändern und löschen, ohne dass sich dies auf aktuelle Projekte auswirkt. Bei Tests sollten auch mehrere Benutzer mit unterschiedlichen Berechtigungssätzen wie Administrator, Projektmanager und Teammitglied beteiligt sein. Durch gründliche Tests können Änderungen aufgezeigt werden, die in der APP vorgenommen werden sollten, was beim Testen während der Entwicklung nicht erkennbar war. In Prozedur 6 werden mehrere Tests für die **Quick Status** -App aufgelistet, es werden jedoch keine erschöpfenden Testreihen eingeschlossen. 
  
### <a name="procedure-6-to-test-the-quickstatus-app"></a>Prozedur 6. So testen Sie die Quick Status-App

1. Führen Sie die **Quick Status** -App aus, in der der Benutzer keine Zuweisungen hat. Die APP sollte eine blaue Meldung am unteren Rand der Seite anzeigen, beispielsweise hat der **Benutzer Name keine Zuweisungen**.
    
   Wählen Sie **Aktualisieren**aus, und die Nachricht ändert sich in eine grüne **Zuweisung wurde aktualisiert**.
    
   > [!NOTE]
   > Das App-Verhalten sollte so geändert werden, dass die Schaltfläche **Aktualisieren** deaktiviert ist, wenn keine Zuweisungen vorhanden sind. 
  
2. Führen Sie die APP aus, bei der der Benutzer mehrere Zuordnungen in mehreren verschiedenen Projekten hat und einige Zuordnungen nicht abgeschlossen sind. Beachten Sie die Darstellung der APP, und führen Sie Aktionen wie folgt aus (siehe Abbildung 15):
    
   1. Die **onGetAssignmentsSuccess** -Funktion erstellt eine Zeile in der Tabelle für jede Zuweisung für den aktuellen Benutzer. Der Projektname wird nur einmal in einer fetten Schriftart für die erste Zuweisung in jedem Projekt angezeigt. 
    
   2. Deaktivieren Sie das Kontrollkästchen in der Spaltenüberschrift **Vorgangsname** . Der Ereignishandler Tabellenkopf Klick löscht alle anderen Kontrollkästchen in den Vorgangszeilen. 
    
   3. Wählen Sie alle Aufgaben aus. Der Click-Ereignishandler für jede Zeile bestimmt, ob alle Zeilen ausgewählt sind, und wenn dies der Fall ist, wird die Spaltenüberschrift **Vorgangsname** ausgewählt. 
    
   4. Deaktivieren Sie erneut alle Kontrollkästchen, und wählen Sie dann eine Zuordnung mit einer verbleibenden Arbeit aus. Beispielsweise zeigt Abbildung 15 die oberste Aufgabe T1 verfügt über 20% verbleibenden Arbeit abgeschlossen.
    
   5. Geben Sie im Textfeld **Prozent fertig stellen** den Text 80 ein, und wählen Sie dann **Aktualisieren**aus. Am unteren Rand der Seite sollte eine grüne Meldung angezeigt werden, **Zuordnungen wurden aktualisiert**.
    
      **Abbildung 15. Aktualisieren einer Zuordnung in der Quick Status-App**

      ![Aktualisieren einer Zuweisung in der QuickStatus-App](media/pj15_CreateStatusingApp_Testing1Update.gif "Aktualisieren einer Zuweisung in der QuickStatus-App")
  
3. Wählen Sie **Aktualisieren** (siehe Abbildung 16). Alle Aufgaben werden erneut ausgewählt, und die oberste Aufgabe zeigt 80% abgeschlossen. 
    
      **Abbildung 16. Aktualisieren der Seite "schnell Status Aktualisierung"**

      ![Aktualisieren der QuickStatus-Seite](media/pj15_CreateStatusingApp_Testing2Refresh.gif "Aktualisieren der QuickStatus-Seite")
  
4. Deaktivieren Sie alle Kontrollkästchen, und wählen Sie dann eine andere Aufgabe aus. Wählen Sie beispielsweise **neuer Vorgang aus PWA aus**. Lassen Sie das Textfeld **Prozentsatz abgeschlossen** leer, löschen Sie den gesamten Text in der Spalte **% abgeschlossen** für den ausgewählten Vorgang, und wählen Sie dann **Aktualisieren**aus. Da beide Textfelder leer sind, wird in der App eine rote Fehlermeldung angezeigt (siehe Abbildung 17).
    
      **Abbildung 17. Testen der Fehlermeldung**

      ![Testen der Fehlermeldung](media/pj15_CreateStatusingApp_Testing3Error.gif "Testen der Fehlermeldung")
  
5. Aktualisieren Sie die vorherige Aufgabe auf 80% abgeschlossen, und wählen Sie dann **Beenden**aus. Die **exitToPwa** -Funktion ändert den Speicherort des Browserfensters auf die Seite Aufgaben in der SharePoint-Hostanwendung (die URL ändert https://ServerName/pwa/Tasks.aspx)sich in. Abbildung 18 zeigt, dass die **T1** -Aufgabe und die **neue Aufgabe aus PWA** -Aufgabe jeweils 80% abgeschlossen anzeigen. 
    
      **Abbildung 18. Überprüfen, ob die Vorgänge in Project Web App aktualisiert wurden**

      ![Überprüfen der aktualisierten Aufgaben in Project Web App](media/pj15_CreateStatusingApp_TasksUpdatedInPWA.gif "Überprüfen der aktualisierten Aufgaben in Project Web App")
  
6. Bevor der aktualisierte Status in Project Professional 2013 angezeigt wird, müssen die Änderungen zur Genehmigung übermittelt und dann vom Projektmanager genehmigt werden.
    
Das Testen zeigt mehrere andere Änderungen, die in der **Quick Status** -App für eine verbesserte Benutzerfreundlichkeit vorgenommen werden sollten. Zum Beispiel:

- Es sollten zusätzliche Fehlerprüfungen und die Validierung von Text Feldwerten erfolgen. Derzeit kann ein Benutzer einen nicht numerischen Wert oder einen negativen Wert für den abgeschlossenen Prozentsatz eingeben, was zu einer unfreundlichen Fehlermeldung führt. Bei einem negativen Wert ist die Fehlermeldung beispielsweise **Fehler beim Aktualisieren der Zuordnungen: PJClientCallableException: StatusingSetDataValueInvalid**.
    
- Die Fehlermeldung für leere Textfelder kann neben der Zeilennummer auch das Projekt und die Aufgabe auflisten.
    
- Die Erfolgsmeldung könnte eine Liste der aktualisierten Aufgaben enthalten. oder wenn die **updateAssignments** -Funktion erfolgreich ist, kann Sie eine automatische Seitenaktualisierung durchführen und aktualisierte Vorgänge oder Prozentsätze in einer anderen Farbe und einer fetten Schriftart anzeigen. 
    
- Um eine sehr große Tabelle zu vermeiden, sollte die Zuordnungstabelle auf Aufgaben limitiert sein, die weniger als 100% abgeschlossen sind. Oder fügen Sie eine Option hinzu, um alle Aufgaben anzuzeigen. Dieses Problem kann auch mithilfe eines auf jQuery basierenden Rasters anstelle einer Tabelle behoben werden, in der Sie die Filterung und das Raster-Paging ganz einfach implementieren können.
    
- Da die **Quick Status** -App den Status nicht übermittelt, wäre das Symbol " **schnell Status** " auf der Registerkarte " **Aufgaben** " des Menübands mehr logisch das erste Symbol in der Gruppe " **Aufgaben** " und nicht das letzte Symbol in der **Submit** -Gruppe. 
    
- Da die **onGetAssignmentsSuccess** -Funktion den **btnSubmitUpdate** -Schaltflächentext initialisiert, aber die anderen Schaltflächen Textwerte in HTML initialisiert werden, bleibt die Seite in einem teilweise initialisierten Zustand, während die **getassigns** -Funktion ausgeführt wird. Schaltflächen auf der Seite werden konsistenter angezeigt, wenn die Textwerte alle in HTML initialisiert wurden. 
    
Am wichtigsten ist, dass der von der **Quick Status** -App verwendete Ansatz, bei dem er für Zuordnungen den abgeschlossenen Prozentsatz ändert, in einer Produktions-App überarbeitet werden sollte. Weitere Informationen finden Sie im Abschnitt " [Nächste Schritte](#pj15_StatusingApp_NextSteps) ". 

<a name="pj15_StatusingApp_Example"> </a>

## <a name="example-code-for-the-quickstatus-app"></a>Beispielcode für die Quick Status-App

### <a name="defaultaspx-file"></a>Datei "default. aspx"

Der folgende Code befindet sich in `Pages\Default.aspx` der Datei des **Quick Status** -Projekts: 
  
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

### <a name="appjs-file"></a>Datei "App. js"

Der folgende Code befindet sich in `Scripts\App.js` der Datei des **Quick Status** -Projekts: 
  
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

Der folgende CSS-Code befindet sich `Content\App.css` in der Datei des **Quick Status** -Projekts: 
  
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

### <a name="elementsxml-file-for-the-ribbon"></a>Datei "Elements. xml" für das Menüband

Die folgende XML-Definition für die Schaltfläche hinzugefügt auf der Registerkarte **Aufgaben** im Menüband befindet `RibbonQuickStatusAction\Elements.xml` sich in der Datei des **Quick Status** -Projekts: 
  
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

Im folgenden finden Sie den XML-Code für das App-Manifest des **Quick Status** -Projekts, das die beiden Berechtigungs Anforderungsbereiche enthält, die für die Aktualisierung des Zuordnungsstatus des App-Benutzers in mehreren Projekten erforderlich sind: 
  
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

### <a name="appiconpng-file"></a>AppIcon. png-Datei

Die vollständige Visual Studio Lösung für die **Quick Status** -app enthält eine benutzerdefinierte AppIcon. png-Datei. Die Lösung wird im Project 2013 SDK-Download enthalten sein. 

<a name="pj15_StatusingApp_NextSteps"> </a>

## <a name="next-steps"></a>Nächste Schritte

Die **Quick Status** -APP ist ein relativ einfaches Beispiel für das Schreiben von apps, die auf Project Server 2013 und Project Online installiert werden können. Im Abschnitt [Testen des Quick Status-App](#pj15_StatusingApp_Testing) werden mehrere Verbesserungen aufgeführt, die für eine bessere Benutzerfreundlichkeit vorgenommen werden können. Die **Quick Status** -App verwendet JavaScript-Funktionen, um den Zuordnungsstatus für Project Web App zu aktualisieren. Das Ändern der Zuordnung "abgeschlossener Prozentsatz" ist jedoch keine empfohlene Projekt Verwaltungsmethode. Ein weiterer Ansatz besteht darin, das tatsächliche Startdatum und die verbleibende Dauer der zugewiesenen Vorgänge zu aktualisieren. Eine Erläuterung der Probleme finden Sie unter [Update besser](https://www.mpug.com/articles/update-better) im MPUG-Newsletter. 

<a name="pj15_StatusingApp_AdditionalResources"> </a>

## <a name="see-also"></a>Siehe auch

- [Project Server-Programmieraufgaben](project-programming-tasks.md)
- [SharePoint-Add-Ins](https://msdn.microsoft.com/library/jj163230.aspx)
- [Verwalten von Vorgangsaktualisierungen in Project Web App](https://technet.microsoft.com/library/hh767481%28v=office.14%29.aspx)
- [Erstellen benutzerdefinierter Aktionen zur Bereitstellung mit SharePoint-Add-Ins](https://msdn.microsoft.com/library/jj163954.aspx)
    

