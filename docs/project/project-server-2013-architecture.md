---
title: Project Server-Architektur
manager: soliver
ms.date: 09/17/2015
ms.audience: Developer
localization_priority: Normal
ms.assetid: 2cfa5a6e-2f5c-440c-b35a-bc7a34648f9c
description: Projektserver 2013 integriert Projektmanagement-Funktionen in einer SharePoint-Farm und ermöglicht die Verwendung von Project Online mit einer Client-seitigen Objektmodell (CSOM) und einem OData-Interface für Berichtsdaten.
ms.openlocfilehash: 992fae3790b8bdb6ab55f41d42ef0229a75e255c
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19796318"
---
# <a name="project-server-architecture"></a>Project Server-Architektur

Projektserver 2013 integriert Projektmanagement-Funktionen in einer SharePoint-Farm und ermöglicht die Verwendung von Project Online mit einer Client-seitigen Objektmodell (CSOM) und einem OData-Interface für Berichtsdaten.
   
Projektserver 2013 ist eine mehrstufige System, das die Architektur in Office Project Server 2007 eingeführt wurde erweitert. Architektonische Änderungen enthalten Zuordnung des Project-Anwendungsdiensts mit SharePoint-Websitesammlungen, die Hinzufügung von einigen von Geschäftsobjekten auf dem Front-End-Web (WFE), Client-seitigen Objektmodell (CSOM) für den Remotezugriff, eine einzelne Projektdatenbank ein OData-Interface für Reporting Tabellen und Ansichten, Integration von Windows Workflow Foundation Version 4 (WF4) bis Workflow-Manager-Client 1.0 in der Cloud oder auf einem lokalen Server und remote-Ereignisempfänger, die von mehreren Project Server zugänglich sind Installationen. Zusätzlich zur lokalen benutzerdefinierten Lösungen können Sie apps erstellen, die remote-Ereignisempfänger und Komponenten, die die CSOM und OData-Schnittstelle zugreifen.
  
Die Front-End-Ebene umfasst Project Professional 2013, Project Web App und Drittanbieter-apps. Clientanwendungen kommunizieren mit der mittleren Ebene über Project Server Interface (PSI) oder über die CSOM-Endpunkte, die wiederum mit den PSI und die geschäftsobjektschicht kommunizieren. Zugriff auf die Datenbank wird in den Geschäftsobjekten integriert. Die Project Server-Ereignisdienst-System können lokale Ereignishandler und remote-Ereignisempfänger zugreifen. Project-Berechnungen implementiert Planungsmodul Project Professional in Project Server. Clientanwendungen nicht (oder nicht) direkt die Project-Datenbank zugreifen; Projektserver Blendet Geschäftsobjekte von Clients.
  
> [!NOTE]
> Projektserver basiert auf der SharePoint-Architektur. Informationen zu SharePoint Server 2013-Architektur und das SharePoint-app-Modell finden Sie im Abschnitt *Erste Schritte mit SharePoint-Entwicklung* in der Dokumentation zur Office 2013-Entwickler. 

<a name="pj15_Architecture_SharePoint"> </a>

## <a name="integrating-with-sharepoint-site-collections"></a>Integration in SharePoint-Websitesammlungen

Project-Anwendungsdienst in Project Server 2013 können einer SharePoint-Websitesammlung für die Verwendung mit SharePoint-Aufgabenlisten zugeordnet werden, die Project-Anwendungsdienst können auch eine SharePoint-Aufgabenliste als Enterprise-Projekt importieren, für vollständige Project Server Steuerelement. Mit einer SharePoint-Vorgangsliste verwaltet SharePoint die Projektwebsite in einer Websitesammlung. Project Professional kann mit synchronisieren und aktualisieren die Aufgabenliste. Eine Projektwebsite kann sein, eine unabhängige SharePoint-Aufgabenliste oder eine Liste der Aufgaben, die mit einer MPP-Datei synchronisiert wird. MPP-Datei kann lokal oder in einer SharePoint-Bibliothek gespeichert werden. 
  
Projektserver verwaltet die Projekte, wenn er über Vollzugriff verfügt. Project Professional speichert die Daten direkt in Project Server. In Tabelle 1 wird das Verhalten von einer Vorgangsliste, den Zeitplan-Webpart und andere Funktionen für SharePoint-Steuerelement mit den Aufgabenlisten und importierten Projekte verglichen, wenn Project Server über Vollzugriff verfügt. Das Zeitplan-Webpart enthält das Raster auf der Project Web App-Seite, in dem Sie einen Projektplan bearbeiten können. Der verknüpften Modus ist, Statusing-Daten einmal für Vorgänge und Arbeitszeittabellen eingegeben werden. in den einfachen Eingabemodus werden Zeitberichte Vorgangsdaten separat aus Arbeitszeittabellen eingegeben.
  
**Tabelle 1. Vergleich von SharePoint-Aufgabenlisten und Vollzugriff**

