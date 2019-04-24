---
title: Project Server-Architektur
manager: soliver
ms.date: 09/17/2015
ms.audience: Developer
ms.assetid: 2cfa5a6e-2f5c-440c-b35a-bc7a34648f9c
description: Project Server 2013 integriert Projektmanagement-Funktionen in eine SharePoint-Farm und ermöglicht die Verwendung von Project Online mit einem clientseitigen Objektmodell (CSOM) sowie einer OData-Schnittstelle für Berichtsdaten.
localization_priority: Priority
ms.openlocfilehash: db4dd0eed9c043021f586041fa0e28708fdbd243
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32301598"
---
# <a name="project-server-architecture"></a>Project Server-Architektur

Project Server 2013 integriert Projektmanagement-Funktionen in eine SharePoint-Farm und ermöglicht die Verwendung von Project Online mit einem clientseitigen Objektmodell (CSOM) sowie einer OData-Schnittstelle für Berichtsdaten.
   
Project Server 2013 ist ein mehrstufiges System, das die in Office Project Server 2007 eingeführte Architektur erweitert. Zu den Architekturänderungen zählt die Zuweisung von Project-Anwendungsdiensten zu SharePoint-Websitesammlungen, die Erweiterung um einige Geschäftsobjekte im Web-Front-End (WFE), das clientseitige Objektmodell (CSOM) für Remotezugriff, eine einzelne Project-Datenbank, eine OData-Schnittstelle für Berichtstabellen und -ansichten, die Integration von Windows Workflow Foundation Version 4 (WF4) über Workflow Manager Client 1.0 in der Cloud oder auf einem lokalen Server sowie Remoteereignisempfänger, auf die mehrere Project Server-Installationen zugreifen können. Zusätzlich zu lokalen benutzerdefinierten Lösungen können Sie Apps erstellen, die Remoteereignisempfänger und Komponenten umfassen, die auf die CSOM- und OData-Schnittstellen zugreifen.
  
Zur Front-End-Stufe gehören Project Professional 2013, Project Web App und Apps von Drittanbietern. Client-Anwendungen kommunizieren über das Project Server Interface (PSI) oder über CSOM-Endpunkte mit der mittleren Schicht, die wiederum mit dem PSI und der Geschäftsobjekt-Schicht kommunizieren. Der Datenbankzugriff ist in die Geschäftsobjekte integriert. Das Project Server-Ereignissystem kann sowohl auf lokale Ereignishandler als auch auf Remoteereignisempfänger zugreifen. Der Project-Berechnungsdienst implementiert das Planungsmodul von Project Professional in Project Server. Clientanwendungen greifen nicht direkt (oder sollten dies zumindest nicht) auf die Project-Datenbank zugreifen, und in Project Server werden Geschäftsobjekte vor Clients verborgen.
  
> [!NOTE]
> Project Server basiert auf der SharePoint-Architektur. Weitere Informationen zur SharePoint Server 2013-Architektur und zum SharePoint-App-Modell finden Sie im Abschnitt *Erste Schritte bei der SharePoint-Entwicklung* in der Entwicklerdokumentation zu Office 2013. 

<a name="pj15_Architecture_SharePoint"> </a>

## <a name="integrating-with-sharepoint-site-collections"></a>Integration in SharePoint-Websitesammlungen

Der Project-Anwendungsdienst in Project Server 2013 kann für die Verwendung mit SharePoint-Aufgabenlisten einer SharePoint-Websitesammlung zugeordnet werden. Der Project-Anwendungsdienst kann zur umfassenden Steuerung von Project Server auch SharePoint-Aufgabenlisten als Enterprise-Projekt importieren. Mit einer SharePoint Aufgabenliste verwaltet SharePoint die Projektwebsite in einer Websitesammlung. Project Professional kann mit der Aufgabenliste synchronisiert werden und diese aktualisieren. Eine Projektwebsite kann eine unabhängige SharePoint-Aufgabenliste oder eine Aufgabenliste sein, die mit einer MPP-Datei synchronisiert ist. Die MPP-Datei kann lokal oder in einer SharePoint Bibliothek gespeichert werden. 
  
Project Server verwaltet die Projekte, wenn Vollzugriff besteht. Project Professional speichert Daten direkt in Project Server. Tabelle 1 bietet eine Vergleichsübersicht zum Verhalten einer Aufgabenliste, des Planungs-Webparts sowie weiterer Funktionen für die SharePoint-Steuerung von Aufgabenlisten und für importierte Projekte bei Vollzugriff durch Project Server. Das Planungs-Webpart enthält das Raster auf der Project Web App-Seite, auf der Sie einen Projektplan bearbeiten können. Im verknüpften Modus können Statusdaten nur einmalig für beide Aufgaben und Arbeitszeittabellen eingegeben werden. Im einfachen Eingabemodus werden die Statuserfassungsdaten für Aufgaben separat in die Arbeitszeittabellen eingegeben.
  
**Tabelle 1. Vergleich von SharePoint-Aufgabenlisten und Vollzugriff**

| Feature | Aufgabenliste | Vollzugriff |
|:-----|:-----|:-----|
|**Aufgabenliste in SharePoint** <br/> |Lesen/Schreiben  <br/> |Schreibgeschützt  <br/> |
|**Planungs-Webpart** <br/> |Schreibgeschützt  <br/> |Lesen/Schreiben  <br/> |
|**Berichterstellung** <br/> |Komplexe Berichterstellung über Project Server  <br/> |Komplexe Berichterstellung über Project Server  <br/> |
|**Sonstige Project Server-Funktionen** <br/> | Gesperrte Funktionen:  <br/>- Serverseitige Projektbearbeitungen mit Project Web App oder benutzerdefinierten Clientanwendungen  <br/>- Statuserfassung  <br/>- Aufgaben werden im verknüpften Modus nicht angezeigt  <br/> |Voller Funktionsumfang ist aktiviert  <br/> |
   
