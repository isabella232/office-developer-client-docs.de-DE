---
title: Was das CSOM durchführen kann und was nicht
manager: soliver
ms.date: 09/17/2015
ms.audience: Developer
localization_priority: Normal
ms.assetid: 6828485c-040b-4278-923f-4cc7c8fe0fb1
description: Das Client-seitigen Objektmodell (CSOM) ist ein Satz von APIs für Project Server 2013, die für beide entworfen wurden, online und lokalen verwenden in apps, die für PCs, Tablets und mobilen Geräten entwickelt werden können. Dieser Artikel enthält einige Standardszenarien für die Verwendung des CSOM und führt außerdem Einschränkungen des CSOM.
ms.openlocfilehash: ad9f9e0404cb0063a1c58c8e66a022372881a24f
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/04/2018
ms.locfileid: "25399291"
---
# <a name="what-the-csom-does-and-does-not-do"></a>Was das CSOM durchführen kann und was nicht

Das Client-seitigen Objektmodell (CSOM) ist ein Satz von APIs für Project Server 2013, die für beide entworfen wurden, online und lokalen verwenden in apps, die für PCs, Tablets und mobilen Geräten entwickelt werden können. Dieser Artikel enthält einige Standardszenarien für die Verwendung des CSOM und führt außerdem Einschränkungen des CSOM.
  
|||
|:-----|:-----|
|||
   
Das CSOM ermöglicht die Entwicklung von apps für Project Server 2013 und Integration von Project Server mit einer anderen Anwendung. Apps können zur Ausführung auf PCs und mobilen Geräten wie Windows Phone 7.5, Tablets wie dem Windows 8-Geräten und iOS und Android-Geräte entwickelt werden. Das CSOM werden APIs, die am häufigsten Funktionen der zwölf abdecken PSI-Dienste in Project Server verwendet. Die CSOM-APIs sind abweichend und einfacher, als die ASMX-basierte und WCF-basierte PSI-Dienste zu verwenden sind. Das CSOM ADO.NET-Datasets wird nicht verwendet und kann über den OData-Protokoll zugegriffen werden. Sie können mithilfe von .NET Framework 4 Bibliotheken, JavaScript, mit dem Clientobjektmodell entwickeln oder Representational State Transfer (REST) Abfragen.
  