| Feature | Aufgabenliste | Vollzugriff |
|:-----|:-----|:-----|
|**Aufgabenliste in SharePoint** <br/> |Lese-/Schreibzugriff  <br/> |Schreibgeschützt  <br/> |
|**Zeitplan-Webpart** <br/> |Schreibgeschützt  <br/> |Lese-/Schreibzugriff  <br/> |
|**Reporting** <br/> |Umfassende Berichterstellung über Project Server  <br/> |Umfassende Berichterstellung über Project Server  <br/> |
|**Sonstige Project Server-Funktionen** <br/> | Gesperrte Funktionen:  <br/>-Serverseitige projektbearbeitungen, mit Project Web App oder benutzerdefinierten-Clientanwendungen  <br/>-Statusing  <br/>-Aufgaben werden nicht im verknüpften Modus angezeigt  <br/> |Es besteht Vollzugriff  <br/> |
   
### <a name="managing-projects-as-sharepoint-task-lists"></a>Verwalten von Projekten als SharePoint-Aufgabenlisten
<a name="pj15_Architecture_VisibilityMode"> </a>

Project Server ist beim zugeordnet, mit einer SharePoint-Websitesammlung, in dem SharePoint verwaltet, Aufgabenlisten und Project Professional 2013 (MPP) Dateien in Dokumentbibliotheken für die Project-Anwendungsdienst sichtbar sind, SharePoint, behält jedoch, die Master-Daten für die Synchronisierung (siehe Abbildung 1). Serverseitige Planung mit dem Zeitplan-Webpart kann nicht erfolgen. Sie können Project Professional mit synchronisieren und Bearbeiten der Aufgabenliste in einer Projektwebsite verwenden. Beginnen Sie mit SharePoint-Aufgabenlisten, können Organisationen schrittweise weiterentwickelt, um den vollen Funktionsumfang von Project Server verwenden.
  
In Abbildung 1 sind die folgenden Prozesse für das Verwalten von Projekten in SharePoint-Aufgabenlisten dargestellt: 
  
- (A) Project Professional kann mit Aufgabenlisten synchronisiert werden und neue Projektwebsites in der Websitesammlung erstellen, bevor oder nachdem eine Verknüpfung mit dem Project-Anwendungsdienst hergestellt wurde.
    
- (B) Project Server wird zu Berichtzwecken mit Projektwebsitedaten synchronisiert, aber SharePoint verwaltete die Stammdaten. Für Aufgabenlisten besteht weiterhin Lese-/Schreibzugriff.
    
- (C) Nach der Verknüpfung kann Project Professional neue Projekte erstellen und in Project Server speichern oder veröffentlichen. Der aktive Cache in Project Professional verwaltet die Datensynchronisierung mit Project Server.
    
- (D) Wenn Sie ein neues Projekt in Project Professional veröffentlicht wurde, hat der Benutzer die Möglichkeit, eine Projektwebsite für das Projekt erstellen. Ein Projekt kann auch in Project Web App als ein Projekt Liste SharePoint oder als einen Vollzugriff Enterprise-Projekttyp (EPT) erstellt. Schritt (D) zeigt die EPT Vollzugriff.
    
**Abbildung 1. Verwenden von Projektwebsites als SharePoint-Aufgabenlisten**

![Verwenden von Projektwebsites im Sichtbarkeitsmodus] (media/pj15_Architecture_VisibilityMode.gif "Verwenden von Projektwebsites im Sichtbarkeitsmodus")

<br/>

### <a name="managing-projects-with-full-control"></a>Verwalten von Projekten mit Vollzugriff
<a name="pj15_Architecture_ManagedMode"> </a>

Bei Project Server einer Websitesammlung zugeordnet ist und verfügt über uneingeschränkten Zugriff, Project Server importiert SharePoint-als Enterprise-Projekte Aufgabenlisten und alle zugehörigen MPP-Dateien löschen können. Projektserver verwaltet die master Daten für die vorgangssynchronisierung-Liste. Aufgabenlisten in der Websitesammlung werden schreibgeschützte (siehe Abbildung 2). Importierte Projekte können mithilfe von Project Professional oder mithilfe von Project Web App bearbeitet werden.
  
> [!NOTE]
> Nachdem Project Server ein Projekt importiert hat, legt der Benutzer fest, ob das Projekt von der Website gelöscht werden soll, oder ob die Verbindung abgebrochen werden soll, bevor das Projekt bearbeitet wird. Diese Auswahl kann in Project Professional getroffen werden. 
  
In Abbildung 2 sind die folgenden Prozesse für das Verwalten von Enterprise-Projekten durch Project Server mit Vollzugriff dargestellt:
  
- (A) Der Benutzer kann festlegen, welche Projektwebsites importiert werden sollen. Project Server importiert die Projektwebsites und löscht optional zugehörige MPP-Dateien. Die SharePoint-Aufgabenliste eines importierten Projekts ist schreibgeschützt.
    
- (B) nach Zuordnung Project Professional erstellt neue Projekte gespeichert und in Project Server veröffentlicht. Dem aktiven Cache in Project Professional verwaltet datensynchronisierung mit Project Server. Das Zeitplan-Webpart in Project Web App kann serverseitige Planung vornehmen.
    
- (C) Wenn Sie ein neues Projekt in Project Professional veröffentlicht wurde, hat der Benutzer die Möglichkeit, eine Projektwebsite für das Projekt erstellen. Ein Projekt kann auch in Project Web App mit einer EPT Vollzugriff erstellt und mit einer nur-Lese-Aufgabenliste zu einer Projektwebsite in der Websitesammlung veröffentlicht werden.
    
**Abbildung 2. Verwenden von Projektwebsites mit Vollzugriff**

