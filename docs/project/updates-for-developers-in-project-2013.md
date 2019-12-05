---
title: Updates für Entwickler in Project
manager: lindalu
ms.date: 12/03/2019
ms.audience: Developer
localization_priority: Normal
ms.assetid: 5b2b22cd-6e28-43a8-9092-b411da8bfb53
description: Zu den neuen Features gehören ein clientseitiges Objektmodell (CSOM), Rest-Schnittstellen, ein OData-Dienst für die Berichterstellung, Remoteereignis Empfänger, deklarative Workflows und Aufgabenbereich-Add-Ins für Projekt Clients.
ms.openlocfilehash: c2bc0b475639a8582422b2091169116428367c60
ms.sourcegitcommit: 37080eb0087261320e24e6f067e5f434a812b2d2
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/04/2019
ms.locfileid: "39819280"
---
# <a name="updates-for-developers-in-project"></a>Updates für Entwickler in Project

Erweiterungsfeatures in Project Server 2013 arbeiten mit Add-Ins für Project Online und mit lokalen Installationen. Zu den neuen Features gehören ein clientseitiges Objektmodell (CSOM), Rest-Schnittstellen, ein OData-Dienst für die Berichterstellung, Remoteereignis Empfänger, deklarative Workflows und Aufgabenbereich-Add-Ins für Projekt Clients. Erfahren Sie auch mehr über veraltete Features, die nicht für die neue Entwicklung verwendet werden sollten.
  
Project Server 2013 basiert auf dem mit Microsoft Office Project Server 2007 eingeführten Framework und wird von Project Server 2010 erweitert. Project Server 2013 fügt ein clientseitiges Objektmodell (CSOM) hinzu, das von der Project Server-Schnittstelle (PSI) umgestaltet und vereinfacht wurde, und enthält eine JavaScript-Bibliothek und .NET Framework 4 Bibliotheken für Windows-apps, Windows Phone 8 und Microsoft Silverlight. Das CSOM ist für die Entwicklung für Project Online konzipiert und kann auch mit einer lokalen Project Server-Installation verwendet werden. 

Die Project Server-Datenbankenwerden zu einer einzigen Datenbank zusammengefasst. Sie können auf die Online Berichtstabellen und-Ansichten über einen OData-Dienst zugreifen. Die CSOM und der OData-Dienst enthalten eine Rest-Schnittstelle (Representational State Transfer). Project Server-Workflows können mithilfe von SharePoint Designer 2013 erstellt werden. Project Professional 2013 können in Project Server-Berichtsdaten, SharePoint-Aufgabenlisten und andere externe Inhalte mithilfe des Office-Add-ins-Erweiterbarkeitsmodells für Aufgabenbereiche integriert werden. Project Standard 2013 können Aufgabenbereich-Add-Ins verwenden, um Sie in allgemeine externe Inhalte zu integrieren.
  
Diagramme und weitere Informationen zu wichtigen Änderungen in Project Server 2013 finden Sie unter [Project Server 2013 Architecture](project-server-2013-architecture.md).
  
