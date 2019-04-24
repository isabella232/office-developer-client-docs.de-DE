---
title: Was die PSI durchführen kann und was nicht
manager: soliver
ms.date: 09/17/2015
ms.audience: Developer
localization_priority: Normal
ms.assetid: eac6be6a-9a20-4bc0-8da2-b2fd93aab04f
description: Die Project Server-Schnittstelle (PSI) kann bei der Automatisierung zahlreicher Server seitiger Prozesse in lokalen Installationen von Project Server 2013 helfen. Mehrere Funktionen erfordern jedoch die Verwendung von Microsoft Project Professional 2013.
ms.openlocfilehash: b93c3535ca6693a84d11370de17bc18375f168ab
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32346529"
---
# <a name="what-the-psi-does-and-does-not-do"></a>Was die PSI durchführen kann und was nicht

Die Project Server-Schnittstelle (PSI) kann bei der Automatisierung zahlreicher Server seitiger Prozesse in lokalen Installationen von Project Server 2013 helfen. Mehrere Funktionen erfordern jedoch die Verwendung von Microsoft Project Professional 2013.
  
|||
|:-----|:-----|
|||
   
Die PSI wurde entwickelt, um die Funktionen von Project Professional 2013 zu ergänzen, statt eine serverbasierte Alternative für alle Project Professional-Funktionen bereitzustellen. Drittanbieterentwickler können das PSI verwenden, um Webparts für lokale Installationen von Project Web App und Projektarbeitsbereichen zu erstellen, benutzerdefinierte Windows-Anwendungen und Webanwendungen zu erstellen, die mit lokalen Project Server-Daten interagieren, Workflow zu entwickeln. Logik für die Projektportfolio Verwaltung, entwickeln Sie lokale voll vertrauenswürdige Ereignishandler, und integrieren Sie Project Server in andere Anwendungen. Das PSI kann nicht für die Entwicklung von Apps für den Office Store, für mobile Geräte oder Tablets verwendet werden. dafür können Sie das clientseitige Objektmodell (CSOM) verwenden.
  
> [!NOTE]
> Das PSI bietet eine umfassendere programmgesteuerte Schnittstelle für Project Server 2013 als die CSOM bereitstellt. Es wird jedoch empfohlen, dass Sie die CSOM verwenden, um neue Anwendungen zu entwickeln, es sei denn, der CSOM bietet nicht die von Ihnen benötigte Funktionalität. Weitere Informationen finden Sie unter Funktionsweise [des CSOM und nicht](what-the-csom-does-and-does-not-do.md). 
  
## <a name="usage-scenarios-for-the-psi"></a>Nutzungsszenarien für die PSI
<a name="pj14_WhatPSIDoes_UsageScenarios"> </a>

Im folgenden finden Sie einige Beispiele für Anwendungen, die von der PSI für serverseitige Projekte und Berechnungen unterstützt werden:
  
- **Automatisieren der Erstellung oder Verwaltung von Entitäten in Project Server** Obwohl Project Professional 2013 und Project Web App zusammen entworfen wurden, um die Verwaltung und Erstellung von Entitäten wie Projekten, Enterprise-Ressourcen und benutzerdefinierten Feldern zu behandeln, gibt es oft Fälle, in denen eine benutzerdefinierte Anwendung Zeit mit Massen-oder wiederkehrende Aufträge. Das PSI kann mehrere Arten von Aufträgen automatisieren, die das CSOM nicht ausführt, beispielsweise mit OLAP-Cubes, Projektportfolio Analysen, Geschäfts Treibern, Benachrichtigungen, Objekt Verknüpfungs Anbietern, Sicherheit und SharePoint-Interoperabilität. 
    
- **Abrufen von Daten in den veröffentlichten oder Archivtabellen der Project-Datenbank** Da der direkte Datenbankzugriff auf die Entwurfs-, Veröffentlichungs-und Archivtabellen nicht unterstützt wird, können Sie die PSI zum Lesen von Daten verwenden, die in den Berichtstabellen oder-Ansichten nicht verfügbar sind. Holen Sie sich beispielsweise Informationen zu Projektversionen, Datumsangaben und Änderungen, die in den Archivtabellen gespeichert sind, und füllen Sie dann ein JS Grid-Steuerelement in einem Webpart mit den Informationen. 
    
