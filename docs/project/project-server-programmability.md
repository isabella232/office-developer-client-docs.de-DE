---
title: Project Server-Programmierbarkeit
manager: soliver
ms.date: 09/17/2015
ms.audience: Developer
f1_keywords:
- events
- PDS
- PDS compatibility
- Project Server databases
- Project Server events
- Project Server Interface
- Project Server workflow
- Project workflow
- PSI
- PSI limitations
- PSI uses
- SharePoint Services
- WF
- workflow
- Workflow Foundation
- WSS
keywords:
- Project 2013, Architektur und Programmierbarkeit, PSI, Projekte, Versionen Programmierbarkeit, Project Server, PSI, Einschränkungen, Project Server Interface nicht unterstützter Features, Project Server Interface PDS Kompatibilität, Project Server Interface, generische Project Server, project Versionen, Versionen, Projekte, Project Server, Project 2013-Datenbanken-Plattform, Project Server Interface, verwenden Sie Szenarien, Project Server-Ereignisse, Project Server, Project Data Service, Kompatibilität mit PSI, Project Server Benutzeroberfläche
localization_priority: Normal
ms.assetid: a93d2153-5132-4289-af51-69350471e248
description: Informationen Sie zu den wichtigsten Programmierbarkeitsfeatures in Project Server 2013. Dieser Artikel enthält Informationen zum Portieren von Anwendungen, die für frühere Versionen von Project Server erstellt wurden.
ms.openlocfilehash: 57802cf8ce1597b759201ef1e2a0ea9bd1e394b1
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/04/2018
ms.locfileid: "25386733"
---
# <a name="project-server-programmability"></a>Project Server-Programmierbarkeit

Informationen Sie zu den wichtigsten Programmierbarkeitsfeatures in Project Server 2013. Dieser Artikel enthält Informationen zum Portieren von Anwendungen, die für frühere Versionen von Project Server erstellt wurden.

Projektserver 2013 unterstützt die meisten Anwendungen, die für Project Server 2010 und neue Lösungen für mehrere Plattformen, wobei apps beide online zugreifen können und lokalen Project Server-Installationen entwickelt wurden. Anwendungen und Erweiterungen, die für Project Server 2003 oder früher entwickelt wurden müssen neu gestaltet, um die Client-seitigen Objektmodell (CSOM) oder die Project Server Interface (PSI) verwenden. Anwendungen, die für Office Project Server 2007 oder Project Server 2010 entwickelt wurden, erfordern einige Änderungen und erneut kompiliert, um die PSI zu verwenden; um die CSOM verwenden, erfordern Anwendungsbereiche eine Umgestalten.
  
Die Project Server-Plattform ermöglicht hohe Programmierproduktivität auf Grundlage von SharePoint Server 2013, .NET Framework 4 und dem OData-Protokoll mit dem Clientobjektmodell. Entwickler können Erweitern von Project Web App mit apps, app-Webparts und Webparts, Definieren von Workflows mithilfe von SharePoint Designer 2013 und Durchsetzen von Geschäftsregeln mit remote-Ereignisempfänger für Project Server-Ereignisse.
  
## <a name="project-server-and-sharepoint-server"></a>Projektserver und SharePoint Server
<a name="pj15_Programmability_MOSS"> </a>

Project Web App basiert auf SharePoint Server 2013 und verwendet Gestaltungsvorlagen und Webparts um zu erleichtern, benutzerdefinierte apps und Project Web App-Lösungen zu erstellen. Projektserver 2013 integriert tief als Plattform für die Zusammenarbeit an einem Projekt, reporting, Site-Verwaltung, Sicherheit und Verwalten von Workflows mit SharePoint Server 2013.
  
Die Projektwebsites enthalten weitere Informationen und Optionen für die Zusammenarbeit für Teammitglieder, in dem Sie Standard-apps, die ein Projekt enthalten zusammenfassende, spezielle SharePoint-für Aufgaben mit einem Zeitachsen, Verfolgen von Problemen, Risiken hinzufügen können Listen, Lieferumfang, project und die zusammen mit der Dokument-Bibliothek und Team Diskussionen Teamkalender. Benutzerdefinierte apps für Project Server 2013 bieten Erweiterungen und Flexibilität für die Teamzusammenarbeit. Sie können auch app-Webparts zum Anpassen einer app mit denselben Mechanismus zum Hinzufügen und Bearbeiten von Webparts beim Bearbeiten einer Seite hinzufügen. Sie können Projektwebsites an einer beliebigen Stelle innerhalb der SharePoint-Farm suchen, auf dem Project Server installiert ist. Verwendung von anderen Basisdienste von SharePoint Server 2013, wie Excel Services und Suche in Unternehmen, kann ein Administrator aktivieren und Konfigurieren der Dienste. 
  
Bei der Installation von Project Server 2013 bereitgestellt die Project Service-Anwendung in der SharePoint-Webdienste-Website. Die Project Service-Anwendung enthält die lokalen Windows Communication Foundation (WCF) und ASMX-Webdienste für die PSI. Weitere Beispiele für dienstanwendungen sind SharePoint-Suche und SharePoint-Dokumentverwaltung. Weitere Informationen finden Sie unter der Entwicklerdokumentation für SharePoint Server 2013.
  