> [!NOTE]
> Project Server 2013 basiert auf der SharePoint Server 2013- Plattform; Project 2013 weist größtenteils dieselbe Infrastruktur wie die anderen Office 2013-Anwendungen auf. Informationen zur Dokumentation der Modell für SharePoint-Add-Ins, SharePoint-basierten Workflows, Webparts, zur Entwicklung mit anderen SharePoint-Features und zur Dokumentation von Office-Add-Ins finden Sie unter [SharePoint-Add-ins](https://docs.microsoft.com/sharepoint/dev/sp-add-ins/sharepoint-add-ins), [Office-Add-ins](https://docs.microsoft.com/office/dev/add-ins/overview/office-add-ins)und [SharePoint 2013-Entwicklungsübersicht](https://msdn.microsoft.com/library/jj164084%28office.15%29.aspx). 
  
## <a name="major-new-features-in-project-2013"></a>Wichtige neue Features in Project 2013
<a name="pj15_WhatsNew_MajorNewFeatures"> </a>

Zu den neuen Features in Project Standard 2013 und Project Professional 2013 gehören eine verbesserte Benutzeroberfläche, die mit anderen Office 2013-Anwendungen übereinstimmt, und unterstützt die moderne Benutzeroberfläche in Windows 8, Integration in Office-Grafikobjekte für Berichte, Burndown Berichte und neue Programmierfunktionen für Berichte. Project Professional 2013 ermöglicht eine umfassendere Freigabe und Synchronisierung von Projekten auf SharePoint Server 2013 sowie die Aufgabenbereich-Add-Ins, die auch in anderen Office 2013 Anwendungen wie Word, Excel und Outlook implementiert sind.
  
In Project Server 2013 gibt es viele neue Features. Einige haben keine wichtige Programmierbarkeit, wie beispielsweise die neue Zeitachse in Project Web App. Diese Features werden in der Produkt-und Endbenutzerdokumentation zu Microsoft Office Online und in Themen, die auf Administratoren und IT-Experten in Microsoft TechNet ausgerichtet sind, dokumentiert. Andere neue Features wie verbesserte Arbeitszeittabellen erleichtern Drittanbieterentwicklern die Interaktion mit Arbeitszeittabellen und dem Status über die Project Server-Schnittstelle (PSI).
  
Das Hinzufügen von Project Online und der Office Storehttps://office.microsoft.com/store) (für Projekt-Add-Ins sind weit reichende Änderungen, bei denen auf Project Server über Microsoft Azure zugegriffen werden kann. Der Cloud-basierte Zugriff auf Project Server verwendet ein clientseitiges Objektmodell (CSOM) für die Entwicklung von Add-Ins mit den Microsoft .NET Framework, Microsoft Silverlight, Windows Phone und Webanwendungen, die JavaScript verwenden. Eine Voraussetzung für Project Online ist, dass die vier Project Server-Datenbanken früherer Versionen in einer Datenbank zusammengeführt werden.
  
Project Server 2013 Leistung und Skalierbarkeit werden in vielen Bereichen wie Aufgabenstatus, Arbeitszeittabellen und Projektmanagement verbessert. Project Server-Workflows werden mit Version 4 von Windows Workflow Foundation (WF4) neu gestaltet. Die Verwendung der .NET Framework 4 und Windows Communication Foundation (WCF) mit dem PSI verbessert die Sicherheit, Leistung und Skalierbarkeit. Beispielsweise können Sie das Transportprotokoll von WCF-basierten Anwendungen mithilfe von Konfigurationsdateien ändern, ohne den Anwendungscode zu ändern oder neu zu kompilieren. In Project Web App werden viele PSI-Aufrufe zwischengespeichert, bei denen sich die Daten nicht erheblich ändern.
  
> [!NOTE]
> Für die Entwicklung mit Project Server 2013 können Sie Visual Studio mit den Office-und SharePoint-Tools-Erweiterungen verwenden, die systemeigene Add-Ins für die Office 2013 Produkte erstellen können. Project Server 2013 erfordert Visual Studio, um die Entwicklung von Features wie Projektdetailseiten und WCF-basierten Anwendungen vollständig zu ermöglichen. Die SharePoint-Tools-Erweiterungen in Visual Studio können Webparts und andere SharePoint-Features direkt für Project Web App und andere SharePoint-Websites bereitstellen. 
>
> Visual Studio ist nicht mehr erforderlich, um Project Server-Workflows zu entwickeln, die benutzerdefinierte Felder, Phasen, Phasen und Enterprise-Projekttypen verwenden, die in Project Web App verwaltet werden können. Sie können zwar Visual Studio zum Entwickeln von Workflows verwenden, diese werden jedoch häufig einfacher und schneller mithilfe von SharePoint Designer erstellt. Visual Studio können für Workflows verwendet werden, die Zugriff auf die CSOM oder andere externe APIs benötigen. 
  
### <a name="project-add-ins"></a>Project-Add-Ins
<a name="pj15_WhatsNew_Apps"> </a>

Die Verteilung und Vermarktung von Software wurde mit dem Konzept eines Add-ins revolutioniert. Für Project 2013 können Add-Ins zum erwerben und herunterladen aus dem öffentlichen Office Store oder in einem privaten Katalog in SharePoint bereitgestellt werden. Ein Add-in ist normalerweise ein eigenständiges, interaktives Programm, das eine kleine Anzahl verwandter Aufgaben ausführt. Ein Project-Add-in kann ein Aufgabenbereich-Add-in für die Project Standard 2013-oder Project Standard 2013-Clients oder ein Add-in für Project Server 2013 oder Project online sein.
  
Informationen zu Add-Ins für die Project-Desktop Clients finden Sie unter [Aufgabenbereich-Add-Ins in Project](#pj15_WhatsNew_Agave). Ein Project Server 2013 Beispiel finden Sie unter [Create a SharePoint-Hosted Project Server Add-in](create-a-sharepoint-hosted-project-server-add-in.md). Zusätzlich zu Artikeln im [Office-und SharePoint-Add-ins SDK](https://msdn.microsoft.com/library/fp161507.aspx)enthält der Office- [Blog](https://blogs.office.com/dev/) viele Beiträge, die auch für Project 2013 und Project Online relevant sind. 
  
Ein Add-in für Project Server 2013 kann sowohl mit einer lokalen Installation als auch mit Project Online funktionieren. Project Server-Add-Ins können Webparts, Remote-Ereignisempfänger und Geschäftslogik enthalten. Der Zugriff auf das Project Server-Objektmodell in einem Add-in erfolgt über die CSOM, nicht über die PSI. Der Datenspeicher kann Cloud-basiert sein, beispielsweise mit SQL Azure, externe wie über Microsoft Business Connectivity Services (BCS), intern mit einer lokalen Datenbank oder gemischten.
  
#### <a name="add-in-security"></a>Add-in-Sicherheit

Im Allgemeinen werden Aktionen, die ein Add-in ausführt, im Namen des Benutzers ausgeführt, der das Add-in ausführt; Sie verwenden nicht explizit den Identitätswechsel oder geben an, wer das Add-in ausführen kann. Aktionen dürfen die Berechtigungsstufe des Benutzers, der das Add-in ausführt, nicht überschreiten. 
  
In Office Developer Tools für Visual Studio 2012 verfügt die Datei AppManifext. XML über einen grafischen Editor, in dem Sie den Bereich für Berechtigungsanforderungen festlegen können. Um beispielsweise ein Add-in zu erstellen, mit dem Projektmanager Ihre Projekte aktualisieren können, wählen Sie auf der Registerkarte **Berechtigungen** des Bereichs **AppManifest. XML** -Designer **mehrere Projekte** für den Bereich aus, und **Schreiben** Sie für die Berechtigung. Wenn der Add-in-Benutzer über Project Manager-Berechtigungen verfügt, kann er das Add-in für von ihm verwaltete Projekte ausführen. Der Code in der Datei AppManifest. XML würde Folgendes umfassen: 
  
```XML
  <AppPermissionRequests>
    <AppPermissionRequest Scope="https://sharepoint/projectserver/projects" Right="Write" />
  </AppPermissionRequests>
```

**Tabelle 1. Berechtigungs Anforderungsbereiche für Project Server-Add-ins**

|Bereich|Berechtigungen|
|:-----|:-----|
|**Project Server** <br/> |**Verwalten** (erfordert Project Server-Administratorberechtigungen)  <br/> |
|**Mehrere Projekte** <br/> |**Lesen**, **Schreiben** (erfordert Projektmanager-Berechtigungen für einige Vorgänge; Projektteammitglieder Berechtigungen für grundlegende Lesevorgänge wie vorgangszuweisungen.)  <br/> |
|**Einzelnes Projekt** <br/> |**Lesen**, **Schreiben** (erfordert mindestens Berechtigungen für Projektteammitglieder; der Zugriff auf einige Daten in einem Projekt hängt von anderen Berechtigungsstufen ab.)  <br/> |
|**Enterprise-Ressourcen** <br/> |**Lesen**, **Schreiben** (erfordert Ressourcen-Manager-Berechtigungen.)  <br/> |
|**Statusing** <br/> |**SubmitStatus** (erfordert die Berechtigung zum Übermitteln des Status für Ihre Projekte.)  <br/> |
|**Berichterstellung** <br/> |**Lesen** (erfordert die Berechtigung zum Anmelden bei Project Server)  <br/> |
|**Workflow** <br/> |**Elevate** (erfordert die Berechtigung zum Ausführen von Workflows. Das Add-in wird mit erhöhten Berechtigungen ausgeführt, um Übergänge von Stage zu Stage in einem Workflow zu aktivieren. Die Geschäftslogik im Add-in steuert die Phasenübergänge.)  <br/> |
   
> [!NOTE]
> Project Server 2013 und Project Online verwenden nicht das nur-App-Authentifizierungsmodell in SharePoint 2013 (Weitere Informationen finden Sie unter [Add-in-Autorisierungsrichtlinientypen in SharePoint 2013](https://msdn.microsoft.com/library/124879c7-a746-4c10-96a7-da76ad5327f0%28Office.15%29.aspx)). 
  
Informationen zum entwickeln, verteilen, hosten und Verwalten von Add-Ins finden Sie unter [SharePoint-Add-ins](https://docs.microsoft.com/sharepoint/dev/sp-add-ins/sharepoint-add-ins) und [Office-Add-ins](https://docs.microsoft.com/office/dev/add-ins/overview/office-add-ins)und Verwandte Themen in der SharePoint Server 2013 und Office 2013 Entwicklerdokumentation. Informationen zum Bereich Berechtigungsanforderung für andere SharePoint-Add-Ins finden Sie unter [Add-in Permissions in SharePoint 2013](https://msdn.microsoft.com/library/5f7a8440-3c09-4cf8-83ec-c236bfa2d6c4%28Office.15%29.aspx).
  
### <a name="integrating-with-sharepoint-server"></a>Integrieren mit SharePoint Server
<a name="pj15_WhatsNew_IntegrationWSS"> </a>

Viele Features in Project Web App erfordern die neue Infrastruktur in SharePoint Server 2013 wie OAuth und anspruchsbasierte Authentifizierung, Project Server-Autorisierung und Berechtigungen über SharePoint-Gruppen, Synchronisierung von Projekten mit SharePoint-Aufgabe Listen und deklarative Workflows in Project Server. Die Project-Dienstanwendung kann einer beliebigen Websitesammlung in einer SharePoint-Farm zugeordnet werden. Die Projektsynchronisierung kann mit einer SharePoint-Aufgabenliste erfolgen, in der SharePoint das Projekt verwaltet. Ein Enterprise-Projekt kann auch mit einer SharePoint-Aufgabenliste synchronisiert werden, in der Project Server den Vollzugriff aufrecht erhält. Informationen zu Architekturdiagrammen und eine Erläuterung der Projektsynchronisierung finden Sie unter [Project Server 2013 Architektur](project-server-2013-architecture.md).
  
In SharePoint Server 2013 gibt es viele neue Features. Weitere Informationen finden Sie unter [SharePoint für Entwickler](https://msdn.microsoft.com/sharepoint).
  
### <a name="integrating-with-workflows"></a>Integrieren in Workflows
<a name="pj15_WhatsNew_Workflow"> </a>

Workflows sind ein Hauptfeature der Projektportfolioverwaltung. Ein Projektlebenszyklus kann lang andauernde Prozesse umfassen, die sich über mehrere Phasen erstrecken. Zu den Steuerungs Phasen zählen Projektvorschläge, Analysen der geschäftlichen Auswirkungen sowie auswählen, erstellen, planen, verwalten und Nachverfolgen von Projekten.
  
Project Server 2013 Workflows basieren auf der SharePoint 2013-Workflow Plattform, die WF4 verwendet. Im Gegensatz zu früheren Versionen können deklarative Workflows für Project Server 2013 mithilfe von SharePoint Designer 2013 erstellt werden und sind sowohl für die lokale als auch für die Online Nutzung zugänglich. Project Server-Workflows verwenden das SharePoint-Workflow Sicherheitsmodell mit OAuth und können auf einer Project Web App Website installiert werden. Abbildung 1 zeigt, dass SharePoint Designer 2013 Stufen zu einem Websiteworkflow für die Bedarfs Verwaltung hinzufügen können, wobei die Phasen in Project Web App definiert sind.
  
**Abbildung 1. Verwenden von SharePoint Designer zum Hinzufügen einer Phase zu einem Workflow für Project Web App**

![Hinzufügen einer Phase zu einem Workflow in SPD](media/pj15_CreateWorkflowSPD_AddStageInSPD.gif "Hinzufügen einer Phase zu einem Workflow in SPD")

<br/>

Sie erstellen einen deklarativen Workflow, indem Sie workflowstufen, Aktionen, Bedingungen und andere Elemente in einem Entwurfstool hinzufügen, das entweder SharePoint Designer 2013 oder Visual Studio 2012 sein kann. Das Entwurfstool speichert dann den Workflow als XAML-Code, der zur Laufzeit interpretiert wird. Deklarative Workflows können entweder in Project Server 2013 lokal oder in Project online ausgeführt werden. Mithilfe von Visual Studio 2012 können Sie auch benutzerdefinierte Aktionen und Formulare für zusätzliche Steuerelemente erstellen und Workflowvorlagen zur Wiederverwendung mit mehreren Project Web App-Instanzen speichern. SharePoint Designer 2013 können benutzerdefinierte Aktionen verarbeiten, die in Visual Studio 2012 erstellt wurden.
  
Ein Project Server 2013-Workflow fungiert als APP, bei der ein Administrator, der über Entwurfsberechtigungen für Project Web App verfügt, einen deklarativen Workflow veröffentlichen und einem Enterprise-Projekttyp (EPT) zuordnen kann. Die EPT muss für ein Enterprise-Projekt gelten, in dem Project Server den Vollzugriff aufrecht erhält. In einer SharePoint-Aufgabenliste kann kein Project Server-Workflow verwendet werden. 
  
OAuth ermöglicht Projektmanagern mit Berechtigungen zum Erstellen von Projekten, den Workflow ohne Identitätswechsel aufzurufen. Workflow Aufrufe an Project Server, beispielsweise um einen benutzerdefinierten Feldwert zu lesen, um zu entscheiden, welche Verzweigung folgen soll, werden im Namen des Projektmanagers vorgenommen. Um zu verhindern, dass der Projektmanager einen Workflow erstellt, der automatisch zur nächsten Stufe wechselt, wird der Aufruf zum Wechseln zur nächsten workflowstufe als Workflowautor (Administrator) ausgeführt. Im Gegensatz dazu führen Benutzer von älteren Project Server 2010-Workflows imitierte Anrufe über das Workflow-Proxy Benutzerkonto durch, um den Administratorzugriff über den gesamten Workflow hinweg zu erhalten.
  
Obwohl Project Server 2013 lokal kompilierte WF 3.5-basierte Workflows verwenden kann, wird empfohlen, dass Sie ältere Workflows auf deklarative Workflows basierend auf WF4 aktualisieren. Die neuere Technologie ist skalierbarer und robuster. Geschäftsanalysten und Mitarbeiter von PMO können Workflow Designs mithilfe von Visio 2013 erstellen oder aktualisieren und Project Server-Workflows ohne Codierung mithilfe von SharePoint Designer 2013 implementieren.
  
Informationen zum Erstellen eines deklarativen Workflows für Project Web App finden Sie unter [Erste Schritte beim Entwickeln von Project Server-Workflows](getting-started-developing-project-server-workflows.md). Einen Vergleich der SharePoint Designer-und Visual Studio Funktionen für Workflows finden Sie unter [develop SharePoint 2013 Workflows using Visual Studio](https://msdn.microsoft.com/library/office/jj163199.aspx).
  
### <a name="client-side-object-model"></a>Clientseitiges Objektmodell
<a name="pj15_WhatsNew_CSOM"> </a>

Für den programmgesteuerten Zugriff auf Project Online ist ein CSOM erforderlich, das auf dem SharePoint-CSOM basiert. Project Online Authentifizierung erfolgt mit OAuth unter Verwendung einer Windows Live ID, nicht der Project Server-Formularauthentifizierung oder der Windows-Authentifizierung.
  
Im folgenden finden Sie die Grundsätze und Features des CSOM in Project Server 2013:
  
- Das CSOM ist für die einfache Verwendung konzipiert. Beispielsweise verwenden Methoden und Eigenschaften direkt oder Bereitstellen von Daten anhand des Namens, statt viele GUIDs, _changeXml_ -Parameter oder um Datasets zu übergeben. 
    
- Die Project Server-CSOM implementiert eine Teilmenge der PSI-Funktionalität basierend auf den am häufigsten verwendeten Anforderungen für Lösungen von Drittanbietern.
    
- Das CSOM-Element ruft intern die PSI auf, wird jedoch unterschiedlich berücksichtigt. Beispielsweise werden Aktualisierungen für alle Statusänderungen über die **StatusAssignmentCollection. SubmitAllStatusUpdates** -Methode und nicht durch die **Statusing. SubmitStatus** PSI-Methode für den Benutzer oder die **SubmitStatusForResource** -Methode für andere Ressourcen durchgeführt. 
    
- Auf die CSOM kann über einen WCF-Dienst (Client. svc) zugegriffen werden, statt über die 22 öffentlichen Dienste des PSI.
    
- Die Initialisierung des Project Server-CSOM erfolgt direkt über die [projectcontext](https://msdn.microsoft.com/library/Microsoft.ProjectServer.Client.ProjectContext.aspx) -Klasse mit der Project Web App-URL, nicht mithilfe eines WCF-Verweises oder einer Proxy-Assembly. 
    
- Das CSOM implementiert mehrere Clientbibliotheken und-Schnittstellen, die von der internen SharePoint CSOM-Infrastruktur unterstützt werden. Die Clientbibliotheken und-Schnittstellen umfassen Folgendes:
    
  - Microsoft .NET-Clientbibliothek in der Microsoft. projectserver. Client. dll-Assembly
    
  - Silverlight-Bibliothek in der Assembly "Microsoft. projectserver. Client. Silverlight. dll"
    
  - Windows Phone 8 Bibliothek in der Assembly "Microsoft. projectserver. Client. Phone. dll"
    
  - JavaScript-Bibliothek für Webanwendungen in der Datei "PS. js" oder "PS. Debug. js"
    
  - Rest-Endpunkte für den Zugriff mit dem OData-Protokoll
    
  - Systemeigene Unterstützung für LINQ-Abfragen mit Filterung, um die zurückgegebene Datenmenge einzuschränken
    
- Das CSOM kann sowohl für Project Online Lösungen als auch für lokale Lösungen verwendet werden, unabhängig von PSI und anderen Project Server-Assemblys wie Microsoft. Office. Project. Server. Library. dll.
    
- Zusätzliche Funktionen der Project Server 2013 CSOM können für kumulative Updates und Service Packs in Betracht gezogen werden, basierend auf Anfragen von Project Server-Partnern und der Entwicklercommunity.
    
> [!NOTE]
> Das CSOM ist die bevorzugte Schnittstelle für Project Server-Entwickler von Drittanbietern. Wir empfehlen, dass Sie für die Entwicklung neuer Anwendungen das CSOM verwenden, sofern das CSOM alle für Ihre Anwendung erforderlichen Funktionen umfasst. 
  
Informationen zum Entwickeln mit dem CSOM finden Sie unter [Client seitiges Objektmodell (CSOM) für Project 2013](client-side-object-model-csom-for-project-2013.md). Informationen zur Rest-Schnittstelle in SharePoint-Anwendungen finden Sie unter *Programmieren mit dem SharePoint Rest-Dienst* im SharePoint 2013: Dokumentation für Entwickler. 
  
### <a name="changes-in-the-reporting-database"></a>Änderungen in der Berichtsdatenbank
<a name="pj15_WhatsNew_RDBChanges"> </a>

Die vier Datenbanken in Project Server 2010 werden in Project Server 2013 in einer einzigen Projektdatenbank zusammengefasst. Der Standardname der Projektdatenbank lautet ProjectService. Berichtstabellen und-Ansichten behalten ihre vorherigen Namen bei, und Tabellen und Ansichten aus der Entwurfs-, Veröffentlichungs-und Archivdatenbank `draft`weisen `pub`die Präfixe und `ver` in der ProjectService-Datenbank auf. Beispielsweise ist die Tabelle veröffentlichter Projekte Pub. MSP_PROJECTS. 
  
> [!IMPORTANT]
> Der direkte Zugriff wird für die Tabellen und Ansichten`draft` Entwurf (Präfix),`pub`publiziert () und Archiv`ver`() nicht unterstützt. In Berichten sollten nur die Berichtstabellen und-Ansichten verwendet werden, `dbo` die über das Präfix verfügen. Beispielsweise wird die dbo. MSP_EpmProject Tabelle enthält die Liste der Projekte in der Project Web App-Instanz. 
>
> Es gibt nichts, das Sie aktiv daran hindert, den direkten programmgesteuerten Datenbankzugriff zu verwenden, um Daten in einer der Tabellen und Ansichten in der Projektdatenbank zu aktualisieren. Beachten Sie, dass der Project Professional Cache, die Tabellen für Entwurf und veröffentlichte Daten und die Berichtstabellen alle auf einem Cache Synchronisierungsprotokoll beruhen, das durch direkte Datenbearbeitung gestört werden kann. Wenn Sie Ihre Project Server-Datenbanken beschädigen oder Project Professional clientseitigen Caches mithilfe des direkten Zugriffs auf Änderungsdaten beschädigt haben, sollten Sie darauf hingewiesen werden, dass der Produktsupport Ihnen nicht helfen kann! 
  
Project Server 2013 stellt einen OData-Dienst für den Online-und lokalen Zugriff vor. Die Online Berichtstabellen und-Ansichten werden nur von der OData-Schnittstelle verfügbar gemacht. für die lokale Verwendung können Sie die OData-Schnittstelle verwenden oder direkt auf die Berichtstabellen und-Ansichten in der ProjectService-Datenbank in der SharePoint-Farm zugreifen. Project Online unterstützt keine Multitenant-Datenbank. Das bedeutet, dass mehrere Instanzen von Project Web App jeweils über eine eigene Projektdatenbank verfügen. Der OData-Dienst führt intern SQL-Abfragen für die Berichtstabellen und-Sichten aus und liefert eine XML-oder JSON-Nutzlast. Eine Einführung in den odata-Dienst für die Berichterstellung in Project Server 2013 und für die **ProjectData** -Schemareferenz finden Sie unter [ProjectData-Project odata Service Reference](https://msdn.microsoft.com/library/office/jj163015.aspx).
  
Allgemeine Informationen zu odata-Abfragen finden Sie unter [odata: URI Conventions](https://www.odata.org/documentation/). Beispielsweise können Sie alle Projekte in einer lokalen Instanz von Project Web App anzeigen, in der der Projektname mit "Test" beginnt, indem Sie die folgende Abfrage in einem Browser verwenden. Klicken Sie mit der rechten Maustaste auf die Browser Seite, und klicken Sie dann auf **Quelle anzeigen**.
  
```html
https://ServerName /ProjectServerName /_api/ProjectData/Projects?$filter=startswith(ProjectName, 'Test') eq true
```

Um Projektdaten in PowerPivot in Excel 2013 zu importieren, wählen Sie auf dem Menüband Daten im Dropdownmenü **aus andere Quellen** den Eintrag **OData-Daten Feed** aus. Geben https://ServerName/ProjectServerName/_api/ProjectData/ Sie im Dialogfeld **Datenverbindungs-Assistent** den Speicherort für den Daten Feed ein, wählen Sie **weiter**aus, und wählen Sie dann im Assistenten auf der Seite **Tabellen auswählen** die Tabelle **Projekte** aus. Name und speichern Sie die ODC-Datei, und wählen Sie dann **Fertig stellen**aus. Wählen Sie im Dialogfeld **Daten importieren** die Option **PivotTable-Bericht**aus. Wählen Sie im Excel-Arbeitsblatt Felder für die Pivot-Tabellenzeilen und-Spalten aus, die Sie anzeigen möchten.
  
Lokale Project Server-Benutzer, die über die richtigen Berechtigungen verfügen, können über Microsoft SQL Server direkt auf die Berichtstabellen und-Ansichten zugreifen, um Berichte wie in Project Server 2010 zu erstellen. In Project Server 2013 können Benutzer auch über die OData-Schnittstelle auf die lokalen Berichtstabellen zugreifen. Sie können Project Server-Daten online oder lokal über Rest-Endpunkte für den OData-Dienst abrufen. Beispielsweise wird die dbo. MSP_PROJECT Tabelle und der dbo. MSP_EpmProject_UserView Ansicht kann für Berichte verwendet werden. Alle Tabellen oder Sichten, die über `draft`ein `pub`,- `ver` oder-Präfix verfügen, sind nur für die interne Verwendung durch Project Server und nicht für die Verwendung in Berichten. Beispiel: der Entwurf. MSP_TASKS Tabelle und Pub. MSP_PROJECTS_WORKING_VIEW Ansicht sind nicht dokumentiert und dienen nur der internen Verwendung. 
  
> [!NOTE]
> Sie können die lokale Berichterstellung erweitern, indem Sie Tabellen, Ansichten, Felder und gespeicherte Prozeduren in einer separaten Datenbank hinzufügen. Sie sollten die vorhandenen Berichtstabellen und-Ansichten in der Project Server-Datenbank nicht ändern. 
  
Die Berichtstabellen, Ansichten und Felder in der Projektdatenbank werden in einer HTML-Hilfedatei in einem späteren Update des Project 2013 SDK-Downloads dokumentiert. Dokumentation des odata-XML-Schemas für den **ProjectData** -Dienst finden Sie unter [ProjectData-Project odata Service Reference](https://msdn.microsoft.com/library/office/jj163015.aspx). Abfragen der Berichtstabellen und Ansichten, die für Project Server 2010 erstellt wurden, arbeiten in den meisten Fällen mit der Project-Datenbank in Project Server 2013. Lokale Benutzer können auf die Project Server-OLAP-Cubes in SQL Server Analysis Services zugreifen, wie Sie dies derzeit tun. In Project Online stehen keine OLAP-Cubes zur Verfügung.
  
### <a name="task-pane-add-ins-in-project"></a>Aufgabenbereich-Add-Ins in Project
<a name="pj15_WhatsNew_Agave"> </a>

Sowohl Project Standard 2013 als auch Project Professional 2013 unterstützen Aufgabenbereich-Add-Ins, die zur Integration in und anzeigen externer Inhalte in einer Webseite verwendet werden können. Im Aufgabenbereich werden Webseiteninhalte angezeigt, die über JavaScript auf Aufgaben, Ressourcen, Ansichten und allgemeine Projektdaten zugreifen können. Das JavaScript-Objektmodell für Project kann Informationen über einen ausgewählten Vorgang oder eine ausgewählte Ressource abrufen und Daten in einer ausgewählten Zelle im Raster für Ansichten wie das Gantt-Diagramm abrufen. Aufgabenbereich-Add-Ins für Project können auch Ereignishandler für geänderte Ereignisse im Hinblick auf Vorgangs-, Ressourcen-oder Ansichtsauswahl implementieren. 
  
Abbildung 2 zeigt das Add-in **Hello ProjectData** -Aufgabenbereich, das den **ProjectData** -Dienst abfragt, und vergleicht dann Daten im aktuellen Projekt mit den Durchschnittswerten für alle Projekte. Der Project 2013 SDK-Download enthält den vollständigen Quellcode für das Add-in. 
  
**Abbildung 2. Ein Aufgabenbereich-Add-in in Project Professional kann auf Daten in Project Server zugreifen.**

![Vergleichen des aktuellen Projekts mit allen Projekten](media/pj15_RestQueryApp_CompareProject.gif "Vergleichen des aktuellen Projekts mit allen Projekten")
  
> [!NOTE]
> Project Standard 2013 können nicht direkt in Project Server 2013 über Aufgabenbereich-Add-Ins integriert werden. 
  
Aufgabenbereich-Add-Ins in Project Professional können Webparts unterstützen, die für Project Server 2013 erstellt wurden, sodass Entwickler eine Erweiterung einmal erstellen können, die sowohl mit Project Web App als auch mit Project Professional ausgeführt wird. Allgemeine Aufgabenbereich-Add-Ins, die für andere Office 2013 Produkte entwickelt wurden, können auch mit Project Standard 2013 und Project Professional 2013 verwendet werden. Weitere Informationen finden Sie unter [Aufgabenbereich-Add-Ins für Project](task-pane-add-ins-for-project.md).
  
### <a name="project-server-event-receivers"></a>Project Server-Ereignisempfänger
<a name="pj15_WhatsNew_Events"> </a>

In einer SharePoint-Farm, die die Back-End-Projektdienst Anwendung enthält, können mehrere Project Web App-Server (auch als "webfront-End-Server" oder "WFEs" bezeichnet) vorhanden sein. Ereignisempfänger werden auch Ereignishandler genannt. Lokale Ereignishandler können mit voll vertrauenswürdigem Code implementiert und auf allen WFEs für eine lokale Project Server-Installation bereitgestellt werden. Remote Ereignisempfänger können in Webdiensten auf lokalen oder Remoteservern implementiert werden, und es werden mehrere WFEs und mehrere Project Server-Installationen verwendet. Project Online können nur Remoteereignis Empfänger verwenden.
  
Project Server-Ereignishandler werden von SharePoint für jede Project Web App Instanz verwaltet, statt auf eine bestimmte Seite mit Project Web App Einstellungen. Klicken Sie in der Anwendung für die SharePoint-zentral Administration auf **Allgemeine Anwendungseinstellungen**, wählen Sie unter **PWA-Einstellungen** **Verwalten** , und wählen Sie dann in der Dropdownliste **Project Web App Instanz** auf der Seite PWA-Einstellungen die Instanz aus. Zum Hinzufügen eines lokalen Ereignishandlers oder eines Remoteereignis Empfängers wählen Sie **Server seitige Ereignis**Handler aus.
  
Für eine lokale Installation von Project Server können Sie einen Remoteereignis Empfänger als SharePoint-Feature erstellen, das die [Microsoft. projectserver. Client. EventHandlerCreationInformation](https://msdn.microsoft.com/library/Microsoft.ProjectServer.Client.EventHandlerCreationInformation.aspx) -Klasse in der CSOM verwendet und dann den Ereignisempfänger mithilfe von Methoden in der [eventhandlercollection](https://msdn.microsoft.com/library/Microsoft.ProjectServer.Client.EventHandlerCollection.aspx) -Klasse programmgesteuert verwaltet. Bei Remoteereignis Empfängern sind Prä-Ereignisse synchron, Post-Ereignisse asynchron und es gibt ein Timeout für Fälle, in denen der Remoteereignis Empfänger nicht zurückgegeben wird. 
  
> [!NOTE]
> Die SharePoint-zentral Administration steht nur für lokale Installationen zur Verfügung. Für Project Online und SharePoint Online können Sie Remoteereignis Empfänger mithilfe eines CSOM-basierten App-Pakets hinzufügen oder entfernen. 
  
Auf der Seite mit den Server seitigen Ereignishandlern ist der Prozess zum Hinzufügen eines lokalen Ereignishandlers für eine lokale Project Server-Installation fast identisch mit dem im Thema [Create a Project Server EventHandler beschriebenen Prozess und Protokollieren eines Ereignis](https://msdn.microsoft.com/library/gg615466.aspx) Themas für Project Server 2010. Der Unterschied besteht darin, dass die neue Seite des Ereignishandlers zusätzliche Optionen aufweist. Wählen Sie beispielsweise **Projekt erstellen** in der Liste **Ereignisse** aus, und wählen Sie dann **neuer Ereignis Handler**aus. Auf der Seite neuer Ereignishandler sind nur die beiden erforderlichen Felder **Name** und **Order** (siehe Abbildung 3). Wenn Sie einen lokalen voll vertrauenswürdigen Ereignishandler hinzufügen, fügen Sie das Feld **Assembly Name** und das Feld **Klassenname** hinzu. lassen Sie die **Endpunkt-URL** leer. Wenn Sie einen Remoteereignis Empfänger hinzufügen, fügen Sie die **Endpunkt-URL**hinzu, und lassen Sie den Namen und den **Klassennamen** der **Assembly** leer. 
  
> [!CAUTION]
> Wenn Sie sowohl den Namen der Assembly *als* auch den Klassennamen und die Endpunkt-URL angeben, ruft Project Server nur den lokalen Ereignishandler (lokal) auf. Der Remoteereignis Empfänger wird ignoriert. 
> 
> Wenn Sie zwei Ereignishandler für dasselbe Ereignis erstellen, wobei ein Ereignishandler lokal und einer der Remoteereignis Empfänger ist und der Wert für " **Order** " für beides identisch ist, ignoriert Project Server den Remoteereignis Empfänger. 
  
**Abbildung 3. Hinzufügen eines lokalen Ereignishandlers oder eines Remoteereignis Empfängers**

![Konfigurieren eines Ereignishandlers oder Ereignisempfängers](media/pj15_EventHandlers_NewEventHandler.gif "Konfigurieren eines Ereignishandlers oder Ereignisempfängers")
    
Wenn Sie Zugriff auf PSI-Datasets für einen lokalen Ereignishandler benötigen, können Sie die Microsoft. Office. Project. Schema. dll-Assembly aus dem Verzeichnis [Windows\_] \Microsoft.NET\assembly\GAC msil\microsoft.Office.Project.schema\v4.0_15.0.0.0__71e9bce111e9429c kopieren. 

Anstelle des PSI wird empfohlen, dass Sie die Ereignisklassen im **Microsoft. projectserver. Client** -Namespace verwenden; für die Entwicklung mit dem CSOM ist keine Manipulation von Datasets erforderlich. Zum Entwickeln von Remoteereignis Empfängern für Project Online müssen Sie die [Ereignis](https://msdn.microsoft.com/library/Microsoft.ProjectServer.Client.Event.aspx) Klasse und die [EventHandlerCreationInformation](https://msdn.microsoft.com/library/Microsoft.ProjectServer.Client.EventHandlerCreationInformation.aspx) -Klasse in der CSOM verwenden. 
  
Bevor Sie einen Project Server-Ereignishandler bereitstellen, müssen Sie den Ereignishandler gründlich in einer Testinstallation von Project Server installieren und testen. Wenn der lokale Ereignishandler, den Sie hinzufügen, in einer lokalen Project Server-Installation nicht mehr funktionsfähig ist, kann der Dienst für Project Server 2013 Ereignisse die anderen gültigen benutzerdefinierten Ereignishandler nicht laden. In diesem Fall müssen Sie den Ereignishandler "Problem" entfernen und den Ereignisdienst neu starten.
  
> [!NOTE]
> Für eine lokale Project Server-Installation empfehlen wir die Migration zu Remoteereignis Empfängern mithilfe der CSOM zum Entwickeln von Ereignisempfängern. Da Remoteereignis Empfänger keinen Code von Drittanbietern im Project Server-Ereignisdienst ausführen, sind Remoteereignis Empfänger stabiler. Lokale Administratoren werden von der Verantwortung für die Verwaltung des Project Server-Ereignis Diensts enthoben. 
  
Allgemeine Informationen zu Ereignissen finden Sie unter [Behandeln von Ereignissen in Apps für SharePoint](https://msdn.microsoft.com/library/jj220048%28office.15%29.aspx). 
  
## <a name="deprecated-features"></a>Veraltete Features
<a name="pj15_WhatsNew_Deprecated"> </a>

> [!NOTE]
> Informationen zu Features und APIs, die in Project Server 2016 Preview veraltet sind oder entfernt wurden, finden Sie unter [What es deprecated or removed in Project Server 2016 Preview](https://docs.microsoft.com/project/what-s-deprecated-or-removed-in-project-server-2016). 
  
Veraltete Features stehen in Project 2013 für einige Lösungen weiterhin zur Verfügung, sollten jedoch nicht für neue Entwicklungen verwendet werden. Die meisten der folgenden Features und Methoden funktionieren nicht mit Project Online oder mit der standardmäßigen lokalen Installation von Project Server 2013 im SharePoint-Berechtigungsmodus. Vorhandene Lösungen, die diese Features verwenden, funktionieren möglicherweise nicht für ein Upgrade von Project Server 2010 auf Project Server 2013. Obwohl Lösungen mit veralteten Features in einigen Fällen möglicherweise weiterhin funktionieren, werden Sie für alle Project 2013 Installationen nicht vollständig unterstützt.
  
Wenn Ihre Lösungen veraltete Features verwenden, sollten Sie vor der Bereitstellung sorgfältig getestet werden, und Sie sollten Sie so ändern, dass die unterstützten Features so schnell wie möglich verwendet werden. Informationen zum Konfigurieren der lokalen Project Server 2013 Sicherheit für den Project-Berechtigungsmodus finden Sie im Abschnitt *SharePoint-Berechtigungsmodus* unter [What es New for IT Pros in Project Server 2013](https://docs.microsoft.com/project/what-s-new-for-it-pros-in-project-server-2016).
  
- **Erweiterungen** [PSI-Erweiterungs Szenarien](https://docs.microsoft.com/previous-versions/office/developer/office-2010/ff843378(v=office.14)) sind veraltet und werden in zukünftigen Versionen nicht unterstützt. Diese lokalen Project Server 2013 Szenarien ermöglichen die Integration mithilfe von benutzerdefinierten Windows Communication Foundation (WCF) Diensten. 
  
- **Project PSI** Die [Project-Klasse](https://docs.microsoft.com/office/client-developer/project/project-psi-reference-overview) der PSI ist veraltet. Verwenden Sie für alle neuen Entwicklungen das [Projekt CSOM](client-side-object-model-csom-for-project-2013.md). Project Server 2013 apps, die das PSI-Projekt verwenden, sind weiterhin funktionsfähig, aber Project Online-apps müssen alle PSI-Methoden der Project-Klasse durch ihre äquivalenten CSOM-Methoden ersetzen.
  
- **Ressourcen Plan PSI** Der [Ressourcen Plan PSI](https://docs.microsoft.com/previous-versions/office/project-class/gg240019(v=office.15)) ist veraltet. Sie wird weiterhin für Project 2013 Entwicklung unterstützt, wird in zukünftigen Versionen jedoch nicht unterstützt. 
  
- **ASMX-Schnittstelle für PSI** Das PSI umfasst doppelte Schnittstellen für die Entwicklung lokaler Project Server-Erweiterungen. Die ASMX-Webdienste-Schnittstelle wurde mit der ersten Implementierung des PSI in Office Project Server 2007 eingeführt. Project Server 2010 wurde die Schnittstelle WCF-Dienste hinzugefügt, in der das Objektmodell die ASMX-Webdienste im wesentlichen dupliziert. Obwohl Project Server 2013 weiterhin sowohl ASMX als auch WCF unterstützt, sollten neue Lösungen, die das PSI erfordern, die WCF-Dienste verwenden. Wenn möglich, sollten neue Lösungen mithilfe der CSOM geschrieben werden. 
  
  Die ASMX-Webdienste des PSI sind in Project Server 2013 veraltet. Um in zukünftigen Project Server-Versionen zu arbeiten, müssen Lösungen, die die ASMX-Webdienste verwenden, umgeschrieben werden, um entweder die WCF-Dienste oder die CSOM zu verwenden. Weitere Informationen finden Sie im Abschnitt *Aktualisieren von Anwendungen mit dem Project Server-APIs* in [Project Server-Programmierbarkeit](project-server-programmability.md).
  
- **Object Link Provider (OLP)** In früheren Versionen von Project Server bietet der **ObjectLinkProvider** -Dienst in der PSI (siehe [WebSvcObjectLinkProvider](https://docs.microsoft.com/previous-versions/office/ms481347(v=office.14)) eine Möglichkeit zum Verwalten von Webobjekt Verknüpfungen zwischen Enterprise-Projektaufgaben und spezialisierten SharePoint-Listen im Projektwebsite für Probleme, Risiken, Lieferumfang und Dokumente. In Project Server 2013 ist die OLP veraltet. 
  
  Sie können die **[RelatedItemManager](https://docs.microsoft.com/previous-versions/office/sharepoint-server/jj168020(v=office.15))** -Klasse in der SharePoint-CSOM verwenden, um Webobjekt Verknüpfungen zwischen Elementen in der Aufgabenliste und den anderen Listen in einem Projektwebsite zu erstellen, zu lesen und zu löschen. Wenn Sie beispielsweise einen Link von einem Aufgabenelement zu einem Problem hinzufügen möchten, können Sie die **[AddSingleLink](https://docs.microsoft.com/previous-versions/office/sharepoint-server/jj166451(v=office.15))** -Methode oder eine von zwei ähnlichen Methoden, **AddSingleLinkFromUrl** oder **AddSingleLinkToUrl**, verwenden. Die **RelatedItemManager** -Klasse enthält auch Methoden zum Löschen einer Webobjekt Verknüpfung und lesen verwandter Elemente. Die entsprechende Klasse in der JSOM (das JavaScript-Objektmodell) finden Sie unter [SP. RelatedItemManager-Objekt (SP. js)](https://docs.microsoft.com/previous-versions/office/sharepoint-visio/jj838582(v=office.15)).
  
  Es wird empfohlen, dass Sie die SharePoint-CSOM verwenden, um OLP-Apps für eine lokale Installation von Project Server 2013 und Project online zu erstellen. Der [Microsoft. SharePoint](https://docs.microsoft.com/previous-versions/office/sharepoint-server/ms464984(v=office.15)) -Namespace enthält keine **RelatedItemManager** * * * *-Klasse. 
  
- **Benutzerdefinierte Berechtigungen** Benutzerdefinierte Sicherheitsberechtigungen für den Zugriff auf bestimmte Project Server-Features oder-Erweiterungen wurden in Office Project Server 2007 unterstützt, wobei in einem SDK-Artikel erklärt wurde, wie Sie diese erstellen, indem Sie die veröffentlichte Datenbank direkt ändern. In Project Server 2010 funktionieren benutzerdefinierte Berechtigungen weiterhin, sind jedoch veraltet. In Project Server 2013 funktionieren benutzerdefinierte Berechtigungen nicht mit dem standardmäßigen SharePoint-Berechtigungsmodus für lokale Installationen. Für den Project-Berechtigungsmodus werden benutzerdefinierte Berechtigungen unterstützt. Mit Project Online ist kein direkter Datenbankzugriff möglich. 
  
- **Identitätswechsel** Identitätswechsel in PSI-basierten apps, bei denen der Benutzer einer APP die Sicherheitsberechtigungen eines anderen Project Server-Benutzers übernehmen kann, ist in Project Server 2013 veraltet. Wie bereits erwähnt, verwendet eine lokale Standard Project Server 2013 Installation den SharePoint-Berechtigungsmodus, der den Identitätswechsel in den Project Server-Sicherheitsgruppen nicht zulässt. Weitere Informationen finden Sie unter [Authentication, authorization, and security in SharePoint 2013](https://docs.microsoft.com/sharepoint/dev/general-development/authentication-authorization-and-security-in-sharepoint).
  
  Status Anwendungen sind typische Erweiterungen, die möglicherweise den Identitätswechsel in früheren Versionen von Project Server verwendet haben. Project Server 2010 hat die **ReadStatusForResource** -Methode und die **SubmitStatusForResource** -Methode in der PSI sowie die globale **StatusBrokerPermission** -Berechtigung eingeführt, wodurch die Notwendigkeit eines Identitätswechsels zum Lesen und Aktualisieren des Status im Namen eines anderen Benutzers entfällt. Das CSOM in Project Server 2013 verwendet den zugrunde liegenden PSI, um Status Erweiterungen transparent zu aktivieren, und kann für Project Online oder lokale Installationen verwendet werden. 
  
- **Berichtsdaten Bank Erweiterungen** Das Hinzufügen von benutzerdefinierten Tabellen und Ansichten zur Berichtsdatenbank ist eine gängige Vorgehensweise für frühere Versionen von Project Server. Da Project Server 2013 die vier Datenbanken früherer Versionen in einer Datenbank kombiniert, übertragen Upgrades keine benutzerdefinierten Tabellen, Ansichten oder Sprocs an die Berichtstabellen in der Project Server 2013-Datenbank. 
  
  Es wird empfohlen, entweder SQL Azure oder eine separate SQL Server Datenbank für benutzerdefinierte Berichtstabellen und-Ansichten zu verwenden, in der Sie Datenbanksicherungen und-Aktualisierungen verwalten können. Für Project Online ist dies erforderlich.
  
- **Berichterstellung** Die lokalen Berichtstabellen und-Ansichten in der Project Server-Datenbank und die OLAP-Cubes sind *nicht* veraltet und werden weiterhin vollständig unterstützt. Die Berichtstabellen und-Ansichten (die Berichtsdatenbank in früheren Versionen von Project Server) sind in Project Online jedoch nicht verfügbar. Ähnlich sind OLAP-Cubes nur bei lokalen Installationen von Project Server 2013 verfügbar. Für Berichtsanwendungen mit Project Online können Sie den **ProjectData** -Dienst über Rest-Abfragen mit dem OData-Protokoll verwenden. 
  
- **Projektberater** Der Projektberater ist eine Standardfunktion in den Office Project 2007 Desktopanwendungen, wobei HTML-und JavaScript-Inhalte in einem Aufgabenbereich interaktive Anleitungen zum Erstellen und Verwalten von Projekten bieten. In Project 2010 ist der Projektberater in einer Standardinstallation nicht verfügbar, kann jedoch über VBA oder ein VSTO-Add-in aktiviert werden. Der Project 2010 SDK-Download enthält die geänderten Projektberater Dateien. 
  
  Das VBA-Objektmodell und das **Microsoft. Office. Interop. MSProject** -Objektmodell in Project 2013 enthalten weiterhin 22 Elemente der **Application** -Klasse und die **Project** -Klasse, die den Projektberater verwalten kann. Project 2013 Aufgabenbereich-Apps können jedoch mit Aktionen in einem Projektberater-Aufgabenbereich in Konflikt stehen, und Projektberater Inhalte können nicht einfach im Office Store verteilt oder verkauft werden. Es wird dringend empfohlen, dass Sie Projektaufgaben Bereich-Lösungen mit Office-Add-Ins, nicht mit benutzerdefinierten Projektberater Inhalten entwickeln. Weitere Informationen zum Projektberater finden Sie in der [Dokumentation zum Project 2010 SDK](https://msdn.microsoft.com/library/ms512767.aspx).
  
## <a name="comparing-project-server-on-premises-with-project-online"></a>Vergleich von Project Server lokal mit Project Online
<a name="pj15_WhatsNew_Comparing"> </a>

Um Sie bei der Entscheidung zu unterstützen, ob Project Server lokal oder Project Online verwendet werden kann und welche Arten von Erweiterungen Sie in beiden Fällen entwickeln können, vergleicht Tabelle 2 die erweiterbaren Features einer lokalen Installation von Project Server 2013 mit Project online. Tabelle 2 enthält keine Unterschiede bei der Bereitstellung, Verwaltung oder Verwendung. Weitere Informationen zu Project Online und Project Server 2013 finden Sie unter [Project 2013 for Developers](https://developer.microsoft.com/project/docs) and [Project Online](https://developer.microsoft.com/project).
  
**Tabelle 2. Erweiterbarkeit von Project Server lokal und Project Online**

| Feature |Project Server lokal | Project Online |
|:-----|:-----|:-----|
|**Programmierbarkeits** <br/> |CSOM-basierte apps; konsistentes Programmiermodell  <br/>-.Net, Silverlight, Windows Phone-Clientbibliotheken  <br/>-JavaScript-Bibliothek für benutzerdefinierte Seiten, Webparts und Menü Band Erweiterungen  <br/>-OData-und Rest-Protokolle<br/><br/> PSI-basierte apps; Komplexes Programmiermodell, kann auch Apps für Verwaltung, Portfolioanalyse, Benachrichtigungen, Sicherheit im Projektmodus, Warteschlangensystem und andere Bereiche erstellen.<br/><br/>PSI-Erweiterungen  <br/><br/>Benutzerdefinierte Berechtigungen mit Project Mode Security (veraltet)  <br/><br/>Identitätswechsel mit dem PSI (veraltet)  <br/><br/>Voll vertrauenswürdiger Code; Installieren von Erweiterungen in der SharePoint-Farm  <br/> |CSOM-basierte apps; konsistentes Programmiermodell  <br/>-.Net, Silverlight, Windows Phone-Clientbibliotheken<br/>-JavaScript-Bibliothek für benutzerdefinierte Seiten, Webparts und Menü Band Erweiterungen<br/>-OData-und Rest-Protokolle<br/><br/>Das PSI kann verwendet werden, wird jedoch nicht unterstützt: keine OAuth und keine Dienst-zu-Dienst-Verbindungen<br/><br/>Keine Erweiterungen der CSOM-API<br/><br/>Keine benutzerdefinierten Berechtigungen<br/><br/>Kein Identitätswechsel<br/><br/>Kein voll vertrauenswürdiger Code  <br/> |
|**Benutzerdefinierte Datenbanken** <br/> |-SQL Azure  <br/>-SQL Server (die Änderung von Berichtstabellen und Ansichten in der Project Server-Datenbank wird nicht unterstützt)  <br/> |-SQL Azure  <br/>-SQL Server (die Änderung von Berichtstabellen und Ansichten in der Project Server-Datenbank wird nicht unterstützt)  <br/> |
|**Berichterstellung** <br/> |- **ProjectData** -Dienst; OData-und Rest-Protokolle  <br/>-Melden von Tabellen und Ansichten in der Project Server-Datenbank<br/>-OLAP-Datenbank  <br/> |- **ProjectData** -Dienst; OData-und Rest-Protokolle  <br/> |
|**Ereignishandler** <br/> |-Remote Ereignisempfänger, auf die über WCF-Endpunkte zugegriffen werden kann<br/>-Voll vertrauenswürdige Ereignishandler, die in der SharePoint-Farm installiert sind  <br/> | -Remote Ereignisempfänger, auf die über WCF-Endpunkte zugegriffen werden kann  <br/> |
|**Workflows** <br/> |Deklarative Workflows, erstellt mit SharePoint Designer 2013<br/>-Nur für eine bestimmte Project Web App Instanz verwenden<br/>-Kann ein Workflow Design aus Visio 2013 importieren<br/>-Kann benutzerdefinierte Aktionen importieren und verwenden<br/><br/> Deklarative Workflows, erstellt mit Visual Studio 2012<br/>-Erstellen einer APP, die Workflows enthalten kann<br/>-Erstellen eines SharePoint-Lösungspakets (WSP), das Workflows enthalten kann<br/>-Erstellen von Workflowvorlagen zur Wiederverwendung<br/>-Erstellen und Verwenden von benutzerdefinierten Aktionen  <br/><br/>Kann ältere kompilierte Workflows verwenden, die mit WF 3.5 erstellt wurden (Empfehlung: Upgrade auf deklarativen WF4-Workflow)  <br/> |Deklarative Workflows, erstellt mit SharePoint Designer 2013<br/>-Nur für eine bestimmte Project Web App Instanz verwenden<br/>-Kann ein Workflow Design aus Visio 2013 importieren<br/>-Kann benutzerdefinierte Aktionen importieren und verwenden  <br/><br/>Deklarative Workflows, erstellt mit Visual Studio 2012<br/>-Erstellen einer APP, die Workflows enthalten kann  <br/>-Erstellen eines SharePoint-Lösungspakets (WSP), das Workflows enthalten kann<br/>-Erstellen von Workflowvorlagen zur Wiederverwendung <br/>-Erstellen und Verwenden von benutzerdefinierten Aktionen  <br/> |
|**Verteiler** <br/> |-Office Store (für CSOM-basierte Apps)<br/>-Privater App-Katalog unter SharePoint<br/>-Intranet-Dateifreigabe  <br/> |-Office Store<br/>-Privater App-Katalog unter SharePoint  <br/> |

   
## <a name="conclusion"></a>Schlussbemerkung
<a name="pj15_WhatsNew_Conclusion"> </a>

Project Server 2013 bietet eine Vielzahl von neuen Entwicklungsfunktionen und Szenarien, mit denen Partner und Kunden die Funktionen und den Nutzen von Project Server in großen Unternehmen und in kleinen Organisationen anpassen und erweitern können. Sie können die Infrastruktur für Office 2013 und SharePoint 2013 verwenden, um Apps für Project 2013 zu erstellen und zu verteilen, die die Marktstellung und die Verwendung benutzerdefinierter Anwendungen erheblich erweitern können. Einige Erweiterbarkeitsfeatures und-Methoden früherer Versionen sind in Project 2013 veraltet, insbesondere die ASMX-Webdienste des PSI und Features, die Identitätswechsel oder direkte Datenbankänderungen beinhalten, die nicht mit Project Online verwendet werden können.
  
Die Einführung des CSOM ermöglicht den programmgesteuerten Zugriff auf Project Online für eine Vielzahl von Geräten und unter Verwendung von JavaScript in Webanwendungen. Das CSOM bietet ein konsistenteres Programmiermodell im Vergleich zum PSI. Auf Project Server-Daten kann auf vielfältige Weise zugegriffen werden als in früheren Versionen, einschließlich über den Online-OData-Dienst und über Rest-Endpunkte für Berichtsdaten in der Projektdatenbank. Vorhandene Berichte funktionieren weiterhin auf die gleiche Weise für die lokale Verwendung; neue Berichte haben mehr Flexibilität.
  
Office-Add-Ins bieten eine neue Allee für den Verkauf von Lösungen und die Integration von Project Standard 2013 mit Webinhalten und anderen Office 2013-Produkten. Sie können auch neue Möglichkeiten zum Integrieren von Project Professional 2013 mit Project Server-Daten und SharePoint-Listen über Aufgabenbereich-Office-Add-Ins erstellen.
  
Weitere Informationen zum Entwickeln von apps und zur Verwendung der Programmierfeatures und der CSOM SharePoint Server 2013 finden Sie unter [SharePoint für Entwickler](https://docs.microsoft.com/sharepoint/dev/) und [Office für Entwickler](https://developer.microsoft.com/office/docs).
  
## <a name="see-also"></a>Siehe auch

- [Project Server 2013-Architektur](project-server-2013-architecture.md)  
- [Project-Programmieraufgaben](project-programming-tasks.md) 
- [Clientseitiges Objektmodell (CSOM) für Project 2013](client-side-object-model-csom-for-project-2013.md) 
- [ProjectData – OData-Dienstreferenz für Project](https://msdn.microsoft.com/library/office/jj163015.aspx)  
- [Aufgabenbereich-Add-Ins für Project](task-pane-add-ins-for-project.md)   
- [OData: URI-Konventionen](https://www.odata.org/documentation/uri-conventions#FilterSystemQueryOption)    
- [SharePoint für Entwickler](https://msdn.microsoft.com/sharepoint)    
- [Office für Entwickler](https://msdn.microsoft.com/office)   
- [Behandeln von Ereignissen in Apps für SharePoint](https://msdn.microsoft.com/library/jj220048%28office.15%29.aspx)   
- [AppSource](https://appsource.microsoft.com/marketplace/apps?product=office)   
- [Project Online](https://developer.microsoft.com/project)
    

