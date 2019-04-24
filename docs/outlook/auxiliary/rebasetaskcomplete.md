---
title: RebaseTaskComplete
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: 2de5c77c-3fac-cfb6-3719-68df4013cf11
description: Meldet den Abschluss für die erneute Erstellung von Terminen.
ms.openlocfilehash: 9fab0d06bf0b9856b9a968f5c0db1bb15b0fe0bd
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32328322"
---
# <a name="rebasetaskcomplete"></a>RebaseTaskComplete

Meldet den Abschluss für die erneute Erstellung von Terminen.
  
## <a name="quick-info"></a>QuickInfo

|||
|:-----|:-----|
|Headerdatei  <br/> |tzmovelib. h  <br/> |
|Implementiert von:  <br/> |MAPI-Clientanwendungen  <br/> |
|Aufgerufen von:  <br/> |Outlook-Objekt wird erneut basiert  <br/> |
|Zeigertyp:  <br/> |**PFNREBASETASKCOMPLETE** wie in tzmovelib. h definiert  <br/> |
   
```cpp
void STDAPICALLTYPE RebaseTaskComplete(  
    ULONG ulRowIndex, 
    const SRow* pRowCur, 
    HRESULT hrResult, 
    BOOL fModified, 
    BOOL fSentUpdate, 
    const MAPIERROR* pError); 

```

## <a name="parameters"></a>Parameter

_ulRowIndex_
  
> in Die Zeile, die verarbeitet wurde. Dieser Index verweist auf die **[SRowSet](https://msdn.microsoft.com/library/7e3761be-afd6-46cb-9a08-25e9016c1241%28Office.15%29.aspx)** -Struktur, die an [IOlkApptRebaser:: beginrebaseappointmentsabgerufen](iolkapptrebaser-beginrebaseappointments.md)übergeben wird.
    
_pRowCur_
  
> in] ein Zeiger auf eine **[SRow](https://msdn.microsoft.com/library/369c2d5c-8c2b-4314-9cb2-aaa89580aa2b%28Office.15%29.aspx)** -Struktur, die das verarbeitete Element beschreibt. 
    
_hrResult_
  
> in Ein **HRESULT** , das das Ergebnis des Wiederverwendungsvorgangs angibt. 
    
_fModified_
  
> in Gibt an, ob das Element geändert wurde.
    
_fSentUpdate_
  
> in Gibt an, ob eine Besprechungs Update Nachricht gesendet wurde. 
    
_pError_
  
> in Ein Zeiger auf eine **MAPIERROR** -Struktur mit erweiterten Fehlerinformationen. 
    
## <a name="return-values"></a>Rückgabewerte

S_OK zurück, wenn der Aufruf erfolgreich war; andernfalls einen Fehlercode.
  
## <a name="remarks"></a>Bemerkungen

MAPI-Clientanwendungen, die die [IOlkApptRebaser](iolkapptrebaser.md) -Schnittstelle verwenden, implementieren diese Funktion, um den Abschluss von Elementaktualisierungen nachzuverfolgen. 
  
## <a name="see-also"></a>Siehe auch

- [Zum neuen Basisadressen Kalender programmgesteuert Sommerzeit](about-rebasing-calendars-programmatically-for-daylight-saving-time.md)