Die Project Service-Anwendung ist eine logische Dienstanbieter, der mehrere Instanzen von Project Web App verwalten können. Project Server-Bereitstellung wird eine bestimmte Project Web App-Website in einer SharePoint-Webanwendung erstellt. Die Homepage der Project Web App enthält Links zu der Seite Projektcenter, Resource Center-Seite und der Business Intelligence Center-Seite für die berichterstellung sowie eine Seite, die eine Liste der zusätzlichen standard apps enthält. Abbildung 1 zeigt den Befehl **Seite bearbeiten** in der **ProxyeinstellungenGehen** Dropdown-Liste auf der Homepage der Project Web App, wodurch Sie zum Hinzufügen oder Bearbeiten von Webparts. 
  
> [!NOTE]
> Einige administrativen Seiten in Project Web App – beispielsweise die Seite PWA-Einstellungen – können nicht bearbeitet werden, und den Befehl **Seite bearbeiten** nicht anzeigen. Bearbeiten von Seiten mithilfe von SharePoint Designer 2013 ist in Project Web App nicht zulässig. Sie können Project von Webseiten mit SharePoint Designer 2013 bearbeiten. 
  
**Abbildung 1. Verwenden das Menü Seite bearbeiten in Project Web App**

![Bearbeiten der Startseite in Project Web Access] (media/pj15_Programmability_PWAHome.gif "Bearbeiten der Startseite in Project Web Access")
  
Wählen Sie Zugriff auf die Seite Websiteeinstellungen in Project Web App das Symbol **Einstellungen** in der oberen rechten Ecke der Seite. Die Seite Websiteeinstellungen ( `https://ServerName/ProjectServerName/_layouts/15/settings.aspx`) ermöglicht das Ändern des Erscheinungsbilds und das Websitedesign, benutzerdefinierte Webparts hinzufügen und ändern oder Erstellen von Masterseiten für Projektwebsites.
  
Anpassung des Codes in ASPX-Seiten oder Anpassung von Gestaltungsvorlagen mit SharePoint Designer 2013, Project Web App wird nicht unterstützt. Anpassung des Codes in Project Web App-Seiten kann Probleme mit Project Server-Updates und Servicepacks. 
  
### <a name="customization-of-project-web-app-with-sharepoint-packages"></a>Anpassung von Project Web App mit SharePoint-Lösungspaketen
<a name="pj15_Programmability_CustomizationOfPWA"> </a>

Da Project Web App eine SharePoint-Anwendung ist und Projektwebsites SharePoint-Websites sind, können Sie mithilfe von SharePoint-Lösungspaketen (WSP-Dateien) oder SharePoint-apps (.spapp-Dateien) benutzerdefinierte apps, Webparts, Ereignishandler, benutzerdefinierte Felder und andere Features hinzufügen. Ein SharePoint-Paket oder ein app-Paket kann mehrere Project Server-Entitäten enthalten, in denen Entitätsdefinitionen in einer elements.xml-Datei, in dem Paket angegeben werden.
  
