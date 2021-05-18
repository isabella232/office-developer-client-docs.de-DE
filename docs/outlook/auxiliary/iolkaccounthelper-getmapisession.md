---
title: IOlkAccountHelperGetMapiSession
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: a431787c-6e9a-9be1-165f-98c778d12e3e
description: Öffnet eine MAPI-Sitzung und verwaltet einen Verweis auf die Sitzung für den Konto-Manager.
ms.openlocfilehash: 5886ac1ae1bb8f3b43e09f49e48434d9a73656ce
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32322176"
---
# <a name="iolkaccounthelpergetmapisession"></a>IOlkAccountHelper::GetMapiSession

Öffnet eine MAPI-Sitzung und verwaltet einen Verweis auf die Sitzung für den Konto-Manager.
  
## <a name="quick-info"></a>QuickInfo

Siehe [IOlkAccountHelper](iolkaccounthelper.md).
  
```cpp
HRESULT IOlkAccountHelper::GetMapiSession(  
    LPUNKNOWN *ppmsess 
);
```

## <a name="parameters"></a>Parameter

_ppmsess_
  
> [out] Die aktuelle MAPI-Sitzung.
    
## <a name="return-values"></a>Rückgabewerte

S_OK zurück, wenn der Aufruf erfolgreich war; andernfalls einen Fehlercode.
  
## <a name="remarks"></a>Hinweise

Aufgrund von Zirkelverweisproblemen kann der Kontomanager selbst den Verweis für die MAPI-Sitzung nicht verwalten.
  
## <a name="see-also"></a>Siehe auch

- [IOlkAccountHelper::HandsOffSession](iolkaccounthelper-handsoffsession.md)
- [IMAPISession : IUnknown](https://msdn.microsoft.com/library/5650fa2a-6e62-451c-964e-363f7bee2344%28Office.15%29.aspx)

