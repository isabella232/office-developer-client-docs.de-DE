---
title: HrCreateApptRebaser
manager: soliver
ms.date: 12/07/2015
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: 265028b7-a583-f6ba-0214-5a4322f98f35
description: Initialisiert ein IOlkApptRebaser-Objekt zur Verwendung beim Neubasieren von Terminen in Outlook Kalendern.
ms.openlocfilehash: 33ad47d59ee2ca1b2461f730494f3466b9f8b54a
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32317612"
---
# <a name="hrcreateapptrebaser"></a>HrCreateApptRebaser

Initialisiert ein [IOlkApptRebaser-Objekt](iolkapptrebaser.md) zur Verwendung beim Neubasieren von Terminen in Outlook Kalendern. 
  
## <a name="quick-info"></a>QuickInfo

|||
|:-----|:-----|
|Headerdatei  <br/> |tzmovelib.h  <br/> |
|Implementiert von:  <br/> |tzmovelib.dll  <br/> |
|Aufgerufen von:  <br/> |MAPI-Clientanwendungen  <br/> |
|Zeigertyp:  <br/> |**LPHRCREATEAPPTREBASER** <br/> |
|DLL-Einstiegspunkt:  <br/> |**HrCreateApptRebaser@44** <br/> |
   
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
  
> [in] Erforderlich. Eine Bitmaske mit Flags, die zum Steuern der Neubasierung verwendet wird. Die folgenden Flags können festgelegt werden und sind in tzmovelib.h definiert:
    
   - **REBASE_FLAG_UPDATE_ORGANIZED_MEETINGS** – Terminelemente, bei denen der Benutzer der Besprechungsorganisator ist, werden neu basisiert. Beachten Sie, dass dies standardmäßig dazu führt, Outlook Besprechungsupdates an alle Teilnehmer einer besprechungsbasierten Besprechung senden. Sie können dieses Flag mit REBASE_FLAG_FORCE_NO_EX_UPDATES **oder** REBASE_FLAG_FORCE_NO_UPDATES, um die Art und **Weise** zu ändern, wie Besprechungsupdates behandelt werden. 
    
   - **REBASE_FLAG_UPDATE_UNMARKED** –Terminelemente aktualisieren, die nicht mit einer Zeitzone markiert wurden. Wenn dieses Flag angegeben wird, wird der  *pTZMissing-Wert*  als Zeitzone verwendet, in der ein Element für alle Elemente erstellt wird, die keine Zeitzonendaten enthalten. 
    
   - **REBASE_FLAG_UPDATE_ONLYRECURRING** – Nur Terminserienelemente aktualisieren. 
    
   - **REBASE_FLAG_NO_UI** – Keine Benutzeroberfläche anzeigen, einschließlich Anmeldedialogfeldern, die beim Öffnen eines Nachrichtenspeichers in der Regel angezeigt werden. 
    
   - **REBASE_FLAG_UPDATE_MINIMIZEAPPTS** – In der Vergangenheit vorkommende Terminelemente dürfen nicht neu basierten werden. 
    
   - **REBASE_FLAG_FORCE_REBASE** – Überprüfen Sie den Organisator nicht auf die Neubasierung von Entscheidungen, sondern erstellen Sie terminbezogene Elemente, bei denen der Benutzer ein Teilnehmer ist, neu. 
    
   - **REBASE_FLAG_FORCE_NO_EX_UPDATES** – Aktualisierungen nur senden, wenn der Benutzer der Organisator ist und der Empfänger nicht mit einer Exchange Server. 
    
   - **REBASE_FLAG_FORCE_NO_UPDATES** – Niemals Updates senden. 
    
   - **REBASE_FLAG_ONLY_CREATED_PRE_PATCH** – Basierten Sie nur Terminelemente mit einer Instanz neu, die vor dem Anwenden des Patches erstellt wurden. 
    
   - **REBASE_FLAG_REPORTING_MODE** – Erstellen Sie keine rebase, sondern melden Sie lediglich Terminelemente, die neubasiert würden. 
    
   - **REBASE_FLAG_SEND_RESOURCE_UPDATES** – Senden von Besprechungsupdates an Ressourcen. 
    