Für Project Online Hinzufügen von Schaltflächen im Menüband von Project Web App, aber Sie nicht entfernen oder Umbenennen von vorhandenen Produkt Schaltflächen und neue Registerkarten auf dem Menüband kann nicht erstellt werden. Weitere Informationen finden Sie unter [Erstellen benutzerdefinierter Aktionen zur Bereitstellung mit apps für SharePoint](https://msdn.microsoft.com/library/office/apps/jj163954%28v=office.15%29.aspx).
  
> [!CAUTION]
> Wenn Sie ein SharePoint-Paket oder ein app-Paket installieren, müssen die Typen von Project Server-Entitäten werden in der Reihenfolge, dass das Schema PSEntityProvision.xsd angibt oder nicht Überprüfung des Pakets Schema erfolgreicher und Installation ist nicht abgeschlossen. 
  
Die Schemadatei PSEntityProvision.xsd ist in der Project 2013-SDK-Download verfügbar in den `Documentation\Schemas\AppProvisioning` Unterverzeichnis. Abbildung 2 zeigt die XML-Schema Explorer-Ansicht in Visual Studio des **PSEntityProvision** -Schemas, auf dem die **LookupTable** -Sequenz erweitert ist. 
  
**Abbildung 2. Visual Studio-Ansicht der Project Server-Entität Schema-Bereitstellung**

![Überblick über die Project Server-Entitätsschemas] (media/pj15_Programmability_EntitySchema.gif "Überblick über die Project Server-Entitätsschemas")
  
SharePoint-Pakete, die Features für Project Server installieren können eine oder mehrere elements.xml-Dateien enthalten, die das **PSEntityProvision** Schema entsprechen. Die Project Server-Entitäten in einer einzigen XML-Datei müssen in der folgenden Reihenfolge angezeigt werden: 
  
1. Workflowphasen
    
2. Nachschlagetabellen
    
3. Benutzerdefinierte Felder
    
4. Workflowstufen
    
5. Enterprise-Projekttypen
    
6. Ereignishandler
    
Beim Erstellen eines SharePoint-Pakets, das Project Server-Entitäten enthält, ist es möglich, die Entitätsdefinitionen in mehreren elements.xml Dateien zu platzieren. Jede XML-Datei konnte die Schema-Überprüfung übergeben, aber die Entitäten in die komplettes Leistungspaket möglicherweise nicht in der richtigen Reihenfolge. Beispielsweise könnte eine benutzerdefiniertes Feld Entität in die erste XML-Datei auf einer Nachschlagetabelle in der zweiten XML-Datei verweisen. Während der Installation kann das benutzerdefinierte Feld erstellt werden, da die Nachschlagetabelle noch nicht erstellt wurde.
  
Wenn eine Paketinstallation ein Fehler auftritt, Objekte, die erstellt wurden bleiben in Project Web App, aber das Paket wird nicht vollständig installiert. Installieren Sie das Paket arbeiten kann, aber das ist noch keine gute Erfahrung für Kunden. Wenn die Entitätsdefinitionen mehrere elements.xml Dateien umfassen, Organisieren Sie die Project Server-Entitäten in die gesamte SharePoint-Lösungspaket, um sicherzustellen, dass die Installation die richtige Reihenfolge folgt. Mit dem PSEntityProvision.xsd Schema in der Project 2013-SDK-Download ist es möglich, ein Tool entwickeln, die der vorgeschriebenen Reihenfolge von Entitäten in der XML-Dateien überprüft.
  
## <a name="upgrading-applications-with-the-project-server-apis"></a>Aktualisieren einer Anwendung mit der Project Server-APIs
<a name="pj15_Programmability_APIs"> </a>

Wenn Sie eine Anwendung, die für eine frühere Version von Project Server entwickelt wurde aktualisieren, können Sie auswählen, die CSOM oder die PSI für eine Programmierschnittstelle zu verwenden, Methoden zum Erstellen enthält, lesen, aktualisieren und Löschen von projektentitäten (CRUD-Vorgänge). Obwohl das CSOM intern die PSI anruft, wird nicht vollständig alle PSI-Methoden ersetzt. Szenarien und Einschränkungen von die PSI und die CSOM finden Sie unter [Was die PSI ist und nicht zu](what-the-psi-does-and-does-not-do.md) und [Was das CSOM ist und nicht zu](what-the-csom-does-and-does-not-do.md).
  
> [!NOTE]
> Wenn das CSOM die Funktionen, die Sie erforderlich sind enthält, wird empfohlen, verwenden Sie das CSOM-Anwendungen zu aktualisieren. Das CSOM ermöglicht, dass Anwendungen für lokalen und online Project Server 2013-Installationen verwendet werden soll. 
  
Wenn Ihre Anwendung hauptsächlich Daten von Project Server liest, können Sie die reporting Tabellen und Ansichten in der Project Server-Datenbank für eine lokale-Szenario verwenden. Wenn Sie beabsichtigen, die Anwendung mit Project Online verwenden, können Sie das OData-Protokoll für den **ProjectData** -Dienst verwenden, die lokalen und online-Zugriff auf die reporting-Daten bereitstellt. Weitere Informationen finden Sie unter [ProjectData - Projekt OData-Dienstverweises](https://msdn.microsoft.com/library/office/jj163015.aspx)
  
### <a name="using-the-psi"></a>Verwenden die PSI
<a name="pj15_Programmability_PSI"> </a>

Die PSI kann voll vertrauenswürdige Clientanwendungen, einschließlich Project Professional 2013, Project Web App und LOB-Anwendungen, Zugriff auf Project Server-Daten in einer Sharepointfarm. Die PSI wird erstellt und mit .NET Framework 4 verwendet und bietet Vorteile wie eine bekannte Entwicklungsumgebung mit integrierter Sicherheit, Fehlerbehandlung und Garbagecollection.
  
Der Zugriff auf die PSI erfolgt über WCF-Dienste oder ASMX-Webdienste. Die ASMX-Schnittstelle basiert auf WCF. Jede PSI-Dienst enthält die Basisklasse in der Regel mit CRUD-Methoden für Elemente innerhalb dieser Klasse. Elemente werden von verwandten **DataSet** -Klassen angegeben. Der Dienst **CustomFields** enthält beispielsweise die **CustomFields** -Klasse mit Methoden wie [CreateCustomFields2](https://msdn.microsoft.com/library/WebSvcCustomFields.CustomFields.CreateCustomFields2.aspx) . Daten für eine oder mehrere benutzerdefinierte Enterprise-Felder werden in der **CustomFieldDataSet**angegeben.
  
> [!NOTE]
> Die ASMX-Dienste Webschnittstelle der PSI ist in Project Server 2013 veraltet. Obwohl die ASMX-Schnittstelle noch verfügbar ist, neue Webanwendungen, die die PSI verwenden soll das WCF-Interface verwenden, oder wenn möglich, sollten neue Applications des CSOM verwenden, anstelle der PSI. Zukünftige Versionen von Project Server erfordern ein Upgrade der vorhandenen ASMX-basierte Anwendungen das WCF-Interface die PSI verwenden oder das CSOM verwenden. 
  
Es gibt 22 Public-, dokumentiert PSI-Dienste in der WCF-Schnittstelle und die ASMX-Schnittstelle dupliziert werden. Die PSI enthält auch acht private, nicht dokumentierte Dienste. Project Web App und Project Professional verwenden Sie die öffentlichen PSI-Dienste und die private PSI-Dienste. Die PSI wird im Allgemeinen entsprechend die Geschäftsobjekten umgerechnet. D. h., ist jede PSI-Methode mit einem Geschäftsobjekt wie **Kalender** oder **Ressource**zugeordnet. Die PSI ist die primäre Schnittstelle für die Business-Objekte. Da Business Layer wieder verwendbare Business Logic Komponenten bereitstellt, verwenden Sie verschiedene Anwendungen, die mit Project Server-Daten interagieren dieselbe Geschäftslogik.
  
PSI-Methoden, die asynchron mit Project Server interagieren haben Namen, die mit der **Warteschlange**beginnen. Jede PSI-Methode ist mit einer separaten-Schnittstelle implementiert, dass verwendet eine Data starke Typisierung. Die **QueueCreateProject** -Methode in den **Project** -Dienst wird beispielsweise den _Dataset_ -Parameter vom Typ **ProjectDataSet**akzeptiert. Die **ProjectDataSet** -Klasse wird von der **DataSet** -Typ abgeleitet. Geben Sie die Vervollständigung von .NET Framework und IntelliSense in Visual Studio-Hilfe zur Reduzierung von Fehlern bei der Entwicklung mit der PSI einchecken. Eine Einführung in die ausführliche Erläuterung PSI-Namespaces Klassen, Methoden, Eigenschaften, Ereignisse und verwandte Assemblys finden Sie unter [Project PSI-Referenz (Übersicht)](project-psi-reference-overview.md).
  
Projektserver 2013 verwendet die Behandlung von Ausnahmen von .NET Framework. Auf dem Server, am oberen Rand der PSI-Stapel werden alle Fehler protokolliert. Einige Fehler senden ein einfaches Berichts an den Client, wie etwa eine **SoapException** oder **FaultException** -Objekts für die WCF-Schnittstelle für die ASMX-Schnittstelle. Ausnahmen im Anwendungsereignisprotokoll aufgezeichnet werden können, und einige Fehler tragen auch einen detaillierten Bericht auf dem Server in den Ablaufverfolgungsprotokollen Unified Logging Service (ULS). 
  
Für lokale voll vertrauenswürdige Anwendungen ist auch die PSI erweiterbar. Sie können eine .NET Assembly mit einem Dienst hinzufügen, die neue Funktionalität bietet, verwendet die gleiche Sicherheitsinfrastruktur Project Server und Anrufe von anderen PSI-Methoden oder von PSI-Klassen erbt. PSI-Erweiterung kann auch die Business Logik und die Datenbank für die neue Funktionalität erforderliche zugreifen.
  
### <a name="using-the-csom"></a>Verwendung des CSOM
<a name="pj15_Programmability_CSOM"> </a>

Mit dem Clientobjektmodell können Sie apps entwickeln, die Zugriff auf Project Online oder einer lokalen Project Server 2013-Installation. Apps können in einem öffentlichen Office Store oder privaten app-Katalog verteilt werden. Das CSOM ist eine leicht zu bedienende API entworfen, die direkt verbraucht oder Daten enthält, anhand des Namens mit LINQ-Abfragen, statt die Daten durch Übergeben von Datasets und _ChangeXml_ -Parameter oder XML- _Filter_ -Parameter erstellen. Das CSOM implementiert die wichtigste Funktionen von Project Server Interface (PSI) für die primären Entitäten wie ** **Project**, **Vorgangs-**, **EnterpriseResource**und**. Das CSOM enthält viele zusätzliche Entitäten wie **benutzerdefiniertes**, **LookupTable**, **WorkflowActivities**, **Ereignishandler**und **QueueJob**, die andere allgemeine Project Server-Funktionen zu unterstützen.
  
Das CSOM kann durch Kopieren die folgenden Ressourcen auf Ihrem lokalen Entwicklungscomputer verwendet werden:
  
- Für die Entwicklung mit .NET Framework 4, kopieren Sie die `%ProgramFiles%\Common Files\Microsoft Shared\Web Server Extensions\15\ISAPI\Microsoft.ProjectServer.Client.dll` Assembly. 
    
  Dokumentation CSOM Klassen und Member finden Sie in den [Microsoft.ProjectServer.Client](https://msdn.microsoft.com/library/Microsoft.ProjectServer.Client.aspx) -Namespace. Beispiel-Anwendung finden Sie unter [Erste Schritte mit dem CSOM und .NET](getting-started-with-the-project-server-csom-and-net.md).
    
- Für Microsoft Silverlight-Entwicklung, kopieren Sie die `%ProgramFiles%\Common Files\Microsoft Shared\Web Server Extensions\15\TEMPLATE\LAYOUTS\ClientBin\Microsoft.ProjectServer.Client.Silverlight.dll` Assembly. 
    
- Informationen zum Entwickeln von apps für Windows Phone 8, kopieren Sie die `%ProgramFiles%\Common Files\Microsoft Shared\Web Server Extensions\15\TEMPLATE\LAYOUTS\ClientBin\Microsoft.ProjectServer.Client.Phone.dll` Assembly. 
    
- Um JavaScript für die Entwicklung von Web apps und apps für andere Geräte zu verwenden, kopieren Sie die `%ProgramFiles%\Common Files\Microsoft Shared\Web Server Extensions\15\TEMPLATE\LAYOUTS\PS.js` Datei und die `PS.debug.js` Datei. Ein Beispiel Web app finden Sie unter [Erste Schritte mit dem Project Server 2013 JavaScript-Objektmodell](getting-started-with-the-project-server-2013-javascript-object-model.md).
    
Das CSOM ruft intern die PSI; aus diesem Grund, wenn die PSI einen Auftrag nicht möglich ist, können Sie weder das CSOM. Einschränkungen von der CSOM finden Sie unter [Was das CSOM ist und nicht zu](what-the-csom-does-and-does-not-do.md) , und [Was die PSI enthält und nicht zu](what-the-psi-does-and-does-not-do.md). Weitere Informationen zum Entwickeln mit dem Clientobjektmodell finden Sie unter [Updates für Entwickler in Project 2013](updates-for-developers-in-project-2013.md) und [mithilfe der clientseitigen Objektmodell (CSOM) für Project 2013](client-side-object-model-csom-for-project-2013.md).
  
### <a name="porting-applications-built-for-project-server-2003"></a>Portieren entwickelte für Project Server 2003
<a name="pj15_Programmability_Porting2003"> </a>

In Project Server 2003 steht viel Daten und Funktionen nur mit Project Professional 2003 oder von direkten Datenbankzugriff. Die PSI, die in Project Server 2007 eingeführt wurde entfernt einen Großteil der diese Einschränkung. Im Gegensatz zu den Project Data Service (PDS) in Project Server 2003 bieten die PSI und dem Clientobjektmodell umfassende Schnittstellen zu den Geschäftsobjekten in Project Server.
  
Entwickelt für PDS Applications sind nicht kompatibel mit höheren Versionen von Project Server. Das CSOM und die PSI funktional gleichwertig sind für PDS bereit, jedoch PDS Methoden oder Parameter nicht übereinstimmen.
  
> [!NOTE]
> Da PDS Applications vollständig für Project Server 2013 neu gestaltet werden müssen, wird empfohlen, dass Sie das CSOM verwenden. 
  
Weitere Informationen zu PDS Kompatibilität und Richtlinien zum Portieren PDS-Erweiterungen für die PSI finden Sie unter [PDS Parität in PSI-Webdienste](https://msdn.microsoft.com/library/61a0b0c7-9b74-46d1-87ed-66ffdd8017f8%28Office.15%29.aspx).
  
### <a name="porting-applications-built-for-project-server-2007-and-project-server-2010"></a>Portieren entwickelte für Project Server 2007 und Project Server 2010
<a name="pj15_Programmability_Porting2007"> </a>

Die PSI in Project Server 2013 ist eine Obermenge von der PSI-Objektmodell in Office Project Server 2007 und Project Server 2010. Viele Clientanwendungen, die für die beiden vorherigen Versionen von Project Server weiterhin in, lokale voll vertrauenswürdige lokale Installationen von Project Server 2013. Die folgenden Arten von Anwendungen erfordern jedoch Updates oder Umgestalten:
  
- Verwenden Sie das CSOM für Anwendungen, die für die Verwendung mit Project Online angepasst werden.
    
- Verwenden Sie das CSOM für Anwendungen, die für die Verwendung auf mobilen Geräten angepasst und tablet-Computer.
    
- Verwenden Sie das CSOM für Anwendungen, die als apps in den Office Store oder privaten app-Katalog zur Verfügung stehen.
    
- Anwendungen, die projektterminierung zu ändern, verwenden Sie das CSOM oder ändern Sie die Anwendung die [QueueUpdateProject2](https://msdn.microsoft.com/library/WebSvcProject.Project.QueueUpdateProject2.aspx) PSI-Methode verwendet. 
    
- Lokale oder Webanwendungen, die sich auf die Benutzer auf verschiedene Instanzen von Project Web App anmelden sollten programmgesteuerte Einstellungen für das CSOM oder die PSI WCF-Endpunkten verwenden. Die Methoden sind veraltet. Apps sollten OAuth-Authentifizierung anstelle von Formularauthentifizierung und für die Verwendung mit Project Online verwenden. Weitere Informationen finden Sie unter [Autorisierung und Authentifizierung für apps in SharePoint 2013](https://msdn.microsoft.com/library/fp142384%28office.15%29.aspx#FileName_uniquekeyword1).
    
- Anwendungen, die abhängig oder bestimmte Sicherheitseinstellungen in Project Server zu ändern.
    
  > [!NOTE]
  > Eine lokale Standardinstallation von Project Server 2013 verwendet den SharePoint-Berechtigungsmodus, auf dem Project Server-Sicherheitseinstellungen nicht zugegriffen werden mittels PSI zugreifen. Um in den Project-Berechtigungsmodus ändern, finden Sie im Abschnitt *SharePoint-Berechtigungsmodus* in [What's new for IT-Spezialisten in Project Server 2013](https://technet.microsoft.com/en-us/library/ff631142%28office.15%29.aspx#section13). 
  
- Für viele benutzerdefinierte Project Server-Workflows können Sie SharePoint Designer 2013 verwenden, um deklarative Workflows zu erstellen. Für benutzerdefinierte Workflows, die zusätzliche Programmierung erfordern, sollten *nicht* direkt verwenden Klassen oder Member im **Microsoft.Office.Project.Server.Workflow** -Namespace. Verwenden Sie stattdessen die [Microsoft.ProjectServer.Client.WorkflowActivities](https://msdn.microsoft.com/library/Microsoft.ProjectServer.Client.WorkflowActivities.aspx) -Klasse in der CSOM. 
    
- Im Allgemeinen sollten Applications, die Identitätswechsel verwenden umgeschrieben werden, um die WCF-Schnittstelle von der PSI verwenden. Anwendungen, die einfache statusaktualisierungen für andere Benutzer zu erledigen ist kein Identitätswechsel erforderlich. Sie können die [StatusAssignment.SubmitStatusUpdates](https://msdn.microsoft.com/library/Microsoft.ProjectServer.Client.StatusAssignment.SubmitStatusUpdates.aspx) -Methode in der CSOM oder die [Statusing.SubmitStatusForResource](https://msdn.microsoft.com/library/WebSvcStatusing.Statusing.SubmitStatusForResource.aspx) -Methode in die PSI verwenden. 
    
- Middleware-Komponenten, die auf dem Project Server-Computer ausgeführt können nur für die lokale Verwendung installiert werden und müssen die WCF-Schnittstelle von der PSI verwenden. Beispielsweise eine Middleware-Komponente, die verwendet das ASMX-Schnittstelle, um den Datenaustausch zwischen lokalen Project Web App und eine externen Arbeitszeittabelle Anwendung umgeschrieben werden, um das WCF-Interface die PSI verwenden müssten. Die Verwendung mit Project Online müssten die Komponente werden als eine app neu gestaltet und das CSOM verwenden.
    
### <a name="migration-and-compatibility-of-custom-solutions"></a>Migration und Kompatibilität von benutzerdefinierten Lösungen
<a name="pj15_Programmability_CustomSolutions"> </a>

Klassen und Member in der öffentlichen ASMX- und WCF-Schnittstellen des die PSI sind identisch. Aber die Anzahl der Spalten und Größe der Datentabellen verwendet oder PSI-Methoden zurückgegebene Project Server 2013 und den beiden vorherigen Project Server-Versionen unterschiedlich sind. Es gibt auch Unterschiede in den reporting Tabellen und Ansichten, mit der Berichtsdatenbank in früheren Versionen verglichen.
  
> [!IMPORTANT]
> Es wird dringend empfohlen, dass Sie Lösungen in einer nicht in der Produktion Installation von Project Server 2013 vor der Bereitstellung auf einem Produktionsserver gründlich testen. 
  
Wenn Sie eine Lösung in Project Server 2013 migrieren oder eine Lösung nicht erwartungsgemäß funktioniert, sollten Sie mindestens Folgendes:
  
- Aktualisieren Sie die Lösung durch Öffnen des Formulars in Visual Studio 2012. Einige Lösungen können auch mit Visual Studio 2010 verwenden.
    
- Ändern Sie das Ziel des Vorgangs in .NET Framework 4.
    
- Ändern der Assemblyverweise Project Server 2013-Assemblys, wie Microsoft.Office.Project.Server.Library.dll und Microsoft.Office.Project.Server.Events.Receivers.dll verwenden.
    
- Erstellen Sie eine Liste der Webverweise ASMX oder WCF-Dienstverweise und Namespacenamen, und löschen Sie die Project Server-Verweise.
    
- Fügen Sie die ProjectServerServices.dll-Proxy-Assembly, die aus den WCF-Proxy-Quelldateien in der Project 2013-SDK-Download erstellen oder die Proxy-Quelldateien für die erforderlichen WCF-Dienste hinzufügen. Für ASMX-Dienste hinzufügen der Front-End-ASMX Webdienstverweise erneut, mithilfe der gleichen Namespacenamen; oder fügen Sie die ProjectServerServices.dll-Proxy-Assembly, die Sie aus der WSDL-Quellen im Project 2013-SDK-Download erstellen können.
    
  > [!NOTE]
  > In der Project 2013-SDK-Download Dateien die Namespaces in der Proxyquelle mit *Svc* alle beginnen. Beispielsweise ist der **Ressource** -Service-Namespace in der WCF-Proxy-Datei und in der ASMX-Proxydatei **SvcResource**. > Wenn für Ihre Anwendung verschiedene Namespacenamen verwendet wird, können Sie erneut kompilieren die Proxyassembly Namespaces verwenden, um oder ändern die PSI-Namespaces in der Anwendung. Sie können beispielsweise das CompileWCFProxyAssembly.cmd-Skript ändern, und kompilieren Sie ProjectServerServices.dll aus den Proxy-Quelldateien in der SDK-Download neu. 
  
- Wenn Sie die ASMX-Schnittstelle von der PSI verwenden, um das WCF-Interface ändern, können Sie die Client-Klassen entweder programmgesteuert oder mithilfe von WCF-Endpunkten in app.config initialisieren. Verwenden Sie die programmgesteuerte Initialisierung, wenn Sie schnell zu verschiedenen Instanzen von Project Web App wechseln, oder wenn Sie ein Webpart entwickeln, die die PSI verwendet.
    
- Es gibt mehrere neue Methoden und Datasets in der PSI-Dienste in Project Server 2013 und einige Klassen **DataRow** neue Eigenschaften enthalten. Beispielsweise die [QueueUpdateProject2](https://msdn.microsoft.com/library/WebSvcProject.Project.QueueUpdateProject2.aspx) -Methode in die PSI Planungsmodul Project Server, um eine aktualisierte Project neu berechnen, ohne dass Sie das Projekt in Project Professional 2013 öffnen verwendet und ermöglicht außerdem hinzufügen oder Löschen von projektentitäten in einem Anruf. 
    
- Kompilieren und Testen der Lösung.
    
## <a name="project-scheduling-on-the-server"></a>Projektterminierung auf dem server
<a name="pj15_Programmability_Scheduling"> </a>

Projektserver 2013 hat zwei scheduling Module. Neuere Planungsmodul entspricht dem Planungsmodul in Project Professional 2013. Wenn Sie Terminplan ändern und veröffentlichen die Änderungen mithilfe des Planung-Webparts (Seite Projektdetails) in Project Web App oder eine Projektwebsite oder unter Verwendung des CSOM, die Berechnung der Termine, Kosten, Dauer, verbleibende Arbeit, Baselines und weitere Änderungen im Zusammenhang mit der Planung sind die gleichen wie bei die Änderungen vorgenommen und das Projekt veröffentlicht mithilfe von Project Professional 2013. Mit Ausnahme der [QueueUpdateProject2](https://msdn.microsoft.com/library/WebSvcProject.Project.QueueUpdateProject2.aspx) -Methode verwenden PSI-Methoden jedoch ältere Planungsmodul, das von Project Server 2010 migriert wurde. Der Grund dafür besteht, um sicherzustellen, dass Legacyanwendungen in Project Server 2013 dasselbe Verhalten wie zuvor. 
  
> [!NOTE]
> Um aktualisierte Planungsmodul in Project Server 2013 verwenden, können Anwendungen das CSOM verwenden. 
  
Das ältere und neuere scheduling Module bieten die folgenden Nachteile auf:
  
- **Planen von nur Einzelprojekt** Planen von wirkt sich nur das aktuelle Projekt über vorgangsstatusaktualisierungen mit den PSI oder das CSOM oder Project Web App Änderungen vorgenommen werden. Wenn das aktuelle Projekt Links zu anderen Projekten, Unterprojekte oder Hauptprojekten aufweist, werden die verknüpften Projekte nicht geändert. 
    
- **Sammelvorgänge** Sammelvorgänge werden in der Regel schreibgeschützt für Project Server. Beispielsweise Zuordnungen für Sammelvorgänge können nicht erstellt werden, und Prozent Abschluss kann nicht geändert werden. Project Server unterstützt jedoch die Datumsangaben und die Dauer von manuell geplanten Sammelvorgängen bearbeiten. 
    
    Aktuelle Werte für Project Server werden nicht automatisch eine Zuordnung Sammelvorgang hinzugefügt, die den Genehmigungsprozess in Project Server umgehen würde. Wenn Sie einen Teilvorgang aktuelle Werte hinzufügen, werden in Project Professional auch die aktuellen Werte für eine Zuordnung für den Sammelvorgang hinzugefügt. Der Unterschied zwischen Verhalten verwirrend für einen Benutzer.
    
    Projektserver gelöscht Berichtszeiträume an einer Zuordnung ein Sammelvorgang, wenn die Dauer Teilvorgang verkürzt oder den Endtermin geändert wird.
    
    > [!CAUTION]
    > Project Professional es ist, zwar möglich wird empfohlen, dass Sie keine Zuordnungen Sammelvorgänge treffen. 
  
Im folgenden werden Probleme, und Einschränkungen der PSI-Programmierung mit älteren Project Server-Planung des Planungsmoduls:
  
- **Ändern des aktiven Status eines Vorgangs** Ältere Planungsmodul Project Server kann inkonsistente Start anzeigen oder Endzeiten Wenn [QueueUpdateProject](https://msdn.microsoft.com/library/WebSvcProject.Project.QueueUpdateProject.aspx) Sie zum Ändern des aktiven Status eines Vorgangs, gehen Wenn mehrere Änderungen in das **ProjectDataSet** -Objekt für die _vorhanden sind DataSet_ Parameter. Wenn die **TASK_IS_ACTIVE** -Eigenschaft die einzige Änderung im _Dataset_ -Parameter der **QueueUpdateProject**ist, können Sie das Projekt aktualisieren.
    
    Weitere Informationen zu inaktive Vorgänge und ältere Planungsmodul, finden Sie im Blog-Artikel [Introducing inaktive Vorgänge in Project 2010](https://blogs.msdn.com/b/project/archive/2010/06/10/introducing-inactive-tasks-in-project-2010.aspx) und [Project Server 2010: Planen von Websites, die PSI und Project Professional](https://blogs.msdn.com/b/brismith/archive/2010/09/10/project-server-2010-scheduling-on-the-web-the-psi-and-project-professional.aspx?wa=wsignin1.0). Einen Vergleich der in Project Professional 2010 und Project Web App in Project Server 2010 planen finden Sie unter [Zeitplan webbasierte Verwaltung Comparison](https://blogs.msdn.microsoft.com/brismith/2010/09/10/project-server-2010-scheduling-on-the-web-the-psi-and-project-professional/).
    
- **Ertragswert nicht berechnet.** Ältere Planungsmodul Ertragswert-Felder nicht berechnet: IKAA, PK, SKAA, SKBA, KLI, KA, KA %, Exchange-Verwaltungskonsole, SPI, PA, PA %, ALI, ANA, Abweichung Dauer, Abweichung Anfang, Abweichung, Abweichung Kosten, und Abweichung Arbeit. Wenn ein Projekt Werte für diese Felder hat und das Projekt mithilfe der **QueueUpdateProject** -Methode aktualisiert wird, ändern Sie die Feldwerte nicht. Verwenden Sie die **QueueUpdateProject2** -Methode, um das Problem zu vermeiden. 
    
Sie können die PSI Planen von Einschränkungen wie folgt behandeln:
  
- Ist das CSOM die Methoden, die Anwendung erfordert, verwenden Sie das CSOM anstelle der PSI.
    
- Öffnen von Projekten in Project Professional, und sie wieder in Project Server speichern.
    
- Fügen Sie in Berichten nicht Felder, die die PSI nicht aktualisiert wird.
    
- Fügen Sie eine Notiz in Berichten zu Daten, die möglicherweise veraltet.
    
In den Tabellen reporting Flags vorhanden sind und die Cubes, die Ihnen helfen erkennen, wenn einige Projektdaten nicht aktualisiert werden. Die Berichtsdaten in der Tabelle MSP_EpmProject und MSP_EpmProject_UserView umfasst die folgenden Felder: 
  
-  _ProjectWbsIsStale_ &ndash; Gibt an, ob der Projektstrukturplan (Vorgangshierarchie Gliederung) veraltet ist. 
    
-  _ProjectEarnedValueIsStale_ &ndash; Gibt Ertragswert-Felder sind veraltet. 
    
-  _ProjectRollupsAreStale_ &ndash; Gibt an, die ein Teilprojekt ist in der Entwurfsdatenbank aktualisiert, aber das Hauptprojekt werden nicht aktualisiert. Die Rollup-Werte aus der Teilprojekt sind veraltet. 
    
-  _ProjectHierarchyNotSynchronized_ &ndash; Hauptprojekt ist nicht mit den dazugehörigen untergeordneten synchronisiert. Dies geschieht, wenn die untergeordneten Projekte explizit, nicht als Teil der Veröffentlichung Hauptprojekt veröffentlicht werden. 
    
-  _ProjectCalculationsAreStale_ &ndash; Project Professional ein Projekt ohne Berechnung des Terminplans gespeichert (d. h., der Berechnungsmodus ist festgelegt auf **manuell** auf der Registerkarte **Terminplan** im Dialogfeld **Project-Optionen** ). 
    
-  _ProjectGhostTaskAreStale_ &ndash; Ähnlich wie _ProjectHierarchyNotSynchronized_, aber gibt eine Warnung aus auf Daten projektübergreifender verknüpfen. Es ist möglich, dass kein Hauptprojekt vorhanden ist, aber die Project-Daten auf einer Seite den Link neuer als auf der anderen Seite ist.
    
## <a name="about-accessing-the-project-server-database"></a>Informationen zum Zugreifen auf die Project Server-Datenbank
<a name="pj15_Programmability_Databases"> </a>

Wenn Sie Berechtigungen in Microsoft SQL Server Zugriff auf die Project Server-Datenbank verfügen, können Sie die Berichte Tabellen und Sichten lesen. Wenn Sie die erforderlichen Berechtigungen für Project Server verfügen, können Sie mithilfe von OData-Abfragen auch Daten aus den Tabellen reporting gelesen. Entwicklern werden abgeraten, aus der direkte Zugriff auf den Entwurf, veröffentlicht, oder Tabellen über SQL Server-Abfragen in der Project Server-Datenbank zu archivieren. Direkte Änderungen in den Tabellen in der Project Server-Datenbank vornehmen kann beschädigen referenziellen Integrität und Datenbankzugriff über die Project Server-Warteschlangendienst beeinflussen.
  
> [!IMPORTANT]
> Es gibt nichts aktiv Sie verhindern Datenbank direkt den programmgesteuerten Zugriff zum Aktualisieren von Daten verwenden. Sie sollten beachten Sie, dass der Project Professional-Cache, der veröffentlichten Tabellen und den reporting Tabellen auf ein Cache Synchronisierungsprotokoll verlassen, die durch direkte Daten bearbeiten unterbrochen werden kann. Wenn Sie Project Server-Datenbank beschädigt oder Project Professional beschädigte zwischengespeichert mit direkter Zugriff zum Ändern von Daten, eine Warnung angezeigt, dass nicht Produktsupport dazu beitragen kann mithilfe der clientseitigen! 
  
Anwendungen, die direkten Zugriff auf den Entwurf, veröffentlicht, oder Archivieren von Tabellen und Ansichten hängen auch das Schema der Datenbank, die in Servicepacks oder höhere Versionen von Project Server 2013 ändern können. Darüber hinaus verlieren Anwendungen, die direkt auf die Datenbanken zugreifen, die integrierte Sicherheit bei Project Server, allgemeine Geschäftslogik, Überwachung, Überwachungen, fehlerüberprüfung, reporting, Workflow und andere Features. Wahrscheinlich müssen Sie eine solche Anwendung schreiben Sie nach dem Project Server 2013 aktualisiert. 
  
Für alle der folgenden Gründe Project Professional und Project Web App nicht direkte Aufrufe für den Entwurf, veröffentlicht, oder Archivieren von Tabellen; sollten Sie weder eine anderen Anwendung, die in Project Server integriert.
  
Die Schemas für den Entwurf, veröffentlicht, und Archivtabellen sind nicht dokumentiert. Sie können die reporting Tabellen Generieren von Berichten und das Schema für die reporting Tabellen und Ansichten ist dokumentiert im Project 2013-SDK-Download. Das Schema OData der Berichtsdaten finden Sie unter [ProjectData - Projekt OData-Dienstverweises](https://msdn.microsoft.com/library/office/jj163015.aspx).
  
## <a name="see-also"></a>Siehe auch

- [Updates für Entwickler in Project 2013](updates-for-developers-in-project-2013.md)    
- [Project Server 2013-Architektur](project-server-2013-architecture.md)    
- [Was die PSI durchführen kann und was nicht](what-the-psi-does-and-does-not-do.md)   
- [Was das CSOM durchführen kann und was nicht](what-the-csom-does-and-does-not-do.md)    
- [Clientseitiges Objektmodell (CSOM) für Project 2013](client-side-object-model-csom-for-project-2013.md)    
- [Erste Schritte beim Entwickeln von Project Server-Workflows](getting-started-developing-project-server-workflows.md)    
- [Project 2013 Programmierreferenzen](project-2013-programming-references.md)    
- [Project-PSI-Referenz – Übersicht](project-psi-reference-overview.md)    
- [Erstellen Sie benutzerdefinierter Aktionen zur Bereitstellung mit apps für SharePoint](https://msdn.microsoft.com/library/office/apps/jj163954%28v=office.15%29.aspx)    
- [Einführung in die inaktive Vorgänge in Project 2010](https://blogs.msdn.com/b/project/archive/2010/06/10/introducing-inactive-tasks-in-project-2010.aspx)    
- [Project Server 2010: Planen auf den Webservern, die PSI und Project Professional](https://blogs.msdn.microsoft.com/brismith/2010/09/10/project-server-2010-scheduling-on-the-web-the-psi-and-project-professional/)