### <a name="managing-projects-as-sharepoint-task-lists"></a>Verwalten von Projekten als SharePoint-Aufgabenlisten
<a name="pj15_Architecture_VisibilityMode"> </a>

Wenn Project Server mit einer SharePoint-Websitesammlung verknüpft ist, in der SharePoint den Zugriff verwaltet, sind Aufgabenlisten und Project Professional 2013-Dateien (MPP) in Dokumentbibliotheken zwar für den Project-Anwendungsdienst zugänglich, aber SharePoint verwaltet die Stammdaten für die Synchronisierung (siehe Abbildung 1). Die serverseitige Zeitplanung mit dem Planungs-Webpart ist nicht möglich. Sie können Project Professional für die Synchronisierung mit Aufgabenlisten und deren Bearbeitung auf einer Projektwebsite verwenden. Wenn Organisationen damit beginnen, SharePoint-Aufgabenlisten einzusetzen, können sie sich schrittweise dahin entwickeln, den vollen Funktionsumfang von Project Server auszuschöpfen.
  
In Abbildung 1 sind die folgenden Prozesse für das Verwalten von Projekten in SharePoint-Aufgabenlisten dargestellt: 
  
- (A) Project Professional kann mit Aufgabenlisten synchronisiert werden und neue Projektwebsites in der Websitesammlung erstellen, bevor oder nachdem eine Verknüpfung mit dem Project-Anwendungsdienst hergestellt wurde.
    
- (B) Project Server wird zu Berichtzwecken mit Projektwebsitedaten synchronisiert, aber SharePoint verwaltete die Stammdaten. Für Aufgabenlisten besteht weiterhin Lese-/Schreibzugriff.
    
- (C) Nach der Verknüpfung kann Project Professional neue Projekte erstellen und in Project Server speichern oder veröffentlichen. Der aktive Cache in Project Professional verwaltet die Datensynchronisierung mit Project Server.
    
- (D) Wenn ein neues Projekt in Project Professional veröffentlicht wird, hat der Benutzer die Möglichkeit, eine Projektwebsite für das Projekt zu erstellen. Ein Projekt kann auch als SharePoint-Aufgabenlistenprojekt oder Enterprise-Projekt (EPT) mit Vollzugriff in Project Web App erstellt werden. Schritt (D) zeigt den ETP mit Vollzugriff.
    
**Abbildung 1. Verwenden von Projektwebsites als SharePoint-Aufgabenlisten**

![Verwenden von Projektwebsites im Sichtbarkeitsmodus](media/pj15_Architecture_VisibilityMode.gif "Verwenden von Projektwebsites im Sichtbarkeitsmodus")

<br/>

### <a name="managing-projects-with-full-control"></a>Verwalten von Projekten mit Vollzugriff
<a name="pj15_Architecture_ManagedMode"> </a>

Wenn Project Server mit einer Websitesammlung verknüpft ist und Vollzugriff besteht, importiert Project Server SharePoint-Aufgabenlisten als Enterprise-Projekte und kann jegliche zugehörigen MPP-Dateien löschen. Des Weiteren verwaltet Project Server die Stammdaten für die Aufgabenlistensynchronisierung. Aufgabenlisten in der Websitesammlung sind schreibgeschützt (siehe Abbildung 2). Importierte Projekte können mit Project Professional oder mit Project Web App bearbeitet werden.
  
> [!NOTE]
> Nachdem Project Server ein Projekt importiert hat, legt der Benutzer fest, ob das Projekt von der Website gelöscht werden soll, oder ob die Verbindung abgebrochen werden soll, bevor das Projekt bearbeitet wird. Diese Auswahl kann in Project Professional getroffen werden. 
  
In Abbildung 2 sind die folgenden Prozesse für das Verwalten von Enterprise-Projekten durch Project Server mit Vollzugriff dargestellt:
  
- (A) Der Benutzer kann festlegen, welche Projektwebsites importiert werden sollen. Project Server importiert die Projektwebsites und löscht optional zugehörige MPP-Dateien. Die SharePoint-Aufgabenliste eines importierten Projekts ist schreibgeschützt.
    
- (B) Nach dem Verknüpfen erstellt Project Professional neue Projekte und speichert oder veröffentlicht sie in Project Server. Der aktive Cache in Project Professional verwaltet die Datensynchronisierung mit Project Server. Die serverseitige Zeitplanung mit dem Planungs-Webpart in Project Web App ist möglich.
    
- (C) Wenn ein neues Projekt in Project Professional veröffentlicht wird, hat der Benutzer die Möglichkeit, eine Projektwebsite für das Projekt zu erstellen. Ein Projekt kann auch als Enterprise-Projekt (EPT) in Project Web App erstellt und mit einer schreibgeschützten Aufgabenliste auf einer Projektwebsite innerhalb der Websitesammlung veröffentlicht werden.
    
**Abbildung 2. Verwenden von Projektwebsites mit Vollzugriff**

![Verwenden von Projektwebsites im verwalteten Modus](media/pj15_Architecture_ManagedMode.gif "Verwenden von Projektwebsites im verwalteten Modus")
  