![Verwenden von Projektwebsites im verwalteten Modus] (media/pj15_Architecture_ManagedMode.gif "Verwenden von Projektwebsites im verwalteten Modus")
  
## <a name="general-architecture"></a>Allgemeine Architektur
<a name="pj15_Architecture_General"> </a>

Abbildung 3 zeigt eine allgemeine Ansicht der Project Server 2013-Architektur, einschließlich der Project-Anwendungsdienst, eine Project Web App-Instanz auf einem WFE und mehrere Clientanwendungen einschließlich Project Professional 2013.
  
Mehrere Project Web App-Instanzen, die mit der Back-End-Project-Anwendungsdienst kommunizieren kann. Für eine lokale Installation das WFE kann auf einem separaten Server in einer SharePoint-Farm sein, oder es kann sein, auf dem gleichen SharePoint-Server mit der Project-Anwendungsdienst. Project Online enthält eine WFE, die Project Service-Anwendung und einem lokalen oder Remotecomputer Workflow-Manager-Client 1.0-Server. 
  
**Abbildung 3. Allgemeine Project Server 2013-Architektur**

![Project Server-Architektur] (media/pj15_Architecture_ProjectServiceApp_WFE.gif "Project Server-Architektur")

<br/>

Für Abbildung 3 gelten die folgenden allgemeinen Anmerkungen:
  
- **Project Online:** Sie können apps erstellen, die die CSOM, REST und OData-Schnittstellen verwenden. Ein app-Paket kann auch remote-Ereignisempfänger in einem benutzerdefinierten Webdienst auf einem lokalen Server, auf einem Azure-Server oder in Windows Azure installieren. Project Online unterstützt keine von Drittanbietern in lokalen Lösungen, die WCF-Schnittstelle, die ASMX-Interface oder lokale Ereignishandler. 
    
- **-Ereignisempfänger:** Ereignisempfänger können auch Ereignishandler aufgerufen werden. Project Online unterstützt die Registrierung von remote Project Server-Ereignisempfänger, indem Sie eine Project Web App-Instanz in der Cloud oder einer lokalen Project Server-Installation verwendet werden können. Eine lokalen Project Server-Installation unterstützt remote-Ereignisempfänger und lokale Ereignishandler volle Vertrauenswürdigkeit. 
    
- **Browser:** In Project Server 2010 vorhanden sind, sind keine browserübergreifende-Einschränkungen auf einigen Seiten Project Web App anzeigen. Die folgenden Browser werden für die vollständige Verwendung mit Project Web App unterstützt: 
    
  - Internet Explorer 8.x (unter Windows 7 und früheren Versionen von Microsoft Windows), Internet Explorer 9.x und Internet Explorer 10.x 
  - Firefox 4.x (unter Windows, Mac OS-X und Linux/Unix)
  - Safari 5.x (unter Windows und Mac OS-X)
  - Chrome
    
- **Programmierschnittstellen:** Für Drittanbieter-apps stellt die HTTP/HTTPS-Schnittstelle (einschließlich REST), die CSOM-Schnittstelle, einen OData-Dienst für das CSOM und einen OData-Dienst für die berichterstellung Project Online. Drittanbieter-Clientanwendungen, die lokal (auf dem Intranet), können die WCF-Schnittstelle für die PSI oder Sie können die CSOM, OData und REST-Schnittstellen über HTTP verwenden. Die Project Web App und Project Professional 2013 Clients verwenden die WCF-Schnittstelle. In einer Einzelserverinstallation rufen Sie die Front-End-ASMX-Webdienste, CSOM und REST intern die Back-End-WCF-Dienste. 
    
    > [!NOTE]
    > Die SOAP-basierte ASMX-Interface für Webdienste im PSI ist in Project Server 2013 weiterhin verfügbar, jedoch ist veraltet. 
  
    OData-Dienst für die berichterstellung wird von der internen OData.svc WCF-Dienst implementiert. Sie können das Metadatendokument Service für die Berichtsdaten abrufen, mithilfe von `http://ServerName/ProjectServerName/_api/ProjectData/$metadata`. 
    
    OData-Dienst für das CSOM ist für Plattformen wie Windows RT, iOS und Android, wo Sie die REST-Schnittstelle mit JavaScript in HTML-Seiten verwenden können vorgesehen. 
    
    > [!NOTE]
    > Obwohl die `$metadata` Option für den **ProjectData** -Dienst ist gültig, reporting der `$metadata` option für die endgültige Produktversion von Project Server 2013 **ProjectServer** -Dienst, der die CSOM entfernt wird. Weitere Informationen zur REST-Abfragen für das CSOM finden Sie unter [Client-seitigen Objektmodell (CSOM) für Project Server](client-side-object-model-csom-for-project-2013.md). 
  
- **PSI-Weiterleitung:** Den programmgesteuerten Zugriff auf die PSI auf einem separaten WFE durchläuft die PSI-Weiterleitung, einschließlich einer WCF-Weiterleitung und eine Web-Service-Weiterleitung. Clients, die die ASMX-Schnittstelle verwenden Zugriff auf die PSI über die Web-Service-Weiterleitung. Clients, die das WCF-Interface verwenden Zugriff auf die PSI über die WCF-Weiterleitung. Programmgesteuerten Zugriff über die CSOM, OData und REST über die WCF-Weiterleitung geleitet. 
    
