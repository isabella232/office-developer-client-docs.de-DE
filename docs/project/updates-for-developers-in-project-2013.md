---
title: Updates für Entwickler in Project
manager: lindalu
ms.date: 12/03/2019
ms.audience: Developer
ms.localizationpriority: medium
ms.assetid: 5b2b22cd-6e28-43a8-9092-b411da8bfb53
description: Zu den neuen Features gehören ein clientseitiges Objektmodell (CSOM), REST-Schnittstellen, ein OData-Dienst für die Berichterstellung, Remoteereignisempfänger, deklarative Workflows und Aufgabenbereich-Add-Ins für Project Clients.
ms.openlocfilehash: 0f9cfc226e7ef4e5c2f81301812578e3ce9e58e9
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59554999"
---
# <a name="updates-for-developers-in-project"></a>Updates für Entwickler in Project

Erweiterbarkeitsfeatures in Project Server 2013 funktionieren mit Add-Ins für Project Online und mit lokalen Installationen. Zu den neuen Features gehören ein clientseitiges Objektmodell (CSOM), REST-Schnittstellen, ein OData-Dienst für die Berichterstellung, Remoteereignisempfänger, deklarative Workflows und Aufgabenbereich-Add-Ins für Project Clients. Erfahren Sie auch mehr über veraltete Features, die nicht für die Neuentwicklung verwendet werden sollten.
  
Project Server 2013 basiert auf dem Framework, das mit Microsoft Office Project Server 2007 eingeführt und um Project Server 2010 erweitert wurde. Project Server 2013 fügt ein clientseitiges Objektmodell (CSOM) hinzu, das von der Project Serverschnittstelle (PSI) umgestaltet und vereinfacht wird und eine JavaScript-Bibliothek und .NET Framework 4 Bibliotheken für Windows Apps, Windows Phone 8 und Microsoft Silverlight enthält. Das CSOM wurde für die Entwicklung für Project Online entwickelt und funktioniert auch mit einer lokalen Project Serverinstallation. 

Die Project Serverdatenbanken werden zu einer einzigen Datenbank kombiniert. Sie können über einen OData-Dienst auf die Onlineberichtstabellen und -ansichten zugreifen. Das CSOM und der OData-Dienst enthalten eine REST-Schnittstelle (Representational State Transfer). Project Serverworkflows können mit SharePoint Designer 2013 erstellt werden. Project Professional 2013 kann mithilfe des Office-Add-Ins-Erweiterbarkeitsmodells für Aufgabenbereiche in Project Serverberichtsdaten, SharePoint Aufgabenlisten und andere externe Inhalte integriert werden. Project Standard 2013 können Aufgabenbereich-Add-Ins für die Integration in allgemeine externe Inhalte verwenden.
  
Diagramme und weitere Informationen zu wichtigen Änderungen in Project Server 2013 finden Sie unter [Project Server 2013-Architektur.](project-server-2013-architecture.md)
  
