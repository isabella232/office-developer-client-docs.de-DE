---
title: Updates für Entwickler in Project
manager: soliver
ms.date: 09/29/2015
ms.audience: Developer
localization_priority: Normal
ms.assetid: 5b2b22cd-6e28-43a8-9092-b411da8bfb53
description: Neue Features umfassen eine Client-seitigen Objektmodell (CSOM), die REST-Schnittstellen, die einen OData-Dienst für reporting, remote-Ereignisempfänger, deklarative Workflows und Task Pane-add-ins für Project-Clients.
ms.openlocfilehash: facd52c5ba2473de41f2a6bede431af0f55ba4ac
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19796315"
---
# <a name="updates-for-developers-in-project"></a>Updates für Entwickler in Project

Erweiterungsmöglichkeiten in Project Server 2013 arbeiten mit der add-ins für Project Online und mit-Installationen vor Ort. Neue Features umfassen eine Client-seitigen Objektmodell (CSOM), die REST-Schnittstellen, die einen OData-Dienst für reporting, remote-Ereignisempfänger, deklarative Workflows und Task Pane-add-ins für Project-Clients. Auch Informationen Sie zu veralteten Features, die nicht für die Entwicklung neuer verwendet werden soll.
  
Projektserver 2013 basiert auf dem Framework mit Microsoft Office Project Server 2007 eingeführt und von Project Server 2010 erweitert. Projektserver 2013 Fügt eine Client-seitigen Objektmodell (CSOM), das umgestaltet wird von Project Server Interface (PSI) vereinfacht und enthält eine JavaScript-Bibliothek und .NET Framework 4-Bibliotheken für apps Windows, Windows Phone 8 und Microsoft Silverlight. Das CSOM ist darauf ausgelegt, für die Entwicklung für Project Online und kann auch mit einer lokalen Project Server-Installation. 

Die Project Server-Datenbanken werden in eine einzelne Datenbank kombiniert. Sie können die online reporting Tabellen und Ansichten über einen OData-Dienst zugreifen. Das CSOM und des OData-Diensts enthalten eine Schnittstelle Representational State Transfer (REST). Project Server-Workflows können mithilfe von SharePoint Designer 2013 erstellt werden. Project Professional 2013 kann in Project Server-Daten, SharePoint-Aufgabenlisten und andere externe Inhalte mithilfe des Office-Add-ins Erweiterbarkeit-Modells für Aufgabenbereiche reporting integriert werden. Project Standard 2013 kann Task Pane-add-ins verwenden, um allgemeine externe Inhalte zu integrieren.
  
Diagramme und Weitere Informationen zu den wichtigsten Änderungen in Project Server 2013 finden Sie unter [Architektur von Project Server 2013](project-server-2013-architecture.md).
  
