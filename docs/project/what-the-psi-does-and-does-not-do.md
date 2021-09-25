---
title: Was die PSI durchführen kann und was nicht
manager: soliver
ms.date: 09/17/2015
ms.audience: Developer
ms.localizationpriority: medium
ms.assetid: eac6be6a-9a20-4bc0-8da2-b2fd93aab04f
description: Die Project Serverschnittstelle (PSI) kann dazu beitragen, viele serverseitige Prozesse in lokalen Installationen von Project Server 2013 zu automatisieren. Für mehrere Funktionen ist jedoch die Verwendung von Microsoft Project Professional 2013 erforderlich.
ms.openlocfilehash: dc81b4d559191368bf1c651fb8ea777d9d3bbe47
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59628983"
---
# <a name="what-the-psi-does-and-does-not-do"></a>Was die PSI durchführen kann und was nicht

Die Project Serverschnittstelle (PSI) kann dazu beitragen, viele serverseitige Prozesse in lokalen Installationen von Project Server 2013 zu automatisieren. Für mehrere Funktionen ist jedoch die Verwendung von Microsoft Project Professional 2013 erforderlich.
  
|||
|:-----|:-----|
|||
   
Das PSI ist so konzipiert, dass es die Funktionen von Project Professional 2013 ergänzt, anstatt eine serverbasierte Alternative für alle Project Professional Funktionen bereitzustellen. Drittanbieterentwickler können die PSI verwenden, um Webparts für lokale Installationen von Project Web App- und Projektarbeitsbereichen zu erstellen, benutzerdefinierte Windows Anwendungen und Webanwendungen zu erstellen, die mit lokalen Project Serverdaten interagieren, Workflowlogik für das Projektportfoliomanagement entwickeln, lokale voll vertrauenswürdige Ereignishandler entwickeln und Project Server in andere Anwendungen integrieren. Die PSI kann nicht für die Entwicklung von Apps für die Office Store, mobile Geräte oder Tablets verwendet werden. Dazu können Sie das clientseitige Objektmodell (CSOM) verwenden.
  
> [!NOTE]
> Die PSI bietet eine umfassendere programmgesteuerte Schnittstelle für Project Server 2013 als das CSOM. Es wird jedoch empfohlen, das CSOM zum Entwickeln neuer Anwendungen zu verwenden, es sei denn, das CSOM stellt nicht die erforderlichen Funktionen bereit. Weitere Informationen finden Sie unter [What the CSOM does and does not do](what-the-csom-does-and-does-not-do.md). 
  
## <a name="usage-scenarios-for-the-psi"></a>Verwendungsszenarien für die PSI
<a name="pj14_WhatPSIDoes_UsageScenarios"> </a>

Es folgen Beispiele für einige Anwendungen, die die PSI für serverseitige Projekte und Berechnungen unterstützt:
  
- **Automatisieren der Erstellung oder Verwaltung von Entitäten in Project Server** Obwohl Project Professional 2013 und Project Web App zusammen für die Verwaltung und Erstellung von Entitäten wie Projekten, Unternehmensressourcen und benutzerdefinierten Feldern konzipiert sind, gibt es häufig Fälle, in denen eine benutzerdefinierte Anwendung Zeit mit Massenaufträgen oder wiederholten Aufträgen sparen kann. Die PSI kann mehrere Arten von Aufträgen automatisieren, die das CSOM nicht ausführt, z. B. mit OLAP-Cubes, Projektportfolioanalysen, Geschäftstreibern, Benachrichtigungen, Objektlinkanbietern, Sicherheit und SharePoint Interoperabilität. 
    
- **Abrufen von Daten in den veröffentlichten oder Archivtabellen der Project-Datenbank** Da der direkte Datenbankzugriff auf die Entwurfs-, Veröffentlichungs- und Archivtabellen nicht unterstützt wird, können Sie die PSI verwenden, um Daten zu lesen, die in den Berichtstabellen oder -ansichten nicht verfügbar sind. Rufen Sie beispielsweise Informationen zu Projektversionen, Datumsangaben und Änderungen ab, die in den Archivtabellen gespeichert sind, und füllen Sie dann ein JS Grid-Steuerelement in einem Webpart mit den Informationen auf. 
    