## <a name="general-architecture"></a>Allgemeine Architektur
<a name="pj15_Architecture_General"> </a>

Abbildung 3 bietet eine allgemeine Übersicht über eine Project Server 2013-Architektur mit der Project-Dienstanwendung, einer Project Web App-Instanz auf einem WFE und diversen weiteren Clientanwendungen, einschließlich Project Professional 2013.
  
Es können mehrere Project Web App-Instanzen mit der Back-End-Project-Dienstanwendung kommunizieren. Bei einer Installation vor Ort kann sich das WFE auf einem separaten Server in einer SharePoint-Farm befinden oder auf demselben SharePoint-Server wie die Project-Dienstanwendung. Project Online umfasst ein WFE, die Project-Dienstanwendung und einen lokalen oder Remoteserver für Workflow-Manager-Client 1.0. 
  
**Abbildung 3. Allgemeine Project Server 2013-Architektur**

![Project Server-Architektur](media/pj15_Architecture_ProjectServiceApp_WFE.gif "Project Server-Architektur")

<br/>

Für Abbildung 3 gelten die folgenden allgemeinen Anmerkungen:
  
- **Project Online:** Sie können Apps erstellen, die die CSOM-, REST- und OData-Schnittstellen verwenden. Ein App-Paket kann auch Remoteereignisempfänger in einem benutzerdefinierten Webdienst auf einem lokalen Server, auf einem Azure-Server oder auf Microsoft Azure installieren. In Project Online werden lokale Drittanbieterlösungen, die WCF-Schnittstelle, die ASMX-Schnittstelle oder lokale Ereignishandler nicht unterstützt 
    
- **Ereignisempfänger:** Ereignisempfänger können auch als Ereignishandler bezeichnet werden. Project Online unterstützt die Registrierung von Project Server-Remoteereignisempfängern, die von einer Project Web App-Instanz in der Cloud oder von einer lokalen Project Server-Installation verwendet werden können. Eine lokale Project Server-Installation unterstützt Remoteereignisempfänger und lokale, voll vertrauenswürdige Ereignishandler. 
    
- **Browser:** Für die Anzeige einiger Project Web App-Seiten bestehen anders als in Project Server 2010 keine browserübergreifenden Einschränkungen. Die folgenden Webbrowser werden für die vollständige Nutzung von Project Web App unterstützt: 
    
  - Internet Explorer 8.x (unter Windows 7 und früheren Versionen von Microsoft Windows), Internet Explorer 9.x und Internet Explorer 10.x 
  - Firefox 4.x (unter Windows, Mac OS-X und Linux/Unix)
  - Safari 5.x (unter Windows und Mac OS-X)
  - Chrome
    
- **Programmgesteuerte Schnittstellen:** Für Drittanbieter-Apps macht Project Online die HTTP-/HTTPS-Schnittstelle (einschließlich REST), die CSOM-Schnittstelle, einen OData-Dienst für CSOM und einen OData-Dienst für die Berichterstellung verfügbar. Für lokale Clientanwendungen von Drittanbietern (im Intranet), können Sie die WCF-Schnittstelle für die PSI oder die CSOM-, OData- und REST-Schnittstellen über HTTP verwenden. Die Project Web App- und Project Professional 2013-Clients verwenden beide die WCF-Schnittstelle. In einer Installation mit einem einzigen Server rufen die Front-End-ASMX-Webdienste, CSOM und REST die Back-End-WCF-Dienste intern auf. 
    
    > [!NOTE]
    > Das SOAP-basierte ASMX-Schnittstelle für Webdienste im PSI ist in Project Server 2013 zwar weiterhin verfügbar, gilt aber als überholt. 
  
    Der OData-Dienst für die Berichterstellung wird von dem internen WCF-Dienst „OData.svc" implementiert. Sie können das Dokument für den Metadatendienst für die Berichterstellungsdaten mithilfe von  `https://ServerName/ProjectServerName/_api/ProjectData/$metadata` abrufen. 
    
    Der OData-Dienst für CSOM ist für Plattformen wie Windows RT, iOS und Android ausgelegt, auf denen Sie die REST-Schnittstelle mit JavaScript in HTML-Seiten verwenden können. 
    
    > [!NOTE]
    > Obwohl die Option `$metadata` für den **ProjectData**-Berichtsdienst gültig ist, wurde die Option `$metadata` für den **ProjectServer**-Dienst des clientseitigen Objektmodells in der veröffentlichten Version von Project Server 2013 entfernt. Weitere Informationen zu REST-Abfragen für das CSOM finden Sie unter [Clientsseitiges Objektmodell (CSOM) für Project Server](client-side-object-model-csom-for-project-2013.md). 
  
- **PSI-Weiterleitung:** Der programmgesteuerte Zugriff auf das PSI über ein separates WFE wird über die PSI-Weiterleitung realisiert, die eine WCF-Weiterleitung und eine Webdienst-Weiterleitung. Clients, die die ASMX-Schnittstelle verwenden, greifen über die Webdienst-Weiterleitung auf das PSI zu. Clients, die das WCF-Interface verwenden, greifen über die WCF-Weiterleitung auf das PSI zu. Der programmgesteuerte Zugriff über CSOM, OData und REST wird ebenfalls über die WCF-Weiterleitung weitergereicht. 
    
