---
title: IOlkApptRebaserEndRebaseAppointments
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: e47d5a8d-6a13-f430-fbfd-00df04b4a006
description: Führen Sie neuen Basisadressen Termin wartet, und ruft die Ergebnisse ab.
ms.openlocfilehash: fd27021ce05b1d5b95fd258e0ee89b5bd4f2c7db
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19791123"
---
# <a name="iolkapptrebaserendrebaseappointments"></a>IOlkApptRebaser::EndRebaseAppointments

Führen Sie neuen Basisadressen Termin wartet, und ruft die Ergebnisse ab.
  
## <a name="quick-info"></a>QuickInfo

Finden Sie unter [IOlkApptRebaser](iolkapptrebaser.md).
  
```cpp
HRESULT EndRebaseAppointments( 
    void *pContext, 
    HRESULT *phResult);
```

## <a name="parameters"></a>Parameter

_pContext_
  
> [in] Erforderlich. Ein Zeiger auf den Kontext von einem Aufruf von [IOlkApptRebaser::BeginRebaseAppointments](iolkapptrebaser-beginrebaseappointments.md)abgerufen.
    
_phResult_
  
> [out] Erforderlich. Ein Zeiger auf ein **HRESULT** zum Abrufen des Ergebnisses des Vorgangs Basisadressen. 
    
## <a name="return-values"></a>Rückgabewerte

S_OK zurück, wenn der Aufruf erfolgreich war; andernfalls einen Fehlercode.
  
## <a name="see-also"></a>Siehe auch

- [Zum neuen Basisadressen Kalender programmgesteuert Sommerzeit](about-rebasing-calendars-programmatically-for-daylight-saving-time.md)

