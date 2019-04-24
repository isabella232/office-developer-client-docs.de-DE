---
title: HrCreateApptRebaser
manager: soliver
ms.date: 12/07/2015
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: 265028b7-a583-f6ba-0214-5a4322f98f35
description: Initialisiert ein IOlkApptRebaser-Objekt für die Verwendung beim erneuten Aufsetzen von Terminen in Outlook-Kalendern.
ms.openlocfilehash: 33ad47d59ee2ca1b2461f730494f3466b9f8b54a
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32317612"
---
# <a name="hrcreateapptrebaser"></a>HrCreateApptRebaser

Initialisiert ein [IOlkApptRebaser](iolkapptrebaser.md) -Objekt für die Verwendung beim erneuten Aufsetzen von Terminen in Outlook-Kalendern. 
  
## <a name="quick-info"></a>QuickInfo

|||
|:-----|:-----|
|Headerdatei  <br/> |tzmovelib. h  <br/> |
|Implementiert von:  <br/> |tzmovelib. dll  <br/> |
|Aufgerufen von:  <br/> |MAPI-Clientanwendungen  <br/> |
|Zeigertyp:  <br/> |**LPHRCREATEAPPTREBASER** <br/> |
|DLL-Einstiegspunkt:  <br/> |**HrCreateApptRebaser @ 44** <br/> |
   
```cpp
HRESULT HrCreateApptRebaser(  
    ULONG ulFlags, 
    IMAPISession *pSession, 
    IMsgStore *pCalendarMsgStore, 
    IMAPIFolder *pCalendarFolder, 
    LPCWSTR pwszUpdatePrefix, 
    const FILETIME *pftInstallDateUTC, 
    LONG lExpansionDepth, 
    const TZDEFINITION *pTZTo, 
    const TZDEFINITION *pTZMissing, 
    MAPIERROR **ppError, 
    IOlkApptRebaser **ppApptRebase); 

```

## <a name="parameters"></a>Parameter

_ulFlags_
  
> [in] Erforderlich. Eine Bitmaske von Flags, die verwendet werden, um zu steuern, wie die rebasis ausgeführt wird. Die folgenden Flags können festgelegt und in tzmovelib. h definiert werden:
    
   - **REBASE_FLAG_UPDATE_ORGANIZED_MEETINGS** – Termin Elemente, in denen der Benutzer der Besprechungsorganisator ist, werden erneut basiert. Beachten Sie, dass Outlook standardmäßig Besprechungsaktualisierungen an alle Teilnehmer einer Besprechung sendet, die erneut basiert. Sie können dieses Flag entweder mit **REBASE_FLAG_FORCE_NO_EX_UPDATES** oder mit **REBASE_FLAG_FORCE_NO_UPDATES** kombinieren, um die Behandlung von Besprechungs Updates zu ändern. 
    
   - **REBASE_FLAG_UPDATE_UNMARKED** -aktualisiert Termin Elemente, die nicht mit einer Zeitzone gekennzeichnet wurden. Wenn dieses Flag angegeben wird, wird der *pTZMissing* -Wert als Zeitzone verwendet, in der ein Element für alle Elemente erstellt wird, die nicht über Zeitzonendaten verfügen. 
    
   - **REBASE_FLAG_UPDATE_ONLYRECURRING** – aktualisieren Sie nur wiederkehrende Termin Elemente. 
    
   - **REBASE_FLAG_NO_UI** – zeigt keine Benutzeroberfläche an, einschließlich Anmeldedialogfelder, die beim Öffnen eines Nachrichtenspeichers Allgemein angezeigt werden. 
    
   - **REBASE_FLAG_UPDATE_MINIMIZEAPPTS** -belegen Sie Termin Elemente, die in der Vergangenheit auftreten, nicht erneut. 
    
   - **REBASE_FLAG_FORCE_REBASE** – überprüfen Sie nicht den Organisator auf die Entscheidungsfindung, sondern setzen Sie Termin Elemente erneut um, in denen der Benutzer ein Teilnehmer ist. 
    
   - **REBASE_FLAG_FORCE_NO_EX_UPDATES** -sendet nur dann Updates, wenn der Benutzer Organisator ist und der Empfänger nicht mit einem Exchange-Server verbunden ist. 
    
   - **REBASE_FLAG_FORCE_NO_UPDATES** – nie Updates senden. 
    
   - **REBASE_FLAG_ONLY_CREATED_PRE_PATCH** – rebasen Sie nur Einzelinstanz-Termin Elemente, die vor dem Anwenden des Patches erstellt wurden. 
    
   - **REBASE_FLAG_REPORTING_MODE** -nicht tatsächlich rebase, sondern nur Berichtstermin Elemente, die rebasiert werden würden. 
    
   - **REBASE_FLAG_SEND_RESOURCE_UPDATES** -sendet Besprechungsaktualisierungen an Ressourcen. 
    