- **Workflows:** Deklarative Workflows (in SharePoint Designer 2013 definierte Workflows) werden zur Verarbeitung an Workflow-Manager-Client 1.0 ausgelagert. Workflow-Manager-Client 1.0 kann auf einem separaten Server in der SharePoint-Farm, unter Microsoft Azure in der Cloud oder zu Test- oder Demonstrationszwecken auf einem einzelnen Computer mit Project Server ausgeführt werden. Codierte Workflows, die mit Visual Studio 2012 entwickelt wurden, werden in der Workflowlaufzeit in SharePoint verarbeitet, so wie auch in Project Server 2010. Weitere Informationen finden Sie unter [Erste Schritte beim Entwickeln von Project Server-Workflows](getting-started-developing-project-server-workflows.md).
    
- **Umkreisnetzwerk (DMZ):** In Abbildung 3 ist nicht dargestellt, dass ein lokaler WFE-Server von einer zusätzlichen Firewall in einem Umkreisnetzwerk (auch als demilitarisierte Zone oder DMZ bezeichnet) isoliert werden kann. Ein Umkreisnetzwerk kann Internetclients den Zugriff auf SharePoint und Project Server über eine Firewall erlauben. 
    
- **SharePoint-Webdienste:** In der Abbildung 3 ist nicht die SharePoint-Infrastruktur dargestellt, z. B. die Back-End-SharePoint-Webdiensteanwendung, die Teil von SharePoint Server 2013 ist. Wenn Sie Project Server installieren, wird die Project-Dienstanwendung den SharePoint-Webdiensten hinzugefügt. 
    
Die Front-End-Ebene umfasst Drittanbieteranwendungen, Project Professional und Project Web App. Ein Browser zeigt ASP.NET 4.0-Seiten (ASPX-Seiten) in Project Web App an. Die Project Web App-Seiten verwenden Project Server-Webparts, die mit der PSI kommunizieren und Standard-SharePoint-Webparts verwenden. 
  
Die mittlere Schicht umfasst das PSI und die Geschäftsobjektschicht, die aus logischen Objekten besteht, die Project Server-Geschäftsentitäten repräsentieren. Zu den Geschäftsentitäten zählen u. a. "Project", "Task", "Resource" und "Assignment". Das PSI und die Geschäftsobjektschicht sind eng miteinander gekoppelt und befinden sich auf demselben Server. Eine Clientanwendung ruft das PSI über eine der verfügbaren Schnittstellen auf, und das PSI ruft daraufhin Geschäftsobjekte auf. Für eine optimierte Leistungsfähigkeit bezieht das WFE von Project Server 2013 einige Geschäftsobjekte in Anforderungen ein, die nicht das Warteschlangensystem von Project Server verwenden oder den Dienst für Project-Berechnungen erfordern. Die WFE-Geschäftsobjekte kommunizieren direkt mit der Project-Datenbank.
  
Die Project Web App-Komponenten von Project Server verwenden die SharePoint 2013-Konfigurationsdatenbank für die Einrichtung von Projektwebsites und die Inhaltsdatenbank für Projektwebsite-Inhalte, wie Aufgabenlisten, benutzerdefinierte Seiten, Workflows, Verwaltungseinstellungen, Dokumente sowie Listen von Problemen, Risiken und Zusicherungen. Die SharePoint-Konfigurations- und -Inhaltsdatenbanken unterstützen weitere Funktionen für das Projektmanagement, wie Projektvorlagen und -arbeitsbereiche, benutzerdefinierte Listen für die Teamzusammenarbeit sowie Berichte.
  
### <a name="project-web-app-and-the-wfe"></a>Project Web App und das WFE
<a name="pj15_Architecture_PWAServer"> </a>

Sie können mehrere Project Web App-Instanzen auf einem WFE und mehrere WFE-Server innerhalb eines Unternehmensintranets konfigurieren, um eine optimale Lastverteilung für Intranet-Clients zu ermöglichen. Wenn eine Client-Anwendung eine Project Web App-Instanz auf einem separaten WFE-Server verwendet, werden PSI-Aufrufe über die PSI-Weiterleitung geleitet. Die PSI-Weiterleitung (entweder WCF-Weiterleitung oder Webdienst-Weiterleitung) führt die folgenden Funktionen aus:
  
- Optimiert Aufrufe von Remoteclients an das PSI.
    
- Unterscheidet zwischen PSI-Aufrufen, die den Project Server-Warteschlangendienst erfordern, und Aufrufen, für die kein Warteschlangendienst erforderlich ist. Die Bezeichnungen von asynchronen PSI-Methoden beginnen mit "Queue", wie **QueueCreateProject**.
    
- Ermittelt PSI-Aufrufe, die registrierte lokale Ereignishandler aufrufen.
    
- Ermittelt PSI-Aufrufe, die den Dienst für Project-Berechnungen erfordern.
    
- Verwendet einen serverbasierten Cache, der gemeinsam mit dem clientseitigen aktiven Cache in Project Professional umlaufende Aufrufe an Project Server reduziert.
    
Nachdem ein SharePoint-Server einen Project Server-Benutzer authentifiziert hat, sendet die PSI-Weiterleitung transparente Anforderungen, die Back-End-Dienste verwenden, an die PSI-Dienste auf dem Computer, auf dem Project Server ausgeführt wird. Anforderungen, für die keine Back-End-Dienste erforderlich sind, werden an die Geschäftsobjekte in der lokalen Project Web App-Instanz gesendet. Die PSI-Weiterleitung verbessert die Skalierbarkeit, Leistungsfähigkeit und Zuverlässigkeit der Project Server-Verarbeitung über das LAN, ein WAN und in Project Online.
  
