---
title: RebaseTaskComplete
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: overview
ms.localizationpriority: medium
ms.assetid: 2de5c77c-3fac-cfb6-3719-68df4013cf11
description: Meldet den Abschluss für die Neubasierung von Terminen.
ms.openlocfilehash: 49061cf21f4a6ffd3218bac2470a1afc6e2ebf81
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59614332"
---
# <a name="rebasetaskcomplete"></a>RebaseTaskComplete

Meldet den Abschluss für die Neubasierung von Terminen.
  
## <a name="quick-info"></a>QuickInfo

|||
|:-----|:-----|
|Headerdatei  <br/> |tzmovelib.h  <br/> |
|Implementiert von:  <br/> |MAPI-Clientanwendungen  <br/> |
|Aufgerufen von:  <br/> |Outlook-Basisobjekt  <br/> |
|Zeigertyp:  <br/> |**PFNREBASETASKCOMPLETE** gemäß Definition in tzmovelib.h  <br/> |
   
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
  
> [in] Die Zeile, die verarbeitet wurde. Dieser Index bezieht sich auf die **[SRowSet-Struktur,](https://msdn.microsoft.com/library/7e3761be-afd6-46cb-9a08-25e9016c1241%28Office.15%29.aspx)** die an [IOlkApptRebaser::BeginRebaseAppointments](iolkapptrebaser-beginrebaseappointments.md)übergeben wird.
    
_pRowCur_
  
> in] Ein Zeiger auf eine **[SRow-Struktur,](https://msdn.microsoft.com/library/369c2d5c-8c2b-4314-9cb2-aaa89580aa2b%28Office.15%29.aspx)** die das verarbeitete Element beschreibt. 
    
_hrResult_
  
> [in] Ein **HRESULT,** das das Ergebnis des Neubasierungsvorgangs angibt. 
    
_fModified_
  
> [in] Gibt an, ob das Element geändert wurde.
    
_fSentUpdate_
  
> [in] Gibt an, ob eine Besprechungsaktualisierungsnachricht gesendet wurde. 
    
_Perror_
  
> [in] Ein Zeiger auf eine **MAPIERROR-Struktur** mit erweiterten Fehlerinformationen. 
    
## <a name="return-values"></a>Rückgabewerte

S_OK zurück, wenn der Aufruf erfolgreich war; andernfalls einen Fehlercode.
  
## <a name="remarks"></a>Bemerkungen

MAPI-Clientanwendungen, die die [IOlkApptRebaser-Schnittstelle](iolkapptrebaser.md) verwenden, implementieren diese Funktion, um den Abschluss von Elementupdates nachzuverfolgen. 
  
## <a name="see-also"></a>Siehe auch

- [Zum neuen Basisadressen Kalender programmgesteuert Sommerzeit](about-rebasing-calendars-programmatically-for-daylight-saving-time.md)

