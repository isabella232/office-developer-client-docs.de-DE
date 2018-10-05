---
title: Was die PSI durchführen kann und was nicht
manager: soliver
ms.date: 09/17/2015
ms.audience: Developer
localization_priority: Normal
ms.assetid: eac6be6a-9a20-4bc0-8da2-b2fd93aab04f
description: Project Server Interface (PSI) kann zum Automatisieren viele serverseitigen Prozessen in lokale Installationen von Project Server 2013 helfen. Aber einige Funktionen erfordern die Verwendung von Microsoft Project Professional 2013.
ms.openlocfilehash: b93c3535ca6693a84d11370de17bc18375f168ab
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/04/2018
ms.locfileid: "25386341"
---
# <a name="what-the-psi-does-and-does-not-do"></a>Was die PSI durchführen kann und was nicht

Project Server Interface (PSI) kann zum Automatisieren viele serverseitigen Prozessen in lokale Installationen von Project Server 2013 helfen. Aber einige Funktionen erfordern die Verwendung von Microsoft Project Professional 2013.
  
|||
|:-----|:-----|
|||
   
Die PSI dient als Ergänzung der Funktionen von Project Professional 2013, statt eine serverbasierte Alternative für alle Project Professional-Funktionen bereitzustellen. Drittanbieter-Entwickler können Sie Webparts für lokale Installationen von Project Web App und Projektarbeitsbereiche erstellen, erstellen Sie benutzerdefinierte Windows und Webanwendungen, die Interaktion mit lokalen Project Server-Daten, Entwickeln von Workflows unterstützen die PSI Logik für Project Portfoliomanagement lokale Ereignishandler voll vertrauenswürdige entwickeln und Integrieren von Project Server mit einer anderen Anwendung. Die PSI kann nicht für die Entwicklung von apps für Office Store, mobile Geräte oder Tablets verwendet werden. Hierzu können Sie das Client-seitigen Objektmodell (CSOM) verwenden.
  
> [!NOTE]
> Die PSI enthält eine umfassendere Programmierschnittstelle für Project Server 2013 als das CSOM bereitgestellt. Aber, es sei denn, das CSOM nicht die Funktionalität, die Sie benötigen bereitstellen, es wird empfohlen, dass Sie das CSOM verwenden, um neue Anwendungsentwicklung. Weitere Informationen finden Sie unter [Was das CSOM ist und nicht zu](what-the-csom-does-and-does-not-do.md). 
  
## <a name="usage-scenarios-for-the-psi"></a>Verwendungsszenarien für die PSI
<a name="pj14_WhatPSIDoes_UsageScenarios"> </a>

Im folgenden sind Beispiele für einige Anwendungen, die die PSI für serverseitige Projekte und Berechnungen unterstützt:
  
- **Automatisieren der Erstellung oder Verwaltung von Entitäten in Project Server** Project Professional 2013 und Project Web App zusammen sind ausgelegt, verwalten und Erstellen von Entitäten wie Projekte, Enterprise-Ressourcen und benutzerdefinierte Felder behandeln, oftmals stehen Fällen, in eine benutzerdefinierte Anwendung Sie Zeit mit Massen sparen kann, oder sich wiederholende Aufträge. Die PSI kann verschiedene Arten von Aufträgen, die dem Clientobjektmodell keine, z. B. mit OLAP-Cubes, Project Portfolioanalysen, von betriebswirtschaftlichen Faktoren, Benachrichtigungen, Object Link Provider, Sicherheit und SharePoint-Interoperabilität automatisieren. 
    
- **Abrufen von Daten in der veröffentlichten oder Archivtabellen der Project-Datenbank** Da Datenbank direkt den Zugriff auf den Entwurf, veröffentlicht, und archivieren Tabellen wird nicht unterstützt, können Sie die PSI zum Lesen von Daten, die in die reporting Tabellen oder Ansichten nicht verfügbar ist. Beispielsweise erhalten Sie Informationen zu Projektversionen, Datumsangaben und Änderungen, die in den Archivtabellen gespeichert sind, und füllen Sie dann eine JS Grid-Steuerelement in einem Webpart mit den Informationen. 
    