Project Web App wird mit ASP.NET 4.0 entwickelt. Die visuellen Elemente in ASPX-Dateien (HTML, Serversteuerelemente und statischer Text) werden getrennt von der Programmierlogik in CodeBehind-Klassen realisiert, die sich in kompilierten Assemblies (DLL-Dateien) befinden. Websiteseiten in Project Web App wie die Seite der obersten Ebene, Project Center und Report Center, können anhand von Webparts angepasst werden. Anwendungsseiten, die im Menü **Websiteaktionen** nicht über die Option **Seite bearbeiten** verfügen, können nicht bearbeitet werden. Dazu zählen die Seite "Servereinstellungen" und die Seite "Arbeitszeittabelle überprüfen". 
  
### <a name="the-csom-and-the-project-server-interface"></a>Das CSOM und das Project Server Interface
<a name="pj15_Architecture_PSI"> </a>

Das PSI umfasst 22 öffentliche Dienste wie **Project**, **Resource**, **CustomField** und **Statusing**. Das PSI enthält auch sieben private Dienste für die interne Verwendung. Das PSI ist die grundlegende API von Project Server. Es macht die Project Server-Funktionen für das CSOM und für externe Anwendungen verfügbar. Das CSOM umfasst Klassen, die auf die häufig verwendeten PSI-Klassen und -Elemente zugreifen, die von Drittanbieteranwendungen verwendet werden. In Project Server 2013 sind einige Project Server-Funktionen wie die Dienste **Admin**, **Calendar**, **PortfolioAnalyses** und **Security** nicht im CSOM verfügbar. 
  
Project Professional 2013 und Project Web App verwenden das PSI, um auf Project Server-Daten in den Entwurfstabellen und -ansichten, veröffentlichten Tabellen und Ansichten sowie den Archivtabellen und -ansichten der Project-Datenbank zuzugreifen. Sie können über eine Proxy-Datei oder ein Proxy-Assembly für WCF-Dienste oder die ASMX-Webdienste auf den PSI-Dienst zugreifen.
  
> [!NOTE]
> Das CSOM ist die bevorzugte Schnittstelle für Project Server-Entwickler von Drittanbietern. Es kann für Anwendungen verwendet werden, die sowohl auf eine lokale Project Server-Installation als auch auf Project Online zugreifen. Wir empfehlen, dass Sie für die Entwicklung neuer Anwendungen das CSOM verwenden, sofern das CSOM alle für Ihre Anwendung erforderlichen Funktionen umfasst. 
  
Einige Branchenanwendungen und andere Drittanbieteranwendungen, die für Project Server 2010 entwickelt wurden, erfordern PSI-Dienste, die noch nicht im CSOM enthalten sind. Wenn derartige Anwendungen nur für lokale Project Server-Installationen bestimmt sind, können diese weiterhin die WCF- oder ASMX-Schnittstelle des PSI verwenden.
  
Clientanwendungen rufen das PSI über Dienstproxies auf. Clients, die die WCF-Webdienstschnittstelle verwenden, greifen über `https://ServerName/ProjectServerName/_vti_bin/psi/ProjectServer.svc` auf alle PSI-Dienste zu. Clients, die eine ASMX-Webdienstschnittstelle verwenden, nutzen die Project Web App-URL für den jeweiligen Dienst. Der Dienst **Resource** ist z. B. über `https://ServerName/ProjectServerName/_vti_bin/psi/resource.asmx?wsdl` verfügbar. Wenn Anwendungen keinen Intranetzugriff auf Project Server haben, können sie einen Project Web App-Server in einem Umkreisnetzwerk verwenden (in Abbildung 3 nicht dargestellt).
  
Abbildung 4 zeigt den Bereich **Verbindungen** im **Internetinformationsdienste (IIS)-Manager** für eine Installation von SharePoint Server 2013, Project Server 2013 und einer lokalen Workflowverwaltungswebsite für Workflow-Manager-Client 1.0 auf einem einzelnen Server. Die SharePoint-Websitesammlung (A) umfasst die Front-End-PSI-Dienste im virtuellen Unterverzeichnis `_vti_bin\PSI`. Die SharePoint-Webdienstanwendung (B) umfasst die Project-Dienstanwendung mit den Back-End-PSI-Diensten im virtuellen Unterverzeichnis `508c23fb7dfd4c83a8919fae24bc68c5/PSI`. Bei der GUID handelt es sich um den Namen der Project-Dienstanwendungsinstanz für diese Project Server-Installation. 
  
**Abbildung 4. Front-End-PSI (A) und Back-End-PSI (B) in IIS-Manager**

![Das Front-End- und das Back-End-PSI](media/pj15_Architecture_PSI_IIS.gif "Das Front-End- und das Back-End-PSI")
  
Clientanwendungen können nicht direkt auf WCF-Dienste für das PSI in der Back-End-Project-Dienstanwendung zugreifen. Wenn für die Clientanwendungen und Komponenten der Branchenanwendungen kein Zugriff auf Project Online erforderlich ist, können diese Proxies für das PSI verwenden. Eine Back-End-URL für die WCF-Schnittstelle des Dienstes **Resource** in Abbildung 4 wäre z. B. `https://ServerName:32843/508c23fb7dfd4c83a8919fae24bc68c5/psi/resource.svc`. Port 32843 ist der Standard-HTTP-Port für die SharePoint-Webdienstanwendung (32844 ist der Port für die HTTPS-Kommunikation). Jedoch sperrt die Datei "web.config" für Project Web App den direkten Zugriff auf Back-End-PSI-Dienste.
  