- **Workflows:** Deklarative Workflows (Workflows, die in SharePoint Designer 2013 definiert werden) sind für die Verarbeitung an Workflow-Manager-Client 1.0 übergeben. Workflow-Manager-Client 1.0 können auf einem separaten Server in der SharePoint-Farm, auf Microsoft Azure in der Cloud oder auf einem Computer zum Testen oder Präsentationen zu Project Server ausführen. Codierten Workflows, die mit Visual Studio 2012 entwickelt werden, werden in die Workflowlaufzeit in SharePoint, wie in Project Server 2010 verarbeitet. Weitere Informationen finden Sie unter [Erste Schritte, Entwickeln von Project Server-Workflows](getting-started-developing-project-server-workflows.md).
    
- **Umkreisnetzwerk (DMZ):** Abbildung 3 zeigt keine, dass ein lokale WFE-Server durch eine zusätzliche Firewall in einem Umkreisnetzwerk (auch bekannt als "Demilitarized Zone" oder DMZ) isoliert werden kann. Einem Umkreisnetzwerk kann Internetclients SharePoint und Project Server über eine Firewall zugreifen können. 
    
- **SharePoint-Webdienste:** Abbildung 3 zeigt keine SharePoint-Infrastruktur, wie die Back-End SharePoint Web Services-Anwendung, der Bestandteil von SharePoint Server 2013 ist. Bei der Installation von Project Server wird die SharePoint-Webdienste die Project Service-Anwendung hinzugefügt. 
    
Die Front-End-Ebene umfasst drittanbieteranwendungen, Project Professional und Project Web App. Ein Browser zeigt ASP.NET 4.0-Seiten (ASPX-Seiten) in Project Web App. Die Project Web App-Seiten verwenden Project Server-Webparts, die Kommunikation mit den PSI und auch die standardmäßigen SharePoint-Webparts verwenden. 
  
Die mittlere Ebene enthält die PSI und die geschäftsobjektschicht, der logischen Objekte besteht, die Project Server-Geschäftseinheiten darstellen. Geschäftseinheiten enthalten Projekts, Aufgabe, Ressource, Zuordnung usw.. Die PSI und die Business-Objekt-Ebene sind eng gekoppelt und auf dem gleichen Server befinden. Eine Clientanwendung ruft die PSI über eine der verfügbaren Schnittstellen und die PSI ruft Geschäftsobjekte. Für verbesserte Leistung enthält WFE von Project Server 2013 einige Geschäftsobjekte für Anforderungen, die nicht das Project Server-Warteschlangensystem verwenden oder die Project-Berechnungen erfordern. Die WFE-Geschäftsobjekte kommunizieren direkt mit der Project-Datenbank.
  
Die Project Web App-Komponenten von Project Server verwenden Sie die Konfigurationsdatenbank der SharePoint 2013 für Project Site-Setups und der Inhaltsdatenbank für Inhalt der Projektwebsite wie Aufgabenlisten, benutzerdefinierte Seiten, Workflows, Einstellungen für die Verwaltung, Dokumente und Listen Probleme, Risiken und zusicherungen. Die SharePoint-Konfigurationsdatenbank und die Inhaltsdatenbanken Support zusätzlichen Features für das Projektmanagement wie Projektvorlagen und Arbeitsbereiche, sind benutzerdefinierte für die Zusammenarbeit im Team und Berichten aufgeführt.
  
### <a name="project-web-app-and-the-wfe"></a>Project Web App und das WFE
<a name="pj15_Architecture_PWAServer"> </a>

Sie können mehrere Instanzen von Project Web App auf einem WFE und mehrere WFE-Server im Intranet eines Unternehmens, die Verteilung der Last für Intranet-Clients zu aktivieren konfigurieren. Wenn eine Clientanwendung eine Project Web App-Instanz auf einem separaten WFE-Server verwendet wird, werden PSI-Aufrufe durch die PSI-Weiterleitung weitergeleitet. Die PSI-Weiterleitung (die WCF-Weiterleitung oder die Weiterleitung der Web-Service) führt die folgenden Funktionen:
  
- Optimiert Aufrufe von Remote-Clients an das PSI.
    
- Unterscheidet zwischen PSI-Aufrufen, die den Project Server-Warteschlangendienst erfordern, und Aufrufen, für die kein Warteschlangendienst erforderlich ist. Die Bezeichnungen von asynchronen PSI-Methoden beginnen mit "Queue", wie **QueueCreateProject**.
    
- Ermittelt PSI-Aufrufe, die registrierte lokale Ereignishandler  aufrufen.
    
- Ermittelt PSI-Aufrufe, die den Dienst für Project-Berechnungen erfordern.
    
- Verwendet einen serverbasierten Cache, der gemeinsam mit dem Client-seitigen aktiven Cache in Project Professional umlaufende Aufrufe an Project Server reduziert.
    
Nach dem SharePoint-Server einen Project Server-Benutzer authentifiziert, sendet die PSI-Weiterleitung transparent Anfragen, die Back-End-Services auf die PSI-Dienste auf dem Computer mit Project Server zu verwenden. Anforderungen, die keine Back-End-Diensten erforderlich ist, werden an die Business-Objekte in der lokalen Project Web App-Instanz gesendet. Die PSI-Weiterleitung verbessert Skalierbarkeit, Leistung und Zuverlässigkeit für Project Server über das LAN, ein WAN und in Project Online verarbeitet.
  
