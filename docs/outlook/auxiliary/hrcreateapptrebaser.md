---
title: HrCreateApptRebaser
manager: soliver
ms.date: 12/07/2015
ms.audience: Developer
ms.topic: overview
ms.localizationpriority: medium
ms.assetid: 265028b7-a583-f6ba-0214-5a4322f98f35
description: Initialisiert ein IOlkApptRebaser-Objekt für die Verwendung beim Neubasieren von Terminen in Outlook Kalendern.
ms.openlocfilehash: 8c9b8e2081904f9e37916a13b904d1595fc108a1
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59592781"
---
# <a name="hrcreateapptrebaser"></a>HrCreateApptRebaser

Initialisiert ein [IOlkApptRebaser-Objekt](iolkapptrebaser.md) für die Verwendung beim Neubasieren von Terminen in Outlook Kalendern. 
  
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
  
> [in] Erforderlich. Eine Bitmaske mit Flags, die zum Steuern der Neubasierung verwendet wird. Die folgenden Flags können festgelegt und in tzmovelib.h definiert werden:
    
   - **REBASE_FLAG_UPDATE_ORGANIZED_MEETINGS** : Terminelemente, in denen der Benutzer der Besprechungsorganisator ist, werden neubasiert. Beachten Sie, dass dies standardmäßig dazu führt, dass Outlook Besprechungsupdates an alle Teilnehmer einer Besprechung senden, die neu basiert. Sie können dieses Flag mit **REBASE_FLAG_FORCE_NO_EX_UPDATES** oder **REBASE_FLAG_FORCE_NO_UPDATES** kombinieren, um die Behandlung von Besprechungsupdates zu ändern. 
    
   - **REBASE_FLAG_UPDATE_UNMARKED** : Terminelemente aktualisieren, die nicht mit einer Zeitzone markiert wurden. Wenn dieses Kennzeichen angegeben ist, wird der  *pTZMissing-Wert*  als Zeitzone verwendet, in der ein Element für alle Elemente erstellt wird, die keine Zeitzonendaten haben. 
    
   - **REBASE_FLAG_UPDATE_ONLYRECURRING** : Aktualisieren Sie nur Terminserienelemente. 
    
   - **REBASE_FLAG_NO_UI** : Zeigen Sie keine Benutzeroberfläche an, einschließlich der Anmeldedialogfelder, die beim Öffnen eines Nachrichtenspeichers in der Regel angezeigt werden. 
    
   - **REBASE_FLAG_UPDATE_MINIMIZEAPPTS** : Erstellen Sie keine Neubasis für Terminelemente, die in der Vergangenheit aufgetreten sind. 
    
   - **REBASE_FLAG_FORCE_REBASE** : Überprüfen Sie den Organisator nicht auf Neubasierungsentscheidungen, sondern überprüfen Sie terminbezogene Elemente, an denen der Benutzer teilnehmerbasiert ist. 
    
   - **REBASE_FLAG_FORCE_NO_EX_UPDATES** : Senden von Updates nur, wenn der Benutzer der Organisator ist und der Empfänger nicht mit einem Exchange Server verbunden ist. 
    
   - **REBASE_FLAG_FORCE_NO_UPDATES** : Updates niemals senden. 
    
   - **REBASE_FLAG_ONLY_CREATED_PRE_PATCH** : Erstellen Sie nur Terminelemente mit einer Instanz, die erstellt wurden, bevor der Patch angewendet wurde, neu. 
    
   - **REBASE_FLAG_REPORTING_MODE** : Erstellen Sie keine rebase, melden Sie nur Terminelemente, die neu basieren würden. 
    
   - **REBASE_FLAG_SEND_RESOURCE_UPDATES** : Senden von Besprechungsupdates an Ressourcen. 
    
_pSession_
  
> [in] Erforderlich. Ein Zeiger auf eine MAPI-Sitzungsschnittstelle.
    
_pCalendarMsgStore_
  
> [in] Erforderlich. Ein Zeiger auf einen Nachrichtenspeicher mit Terminelementen, die neubasiert werden sollen.
    
_pCalendarFolder_
  
> [in] Erforderlich. Ein Zeiger auf einen Kalenderordner mit Terminelementen, die neu erstellt werden sollen.
    
_pwszUpdatePrefix_
  
> [in] Optional. Ein Zeiger auf eine Zeichenfolge, die das Präfix enthält, das bei Besprechungsanfragen vorangestellt werden soll. Kann NULL sein.
    
_pftInstallDateUTC_
  
> [in] Optional. Das Installationsdatum des Zeitzonenpatches. Wird nur verwendet, wenn das **REBASE_FLAG_ONLY_CREATED_PRE_PATCH-Flag** festgelegt ist. 
    
_IExpansionDepth_
  
> [in] Optional. Die Erweiterungstiefe beim Erweitern von Verteilerlisten, um Empfänger auszuschließen, die mit Exchange Server verbunden sind. Wird nur verwendet, wenn das **REBASE_FLAG_FORCE_NO_EX_UPDATES-Flag** festgelegt ist. 
    
_pTZTo_
  
> [in] Erforderlich. Ein Zeiger auf eine **TZDEFINITION-Struktur,** die die Zeitzone beschreibt, auf die neu basiert werden soll. **TZDEFINITION** ist in tzmovelib definiert. 
    
pTZMissing
  
> [in] Erforderlich. Ein Zeiger auf eine **TZDEFINITION-Struktur,** die die Zeitzone beschreibt, die angenommen werden soll, wenn Zeitzoneninformationen für ein Element nicht gestempelt werden. Darf nicht NULL sein, sondern nur verwendet werden, wenn das **REBASE_FLAG_UPDATE_UNMARKED-Flag** festgelegt ist. 
    
_ppError_
  
> [out] Ein Zeiger auf einen Zeiger auf eine **MAPIERROR-Struktur,** die Versions-, Komponenten- und Kontextinformationen für den Fehler enthält. Kann NULL sein, wenn keine erweiterten Fehlerinformationen gewünscht werden. Kostenlos mit [MAPIFreeBuffer](https://msdn.microsoft.com/library/9412594f-8acc-4c7e-a668-4ec1da0ad9cf%28Office.15%29.aspx). 
    
_ppApptRebase_
  
> [out] Ein Zeiger auf einen Zeiger auf die zurückgegebene **IOlkApptRebaser-Schnittstelle.** 
    
## <a name="return-values"></a>Rückgabewerte

S_OK zurück, wenn der Aufruf erfolgreich war; andernfalls einen Fehlercode.
  
## <a name="remarks"></a>HinwBemerkungeneise

Wenn [Sie GetProcAddress](https://msdn.microsoft.com/library/a0d7fc09-f888-4f46-a571-d3719a627597%28Office.15%29.aspx) zum Suchen nach der Adresse dieser Funktion in tzmovelib.dll verwenden, geben Sie **HrCreateApptRebaser@44** als Prozedurnamen an. Nicht alle Flags sind in Kombination miteinander gültig. 
  
Weitere Informationen zu den verschiedenen Optionen finden Sie im Abschnitt "Glossar der Befehlszeilenoptionen für das Tool Outlook Zeitzonen-Datenaktualisierung" in [KB 931667: Behandeln von Zeitzonenänderungen mithilfe des](https://support.microsoft.com/kb/931667/en-us)Tools zur Aktualisierung von Zeitzonen für Microsoft Office Outlook .
  
## <a name="see-also"></a>Siehe auch

- [Zum neuen Basisadressen Kalender programmgesteuert Sommerzeit](about-rebasing-calendars-programmatically-for-daylight-saving-time.md)