- **Überprüfen von Zeitberichte und Arbeitszeittabellen-Daten** Verwenden Sie die PSI Zuordnungsdaten Status oder Arbeitszeittabellen-Warteschlange überprüfen, die Benutzer eingeben, bevor die Daten in Project Web App gespeichert werden, in lokalen Pre-Event Handler. 
    
- **Wartungsprojekten** Erstellen Sie Platzhalter Projekte mit Ressourcenpläne verwenden. Reservieren oder Adressbuch Zeit mit Ressourcen für Wartungsarbeiten oder Basis Business. Wartungsprojekten müssen nicht im allgemeinen Aufgaben. 
    
- **Finanzielle Projekte erstellen** Erstellen Sie Projekte für die Erfassung der Zeit über die Arbeitszeittabelle für die Integration mit einem finanzielle System. Erstellen einer Hierarchie von finanziellen Codes, die die Kosten des Ressourcenstrukturplans Struktur des Systems finanzielle widerspiegeln. Finanzielle Projekte erfordern keinen planen oder Status Updates. 
    
- **Integration mit Buchhaltungssystemen** Erfassen Sie die Ressourcenkosten und Ausgaben im Zusammenhang mit Projekten Feed Systeme finanzielle und zur Abrechnung und zu Vergleichszwecken Budget. Synchronisieren von Aufgaben, Ressourcen und Zuordnungen zwischen den Systemen. Erfassen von Daten in Arbeitszeittabellen in einem System zum anderen feed (verwendet wird, welche Arbeitszeittabelle hängt von den Anforderungen der Organisation oder von einzelnen Projekten). 
    
- **Automatisieren von Updates von Teammitgliedern** Aktualisieren Sie für Projekte, die nicht aktiv verwaltet werden automatisch Projekte auf dem Server mit des Fortschritts und der andere Änderungen von Projektteammitgliedern. Projekte können aktualisiert und ohne ein Projektmanager Überprüfen der Ergebnisse oder Anpassungen an den Plan erneut veröffentlicht werden. 
    
- **Bewerten der Project Server-Daten in die lokale Ereignishandler voll vertrauenswürdige** Ein lokale Ereignishandler für das **ProjectCreating** vor dem Ereignis kann Project Server-Daten aus der PSI verwenden, um zu bestimmen, ob ein Ereignis abgebrochen. Vergleichen Sie vor dem Erstellen eines Projekts, beispielsweise den Projektvorschlag mit vorhandenen Projekten. 
    
- **Erstellen benutzerdefinierter Workflowaktivitäten für das bedarfsmanagement** Verwenden Sie die PSI in lokale, voll vertrauenswürdige Workflowaktivitäten zum Ändern und Aktualisieren von Projektvorschlägen wird basierend auf Enterprise-Projektvorlagen. Verwenden Sie benutzerdefinierte Projektfelder, markieren Sie das Projekt mit den Informationen, die für die Initiierung und Genehmigung Prozess benötigt. Hinzufügen von Aufgaben aus, um das Projektphasen für wichtige Meilensteine oder Lieferumfang zu identifizieren. Wenn Projektvorschlägen genehmigt werden, kann ein Workflow ändern, Vorschläge in umfassende Projekte, die verwaltet werden mit Project Professional. 
    