_pSession_
  
> [in] Erforderlich. Ein Zeiger auf eine MAPI-Sitzungs Schnittstelle.
    
_pCalendarMsgStore_
  
> [in] Erforderlich. Ein Zeiger auf einen Nachrichtenspeicher mit Terminelementen, die erneut basiert werden sollen.
    
_pCalendarFolder_
  
> [in] Erforderlich. Ein Zeiger auf einen Kalenderordner mit Terminelementen, die erneut basiert werden sollen.
    
_pwszUpdatePrefix_
  
> [in] Optional. Ein Zeiger auf eine Zeichenfolge mit dem Präfix, das in Besprechungsanfragen vorangestellt werden soll. Kann NULL sein.
    
_pftInstallDateUTC_
  
> [in] Optional. Das Installationsdatum für das Zeit Zonen Patch. Wird nur verwendet, wenn das **REBASE_FLAG_ONLY_CREATED_PRE_PATCH** -Flag festgelegt ist. 
    
_IExpansionDepth_
  
> [in] Optional. Die Expansions Tiefe beim Erweitern von Verteilerlisten zum Ausschließen von Empfängern, die mit Exchange Server verbunden sind. Wird nur verwendet, wenn das **REBASE_FLAG_FORCE_NO_EX_UPDATES** -Flag festgelegt ist. 
    
_pTZTo_
  
> [in] Erforderlich. Ein Zeiger auf eine **TZDEFINITION** -Struktur, die die Zeitzone beschreibt, auf die eine neubasis erfolgen soll. **TZDEFINITION** ist in tzmovelib definiert. 
    
pTZMissing
  
> [in] Erforderlich. Ein Zeiger auf eine **TZDEFINITION** -Struktur, die die Zeitzone beschreibt, die angenommen werden soll, wenn Zeitzoneninformationen nicht für ein Element gestempelt werden. Darf nicht NULL sein, sondern nur verwendet werden, wenn das **REBASE_FLAG_UPDATE_UNMARKED** -Flag festgelegt ist. 
    
_ppError_
  
> Out Ein Zeiger auf einen Zeiger auf eine **MAPIERROR** -Struktur, die Versions-, Komponenten-und Kontextinformationen für den Fehler enthält. Kann NULL sein, wenn keine erweiterten Fehlerinformationen erwünscht sind. Kostenlos mit [mapifreebufferfreigegeben](https://msdn.microsoft.com/library/9412594f-8acc-4c7e-a668-4ec1da0ad9cf%28Office.15%29.aspx). 
    
_ppApptRebase_
  
> Out Ein Zeiger auf einen Zeiger auf die zurückgegebene **IOlkApptRebaser** -Schnittstelle. 
    
## <a name="return-values"></a>Rückgabewerte

S_OK zurück, wenn der Aufruf erfolgreich war; andernfalls einen Fehlercode.
  
## <a name="remarks"></a>Bemerkungen

Wenn Sie [GetProcAddress](https://msdn.microsoft.com/library/a0d7fc09-f888-4f46-a571-d3719a627597%28Office.15%29.aspx) verwenden, um nach der Adresse dieser Funktion in tzmovelib. dll zu suchen, geben Sie **HrCreateApptRebaser @ 44** als Prozedurnamen an. Nicht alle Flags sind in Kombination mit einander gültig. 
  
Weitere Informationen zu den verschiedenen Optionen finden Sie im Abschnitt "Glossar der Befehlszeilenoptionen für das Outlook Time Zone Data Update Tool" in [KB 931667: wie Sie Zeitzonenänderungen mithilfe des Time Zone Data Update Tool für Microsoft Office Outlook behandeln](https://support.microsoft.com/kb/931667/en-us).
  
## <a name="see-also"></a>Siehe auch

- [Zum neuen Basisadressen Kalender programmgesteuert Sommerzeit](about-rebasing-calendars-programmatically-for-daylight-saving-time.md)

