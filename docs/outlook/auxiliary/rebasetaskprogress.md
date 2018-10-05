---
title: RebaseTaskProgress
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: 8b8368d2-b04b-42a5-fdc3-955fc873c2f5
description: Meldet den Status Enumeration und Neuzuordnen von Terminen.
ms.openlocfilehash: e5df0cd6df10ab86b1a125b9807637438976726f
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/04/2018
ms.locfileid: "25384353"
---
# <a name="rebasetaskprogress"></a>RebaseTaskProgress

Meldet den Status Enumeration und Neuzuordnen von Terminen.
  
## <a name="quick-info"></a>QuickInfo

|||
|:-----|:-----|
|Headerdatei:  <br/> |tzmovelib.h  <br/> |
|Implementiert von:  <br/> |MAPI-Clientanwendungen  <br/> |
|Aufgerufen von:  <br/> |Basisadressen Outlook-Objekt  <br/> |
|Zeigertyp:  <br/> |**PFNREBASETASKPROGRESS** gemäß Definition im tzmovelib.h  <br/> |
   
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
  
> [in] Niedrige Ende des Bereichs von Terminen verarbeitet werden. Es ist normalerweise 0 (null).
    
_ulMax_
  
> [in] Hohe Ende des Bereichs von Terminen verarbeitet werden. Es ist in der Regel die Anzahl der Elemente im Ordner "Kalender" verarbeitet werden.
    
_ulCur_
  
> [in] Das aktuelle Element verarbeitet werden.
    
_State_
  
> [in] Ein Wert, der den Status der das verarbeitete Element angibt. Die **REBASE_APPT_STATE** -Enumeration wird in tzmovelib.h definiert.  _Zustand_ hat einen der folgenden Werte: 
    
   - **REBASE_APPT_STATE_SCANNING_EXAMINING** – Scannen und Untersuchen eines Elements. 
    
   - **REBASE_APPT_STATE_SCANNING_FOUND** – Überprüfung und ein Element gefunden. 
    
   - **REBASE_APPT_STATE_BEGIN** – behoben und Starten eines Elements. 
    
   - **REBASE_APPT_STATE_REBASING** – behoben und Anpassen eines Elements. 
    
   - **REBASE_APPT_STATE_SENDING** – behoben und Senden einer Besprechungsanfrage. 
    
   - **REBASE_APPT_STATE_DONE** – korrigieren und mit einem Artikel fertig. 
    
_pRowCur_
  
> [in] Ein Zeiger auf eine **[SRow](https://msdn.microsoft.com/library/369c2d5c-8c2b-4314-9cb2-aaa89580aa2b%28Office.15%29.aspx)** -Struktur, die das Element überprüften oder feste beschreibt. 
    
## <a name="return-values"></a>Rückgabewerte

S_OK zurück, wenn der Aufruf erfolgreich war; andernfalls einen Fehlercode.
  
## <a name="remarks"></a>Anmerkungen

MAPI-Clientanwendungen, die verwenden die [IOlkApptRebaser](iolkapptrebaser.md) -Schnittstelle, implementieren Sie diese Funktion, um die Verarbeitung des Elements zu verfolgen. 
  
## <a name="see-also"></a>Siehe auch

- [Zum neuen Basisadressen Kalender programmgesteuert Sommerzeit](about-rebasing-calendars-programmatically-for-daylight-saving-time.md)