> [!NOTE]
> Projektserver 2013 basiert auf der Plattform für SharePoint Server 2013 und Project 2013 enthält einen Großteil der gleichen Infrastruktur als andere Office 2013-Anwendungen. Eine Dokumentation der einzelnen Details des Modells für SharePoint-Add-ins, SharePoint-basierten Workflows finden Sie unter Webparts, Entwicklung mit anderen SharePoint-Features und eine Dokumentation der Office-Add-ins, [Office und SharePoint-Add-ins](http://msdn.microsoft.com/library/fp161507%28office.15%29.aspx) und [SharePoint 2013-Entwicklung Übersicht über die](http://msdn.microsoft.com/library/jj164084%28office.15%29.aspx). 
  
## <a name="major-new-features-in-project-2013"></a>Wichtigsten neuen Features in Project 2013
<a name="pj15_WhatsNew_MajorNewFeatures"> </a>

Neue Features in Project Standard 2013 und Project Professional 2013 umfassen eine verbesserte Benutzeroberfläche, die andere Office 2013-Anwendungen entspricht und unterstützt die modernen Style-Benutzeroberfläche in Windows 8, Integration in Office Art-Objekte für Berichte, burndown Berichte und neue Programmierbarkeit Features für Berichte. Project Professional 2013 ermöglicht eine ausführlichere Freigabe und Synchronisierung von Projekten in SharePoint Server 2013, zusammen mit der Task Pane-add-ins, die auch in anderen Office 2013-Anwendungen wie Word, Excel und Outlook implementiert sind.
  
Es gibt viele neue Features in Project Server 2013. Einige verfügen nicht über die wichtigsten Programmierbarkeit Textabschnitt, wie die neuen Zeitachse in Project Web App. Diese Features werden in der Produktdokumentation Hilfe und Endbenutzer auf Microsoft Office Online und in den Themen in der Übergangsphase Administratoren und IT-Experten im Microsoft TechNet dokumentiert. Andere neuen Funktionen, beispielsweise verbesserte Arbeitszeittabellen erleichtern für Entwickler von Drittanbietern zur Interaktion mit Arbeitszeittabellen und statuserfassung über Project Server Interface (PSI).
  
Das Hinzufügen von Project Online und den Office Store (http://office.microsoft.com/store) für Projekt-add-ins weit reichende Änderungen sind, auf dem Project Server über Microsoft Azure zugänglich ist. Cloud-basierten Zugriff auf Project Server verwendet ein Client-seitigen Objektmodell (CSOM) für die Entwicklung von add-ins mit dem Microsoft .NET Framework, Microsoft Silverlight, Windows Phone und Web-apps, die JavaScript verwenden. Eine Anforderung von Project Online ist, dass die vier Project Server-Datenbanken aus früheren Versionen in einer einzigen Datenbank zusammengeführt werden.
  
Project Server 2013 Leistung und Skalierbarkeit wird in vielen Bereichen wie Vorgangsstatus, Arbeitszeittabellen und Projektmanagement verbessert. Project Server-Workflows werden mit 4-Version von Windows Workflow Foundation (WF4) neu gestaltet. Verwendung der .NET Framework 4 und Windows Communication Foundation (WCF) mit der PSI verbessert die Sicherheit, Leistung und Skalierbarkeit. Beispielsweise können Sie das Transportprotokoll der WCF-basierte Anwendungen ändern, mithilfe von Konfigurationsdateien, ohne den Code ändern oder neu zu kompilieren. Project Web App speichert viele der PSI-Aufrufe, in dem Daten nicht erheblich geändert wird.
  
> [!NOTE]
> Für die Entwicklung mit Project Server 2013 können Sie Visual Studio mit den Office und SharePoint-Tools-Erweiterungen, die systemintern-add-ins für Office 2013-Produkte erstellen können. Projektserver 2013 erfordert Visual Studio, um die Entwicklung von Features wie Projektdetailseiten und WCF-basierte Anwendungen vollständig zu aktivieren. Die SharePoint-Tools-Erweiterungen in Visual Studio können Webparts und anderen SharePoint-Features direkt in Project Web App und anderen SharePoint-Websites bereitstellen. 
>
> Visual Studio ist nicht mehr erforderlich, zum Entwickeln von Project Server-Workflows, mit denen benutzerdefinierte Felder, Phasen, Phasen und Enterprise-Projekttypen, die in Project Web App verwaltet werden können. Obwohl Sie Visual Studio zum Entwickeln von Workflows verwenden können, sind sie häufig leichter und schneller zu erstellen, indem Sie mithilfe von SharePoint Designer. Visual Studio kann für Workflows verwendet werden, die Zugriff auf das CSOM oder andere externe APIs erfordern. 
  
### <a name="project-add-ins"></a>Project-Add-ins
<a name="pj15_WhatsNew_Apps"> </a>

Vertrieb und Marketing Software hat wurde mit dem Konzept ein Add-in revolutioniert. Für Project 2013 können-add-ins für Erwerb und Download zur Verfügung gestellt, aus dem öffentlichen Office Store oder in einem privaten Katalog unter SharePoint verteilt werden. Ein Add-In wird in der Regel eine eigenständige, interaktive Programm, das eine kleine Anzahl von Aufgaben im Zusammenhang mit ausführt. Ein Projekt-Add-in kann ein Task Pane Add-in für die Project Standard 2013 oder Project Standard 2013-Clients oder ein Add-In für Project Server 2013 oder Project Online.
  
Informationen zu Add-Ins für die Project-desktop-Clients finden Sie unter [Task Pane-add-ins in Project](#pj15_WhatsNew_Agave). Ein Beispiel für Project Server 2013 finden Sie unter [Erstellen einer SharePoint gehosteten Project Server-add-in](create-a-sharepoint-hosted-project-server-add-in.md). Zusätzlich zu den Artikeln in [Office und SharePoint-Add-ins SDK](http://msdn.microsoft.com/library/fp161507.aspx)hat der [Office-Blog](https://blogs.office.com/dev/) viele Beiträge, die auch für Project 2013 und Project Online relevant sind. 
  
Ein Add-In für Project Server 2013 kann mit einer lokalen Installation und Project Online arbeiten. Project Server-add-ins kann Webparts, remote-Ereignisempfänger und Geschäftslogik enthalten. Zugriff auf das Objektmodell von Project Server in einem Add-in ist über die CSOM, nicht die PSI. Datenspeicher kann Cloud-basierten wie mit SQL Azure, wie beispielsweise über Microsoft Business Connectivity Services (BCS), interne mit einer lokalen Datenbank, externe oder gemischten sein.
  
#### <a name="add-in-security"></a>Add-in-Sicherheit

Im Allgemeinen sind Aktionen, die ein Add-in im Auftrag des Benutzers ausgeführt, die das Add-in ausgeführt wird. Sie verwenden nicht explizit Identitätswechsel oder angeben, die das Add-in ausgeführt werden kann. Aktionen darf die Berechtigungsstufe des Benutzers nicht überschreiten, die das Add-in ausgeführt wird. 
  
In den Office Developer Tools für Visual Studio 2012 hat die AppManifext.xml-Datei einen Grafiken-Editor, in dem Sie den berechtigungsanforderungsbereich festlegen. Wählen Sie zum Beispiel ein Add-in erstellen, Projektmanager ihre Projekte, auf der Registerkarte **Berechtigungen** des **AppManifest.xml** -Designer-Bereich aktualisieren ermöglicht, **Mehrere Projekte** für den Bereich und **Schreiben** für die Berechtigung. Wenn der Benutzer Add-In-Projekt-Manager-Berechtigungen verfügt, können sie das Add-in für Projekte ausführen, die er verwaltet. Der Code in der Datei AppManifest.XML würde Folgendes umfassen: 
  
```XML
  <AppPermissionRequests>
    <AppPermissionRequest Scope="http://sharepoint/projectserver/projects" Right="Write" />
  </AppPermissionRequests>
```

**In Tabelle 1. Berechtigungsanforderungsbereiche für Project Server-add-ins**

|Umfang|Berechtigungen|
|:-----|:-----|
|**Projektserver** <br/> |**Verwalten** (Erfordert Administratorberechtigungen für Project Server).  <br/> |
|**Mehrere Projekte** <br/> |**Lesen**, **Schreiben** (Project-Manager-Berechtigungen für einige Vorgänge; erfordert Team Members Berechtigungen in project finden Sie Basic Vorgänge, wie etwa vorgangszuordnungen.)  <br/> |
|**Einzelnes Projekt** <br/> |**Lesen**, **Schreiben** (unter erfordert mindestens Team Members Berechtigungen in project Abhängigkeit von Zugriff auf Daten in einem Projekt auf andere Berechtigungsstufen.)  <br/> |
|**Enterprise-Ressourcen** <br/> |**Lesen**, **Schreiben** (erfordert Berechtigungen für Ressourcen-Manager.)  <br/> |
|**Statuserfassung** <br/> |**SubmitStatus** (Erfordert die Berechtigung zum Status für Ihre Projekte zu übermitteln.)  <br/> |
|**Reporting** <br/> |**Lesen** (Erfordert die Berechtigung zur Anmeldung in Project Server).  <br/> |
|**Workflow** <br/> |**Zu erhöhen** (Erfordert die Berechtigung zur Ausführung von Workflows. Das Add-in ausgeführt wird mit erhöhten Berechtigungen, um Übergänge zwischen diesen Phasen berücksichtigt in einen Workflow zu aktivieren. Geschäftslogik in das Add-in steuert die Phasenübergänge.)  <br/> |
   
> [!NOTE]
> Projektserver 2013 und Project Online verwenden nicht im nur-app-Authentifizierungsmodell in SharePoint 2013 (siehe [-Add-in-autorisierungsrichtlinientypen in SharePoint 2013](http://msdn.microsoft.com/library/124879c7-a746-4c10-96a7-da76ad5327f0%28Office.15%29.aspx)). 
  
Informationen zum Entwickeln verteilen, hosten und Verwalten von Add-Ins, finden Sie unter [SharePoint-Add-ins](http://msdn.microsoft.com/library/cd1eda9e-8e54-4223-93a9-a6ea0d18df70%28Office.15%29.aspx) und [Office-Add-ins](http://msdn.microsoft.com/library/1e123201-6e70-45c1-a48c-d5b955896ddb%28Office.15%29.aspx)und Verwandte Themen in der Entwicklerdokumentation für SharePoint Server 2013 und Office 2013. Informationen zu berechtigungsanforderungsbereiche für andere SharePoint-add-ins finden Sie unter [-Add-in-Berechtigungen in SharePoint 2013](http://msdn.microsoft.com/library/5f7a8440-3c09-4cf8-83ec-c236bfa2d6c4%28Office.15%29.aspx).
  
### <a name="integrating-with-sharepoint-server"></a>Integrieren von SharePoint Server
<a name="pj15_WhatsNew_IntegrationWSS"> </a>

Viele Funktionen in Project Web App erfordern die neue Infrastruktur in SharePoint Server 2013 wie OAuth und anspruchsbasierte Authentifizierung, Autorisierung von Project Server und über die SharePoint-Gruppen, Berechtigungen Synchronisierung von Projekten mit den SharePoint-Aufgabe Listen und deklarative Workflows für Project Server. Die Project Service-Anwendung kann eine Websitesammlung in einer SharePoint-Farm zugeordnet werden. Project-Synchronisierung kann SharePoint verwaltet, in dem das Projekt mit einer SharePoint-Aufgabenliste. Enterprise-Projekt kann auch mit einer SharePoint-Aufgabenliste synchronisiert werden, auf dem Project Server Vollzugriff verwaltet. Architekturdiagramme und eine Erläuterung der Project-Synchronisierung finden Sie unter [Architektur von Project Server 2013](project-server-2013-architecture.md).
  
Es gibt viele neue Features in SharePoint Server 2013. Weitere Informationen finden Sie unter [SharePoint für Entwickler](http://msdn.microsoft.com/en-US/sharepoint).
  
### <a name="integrating-with-workflows"></a>Integrieren von workflows
<a name="pj15_WhatsNew_Workflow"> </a>

Workflows werden als zentrale Features von Project Portfoliomanagement. Projektlebenszyklus kann lange Prozesse enthalten, die viele Phasen umfassen. Governance Phasen gehören Projektvorschläge, Analysen geschäftliche Relevanz, auswählen, erstellen, planen, verwalten und Nachverfolgen von Projekten.
  
Project Server 2013-Workflows werden auf der SharePoint 2013-Workflow-Plattform integriert, die WF4 verwendet. Anders als in früheren Versionen deklarative Workflows für Project Server 2013 mithilfe von SharePoint Designer 2013 erstellt werden können und für lokale und Onlineverwendung zugänglich sind. Project Server-Workflows verwenden Sie das SharePoint-Workflow-Sicherheitsmodell mit OAuth und auf einer Project Web App-Website installiert werden können. Abbildung 1 zeigt, dass SharePoint Designer 2013 Phasen eines Website-Workflows für das Bedarfsmanagement, hinzugefügt werden können, auf dem die Phasen in Project Web App definiert sind.
  
**Abbildung 1. Verwenden SharePoint Designer zum Hinzufügen von einer Phase zu einem Workflow für Project Web App**

![Hinzufügen einer Stufe zu einem Workflow in SPD] (media/pj15_CreateWorkflowSPD_AddStageInSPD.gif "Hinzufügen einer Stufe zu einem Workflow in SPD")

<br/>

Erstellen Sie einen deklarativen Workflow durch Hinzufügen von Workflowstufen, Aktionen, Bedingungen und andere Elemente in einem Entwurfstool, die SharePoint Designer 2013 oder Visual Studio 2012 sein kann. Das Entwurfstool speichert dann den Workflow als XAML-Code, der zur Laufzeit interpretiert wird. Deklarative Workflows können in Project Server 2013 lokal oder in Project Online ausführen. Mithilfe von Visual Studio 2012, können Sie auch benutzerdefinierte Aktionen und Formularen für zusätzliche Kontrolle erstellen, und speichern Workflowvorlagen für die Wiederverwendung mit mehreren Project Web App-Instanzen. SharePoint Designer 2013 können benutzerdefinierte Aktionen nutzen, die in Visual Studio 2012 erstellt werden.
  
Ein Project Server 2013-Workflow fungiert als eine app, in denen ein Administrator – Entwurf Berechtigungen für Project Web App – kann einen deklarativen Workflow veröffentlichen und einen Enterprise-Projekttyp (EPT) zuzuordnen. Die EPT muss für Enterprise-Projekt sein, auf dem Project Server Vollzugriff verwaltet. SharePoint-Aufgabenliste kann nicht mithilfe eines Project Server-Workflows. 
  
OAuth kann Projektmanager, die über Berechtigungen, die den Workflow ohne Verwenden des Identitätswechsels aufgerufen werden. Workflow-Aufrufe an Project Server, beispielsweise zum Lesen Sie eines Werts des benutzerdefinierten Feldes, um zu entscheiden, welche zweigstellenbereitstellung, denen Sie folgen, werden im Namen der Projektmanager vorgenommen. Um zu verhindern, dass den Projektmanager Erstellen eines Workflows, das automatisch in die nächste Phase setzt, wird der Anruf zum Verschieben auf der nächsten Workflowstufe als workflowautor (Administrator) ausgeführt. Im Gegensatz dazu stellen Benutzern der Vorversion Project Server 2010-Workflows angenommener Anrufe über das Konto Workflow-Proxybenutzer, Administrator im Verlauf des gesamten Workflows zuzugreifen.
  
Obwohl Project Server 2013 lokal kompilierte WF3.5 basierenden Workflows verwenden können, wird empfohlen, legacy-Workflows auf deklarative Workflows basierend auf WF4 zu aktualisieren. Die neuere Technologie ist besser skalierbar und robuste. Geschäftsanalysten und PMO Mitarbeiter erstellen oder Aktualisieren von Workflow-Designs mithilfe von Visio 2013 und Project Server-Workflows ohne Code mithilfe von SharePoint Designer 2013 zu implementieren.
  
Informationen zum Erstellen eines deklarativen Workflows für Project Web App finden Sie unter [Erste Schritte bei der Entwicklung Project Server-Workflows](getting-started-developing-project-server-workflows.md). Einen Vergleich mit SharePoint Designer und Visual Studio-Funktionen für Workflows finden Sie unter [Develop SharePoint 2013-Workflows mit Visual Studio](http://msdn.microsoft.com/en-us/library/office/jj163199.aspx).
  
### <a name="client-side-object-model"></a>Clientseitiges Objektmodell
<a name="pj15_WhatsNew_CSOM"> </a>

Den programmgesteuerten Zugriff auf Project Online erfordert eine CSOM, die auf der SharePoint-CSOM basiert. Project Online-Authentifizierung werden mit OAuth mit einer Windows Live ID, nicht Project Server formularbasierte Authentifizierung oder Windows-Authentifizierung.
  
Es folgen die Prinzipien und dem CSOM in Project Server 2013-Features:
  
- Das CSOM dient zur Bedienung. Angenommen, Methoden und Eigenschaften direkt verwenden oder Bereitstellen von Daten nach Name, statt dass viele GUIDs, _ChangeXml_ -Parameter oder um Datasets übergeben. 
    
- Die Project Server-CSOM implementiert eine Teilmenge der PSI-Funktionen, basierend auf den am häufigsten verwendeten Anforderungen für Drittanbieter-Lösungen.
    
- Das CSOM intern Ruft die PSI, doch unterschiedlich angepasst ist. Beispielsweise Updates für alle Statusing-Änderungen über die **StatusAssignmentCollection.SubmitAllStatusUpdates** -Methode, durch die **Statusing.SubmitStatus** PSI-Methode für den Benutzer oder die **SubmitStatusForResource** -Methode nicht ausgeführt werden. für andere Ressourcen. 
    
- Das CSOM kann zugegriffen werden über einen WCF-Dienst (Client.svc), statt die Daten über die 22 öffentliche Webdienste von die PSI.
    
- Initialisierung des Project Server-CSOM ist direkt über die [ProjectContext](https://msdn.microsoft.com/library/Microsoft.ProjectServer.Client.ProjectContext.aspx) -Klasse, mit der Project Web App-URL nicht mithilfe einer WCF-Verweis oder der Proxy-Assembly. 
    
- Das CSOM implementiert mehrere Client-Bibliotheken und Schnittstellen, die von der internen SharePoint-CSOM-Infrastruktur unterstützt werden. Die Client-Bibliotheken und Schnittstellen umfassen Folgendes:
    
  - Microsoft .NET-Clientbibliothek in der Assembly Microsoft.ProjectServer.Client.dll
    
  - Silverlight-Bibliothek in der Assembly Microsoft.ProjectServer.Client.Silverlight.dll
    
  - Windows Phone 8-Bibliothek in der Assembly Microsoft.ProjectServer.Client.Phone.dll
    
  - JavaScript-Bibliothek für Webanwendungen in die PS.js oder PS.debug.js-Datei
    
  - REST-Endpunkte für den Zugriff mit dem OData-Protokoll
    
  - Systemeigene Unterstützung für LINQ-Abfragen mit dem Filter, um die Menge der Daten zu begrenzen, die zurückgegeben wird
    
- Das CSOM kann sowohl für Project Online Solutions und in lokalen Lösungen, unabhängig von der PSI und anderen Project Server-Assemblys wie Microsoft.Office.Project.Server.Library.dll verwendet werden.
    
- Zusätzliche Funktionalität von Project Server 2013-CSOM gilt für kumulative Updates und Servicepacks, basierend auf Anfragen von Project Server-Partnern und der Entwicklercommunity.
    
> [!NOTE]
> Das CSOM ist die bevorzugte Schnittstelle für Project Server-Entwickler von Drittanbietern. Es wird empfohlen, dass Sie das CSOM verwenden für die Entwicklung von neuen Anwendung, wenn das CSOM die Funktionen enthält, die die Anwendung erfordert. 
  
Informationen zum Entwickeln mit dem Clientobjektmodell finden Sie unter [Client-seitigen Objektmodell (CSOM) für Project 2013](client-side-object-model-csom-for-project-2013.md). Informationen über die REST-Schnittstelle in SharePoint-Anwendungen finden Sie unter *Programmierung mithilfe des SharePoint-REST-Diensts* in der SharePoint 2013-Entwicklerdokumentation. 
  
### <a name="changes-in-the-reporting-database"></a>Änderungen in der Berichtsdatenbank
<a name="pj15_WhatsNew_RDBChanges"> </a>

Die vier Datenbanken in Project Server 2010 werden in einer einzelnen Projektdatenbank in Project Server 2013 zusammengefasst. Der Standardname der Project-Datenbank ist ProjectService. Tabellen und Sichten behalten ihre vorherigen Namen und Tabellen und Sichten aus der Datenbanken Entwurf, veröffentlicht und Archivierung haben die Präfixe Reporting `draft`, `pub`, und `ver` in der Datenbank ProjectService. Beispielsweise ist die Tabelle veröffentlichte Projekte Pub. MSP_PROJECTS. 
  
> [!IMPORTANT]
> Direkter Zugriff wird nicht unterstützt, für den Entwurf (`draft` Präfix), veröffentlichte (`pub`), und die Archivdatenbank (`ver`) Tabellen und Ansichten. Nur die reporting Tabellen und Ansichten, in denen haben verwenden die `dbo` Präfix. Beispielsweise der Tabelle Dbo. MSP_EpmProject-Tabelle enthält die Liste der Projekte in der Project Web App-Instanz. 
>
> Es gibt nichts aktiv Sie verhindern, dass Datenbank direkt den programmgesteuerten Zugriff zum Aktualisieren von Daten in den Tabellen und Ansichten in der Project-Datenbank verwenden. Sie sollten beachten Sie, dass der Project Professional-Cache, der Tabellen für die Entwurfsdatenbank und die veröffentlichten Daten und reporting Tabellen, die alle auf ein Cache Synchronisierungsprotokoll verlassen, die durch unterbrochen werden können Bearbeitung von Daten direkte. Wenn Sie Ihrer Project Server-Datenbanken beschädigen oder Project Professional beschädigte zwischengespeichert mit direkter Zugriff zum Ändern von Daten, eine Warnung angezeigt, dass nicht Produktsupport dazu beitragen kann mithilfe der clientseitigen! 
  
Projektserver 2013 stellt einen OData-Dienst für online und lokalen Zugriff. Online reporting Tabellen und Sichten, werden nur die von der OData-Schnittstelle verfügbar gemacht. für die Verwendung von lokalen können Sie die OData-Schnittstelle verwenden oder direkt Zugriff auf die Berichte Tabellen und Ansichten in der Datenbank ProjectService in der SharePoint-Farm. Project Online wird eine mandantenfähigen Datenbank nicht unterstützt werden. Mehrere Instanzen von Project Web App jedes haben d. h., ihre eigenen Project-Datenbank. OData-Dienst intern SQL-Abfragen auf reporting Tabellen und Sichten ausgeführt wird, und bietet eine XML- oder JSON-Nutzlast. Eine Einführung in die OData-Dienst für die berichterstellung in Project Server 2013 und für den **ProjectData** -Schemareferenz (engl.) finden Sie unter [ProjectData - Projekt OData-Dienstverweises](https://msdn.microsoft.com/en-us/library/office/jj163015.aspx).
  
Allgemeine Informationen zu OData-Abfragen finden Sie unter [OData: URI Konventionen](http://www.odata.org/developers/protocols/uri-conventions#FilterSystemQueryOption). Beispielsweise können Sie alle Projekte in einer lokalen Instanz von Project Web App finden Sie unter der Namen des Projekts, in dem mit "Test" beginnt, mithilfe der folgenden Abfrage in einem Browser. Mit der rechten Maustaste auf der Browser, und klicken Sie dann auf **Quelle anzeigen**.
  
```html
http://ServerName /ProjectServerName /_api/ProjectData/Projects?$filter=startswith(ProjectName, 'Test') eq true
```

Zum Importieren von Project-Daten in PowerPivot in Excel 2013, auf dem Menüband Daten, wählen Sie im Dropdown-Menü **Aus anderen Quellen** **aus OData-Datenfeeds** aus. Geben Sie im Dialogfeld **Datenverbindungs-Assistenten** http://ServerName/ProjectServerName/_api/ProjectData/ in den Daten feed Speicherort, wählen Sie **Weiter,** und wählen Sie dann in den **Tabellen auswählen** -Seite des Assistenten die **Projects** -Tabelle aus. Benennen Sie und speichern Sie die ODC-Datei, und wählen Sie dann auf **Fertig stellen**. Wählen Sie im Dialogfeld **Daten importieren** **PivotTable-Bericht**aus. Wählen Sie die Felder für die Pivot-Tabellenzeilen und Spalten an, denen Sie anzeigen möchten, auf dem Excel-Arbeitsblatt.
  
Der lokale Project Server-Benutzer, die über die richtigen Berechtigungen verfügen, können direkt reporting Tabellen und Sichten über Microsoft SQL Server zum Erstellen von Berichten, zugreifen wie in Project Server 2010. In Project Server 2013 können Benutzer auch Zugriff auf das lokale reporting Tabellen über die OData-Schnittstelle. Sie können Project Server-Daten online oder lokalen über REST-Endpunkte für den OData-Dienst abrufen. Beispielsweise der Tabelle Dbo. MSP_PROJECT Tabelle und der Tabelle Dbo. MSP_EpmProject_UserView Ansicht kann für Berichte verwendet werden. Tabellen und Ansichten, die ein `draft`, `pub`, oder `ver` Präfix sind nur zur internen Verwendung von Project Server, und nicht für die berichterstellung verwenden. Beispielsweise ist der Entwurf. MSP_TASKS-Tabelle und die Pub. MSP_PROJECTS_WORKING_VIEW Ansicht nicht dokumentiert werden und werden nur zur internen Verwendung. 
  
> [!NOTE]
> Sie können lokale reporting durch Hinzufügen von Tabellen, Ansichten, Felder und gespeicherte Prozeduren in einer separaten Datenbank erweitern. Sie sollten die vorhandenen reporting Tabellen und Ansichten in der Project Server-Datenbank nicht ändern. 
  
Die Berichte Tabellen, Ansichten und Feldern in der Project-Datenbank werden in einer HTML-Hilfe-Datei in einem neueren Update des Project 2013-SDK-Downloads dokumentiert. Eine Dokumentation der OData-XML-Schema für den **ProjectData** -Dienst finden Sie unter [ProjectData - Projekt OData-Dienstverweises](https://msdn.microsoft.com/en-us/library/office/jj163015.aspx). Abfragen der reporting Tabellen und Ansichten, die für Project Server 2010 erstellt wurden, in den meisten Fällen mit der Project-Datenbank in Project Server 2013 funktioniert. Lokale Benutzer können die Project Server-OLAP-Cubes in SQL Server Analysis Services zugreifen, wie aktuell. OLAP-Cubes sind in Project Online nicht verfügbar.
  
### <a name="task-pane-add-ins-in-project"></a>Task Pane-add-ins in Project
<a name="pj15_WhatsNew_Agave"> </a>

Project Standard 2013 und Project Professional 2013 unterstützen Aufgabe Bereich-add-ins, die zum integrieren und anzeigen externer Inhalte auf einer Webseite verwendet werden können. Der Aufgabenbereich zeigt Webseiteninhalten, die über JavaScript auf Aufgaben, Ressourcen, Ansichten und allgemeine Project-Daten zugreifen. Das JavaScript-Objektmodell für Project kann Abrufen von Informationen über einen ausgewählten Vorgang oder eine Ressource, und kann Abrufen von Daten in einer ausgewählten Zelle im Raster für Ansichten wie das Gantt-Diagramm. Task Pane-add-ins für Project können auch implementieren die Ereignishandler für Vorgangs-, Ressourcen- oder SelectionChanged-Ereignisse anzeigen. 
  
Abbildung 2 zeigt die **Hallo ProjectData** Aufgabe Bereich add-Ins, die fragt des **ProjectData** -Diensts, und klicken Sie dann vergleicht die Daten im aktuellen Projekt mit die Durchschnittswerte für alle Projekte. Der Project 2013-SDK-Download enthält den vollständigen Quellcode für das Add-in. 
  
**Abbildung 2. Eine Aufgabe Bereich add-Ins in Project Professional kann die Daten in Project Server zugreifen.**

![Vergleichen des aktuellen Projekts mit allen Projekten] (media/pj15_RestQueryApp_CompareProject.gif "Vergleichen des aktuellen Projekts mit allen Projekten")
  
> [!NOTE]
> Project Standard 2013 kann nicht direkt in Project Server 2013 über Task Pane-add-ins integriert werden. 
  
Task Pane-add-ins in Project Professional kann Webparts unterstützen, die für Project Server 2013 integriert sind, so dass Entwickler eine Erweiterung erstellen können, nachdem mit Project Web App und Project Professional ausgeführt wird. Allgemeine Task Pane-add-ins, die für andere Office 2013-Produkte entwickelt werden kann auch mit Project Standard 2013 und Project Professional 2013 verwendet werden. Weitere Informationen finden Sie unter [Task Pane-add-ins für Project](task-pane-add-ins-for-project.md).
  
### <a name="project-server-event-receivers"></a>Project Server-Ereignisempfänger
<a name="pj15_WhatsNew_Events"> </a>

In einer SharePoint-Farm, die die Back-End-Project Service-Anwendung enthält, kann mehrere Project Web App-Server (auch als Front-End-Webserver oder WFEs bezeichnet) sein. Ereignisempfänger können auch Ereignishandler aufgerufen werden. Lokale Ereignishandler können mit voll vertrauenswürdiger Code implementiert und auf allen der WFEs für eine lokale Installation von Project Server bereitgestellt werden. Remote-Ereignisempfänger können in Webdiensten auf lokalen oder Remoteservern implementiert und von mehreren WFEs und mehrere Project Server-Installationen aufgerufen werden. Project Online kann nur remote-Ereignisempfänger verwenden.
  
Project Server-Ereignishandler werden von SharePoint für jede Project Web App-Instanz, statt die Daten von einer bestimmten Project Web App-Einstellungen-Seite verwaltet. Wählen Sie in der Anwendung der SharePoint-Zentraladministration **Allgemeine Anwendungseinstellungen**, wählen Sie **Verwalten** unter **Einstellungen für PWA**und wählen Sie dann die Instanz in der **Project Web App-Instanz** Dropdown-Liste auf der PWA-Einstellungen auf der Seite. Um eine lokale Ereignishandler oder einen remote-Ereignisempfänger hinzuzufügen, wählen Sie **Serverseitige Ereignishandler**.
  
Für eine lokale Installation von Project Server, können Sie einen remote-Ereignisempfänger als SharePoint-Feature, das die [Microsoft.ProjectServer.Client.EventHandlerCreationInformation](https://msdn.microsoft.com/library/Microsoft.ProjectServer.Client.EventHandlerCreationInformation.aspx) -Klasse verwendet, in dem Clientobjektmodell wird erstellen und anschließend programmgesteuert verwalten die Ereignisempfänger mithilfe der Methoden in der [EventHandlerCollection](https://msdn.microsoft.com/library/Microsoft.ProjectServer.Client.EventHandlerCollection.aspx) -Klasse. Für remote-Ereignisempfänger, Pre-Ereignisse sind synchrone, nach der Ereignisse sind asynchron und es ist ein Timeout für Fälle, in dem der remote-Ereignisempfänger nicht zurückgegeben wird. 
  
> [!NOTE]
> SharePoint-Zentraladministration wird nur für lokale Installationen zur Verfügung. Für Project Online und SharePoint Online können Sie hinzufügen oder Entfernen von remote-Ereignisempfänger mithilfe eines CSOM-basierte app-Pakets. 
  
Auf der Seite serverseitige Ereignishandler ist der Prozess zum Hinzufügen eines lokalen-ereignishandlers für eine lokale Project Server-Installation nahezu identisch mit dem für Project Server in das [Erstellen eines Project Server-ereignishandlers und Protokollieren eines Ereignisses](http://msdn.microsoft.com/en-us/library/gg615466.aspx) Thema beschriebenen Prozess 2010. Der Unterschied besteht darin, dass die Seite neuer Ereignishandler zusätzliche Optionen verfügt. Angenommen, wählen Sie in der Liste **Ereignisse** **Projekt zu erstellen** , und wählen Sie dann auf **Neuer EREIGNISHANDLER**. Auf der Seite Neues Ereignis-Handler erforderlichen nur zwei Felder werden **Name** und **Reihenfolge** (siehe Abbildung 3). Wenn Sie einen lokalen voll vertrauenswürdige-Ereignishandler hinzufügen, fügen Sie das Feld **Assembly-Name** und das Feld **Klassenname** ; Lassen Sie **Endpunkt-Url** leer. Wenn Sie einen remote-Ereignisempfänger hinzufügen möchten, fügen Sie **Endpunkt-Url**, und lassen Sie **Assemblynamen** und den **Namen der Klasse** leer. 
  
> [!CAUTION]
> Wenn Sie *sowohl* den Namen der Assembly-Name-Klasse und die Endpunkt-URL angeben, Project Server ruft nur die lokale (lokal)-Ereignishandler. Der remote-Ereignisempfänger wird ignoriert. 
> 
> Wenn Sie zwei Ereignishandler für das gleiche-Ereignis erstellen, in dem ein Ereignishandler ist lokal und einer ist eine remote-Ereignisempfänger und der **Order** -Wert wird sowohl für, wird von Project Server den remote-Ereignisempfänger ignoriert. 
  
**Abbildung 3. Eine lokale Ereignishandler oder einen remote-Ereignisempfänger hinzufügen**

![Konfigurieren eines ereignishandlers oder Ereignisempfängers] (media/pj15_EventHandlers_NewEventHandler.gif "Konfigurieren eines ereignishandlers oder Ereignisempfängers")
    
Wenn Sie Zugriff auf die PSI Datasets für eine lokale Ereignishandler benötigen, können Sie kopieren Sie die Assembly Microsoft.Office.Project.Schema.dll, aus der [Windows]\Microsoft.NET\assembly\GAC\_MSIL\Microsoft.Office.Project.Schema\v4.0_15.0.0.0__ 71e9bce111e9429c Verzeichnis. 

Anstelle der PSI wird empfohlen, dass Sie die Ereignisklassen im **Microsoft.ProjectServer.Client** -Namespace verwenden; Entwicklung mit dem Clientobjektmodell erforderlich keine Bearbeitung des Datasets. Informationen zum Entwickeln von remote-Ereignisempfänger für Project Online, müssen Sie die [Event](https://msdn.microsoft.com/library/Microsoft.ProjectServer.Client.Event.aspx) -Klasse und die [EventHandlerCreationInformation](https://msdn.microsoft.com/library/Microsoft.ProjectServer.Client.EventHandlerCreationInformation.aspx) -Klasse in der CSOM verwenden. 
  
Bevor Sie einen Project Server-Ereignishandler bereitstellen, installieren und Testen des ereignishandlers sorgfältig auf einer Testinstallation von Project Server. Für eine lokale Project Server-Installation Wenn der lokale Ereignishandler, den Sie hinzufügen nicht funktionsfähigen, wird wird nicht der Project Server 2013-Ereignisdienst der anderen gültigen benutzerdefinierte Ereignishandler geladen. In diesem Fall müssen Sie den Ereignishandler Problem entfernen und erneutes Starten des Diensts Ereignisse.
  
> [!NOTE]
> Für eine lokale Project Server-Installation wird empfohlen, dass Sie die Migration zu remote-Ereignisempfänger mit dem Clientobjektmodell zur Entwicklung von Ereignisempfängern an. Da remote-Ereignisempfänger nicht Drittanbieter-Code, der in der Project Server-Ereignisdienst ausgeführt haben, sind die remote-Ereignisempfänger stabiler. Lokale Administratoren sind erlassene der Zuständigkeit für die Verwaltung der Project Server-Ereignisdienst. 
  
Allgemeine Informationen zu Ereignissen finden Sie unter [Behandeln von Ereignissen in apps für SharePoint](http://msdn.microsoft.com/en-us/library/jj220048%28office.15%29.aspx). 
  
## <a name="deprecated-features"></a>Veraltete features
<a name="pj15_WhatsNew_Deprecated"> </a>

> [!NOTE]
> Informationen zu Features und APIs, die als veraltet gekennzeichnet oder in Project Server 2016 Preview entfernt werden, finden Sie unter [Was als veraltet gekennzeichnet oder in Project Server 2016 Preview entfernt wurde](https://technet.microsoft.com/library/mt422816%28v=office.16%29.aspx). 
  
Veraltete Features in Project 2013 für einige Lösungen weiterhin verfügbar sind, aber sollte nicht für die Entwicklung neuer verwendet werden. Die meisten der folgenden Methoden und Features funktionieren nicht mit Project Online oder mit der standardmäßigen lokalen Installation von Project Server 2013 in SharePoint-Berechtigungsmodus. Vorhandene Lösungen, die diese Features verwenden, funktionieren möglicherweise nicht für ein Upgrade von Project Server 2010 auf Project Server 2013. Jedoch veraltet Lösungen, mit denen Features können weiterhin in einigen Fällen arbeiten, sie werden nicht vollständig für alle Project 2013-Installationen unterstützt.
  
Wenn Ihre Lösungen veralteten Features verwenden, sie sollten vor der Bereitstellung sorgfältig getestet werden, und Sie sollten ändern sie auf Features verwenden, die unterstützt, sobald praktische unverändert. Informationen zum Konfigurieren von lokalen Project Server 2013-Sicherheit für Project-Berechtigungsmodus finden Sie im Abschnitt *SharePoint-Berechtigungsmodus* in [What's new for IT-Spezialisten in Project Server 2013](http://technet.microsoft.com/en-us/library/ff631142%28office.15%29.aspx).
  
- **Erweiterungen** [PSI-Erweiterung Szenarien](https://msdn.microsoft.com/library/office/ff843378%28v=office.14%29.aspx) sind veraltet und wird in zukünftigen Versionen nicht unterstützt. Diese Szenarien des lokalen Project Server 2013 aktiviert Integration mithilfe von benutzerdefinierten Windows Communication Foundation (WCF) Dienste. 
  
- **Project-PSI** Die [Project-Klasse](https://msdn.microsoft.com/library/office/websvcproject.project_di_pj14mref.aspx%28Office.15%29.aspx) von der PSI ist veraltet. Verwenden Sie für alle Neuentwicklungen des [Project-CSOM](https://msdn.microsoft.com/library/office/microsoft.projectserver.client_di_pj14mref.aspx%28Office.15%29.aspx). Project Server 2013-apps, die die Project-PSI zu verwenden sind weiterhin funktionsfähig, aber Project Online apps müssen alle Projektklasse PSI-Methoden mit ihren entsprechenden CSOM-Methoden zu ersetzen.
  
- **Ressourcenplan-PSI** Die [Ressource planen PSI](https://msdn.microsoft.com/library/office/websvcresourceplan_di_pj14mref.aspx) ist veraltet. Es werden weiterhin für die Entwicklung für Project 2013 unterstützt werden, jedoch wird in zukünftigen Versionen nicht unterstützt. 
  
- **ASMX-Schnittstelle für die PSI** Die PSI enthält doppelte Schnittstellen für die Entwicklung von lokalen Project Server Extensions. Die ASMX-Dienste Weboberfläche wurde mit der ersten Implementierung von die PSI in Office Project Server 2007 eingeführt. Projektserver 2010 hinzugefügt, die WCF-Dienste-Schnittstelle, in dem das Objektmodell der ASMX-Webdienste im Wesentlichen dupliziert. Obwohl Project Server 2013 ASMX- und WCF unterstützt weiterhin, sollten neue Lösungen, die die PSI erfordern die WCF-Dienste verwenden. Wenn möglich, sollten neue Lösungen mit dem Clientobjektmodell geschrieben werden. 
  
  Die ASMX-Webdienste auf die PSI sind in Project Server 2013 veraltet. Um in zukünftigen Versionen von Project Server zu arbeiten, müssen Lösungen, die die ASMX-Webdienste umgeschrieben werden, um die WCF-Dienste oder das CSOM verwenden. Weitere Informationen finden Sie im Abschnitt *Aktualisieren von Clientanwendungen mit den Project Server-APIs* in [Project Server-Programmierbarkeit](project-server-programmability.md).
  
- **Object Link Provider (OLP)** In früheren Versionen von Project Server bietet (siehe [WebSvcObjectLinkProvider](https://msdn.microsoft.com/library/WebSvcObjectLinkProvider.aspx) ) der **ObjectLinkProvider** -Dienst in die PSI eine Möglichkeit zum Verwalten von Web-objektverknüpfungen zwischen Projektvorgängen Enterprise und spezielle SharePoint-Listen in der Projektwebsite für Probleme, Risiken, Lieferumfang und Dokumenten. In Project Server 2013 ist OLP veraltet. 
  
  Sie können mithilfe der **[RelatedItemManager](http://msdn.microsoft.com/en-us/library/microsoft.sharepoint.client.relateditemmanager.aspx)** -Klasse in der SharePoint-CSOM zum Erstellen, lesen, und Web-Objekt Links zwischen Elementen in der Aufgabenliste und andere Listen in eine Projektwebsite löschen. Um einen Link aus ein Aufgabenelement ein Problem hinzugefügt haben, können Sie beispielsweise die **[AddSingleLink](http://msdn.microsoft.com/en-us/library/office/microsoft.sharepoint.client.relateditemmanager.addsinglelink.aspx)** -Methode oder einer der beiden ähnliche Methoden **AddSingleLinkFromUrl** oder **AddSingleLinkToUrl**verwenden. Die **RelatedItemManager** -Klasse enthält auch Methoden zum Löschen einer webobjektverknüpfung und verwandte Elemente lesen. Die entsprechende Klasse in der JSOM (JavaScript-Objektmodell) finden Sie unter [SP. RelatedItemManager Object (sp.js)](http://msdn.microsoft.com/en-us/library/jj838582.aspx).
  
  Es wird empfohlen, für die Verwendung des SharePoint-CSOM zum Erstellen von OLP-Typ apps für eine lokale Installation von Project Server 2013 und Project Online. Der [Microsoft.SharePoint](http://msdn.microsoft.com/en-us/library/microsoft.sharepoint.aspx) -Namespace enthält keine **RelatedItemManager** *** Klasse. 
  
- **Benutzerdefinierte Berechtigungen** Benutzerdefinierte Sicherheitsberechtigungen für den Zugriff auf bestimmte Features von Project Server oder Erweiterungen wurden in Office Project Server 2007 unterstützt, in dem ein SDK-Artikel erläutert wird, deren Erstellung die veröffentlichten Datenbank direkt geändert. In Project Server 2010 benutzerdefinierte Berechtigungen weiterhin funktionieren jedoch veraltet sind. In Project Server 2013 funktionieren benutzerdefinierte Berechtigungen nicht mit der standardmäßigen SharePoint-Berechtigungsmodus für lokale Installationen. Benutzerdefinierte Berechtigungen werden für den Berechtigungsmodus Project unterstützt. Mit Project Online ist direkten Datenbankzugriff nicht möglich. 
  
- **Identitätswechsel** Identitätswechsel in PSI-basierten apps ist, in dem der Benutzer einer App die Sicherheitsberechtigungen von einem anderen Project Server-Benutzer übernehmen kann in Project Server 2013 veraltet. Wie zuvor angegeben in der lokalen einer standardmäßiges Project Server 2013-Installation SharePoint-Berechtigungsmodus verwendet, der kein Identitätswechsel in der Project Server-Sicherheitsgruppen erlaubt. Weitere Informationen finden Sie unter [Authentifizierung, Autorisierung und Sicherheit in SharePoint 2013](http://msdn.microsoft.com/en-us/library/ms457529%28office.15%29.aspx).
  
  Statusing sind typische Erweiterungen, die in früheren Versionen von Project Server möglicherweise Identitätswechsel verwendet haben. Projektserver 2010 eingeführt, die **ReadStatusForResource** -Methode und der **SubmitStatusForResource** -Methode in die PSI, zusammen mit der **StatusBrokerPermission** globale Berechtigung für die Notwendigkeit für den Identitätswechsel zum Lesen von eliminiert und Aktualisieren des Status im Auftrag eines anderen Benutzers. Das CSOM in Project Server 2013 verwendet, die zugrunde liegenden PSI um transparent Zeitberichte Extensions aktivieren, und für Project Online oder lokale-Installationen verwendet werden kann. 
  
- **Datenbank-Erweiterungen Reporting** Hinzufügen von benutzerdefinierten Tabellen und Ansichten auf die Berichtsdatenbank ist üblich mit früheren Versionen von Project Server. Da Project Server 2013 früherer Versionen die vier Datenbanken in einer einzigen Datenbank kombiniert werden, werden Upgrades nicht benutzerdefinierte Tabellen, Sichten oder Routeninformationen an den reporting Tabellen in der Project Server 2013-Datenbank übertragen. 
  
  Es wird empfohlen, dass Sie verwenden SQL Azure oder einer separaten SQL Server-Datenbank für benutzerdefinierte Berichte Tabellen und Sichten, in dem Sie datenbanksicherungen und Updates verwalten. Dies ist für Project Online erforderlich.
  
- **Reporting** Lokale reporting Tabellen und Sichten in der Project Server-Datenbank und der OLAP-Cubes werden *nicht* als veraltet markiert, und bleiben vollständig unterstützt. Die Berichte Tabellen und Ansichten (die Berichtsdatenbank in früheren Versionen von Project Server) sind jedoch nicht in Project Online zugegriffen werden. OLAP-Cubes werden auf ähnliche Weise nur für lokale Installationen von Project Server 2013 verfügbar. Für Anwendungen mit Project Online-Berichte, können Sie den **ProjectData** -Dienst über die REST-Abfragen mit dem OData-Protokoll verwenden. 
  
- **Leitfaden für Project** Der Projektberater ist ein standard-Feature in Office Project 2007-desktopanwendungen, in dem enthält HTML- und JavaScript-Inhalten in einem Aufgabenbereich interaktive Anleitungen für das Erstellen und Verwalten von Projekten. In Project 2010 der Projektberater ist in einer Standardinstallation nicht verfügbar, aber über VBA oder eines VSTO-add-Ins aktiviert werden kann. Der Project 2010 SDK-Download enthält die geänderten Projektberater-Dateien. 
  
  Das Objektmodell für VBA und das **Microsoft.Office.Interop.MSProject** -Objektmodell in Project 2013 umfassen weiterhin 22 Member der Klasse **Application** und der **Project** -Klasse, die im Projektberater verwalten können. Jedoch werden Project 2013 Aufgabenbereich-apps in Konflikt mit Aktionen in einem Aufgabenbereich Projektberater und Projektberater Inhalt können nicht auf einfache Weise verteilten oder im Office Store verkauft. Es wird dringend empfohlen, Project Aufgabe Bereich Lösungen mit Office-Add-ins nicht benutzerdefinierten Projektberater Inhalt zu entwickeln. Weitere Informationen zu den Projektberater finden Sie in der [Project 2010 SDK-Dokumentation](http://msdn.microsoft.com/en-us/library/ms512767.aspx).
  
## <a name="comparing-project-server-on-premises-with-project-online"></a>Vergleichen von Projektserver zur lokalen Verwendung mit Project Online
<a name="pj15_WhatsNew_Comparing"> </a>

Um besser entscheiden, ob Sie Project Server lokale oder Project Online verwenden, und welche Arten von Erweiterungen in beiden Fällen entwickeln können, werden in Tabelle 2 die extensible Features einer lokalen Installation von Project Server 2013 mit Project Online verglichen. In Tabelle 2 sind die Unterschiede in der Bereitstellung, Verwaltung oder Usage nicht enthalten. Weitere Informationen zu Project Online und Project Server 2013 finden Sie unter [Project 2013 für Entwickler](http://msdn.microsoft.com/en-US/office/fp161502) und [Project Online](http://www.microsoft.com/project/).
  
**In Tabelle 2. Erweiterbarkeit von Projektserver: lokal und Project Online**

| Feature |Projektserver lokal | Project Online |
|:-----|:-----|:-----|
|**Programmierbarkeit** <br/> |CSOM-basierter apps; konsistente Programmiermodell  <br/>-.NET, Silverlight, Windows Phone-Client-Bibliotheken  <br/>-JavaScript Bibliothek für benutzerdefinierte Seiten, Webparts und menübanderweiterungen  <br/>-OData und REST-Protokolle<br/><br/> PSI-basierten apps; komplexe Programmiermodell sowie können auch Erstellen von apps für die Administration, Portfolioanalyse, Benachrichtigungen, Project-Sicherheitsmodus, Warteschlangensystem und andere Bereiche<br/><br/>PSI-Erweiterungen  <br/><br/>Benutzerdefinierte Berechtigungen mit Project-Sicherheitsmodus (veraltet)  <br/><br/>Identitätswechsel mit der PSI (veraltet)  <br/><br/>Voll vertrauenswürdiger Code; Installieren von Erweiterungen in SharePoint-farm  <br/> |CSOM-basierter apps; konsistente Programmiermodell  <br/>-.NET, Silverlight, Windows Phone-Client-Bibliotheken<br/>-JavaScript Bibliothek für benutzerdefinierte Seiten, Webparts und menübanderweiterungen<br/>-OData und REST-Protokolle<br/><br/>Die PSI verwenden können, jedoch nicht unterstützt: keine OAuth und keine Verbindungen Dienst<br/><br/>Keine Erweiterungen der CSOM-API<br/><br/>Keine benutzerdefinierten Berechtigungen<br/><br/>Kein Identitätswechsel<br/><br/>Keine voll vertrauenswürdiger code  <br/> |
|**Benutzerdefinierte Datenbanken** <br/> |-SQL Azure  <br/>-SQL Server (Änderung der reporting Tabellen und Ansichten in der Project Server-Datenbank nicht unterstützt wird)  <br/> |-SQL Azure  <br/>-SQL Server (Änderung der reporting Tabellen und Ansichten in der Project Server-Datenbank nicht unterstützt wird)  <br/> |
|**Reporting** <br/> |- **ProjectData** -Dienst OData und REST-Protokolle  <br/>-Reporting Tabellen und Ansichten in der Project Server-Datenbank<br/>-OLAP Datenbank  <br/> |- **ProjectData** -Dienst OData und REST-Protokolle  <br/> |
|**Ereignishandler** <br/> |-Remote-Ereignisempfänger, zugänglich über WCF-Endpunkten<br/>-Full-Trust-Ereignishandler in SharePoint-Farm installiert  <br/> | -Remote-Ereignisempfänger, zugänglich über WCF-Endpunkten  <br/> |
|**Workflows** <br/> |Deklarative Workflows mit SharePoint Designer 2013 erstellt wurden<br/>-Verwenden Sie nur auf einer bestimmten Project Web App-Instanz<br/>-Einen Workflowentwurf für können aus Visio 2013 importiert werden.<br/>-Importieren und Verwenden von benutzerdefinierten Aktionen können<br/><br/> Deklarative Workflows mit Visual Studio 2012 erstellt wurden<br/>-Erstellen Sie eine app, die Workflows enthalten kann<br/>-Erstellen Sie ein SharePoint-Lösungspaket (WSP-Datei), die Workflows enthalten kann<br/>-Erstellen von Workflow-Vorlagen für die Wiederverwendung<br/>-Erstellen und Verwenden von benutzerdefinierten Aktionen  <br/><br/>Können legacy kompilierte, erstellte Workflows mit WF3.5 (Upgrade auf deklarative WF4 Workflow empfohlen)  <br/> |Deklarative Workflows mit SharePoint Designer 2013 erstellt wurden<br/>-Verwenden Sie nur auf einer bestimmten Project Web App-Instanz<br/>-Einen Workflowentwurf für können aus Visio 2013 importiert werden.<br/>-Importieren und Verwenden von benutzerdefinierten Aktionen können  <br/><br/>Deklarative Workflows mit Visual Studio 2012 erstellt wurden<br/>-Erstellen Sie eine app, die Workflows enthalten kann  <br/>-Erstellen Sie ein SharePoint-Lösungspaket (WSP-Datei), die Workflows enthalten kann<br/>-Erstellen von Workflow-Vorlagen für die Wiederverwendung <br/>-Erstellen und Verwenden von benutzerdefinierten Aktionen  <br/> |
|**Verteilung** <br/> |-Office Shop (für CSOM-basierter apps)<br/>-Privaten app-Katalog in SharePoint<br/>-Intranet Dateifreigabe  <br/> |-Office Shop<br/>-Privaten app-Katalog in SharePoint  <br/> |

   
## <a name="conclusion"></a>Schlussbemerkung
<a name="pj15_WhatsNew_Conclusion"> </a>

Projektserver 2013 bietet eine Vielzahl von neuen Entwicklungsfunktionen und Szenarios, in denen Geschäftspartnern und Kunden können Sie anpassen und erweitern die Funktionalität und die Nützlichkeit von Project Server in großen Unternehmen und kleine Unternehmen. Sie können die Infrastruktur für Office 2013 und SharePoint 2013 zum Erstellen und Verteilen von apps für Project 2013, die deutlich die Marktwert und Verwendung von benutzerdefinierten Anwendungen erweitern können. Einige Features für die Erweiterbarkeit und-Verwendung von früheren Versionen sind veraltet in Project 2013, insbesondere die ASMX-Webdienste PSI und Features, die betreffen Identitätswechsel oder Datenbank direkt Änderungen, die mit Project Online verwendet werden kann.
  
Die Einführung der CSOM ermöglicht den programmgesteuerten Zugriff auf Project Online für eine Vielzahl von Geräten und mithilfe von JavaScript in Webanwendungen. Das CSOM bietet ein konsistentes Programmiermodell im Vergleich zu den PSI. Project Server-Daten können auf viele weitere Weise als in früheren Versionen, einschließlich über den OData-Onlinedienst und über die REST-Endpunkte für Berichtsdaten in der Project-Datenbank zugegriffen werden. Vorhandene Berichte funktionieren weiterhin auf die gleiche Weise für die lokale Verwendung; neue Berichte haben mehr Flexibilität.
  
Office-Add-ins bieten eine neue öffnet Verkauf Solutions und Integrieren von Project Standard 2013 mit Web-Inhalt und andere Office 2013-Produkte. Sie können auch neue Möglichkeiten zum Integrieren von Project Professional 2013 mit Project Server-Daten erstellen, und SharePoint-Listen durch Aufgabenbereich Office-Add-ins.
  
Weitere Informationen zum Entwickeln von apps, und verwenden die Programmierbarkeit Features und CSOM von SharePoint Server 2013 finden Sie unter [SharePoint für Entwickler](http://msdn.microsoft.com/en-US/sharepoint) und [Office für Entwickler](http://msdn.microsoft.com/en-US/office).
  
## <a name="see-also"></a>Siehe auch

- [Project Server 2013-Architektur](project-server-2013-architecture.md)  
- [Project-Programmieraufgaben](project-programming-tasks.md) 
- [Clientseitiges Objektmodell (CSOM) für Project 2013](client-side-object-model-csom-for-project-2013.md) 
- [ProjectData – OData-Dienstreferenz für Project](https://msdn.microsoft.com/en-us/library/office/jj163015.aspx)  
- [Aufgabenbereich-Add-Ins für Project](task-pane-add-ins-for-project.md)   
- [OData: URI-Konventionen](http://www.odata.org/documentation/uri-conventions#FilterSystemQueryOption)    
- [SharePoint für Entwickler](http://msdn.microsoft.com/en-US/sharepoint)    
- [Office für Entwickler](http://msdn.microsoft.com/en-US/office)   
- [Behandeln von Ereignissen in apps für SharePoint](http://msdn.microsoft.com/en-us/library/jj220048%28office.15%29.aspx)   
- [Office Store](http://office.microsoft.com/en-us/store/)   
- [Project Online](http://www.microsoft.com/project/)
    