> [!NOTE]
> Project Server 2013 basiert auf der SharePoint Server 2013- Plattform; Project 2013 weist größtenteils dieselbe Infrastruktur wie die anderen Office 2013-Anwendungen auf. Dokumentation zum Modell für SharePoint-Add-Ins, SharePoint-basierten Workflows, Webparts, Entwicklung mit anderen SharePoint Features und Dokumentation zu Office-Add-Ins finden Sie unter [SharePoint Add-Ins,](https://docs.microsoft.com/sharepoint/dev/sp-add-ins/sharepoint-add-ins) [Office Add-Ins](https://docs.microsoft.com/office/dev/add-ins/overview/office-add-ins)und [SharePoint 2013 – Übersicht über die Entwicklung.](https://msdn.microsoft.com/library/jj164084%28office.15%29.aspx) 
  
## <a name="major-new-features-in-project-2013"></a>Wichtige neue Features in Project 2013
<a name="pj15_WhatsNew_MajorNewFeatures"> </a>

Zu den neuen Features in Project Standard 2013 und Project Professional 2013 gehört eine verbesserte Benutzeroberfläche, die mit anderen Office 2013-Anwendungen übereinstimmt und die moderne Benutzeroberfläche in Windows 8, die Integration mit Office Art-Objekten für Berichte, Burndown-Berichte und neue Programmierbarkeitsfeatures für Berichte. Project Professional 2013 ermöglicht die umfassendere Freigabe und Synchronisierung von Projekten auf SharePoint Server 2013 sowie die Aufgabenbereich-Add-Ins, die auch in anderen Office 2013-Anwendungen wie Word, Excel und Outlook implementiert sind.
  
Es gibt viele neue Features in Project Server 2013. Einige haben keine größere Programmierbarkeit, z. B. die neue Zeitachse in Project Web App. Diese Features werden in der Produkthilfe und in der Endbenutzerdokumentation auf Microsoft Office Online und in Themen für Administratoren und IT-Experten auf Microsoft TechNet dokumentiert. Andere neue Features, z. B. verbesserte Arbeitszeittabellen, erleichtern Entwicklern von Drittanbietern die Interaktion mit Arbeitszeittabellen und die Statuserfassung über die Project Serverschnittstelle (PSI).
  
Das Hinzufügen von Project Online und der Office Store ( https://office.microsoft.com/store) für Project-Add-Ins sind umfassende Änderungen, bei denen Project Server über Microsoft Azure zugänglich ist. Der cloudbasierte Zugriff auf Project Server verwendet ein clientseitiges Objektmodell (CSOM) für die Entwicklung von Add-Ins mit den Microsoft .NET Framework-, Microsoft Silverlight-, Windows Phone- und Web-Apps, die JavaScript verwenden. Eine Anforderung von Project Online besteht darin, dass die vier Project Serverdatenbanken früherer Versionen in einer Datenbank zusammengeführt werden.
  
Project Die Leistung und Skalierbarkeit von Server 2013 wurden in vielen Bereichen wie Aufgabenstatus, Arbeitszeittabellen und Projektmanagement verbessert. Project Serverworkflows werden mit Version 4 von Windows Workflow Foundation (WF4) neu gestaltet. Die Verwendung der .NET Framework 4 und Windows Communication Foundation (WCF) mit der PSI verbessert die Sicherheit, Leistung und Skalierbarkeit. Sie können z. B. das Transportprotokoll wcfbasierter Anwendungen mithilfe von Konfigurationsdateien ändern, ohne den Anwendungscode zu ändern oder neu zu kompilieren. Project Web App speichert viele der PSI-Aufrufe zwischen, bei denen daten nicht wesentlich geändert werden.
  
> [!NOTE]
> Für die Entwicklung mit Project Server 2013 können Sie Visual Studio mit den Office- und SharePoint-Toolserweiterungen verwenden, die systemeigene Add-Ins für die Office 2013-Produkte erstellen können. Project Server 2013 erfordert Visual Studio, um die Entwicklung von Features wie Projektdetailseiten und WCF-basierten Anwendungen vollständig zu ermöglichen. Die SharePoint Toolserweiterungen in Visual Studio können Webparts und andere SharePoint Features direkt auf Project Web App und anderen SharePoint Websites bereitstellen. 
>
> Visual Studio ist nicht mehr erforderlich, um Project Serverworkflows zu entwickeln, die benutzerdefinierte Felder, Phasen, Phasen und Enterprise-Projekttypen verwenden, die in Project Web App verwaltet werden können. Obwohl Sie Visual Studio zum Entwickeln von Workflows verwenden können, sind sie mithilfe von SharePoint Designer häufig einfacher und schneller zu erstellen. Visual Studio können für Workflows verwendet werden, die Zugriff auf das CSOM oder andere externe APIs benötigen. 
  
### <a name="project-add-ins"></a>Project-Add-Ins
<a name="pj15_WhatsNew_Apps"> </a>

Die Verteilung und Vermarktung von Software wurde mit dem Konzept eines Add-Ins revolutioniert. Für Project 2013 können Add-Ins zum Kauf und Download über die öffentliche Office Store zur Verfügung gestellt oder in einem privaten Katalog auf SharePoint verteilt werden. Ein Add-In ist in der Regel ein eigenständiges, interaktives Programm, das eine kleine Anzahl verwandter Aufgaben ausführt. Ein Project-Add-In kann ein Aufgabenbereich-Add-In für die Clients Project Standard 2013 oder Project Standard 2013 oder ein Add-In für Project Server 2013 oder Project Online sein.
  
Informationen zu Add-Ins für die Project-Desktopclients finden Sie unter [Aufgabenbereich-Add-Ins in Project.](#pj15_WhatsNew_Agave) Ein Beispiel für ein Project Server 2013 finden Sie unter [Erstellen eines SharePoint gehosteten Project Server-Add-Ins.](create-a-sharepoint-hosted-project-server-add-in.md) Zusätzlich zu den Artikeln im [Office und SharePoint Add-Ins SDK](https://msdn.microsoft.com/library/fp161507.aspx)enthält der Office [Blog](https://blogs.office.com/dev/) viele Beiträge, die auch für Project 2013 und Project Online relevant sind. 
  
Ein Add-In für Project Server 2013 kann sowohl mit einer lokalen Installation als auch mit Project Online verwendet werden. Project Server-Add-Ins können Webparts, Remoteereignisempfänger und Geschäftslogik enthalten. Der Zugriff auf das Project Server-Objektmodell in einem Add-In erfolgt über das CSOM, nicht über die PSI. Der Datenspeicher kann cloudbasiert sein, z. B. mit SQL Azure, extern, z. B. über Microsoft Business Connectivity Services (BCS), intern mit einer lokalen Datenbank oder gemischt.
  
#### <a name="add-in-security"></a>Add-In-Sicherheit

Im Allgemeinen werden Aktionen, die ein Add-In ausführt, im Namen des Benutzers ausgeführt, der das Add-In ausführt. Sie verwenden nicht explizit den Identitätswechsel oder geben an, wer das Add-In ausführen kann. Aktionen dürfen die Berechtigungsstufe des Benutzers, der das Add-In ausführt, nicht überschreiten. 
  
In Office Developer Tools for Visual Studio 2012 verfügt die AppManifext.xml-Datei über einen grafischen Editor, in dem Sie den Berechtigungsanforderungsbereich festlegen können. Wenn Sie beispielsweise ein Add-In erstellen möchten, mit dem Projektmanager ihre Projekte aktualisieren können, wählen Sie auf der Registerkarte **"Berechtigungen"** im **DesignerbereichAppManifest.xml** **"Mehrere Projekte"** für den Bereich und **"Schreiben"** für die Berechtigung aus. Wenn der Add-In-Benutzer über Projektmanagerberechtigungen verfügt, kann er das Add-In für von ihm verwalteten Projekte ausführen. Der Code in der datei AppManifest.xml würde Folgendes enthalten: 
  
```XML
  <AppPermissionRequests>
    <AppPermissionRequest Scope="https://sharepoint/projectserver/projects" Right="Write" />
  </AppPermissionRequests>
```

**Tabelle 1. Berechtigungsanforderungsbereiche für Project Server-Add-Ins**

|Umfang|Berechtigungen|
|:-----|:-----|
|**Project Server** <br/> |**Verwalten** (erfordert Project Serveradministratorberechtigungen.)  <br/> |
|**Mehrere Projekte** <br/> |**Lese-,** **Schreibzugriff** (erfordert Project Manager-Berechtigungen für einige Vorgänge; Project Team Member-Berechtigungen für grundlegende Lesevorgänge, z. B. Aufgabenzuweisungen).)  <br/> |
|**Einzelne Project** <br/> |**Lese-,** **Schreibzugriff** (erfordert mindestens Berechtigungen für Teammitglieder; der Zugriff auf einige Daten in einem Projekt hängt von anderen Berechtigungsstufen ab.)  <br/> |
|**Enterprise Ressourcen** <br/> |**Lese-,** **Schreibzugriff** (Erfordert Ressourcen-Manager-Berechtigungen.)  <br/> |
|**Statusing** <br/> |**SubmitStatus** (Erfordert die Berechtigung zum Übermitteln des Status für Ihre Projekte.)  <br/> |
|**Berichterstellung** <br/> |**Lesen** (Erfordert die Berechtigung zum Anmelden Project Servers.)  <br/> |
|**Workflow** <br/> |**Erhöhte Rechte** (Erfordert die Berechtigung zum Ausführen von Workflows. Das Add-In wird mit erhöhten Berechtigungen ausgeführt, um Übergänge von Phase zu Phase in einem Workflow zu ermöglichen. Die Geschäftslogik in den Add-In-Steuerelementen steuert Phasenübergänge.)  <br/> |
   
> [!NOTE]
> Project Server 2013 und Project Online verwenden nicht das Nur-App-Authentifizierungsmodell in SharePoint 2013 (siehe [Add-In-Autorisierungsrichtlinientypen in SharePoint 2013).](https://msdn.microsoft.com/library/124879c7-a746-4c10-96a7-da76ad5327f0%28Office.15%29.aspx) 
  
Informationen zum Entwickeln, Verteilen, Hosten und Verwalten von Add-Ins finden Sie unter [SharePoint Add-Ins](https://docs.microsoft.com/sharepoint/dev/sp-add-ins/sharepoint-add-ins) und [Office Add-Ins](https://docs.microsoft.com/office/dev/add-ins/overview/office-add-ins)sowie verwandte Themen in der Entwicklerdokumentation SharePoint Server 2013 und Office 2013. Informationen zum Berechtigungsanforderungsbereich für andere SharePoint-Add-Ins finden Sie unter [Add-In-Berechtigungen in SharePoint 2013.](https://msdn.microsoft.com/library/5f7a8440-3c09-4cf8-83ec-c236bfa2d6c4%28Office.15%29.aspx)
  
### <a name="integrating-with-sharepoint-server"></a>Integration mit SharePoint Server
<a name="pj15_WhatsNew_IntegrationWSS"> </a>

Viele Features in Project Web App erfordern die neue Infrastruktur in SharePoint Server 2013, z. B. OAuth und anspruchsbasierte Authentifizierung, Project Serverautorisierung und Berechtigungen über SharePoint Gruppen, Synchronisierung von Projekten mit SharePoint Aufgabenlisten und Project Server deklarative Workflows. Die Project Dienstanwendung kann einer beliebigen Websitesammlung in einer SharePoint Farm zugeordnet werden. Project Synchronisierung kann mit einer SharePoint Aufgabenliste erfolgen, in der SharePoint das Projekt verwaltet. Ein Enterprise-Projekt kann auch mit einer SharePoint Aufgabenliste synchronisiert werden, in der Project Server die Vollständige Kontrolle behält. Architekturdiagramme und eine Erläuterung der Projektsynchronisierung finden Sie unter [Project Server 2013-Architektur.](project-server-2013-architecture.md)
  
Es gibt viele neue Features in SharePoint Server 2013. Weitere Informationen finden Sie unter [SharePoint für Entwickler.](https://msdn.microsoft.com/sharepoint)
  
### <a name="integrating-with-workflows"></a>Integration in Workflows
<a name="pj15_WhatsNew_Workflow"> </a>

Workflows sind ein Hauptfeature der Projektportfolioverwaltung. Ein Projektlebenszyklus kann lange dauernde Prozesse umfassen, die sich über viele Phasen erstrecken. Zu den Governance-Phasen gehören Projektvorschläge, Analysen der geschäftlichen Auswirkungen sowie Auswahl, Erstellung, Planung, Verwaltung und Nachverfolgung von Projekten.
  
Project Server 2013-Workflows basieren auf der SharePoint 2013-Workflowplattform, die WF4 verwendet. Im Gegensatz zu früheren Versionen können deklarative Workflows für Project Server 2013 mit SharePoint Designer 2013 erstellt werden und können sowohl lokal als auch online verwendet werden. Project Serverworkflows verwenden das SharePoint-Workflowsicherheitsmodell mit OAuth und können auf einer Project Web App-Website installiert werden. Abbildung 1 zeigt, dass SharePoint Designer 2013 einem Websiteworkflow für die Bedarfsverwaltung Phasen hinzufügen kann, wobei die Phasen in Project Web App definiert sind.
  
**Abbildung 1. Verwenden von SharePoint Designer zum Hinzufügen einer Phase zu einem Workflow für Project Web App**

![Hinzufügen einer Phase zu einem Workflow in SPD](media/pj15_CreateWorkflowSPD_AddStageInSPD.gif "Hinzufügen einer Phase zu einem Workflow in SPD")

<br/>

Sie erstellen einen deklarativen Workflow, indem Sie Workflowphasen, Aktionen, Bedingungen und andere Elemente in einem Entwurfstool hinzufügen, das entweder SharePoint Designer 2013 oder Visual Studio 2012 sein kann. Das Designtool speichert dann den Workflow als XAML-Code, der zur Laufzeit interpretiert wird. Deklarative Workflows können entweder lokal in Project Server 2013 oder in Project Online ausgeführt werden. Mithilfe von Visual Studio 2012 können Sie auch benutzerdefinierte Aktionen und Formulare für zusätzliche Steuerelemente erstellen und Workflowvorlagen zur Wiederverwendung mit mehreren Project Web App-Instanzen speichern. SharePoint Designer 2013 kann benutzerdefinierte Aktionen nutzen, die in Visual Studio 2012 erstellt wurden.
  
Ein Project Server 2013-Workflow fungiert als App, in der ein Administrator, der über Entwurfsberechtigungen für Project Web App verfügt, einen deklarativen Workflow veröffentlichen und einem Enterprise-Projekttyp (EPT) zuordnen kann. Die EPT muss für ein Enterprise-Projekt verwendet werden, bei dem Project Server die Vollständige Kontrolle behält. Eine SharePoint Aufgabenliste kann keinen Project Serverworkflow verwenden. 
  
OAuth ermöglicht Projektmanagern mit Berechtigungen zum Erstellen von Projekten, den Workflow ohne Identitätswechsel aufzurufen. Workflowaufrufe an Project Server, z. B. zum Lesen eines benutzerdefinierten Feldwerts, um zu entscheiden, welche Verzweigung folgen soll, werden im Auftrag des Projektmanagers ausgeführt. Um zu verhindern, dass der Projektmanager einen Workflow erstellt, der automatisch zur nächsten Phase wechselt, wird der Aufruf für den Wechsel zur nächsten Workflowstufe als Workflowautor (Administrator) ausgeführt. Im Gegensatz dazu führen Benutzer von Legacy-Project Server 2010-Workflows imitierte Aufrufe über das Workflowproxybenutzerkonto durch, um Administratorzugriff im gesamten Workflow zu erhalten.
  
Obwohl Project server 2013 lokal kompilierte WF3.5-basierte Workflows verwenden kann, empfehlen wir, ältere Workflows auf deklarative Workflows basierend auf WF4 zu aktualisieren. Die neuere Technologie ist skalierbarer und robuster. Geschäftsanalysten und PMO-Mitarbeiter können Workflowdesigns mit Visio 2013 erstellen oder aktualisieren und Project Serverworkflows ohne Codierung mit SharePoint Designer 2013 implementieren.
  
Informationen zum Erstellen eines deklarativen Workflows für Project Web App finden Sie unter [Erste Schritte beim Entwickeln von Project Serverworkflows.](getting-started-developing-project-server-workflows.md) Einen Vergleich der SharePoint Designer- und Visual Studio-Funktionen für Workflows finden Sie unter [Entwickeln SharePoint 2013-Workflows mithilfe von Visual Studio.](https://msdn.microsoft.com/library/office/jj163199.aspx)
  
### <a name="client-side-object-model"></a>Clientseitiges Objektmodell
<a name="pj15_WhatsNew_CSOM"> </a>

Für den programmgesteuerten Zugriff auf Project Online ist ein CSOM erforderlich, das auf dem SharePoint CSOM basiert. Project Online Authentifizierung erfolgt mit OAuth unter Verwendung einer Windows Live-ID, nicht Project Serverformularauthentifizierung oder Windows Authentifizierung.
  
Es folgen die Prinzipien und Features des CSOM in Project Server 2013:
  
- Das CSOM wurde für benutzerfreundlichkeit entwickelt. Methoden und Eigenschaften verwenden oder stellen beispielsweise Daten direkt nach Namen bereit, anstatt viele GUIDs,  _changeXml-Parameter_ oder das Übergeben von Datasets zu erfordern. 
    
- Das Project Server-CSOM implementiert eine Teilmenge der PSI-Funktionalität, basierend auf den gängigsten Anforderungen für Lösungen von Drittanbietern.
    
- Das CSOM ruft intern die PSI auf, wird jedoch unterschiedlich faktoriert. Aktualisierungen für alle Statuserfassungsänderungen erfolgen beispielsweise über die **StatusAssignmentCollection.SubmitAllStatusUpdates-Methode,** nicht durch die **Statusing.SubmitStatus** PSI-Methode für den Benutzer oder die **SubmitStatusForResource-Methode** für andere Ressourcen. 
    
- Der Zugriff auf das CSOM erfolgt über einen WCF-Dienst (Client.svc) und nicht über die 22 öffentlichen Dienste der PSI.
    
- Die Initialisierung des Project Server-CSOM erfolgt direkt über die [ProjectContext-Klasse](https://msdn.microsoft.com/library/Microsoft.ProjectServer.Client.ProjectContext.aspx) mit der Project Web App-URL, nicht mithilfe eines WCF-Verweises oder einer Proxyassembly. 
    
- Das CSOM implementiert mehrere Clientbibliotheken und Schnittstellen, die von der internen SharePoint CSOM-Infrastruktur unterstützt werden. Die Clientbibliotheken und Schnittstellen umfassen Folgendes:
    
  - Microsoft .NET-Clientbibliothek in der Microsoft.ProjectServer.Client.dll assembly
    
  - Silverlight-Bibliothek in der Microsoft.ProjectServer.Client.Silverlight.dll Assembly
    
  - Windows Phone 8 Bibliothek in der Microsoft.ProjectServer.Client.Phone.dll Assembly
    
  - JavaScript-Bibliothek für Webanwendungen in der PS.js- oder PS.debug.js datei
    
  - REST-Endpunkte für den Zugriff mit dem OData-Protokoll
    
  - Native Unterstützung für LINQ-Abfragen mit Filterung, um die zurückgegebene Datenmenge zu begrenzen
    
- Das CSOM kann unabhängig von der PSI und anderen Project Serverassemblys wie Microsoft.Office.Project.Server.Library.dll sowohl für Project Online als auch für lokale Lösungen verwendet werden.
    
- Zusätzliche Funktionen des Project Server 2013-CSOM können für kumulative Updates und Service Packs berücksichtigt werden, basierend auf Anforderungen von Project Server-Partnern und der Entwicklercommunity.
    
> [!NOTE]
> Das CSOM ist die bevorzugte Schnittstelle für Drittanbieter-Project Serverentwickler. Wir empfehlen, dass Sie für die Entwicklung neuer Anwendungen das CSOM verwenden, sofern das CSOM alle für Ihre Anwendung erforderlichen Funktionen umfasst. 
  
Informationen zum Entwickeln mit dem CSOM finden Sie unter [Clientseitiges Objektmodell (CSOM) für Project 2013.](client-side-object-model-csom-for-project-2013.md) Informationen zur REST-Schnittstelle in SharePoint Anwendungen finden Sie in der SharePoint 2013-Entwicklerdokumentation unter *Programmieren mithilfe des SharePoint REST-Diensts.* 
  
### <a name="changes-in-the-reporting-database"></a>Änderungen in der Berichtsdatenbank
<a name="pj15_WhatsNew_RDBChanges"> </a>

Die vier Datenbanken in Project Server 2010 werden in Project Server 2013 zu einer einzigen Project Datenbank kombiniert. Der Standardname der Project-Datenbank lautet ProjectService. Berichtstabellen und -ansichten behalten ihre vorherigen Namen bei, und Tabellen und Ansichten aus den Datenbanken "Entwurf", "Veröffentlicht" und "Archiv" haben die Präfixe  `draft`  `pub` und in der  `ver` ProjectService-Datenbank. Die veröffentlichte Projekttabelle ist z. B. "pub". MSP_PROJECTS. 
  
> [!IMPORTANT]
> Der direkte Zugriff wird für die `draft` Entwurfstabellen ( Präfix), veröffentlichten ( `pub` ) und Archivtabellen und -ansichten ( ) nicht `ver` unterstützt. Berichte sollten nur die Berichtstabellen und -ansichten verwenden, die das `dbo` Präfix aufweisen. Beispiel: der DBO. MSP_EpmProject Tabelle enthält die Liste der Projekte in der Project Web App-Instanz. 
>
> Es gibt nichts, was Sie aktiv daran hindert, den direkten programmgesteuerten Datenbankzugriff zum Aktualisieren von Daten in tabellen und Ansichten in der Project Datenbank zu verwenden. Beachten Sie, dass die Project Professional Cache, die Tabellen für Entwurfs- und veröffentlichte Daten sowie die Berichtstabellen alle auf einem Cachesynchronisierungsprotokoll basieren, das durch direkte Datenbearbeitung unterbrochen werden kann. Wenn Sie Ihre Project Serverdatenbanken beschädigen oder Project Professional clientseitigen Caches mithilfe des direkten Zugriffs zum Ändern von Daten beschädigen, werden Sie gewarnt, dass der Produktsupport nicht helfen kann! 
  
Project Server 2013 führt einen OData-Dienst für den Online- und lokalen Zugriff ein. Die Onlineberichtstabellen und -ansichten werden nur von der OData-Schnittstelle verfügbar gemacht. Zur lokalen Verwendung können Sie die OData-Schnittstelle verwenden oder direkt auf die Berichtstabellen und -ansichten in der ProjectService-Datenbank in der SharePoint Farm zugreifen. Project Online unterstützt keine mehrinstanzenfähige Datenbank. Das heißt, mehrere Instanzen von Project Web App verfügen jeweils über eine eigene Project Datenbank. Der OData-Dienst führt intern SQL Abfragen der Berichtstabellen und -ansichten aus und liefert eine XML- oder JSON-Nutzlast. Eine Einführung in den OData-Dienst für die Berichterstellung in Project Server 2013 und die **ProjectData-Schemareferenz** finden Sie unter [ProjectData – Project OData-Dienstreferenz.](https://msdn.microsoft.com/library/office/jj163015.aspx)
  
Allgemeine Informationen zu OData-Abfragen finden Sie unter [OData: URI-Konventionen.](https://www.odata.org/documentation/) Beispielsweise können Sie alle Projekte in einer lokalen Instanz von Project Web App sehen, in der der Projektname mit "Test" beginnt, indem Sie die folgende Abfrage in einem Browser verwenden. Klicken Sie mit der rechten Maustaste auf die Browserseite, und klicken Sie dann auf **Quelle anzeigen.**
  
```html
https://ServerName /ProjectServerName /_api/ProjectData/Projects?$filter=startswith(ProjectName, 'Test') eq true
```

Um Projektdaten in PowerPivot in Excel 2013 zu importieren, wählen Sie im Menüband "DATEN" im Dropdownmenü **"Aus anderen Quellen"** die Option **"Aus OData-Datenfeed" aus.** Geben Sie im Dialogfeld **"Datenverbindungs-Assistent"** https://ServerName/ProjectServerName/_api/ProjectData/ den Datenfeedspeicherort ein, wählen Sie **"Weiter"** aus, und wählen Sie dann auf der Seite **"Tabellen auswählen"** des Assistenten die Tabelle **"Projekte"** aus. Nennen Sie die ODC-Datei, speichern Sie sie, und wählen Sie dann **"Fertig stellen"** aus. Wählen Sie im Dialogfeld **"Daten importieren"** die Option **"PivotTable-Bericht"** aus. Wählen Sie im Excel Arbeitsblatt Felder für die PivotTable-Zeilen und -Spalten aus, die Sie anzeigen möchten.
  
Lokale Project Serverbenutzer, die über die richtigen Berechtigungen verfügen, können wie in Project Server 2010 direkt über Microsoft SQL Server auf berichtstabellen und -ansichten zugreifen, um Berichte zu erstellen. In Project Server 2013 können Benutzer auch über die OData-Schnittstelle auf die lokalen Berichtstabellen zugreifen. Sie können Project Serverdaten online oder lokal über REST-Endpunkte für den OData-Dienst abrufen. Beispiel: der DBO. MSP_PROJECT Tabelle und dem DBO. MSP_EpmProject_UserView Ansicht kann für Berichte verwendet werden. Alle Tabellen oder Ansichten mit einem `draft` `pub` , oder `ver` Präfix sind nur für die interne Verwendung durch Project Server vorgesehen und dienen nicht der Berichterstellung. Beispielsweise der Entwurf. MSP_TASKS Tabelle und die Veröffentlichung. MSP_PROJECTS_WORKING_VIEW Ansicht sind nicht dokumentiert und dienen nur der internen Verwendung. 
  
> [!NOTE]
> Sie können die lokale Berichterstellung erweitern, indem Sie Tabellen, Ansichten, Felder und gespeicherte Prozeduren in einer separaten Datenbank hinzufügen. Sie sollten die vorhandenen Berichtstabellen und -ansichten in der Project Serverdatenbank nicht ändern. 
  
Die Berichtstabellen, Ansichten und Felder in der Project Datenbank werden in einer HTML-Hilfedatei in einem späteren Update des Project 2013 SDK-Downloads dokumentiert. Eine Dokumentation des OData-XML-Schemas für den **ProjectData-Dienst** finden Sie unter [ProjectData – Project OData-Dienstreferenz.](https://msdn.microsoft.com/library/office/jj163015.aspx) Abfragen der Berichtstabellen und -ansichten, die für Project Server 2010 erstellt wurden, funktionieren in den meisten Fällen mit der Project-Datenbank in Project Server 2013. Lokale Benutzer können auf die Project Server-OLAP-Cubes in SQL Server Analysis Services zugreifen, wie dies derzeit der Fall ist. In Project Online stehen keine OLAP-Cubes zur Verfügung.
  
### <a name="task-pane-add-ins-in-project"></a>Aufgabenbereich-Add-Ins in Project
<a name="pj15_WhatsNew_Agave"> </a>

Sowohl Project Standard 2013 als auch Project Professional 2013 unterstützen Aufgabenbereich-Add-Ins, mit denen externe Inhalte in einer Webseite integriert und angezeigt werden können. Im Aufgabenbereich werden Webseiteninhalte angezeigt, die über JavaScript Zugriff auf Aufgaben, Ressourcen, Ansichten und allgemeine Projektdaten haben. Das JavaScript-Objektmodell für Project kann Informationen zu einem ausgewählten Vorgang oder einer ausgewählten Ressource abrufen und Daten in einer ausgewählten Zelle im Raster für Ansichten wie das Gantt-Diagramm abrufen. Aufgabenbereich-Add-Ins für Project können auch Ereignishandler für Aufgaben-, Ressourcen- oder Ansichtsauswahlereignisse implementieren. 
  
Abbildung 2 zeigt das Aufgabenbereich-Add-In **"Hello ProjectData",** das den **ProjectData-Dienst** abfragt und dann die Daten im aktuellen Projekt mit den Durchschnittswerten für alle Projekte vergleicht. Der Project 2013 SDK-Download enthält den vollständigen Quellcode für das Add-In. 
  
**Abbildung 2. Ein Aufgabenbereich-Add-In in Project Professional kann auf Daten in Project Server zugreifen**

![Vergleichen des aktuellen Projekts mit allen Projekten](media/pj15_RestQueryApp_CompareProject.gif "Vergleichen des aktuellen Projekts mit allen Projekten")
  
> [!NOTE]
> Project Standard 2013 kann nicht direkt mit Project Server 2013 über Aufgabenbereich-Add-Ins integriert werden. 
  
Aufgabenbereich-Add-Ins in Project Professional können Webparts unterstützen, die für Project Server 2013 erstellt wurden, sodass Entwickler eine Erweiterung erstellen können, sobald sie mit Project Web App und Project Professional ausgeführt wird. Allgemeine Aufgabenbereich-Add-Ins, die für andere Office 2013-Produkte entwickelt wurden, können auch mit Project Standard 2013 und Project Professional 2013 verwendet werden. Weitere Informationen finden Sie unter [Aufgabenbereich-Add-Ins für Project.](task-pane-add-ins-for-project.md)
  
### <a name="project-server-event-receivers"></a>Project Serverereignisempfänger
<a name="pj15_WhatsNew_Events"> </a>

Es können mehrere Project Web App-Server (auch als Web-Front-End-Server oder WFEs bezeichnet) in einer SharePoint Farm vorhanden sein, die die Back-End-Project-Dienstanwendung enthält. Ereignisempfänger werden auch Ereignishandler genannt. Lokale Ereignishandler können mit voll vertrauenswürdigem Code implementiert und auf allen WFEs für eine lokale Project Serverinstallation bereitgestellt werden. Remoteereignisempfänger können in Webdiensten auf lokalen oder Remoteservern implementiert werden und von mehreren WFEs und mehreren Project Serverinstallationen aufgerufen werden. Project Online können nur Remoteereignisempfänger verwenden.
  
Project Serverereignishandler werden von SharePoint für jede Project Web App-Instanz und nicht von einer bestimmten Project Web App Einstellungen Seite verwaltet. Wählen Sie in der Anwendung SharePoint Zentraladministration die Option **"Allgemeine Anwendung Einstellungen"** aus, **wählen** Sie unter **PWA Einstellungen** verwalten und dann die Instanz in der Dropdownliste Project **Web App-Instanz** auf der PWA Einstellungen Seite aus. Um einen lokalen Ereignishandler oder einen Remoteereignisempfänger hinzuzufügen, wählen Sie **serverseitige Ereignishandler aus.**
  
Für eine lokale Installation von Project Server können Sie einen Remoteereignisempfänger als SharePoint Feature erstellen, das die [Microsoft.ProjectServer.Client.EventHandlerCreationInformation-Klasse](https://msdn.microsoft.com/library/Microsoft.ProjectServer.Client.EventHandlerCreationInformation.aspx) im CSOM verwendet, und dann den Ereignisempfänger programmgesteuert mithilfe von Methoden in der [EventHandlerCollection-Klasse](https://msdn.microsoft.com/library/Microsoft.ProjectServer.Client.EventHandlerCollection.aspx) verwalten. Bei Remoteereignisempfängern sind Pre-Ereignisse synchron, Post-Ereignisse asynchron, und es gibt ein Timeout für Fälle, in denen der Remoteereignisempfänger nicht zurückgegeben wird. 
  
> [!NOTE]
> SharePoint Die Zentraladministration ist nur für lokale Installationen verfügbar. Für Project Online und SharePoint Online können Sie Remoteereignisempfänger mithilfe eines CSOM-basierten App-Pakets hinzufügen oder entfernen. 
  
Auf der Seite "Serverseitige Ereignishandler" entspricht der Vorgang zum Hinzufügen eines lokalen Ereignishandlers für eine lokale Project Serverinstallation fast dem im [Ereignishandler "Erstellen eines Project Servers"](https://msdn.microsoft.com/library/gg615466.aspx) beschriebenen Prozess und dem Protokollieren eines Ereignisthemas für Project Server 2010. Der Unterschied besteht darin, dass die Seite "Neuer Ereignishandler" über zusätzliche Optionen verfügt. For example, choose **Project Creating** in the **Events** list, and then choose NEW **EVENT HANDLER**. Auf der Seite "Neuer Ereignishandler" sind die einzigen beiden erforderlichen Felder **Name** und **Reihenfolge** (siehe Abbildung 3). Wenn Sie einen lokalen voll vertrauenswürdigen Ereignishandler hinzufügen, fügen Sie das **Feld Assemblyname** und das Feld Class **Name** hinzu. **Endpunkt-URL** leer lassen. Wenn Sie einen Remoteereignisempfänger hinzufügen, fügen Sie **die Endpunkt-URL** hinzu, und lassen **Sie Assemblyname** und **Klassenname** leer. 
  
> [!CAUTION]
> Wenn Sie *sowohl* den Assemblynamen/den Klassennamen als auch die Endpunkt-URL angeben, ruft Project Server nur den lokalen Ereignishandler auf. Der Remoteereignisempfänger wird ignoriert. 
> 
> Wenn Sie zwei Ereignishandler für dasselbe Ereignis erstellen, wobei ein Ereignishandler lokal und einer ein Remoteereignisempfänger ist und der **Order-Wert** für beide identisch ist, ignoriert Project Server den Remoteereignisempfänger. 
  
**Abbildung 3. Hinzufügen eines lokalen Ereignishandlers oder eines Remoteereignisempfängers**

![Konfigurieren eines Ereignishandlers oder Ereignisempfängers](media/pj15_EventHandlers_NewEventHandler.gif "Konfigurieren eines Ereignishandlers oder Ereignisempfängers")
    
Wenn Sie Zugriff auf PSI-Datasets für einen lokalen Ereignishandler benötigen, können Sie die Microsoft.Office.Project.Schema.dll Assembly aus der [Windows]\Microsoft.NET\assembly\GAC \_ MSIL\Microsoft.Office kopieren. Project. Schema\v4.0_15.0.0.0__71e9bce111e9429c directory. 

Anstelle der PSI wird empfohlen, die Ereignisklassen im **Microsoft.ProjectServer.Client-Namespace** zu verwenden. für die Entwicklung mit dem CSOM ist keine Bearbeitung von Datasets erforderlich. Zum Entwickeln von Remoteereignisempfängern für Project Online müssen Sie die [Ereignisklasse](https://msdn.microsoft.com/library/Microsoft.ProjectServer.Client.Event.aspx) und die [EventHandlerCreationInformation-Klasse](https://msdn.microsoft.com/library/Microsoft.ProjectServer.Client.EventHandlerCreationInformation.aspx) im CSOM verwenden. 
  
Bevor Sie einen Project Server-Ereignishandler bereitstellen, installieren und testen Sie den Ereignishandler sorgfältig bei einer Testinstallation von Project Server. Bei einer lokalen Project Serverinstallation kann der Project Server 2013-Ereignisdienst die anderen gültigen benutzerdefinierten Ereignishandler nicht laden, wenn der von Ihnen hinzugefügte lokale Ereignishandler nicht mehr funktioniert. In diesem Fall müssen Sie den Problemereignishandler entfernen und den Ereignisdienst neu starten.
  
> [!NOTE]
> Für eine lokale Project Serverinstallation wird empfohlen, dass Sie mithilfe des CSOM zu Remoteereignisempfängern migrieren, um Ereignisempfänger zu entwickeln. Da Remoteereignisempfänger keinen Code von Drittanbietern im Project Serverereignisdienst ausführen, sind Remoteereignisempfänger stabiler. Lokale Administratoren sind nicht für die Verwaltung des Project Serverereignisdiensts verantwortlich. 
  
Allgemeine Informationen zu Ereignissen finden Sie unter [Behandeln von Ereignissen in Apps für SharePoint.](https://msdn.microsoft.com/library/jj220048%28office.15%29.aspx) 
  
## <a name="deprecated-features"></a>Veraltete Features
<a name="pj15_WhatsNew_Deprecated"> </a>

> [!NOTE]
> Informationen zu Features und APIs, die in Project Server 2016 Vorschau veraltet oder entfernt sind, finden Sie unter ["Veraltet" oder "Entfernt" in Project Server 2016 Vorschau.](https://docs.microsoft.com/project/what-s-deprecated-or-removed-in-project-server-2016) 
  
Veraltete Features sind in Project 2013 für einige Lösungen weiterhin verfügbar, sollten jedoch nicht für die Neuentwicklung verwendet werden. Die meisten der folgenden Features und Methoden funktionieren nicht mit Project Online oder mit der standardmäßigen lokalen Installation von Project Server 2013 im SharePoint Berechtigungsmodus. Vorhandene Lösungen, die diese Features verwenden, funktionieren möglicherweise nicht für ein Upgrade von Project Server 2010 auf Project Server 2013. Obwohl Lösungen, die veraltete Features verwenden, in einigen Fällen weiterhin funktionieren, werden sie nicht für alle Project 2013-Installationen vollständig unterstützt.
  
Wenn Ihre Lösungen veraltete Features verwenden, sollten sie vor der Bereitstellung sorgfältig getestet werden, und Sie sollten sie so ändern, dass unterstützte Features verwendet werden, sobald dies praktisch ist. Informationen zum Konfigurieren lokaler Project Server 2013-Sicherheit für Project Berechtigungsmodus finden Sie im Abschnitt *SharePoint Berechtigungsmodus* unter [Neuigkeiten für IT-Spezialisten in Project Server 2013.](https://docs.microsoft.com/project/what-s-new-for-it-pros-in-project-server-2016)
  
-  [Erweiterungs-PSI-Erweiterungsszenarien](https://docs.microsoft.com/previous-versions/office/developer/office-2010/ff843378(v=office.14)) sind veraltet und werden in zukünftigen Versionen nicht unterstützt. Diese lokalen Project Server 2013-Szenarien ermöglichten die Integration mithilfe von benutzerdefinierten Windows Communication Foundation (WCF)-Diensten. 
  
- **Project PSI** Die [Project-Klasse](https://docs.microsoft.com/office/client-developer/project/project-psi-reference-overview) der PSI ist veraltet. Verwenden Sie für alle Neuentwicklungen das [Project CSOM.](client-side-object-model-csom-for-project-2013.md) Project Server 2013-Apps, die die Project PSI verwenden, funktionieren weiterhin, aber Project Online Apps müssen alle PSI-Methoden der Project-Klasse durch ihre entsprechenden CSOM-Methoden ersetzen.
  
- **Ressourcenplan-PSI** Die [PSI des Ressourcenplans](https://docs.microsoft.com/previous-versions/office/project-class/gg240019(v=office.15)) ist veraltet. Es wird weiterhin für Project 2013-Entwicklung unterstützt, aber in zukünftigen Versionen nicht unterstützt. 
  
- **ASMX-Schnittstelle für die PSI** Die PSI enthält doppelte Schnittstellen für die Entwicklung lokaler Project Servererweiterungen. Die ASMX-Webdienstschnittstelle wurde mit der ersten Implementierung der PSI in Office Project Server 2007 eingeführt. Project Server 2010 hat die WCF-Dienstschnittstelle hinzugefügt, wobei das Objektmodell im Wesentlichen die ASMX-Webdienste dupliziert. Obwohl Project Server 2013 weiterhin ASMX und WCF unterstützt, sollten neue Lösungen, die die PSI erfordern, die WCF-Dienste verwenden. Wenn möglich, sollten neue Lösungen mithilfe des CSOM geschrieben werden. 
  
  Die ASMX-Webdienste der PSI sind in Project Server 2013 veraltet. Um in zukünftigen Project Serverversionen funktionieren zu können, müssen Lösungen, die die ASMX-Webdienste verwenden, so umgeschrieben werden, dass sie entweder die WCF-Dienste oder das CSOM verwenden. Weitere Informationen finden Sie im Abschnitt zum Aktualisieren von Anwendungen mit dem Abschnitt *Project Server-APIs* in [Project Serverprogrammierbarkeit.](project-server-programmability.md)
  
- **Objektlinkanbieter (Object Link Provider, OLP)** In früheren Versionen von Project Server bietet der **ObjectLinkProvider-Dienst** in der PSI (siehe [WebSvcObjectLinkProvider)](https://docs.microsoft.com/previous-versions/office/ms481347(v=office.14)) eine Möglichkeit, Webobjektverknüpfungen zwischen Enterprise-Projektaufgaben und speziellen SharePoint Listen auf der Projektwebsite für Probleme, Risiken, Lieferumfang und Dokumente zu verwalten. In Project Server 2013 ist olp veraltet. 
  
  Sie können die **[RelatedItemManager-Klasse](https://docs.microsoft.com/previous-versions/office/sharepoint-server/jj168020(v=office.15))** im SharePoint CSOM verwenden, um Webobjektverknüpfung zwischen Elementen in der Aufgabenliste und den anderen Listen in einer Projektwebsite zu erstellen, zu lesen und zu löschen. Um beispielsweise einen Link von einem Aufgabenelement zu einem Problem hinzuzufügen, können Sie die **[AddSingleLink](https://docs.microsoft.com/previous-versions/office/sharepoint-server/jj166451(v=office.15))** -Methode oder eine der beiden ähnlichen Methoden, **AddSingleLinkFromUrl** oder **AddSingleLinkToUrl** verwenden. Die **RelatedItemManager-Klasse** enthält auch Methoden zum Löschen eines Webobjektlinks und zum Lesen verwandter Elemente. Die entsprechende Klasse im JSOM (das JavaScript-Objektmodell) finden Sie unter [SP. RelatedItemManager-Objekt (sp.js)](https://docs.microsoft.com/previous-versions/office/sharepoint-visio/jj838582(v=office.15)).
  
  Es wird empfohlen, die SharePoint CSOM zum Erstellen von OLP-Apps für eine lokale Installation von Project Server 2013 und für Project Online zu verwenden. Der [Namespace "Microsoft.SharePoint"](https://docs.microsoft.com/previous-versions/office/sharepoint-server/ms464984(v=office.15)) enthält keine **RelatedItemManager** - Klasse. 
  
- **Benutzerdefinierte Berechtigungen** Benutzerdefinierte Sicherheitsberechtigungen für den Zugriff auf bestimmte Project Serverfeatures oder -erweiterungen wurden in Office Project Server 2007 unterstützt, in dem in einem SDK-Artikel erläutert wurde, wie sie durch direktes Ändern der veröffentlichten Datenbank erstellt werden. In Project Server 2010 funktionieren benutzerdefinierte Berechtigungen weiterhin, sind jedoch veraltet. In Project Server 2013 funktionieren benutzerdefinierte Berechtigungen nicht mit dem Standardmäßigen SharePoint Berechtigungsmodus für lokale Installationen. Für den Project Berechtigungsmodus werden benutzerdefinierte Berechtigungen unterstützt. Bei Project Online ist kein direkter Datenbankzugriff möglich. 
  
- **Identitätswechsel** Der Identitätswechsel in PSI-basierten Apps, bei denen der Benutzer einer App die Sicherheitsberechtigungen eines anderen Project Serverbenutzers annehmen kann, ist in Project Server 2013 veraltet. Wie bereits erwähnt, verwendet eine standardmäßige lokale Project Server 2013-Installation SharePoint Berechtigungsmodus, der den Identitätswechsel in den Project Server-Sicherheitsgruppen nicht zulässt. Weitere Informationen finden Sie unter [Authentication, authorization, and security in SharePoint 2013](https://docs.microsoft.com/sharepoint/dev/general-development/authentication-authorization-and-security-in-sharepoint).
  
  Statuserfassungsanwendungen sind typische Erweiterungen, die in früheren Versionen von Project Server möglicherweise den Identitätswechsel verwendet haben. Project Server 2010 führte die **ReadStatusForResource-Methode** und die **SubmitStatusForResource-Methode** in der PSI zusammen mit der globalen **StatusBrokerPermission-Berechtigung** ein, wodurch der Identitätswechsel den Status im Namen eines anderen Benutzers lesen und aktualisieren musste. Das CSOM in Project Server 2013 verwendet die zugrunde liegende PSI, um Statuserweiterungen transparent zu aktivieren, und kann für Project Online oder lokale Installationen verwendet werden. 
  
- **Berichtsdatenbankerweiterungen** Das Hinzufügen von benutzerdefinierten Tabellen und Ansichten zur Berichtsdatenbank ist bei früheren Versionen von Project Server üblich. Da Project Server 2013 die vier Datenbanken früherer Versionen in einer Datenbank kombiniert, übertragen Upgrades keine benutzerdefinierten Tabellen, Ansichten oder SPROCs in die Berichtstabellen in der Project Server 2013-Datenbank. 
  
  Es wird empfohlen, entweder SQL Azure oder eine separate SQL Server Datenbank für benutzerdefinierte Berichtstabellen und Ansichten zu verwenden, in denen Sie Datenbanksicherungen und -updates verwalten können. Für Project Online ist dies erforderlich.
  
- **Berichterstellung** Die lokalen Berichtstabellen und -ansichten in der Project Serverdatenbank sowie die OLAP-Cubes sind *nicht* veraltet und werden weiterhin vollständig unterstützt. Auf berichtstabellen und -ansichten (die Berichtsdatenbank in früheren Project Serverversionen) kann in Project Online jedoch nicht zugegriffen werden. In ähnlicher Weise sind OLAP-Cubes nur für lokale Installationen von Project Server 2013 verfügbar. Für Berichterstellungsanwendungen mit Project Online können Sie den **ProjectData-Dienst** über REST-Abfragen mit dem OData-Protokoll verwenden. 
  
- **Project Handbuch** Das Project Handbuch ist ein Standardfeature in den Office Project 2007-Desktopanwendungen, bei dem HTML- und JavaScript-Inhalte in einem Aufgabenbereich interaktive Anleitungen zum Erstellen und Verwalten von Projekten bereitstellen. In Project 2010 ist das Project Handbuch nicht in einer Standardinstallation verfügbar, kann aber über VBA oder ein VSTO-Add-In aktiviert werden. Der Project 2010 SDK-Download enthält die geänderten Project Handbuchdateien. 
  
  Das VBA-Objektmodell und die **Microsoft.Office. Das Interop.MSProject-Objektmodell** in Project 2013 enthält weiterhin die 22 Member der **Application-Klasse** und die **Project-Klasse,** die das Project Handbuch verwalten kann. Project 2013-Aufgabenbereich-Apps können jedoch mit Aktionen in einem Project Aufgabenbereich "Handbuch" in Konflikt stehen, und Project Handbuchinhalte können nicht einfach verteilt oder im Office Store verkauft werden. Es wird dringend empfohlen, Project Aufgabenbereichslösungen mit Office Add-Ins zu entwickeln, nicht mit benutzerdefinierten Project Guide-Inhalten. Weitere Informationen zum Project Handbuch finden Sie in der [Project 2010 SDK-Dokumentation.](https://msdn.microsoft.com/library/ms512767.aspx)
  
## <a name="comparing-project-server-on-premises-with-project-online"></a>Vergleich Project lokalen Servers mit Project Online
<a name="pj15_WhatsNew_Comparing"> </a>

Project In Tabelle 2 werden die erweiterbaren Features einer Project Online lokalen Installation von Project Server 2013 mit Project Online verglichen. Tabelle 2 enthält keine Unterschiede bei der Bereitstellung, Verwaltung oder Verwendung. Weitere Informationen zu Project Online und Project Server 2013 finden Sie unter [Project 2013 für Entwickler](https://developer.microsoft.com/project/docs) und [Project Online.](https://developer.microsoft.com/project)
  
**Tabelle 2. Erweiterbarkeit von lokalen Project Server und Project Online**

| Feature |Project Lokaler Server | Project Online |
|:-----|:-----|:-----|
|**Programmierbarkeit** <br/> |CSOM-basierte Apps; Einheitliches Programmiermodell  <br/>– .NET-, Silverlight-, Windows Phone-Clientbibliotheken  <br/>- JavaScript-Bibliothek für benutzerdefinierte Seiten, Webparts und Menübanderweiterungen  <br/>- OData- und REST-Protokolle<br/><br/> PSI-basierte Apps; Komplexes Programmiermodell, kann auch Apps für Verwaltung, Portfolioanalyse, Benachrichtigungen, sicherheit im Project modus, Warteschlangensystem und andere Bereiche erstellen.<br/><br/>PSI-Erweiterungen  <br/><br/>Benutzerdefinierte Berechtigungen mit Project-Modussicherheit (veraltet)  <br/><br/>Identitätswechsel mit der PSI (veraltet)  <br/><br/>Voll vertrauenswürdiger Code; Installieren von Erweiterungen in SharePoint Farm  <br/> |CSOM-basierte Apps; Einheitliches Programmiermodell  <br/>– .NET-, Silverlight-, Windows Phone-Clientbibliotheken<br/>- JavaScript-Bibliothek für benutzerdefinierte Seiten, Webparts und Menübanderweiterungen<br/>- OData- und REST-Protokolle<br/><br/>Kann die PSI verwenden, wird jedoch nicht unterstützt: keine OAuth- und keine Dienst-zu-Dienst-Verbindungen<br/><br/>Keine Erweiterungen der CSOM-API<br/><br/>Keine benutzerdefinierten Berechtigungen<br/><br/>Kein Identitätswechsel<br/><br/>Kein voll vertrauenswürdiger Code  <br/> |
|**Benutzerdefinierte Datenbanken** <br/> |- SQL Azure  <br/>- SQL Server (Das Ändern von Berichtstabellen und Ansichten in der Project Serverdatenbank wird nicht unterstützt)  <br/> |- SQL Azure  <br/>- SQL Server (Das Ändern von Berichtstabellen und Ansichten in der Project Serverdatenbank wird nicht unterstützt)  <br/> |
|**Berichterstellung** <br/> |- **ProjectData-Dienst;** OData- und REST-Protokolle  <br/>– Berichterstellungstabellen und -ansichten in der Project Serverdatenbank<br/>– OLAP-Datenbank  <br/> |- **ProjectData-Dienst;** OData- und REST-Protokolle  <br/> |
|**Ereignishandler** <br/> |– Remoteereignisempfänger, auf die über WCF-Endpunkte zugegriffen werden kann<br/>– Voll vertrauenswürdige Ereignishandler, installiert in SharePoint Farm  <br/> | – Remoteereignisempfänger, auf die über WCF-Endpunkte zugegriffen werden kann  <br/> |
|**Workflows** <br/> |Deklarative Workflows, erstellt mit SharePoint Designer 2013<br/>– Nur für eine bestimmte Project Web App-Instanz verwenden<br/>- Kann ein Workflowdesign aus Visio 2013 importieren<br/>- Kann benutzerdefinierte Aktionen importieren und verwenden<br/><br/> Deklarative Workflows, erstellt mit Visual Studio 2012<br/>– Erstellen einer App, die Workflows enthalten kann<br/>– Erstellen eines SharePoint Lösungspakets (WSP), das Workflows enthalten kann<br/>- Erstellen von Workflowvorlagen zur Wiederverwendung<br/>- Erstellen und Verwenden von benutzerdefinierten Aktionen  <br/><br/>Kann ältere kompilierte Workflows verwenden, die mit WF3.5 erstellt wurden (Upgrade auf deklarativen WF4-Workflow empfehlen)  <br/> |Deklarative Workflows, erstellt mit SharePoint Designer 2013<br/>– Nur für eine bestimmte Project Web App-Instanz verwenden<br/>- Kann ein Workflowdesign aus Visio 2013 importieren<br/>- Kann benutzerdefinierte Aktionen importieren und verwenden  <br/><br/>Deklarative Workflows, erstellt mit Visual Studio 2012<br/>– Erstellen einer App, die Workflows enthalten kann  <br/>– Erstellen eines SharePoint Lösungspakets (WSP), das Workflows enthalten kann<br/>- Erstellen von Workflowvorlagen zur Wiederverwendung <br/>- Erstellen und Verwenden von benutzerdefinierten Aktionen  <br/> |
|**Verteilung** <br/> |– Office Store (für CSOM-basierte Apps)<br/>– Privater App-Katalog auf SharePoint<br/>– Intranet-Dateifreigabe  <br/> |- Office Store<br/>– Privater App-Katalog auf SharePoint  <br/> |

   
## <a name="conclusion"></a>Schlussbemerkung
<a name="pj15_WhatsNew_Conclusion"> </a>

Project Server 2013 bietet eine Fülle neuer Entwicklungsfunktionen und Szenarien, die Partner und Kunden verwenden können, um die Funktionen und den Nutzen von Project Server in großen Unternehmen und in kleinen Organisationen anzupassen und zu erweitern. Sie können die Infrastruktur für Office 2013 und SharePoint 2013 verwenden, um Apps für Project 2013 zu erstellen und zu verteilen, die die Marktfähigkeit und Verwendung von benutzerdefinierten Anwendungen erheblich erweitern können. Einige Erweiterungsfeatures und -methoden früherer Versionen sind in Project 2013 veraltet, insbesondere die ASMX-Webdienste der PSI und Features, die Identitätswechsel oder direkte Datenbankänderungen beinhalten, die nicht mit Project Online verwendet werden können.
  
Die Einführung des CSOM ermöglicht den programmgesteuerten Zugriff auf Project Online für eine Vielzahl von Geräten und die Verwendung von JavaScript in Webanwendungen. Das CSOM bietet ein konsistenteres Programmiermodell im Vergleich zur PSI. Project Auf Serverdaten kann viel mehr zugegriffen werden als in früheren Versionen, einschließlich über den Online-OData-Dienst und über REST-Endpunkte zum Melden von Daten in der Project-Datenbank. Vorhandene Berichte funktionieren weiterhin auf die gleiche Weise für die lokale Verwendung. Neue Berichte haben mehr Flexibilität.
  
Office Add-Ins bieten eine neue Möglichkeit, Lösungen zu verkaufen und Project Standard 2013 mit Webinhalten und anderen Office 2013-Produkten zu integrieren. Sie können auch neue Möglichkeiten zur Integration von Project Professional 2013 mit Project Serverdaten und SharePoint Listen über Aufgabenbereich-Office-Add-Ins erstellen.
  
Weitere Informationen zum Entwickeln von Apps und zur Verwendung der Programmierbarkeitsfeatures und des CSOM von SharePoint Server 2013 finden Sie unter [SharePoint für Entwickler](https://docs.microsoft.com/sharepoint/dev/) und Office für [Entwickler.](https://developer.microsoft.com/office/docs)
  
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
    

