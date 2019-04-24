---
title: Was das CSOM durchführen kann und was nicht
manager: soliver
ms.date: 09/17/2015
ms.audience: Developer
ms.assetid: 6828485c-040b-4278-923f-4cc7c8fe0fb1
description: Bei dem clientseitigen Objektmodell (CSOM) handelt es sich um eine Gruppe von APIs für Project Server 2013, die zur Verwendung in Online-Apps und in lokalen Apps konzipiert wurden, die für PCs, mobile Geräte und Tablets entwickelt werden können. Dieser Artikel enthält einige typische Szenarien für die Verwendung des CSOM und auch die Einschränkungen des CSOM.
localization_priority: Priority
ms.openlocfilehash: 6cdcb72c24e352365b6dcc9268ddf0bd249369af
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32315225"
---
# <a name="what-the-csom-does-and-does-not-do"></a>Was das CSOM durchführen kann und was nicht

Bei dem clientseitigen Objektmodell (CSOM) handelt es sich um eine Gruppe von APIs für Project Server 2013, die zur Verwendung in Online-Apps und in lokalen Apps konzipiert wurden, die für PCs, mobile Geräte und Tablets entwickelt werden können. Dieser Artikel enthält einige typische Szenarien für die Verwendung des CSOM und auch die Einschränkungen des CSOM.
  
|||
|:-----|:-----|
|||
   
Das CSOM ermöglicht die Entwicklung von Apps für Project Server 2013 und die Integration von Project Server in andere Anwendungen. Die Apps können zur Ausführung auf PCs, mobilen Geräten wie Windows Phone 7.5, Tablets wie Windows 8-Geräten, und IOS- und Android-Geräten entwickelt werden. Das CSOM bietet APIs, die die Funktionalität der zwölf am häufigsten verwendeten PSI-Dienste in Project Server abdecken. Die CSOM-APIs werden organisiert und sind einfacher zu verwenden als die ASMX-basierten und WCF-basierten PSI-Dienste. Das CSOM verwendet keine ADO.NET-Datasets; auf das CSOM kann über das OData-Protokoll zugegriffen werden. Sie können es mithilfe von .NET Framework 4-Bibliotheken, JavaScript oder REST-Abfragen (Representational State Transfer) entwickeln.
  
