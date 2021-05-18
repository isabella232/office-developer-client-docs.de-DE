---
title: IOlkApptRebaserBeginEnumerateAppointments
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 8946703a-aaa8-6b3f-aa68-931365db620d
description: Beginnt eine Aufgabe für die Enumeration der Termin im Kalenderordner Termine zu finden, die neuen Basisadressen benötigen.
ms.openlocfilehash: cc89b3510f09bb98fd6720cb6d5ab3edeb13eac8
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33407270"
---
# <a name="iolkapptrebaserbeginenumerateappointments"></a>IOlkApptRebaser::BeginEnumerateAppointments

Beginnt eine Aufgabe für die Enumeration der Termin im Kalenderordner Termine zu finden, die neuen Basisadressen benötigen.
  
## <a name="quick-info"></a>QuickInfo

Finden Sie unter [IOlkApptRebaser](iolkapptrebaser.md).
  
```cpp
HRESULT BeginEnumerateAppointments( 
    PFNREBASETASKPROGRESS pfnProgress, 
    void **ppContext);
```

## <a name="parameters"></a>Parameter

_pfnProgress_
  
> [in] Optional. Ein Zeiger auf ein Rebase-Funktion zum Fortschritt Task Status empfangen. **PFNREBASETASKPROGRESS** wird in tzmovelib.h definiert. 
    
_ppContext_
  
> [out] Erforderlich. Ein Zeiger auf einen Zeiger auf den zurückgegebenen Kontext. Dieser Kontext wird an [IOlkApptRebaser::EndEnumerateAppointments](iolkapptrebaser-endenumerateappointments.md)übergeben werden.
    
## <a name="return-values"></a>Rückgabewerte

S_OK zurück, wenn der Aufruf erfolgreich war; andernfalls einen Fehlercode.
  
## <a name="remarks"></a>Hinweise

Diese Aufgabe wird in einem neuen Thread ausgeführt.
  
## <a name="see-also"></a>Siehe auch

- [Zum neuen Basisadressen Kalender programmgesteuert Sommerzeit](about-rebasing-calendars-programmatically-for-daylight-saving-time.md)

