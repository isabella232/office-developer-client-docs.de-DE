---
title: RebaseTaskProgress
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: 8b8368d2-b04b-42a5-fdc3-955fc873c2f5
description: Meldet den Fortschritt für die Aufzählung und die Begründung von Terminen.
ms.openlocfilehash: e5df0cd6df10ab86b1a125b9807637438976726f
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32326453"
---
# <a name="rebasetaskprogress"></a>RebaseTaskProgress

Meldet den Fortschritt für die Aufzählung und die Begründung von Terminen.
  
## <a name="quick-info"></a>QuickInfo

|||
|:-----|:-----|
|Headerdatei  <br/> |tzmovelib. h  <br/> |
|Implementiert von:  <br/> |MAPI-Clientanwendungen  <br/> |
|Aufgerufen von:  <br/> |Outlook-Objekt wird erneut basiert  <br/> |
|Zeigertyp:  <br/> |**PFNREBASETASKPROGRESS** wie in tzmovelib. h definiert  <br/> |
   
```cpp
void STDAPICALLTYPE RebaseTaskProgress(  
    ULONG ulMin, 
    ULONG ulMax, 
    ULONG ulCur, 
    REBASE_APPT_STATE State, 
    const SRow* pRowCur); 

```

## <a name="parameters"></a>Parameter

_ulMin_
  
> in Das untere Ende des Bereiches der zu verarbeitenden Termine. Es ist normalerweise Null.
    
_ulMax_
  
> in Das obere Ende des Bereiches der zu verarbeitenden Termine. In der Regel wird die Anzahl der Elemente im Kalenderordner verarbeitet.
    
_ulCur_
  
> in Das aktuelle Element, das verarbeitet wird.
    
_State_
  
> in Ein Wert, der den Status des zu verarbeitenden Elements angibt. Die Aufzählung **REBASE_APPT_STATE** ist in tzmovelib. h definiert.  _State_ hat einen der folgenden Werte: 
    
   - **REBASE_APPT_STATE_SCANNING_EXAMINING** – überprüfen und untersuchen eines Elements. 
    
   - **REBASE_APPT_STATE_SCANNING_FOUND** – ein Element wird gescannt und gefunden. 
    
   - **REBASE_APPT_STATE_BEGIN** – fixieren und Starten eines Elements. 
    
   - **REBASE_APPT_STATE_REBASING** – Behebung und Anpassung eines Elements. 
    
   - **REBASE_APPT_STATE_SENDING** – Behebung und Senden eines Besprechungs Updates. 
    
   - **REBASE_APPT_STATE_DONE** – Behebung und fertig mit einem Element. 
    
_pRowCur_
  
> in Ein Zeiger auf eine **[SRow](https://msdn.microsoft.com/library/369c2d5c-8c2b-4314-9cb2-aaa89580aa2b%28Office.15%29.aspx)** -Struktur, die das Element beschreibt, das überprüft oder korrigiert wird. 
    
## <a name="return-values"></a>Rückgabewerte

S_OK zurück, wenn der Aufruf erfolgreich war; andernfalls einen Fehlercode.
  
## <a name="remarks"></a>Bemerkungen

MAPI-Clientanwendungen, die die [IOlkApptRebaser](iolkapptrebaser.md) -Schnittstelle verwenden, implementieren diese Funktion, um die Elementverarbeitung nachzuverfolgen. 
  
## <a name="see-also"></a>Siehe auch

- [Zum neuen Basisadressen Kalender programmgesteuert Sommerzeit](about-rebasing-calendars-programmatically-for-daylight-saving-time.md)