Project Web App wird mit ASP.NET 4.0 entwickelt. Die visuellen Elemente in ASPX-Dateien (HTML, Serversteuerelemente und statischen Text) unterscheiden sich von die Programmierlogik im Code-Behind-Klassen, die in kompilierten Assemblys (DLL-Dateien) sind. Seiten der Website in Project Web App, wie die Seite auf höchster Ebene, Project Center und Berichtscenter, können mithilfe von Webparts angepasst werden. Anwendungsseiten, die nicht über eine Option **Seite bearbeiten** im Menü **Websiteaktionen** verfügen können nicht bearbeitet werden, wie der Seite servereinstellungen und der Seite Überprüfung Arbeitszeittabelle. 
  
### <a name="the-csom-and-the-project-server-interface"></a>Das CSOM und das Project Server Interface
<a name="pj15_Architecture_PSI"> </a>

Die PSI wird 22 öffentlichen Diensten wie **Projekt-**, **Ressourcen-**, **benutzerdefiniertes**und **Zeitberichte**umgerechnet. Die PSI enthält auch sieben private Dienste für die interne Verwendung. Die PSI ist die grundlegende API von Project Server. Project Server-Funktionalität der csom und zum externen Anwendungen macht. Das CSOM enthält Klassen, die Zugriff auf die am häufigsten verwendeten PSI-Klassen und Member, die für Anwendungen von Drittanbietern verwendet werden. In Project Server 2013 ist einige Project Server-Funktionen nicht verfügbar in den CSOM, wie die Dienste **Admin**, **Kalender**, **PortfolioAnalyses**und **Sicherheit** . 
  
Project Professional 2013 und Project Web App verwenden die PSI Zugriff auf Project Server-Daten in den Entwurf, veröffentlicht, und Archivieren von Tabellen und Ansichten der Project-Datenbank. Sie können einen PSI-Dienst über eine Proxydatei oder einer Proxyassembly für die WCF-Dienste oder die ASMX-Webdienste zugreifen.
  
> [!NOTE]
> Das CSOM ist die bevorzugte Schnittstelle für Project Server-Entwickler von Drittanbietern. Sie können für Anwendungen verwendet werden, die sowohl einen lokalen Project Server-Installation und Project Online zugreifen. Es wird empfohlen, dass Sie das CSOM verwenden für die Entwicklung von neuen Anwendung, wenn das CSOM die Funktionen enthält, die die Anwendung erfordert. 
  
Einige Line-of-Business (LOB)-Anwendungen und andere drittanbieteranwendungen, die für Project Server 2010 entwickelt wurden erfordern PSI-Dienste, die noch nicht in der CSOM dargestellt werden. Wenn sie nur eine lokale Installation von Project Server abzielen, können Applikationen auch weiterhin mithilfe der WCF-Schnittstelle oder die ASMX-Schnittstelle von der PSI.
  
Clientanwendungen rufen Sie die PSI über Webdienstproxys. Clients, die das WCF-Interface verwenden Zugriff auf alle PSI-Dienste über `http://ServerName/ProjectServerName/_vti_bin/psi/ProjectServer.svc`. Clients, die eine Webdienstschnittstelle ASMX verwenden verwenden Sie die Project Web App-URL für den bestimmten Dienst. Der Dienst für die **Ressource** ist beispielsweise unter `http://ServerName/ProjectServerName/_vti_bin/psi/resource.asmx?wsdl`. Wenn Applikationen nicht Intranetzugriff auf Project Server verfügen, können sie einen Project Web App-Server in einem Umkreisnetzwerk bereit (nicht in Abbildung 3 dargestellt).
  
Abbildung 4 zeigt den Bereich **Verbindungen** in **Internetinformationsdienste (Internet Information Services, IIS)-Manager** für eine Einzelserverinstallation von SharePoint Server 2013, Project Server 2013 und einer lokalen Website verwalten von Workflows für Workflow-Manager-Client 1.0. SharePoint-Websitesammlung (A) enthält die Front-End-PSI-Dienste in der `_vti_bin\PSI` virtuellen Unterverzeichnis. Die SharePoint-Webdienste-Anwendung (B) enthält die Project Service-Anwendung, mit der Back-End-PSI-Dienste in der `508c23fb7dfd4c83a8919fae24bc68c5/PSI` virtuellen Unterverzeichnis. Die GUID ist der Name der Instanz Project Service-Anwendung für die Project Server-Installation. 
  
**Abbildung 4. Front-End-PSI (A) und Back-End-PSI (B) in IIS-Manager**

![Die Front-End-PSI und die Back-End-PSI] (media/pj15_Architecture_PSI_IIS.gif "Die Front-End-PSI und die Back-End-PSI")
  
Clientanwendungen können nicht direkt die WCF-Dienste für die in der Back-End-Project-Anwendungsdienst PSI zugreifen. Wenn sie Zugriff auf Project Online keine erfordern, verwenden Clientanwendungen und Komponenten von LOB-Anwendungen für die PSI Proxys. Eine Back-End-URL für die WCF-Schnittstelle von der **Ressource** Dienst in Abbildung 4 ist, zum Beispiel wäre `http://ServerName:32843/508c23fb7dfd4c83a8919fae24bc68c5/psi/resource.svc`. Port 32843 ist der Standard-HTTP-Port für die SharePoint-Webdienste-Anwendung (32844 ist der Port für die Kommunikation mit HTTPS). Jedoch die Datei "Web.config" für Project Web App-Blöcke direkter Zugriff auf Back-End-PSI-Dienste.
  
