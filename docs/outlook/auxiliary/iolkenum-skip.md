---
title: IOlkEnumSkip
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.localizationpriority: medium
ms.assetid: e83e409c-f201-df9d-5e30-879adf15318d
description: Überspringt eine angegebene Anzahl von Konten im Enumerator.
ms.openlocfilehash: c8c7dbcf58b5e66de4291a489f8afd3a71474eca
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59617090"
---
# <a name="iolkenumskip"></a>IOlkEnum::Skip

Überspringt eine angegebene Anzahl von Konten im Enumerator.
  
## <a name="quick-info"></a>QuickInfo

Siehe [IOlkEnum](iolkenum.md).
  
```cpp
HRESULT IOlkEnum::Skip(  
    DWORD cSkip 
);
```

## <a name="parameters"></a>Parameter

_cSkip_
  
> [in] Die Anzahl der Konten, die übersprungen werden sollen.
    
## <a name="return-values"></a>Rückgabewerte

S_OK zurück, wenn der Aufruf erfolgreich war; andernfalls einen Fehlercode.
  
## <a name="see-also"></a>Siehe auch

- [IOlkEnum::GetCount](iolkenum-getcount.md) 
- [IOlkEnum::GetNext](iolkenum-getnext.md)  
- [IOlkEnum::Reset](iolkenum-reset.md)