_pSession_
  
> [in] Erforderlich. Ein Zeiger auf eine MAPI-Sitzungsschnittstelle.
    
_pCalendarMsgStore_
  
> [in] Erforderlich. Ein Zeiger auf einen Nachrichtenspeicher, der neu zu erstellende Terminelemente enthält.
    
_pCalendarFolder_
  
> [in] Erforderlich. Ein Zeiger auf einen Kalenderordner, der neu zu erstellende Terminelemente enthält.
    
_pwszUpdatePrefix_
  
> [in] Optional. Ein Zeiger auf eine Zeichenfolge, die das Präfix enthält, das für Besprechungsanfragen vorangestellt werden soll. Kann NULL sein.
    
_pftInstallDateUTC_
  
> [in] Optional. Das Installationsdatum des Zeitzonenpatches. Wird nur verwendet, **wenn REBASE_FLAG_ONLY_CREATED_PRE_PATCH** festgelegt ist. 
    
_IExpansionDepth_
  
> [in] Optional. Die Erweiterungstiefe beim Erweitern von Verteilerlisten, um Empfänger auszuschließen, die mit Exchange Server. Wird nur verwendet, **wenn REBASE_FLAG_FORCE_NO_EX_UPDATES** festgelegt ist. 
    
_pTZTo_
  
> [in] Erforderlich. Ein Zeiger auf eine **TZDEFINITION-Struktur,** in der die Zeitzone beschrieben wird, in der eine erneute Datenbank verwendet werden soll. **TZDEFINITION** ist in tzmovelib definiert. 
    
pTZMissing
  
> [in] Erforderlich. Ein Zeiger auf eine **TZDEFINITION-Struktur,** die die anzunehmende Zeitzone beschreibt, wenn Zeitzoneninformationen nicht für ein Element gestempelt werden. Darf nicht NULL sein, sondern nur verwendet werden, wenn **das REBASE_FLAG_UPDATE_UNMARKED** festgelegt ist. 
    
_ppError_
  
> [out] Ein Zeiger auf einen Zeiger auf eine **MAPIERROR-Struktur,** die Versions-, Komponenten- und Kontextinformationen für den Fehler enthält. Kann NULL sein, wenn keine erweiterten Fehlerinformationen gewünscht werden. Kostenlos mit [MAPIFreeBuffer](https://msdn.microsoft.com/library/9412594f-8acc-4c7e-a668-4ec1da0ad9cf%28Office.15%29.aspx). 
    
_ppApptRebase_
  
> [out] Ein Zeiger auf einen Zeiger auf die **zurückgegebene IOlkApptRebaser-Schnittstelle.** 
    
## <a name="return-values"></a>Rückgabewerte

S_OK zurück, wenn der Aufruf erfolgreich war; andernfalls einen Fehlercode.
  
## <a name="remarks"></a>Hinweise

Wenn Sie [GetProcAddress](https://msdn.microsoft.com/library/a0d7fc09-f888-4f46-a571-d3719a627597%28Office.15%29.aspx) zum Suchen nach der Adresse dieser Funktion in tzmovelib.dll verwenden, geben Sie HrCreateApptRebaser@44 **Prozedurnamen** an. Nicht alle Flags sind in Kombination miteinander gültig. 
  
Weitere Informationen zu den verschiedenen Optionen finden Sie im Abschnitt "Glossar der Befehlszeilenoptionen für das Outlook Time Zone Data Update Tool" in [KB 931667:](https://support.microsoft.com/kb/931667/en-us)How to address time zone changes by using the Time Zone Data Update Tool for Microsoft Office Outlook .
  
## <a name="see-also"></a>Siehe auch

- [Zum neuen Basisadressen Kalender programmgesteuert Sommerzeit](about-rebasing-calendars-programmatically-for-daylight-saving-time.md)