- Über **prüfen des Status und der Arbeitszeittabellendaten** Verwenden Sie die PSI in lokalen vor-Ereignishandlern, um den Zuordnungsstatus oder die Arbeitszeittabellendaten zu überprüfen, die Benutzer eingeben, bevor die Daten in Project Web App gespeichert werden. 
    
- **Wartungsprojekte**: Erstellen Sie Platzhalterprojekte für die Verwendung mit Ressourcenplänen. Reservieren oder buchen Sie Zeit gegen Ressourcen für Wartungsarbeiten oder grundlegende Geschäftsvorgänge. Wartungsprojekte weisen normalerweise keine Aufgaben auf. 
    
- **Erstellen von Finanzprojekten**: Erstellen Sie Projekte für Zeiterfassung über die Arbeitszeittabelle für die Integration in ein Finanzsystem. Erstellen Sie eine Hierarchie von Finanzsystemcodes, die die Struktur der Kostenaufschlüsselung des Finanzsystems wiedergeben. Für Finanzprojekte sind keine Zeitplanungs- oder Statusaktualisierungen erforderlich. 
    
- **Integration in Nachverfolgungssysteme**: Erfassen Sie die Ressourcenkosten und Ausgaben, die mit Projekten verknüpft sind, um Finanz- und Abrechnungssystemen Informationen zur Verfügung zu stellen und um Budgetvergleiche auszuführen. Synchronisieren Sie Vorgänge, Ressourcen und Zuweisungen zwischen den Systemen. Erfassen Sie Arbeitszeittabellendaten in einem System, um die Daten dem anderen System zur Verfügung zu stellen (welche Arbeitszeittabelle verwendet wird, hängt von den Anforderungen der Organisation oder der einzelnen Projekte ab). 
    
- **Automatisieren von Aktualisierungen von Teammitgliedern**: Für Projekte, die nicht aktiv verwaltet werden, aktualisieren Sie automatisch Projekte auf dem Server mithilfe von Informationen von Teammitgliedern zu Fortschritt und anderen Änderungen. Projekte können aktualisiert und neu veröffentlicht werden, ohne dass ein Projektmanager die Ergebnisse überprüft oder Anpassungen am Plan vornimmt. 
    
- **Auswerten von Project Server-Daten in lokalen voll vertrauenswürdigen Ereignishandlern** Ein lokaler Ereignishandler für das **ProjectCreating** -Pre-Event kann Project Server-Daten aus dem PSI verwenden, um zu ermitteln, ob ein Ereignis abgebrochen werden soll. Vergleichen Sie zum Beispiel vor dem Erstellen eines Projekts den Projektvorschlag mit vorhandenen Projekten. 
    
- **Erstellen benutzerdefinierter Workflowaktivitäten für das Bedarfsmanagement** Verwenden Sie die PSI in lokalen, voll vertrauenswürdigen Workflowaktivitäten, um Projektvorschläge basierend auf Enterprise-Projektvorlagen zu ändern und zu aktualisieren. Verwenden Sie benutzerdefinierte Project-Felder, um das Projekt mit Informationen zu versehen, die für den Initiierungs-und Genehmigungsprozess benötigt werden. Fügen Sie Aufgaben zum Identifizieren von Projektphasen für wichtige Meilensteine oder Projektergebnisse hinzu. Wenn Projektvorschläge genehmigt werden, kann ein Workflow die Vorschläge in vollständige Projekte ändern, die mit Project Professional verwaltet werden. 
    
