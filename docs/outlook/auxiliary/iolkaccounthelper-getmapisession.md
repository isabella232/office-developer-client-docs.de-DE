---
title: IOlkAccountHelperGetMapiSession
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: a431787c-6e9a-9be1-165f-98c778d12e3e
description: Öffnet eine MAPI-Sitzung, und behält einen Verweis auf die Sitzung für den Kontomanager.
ms.openlocfilehash: 50809a00d13fd9f2a93bebc2961a134b3625e82c
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19791106"
---
# <a name="iolkaccounthelpergetmapisession"></a>IOlkAccountHelper::GetMapiSession

Öffnet eine MAPI-Sitzung, und behält einen Verweis auf die Sitzung für den Kontomanager.
  
## <a name="quick-info"></a>QuickInfo

Finden Sie unter [IOlkAccountHelper](iolkaccounthelper.md).
  
```cpp
HRESULT IOlkAccountHelper::GetMapiSession(  
    LPUNKNOWN *ppmsess 
);
```

## <a name="parameters"></a>Parameter

_ppmsess_
  
> [out] Der aktuellen MAPI-Sitzung.
    
## <a name="return-values"></a>Rückgabewerte

S_OK zurück, wenn der Aufruf erfolgreich war; andernfalls einen Fehlercode.
  
## <a name="remarks"></a>Anmerkungen

Aufgrund von Problemen in Zirkelverweis kann nicht selbst Konto-Manager den Verweis für die MAPI-Sitzung verwalten.
  
## <a name="see-also"></a>Siehe auch

- [IOlkAccountHelper::HandsOffSession](iolkaccounthelper-handsoffsession.md)
- [IMAPISession: IUnknown](http://msdn.microsoft.com/library/5650fa2a-6e62-451c-964e-363f7bee2344%28Office.15%29.aspx)

