---
title: HrCreateApptRebaser
manager: soliver
ms.date: 12/07/2015
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: 265028b7-a583-f6ba-0214-5a4322f98f35
description: Initialisiert ein IOlkApptRebaser-Objekt für die Verwendung in Neuzuordnen Termine im Outlook-Kalender.
ms.openlocfilehash: 33ad47d59ee2ca1b2461f730494f3466b9f8b54a
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/04/2018
ms.locfileid: "25397541"
---
# <a name="hrcreateapptrebaser"></a>HrCreateApptRebaser

Initialisiert ein [IOlkApptRebaser](iolkapptrebaser.md) -Objekt für die Verwendung in Neuzuordnen Termine im Outlook-Kalender. 
  
## <a name="quick-info"></a>QuickInfo

|||
|:-----|:-----|
|Headerdatei:  <br/> |tzmovelib.h  <br/> |
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
  
> [in] Erforderlich. Eine Bitmaske der Flags verwendet, um zu steuern, wie Neuzuordnen ausgeführt wird. Die folgenden Kennzeichen können festgelegt werden und sind in tzmovelib.h definiert:
    
   - **REBASE_FLAG_UPDATE_ORGANIZED_MEETINGS** – Terminelemente, in dem der Benutzer der Organisator der Besprechung ist, zurückgesetzt werden. Beachten Sie, dass in der Standardeinstellung dadurch Outlook senden besprechungsaktualisierungen an alle Teilnehmer einer Sitzung zurückgesetzt wird. Sie können dieses Flag kombinieren, mit **REBASE_FLAG_FORCE_NO_EX_UPDATES** oder **REBASE_FLAG_FORCE_NO_UPDATES** ändern, wie die Besprechung aktualisiert behandelt werden. 
    
   - **REBASE_FLAG_UPDATE_UNMARKED** – aktualisieren Terminelemente, die nicht gekennzeichnet wurden mit einer Zeitzone. Wenn dieses Flag angegeben wird, wird der *pTZMissing* Wert als die Zeitzone, die in ein Element erstellt wird für alle Elemente verwendet, die nicht Zeitzonendaten verfügen. 
    
   - **REBASE_FLAG_UPDATE_ONLYRECURRING** – nur Termin Terminserien aktualisieren. 
    
   - **REBASE_FLAG_NO_UI** – einschließlich Anmeldung Dialogfelder angezeigt, in der Regel beim Öffnen eines Nachrichtenspeichers Benutzeroberfläche (UI), nicht anzeigen. 
    
   - **REBASE_FLAG_UPDATE_MINIMIZEAPPTS** – führen Sie nicht einer Terminelemente, die in der Vergangenheit auftreten. 
    
   - **REBASE_FLAG_FORCE_REBASE** – nicht den Organisator zum Neuzuordnen von Entscheidungen prüfen, aber einer Terminelemente, in dem der Benutzer ein Teilnehmer ist. 
    
   - **REBASE_FLAG_FORCE_NO_EX_UPDATES** – senden nur aktualisiert, wenn der Benutzer der Organisator ist und Empfänger nicht mit einem Exchange-Server verbunden ist. 
    
   - **REBASE_FLAG_FORCE_NO_UPDATES** – Updates nie senden. 
    
   - **REBASE_FLAG_ONLY_CREATED_PRE_PATCH** – einer nur Einzel-Instanz Terminelemente erstellt, bevor der Patch angewendet wurde. 
    
   - **REBASE_FLAG_REPORTING_MODE** – nicht tatsächlich Rebase ausführen, würde nur Bericht Termin Elemente, die zurückgesetzt werden. 
    
   - **REBASE_FLAG_SEND_RESOURCE_UPDATES** – besprechungsaktualisierungen auf Ressourcen zu senden. 
    
_pSession_
  
> [in] Erforderlich. Ein Zeiger auf eine MAPI-Sitzung-Schnittstelle.
    
_pCalendarMsgStore_
  
> [in] Erforderlich. Ein Zeiger auf einen Nachrichtenspeicher mit Terminelemente zu zurückgesetzt werden.
    
_pCalendarFolder_
  
> [in] Erforderlich. Ein Zeiger auf einen Kalenderordner mit Terminelemente zu zurückgesetzt werden.
    
_pwszUpdatePrefix_
  
> [in] Optional. Ein Zeiger auf eine Zeichenfolge mit dem Präfix, das auf Besprechungsanfragen vorangestellt werden. NULL kann sein.
    
_pftInstallDateUTC_
  
> [in] Optional. Der Zeitzone Patch installieren Datum. Nur verwendet, wenn das Flag **REBASE_FLAG_ONLY_CREATED_PRE_PATCH** festgelegt ist. 
    
_IExpansionDepth_
  
> [in] Optional. Die Erweiterung Tiefe beim Empfänger ausschließen listet Verteilerlisten mit Exchange Server verbunden ist. Nur verwendet, wenn das Flag **REBASE_FLAG_FORCE_NO_EX_UPDATES** festgelegt ist. 
    
_pTZTo_
  
> [in] Erforderlich. Ein Zeiger auf eine **TZDEFINITION** -Struktur, beschreibt die Zeitzone, um zurückgesetzt werden. **TZDEFINITION** ist in Tzmovelib definiert. 
    
pTZMissing
  
> [in] Erforderlich. Ein Zeiger auf eine **TZDEFINITION** -Struktur, beschreibt die Zeitzone um betrachtet werden, wenn die Informationen zur Zeitzone für ein Element nicht versehen ist. Darf nicht NULL, aber nur sein verwendet, wenn das Flag **REBASE_FLAG_UPDATE_UNMARKED** festgelegt ist. 
    
_ppError_
  
> [out] Ein Zeiger auf einen Zeiger auf eine **MAPIERROR** -Struktur, die Angaben zu Version, Komponente und Kontext für den Fehler enthält. NULL, wenn keine erweiterten Fehlerinformationen erwünscht ist. Mit [MAPIFreeBuffer](https://msdn.microsoft.com/library/9412594f-8acc-4c7e-a668-4ec1da0ad9cf%28Office.15%29.aspx)frei. 
    
_ppApptRebase_
  
> [out] Ein Zeiger auf einen Zeiger auf die zurückgegebene Schnittstelle **IOlkApptRebaser** . 
    
## <a name="return-values"></a>Rückgabewerte

S_OK zurück, wenn der Aufruf erfolgreich war; andernfalls einen Fehlercode.
  
## <a name="remarks"></a>Anmerkungen

Wenn [GetProcAddress](https://msdn.microsoft.com/library/a0d7fc09-f888-4f46-a571-d3719a627597%28Office.15%29.aspx) für die Adresse des dieser Funktion in tzmovelib.dll suchen, geben Sie **HrCreateApptRebaser@44** als den Namen der Prozedur. Nicht alle der Werte sind gültig in Kombination mit anderen. 
  
Weitere Informationen zu den verschiedenen Optionen finden Sie im Abschnitt "Glossar mit Befehlszeilenoptionen für die Outlook-Zeitzone Aktualisierungstool" in [KB 931667: wie Adresse, Zeitzone Änderungen mithilfe der Zeit Zeitzonendaten für Microsoft Office Outlook](https://support.microsoft.com/kb/931667/en-us).
  
## <a name="see-also"></a>Siehe auch

- [Zum neuen Basisadressen Kalender programmgesteuert Sommerzeit](about-rebasing-calendars-programmatically-for-daylight-saving-time.md)