- **PSI-Erweiterungen erstellen** (**Veraltet.** Erweiterungen sind in Project Server 2013 veraltet und werden in zukünftigen Versionen nicht unterstützt.) Die PSI kann mithilfe der Windows Communication Foundation (WCF)-Schnittstelle mit benutzerdefinierten Diensten erweitert werden. PSI-Erweiterungen werden auf dem Project Server-Computer ausgeführt und können dieselbe Sicherheitsinfrastruktur verwenden, die von den integrierten PSI-Diensten verwendet wird. Erweiterungen können die Berichtstabellen Abfragen, separate Datenbanktabellen verwenden, PSI-Aufrufe konsolidieren, um Bandbreite zu sparen und mit Drittanbieteranwendungen und anderen serverseitigen Komponenten zu integrieren. Weitere Informationen finden Sie unter [developING PSI Extensions](https://msdn.microsoft.com/library/1b484623-94fb-47c9-84c1-3e68a9133042%28Office.15%29.aspx).
    
- **Verwenden des Identitätswechsels in lokalen, voll vertrauenswürdigen Anwendungen** Aufrufe an die WCF-Schnittstelle der PSI können imitiert werden, sodass eine Anwendung die Sicherheitsberechtigungen des imitierten Benutzers übernimmt. Der Identitätswechsel sollte sparsam und vorsichtig verwendet werden. Das Lesen und Aktualisieren von Statusinformationen für andere Benutzer erfordert keinen Identitätswechsel. Neue Anwendungen, die Identitätswechsel erfordern, sollten die CSOM und das OAuth-Protokoll anstelle der PSI verwenden. Weitere Informationen zum Identitätswechsel mit dem PSI finden Sie unter [use Impersonation with WCF](https://msdn.microsoft.com/library/e3597901-2f02-44a2-8076-d32aae540b38%28Office.15%29.aspx).
    
> [!NOTE]
> In einigen Fällen kann das PSI in Clientanwendungen mit dem CSOM und Project Online verwendet werden. Wenn Sie einen ASMX-basierten PSI-Webdienst verwenden, muss die Anwendung eine Methode zum Authentifizieren des [Microsoft. projectserver. Client. projectcontext](https://msdn.microsoft.com/library/Microsoft.ProjectServer.Client.ProjectContext.aspx) -Objekts in der CSOM und eine Methode zum Authentifizieren des ** System. Web. Services. Protocols. SoapHttpClientProtocol** -Clientobjekt. Ein Beispiel, in dem ein Webdienst mit der SharePoint-CSOM verwendet wird, finden Sie unter [Remote Authentication in SharePoint Online using Claims-Based Authentication](https://msdn.microsoft.com/library/49067f7a-3020-478f-ba97-4b7ce3ea9b87%28Office.15%29.aspx). > aufgrund der eingeschränkten Berechtigungen auf App-Ebene kann das PSI nicht in Apps verwendet werden, die für die Verteilung im öffentlichen Office Store entwickelt wurden. In diesem Fall können Sie nur die CSOM verwenden. 
  
## <a name="what-the-psi-does-not-do"></a>Was die PSI nicht tut
<a name="pj14_WhatPSIDoes_DoesNotDo"> </a>

Zwar gibt es viele Dinge, die das PSI ausführen kann, aber es gibt einige Dinge, die das PSI nicht tut. Im folgenden finden Sie zwei Dinge, die das PSI nicht kann, aber die CSOM ausführen kann.
  
### <a name="project-online-and-remote-event-receivers"></a>Project Online-und Remoteereignis Empfänger

Die primäre Einschränkung der PSI ist mit Project online. Für Anwendungen, die das PSI verwenden, ist der voll vertrauenswürdige Zugriff auf eine lokale Installation von Project Server erforderlich. Die PSI kann beispielsweise nicht in Remoteereignis Empfängern verwendet werden, in denen der Ereignis Receiver als Dienst in Microsoft Azure installiert wird.
  
### <a name="workflows-and-claims-authentication"></a>Workflows und Anspruchsauthentifizierung

Eine Workflowdefinition, die Windows Workflow Foundation, Version 4 (WF4) verwendet, erfordert die Forderungsauthentifizierung, die von der PSI nicht direkt unterstützt wird. Das PSI kann daher nicht zum Erstellen eines Projekts in Project Server 2013 mit einem Enterprise-Projekttyp (EPT) mit einer WF4-Workflowdefinition verwendet werden.
  
Sie können die PSI verwenden, um Projekte mit EPTs zu erstellen, die entweder keinen Workflow besitzen oder eine Legacy-WF 3.5-Definition verwenden (die Workflow Version in Project Server 2010). Wenn Sie ein Projekt mit einer EPT mit einer WF4-Definition erstellen möchten, verwenden Sie die CSOM.
  
 **Aktionen, die Project Professional erfordern:**
  
Die folgende Liste ist Dinge, die weder die PSI noch die CSOM ausführen können.
  
#### <a name="local-data"></a>Lokale Daten

- Bearbeiten von Daten in lokalen Projekten (MPP-Dateien). Beispiel: Definieren von Kostensatztabellen oder Verfügbarkeits Konturen für lokale Ressourcen. 
    
- Definieren oder Bearbeiten von lokalen Basiskalendern oder Ressourcenkalendern, einschließlich Kalenderausnahmen.
    
- Definieren lokaler benutzerdefinierter Felder. (Die PSI unterstützt das Bearbeiten lokaler benutzerdefinierter Feldwerte für Vorgänge, Ressourcen und Zuordnungen.)
    
#### <a name="enterprise-data"></a>Enterprise-Daten

- AusChecken oder Bearbeiten der Enterprise-Global-Projektvorlage. Die Enterprise-Global-Daten in Project Server 2013 sind eine Reihe von binären Datentabellen in der Projektdatenbank, keine Projektvorlage wie in Office Project Server 2007 und früheren Versionen.
    
- Definieren oder Bearbeiten von Enterprise-Kalendern. Die [Calendar](https://msdn.microsoft.com/library/WebSvcCalendar.Calendar.aspx) -Methoden verwalten nur Kalenderausnahmen. 
    
#### <a name="master-projects-and-cross-project-links"></a>Hauptprojekte und projektübergreifende Verknüpfungen

- Erstellen von Hauptprojekten und Einfügen von Teilprojekten.
    
- Planen eines kritischen Pfads in einem Hauptprojekt 
    
- Erstellen projektübergreifender Verknüpfungen.
    
#### <a name="resources"></a>Ressourcen

- Anfordern oder Durchführen des Ressourcenabgleichs.
    
- Ändern der Ressource für eine Zuordnung. (Sie können die PSI verwenden, um die Zuordnung zu löschen und eine neue zu erstellen.)
    
- Löschen oder Ersetzen einer Ressource, die tatsächliche Arbeit akzeptiert hat (aktuelle Werte).
    
- Ändern eines Ressourcentyps zwischen Arbeit, Material und Kosten.
    
- Erstellen oder Bearbeiten von Ressourcenkalendern.
    
- Beim Hinzufügen einer Ressource zu einem Vorgang wird die Arbeitsweise von Project Professional nicht automatisch neu verteilt. Es ist Aufgabe des Entwicklers, die Arbeitsverteilung für die Zuordnungen auszuwählen und explizit festzulegen.
    
#### <a name="cost-resources"></a>Kostenressourcen

- Bearbeiten, erstellen oder Löschen von Kostenressourcen und Zuordnungen mithilfe der [Project](https://msdn.microsoft.com/library/WebSvcProject.Project.aspx) -Methoden. Mit den [Ressourcen](https://msdn.microsoft.com/library/WebSvcResource.Resource.aspx) Methoden können Kostenressourcen erstellt, aber nicht bearbeitet werden. 
    
#### <a name="work-contours"></a>Arbeits Konturen

- Bearbeiten von Zeitphasendaten.
    
    > [!NOTE]
    > Die [UpdateStatus](https://msdn.microsoft.com/library/WebSvcStatusing.Statusing.UpdateStatus.aspx) -Methode im **Statusing** -Webdienst kann Zeitphasen-Istwerte für Zuordnungen bearbeiten, nachdem der Projektmanager die Zuordnungsdaten aktualisiert und veröffentlicht hat. 
  
- Festlegen oder Ändern des Typs der Zuordnungs Kontur (beispielsweise flach, rückwärts geladen oder Front-loaded).
    
#### <a name="baselines-and-earned-value"></a>Basispläne und Ertragswert

- Speichern einer Baseline oder Bearbeiten von Basisdaten. 
    
- Festlegen eines Fortschrittsdatums.
    
- Berechnen von Varianz und Ertragswert. 
    
#### <a name="interactive-scheduling"></a>InterAktiver Terminplan

- Unterstützen der interaktiven Planung. (Da Project Server die Interaktionen asynchron verarbeitet, sollte die interaktive Planung mit Project Professional durchgeführt werden.)
    
    > [!NOTE]
    > Um eine Änderung des programmgesteuerten Verhaltens zu vermeiden, fungieren die PSI-Methoden, die von Project Server 2010 weitergeleitet werden, in Project Server 2013 auf die gleiche Weise. [Queue](https://msdn.microsoft.com/library/WebSvcProject.Project.QueueUpdateProject.aspx) hat beispielsweise weiterhin die gleichen Einschränkungen und verwendet das ältere serverseitige Planungsmodul. Die neue [Methode queueupdateproject2](https://msdn.microsoft.com/library/WebSvcProject.Project.QueueUpdateProject2.aspx) -Methode entfernt viele dieser Einschränkungen und verwendet das neue serverseitige Planungsmodul von project Server 2013, bei dem es sich um das gleiche Planungsmodul in project Professional 2013 handelt. 
  
#### <a name="wbs"></a>WBS

- Definieren eines Projektstrukturplan-Codeformats (PSP). 
    
#### <a name="tasks"></a>Aufgaben

- Ändern des Vorgangstyps (Feste Arbeit, Dauer oder Einheiten)
    
- Ändern, ob ein Vorgang leistungsgesteuert ist.
    
- Änderung der festgelegten Kosten Abgrenzung.
    
- Ändern des Inhalts des [TASK_NOTES](https://msdn.microsoft.com/library/WebSvcProject.ProjectDataSet.TaskRow.TASK_NOTES.aspx) -Felds. Die PSI kann nur den Text Teil der Aufgaben Notizen lesen, die binäre RTF-Daten sind. Sie können jedoch Zuordnungsnotizen ( [ASSN_NOTES](https://msdn.microsoft.com/library/WebSvcProject.ProjectDataSet.AssignmentRow.ASSN_NOTES.aspx) ) bearbeiten, die Textdaten sind. Die Berichtsdatenbank enthält keine Aufgaben-oder Zuordnungsnotizen. 
    
- Erstellen oder Bearbeiten von wiederkehrenden Vorgängen.
    
- Zuweisen oder Ändern des Vorgangskalenders für vorhandene Vorgänge.
    
- Erstellen einer neuen Aufgabe mit einem Vorgangskalender.
    
- Ändern des Werts des [TASK_IGNORES_RES_CAL](https://msdn.microsoft.com/library/WebSvcProject.ProjectDataSet.TaskRow.TASK_IGNORES_RES_CAL.aspx) -Felds (Vorgangs ignoriert Ressourcenkalender). 
    
- Ändern des aktiven Status einer Aufgabe mithilfe von [Queue](https://msdn.microsoft.com/library/WebSvcProject.Project.QueueUpdateProject.aspx) , wenn im selben Aufruf zusätzliche Änderungen vorgenommen werden. Weitere Informationen finden Sie im Abschnitt *Projektplanung auf dem Server* in [Project Server-Programmierbarkeit](project-server-programmability.md).
    
#### <a name="summary-tasks"></a>Sammelvorgänge

- Erstellen oder Ändern von Zuordnungen für Sammelvorgänge.
    
    > [!NOTE]
    > Es wird empfohlen, keine Zuordnungen für Sammelvorgänge in Project Professional oder auf andere Weise vorzunehmen. Weitere Informationen finden Sie im Abschnitt *Projektplanung auf dem Server* in [Project Server-Programmierbarkeit](project-server-programmability.md). 
  
- Bearbeiten von Sammelvorgangs Feldern, die normalerweise aus dem Teilvorgang rollupiert werden. Server seitige Projekte Rollup zusammenfassende Informationen, anstatt Informationen über den Sammelvorgang festzulegen und ihn auf die Teilvorgänge zu verschieben. Sie können nur die folgenden Felder für Sammelvorgänge bearbeiten:
    
  - Anordnungsbeziehungen
    
  - Benutzerdefinierte Felder ohne Formel
    
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
    
Für den Projektsammelvorgang sind die PSI-Einschränkungen identisch mit Project Professional. Das PSI kann Budget Zuordnungen bearbeiten, einschließlich Kostenbudgets.
  
#### <a name="project-level-calculation-options"></a>Berechnungsoptionen auf Projektebene

- Ändern eines Projekttyps zwischen schedule from Start (SFS) und schedule from Finish (SFF). (Das PSI kann ein Projekt entweder als SFS oder als SFF erstellen, aber nach der Erstellung kann es nur in Project Professional geändert werden.)
    
- Ändern des Projektbasis Kalenders ([CAL_UID](https://msdn.microsoft.com/library/WebSvcProject.ProjectDataSet.ProjectRow.CAL_UID.aspx) ) nach der Projekterstellung. 
    
- Ändern von Optionen für Berechnungen. Sie können die PSI verwenden, um die folgenden Berechnungsoptionen festzulegen, wenn das Projekt erstellt wird, aber die Änderung der Optionen erfordert Project Professional. (Wählen Sie in der backstaging-Ansicht **Optionen**aus, und wählen Sie dann im Dialogfeld **Projektoptionen** die Registerkarte **Zeitplan** aus.) 
    
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
    