> [!NOTE]
> Der Project 2013-SDK-Download umfasst PSI-Proxydateien für die WCF- und ASMX-Dienste sowie Anweisungen für das Kompilieren der Dateien in Proxy-Assemblies. > Um aktualisierte PSI-Proxydateien zu erstellen, die die WCF-Schnittstelle verwenden, müssen Sie das Hilfsprogramm "svcutil.exe" oder Visual Studio direkt auf dem Project Server-Computer verwenden. 
  
Elemente des PSI-Dienstes generieren oder verarbeiten in der Regel typisierte **DataSet**-Objekte, um Informationen mit Geschäftsobjekten auszutauschen. Des Weiteren gibt es mehrere verschiedene Modelle für die PSI-Entwicklung. So verwenden z. B. die PSI-Dienste **Resource**, **CustomFields** und **LookupTable** XML-Filterobjekte für die **DataSet**-Manipulation und andere Dienste nicht. Einige Methoden im Dienst **Statusing** verwenden einen _changeXml_-Parameter, während dies bei anderen Methoden und Diensten nicht der Fall ist. Das CSOM verwendet keine DataSets. Obwohl das CSOM ein anderes Programmiermodell als das PSI aufweist und Sie entweder .NET-Assemblys oder JavaScript verwenden können, ist die Entwicklung mit dem CSOM in der Regel einfacher und konsistenter als die Entwicklung mit dem PSI. 
  
Weitere Informationen zur PSI finden Sie unter [Übersicht über die Project PSI-Referenz](project-psi-reference-overview.md). Weitere Informationen zum CSOM finden Sie unter [Clientsseitiges Objektmodell (CSOM) für Project 2013](client-side-object-model-csom-for-project-2013.md).
  
### <a name="business-objects-in-the-wfe-and-the-project-service-application"></a>Geschäftsobjekte im WFE und die Project-Dienstanwendung
<a name="pj15_Architecture_BusinessObjects"> </a>

Das interne Objektmodell von Project Server umfasst die Geschäftsobjekte, die logische Entitäten wie "Project" und "Resource" repräsentieren. Client-Anwendungen greifen ausschließlich über das CSOM oder das PSI auf Geschäftsobjekte zu. Geschäftsobjekte wiederum greifen auf die Entwurfstabellen und -ansichten, veröffentlichten Tabellen und Ansichten sowie die Archivtabellen und -ansichten der Project-Datenbank zu.
  
Geschäftsobjekte sind für Drittanbieterentwickler nicht zugänglich. Das PSI verwaltet die Zuordnung des API zu den Geschäftsobjekten, und das CSOM ordnet sein API dem PSI zu. Die logischen Entitäten von Geschäftsobjekten können in drei Typen unterteilt werden:
  
- **Kernentitäten** sind Objekte wie Projekte, Aufgaben, Aufträge, Ressourcen und Kalender. Die Kernentitäten umfassen grundlegende Bestandteile der Geschäftslogik wie Berechtigungen und Benennungsregeln. 
    
- **Geschäftsentitäten** sind Objekte wie Arbeitszeittabellen, Projektportfolios und Modelle. Geschäftsentitäten umfassen weiterreichende Bestandteile der Geschäftslogik und werden in der Regel durch die Kombination von Kernentitäten gebildet. 
    
- **Unterstützende Entitäten** sind u. a. Objekte für die Sicherheit und Validierung. 
    
In Project Server 2010 werden alle Geschäftsobjekte in der Project-Dienstanwendung implementiert. In Project Server 2013 hostet das WFE viele der Geschäftsobjekte, die synchrone Methoden verarbeiten und nicht den Dienst für Project-Berechnungen erfordern. Synchrone PSI-Methoden wie **DeleteProject** und **ReadAssignments** verwenden nicht den Project Server-Warteschlangendienst. Die Bezeichnungen von asynchronen Methoden im PSI beginnen mit `Queue` wie **QueueCreateProject** und **QueueUpdateTimesheet**. Eine asynchrone Methode sendet eine Nachricht an den Project Server-Warteschlangendienst, der die Verarbeitung der Methode plant, während die Kontrolle wieder an den Benutzer übergeben wird.
  
Die PSI-Weiterleitung bestimmt, welche Anforderungen an die Project-Dienstanwendung gesendet werden und welche Anforderungen von den Geschäftsobjekten im WFE verarbeitet werden können. Die Geschäftsobjekte im WFE umgehen die Project-Dienstanwendung und haben direkten Zugriff auf die Project-Datenbank, ganz ähnlich wie es bei SharePoint-Prozessen in einem WFE der Fall ist, die direkt auf die Konfigurations- und Inhaltsdatenbanken zugreifen. Je mehr Geschäftsobjekte auf dem WFE ausgeführt werden, umso höher ist die Effizienz von Project Server, umso mehr wird die Anwendungsschicht entlastet und umso besser kann Project Server für eine steigende Arbeitsauslastung skaliert werden.
  
> [!NOTE]
> In Project Server 2013 müssen für das WFE und den Back-End-Project-Server-Computer lokale Ereignishandler bereitgestellt werden. 
  
### <a name="project-server-database"></a>Project Server-Datenbank
<a name="pj15_Architecture_DAL"> </a>

