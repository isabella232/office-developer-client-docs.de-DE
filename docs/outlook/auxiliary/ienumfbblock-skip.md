---
title: IEnumFBBlockSkip
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.localizationpriority: medium
ms.assetid: 70fbdb41-46ea-d016-25a2-37e94962095d
description: Überspringt eine angegebene Anzahl von Frei/Gebucht-Datenblöcken.
ms.openlocfilehash: baf13acb36d1455873771f1191461b7d17677959
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59580412"
---
# <a name="ienumfbblockskip"></a>IEnumFBBlock::Skip

Überspringt eine angegebene Anzahl von Frei/Gebucht-Datenblöcken.
  
## <a name="quick-info"></a>QuickInfo

Siehe [IEnumFBBlock](ienumfbblock.md).
  
```cpp
HRESULT Skip(  
    LONG celt 
);
```

## <a name="parameters"></a>Parameter

_Celt_
  
>  [in] Die Anzahl der frei/Gebucht-Blöcke, die übersprungen werden sollen. 
    
## <a name="return-values"></a>Rückgabewerte

S_OK zurück, wenn der Aufruf erfolgreich war; andernfalls einen Fehlercode.
  
## <a name="see-also"></a>Siehe auch

- [IEnumFBBlock::Clone](ienumfbblock-clone.md)  
- [IEnumFBBlock::Next](ienumfbblock-next.md)  
- [IEnumFBBlock::Reset](ienumfbblock-reset.md)  
- [IEnumFBBlock::Restrict](ienumfbblock-restrict.md)