- **Überprüfen der Statuserfassung und Arbeitszeittabellendaten** Verwenden Sie die PSI in lokalen Vorereignishandlern, um den Zuweisungsstatus oder die Arbeitszeittabellendaten zu überprüfen, die Benutzer eingeben, bevor die Daten in Project Web App gespeichert werden. 
    
- **Wartungsprojekte**: Erstellen Sie Platzhalterprojekte für die Verwendung mit Ressourcenplänen. Reservieren oder buchen Sie Zeit gegen Ressourcen für Wartungsarbeiten oder grundlegende Geschäftsvorgänge. Wartungsprojekte weisen normalerweise keine Aufgaben auf. 
    
- **Erstellen von Finanzprojekten**: Erstellen Sie Projekte für Zeiterfassung über die Arbeitszeittabelle für die Integration in ein Finanzsystem. Erstellen Sie eine Hierarchie von Finanzsystemcodes, die die Struktur der Kostenaufschlüsselung des Finanzsystems wiedergeben. Für Finanzprojekte sind keine Zeitplanungs- oder Statusaktualisierungen erforderlich. 
    
- **Integration in Nachverfolgungssysteme**: Erfassen Sie die Ressourcenkosten und Ausgaben, die mit Projekten verknüpft sind, um Finanz- und Abrechnungssystemen Informationen zur Verfügung zu stellen und um Budgetvergleiche auszuführen. Synchronisieren Sie Vorgänge, Ressourcen und Zuweisungen zwischen den Systemen. Erfassen Sie Arbeitszeittabellendaten in einem System, um die Daten dem anderen System zur Verfügung zu stellen (welche Arbeitszeittabelle verwendet wird, hängt von den Anforderungen der Organisation oder der einzelnen Projekte ab). 
    
- **Automatisieren von Aktualisierungen von Teammitgliedern**: Für Projekte, die nicht aktiv verwaltet werden, aktualisieren Sie automatisch Projekte auf dem Server mithilfe von Informationen von Teammitgliedern zu Fortschritt und anderen Änderungen. Projekte können aktualisiert und neu veröffentlicht werden, ohne dass ein Projektmanager die Ergebnisse überprüft oder Anpassungen am Plan vornimmt. 
    
- **Auswerten Project Serverdaten in lokalen voll vertrauenswürdigen Ereignishandlern** Ein lokaler Ereignishandler für das **ProjectCreating-Vorabereignis** kann Project Serverdaten aus der PSI verwenden, um zu bestimmen, ob ein Ereignis abgebrochen werden soll. Vergleichen Sie zum Beispiel vor dem Erstellen eines Projekts den Projektvorschlag mit vorhandenen Projekten. 
    
- **Erstellen benutzerdefinierter Workflowaktivitäten für das Bedarfsmanagement** Verwenden Sie die PSI in lokalen, voll vertrauenswürdigen Workflowaktivitäten, um Projektvorschläge basierend auf Enterprise-Projektvorlagen zu ändern und zu aktualisieren. Verwenden Sie benutzerdefinierte Projektfelder, um das Projekt mit Informationen zu markieren, die für den Initiierungs- und Genehmigungsprozess erforderlich sind. Fügen Sie Aufgaben zum Identifizieren von Projektphasen für wichtige Meilensteine oder Projektergebnisse hinzu. Wenn Projektvorschläge genehmigt werden, kann ein Workflow die Vorschläge in umfassende Projekte umwandeln, die mit Project Professional verwaltet werden. 
    
