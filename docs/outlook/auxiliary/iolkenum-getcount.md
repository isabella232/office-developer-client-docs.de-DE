---
title: IOlkEnumGetCount
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.localizationpriority: medium
ms.assetid: dd7a7e62-4cf2-bdd3-8a00-4fff5ac575d3
description: Ruft die Anzahl der Konten im Enumerator ab.
ms.openlocfilehash: 5f5db79228791e3a9dc745f42560edb6901e8766
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59551989"
---
# <a name="iolkenumgetcount"></a>IOlkEnum::GetCount

Ruft die Anzahl der Konten im Enumerator ab.
  
## <a name="quick-info"></a>QuickInfo

Siehe [IOlkEnum](iolkenum.md).
  
```cpp
HRESULT IOlkEnum::GetCount ( 
    DWORD *pulCount 
);

```

## <a name="parameters"></a>Parameter

_pulCount_
  
> [out] Ein Zeiger auf die Anzahl der Objekte, die aufgezählt werden.
    
## <a name="return-values"></a>Rückgabewerte

S_OK zurück, wenn der Aufruf erfolgreich war; andernfalls einen Fehlercode.
  
## <a name="see-also"></a>Siehe auch

- [IOlkEnum::GetNext](iolkenum-getnext.md)  
- [IOlkEnum::Reset](iolkenum-reset.md) 
- [IOlkEnum::Skip](iolkenum-skip.md)