Eine Übersicht über das CSOM und Artikel, in denen die Verwendung von JavaScript und .NET Framework 4 mit dem CSOM gezeigt wird, finden Sie unter [Clientseitiges Objektmodell (CSOM) für Project Server](client-side-object-model-csom-for-project-2013.md). Weitere Informationen zu den COM-Assemblys, -Klassen und -Mitgliedern finden Sie in der Namespacereferenz [Microsoft.ProjectServer.Client](https://msdn.microsoft.com/library/Microsoft.ProjectServer.Client.aspx). 
  
## <a name="usage-scenarios-for-the-csom"></a>Verwendungsszenarien für das CSOM
<a name="pj15_WhatTheCSOM_UsageScenarios"> </a>

Nachfolgend finden Sie Beispiele für einige Arten von Apps, die das CSOM unterstützt. Das CSOM kann anstelle der PSI für viele Szenarien verwendet werden:
  
- **Entwickeln von Apps, die Project Server erweitern** Der Hauptzweck des CSOM ist die App-Entwicklung für Project Server 2013, bei der Apps für eine Vielzahl von Geräten, z. B. PCs, mobile Geräte und Tablets, erstellt werden können. Apps können in einem privaten App-Katalog oder im öffentlichen Office Store verteilt werden. 
    
- **Automatisieren der Erstellung oder Verwaltung von Entitäten in Project Server** Das CSOM kann CRUD-Vorgänge für Entitäten wie Projekte, Aufgaben, Zuweisungen, Unternehmensressourcen, benutzerdefinierte Felder, Nachschlagetabellen, Arbeitszeittabellen, Ereignishandler sowie Workflowphasen und Phasen, ausführen. Eine benutzerdefinierte App kann in vielen Fällen bei Massenaufträgen oder sich wiederholenden Aufgaben Zeit sparen. 
    
- **Abrufen von Daten in den veröffentlichten Tabellen der Project-Datenbank** Da kein direkter Datenbankzugriff auf die entworfenen, veröffentlichten und archivierten Tabellen unterstützt wird, können Sie das CSOM verwenden, um Daten zu lesen, die nicht in den Berichtstabellen oder Sichten verfügbar ist. Rufen Sie zum Beispiel Informationen zu Workflowphasen, Phasen und Aktivitäten ab. Um Daten in den Berichtstabellen zu lesen, können Sie OData-Abfragen verwenden. 
    
- **Überprüfen von Statusdaten und Arbeitszeittabellen** Verwenden Sie das CSOM in lokalen Ereignishandlern oder Remoteereignisempfängern für Vorereignisse, um den Status von Zuweisungen oder Daten in Arbeitszeittabellen zu überprüfen, die Benutzer eingeben, bevor die Daten in Project Web App gespeichert werden. 
    
- **Erstellen von Finanzprojekten**: Erstellen Sie Projekte für Zeiterfassung über die Arbeitszeittabelle für die Integration in ein Finanzsystem. Erstellen Sie eine Hierarchie von Finanzsystemcodes, die die Struktur der Kostenaufschlüsselung des Finanzsystems wiedergeben. Für Finanzprojekte sind keine Zeitplanungs- oder Statusaktualisierungen erforderlich. 
    
- **Integration in Nachverfolgungssysteme**: Erfassen Sie die Ressourcenkosten und Ausgaben, die mit Projekten verknüpft sind, um Finanz- und Abrechnungssystemen Informationen zur Verfügung zu stellen und um Budgetvergleiche auszuführen. Synchronisieren Sie Vorgänge, Ressourcen und Zuweisungen zwischen den Systemen. Erfassen Sie Arbeitszeittabellendaten in einem System, um die Daten dem anderen System zur Verfügung zu stellen (welche Arbeitszeittabelle verwendet wird, hängt von den Anforderungen der Organisation oder der einzelnen Projekte ab). 
    
- **Automatisieren von Aktualisierungen von Teammitgliedern**: Für Projekte, die nicht aktiv verwaltet werden, aktualisieren Sie automatisch Projekte auf dem Server mithilfe von Informationen von Teammitgliedern zu Fortschritt und anderen Änderungen. Projekte können aktualisiert und neu veröffentlicht werden, ohne dass ein Projektmanager die Ergebnisse überprüft oder Anpassungen am Plan vornimmt. 
    
    > [!NOTE]
    > Das CSOM unterstützt das Übermitteln von Statusupdates, derzeit werden aber keine Statusgenehmigungen unterstützt. 
  
- **Auswerten von Project Server-Daten in Remoteereignisempfängern** Ein Remoteereignisempfänger für ein **ProjectCreating**-Vorereignis kann Project Server-Daten aus dem CSOM verwenden, um herauszufinden, ob das Ereignis abgebrochen werden soll. Vergleichen Sie zum Beispiel vor dem Erstellen eines Projekts den Projektvorschlag mit vorhandenen Projekten. 
    
- **Unterstützung deklarativer Workflows für Project Server** Das CSOM ermöglicht Project Server-Workflows, die in SharePoint Designer 2013 erstellt werden. Das CSOM unterstützt Workflowdefinitionen, die Windows Workflow Foundation, Version 4, (WF4) verwenden. (Die PSI bietet keine Unterstützung für WF4-Workflows.) 
    
- **Erstellen von komplexen Project Server-Workflows** Beim Entwickeln von Workflows mit Visual Studio 2012 können Sie das CSOM für komplexe Aktionen in Workflowphasen oder zum Erstellen benutzerdefinierter Workflowaktionen verwenden. 
    
## <a name="what-the-csom-does-not-do"></a>Was das CSOM nicht durchführen kann
<a name="pj15_WhatTheCSOM_DoesNotDo"> </a>

Das CSOM ist kein vollständiger Ersatz für die PSI. Da das CSOM intern die PSI-Dienste verwendet, gelten für das CSOM viele gleiche funktionale Beschränkungen, die auch die PSI aufweist. Zusätzlich zu Einschränkungen der PSI, z. B. kein Zugriff auf Daten in lokalen Projekten (MPP-Dateien), umfasst das CSOM keine Administratorfunktionen, die Project Web App in der Regel verarbeitet. Beispielsweise kann das Erstellen benutzerdefinierter Sicherheitsgruppen auf der Seite „Websiteeinstellungen – Berechtigungen“ für Project Web App verarbeitet werden. 
  
Eine Liste von Aktionen, die weder die PSI noch das CSOM verarbeiten, finden Sie im Abschnitt *Was die PSI nicht durchführen kann* unter [Was die PSI durchführen kann und was nicht](what-the-psi-does-and-does-not-do.md).
  
### <a name="psi-services-that-the-csom-does-not-cover"></a>PSI-Dienste, die das CSOM nicht abdeckt
<a name="pj15_WhatTheCSOM_PSIServices"> </a>

Das CSOM enthält keine Funktionalität der folgenden PSI-Dienste:
  
- **Admin-Dienst** Verwenden Sie zum Verwalten von administrativen Einstellungen und Vorgängen in Project Server und für zugehörige Projektwebsites, z. B. das Erstellen von Geschäftszeiträumen und das Vornehmen von Einstellungen für Arbeitszeittabellen, PSI-Methoden in der [WebSvcAdmin.Admin](https://msdn.microsoft.com/library/WebSvcAdmin.Admin.aspx)-Klasse. Project Web App selbst verwendet **Admin**-Methoden auf vielen der Seiten, die mit der Seite „Servereinstellungen“ verknüpft sind (https:// *ServerName*  /  *ProjectServerName*/_layouts/15/pwa/Admin/Admin.aspx). 
    
- **Archivdienst** Zum Speichern und Verwalten von Entitäten, z. B. Projekte, Ressourcen und benutzerdefinierte Felder in den Archivtabellen, verwenden Sie PSI-Methoden in der [Archive](https://msdn.microsoft.com/library/WebSvcArchive.Archive.aspx)-Klasse. 
    
- **CubeAdmin-Dienst** Zum Erstellen und Verwalten von OLAP-Cubes für lokale Installationen verwenden Sie PSI-Methoden in der [WebSvcCubeAdmin.CubeAdmin](https://msdn.microsoft.com/library/WebSvcCubeAdmin.CubeAdmin.aspx)-Klasse, oder verwenden Sie die Seite der OLAP-Datenbankverwaltung (https:// * ServerName*  /  *ProjectServerName* /_layouts/15/pwa/CubeAdmin/CubeAnalysisAdmin.aspx) in Project Web App. 
    
    > [!NOTE]
    > Project Online unterstützt keine OLAP-Cubes. 
  
- **Treiberdienst** Zum Erstellen und Verwalten von Geschäftsfaktoren für Projektportfolioanalysen verwenden Sie PSI-Methoden in der [WebSvcDriver.Driver](https://msdn.microsoft.com/library/WebSvcDriver.Driver.aspx)-Klasse. 
    
- **LoginForms-Dienst und LoginWindows-Dienst** Die Authentifizierung im CSOM erfolgt bei der Initialisierung des **ProjectContext**-Objekts mit der OAuth- oder Windows-Authentifizierung. Um Anwendungen für die mehrstufige Authentifizierung zu erstellen, bei denen eine lokale, voll vertrauenswürdige Anwendung sowohl die Formularauthentifizierung als auch die Windows-Authentifizierung verwenden kann, verwenden Sie PSI-Methoden in der [WebSvcLoginForms.LoginForms](https://msdn.microsoft.com/library/WebSvcLoginForms.LoginForms.aspx)-Klasse und in der [WebSvcLoginWindows.LoginWindows](https://msdn.microsoft.com/library/WebSvcLoginWindows.LoginWindows.aspx)-Klasse. 
    
- **Benachrichtigungsdienst** Zum Erstellen und Verwalten von Warnungen und Erinnerungen verwenden Sie PSI-Methoden in der [WebSvcNotifications.Notifications](https://msdn.microsoft.com/library/WebSvcNotifications.Notifications.aspx)-Klasse. 
    
- **ObjectLinkProvider-Dienst** Zum Erstellen und Verwalten von Webobjekten und Links zu Dokumenten und SharePoint-Listenelementen verwenden Sie PSI-Methoden in der [WebSvcObjectLinkProvider.ObjectLinkProvider](https://msdn.microsoft.com/library/WebSvcObjectLinkProvider.ObjectLinkProvider.aspx)-Klasse. 
    
- **PortfolioAnalyses-Dienst** Zum Erstellen und Verwalten von Projektportfolioanalysen, einschließlich Planer- und Optimierungslösungen, verwenden Sie PSI-Methoden in der [WebSvcPortfolioAnalyses.PortfolioAnalyses](https://msdn.microsoft.com/library/WebSvcPortfolioAnalyses.PortfolioAnalyses.aspx)-Klasse. 
    
- **QueueSystem-Dienst** Das CSOM kann grundlegende Informationen zu Project Server-Warteschlangenaufträgen abrufen und umfasst die [ProjectContext.WaitForQueue](https://msdn.microsoft.com/library/Microsoft.ProjectServer.Client.ProjectContext.WaitForQueue.aspx)-Methode. Verwenden Sie für eine umfangreichere Verwaltung des Project Server-Warteschlangensystems PSI-Methoden in der [WebSvcQueueSystem.QueueSystem](https://msdn.microsoft.com/library/WebSvcQueueSystem.QueueSystem.aspx)-Klasse. 
    
- **Sicherheitsdienst** Zum Erstellen und Verwalten von Project Server-Sicherheitsgruppen, -Vorlagen und -Kategorien und zum Überprüfen der Berechtigungen für den aktuellen Benutzer verwenden Sie PSI-Methoden in der [WebSvcSecurity.Security](https://msdn.microsoft.com/library/WebSvcSecurity.Security.aspx)-Klasse. 
    
- **WssInterop-Dienst** Zum Abrufen von Informationen zu Projektwebsites und zum Verwalten verwenden Sie PSI-Methoden in der [WebSvcWssInterop.WssInterop](https://msdn.microsoft.com/library/WebSvcWssInterop.WssInterop.aspx)-Klasse. 
    
    > [!NOTE]
    > Sie können das CSOM in SharePoint Server 2013 verwenden. Projektwebsites sind SharePoint-Websites. 
  
Das CSOM aktiviert keine Erweiterungen, die die PSI beispielsweise haben kann. Wenn Sie zum Beispiel eine PSI-Erweiterung für die lokale Verwendung erstellen, kann das CSOM nicht so geändert werden, dass es die PSI-Erweiterung verwendet. Sie können Erweiterungsszenarios auf andere Art und Weise implementieren:
  
- Sammeln Sie CSOM-Aufrufe in einer lokalen Komponente oder in einer Komponente, die auf Microsoft Azure ausgeführt wird.
    
- Verwenden Sie OData-Abfragen der Berichtsdaten anstatt direkt auf Berichtstabellen in der Project Server-Datenbank zuzugreifen.
    
- Integrieren Sie CSOM-Aufrufe mit Drittanbieteranwendungen über OAuth-Authentifizierung von Project Online oder mit serverseitigen Komponenten für die lokale Verwendung.
    
- Anwendungen, die das CSOM verwenden, können auch benutzerdefinierte Datenbanken entweder lokal oder mit SQL Azure verwenden.
    
### <a name="request-limits-of-the-csom"></a>Anforderungslimits des CSOM
<a name="pj15_WhatTheCSOM_RequestLimits"> </a>

Das CSOM in Project Server 2013 basiert auf der CSOM-Implementierung in SharePoint Server 2013 und erbt die Grenzwerte für die maximale Größe einer Anforderung. SharePoint weist eine Grenze von 2 MB für eine Vorgangsanforderung auf, und eine Grenze von 50 MB für die Größe eines übermittelten binären Objekts. Die Anforderungsgröße ist beschränkt, um den Server vor übermäßig langen Warteschlangen mit Vorgängen und vor Verarbeitungsverzögerungen für große binäre Objekte zu schützen.
  
Wenn Sie beispielsweise das CSOM zum Erstellen eines Projekts verwenden und dann das Projekt so bearbeiten, dass 252 Aufgaben mit einer minimalen Menge von Informationen hinzugefügt werden, z. B. ein kurzer Name, die Aufgaben-GUID und eine Dauer von 1d, so beträgt die Gesamtmenge von Daten in der **DraftProject.Update**-Anforderung weniger als 2 MB. Wenn Sie aber versuchen, 253 solche Aufgaben zu einem leeren Projekt hinzuzufügen, wird die Grenze von 2 MB überschritten, und Sie erhalten die folgende Ausnahme: **Microsoft.SharePoint.Client.ServerException: Die Anforderung verwendet zu viele Ressourcen.**
  
Um die Daten in einer CSOM-Anforderung über HTTP oder HTTPS zu erfassen, können Sie ein Webdebuggingtool verwenden, z. B. [Fiddler](https://www.fiddler2.com) (https://www.fiddler2.com). Ein Codebeispiel, das einen Test für die Größe der Anforderung implementiert und eine Lösung enthält, die eine große Anforderung in kleinere Gruppen unterteilt, finden Sie unter [DraftProject.Update](https://msdn.microsoft.com/library/Microsoft.ProjectServer.Client.DraftProject.Update.aspx) . 
  
## <a name="see-also"></a>Siehe auch
<a name="pj15_WhatTheCSOM_AR"> </a>

- [Clientseitiges Objektmodell (CSOM) für Project Server](client-side-object-model-csom-for-project-2013.md)
    
- [Was die PSI durchführen kann und was nicht](what-the-psi-does-and-does-not-do.md)
    
- [Microsoft.ProjectServer.Client](https://msdn.microsoft.com/library/Microsoft.ProjectServer.Client.aspx)
    

