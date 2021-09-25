---
title: IOlkApptRebaserEndRebaseAppointments
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.localizationpriority: medium
ms.assetid: e47d5a8d-6a13-f430-fbfd-00df04b4a006
description: Führen Sie neuen Basisadressen Termin wartet, und ruft die Ergebnisse ab.
ms.openlocfilehash: 0b2d76308fbc46134db6a1bb8ac5f79c63ee365a
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59557148"
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

