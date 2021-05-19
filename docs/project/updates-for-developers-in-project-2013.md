---
title: Updates für Entwickler in Project
manager: lindalu
ms.date: 12/03/2019
ms.audience: Developer
localization_priority: Normal
ms.assetid: 5b2b22cd-6e28-43a8-9092-b411da8bfb53
description: Zu den neuen Features gehören ein clientseitiges Objektmodell (CSOM), REST-Schnittstellen, ein OData-Dienst für die Berichterstellung, Remoteereignisempfänger, deklarative Workflows und Aufgabenbereich-Add-Ins für Project Clients.
ms.openlocfilehash: c2bc0b475639a8582422b2091169116428367c60
ms.sourcegitcommit: 37080eb0087261320e24e6f067e5f434a812b2d2
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/04/2019
ms.locfileid: "39819280"
---
# <a name="updates-for-developers-in-project"></a>Updates für Entwickler in Project

Erweiterbarkeitsfeatures in Project Server 2013 funktionieren mit Add-Ins für Project Online und mit lokalen Installationen. Zu den neuen Features gehören ein clientseitiges Objektmodell (CSOM), REST-Schnittstellen, ein OData-Dienst für die Berichterstellung, Remoteereignisempfänger, deklarative Workflows und Aufgabenbereich-Add-Ins für Project Clients. Erfahren Sie auch mehr über veraltete Features, die nicht für die Neuentwicklung verwendet werden sollten.
  
Project Server 2013 baut auf dem framework auf, das mit Microsoft Office Project Server 2007 eingeführt und von Project Server 2010 erweitert wurde. Project Server 2013 fügt ein clientseitiges Objektmodell (CSOM) hinzu, das von der Project Server Interface (PSI) umgestaltet und vereinfacht wird und eine JavaScript-Bibliothek und .NET Framework 4 Bibliotheken für Windows-Apps, Windows Phone 8 und Microsoft Silverlight enthält. Das CSOM ist für die Entwicklung von Project Online konzipiert und kann auch mit einer lokalen Serverinstallation Project werden. 

Die Project Serverdatenbanken werden in einer einzigen Datenbank kombiniert. Sie können über einen OData-Dienst auf die Onlineberichtstabellen und -ansichten zugreifen. Das CSOM und der OData-Dienst enthalten eine Representational State Transfer (REST)-Schnittstelle. Project Serverworkflows können mithilfe von SharePoint Designer 2013 erstellt werden. Project Professional 2013 kann mithilfe des Office-Add-Ins-Erweiterbarkeitsmodells für Aufgabenbereiche in Project Server-Berichtsdaten, SharePoint-Aufgabenlisten und andere externe Inhalte integriert werden. Project Standard 2013 kann Aufgabenbereich-Add-Ins für die Integration in allgemeine externe Inhalte verwenden.
  
Diagramme und weitere Informationen zu wichtigen Änderungen in Project Server 2013 finden Sie unter [Project Server 2013 architecture](project-server-2013-architecture.md).
  
