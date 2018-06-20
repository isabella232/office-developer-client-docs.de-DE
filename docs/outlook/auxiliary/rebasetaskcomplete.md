---
title: RebaseTaskComplete
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: 2de5c77c-3fac-cfb6-3719-68df4013cf11
description: Berichte Abschluss zum Neuzuordnen von Terminen.
ms.openlocfilehash: 735d875b4151c86103a1ac0378bd33b84de64997
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19791212"
---
# <a name="rebasetaskcomplete"></a>RebaseTaskComplete

Berichte Abschluss zum Neuzuordnen von Terminen.
  
## <a name="quick-info"></a>QuickInfo

|||
|:-----|:-----|
|Headerdatei  <br/> |tzmovelib.h  <br/> |
|Implementiert von:  <br/> |MAPI-Clientanwendungen  <br/> |
|Aufgerufen von:  <br/> |Basisadressen Outlook-Objekt  <br/> |
|Zeigertyp:  <br/> |**PFNREBASETASKCOMPLETE** gemäß Definition im tzmovelib.h  <br/> |
   
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
  
> [in] Die Zeile, die verarbeitet wurde. Dieser Index bezieht sich auf die **[SRowSet](http://msdn.microsoft.com/library/7e3761be-afd6-46cb-9a08-25e9016c1241%28Office.15%29.aspx)** Struktur [IOlkApptRebaser::BeginRebaseAppointments](iolkapptrebaser-beginrebaseappointments.md)übergeben.
    
_pRowCur_
  
> [in] ein Zeiger auf eine **[SRow](http://msdn.microsoft.com/library/369c2d5c-8c2b-4314-9cb2-aaa89580aa2b%28Office.15%29.aspx)** -Struktur, die Beschreibung des Artikels, die verarbeitet wurde. 
    
_hrResult_
  
> [in] Ein **HRESULT** zurück, der das Ergebnis des Vorgangs Basisadressen angibt. 
    
_fModified_
  
> [in] Gibt an, ob das Element geändert wurde.
    
_fSentUpdate_
  
> [in] Gibt an, ob die Aktualisierung einer Besprechungsanfrage Nachricht gesendet wurde. 
    
_pError_
  
> [in] Ein Zeiger auf eine **MAPIERROR** -Struktur mit erweiterten Fehlerinformationen. 
    
## <a name="return-values"></a>Rückgabewerte

S_OK zurück, wenn der Aufruf erfolgreich war; andernfalls einen Fehlercode.
  
## <a name="remarks"></a>Anmerkungen

MAPI-Clientanwendungen, die verwenden die [IOlkApptRebaser](iolkapptrebaser.md) -Schnittstelle, implementieren Sie diese Funktion zum Abschluss des elementupdates nachverfolgen. 
  
## <a name="see-also"></a>Siehe auch

- [Zum neuen Basisadressen Kalender programmgesteuert Sommerzeit](about-rebasing-calendars-programmatically-for-daylight-saving-time.md)

