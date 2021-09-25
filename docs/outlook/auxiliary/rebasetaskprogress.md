---
title: RebaseTaskProgress
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: overview
ms.localizationpriority: medium
ms.assetid: 8b8368d2-b04b-42a5-fdc3-955fc873c2f5
description: Meldet den Fortschritt für die Aufzählung und Neubasierung von Terminen.
ms.openlocfilehash: 8ea71e8a76baf8b7f69afa90ac9f0c06c1a64a1b
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59614311"
---
# <a name="rebasetaskprogress"></a>RebaseTaskProgress

Meldet den Fortschritt für die Aufzählung und Neubasierung von Terminen.
  
## <a name="quick-info"></a>QuickInfo

|||
|:-----|:-----|
|Headerdatei  <br/> |tzmovelib.h  <br/> |
|Implementiert von:  <br/> |MAPI-Clientanwendungen  <br/> |
|Aufgerufen von:  <br/> |Outlook-Basisobjekt  <br/> |
|Zeigertyp:  <br/> |**PFNREBASETASKPROGRESS** gemäß Definition in tzmovelib.h  <br/> |
   
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
  
> [in] Das untere Ende des Bereichs von Terminen, die verarbeitet werden. Normalerweise ist dies Null.
    
_ulMax_
  
> [in] Das obere Ende des Bereichs von Terminen, die verarbeitet werden. Dies ist in der Regel die Anzahl der Elemente im Kalenderordner, der verarbeitet wird.
    
_ulCur_
  
> [in] Das aktuelle Element, das verarbeitet wird.
    
_State_
  
> [in] Ein Wert, der den Status des verarbeiteten Elements angibt. Die Enumeration **REBASE_APPT_STATE** ist in tzmovelib.h definiert.  _State_ hat einen der folgenden Werte: 
    
   - **REBASE_APPT_STATE_SCANNING_EXAMINING** : Scannen und Untersuchen eines Elements. 
    
   - **REBASE_APPT_STATE_SCANNING_FOUND** : Ein Element wird gescannt und gefunden. 
    
   - **REBASE_APPT_STATE_BEGIN** : Korrigieren und Starten eines Elements. 
    
   - **REBASE_APPT_STATE_REBASING** : Korrigieren und Anpassen eines Elements. 
    
   - **REBASE_APPT_STATE_SENDING** – Korrigieren und Senden eines Besprechungsupdates. 
    
   - **REBASE_APPT_STATE_DONE** : Korrigieren und Mit einem Element fertig. 
    
_pRowCur_
  
> [in] Ein Zeiger auf eine **[SRow-Struktur,](https://msdn.microsoft.com/library/369c2d5c-8c2b-4314-9cb2-aaa89580aa2b%28Office.15%29.aspx)** die das gescannte oder feste Element beschreibt. 
    
## <a name="return-values"></a>Rückgabewerte

S_OK zurück, wenn der Aufruf erfolgreich war; andernfalls einen Fehlercode.
  
## <a name="remarks"></a>Bemerkungen

MAPI-Clientanwendungen, die die [IOlkApptRebaser-Schnittstelle](iolkapptrebaser.md) verwenden, implementieren diese Funktion zum Nachverfolgen der Elementverarbeitung. 
  
## <a name="see-also"></a>Siehe auch

- [Zum neuen Basisadressen Kalender programmgesteuert Sommerzeit](about-rebasing-calendars-programmatically-for-daylight-saving-time.md)

