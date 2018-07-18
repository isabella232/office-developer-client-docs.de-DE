---
title: IOlkEnumGetCount
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: dd7a7e62-4cf2-bdd3-8a00-4fff5ac575d3
description: Ruft die Anzahl von Konten in den Enumerator ab.
ms.openlocfilehash: dd4152a898bdaa96883bcd27ab3ec0d94e80fd90
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19791116"
---
# <a name="iolkenumgetcount"></a>IOlkEnum::GetCount

Ruft die Anzahl von Konten in den Enumerator ab.
  
## <a name="quick-info"></a>QuickInfo

Finden Sie unter [IOlkEnum](iolkenum.md).
  
```cpp
HRESULT IOlkEnum::GetCount ( 
    DWORD *pulCount 
);

```

## <a name="parameters"></a>Parameter

_pulCount_
  
> [out] Ein Zeiger auf die Anzahl der Objekte, die aufgelistet.
    
## <a name="return-values"></a>Rückgabewerte

S_OK zurück, wenn der Aufruf erfolgreich war; andernfalls einen Fehlercode.
  
## <a name="see-also"></a>Siehe auch

- [IOlkEnum::GetNext](iolkenum-getnext.md)  
- [IOlkEnum::Reset](iolkenum-reset.md) 
- [IOlkEnum::Skip](iolkenum-skip.md)