> [!NOTE]
> Der Project 2013-SDK-Download umfasst PSI-Proxydateien für die WCF-Dienste und die ASMX-Dienste und Anleitungen zur Verwendung in Proxy-Assemblies diese zu kompilieren. > Um aktualisierte PSI-Proxydateien zu erstellen, die das WCF-Interface verwenden, müssen Sie das Hilfsprogramm "svcutil.exe" oder Visual Studio direkt auf dem Project Server-Computer verwenden. 
  
Mitglieder der PSI-Dienste in der Regel erstellen oder nutzen typisierte **DataSet** -Objekte als Mittel zum Austauschen von Informationen mit der Business-Objekten. Es gibt auch mehrere verschiedene Modelle für die PSI-Entwicklung. Beispiel der **Ressource**, **CustomFields**und **LookupTable** PSI-Dienste verwenden XML-Filter-Objekte für die Bearbeitung von **DataSet** und andere Dienste nicht; Einige Methoden in den **Statusing** -Dienst verwenden einen _ChangeXml_ -Parameter, während andere Methoden und die Dienste nicht der Fall ist. Das CSOM wird Datasets nicht verwendet werden. Obwohl das CSOM verfügt über ein anderes Programmiermodell als die PSI und .NET Assemblies oder JavaScript können, ist-Entwicklung mit dem Clientobjektmodell im Allgemeinen einfacher und konsistenter als-Entwicklung mit den PSI. 
  
Weitere Informationen zu den PSI finden Sie unter [Project PSI-Referenz (Übersicht)](project-psi-reference-overview.md). Weitere Informationen zu den CSOM finden Sie unter [Client-seitigen Objektmodell (CSOM) für Project 2013](client-side-object-model-csom-for-project-2013.md).
  
### <a name="business-objects-in-the-wfe-and-the-project-service-application"></a>Geschäftsobjekte im WFE und die Project-Dienstanwendung
<a name="pj15_Architecture_BusinessObjects"> </a>

Das interne Objektmodell von Project Server umfasst die Geschäftsobjekte, die logische Entitäten wie "Project" und "Resource" repräsentieren. Client-Anwendungen greifen ausschließlich über das CSOM oder das PSI auf Geschäftsobjekte zu. Geschäftsobjekte wiederum greifen auf die Entwurfstabellen und -ansichten, veröffentlichten Tabellen und Ansichten sowie die Archivtabellen und -ansichten der Project-Datenbank zu.
  
Geschäftsobjekte sind für Drittanbieterentwickler nicht zugänglich. Das PSI verwaltet die Zuordnung des API zu den Geschäftsobjekten, und das CSOM ordnet sein API dem PSI zu. Die logischen Entitäten von Geschäftsobjekten können in drei Typen unterteilt werden:
  
- **Kernentitäten** sind Objekte wie Projekte, Aufgaben, Aufträge, Ressourcen und Kalender. Die Kernentitäten umfassen grundlegende Bestandteile der Geschäftslogik wie Berechtigungen und Benennungsregeln. 
    
- **Geschäftsentitäten** sind Objekte wie Arbeitszeittabellen, Projektportfolios und Modelle. Geschäftsentitäten umfassen weiterreichende Bestandteile der Geschäftslogik und werden in der Regel durch die Kombination von Kernentitäten gebildet. 
    
- **Unterstützende Entitäten** sind u. a. Objekte für die Sicherheit und Validierung. 
    
In Project Server 2010 werden alle von Geschäftsobjekten in der Project-Anwendung implementiert. In Project Server 2013 hostet das WFE viele Business-Objekten, die synchrone Methoden zu verarbeiten und erfordern keinen Project-Berechnungen. Synchrone PSI-Methoden wie **DeleteProject** und **ReadAssignments** verwenden Sie die Project Server-Warteschlangendienst nicht. Asynchrone Methoden in die PSI haben Namen, die beginnen mit `Queue`, wie **QueueCreateProject** und **QueueUpdateTimesheet**. Eine asynchrone Methode sendet eine Nachricht an die Project Server-Warteschlangendienst, der Verarbeitung der Methode plant, während die Steuerung an den Benutzer zurückgegeben wird.
  
Die PSI-Weiterleitung bestimmt, welche Anforderungen an die Project-Dienstanwendung gesendet werden und welche Anforderungen von den Geschäftsobjekten im WFE verarbeitet werden können. Die Geschäftsobjekte im WFE umgehen die Project-Dienstanwendung und haben direkten Zugriff auf die Project-Datenbank, ganz ähnlich wie es bei SharePoint-Prozessen in einem WFE der Fall ist, die direkt auf die Konfigurations- und Inhaltsdatenbanken zugreifen. Je mehr Geschäftsobjekte auf dem WFE ausgeführt werden, umso höher ist die Effizienz von Project Server, umso mehr wird die Anwendungsschicht entlastet und umso besser kann Project Server für eine steigende Arbeitsauslastung skaliert werden.
  
> [!NOTE]
> In Project Server 2013 müssen das WFE und die Project Server-Back-End-Computer lokale Ereignishandler bereitgestellt werden. 
  
### <a name="project-server-database"></a>Project Server-Datenbank
<a name="pj15_Architecture_DAL"> </a>