Eine Übersicht über die CSOM und Artikel, die zeigen, wie Sie mit dem Clientobjektmodell JavaScript und .NET Framework 4 verwenden, finden Sie unter [Client-seitigen Objektmodell (CSOM) für Project Server](client-side-object-model-csom-for-project-2013.md). Weitere Informationen über die CSOM-Assemblys, Klassen und Member finden Sie unter den [Microsoft.ProjectServer.Client](https://msdn.microsoft.com/library/Microsoft.ProjectServer.Client.aspx) Namespaceverweis. 
  
## <a name="usage-scenarios-for-the-csom"></a>Verwendungsszenarien für das CSOM
<a name="pj15_WhatTheCSOM_UsageScenarios"> </a>

Es folgen Beispiele für einige Arten von apps, die das CSOM unterstützt. Dem Clientobjektmodell kann anstelle der PSI für viele Szenarien verwendet werden:
  
- **Entwickeln von apps, die Project Server erweitern** Der primäre Zweck der des CSOM ist app-Entwicklung für Project Server 2013, wo apps für eine Vielzahl von Geräten erstellt werden können, die PCs, Mobilgeräten und Tablets enthalten. Apps können innerhalb einer privaten app-Katalog oder in den öffentlichen Office Store verteilt werden. 
    
- **Automatisieren der Erstellung oder Verwaltung von Entitäten in Project Server** Dem Clientobjektmodell kann CRUD-Vorgänge für Entitäten wie Projekte, Aufgaben, Zuordnungen, Enterprise-Ressourcen, benutzerdefinierten Feldern, Nachschlagetabellen, Arbeitszeittabellen, Ereignishandler und Workflowphasen und-Stufen ausführen. Oftmals stehen Fällen, in dem eine benutzerdefinierte Anwendung Zeit mit Massen oder wiederkehrende Aufträge speichern können. 
    
- **Abrufen von Daten in den veröffentlichten Tabellen der Project-Datenbank** Da Datenbank direkt den Zugriff auf den Entwurf, veröffentlicht, und archivieren Tabellen wird nicht unterstützt, können Sie das CSOM zum Lesen von Daten, die in die reporting Tabellen oder Ansichten nicht verfügbar ist. Beispielsweise erhalten Sie Informationen zu Workflowstufen, Phasen und Aktivitäten. Zum Lesen von Daten in den Tabellen reporting, können Sie den OData-Abfragen verwenden. 
    
- **Überprüfen von Zeitberichte und Arbeitszeittabellen-Daten** Verwenden Sie das CSOM in lokale Ereignishandler oder remote-Ereignisempfänger für Ereignisse vor, um Zuordnungsdaten Status oder Arbeitszeittabellen-Warteschlange überprüfen, die Benutzer eingeben, bevor die Daten in Project Web App gespeichert werden. 
    
- **Finanzielle Projekte erstellen** Erstellen Sie Projekte für die Erfassung der Zeit über die Arbeitszeittabelle für die Integration mit einem finanzielle System. Erstellen einer Hierarchie von finanziellen Codes, die die Kosten des Ressourcenstrukturplans Struktur des Systems finanzielle widerspiegeln. Finanzielle Projekte erfordern keinen planen oder Status Updates. 
    
- **Integration mit Buchhaltungssystemen** Erfassen Sie die Ressourcenkosten und Ausgaben im Zusammenhang mit Projekten Feed Systeme finanzielle und zur Abrechnung und zu Vergleichszwecken Budget. Synchronisieren von Aufgaben, Ressourcen und Zuordnungen zwischen den Systemen. Erfassen von Daten in Arbeitszeittabellen in einem System zum anderen feed (verwendet wird, welche Arbeitszeittabelle hängt von den Anforderungen der Organisation oder von einzelnen Projekten). 
    
- **Automatisieren von Updates von Teammitgliedern** Aktualisieren Sie für Projekte, die nicht aktiv verwaltet werden automatisch Projekte auf dem Server mit des Fortschritts und der andere Änderungen von Projektteammitgliedern. Projekte können aktualisiert und ohne ein Projektmanager Überprüfen der Ergebnisse oder Anpassungen an den Plan erneut veröffentlicht werden. 
    
    > [!NOTE]
    > Das CSOM Übermitteln von Statusupdates unterstützt, aber Status Genehmigungen derzeit nicht unterstützt. 
  
- **Bewerten der Project Server-Daten in remote-Ereignisempfänger** Project Server-Daten aus dem Clientobjektmodell können ein remote-Ereignisempfänger für ein **ProjectCreating** Pre-Ereignis können Sie bestimmen, ob das Ereignis abgebrochen. Vergleichen Sie vor dem Erstellen eines Projekts, beispielsweise den Projektvorschlag mit vorhandenen Projekten. 
    
- **Unterstützung für deklarative Project Server-workflows** Dem Clientobjektmodell kann Project Server-Workflows, die in SharePoint Designer 2013 erstellt werden. Das CSOM unterstützt workflowdefinitionen, die Windows Workflow Foundation Version 4 (WF4) verwenden. (Die PSI bietet keine Unterstützung für Workflows WF4.) 
    
- **Erstellen komplexer Project Server-workflows** Beim Entwickeln von Workflows mit Visual Studio 2012 können Sie das CSOM für komplexe Aktionen innerhalb Workflowstufen verwenden oder benutzerdefinierte Workflowaktionen erstellen. 
    
## <a name="what-the-csom-does-not-do"></a>Was das CSOM nicht zu
<a name="pj15_WhatTheCSOM_DoesNotDo"> </a>

Das CSOM ist kein vollständiger Ersatz für die PSI. Da das CSOM intern der PSI-Dienste verwendet wird, hat das CSOM vieler die gleichen funktionalen Einschränkungen, die die PSI hat. Zusätzlich zu den Einschränkungen des die PSI, wie etwa haben keinen Zugriff auf Daten in lokalen Projekten (MPP-Dateien) enthält das CSOM keinen Verwaltungsfunktionen, die in der Regel Project Web App behandelt. Beispielsweise kann das Erstellen von benutzerdefinierten Sicherheitsgruppen in den Websiteeinstellungen - Seite Berechtigungen für Project Web App behandelt werden. 
  
Eine Liste der Aktionen, die die PSI weder das CSOM behandelt, finden Sie im Abschnitt *Was die PSI nicht* in [die PSI Was ist und nicht zu](what-the-psi-does-and-does-not-do.md).
  
### <a name="psi-services-that-the-csom-does-not-cover"></a>PSI-Dienste, die dem Clientobjektmodell keine abdeckt.
<a name="pj15_WhatTheCSOM_PSIServices"> </a>

Das CSOM umfasst keine Funktionalität von der folgenden PSI-Dienste:
  
- **Verwaltungsdienst** Verwenden Sie zum Verwalten von administrativen Einstellungen und Vorgänge in Project Server und verwandte Projektwebsites, z. B. Geschäftszeiträume erstellen und das Arbeitszeittabellen-Einstellungen PSI-Methoden in der [WebSvcAdmin.Admin](https://msdn.microsoft.com/library/WebSvcAdmin.Admin.aspx) -Klasse. Project Web App selbst verwendet **Admin** Methoden in vielen Seiten, die mit der Seite servereinstellungen verknüpft sind (https:// *ServerName*  /  *ProjectServerName* /_layouts/15/pwa/Admin/Admin.aspx). 
    
- **Archivierungsdienst** Verwenden Sie zum Speichern und Verwalten von Entitäten wie Projekten, Ressourcen und benutzerdefinierte Felder in die Archivtabellen, PSI-Methoden in das [Archiv](https://msdn.microsoft.com/library/WebSvcArchive.Archive.aspx) -Klasse. 
    
- **CubeAdmin-Dienst** Zum Erstellen und Verwalten von OLAP-Cubes für lokale Installationen, PSI-Methoden in der [WebSvcCubeAdmin.CubeAdmin](https://msdn.microsoft.com/library/WebSvcCubeAdmin.CubeAdmin.aspx) -Klasse verwenden, oder verwenden Sie die Seite OLAP-Datenbankverwaltung (https:// *ServerName*  /  *ProjectServerName* /_layouts/15/pwa / CubeAdmin/CubeAnalysisAdmin.aspx) in Project Web App. 
    
    > [!NOTE]
    > Project Online unterstützt keine OLAP-Cubes. 
  
- **Treiber-Dienst** Verwenden Sie zum Erstellen und Verwalten von betriebswirtschaftlichen Faktoren für Project Portfolio-Analysen, PSI-Methoden in der [WebSvcDriver.Driver](https://msdn.microsoft.com/library/WebSvcDriver.Driver.aspx) -Klasse. 
    
- **LoginForms-Dienst und LoginWindows-Dienst** Authentifizierung in das CSOM erfolgt während der Initialisierung des **ProjectContext** -Objekts mit OAuth oder die Windows-Authentifizierung. Verwenden Sie zum Erstellen von Anwendungen für mehrfach-Authentifizierung, in dem eine lokale voll vertrauenswürdige Anwendung Formularauthentifizierung und Windows-Authentifizierung verwenden können, PSI-Methoden in der [WebSvcLoginForms.LoginForms](https://msdn.microsoft.com/library/WebSvcLoginForms.LoginForms.aspx) -Klasse und die [ WebSvcLoginWindows.LoginWindows](https://msdn.microsoft.com/library/WebSvcLoginWindows.LoginWindows.aspx) Klasse. 
    
- **Benachrichtigungsdienst** Verwenden Sie zum Erstellen und Verwalten von Warnungen und Erinnerungen, PSI-Methoden in der [WebSvcNotifications.Notifications](https://msdn.microsoft.com/library/WebSvcNotifications.Notifications.aspx) -Klasse. 
    
- **ObjectLinkProvider-Dienst** Verwenden Sie zum Erstellen und Verwalten von Webobjekten und Links zu Dokumenten und Listenelementen SharePoint, PSI-Methoden in der [WebSvcObjectLinkProvider.ObjectLinkProvider](https://msdn.microsoft.com/library/WebSvcObjectLinkProvider.ObjectLinkProvider.aspx) -Klasse. 
    
- **PortfolioAnalyses-Dienst** Verwenden Sie zum Erstellen und Verwalten von Project Portfolioanalysen, einschließlich Planner Lösungen und Optimierer Lösungen, PSI-Methoden in der [WebSvcPortfolioAnalyses.PortfolioAnalyses](https://msdn.microsoft.com/library/WebSvcPortfolioAnalyses.PortfolioAnalyses.aspx) -Klasse. 
    
- **QueueSystem-Dienst** Das CSOM grundlegende Informationen zu Project Server-Warteschlangenaufträge finde und enthält die [ProjectContext.WaitForQueue](https://msdn.microsoft.com/library/Microsoft.ProjectServer.Client.ProjectContext.WaitForQueue.aspx) -Methode. Verwenden Sie zur Verwaltung der Project Server-Warteschlangensystem umfangreichere PSI-Methoden in der [WebSvcQueueSystem.QueueSystem](https://msdn.microsoft.com/library/WebSvcQueueSystem.QueueSystem.aspx) -Klasse. 
    
- **Sicherheitsdienst** Erstellen und Verwalten von Project Server-Sicherheitsgruppen, Vorlagen und Kategorien und Berechtigungen für den aktuellen Benutzer zu überprüfen, verwenden Sie PSI-Methoden in der [WebSvcSecurity.Security](https://msdn.microsoft.com/library/WebSvcSecurity.Security.aspx) -Klasse. 
    
- **WssInterop-Dienst** Verwenden Sie zum Abrufen von Informationen zu und Verwalten von Projektwebsites, PSI-Methoden in der [WebSvcWssInterop.WssInterop](https://msdn.microsoft.com/library/WebSvcWssInterop.WssInterop.aspx) -Klasse. 
    
    > [!NOTE]
    > Sie können das CSOM in SharePoint Server 2013. Projektwebsites sind SharePoint-Websites. 
  
Das CSOM ermöglicht keine Erweiterungen, wie die PSI haben kann. Bei der Erstellung einer PSI-Erweiterungs für die lokale Verwendung kann beispielsweise das CSOM geändert werden zum Verwenden der PSI-Erweiterungs. Sie können auf andere Weise Erweiterung Szenarien implementieren:
  
- Aggregierte CSOM-Aufrufe innerhalb einer lokalen Komponente oder eine Komponente, die auf Microsoft Azure ausgeführt wird.
    
- Verwenden von OData-Abfragen von Berichtsdaten, anstelle der direkte Zugriff auf reporting Tabellen in der Project Server-Datenbank.
    
- Integrieren von CSOM-Aufrufe mit drittanbieteranwendungen über OAuth-Authentifizierung aus Project Online oder serverseitige Komponenten für die lokale Verwendung.
    
- Webanwendungen, die das CSOM verwenden können auch benutzerdefinierten Datenbanken entweder lokal oder mit SQL Azure.
    
### <a name="request-limits-of-the-csom"></a>Grenzen eines des CSOM anfordern
<a name="pj15_WhatTheCSOM_RequestLimits"> </a>

Das CSOM in Project Server 2013 basiert auf die CSOM-Implementierung in SharePoint Server 2013 und erbt die Grenzwerte für die maximale Größe einer Anforderung. SharePoint hat maximal 2 MB für eine Anforderung Vorgänge und maximal 50 MB für die Größe eines gesendete binary-Objekts. Die Größe der Anforderung ist auf den Server aus übermäßig lange Warteschlangen von Vorgängen und die Bearbeitung für große binäre Objekte zu schützen beschränkt.
  
Beispielsweise, wenn Sie des CSOM mithilfe erstellen Sie ein Projekt, und klicken Sie dann Bearbeiten des Projekts, um 252 Aufgaben mit einem Mindestmaß an Informationen wie einen kurzen Namen, die Vorgangs-GUID und eine Dauer von 1D hinzufügen, der die Gesamtmenge der Daten in der Anforderung **DraftProject.Update** ist kleiner als 2 MB. Aber, wenn Sie versuchen, ein leeres Projekt 253 Aufgaben hinzuzufügen, die 2 MB überschritten ist, und erhalten Sie die folgende Ausnahme: **Microsoft.SharePoint.Client.ServerException: die Anforderung verwendet zu viele Ressourcen**
  
Zum Erfassen der Datenteils in eine CSOM-Anforderung über HTTP oder HTTPS, können Sie eine Tool wie [Fiddler](https://www.fiddler2.com) Debuggen Web (https://www.fiddler2.com). Ein Codebeispiel, das einen Test für Anforderungsgröße implementiert und umfasst eine Lösung, die eine große Anforderung in kleinere Gruppen aufgehoben, finden Sie unter [DraftProject.Update](https://msdn.microsoft.com/library/Microsoft.ProjectServer.Client.DraftProject.Update.aspx) . 
  
## <a name="see-also"></a>Siehe auch
<a name="pj15_WhatTheCSOM_AR"> </a>

- [Client-seitigen Objektmodell (CSOM) für Project Server](client-side-object-model-csom-for-project-2013.md)
    
- [Was die PSI durchführen kann und was nicht](what-the-psi-does-and-does-not-do.md)
    
- [Microsoft.ProjectServer.Client](https://msdn.microsoft.com/library/Microsoft.ProjectServer.Client.aspx)
    