- **Erstellen von PSI-Erweiterungen** (**Veraltet.** Erweiterungen in Project Server 2013 veraltet sind, und werden in zukünftigen Versionen nicht unterstützt.) Die PSI kann mit benutzerdefinierte Dienste mithilfe der Windows Communication Foundation (WCF)-Schnittstelle erweitert werden. PSI-Erweiterungen führen Sie auf der Project Server-Computer, und verwenden Sie die gleichen Sicherheitsinfrastruktur, die der integrierten PSI-Dienste verwenden können. Extensions können reporting Abfragetabellen, verwenden Sie separate Datenbanktabellen, konsolidieren PSI-Aufrufe Bandbreite zu speichern, und drittanbieteranwendungen und andere serverseitige Komponenten integriert. Weitere Informationen finden Sie unter [Entwickeln von PSI-Erweiterungen](https://msdn.microsoft.com/library/1b484623-94fb-47c9-84c1-3e68a9133042%28Office.15%29.aspx).
    
- **Verwenden des Identitätswechsels in lokalen, voll vertrauenswürdige Anwendungen** Aufrufe der WCF-Schnittstelle von der PSI können nicht imitiert werden, damit eine Anwendung die Sicherheitsberechtigungen des Benutzers, dessen Identität verwendet wird davon ausgegangen. Identitätswechsel sollte sparsame und sorgfältig verwendet werden. Lesen und Aktualisieren von Statusinformationen für andere Benutzer ist kein Identitätswechsel erforderlich. Neue Anwendungen, die ein Identitätswechsel erforderlich sein sollte das CSOM und OAuth-Protokolls anstelle der PSI verwenden. Weitere Informationen zum Identitätswechsel mit der PSI finden Sie unter [Verwenden des Identitätswechsels mit WCF](https://msdn.microsoft.com/library/e3597901-2f02-44a2-8076-d32aae540b38%28Office.15%29.aspx).
    
> [!NOTE]
> In einigen Fällen kann die PSI in Clientanwendungen mit dem CSOM und Project Online verwendet werden. Wenn Sie einen ASMX-basierte PSI-Webdienst verwenden, muss die Anwendung eine Methode zum Authentifizieren des [Microsoft.ProjectServer.Client.ProjectContext](https://msdn.microsoft.com/library/Microsoft.ProjectServer.Client.ProjectContext.aspx) -Objekts in der CSOM und eine Methode zum Authentifizieren der **enthalten System.Web.Services.Protocols.SoapHttpClientProtocol** Clientobjekt. Ein Beispiel, die einen Webdienst mit der SharePoint-CSOM verwendet, finden Sie unter [Remoteauthentifizierung in SharePoint Online Using Claims-Based Authentifizierung](https://msdn.microsoft.com/library/49067f7a-3020-478f-ba97-4b7ce3ea9b87%28Office.15%29.aspx). > Die PSI aufgrund von eingeschränkten app-Berechtigungen kann nicht verwendet werden in apps, die entworfen wurden, für die Verteilung in den öffentlichen Office Store. In diesem Fall können Sie nur das CSOM verwenden. 
  
## <a name="what-the-psi-does-not-do"></a>Was die PSI nicht zu
<a name="pj14_WhatPSIDoes_DoesNotDo"> </a>

Obwohl es viele Dinge, die die PSI möglich ist gibt, sind einige Dinge, die die PSI nicht der Fall ist. Es folgen zwei Dinge die PSI nicht möglich, aber das CSOM möglich.
  
### <a name="project-online-and-remote-event-receivers"></a>Project Online und remote-Ereignisempfänger

Die primäre Einschränkung des die PSI ist mit Project Online. Clientanwendungen, die die PSI verwenden erfordern voll vertrauenswürdige Zugriff auf eine lokale Installation von Project Server. Beispielsweise kann nicht die PSI in remote-Ereignisempfänger, verwendet werden, auf dem der Ereignisempfänger als in Windows Azure-Dienst installiert.
  
### <a name="workflows-and-claims-authentication"></a>Workflows und Anspruchsauthentifizierung

Eine Workflowdefinition verwendet, die Windows Workflow Foundation der Version 4 (WF4) Forderungsauthentifizierung, die die PSI nicht direkt unterstützt wird. Dies bedeutet, dass Sie die PSI verwenden können, um ein Projekt in Project Server 2013 erstellen, die Enterprise-Projekttyp (EPT) mit einer Workflowdefinition WF4 hat.
  
Die PSI können zum Erstellen von Projekten mit EPTs, die entweder keine Workflows oder verwenden Sie eine Vorversion WF3.5 Definition (die Workflowversion in Project Server 2010). Zum Erstellen eines Projekts mit einer EPT, die eine Definition WF4 hat, verwenden Sie das CSOM.
  
 **Aktionen, die Project Professional erfordern:**
  
In der folgenden Liste sind die Aufgaben, die PSI weder das CSOM erledigen kann.
  
#### <a name="local-data"></a>Lokale Daten

- Bearbeiten von Daten in lokalen Projekte (MPP-Dateien). Definieren beispielsweise Kostensatztabellen oder Verfügbarkeit Konturen für lokale Ressourcen. 
    
- Definieren oder Bearbeiten lokaler Basiskalender oder Ressourcenkalender, einschließlich Kalenderausnahmen.
    
- Lokale benutzerdefinierte Felder definieren. (Die PSI bietet Unterstützung für lokales benutzerdefiniertes Feldwerte auf Aufgaben, Ressourcen und Zuordnungen bearbeiten.)
    
#### <a name="enterprise-data"></a>Enterprise-Daten

- Auszuchecken, oder bearbeiten die Enterprise-global-Vorlage. Die Enterprise-global-Daten in Project Server 2013 ist eine Reihe von Binärdaten Tabellen in der Project-Datenbank keine Projektvorlage in Office Project Server 2007 und früheren Versionen.
    
- Definieren oder Bearbeiten von Enterprise-Kalender. Die Methoden [Kalender](https://msdn.microsoft.com/library/WebSvcCalendar.Calendar.aspx) verwalten nur Kalenderausnahmen. 
    
#### <a name="master-projects-and-cross-project-links"></a>Hauptprojekte und projektübergreifenden Verknüpfungen

- Erstellen von Hauptprojekten und Teilprojekten einfügen.
    
- Planen einen kritischen Weg über eines Hauptprojekts. 
    
- Erstellen von projektübergreifenden Verknüpfungen.
    
#### <a name="resources"></a>Ressourcen

- Anfordern oder Kapazitätsabgleich durchführen.
    
- Ändern die Ressource bei einer Zuordnung. (Sie können die PSI löschen die Zuordnung, und erstellen Sie einen neuen Anwendungspool.)
    
- Löschen oder Ersetzen eine Ressource, die aktuelle Arbeit wurde angenommen (aktuelle Werte).
    
- Ändern der Ressourcentyp zwischen Arbeit, Material und Kosten.
    
- Erstellen oder Bearbeiten von Ressourcenkalender.
    
- Wenn Sie eine Ressource mit einer Aufgabe hinzufügen, die PSI wird nicht automatisch verteilt die Funktionsweise Project Professional ist. Es ist Aufgabe des Entwicklers zum auswählen und die Verteilung der Arbeit explizit für die Zuordnungen festlegen.
    
#### <a name="cost-resources"></a>Kostenressourcen

- Bearbeiten, erstellen oder Löschen von Kostenressourcen und Zuordnungen mithilfe der [Project](https://msdn.microsoft.com/library/WebSvcProject.Project.aspx) -Methoden. Die [Ressource](https://msdn.microsoft.com/library/WebSvcResource.Resource.aspx) Methoden Kostenressourcen erstellt, aber nicht bearbeitet werden. 
    
#### <a name="work-contours"></a>Arbeit Konturen

- Bearbeiten von Zeitphasendaten mit.
    
    > [!NOTE]
    > Die [UpdateStatus](https://msdn.microsoft.com/library/WebSvcStatusing.Statusing.UpdateStatus.aspx) -Methode in den **Statusing** -Webdienst kann aktuelle Werte mit Zeitphasen für Zuordnungen bearbeiten, nachdem der Projektmanager aktualisiert und die Zuordnungsdaten veröffentlicht. 
  
- Festlegen oder Ändern der Zuordnung Kontur Typs (beispielsweise flach, Back-geladen oder vorn zugängliche).
    
#### <a name="baselines-and-earned-value"></a>Baselines und Ertragswert

- Einen Basisplan speichern, oder bearbeiten Basisdaten. 
    
- Wenn ein Datum ausgeführt.
    
- Berechnung Varianz und Ertragswert. 
    
#### <a name="interactive-scheduling"></a>Interaktive planen

- Unterstützung für interaktive planen. (, Da es sich bei Project Server Interaktionen asynchron verarbeitet, sollte interaktive Planung mit Project Professional erfolgen.)
    
    > [!NOTE]
    > Zum Ändern des Verhaltens von programmgesteuerten vermeiden fungieren die PSI-Methoden, die von Project Server 2010 Forward geschaltet werden die gleiche Weise wie in Project Server 2013. Beispielsweise, [QueueUpdateProject](https://msdn.microsoft.com/library/WebSvcProject.Project.QueueUpdateProject.aspx) weiterhin hat die gleichen Einschränkungen und ältere serverseitige Planungsmodul verwendet. Die neue [QueueUpdateProject2](https://msdn.microsoft.com/library/WebSvcProject.Project.QueueUpdateProject2.aspx) -Methode entfernt viele diese Einschränkungen und verwendet die neue Project Server 2013 serverseitige Zeitplanungsmodul, die sich gleichen Planungsmodul handelt, das in Project Professional 2013 ist. 
  
#### <a name="wbs"></a>WBS

- Definieren eine Codemaske für Arbeit des Ressourcenstrukturplans (Projektstrukturplan). 
    
#### <a name="tasks"></a>Aufgaben

- Ändern den Aufgabentyp (Feste Arbeit, Dauer und Einheiten).
    
- Ändern, ob ein Vorgang leistungsgesteuert ist.
    
- Vorgangsfeld feste Kosten Fälligkeit ändern.
    
- Ändern den Inhalt des Felds [TASK_NOTES](https://msdn.microsoft.com/library/WebSvcProject.ProjectDataSet.TaskRow.TASK_NOTES.aspx) . Die PSI kann nur den Text in die Vorgangsnotizen lesen, in denen RTF binäre Daten sind. Jedoch können Sie Zuordnungsnotizen ( [ASSN_NOTES](https://msdn.microsoft.com/library/WebSvcProject.ProjectDataSet.AssignmentRow.ASSN_NOTES.aspx) ), die Text-Daten sind bearbeiten. Die Berichtsdatenbank enthält keinen Vorgang oder eine Zuordnung Notizen. 
    
- Erstellen oder Bearbeiten von sich wiederholenden Tasks.
    
- Zuweisen oder das Ändern des Vorgangskalenders auf vorhandene Aufgaben.
    
- Erstellen eine neue Aufgabe mit einem Vorgangskalenders.
    
- Ändern den Wert des Felds [TASK_IGNORES_RES_CAL](https://msdn.microsoft.com/library/WebSvcProject.ProjectDataSet.TaskRow.TASK_IGNORES_RES_CAL.aspx) (Aufgabe ignoriert Ressourcenkalender). 
    
- Ändern des aktiven Status eines Vorgangs mit [QueueUpdateProject](https://msdn.microsoft.com/library/WebSvcProject.Project.QueueUpdateProject.aspx) , falls zusätzliche Änderungen in einem Anruf vorgenommen werden. Weitere Informationen finden Sie im Abschnitt *Project Scheduling auf dem Server* in [Project Server-Programmierbarkeit](project-server-programmability.md).
    
#### <a name="summary-tasks"></a>Sammelvorgänge

- Erstellen oder Ändern von Zuordnungen auf Sammelvorgänge dar.
    
    > [!NOTE]
    > Es wird empfohlen, dass Sie keine Zuordnungen mit Project Professional oder beliebige andere Weise Sammelvorgänge treffen. Weitere Informationen finden Sie im Abschnitt *Project Scheduling auf dem Server* in [Project Server-Programmierbarkeit](project-server-programmability.md). 
  
- Bearbeiten der Felder für Sammelvorgang, die normalerweise aus der Teilvorgang Sammelvorgängen durchgeführt wird. Serverseitige Projekte Sammelvorgängen immer zusammenfassende Informationen, anstelle von Informationen für den Sammelvorgang festlegen und ihn nach unten zu den Teilvorgängen pushen. Sie können nur die folgenden Felder auf Sammelvorgänge bearbeiten:
    
  - Anordnungsbeziehungen
    
  - Benutzerdefinierte Felder für nicht-Formel
    
  - [TASK_NAME](https://msdn.microsoft.com/library/WebSvcProject.ProjectDataSet.TaskRow.TASK_NAME.aspx)
    
  - [TASK_OUTLINE_LEVEL](https://msdn.microsoft.com/library/WebSvcProject.ProjectDataSet.TaskRow.TASK_OUTLINE_LEVEL.aspx)
    
  - [TASK_IS_MARKED](https://msdn.microsoft.com/library/WebSvcProject.ProjectDataSet.TaskRow.TASK_IS_MARKED.aspx)
    
  - [TASK_CONSTRAINT_TYPE](https://msdn.microsoft.com/library/WebSvcProject.ProjectDataSet.TaskRow.TASK_CONSTRAINT_TYPE.aspx)
    
  - [TASK_CONSTRAINT_DATE](https://msdn.microsoft.com/library/WebSvcProject.ProjectDataSet.TaskRow.TASK_CONSTRAINT_DATE.aspx)
    
  - [TASK_PRIORITY](https://msdn.microsoft.com/library/WebSvcProject.ProjectDataSet.TaskRow.TASK_PRIORITY.aspx)
    
  - [TASK_DEADLINE](https://msdn.microsoft.com/library/WebSvcProject.ProjectDataSet.TaskRow.TASK_DEADLINE.aspx)
    
  - [TASK_FIXED_COST](https://msdn.microsoft.com/library/WebSvcProject.ProjectDataSet.TaskRow.TASK_FIXED_COST.aspx)
    
  - [TASK_FIXED_COST_ACCRUAL](https://msdn.microsoft.com/library/WebSvcProject.ProjectDataSet.TaskRow.TASK_FIXED_COST_ACCRUAL.aspx) (Legen Sie den Wert nur beim Erstellen des Tasks) 
    
  - [TASK_WBS](https://msdn.microsoft.com/library/WebSvcProject.ProjectDataSet.TaskRow.TASK_WBS.aspx)
    
Für den Projektsammelvorgang sind die PSI-Einschränkungen die gleichen wie für Project Professional. Die PSI kann Budget Zuordnungen bearbeiten – einschließlich Kostenbudgets.
  
#### <a name="project-level-calculation-options"></a>Berechnungsoptionen auf Projektebene

- Ändern eines Projekttyps zwischen Zeitplan aus starten (angewendet) und Planen von Fertig stellen (SFF). (Die PSI ein Projekts als angewendet oder SFF erstellen können, aber nach der Erstellung kann nur in Project Professional geändert werden.)
    
- Ändern des Project-Basiskalenders ([CAL_UID](https://msdn.microsoft.com/library/WebSvcProject.ProjectDataSet.ProjectRow.CAL_UID.aspx) ) nach der projekterstellung. 
    
- Ändern der Optionen für die Berechnung. Die PSI können Sie die folgenden Optionen für die Berechnung festgelegt, wenn das Projekt wird erstellt, aber ändern die Optionen für Project Professional erforderlich. (In der Backstage-Ansicht, wählen Sie **Optionen**, und wählen Sie dann die Registerkarte **Terminplan** im Dialogfeld **Projektoptionen** .) 
    
  - [PROJ_OPT_CALC_ACT_COSTS](https://msdn.microsoft.com/library/WebSvcProject.ProjectDataSet.ProjectRow.PROJ_OPT_CALC_ACT_COSTS.aspx)
    
  - [PROJ_OPT_CRITICAL_SLACK_LIMIT](https://msdn.microsoft.com/library/WebSvcProject.ProjectDataSet.ProjectRow.PROJ_OPT_CRITICAL_SLACK_LIMIT.aspx)
    
  - [PROJ_OPT_HONOR_CONSTRAINTS](https://msdn.microsoft.com/library/WebSvcProject.ProjectDataSet.ProjectRow.PROJ_OPT_HONOR_CONSTRAINTS.aspx)
    
  - [PROJ_OPT_MOVE_ACTUAL_IF_LATER](https://msdn.microsoft.com/library/WebSvcProject.ProjectDataSet.ProjectRow.PROJ_OPT_MOVE_ACTUAL_IF_LATER.aspx)
    
  - [PROJ_OPT_MOVE_ACTUAL_TO_STATUS](https://msdn.microsoft.com/library/WebSvcProject.ProjectDataSet.ProjectRow.PROJ_OPT_MOVE_ACTUAL_TO_STATUS.aspx)
    
  - [PROJ_OPT_MOVE_REMAINING_IF_EARLIER](https://msdn.microsoft.com/library/WebSvcProject.ProjectDataSet.ProjectRow.PROJ_OPT_MOVE_REMAINING_IF_EARLIER.aspx)
    
  - [PROJ_OPT_MOVE_REMAINING_TO_STATUS](https://msdn.microsoft.com/library/WebSvcProject.ProjectDataSet.ProjectRow.PROJ_OPT_MOVE_REMAINING_TO_STATUS.aspx)
    
  - [PROJ_OPT_MULT_CRITICAL_PATHS](https://msdn.microsoft.com/library/WebSvcProject.ProjectDataSet.ProjectRow.PROJ_OPT_MULT_CRITICAL_PATHS.aspx)
    
  - [PROJ_OPT_SPLIT_IN_PROGRESS](https://msdn.microsoft.com/library/WebSvcProject.ProjectDataSet.ProjectRow.PROJ_OPT_SPLIT_IN_PROGRESS.aspx)
    
  - [PROJ_OPT_SPREAD_ACT_COSTS](https://msdn.microsoft.com/library/WebSvcProject.ProjectDataSet.ProjectRow.PROJ_OPT_SPREAD_ACT_COSTS.aspx)
    
  - [PROJ_OPT_SPREAD_PCT_COMP](https://msdn.microsoft.com/library/WebSvcProject.ProjectDataSet.ProjectRow.PROJ_OPT_SPREAD_PCT_COMP.aspx)
    
  - [PROJ_OPT_TASK_UPDATES_RES](https://msdn.microsoft.com/library/WebSvcProject.ProjectDataSet.ProjectRow.PROJ_OPT_TASK_UPDATES_RES.aspx)
    
## <a name="see-also"></a>Siehe auch

- [Was das CSOM durchführen kann und was nicht](what-the-csom-does-and-does-not-do.md)  
- [Project Server-Programmierbarkeit](project-server-programmability.md)   
- [Anspruchsbasierte Remoteauthentifizierung in SharePoint Online](https://msdn.microsoft.com/library/49067f7a-3020-478f-ba97-4b7ce3ea9b87%28Office.15%29.aspx)  
- [Office-Add-Ins](https://docs.microsoft.com/office/dev/add-ins/overview/office-add-ins) 
    