Die vier Project Server-Datenbanken der vorherigen Versionen werden in Project Server 2013 in einer Project-Datenbank in SQL Server zusammengefasst. Der Standardname der Project-Datenbank ist ProjectService. Reporting Tabellen und Sichten behalten ihre vorherigen Namen mit der `dbo` Präfix, wie beispielsweise Dbo. MSP_EpmProject und die Tabelle Dbo. MSP_EpmProject_UserView. Tabellen und Ansichten, die bereits in der Datenbank Entwurf der `draft` Präfix. Tabellen und Sichten aus der veröffentlichten Datenbank haben die `pub` Präfix. Tabellen und Sichten aus der Archivdatenbank haben die `ver` Präfix. 
  
> [!IMPORTANT]
> Direkter Zugriff wird nicht unterstützt, für den Entwurf ( `draft` Präfix), veröffentlichte ( `pub` Präfix), und die Archivdatenbank ( `ver` Präfix) Tabellen und Ansichten. Nur die reporting Tabellen und Ansichten, in denen haben verwenden die `dbo` Präfix. 
  
Project Server-Daten werden wie folgt in der Project-Datenbank aufgeteilt:
  
- Der Entwurf Tabellen und Ansichten enthalten Daten aus nicht veröffentlichte Projekte, die von Project Professional und andere Clientanwendungen erstellt wurden. Project-Daten aus den Entwurf Tabellen und Ansichten wird von Project Web App nicht angezeigt.
    
- Veröffentlichte Tabellen und Ansichten enthalten alle die veröffentlichten Projekte und Enterprise-Ressourcen, globale Daten für Enterprise-Projekttypen (EPTs) und anderen Projektvorlagen. Veröffentlichte Projekte werden in Project Web App angezeigt. Die veröffentlichten Daten enthält auch Tabellen, die speziell für Project Web App (Arbeitszeittabellen, Modelle, Ansichten usw.) sind und globalen Datentabellen (benutzerdefinierte Felder, Nachschlagetabellen, Autorisierungsberechtigungen für Project Server und Metadaten).
    
- In Archivdaten werden Sicherungsversionen von Projekten, Ressourcen, benutzerdefinierten Felder und weiteren Daten gespeichert.
    
- Die Berichtsdaten können für schreibgeschützten Zugriff in Anwendungen von Drittanbietern sowie für Berichte verwendet werden. Project Server-OLAP-Cubes verwenden Sie die Berichtsansichten, die die `_OlapView` Suffix. OLAP-Cubes in einer lokalen Project Server-Installation verfügbar sind, jedoch stehen nicht in Project Online. 
    
    Berichtsdaten sind sehr umfangreich und werden nahezu in Echtzeit aktualisiert. Die Berichtstabellen und -ansichten sind für die Generierung von schreibgeschützten Berichten optimiert. So sind Berichtstabellen z. B. denormalisiert, um redundante Daten zu ermöglichen und die Anzahl relationaler Tabellen zu reduzieren.
    
Logische Entitäten wie "Resource" oder "Project" können sich über mehrere Tabellen erstrecken, und alle Tabellen für eine bestimmte Entität haben denselben Primärschlüssel. Der Primärschlüssel ist eine GUID in einer einzelnen Spalte, die eine Instanz einer bestimmten Entität eindeutig kennzeichnet.
  
Project Server-Daten für jede Instanz von Project Web App werden in einer separaten Projektdatenbank mit einem anderen Namen gespeichert. Clientanwendungen, die direkten auf Project Server Zugriff können direkt reporting Tabellen und Ansichten gelesen werden. Für den Remotezugriff können-Clientanwendungen die OData und der REST-Schnittstelle Sie Daten für Berichte abrufen. Clients verwenden Sie nur das CSOM oder die PSI für den Entwurf, veröffentlicht, Zugriff auf und Archivieren von Tabellen und Ansichten. Reporting Data Service (RDS, der in Abbildung 3 nicht angezeigt wird) aktualisiert die Berichtsdaten aus veröffentlichte Daten in nahezu in Echtzeit. Die Project-Datenbank kann auf einem separaten Server befinden.
  
Schemas sind nur für Tabellen und Sichten reporting dokumentiert. Für eine lokale Project Server-Installation können Sie hinzufügen reporting Tabellen und Ansichten für Entitäten, die nicht im Project-Datenbankschema definiert sind. Sie können auch separate Datenbanken für lokale benutzerdefinierte Anwendungen erstellen. Änderung wird nicht unterstützt, für den Entwurf, veröffentlicht und Archivieren von Tabellen und Ansichten. Da die Project-Datenbank nicht direkt in Project Online zugänglich ist, kann nicht reporting Tabellen und Ansichten geändert werden. Wenn Sie eine SQL Azure-Konto verfügen, können Sie separate Datenbanken für die benutzerdefinierte Verwendung mit Project Online erstellen.
  
### <a name="event-receivers"></a>Ereignisempfänger
<a name="pj15_Architecture_EventHandlers"> </a>