In Project Server 2013 wurden die vier Project Server-Datenbanken der früheren Versionen zu einer Project-Datenbank in SQL Server zusammengelegt. Der Standardname der Project-Datenbank ist "ProjectService". Die Berichtstabellen und -ansichten werden wie gewohnt mit dem Präfix `dbo` benannt wie "dbo.MSP_EpmProject" und "dbo.MSP_EpmProject_UserView". Tabellen und Ansichten die in früheren Versionen in der Entwurfsdatenbank gespeichert waren, werden mit dem Präfix `draft` benannt. Tabellen und Ansichten aus der veröffentlichten Datenbank tragen das Präfix `pub`. Tabellen und Ansichten aus der Archivdatenbank haben das Präfix `ver`. 
  
> [!IMPORTANT]
> Der direkte Zugriff wird nicht unterstützt für die Entwurfstabellen und -ansichten (Präfix `draft`), die veröffentlichten Tabellen und Ansichten (Präfix `pub`) sowie die Archivtabellen und -ansichten (Präfix `ver`). Berichte sollten nur die Berichtstabellen und -ansichten mit dem Präfix `dbo` verwenden. 
  
Project Server-Daten werden wie folgt in der Project-Datenbank aufgeteilt:
  
- Die Entwurfstabellen und -ansichten enthalten Daten von unveröffentlichten Projekten, die von Project Professional und anderen Anwendungen erstellt wurden. Project Web App zeigt keine Projektdaten aus Entwurfstabellen und -ansichten an.
    
- Die veröffentlichten Tabellen und Ansichten enthalten alle veröffentlichten Projekte und Enterprise-Ressourcen, globale Daten für Enterprise-Projekttypen (EPTs) sowie weitere Projektvorlagen. Veröffentlichte Projekte werden in Project Web App angezeigt. Die veröffentlichten Daten umfassen auch Tabellen, die spezifisch für Project Web App sind (Arbeitszeittabellen, Modelle, Ansichten usw.), sowie globale Datentabellen (benutzerdefinierte Felder, Nachschlagetabellen, Project Server-Autorisierungsberechtigungen und Metadaten).
    
- In Archivdaten werden Sicherungsversionen von Projekten, Ressourcen, benutzerdefinierten Felder und weiteren Daten gespeichert.
    
- Die Berichtsdaten können für den schreibgeschützten Zugriff in Drittanbieteranwendungen sowie für Berichte verwendet werden. Project Server-OLAP-Cubes verwenden Berichtsansichten mit dem Suffix `_OlapView`. OLAP-Cubes sind in einer lokalen Project Server-Installation verfügbar, aber nicht in Project Online. 
    
    Berichtsdaten sind sehr umfangreich und werden nahezu in Echtzeit aktualisiert. Die Berichtstabellen und -ansichten sind für die Generierung von schreibgeschützten Berichten optimiert. So sind Berichtstabellen z. B. denormalisiert, um redundante Daten zu ermöglichen und die Anzahl relationaler Tabellen zu reduzieren.
    
Logische Entitäten wie "Resource" oder "Project" können sich über mehrere Tabellen erstrecken, und alle Tabellen für eine bestimmte Entität haben denselben Primärschlüssel. Der Primärschlüssel ist eine GUID in einer einzelnen Spalte, die eine Instanz einer bestimmten Entität eindeutig kennzeichnet.
  
Project Server-Daten werden für jede Instanz von Project Web App in einer separaten Project-Datenbank mit jeweils unterschiedlichem Namen gespeichert. Clientanwendungen, die direkten Zugriff auf Project Server haben, können die Berichtstabellen und -ansichten direkt lesen. Bei Remote-Zugriff können die Client-Anwendungen das OData-Interface und das REST-Interface verwenden, um Daten für Berichte abzurufen. Clients sollten nur das CSOM oder das PSI verwenden, um auf Entwurfstabellen und -ansichten, veröffentlichte Tabellen und Ansichten sowie Archivtabellen und -ansichten zuzugreifen. Der Berichtsdatendienst (in Abbildung 3 nicht dargestellt) aktualisiert die Berichtsdaten von veröffentlichten Daten nahezu in Echtzeit. Die Project-Datenbank kann sich auf einem separaten Server befinden.
  
Schemas werden nur für die Berichtstabellen und -ansichten dokumentiert. Bei einer lokalen Project Server-Installation können Sie Berichtstabellen und -ansichten für Entitäten hinzufügen, die nicht im Schema der Project-Datenbank definiert sind. Sie können auch separate Datenbanken für benutzerdefinierte Anwendungen vor Ort erstellen. Änderungen an den Entwurfstabellen und -ansichten, veröffentlichte Tabellen und Ansichten sowie Archivtabellen und -ansichten werden nicht unterstützt. Da nicht direkt in Project Online auf die Project-Datenbank zugegriffen werden kann, können Berichtstabellen und -ansichten nicht geändert werden. Wenn Sie jedoch über ein SQL Azure-Konto verfügen, können Sie separate Datenbanken für die benutzerdefinierte Verwendung erstellen Project Online.
  
### <a name="event-receivers"></a>Ereignisempfänger
<a name="pj15_Architecture_EventHandlers"> </a>

