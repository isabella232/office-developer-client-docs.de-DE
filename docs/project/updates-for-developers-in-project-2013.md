---
title: Updates für Entwickler in Project
manager: soliver
ms.date: 09/29/2015
ms.audience: Developer
localization_priority: Normal
ms.assetid: 5b2b22cd-6e28-43a8-9092-b411da8bfb53
description: Zu den neuen Features gehören ein clientseitiges Objektmodell (CSOM), REST-Schnittstellen, ein OData-Dienst für die Berichterstellung, Remoteereignis Empfänger, deklarative Workflows und Aufgabenbereich-Add-Ins für Projekt Clients.
ms.openlocfilehash: 0c4c3f9b4bb5852f2a620b2695c15de390ac9d78
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32315321"
---
# <a name="updates-for-developers-in-project"></a>Updates für Entwickler in Project

Erweiterbarkeitsfeatures in Project Server 2013 arbeiten mit Add-Ins für Project Online und mit lokalen Installationen. Zu den neuen Features gehören ein clientseitiges Objektmodell (CSOM), REST-Schnittstellen, ein OData-Dienst für die Berichterstellung, Remoteereignis Empfänger, deklarative Workflows und Aufgabenbereich-Add-Ins für Projekt Clients. Erfahren Sie auch mehr über veraltete Features, die für die Neuentwicklung nicht verwendet werden sollten.
  
Project Server 2013 baut auf dem mit Microsoft Office Project Server 2007 eingeführten Framework auf und wird von Project Server 2010 erweitert. Project Server 2013 fügt ein clientseitiges Objektmodell (CSOM) hinzu, das von der Project Server-Schnittstelle (PSI) umgestaltet und vereinfacht wird und eine JavaScript-Bibliothek und .NET Framework 4-Bibliotheken für Windows-apps, Windows Phone 8 und Microsoft Silverlight enthält. Das CSOM ist für die Entwicklung für Project Online und funktioniert auch mit einer lokalen Project Server-Installation. 

Die Project Server-Datenbankenwerden in einer einzigen Datenbank kombiniert; Sie können über einen OData-Dienst auf die Online Berichtstabellen und-Ansichten zugreifen. Die CSOM und der OData-Dienst schließen eine Representational State Transfer (REST)-Schnittstelle ein. Project Server-Workflows können mithilfe von SharePoint Designer 2013 erstellt werden. Project Professional 2013 kann mit Project Server-Berichtsdaten, SharePoint-Aufgabenlisten und anderen externen Inhalten mithilfe des Erweiterungsmodells für Office-Add-Ins für Aufgabenbereiche integriert werden. Project Standard 2013 kann Aufgabenbereich-Add-Ins verwenden, um in allgemeine externe Inhalte zu integrieren.
  
Diagramme und weitere Informationen zu wichtigen Änderungen in Project Server 2013 finden Sie unter [Project server 2013 Architecture](project-server-2013-architecture.md).
  