> [!NOTE]
> Project Server 2013 basiert auf der SharePoint Server 2013- Plattform; Project 2013 weist größtenteils dieselbe Infrastruktur wie die anderen Office 2013-Anwendungen auf. Eine Dokumentation des Modells für SharePoint-Add-Ins, SharePoint-basierte Workflows, Webparts, Entwicklung mit anderen SharePoint-Features und Dokumentation zu Office-Add-Ins finden Sie unter [SharePoint Add-Ins](https://docs.microsoft.com/sharepoint/dev/sp-add-ins/sharepoint-add-ins), [Office-Add-Ins](https://docs.microsoft.com/office/dev/add-ins/overview/office-add-ins)und [SharePoint 2013-Entwicklungsübersicht](https://msdn.microsoft.com/library/jj164084%28office.15%29.aspx). 
  
## <a name="major-new-features-in-project-2013"></a>Wichtige neue Features in Project 2013
<a name="pj15_WhatsNew_MajorNewFeatures"> </a>

Neue Features in Project Standard 2013 und Project Professional 2013 umfassen eine verbesserte Benutzeroberfläche, die anderen Office 2013-Anwendungen entspricht und die benutzeroberfläche für moderne Stile in Windows 8, die Integration in Office Art-Objekte für Berichte, Burndownberichte und neue Programmierbarkeitsfeatures für Berichte unterstützt. Project Professional 2013 ermöglicht eine umfangreichere Freigabe und Synchronisierung von Projekten auf SharePoint Server 2013 sowie die Aufgabenbereich-Add-Ins, die auch in anderen Office 2013-Anwendungen wie Word, Excel und Outlook implementiert sind.
  
Es gibt viele neue Features in Project Server 2013. Einige verfügen nicht über eine wichtige Programmierbarkeitsgeschichte, z. B. die neue Zeitachse in Project Web App. Diese Features werden in der Produkthilfe und der Endbenutzerdokumentation auf Microsoft Office Online und in Themen dokumentiert, die für Administratoren und IT-Experten auf Microsoft TechNet vorgesehen sind. Andere neue Features, z. B. verbesserte Arbeitszeittabellen, erleichtern Entwicklern von Drittanbietern die Interaktion mit Arbeitszeittabellen und statusing über die Project Server Interface (PSI).
  
Das Hinzufügen von Project Online und Office Store ( für Project-Add-Ins sind weitreichende Änderungen, bei denen auf Project Server über eine https://office.microsoft.com/store) Microsoft Azure. Der cloudbasierte Zugriff auf Project Server verwendet ein clientseitiges Objektmodell (CSOM) für die Entwicklung von Add-Ins mit microsoft .NET Framework, Microsoft Silverlight, Windows Phone und Web-Apps, die JavaScript verwenden. Eine Voraussetzung für Project Online ist, dass die vier Project Serverdatenbanken früherer Versionen in einer Datenbank zusammengeführt werden.
  
Project Die Leistung und Skalierbarkeit von Server 2013 wird in vielen Bereichen wie Vorgangsstatus, Arbeitszeittabellen und Projektverwaltung verbessert. Project Serverworkflows wurden mit Version 4 von Windows Workflow Foundation (WF4) neu gestaltet. Die Verwendung der .NET Framework 4 und Windows Communication Foundation (WCF) mit der PSI verbessert Sicherheit, Leistung und Skalierbarkeit. Beispielsweise können Sie das Transportprotokoll von WCF-basierten Anwendungen mithilfe von Konfigurationsdateien ändern, ohne den Anwendungscode zu ändern oder neu zu kompilieren. Project Web App speichert viele PSI-Aufrufe zwischen, bei denen sich die Daten nicht wesentlich ändern.
  
> [!NOTE]
> Für die Entwicklung mit Project Server 2013 können Sie Visual Studio mit den Office- und SharePoint-Toolserweiterungen verwenden, die nativ Add-Ins für die Office 2013-Produkte erstellen können. Project Server 2013 erfordert Visual Studio, um die Entwicklung von Features wie Projektdetailseseiten und WCF-basierten Anwendungen vollständig zu ermöglichen. Die SharePoint tools extensions in Visual Studio können Webparts und andere SharePoint-Features direkt für Project Web App und andere SharePoint bereitstellen. 
>
> Visual Studio ist nicht mehr erforderlich, um Project Server-Workflows zu entwickeln, die benutzerdefinierte Felder, Phasen, Phasen und Unternehmensprojekttypen verwenden, die in Project Web App verwaltet werden können. Obwohl Sie workflows Visual Studio können, sind sie häufig einfacher und schneller mithilfe von SharePoint zu erstellen. Visual Studio kann für Workflows verwendet werden, die Zugriff auf das CSOM oder andere externe APIs erfordern. 
  
### <a name="project-add-ins"></a>Project-Add-Ins
<a name="pj15_WhatsNew_Apps"> </a>

Die Verteilung und Vermarktung von Software wurde mit dem Konzept eines Add-Ins revolutioniert. For Project 2013, add-ins can be available for purchase and download from the public Office Store or distributed within a private catalog on SharePoint. Ein Add-In ist in der Regel ein eigenständiges, interaktives Programm, das eine kleine Anzahl verwandter Aufgaben ausführt. Ein Project kann ein Aufgabenbereich-Add-In für die clients Project Standard 2013 oder Project Standard 2013 oder ein Add-In für Project Server 2013 oder Project Online.
  
Informationen zu Add-Ins für Project Desktopclients finden Sie unter [Aufgabenbereich-Add-Ins in Project](#pj15_WhatsNew_Agave). Ein Beispiel Project Server 2013 finden Sie unter [Create a SharePoint-hosted Project Server add-in](create-a-sharepoint-hosted-project-server-add-in.md). Neben Artikeln im [Office- und SharePoint-Add-Ins-SDK](https://msdn.microsoft.com/library/fp161507.aspx)enthält der [Office-Blog](https://blogs.office.com/dev/) viele Beiträge, die auch für Project 2013 und Project Online. 
  
Ein Add-In für Project Server 2013 kann sowohl mit einer lokalen Installation als auch mit Project Online. Project Server-Add-Ins können Webparts, Remoteereignisempfänger und Geschäftslogik enthalten. Der Zugriff auf Project Server-Objektmodell in einem Add-In wird über das CSOM und nicht über die PSI ausgeführt. Datenspeicherung kann cloudbasierter sein, z. B. mit SQL Azure, extern, z. B. über Microsoft Business Connectivity Services (BCS), intern mit einer lokalen Datenbank oder gemischt.
  
#### <a name="add-in-security"></a>Add-In-Sicherheit

Im Allgemeinen werden Aktionen, die von einem #A0 ausgeführt werden, im Namen des Benutzers ausgeführt, der das #A1 ausgeführt hat. Sie verwenden nicht explizit den Identitätswechsel oder geben an, wer das Add-In ausführen kann. Aktionen dürfen die Berechtigungsstufe des Benutzers, der das Add-In ausgeführt hat, nicht überschreiten. 
  
In Office Developer Tools for Visual Studio 2012 verfügt die AppManifext.xml-Datei über einen grafischen Editor, in dem Sie den Berechtigungsanforderungsbereich festlegen können. Wenn Sie beispielsweise ein Add-In erstellen möchten, mit dem  Projektmanager ihre Projekte aktualisieren können,  wählen Sie auf  der Registerkarte Berechtigungen im **DesignerbereichAppManifest.xml** mehrere Projekte für den Bereich aus, und schreiben Sie für die Berechtigung. Wenn der Add-In-Benutzer über Projektmanagerberechtigungen verfügt, kann er das Add-In für Projekte ausführen, die sie verwaltet. Der Code in der AppManifest.xml würde Folgendes enthalten: 
  
```XML
  <AppPermissionRequests>
    <AppPermissionRequest Scope="https://sharepoint/projectserver/projects" Right="Write" />
  </AppPermissionRequests>
```

**Tabelle 1. Berechtigungsanforderungsbereich für Project Server-Add-Ins**

|Bereich|Berechtigungen|
|:-----|:-----|
|**Project Server** <br/> |**Verwalten** (Erfordert Project Serveradministratorberechtigungen.)  <br/> |
|**Mehrere Projekte** <br/> |**Read**, **Write** (Erfordert Projektmanagerberechtigungen für einige Vorgänge; Berechtigungen für Projektteammitglied für grundlegende Lesevorgänge, z. B. Aufgabenzuweisungen).)  <br/> |
|**Einzelne Project** <br/> |**Read**, **Write** (Erfordert mindestens Berechtigungen für Projektteammitglied; der Zugriff auf einige Daten in einem Projekt hängt von anderen Berechtigungsstufen ab.)  <br/> |
|**Enterprise Ressourcen** <br/> |**Read**, **Write** (Erfordert Ressourcen-Manager-Berechtigungen.)  <br/> |
|**Statusing** <br/> |**SubmitStatus** (Erfordert die Berechtigung zum Übermitteln des Status für Ihre Projekte.)  <br/> |
|**Berichterstellung** <br/> |**Read** (Erfordert die Berechtigung zum Anmelden Project Server.)  <br/> |
|**Workflow** <br/> |**Elevate** (Erfordert die Berechtigung zum Ausführen von Workflows. Das Add-In wird mit erhöhten Berechtigungen ausgeführt, um Übergänge von Phase zu Stufe in einem Workflow zu ermöglichen. Geschäftslogik im Add-In steuert Übergänge in der Phase.)  <br/> |
   
> [!NOTE]
> Project Server 2013 und Project Online verwenden nicht das Authentifizierungsmodell nur für Apps in SharePoint 2013 (siehe [Add-In-Autorisierungsrichtlinientypen in SharePoint 2013](https://msdn.microsoft.com/library/124879c7-a746-4c10-96a7-da76ad5327f0%28Office.15%29.aspx)). 
  
Informationen zum Entwickeln, Verteilen, Hosten und Verwalten von Add-Ins finden Sie unter [SharePoint Add-Ins](https://docs.microsoft.com/sharepoint/dev/sp-add-ins/sharepoint-add-ins) und [Office-Add-Ins](https://docs.microsoft.com/office/dev/add-ins/overview/office-add-ins)sowie verwandte Themen in der Entwicklerdokumentation zu SharePoint Server 2013 und Office 2013. Informationen zum Berechtigungsanforderungsbereich für andere SharePoint-Add-Ins finden Sie unter [Add-In permissions in SharePoint 2013](https://msdn.microsoft.com/library/5f7a8440-3c09-4cf8-83ec-c236bfa2d6c4%28Office.15%29.aspx).
  
### <a name="integrating-with-sharepoint-server"></a>Integration in SharePoint Server
<a name="pj15_WhatsNew_IntegrationWSS"> </a>

Viele Features in Project Web App erfordern die neue Infrastruktur in SharePoint Server 2013, z. B. OAuth und anspruchsbasierte Authentifizierung, Project Serverautorisierung und Berechtigungen über SharePoint-Gruppen, Synchronisierung von Projekten mit SharePoint-Aufgabenlisten und deklarative Workflows von Project Server. Die Project-Dienstanwendung kann jeder Websitesammlung in einer SharePoint zugeordnet werden. Project Synchronisierung kann mit einer SharePoint werden, in der SharePoint das Projekt verwaltet. Ein Unternehmensprojekt kann auch mit einer SharePoint synchronisiert werden, in der Project Server die volle Kontrolle behält. Architekturdiagramme und eine Erläuterung der Projektsynchronisierung finden Sie unter [Project Server 2013-Architektur](project-server-2013-architecture.md).
  
Es gibt viele neue Features in SharePoint Server 2013. Weitere Informationen finden Sie [unter SharePoint für Entwickler](https://msdn.microsoft.com/sharepoint).
  
### <a name="integrating-with-workflows"></a>Integrieren in Workflows
<a name="pj15_WhatsNew_Workflow"> </a>

Workflows sind ein Hauptfeature der Projektportfolioverwaltung. Ein Projektlebenszyklus kann lange laufende Prozesse umfassen, die viele Phasen umfassen. Zu den Steuerungsphasen gehören Projektvorschläge, Analysen der Geschäftlichen Auswirkungen sowie das Auswählen, Erstellen, Planen, Verwalten und Nachverfolgen von Projekten.
  
Project Server 2013-Workflows bauen auf der SharePoint 2013-Workflowplattform auf, die WF4 verwendet. Im Gegensatz zu früheren Versionen können deklarative Workflows für Project Server 2013 mithilfe von SharePoint Designer 2013 erstellt werden und können sowohl lokal als auch online verwendet werden. Project Serverworkflows verwenden SharePoint Workflowsicherheitsmodell mit OAuth und können auf einer Project Installiert werden. Abbildung 1 zeigt, dass SharePoint Designer 2013 einem Websiteworkflow für die Bedarfsverwaltung Stufen hinzufügen kann, in denen die Phasen in Project Web App definiert sind.
  
**Abbildung 1. Verwenden SharePoint Designers zum Hinzufügen einer Phase zu einem Workflow für Project Web App**

![Hinzufügen einer Phase zu einem Workflow in SPD](media/pj15_CreateWorkflowSPD_AddStageInSPD.gif "Hinzufügen einer Phase zu einem Workflow in SPD")

<br/>

Sie erstellen einen deklarativen Workflow, indem Sie Workflowphasen, Aktionen, Bedingungen und andere Elemente in einem Entwurfstool hinzufügen, das entweder SharePoint Designer 2013 oder Visual Studio 2012 sein kann. Anschließend speichert das Entwurfstool den Workflow als XAML-Code, der zur Laufzeit interpretiert wird. Deklarative Workflows können entweder lokal oder in Project Server 2013 Project Online. Mithilfe von Visual Studio 2012 können Sie auch benutzerdefinierte Aktionen und Formulare für zusätzliche Steuerung erstellen und Workflowvorlagen für die Wiederverwendung mit mehreren Project Web App-Instanzen speichern. SharePoint Designer 2013 kann benutzerdefinierte Aktionen verwenden, die in Visual Studio 2012 erstellt werden.
  
Ein Project Server 2013-Workflow fungiert als App, in der ein Administrator , der über Entwurfsberechtigungen für Project Web App verfügt, einen deklarativen Workflow veröffentlichen und einem Unternehmensprojekttyp (EPT) zuordnen kann. Die EPT muss für ein Unternehmensprojekt verwendet werden, bei dem Project Server die volle Kontrolle behält. Eine SharePoint Aufgabenliste kann keinen Project Serverworkflows verwenden. 
  
OAuth ermöglicht Projektmanagern, die über Berechtigungen zum Erstellen von Projekt verfügen, das Aufrufen des Workflows ohne Identitätswechsel. Workflowaufrufe an Project Server, z. B. zum Lesen eines benutzerdefinierten Feldwerts, um zu entscheiden, welche Verzweigung folgen soll, werden im Auftrag des Projektmanagers ausgeführt. Um zu verhindern, dass der Projektmanager einen Workflow erstellt, der automatisch in die nächste Phase vorgesetzt wird, wird der Aufruf für den Wechsel zur nächsten Workflowphase als Workflowautor (der Administrator) ausgeführt. Im Gegensatz dazu werden Benutzer von Project Server 2010-Workflows imitierte Aufrufe über das Workflowproxybenutzerkonto ausführen, um über den gesamten Workflow Administratorzugriff zu erhalten.
  
Obwohl Project Server 2013 lokal kompilierte WF3.5-basierte Workflows verwenden kann, wird empfohlen, ältere Workflows auf deklarative Workflows basierend auf WF4 zu aktualisieren. Die neuere Technologie ist skalierbarer und robuster. Business analysts and PMO staff can create or update workflow designs by using Visio 2013 and implement Project Server workflows without coding by using SharePoint Designer 2013.
  
Informationen zum Erstellen eines deklarativen Workflows für Project Web App finden Sie unter Erste Schritte beim Entwickeln [Project Server-Workflows](getting-started-developing-project-server-workflows.md). Einen Vergleich der SharePoint Designer- und Visual Studio für Workflows finden Sie unter [Entwickeln von SharePoint 2013-Workflows mithilfe Visual Studio](https://msdn.microsoft.com/library/office/jj163199.aspx).
  
### <a name="client-side-object-model"></a>Clientseitiges Objektmodell
<a name="pj15_WhatsNew_CSOM"> </a>

Der programmgesteuerte Zugriff auf Project Online erfordert ein CSOM, das auf dem SharePoint csOM aufgebaut ist. Project Online Authentifizierung wird bei OAuth mit einer Windows Live-ID ausgeführt, nicht Project serverformularauthentifizierung oder Windows Authentifizierung.
  
Nachfolgend finden Sie die Prinzipien und Features des CSOM in Project Server 2013:
  
- Das CSOM ist für die benutzerfreundlichkeit konzipiert. Methoden und Eigenschaften verwenden z. B. Daten direkt nach Namen, anstatt viele GUIDs,  _changeXml-Parameter_ oder Datasets zu übergeben. 
    
- Der Project Server CSOM implementiert eine Teilmenge der PSI-Funktionalität, basierend auf den gängigsten Anforderungen für Drittanbieterlösungen.
    
- Das CSOM ruft intern die PSI auf, wird jedoch unterschiedlich einbeet. Beispielsweise werden Aktualisierungen für alle Statusänderungen über die **StatusAssignmentCollection.SubmitAllStatusUpdates-Methode** durchgeführt, nicht über die **Statusing.SubmitStatus-PSI-Methode** für den Benutzer oder die **SubmitStatusForResource-Methode** für andere Ressourcen. 
    
- Der Zugriff auf das CSOM ist über einen WCF-Dienst (Client.svc) und nicht über die 22 öffentlichen Dienste der PSI möglich.
    
- Die Initialisierung des Project Server-CSOM wird direkt über die [ProjectContext-Klasse](https://msdn.microsoft.com/library/Microsoft.ProjectServer.Client.ProjectContext.aspx) mit der Project Web App-URL ausgeführt, nicht mithilfe eines WCF-Verweises oder einer Proxy assembly. 
    
- Das CSOM implementiert mehrere Clientbibliotheken und Schnittstellen, die von der internen SharePoint unterstützt werden. Die Clientbibliotheken und -schnittstellen umfassen Folgendes:
    
  - Microsoft .NET-Clientbibliothek in der Microsoft.ProjectServer.Client.dll Assembly
    
  - Silverlight-Bibliothek in der Microsoft.ProjectServer.Client.Silverlight.dll Assembly
    
  - Windows Phone 8-Bibliothek in der Microsoft.ProjectServer.Client.Phone.dll Assembly
    
  - JavaScript-Bibliothek für Webanwendungen in der PS.js oder PS.debug.js Datei
    
  - REST-Endpunkte für den Zugriff mit dem OData-Protokoll
    
  - Systemeigene Unterstützung für LINQ-Abfragen mit Filterung, um die zurückgegebene Datenmenge zu begrenzen
    
- Das CSOM kann sowohl für Project Online als auch für lokale Lösungen verwendet werden, unabhängig von der PSI und anderen Project Serverassemblys wie Microsoft.Office.Project.Server.Library.dll.
    
- Zusätzliche Funktionen des Project Server 2013-CSOM können für kumulative Updates und Service Packs berücksichtigt werden, basierend auf Anforderungen von Project Server-Partnern und der Entwickler-Community.
    
> [!NOTE]
> Das CSOM ist die bevorzugte Schnittstelle für Project Server-Entwickler. Wir empfehlen, dass Sie für die Entwicklung neuer Anwendungen das CSOM verwenden, sofern das CSOM alle für Ihre Anwendung erforderlichen Funktionen umfasst. 
  
Informationen zum Entwickeln mit dem CSOM finden Sie unter [Clientseitiges Objektmodell (CSOM) für Project 2013](client-side-object-model-csom-for-project-2013.md). Informationen zur REST-Schnittstelle in SharePoint finden Sie unter *Programming using the SharePoint REST service* in SharePoint 2013 developer documentation. 
  
### <a name="changes-in-the-reporting-database"></a>Änderungen in der Berichtsdatenbank
<a name="pj15_WhatsNew_RDBChanges"> </a>

Die vier Datenbanken in Project Server 2010 werden in Project Server 2013 zu einer Project kombiniert. Der Standardname der Project ist ProjectService. Berichtstabellen und -ansichten behalten ihre vorherigen Namen bei, und Tabellen und Ansichten aus den Draft-, Published- und Archive-Datenbanken haben die Präfixe , und in der  `draft`  `pub`  `ver` ProjectService-Datenbank. Die Tabelle veröffentlichte Projekte ist z. B. Pub. MSP_PROJECTS. 
  
> [!IMPORTANT]
> Der direkte Zugriff wird für die Tabellen und Ansichten des Entwurfs ( Präfix), veröffentlicht ( ) und `draft` `pub` Archivs ( `ver` ) nicht unterstützt. Berichte sollten nur die Berichtstabellen und -ansichten verwenden, die das Präfix `dbo` haben. Beispiel: dbo. MSP_EpmProject enthält die Liste der Projekte in der Project Web App-Instanz. 
>
> Es gibt nichts, was Sie aktiv daran hindern kann, den direkten programmgesteuerten Datenbankzugriff zum Aktualisieren von Daten in tabellen und Ansichten in der Project verwenden. Beachten Sie, dass Project Professional Cache, die Tabellen für Entwurfs- und veröffentlichte Daten und die Berichtstabellen alle auf einem Cachesynchronisierungsprotokoll beruhen, das durch direkte Datenbearbeitung unterbrochen werden kann. Wenn Sie Ihre Project Server-Datenbanken beschädigen oder Project Professional clientseitigen Caches beschädigt haben, indem Sie den direkten Zugriff zum Ändern von Daten verwenden, sollten Sie gewarnt werden, dass der Produktsupport nicht helfen kann! 
  
Project Server 2013 führt einen OData-Dienst für den Online- und lokalen Zugriff ein. Die Onlineberichtstabellen und -ansichten werden nur von der #A0 verfügbar gemacht. Für die lokale Verwendung können Sie die OData-Schnittstelle verwenden oder direkt auf die Berichtstabellen und -ansichten in der ProjectService-Datenbank in der SharePoint zugreifen. Project Online unterstützt keine mehrstufige Datenbank. Das heißt, mehrere Instanzen Project Web App verfügen jeweils über eine eigene Project Datenbank. Der OData-Dienst führt intern SQL in den Berichtstabellen und -ansichten aus und liefert eine XML- oder JSON-Nutzlast. Eine Einführung in den OData-Dienst für die Berichterstellung in Project Server 2013 und zur **ProjectData-Schemareferenz** finden Sie unter [ProjectData - Project OData service reference](https://msdn.microsoft.com/library/office/jj163015.aspx).
  
Allgemeine Informationen zu OData-Abfragen finden Sie unter [OData: URI-Konventionen](https://www.odata.org/documentation/). Sie können beispielsweise alle Projekte in einer lokalen Instanz von Project Web App anzeigen, bei der der Projektname mit "Test" beginnt, indem Sie die folgende Abfrage in einem Browser verwenden. Klicken Sie mit der rechten Maustaste auf die Browserseite, und klicken Sie dann auf **Quelle anzeigen**.
  
```html
https://ServerName /ProjectServerName /_api/ProjectData/Projects?$filter=startswith(ProjectName, 'Test') eq true
```

Um Projektdaten in PowerPivot in Excel 2013 zu importieren, wählen Sie im Menüband  DATA im Dropdownmenü Aus anderen Quellen aus **OData-Datenfeed** aus. Geben Sie **im** Dialogfeld Datenverbindungs-Assistent den Speicherort des Datenfeeds ein, wählen Sie Weiter aus, und wählen Sie dann auf der Seite Tabellen auswählen des Assistenten die Tabelle Projekte https://ServerName/ProjectServerName/_api/ProjectData/ aus.    Nennen Sie die ODC-Datei, und speichern Sie sie, und wählen Sie dann **Fertig stellen aus.** Wählen Sie **im** Dialogfeld Daten importieren die Option **PivotTable Report aus.** Wählen Sie Excel Arbeitsblatt Felder für die Zeilen und Spalten der Pivottabelle aus, die Sie anzeigen möchten.
  
Lokale Project Serverbenutzer, die über die richtigen Berechtigungen verfügen, können über Microsoft SQL Server direkt auf die Berichtstabellen und -ansichten zugreifen, um Berichte zu erstellen, wie in Project Server 2010. In Project Server 2013 können Benutzer auch über die OData-Schnittstelle auf die lokalen Berichtstabellen zugreifen. Sie können Project Serverdaten online oder lokal über REST-Endpunkte für den OData-Dienst abrufen. Beispiel: dbo. MSP_PROJECT tabelle und dem dbo. MSP_EpmProject_UserView ansicht kann für Berichte verwendet werden. Alle Tabellen oder Ansichten mit einem , oder Präfix sind nur für die interne Verwendung durch Project Server und nicht für die `draft` `pub` `ver` Berichterstellungsnutzung. Beispielsweise der Entwurf. MSP_TASKS tabelle und dem Pub. MSP_PROJECTS_WORKING_VIEW sind nicht dokumentiert und nur für die interne Verwendung. 
  
> [!NOTE]
> Sie können die lokale Berichterstellung erweitern, indem Sie Tabellen, Ansichten, Felder und gespeicherte Prozeduren in einer separaten Datenbank hinzufügen. Sie sollten die vorhandenen Berichtstabellen und -ansichten in der Serverdatenbank nicht Project ändern. 
  
Die Berichtstabellen, -ansichten und -felder in der Project-Datenbank werden in einer HTML-Hilfedatei in einem späteren Update des Project 2013 SDK-Downloads dokumentiert. Eine Dokumentation des OData-XML-Schemas für den **ProjectData-Dienst** finden Sie unter [ProjectData - Project OData service reference](https://msdn.microsoft.com/library/office/jj163015.aspx). Abfragen der Berichtstabellen und -ansichten, die für Project Server 2010 erstellt wurden, funktionieren in den meisten Fällen mit der Project-Datenbank in Project Server 2013. Lokale Benutzer können auf die Project Server-OLAP-Cubes in SQL Server Analysis Services zugreifen. In Project Online stehen keine OLAP-Cubes zur Verfügung.
  
### <a name="task-pane-add-ins-in-project"></a>Aufgabenbereich-Add-Ins in Project
<a name="pj15_WhatsNew_Agave"> </a>

Sowohl Project Standard 2013 als auch Project Professional 2013 unterstützen Aufgabenbereich-Add-Ins, die verwendet werden können, um externe Inhalte in einer Webseite zu integrieren und anzuzeigen. Der Aufgabenbereich zeigt Webseiteninhalte an, die über JavaScript Auf Vorgänge, Ressourcen, Ansichten und allgemeine Projektdaten zugreifen können. Das JavaScript-Objektmodell für Project kann Informationen zu einem ausgewählten Vorgang oder einer ausgewählten Ressource und Daten in einer ausgewählten Zelle im Raster für Ansichten wie das Gantt-Diagramm erhalten. Aufgabenbereich-Add-Ins für Project können auch Ereignishandler für geänderte Ereignisse für Vorgänge, Ressourcen oder Anzeigen geänderter Ereignisse implementieren. 
  
Abbildung 2 zeigt das Hello ProjectData-Aufgabenbereich-Add-In, das den **ProjectData-Dienst** abfragt und dann Die Daten im aktuellen Projekt mit den Mittelwerten für alle Projekte vergleicht.  Der Project 2013 SDK-Download enthält den vollständigen Quellcode für das Add-In. 
  
**Abbildung 2. Ein Aufgabenbereich-Add-In in Project Professional auf Daten in Project Server**

![Vergleichen des aktuellen Projekts mit allen Projekten](media/pj15_RestQueryApp_CompareProject.gif "Vergleichen des aktuellen Projekts mit allen Projekten")
  
> [!NOTE]
> Project Standard 2013 kann nicht direkt über Aufgabenbereich-Add-Ins Project Server 2013 integriert werden. 
  
Aufgabenbereich-Add-Ins in Project Professional können Webparts unterstützen, die für Project Server 2013 erstellt wurden, sodass Entwickler eine Erweiterung erstellen können, sobald sie mit Project Web App und Project Professional. Allgemeine Aufgabenbereich-Add-Ins, die für andere Office 2013-Produkte entwickelt wurden, können auch mit Project Standard 2013 und Project Professional 2013 verwendet werden. Weitere Informationen finden Sie unter [Aufgabenbereich-Add-Ins für Project](task-pane-add-ins-for-project.md).
  
### <a name="project-server-event-receivers"></a>Project Serverereignisempfänger
<a name="pj15_WhatsNew_Events"> </a>

In einer SharePoint-Farm, die das Back-End-Project-Dienstanwendung enthält, können mehrere Project-Web-App-Server (auch als Web-Front-End-Server oder WFEs bezeichnet) enthalten sein. Ereignisempfänger werden auch Ereignishandler genannt. Lokale Ereignishandler können mit voll vertrauenswürdigen Code implementiert und auf allen WFEs für eine lokale Serverinstallation Project bereitgestellt werden. Remoteereignisempfänger können in Webdiensten auf lokalen oder Remoteservern implementiert und von mehreren WFEs und mehreren Serverinstallationen Project werden. Project Online können nur Remoteereignisempfänger verwenden.
  
Project Serverereignishandler werden von SharePoint für jede Project Web App-Instanz und nicht von einer bestimmten Project Web App-Einstellungen verwaltet. Wählen Sie in der SharePoint-Zentraladministrationsanwendung allgemeine Anwendung  **Einstellungen** aus, wählen Sie Unter **PWA Einstellungen** verwalten aus, und wählen Sie dann die Instanz in der Dropdownliste **Project Web App-Instanz** auf der Seite PWA Einstellungen aus. Wenn Sie einen lokalen Ereignishandler oder einen Remoteereignisempfänger hinzufügen möchten, wählen Sie **Serverseitige Ereignishandler aus.**
  
Für eine lokale Installation von Project Server können Sie einen Remoteereignisempfänger als SharePoint-Feature erstellen, das die [Microsoft.ProjectServer.Client.EventHandlerCreationInformation-Klasse](https://msdn.microsoft.com/library/Microsoft.ProjectServer.Client.EventHandlerCreationInformation.aspx) im CSOM verwendet, und dann den Ereignisempfänger mithilfe von Methoden in der [EventHandlerCollection-Klasse](https://msdn.microsoft.com/library/Microsoft.ProjectServer.Client.EventHandlerCollection.aspx) programmgesteuert verwalten. Bei Remoteereignisempfängern sind Vorabereignisse synchron, Nachereignisse asynchron, und es gibt ein Timeout für Fälle, in denen der Remoteereignisempfänger nicht zurückkehrt. 
  
> [!NOTE]
> SharePoint Die Zentraladministration ist nur für lokale Installationen verfügbar. Für Project Online und SharePoint Online können Sie Remoteereignisempfänger mithilfe eines CSOM-basierten App-Pakets hinzufügen oder entfernen. 
  
Auf der Seite Serverseitige Ereignishandler ist der Vorgang zum Hinzufügen eines lokalen Ereignishandlers für eine lokale Project Server-Installation nahezu identisch mit dem im Ereignishandler Erstellen eines [Project Server](https://msdn.microsoft.com/library/gg615466.aspx) beschriebenen Prozesses und protokollieren eines Ereignisthemas für Project Server 2010. Der Unterschied ist, dass die Seite Neuer Ereignishandler über zusätzliche Optionen verfügt. Wählen Sie z. **B. Project Erstellen** in der Liste **Ereignisse** aus, und wählen Sie dann NEW EVENT **HANDLER aus.** Auf der Seite Neuer Ereignishandler sind die beiden einzigen erforderlichen Felder **Name** und **Order** (siehe Abbildung 3). Wenn Sie einen lokalen Ereignishandler mit voller Vertrauenswürdigkeit hinzufügen, fügen Sie das Feld **Assemblyname** und das Feld **Klassenname** hinzu. **Endpunkt-URL leer** lassen. Wenn Sie einen Remoteereignisempfänger hinzufügen, fügen Sie **Endpoint URL** hinzu, und lassen **Sie Assemblyname** und **Klassenname** leer. 
  
> [!CAUTION]
> Wenn Sie *sowohl* den Assemblynamen/Klassennamen als auch die Endpunkt-URL angeben, ruft Project Server nur den lokalen (lokalen) Ereignishandler auf. Der Remoteereignisempfänger wird ignoriert. 
> 
> Wenn Sie zwei Ereignishandler für dasselbe Ereignis erstellen, wobei ein Ereignishandler lokal und einer ein Remoteereignisempfänger ist und der **Order-Wert** für beide identisch ist, ignoriert Project Server den Remoteereignisempfänger. 
  
**Abbildung 3. Hinzufügen eines lokalen Ereignishandlers oder eines Remoteereignisempfängers**

![Konfigurieren eines Ereignishandlers oder Ereignisempfängers](media/pj15_EventHandlers_NewEventHandler.gif "Konfigurieren eines Ereignishandlers oder Ereignisempfängers")
    
Wenn Sie zugriff auf PSI-Datasets für einen lokalen Ereignishandler benötigen, können Sie die Microsoft.Office.Project.Schema.dll-Assembly aus der [Windows]\Microsoft.NET\assembly\GAC \_ MSIL\Microsoft.Office kopieren. Project. Schema\v4.0_15.0.0.0__71e9bce111e9429c-Verzeichnis. 

Anstelle der PSI wird empfohlen, die Ereignisklassen im **Microsoft.ProjectServer.Client-Namespace** zu verwenden. Die Entwicklung mit dem CSOM erfordert keine Manipulation von Datasets. Zum Entwickeln von Remoteereignisempfängern für Project Online müssen Sie die [Event-Klasse](https://msdn.microsoft.com/library/Microsoft.ProjectServer.Client.Event.aspx) und die [EventHandlerCreationInformation-Klasse](https://msdn.microsoft.com/library/Microsoft.ProjectServer.Client.EventHandlerCreationInformation.aspx) im CSOM verwenden. 
  
Bevor Sie einen Project Server-Ereignishandler bereitstellen, installieren und testen Sie den Ereignishandler gründlich in einer Testinstallation von Project Server. Wenn bei einer lokalen Project Server-Installation der lokale Ereignishandler, den Sie hinzufügen, nicht mehr funktioniert, kann der Project Server 2013-Ereignisdienst die anderen gültigen benutzerdefinierten Ereignishandler nicht laden. In diesem Fall müssen Sie den Problemereignishandler entfernen und den Ereignisdienst neu starten.
  
> [!NOTE]
> Für eine lokale Project Serverinstallation wird empfohlen, zu Remoteereignisempfängern zu migrieren, indem Sie das CSOM zum Entwickeln von Ereignisempfängern verwenden. Da für Remoteereignisempfänger kein Code von Drittanbietern innerhalb des Project Server Events Service ausgeführt wird, sind Remoteereignisempfänger stabiler. Lokale Administratoren werden von der Verantwortung für die Verwaltung des Project Server-Ereignisdiensts entlasten. 
  
Allgemeine Informationen zu Ereignissen finden Sie unter [Handling events in apps for SharePoint](https://msdn.microsoft.com/library/jj220048%28office.15%29.aspx). 
  
## <a name="deprecated-features"></a>Veraltete Features
<a name="pj15_WhatsNew_Deprecated"> </a>

> [!NOTE]
> Weitere Informationen zu Features und APIs, die in Project Server 2016 Preview veraltet oder entfernt sind, finden Sie unter Veraltete oder entfernte Features [in Project Server 2016 Preview](https://docs.microsoft.com/project/what-s-deprecated-or-removed-in-project-server-2016). 
  
Veraltete Features sind in Project 2013 für einige Lösungen weiterhin verfügbar, sollten jedoch nicht für die Neuentwicklung verwendet werden. Die meisten der folgenden Features und Methoden funktionieren nicht mit Project Online oder mit der standardmäßigen lokalen Installation von Project Server 2013 im SharePoint Berechtigungsmodus. Vorhandene Lösungen, die diese Features verwenden, funktionieren möglicherweise nicht für ein Upgrade von Project Server 2010 auf Project Server 2013. Auch wenn Lösungen, die veraltete Features verwenden, in einigen Fällen weiterhin funktionieren, werden sie für alle Installationen von Project 2013 nicht vollständig unterstützt.
  
Wenn Ihre Lösungen veraltete Features verwenden, sollten sie vor der Bereitstellung gründlich getestet werden, und Sie sollten sie so ändern, dass unterstützte Features so bald wie möglich verwendet werden. Informationen zum Konfigurieren der lokalen Project Server 2013-Sicherheit für den Project-Berechtigungsmodus finden Sie im Abschnitt *SharePoint Permission Mode* unter [What's new for IT pros in Project Server 2013](https://docs.microsoft.com/project/what-s-new-for-it-pros-in-project-server-2016).
  
-  [Psi-Erweiterungsszenarien für](https://docs.microsoft.com/previous-versions/office/developer/office-2010/ff843378(v=office.14)) Erweiterungen sind veraltet und werden in zukünftigen Versionen nicht mehr unterstützt. Diese lokalen Project Server 2013-Szenarien ermöglichten die Integration mithilfe von benutzerdefinierten Windows Communication Foundation (WCF)-Diensten. 
  
- **Project PSI** Die [Project der](https://docs.microsoft.com/office/client-developer/project/project-psi-reference-overview) PSI ist veraltet. Verwenden Sie für alle Neuentwicklungen [das Project CSOM](client-side-object-model-csom-for-project-2013.md). Project Server 2013-Apps, die die Project PSI verwenden, funktionieren weiterhin, aber Project Online-Apps müssen alle Project-Klasse-PSI-Methoden durch ihre entsprechenden CSOM-Methoden ersetzen.
  
- **Ressourcenplan PSI** Die [PSI für den Ressourcenplan](https://docs.microsoft.com/previous-versions/office/project-class/gg240019(v=office.15)) ist veraltet. Es wird weiterhin für die Project 2013-Entwicklung unterstützt, wird jedoch in zukünftigen Versionen nicht unterstützt. 
  
- **ASMX-Schnittstelle für die PSI** Die PSI enthält doppelte Schnittstellen für die Entwicklung von lokalen Project Servererweiterungen. Die ASMX-Webdienstschnittstelle wurde mit der ersten Implementierung der PSI in Office Project Server 2007 eingeführt. Project Server 2010 hat die WCF-Dienstschnittstelle hinzugefügt, bei der das Objektmodell im Wesentlichen die ASMX-Webdienste dupliziert. Obwohl Project Server 2013 sowohl ASMX als auch WCF unterstützt, sollten neue Lösungen, für die die PSI erforderlich ist, die WCF-Dienste verwenden. Wenn möglich, sollten neue Lösungen mit dem CSOM geschrieben werden. 
  
  Die ASMX-Webdienste der PSI sind in Project Server 2013 veraltet. Um in zukünftigen Project Serverversionen zu funktionieren, müssen Lösungen, die die ASMX-Webdienste verwenden, so umgeschrieben werden, dass sie entweder die WCF-Dienste oder das CSOM verwenden. Weitere Informationen finden Sie im Abschnitt Upgraden von Anwendungen *mit Project Server-APIs* unter [Project Serverprogrammierbarkeit](project-server-programmability.md).
  
- **Objektverknüpfungsanbieter (Object Link Provider, OLP)** In früheren Versionen von Project Server bietet der **ObjectLinkProvider-Dienst** in der PSI (siehe [WebSvcObjectLinkProvider](https://docs.microsoft.com/previous-versions/office/ms481347(v=office.14)) eine Möglichkeit zum Verwalten von Webobjektverbindungen zwischen Enterpriseprojektaufgaben und spezialisierten SharePoint-Listen auf der Projektwebsite für Probleme, Risiken, Lieferdaten und Dokumente. In Project Server 2013 ist das OLP veraltet. 
  
  Sie können die **[RelatedItemManager-Klasse](https://docs.microsoft.com/previous-versions/office/sharepoint-server/jj168020(v=office.15))** im SharePoint CSOM verwenden, um Webobjektverknüpfungen zwischen Elementen in der Aufgabenliste und den anderen Listen auf einer Projektwebsite zu erstellen, zu lesen und zu löschen. Um z. B. einem Problem einen Link aus einem Aufgabenelement hinzuzufügen, können Sie die **[AddSingleLink-Methode](https://docs.microsoft.com/previous-versions/office/sharepoint-server/jj166451(v=office.15))** oder eine der beiden ähnlichen **Methoden, AddSingleLinkFromUrl** oder **AddSingleLinkToUrl, verwenden.** Die **RelatedItemManager-Klasse** enthält auch Methoden zum Löschen einer Webobjektverknüpfung und zum Lesen verwandter Elemente. Informationen zur entsprechenden Klasse im JSOM (dem JavaScript-Objektmodell) finden Sie unter [SP. RelatedItemManager-Objekt (sp.js)](https://docs.microsoft.com/previous-versions/office/sharepoint-visio/jj838582(v=office.15)).
  
  Es wird empfohlen, das SharePoint CSOM zum Erstellen von OLP-Apps für eine lokale Installation von Project Server 2013 und für Project Online. Der [Microsoft.SharePoint-Namespace](https://docs.microsoft.com/previous-versions/office/sharepoint-server/ms464984(v=office.15)) enthält keine **RelatedItemManager** **** -Klasse. 
  
- **Benutzerdefinierte Berechtigungen** Benutzerdefinierte Sicherheitsberechtigungen für den Zugriff auf bestimmte Project Serverfeatures oder -erweiterungen wurden in Office Project Server 2007 unterstützt, in dem in einem SDK-Artikel erläutert wurde, wie sie durch direktes Ändern der veröffentlichten Datenbank erstellt werden. In Project Server 2010 funktionieren benutzerdefinierte Berechtigungen weiterhin, sind jedoch veraltet. In Project Server 2013 funktionieren benutzerdefinierte Berechtigungen nicht mit dem Standardberechtigungsmodus SharePoint lokalen Installationen. Für den Project werden benutzerdefinierte Berechtigungen unterstützt. Bei Project Online ist der direkte Datenbankzugriff nicht möglich. 
  
- **Identitätswechsel** Identitätswechsel in PSI-basierten Apps, bei denen der Benutzer einer App die Sicherheitsberechtigungen eines anderen Project Server-Benutzers annehmen kann, ist in Project Server 2013 veraltet. Wie bereits erwähnt, verwendet eine lokale Standardinstallation Project Server 2013 den SharePoint-Berechtigungsmodus, der keinen Identitätswechsel in den Project Server-Sicherheitsgruppen zu ermöglicht. Weitere Informationen finden Sie unter [Authentication, authorization, and security in SharePoint 2013](https://docs.microsoft.com/sharepoint/dev/general-development/authentication-authorization-and-security-in-sharepoint).
  
  Statusing applications are typical extensions that might have used impersonation in previous versions of Project Server. Project Server 2010 führte die **ReadStatusForResource-Methode** und die **SubmitStatusForResource-Methode** in der PSI zusammen mit der globalen **StatusBrokerPermission-Berechtigung** ein, wodurch der Identitätswechsel zum Lesen und Aktualisieren des Status im Namen eines anderen Benutzers entfällt. Das CSOM in Project Server 2013 verwendet die zugrunde liegende PSI, um Statuserweiterungen transparent zu aktivieren und kann für Project Online oder lokale Installationen verwendet werden. 
  
- **Melden von Datenbankerweiterungen** Das Hinzufügen benutzerdefinierter Tabellen und Ansichten zur Berichtsdatenbank ist bei früheren Versionen von Project Server üblich. Da Project Server 2013 die vier Datenbanken früherer Versionen in einer Datenbank kombiniert, übertragen Upgrades keine benutzerdefinierten Tabellen, Ansichten oder SPROCs an die Berichtstabellen in der Project Server 2013-Datenbank. 
  
  Es wird empfohlen, entweder eine SQL Azure oder eine separate SQL Server für benutzerdefinierte Berichtstabellen und -ansichten zu verwenden, in denen Sie Datenbanksicherungen und -updates verwalten können. Für Project Online ist dies erforderlich.
  
- **Berichterstellung** Die lokalen Berichtstabellen und -ansichten in der Project Server-Datenbank und  die OLAP-Cubes sind nicht veraltet und werden weiterhin vollständig unterstützt. Der Zugriff auf die Berichtstabellen und -ansichten (die Berichtsdatenbank in früheren Project Serverversionen) ist jedoch nicht in Project Online. Entsprechend sind OLAP-Cubes nur bei lokalen Installationen von Project Server 2013 verfügbar. Für Berichterstellungsanwendungen mit Project Online können Sie den **ProjectData-Dienst** über REST-Abfragen mit dem OData-Protokoll verwenden. 
  
- **Project Guide** Das Project-Handbuch ist ein Standardfeature in den Office Project 2007-Desktopanwendungen, in denen HTML- und JavaScript-Inhalte in einem Aufgabenbereich interaktive Anleitungen zum Erstellen und Verwalten von Projekten bieten. In Project 2010 ist der Project Guide nicht in einer Standardinstallation verfügbar, kann jedoch über VBA oder ein VSTO aktiviert werden. Der Project 2010 SDK-Download enthält die geänderten Project Guide-Dateien. 
  
  Das VBA-Objektmodell und **microsoft.Office. Das Interop.MSProject-Objektmodell** in Project 2013 umfasst weiterhin die 22 Member der **Application-Klasse** und die **Project-Klasse,** die das Project verwalten kann. Bei Project 2013-Aufgabenbereich-Apps kann es jedoch zu Konflikten mit Aktionen in einem Project-Leitfaden-Aufgabenbereich und zu Project Guide-Inhalten im Office Store. Es wird dringend empfohlen, Project Aufgabenbereichslösungen mit Office-Add-Ins und nicht mit benutzerdefinierten Project zu entwickeln. Weitere Informationen zum Project finden Sie in der [Project 2010 SDK-Dokumentation](https://msdn.microsoft.com/library/ms512767.aspx).
  
## <a name="comparing-project-server-on-premises-with-project-online"></a>Vergleich Project lokalen Servers mit Project Online
<a name="pj15_WhatsNew_Comparing"> </a>

Damit Sie entscheiden können, ob Project Server lokal oder Project Online verwendet werden soll und welche Arten von Erweiterungen Sie in beiden Fällen entwickeln können, vergleicht Tabelle 2 die erweiterbaren Features einer lokalen Installation von Project Server 2013 mit Project Online. Tabelle 2 enthält keine Unterschiede bei der Bereitstellung, Verwaltung oder Verwendung. Weitere Informationen zu Project Online und Project Server 2013 finden Sie unter [Project 2013 für](https://developer.microsoft.com/project/docs) [Entwickler und Project Online](https://developer.microsoft.com/project).
  
**Tabelle 2. Erweiterbarkeit von Project server lokal und Project Online**

| Feature |Project Server lokal | Project Online |
|:-----|:-----|:-----|
|**Programmierbarkeit** <br/> |CSOM-basierte Apps; konsistentes Programmiermodell  <br/>- .NET, Silverlight, Windows Phone Clientbibliotheken  <br/>- JavaScript-Bibliothek für benutzerdefinierte Seiten, Webparts und Menübanderweiterungen  <br/>- OData- und REST-Protokolle<br/><br/> PSI-basierte Apps; komplexes Programmiermodell, kann auch Apps für Verwaltung, Portfolioanalyse, Benachrichtigungen, Project, Warteschlangensystem und andere Bereiche erstellen<br/><br/>PSI-Erweiterungen  <br/><br/>Benutzerdefinierte Berechtigungen mit Project (veraltet)  <br/><br/>Identitätswechsel mit der PSI (veraltet)  <br/><br/>Voll vertrauenswürdiger Code; Installieren von Erweiterungen in SharePoint Farm  <br/> |CSOM-basierte Apps; konsistentes Programmiermodell  <br/>- .NET, Silverlight, Windows Phone Clientbibliotheken<br/>- JavaScript-Bibliothek für benutzerdefinierte Seiten, Webparts und Menübanderweiterungen<br/>- OData- und REST-Protokolle<br/><br/>Kann die PSI verwenden, aber nicht unterstützt: keine OAuth- und keine Dienst-zu-Dienst-Verbindungen<br/><br/>Keine Erweiterungen der CSOM-API<br/><br/>Keine benutzerdefinierten Berechtigungen<br/><br/>Kein Identitätswechsel<br/><br/>Kein voll vertrauenswürdiger Code  <br/> |
|**Benutzerdefinierte Datenbanken** <br/> |- SQL Azure  <br/>- SQL Server (Änderung von Berichtstabellen und -ansichten in der Project Serverdatenbank wird nicht unterstützt)  <br/> |- SQL Azure  <br/>- SQL Server (Änderung von Berichtstabellen und -ansichten in der Project Serverdatenbank wird nicht unterstützt)  <br/> |
|**Berichterstellung** <br/> |- **ProjectData-Dienst;** OData- und REST-Protokolle  <br/>- Berichtstabellen und -ansichten in der Project Serverdatenbank<br/>- OLAP-Datenbank  <br/> |- **ProjectData-Dienst;** OData- und REST-Protokolle  <br/> |
|**Ereignishandler** <br/> |- Remoteereignisempfänger, auf die über WCF-Endpunkte zugegriffen werden kann<br/>- Voll vertrauenswürdige Ereignishandler, die in einer SharePoint installiert sind  <br/> | - Remoteereignisempfänger, auf die über WCF-Endpunkte zugegriffen werden kann  <br/> |
|**Workflows** <br/> |Deklarative Workflows, erstellt mit SharePoint Designer 2013<br/>- Nur für eine bestimmte web Project-App-Instanz verwenden<br/>– Kann ein Workflowdesign aus Visio 2013 importieren<br/>- Kann benutzerdefinierte Aktionen importieren und verwenden<br/><br/> Deklarative Workflows, erstellt mit Visual Studio 2012<br/>– Erstellen einer App, die Workflows enthalten kann<br/>– Erstellen eines SharePoint Lösungspakets (WSP), das Workflows enthalten kann<br/>– Erstellen von Workflowvorlagen für die Wiederverwendung<br/>- Erstellen und Verwenden benutzerdefinierter Aktionen  <br/><br/>Kann ältere kompilierte Workflows verwenden, die mit WF3.5 erstellt wurden (Empfehlen eines Upgrades auf deklarativen WF4-Workflow)  <br/> |Deklarative Workflows, erstellt mit SharePoint Designer 2013<br/>- Nur für eine bestimmte web Project-App-Instanz verwenden<br/>– Kann ein Workflowdesign aus Visio 2013 importieren<br/>- Kann benutzerdefinierte Aktionen importieren und verwenden  <br/><br/>Deklarative Workflows, erstellt mit Visual Studio 2012<br/>– Erstellen einer App, die Workflows enthalten kann  <br/>– Erstellen eines SharePoint Lösungspakets (WSP), das Workflows enthalten kann<br/>– Erstellen von Workflowvorlagen für die Wiederverwendung <br/>- Erstellen und Verwenden benutzerdefinierter Aktionen  <br/> |
|**Verteilung** <br/> |- Office Store (für CSOM-basierte Apps)<br/>– Privater App-Katalog auf SharePoint<br/>- Intranetdateifreigabe  <br/> |- Office Store<br/>– Privater App-Katalog auf SharePoint  <br/> |

   
## <a name="conclusion"></a>Schlussbemerkung
<a name="pj15_WhatsNew_Conclusion"> </a>

Project Server 2013 bietet eine Vielzahl neuer Entwicklungsfunktionen und Szenarien, die Partner und Kunden verwenden können, um die Funktionen und den Nutzen von Project Server in großen Unternehmen und kleinen Organisationen anzupassen und zu erweitern. Mithilfe der Infrastruktur für Office 2013 und SharePoint 2013 können Sie Apps für Project 2013 erstellen und verteilen, die die Vermarktbarkeit und Verwendung benutzerdefinierter Anwendungen erheblich erweitern können. Einige Erweiterbarkeitsfeatures und -methoden früherer Versionen sind in Project 2013 veraltet, insbesondere die ASMX-Webdienste der PSI und Features, die Identitätswechsel oder direkte Datenbankänderungen beinhalten, die nicht mit Project Online.
  
Die Einführung des CSOM ermöglicht programmgesteuerten Zugriff auf Project Online für eine Vielzahl von Geräten und mithilfe von JavaScript in Webanwendungen. Das CSOM bietet ein konsistentes Programmiermodell im Vergleich zur PSI. Project Der Zugriff auf Serverdaten ist viel mehr möglich als in früheren Versionen, z. B. über den Online-OData-Dienst und über REST-Endpunkte für die Berichterstellung von Daten in Project Datenbank. Vorhandene Berichte funktionieren für die lokale Verwendung weiterhin auf die gleiche Weise. Neue Berichte bieten mehr Flexibilität.
  
Office Add-Ins bieten eine neue Möglichkeit, Lösungen zu verkaufen und Project Standard 2013 in Webinhalte und andere Office 2013-Produkte zu integrieren. Sie können auch neue Möglichkeiten zum Integrieren von Project Professional 2013 in Project Server-Daten und SharePoint-Listen über den Aufgabenbereich Office Erstellen von Add-Ins erstellen.
  
Weitere Informationen zum Entwickeln von Apps und zum Verwenden der [Programmierbarkeitsfeatures](https://docs.microsoft.com/sharepoint/dev/) und des CSOM von SharePoint Server 2013 finden Sie unter SharePoint for developers and [Office for developers](https://developer.microsoft.com/office/docs).
  
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
    