Lokale Ereignishandler und Remoteereignisempfänger für Project Server ermöglichen eine Drittanbieter-Erweiterbarkeit und die Reaktion auf Project Server-Ereignisse wie das Erstellen oder Veröffentlichen eines Projekts. In Project Server 2010 sind alle Ereignishandler lokal und werden in voll vertrauenswürdigem Code geschrieben. Des Weiteren werden sie direkt auf dem Computer bereitgestellt, auf dem Project Server ausgeführt wird, sowie auf den WFEs, und sie werden innerhalb des Project Server-Ereignissystems ausgeführt. Da Project Online keine voll vertrauenswürdigen Ereignishandler unterstützt, implementiert Project Server 2013 Remoteereignisempfänger, die den Remote-Ereignisempfängern in SharePoint Server 2013 ähneln. Eine lokale Installation von Project Server 2013 unterstützt herkömmliche, voll vertrauenswürdige Ereignishandler und Remoteereignisempfänger.
  
Ein Project Server-Remoteereignisempfänger kann in einem benutzerdefinierten Webdienst implementiert werden, mit einem SOAP-Endpunkt, der in Microsoft Azure oder in anderen Umgebungen ausgeführt wird, die SOAP-Webdienste unterstützen. Ein Project Server-App-Paket kann Remoteereignisempfänger einbeziehen, die mit der App installiert werden.
  
Remoteereignisempfänger können Aufrufe über CSOM-Endpunkte (in Abbildung 3 nicht dargestellt) zurück an Project Server senden. Der Aufruf an einen Remoteereignisempfänger umfasst Informationen von dem Project Server-Ereignissystem und der Project Web App-Instanz (oder vom Project Web App-Mandanten in Project Online), das bzw. die den Aufruf gesendet hat. Mit Remoteereignisempfängern können Sie einen einzelnen Webdienst erstellen und hosten, der von mehreren Project Server-Installationen verwendet werden kann. Im Gegensatz dazu müssen lokale, voll vertrauenswürdige Ereignishandler für jede Project Server-Installation einzeln bereitgestellt werden.
  
### <a name="publishing-and-server-side-scheduling"></a>Veröffentlichung und serverseitige Zeitplanung
<a name="pj15_Architecture_PublishingScheduling"> </a>

Project Server 2013 unterstützt sowohl die manuelle als auch die automatische Aktualisierung von Projektplänen. Der Standardprozess ist die manuelle Aktualisierung. Das bedeutet, der Projektmanager checkt ein Projekt in Project Professional oder Project Web App aus, öffnet es, übernimmt die Änderungen, speichert das Projekt und veröffentlicht es, um die Änderungen allen Beteiligten verfügbar zu machen. Project Professional verfügt über ein Planungsmodul, das Änderungen berechnet und die Änderungen anschließend in Project Server speichert. Das in Project Server 2010 implementierte serverseitige Planungsmodul unterscheidet sich von dem Planungsmodul in Project Professional.
  
In Project Server 2013 implementiert der Dienst für Project-Berechnungen dasselbe Planungsmodul wie in Project Professional 2013. Der Dienst für Project-Berechnungen wird in einem Windows-Dienst namens **Microsoft Project Server-Berechnungsdienst** ausgeführt. Das Ändern eines Projektplans in Project Web App oder mit Drittanbieteranwendungen, die das CSOM verwenden, bewirkt exakt dieselben Planänderungen, die auch in Project Professional implementiert würden.
  
> [!NOTE]
> Bei Drittanbieteranwendungen, die das PSI verwenden, weicht die Planung möglicherweise geringfügig von den in Project Web App berechneten Plänen ab. Um eine Abwärtskompatibilität zu gewährleisten, verwenden die öffentlichen PSI-Methoden, die für die serverseitige Planung verantwortlich sind, weiterhin das Planungsmodul, das mit Project Server 2010 eingeführt wurde. Eine Ausnahme hierbei ist die Methode **QueueUpdateProject2**, wobei es sich um eine neue PSI-Methode in Project Server 2013 handelt. Das frühere Planungsmodul plant z. B. keine Unterprojekte oder Verknüpfungen zu anderen Projekten und berechnet keine Ertragswertfelder. Um mögliche Planungsabweichungen zwischen Drittanbieteranwendungen und Project Professional oder Project Web App zu vermeiden, sollten Sie nach Möglichkeiten Anwendungen mit dem CSOM entwickeln. 
  
Project Server ermöglicht es anhand der folgenden Schritte, dass die veröffentlichte Version aktualisiert werden kann, während ein Projektmanager die Entwurfsversion verwendet:
  
1. Project Server übernimmt Aktualisierungen und plant die veröffentlichte Version neu.
    
2. Project Server speichert die Aktualisierung, um sie in die Entwurfsversion zu implementieren, wenn eines der folgenden Ereignisse eintritt:
    
   - Project Professional öffnet das Projekt.
    
   - Project Professional versucht, das Projekt zu veröffentlichen.
    
3. Bei einem Konflikt wird der Projektmanager benachrichtigt und muss den Konflikt beheben, damit die Entwurfsversion veröffentlicht werden kann.
    
## <a name="see-also"></a>Siehe auch

- [Übersicht über Project 2013 für Entwickler](https://msdn.microsoft.com/library/8da91ab0-af4f-429f-8241-490600e3f7bd%28Office.15%29.aspx)
- [Project Server-Programmierbarkeit](project-server-programmability.md)  
- [Clientseitiges Objektmodell (CSOM) für Project 2013](client-side-object-model-csom-for-project-2013.md)  
- [Was das PSI durchführen kann und was nicht](what-the-psi-does-and-does-not-do.md)  
- [Erste Schritte beim Entwickeln von Project Server-Workflows](getting-started-developing-project-server-workflows.md)   
- [Übersicht über die Project PSI-Referenz](project-psi-reference-overview.md)   
- [Open Data Protocol](https://www.odata.org/)
    

