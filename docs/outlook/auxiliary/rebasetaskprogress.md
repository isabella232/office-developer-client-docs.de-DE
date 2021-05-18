---
title: RebaseTaskProgress
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: 8b8368d2-b04b-42a5-fdc3-955fc873c2f5
description: Meldet den Fortschritt für die Aufzählung und Neubasierung von Terminen.
ms.openlocfilehash: e5df0cd6df10ab86b1a125b9807637438976726f
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32326453"
---
# <a name="rebasetaskprogress"></a>RebaseTaskProgress

Meldet den Fortschritt für die Aufzählung und Neubasierung von Terminen.
  
## <a name="quick-info"></a>QuickInfo

|||
|:-----|:-----|
|Headerdatei  <br/> |tzmovelib.h  <br/> |
|Implementiert von:  <br/> |MAPI-Clientanwendungen  <br/> |
|Aufgerufen von:  <br/> |Outlook-Neubasierungsobjekt  <br/> |
|Zeigertyp:  <br/> |**PFNREBASETASKPROGRESS** gemäß definition in tzmovelib.h  <br/> |
   
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
  
> [in] Das niedrige Ende des zu verarbeitenden Terminbereichs. In der Regel ist es null.
    
_ulMax_
  
> [in] Das hohe Ende des zu verarbeitenden Terminbereichs. Dies ist in der Regel die Anzahl der Elemente im zu verarbeitende Kalenderordner.
    
_ulCur_
  
> [in] Das aktuelle Element, das verarbeitet wird.
    
_State_
  
> [in] Ein Wert, der den Status des verarbeiteten Elements angibt. Die Enumeration **REBASE_APPT_STATE** in tzmovelib.h definiert.  _State_ hat einen der folgenden Werte: 
    
   - **REBASE_APPT_STATE_SCANNING_EXAMINING** – Scannen und Untersuchen eines Elements. 
    
   - **REBASE_APPT_STATE_SCANNING_FOUND** – Ein Element wurde gescannt und gefunden. 
    
   - **REBASE_APPT_STATE_BEGIN** – Fixieren und Starten eines Elements. 
    
   - **REBASE_APPT_STATE_REBASING** – Fixieren und Anpassen eines Elements. 
    
   - **REBASE_APPT_STATE_SENDING** – Beheben und Senden eines Besprechungsupdates. 
    
   - **REBASE_APPT_STATE_DONE** – Fixieren und Fertig mit einem Element. 
    
_pRowCur_
  
> [in] Ein Zeiger auf eine **[SRow-Struktur,](https://msdn.microsoft.com/library/369c2d5c-8c2b-4314-9cb2-aaa89580aa2b%28Office.15%29.aspx)** die das gescannte oder feste Element beschreibt. 
    
## <a name="return-values"></a>Rückgabewerte

S_OK zurück, wenn der Aufruf erfolgreich war; andernfalls einen Fehlercode.
  
## <a name="remarks"></a>Hinweise

MAPI-Clientanwendungen, die die [IOlkApptRebaser-Schnittstelle](iolkapptrebaser.md) verwenden, implementieren diese Funktion, um die Elementverarbeitung nachzuverfolgen. 
  
## <a name="see-also"></a>Siehe auch

- [Zum neuen Basisadressen Kalender programmgesteuert Sommerzeit](about-rebasing-calendars-programmatically-for-daylight-saving-time.md)

