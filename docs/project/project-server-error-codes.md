---
title: Project Server-Fehlercodes
manager: soliver
ms.date: 09/17/2015
ms.audience: Developer
f1_keywords:
- error codes
- errors
- Project Server errors
- PSErrorID
- PSI errors
keywords:
- PSI, Fehlercodes, Fehlercodes, Project Server, PSErrorID, Project Server Interface, Error Codes, Project Server-Fehlercodes
localization_priority: Normal
ms.assetid: db78a09c-ebef-47cc-8623-40abe117aa08
description: Dieses Thema enthält Tabellen mit Fehlercodes für Project Server Interface (PSI) in Project Server 2013. In den Tabellen werden nach Funktionsbereich und fehlercodebereich angeordnet.
ms.openlocfilehash: 7fdfafa562492fe4d5671f1335ca58cf50c91e88
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/04/2018
ms.locfileid: "25401783"
---
# <a name="project-server-error-codes"></a>Project Server-Fehlercodes

Dieses Thema enthält Tabellen mit Fehlercodes für Project Server Interface (PSI) in Project Server 2013. In den Tabellen werden nach Funktionsbereich und fehlercodebereich angeordnet.
   
Project Server 2013-Prozesse und PSI-Methoden haben Code Fehlernummern, die in der Regel von Funktionsbereich angeordnet sind. Die [Microsoft.Office.Project.Server.Library.PSErrorID](https://msdn.microsoft.com/library/microsoft.office.project.server.library.pserrorid_di_pj14mref(v=office.14).aspx) -Aufzählung wird in [WebSvcProject.PSErrorID](https://msdn.microsoft.com/library/office/websvcproject.pserrorid_di_pj14mref.aspx)dupliziert. Sie können die Fehlercodes in alphabetischer Reihenfolge nach Name aufgelistet. In diesem Thema werden die Fehlercodes in Tabellen, die von der PSI-Klasse oder Funktionsbereich und von einer Fehlernummer Bezeichner (ID) angeordnet werden. 
  
> [!NOTE]
>  Viele der Fehlercodes haben allgemeingültigen Charakter und können auf mehrere Ursachen verweisen. Gehen Sie wir folgt vor, um weitere Informationen zu Fehlern abzurufen: 
> - Verwenden Sie bei ASMX-basierten Anwendungen **System.Web.Services.Protocols.SoapException** mit dem **PSClientError**-Objekt, um eine Liste der Fehlerhierarchie in einem PSI-Methodenaufruf anzuzeigen. Weitere Informationen finden Sie im [Fehlercodebeispiel für ASMX](#pj15_ErrorCodes_ASMXExample). 
> - In WCF-basierten Anwendungen können Sie **System.ServiceModel.FaultException** verwenden, um ein **PSClientError**-Objekt und weitere Fehlerinformationen abzurufen. Weitere Informationen dazu finden Sie im [Fehlercodebeispiel für WCF](#pj15_ErrorCodes_WCFExample). 
> - Verwenden Sie das Anwendungsereignisprotokoll auf dem Project Server-Computer.
> - Verwenden Sie die Ablaufverfolgungsprotokolle Unified Logging Service (ULS). Eine Erläuterung finden Sie unter [Erste Schritte bei der Entwicklung für Project 2010](https://msdn.microsoft.com/library/gg607685.aspx)im Abschnitt *Fehler überprüfen* . 
> - Weitere Informationen zur Verwendung von ULS-Protokollen finden Sie unter Project Support-Blog-Artikel [Project Server 2010: Was Sie erwartet, wenn Sie die unerwarteten erhalten](https://blogs.msdn.com/b/brismith/archive/2010/03/24/project-server-2010-what-to-expect-when-you-get-the-unexpected.aspx), und suchen Sie im Blog für "Lesen von ULS-Protokolle." 
> - Um besser zu suchen, oder schauen Sie sich für bestimmte Probleme im ULS-Daten, mit dem [ULS Viewer](https://www.codeproject.com/Articles/458052/ULS-Log-Viewer). 
> - Verwenden Sie den Microsoft SQL Server Profiler, um Datenbankfehler zu ermitteln oder zu überwachen. Weitere Informationen finden Sie unter [SQL Server Profiler](https://msdn.microsoft.com/library/3ad5f33d-559e-41a4-bde6-bb98792f7f1a.aspx). 
> - Viele der Fehlercode werden nur intern verwendet. Beispiel: Da die Webdienste **ExchangeSync** und **PWA** eine Entwicklung durch Drittanbieter nicht unterstützen, können Sie keine Fehlercodes vom Methoden in diesen Bereichen, wie **Rules**- und **StatusReports**-Methoden anzeigen. Die Tabellen in diesem Artikel enthalten aber aus Gründen der Vollständigkeit alle Project Server-Fehlercodes. 
  
## <a name="table-1-error-code-functional-areas-and-related-number-ranges"></a>Tabelle 1. Fehlercodes - Funktionsbereiche und zugehörige Zahlenbereiche

|Project Server-Funktionsbereich|Fehlercode-Zahlenbereiche|
|:-----|:-----|
|[Tabelle 3: Allgemeine Fehlercodes](#pj15_ErrorCodes_General) <br/> |0 – 99; 500 - 999; 9131; 10000 - 10099; 20000 - 20099 auf den; 26000 - 26099  <br/> |
|[Tabelle 4: Aktiver Cache](#pj15_ErrorCodes_ActiveCache) <br/> |12000 - 12099  <br/> |
|[Tabelle 5: Active Directory-Synchronisierung](#pj15_ErrorCodes_ActiveDirectory) <br/> |27000 - 27999  <br/> |
|[Tabelle 6: Admin-Webdienst](#pj15_ErrorCodes_Admin) <br/> |16600 - 16699; 19011, 19012 und 19032; 20003 und 25000 - 25099  <br/> |
|[Tabelle 7: Archivierung (Sicherung und Wiederherstellung)](#pj15_ErrorCodes_Archive) <br/> |25000 - 25999 und 29000 - 29099  <br/> |
|[Tabelle 8: Zuordnungen](#pj15_ErrorCodes_Assignments) <br/> |120 - 199  <br/> |
|[Tabelle 9: Kalender](#pj15_ErrorCodes_Calendar) <br/> |77 und 13000 - 13999  <br/> |
|[Tabelle 10: Cube Build Service (CBS)](#pj15_ErrorCodes_CBS) <br/> |17000 - 17999  <br/> |
|[Tabelle 11: Einchecken - Auschecken](#pj15_ErrorCodes_CICO) <br/> |10100 - 10199  <br/> |
|[Tabelle 12: Benutzerdefinierte Felder](#pj15_ErrorCodes_CustomFields) <br/> |11500 - 11999  <br/> |
|[Tabelle 13: Nachschlagetabellen](#pj15_ErrorCodes_LookupTables) <br/> |11000 - 11499  <br/> |
|[Tabelle 14: Sonstige](#pj15_ErrorCodes_Miscellaneous) <br/> |11000 - 11499  <br/> |
|[Tabelle 15: Benachrichtigungen](#pj15_ErrorCodes_Notifications) <br/> |16000 - 16599  <br/> |
|[Tabelle 16: Optimierer](#pj15_ErrorCodes_Optimizer) (Projektportfolioanalyse)  <br/> |29000 - 29999  <br/> |
|[Tabelle 17: Planner](#pj15_ErrorCodes_Planner) (Projektportfolioanalyse)  <br/> |28000 - 28999  <br/> |
|[Tabelle 18: Projekte](#pj15_ErrorCodes_Projects) <br/> |100 - 499; 1000 - 1199; 9100 - 9199; und 23000 23999  <br/> |
|[Tabelle 19: Reporting Data Service](#pj15_ErrorCodes_RDS) (RDS)  <br/> |24000 - 24999  <br/> |
|[Tabelle 20: Ressourcen](#pj15_ErrorCodes_Resources) <br/> |2000 - 2999  <br/> |
|[Tabelle 21: Ressourcenpläne](#pj15_ErrorCodes_ResourcePlans) <br/> |30000 - 30999  <br/> |
|[Tabelle 22: Regeln](#pj15_ErrorCodes_Rules) <br/> |21000 - 21099  <br/> |
|[Tabelle 23: Sicherheit](#pj15_ErrorCodes_Security) <br/> |19000 - 19099  <br/> |
|[Tabelle 24: Serverereignisse](#pj15_ErrorCodes_Events) <br/> |19033 und 22000 - 22999  <br/> |
|[Tabelle 25: Statuserfassung](#pj15_ErrorCodes_Statusing) <br/> |3100 - 3199  <br/> |
|[Tabelle 26: Statusberichte](#pj15_ErrorCodes_StatusReports) <br/> |12100 - 12299  <br/> |
|[Tabelle 27: Vorgänge](#pj15_ErrorCodes_Tasks) <br/> |7000 - 7099  <br/> |
|[Tabelle 28: Arbeitszeittabellen](#pj15_ErrorCodes_Timesheets) <br/> |3200 - 3299  <br/> |
|[Tabelle 29: Benutzerstellvertretung](#pj15_ErrorCodes_UserDelegation) <br/> |43000 - 43500  <br/> |
|[Tabelle 30: Workflow](#pj15_ErrorCodes_Workflow) <br/> |35000 - 35999: Workflow  <br/> |
|[Tabelle 31: WSSInterop und ObjectLinkProvider (SharePoint-Integration)](#pj15_ErrorCodes_WSS) <br/> |16400 - 16499: SharePoint-Integration und Project-Arbeitsbereiche  <br/> 18000 - 18099: Object Link Provider und SharePoint-Projektimport  <br/> |
   
## <a name="table-2-error-code-table-by-number-range"></a>Tabelle 2. Fehlercodetabelle nach Zahlenbereich

|Fehlercodebereich|Fehlercodetabelle|
|:-----|:-----|
|0 – 99  <br/> |[Tabelle 3: Allgemeine Fehlercode](#pj15_ErrorCodes_General), mit Ausnahme von 77, der in [Tabelle 9: Kalender](#pj15_ErrorCodes_Calendar) enthalten ist <br/> |
|100 - 119  <br/> |[Tabelle 18: Projekte](#pj15_ErrorCodes_Projects) <br/> |
|120 - 199  <br/> |[Tabelle 8: Zuordnungen](#pj15_ErrorCodes_Assignments) <br/> |
|500 - 999  <br/> |[Tabelle 3: Allgemeine Fehlercodes](#pj15_ErrorCodes_General) <br/> |
|1000 - 1199  <br/> |[Tabelle 18: Projekte](#pj15_ErrorCodes_Projects) <br/> |
|2000 - 2999  <br/> |[Tabelle 20: Ressourcen](#pj15_ErrorCodes_Resources) <br/> |
|3100 - 3199  <br/> |[Tabelle 25: Statuserfassung](#pj15_ErrorCodes_Statusing) <br/> |
|3200 - 3299  <br/> |[Tabelle 28: Arbeitszeittabellen](#pj15_ErrorCodes_Timesheets) <br/> |
|7000 - 7099  <br/> |[Tabelle 27: Vorgänge](#pj15_ErrorCodes_Tasks) <br/> |
|9100 - 9199  <br/> |[Tabelle 18: Projekte](#pj15_ErrorCodes_Projects), mit Ausnahme von 9131, der in [Tabelle 3: Allgemeine Fehlercodes](#pj15_ErrorCodes_General) enthalten ist <br/> |
|10000 - 10099  <br/> |[Tabelle 3: Allgemeine Fehlercodes](#pj15_ErrorCodes_General) <br/> |
|10100 - 10199  <br/> |[Tabelle 11: Einchecken - Auschecken](#pj15_ErrorCodes_CICO) <br/> |
|11000 - 11499  <br/> |[Tabelle 13: Nachschlagetabellen](#pj15_ErrorCodes_LookupTables) <br/> |
|11500 - 11999  <br/> |[Tabelle 12: Benutzerdefinierte Felder](#pj15_ErrorCodes_CustomFields) <br/> |
|12000 - 12099  <br/> |[Tabelle 4: Aktiver Cache](#pj15_ErrorCodes_ActiveCache) <br/> |
|12100 - 12299  <br/> |[Tabelle 26: Statusberichte](#pj15_ErrorCodes_StatusReports) <br/> |
|13000 - 13999  <br/> |[Tabelle 9: Kalender](#pj15_ErrorCodes_Calendar) <br/> |
|16000 - 16399  <br/> |[Tabelle 15: Benachrichtigungen](#pj15_ErrorCodes_Notifications) <br/> |
|16400 - 16499  <br/> |[Tabelle 31: WssInterop und Object Link Provider (SharePoint-Integration)](#pj15_ErrorCodes_WSS) <br/> |
|16600 - 16699  <br/> |[Tabelle 6: Admin-Webdienst](#pj15_ErrorCodes_Admin) <br/> |
|17000 - 17999  <br/> |[Tabelle 10: Cube Build Service (CBS)](#pj15_ErrorCodes_CBS) <br/> |
|18000 - 18099  <br/> |[Tabelle 31: SharePoint-Integration](#pj15_ErrorCodes_WSS) <br/> |
|19000 - 19099  <br/> |[Tabelle 23: Sicherheit](#pj15_ErrorCodes_Security), mit Ausnahme von 19011, 19012 und 19032, die sicherheitsbezogene Codes und in [Tabelle 6: Admin-Webdienst](#pj15_ErrorCodes_Admin) enthalten sind <br/> |
|20000 - 20099 auf den  <br/> |[Tabelle 3: Allgemeine Fehlercodes](#pj15_ErrorCodes_General), mit Ausnahme von 20003, der in [Tabelle 6: Admin-Webdienst](#pj15_ErrorCodes_Admin) enthalten ist <br/> |
|21000 - 21099  <br/> |[Tabelle 22: Regeln](#pj15_ErrorCodes_Rules) <br/> |
|22000 - 22999  <br/> |[Tabelle 24: Serverereignisse](#pj15_ErrorCodes_Events) <br/> |
|23000 - 23999  <br/> |[Tabelle 18: Projekte](#pj15_ErrorCodes_Projects) <br/> |
|24000 - 24999  <br/> |[Tabelle 19: Reporting Data Service](#pj15_ErrorCodes_RDS) (RDS)  <br/> |
|25000 - 25999  <br/> |[Tabelle 7: Archivierung (Sicherung und Wiederherstellung)](#pj15_ErrorCodes_Archive), mit Ausnahme von 25004, 25006, die in [Tabelle 6: Admin-Webdienst](#pj15_ErrorCodes_Admin) enthalten sind <br/> |
|26000 - 26099  <br/> |[Tabelle 3: Allgemeine Fehlercodes](#pj15_ErrorCodes_General) <br/> |
|27000 - 27999  <br/> |[Tabelle 5: Active Directory-Synchronisierung](#pj15_ErrorCodes_ActiveDirectory) <br/> |
|28000 - 28999  <br/> |[Tabelle 17: Planner](#pj15_ErrorCodes_Planner) (Projektportfolioanalyse)  <br/> |
|29000 - 29999  <br/> |[Tabelle 16: Optimierer](#pj15_ErrorCodes_Optimizer) (Projektportfolioanalyse), mit Ausnahme von 29021, der in [Tabelle 7: Archivierung](#pj15_ErrorCodes_Archive) enthalten ist <br/> |
|30000 - 30999  <br/> |[Tabelle 21: Ressourcenpläne](#pj15_ErrorCodes_ResourcePlans) <br/> |
|31000 - 31999  <br/> 32000 - 32100  <br/> |[Tabelle 14: Sonstige](#pj15_ErrorCodes_Miscellaneous) (Überwachung; nicht verwendet)  <br/> Projektdetailseiten  <br/> |
|35000 - 35999  <br/> 40000 - 40499  <br/> |[Tabelle 30: Workflow](#pj15_ErrorCodes_Workflow) <br/> |
|40500 - 40999  <br/> 42000 - 42999  <br/> |[Tabelle 14: Sonstige](#pj15_ErrorCodes_Miscellaneous) (**ExchangeSync**; interner Gebrauch)  <br/> Zeitachse für Project Web App  <br/> |
|43000 - 43500  <br/> |[Tabelle 29: Benutzerstellvertretung](#pj15_ErrorCodes_UserDelegation) <br/> |
|50000 - 51999  <br/> |[Tabelle 14: Sonstige](#pj15_ErrorCodes_Miscellaneous) (Datenbankfehler)  <br/> |

<a name="pj15_ErrorCodes_General"></a>

## <a name="table-3-general-error-codes"></a>Tabelle 3. Allgemeine Fehlercodes

|Allgemeiner Fehlercode|Beschreibung|
|:-----|:-----|
|NoError = 0; Success = 0  <br/> |Kein Fehler oder Erfolg.  <br/> |
|GeneralRequestInvalidParameter = 6  <br/> |Einer der Anforderungsknoten oder Parameter ist entweder ungültig oder ungültig im Rahmen der Anforderung.  <br/> |
|GeneralInvalidValue = 11  <br/> |Anforderungswert ungültig; Beispiel: eine GUID wurde mit 0 angegeben.  <br/> |
|GeneralStartDateGTorEQFinishDate = 26  <br/> |Der angegebene Datumsbereich ist ungültig.  <br/> |
|GeneralQueueOperationInProcess = 29  <br/> |Generischer Fehler für einen Vorgang, der noch in der Warteschlange verarbeitet wird.  <br/> |
|GeneralUnhandledException = 42  <br/> |Eine unbehandelte Ausnahme ist eingetreten.  <br/> |
|GeneralDuplicateGUIDSpecified = 66  <br/> |Eine doppelte GUID in der Anforderung.  <br/> |
|GeneralDateNotValid = 69  <br/> |Die Datumsangaben müssen im Bereich von 1/1/1984 bis 12/12/2049 liegen.  <br/> |
|GeneralCostInvalid = 70  <br/> |Ein Kostenparameter ist ungültig.  <br/> |
|GeneralWorkInvalid = 71  <br/> |Ein Arbeitsparameter ist ungültig.  <br/> |
|GeneralDurationInvalid = 72  <br/> |Ein Dauerparameter ist ungültig.  <br/> |
|GeneralUnitsInvalid = 73  <br/> |Die angegebene Einheit ist ungültig.  <br/> |
|GeneralOnlyInsertsAllowed = 74  <br/> |Nur Einfügevorgänge sind zulässig.  <br/> |
|GeneralOnlyUpdatesAllowed = 75  <br/> |Nur Aktualisierungen sind zulässig.  <br/> |
|GeneralSessionInvalid = 76  <br/> |Der Sitzungsparameter ist ungültig.  <br/> |
|GeneralDependencyUidInvalid = 78  <br/> |Die Abhängigkeits-GUID ist ungültig.  <br/> |
|GeneralNumberInvalid = 79  <br/> |Eine Zahl ist ungültig.  <br/> |
|GeneralInvalidDataStore = 80  <br/> |Die angegebene Datenbank ist nicht vorhanden. Verwenden Sie eine Datenbank in [DataStoreEnum](https://msdn.microsoft.com/library/Microsoft.Office.Project.Server.Library.DataStoreEnum.aspx) .  <br/> |
|GeneralDurationOrWorkFormatInvalid = 513  <br/> |Die Arbeitsdauer oder das Format ist ungültig.  <br/> |
|GeneralRateFormatInvalid = 518  <br/> |Das Satzformat ist ungültig.  <br/> |
|GeneralQueueException = 9131  <br/> |Ausnahme: Allgemeiner Fehler im Queuing-Dienst.  <br/> |
|GeneralItemDoesNotExist = 10000  <br/> |Eine bestimmtes Element ist nicht vorhanden.  <br/> |
|GeneralLCIDInvalid = 10001  <br/> |Die Gebietsschema-ID (Sprach-ID) ist ungültig.  <br/> |
|GeneralRowDoesNotExist = 10002  <br/> |Die angegebene Zeile in einer **DataTable** ist nicht vorhanden.  <br/> |
|GeneralInvalidColumnValue = 20000  <br/> |Ein Spaltenwert in einer **DataTable** ist ungültig.  <br/> |
|GeneralInvalidDataRowState = 20001  <br/> |Ein **DataRow**-Status ist ungültig.  <br/> |
|GeneralDuplicatedNames = 20004  <br/> |Eine Name ist doppelt. Namen müssen eindeutig sein.  <br/> |
|GeneralReadOnlyColumn = 20005  <br/> |Die Spalte ist schreibgeschützt.  <br/> |
|GeneralReadOnlyRow = 20006  <br/> |Die Zeile ist schreibgeschützt.  <br/> |
|GeneralNotNullColumn = 20007  <br/> |Die Spalte darf nicht null sein.  <br/> |
|GeneralObjectAlreadyExists = 20008  <br/> |Das Objekt ist bereits vorhanden.  <br/> |
|GeneralInvalidObject = 20009  <br/> |Das Objekt ist ungültig.  <br/> |
|GeneralSecurityAccessDenied = 20010  <br/> |Zugriff aufgrund von Sicherheitsberechtigungen verweigert.  <br/> |
|GeneralInvalidOperation = 20011  <br/> |Der Vorgang ist ungültig.  <br/> |
|GeneralInvalidCharacters = 20012  <br/> |Einige Zeichen sind ungültig. Zusätzlich zu den Tabulatorzeichen die folgenden Zeichen sind nicht gültig in einen Projektnamen: ' \ / ":; < > | , . ' ? * #` <br/> |
|GeneralNameTooLong = 20013  <br/> |Der Name ist zu lang.  <br/> |
|GeneralNameCannotBeBlank = 20014  <br/> |Der Name darf nicht leer sein. Verwenden Sie keine Null oder eine leere Zeichenfolge.  <br/> |
|GeneralInvalidOperationOnReadOnlyValue = 20016  <br/> |Der versuchte Vorgang bei einem schreibgeschützten Wert ist ungültig.  <br/> |
|GeneralInvalidDateOverlap = 20018  <br/> |Die Anorderung enthält sich überlappende Daten.  <br/> |
|GeneralParameterCannotBeNull = 20020  <br/> |Der Parameter darf nicht null sein.  <br/> |
|GeneralDescTooLong = 20021  <br/> |Die Beschreibung ist zu lang.  <br/> |
|GeneralCategoryPermissionDenied = 20022  <br/> |Die Kategorieberechtigung wurde abgelehnt.  <br/> |
|GeneralNotLicensed = 20024  <br/> |Benutzer ist für Project Server nicht berechtigt.  <br/> |
|GeneralGlobalPermissionDenied = 20023  <br/> |Die globale Berechtigung wurde verweigert.  <br/> |
|GeneralActionCanceledByEventHandler = 22000  <br/> |Die Aktion wurde von Ereignis-Handler abgebrochen.  <br/> |
|GeneralActionCanceledBecauseServerEventServiceNotFound = 22001  <br/> |Der Project Server-Ereignisdienst wurde nicht gefunden.  <br/> |
|GeneralActionCanceledBecauseServerEventServiceProblem = 22002  <br/> |Es gibt ein Problem im Project Server-Ereignisdienst.  <br/> |
|GeneralQueueJobFailed = 26000  <br/> |Der Warteschlangenauftrag war nicht erfolgreich.  <br/> |
|GeneralQueueInvalidJobUID = 26001  <br/> |Die Auftrags-GUID ist ungültig.  <br/> |
|GeneralQueueInvalidTrackingUID = 26002  <br/> |Die Überwachungs-GUID für die Warteschlange ist ungültig.  <br/> |
|GeneralQueueInvalidJobInfoUID = 26003  <br/> |Die Auftragsinformations-GUID für die Warteschlange ist ungültig.  <br/> |
|GeneralQueueInvalidCorrelationUID = 26004  <br/> |Die Warteschlangenkorrelations-GUID ist ungültig.  <br/> |
|GeneralQueueCorrelationBlocked = 26005  <br/> |Die Warteschlangenkorrelation ist gesperrt.  <br/> |
|GeneralQueueInvalidMessageType = 26006  <br/> |Der Warteschlangennachrichtentyp ist ungültig.  <br/> |
|GeneralQueueInvalidJobState = 26007  <br/> |Der Warteschlangenauftragsstatus ist ungültig.  <br/> |
|GeneralQueueInvalidGroupState = 26008  <br/> |Der Gruppenstatus in der Warteschlange ist ungültig.  <br/> |
|GeneralQueueInvalidGroupPriority = 26009  <br/> |Die Gruppenpriorität in der Warteschlange ist ungültig.  <br/> |
|GeneralQueueInvalidCorrelationPriority = 26010  <br/> |Die Korrelationspriorität in der Warteschlange ist ungültig.  <br/> |
|GeneralQueueInvalidQueueID = 26011  <br/> |Die Warteschlangen-Kennnummer ist ungültig.  <br/> |
|GeneralQueueInvalidAdminAction = 26012  <br/> |Die **Admin**Aktion ist für die Warteschlange ungültig.  <br/> |
|GeneralQueueInvalidStatType = 26013  <br/> |Der Warteschlangenstatustyp ist ungültig.  <br/> |
|GeneralQueueInvalidBlockPolicy = 26014  <br/> |Die Richtlinie zur Warteschlangensperrung ist ungültig.  <br/> |
|GeneralQueueCannotRetryJob = 26015  <br/> |Die Warteschlange kann den Auftrag nicht erneut versuchen.  <br/> |
|GeneralQueueInvalidSetting = 26016  <br/> |Eine Einstellung für die Warteschlange ist ungültig.  <br/> |
|GeneralQueueInvalidRendezvousUID = 26017  <br/> |Die Warteschlangen-Rendezvous-GUID ist ungültig.  <br/> |
|GeneralDalErrorGettingConnectionStrings = 26018  <br/> |Fehler beim Abrufen von Verbindungszeichenfolgen für die Datenzugriffsschicht (DAL).  <br/> |
|GeneralDalErrorConnectingToDatabase = 26019  <br/> |Fehler bei der DAL-Verbindung zur Datenbank.  <br/> |
|GeneralDalInvalidArgumentCountCreatingFilter = 26020  <br/> |Die Anzahl Argumente zum Erstellen eines Filters ist ungültig.  <br/> |
|GeneralDataTableCannotBeNull = 26024  <br/> |Eine **DataTable** darf nicht **null** sein.  <br/> |
|GeneralDatasetConstraints = 26025  <br/> |Fehler in **DataSet**-Einschränkungen.  <br/> |
|GeneralInvalidDataSetStructure = 26027  <br/> |Die **DataSet**Struktur ist ungültig.  <br/> |
|GeneralDalNoRowsUpdated = 26028  <br/> |Es wurde keine Zeilen aktualisiert in der Datenzugriffsschicht (DAL).  <br/> |
|GeneralDataTableCannotBeEmpty = 26029  <br/> |Die **DataTable** darf nicht leer sein.  <br/> |
|GeneralWSSContentDBNotWritable = 26030  <br/> |In SharePoint-Inhaltsdatenbank kann nicht geschrieben werden. Entweder ist die Inhaltsdatenbank schreibgeschützt, oder es gibt eine Sperre auf Websitesammlungsebene.  <br/> |
|GeneralSPValidateFormDigestError = 26031  <br/> |Fehler beim Validieren des formulardigests in Project Web App-Callback, in der Regel aufgrund eines Timeouts.  <br/> |
|GeneralDelegationActiveForCurrentUser = 26032  <br/> |Der Benutzer hat eine aktive Stellvertretung. Dieser Fehler wird von Webmethoden im **WinProj**-Dienst für Project Professional ausgelöst.<br/> |

<a name="pj15_ErrorCodes_ActiveCache"></a>

## <a name="table-4-active-cache"></a>Tabelle 4 Aktiver cache

|Fehlercode - Aktiver Cache|Beschreibung|
|:-----|:-----|
|ActiveCacheInvalidDataFormat = 12000  <br/> |Das Datenformat ist ungültig.  <br/> |
|ActiveCacheUnsupportedDataFormatVersion = 12001  <br/> |Die Datenformatversion wird nicht unterstützt  <br/> |
|ActiveCacheInvalidQueuedMessageType = 12003  <br/> |Der Nachrichtentyp in der Warteschlange ist ungültig.  <br/> |
|ActiveCacheNullQueuedMessage = 12004  <br/> |Die Nachricht in der Warteschlange ist null.  <br/> |
|ActiveCacheQueuedMessageExecutionError = 12005  <br/> |Es gibt einen Ausnahmefehler für die Nachricht in der Warteschlange.  <br/> |
|ActiveCacheInvalidDataSize = 12006  <br/> |Die Datengröße ist ungültig.  <br/> |
|ActiveCacheQueueJobAlreadyStarted = 12007  <br/> |Der Warteschlangenauftrag wurde bereits gestartet.  <br/> |
|ActiveCacheInvalidQueuedMessageFormat = 12008  <br/> |Das Nachrichtenformat in der Warteschlange ist ungültig.  <br/> |
|ActiveCacheUnsupportedQueuedMessageVersion = 12009  <br/> |Die Nachrichtenversion in der Warteschlange ist ungültig.  <br/> |
|ActiveCacheUnsupportedQueueDataType = 12011  <br/> |Der Datentyp in der Warteschlange wird nicht unterstützt.  <br/> |
|ActiveCacheInvalidVersionStampForSave = 12012  <br/> |Der Versionsstempel für den Speicherungsvorgang ist ungültig.  <br/> |
|ActiveCacheProjectTypeMismatch = 12013  <br/> |Der Projekttyp stimmt nicht mit dem erwarteten Typ überein.  <br/> |
|ActiveCacheDataValidationFailed = 12014  <br/> |Datenüberprüfung nicht erfolgreich.  <br/> |
|ActiveCacheUnsupportedProjectProfessionalVersion = 12015  <br/> |Die Project Professional-Version wird nicht unterstützt.  <br/> |
|ActiveCacheGeneralSQLException = 12016  <br/> |Allgemeiner SQL-Fehler.  <br/> |

<a name="pj15_ErrorCodes_ActiveDirectory"></a>

## <a name="table-5-active-directory-synchronization"></a>Tabelle 5 Active Directory-Synchronisierung

|Fehlercode - Active Directory-Synchronisierung|Beschreibung|
|:-----|:-----|
|AdSyncUpdateTimerJobFailed = 27002  <br/> |Der Aktualisierungszeitgeberauftrag für Synchronisierung mit Active Directory-Verzeichnisdiensten war nicht erfolgreich.  <br/> |
|AdSyncDeleteTimerJobFailed = 27003  <br/> |Der Löschungszeitgeberauftrag für Synchronisierung mit Active Directory war nicht erfolgreich.  <br/> |
|AdSyncAdConnectFail = 27006  <br/> |Verbindung mit Active Directory kann nicht hergestellt werden.  <br/> |
|AdMaximumGroupsCountExceeded = 27007  <br/> |Die maximale Gruppenanzahl wurde überschritten.  <br/> |
|SRAInvalidVersion = 27300  <br/> |Ungültige SRA-Version.  <br/> |
|SRADelayedUpgradeFailed = 27301  <br/> |Die asynchrone SRA-Aktualisierung war nicht erfolgreich.  <br/> |
|(27000 - 27999)  <br/> |Andere Synchronisierungsfehler für Active Directory werden in Project Server nicht aufgelistet.  <br/> |

<a name="pj15_ErrorCodes_Admin"></a>

## <a name="table-6-admin-web-service"></a>Tabelle 6 Suchverwaltungs-Webdienst

|Fehlercode-Admin Web service|Beschreibung|
|:-----|:-----|
|AdminViewNameAlreadyExists = 16600  <br/> |Der Ansichtsname ist bereits vorhanden. Namen müssen eindeutig sein.  <br/> |
|AdminViewInvalidDividerPosition = 16601  <br/> |Die Trennlinienposition ist ungütig.  <br/> |
|AdminViewDataWasTampered = 16602  <br/> |Die Daten wurden geändert.  <br/> |
|AdminViewMaxDisplayedFieldsNumberExceeded = 16603  <br/> |Die Anzeige überschreitet die maximale Anzahl Felder.  <br/> |
|AdminViewCannotDeleteDefaultView = 16604  <br/> |Standardansicht kann nicht gelöscht werden.  <br/> |
|AdminViewCannotCopyDefaultView = 16605  <br/> |Standardansicht kann nicht kopiert werden.  <br/> |
|AdminLocalCustomFieldInvalid = 19011  <br/> |Das lokale benutzerdefinierte Feld ist ungültig.  <br/> |
|AdminEnterpriseCustomFieldInvalid = 19012  <br/> |Das benutzerdefinierte Enterprise-Feld ist ungültig.  <br/> |
|AdminNTAccountNotFound = 19032  <br/> |Das Windows (NTLM)-Konto wurde nicht gefunden.  <br/> |
|AdminUnableToMerge = 20003  <br/> |Daten können nicht zusammengeführt werden.  <br/> |
|AdminDeleteArchivedProjectsFailed = 25004  <br/> |Der gelöschte Vorgang für archivierte Projekte war nicht erfolgreich.  <br/> |
|AdminUpdateArchiveScheduleFailed = 25006  <br/> |Der Archivierungszeitplan konnte nicht aktualisiert werden.  <br/> |
|AdminArchiveScheduleFailed = 28018  <br/> |Der Archivierungszeitplan war nicht erfolgreich.  <br/> |
|AdminReadArchivedProjectsListFailed = 28019  <br/> |Die Liste der archivierten Projekten konnte nicht gelesen werden.  <br/> |
|AdminReadArchiveScheduleFailed = 28020  <br/> |Der Archivierungszeitplan konnte nicht gelesen werden.  <br/> |
|AdminUserAccountNameNull = 28021  <br/> |Der Name des Benutzerkontos ist null.  <br/> |
|AdminIsWindowsUserNull = 28022  <br/> |Das Windows (NTLM)-Benutzerkonto scheint null zu sein.  <br/> |
|AdminInvalidTimePeriodState = 28023  <br/> |Der Zeitraumstatus ist ungültig.  <br/> |
|AdminGlobalUpdateFailed = 28024  <br/> |Die Enterprise-Global-Aktualisierung während des Aufrufs von **SetServerCurrency** war nicht erfolgreich.  <br/> |
|AdminGlobalCheckedOut = 28025  <br/> |Die Enterprise-Global-Vorlage wurde bereits während des Aufrufs von **SetServerCurrency** geprüft.  <br/> |
|AdminInvalidDatabaseTimeout = 28026  <br/> |Zeitüberschreitung aufgrund einer ungültigen Datenbank.  <br/> |
|AdminInvalidDatabaseTimeoutType = 28027  <br/> |Zeitüberschreitung aufgrund eines ungültigen Datenbanktyps.  <br/> |
|AdminInvalidEntityType = 28028  <br/> |Der Entitätstyp ist ungültig. Finden Sie unter [EntityCollection](https://msdn.microsoft.com/library/Microsoft.Office.Project.Server.Library.EntityCollection.aspx) .  <br/> |
|AdminInvalidCompatibilityModeChange = 28029  <br/> |Die Änderung vom Kompatibilitätsmodus ist ungültig.  <br/> |
|AdminInvalidCompatibilityMode = 28030  <br/> |Der Kompatibilitätsmodus ist ungültig.  <br/> |
|AdminInvalidProjectProfessionalVersions = 28031  <br/> |Der Project Professional-Versionssatz ist ungültig.  <br/> |
|AdminInvalidProjectProfessionalVersion = 28032  <br/> |Die Project Professional-Version ist ungültig.  <br/> |
|AdminTooManyProjectProfessionalVersions = 28033  <br/> |Zu viele Project Professional-Versionen angegeben.  <br/> |
|AdminDuplicateProjectProfessionalMajorVersions = 28034  <br/> |Es gibt doppelte Haupt-Project Professional-Versionen. Sie dürfen nur eine Version pro Hauptversion angeben, beginnend mit Project Professional 2007.  <br/> |
|AdminInvalidServerFlags = 28035  <br/> |Mindestens ein Flag in den Project Server-Einstellungen ist ungültig.  <br/> |
|AdminNullProjectProfessionalVersions = 28036  <br/> |Mindestens eine Project Professional-Version ist null.  <br/> |

<a name="pj15_ErrorCodes_Archive"></a>

## <a name="table-7-archive-web-service"></a>Tabelle 7 Archiv-Webdienst

|Archivieren von Web Service (Sicherung und Wiederherstellung) Fehlercode|Beschreibung|
|:-----|:-----|
|ArchiveProjectFailure = 25000  <br/> |Die Projektarchivierung war nicht erfolgreich.  <br/> |
|ArchiveProjectsFailed = 25001  <br/> |Keines der Projekte konnte in der Archivierungsdatenbank gespeichert werden.  <br/> |
|ArchiveProjectFailed = 25002  <br/> |Projektarchiv konnte nicht gespeichert werden.  <br/> |
|RestoreProjectFailed = 25003  <br/> |Projekt kann nicht wiederhergestellt werden.  <br/> |
|ArchiveResourcesFailed = 25007  <br/> |Das Ressourcenarchiv kann nicht gespeichert werden.  <br/> |
|ArchiveCustomFieldsFailed = 25008  <br/> |Das Archiv der benutzerdefinierten Felder kann nicht gespeichert werden.  <br/> |
|RestoreCustomFieldsFailed = 25009  <br/> |Benutzerdefinierte Felder können nicht wiederhergestellt werden.  <br/> |
|ArchiveSystemSettingsFailed = 25010  <br/> |Archiv der Systemeinstellungen kann nicht gespeichert werden.  <br/> |
|RestoreSystemSettingsFailed = 25011  <br/> |Systemeinstellungen können nicht gespeichert werden.  <br/> |
|ArchiveCategoriesFailed = 25012  <br/> |Archiv der Sicherheitskategorien kann nicht gespeichert werden.  <br/> |
|RestoreCategoriesFailed = 25013  <br/> |Sicherheitskategorien können nicht gespeichert werden.  <br/> |
|ArchiveViewsFailed = 25014  <br/> |Ansichtsarchiv kann nicht gespeichert werden.  <br/> |
|RestoreViewsFailed = 25015  <br/> |Ansichten können nicht wiederhergestellt werden.  <br/> |
|ArchiveGlobalProjectFailed = 25016  <br/> |Das Enterprise-Global-Archiv kann nicht gespeichert werden.  <br/> |
|RestoreGlobalProjectFailed = 25017  <br/> |Die Enterprise-Global-Vorlage kann nicht wiederhergestellt werden.  <br/> |
|ArchiveInvalidRetentionPolicyValue = 25018  <br/> |Die Archivaufbewahrungsrichtlinie ist ungültig.  <br/> |
|ArchiveCustomFieldsFailure = 25019  <br/> |Das Archiv der benutzerdefinierten Felder kann nicht gelesen werden.  <br/> |
|ArchiveGlobalProjectFailure = 25020  <br/> |Das Enterprise-Global-Archiv kann nicht gelesen werden.  <br/> |
|ArchiveResourcesFailure = 25021  <br/> |Das Ressourcenarchiv kann nicht gelesen werden.  <br/> |
|ArchiveSystemSettingsFailure = 25022  <br/> |Das Archiv der Systemeinstellungen kann nicht gelesen werden.  <br/> |
|ArchiveViewsFailure = 25023  <br/> |Ansichtsarchiv kann nicht gelesen werden.  <br/> |
|ArchiveCategoriesFailure = 25024  <br/> |Das Archiv der Sicherheitskategorien kann nicht gelesen werden.  <br/> |
|ResourcePlanPublishFailure = 25025  <br/> |Der Ressourcenplan kann nicht veröffentlicht werden.  <br/> |
|RestoreCategoriesFailure = 25026  <br/> |Sicherheitskategorien können nicht aus dem Archiv wiederhergestellt werden.  <br/> |
|RestoreCustomFieldsFailure = 25027  <br/> |Benutzerdefinierte Felder können nicht aus dem Archiv wiederhergestellt werden.  <br/> |
|RestoreGlobalProjectFailure = 25028  <br/> |Enterprise-Global-Vorlage kann nicht aus dem Archiv wiederhergestellt werden.  <br/> |
|RestoreProjectFailure = 25029  <br/> |Das Projekt kann nicht aus dem Archiv wiederhergestellt werden.  <br/> |
|RestoreResourcesFailure = 25030  <br/> |Die Ressourcen können nicht aus dem Archiv wiederhergestellt werden.  <br/> |
|RestoreSystemSettingsFailure = 25031  <br/> |Die Systemeinstellungen können nicht aus dem Archiv wiederhergestellt werden.  <br/> |
|RestoreViewsFailure = 25032  <br/> |Die Ansichten können nicht aus dem Archiv wiederhergestellt werden.  <br/> |
|ArchiveReadProjectArchiveRetentionSettingFailed = 25033  <br/> |Die Aufbewahrungseinstellungen für das Projektarchiv können nicht gelesen werden.  <br/> |
|RestoreResourcesFailed = 29021  <br/> |Die Ressourcen könne nicht wiederhergestellt werden  <br/> |

<a name="pj15_ErrorCodes_Assignments"></a>

## <a name="table-8-assignment"></a>Tabelle 8 Zuweisung

|Fehlercode - Zuordnung|Beschreibung|
|:-----|:-----|
|AssignmentNotFound = 120  <br/> |Zuordnung nicht gefunden.  <br/> |
|AssignmentWrongTrackingMethod = 122  <br/> |Die Zuordnung hat eine ungültige Überwachungsmethode.  <br/> |
|AssignmentWorkTypeInvalid = 127  <br/> |Der Zuordnungsarbeitstyp ist ungültig.  <br/> |
|AssignmentRateTableInvalid = 130  <br/> |Die Satztabelle für die Zuordnung ist ungültig.  <br/> |
|AssignmentAlreadyExists = 131  <br/> |Die Zuordnung ist bereits vorhanden.  <br/> |
|AssignmentDuplicateSpecified = 132  <br/> |Es gibt eine doppelte Zuordnung.  <br/> |
|AssignmentUidInvalid = 133  <br/> |Die Zuordnungs-GUID ist ungültig.  <br/> |
|AssignmentDelayInvalid = 134  <br/> |Die Zuordnungsverzögerung ist ungültig.  <br/> |
|AssignmentCannotEditSummaryTask = 135  <br/> |Ein Sammelvorgang kann nicht für Zuordnungen bearbeitet werden.  <br/> |
|AssignmentInvalid = 136  <br/> |Die Zuordnung ist ungültig.  <br/> |
|AssignmentFieldsInvalidForBudget = 137  <br/> |Die Zuordnungsfelder sind nicht gültig für das Budget.  <br/> |
|AssignmentAlreadyAssignedToResource = 138  <br/> |Die Ressource hat bereits eine Zuordnung.  <br/> |
|AssignmentInvalidOwner = 139  <br/> |Der Zuordnungsbesitzer ist ungültig.  <br/> |

<a name="pj15_ErrorCodes_Calendar"></a>

## <a name="table-9-calendar"></a>Tabelle 9 Kalender

|Fehlercode - Kalender|Beschreibung|
|:-----|:-----|
|CalendarUidInvalid = 77  <br/> |Die Kalender-GUID ist ungültig.  <br/> |
|CalendarOnlyOneShiftIsNull = 13000  <br/> |Nur eine Schicht ist null  <br/> |
|CalendarRecurrenceDaysShouldBeNull = 13001  <br/> |Serie Tage muss null sein.  <br/> |
|CalendarRecurrenceMonthDayShouldBeNull = 13002  <br/> |Serie Monat und Serie Tag müssen null sein.  <br/> |
|CalendarRecurrenceMonthShouldBeNull = 13003  <br/> |Serie Monat muss null sein.  <br/> |
|CalendarRecurrenceMonthShouldNotBeNull = 13004  <br/> |Serie Monat darf nicht null sein.  <br/> |
|CalendarRecurrencePositionShouldBeNull = 13005  <br/> |Serie Position muss null sein  <br/> |
|CalendarRecurrencePositionShouldNotBeNull = 13006  <br/> |Serie Position darf nicht null sein.  <br/> |
|CalendarRecurrenceDaysShouldNotBeNull = 13007  <br/> |Serie Tage darf nicht null sein.  <br/> |
|CalendarInvalidRecurrenceFrequency = 13008  <br/> |Serie Frequenz ist ungültig.  <br/> |
|CalendarInvalidRecurrenceType = 13009  <br/> |Serie Typ ist ungültig.  <br/> |
|CalendarInvalidRecurrenceDays = 13010  <br/> |Serie Tage ist ungültig.  <br/> |
|CalendarInvalidCombinationOfMonthDayAndPosition = 13011  <br/> |Die Kombination aus Monat, Tag und Position ist ungültig.  <br/> |
|CalendarInvalidRecurrencePosition = 13012  <br/> |Serie Position ist ungültig.  <br/> |
|CalendarCannotModifyExceptionsForCalendarBeingDeleted = 13013  <br/> |Die Kalenderausnahmen können nicht geändert werden, wenn ein Kalender gelöscht wird.  <br/> |
|CalendarExceptionConflict = 13014  <br/> |Es gibt einen Konflikt bei den Kalenderausnahmen.  <br/> |
|CalendarBadDateValue = 13015  <br/> |Das Datum ist ungültig.  <br/> |
|CalendarNotFound = 13021  <br/> |Der Kalender wurde nicht gefunden.  <br/> |
|CalendarAlreadyExists = 13022  <br/> |Der Kalender ist bereits vorhanden.  <br/> |
|CalendarNameShouldNotBeNull = 13023  <br/> |Der Kalendername ist null.  <br/> |
|CalendarInternalError = 13025  <br/> |Es gibt einen internen Fehler im Kalendervorgang.  <br/> |
|CalendarNameTooLong = 13027  <br/> |Der Kalendername ist zu lang.  <br/> |
|CalendarInvalidCalendarName = 13028  <br/> |Der Kalendername ist ungültig.  <br/> |
|CalendarStandardCalendarNotFound = 13031  <br/> |Der Standardkalender wurde nicht gefunden.  <br/> |
|CalendarInvalidShifts = 13032  <br/> |Die Schichten sind ungültig.  <br/> |
|CalendarCannotDeleteCalendarUsedByProject = 13033  <br/> |Kalender, der in einem Projekt verwendet wird, kann nicht gelöscht werden.  <br/> |
|CalCalendarUniqueIdToDuplicateShouldBeNull = 13035  <br/> |Die GUID muss null sein, um einen Kalender zu duplizieren.  <br/> |
|CalendarInvalidBaseCalendarUniqueId = 13037  <br/> |Die Basiskalender-GUID ist ungültig.  <br/> |
|CalendarInvalidUniqueIdToDuplicate = 13038  <br/> |Die GUID ist nicht gültig, um einen Kalender zu duplizieren.  <br/> |
|CalendarUnusedCalendarException = 13039  <br/> |Die Kalenderausnahme hat keinen entsprechenden Kalender. Dieser Fehler tritt auf, falls die **UpdateResources**-Methode verwendet wird, wenn ein Eintrag in der **ResourceDataSet.CalendarExceptions**-Tabelle vorgenommen wird, aber kein **BaseCalendarUniqueId** für diese Ressource in der **Resources**-Tabelle vorhanden ist.<br/> |
|CalendarCannotDeleteStandardCalendar = 13040  <br/> |Der Standardkalender kann nicht gelöscht werden.  <br/> |
|CalendarCannotRenameStandardCalendar = 13041  <br/> |Der Standardkalender kann nicht umbenannt werden.  <br/> |
|CalendarCannotDeleteCalendarUsedByEnterpriseResource = 13042  <br/> |Der Kalender wird von einer Enterprise-Ressource verwendet und kann nicht gelöscht werden.  <br/> |
|CalendarFilterInvalid = 13043  <br/> |Der Filter ist nicht gültig für einen Kalender.  <br/> |

<a name="pj15_ErrorCodes_CBS"></a>

## <a name="table-10-cubeadmin-and-cube-build-service"></a>Tabelle 10 CubeAdmin und Cube Build Service

|CubeAdmin und Cube-Erstellungdienstes (CBS) Fehlercode|Beschreibung|
|:-----|:-----|
|CBSGeneralFailure = 17001  <br/> |Fehler im Cube Build Service (CBS). Dies ist ein allgemeiner Fehler, der vielfältige Ursachen haben kann.  <br/> |
|CBSDsoNotInstalled = 17002  <br/> |Der CBS benötigt die Installation einer DSO-Komponente (Decision Support Objects) für Analysis Server.  <br/> |
|CBSASConnectionFailure = 17003  <br/> |Der CBS konnte keine Verbindung zum Analysis Services-Server herstellen.  <br/> |
|CBSOlapProcessingFailure = 17004  <br/> |Verarbeitung von OLAP-Cube nicht erfolgreich.  <br/> |
|CBSMetadataProcessingFailure = 17005  <br/> |Verarbeitung der Cube-Metadaten nicht erfolgreich.  <br/> |
|CBSASServerLockTimeOut = 17006  <br/> |Zeitüberschreitung der Analysis Services-Serversperre.  <br/> |
|CBSOlapDatabaseSetupFailure = 17007  <br/> |Einrichtung der OLAP-Cube-Datenbank nicht erfolgreich.  <br/> |
|CBSASEntityLimitation = 17008  <br/> |Anzahl der Entitäten, die Analysis Services verwenden kann, ist überschritten.  <br/> |
|CBSRequestInvalidArguments = 17009  <br/> |Mindestens ein Argument in der CBS-Anforderung ist ungültig.  <br/> |
|CBSQueueingRequestFailed = 17010  <br/> |Der CBS konnte den Auftrag nicht an die Warteschlange senden.  <br/> |
|CBSUpdateCubeCalculatedMeasureDefintionError = 17011  <br/> |Es ist ein Fehler in einem vom Cube berechneten Element aufgetreten.  <br/> |
|CBSAttemptToOverwrite = 17013  <br/> |Daten im Cube könne nicht überschrieben werden.  <br/> |
|CBSCustomFieldCannotBeAddedAsDimension = 17014  <br/> |Das benutzerdefinierte Feld darf keine Cube-Dimension sein.  <br/> |
|CBSCustomFieldFailedToBeAddedAsDimension = 17015  <br/> |Das benutzerdefinierte Feld konnte nicht als Dimension im Cube hinzugefügt werden.  <br/> |
|CBSCustomFieldCannotBeAddedAsMeasure = 17016  <br/> |Das benutzerdefinierte Feld darf keine Cubemeasure sein.  <br/> |
|CBSCustomFieldFailedToBeAddedAsMeasure = 17017  <br/> |Das benutzerdefinierte Feld konnte nicht als Maßheit im Cube hinzugefügt werden.  <br/> |
|CBSDsoTranslatorNotFound = 17018  <br/> |Der Decision Support Objects-Übersetzer wurde nicht gefunden.  <br/> |
|CBSUpdateOlapDBOperationFailure = 17019  <br/> |OLAP-Datenbank konnte nicht aktualisiert werden.  <br/> |
|CBSOlapDBInvalidArguments = 17020  <br/> |Mindestens ein Argument für die OLAP-Datenbank ist ungültig.  <br/> |
|CBSOlapDatabaseReadSettingListFailed = 17021  <br/> |Die Liste der Einstellungen für die OLAP-Datenbank konnte nicht gelesen werden.  <br/> |
|CBSOlapDatabaseReadSettingFailed = 17022  <br/> |OLAP-Datenbankeinstellung konnte nicht gelesen werden.  <br/> |
|CBSDeleteOlapDatabaseSetting = 17023  <br/> |Fehler beim Löschen von OLAP-Datenbankeinstellung.  <br/> |
|CBSSetDefaultOlapDatabase = 17024  <br/> |Fehler beim Einrichten der Standard-OLAP-Datenbank.  <br/> |
|CBSSetOlapDatabaseEnabled = 17025  <br/> |Fehler beim aktivieren der OLAP-Datenbank.  <br/> |
|CBSGetDefaultOlapDatabase = 17026  <br/> |Fehler beim Abrufen der Standard-OLAP-Datenbank.  <br/> |
|CBSCustomFieldFailedToBeAddedAsDimensionOrMeasure = 17027  <br/> |Benutzerdefiniertes Feld kann nicht als Dimension oder Measure hinzugefügt werden.  <br/> |
|CBSOlapDatabaseAssocFieldsSettings = 17028  <br/> |Fehler in Feldeinstellungen, die der OLAP-Datenbank zugeordnet sind.  <br/> |
|CBSUpdateOlapDBOperationDuplicateOrFailure = 17029  <br/> |Fehler oder Dopplung des OLAP-Datenbankaktualisierungsvorgangs.  <br/> |
|CBSErrorReadingDefaultDatabase = 17030  <br/> |Fehler beim Lesen der Standard-OLAP-Datenbank.  <br/> |
|CBSCreateOlapDBOperationFailure = 17031  <br/> |OLAP-Datenbankvorgang konnte nicht erstellt werden.  <br/> |
|CBSSetCubeFieldsSettingsFromListForGroupMeasureFailed = 17032  <br/> |Liste für Gruppenkennzahleinstellungen der Cube-Felder konnte nicht festgelegt werden.  <br/> |
|CBSErrorReadingCubeDepartments = 17033  <br/> |Fehler beim Lesen von Abteilungen im OLAP-Cube.  <br/> |
|CBSErrorMaxOlapDatabaseCountReached = 17034  <br/> |Maximale Anzahl in OLAP-Datenbank erreicht.  <br/> |
|CBSErrorReadingCubeFieldsSettings = 17035  <br/> |Fehler beim Lesen von Cube-Feldeinstellungen.  <br/> |

<a name="pj15_ErrorCodes_CICO"></a>

## <a name="table-11-check-in-and-check-out"></a>In Tabelle 11. Einchecken und Auschecken

|Fehlercode - Einchecken, Auschecken|Beschreibung|
|:-----|:-----|
|CICOCheckedOutToOtherUser = 10100  <br/> |Für einen anderen Benutzer ausgecheckt.  <br/> |
|CICOAlreadyCheckedOutToYou = 10101  <br/> |Bereits für Sie ausgecheckt.  <br/> |
|CICONotCheckedOut = 10102  <br/> |Nicht ausgecheckt.  <br/> |
|CICOCheckedOutInOtherSession = 10103  <br/> |In einer anderen Sitzung ausgecheckt.  <br/> |
|CICOInvalidSessionGuid = 10104  <br/> |Die Sitzungs-GUID ist ungültig.  <br/> |
|CICOAlreadyCheckedOutInSameSession = 10105  <br/> |Bereits in derselben Sitzung ausgecheckt.  <br/> |
|CICOCannotCheckOutVisibilityModeProjectWithMppInDocLib = 10106  <br/> |Sichtbarkeitsmodus-Projekt mit MPP-Datei in der DOC-Bibliothek kann nicht ausgecheckt werden.  <br/> |

<a name="pj15_ErrorCodes_CustomFields"></a>

## <a name="table-12-custom-field"></a>Tabelle 12. Benutzerdefiniertes Feld

|Fehlercode - Benutzerdefiniertes Feld|Beschreibung|
|:-----|:-----|
|CustomFieldInvalidPropertyType = 11500  <br/> |Der Eigenschaftstyp ist ungültig.  <br/> |
|CustomFieldInvalidScope = 11503  <br/> |Der Geltungsbereich des benutzerdefinierten Felds ist ungültig.  <br/> |
|CustomFieldScopesMustBeIdentical = 11504  <br/> |Die Geltungsbereiche müssen identisch sein.  <br/> |
|CustomFieldInvalidEntityUID = 11505  <br/> |Die Entitäts-GUID des benutzerdefinierten Felds ist ungültig.  <br/> |
|CustomFieldHasInvalidPropertiesForNonLookupTableCF = 11506  <br/> |Die Eigenschaften sind nicht gültig für ein benutzerdefiniertes Feld ohne Nachschlagetabelle.  <br/> |
|CustomFieldNonExistentWeightsTableUID = 11507  <br/> |Die GUID der Gewichtstabelle ist nicht vorhanden.  <br/> |
|CustomFieldInvalidName = 11508  <br/> |Der Name des benutzerdefinierten Felds ist ungültig.  <br/> |
|CustomFieldInvalidDefault = 11510  <br/> |Der Standardwert für das benutzerdefinierte Feld ist ungültig.  <br/> |
|CustomFieldInvalidLookupTableUID = 11511  <br/> |Die GUID der Nachschlagetabelle ist ungültig.  <br/> |
|CustomFieldTypeDoesNotMatchLookupTableMask = 11512  <br/> |Der Typ des benutzerdefinierten Felds stimmt nicht mit dem Nachschlagetabellenformat überein.  <br/> |
|CustomFieldCannotHaveNonLeafNodeDefault = 11513  <br/> |Der Standardwert des benutzerdefinierten Felds muss einen Endknoten haben.  <br/> |
|CustomFieldMatchingOnlyAvailableForResources = 11514  <br/> |Übereinstimmung von benutzerdefinierten Feldern ist nur für Ressourcen verfügbar.  <br/> |
|CustomFieldUIDCannotMatchLookupTableUID = 11516  <br/> |Die GUID stimmt nicht mit der GUID der Nachschlagetabelle überein.  <br/> |
|CustomFieldUIDAlreadyExists = 11517  <br/> |Die GUID des benutzerdefinierten Felds ist bereits vorhanden.  <br/> |
|CustomFieldIDAlreadyExists = 11518  <br/> |Die Kennnummer des benutzerdefinierten Felds ist bereits vorhanden.  <br/> |
|CustomFieldNameAlreadyExists = 11519  <br/> |Der Name des benutzerdefinierten Felds ist bereits vorhanden.  <br/> |
|CustomFieldInvalidEntity = 11520  <br/> |Die Entität ist nicht gültig für das benutzerdefinierte Feld  <br/> |
|CustomFieldMaskDoesNotMatchEntityType = 11521  <br/> |Das Codeformat stimmt nicht mit dem Entitätstyp überein.  <br/> |
|CustomFieldLowerOrderBitsOutOfRange = 11522  <br/> |Die unteren Bits sind außerhalb des zulässigen Bereichs.  <br/> |
|CustomFieldInvalidMaxValues = 11523  <br/> |Mindestens ein Maximalwert ist ungültig.  <br/> |
|CustomFieldCannotModifyCertainValuesOnceDefined = 11524  <br/> |Bestimmte Werte können nach ihrer Festlegung nicht mehr geändert werden.  <br/> |
|CustomFieldNonExistentPID = 11526  <br/> |Die Eigenschaftskennnummer des benutzerdefinierten Felds ist nicht vorhanden.  <br/> |
|CustomFieldCannotChangeBuiltInFields = 11527  <br/> |Die integrierten Project Server-Felder, wie "Kostentyp", "Status" und "RSP" können nicht geändert werden.  <br/> |
|CustomFieldSecondaryUidCannotEqualUid = 11528  <br/> |Die sekundäre GUID darf nicht mit der primären GUID identisch sein.  <br/> |
|CustomFieldCannotHaveSecondaryUIDorIDForThisEntityType = 11529  <br/> |Das benutzerdefinierte Feld kann keine sekundäre GUID oder eine GUID für diesen Entitätstyp haben.  <br/> |
|CustomFieldNameMatchesIntrinsicField = 11530  <br/> |Der Name des benutzerdefinierten Felds stimmt mit einem systeminternen Feld überein.  <br/> |
|CustomFieldInvalidAggregationType = 11531  <br/> |Der Aggregationstyp ist ungültig.  <br/> |
|CustomFieldProjectFormulaFieldsMustUseFormulaAggregation = 11532  <br/> |Die Projektformelfelder müssen Formelaggregation verwenden.  <br/> |
|CustomFieldMustSpecifyEitherIDorUID = 11700  <br/> |Kennnummer oder GUID des benutzerdefinierten Felds muss angegeben werden.  <br/> |
|CustomFieldInvalidID = 11701  <br/> |Die Kennnummer des benutzerdefinierten Felds ist ungültig.  <br/> |
|CustomFieldInvalidUID = 11702  <br/> |Die GUID des benutzerdefinierten Felds ist ungültig.  <br/> |
|CustomFieldInvalidType = 11703  <br/> |Der Typ des benutzerdefinierten Felds ist ungültig.  <br/> |
|CustomFieldInvalidTypeColumnFilledIn = 11704  <br/> |Der Wert des benutzerdefinierten Felds Typ Spalte ist ungültig. Siehe Beispiel in [Fehlercodebeispiel für WCF](#pj15_ErrorCodes_WCFExample).  <br/> |
|CustomFieldCodeValueDoesNotMatchLookupTable = 11706  <br/> |Der Codewert stimmt nicht mit der Nachschlagetabelle überein.  <br/> |
|CustomFieldCodeValueIsNotLeafNode = 11707  <br/> |Der Codewert ist kein Endknoten der Nachschlagetabelle.  <br/> |
|CustomFieldRowAlreadyExists = 11708  <br/> |Die Zeile des benutzerdefinierten Felds ist bereits vorhanden.  <br/> |
|CustomFieldRowDoesNotMatchCorrespondingDefinitionInDB = 11710  <br/> |Die Zeile des benutzerdefinierten Felds stimmt nicht mit der Datenbankdefinition überein.  <br/> |
|CustomFieldCodeValueAlreadyUsed = 11711  <br/> |Der Codewert wird bereits verwendet.  <br/> |
|CustomFieldMaxValuesExceeded = 11712  <br/> |Maximalwerte für benutzerdefiniertes Feld überschritten.  <br/> |
|CustomFieldRequiredValueNotProvided = 11713  <br/> |Ein Wert erforderlich des benutzerdefinierten Feldes ist nicht verfügbar. Siehe Beispiel in [Fehlercodebeispiel für WCF](#pj15_ErrorCodes_WCFExample).  <br/> |
|CustomFieldCannotChangeLookupTable = 11715  <br/> |Die Nachschlagetabelle für das benutzerdefinierte Feld kann nicht geändert werden.  <br/> |
|CustomFieldFilterInvalid = 11716  <br/> |Der Filter für das benutzerdefinierte Feld ist ungültig.  <br/> |
|CustomFieldRolldownInvalidOnFormulaFields = 11717  <br/> |Ein Rolldown kann nicht in einem benutzerdefinierten Formelfeld auftreten.  <br/> |
|CustomFieldFormulaFieldCannotBeRequired = 11718  <br/> |Das Formelfeld kann kein Pflichtfeld sein.  <br/> |
|CustomFieldFormulaFieldCannotBeWorkflowControlled = 11719  <br/> |Das Formelfeld kann nicht von einem Workflow gesteuert werden.  <br/> |
|CustomFieldCannotSetValueOnFormulaFields = 11720  <br/> |Es können keine Werte in Formelfeldern festgelegt werden.  <br/> |
|CustomFieldNewPerRequestLimitExcedeed = 11721  <br/> |Anforderung überschritten für neue benutzerdefinierte Felder. Die Grenze liegt bei [NEW_CF_PER_REQUEST_LIMIT](https://msdn.microsoft.com/library/Microsoft.Office.Project.Server.Library.CustomField.NEW_CF_PER_REQUEST_LIMIT.aspx) in einer Anforderung.  <br/> |
|CustomFieldNameIsReservedName = 11722  <br/> |Der Name eines benutzerdefinierten Felds darf kein reservierter Name sein.  <br/> |
|CustomFieldNameInvalidForOlapMeasure = 11723  <br/> |Der Name des benutzerdefinierten Felds ist nicht gültig für eine OLAP-Cubemeasure.  <br/> |
|CustomFieldNameInvalidForOlapDimension = 11724  <br/> |Der Name des benutzerdefinierten Felds ist nicht gültig für eine OLAP-Cubedimension.  <br/> |
|CustomFieldSettingsInvalidForOlapMeasure = 11725  <br/> |Die Einstellungen des benutzerdefinierten Felds sind nicht gültig für eine OLAP-Cubemeasure.  <br/> |
|CustomFieldSettingsInvalidForOlapDimension = 11726  <br/> |Die Einstellungen des benutzerdefinierten Felds sind nicht gültig für eine OLAP-Cubedimension  <br/> |
|CustomFieldCannotAddRelativeImportanceField = 11727  <br/> |Ein Relative-Wichtigkeit-Feld kann nicht hinzugefügt werden.  <br/> |
|CustomFieldCannotAddProjectImpactField = 11728  <br/> |Ein Projektauswirkung-Feld kann nicht hinzugefügt werden.  <br/> |
|CustomFieldInvalidDepartmentUid = 11731  <br/> |Die Abteilungs-GUID im benutzerdefinierten Feld ist ungültig.  <br/> |
|CustomFieldCannotModifyDepartmentUidOnBuiltinFields = 11732  <br/> |Die Abteilungs-GUID kann nicht in integrierten benutzerdefinierten Feldern geändert werden.  <br/> |
|CustomFieldCannotHaveBothLookupTableAndMultilineText = 11733  <br/> |Ein benutzerdefiniertes Feld kann nicht zugleich eine Nachschlagetabelle und einen mehrzeiligen Text enthalten.  <br/> |
|CustomFieldCannotHaveBothFormulaAndMultilineText = 11734  <br/> |Ein benutzerdefiniertes Feld kann nicht zugleich eine Formel und einen mehrzeiligen Text enthalten  <br/> |
|CustomFieldDescriptionExceedsLimit = 11735  <br/> |Die Beschreibung des benutzerdefinierten Felds ist zu lang. Die maximale Länge der **MD_PROP_DESCRIPTION**-Eigenschaft ist 1000 Zeichen.<br/> |
|CustomFieldOnlyTextFieldsCanHaveMultilineText = 11736  <br/> |Nur benutzerdefinierte Textfelder können mehrzeiligen Text enthalten.  <br/> |
|CustomFieldOnlyProjectFieldsCanHaveMultilineText = 11737  <br/> |Nur benutzerdefinierte Projektfelder können mehrzeiligen Text enthalten  <br/> |
|CustomFieldCannotChangeWorkflowControlledBehaviorForNonProjectCustomFields = 11738  <br/> |Ein benutzerdefiniertes Feld kann das Verhalten eines benutzerdefinierten und von einem Workflow gesteuerten Nicht-Projektfelds nicht ändern.  <br/> |
|CustomFieldIsWorkflowControlledAndCannotBeChanged = 11739  <br/> |Das benutzerdefinierte Feld wird von einem Workflow gesteuert und kann nicht geändert werden.  <br/> |
|CustomFieldCannotHaveRequiredFlagWhenWorkflowControlledFlagIsSet = 11740  <br/> |Das benutzerdefinierte Feld kann nicht angefordert werden, wenn es von einem Workflow gesteuert wird.  <br/> |
|CustomFieldFormulaCreatesCircularReference = 11742  <br/> |Die Formel des benutzerdefinierten Felds generiert einen Zirkelverweis.  <br/> |
|CustomFieldFormulaContainsInvalidFieldReference = 11743  <br/> |Die Formel des benutzerdefinierten Felds enthält einen ungültigen Feldverweis.  <br/> |
|CustomFieldFormulaContainsErrors = 11744  <br/> |Die Formel des benutzerdefinierten Felds enthält mindestens einen Fehler.  <br/> |
|CustomFieldLocalCustomFieldNotDefined = 11745  <br/> |Das lokale benutzerdefinierte Feld ist nicht definiert.  <br/> |
|CustomFieldGraphicalIndicatorContainsErrors = 11746  <br/> |Die grafische Anzeige des benutzerdefinierten Felds enthält Fehler.  <br/> |
|CustomFieldGraphicalIndicatorContainsInvalidFieldReference = 11747  <br/> |Die grafische Anzeige des benutzerdefinierten Felds enthält einen ungültigen Feldverweis.  <br/> |
|CustomFieldGraphicalIndicatorTypeMismatch = 11748  <br/> |Es gibt keine Typübereinstimmung bei der grafischen Anzeige des benutzerdefinierten Felds.  <br/> |
|CustomFieldFormulaFieldCannotReferenceWorkflowControlledField = 11749  <br/> |Ein Feld in der Formel kann auf kein Feld verweisen, das von einem Workflow gesteuert wird.  <br/> |
|CustomFieldWorkflowCustomFieldBeingReferencedByFormula = 11750  <br/> |Eine Formel versucht auf ein benutzerdefiniertes Workflowfeld zu verweisen.  <br/> |

<a name="pj15_ErrorCodes_LookupTables"></a>

## <a name="table-13-lookup-table"></a>In Tabelle 13. Nachschlagetabelle

|Fehlercode - Nachschlagetabelle|Beschreibung|
|:-----|:-----|
|LookupTableMaskNotDefined = 11000  <br/> |Das Codeformat der Nachschlagetabelle ist nicht definiert.  <br/> |
|LookupTableMaskHasTooManyValues = 11001  <br/> |Das Codeformat der Nachschlagetabelle hat zu viele Werte  <br/> |
|LookupTableMaskHasGaps = 11002  <br/> |Das Codeformat der Nachschlagetabelle hat Lücken.  <br/> |
|LookupTableMaskSequenceTypeLimitedToOneLevelDeep = 11003  <br/> |Der Sequenztyp des Codeformats ist auf eine Ebene begrenzt.  <br/> |
|LookupTableMaskSequenceTypeInvalid = 11004  <br/> |Der Sequenztyp des Codeformats ist ungültig.  <br/> |
|LookupTableMaskSequenceRequiresAnyLength = 11005  <br/> |Die codeformatsequenz erfordert eine Länge von _jeder_.  <br/> |
|LookupTableMaskSeparatorTooLong = 11006  <br/> |Das Codeformat-Trennzeichen hat zu viele Zeichen.  <br/> |
|LookupTableMaskLevelMustBeBlankAcrossLCIDs = 11007  <br/> |Die Codeformatebene muss bei den Gebietsschema-IDs (Sprachen-IDs) leer sein.  <br/> |
|LookupTableMaskSeparatorInvalid = 11008  <br/> |Ein Trennzeichen des Codeformats ist ungültig.  <br/> |
|LookupTableMaskBlankSeparatorInvalidAfterAnyLengthSequence = 11009  <br/> |Ein leeres Trennzeichen ist nach einer Sequenzlänge von _jeder_ungültig.  <br/> |
|LookupTableMaskSequenceLengthInvalid = 11010  <br/> |Die Sequenzlänge des Codeformats ist ungültig.  <br/> |
|LookupTableMaskLevelMustBeOneOrMore = 11011  <br/> |Das Codeformat muss Ebene 1 oder höher entsprechen.  <br/> |
|LookupTableItemDoesNotFitMask = 11050  <br/> |Das Nachschlagetabellenelement passt nicht zur Codeformatdefinition.  <br/> |
|LookupTableItemContainsSeparator = 11051  <br/> |Das Nachschlagetabellenelement enthält ein Trennzeichen.  <br/> |
|LookupTableItemFullValueTooLong = 11052  <br/> |Der vollständige Wert der Nachschlagetabelle ist zu lang.  <br/> |
|LookupTableDuplicateSiblingsDisallowed = 11053  <br/> |Doppelte gleichgeordnete Elemente in der Nachschlagetabelle sind nicht zulässig.  <br/> |
|LookupTableSortOrderIndexInvalid = 11054  <br/> |Der Index der Nachschlagetabellen-Sortierreihenfolge ist ungültig.  <br/> |
|LookupTableSortOrderIndexDuplicate = 11055  <br/> |Doppelter Index der Nachschlagetabellen-Sortierreihenfolge.  <br/> |
|LookupTableSortOrderTypeInvalid = 11056  <br/> |Der Typ der Nachschlagetabellen-Sortierreihenfolge ist ungültig.  <br/> |
|LookupTableSortOrderMustComeAfterParentSortOrder = 11057  <br/> |Die Sortierreihenfolge muss nach der übergeordneten Sortierreihenfolge erfolgen.  <br/> |
|LookupTableSortOrderMustComeBeforeParentNextSiblingSortOrder = 11058  <br/> |Die Sortierreihenfolge muss vor dem übergeordneten Element der Sortierreihenfolge des nächstes gleichgeordneten Elements erfolgen.  <br/> |
|LookupTableInvalidCookieLength = 11060  <br/> |Die Cookielänge für eine Nachschlagetabelle ist ungültig.  <br/> |
|LookupTableMustHaveValuesForPrimaryLCIDorJustOneValue = 11061  <br/> |Die Nachschlagetabelle muss Werte für die primäre Gebietsschema-ID (Sprachen-ID) oder wenigsten einen Wert haben. Wenn Sie eine mehrsprachige Nachschlagetabelle einrichten, fügen Sie beispielsweise nur einen Formatwert für jede Ebene hinzu bzw. fügen Sie erst den Wert der primären LCID hinzu.  <br/> |
|LookupTableLCIDNotSupportedInLookupTableLanguages = 11062  <br/> |Die Gebietsschema-ID (Sprachen-ID) ist nicht in den Nachschlagetabellensprachen enthalten.  <br/> |
|LookupTableInvalidDescriptionLength = 11063  <br/> |Die Beschreibungslänge eines Elements der Nachschlagetabelle ist ungültig.  <br/> |
|LookupTableCannotChangeBuiltInTables = 11064  <br/> |Die integrierten Nachschlagetabellen können nicht geändert werden.  <br/> |
|LookupTableCannotChangeTypeOnceCreated = 11065  <br/> |Nach Erstellen der Nachschlagetabelle kann der Nachschlagetabellentyp nicht mehr geändert werden.  <br/> |
|LookupTableCannotDeleteLTWithDependantCustomField = 11066  <br/> |Eine Nachschlagetabelle, die in einem benutzerdefinierten Feld verwendet wird, kann nicht gelöscht werden.  <br/> |
|LookupTableAllLevelsNotFilled = 11067  <br/> |Alle Nachschlagetabellenebenen müssen ausgefüllt werden.  <br/> |
|LookupTableDuplicateName = 11068  <br/> |Nachschlagetabellennamen müssen eindeutig sein.  <br/> |
|LookupTableInvalidName = 11069  <br/> |Der Nachschlagetabellenname ist ungültig.  <br/> |
|LookupTableDuplicateSiblingPhoneticsDisallowed = 11071  <br/> |Doppelte Lautschrift von gleichgeordneten Elementen in einer Nachschlagetabelle ist nicht möglich.  <br/> |
|LookupTableItemInvalidLookupTable = 11073  <br/> |Ein Element in der Nachschlagetabelle ist ungültig.  <br/> |
|LookupTableInvalidPhoneticsLength = 11074  <br/> |Die Länge des Lautschrift-Felds ist ungültig.  <br/> |
|LookupTableAlreadyExists = 11076  <br/> |Die Nachschlagetabelle ist bereits vorhanden.  <br/> |
|LookupTableInvalidUID = 11078  <br/> |Die Nachschlagetabellen-GUID ist ungültig.  <br/> |
|LookupTableFilterInvalid = 11079  <br/> |Der Filter der Nachschlagetabelle ist ungültig.  <br/> |
|LookupTableLanguageParameterInvalidWithXmlFilter = 11080  <br/> |Ein Sprachparameter ist nicht gültig bei einem _XmlFilter_ -Parameter der.  <br/> |
|LookupTableInvalidParentStructUid = 11081  <br/> |Die GUID für eine übergeordnete Nachschlagetabellenstruktur ist ungültig.  <br/> |
|LookupTableItemContainsListSeparator = 11082  <br/> |Das Nachschlagetabellenelement enthält ein Listentrennzeichen.  <br/> |
   
Fehlercodes in Tabelle 14 umfassen Elementen für Projektdetailseiten (PDPs), Exchange-Synchronisierung, die Project Web App-Zeitachse und Datenbankfehler. Viele der miscellaneous Fehlercodes in Tabelle 14 werden intern verwendet.
  
> [!NOTE]
> Die überwachungsfehlercodes werden in Project Server 2013 nicht verwendet. 

<a name="pj15_ErrorCodes_Miscellaneous"></a>

## <a name="table-14-miscellaneous-error-codes"></a>Tabelle 14. Sonstige Fehlercodes

|Sonstige Fehlercode|Beschreibung|
|:-----|:-----|
|AuditingUpdateFailure = 31000  <br/> |Nicht verwendet.  <br/> |
|AuditingCannotDeleteFeature = 31001  <br/> |Nicht verwendet.  <br/> |
|AuditingCannotAddFeature = 31002  <br/> |Nicht verwendet  <br/> |
|AuditingFeatureIsNoLongerAudited = 31003  <br/> |Nicht verwendet  <br/> |
|AuditingItemIsNotYetAvailable = 31004  <br/> |Nicht verwendet  <br/> |
|AuditingInvalidFeatureUid = 31005  <br/> |Nicht verwendet  <br/> |
|AuditingInvalidStoreForSelectedFeature = 31006  <br/> |Nicht verwendet  <br/> |
|AuditingInvalidStore = 31007  <br/> |Nicht verwendet  <br/> |
|AuditingVersionNameTooLong = 31008  <br/> |Nicht verwendet  <br/> |
|AuditingBeginVersionFailure = 31009  <br/> |Nicht verwendet  <br/> |
|AuditingEndVersionFailure = 31010  <br/> |Nicht verwendet  <br/> |
|ProjectDetailPagesStrategicImpactRatingRequired = 32000  <br/> |Es ist eine strategische Auswirkungsbewertung für die Projektdetailseite erforderlich.  <br/> |
|ProjectDetailPagesMissingPDPLinks = 32001  <br/> |Fehlende Links zu den Projektdetailseiten.  <br/> |
|ProjectDetailPagesUnavailableWorker = 32002  <br/> |Laden von Projektdrilldown nicht erfolgreich. Keine Worker verfügbar.  <br/> |
|ProjectDetailPagesFailedToLoadProjectInWorker = 32003  <br/> |Worker konnte nicht geladen werden.  <br/> |
|AppPermissionInvalidAppPermissionId = 32300  <br/> |Es gibt ein Problem mit der App-Berechtigungs-ID.  <br/> |
|InvariantValidationPSIFailed = 40000  <br/> |Wird von **PWA**-Methoden zurückgegeben, wenn eine private Methode **ValidationMethodFailed** zurückgibt. Interne Verwendung.<br/> |
|ValidationMethodFailed = 40001  <br/> |Wird von privaten **PWA**-Methoden zurückgegeben, wenn diese Datenbankinkonsistenzen erkennen. Interne Verwendung.<br/> |
|GeneralExchangeSyncError = 40500  <br/> |Allgemeiner Fehler bei der Microsoft Exchange-Synchronisierung. Interne Verwendung.  <br/> |
|ExchangeSyncRootFolderCreationFailed = 40501  <br/> |Fehler beim Erstellen des Stammordners in der Microsoft Exchange-Synchronisierung.  <br/> |
|ExchangeSyncTaskFolderCreationFailed = 40502  <br/> |Fehler beim Erstellen des Vorgangsordners.  <br/> |
|ExchangeSyncCouldNotGetRootFolder = 40503  <br/> |Stammordner konnte nicht abgerufen werden.  <br/> |
|ExchangeSyncCouldNotLoadTaskObject = 40504  <br/> |Das Vorgangsobjekt konnte nicht geladen werden.  <br/> |
|ExchangeSyncNewExchangeTaskCreationFailed = 40505  <br/> |Erstellung eines neuen Vorgangs in der Exchange-Synchronisierung fehlgeschlagen.  <br/> |
|ExchangeSyncFailedToUpdateCacheForUser = 40506  <br/> |Fehler beim Aktualisieren des Caches der Exchange-Synchronisierung für den Benutzer.  <br/> |
|ExchangeSyncFailedToUpdateExchangeTask = 40507  <br/> |Fehler beim Aktualisieren des Vorgangs in Microsoft Exchange.  <br/> |
|ExchangeSyncSubscriptionUpdateFailed = 40508  <br/> |Fehler beim Aktualisieren des Exchange-Synchronisationsabonnements.  <br/> |
|ExchangeSyncEWSUrlFailed = 40509  <br/> |Die Microsoft Exchange-Webdienst-URL ist fehlgeschlagen.  <br/> |
|ExchangeSyncExchangeUrlRefreshFailed = 40510  <br/> |Fehler beim Aktualisieren der Exchange-URL.  <br/> |
|ExchangeSyncExchangeSubscriptionUpdateForUserFailed = 40511  <br/> |Fehler beim Aktualisieren des Exchange-Abonnements für den Benutzer.  <br/> |
|ExchangeSyncGeneralProcessingFailure = 40512  <br/> |Allgemeiner Verarbeitungsfehler bei Microsoft Exchange-­Synchronisierung.  <br/> |
|ExchangeSyncDeletionOfTasksInExchangeFailure = 40513  <br/> |Fehler beim Löschen von Vorgängen in der Exchange-Synchronisierung.  <br/> |
|ExchangeSyncAttemptedSyncOfInvalidConfiguredResource = 40514  <br/> |Es wurde versucht, eine Ressource mit einer ungültigen Konfiguration zu synchronisieren.  <br/> |
|ExchangeSyncRetrievalOfEWSUrlCausedException = 40515  <br/> |Beim Abrufen des Exchange-Webdiensts ist eine Ausnahme aufgetreten.  <br/> |
|TimelineViewDataDoesNotExist = 42000  <br/> |Daten für die Zeitachsenansicht in Project Web App ist nicht vorhanden.  <br/> |
|DatabaseUndefinedError = 50000  <br/> |Die Datenbank ist nicht definiert.  <br/> |
|DatabaseCannotInsertDuplicateKeyError = 50001  <br/> |Die Datenbank kann keinen doppelten Schlüssel einfügen.  <br/> |

<a name="pj15_ErrorCodes_Notifications"></a>

## <a name="table-15-notification"></a>In Tabelle 15. Benachrichtigung

|Fehlercode - Benachrichtigung|Beschreibung|
|:-----|:-----|
|NotificationReminderUnknown = 16050  <br/> |Unbekannte Erinnerung.  <br/> |
|NotificationReminderParentNotSubscribed = 16051  <br/> |Es gibt kein Abonnement für das übergeordnete Elemente der Erinnerung.  <br/> |
|NotificationReminderParentNotFound = 16052  <br/> |Das übergeordnete Elemente der Erinnerung wurde nicht gefunden.  <br/> |
|NotificationReminderChildStillSubscribed = 16053  <br/> |Es gibt immer noch ein Abonnement für das untergeordnete Element der Erinnerung.  <br/> |
|NotificationReminderChildNotFound = 16054  <br/> |Das untergeordnete Element der Erinnerung wurde nicht gefunden.  <br/> |
|NotificationEMailDeliveryFailed = 16080  <br/> |Zustellung der Benachrichtigungs-E-Mail nicht erfolgreich.  <br/> |
|NotificationQueueMessageFailed = 16082  <br/> |Nachricht der Benachrichtigungswarteschlange nicht erfolgreich.  <br/> |
|NotificationXSLTTransformationError = 16084  <br/> |Fehler in der Benachrichtigungs-XSLT-Transformation.  <br/> |
   
Alle Fehlercodes in Tabelle 16 gelten für den Optimierer, der eine Komponente in der Projektportfolioanalyse ist.

<a name="pj15_ErrorCodes_Optimizer"></a>

## <a name="table-16-optimizer-project-portfolio-analysis"></a>Tabelle 16. Optimierer (projektportfolioanalyse)

|Fehlercode - Optimierer|Beschreibung|
|:-----|:-----|
|OptimizerDepInvalidDepType = 29000  <br/> |Der Optimierer **DEPENDENCY_TYPE** Wert in der [OptimizerDependencyDataSet.OptimizerDependenciesRow](https://msdn.microsoft.com/library/WebSvcPortfolioAnalyses.OptimizerDependencyDataSet.OptimizerDependenciesRow.aspx) ist ungültig. Finden Sie unter [Optimizer.DependencyTypes](https://msdn.microsoft.com/library/Microsoft.Office.Project.Server.Library.Optimizer.DependencyTypes.aspx) .  <br/> |
|OptimizerDepInvalidEntityType = 29001  <br/> |Der Entitätstyp ist ungültig. Finden Sie unter [Entities](https://msdn.microsoft.com/library/Microsoft.Office.Project.Server.Library.EntityCollection.Entities.aspx) -Eigenschaft.  <br/> |
|OptimizerDepInvalidPosition = 29003  <br/> |Wert für die [POSITION](https://msdn.microsoft.com/library/WebSvcPortfolioAnalyses.OptimizerDependencyDataSet.OptimizerDependencyDetailsRow.POSITION.aspx) ist ungültig.  <br/> |
|OptimizerDepDuplicateDependentProjects = 29004  <br/> |Es gibt doppelte Projekte in der [OptimizerDependencyDataSet.OptimizerDependencyDetailsDataTable](https://msdn.microsoft.com/library/WebSvcPortfolioAnalyses.OptimizerDependencyDataSet.OptimizerDependencyDetailsDataTable.aspx) .  <br/> |
|OptimizerDepInvalidDependency = 29005  <br/> |Die Optimiererabhängigkeit ist ungültig.  <br/> |
|OptimizerDepCircularDependency = 29006  <br/> |Es gibt eine Ringabhängigkeit.  <br/> |
|OptimizerCannotDeleteDependency = 29007  <br/> |Die Abhängigkeit kann nicht gelöscht werden.  <br/> |
|OptimizerCannotCreateDependency = 29008  <br/> |Die Abhängigkeit kann nicht erstellt werden.  <br/> |
|OptimizerCannotUpdateDependency = 29009  <br/> |Die Abhängigkeit kann nicht aktualisiert werden.  <br/> |
|OptimizerCannotCreateMultipleDependencies = 29010  <br/> |Mehrere Abhängigkeiten können nicht erstellt werden.  <br/> |
|OptimizerCannotUpdateMultipleDependencies = 29011  <br/> |Mehrere Abhängigkeiten können nicht aktualisiert werden.  <br/> |
|OptimizerEngineMatrixNotFilled = 29100  <br/> |Der Optimierer hat nicht ausreichend Daten für die Berechnung.  <br/> |
|OptimizerEngineCustomFieldIsNotAConstraint = 29101  <br/> |Das benutzerdefinierte Feld ist keine Einschränkung für den Optimierer.  <br/> |
|OptimizerCouldNotCalculatePrioritiesFromCustomFields = 29102  <br/> |Prioritäten von angegebenen benutzerdefinierten Feldern können nicht berechnet werden.  <br/> |
|OptimizerEngineBinaryInfeasibleSolution = 29103  <br/> |Die Optimiererberechnung führt zu einer nicht realisierbaren Lösung.  <br/> |
|OptimizerEngineBinaryNumericalError = 29104  <br/> |Bei der Optimiererberechnung liegt ein numerischer Fehler vor.
.  <br/> |
|OptimizerEngineBinaryTimedOut = 29105  <br/> |Bei der Optimiererberechnung ist eine Zeitüberschreitung aufgetreten.  <br/> |
|OptimizerEngineBinaryMaxedIterations = 29106  <br/> |Die Optimiererberechnung hat die maximale Anzahl von Iterationen erreicht.  <br/> |
|OptimizerEngineBinarySubOptimal = 29107  <br/> |Die Ergebnisse der Optimiererberechnung sind nicht optimal.  <br/> |
|OptimizerEngineBinaryInternalError = 29108  <br/> |Es gibt einen internen Fehler bei der Optimiererberechnung.  <br/> |
|OptimizerInvalidRange = 29200  <br/> |Der Datumsbereich für den Optimierer ist ungültig.  <br/> |
|OptimizerNonNormalizedWeights = 29201  <br/> |**WEIGHT** -Werte in der [AnalysisDataSet.AnalysisPriorityDataDataTable](https://msdn.microsoft.com/library/WebSvcPortfolioAnalyses.AnalysisDataSet.AnalysisPriorityDataDataTable.aspx) sind nicht normalisiert.  <br/> |
|OptimizerCannotEditPrioritization = 29300  <br/> |Treiberpriorisierung kann nicht bearbeitet werden.  <br/> |
|OptimizerCannotDeletePrioritization = 29301  <br/> |Treiberpriorisierung kann nicht gelöscht werden.  <br/> |
|OptimizerCannotCreatePrioritization = 29302  <br/> |Treiberpriorisierung kann nicht erstellt werden.  <br/> |
|OptimizerCannotUpdatePrioritization = 29303  <br/> |Treiberpriorisierung kann nicht aktualisiert werden.  <br/> |
|OptimizerCannotCalculateDriverPriorities = 29304  <br/> |Treiberpriorisierungen können nicht berechnet werden.  <br/> |
|OptimizerCannotCreateMultiplePrioritizations = 29305  <br/> |Es können nicht mehrere Treiberpriorisierungen erstellt werden.  <br/> |
|OptimizerCannotUpdateMultiplePrioritizations = 29306  <br/> |Es können nicht mehrere Treiberpriorisierungen aktualisiert werden.  <br/> |
|OptimizerDriverRelationsNotFilled = 29307  <br/> |Die DriverRelationsRow-Daten ist nicht abgeschlossen.  <br/> |
|OptimizerDriversNotFilled = 29308  <br/> |Nicht ausreichend Informationen in den Projekttreibern für eine Lösung vorhanden.  <br/> |
|OptimizerDriverRelationsInvalidInversedValue = 29309  <br/> |Inverse Werte sind in der [DriverPrioritizationDataSet.DriverRelationsRow](https://msdn.microsoft.com/library/WebSvcDriver.DriverPrioritizationDataSet.DriverRelationsRow.aspx) vorhanden.  <br/> |
|OptimizerCannotCreatePrioritizationUsingInactiveDrivers = 29310  <br/> |Es ist eine inaktive Treiber in der [DriverPrioritizationDataSet.DriverRelationsRow](https://msdn.microsoft.com/library/WebSvcDriver.DriverPrioritizationDataSet.DriverRelationsRow.aspx) angegeben. Überprüfen Sie die Eigenschaften **DRIVER1_UID** und **DRIVER2_UID** .  <br/> |
|OptimizerCannotChangePrioritizationType = 29311  <br/> |Der Priorisierungstyp kann nicht geändert werden.  <br/> |
|OptimizerCannotSpecifyPriorityValuesForCalculatedPrioritizations = 29312  <br/> |Wurde eine Priorisierung berechnet, können Sie keinen Prioritätswert angeben.  <br/> |
|OptimizerCannotNormalizePriorityValues = 29313  <br/> |Prioritätswerte können nicht normalisiert werden.  <br/> |
|OptimizerTooManyDriversInPrioritization = 29314  <br/> |Es sind zu viele Business-Treiber in der Priorisierung.  <br/> |
|OptimizerInvalidProjectImpactValue = 29400  <br/> |Der Projektauswirkungswert ist ungültig.  <br/> |
|OptimizerCannotDeleteDriver = 29401  <br/> |Der Projekttreiber kann nicht gelöscht werden.  <br/> |
|OptimizerCannotCreateDriver = 29402  <br/> |Der Projekttreiber kann nicht erstellt werden.  <br/> |
|OptimizerCannotUpdateDriver = 29403  <br/> |Der Projekttreiber kann nicht aktualisiert werden.  <br/> |
|OptimizerCannotEditDriver = 29404  <br/> |Der Projekttreiber kann nicht bearbeitet werden.  <br/> |
|OptimizerCannotCreateMultipleDrivers = 29405  <br/> |Es kann nicht mehrere Treiber geben.  <br/> |
|OptimizerCannotUpdateMultipleDrivers = 29406  <br/> |Mehrere Treiber können nicht aktualisiert werden.  <br/> |
|OptimizerInvalidRelativeImportanceValue = 29407  <br/> |Der Relative-Wichtigkeit-Wert ist ungültig.  <br/> |
|OptimizerInvalidDriverUid = 29500  <br/> |Die Treiber-GUID ist ungültig.  <br/> |
|OptimizerInvalidEntityType = 29501  <br/> |Der Entitätstyp ist nicht gültig für den Optimierer.  <br/> |
|OptimizerInvalidProjectUid = 29502  <br/> |Die Projekt-GUID ist ungültig.  <br/> |
|OptimizerInvalidCustomFieldUid = 29503  <br/> |Die GUID des benutzerdefinierten Felds ist nicht gültig für den Optimierer.  <br/> |
|OptimizerInvalidHardConstraintUid = 29504  <br/> |Die GUID der schwerwiegenden Beschränkung ist ungültig.  <br/> |
|OptimizerInvalidAnalysisUid = 29505  <br/> |Die Analyse-GUID ist ungültig.  <br/> |
|OptimizerDriverFilterInvalid = 29506  <br/> |Der Treiberfilter ist ungültig.  <br/> |
|OptimizerPrioritizationFilterInvalid = 29507  <br/> |Der Priorisierungsfilter ist ungültig.  <br/> |
|OptimizerCannotLoadOptimizationEngine = 29508  <br/> |Die Optimiererberechnungsmodul kann nicht geladen werden.  <br/> |
|OptimizerAnalysisFilterInvalid = 29509  <br/> |Der Analysefilter ist ungültig.  <br/> |
|OptimizerSolutionFilterInvalid = 29510  <br/> |Der Lösungsfilter für den Optimierer ist ungültig.  <br/> |
|OptimizerDependenciesFilterInvalid = 29511  <br/> |Der Abhängigkeitsfilter für den Optimierer ist ungültig.  <br/> |
|OptimizerInvalidSolutionUid = 29512  <br/> |Die Lösungs-GUID für den Optimierer ist ungültig.  <br/> |
|OptimizerInvalidViewUid = 29513  <br/> |Die Ansichts-GUID für den Optimierer ist ungültig  <br/> |
|OptimizerInvalidAnalysisType = 29600  <br/> |Der Typ der Portfolioanalyse ist ungültig.  <br/> |
|OptimizerInvalidPrioritizationType = 29601  <br/> |Der Priorisierungstyp für den Optimierer ist ungültig.  <br/> |
|OptimizerCannotDeleteAnalysis = 29602  <br/> |Portfolioanalyse kann nicht gelöscht werden.  <br/> |
|OptimizerCannotCreateAnalysis = 29603  <br/> |Portfolioanalyse kann nicht erstellt werden.  <br/> |
|OptimizerCannotUpdateAnalysis = 29604  <br/> |Portfolioanalyse kann nicht aktualisiert werden.  <br/> |
|OptimizerInvalidPrioritizationUid = 29607  <br/> |Die Priorisierungs-GUID ist ungültig.  <br/> |
|OptimizerCannotCreateMultipleAnalyses = 29608  <br/> |Mehrere Portfolioanalysen können nicht erstellt werden.  <br/> |
|OptimizerCannotUpdateMultipleAnalyses = 29609  <br/> |Mehrere Portfolioanalysen können nicht aktualisiert werden.  <br/> |
|OptimizerCannotCalculateProjectPriorities = 29610  <br/> |Der Optimierer kann Projektprioritäten nicht berechnen.  <br/> |
|OptimizerCannotDeleteAnalysisProjectImpact = 29611  <br/> |Projektauswirkungen in der Portfolioanalyse können nicht gelöscht werden.  <br/> |
|OptimizerCannotChangeAnalysisProjects = 29612  <br/> |Projekte in der Portfolioanalyse können nicht geändert werden.  <br/> |
|OptimizerCannotChangePriorityData = 29613  <br/> |Prioritätsdaten können nicht geändert werden.  <br/> |
|OptimizerCannotEditAnalysis = 29614  <br/> |Portfolioanalyse kann nicht bearbeitet werden.  <br/> |
|OptimizerInvalidPlannerData = 29615  <br/> |Die Planner-Daten sind nicht gültig für den Optimierer.  <br/> |
|OptimizerCannotChangeImpactData = 29616  <br/> |Die Projektauswirkungsdaten können nicht geändert werden.  <br/> |
|OptimizerInvalidProjectsNumber = 29617  <br/> |Die Anzahl der Projekte ist ungültig.  <br/> |
|OptimizerCannotAddImpactCFUIDToCFAnalysis = 29618  <br/> |Kann nicht die Project Auswirkungen GUID des benutzerdefinierten Felds ([PROJECT_IMPACT_CF_UID](https://msdn.microsoft.com/library/WebSvcPortfolioAnalyses.AnalysisDataSet.AnalysisRow.PROJECT_IMPACT_CF_UID.aspx) ) für die Portfolioanalyse hinzufügen.  <br/> |
|OptimizerInvalidDepartmentUid = 29619  <br/> |Die [DEPARTMENT_UID](https://msdn.microsoft.com/library/WebSvcPortfolioAnalyses.AnalysisDataSet.AnalysisRow.DEPARTMENT_UID.aspx) ist ungültig.  <br/> |
|OptimizerTooManyProjectsInAnalysis = 29620  <br/> |Es sind zu viele Projekte in der Analyse.  <br/> |
|QueueAnalysisCannotDeleteAnalysis = 29680  <br/> |Die [QueueDeleteAnalyses](https://msdn.microsoft.com/library/WebSvcPortfolioAnalyses.PortfolioAnalyses.QueueDeleteAnalyses.aspx) -Methode kann die Analyse nicht löschen.  <br/> |
|QueueAnalysisCannotCreateAnalysis = 29681  <br/> |Die [QueueCreateAnalysis](https://msdn.microsoft.com/library/WebSvcPortfolioAnalyses.PortfolioAnalyses.QueueCreateAnalysis.aspx) -Methode kann nicht die Analyse nicht erstellen.  <br/> |
|QueueAnalysisCannotUpdateAnalysis = 29682  <br/> |Die [QueueUpdateAnalysis](https://msdn.microsoft.com/library/WebSvcPortfolioAnalyses.PortfolioAnalyses.QueueUpdateAnalysis.aspx) -Methode kann die Analyse nicht aktualisieren.  <br/> |
|AnalysisMismatchedJobList = 29690  <br/> |Die Analyseauftragsliste stimmt nicht überein.  <br/> |
|OptimizerInvalidForceInLookupTableUid = 29691  <br/> |Die GUID der Nachschlagetabelle kann nicht hereingezwungen werden.  <br/> |
|OptimizerInvalidForceOutLookupTableUid = 29692  <br/> |Die GUID der Nachschlagetabelle kann nicht herausgezwungen werden.  <br/> |
|OptimizerDuplicateForceLookupTableUids = 29693  <br/> |Es sind erzwungene doppelte GUIDs der Nachschlagetabelle vorhanden.  <br/> |
|OptimizerInvalidDecisionResult = 29701  <br/> |Das Entscheidungsergebnis ist ungültig.  <br/> |
|OptimizerInvalidForcedStatus = 29702  <br/> |Der erzwungene Status ist ungültig.  <br/> |
|OptimizerCannotDeleteSolution = 29703  <br/> |Die [QueueDeleteOptimizerSolutions](https://msdn.microsoft.com/library/WebSvcPortfolioAnalyses.PortfolioAnalyses.QueueDeleteOptimizerSolutions.aspx) -Methode kann die optimiererlösung nicht löschen.  <br/> |
|OptimizerCannotCreateSolution = 29704  <br/> |Die [QueueCreateOptimizerSolution](https://msdn.microsoft.com/library/WebSvcPortfolioAnalyses.PortfolioAnalyses.QueueCreateOptimizerSolution.aspx) -Methode kann nicht erstellt eine der optimiererlösung.  <br/> |
|OptimizerCannotUpdateSolution = 29705  <br/> |Die [QueueUpdateAnalysis](https://msdn.microsoft.com/library/WebSvcPortfolioAnalyses.PortfolioAnalyses.QueueUpdateAnalysis.aspx) -Methode kann die optimiererlösung nicht aktualisieren.  <br/> |
|OptimizerCannotCalculateSolutionStrategicAlignment = 29706  <br/> |Der Optimierer kann die Lösung für eine strategische Ausrichtung nicht berechnen.  <br/> |
|OptimizerCannotCreateMultipleSolutions = 29707  <br/> |Der Optimierer kann nicht mehrere Lösungen erstellen.  <br/> |
|OptimizerCannotUpdateMultipleSolutions = 29708  <br/> |Der Optimierer kann nicht mehrere Lösungen aktualisieren.  <br/> |
|OptimizerCannotAddPrioritizationToCFAnalysis = 29709  <br/> |Der Optimierer kann keine Priorisierung zu einem benutzerdefinierten Feld für die Analyse hinzufügen.  <br/> |
|OptimizerTableIsReadOnly = 29710  <br/> |Die Optimierer-Tabelle ist schreibgeschützt.  <br/> |
|OptimizerSolutionCreateMessageFailed = 29711  <br/> |Der Optimierer konnte keine von der "Lösung erstellte" Nachricht generieren.  <br/> |
|OptimizerSolutionDeleteMessageFailed = 29712  <br/> |Der Optimierer konnte keine von der "Lösung gelöschte" Nachricht generieren.  <br/> |
|OptimizerCannotCalculateEfficientFrontier = 29714  <br/> |Der Optimierer kann die Effizienzlinie für die Analyse nicht berechnen.  <br/> |
|OptimizerCannotUpdateSolutionProperties = 29715  <br/> |Die Lösungseigenschaften könnten nicht aktualisiert werden.  <br/> |
|OptimizerInvalidConstraintPosition = 29716  <br/> |Die Einschränkungsposition im Optimierer ist ungültig.  <br/> |
|OptimizerInvalidHardConstraintPosition = 29717  <br/> |Die feste Einschränkungsposition im Optimierer ist ungültig.  <br/> |
|OptimizerInvalidConstraintLimit = 29718  <br/> |Der Grenzwert der Einschränkung im Optimierer ist ungültig.  <br/> |
|OptimizerInvalidConstraintValue = 29719  <br/> |Der Einschränkungswert ist ungültig.  <br/> |
|OptimizerInvalidSolutionProjectsSet = 29720  <br/> |Die Gruppe von Projekten in der Lösung ist ungültig.  <br/> |
|OptimizerCannotCommitSolution = 29721  <br/> |Die [CommitOptimizerSolution](https://msdn.microsoft.com/library/WebSvcPortfolioAnalyses.PortfolioAnalyses.CommitOptimizerSolution.aspx) -Methode kann nicht die Lösung nicht festschreiben.  <br/> |
|OptimizerInvalidInputData = 29723  <br/> |Die Eingabedaten für den Optimierer sind ungültig.  <br/> |
|OptimizerInvalidConstraintSet = 29724  <br/> |Die für den Optimierer festgelegte Einschränkung ist ungültig.  <br/> |
|OptimizerCannotUpdateAnalysisMetrics = 29725  <br/> |Die Analysemetriken können nicht aktualisiert werden.  <br/> |
|OptimizerSolutionMismatchedJobList = 29726  <br/> |Die Auftragsliste in der Lösung stimmt nicht überein.  <br/> |
|OptimizerInvalidForceLookupTableValue = 29727  <br/> |Der erzwungene Nachschlagetabellenwert ist ungültig.  <br/> |
|OptimizerCannotCreateSolutionWhileAnalysisUpdateIsPending = 29728  <br/> |Optimiererlösung kann nicht erstellt werden, wenn die Analyseaktualisierung noch aussteht.  <br/> |
|OptimizerProjectSelectorAtLeastOne = 29800  <br/> |Für den Optimierer muss mindestens ein Projekt ausgewählt werden.  <br/> |
   
Die Fehlercodes in Tabelle 17 sind für den Planner bestimmt, der eine Komponente in der Projektportfolioanalyse ist.

<a name="pj15_ErrorCodes_Planner"></a>

## <a name="table-17-planner-project-portfolio-analysis"></a>Tabelle 17. Planner (projektportfolioanalyse)

|Fehlercode - Planner|Beschreibung|
|:-----|:-----|
|PlannerSolutionMessageDeleteFailed = 28000  <br/> |Warteschlangenfehler: Die Nachricht zum Löschen der Planner-Lösung war nicht erfolgreich.  <br/> |
|PlannerSolutionMessageCreateFailed = 28001  <br/> |Warteschlangenfehler: Die Nachricht zum Erstellen der Planner-Lösung war nicht erfolgreich.  <br/> |
|PlannerInvalidRBSValueUid = 28002  <br/> |Die GUID für einen Wert des Ressourcenstrukturplans ist nicht gültig in den Planner-Daten.  <br/> |
|PlannerInvalidCustomFieldUid = 28003  <br/> |Die GUID für ein benutzerdefiniertes Feld ist ungültig.  <br/> |
|PlannerHorizonInvalid = 28004  <br/> |Der Planner-Zeithorizont ist ungültig. Ein Zeithorizont ist ein für die Kapazitätsplanung angegebener Zeitraum.  <br/> |
|PlannerHorizonTooBig = 28005  <br/> |Der Zeithorizont liegt zu weit in der Zukunft.  <br/> |
|PlannerInvalidBookingType = 28006  <br/> |Der Ressourcenbuchungstyp ist ungültig.  <br/> |
|PlannerInvalidTimeScale = 28007  <br/> |Die Zeitskala ist ungültig.  <br/> |
|PlannerInvalidProjectSNET = 28008  <br/> |Das "Anfang nicht früher als"-Datum für das Projekt ist ungültig.  <br/> |
|PlannerInvalidProjectFNLT = 28009  <br/> |Das "Ende nicht später als"-Datum für das Projekt ist ungültig.  <br/> |
|PlannerInvalidAnalysisStartDate = 28010  <br/> |[Ausgangsdatum](https://msdn.microsoft.com/library/WebSvcPortfolioAnalyses.PlannerSolutionDataSet.SolutionProjectRequirementsByRoleRow.START_DATE.aspx) für das Projekt ist ungültig.  <br/> |
|PlannerInvalidAnalysisDuration = 28011  <br/> |Die [Dauer](https://msdn.microsoft.com/library/WebSvcPortfolioAnalyses.PlannerSolutionDataSet.SolutionProjectsRow.DURATION.aspx) ist nicht gültig für die Portfolioanalyse.  <br/> |
|PlannerInvalidHorizonStartDate = 28012  <br/> |Das Startdatum des Zeithorizonts ist ungültig.  <br/> |
|PlannerInvalidHorizonEndDate = 28013  <br/> |Das Enddatum des Zeithorizonts ist ungültig.  <br/> |
|PlannerInvalidHorizonTimeScale = 28014  <br/> |Die Zeitskala des Zeithorizonts ist ungültig.  <br/> |
|PlannerInvalidAnalysisType = 28015  <br/> |Der Typ der Portfolioanalyse ist ungültig.  <br/> |
|PlannerHorizonStartDateDoesNotMatchTimeScale = 28016  <br/> |Das Startdatum des Zeithorizonts entspricht nicht der Zeitskala.  <br/> |
|PlannerHorizonEndDateDoesNotMatchTimeScale = 28017  <br/> |Das Enddatum des Zeithorizonts entspricht nicht der Zeitskala.  <br/> |
|PlannerAnalysisNoCapacityData = 28037  <br/> |Es gibt keine Ressourcenkapazitätsdaten für die Portfolioanalyse.  <br/> |
|PlannerInvalidSolutionUid = 28100  <br/> |Die GUID der Analyselösung ist ungültig.  <br/> |
|PlannerInvalidOptimizerSolutionUid = 28101  <br/> |Die GUID der Optimiererlösung ist ungültig.  <br/> |
|PlannerInvalidLookupTableValueUid = 28102  <br/> |Die GUID des Nachschlagetabellenwerts ist ungültig.  <br/> |
|PlannerInvalidEfficientFrontierUid = 28103  <br/> |Die [FRONTIER_UID](https://msdn.microsoft.com/library/WebSvcPortfolioAnalyses.PlannerSolutionDataSet.SolutionEfficientFrontierRow.FRONTIER_UID.aspx) ist ungültig.  <br/> |
|PlannerInvalidProjectUid = 28104  <br/> |Die Projekt-GUID ist ungültig.  <br/> |
|PlannerInvalidAllocationThreshold = 28105  <br/> |Die Zuordnungsschwelle ist ungültig.  <br/> |
|PlannerInvalidHiringType = 28109  <br/> |Die [HIRING_TYPE](https://msdn.microsoft.com/library/WebSvcPortfolioAnalyses.PlannerSolutionDataSet.SolutionsRow.HIRING_TYPE.aspx) ist ungültig. Finden Sie unter [Planner.PlannerHiringType](https://msdn.microsoft.com/library/Microsoft.Office.Project.Server.Library.Planner.PlannerHiringType.aspx) .  <br/> |
|PlannerInvalidConstraintType = 28110  <br/> |Die [CONSTRAINT_TYPE](https://msdn.microsoft.com/library/WebSvcPortfolioAnalyses.PlannerSolutionDataSet.SolutionsRow.CONSTRAINT_TYPE.aspx) ist ungültig. Finden Sie unter [Planner.ConstraintType](https://msdn.microsoft.com/library/Microsoft.Office.Project.Server.Library.Planner.ConstraintType.aspx) .  <br/> |
|PlannerInvalidConstraintValue = 28111  <br/> |Die [CONSTRAINT_VALUE](https://msdn.microsoft.com/library/WebSvcPortfolioAnalyses.PlannerSolutionDataSet.SolutionsRow.CONSTRAINT_VALUE.aspx) ist ungültig.  <br/> |
|PlannerInvalidRateTable = 28112  <br/> |Die [RATE_TABLE](https://msdn.microsoft.com/library/WebSvcPortfolioAnalyses.PlannerSolutionDataSet.SolutionsRow.RATE_TABLE.aspx) ist ungültig.  <br/> |
|PlannerInvalidSolutionForConstraint = 28113  <br/> |Die Planner-Lösung gilt nicht für die Einschränkung. Zu viele Projekte wurden während des ersten Planner-Laufs hineingezwungen.  <br/> |
|PlannerInvalidSolutionForDependencies = 28114  <br/> |Die Planner-Lösung ist ungültig, da es zu viele Projekte für die Betrachtung von Business-Abhängigkeit oder Konflikten gibt. Dieser Fehler tritt beim zweiten Lauf auf.  <br/> |
|PlannerInvalidSolutionForScheduling = 28115  <br/> |Die Planner-Lösung ist nicht gültig für die Terminplanung, da es Ringabhängigkeiten gibt.  <br/> |
|PlannerInvalidAnalysisUid = 28116  <br/> |Die [ANALYSIS_UID](https://msdn.microsoft.com/library/WebSvcPortfolioAnalyses.PlannerSolutionDataSet.SolutionsRow.ANALYSIS_UID.aspx) ist ungültig.  <br/> |
|PlannerInvalidProjectStartDate = 28200  <br/> |Das Datum des Projektstarts ist ungültig.  <br/> |
|PlannerInvalidProjectEndDate = 28201  <br/> |Das Datum des Projektendes ist ungültig.  <br/> |
|PlannerInvalidProjectDuration = 28202  <br/> |Die Projektdauer ist ungültig.  <br/> |
|PlannerInvalidProjectFNLTDate = 28203  <br/> |Das "Ende nicht später als"-Datum für das Projekt ist ungültig.  <br/> |
|PlannerInvalidProjectSNETDate = 28204  <br/> |Das"Anfang nicht früher als"-Datum für das Projekt ist ungültig.  <br/> |
|PlannerCannotCreateSolution = 28900  <br/> |Der Planner kann keine Lösung erstellen.  <br/> |
|PlannerCannotUpdateSolution = 28901  <br/> |Der Planner kann die Lösung nicht aktualisieren.  <br/> |
|PlannerCannotDeleteSolution = 28902  <br/> |Der Planner kann die Lösung nicht löschen.  <br/> |
|PlannerCannotCreateMultipleSolutions = 28903  <br/> |Der Planner kann nicht mehrere Lösungen erstellen.  <br/> |
|PlannerCannotUpdateMultipleSolutions = 28904  <br/> |Der Planner kann nicht mehrere Lösungen aktualisieren.  <br/> |
|PlannerTableIsReadOnly = 28907  <br/> |Die **DataTable** ist schreibgeschützt.  <br/> |
|PlannerCannotCommitSolution = 28908  <br/> |Der Planner kann die Lösung nicht an die Datenbank übergeben.  <br/> |
|PlannerFieldIsReadOnly = 28909  <br/> |Das Feld ist schreibgeschützt.  <br/> |
|PlannerProjectNotInParentSolution = 28910  <br/> |Das Projekt ist nicht in der übergeordneten Lösung.  <br/> |
|PlannerProjectNotSelectedInParentSolution = 28911  <br/> |Das Projekt wurde nicht in der übergeordneten Lösung ausgewählt.  <br/> |
|PlannerProjectNotInParentAnalysis = 28912  <br/> |Das Projekt ist nicht in der übergeordneten Portfolioanalyse.  <br/> |
|PlannerProjectBeyondHorizon = 28913  <br/> |Das Projekt erstreckt sich über den Zeithorizont hinaus.  <br/> |
|PlannerResourceAllocationInternalError = 28915  <br/> |Es gibt einen interner Fehler in der Ressourcenzuordnung.  <br/> |
|PlannerResourceAllocationInfeasibleSolution = 28916  <br/> |Die Ressourcenzuordnung ist eine nicht realisierbare Lösung.  <br/> |
|PlannerProjectEndDateViolatesDependency = 28917  <br/> |Der Endtermin des Projekts verstößt gegen eine Abhängigkeit.  <br/> |
|PlannerInvalidProjectsSet = 28919  <br/> |Die Gruppe von Projekten ist ungültig.  <br/> |
|PlannerInvalidInputData = 28920  <br/> |Der Planner enthält ungültige Eingabedaten.  <br/> |
|PlannerDecimalOverflowError = 28921  <br/> |In Planner ist ein Dezimalüberlauffehler.  <br/> |
|PlannerSolutionMismatchedJobList = 28922  <br/> |Die Lösung enthält eine nicht übereinstimmende Auftragsliste.  <br/> |
|PlannerInvalidForceLookupTableValue = 28923  <br/> |Der erzwungene Wert einer Nachschlagetabelle ist ungültig.  <br/> |
|PlannerNoHiredResource = 28924  <br/> |Es wurde keine Ressource für das Angebot eingestellt.  <br/> |

<a name="pj15_ErrorCodes_Projects"></a>

## <a name="table-18-project"></a>In Tabelle 18. Project

|Fehlercode - Projekt|Beschreibung|
|:-----|:-----|
|ProjectGlobalNotFound = 100  <br/> |Die Enterprise Global-Projektvorlage kann nicht gefunden werden.  <br/> |
|ProjectGlobalCannotBeDeleted = 101  <br/> |Die Enterprise Global-Projektvorlage kann nicht gelöscht werden.  <br/> |
|ProjectNotFound = 1000  <br/> |Projekt nicht gefunden.  <br/> |
|ProjectAlreadyExists = 1001  <br/> |Projekt ist bereits vorhanden.  <br/> |
|ProjectCheckedoutToOtherUser = 1002  <br/> |Das Projekt wurde an einen anderen Benutzer ausgecheckt.  <br/> |
|ProjectTypeInvalidForCreate = 1003  <br/> |Der Projekttyp für den Erstellungsvorgang ist ungültig.  <br/> |
|ProjectParametersInvalid = 1004  <br/> |Mindestens ein Projektparameter ist ungültig.  <br/> |
|ProjectNotCheckedoutToUser = 1006  <br/> |Projekt nicht für Benutzer ausgecheckt.  <br/> |
|ProjectCheckedout = 1007  <br/> |Projekt ausgecheckt.  <br/> |
|ProjectTypeInvalid = 1008  <br/> |Projekttyp ist ungültig.  <br/> |
|ProjectIDInvalid = 1009  <br/> |Die Projekt-Kennnummer ist ungültig.  <br/> |
|ProjectNameTooLong = 1014  <br/> |Projektname ist zu lang.  <br/> |
|ProjectManagerNameTooLong = 1015  <br/> |Name des Projektmanagers ist zu lang.  <br/> |
|ProjectNameInvalid = 1016  <br/> |Projektname ist ungültig.  <br/> |
|ProjectStartDateMissing = 1025  <br/> |Starttermin des Projekts fehlt.  <br/> |
|ProjectNameMissing = 1026  <br/> |Projektname fehlt.  <br/> |
|ProjectVersionMissing = 1027  <br/> |Project-Version fehlt.  <br/> |
|ProjectDoesNotExist = 1028  <br/> |Projekt ist nicht vorhanden.  <br/> |
|ProjectMultipleProjectsInvalid = 1029  <br/> |Mehrere Projekte sind ungültig.  <br/> |
|ProjectHasWriteLock = 1030  <br/> |Projekt hat Schreibsperre in der Datenbank.  <br/> |
|ProjectHasPendingWriteLock = 1031  <br/> |Projekt hat ausstehende Schreibsperre.  <br/> |
|ProjectHasNoReadLock = 1032  <br/> |Projekt hat keine Lesesperre.  <br/> |
|ProjectHasReadLock = 1033  <br/> |Projekt hat eine Lesesperre.  <br/> |
|ProjectNameAlreadyExists = 1034  <br/> |Projektname ist bereits vorhanden.  <br/> |
|ProjectOptCriticalSlackLimitInvalid = 1035  <br/> |Die optionale kritische Puffergrenze ist ungültig.  <br/> |
|ProjectOptCurrencyPositionInvalid = 1036  <br/> |Die optionale Währungsposition ist ungültig.  <br/> |
|ProjectOptCurrencyDigitsInvalid = 1037  <br/> |Die optionalen Dezimalstellen für die Währung sind ungültig.  <br/> |
|ProjectOptCurrencySymbolTooLong = 1038  <br/> |Das optionale Währungssymbol ist zu lang.  <br/> |
|ProjectCannotDelete = 1039  <br/> |Das Projekt kann nicht gelöscht werden. Nur reguläre oder serverseitige-Vorlagenprojekte können gelöscht werden.  <br/> |
|ProjectCannotAdd = 1040  <br/> |**AddToProject**-Methode kann nicht für das serverseitige Projekt verwendet werden.  <br/> |
|ProjectOptCurrencySymbolInvalid = 1041  <br/> |Das optionale Währungssymbol ist ungültig.  <br/> |
|ProjectHasNoWriteLock = 1042  <br/> |Das Projekt hat keine Schreibsperre.  <br/> |
|ProjectFilterInvalid = 1043  <br/> |Der Projektfilter ist ungültig.  <br/> |
|ProjectTooLarge = 1044  <br/> |Der Projektvorschlag ist zu groß.  <br/> |
|ProjectOptCurrencyCodeNot3Chars = 1045  <br/> |Der optionale Währungscode besteht nicht aus drei Zeichen.  <br/> |
|ProjectOptCurrencyCodeInvalid = 1046  <br/> |Der Währungscode ist ungültig in den Projektoptionen.  <br/> |
|ProjectActualsAreProtected = 1047  <br/> |Die aktuelle Projektwerte sind geschützt.  <br/> |
|ProjectTemplateNotFound = 1048  <br/> |Projektvorlage wurde nicht gefunden.  <br/> |
|ProjectCurrencyCodeInvalid = 1049  <br/> |Der Währungscode ist ungültig.  <br/> |
|ProjectCannotEditCostResource = 1050  <br/> |Kostenressourcen kann nicht bearbeitet werden.  <br/> |
|ProjectIsNotPublished = 1051  <br/> |Projekt nicht veröffentlicht.  <br/> |
|ProjectExceededLWPTaskLimit = 1052  <br/> |Die Vorgangsgrenze für einen Projektvorschlag wurde überschritten (kleines Projekt).  <br/> |
|ProjectOptFinishDateInvalid = 1053  <br/> |Der Endtermin in den Projektoptionen ist ungültig.  <br/> |
|ProjectExceededItemsLimit = 1054  <br/> |Die Anzahl der zu verarbeitenden Elemente ist überschritten. Die Project Server-Dienstanwendung kann **ProjectDataSet** nicht verwenden, um mehr als 1000 Elemente insgesamt in allen Tabellen hinzuzufügen oder zu aktualisieren. Um mehr als 1000 Elemente zu verarbeiten, verwenden Sie Mehrfachaufrufe wie beispielsweise an **QueueUpdateProject**.<br/> |
|ProjectColumnNotReadOnly = 1055  <br/> |Die Spalte ist nicht schreibgeschützt.  <br/> |
|ProjectInvalidOwner = 1056  <br/> |Der Projektbesitzer ist ungültig.  <br/> |
|ProjectCantEditPctWrkCompForNonWrkRscs = 1057  <br/> |**PctWorkComplete** kann nicht für eine Aufgabe ohne wirkliche Arbeitszuordnung bearbeitet werden.  <br/> |
|ProjectCannotEditMaterialResource = 1058  <br/> |Die Materialressource kann nicht bearbeitet werden.  <br/> |
|ProjectCannotEditFieldWhenTaskHasNoWorkAssignment = 1059  <br/> |Das Feld kann nicht bearbeitet werden, da die Aufgabe keine Arbeitszuordnung hat.  <br/> |
|ProjectSubProjectNotFound = 1070  <br/> |. Es wurden keine Unterprojekte gefunden.  <br/> |
|ProjectResourceNotFound = 1100  <br/> |Ressource nicht gefunden.  <br/> |
|ProjectResourceAlreadyExists = 1101  <br/> |Ressource bereits vorhanden.  <br/> |
|ProjectCannotReplaceResourceWithSelf = 1106  <br/> |Ressource kann nicht durch dasselbe Objekt ersetzt werden.  <br/> |
|ProjectCannotChangeLockedTrackingMethod = 1107  <br/> |Kann nicht geändert werden, da die Überwachungsmethode gesperrt ist.  <br/> |
|ProjectInvalidColumnForCompatibilityMode = 1108  <br/> |Die Spalte für den Kompatibilitätsmodus ist ungültig.  <br/> |
|ProjectUpdateInvalidUpdateSequenceNumber = 1151  <br/> |Die laufende Nummer in der Projektaktualisierung ist ungültig.  <br/> |
|ProjectUpdateDuplicateUpdateSequenceNumber = 1152  <br/> |Doppelte Sequenznummer in der Projektaktualisierung.  <br/> |
|ProjectUpdateNullUpdateSequenceNumber = 1153  <br/> |Keine Sequenznummer in der Projektaktualisierung.  <br/> |
|ProjectUpdateNullUpdateColumnNames = 1154  <br/> |Keine Spaltennamen in der Projektaktualisierung.  <br/> |
|ProjectUpdateInvalidProjectUID = 1155  <br/> |Die Projekt-GUID ist nicht gültig in der Projektaktualisierung.  <br/> |
|ProjectUpdateInvalidColumnForUpdate = 1156  <br/> |Die Spalte ist nicht gültig in der Projektaktualisierung.  <br/> |
|ProjectUpdateCannotEditColumn = 1157  <br/> |Spalte in der Projektaktualisierung kann nicht bearbeitet werden.  <br/> |
|ProjectUpdateNoChangesToValidateAndSchedule = 1158  <br/> |Die Projektaktualisierung enthält keine Änderungen, die bestätigt oder terminiert werden können.  <br/> |
|LinkNotFound = 1159  <br/> |Die Verknüpfung wurde nicht gefunden.  <br/> |
|ProjectUpdateInvalidColumnValue = 1160  <br/> |Der Spaltenwert ist in der Projektaktualisierung ungültig.  <br/> |
|ProjectCannotDeleteItem = 1161  <br/> |Das Projektelement kann nicht gelöscht werden.  <br/> |
|ProjectUpdateCannotComputeOptIndex = 1162  <br/> |Der Optimierungsindex in der Projektaktualisierung kann nicht berechnet werden.  <br/> |
|ProjectCannotUpdateDueToVisibilityMode = 1163  <br/> |Kann nicht aktualisiert werden, da sich das Projekt im Sichtbarkeitsmodus befindet.  <br/> |
|ProjectNodeConsistencyException = 9132  <br/> |Ausnahme: Der Knoten ist nicht konsistent.  <br/> |
|ProjectSchedulingEngineException = 9133  <br/> |Ausnahme im Planungsmodul.  <br/> |
|ProjectFormulaCalculationException = 9134  <br/> |Ausnahme in der Formelberechnung.  <br/> |
|ProjectUpdateDatabaseException = 9135  <br/> |Ausnahme bei der Datenbankaktualisierung.  <br/> |
|ProjectDeleteException = 9136  <br/> |Ausnahme beim Löschen des Projekts.  <br/> |
|ProjectOperationException = 9137  <br/> |Ausnahme beim Projektvorgang.  <br/> |
|ProjectCannotComunicateWithPCS = 9138  <br/> |Fehler bei Kommunikation mit PCS-Worker.  <br/> |
|ProjectPCSSessionInvalid = 9139  <br/> |Projekt konnte in einer Modulsitzung nicht geöffnet werden.  <br/> |
|ProjectPublishFailure = 23000  <br/> |Fehler in der Warteschlange beim Veröffentlichen des Projekts.  <br/> |
|ProjectCurrencyConflict = 23001  <br/> |Es besteht ein Konflikt in der angegebenen Währung.  <br/> |
|ProjectPublishFailed = 23002  <br/> |Veröffentlichung des Projekts nicht erfolgreich, als es in die Warteschlange gestellt wurde.  <br/> |
|ProjectReversePublishFailed = 23003  <br/> |Veröffentlichung des Projekts nicht erfolgreich, als es in die Warteschlange gestellt wurde.  <br/> |
|ProjectReversePublishFailure = 23004  <br/> |Rückgängigmachen der Projektveröffentlichung während der Warteschlangenverarbeitung nicht erfolgreich.  <br/> |
|ProjectArchiveRetentionDeleteFailure = 23005  <br/> |Fehler beim Löschen des Projekts aufgrund der Archivaufbewahrung.  <br/> |
|ProjectDeleteFailure = 23006  <br/> |Fehler beim Löschen von Projekt.  <br/> |
|ProjectPublishEnqueueFailure = 23007  <br/> |Fehler beim Projektveröffentlichung, als es in die Warteschlange gestellt wurde.  <br/> |
|ProjectCheckinFailure = 23008  <br/> |Einchecken von Projekt während der Warteschlangenverarbeitung nicht erfolgreich.  <br/> |
|ProjectCheckinFailed = 23009  <br/> |Einchecken von Projekt nicht erfolgreich, als es in die Warteschlange gestellt wurde.  <br/> |
|ProjectCheckoutFailed = 23010  <br/> |Der Benutzer hat keinen Berechtigung zum Auschecken des Projekts.  <br/> |
|ProjectPublishSummaryEnqueueFailure = 23011  <br/> |Veröffentlichung der Zusammenfassung nicht erfolgreich, als sie in die Warteschlange gestellt wurde.  <br/> |
|ProjectPublishSummaryFailed = 23012  <br/> |Fehler beim Veröffentlichen der Zusammenfassung.  <br/> |
|ProjectUpdateScheduledProjectFailure = 26026  <br/> |Fehler bei der Aktualisierung der Projektterminierung während der Warteschlangenverarbeitung.  <br/> |
|ProjectSyncProjectEnterpriseEntitiesFailure = 26033  <br/> |Fehler bei der Synchronisierung von Enterprise-Entitäten des Projekts während der Warteschlangenverarbeitung.  <br/> |
|GeneralDalDatabaseIsReadOnly = 26034  <br/> |Laden von Projektdrilldown nicht erfolgreich. Datenbank ist schreibgeschützt.  <br/> |
|GeneralDatabaseCommunicationError = 26035  <br/> |Dies kann mehrere Ursachen haben, wie Netzwerk- oder Authentifizierungsprobleme.  <br/> |

<a name="pj15_ErrorCodes_RDS"></a>

## <a name="table-19-reporting-data-service-rds"></a>Tabelle 19. Reporting Data Service (RDS)

|Fehlercode - RDS|Beschreibung|
|:-----|:-----|
|ReportingAttributeCubeSettingsChangedMessageFailed = 24000  <br/> |RDS-Änderungsnachricht für ein Cube-Einstellungsattribut nicht erfolgreich.  <br/> |
|ReportingBaseCalendarChangeMessageFailed = 24001  <br/> |RDS-Änderungsnachricht für einen Basiskalender nicht erfolgreich.  <br/> |
|ReportingCustomFieldMetadataChangeMessageFailed = 24002  <br/> |RDS-Änderungsnachricht für Metadaten eines benutzerdefinierten Felds nicht erfolgreich.  <br/> |
|ReportingEntityUserViewChangedMessageFailed = 24003  <br/> |RDS-Änderungsnachricht für eine Benutzersicht einer Entität nicht erfolgreich.  <br/> |
|ReportingFiscalPeriodChangeMessageFailed = 24004  <br/> |RDS-Änderungsnachricht für ein Geschäftsjahr nicht erfolgreich.  <br/> |
|ReportingLookupTableChangeMessageFailed = 24005  <br/> |RDS-Änderungsnachricht für eine Nachschlagetabelle nicht erfolgreich.  <br/> |
|ReportingProjectChangeMessageFailed = 24006  <br/> |RDS-Änderungsnachricht für ein Projekt nicht erfolgreich.  <br/> |
|ReportingResourceCapacityUpdateMessageFailed = 24007  <br/> |RDS-Aktualisierungsnacht für Ressourcenkapazität nicht erfolgreich.  <br/> |
|ReportingResourceChangeMessageFailed = 24008  <br/> |RDS-Änderungsnachricht für eine Ressource nicht erfolgreich.  <br/> |
|ReportingTimesheetAdjustMessageFailed = 24009  <br/> |RDS-Anpassungsnachricht für eine Arbeitszeittabelle nicht erfolgreich.  <br/> |
|ReportingTimesheetClassCreateMessageFailed = 24010  <br/> |RDS-Erstellungsnachricht für eine Arbeitszeittabellenklasse nicht erfolgreich.  <br/> |
|ReportingTimesheetDeleteMessageFailed = 24011  <br/> |RDS-Löschnachricht für eine Arbeitszeittabelle nicht erfolgreich.  <br/> |
|ReportingTimesheetPeriodDeleteMessageFailed = 24012  <br/> |RDS-Löschnachricht für eine Arbeitszeittabellenperiode nicht erfolgreich.  <br/> |
|ReportingTimesheetPeriodMessageFailed = 24013  <br/> |RDS-Nachricht für eine Arbeitszeittabellenperiode nicht erfolgreich.  <br/> |
|ReportingTimesheetSaveMessageFailed = 24014  <br/> |RDS-Speicherungsnachricht für eine Arbeitszeittabelle nicht erfolgreich.  <br/> |
|ReportingTimesheetStatusChangeMessageFailed = 24015  <br/> |RDS-Änderungsnachricht für einen Arbeitszeittabellenstatus nicht erfolgreich.  <br/> |
|ReportingWSSSyncMessageFailed = 24016  <br/> |RDS-Nachricht für SharePoint-Synchronisierung nicht erfolgreich.  <br/> |
|ReportingGetSPWebFailed = 24017  <br/> |RDS nicht erfolgreich beim Abrufen des SharePoint-Webwerts.  <br/> |
|ReportingWssSyncListFailed = 24018  <br/> |RDS nicht erfolgreich beim Synchronisieren mit der SharePoint-Liste.  <br/> |
|ReportingWssTransferLinksFailed = 24019  <br/> |RDS nicht erfolgreich beim Übertragen von SharePoint-Links.  <br/> |
|ReportingQueueMessageSubmitFailed = 24020  <br/> |RDS nicht erfolgreich beim Übertragen einer Nachricht an die Warteschlange.  <br/> |
|ReportingWssSyncHRefFailed = 24021  <br/> |RDS nicht erfolgreich beim Synchronisieren mit dem SharePoint-HRef-Wert.  <br/> |
|ReportingSyncGlobalDataMessageFailed = 24022  <br/> |RDS-Nachricht nicht erfolgreich beim Synchronisieren mit Enterprise Global-Daten.  <br/> |
|ReportingRDBRefreshMessageFailed = 24023  <br/> |RDS-Nachricht beim Aktualisieren der RDB nicht erfolgreich.  <br/> |
|ReportingAttributeCubeDepartmentsChangedMessageFailed = 24024  <br/> |RDS-Nachricht beim Ändern des Abteilungsattributs für den OLAP-Cube nicht erfolgreich.  <br/> |
|ReportingTimesheetProjectAggregationMessageFailed = 24025  <br/> |RDS-Nachricht bei Aggregieren von Projekten für Arbeitszeittabellen in der RDB nicht erfolgreich.  <br/> |
|ReportingRdbBulkDataSyncMessageFailed = 24026  <br/> |RDS-Nachricht nicht erfolgreich bei der Massendatensynchronisierung in der RDB.  <br/> |
|ReportingWorkflowMetadataSyncMessageFailed = 24027  <br/> |RDS-Nachricht beim Synchronisieren von Workflowdaten nicht erfolgreich.  <br/> |
|ReportingProjectWorkflowInformationSyncMessageFailed = 24028  <br/> |RDS-Nachricht beim Synchronisieren von Projektworkflowinformationen nicht erfolgreich.  <br/> |
|ReportingEptSyncMessageFailed = 24029  <br/> |RDS-Nachricht beim Synchronisieren der Enterprise-Projektvorlage nicht erfolgreich.  <br/> |
|ReportingSummaryProjectPublishMessageFailed = 24030  <br/> |RDS-Nachricht beim Publizieren des Zusammenfassungsprojekts nicht erfolgreich.  <br/> |
|ReportingSolutionCommitedDecisionChangedMessageFailed = 24031  <br/> |RDS-Nachricht beim Ändern der gewählten Entscheidung für die Lösung nicht erfolgreich.  <br/> |
|ReportingDelayedUpgradeFailed = 24032  <br/> |Verzögerte RDB-Aktualisierung nicht erfolgreich.  <br/> |

<a name="pj15_ErrorCodes_Resources"></a>

## <a name="table-20-resource"></a>Tabelle 20. Ressource

|Fehlercode - Ressource|Beschreibung|
|:-----|:-----|
|ResourceNotFound = 2000  <br/> |Ressource nicht gefunden.  <br/> |
|ResourceAlreadyExists = 2001  <br/> |Ressource ist bereits vorhanden.  <br/> |
|ResourceCheckedoutToOtherUser = 2002  <br/> |Ressource für einen anderen Benutzer ausgecheckt..  <br/> |
|ResourceUIDInvalid = 2011  <br/> |Die Ressourcen-GUID ist ungültig.  <br/> |
|ResourceNameInvalid = 2016  <br/> |Der Ressourcenname ist ungültig.  <br/> |
|ResourceNameTooLong = 2017  <br/> |Ressourcenname ist zu lang.  <br/> |
|ResourceInitialsTooLong = 2018  <br/> |Ressourcenkürzel sind zu lang.  <br/> |
|ResourceCheckedout = 2025  <br/> |Die Ressource ist ausgecheckt.  <br/> |
|ResourceNTAccountInvalid = 2026  <br/> |Das Windows (NTLM)-Ressourcenkonto ist ungültig.  <br/> |
|ResourceNameAlreadyInUse = 2027  <br/> |Ressourcenname wird bereits verwendet. Namen müssen eindeutig sein.  <br/> |
|ResourceNTAccountAlreadyInUse = 2028  <br/> |Das NTLM-Ressourcenkonto wird bereits verwendet.  <br/> |
|ResourceAdGuidAlreadyInUse = 2029  <br/> |Die Ressourcen-GUID wird bereits verwendet.  <br/> |
|ResourceHasActuals = 2031  <br/> |Die Ressource hat aktuelle Werte.  <br/> |
|ResourceNTAccountTooLong = 2035  <br/> |Das NTLM-Konto ist zu lang.  <br/> |
|ResourceEMailAddressTooLong = 2036  <br/> |Die Ressourcen-E-Mail-Adresse ist zu lang.  <br/> |
|ResourceCodeTooLong = 2037  <br/> |Der Ressourcencode ist zu lang.  <br/> |
|ResourceGroupTooLong = 2038  <br/> |Die Ressourcengruppe ist zu lang.  <br/> |
|ResourceWorkGroupInvalid = 2039  <br/> |Die Arbeitsgruppe für Ressource ist ungültig.  <br/> |
|ResourceTypeInvalid = 2040  <br/> |Der Ressourcentyp ist ungültig.  <br/> |
|ResourceNonWorkResourceWithEMailInvalid = 2044  <br/> |Eine nicht funktionierende Ressource kann keine E-Mail-Adresse haben.  <br/> |
|rsResourceNameHasTrailingOrLeadingWhitespace = 2046  <br/> |Die Ressource hat führende oder nachfolgende Leerzeichen.  <br/> |
|ResourceCannotDeleteCallingUserAccount = 2047  <br/> |Der Benutzer kann nicht sein eigenes Konto nicht löschen.  <br/> |
|ResourceInitialsInvalid = 2048  <br/> |Die Ressourcenkürzel sind ungültig.  <br/> |
|ResourceAccrueAtInvalid = 2049  <br/> |Der Wert für die Fälligkeit ist ungültig.  <br/> |
|ResourceNonMaterialResourceCannotHaveMaterialLabel = 2050  <br/> |Eine Nicht-Materialressource kann nicht keine Materialbeschriftung aufweisen  <br/> |
|ResourceMaterialResourceCannotHaveCertainFields = 2051  <br/> |Eine Materialressource kann bestimmte Felder nicht haben.  <br/> |
|ResourceAvailFromAvailToOverlap = 2052  <br/> |Überlappung von Verfügbar-Ab- und Verfügbar-Bis-Daten.  <br/> |
|ResourceInvalidEmailLanguage = 2053  <br/> |Die E-Mail-Sprache ist ungültig.  <br/> |
|ResourceBookingTypeInvalid = 2055  <br/> |Der Buchungstyp ist ungültig.  <br/> |
|ResourceCannotReplaceMaterialResourceWithNonMaterialResource = 2056  <br/> |Materialressource kann nicht durch Nicht-Materialressource ersetzt werden.  <br/> |
|ResourceCannotUpdateEnterpriseResource = 2057  <br/> |Enterprise-Ressource kann nicht aktualisiert werden.  <br/> |
|rsResourceCannotAddLocalWithSameNameAsEnterprise = 2058  <br/> |Lokale Ressource gleichen Namens kann nicht als Enterprise-Ressourcen hinzugefügt werden.  <br/> |
|ResourceCannotSetRateOnCostResource = 2059  <br/> |Satz für Kostenressource kann nicht festgelegt werden.  <br/> |
|ResourceCannotSetRateOnMaterialResource = 2060  <br/> |Satz für Materialressource kann nicht festgelegt werden.  <br/> |
|ResourceCannotSetCanLevelOnNonWorkResource = 2061  <br/> |Ebene für Nicht-Arbeitsressource kann nicht festgelegt werden.  <br/> |
|ResourceCannotDeleteThisUser = 2062  <br/> |Dieser Benutzer kann nicht gelöscht werden.  <br/> |
|ResourceCannotDeactivateSelf = 2063  <br/> |Eine Ressource kann nicht sich selbst deaktivieren.  <br/> |
|ResourceAvailabilityDateRangesOverlap = 2064  <br/> |Datumsbereich der Ressourcenverfügbarkeit überlappen sich.  <br/> |
|ResourceAvailabilityOutsideTheHireAndTerminationDateRange = 2065  <br/> |Das Datum der Ressourcenverfügbarkeit liegt außerhalb des Datumsbereichs für Einstellung und Kündigung.  <br/> |
|ResourceFilterInvalid = 2066  <br/> |Der Filter für eine Ressource ist ungültig.  <br/> |
|ResourceSegmentWithThisEffectiveDateDoesNotExist = 2067  <br/> |Ein Ressourcensatz, der noch nicht gespeichert wurde, kann nicht gelöscht werden.  <br/> |
|ResourceSegmentWithThisEffectiveDateAlready = 2068  <br/> |Ein Segment mit diesem Gültigkeitsdatum bereits vorhanden ist.  <br/> |
|ResourceUserHasItemCheckedOutToItStill = 2069  <br/> |Der Benutzer hat ein Element immer noch ausgecheckt..  <br/> |
|ResourceInvalidHireDate = 2070  <br/> |Das Einstellungsdatum ist ungültig.  <br/> |
|ResourceInvalidTerminationDate = 2071  <br/> |Das Enddatum ist ungültig.  <br/> |
|ResourceCannotChangeExistingResourceType = 2072  <br/> |Ressourcentyp kann nicht geändert werden.  <br/> |
|ResourceCannotSetTimesheetManagerOnSpecifiedResource = 2073  <br/> |Der Arbeitszeittabellen-Manager kann nicht für die angegebene Ressource festgelegt werden.  <br/> |
|ResourceInvalidTimesheetManager = 2074  <br/> |Der Arbeitszeittabellen-Manager ist ungültig.  <br/> |
|ResourceInvalidAssignmentOwner = 2075  <br/> |Der Zuordnungsbesitzer ist ungültig.  <br/> |
|ResourceCannotCreateCostResource = 2076  <br/> |Kostenressource kann nicht erstellt werden.  <br/> |
|ResourceInvalidRbsValue = 2077  <br/> |Der RSP-Wert ist ungültig.  <br/> |
|ResourceCannotSetAssignmentOwnerOnSpecifiedResource = 2078  <br/> |Zuordnungsbesitzer kann nicht für die angegebene Ressource festgelegt werden.  <br/> |
|ResourceFieldsInvalidForBudget = 2079  <br/> |Mindestens ein Feld für das Budget ist ungültig.  <br/> |
|ResourceHyperlinkInvalid = 2080  <br/> |Der Ressourcenhyperlink ist ungültig.  <br/> |
|ResourceAuthorizationValidOnlyOnWorkResources = 2081  <br/> |Die Autorisierung gilt nur für Arbeitsressourcen.  <br/> |
|ResourceIsProjectOwner = 2082  <br/> |Ressource kann nicht gelöscht werden, da die Ressource der Projektbesitzer ist.  <br/> |
|ResourceIsTimesheetManager = 2083  <br/> |Ressource kann nicht gelöscht werden, da die Ressource der Arbeitszeittabellen-Manager ist.  <br/> |
|ResourceIsDefaultAssignmentOwner = 2084  <br/> |Ressource kann nicht gelöscht werden, da die Ressource der Standardzuordnungsbesitzer ist.  <br/> |
|ResourceIsAssignmentOwner = 2085  <br/> |Ressource kann nicht gelöscht werden, da die Ressource des Zuordnungsbesitzers ist.  <br/> |
|ResourceIsUsedInResourcePlan = 2086  <br/> |Ressource kann nicht gelöscht werden, da sie im Ressourcenplan verwendet wird.  <br/> |
|ResourceCannotDeleteEnterpriseResource = 2087  <br/> |Enterprise-Ressource kann aus unbekanntem Grund nicht gelöscht werden.  <br/> |
|ResourceSetResourceAuthorizationFailed = 2088  <br/> |Fehler beim Festlegen der Ressourcenautorisierung.  <br/> |
|ResourceTooManyResourcesSpecifiedToDelete = 2089  <br/> |Die Anzahl der angegebenen Ressourcen kann nicht gelöscht werden.  <br/> |
|ResourceTooManyResourcesReturned = 2090  <br/> |Die Methode kann nicht die Anzahl der Ressourcen nicht verarbeiten.  <br/> |
|ResourceCannotDeleteWorkflowProxyUser = 2091  <br/> |Der Workflow-Proxybenutzer kann nicht gelöscht werden.  <br/> |
|ResourceInvalidEmailWithExchangeSync = 2092  <br/> |Die E-Mail ist nicht gültig für eine Synchronisierung mit Microsoft Exchange Server.  <br/> |
|ResourceInvalidResourceTypeWithExchangeSync = 2093  <br/> |Der Ressourcentyp ist nicht gültig für eine Synchronisierung mit Exchange Server.  <br/> |
|ResourceInvalidPrincipalNameWithExchangeSync = 2094  <br/> |Der Prinzipalname der Ressource ist nicht gültig für eine Synchronisierung mit Exchange Server.  <br/> |
|ResourceInvalidAuthenticationTypeWithExchangeSync = 2095  <br/> |Der Authentifizierungstyp der Ressource ist nicht gültig für eine Synchronisierung mit Exchange Server.  <br/> |
|ResourceExchangeSyncFlagAndPrincipalNameMismatch = 2096  <br/> |Keine Übereinstimmung zwischen dem Exchange Server-Synchronisierungskennzeichen und dem Prinzipalnamen für die Ressource.  <br/> |
|ResourceUnsupportedUserUpdateInSharePointSecurityMode = 2097  <br/> |Die Erstellung des Benutzers wird im Sicherheitsmodus SharePoint nicht unterstützt.  <br/> |

<a name="pj15_ErrorCodes_ResourcePlans"></a>

## <a name="table-21-resource-plan"></a>Tabelle 21. Ressourcenplan

|Fehlercode - Ressourcenplan|Beschreibung|
|:-----|:-----|
|ResourcePlanProjectPublishIncomplete = 30000  <br/> |Veröffentlichen des Projekts für den Ressourcenplan konnte nicht abgeschlossen werden.  <br/> |
|ResourcePlanInvalidResourceType = 30001  <br/> |Der Ressourcentyp im Ressourcenplan ist ungültig.  <br/> |
|ResourcePlanInactiveResourcesDisallowed = 30002  <br/> |Inaktive Ressourcen sind in einem Ressourcenplan nicht zulässig.  <br/> |
|ResourcePlanFilterInvalid = 30003  <br/> |Der Ressourcenplanfilter ist ungültig.  <br/> |
|ResourcePlanSaveFailure = 30004  <br/> |Speichern des Ressourcenplans nicht erfolgreich.  <br/> |
|ResourcePlanCheckinFailure = 30005  <br/> |Einchecken des Ressourcenplans nicht erfolgreich.  <br/> |
|ResourcePlanDeleteFailure = 30006  <br/> |Löschen des Ressourcenplans nicht erfolgreich.  <br/> |
|ResourcePlanInvalidUtilizationType = 30007  <br/> |Der Typ der Ressourcenplanauslastung ist ungültig.  <br/> |
|ResourcePlanInvalidTimescale = 30008  <br/> |Die Ressourceplan-Zeitskala ist ungültig.  <br/> |
|ResourcePlanMismatchedJobList = 30009  <br/> |Vorgangsliste für Ressourcenplan stimmt nicht überein  <br/> |
|ResourcePlanAlreadyExists = 30010  <br/> |Ressourcenplan ist bereits vorhanden.  <br/> |
|ResourcePlanInvalidProjectUID = 30011  <br/> |Die Projekt-GUID für den Ressourcenplan ist ungültig.  <br/> |
|ResourcePlanResourceAlreadyExists = 30012  <br/> |Die Ressource ist bereits im Ressourcenplan vorhanden.  <br/> |
   
Die Fehlercodes in Tabelle 22 gelten für die **Rules**-Methoden im **PWA**-Webdienst. Sie werden intern verwendet. 

<a name="pj15_ErrorCodes_Rules"></a>

## <a name="table-22-rules"></a>Tabelle 22. Regeln

|Fehlercode Regeln|Beschreibung|
|:-----|:-----|
|RulesNameTooLong = 21001  <br/> |Der Name der genehmigungsregel ist zu lang. Nur in Project Web App zur internen Verwendung.  <br/> |
|RulesDescriptionTooLong = 21002  <br/> |Beschreibung der Regel ist zu lang. Nur in Project Web App zur internen Verwendung.  <br/> |
|RulesInvalidRuleType = 21003  <br/> |Der Typ ist ungültig. Nur in Project Web App zur internen Verwendung.  <br/> |
|RulesInvalidConditionType = 21004  <br/> |Bedingungstyp für eine Regel ist ungültig. Nur in Project Web App zur internen Verwendung.  <br/> |
|RulesInvalidOperatorType = 21005  <br/> |Der Operatortyp für eine Regel ist ungültig. Nur in Project Web App zur internen Verwendung.  <br/> |
|RulesInvalidListItemType = 21007  <br/> |Der Listenelementtyp für eine Regel ist ungültig. Nur in Project Web App zur internen Verwendung.  <br/> |
|RulesNameInvalidCharacters = 21008  <br/> |Es gibt ein oder mehrere Zeichen im Namen Regel, die nicht gültig sind. Nur in Project Web App zur internen Verwendung.  <br/> |
|RulesDescriptionInvalidCharacters = 21009  <br/> |Es gibt eine oder mehrere Zeichen in der Regel Beschreibung, die nicht gültig sind. Nur in Project Web App zur internen Verwendung.  <br/> |
|RulesInvalidValueType = 21010  <br/> |Der Werttyp in der Regel ist ungültig. Nur in Project Web App zur internen Verwendung.  <br/> |

<a name="pj15_ErrorCodes_Security"></a>

## <a name="table-23-security"></a>Tabelle 23. Sicherheit

|Fehlercode - Sicherheit|Beschreibung|
|:-----|:-----|
|SecurityGroupCouldNotBeCreated = 19001  <br/> |Sicherheitsgruppe kann nicht erstellt werden.  <br/> |
|SecurityFieldAccessIDInvalid = 19003  <br/> |Die Kennnummer des Zugriffscodes für das Sicherheitsfeld ist ungültig.  <br/> |
|SecurityCannotUpdateFacForNonExistentCategory = 19004  <br/> |Kategorie "Sicherheit" ist nicht vorhanden. Der Feldzugriffscode kann nicht aktualisiert werden.  <br/> |
|SecurityDuplicateCategoryUid = 19005  <br/> |Doppelte Sicherheitskategorie-GUID.  <br/> |
|SecurityDuplicateGroupUid = 19006  <br/> |Doppelte Sicherheitsgruppen-GUID.  <br/> |
|SecurityDuplicateTemplateUid = 19007  <br/> |Doppelte Sicherheitsvorlagen-GUID.  <br/> |
|SecurityInvalidTemplateUidRef = 19008  <br/> |Die Sicherheitsvorlagen-GUID ist ungültig.  <br/> |
|SecurityInvalidGlobalPermission = 19009  <br/> |Die globale Sicherheitsberechtigung ist ungültig.  <br/> |
|SecurityInvalidCategoryPermission = 19010  <br/> |Die Sicherheitskategorieberechtigung ist ungültig.  <br/> |
|SecurityUpdatedGroupNotFound = 19013  <br/> |Aktualisierte Sicherheitsgruppe wurde nicht gefunden.  <br/> |
|SecurityUpdatedCategoryNotFound = 19014  <br/> |Aktualisierte Sicherheitskategorie wurde nicht gefunden.  <br/> |
|SecurityUpdatedTemplateNotFound = 19015  <br/> |Aktualisierte Sicherheitsvorlage wurde nicht gefunden.  <br/> |
|SecurityGroupMemberNotFound = 19016  <br/> |Mitglied der Sicherheitsgruppe wurde nicht gefunden.  <br/> |
|SecurityUserNotFound = 19018  <br/> |Project Server-Benutzer nicht gefunden.  <br/> |
|SecurityNoCategoryRelationForPermission = 19019  <br/> |Sicherheitskategoriebeziehung für die Berechtigung wurde nicht gefunden.  <br/> |
|SecurityCannotDeleteDefaultGroup = 19020  <br/> |Standardsicherheitsgruppe kann nicht gelöscht werden.  <br/> |
|SecurityCannotDeleteDefaultCategory = 19021  <br/> |Standardsicherheitskategorie kann nicht gelöscht werden.  <br/> |
|SecurityCategoryCouldNotBeCreated = 19022  <br/> |Sicherheitskategorie kann nicht erstellt werden.  <br/> |
|SecurityNoCategoryForPermission = 19023  <br/> |Sicherheitskategorie für die Berechtigung wurde nicht gefunden.  <br/> |
|SecurityNoCategoryForObject = 19024  <br/> |Sicherheitskategorie für das Objekt wurde nicht gefunden.  <br/> |
|SecurityNoCategoryForRule = 19025  <br/> |Sicherheitskategorie für die Regel wurde nicht gefunden.  <br/> |
|SecurityNoGroupForPermission = 19026  <br/> |Sicherheitsgruppe für die Berechtigung wurde nicht gefunden.  <br/> |
|SecurityCannotSetPermissionForFieldGroup = 19027  <br/> |Berechtigung für das Sicherheitsgruppenfeld kann nicht festgelegt werden.  <br/> |
|SecurityInvalidFieldGroup = 19028  <br/> |Das Sicherheitsgruppenfeld ist ungültig.  <br/> |
|SecurityCannotSetOrgPermission = 19029  <br/> |Die Sicherheitsberechtigung für die Organisation kann nicht festgelegt werden.  <br/> |
|SecurityInvalidOrgPermission = 19030  <br/> |Die Sicherheitsberechtigung für die Organisation ist ungültig.  <br/> |
|SecurityInvalidSecurityRule = 19031  <br/> |Die Sicherheitsregel ist ungültig.  <br/> |
|SecurityTemplateNotFound = 19034  <br/> |Sicherheitsvorlage wurde nicht gefunden.  <br/> |
|SecurityInvalidObjectType = 19035  <br/> |Der Typ des Sicherheitsobjekts ist ungültig.  <br/> |
|SecurityDuplicateUid = 19036  <br/> |Die GUID des Sicherheitsobjekts ist ein Duplikat.  <br/> |
|SecurityObjectNotFound = 19037  <br/> |Das Sicherheitsobjekt wurde nicht gefunden.  <br/> |
|SecurityInvalidCategoryUidRef = 19080  <br/> |Die GUID der Sicherheitskategorie ist ungültig.  <br/> |
|SecurityInvalidProjectUidRef = 19081  <br/> |Das Projekt-GUID für das Sicherheitsobjekt ist ungültig.  <br/> |
|SecurityInvalidGroupUidRef = 19082  <br/> |Die Sicherheitsgruppen-GUID ist ungültig.  <br/> |
|SecurityInvalidUserUidRef = 19083  <br/> |Die Benutzer-GUID für das Sicherheitsobjekt ist ungültig.  <br/> |
|SecurityInvalidCategoryPermissionUidRef = 19084  <br/> |Die Berechtigungs-GUID für die Sicherheitskategorie ist ungültig.  <br/> |
|SecurityInvalidGlobalPermissionUidRef = 19085  <br/> |Die globale Sicherheitsberechtigungs-GUID ist ungültig.  <br/> |
|SecurityInvalidResourceUidRef = 19086  <br/> |Die Ressourcen-GUID für das Sicherheitsobjekt ist ungültig.  <br/> |
|SecurityDeleteNotSupportedBySetMethod = 19087  <br/> |Die Methode kann das Sicherheitsobjekt nicht löschen.  <br/> |
|SecurityInvalidProjectCategoryPermissionUidRef = 19088  <br/> |Die GUID der Projektkategorieberechtigung ist ungültig.  <br/> |
|SecurityCannotModifyCoreProjectCategoryDataInUpdate = 19089  <br/> |Die Methode zur Sicherheitsaktualisierung kann die Daten der Kernprojektkategorie nicht ändern.  <br/> |
|SecurityProjectCategoryEntitiesDoNotAllowInPlaceChanges = 19090  <br/> |Entitäten der Sicherheitskategorie können in einer Aktualisierung nicht geändert werden.  <br/> |
|SecurityCategoryCannotAddRelationForDeletedCategory = 19091  <br/> |Eine Beziehung für eine gelöschte Sicherheitskategorie kann nicht hinzugefügt werden.  <br/> |
|SecurityCategoryCannotAddPermissionForDeletedCategory = 19092  <br/> |Eine Berechtigung für eine gelöschte Sicherheitskategorie kann nicht hinzugefügt werden.  <br/> |
|SecurityCategoryCannotAddPermissionForDeletedRelation = 19093  <br/> |Eine Berechtigung für eine Sicherheitskategoriebeziehung gelöschten Sicherheit kann nicht hinzugefügt werden.  <br/> |
|SecurityCategoryCannotDeleteRelationForNewlyAddedCategory = 19094  <br/> |Die Beziehung für eine neu hinzugefügte Sicherheitskategorie kann nicht gelöscht werden.  <br/> |
|SecurityCategoryCannotDeletePermissionForNewlyAddedCategory = 19095  <br/> |Die Berechtigung für eine neu hinzugefügte Sicherheitskategorie kann nicht gelöscht werden.  <br/> |
|SecurityCategoryCannotDeletePermissionForNewlyAddedRelation = 19096  <br/> |Die Berechtigung für eine neu hinzugefügte Beziehung in einer Sicherheitskategorie kann nicht gelöscht werden.  <br/> |
|SecurityCategoryCannotHaveDuplicateUserOrGroupUidsForRelation = 19097  <br/> |Doppelte Benutzer- oder Gruppen-UIDs für eine Sicherheitskategoriebeziehung sind nicht möglich.  <br/> |
|SecurityCategoryPermissionMustHaveMatchingRelation = 19098  <br/> |Eine Kategorieberechtigung muss eine entsprechende Sicherheitskategoriebeziehung haben.  <br/> |
|SecurityCategoryProjectAlreadyHasSecurityProjectCategory = 19099  <br/> |Die Liste der gewählten Kategorien hat bereits eine Projektsicherheitskategorie.  <br/> |

<a name="pj15_ErrorCodes_Events"></a>

## <a name="table-24-project-server-event"></a>Tabelle 24. Project Server-Ereignis

|Fehlercode - Project Server-Ereignis|Beschreibung|
|:-----|:-----|
|ServerEventInvalidEventId = 19033  <br/> |Die Project Server-Ereignis-Kennnummer ist ungültig.  <br/> |
|ServerEventServiceNotFound = 22003  <br/> |Der Project Server-Ereignisdienst wurde nicht gefunden. Dieser Fehler gilt nicht für den Project Server-Code, aber er stimmt mit einem Raw-ULS-Ereignis (Unified Logging Service) überein.  <br/> |
|ServerEventRemoteCouldNotReachProxy = 22005  <br/> |Remoteanrufsteuerung Project Web App konnte den Project Server-Ereignis-Manager-Proxy nicht erreichen. Dieser Fehler wird nicht in Project Server-Code verwendet, aber es wird ein Roh ULS-Ereignis zugeordnet.  <br/> |
|ServerEventManagerCouldNotReachRemote = 22006  <br/> |Der Project Server-Ereignis-Manager konnte die remote Project Web App nicht erreicht werden. Dieser Fehler wird nicht in Project Server-Code verwendet, aber es wird ein Roh ULS-Ereignis zugeordnet.  <br/> |
|ServerEventHandlerNotSigned = 22007  <br/> |Der Project Server-Ereignishandler ist nicht signiert.  <br/> |
|ServerEventHandlerMalformedAssemblyName = 22008  <br/> |Der Assembly-Name für den Project Server-Ereignishandler ist ungültig.  <br/> |
|ServerEventHandlerOrderInvalid = 22009  <br/> |Die Reihenfolge für den Project Server-Ereignishandler ist ungültig.  <br/> |
|ServerEventHandlerDuplicateEntry = 22010  <br/> |Doppelter Eintrag für den Project Server-Ereignishandler.  <br/> |
|ServerEventHandlerNotFound = 22011  <br/> |Project Server-Ereignishandler nicht gefunden.  <br/> |
|ServerEventHandlerDuplicateName = 22012  <br/> |Doppelter Name für den Project Server-Ereignishandler.  <br/> |
|ServerEventHandlerNullAssemblyNameAndEndpointUrl = 22013  <br/> |bestätigen, dass es entweder eine Endpunkt-URL oder einen Assembly-Namen gibt.  <br/> |

<a name="pj15_ErrorCodes_Statusing"></a>

## <a name="table-25-statusing-web-service"></a>Tabelle 25. Statusing-Webdienst 

|Fehlercode-statuserfassung Web service|Beschreibung|
|:-----|:-----|
|StatusingInvalidEntity = 3102  <br/> |Die Entität für **Statusing** ist ungültig.  <br/> |
|StatusingGetDataForTaskFailed = 3103  <br/> |Abrufen von Daten für Vorgangsstatus nicht erfolgreich.  <br/> |
|StatusingGetTaskOrAssnCntrFailed = 3104  <br/> |Abrufen von Vorgang oder Zuordnungscenter für Status nicht erfolgreich.  <br/> |
|StatusingInvalidPIDForProjCntr = 3105  <br/> |Die **Statusing**-Eigenschaftskennnummer für Project Center ist ungültig.  <br/> |
|StatusingDeleteAssnFailed = 3106  <br/> |Die Zuordnung im **Statusing**-Prozess konnte nicht gelöscht werden.  <br/> |
|StatusingAssnSaveFailed = 3107  <br/> |Die Zuordnung im **Statusing**-Prozess konnten nicht gespeichert werden.  <br/> |
|StatusingTaskSaveFailed = 3108  <br/> |Der Vorgang im **Statusing**-Prozess konnte nicht gespeichert werden.  <br/> |
|StatusingInvalidPID = 3109  <br/> |Die **Statusing**-Eigenschaftskennnummer ist ungültig.  <br/> |
|StatusingSetDataValueInvalid = 3111  <br/> |Der **Statusing**-Datenwert ist ungültig.  <br/> |
|StatusingSetDataFailed = 3112  <br/> |Der **Statusing**-Datenwert konnte nicht festgelegt werden.  <br/> |
|StatusingInvalidDelegationStart = 3113  <br/> |Die Startzeit für eine Zuordnung in der **DelegateAssignments**-Methode ist ungültig.  <br/> |
|StatusingApprovalUpdateFailed = 3114  <br/> |Statusgenehmigung konnte nicht aktualisiert werden.  <br/> |
|StatusingInvalidApprovalType = 3115  <br/> |Der Typ der Statusgenehmigung ist ungültig.  <br/> |
|StatusingInternalError = 3116  <br/> |Interner Verarbeitungsfehler in einer **Statusing**-Methode.  <br/> |
|StatusingInvalidUpdateData = 3117  <br/> |Die Aktualisierungsdaten in einer **Statusing**-Methode sind ungültig.  <br/> |
|StatusingProjectUpdateFailed = 3118  <br/> |**Statusing**-Aktualisierung von Projekt nicht erfolgreich.  <br/> |
|StatusingInvalidPreviewData = 3119  <br/> |Die **Statusing**-Datenvorschau ist ungültig.  <br/> |
|StatusingInvalidTransaction = 3120  <br/> |Die **Statusing**-Transaktion ist ungültig.  <br/> |
|StatusingTooManyResults = 3121  <br/> |Zu viele Ergebnisse. Es würden mehr als 5.000 Zeilen beim Lesen von Statusdaten mit Zeitphasen zurückgegeben.  <br/> |
|StatusingInvalidInterval = 3122  <br/> |Das Intervall in einer **Statusing**-Methode ist ungültig. Das Intervall muss in Minuten angegeben werden und größer null sein.<br/> |
|StatusingApplyUpdatesFailed = 3123  <br/> |**Statusing**-Aktualisierungen konnten nicht angewendet werden, als die Anforderung in die Warteschlange gestellt wurde.  <br/> |
|StatusingApplyUpdatesFailure = 3124  <br/> |**Statusing**-Aktualisierungen konnten während der Verarbeitung der Warteschlange nicht angewendet werden.  <br/> |
|StatusingInvalidWorkData = 3125  <br/> |Die Arbeitsdaten für **Statusing** sind ungültig.  <br/> |
|StatusingMissingNameAttribute = 3126  <br/> |Namensattribut für **Statusing** fehlt.  <br/> |
|StatusingInvalidNameAttribute = 3127  <br/> |Das Namensattribut für **Statusing** ist ungültig.  <br/> |
|StatusingInvalidData = 3128  <br/> |Die **Statusing**-Daten sind ungültig.  <br/> |
|StatusingInvalidChangelist = 3130  <br/> |Die XML-Daten ist ungültig im _Changexml_ -Parameter der **UpdateStatus** -Methode.  <br/> |
|StatusingInsufficientAssignmentRights = 3131  <br/> |**SetAssignmentWorkData** kann eine Zuordnung nicht aktualisieren, da der Benutzer keine Berechtigung hat.  <br/> |
|StatusingInvalidChangeNumber = 3132  <br/> |Die **Statusing**-Änderungsnummer ist ungültig.  <br/> |
|StatusingPidNotEditable = 3133  <br/> |Die **Statusing**-Eigenschaftskennnummer kann nicht bearbeitet werden.  <br/> |
|StatusingCannotSetTimephasedDataInManualTasks = 3134  <br/> |Daten mit Zeitphase in manuellen Vorgängen für **Statusing** können nicht festgelegt werden.  <br/> |
|StatusingCannotChangeTaskMode = 3135  <br/> |Der Vorgangsmodus für **Statusing** kann nicht geändert werden.  <br/> |
   
Die Fehlercodes in Tabelle 26 sind für **StatusReports** Methoden in der **PWA** -Webdienst. Sie werden in Project Web App intern verwendet. 

<a name="pj15_ErrorCodes_StatusReports"></a>

## <a name="table-26-statusreports"></a>Tabelle 26. StatusReports 

|Fehlercode - Statusbericht|Beschreibung|
|:-----|:-----|
|StatusReportsUnknownError = 12100  <br/> |Unbekannter Fehler in **StatusReports**.  <br/> |
|StatusReportsPeriodUnmatched = 12101  <br/> |Zeitraum für Statusbericht stimmt nicht überein.  <br/> |
|StatusReportsPeriodUnavailable = 12102  <br/> |Zeitraum für Statusbericht ist nicht verfügbar.  <br/> |
|StatusReportsInvalidFormInput = 12103  <br/> |Daten im Statusberichtsformular sind ungültig.  <br/> |

<a name="pj15_ErrorCodes_Tasks"></a>

## <a name="table-27-task"></a>Tabelle 27. Aufgabe 

|Fehlercode - Vorgang|Beschreibung|
|:-----|:-----|
|TaskIDInvalid = 7001  <br/> |Die Vorgangs-GUID ist ungültig.  <br/> |
|TaskNameTooLong = 7003  <br/> |Vorgangsname ist zu lang.  <br/> |
|TaskTypeInvalid = 7005  <br/> |Der Vorgangstyp ist ungültig.  <br/> |
|TaskPriorityInvalid = 7006  <br/> |Die Vorgangspriorität ist ungültig.  <br/> |
|TaskConstraintTypeInvalid = 7007  <br/> |Einschränkungsart des Vorgangs ist ungültig.  <br/> |
|TaskNameInvalid = 7008  <br/> |Der Vorgangsname ist ungültig.  <br/> |
|TaskConstraintTypeRequiresConstraint = 7010  <br/> |Der Vorgang erfordert eine Einschränkungsart.  <br/> |
|TaskConstraintTypeCannotHaveConstraintDate = 7011  <br/> |Eine Termineinschränkung für den Typ der Einschränkung nicht möglich.  <br/> |
|TaskSummaryTaskCannotBeMilestone = 7013  <br/> |Der Sammelvorgang kann kein Meilenstein sein.  <br/> |
|TaskFixedCostAccrualInvalid = 7014  <br/> |Die Fälligkeit der festen Kosten für einen Vorgang ist ungültig.  <br/> |
|TaskPercentCompleteInvalid = 7015  <br/> |Der Prozentwert der Fertigstellung des Vorgangs ist ungültig.  <br/> |
|TaskWorkPercentCompleteInvalid = 7016  <br/> |Der Prozentwert der Fertigstellung der Vorgangsarbeit ist ungültig.  <br/> |
|TaskPhysicalPercentCompleteInvalid = 7017  <br/> |Der physischen Prozentwert der Fertigstellung des Vorgangs ist ungültig.  <br/> |
|TaskLinkTypeInvalid = 7018  <br/> |Der Verknüpfungstyp des Vorgangs ist ungültig.  <br/> |
|TaskAlreadyExists = 7019  <br/> |Der Vorgang ist bereits vorhanden.  <br/> |
|TaskLinkAlreadyExists = 7020  <br/> |Die Vorgangsverknüpfung ist bereits vorhanden.  <br/> |
|TaskNotFound = 7021  <br/> |Vorgang nicht gefunden.  <br/> |
|TaskLinkNotFound = 7022  <br/> |Vorgangsverknüpfung nicht gefunden.  <br/> |
|TaskLinkLagInvalid = 7023  <br/> |Die Zeitabstände für eine Vorgangsverknüpfung sind ungültig.  <br/> |
|TaskUnableToInsert = 7025  <br/> |Ein Vorgang kann nicht eingefügt werden  <br/> |
|TaskAddPositionInvalid = 7026  <br/> |Die Einfügeposition für einen Vorgang ist ungültig.  <br/> |
|TaskOutlineLevelInvalid = 7027  <br/> |Die Gliederungsebene des Vorgangs ist ungültig.  <br/> |
|TaskDurationFormatInvalid = 7028  <br/> |Das Dauerformat des Vorgangs ist ungültig.  <br/> |
|TaskCannotAddWhereSpecified = 7029  <br/> |Vorgang kann nicht an angegebener Position hinzugefügt werden.  <br/> |
|TaskEarnedValueMethodInvalid = 7030  <br/> |Die Methode für den Ertragswert des Vorgangs ist ungültig.  <br/> |
|TaskCannotModifyProjectSummary = 7031  <br/> |Projektsammelvorgang kann nicht geändert werden.  <br/> |
|TaskCannotDeleteProjectSummary = 7032  <br/> |Projektsammelvorgang kann nicht gelöscht werden.  <br/> |
|TaskCannotSetActualCost = 7033  <br/> |Istkosten für Vorgang können nicht festgelegt werden.  <br/> |
|TaskLevelingDelayInvalid = 7034  <br/> |Die Abgleichsverzögerung eines Vorgangs ist ungültig.  <br/> |
|TaskCannotEditSummary = 7035  <br/> |Sammelvorgang kann nicht bearbeitet werden.  <br/> |
|TaskCannotCreateSubTasksUnderTasksWithAssignments = 7036  <br/> |Teilvorgänge könne nicht unter einem Vorgang erstellt werden, der Zuordnungen hat.  <br/> |
|TaskCannotDeleteSubProject = 7037  <br/> |Teilprojekt für den Vorgang kann nicht gelöscht werden.  <br/> |
|TaskCannotEditExternal = 7038  <br/> |Externer Vorgang kann nicht bearbeitet werden.  <br/> |
|TaskCannotDeleteExternal = 7039  <br/> |Ein externer Vorgang kann nicht gelöscht werden.  <br/> |
|TaskLinkCannotDeleteExternal = 7040  <br/> |Ein Link zu einem externen Vorgang kann nicht gelöscht werden.  <br/> |
|TaskCannotModifyNullTask = 7041  <br/> |Ein Null-Vorgang kann nicht geändert werden.  <br/> |
|TaskCannotModifyLeafTaskWithNoAssignment = 7042  <br/> |Ein Blattvorgang, der keine Zuordnung hat, kann nicht geändert werden.  <br/> |
|TaskCannotModifyExternalTask = 7043  <br/> |Ein externer Vorgang kann nicht geändert werden.  <br/> |
|TaskStatusManagerInvalid = 7044  <br/> |Der Vorgangsstatus-Manager ist ungültig.  <br/> |
|TaskLinkCyclicDependency = 7045  <br/> |Die Vorgangsverknüpfung ist eine zyklische Abhängigkeit.  <br/> |
|TaskCannotCreateOrModifySubTasksUnderTasksWithAssignments = 7046  <br/> |Teilvorgänge unter einem Sammelvorgang mit Zuordnungen kann nicht erstellt oder geändert werden.  <br/> |
|TaskLinkCannotEditExternal = 7047  <br/> |Die Verknüpfung zu einem externen Vorgang kann nicht bearbeitet werden.  <br/> |

<a name="pj15_ErrorCodes_Timesheets"></a>

## <a name="table-28-timesheet"></a>Tabelle 28. Arbeitszeittabelle 

|Fehlercode - Arbeitszeittabelle|Beschreibung|
|:-----|:-----|
|TimesheetMaxHourPerDayExceeded = 3201  <br/> |Maximale Stunden pro Tag für Arbeitszeittabelle überschritten.  <br/> |
|TimesheetHoursPerTSLimitExceeded = 3202  <br/> |Der Grenzwert für die Anzahl Stunden in einer Arbeitszeittabelle wurde überschritten.  <br/> |
|TimesheetUnverifiedTSLineNotAllowed = 3203  <br/> |Eine nicht überprüfte Zeile der Arbeitszeittabelle ist in diesem Fall unzulässig.  <br/> |
|TimesheetIncorrectMode = 3204  <br/> |Der Modus der Arbeitszeittabelle ist ungültig.  <br/> |
|TimesheetInvalidApprover = 3205  <br/> |Die genehmigende Person der Arbeitszeittabelle ist ungültig.  <br/> |
|TimesheetFutureReportingNotAllowed = 3206  <br/> |Melden von zukünftigen Elemente für Arbeitszeittabelle ist unzulässig.  <br/> |
|TimesheetIncorrectPeriod = 3208  <br/> |Der Zeitraum in der Arbeitszeittabelle ist ungültig.  <br/> |
|TimesheetPeriodClosed = 3209  <br/> |Zeitraum in der Arbeitszeittabelle wurde geschlossen.  <br/> |
|TimesheetPendingLines = 3210  <br/> |Zeilen der Arbeitszeittabelle stehen aus.  <br/> |
|TimesheetInvalidDateRange = 3211  <br/> |Der Datumsbereich der Arbeitszeittabelle ist ungültig.  <br/> |
|TimesheetLineClassDisabled = 3212  <br/> |Die Klasse der Arbeitszeittabellenzeile ist deaktiviert.  <br/> |
|TimesheetLineHasNonExistentItem = 3213  <br/> |Die Zeile der Arbeitszeittabelle enthält ein Element, das nicht vorhanden ist.  <br/> |
|TimesheetLineInvalidStatus = 3214  <br/> |Der Status der Arbeitszeittabellenzeile ist ungültig.  <br/> |

<a name="pj15_ErrorCodes_UserDelegation"></a>

## <a name="table-29-user-delegation"></a>Tabelle 29. Benutzerdelegierung 

|Fehlercode - Benutzerdelegierung|Beschreibung|
|:-----|:-----|
|UserDelegationExpired = 43000  <br/> |Die Benutzerdelegierung ist abgelaufen.  <br/> |
|UserDelegationCannotSelfDelegate = 43001  <br/> |Ein Benutzer kann nicht auf sich selbst delegieren.  <br/> |
|UserDelegationInvalidDelegate = 43002  <br/> |Der Benutzerdelegat ist ungültig.  <br/> |
|UserDelegationInvalidUser = 43003  <br/> |Der Benutzer ist für eine Delegierung nicht gültig.  <br/> |
|UserDelegationInvalidDates = 43004  <br/> |Die Datumsabgaben der Benutzerdelegation sind ungültig.  <br/> |
|UserDelegationCannotDoubleDelegate = 43005  <br/> |Zwei Delegate können nicht erstellt werden.  <br/> |
|UserDelegationDelegateCannotLogon = 43006  <br/> |Der Benutzerdelegat kann sich nicht bei Project Server anmelden.  <br/> |
|UserDelegationDelegateIsInactive = 43007  <br/> |Der Benutzerdelegat ist inaktiv.  <br/> |
|UserDelegationInvalidFilter = 43008  <br/> |Der Benutzerdelegatfilter ist ungültig.  <br/> |
|UserDelegationUserCannotLogon = 43010  <br/> |Der Benutzer kann sich nicht bei Project Server anmelden.  <br/> |
|UserDelegationUserIsInactive = 43011  <br/> |Der Benutzerdelegat ist inaktiv.  <br/> |

<a name="pj15_ErrorCodes_Workflow"></a>

## <a name="table-30-workflow"></a>Tabelle 30. Workflow 

|Fehlercode - Workflow|Beschreibung|
|:-----|:-----|
|WorkflowPhasesCannotCreatePhase = 35000  <br/> |Die Workflowphase kann nicht erstellt werden.  <br/> |
|WorkflowPhasesCannotUpdatePhase = 35001  <br/> |Die Workflowphase konnte nicht aktualisiert werden.  <br/> |
|WorkflowPhasesCannotDeletePhase = 35002  <br/> |Die Workflowphase kann nicht gelöscht werden.  <br/> |
|WorkflowPhaseNameIsRequired = 35003  <br/> |Der Workflow [PHASE_NAME](https://msdn.microsoft.com/library/WebSvcWorkflow.WorkflowDataSet.WorkflowPhaseRow.PHASE_NAME.aspx) ist erforderlich.  <br/> |
|WorkflowStagesCannotCreateStage = 35004  <br/> |Die Workflowstufe kann nicht erstellt werden.  <br/> |
|WorkflowStagesCannotUpdateStage = 35005  <br/> |Die Workflowstufe kann nicht aktualisiert werden.  <br/> |
|WorkflowStagesCannotDeleteStage = 35006  <br/> |Die Workflowstufe kann nicht gelöscht werden.  <br/> |
|WorkflowStagesProjectsInStage = 35007  <br/> |Es sind Projekte in der Workflowstufe.  <br/> |
|WorkflowCannotAccessPDPLibrary = 35008  <br/> |Auf die Bibliothek der Projektdetailseiten kann nicht zugegriffen werden.  <br/> |
|WorkflowInvalidPDPUid = 35009  <br/> |Die GUID der Projektdetailseite ist ungültig.  <br/> |
|WorkflowInvalidCustomFieldUid = 35010  <br/> |Die GUID des benutzerdefinierten Felds ist ungültig.  <br/> |
|WorkflowCustomFieldNotWorkflowControlled = 35011  <br/> |Das benutzerdefinierte Feld wird nicht durch einen Workflow gesteuert.  <br/> |
|WorkflowCustomFieldCannotBeRequiredAndReadOnly = 35012  <br/> |Das benutzerdefinierte Workflowfeld kann nicht zugleich erforderlich und schreibgeschützt sein.  <br/> |
|WorkflowInvalidWorkflowPhaseUid = 35013  <br/> |Der Workflow [PHASE_UID](https://msdn.microsoft.com/library/WebSvcWorkflow.WorkflowDataSet.WorkflowPhaseRow.PHASE_UID.aspx) ist ungültig.  <br/> |
|WorkflowInsertWorkflowPhaseNotAllowed = 35014  <br/> |Eine Workflowphase kann nicht eingefügt werden.  <br/> |
|WorkflowInvalidWorkflowStageUid = 35015  <br/> |Der Workflow [STAGE_UID](https://msdn.microsoft.com/library/WebSvcWorkflow.WorkflowDataSet.WorkflowStageRow.STAGE_UID.aspx) ist ungültig.  <br/> |
|WorkflowPhaseHasStages = 35016  <br/> |Die Workflowphase hat Stufen.  <br/> |
|WorkflowStageNameIsRequired = 35020  <br/> |Der Workflow [STAGE_NAME](https://msdn.microsoft.com/library/WebSvcWorkflow.WorkflowDataSet.WorkflowStageRow.STAGE_NAME.aspx) ist erforderlich.  <br/> |
|WorkflowStageAtLeastOnePDPIsRequired = 35021  <br/> |Mindestens eine Projektdetailseite ist für die Workflowstufe erforderlich.  <br/> |
|WorkflowCannotStartWorkflow = 35100  <br/> |Der Workflow kann nicht gestartet werden.  <br/> |
|WorkflowStatusCannotUpdateStatus = 35101  <br/> |Der Workflowstatus konnte nicht aktualisiert werden.  <br/> |
|WorkflowOnlyProjectsHaveWorkflow = 35102  <br/> |Nur Projekte können ein Workflow enthalten.  <br/> |
|WorkflowNoWorkflowsDefined = 35103  <br/> |Es wurden keine Workflows definiert.  <br/> |
|WorkflowInvalidStageForProject = 35104  <br/> |Die Workflowstufe für das Projekt ist ungültig.  <br/> |
|WorkflowNoWorkflowForProject = 35105  <br/> |Das Projekt hat keinen Workflow.  <br/> |
|WorkflowCheckinRequiredAndProjectNotCheckedin = 35106  <br/> |Das Projekt muss eingecheckt sein, bevor der Workflow ausgeführt werden kann.  <br/> |
|WorkflowWaitingForRequiredData = 35107  <br/> |Der Workflow wartet auf die erforderlichen Daten.  <br/> |
|WorkflowFlagCustomFieldsCannotBeRequired = 35108  <br/> |Ein benutzerdefiniertes Flag-Feld darf in einem Workflow nicht erforderlich sein.  <br/> |
|WorkflowCannotChangeWorkflow = 35109  <br/> |Der Workflow kann nicht geändert werden.  <br/> |
|WorkflowWorkflowStatusPDPNotAllowed = 35110  <br/> |Eine Projektdetailseite für Workflowstatus ist nicht zulässig.  <br/> |
|WorkflowInvalidWorkflowStatusPDPUid = 35111  <br/> |Die GUID für die Projektdetailseite des Workflowstatus ist ungültig.  <br/> |
|WorkflowInvalidStageStatusValue = 35112  <br/> |Der Wert der der Workflowstufenstatus ist ungültig. Wenn Sie den Status der Projektstufe innerhalb des Workflows festlegen, werden nur die Werte **InProgressRequestSent**, **InProgressRunning**oder **InProgressWaiting** in [Workflow.StageStatus](https://msdn.microsoft.com/library/Microsoft.Office.Project.Server.Library.Workflow.StageStatus.aspx) zulässig.  <br/> |
|WorkflowCannotCheckinNotify = 35113  <br/> |Benachrichtigen des Workflows, dass das Projekt eingecheckt ist, nicht möglich.  <br/> |
|WorkflowCannotCommitNotify = 35114  <br/> |Benachrichtigen des Workflows, dass das Projekt in Planner oder Optimierer gespeichert ist, nicht möglich.  <br/> |
|WorkflowExceptionStartingWorkflow = 35115  <br/> |Fehler beim Starten des Workflows.  <br/> |
|WorkflowStatusPDPMustBeSupplied = 35116  <br/> |Eine Projektdetailseite ist für den Workflowstatus erforderlich.  <br/> |
|WorkflowWorkflowProxyAccountNotFound = 35117  <br/> |Das Proxykonto des Workflows wurde nicht gefunden.  <br/> |
|WorkflowInvalidCurrentStage = 35118  <br/> |Die aktuelle Stufe des Workflows ist ungültig.  <br/> |
|WorkflowMultipleStagesInProgress = 35119  <br/> |Es werden mehrere Stufen im Workflow verarbeitet.  <br/> |
|WorkflowActivityInvalidArgument = 35120  <br/> |Die Nachricht, die bei Empfang einer Workflowaktivität erhalten wird, ist ungültig.  <br/> |
|WorkflowMTWConfigurationError = 35121  <br/> |Microsoft Azure Workflow Konfigurationsfehler.  <br/> |
|EnterpriseProjectTypeInvalidEnterpriseProjectTypeUid = 35200  <br/> |**ENTERPRISE_PROJECT_TYPE_UID** ist ungültig.  <br/> |
|EnterpriseProjectTypeCannotCreateEnterpriseProjectType = 35201  <br/> |Enterprise-Projekttyp kann nicht erstellt werden.  <br/> |
|EnterpriseProjectTypeCannotUpdateEnterpriseProjectType = 35202  <br/> |Enterprise-Projekttyp kann nicht aktualisiert werden.  <br/> |
|EnterpriseProjectTypeCannotDeleteEnterpriseProjectType = 35203  <br/> |Enterprise-Projekttyp kann nicht gelöscht werden.  <br/> |
|EnterpriseProjectTypeCannotCreateMultipleEnterpriseProjectTypes = 35204  <br/> |Es können nicht mehrere Enterprise-Projekttypen erstellt werden.  <br/> |
|EnterpriseProjectTypeCannotUpdateMultipleEnterpriseProjectTypes = 35205  <br/> |Es können nicht mehrere Enterprise-Projekttypen aktualisiert werden.  <br/> |
|EnterpriseProjectTypeInvalidCreatePDPUid = 35206  <br/> |Eine Enterprise-Projektvorlage (EPT) erfordert eine zugeordnete Projektdetailseite (PDP) zum Erstellen eines Projekts mithilfe des EPT. Ist die EPT für einen Workflow, tritt dieser Fehler bei der Validierung annehmen, wenn die Projektdetailseite (PDP) nicht der *Create* -Typ ist. Andere PDP Typen werden *Normal* für ein Projekt und *Workflow-Status* für das Anzeigen von Details eines Projekts im Zusammenhang mit Workflow bearbeiten.  <br/> |
|EnterpriseProjectTypeInvalidProjectPlanTemplateUid = 35207  <br/> |Die [ENTERPRISE_PROJECT_PLAN_TEMPLATE_UID](https://msdn.microsoft.com/library/WebSvcWorkflow.WorkflowDataSet.EnterpriseProjectTypeRow.ENTERPRISE_PROJECT_PLAN_TEMPLATE_UID.aspx) ist ungültig.  <br/> |
|EnterpriseProjectTypeInvalidWorkspaceTemplateName = 35208  <br/> |Die [ENTERPRISE_PROJECT_WORKSPACE_TEMPLATE_NAME](https://msdn.microsoft.com/library/WebSvcWorkflow.WorkflowDataSet.EnterpriseProjectTypeRow.ENTERPRISE_PROJECT_WORKSPACE_TEMPLATE_NAME.aspx) ist ungültig.  <br/> |
|EnterpriseProjectTypeInvalidWorkflowAssociationUid = 35209  <br/> |Die [WORKFLOW_ASSOCIATION_UID](https://msdn.microsoft.com/library/WebSvcWorkflow.WorkflowDataSet.EnterpriseProjectTypeRow.WORKFLOW_ASSOCIATION_UID.aspx) ist ungültig.  <br/> |
|EnterpriseProjectTypeCannotReadWssSettings = 35210  <br/> |Die Einstellungen für SharePoint können nicht gelesen werden.  <br/> |
|EnterpriseProjectTypeCannotReadWssLanguagesAndTemplates = 35211  <br/> |Die SharePoint-Sprachen und Websitevorlagen können nicht gelesen werden.  <br/> |
|EnterpriseProjectTypeInvalidDepartmentUid = 35212  <br/> |Die [DEPARTMENT_UID](https://msdn.microsoft.com/library/WebSvcWorkflow.WorkflowDataSet.EnterpriseProjectTypeDepartmentsRow.DEPARTMENT_UID.aspx) ist ungültig.  <br/> |
|EnterpriseProjectTypeInvalidUri = 35213  <br/> |[ENTERPRISE_PROJECT_TYPE_UID](https://msdn.microsoft.com/library/WebSvcWorkflow.WorkflowDataSet.EnterpriseProjectTypeDepartmentsRow.ENTERPRISE_PROJECT_TYPE_UID.aspx) ist ungültig.  <br/> |
|EnterpriseProjectTypeUriRequiresHttp = 35214  <br/> |Die Enterprise-Projekttyp-URI erfordert das HTTP-Protokoll.  <br/> |
|EnterpriseProjectTypeCannotDeleteDefault = 35215  <br/> |Der standardmäßige Enterprise-Projekttyp kann nicht gelöscht werden.  <br/> |
|EnterpriseProjectTypeCannotChangeDefault = 35216  <br/> |Der standardmäßige Enterprise-Projekttyp kann nicht geändert werden.  <br/> |
|EnterpriseProjectTypeHasProjectsCannotDelete = 35217  <br/> |Ein Enterprise-Projekttyp, der Projekte enthält, kann nicht gelöscht werden.  <br/> |
|EnterpriseProjectTypeCreatePDPIsRequired = 35218  <br/> |Eine Enterprise-Projektvorlage (EPT) für einen Workflow erfordert eine zugeordnete *Erstellen* Typ Projektdetailseite (PDP) zum Erstellen eines Projekts mithilfe des EPT. Dieser Fehler tritt auf, wenn die PDP nicht in die EPT-Definition enthalten ist. Andere PDP Typen werden *Normal* für ein Projekt und *Workflow-Status* für das Anzeigen von Details eines Projekts im Zusammenhang mit Workflow bearbeiten.  <br/> |
|EnterpriseProjectTypeOnlyOneCreatePDPAllowed = 35219  <br/> |Die EPT-Definition lässt nur einen Typ *Create* -Projektdetailseite.  <br/> |
|EnterpriseProjectTypeHasWorkflowOnlyCreatePDPAllowed = 35220  <br/> |Eine Enterprise-Projektvorlage (EPT) für einen Workflow erfordert eine zugeordnete *Erstellen* Typ Projektdetailseite (PDP) zum Erstellen eines Projekts mithilfe des EPT. Dieser Fehler tritt auf, wenn die PDP im Workflow EPT-Definition eines anderen Typs ist. Andere PDP Typen werden *Normal* für ein Projekt und *Workflow-Status* für das Anzeigen von Details eines Projekts im Zusammenhang mit Workflow bearbeiten.  <br/> |
|EnterpriseProjectTypeInvalidData = 35221  <br/> |Das **WorkflowDataSet** für den Enterprise-Projekttyp hat ungültige Daten.  <br/> |
|EnterpriseProjectNoDefaultEnterpriseProjectTypeDefined = 35222  <br/> |Es ist kein standardmäßiger Enterprise-Projekttyp definiert  <br/> |
|EnterpriseProjectTypeAtLeastOnePDPIsRequired = 35223  <br/> |Mindestens eine Projektdetailseite ist für den Enterprise-Projekttyp erforderlich.  <br/> |
|EnterpriseProjectTypeWorkflowStatusPDPNotAllowed = 35224  <br/> |Eine Projektdetailseite für den Workflowstatus ist nicht zulässig für den Enterprise-Projekttyp.  <br/> |
|EnterpriseProjectTypeCannotChangeWorkflowAssociation = 35225  <br/> |Das Projekt enthält bereits einen Enterprise-Projekttyp (EPT); die EPT für das Projekt kann nicht geändert werden.  <br/> |

<a name="pj15_ErrorCodes_WSS"></a>

## <a name="table-31-wssinterop-and-objectlinkprovider-sharepoint-integration"></a>Tabelle 31. WssInterop und ObjectLinkProvider (SharePoint-Integration)

|Fehlercode - SharePoint-Integration|Beschreibung|
|:-----|:-----|
|WSSCreateSiteFailure = 16400  <br/> |Fehler beim Erstellen der SharePoint-Website für den Projektarbeitsbereich.  <br/> |
|WSSCannotCreateWebWithBlankName = 16401  <br/> |SharePoint-Website kann nicht mit leerem Namen erstellt werden.  <br/> |
|WSSWebAlreadyExists = 16402  <br/> |Die SharePoint-Website ist bereits vorhanden.  <br/> |
|WSSInvalidProjectUID = 16403  <br/> |Die Projekt-GUID ist nicht gültig für den SharePoint-Projektarbeitsbereich.  <br/> |
|WSSProjectAlreadyHasSpWeb = 16404  <br/> |Das Projekt enthält bereits eine SharePoint Workspace-Website  <br/> |
|WSSWebDoesNotExist = 16405  <br/> |Die SharePoint-Website ist nicht vorhanden.  <br/> |
|WSSSpWebAlreadyLinkedToProject = 16406  <br/> |Die SharePoint-Website ist bereits mit einem Projekt verknüpft.  <br/> |
|WSSWebHierarchyDoesNotExist = 16407  <br/> |Die SharePoint-Hierarchie ist nicht vorhanden.  <br/> |
|WSSSPWebHasChildren = 16408  <br/> |Die SharePoint-Webanwendung verfügt über untergeordneten Webanwendungen.  <br/> |
|WSSURIInvalidFormat = 16409  <br/> |Das Format für eine SharePoint-Webanwendung-URI ist ungültig.  <br/> |
|WSSSyncReportingDataFailed = 16410  <br/> |Fehler beim Synchronisieren der Berichtsdaten für SharePoint.  <br/> |
|WSSWorkspaceUrlPathTooLong = 16411  <br/> |URL-Pfad des SharePoint-Projektarbeitsbereichs ist zu lang.  <br/> |
|WSSWorkspaceNameContainsIllegalChars = 16412  <br/> |Ein oder mehrere Zeichen in einer SharePoint-Website Projektname ist ungültig. Die folgenden Zeichen sind nicht gültig in einen Projektnamen: / ": \<\> | , . ' ? \* #  <br/> |
|WSSInvalidWssServerUid = 16413  <br/> |Die SharePoint Server-GUID ist ungültig.  <br/> |
|WSSSyncUsersFailed = 16414  <br/> |Project Server-Benutzer konnten nicht mit SharePoint synchronisiert werden.  <br/> |
|WSSWrongWebTemplateLCID = 16415  <br/> |Die Gebietsschema-ID der SharePoint-Webvorlage (Sprachen-ID) ist ungültig.  <br/> |
|WSSWrongWebTemplate = 16416  <br/> |Die SharePoint-Webvorlage ist ungültig.  <br/> |
|WSSWebIsNotProjectWorkspace = 16417  <br/> |Die SharePoint-Website ist kein Projektarbeitsbereich.  <br/> |
|WSSWebCannotStartOrEndOnPeriod = 16418  <br/> |Ein SharePoint-Webname darf nicht mit einem Punkt beginnen oder enden.  <br/> |
|WSSCannotDeleteSiteCollection = 16419  <br/> |Die Websitesammlung kann nicht gelöscht werden.  <br/> |
|WSSListUidInvalid = 16420  <br/> |SharePoint-Listen-GUID ist ungültig.  <br/> |
|WSSSyncDataSetListUidMismatch = 16421  <br/> |Die SharePoint-Listen-GUID stimmt nicht mit der Listen-GUID überein bei der Synchronisierung von **DataSet**.  <br/> |
|WSSSyncDataSetMissingProjectSettingsRow = 16422  <br/> |**DataSet** für eine Synchronisierung mit SharePoint hat keine Projekteinstellungszeilen.  <br/> |
|WSSSyncDataSetTaskMappingsNotAllowed = 16423  <br/> |Vorgangsschemata sind in **DataSet** nicht zulässig für eine Synchronisierung mit SharePoint.  <br/> |
|WSSSyncDataSetWssListUidEmpty = 16424  <br/> |Die SharePoint-Listen-GUID ist in **DataSet** leer für eine Synchronisierung mit SharePoint.  <br/> |
|WSSSyncDataNotFound = 16425  <br/> |Es fehlen Daten bei der Synchronisierung mit SharePoint.  <br/> |
|WSSSyncCriticalDataValidationError = 16426  <br/> |Es gibt einen kritischen Datenvalidierungsfehler bei der Synchronisierung mit SharePoint.  <br/> |
|WSSSyncSharePointListNotAccessibleError = 16427  <br/> |Auf die SharePoint-Liste kann nicht zugegriffen werden.  <br/> |
|WSSSyncInvalidEntityUids = 16428  <br/> |Die Entitäts-GUIDs sind nicht gültig für die Synchronisierung mit SharePoint.  <br/> |
|WSSSyncInvalidSyncData = 16429  <br/> |SharePoint-Synchronisierung enthält ungültige Daten.  <br/> |
|WSSSyncSPSummaryTaskAssignedToResourceError = 16430  <br/> |Die SharePoint-Synchronisierung enthält einen Sammelvorgang, der eine Ressource zugewiesen ist.  <br/> |
|WSSSyncInsufficientPermissionsToCreateWinUser = 16431  <br/> |Die Berechtigungen sind nicht ausreichend, um einen Windows-Benutzer bei der Synchronisierung mit SharePoint zu erstellen.  <br/> |
|WSSSyncNoDefaultValueForCustomField = 16432  <br/> |Ein benutzerdefiniertes Feld hat keinen Standardwert bei der SharePoint-Synchronisierung.  <br/> |
|WSSOLPCreateLinkFailure = 18000  <br/> |Fehler beim Erstellen der Verknüpfung für den SharePoint-Objekt Link Provider.  <br/> |
|WSSOLPDeleteWebObjectLinkError = 18001  <br/> |Fehler beim Löschen einer Webobjektverknüpfung im SharePoint-Objekt Link Provider.  <br/> |
|WSSInvalidPermissionsToWssList = 18002  <br/> |Berechtigungen gelten nicht für die SharePoint-Liste.  <br/> |
|WSSWebIsNotUnderDefaultCollection = 18003  <br/> |Die SharePoint-Webanwendung ist nicht in der Standardsammlung.  <br/> |
|WSSWorkspaceUrlIsNotUnderPrimaryCollection = 18004  <br/> |Der angegebene Arbeitsbereich ist die Url nicht in der Websitesammlung, die diese Instanz von Projektserver zugeordnet. Dies ist der aktuellen Berechtigungsmodus erforderlich.  <br/> |
|WSSWorkspacesMustBeRestrictedToDefaultCollection = 18005  <br/> |Workspaces müssen im aktuellen Berechtigungsmodus auf die Standardwebsitesammlung beschränkt werden.  <br/> |

<a name="pj15_ErrorCodes_ASMXExample"> </a>

## <a name="error-code-example-for-asmx"></a>Fehlercodebeispiel für ASMX

Um eine Liste der Fehler erhalten, wenn eine Ausnahme ausgelöst, wenn Sie eine PSI-Methode aufrufen möchten, übergeben Sie das **SoapException** -Objekt an den Klassenkonstruktor [Microsoft.Office.Project.Server.Library.PSClientError](https://msdn.microsoft.com/library/Microsoft.Office.Project.Server.Library.PSClientError.aspx) . Sie können dann [GetAllErrors](https://msdn.microsoft.com/library/Microsoft.Office.Project.Server.Library.PSClientError.GetAllErrors.aspx) verwenden, speichern die Fehlerinformationen in einem Array **PSErrorInfo** und Auflisten der Fehler, wie im folgenden Beispiel. 
  
> [!NOTE]
> Das **PSErrorInfo** -Objekt schließt nicht alle Informationen ein, die möglicherweise erforderlich. Wenn Sie **Resource.CheckOutResources** verwenden, in denen eine der Ressourcen bereits ausgecheckt ist, wird beispielsweise **PSErrorInfo** für jede Ressource, die nicht ausgecheckt werden, aber enthält keinen der Ressourcenname oder die GUID der Fehlerursache. Eine Möglichkeit zum Abrufen von Informationen in eine ASMX-basierte Anwendung finden Sie unter [CheckOutResources](https://msdn.microsoft.com/library/WebSvcResource.Resource.CheckOutResources.aspx) . 
  
```cs
using System;
using System.Collections.Generic;
using System.Text;
using System.Web.Services.Protocols;
using System.Windows.Forms;
using PSLibrary = Microsoft.Office.Project.Server.Library;
. . .
try
{
    /* Call a PSI method. */
}
catch (SoapException ex)
{
    string errAttributeName;
    string errAttribute;
    string errMess = "".PadRight(30, '=') + "\r\n" + "Error: " + "\r\n";
    PSLibrary.PSClientError error = new PSLibrary.PSClientError(ex);
    PSLibrary.PSErrorInfo[] errors = error.GetAllErrors();
    PSLibrary.PSErrorInfo thisError;
    for (int i = 0; i < errors.Length; i++)
    {
        thisError = errors[i];
        errMess += "\n" + ex.Message.ToString() + "\r\n";
        errMess += "".PadRight(30, '=') + "\r\nPSCLientError Output:\r\n \r\n";
        errMess += thisError.ErrId.ToString() + "\n";
        for (int j = 0; j < thisError.ErrorAttributes.Length; j++)
        {
            errAttributeName = thisError.ErrorAttributeNames()[j];
            errAttribute = thisError.ErrorAttributes[j];
            errMess += "\r\n\t" + errAttributeName +
                       ": " + errAttribute;
        }
        errMess += "\r\n".PadRight(30, '=');
    }
    MessageBox.Show(errMess, "Error", MessageBoxButtons.OK,
        MessageBoxIcon.Error);
}
```

<a name="pj15_ErrorCodes_WCFExample"> </a>

## <a name="error-code-example-for-wcf"></a>Fehlercodebeispiel für WCF

Um erhalten eine Liste der Fehler, wenn Sie beim Aufruf einer PSI-Methode in einer WCF-basierte Anwendung ein **System.ServiceModel.FaultException** erhalten, können Sie ein **PSClientError** -Objekt aus dem Objekt **FaultException** extrahieren. Sie können dann [GetAllErrors](https://msdn.microsoft.com/library/Microsoft.Office.Project.Server.Library.PSClientError.GetAllErrors.aspx) verwenden, die Fehlerinformationen in einem Array **PSErrorInfo** gespeichert und Auflisten der Fehler, wie im vorherigen Beispiel ASMX. 
  
```cs
using System;
using System.Text;
using System.ServiceModel;
using System.Xml;
using PSLibrary = Microsoft.Office.Project.Server.Library;
. . .
try
{
    /* Call a PSI method. */
}
catch(FaultException fault)
{
    // Use the WCF FaultException, because the ASMX SoapException does not 
    // exist in a WCF-based application.
    WriteFaultOutput(fault);
}
// Get a PSClientError object from the WCF FaultException object, and
// then display the exception details and each error in the PSClientError stack.
private static void WriteFaultOutput(FaultException fault)
{
    string errAttributeName;
    string errAttribute;
    string errOut;
    string errMess = "".PadRight(30, '=') + "\r\n"
        + "Error details: " + "\r\n";
    PSLibrary.PSClientError error = GetPSClientError(fault, out errOut);
    errMess += errOut;
    PSLibrary.PSErrorInfo[] errors = error.GetAllErrors();
    PSLibrary.PSErrorInfo thisError;
    for (int i = 0; i < errors.Length; i++)
    {
        thisError = errors[i];
        errMess += "\r\n".PadRight(30, '=') + "\r\nPSClientError output:\r\n";
        errMess += thisError.ErrId.ToString() + "\n";
        for (int j = 0; j < thisError.ErrorAttributes.Length; j++)
        {
            errAttributeName = thisError.ErrorAttributeNames()[j];
            errAttribute = thisError.ErrorAttributes[j];
            errMess += "\r\n\t" + errAttributeName
                + ": " + errAttribute;
        }
    }
    Console.ForegroundColor = ConsoleColor.Red;
    Console.WriteLine(errMess);
    Console.ResetColor();
}
/// <summary>
/// Extract a PSClientError object from the ServiceModel.FaultException,
/// for use in output of the GetPSClientError stack of errors.
/// </summary>
/// <param name="e"></param>
/// <param name="errOut">Shows that FaultException has more information 
/// about the errors than PSClientError has. FaultException can also contain 
/// other types of errors, such as failure to connect to the server.</param>
/// <returns>PSClientError object, for enumerating errors.</returns>
public static PSLibrary.PSClientError GetPSClientError(FaultException e, 
                                                        out string errOut)
{
    const string PREFIX = "GetPSClientError() returns null: ";
    errOut = string.Empty;
    PSLibrary.PSClientError psClientError = null;
    if (e == null)
    {
        errOut = PREFIX + "Null parameter (FaultException e) passed in.";
        psClientError = null;
    }
    else
    {
        // Get a ServiceModel.MessageFault object.
        var messageFault = e.CreateMessageFault();
        if (messageFault.HasDetail)
        {
            using (var xmlReader = messageFault.GetReaderAtDetailContents())
            {
                var xml = new XmlDocument();
                xml.Load(xmlReader);
                var serverExecutionFault = xml["ServerExecutionFault"];
                if (serverExecutionFault != null)
                {
                    var exceptionDetails = serverExecutionFault["ExceptionDetails"];
                    if (exceptionDetails != null)
                    {
                        try
                        {
                            errOut = exceptionDetails.InnerXml + "\r\n";
                            psClientError = 
                                new PSLibrary.PSClientError(exceptionDetails.InnerXml);
                        }
                        catch (InvalidOperationException ex)
                        {
                            errOut = PREFIX + "Unable to convert fault exception info ";
                            errOut += "a valid Project Server error message. Message: \n\t";
                            errOut += ex.Message;
                            psClientError = null;
                        }
                    }
                    else
                    {
                        errOut = PREFIX + "The FaultException e is a ServerExecutionFault, "
                            + "but does not have ExceptionDetails.";
                    }
                }
                else
                {
                    errOut = PREFIX + "The FaultException e is not a ServerExecutionFault.";
                }
            }
        }
        else // No detail in the MessageFault.
        {
            errOut = PREFIX + "The FaultException e does not have any detail.";
        }
    }
    errOut += "\r\n" + e.ToString() + "\r\n";
    return psClientError;
}

```

<br/>

Zusätzlich zu den Daten im **PSClientError** -Objekt kann das Objekt **FaultException** anderen Arten von Fehlern, beispielsweise Fehler beim Verbinden mit Project Server enthalten. Der Parameter _ErrOut_ der **GetPSClientError** -Methode im vorherigen Beispiel zeigt zusätzliche Informationen an. Beispielsweise enthält das **CreateProject4Department** -Codebeispiel in der [QueueCreateProject](https://msdn.microsoft.com/library/WebSvcProject.Project.QueueCreateProject.aspx) -Methode Kommentare, die zeigen, wie Fehler beim Festlegen von Eigenschaften in der Tabelle **ProjectCustomFields** erstellen. Wenn die Anwendung ausgeführt wird, enthält der Parameter _ErrOut_ **Errinfo** -Element und andere Daten (hier aus der Konsolenausgabe formatiert). 
  
```XML
==============================
Error details:
<errinfo xmlns="">
  <dataset name="ProjectDataSet">
    <table name="ProjectCustomFields">
      <row CUSTOM_FIELD_UID="976d3bd9-95ff-40a2-a938-960c410b0341">
        <error id="11704" name="CustomFieldInvalidTypeColumnFilledIn" 
               uid="aa8a2fab-9262-422f-b022-ca1cb12bc75f"></error>
        <error id="11713" name="CustomFieldRequiredValueNotProvided" 
               uid="dc2e2156-86e9-4aac-bede-d07dc44dfedc"></error>
      </row>
    </table>
  </dataset>
</errinfo>
System.ServiceModel.FaultException`1[SvcProject.ServerExecutionFault]: 
ProjectServerError(s) LastError=CustomFieldRequiredValueNotProvided Instructions: 
Pass this into PSClientError constructor to access all error information 
(Fault Detail is equal to SvcProject.ServerExecutionFault).
============================
PSClientError output:
CustomFieldInvalidTypeColumnFilledIn
============================
PSClientError output:
CustomFieldRequiredValueNotProvided
```

<a name="pj15_ErrorCodes_AR"> </a>

## <a name="see-also"></a>Siehe auch

- [Projekt Konzept- und Anleitungsthemen Artikel](project-conceptual-and-how-to-articles.md)
- [SQL Server Profiler](https://msdn.microsoft.com/library/3ad5f33d-559e-41a4-bde6-bb98792f7f1a.aspx)
- [Project Server 2010: Was Sie erwartet, wenn Sie die unerwarteten abrufen](https://blogs.msdn.com/b/brismith/archive/2010/03/24/project-server-2010-what-to-expect-when-you-get-the-unexpected.aspx)
- [ULS Viewer](https://www.codeproject.com/Articles/458052/ULS-Log-Viewer)
    