Lokale Ereignishandler und remote-Ereignisempfänger für Project Server von Drittanbietern Erweiterbarkeit Reaktion auf Project Server-Ereignisse wie erstellen oder die Veröffentlichung eines Projekts zu ermöglichen. In Project Server 2010 alle Ereignishandler lokal und in voll vertrauenswürdiger Code, direkt auf dem Computer mit Project Server und der WFEs bereitgestellt, und führen in der Project Server-Ereignisdienst System geschrieben werden. Da Project Online voll vertrauenswürdige-Ereignishandler nicht verwendet werden, implementiert Project Server 2013 remote-Ereignisempfänger, die die remote-Ereignisempfänger in SharePoint Server 2013 ähneln. Eine lokale Installation von Project Server 2013 kann herkömmliche voll vertrauenswürdige Ereignishandler und remote-Ereignisempfänger verwenden.
  
Ein Project Server-remote-Ereignisempfänger kann in einem benutzerdefinierten Webdienst mit einem SOAP-Endpunkt implementiert werden, die in Microsoft Azure oder anderen Umgebungen, die SOAP-Webdienste unterstützen ausgeführt wird. Ein Project Server-app-Paket kann remote-Ereignisempfänger enthalten, die mit der app installiert sind.
  
Remote-Ereignisempfänger können in Project Server erreichen mithilfe der CSOM-Endpunkte (nicht in Abbildung 3 dargestellt). Der Anruf an einen remote-Ereignisempfänger enthält die Informationen aus der Project Server-Ereignis-System und die Project Web App-Instanz (oder den Project Web App-Mandanten in Project Online), der den Anruf. Remote-Ereignisempfänger ermöglichen Ihnen das Erstellen und Hosten von einem einzigen Webdienst, der von mehreren Project Server-Installationen verwendet werden kann. Dagegen müssen lokale Ereignishandler voll vertrauenswürdige auf jede Installation von Project Server bereitgestellt werden.
  
### <a name="publishing-and-server-side-scheduling"></a>Veröffentlichung und serverseitige Zeitplanung
<a name="pj15_Architecture_PublishingScheduling"> </a>

Projektserver 2013 unterstützt sowohl manuelle und automatisierte Projekt Planen von Updates. Standardmäßig wird ein Update manuellen Zeitplan. D. h., der Projektmanager checkt und öffnet ein Projekt in Project Professional oder Project Web App, gilt die Änderungen, und klicken Sie dann gespeichert und veröffentlicht das Projekt, um die Änderungen für alle Benutzer verfügbar zu machen. Project Professional verfügt über eine Planungsmodul, die Änderungen berechnet und speichert dann die Änderungen in Project Server. In Project Server 2010 ist das serverseitige Planungsmodul Implementierung unterscheidet sich vom Planungsmodul in Project Professional.
  
In Project Server 2013 implementiert die Project-Berechnungen gleiche Planungsmodul, das in Project Professional 2013 ist. Project-Berechnungen in einem Windowsdienst mit dem Namen **Microsoft Project Server-Berechnungen**ausgeführt wird. Bearbeiten einen Projektplan in Project Web App oder drittanbieteranwendungen, die die CSOM-Ergebnisse in genau die gleiche Änderung Zeitplan verwenden, die Project Professional machen.
  
> [!NOTE]
> Drittanbieteranwendungen, mit denen die PSI möglicherweise Unterschiede Terminplan aus einem Zeitplan angezeigt, die Project Web App berechnet. Zur Abwärtskompatibilität verwenden Sie öffentlichen PSI-Methoden, die serverseitige Planung noch erledigen Planungsmodul, das in Project Server 2010 eingeführt wurde. Eine Ausnahme ist **QueueUpdateProject2**, das eine neue PSI-Methode in Project Server 2013 ist. Beispielsweise das ältere Planungsmodul überhaupt nicht plant, Unterprojekte oder Hyperlinks zu anderen Projekten und Ertragswert-Felder werden nicht berechnet. Zur Vermeidung von sollten potenzielle Unterschiede zwischen drittanbieteranwendungen und Project Professional oder Project Web App planen, Sie Anwendungen mit dem Clientobjektmodell möglichst entwickeln. 
  
Project Server ermöglicht es anhand der folgenden Schritte, dass die veröffentlichte Version aktualisiert werden kann, während ein Projektmanager die Entwurfsversion verwendet:
  
1. Project Server übernimmt Aktualisierungen und plant die veröffentlichte Version neu.
    
2. Project Server speichert die Aktualisierung, um sie in die Entwurfsversion zu implementieren, wenn eines der folgenden Ereignisse eintritt:
    
   - Project Professional öffnet das Projekt.
    
   - Project Professional versucht, das Projekt zu veröffentlichen.
    
3. Bei einem Konflikt wird der Projektmanager benachrichtigt und muss den Konflikt beheben, damit die Entwurfsversion veröffentlicht werden kann.
    
## <a name="see-also"></a>Siehe auch

- [Übersicht über Project 2013 für Entwickler](http://msdn.microsoft.com/library/8da91ab0-af4f-429f-8241-490600e3f7bd%28Office.15%29.aspx)
- [Project Server-Programmierbarkeit](project-server-programmability.md)  
- [Clientseitiges Objektmodell (CSOM) für Project 2013](client-side-object-model-csom-for-project-2013.md)  
- [Was die PSI durchführen kann und was nicht](what-the-psi-does-and-does-not-do.md)  
- [Erste Schritte beim Entwickeln von Project Server-Workflows](getting-started-developing-project-server-workflows.md)   
- [Project-PSI-Referenz – Übersicht](project-psi-reference-overview.md)   
- [Open Data Protocol](http://www.odata.org/)
    