- **Psi-Erweiterungen erstellen** (**veraltet.** Erweiterungen sind in Project Server 2013 veraltet und werden in zukünftigen Versionen nicht unterstützt.) Die PSI kann mithilfe der Windows Communication Foundation (WCF)-Schnittstelle mit benutzerdefinierten Diensten erweitert werden. PSI-Erweiterungen werden auf dem Project Servercomputer ausgeführt und können dieselbe Sicherheitsinfrastruktur wie die integrierten PSI-Dienste verwenden. Erweiterungen können die Berichtstabellen abfragen, separate Datenbanktabellen verwenden, PSI-Aufrufe konsolidieren, um Bandbreite zu sparen, und in Drittanbieteranwendungen und andere serverseitige Komponenten integrieren. Weitere Informationen finden Sie unter [Entwickeln von PSI-Erweiterungen.](https://msdn.microsoft.com/library/1b484623-94fb-47c9-84c1-3e68a9133042%28Office.15%29.aspx)
    
- **Verwenden des Identitätswechsels in lokalen, voll vertrauenswürdigen Anwendungen** Aufrufe der WCF-Schnittstelle der PSI können imitiert werden, sodass eine Anwendung von den Sicherheitsberechtigungen des imitierten Benutzers ausgeht. Der Identitätswechsel sollte sparsam und sorgfältig verwendet werden. Das Lesen und Aktualisieren von Statusinformationen für andere Benutzer erfordert keinen Identitätswechsel. Neue Anwendungen, die einen Identitätswechsel erfordern, sollten das CSOM und das OAuth-Protokoll anstelle der PSI verwenden. Weitere Informationen zum Identitätswechsel mit der PSI finden Sie unter [Verwenden des Identitätswechsels mit WCF.](https://msdn.microsoft.com/library/e3597901-2f02-44a2-8076-d32aae540b38%28Office.15%29.aspx)
    
> [!NOTE]
> In einigen Fällen kann die PSI in Clientanwendungen mit dem CSOM und Project Online verwendet werden. Wenn Sie einen ASMX-basierten PSI-Webdienst verwenden, muss die Anwendung eine Methode zum Authentifizieren des [Microsoft.ProjectServer.Client.ProjectContext-Objekts](https://msdn.microsoft.com/library/Microsoft.ProjectServer.Client.ProjectContext.aspx) im CSOM und eine Methode zum Authentifizieren des **System.Web.Services.Protocols.SoapHttpClientProtocol-Clientobjekts** enthalten. Ein Beispiel, das einen Webdienst mit dem SharePoint CSOM verwendet, finden Sie unter [Remoteauthentifizierung in SharePoint Online unter Verwendung der anspruchsbasierten Authentifizierung.](https://msdn.microsoft.com/library/49067f7a-3020-478f-ba97-4b7ce3ea9b87%28Office.15%29.aspx) > Aufgrund eingeschränkter Berechtigungen auf App-Ebene kann die PSI nicht in Apps verwendet werden, die für die Verteilung in der öffentlichen Office Store entwickelt wurden. In diesem Fall können Sie nur das CSOM verwenden. 
  
## <a name="what-the-psi-does-not-do"></a>Was die PSI nicht tut
<a name="pj14_WhatPSIDoes_DoesNotDo"> </a>

Obwohl die PSI viele Möglichkeiten hat, gibt es einige Dinge, die die PSI nicht ausführt. Es folgen zwei Dinge, die die PSI nicht ausführen kann, aber das CSOM kann dies tun.
  
### <a name="project-online-and-remote-event-receivers"></a>Project Online und Remoteereignisempfänger

Die primäre Beschränkung der PSI liegt bei Project Online. Anwendungen, die die PSI verwenden, erfordern voll vertrauenswürdigen Zugriff auf eine lokale Installation von Project Server. Beispielsweise kann die PSI nicht in Remoteereignisempfängern verwendet werden, in denen der Ereignisempfänger als Dienst auf Microsoft Azure installiert ist.
  
### <a name="workflows-and-claims-authentication"></a>Workflows und Anspruchsauthentifizierung

Eine Workflowdefinition, die Windows Workflow Foundation Version 4 (WF4) verwendet, erfordert eine Anspruchsauthentifizierung, die die PSI nicht direkt unterstützt. Dies bedeutet, dass Sie die PSI nicht verwenden können, um ein Projekt in Project Server 2013 zu erstellen, das über einen Enterprise-Projekttyp (EPT) mit einer WF4-Workflowdefinition verfügt.
  
Sie können die PSI verwenden, um Projekte mit EPTs zu erstellen, die entweder keinen Workflow haben oder eine ältere WF3.5-Definition verwenden (die Workflowversion in Project Server 2010). Verwenden Sie das CSOM, um ein Projekt mit einer EPT mit einer WF4-Definition zu erstellen.
  
 **Aktionen, die Project Professional erfordern:**
  
Die folgende Liste enthält Dinge, die weder die PSI noch das CSOM ausführen können.
  
#### <a name="local-data"></a>Lokale Daten

- Bearbeiten von Daten in lokalen Projekten (MPP-Dateien). Beispielsweise definieren Sie Kostensatztabellen oder Verfügbarkeitskonturen für lokale Ressourcen. 
    
- Definieren oder Bearbeiten von lokalen Basiskalendern oder Ressourcenkalendern, einschließlich Kalender ausnahmen.
    
- Definieren lokaler benutzerdefinierter Felder. (Die PSI unterstützt das Bearbeiten lokaler benutzerdefinierter Feldwerte für Vorgänge, Ressourcen und Zuordnungen.)
    
#### <a name="enterprise-data"></a>Enterprise-Daten

- Auschecken oder Bearbeiten der Enterprise-Global-Vorlage. Die Enterprise-Global-Daten in Project Server 2013 sind eine Gruppe von Binärdatentabellen in der Project-Datenbank und keine Projektvorlage wie in Office Project Server 2007 und früheren Versionen.
    
- Definieren oder Bearbeiten von Unternehmenskalendern. Die [Kalendermethoden](https://msdn.microsoft.com/library/WebSvcCalendar.Calendar.aspx) verwalten nur Kalender-Ausnahmen. 
    
#### <a name="master-projects-and-cross-project-links"></a>Masterprojekte und projektübergreifende Verknüpfungen

- Erstellen von Hauptprojekten und Einfügen von Teilprojekten.
    
- Planen eines kritischen Pfads für ein Hauptprojekt. 
    
- Erstellen projektübergreifender Verknüpfungen.
    
#### <a name="resources"></a>Ressourcen

- Anfordern oder Ausführen des Ressourcen-Abgleichs.
    
- Ändern der Ressource für eine Zuordnung. (Sie können die PSI verwenden, um die Zuordnung zu löschen und eine neue zu erstellen.)
    
- Löschen oder Ersetzen einer Ressource, für die die aktuelle Arbeit akzeptiert wurde (ist).
    
- Ändern eines Ressourcentyps zwischen Arbeit, Material und Kosten.
    
- Erstellen oder Bearbeiten von Ressourcenkalendern.
    
- Beim Hinzufügen einer Ressource zu einem Vorgang verteilt die PSI die Arbeit nicht automatisch wie Project Professional. Der Entwickler muss die Arbeitsverteilung für die Zuordnungen auswählen und explizit festlegen.
    
#### <a name="cost-resources"></a>Kostenressourcen

- Bearbeiten, Erstellen oder Löschen von Kostenressourcen und Zuordnungen mithilfe der [Project](https://msdn.microsoft.com/library/WebSvcProject.Project.aspx) Methoden. Die [Ressourcenmethoden](https://msdn.microsoft.com/library/WebSvcResource.Resource.aspx) können Kostenressourcen erstellen, aber nicht bearbeiten. 
    
#### <a name="work-contours"></a>Arbeitskonturen

- Bearbeiten von Zeitphasendaten.
    
    > [!NOTE]
    > Die [UpdateStatus-Methode](https://msdn.microsoft.com/library/WebSvcStatusing.Statusing.UpdateStatus.aspx) im **Statuserfassungswebdienst** kann aktuelle Zeitphasen für Zuordnungen bearbeiten, nachdem der Projektmanager die Zuordnungsdaten aktualisiert und veröffentlicht hat. 
  
- Festlegen oder Ändern des Zuweisungskonturtyps (z. B. flach, zurückgeladen oder vorne geladen).
    
#### <a name="baselines-and-earned-value"></a>Basispläne und Ertragswert

- Speichern einer Basislinie oder Bearbeiten von Basisplandaten. 
    
- Festlegen eines Statusdatums.
    
- Berechnen der Varianz und des Ertragswerts. 
    
#### <a name="interactive-scheduling"></a>Interaktive Planung

- Unterstützung der interaktiven Planung. (Da Project Server Interaktionen asynchron verarbeitet, sollte die interaktive Planung mit Project Professional erfolgen.)
    
    > [!NOTE]
    > Um programmgesteuertes Verhalten zu vermeiden, verhalten sich die PSI-Methoden, die von Project Server 2010 übertragen werden, in Project Server 2013 auf die gleiche Weise. [QueueUpdateProject](https://msdn.microsoft.com/library/WebSvcProject.Project.QueueUpdateProject.aspx) hat beispielsweise weiterhin die gleichen Einschränkungen und verwendet das ältere serverseitige Planungsmodul. Die neue [QueueUpdateProject2-Methode](https://msdn.microsoft.com/library/WebSvcProject.Project.QueueUpdateProject2.aspx) entfernt viele dieser Einschränkungen und verwendet das neue serverseitige Planungsmodul Project Server 2013, das dasselbe Planungsmodul wie in Project Professional 2013 ist. 
  
#### <a name="wbs"></a>WBS

- Definieren eines PSP-Codeformats (Work Breakdown Structure). 
    
#### <a name="tasks"></a>Aufgaben

- Ändern des Vorgangstyps (feste Arbeit, Dauer oder Einheiten).
    
- Ändern, ob eine Aufgabe leistungsgesteuert ist.
    
- Ändern der Fixkostenabgrenzung des Vorgangs.
    
- Ändern des Inhalts des [TASK_NOTES](https://msdn.microsoft.com/library/WebSvcProject.ProjectDataSet.TaskRow.TASK_NOTES.aspx) Felds. Die PSI kann nur den Textteil der Aufgabenhinweise lesen, bei denen es sich um RTF-Binärdaten handelt. Sie können jedoch Zuordnungsnotizen ( [ASSN_NOTES](https://msdn.microsoft.com/library/WebSvcProject.ProjectDataSet.AssignmentRow.ASSN_NOTES.aspx) ) bearbeiten, bei denen es sich um Textdaten handelt. Die Berichtsdatenbank enthält keine Aufgaben- oder Zuweisungsnotizen. 
    
- Erstellen oder Bearbeiten von wiederkehrenden Aufgaben.
    
- Zuweisen oder Ändern des Aufgabenkalenders für vorhandene Vorgänge.
    
- Erstellen einer neuen Aufgabe mit einem Aufgabenkalender.
    
- Ändern des Werts des [TASK_IGNORES_RES_CAL](https://msdn.microsoft.com/library/WebSvcProject.ProjectDataSet.TaskRow.TASK_IGNORES_RES_CAL.aspx) Felds (Vorgang ignoriert Ressourcenkalender). 
    
- Ändern des aktiven Status eines Vorgangs mithilfe von [QueueUpdateProject,](https://msdn.microsoft.com/library/WebSvcProject.Project.QueueUpdateProject.aspx) wenn im gleichen Aufruf weitere Änderungen vorgenommen werden. Weitere Informationen finden Sie im Abschnitt *Project Planung auf dem Server* unter Project [Serverprogrammierbarkeit.](project-server-programmability.md)
    
#### <a name="summary-tasks"></a>Sammelvorgänge

- Erstellen oder Ändern von Zuordnungen für Sammelvorgänge.
    
    > [!NOTE]
    > Es wird empfohlen, keine Zuordnungen für Sammelvorgänge mit Project Professional oder auf andere Weise durchzuführen. Weitere Informationen finden Sie im Abschnitt *Project Planung auf dem Server* unter Project [Serverprogrammierbarkeit.](project-server-programmability.md) 
  
- Bearbeiten von Sammelvorgangsfeldern, die normalerweise aus dem Teilvorgang rolliert werden. Serverseitige Projekte führen immer ein Rollup der Zusammenfassungsinformationen durch, anstatt Informationen für den Sammelvorgang festzulegen und an die Teilvorgänge weiterzuschieben. Sie können nur die folgenden Felder für Sammelvorgänge bearbeiten:
    
  - Anordnungsbeziehungen
    
  - Benutzerdefinierte Felder ohne Formeln
    
  - [TASK_NAME](https://msdn.microsoft.com/library/WebSvcProject.ProjectDataSet.TaskRow.TASK_NAME.aspx)
    
  - [TASK_OUTLINE_LEVEL](https://msdn.microsoft.com/library/WebSvcProject.ProjectDataSet.TaskRow.TASK_OUTLINE_LEVEL.aspx)
    
  - [TASK_IS_MARKED](https://msdn.microsoft.com/library/WebSvcProject.ProjectDataSet.TaskRow.TASK_IS_MARKED.aspx)
    
  - [TASK_CONSTRAINT_TYPE](https://msdn.microsoft.com/library/WebSvcProject.ProjectDataSet.TaskRow.TASK_CONSTRAINT_TYPE.aspx)
    
  - [TASK_CONSTRAINT_DATE](https://msdn.microsoft.com/library/WebSvcProject.ProjectDataSet.TaskRow.TASK_CONSTRAINT_DATE.aspx)
    
  - [TASK_PRIORITY](https://msdn.microsoft.com/library/WebSvcProject.ProjectDataSet.TaskRow.TASK_PRIORITY.aspx)
    
  - [TASK_DEADLINE](https://msdn.microsoft.com/library/WebSvcProject.ProjectDataSet.TaskRow.TASK_DEADLINE.aspx)
    
  - [TASK_FIXED_COST](https://msdn.microsoft.com/library/WebSvcProject.ProjectDataSet.TaskRow.TASK_FIXED_COST.aspx)
    
  - [TASK_FIXED_COST_ACCRUAL](https://msdn.microsoft.com/library/WebSvcProject.ProjectDataSet.TaskRow.TASK_FIXED_COST_ACCRUAL.aspx) (legen Sie den Wert nur beim Erstellen der Aufgabe fest) 
    
  - [TASK_WBS](https://msdn.microsoft.com/library/WebSvcProject.ProjectDataSet.TaskRow.TASK_WBS.aspx)
    
Für die Projektzusammenfassungsaufgabe sind die PSI-Einschränkungen die gleichen wie für Project Professional. Die PSI kann Budgetzuweisungen bearbeiten, einschließlich Kostenbudgets.
  
#### <a name="project-level-calculation-options"></a>Berechnungsoptionen auf Project Ebene

- Ändern eines Projekttyps zwischen Schedule From Start (SFS) und Schedule From Finish (SFF). (Die PSI kann ein Projekt entweder als SFS oder als SFF erstellen, aber nachdem es erstellt wurde, kann es nur in Project Professional geändert werden.)
    
- Ändern des Projektbasiskalenders ([CAL_UID](https://msdn.microsoft.com/library/WebSvcProject.ProjectDataSet.ProjectRow.CAL_UID.aspx) ) nach der Projekterstellung. 
    
- Änderungsoptionen für Berechnungen. Sie können die PSI verwenden, um die folgenden Berechnungsoptionen festzulegen, wenn das Projekt erstellt wird, aber das Ändern der Optionen erfordert Project Professional. (Wählen Sie in der Backstage-Ansicht **Optionen** und dann im Dialogfeld **Project Optionen** die Registerkarte **"Zeitplan"** aus.) 
    
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
    