> [!NOTE]
> Project Server 2013 basiert auf der SharePoint Server 2013- Plattform; Project 2013 weist größtenteils dieselbe Infrastruktur wie die anderen Office 2013-Anwendungen auf. Eine Dokumentation des Modells für SharePoint-Add-Ins, SharePoint-basierte Workflows, Webparts, Entwicklung mit anderen SharePoint-Features und Dokumentation von Office-Add-Ins finden Sie unter [SharePoint-Add-ins](https://docs.microsoft.com/sharepoint/dev/sp-add-ins/sharepoint-add-ins), [Office-Add-ins](https://docs.microsoft.com/office/dev/add-ins/overview/office-add-ins)und [SharePoint 2013 Entwicklungsübersicht](https://msdn.microsoft.com/library/jj164084%28office.15%29.aspx). 
  
## <a name="major-new-features-in-project-2013"></a>Wichtige neue Features in Project 2013
<a name="pj15_WhatsNew_MajorNewFeatures"> </a>

Zu den neuen Features in Project Standard 2013 und Project Professional 2013 gehört eine verbesserte Benutzeroberfläche, die mit anderen Office 2013-Anwendungen übereinstimmt und die moderne Benutzeroberfläche in Windows 8 unterstützt, Integration in Office Art-Objekte für Berichte, Burndown Berichte und neue Programmierfunktionen für Berichte. Project Professional 2013 ermöglicht eine umfassendere Freigabe und Synchronisierung von Projekten in SharePoint Server 2013, zusammen mit den Aufgabenbereich-Add-Ins, die auch in anderen Office 2013-Anwendungen wie Word, Excel und Outlook implementiert sind.
  
Es gibt viele neue Features in Project Server 2013. Einige verfügen nicht über eine wichtige Programmier-Story, wie etwa die neue Zeitachse in Project Web App. Diese Features werden in der Produkt-und Endbenutzerdokumentation zu Microsoft Office Online und in Themen behandelt, die für Administratoren und IT-Experten auf Microsoft TechNet gedacht sind. Andere neue Features wie verbesserte Arbeitszeittabellen erleichtern Drittanbieterentwicklern die Interaktion mit Arbeitszeittabellen und dem Status über die Project Server-Schnittstelle (PSI).
  
Das Hinzufügen von Project Online und dem Office Storehttps://office.microsoft.com/store) (für Projekt-Add-Ins sind weit reichende Änderungen, auf die Project Server über Microsoft Azure zugreifen kann. Der Cloud-basierte Zugriff auf Project Server verwendet ein clientseitiges Objektmodell (CSOM) für die Entwicklung von Add-Ins mit den Microsoft .NET Framework-, Microsoft Silverlight-, Windows Phone-und Web-Apps, die JavaScript verwenden. Eine Anforderung von Project Online ist, dass die vier Project Server-Datenbanken früherer Versionen mit einer Datenbank zusammengeführt werden.
  
Leistung und Skalierbarkeit von Project Server 2013 werden in vielen Bereichen wie Aufgabenstatus, Arbeitszeittabellen und Projektverwaltung verbessert. Project Server-Workflows werden mit Version 4 von Windows Workflow Foundation (WF4) neu entworfen. Die Verwendung von .NET Framework 4 und Windows Communication Foundation (WCF) mit dem PSI verbessert die Sicherheit, Leistung und Skalierbarkeit. Sie können beispielsweise das Transportprotokoll von WCF-basierten Anwendungen mithilfe von Konfigurationsdateien ändern, ohne den Anwendungscode zu ändern oder neu zu kompilieren. Project Web App speichert viele der PSI-Aufrufe zwischen, bei denen sich Daten nicht signifikant ändern.
  
> [!NOTE]
> Für die Entwicklung mit Project Server 2013 können Sie Visual Studio mit den Office-und SharePoint-Tools-Erweiterungen verwenden, die systemeigene Add-Ins für die Office 2013-Produkte erstellen können. Für Project Server 2013 wird Visual Studio benötigt, um die Entwicklung von Features wie Projektdetailseiten und WCF-basierten Anwendungen vollständig zu ermöglichen. Die SharePoint-Tools-Erweiterungen in Visual Studio können Webparts und andere SharePoint-Features direkt in Project Web App und anderen SharePoint-Websites bereitstellen. 
>
> Visual Studio ist nicht mehr erforderlich, um Project Server-Workflows zu entwickeln, die benutzerdefinierte Felder, Stufen, Phasen und Enterprise-Projekttypen verwenden, die in Project Web App verwaltet werden können. Obwohl Sie Visual Studio zum Entwickeln von Workflows verwenden können, sind Sie oft einfacher und schneller zu erstellen, indem Sie SharePoint Designer verwenden. Visual Studio kann für Workflows verwendet werden, die Zugriff auf die CSOM oder andere externe APIs erfordern. 
  
### <a name="project-add-ins"></a>Project-Add-ins
<a name="pj15_WhatsNew_Apps"> </a>

Verteilung und Vermarktung von Software wurde mit dem Konzept eines Add-ins revolutioniert. Für Project 2013 können Add-Ins im öffentlichen Office Store erworben und heruntergeladen oder in einem privaten Katalog auf SharePoint verteilt werden. Ein Add-in ist in der Regel ein eigenständiges, interaktives Programm, das eine kleine Anzahl verwandter Aufgaben ausführt. Ein Projekt-Add-in kann ein Aufgabenbereich-Add-in für die Project Standard-2013-oder Project Standard 2013-Clients oder ein Add-in für Project Server 2013 oder Project online sein.
  
Informationen zu Add-Ins für die Project-Desktop Clients finden Sie unter [Aufgabenbereich-Add-Ins in Project](#pj15_WhatsNew_Agave). Ein Beispiel für Project Server 2013 finden Sie unter [Create a SharePoint-hostEd Project Server Add-in](create-a-sharepoint-hosted-project-server-add-in.md). Zusätzlich zu Artikeln im Office- [und SharePoint-Add-ins-SDK](https://msdn.microsoft.com/library/fp161507.aspx)hat der [Office-Blog](https://blogs.office.com/dev/) viele Beiträge, die auch für Project 2013 und Project Online relevant sind. 
  
Ein Add-in für Project Server 2013 kann sowohl mit einer lokalen Installation als auch mit Project online zusammenarbeiten. Project Server-Add-Ins können Webparts, Remoteereignis Empfänger und Geschäftslogik sein. Der Zugriff auf das Project Server-Objektmodell in einem Add-in erfolgt über den CSOM, nicht über die PSI. Die Datenspeicherung kann Cloud-basiert sein, wie beispielsweise in SQL Azure, extern, beispielsweise über Microsoft Business Connectivity Services (BCS), intern mit einer lokalen Datenbank oder gemischt.
  
#### <a name="add-in-security"></a>Add-in-Sicherheit

Im Allgemeinen werden Aktionen, die ein Add-in ausführt, im Auftrag des Benutzers ausgeführt, der das Add-in ausführt. Sie verwenden nicht explizit den Identitätswechsel oder geben an, wer das Add-in ausführen kann. Aktionen dürfen die Berechtigungsstufe des Benutzers, der das Add-in ausführt, nicht überschreiten. 
  
In Office Developer Tools für Visual Studio 2012 hat die Datei AppManifext. XML einen grafischen Editor, in dem Sie den Berechtigungs Anforderungsbereich festlegen können. Um beispielsweise ein Add-in zu erstellen, das es Projektmanagern ermöglicht, Ihre Projekte zu aktualisieren, wählen Sie auf der Registerkarte **Berechtigungen** im Bereich **Datei AppManifest. XML** Designer **mehrere Projekte** für den Bereich aus, und **Schreiben** Sie für die Berechtigung. Wenn der Add-in-Benutzer über Project Manager-Berechtigungen verfügt, kann Sie das Add-in für von ihr verwaltete Projekte ausführen. Der Code in der Datei Datei AppManifest. XML enthält Folgendes: 
  
```XML
  <AppPermissionRequests>
    <AppPermissionRequest Scope="https://sharepoint/projectserver/projects" Right="Write" />
  </AppPermissionRequests>
```

**Tabelle 1. Berechtigungs Anforderungsbereiche für Project Server-Add-ins**

|Bereich|Berechtigungen|
|:-----|:-----|
|**Project Server** <br/> |**Verwalten** (Erfordert Project Server-Administratorberechtigungen.)  <br/> |
|**Mehrere Projekte** <br/> |**Lesen**, **Schreiben** (erfordert Project Manager-Berechtigungen für einige Vorgänge; Projektteammitglied Berechtigungen für grundlegende Lesevorgänge wie Vorgangszuordnungen.)  <br/> |
|**Einzelnes Projekt** <br/> |**Lesen**, **Schreiben** (erfordert mindestens Projektteammitglied-Berechtigungen; der Zugriff auf einige Daten in einem Projekt hängt von anderen Berechtigungsstufen ab.)  <br/> |
|**Enterprise-Ressourcen** <br/> |**Lesen**, **Schreiben** (erfordert Ressourcen-Manager-Berechtigungen.)  <br/> |
|**Statusing** <br/> |**SubmitStatus** (Erfordert die Berechtigung zum Übermitteln des Status für Ihre Projekte.)  <br/> |
|**Berichterstellung** <br/> |**Lesen Sie** (Erfordert die Berechtigung zum Anmelden bei Project Server.)  <br/> |
|**Workflow** <br/> |**Erhöhen** (Erfordert die Berechtigung zum Ausführen von Workflows. Das Add-in wird mit erhöhten Berechtigungen ausgeführt, um Übergänge von der Stufe in die Stufe in einem Workflow zu ermöglichen. Die Geschäftslogik im Add-in steuert die Phasenübergänge.)  <br/> |
   
> [!NOTE]
> Project Server 2013 und Project Online verwenden nicht das nur-App-Authentifizierungsmodell in SharePoint 2013 (Weitere Informationen finden Sie unter [Add-in-Autorisierungsrichtlinientypen in SharePoint 2013](https://msdn.microsoft.com/library/124879c7-a746-4c10-96a7-da76ad5327f0%28Office.15%29.aspx)). 
  
Informationen zum entwickeln, verteilen, hosten und Verwalten von Add-Ins finden Sie unter [SharePoint-Add-ins](https://docs.microsoft.com/sharepoint/dev/sp-add-ins/sharepoint-add-ins) und [Office-Add-ins](https://docs.microsoft.com/office/dev/add-ins/overview/office-add-ins)und Verwandte Themen in der SharePoint Server 2013-und Office 2013-Entwicklerdokumentation. Weitere Informationen zum Berechtigungs Anforderungsbereich für andere SharePoint-Add-Ins finden Sie unter [Add-in-Berechtigungen in SharePoint 2013](https://msdn.microsoft.com/library/5f7a8440-3c09-4cf8-83ec-c236bfa2d6c4%28Office.15%29.aspx).
  
### <a name="integrating-with-sharepoint-server"></a>Integration in SharePoint Server
<a name="pj15_WhatsNew_IntegrationWSS"> </a>

Für viele Features in Project Web App ist die neue Infrastruktur in SharePoint Server 2013 wie OAuth und anspruchsbasierte Authentifizierung, Project Server-Autorisierung und Berechtigungen über SharePoint-Gruppen, die Synchronisierung von Projekten mit SharePoint-Aufgaben erforderlich. Listen und deklarative Project Server-Workflows. Die Project-Dienstanwendung kann jeder Websitesammlung in einer SharePoint-Farm zugeordnet werden. Die Projektsynchronisierung kann mit einer SharePoint-Aufgabenliste erfolgen, bei der SharePoint das Projekt verwaltet. Ein Enterprise-Projekt kann auch mit einer SharePoint-Aufgabenliste synchronisiert werden, in der Project Server Vollzugriff behält. Architekturdiagramme und eine Erläuterung der Projektsynchronisierung finden Sie unter [Project Server 2013 Architecture](project-server-2013-architecture.md).
  
Es gibt viele neue Features in SharePoint Server 2013. Weitere Informationen finden Sie unter [SharePoint für Entwickler](https://msdn.microsoft.com/sharepoint).
  
### <a name="integrating-with-workflows"></a>Integrieren in Workflows
<a name="pj15_WhatsNew_Workflow"> </a>

Workflows sind ein Hauptfeature der Projektportfolioverwaltung. Ein Projektlebenszyklus kann lange andauernde Prozesse umfassen, die sich über viele Phasen erstrecken. Die Steuerungs Phasen umfassen Projektvorschläge, Analysen der geschäftlichen Auswirkungen und Auswahl, Erstellung, Planung, Verwaltung und Verfolgung von Projekten.
  
Project Server 2013-Workflows basieren auf der SharePoint 2013-Workflow Plattform, die WF4 verwendet. Anders als in früheren Versionen können deklarative Workflows für Project Server 2013 mithilfe von SharePoint Designer 2013 erstellt werden und sind sowohl für die lokale als auch für die Onlineverwendung zugänglich. Project Server-Workflows verwenden das SharePoint-Workflow Sicherheitsmodell mit OAuth und können auf einer Project Web App-Website installiert werden. Abbildung 1 zeigt, dass SharePoint Designer 2013 Stufen zu einem Website-Workflow für die Bedarfs Verwaltung hinzufügen kann, wobei die Phasen in Project Web App definiert sind.
  
**Abbildung 1. Verwenden von SharePoint Designer zum Hinzufügen einer Stufe zu einem Workflow für Project Web App**

![Hinzufügen einer Stufe zu einem Workflow in SPD] (media/pj15_CreateWorkflowSPD_AddStageInSPD.gif "Hinzufügen einer Stufe zu einem Workflow in SPD")

<br/>

Sie erstellen einen deklarativen Workflow, indem Sie workflowstufen, Aktionen, Bedingungen und andere Elemente in einem Entwurfstool hinzufügen, bei dem es sich um SharePoint Designer 2013 oder Visual Studio 2012 handeln kann. Das Entwurfstool speichert dann den Workflow als XAML-Code, der zur Laufzeit interpretiert wird. Deklarative Workflows können entweder in Project Server 2013 lokal oder in Project online ausgeführt werden. Mithilfe von Visual Studio 2012 können Sie auch benutzerdefinierte Aktionen und Formulare für zusätzliches Steuerelement erstellen und Workflowvorlagen zur Wiederverwendung mit mehreren Project Web App-Instanzen speichern. SharePoint Designer 2013 kann benutzerdefinierte Aktionen verwenden, die in Visual Studio 2012 erstellt werden.
  
Ein Project Server 2013-Workflow fungiert als APP, bei der ein Administrator, der über Entwurfsberechtigungen für Project Web App verfügt, einen deklarativen Workflow veröffentlichen und ihm einen Enterprise-Projekttyp (EPT) zuordnen kann. Die EPT muss für ein Enterprise-Projekt sein, in dem Project Server die vollständige Kontrolle behält. Eine SharePoint-Aufgabenliste kann keinen Project Server-Workflow verwenden. 
  
OAuth ermöglicht Projektmanagern, die über Projekt Erstellungsberechtigungen verfügen, den Workflow ohne Identitätswechsel aufzurufen. Workflow Aufrufe an Project Server, um beispielsweise einen benutzerdefinierten Feldwert zu lesen, um zu entscheiden, welche Verzweigung befolgt werden soll, werden im Namen des Projektmanagers vorgenommen. Um zu verhindern, dass der Projektmanager einen Workflow erstellt, der automatisch zur nächsten Stufe wechselt, wird der Aufruf zum Wechseln zur nächsten workflowstufe als Workflowautor (Administrator) ausgeführt. Im Gegensatz dazu stellen Benutzer von Legacy Project Server 2010-Workflows imitierte Aufrufe über das Workflow-Proxy Benutzerkonto bereit, um über den gesamten Workflow Administratorzugriff zu erhalten.
  
Auch wenn Project Server 2013 lokal kompilierte WF 3.5-basierte Workflows verwenden kann, empfiehlt es sich, ältere Workflows auf deklarative Workflows basierend auf WF4 zu aktualisieren. Die neuere Technologie ist skalierbarer und robuster. Geschäftsanalysten und PMO-Mitarbeiter können Workflow Entwürfe mithilfe von Visio 2013 erstellen oder aktualisieren und Project Server-Workflows ohne Codierung mithilfe von SharePoint Designer 2013 implementieren.
  
Weitere Informationen zum Erstellen eines deklarativen Workflows für Project Web App finden Sie unter [Erste Schritte beim Entwickeln von Project Server-Workflows](getting-started-developing-project-server-workflows.md). Einen Vergleich der Funktionen von SharePoint Designer und Visual Studio für Workflows finden Sie unter [entwickeln von SharePoint 2013-Workflows mithilfe von Visual Studio](https://msdn.microsoft.com/library/office/jj163199.aspx).
  
### <a name="client-side-object-model"></a>Clientseitiges Objektmodell
<a name="pj15_WhatsNew_CSOM"> </a>

Für den ProgrammgeSteuerten Zugriff auf Project Online ist ein CSOM erforderlich, das auf dem SharePoint-CSOM basiert. Die Project Online-Authentifizierung erfolgt mit OAuth unter Verwendung einer Windows Live ID, nicht der Project Server-Formularauthentifizierung oder der Windows-Authentifizierung.
  
Es folgen die Grundsätze und Features des CSOM in Project Server 2013:
  
- Das CSOM ist für Benutzerfreundlichkeit ausgelegt. Beispielsweise verwenden Methoden und Eigenschaften direkt oder geben Daten nach Namen, anstatt viele GUIDs, _changeXml_ -Parameter oder übergeben von Datasets. 
    
- Der Project Server-CSOM implementiert eine Teilmenge der PSI-Funktionalität basierend auf den gängigsten Anforderungen für Lösungen von Drittanbietern.
    
- Die CSOM ruft intern die PSI auf, ist jedoch unterschiedlich. Aktualisierungen für alle Statusänderungen werden beispielsweise über die **StatusAssignmentCollection. SubmitAllStatusUpdates** -Methode durchgeführt, nicht über die " **Statusing. SubmitStatus** psi"-Methode für den Benutzer oder die **SubmitStatusForResource** -Methode. für andere Ressourcen. 
    
- Auf die CSOM kann über einen einzigen WCF-Dienst (Client. svc) zugegriffen werden, statt über die 22 öffentlichen Dienste der PSI.
    
- Die Initialisierung des Project Server-CSOM erfolgt direkt über [](https://msdn.microsoft.com/library/Microsoft.ProjectServer.Client.ProjectContext.aspx) die projectcontext-Klasse mit der Project Web App-URL, nicht mithilfe eines WCF-Verweises oder einer Proxy Assembly. 
    
- Die CSOM implementiert mehrere Clientbibliotheken und-Schnittstellen, die von der internen SharePoint-CSOM-Infrastruktur unterstützt werden. Zu den Clientbibliotheken und-Schnittstellen gehört Folgendes:
    
  - Microsoft .NET-Clientbibliothek in der Microsoft. ProjectServer. Client. dll-Assembly
    
  - Silverlight-Bibliothek in der Microsoft. ProjectServer. Client. Silverlight. dll-Assembly
    
  - Windows Phone 8-Bibliothek in der Microsoft. ProjectServer. Client. Phone. dll-Assembly
    
  - JavaScript-Bibliothek für Webanwendungen in der Datei "PS. js" oder "PS. Debug. js"
    
  - REST-Endpunkte für Zugriff mit dem OData-Protokoll
    
  - Systemeigene Unterstützung für LINQ-Abfragen mit Filterung, um die zurückgegebene Datenmenge einzuschränken
    
- Das CSOM kann sowohl für Project Online-Lösungen als auch für lokale Lösungen unabhängig von der PSI und anderen Project Server-Assemblys wie Microsoft. Office. Project. Server. Library. dll verwendet werden.
    
- Weitere Funktionen von Project Server 2013 CSOM können für kumulative Updates und Service Packs auf der Grundlage von Anforderungen von Project Server-Partnern und der Entwicklercommunity berücksichtigt werden.
    
> [!NOTE]
> CSOM ist die bevorzugte Schnittstelle für Project Server-Entwickler von Drittanbietern. Wir empfehlen, dass Sie für die Entwicklung neuer Anwendungen das CSOM verwenden, sofern das CSOM alle für Ihre Anwendung erforderlichen Funktionen umfasst. 
  
Informationen zum Entwickeln mit CSOM finden Sie unter [Client seitiges Objektmodell (CSOM) für Project 2013](client-side-object-model-csom-for-project-2013.md). Informationen zur REST-Schnittstelle in SharePoint-Anwendungen finden Sie unter *Programmieren mit dem SharePoint-Rest-Dienst* in der sharepoint 2013-Entwicklerdokumentation. 
  
### <a name="changes-in-the-reporting-database"></a>Änderungen in der Berichtsdatenbank
<a name="pj15_WhatsNew_RDBChanges"> </a>

Die vier Datenbanken in Project Server 2010 werden in Project Server 2013 zu einer einzelnen Projektdatenbank kombiniert. Der Standardname der Projektdatenbank lautet ProjectService. Berichtstabellen und-Ansichten behalten ihre vorherigen Namen bei, und Tabellen und Ansichten aus den Entwurfs-, Veröffentlichungs-und Archivdatenbanken `draft`weisen `pub`die Präfixe und `ver` in der ProjectService-Datenbank auf. Die Tabelle veröffentlichte Projekte lautet beispielsweise Pub. MSP_PROJECTS. 
  
> [!IMPORTANT]
> Der direkte Zugriff wird für die Tabellen und Ansichten`draft` Entwurf (Präfix),`pub`veröffentlicht () und Archiv`ver`() nicht unterstützt. Berichte sollten nur die Berichtstabellen und-Ansichten verwenden, die das `dbo` Präfix haben. Beispiel: der dbo. Die MSP_EpmProject-Tabelle enthält die Liste der Projekte in der Project Web App-Instanz. 
>
> Sie können nicht aktiv verhindern, dass Sie den direkten programmgesteuerten Datenbankzugriff verwenden, um Daten in einer der Tabellen und Ansichten in der Project-Datenbank zu aktualisieren. Sie sollten sich darüber im klaren sein, dass der Project Professional-Cache, die Tabellen für Entwurfs-und Veröffentlichungsdaten sowie die Berichtstabellen alle auf einem Cache Synchronisierungsprotokoll basieren, das durch direkte Datenbearbeitung gestört werden kann. Wenn Sie Ihre Project Server-Datenbanken oder beschädigte Project Professional-clientseitige Caches mit direktem Zugriff zum Ändern von Daten beschädigt haben, werden Sie gewarnt, dass der Produktsupport nicht helfen kann! 
  
Project Server 2013 bietet einen OData-Dienst für Online-und lokalen Zugriff. Die Tabellen und Ansichten der Online Berichterstattung werden nur von der OData-Schnittstelle verfügbar gemacht. für die lokale Verwendung können Sie die OData-Schnittstelle verwenden oder direkt auf die Berichtstabellen und-Ansichten in der ProjectService-Datenbank in der SharePoint-Farm zugreifen. Project Online unterstützt keine Datenbank mit mehr Mandanten. Das heißt, mehrere Instanzen von Project Web App verfügen jeweils über eine eigene Projektdatenbank. Der OData-Dienst führt intern SQL-Abfragen in den Berichtstabellen und-Ansichten aus und übermittelt eine XML-oder JSON-Nutzlast. Eine Einführung in den OData-Dienst für die Berichterstellung in Project Server 2013 und für die **ProjectData** -Schemareferenz finden Sie unter [ProjectData-Project odata Service Reference](https://msdn.microsoft.com/library/office/jj163015.aspx).
  
Allgemeine Informationen zu OData-Abfragen finden Sie unter [odata: URI Conventions](https://www.odata.org/documentation/). Sie können beispielsweise alle Projekte in einer lokalen Instanz von Project Web App anzeigen, wobei der Projektname mit "Test" beginnt, indem Sie die folgende Abfrage in einem Browser verwenden. Klicken Sie mit der rechten Maustaste auf die Browser Seite, und klicken Sie dann auf **Quelltext anzeigen**.
  
```html
https://ServerName /ProjectServerName /_api/ProjectData/Projects?$filter=startswith(ProjectName, 'Test') eq true
```

Wenn Sie Project-Daten in PowerPivot in Excel 2013 importieren möchten, wählen Sie auf dem Menüband Daten im Dropdownmenü **aus anderen Quellen** **aus OData-Datenfeed aus** . Geben https://ServerName/ProjectServerName/_api/ProjectData/ Sie im dialogFeld Datenverbindungs- **Assistent** den datenfeedsort ein, wählen Sie **weiter**aus, und wählen Sie dann auf der Seite **Tabellen auswählen** des Assistenten die Tabelle **Projekte** aus. Benennen Sie die ODC-Datei, und speichern Sie Sie, und wählen Sie dann **Fertig stellen**aus. Wählen Sie im Dialogfeld **Daten importieren** die Option **PivotTable-Bericht**aus. Wählen Sie im Excel-Arbeitsblatt Felder für die PivotTable-Zeilen und-Spalten aus, die angezeigt werden sollen.
  
Lokale Project Server-Benutzer, die über die richtigen Berechtigungen verfügen, können direkt auf die Berichtstabellen und-Ansichten über Microsoft SQL Server zugreifen, um Berichte zu erstellen, wie dies in Project Server 2010 der Fall ist. In Project Server 2013 können Benutzer auch über die OData-Schnittstelle auf die lokalen Berichtstabellen zugreifen. Sie können Project Server-Daten online oder lokal über REST-Endpunkte für den OData-Dienst abrufen. Beispiel: der dbo. MSP_PROJECT-Tabelle und dbo. MSP_EpmProject_UserView-Ansicht kann für Berichte verwendet werden. Alle Tabellen oder Sichten, die ein `draft`, `pub`oder `ver` Präfix haben, sind nur für die interne Verwendung durch Project Server und nicht für die Verwendung in Berichten. Beispiel: der Entwurf. MSP_TASKS-Tabelle und das Pub. Die MSP_PROJECTS_WORKING_VIEW-Ansicht ist nicht dokumentiert und darf nur intern verwendet werden. 
  
> [!NOTE]
> Sie können die lokale Berichterstellung erweitern, indem Sie Tabellen, Ansichten, Felder und gespeicherte Prozeduren in einer separaten Datenbank hinzufügen. Sie sollten die vorhandenen Berichtstabellen und-Ansichten in der Project Server-Datenbank nicht ändern. 
  
Die Berichtstabellen, Ansichten und Felder in der Project-Datenbank werden in einer HTML-Hilfedatei in einem späteren Update des Project 2013 SDK-Downloads dokumentiert. Eine Dokumentation des OData-XML-Schemas für den **ProjectData** -Dienst finden Sie unter [ProjectData-Project odata Service Reference](https://msdn.microsoft.com/library/office/jj163015.aspx). Abfragen der Berichtstabellen und-Ansichten, die für Project Server 2010 erstellt wurden, können in den meisten Fällen mit der Project-Datenbank in Project Server 2013 verwendet werden. Lokale Benutzer können wie bisher auf die Project Server-OLAP-Cubes in SQL Server Analysis Services zugreifen. In Project Online stehen keine OLAP-Cubes zur Verfügung.
  
### <a name="task-pane-add-ins-in-project"></a>Aufgabenbereich-Add-Ins in Project
<a name="pj15_WhatsNew_Agave"> </a>

Sowohl Project Standard 2013 als auch Project Professional 2013 unterstützen Aufgabenbereich-Add-Ins, die verwendet werden können, um externe Inhalte in einer Webseite zu integrieren und anzuzeigen. Im Aufgabenbereich werden Webseiteninhalte mit Zugriff über JavaScript auf Aufgaben, Ressourcen, Ansichten und allgemeine Projektdaten angezeigt. Das JavaScript-Objektmodell für Project kann Informationen zu einer ausgewählten Aufgabe oder Ressource abrufen und Daten in einer ausgewählten Zelle im Raster für Ansichten wie das Gantt-Diagramm abrufen. Aufgabenbereich-Add-Ins für Project können auch Ereignishandler für die Ereignisse Task, Resource oder View selection changed implementieren. 
  
Abbildung 2 zeigt das Add-in " **Hello ProjectData** -Aufgabenbereich", das den **ProjectData** -Dienst abfragt, und vergleicht dann Daten im aktuellen Projekt mit den Durchschnittswerten für alle Projekte. Der Project 2013 SDK-Download enthält den vollständigen Quellcode für das Add-in. 
  
**Abbildung 2. Ein Aufgabenbereich-Add-in in Project Professional kann auf Daten in Project Server zugreifen**

![Vergleichen des aktuellen Projekts mit allen Projekten] (media/pj15_RestQueryApp_CompareProject.gif "Vergleichen des aktuellen Projekts mit allen Projekten")
  
> [!NOTE]
> Project Standard 2013 kann nicht direkt in Project Server 2013 über Aufgabenbereich-Add-Ins integriert werden. 
  
Aufgabenbereich-Add-Ins in Project Professional können Webparts unterstützen, die für Project Server 2013 erstellt wurden, sodass Entwickler eine Erweiterung erstellen können, die sowohl mit Project Web App als auch mit Project Professional ausgeführt wird. Allgemeine Aufgabenbereich-Add-Ins, die für andere Office 2013-Produkte entwickelt wurden, können auch mit Project Standard 2013 und Project Professional 2013 verwendet werden. Weitere Informationen finden Sie unter [Aufgabenbereich-Add-Ins für Project](task-pane-add-ins-for-project.md).
  
### <a name="project-server-event-receivers"></a>Project Server-Ereignisempfänger
<a name="pj15_WhatsNew_Events"> </a>

In einer SharePoint-Farm, die die Back-End-Project-Dienstanwendung enthält, können mehrere Project Web App-Server (auch Web-Front-End-Server oder WFEs) vorhanden sein. Ereignisempfänger werden auch Ereignishandler genannt. Lokale Ereignishandler können mit vollständig vertrauenswürdigem Code implementiert und auf allen WFEs für eine lokale Project Server-Installation bereitgestellt werden. Remote Ereignisempfänger können in Webdiensten auf lokalen oder Remoteservern implementiert werden, auf die über mehrere WFEs und mehrere Project Server-Installationen zugegriffen wird. Project Online kann nur Remoteereignis Empfänger verwenden.
  
Project Server-Ereignishandler werden von SharePoint für jede Project Web App-Instanz statt von einer bestimmten Project Web App-Einstellungsseite verwaltet. Wählen Sie in der Anwendung für die SharePoint-zentral Administration **Allgemeine Anwendungseinstellungen**aus, wählen Sie unter **PWA-Einstellungen** **Verwalten** aus, und wählen Sie dann in der Dropdownliste **Project Web App-Instanz** in den PWA-Einstellungen die Instanz aus. Seite. Wenn Sie einen lokalen Ereignishandler oder einen Remoteereignis Empfänger hinzufügen möchten, wählen Sie **Server seitige Ereignis**Handler aus.
  
Für eine lokale Installation von Project Server können Sie einen Remoteereignis Empfänger als SharePoint-Feature erstellen, das die [Microsoft. projectserver. Client. EventHandlerCreationInformation](https://msdn.microsoft.com/library/Microsoft.ProjectServer.Client.EventHandlerCreationInformation.aspx) -Klasse in der CSOM verwendet und dann programmgesteuert die Ereignisempfänger mithilfe von Methoden in der [eventhandlercollection](https://msdn.microsoft.com/library/Microsoft.ProjectServer.Client.EventHandlerCollection.aspx) -Klasse. Bei Remoteereignis Empfängern sind Pre-Events synchron, Post-Events sind asynchron und es gibt ein Timeout für Fälle, in denen der Remoteereignis Empfänger nicht zurückkehrt. 
  
> [!NOTE]
> Die SharePoint-zentral Administration ist nur für lokale Installationen verfügbar. Für Project Online und SharePoint Online können Sie Remoteereignis Empfänger mithilfe eines CSOM-basierten App-Pakets hinzufügen oder entfernen. 
  
Auf der Seite mit den Server seitigen Ereignishandlern ist der Prozess zum Hinzufügen eines lokalen Ereignishandlers für eine lokale Project Server-Installation nahezu identisch mit dem im Thema [Create a Project Server-Ereignishandler und Protokollieren eines Ereignisprotokolls](https://msdn.microsoft.com/library/gg615466.aspx) für Project Server beschriebenen Prozess. 2010. Der Unterschied besteht darin, dass die Seite neuer Ereignis Handler zusätzliche Optionen enthält. Wählen Sie beispielsweise **Projekterstellung** in der Liste **Ereignisse** aus, und wählen Sie dann **neuer Ereignis Handler**aus. Auf der Seite neuer Ereignishandler sind nur die beiden erforderlichen Felder **Name** und **Reihenfolge** (siehe Abbildung 3). Wenn Sie einen lokalen voll vertrauenswürdigen Ereignishandler hinzufügen, fügen Sie das Feld **AssemblyName** und das Feld **Klassenname** hinzu. lassen Sie die **Endpunkt-URL** leer. Wenn Sie einen Remoteereignis Empfänger hinzufügen, fügen Sie die **Endpunkt-URL**hinzu, und lassen Sie den **Assemblynamen** und den **Klassennamen** leer. 
  
> [!CAUTION]
> Wenn Sie sowohl den Assemblynamen *als* auch den Klassennamen und die Endpunkt-URL angeben, ruft Project Server nur den lokalen Ereignishandler auf. Der Remoteereignis Empfänger wird ignoriert. 
> 
> Wenn Sie zwei Ereignishandler für dasselbe Ereignis erstellen, wobei der eine lokale und ein Remoteereignis Empfänger ist und der **Auftrags** Wert für beide identisch ist, ignoriert Project Server den Remoteereignis Empfänger. 
  
**Abbildung 3. Hinzufügen eines lokalen Ereignishandlers oder eines Remoteereignis Empfängers**

![Konfigurieren eines Ereignishandlers oder Ereignisempfängers] (media/pj15_EventHandlers_NewEventHandler.gif "Konfigurieren eines Ereignishandlers oder Ereignisempfängers")
    
Wenn Sie Zugriff auf PSI-Datasets für einen lokalen Ereignishandler benötigen, können Sie die Microsoft. Office. Project. Schema. dll-Assembly aus dem [Windows]\_\Microsoft.NET\assembly\GAC MSIL\Microsoft.Office.Project.Schema\v4.0_15.0.0.0__ 71e9bce111e9429c-Verzeichnis. 

Anstelle der PSI empfiehlt es sich, die Ereignisklassen im **Microsoft. projectserver. Client** -Namespace zu verwenden; für die Entwicklung mit dem CSOM ist keine Manipulation von Datasets erforderlich. Zum Entwickeln von Remoteereignis Empfängern für Project Online müssen Sie die [Event](https://msdn.microsoft.com/library/Microsoft.ProjectServer.Client.Event.aspx) -Klasse und die [EventHandlerCreationInformation](https://msdn.microsoft.com/library/Microsoft.ProjectServer.Client.EventHandlerCreationInformation.aspx) -Klasse in der CSOM verwenden. 
  
Bevor Sie einen Project Server-Ereignishandler bereitstellen, installieren und testen Sie den Ereignishandler gründlich in einer Testinstallation von Project Server. Bei einer lokalen Project Server-Installation kann der Project Server 2013-ereignisDienst die anderen gültigen benutzerdefinierten Ereignishandler nicht laden, wenn der von Ihnen hinzugefügte lokale Ereignishandler nicht funktionsfähig ist. In diesem Fall müssen Sie den Problem Behandlungs Handler entfernen und den Ereignisdienst neu starten.
  
> [!NOTE]
> Für eine lokale Project Server-Installation wird empfohlen, zu Remoteereignis Empfängern zu migrieren, indem Sie mithilfe der CSOM Ereignisempfänger entwickeln. Da Remoteereignis Empfänger keinen Code von Drittanbietern innerhalb des Project Server-Ereignis Diensts ausführen, sind Remote ereignisreceiver stabiler. Lokale Administratoren werden von der Verantwortung für die Verwaltung des Project Server-Ereignis Diensts enthoben. 
  
Allgemeine Informationen zu Ereignissen finden Sie unter [Behandeln von Ereignissen in Apps für SharePoint](https://msdn.microsoft.com/library/jj220048%28office.15%29.aspx). 
  
## <a name="deprecated-features"></a>Veraltete Features
<a name="pj15_WhatsNew_Deprecated"> </a>

> [!NOTE]
> Informationen zu Features und APIs, die in Project Server 2016 Preview veraltet oder entfernt wurden, finden Sie unter [What es deprecated or removed in Project server 2016 Preview](https://technet.microsoft.com/library/mt422816%28v=office.16%29.aspx). 
  
VerAltete Features stehen in Project 2013 für einige Lösungen weiterhin zur Verfügung, sollten jedoch nicht für neue Entwicklungen verwendet werden. Die meisten der folgenden Features und Methoden funktionieren nicht mit Project Online oder mit der standardmäßigen lokalen Installation von Project Server 2013 im SharePoint-Berechtigungsmodus. Vorhandene Lösungen, die diese Funktionen verwenden, funktionieren möglicherweise nicht für ein Upgrade von Project Server 2010 auf Project Server 2013. Lösungen, die veraltete Features verwenden, können zwar in einigen Fällen weiterhin funktionieren, Sie werden jedoch für alle Project 2013-Installationen nicht vollständig unterstützt.
  
Wenn Ihre Lösungen veraltete Features verwenden, sollten Sie vor der Bereitstellung gründlich getestet werden, und Sie sollten Sie so schnell wie möglich ändern, um die unterstützten Features zu verwenden. Informationen zum Konfigurieren von Project Server 2013 Security für den Project-Berechtigungsmodus im *SharePoint-Berechtigungsmodus* finden Sie unter [What es New for IT Pros in Project Server 2013](https://technet.microsoft.com/en-us/library/ff631142%28office.15%29.aspx).
  
- **Extensions** [PSI-Erweiterungs Szenarien](https://msdn.microsoft.com/library/office/ff843378%28v=office.14%29.aspx) sind veraltet und werden in zukünftigen Versionen nicht unterstützt. Diese lokalen Project Server 2013-Szenarien haben die Integration mithilfe benutzerdefinierter Windows Communication Foundation (WCF)-Dienste aktiviert. 
  
- **Projekt PSI** Die [Project-Klasse](https://docs.microsoft.com/office/client-developer/project/project-psi-reference-overview) der PSI ist veraltet. Verwenden Sie für alle Neuentwicklungen das [Projekt CSOM](client-side-object-model-csom-for-project-2013.md). Project Server 2013-apps, die das PSI-Projekt verwenden, funktionieren weiterhin, aber Project Online-apps müssen alle PSI-Methoden der Project-Klasse durch ihre entsprechenden CSOM-Methoden ersetzen.
  
- **Ressourcen Plan PSI** Der [Ressourcen Plan PSI](https://msdn.microsoft.com/library/office/websvcresourceplan_di_pj14mref.aspx) ist veraltet. Sie wird weiterhin für die Entwicklung von Project 2013 unterstützt, wird in zukünftigen Versionen jedoch nicht unterstützt. 
  
- **ASMX-Schnittstelle für die PSI** Die PSI enthält doppelte Schnittstellen für die Entwicklung von lokalen Project Server-Erweiterungen. Die ASMX-Webdienste-Schnittstelle wurde mit der ersten Implementierung der PSI in Office Project Server 2007 eingeführt. Project Server 2010 hat die Schnittstelle der WCF-Dienste hinzugefügt, bei der das Objektmodell im Wesentlichen die ASMX-Webdienste dupliziert. Obwohl Project Server 2013 sowohl ASMX als auch WCF weiterhin unterstützt, sollten neue Lösungen, die das PSI erfordern, die WCF-Dienste verwenden. Wenn möglich, sollten neue Lösungen mithilfe der CSOM geschrieben werden. 
  
  Die ASMX-Webdienste der PSI sind in Project Server 2013 veraltet. Um in zukünftigen Project Server-Versionen zu arbeiten, müssen Lösungen, die die ASMX-Webdienste verwenden, so umgeschrieben werden, dass Sie entweder die WCF-Dienste oder die CSOM verwenden. Weitere Informationen finden Sie im Abschnitt *Aktualisieren von Anwendungen mit dem Project Server-APIs* in [Project Server-Programmierbarkeit](project-server-programmability.md).
  
- **Objekt Verknüpfungs Anbieter (OLP)** In früheren Versionen von Project Server bietet der **ObjectLinkProvider** -Dienst im PSI (siehe [WebSvcObjectLinkProvider](https://msdn.microsoft.com/library/WebSvcObjectLinkProvider.aspx) ) eine Möglichkeit, Webobjekt Verknüpfungen zwischen Enterprise-projektAufgaben und spezialisierten SharePoint-Listen auf der Projektwebsite zu verwalten. für Probleme, Risiken, Lieferumfang und Dokumente. In Project Server 2013 ist die OLP veraltet. 
  
  Sie können die **[RelatedItemManager](https://msdn.microsoft.com/library/microsoft.sharepoint.client.relateditemmanager.aspx)** -Klasse im sharePOINT-CSOM verwenden, um Webobjekt Verknüpfungen zwischen Elementen in der Aufgabenliste und den anderen Listen in einer Projektwebsite zu erstellen, zu lesen und zu löschen. Wenn Sie beispielsweise einen Link eines Aufgabenelements zu einem Problem hinzufügen möchten, können Sie die **[AddSingleLink](https://msdn.microsoft.com/library/office/microsoft.sharepoint.client.relateditemmanager.addsinglelink.aspx)** -Methode oder eine der beiden ähnlichen Methoden **AddSingleLinkFromUrl** oder **AddSingleLinkToUrl**verwenden. Die **RelatedItemManager** -Klasse enthält auch Methoden zum Löschen einer Webobjekt Verknüpfung und zum Lesen zugehöriger Elemente. Informationen zur äquivalenten Klasse in der JSOM (dem JavaScript-Objektmodell) finden Sie unter [SP. RelatedItemManager-Objekt (SP. js)](https://msdn.microsoft.com/library/jj838582.aspx).
  
  Es wird empfohlen, dass Sie die SharePoint-CSOM verwenden, um OLP-Typ-Apps für eine lokale Installation von Project Server 2013 und für Project online zu erstellen. Der [Microsoft. SharePoint](https://msdn.microsoft.com/library/microsoft.sharepoint.aspx) -Namespace enthält keine **RelatedItemManager** * * * *-Klasse. 
  
- **Benutzerdefinierte Berechtigungen** Benutzerdefinierte Sicherheitsberechtigungen für den Zugriff auf bestimmte Project Server-Features oder-Erweiterungen wurden in Office Project Server 2007 unterstützt, wobei in einem SDK-Artikel erläutert wird, wie Sie erstellt werden, indem die veröffentlichte Datenbank direkt geändert wird. In Project Server 2010 sind benutzerdefinierte Berechtigungen weiterhin funktionsfähig, aber veraltet. In Project Server 2013 funktionieren benutzerdefinierte Berechtigungen nicht mit dem standardmäßigen SharePoint-Berechtigungsmodus für lokale Installationen. Für den Project-Berechtigungsmodus werden benutzerdefinierte Berechtigungen unterstützt. Mit Project Online ist der direkte Datenbankzugriff nicht möglich. 
  
- **Identitätswechsel** Identitätswechsel in PSI-basierten apps, bei denen der Benutzer einer APP die Sicherheitsberechtigungen eines anderen Project Server-Benutzers annehmen kann, ist in Project Server 2013 veraltet. Wie bereits erwähnt, verwendet eine lokale Standardinstallation von Project Server 2013 den SharePoint-Berechtigungsmodus, der den Identitätswechsel in den Project Server-Sicherheitsgruppen nicht zulässt. Weitere Informationen finden Sie unter [Authentication, authorization, and security in SharePoint 2013](https://msdn.microsoft.com/library/ms457529%28office.15%29.aspx).
  
  Status Anwendungen sind typische Erweiterungen, die den Identitätswechsel in früheren Versionen von Project Server möglicherweise verwendet haben. In Project Server 2010 wurden die **ReadStatusForResource** -Methode und die **SubmitStatusForResource** -Methode in der PSI zusammen mit der globalen **StatusBrokerPermission** -Berechtigung eingeführt, sodass der Identitätswechsel nicht gelesen werden muss. und Aktualisieren des Status im Auftrag eines anderen Benutzers. Der CSOM in Project Server 2013 verwendet das zugrunde liegende PSI, um Status Erweiterungen transparent zu aktivieren, und kann für Project Online oder lokale Installationen verwendet werden. 
  
- **Berichtsdaten Bank Erweiterungen** Das Hinzufügen von benutzerdefinierten Tabellen und Ansichten zur Berichtsdatenbank ist eine gängige Vorgehensweise für frühere Versionen von Project Server. Da Project Server 2013 die vier Datenbanken früherer Versionen in einer Datenbank kombiniert, werden keine benutzerdefinierten Tabellen, Sichten oder SPROCs an die Berichtstabellen in der Project Server 2013-Datenbank übertragen. 
  
  Es wird empfohlen, SQL Azure oder eine separate SQL Server-Datenbank für benutzerdefinierte Berichtstabellen und-Ansichten zu verwenden, in denen Sie Datenbanksicherungen und-Updates verwalten können. Für Project Online ist dies erforderlich.
  
- **Berichterstellung** Die lokalen Berichtstabellen und-Ansichten in der Project Server-Datenbank und die OLAP-Cubes sind *nicht* veraltet und werden weiterhin vollständig unterstützt. Die Berichtstabellen und-Ansichten (die Berichtsdatenbank in früheren Project Server-Versionen) können in Project Online jedoch nicht zugegriffen werden. Entsprechend sind OLAP-Cubes nur für lokale Installationen von Project Server 2013 verfügbar. Für das Melden von Anwendungen mit Project Online können Sie den **ProjectData** -Dienst über Rest-Abfragen mit dem OData-Protokoll verwenden. 
  
- **Projektberater** Der Projektberater ist ein Standardfeature in den Office Project 2007-Desktopanwendungen, in dem HTML-und JavaScript-Inhalte in einem Aufgabenbereich interaktive Anleitungen für das Erstellen und Verwalten von Projekten bieten. In Project 2010 ist der Projektberater nicht in einer Standardinstallation verfügbar, kann aber über VBA oder ein VSTO-Add-in aktiviert werden. Der Project 2010 SDK-Download enthält die geänderten Projektberater Dateien. 
  
  Das VBA-Objektmodell und das **Microsoft. Office. Interop. MSProject** -Objektmodell in Project 2013 schließen weiterhin die 22 Mitglieder der **Application** -Klasse und die **Project** -Klasse, die den Projektberater verwalten kann. Projekt-2013-Aufgabenbereich-Apps können jedoch mit Aktionen in einem Projektberater-Aufgabenbereich in Konflikt stehen und Projektberater Inhalte können im Office Store nicht einfach verteilt oder verkauft werden. Es wird dringend empfohlen, Projekt-Aufgabenbereich-Lösungen mit Office-Add-Ins zu entwickeln, nicht benutzerdefinierter Projektberaterinhalt. Weitere Informationen zum Projektberater finden Sie in der [project 2010 SDK-Dokumentation](https://msdn.microsoft.com/library/ms512767.aspx).
  
## <a name="comparing-project-server-on-premises-with-project-online"></a>Vergleichen von Project Server lokal mit Project Online
<a name="pj15_WhatsNew_Comparing"> </a>

Damit Sie entscheiden können, ob Project Server lokal oder Project Online verwendet werden soll und welche Arten von Erweiterungen Sie in beiden Fällen entwickeln dürfen, vergleicht Tabelle 2 die erweiterbaren Features einer lokalen Installation von Project Server 2013 mit Project online. Tabelle 2 enthält keine Unterschiede bei der Bereitstellung, Verwaltung oder Verwendung. Weitere Informationen zu Project Online und Project Server 2013 finden Sie unter [project 2013 für Entwickler](https://msdn.microsoft.com/office/fp161502) und [Project Online](https://developer.microsoft.com/en-us/project).
  
**Tabelle 2. Erweiterbarkeit von Project Server lokal und Project Online**

| Feature |Project Server lokal | Project Online |
|:-----|:-----|:-----|
|**Programmierbarkeits** <br/> |CSOM-basierte apps; konsistentes Programmiermodell  <br/>-.NET, Silverlight, Windows Phone-Clientbibliotheken  <br/>-JavaScript-Bibliothek für benutzerdefinierte Seiten, Webparts und Menüband-Erweiterungen  <br/>-OData-und REST-Protokolle<br/><br/> PSI-basierte apps; Komplexes Programmiermodell, kann auch Apps für Verwaltung, Portfolioanalyse, Benachrichtigungen, Projektmodus Sicherheit, Warteschlangensystem und andere Bereiche erstellen.<br/><br/>PSI-Erweiterungen  <br/><br/>Benutzerdefinierte Berechtigungen mit Project-Modus-Sicherheit (veraltet)  <br/><br/>Identitätswechsel mit dem PSI (veraltet)  <br/><br/>Voll vertrauenswürdiger Code; Installieren von Erweiterungen in der SharePoint-Farm  <br/> |CSOM-basierte apps; konsistentes Programmiermodell  <br/>-.NET, Silverlight, Windows Phone-Clientbibliotheken<br/>-JavaScript-Bibliothek für benutzerdefinierte Seiten, Webparts und Menüband-Erweiterungen<br/>-OData-und REST-Protokolle<br/><br/>PSI kann verwendet werden, aber nicht unterstützt: keine OAuth und keine Dienst-zu-Dienst-Verbindungen<br/><br/>Keine Erweiterungen der CSOM-API<br/><br/>Keine benutzerdefinierten Berechtigungen<br/><br/>Kein Identitätswechsel<br/><br/>Kein voll vertrauenswürdiger Code  <br/> |
|**Benutzerdefinierte Datenbanken** <br/> |-SQL Azure  <br/>-SQL Server (Änderung von Berichtstabellen und Ansichten in der Project Server-Datenbank wird nicht unterstützt)  <br/> |-SQL Azure  <br/>-SQL Server (Änderung von Berichtstabellen und Ansichten in der Project Server-Datenbank wird nicht unterstützt)  <br/> |
|**Berichterstellung** <br/> |- **ProjectData** -Dienst; OData-und REST-Protokolle  <br/>-Melden von Tabellen und Ansichten in der Project Server-Datenbank<br/>-OLAP-Datenbank  <br/> |- **ProjectData** -Dienst; OData-und REST-Protokolle  <br/> |
|**Ereignishandler** <br/> |-Remote Ereignisempfänger, auf die über WCF-Endpunkte zugegriffen werden kann<br/>-Voll vertrauenswürdige Ereignishandler, installiert in der SharePoint-Farm  <br/> | -Remote Ereignisempfänger, auf die über WCF-Endpunkte zugegriffen werden kann  <br/> |
|**Workflows** <br/> |Deklarative Workflows, erstellt mit SharePoint Designer 2013<br/>– Nur für eine bestimmte Project Web App-Instanz verwenden<br/>-Kann einen Workflowentwurf aus Visio 2013 importieren<br/>-Kann benutzerdefinierte Aktionen importieren und verwenden<br/><br/> Mit Visual Studio 2012 erstellte deklarative Workflows<br/>-Erstellen einer APP, die Workflows umfasst<br/>-Erstellen eines SharePoint-Lösungspakets (. wsp), das Workflows einbeziehen kann<br/>-Erstellen von Workflowvorlagen zur Wiederverwendung<br/>-Erstellen und Verwenden von benutzerdefinierten Aktionen  <br/><br/>Kann Legacy kompilierte Workflows verwenden, die mit WF 3.5 erstellt wurden (Upgrade auf deklarativen WF4-Workflow empfehlen)  <br/> |Deklarative Workflows, erstellt mit SharePoint Designer 2013<br/>– Nur für eine bestimmte Project Web App-Instanz verwenden<br/>-Kann einen Workflowentwurf aus Visio 2013 importieren<br/>-Kann benutzerdefinierte Aktionen importieren und verwenden  <br/><br/>Mit Visual Studio 2012 erstellte deklarative Workflows<br/>-Erstellen einer APP, die Workflows umfasst  <br/>-Erstellen eines SharePoint-Lösungspakets (. wsp), das Workflows einbeziehen kann<br/>-Erstellen von Workflowvorlagen zur Wiederverwendung <br/>-Erstellen und Verwenden von benutzerdefinierten Aktionen  <br/> |
|**Verteilung** <br/> |-Office Store (für CSOM-basierte Apps)<br/>-Privater App-Katalog auf SharePoint<br/>-Intranet-Dateifreigabe  <br/> |-Office Store<br/>-Privater App-Katalog auf SharePoint  <br/> |

   
## <a name="conclusion"></a>Schlussbemerkung
<a name="pj15_WhatsNew_Conclusion"> </a>

Project Server 2013 bietet eine Fülle neuer Entwicklungsmöglichkeiten und Szenarien, mit denen Partner und Kunden die Funktionen und den Nutzen von Project Server in großen Unternehmen und in kleinen Organisationen anpassen und erweitern können. Sie können die Infrastruktur für Office 2013 und SharePoint 2013 verwenden, um Apps für Project 2013 zu erstellen und zu verteilen, die die Markt-und Nutzungsmöglichkeiten von benutzerdefinierten Anwendungen erheblich erweitern können. Einige Erweiterbarkeitsfeatures und-Methoden früherer Versionen sind in Project 2013 veraltet, insbesondere die ASMX-Webdienste der PSI und Features, die Identitätswechsel oder direkte Datenbankänderungen betreffen, die nicht mit Project Online verwendet werden können.
  
Die Einführung des CSOM ermöglicht den programmgesteuerten Zugriff auf Project Online für eine Vielzahl von Geräten und die Verwendung von JavaScript in Webanwendungen. Das CSOM bietet ein konsistenteres Programmiermodell als das PSI. Auf Project Server-Daten kann auf viel mehr Möglichkeiten zugegriffen werden als in früheren Versionen, einschließlich über den Online OData-Dienst und über REST-Endpunkte für das Melden von Daten in der Project-Datenbank. Vorhandene Berichte funktionieren weiterhin für die lokale Verwendung. neue Berichte haben mehr Flexibilität.
  
Office-Add-Ins bieten eine neue Allee für den Verkauf von Lösungen und die Integration von Project Standard 2013 mit Webinhalten und anderen Office 2013-Produkten. Sie können auch neue Möglichkeiten zum Integrieren von Project Professional 2013 mit Project Server-Daten und SharePoint-Listen über Aufgabenbereich-Office-Add-Ins erstellen.
  
Weitere Informationen zum Entwickeln von apps und zum Verwenden der Programmierfeatures und der CSOM von SharePoint Server 2013 finden Sie unter [SharePoint für Entwickler](https://msdn.microsoft.com/sharepoint) und [Office für Entwickler](https://msdn.microsoft.com/office).
  
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
- [Office Store](https://office.microsoft.com/en-us/store/)   
- [Project Online](https://developer.microsoft.com/en-us/project)
    

