---
title: IEnumFBBlockRestrict
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 887cea55-8f1c-45ec-3100-d03e1213d7c9
description: Legt eine Beschränkung auf die Enumeration, die einen angegebenen Zeitraum.
ms.openlocfilehash: 6b07fe52a84d6a808ab7400ff3e8982b1cce51ca
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19790948"
---
# <a name="ienumfbblockrestrict"></a>IEnumFBBlock::Restrict

Legt eine Beschränkung auf die Enumeration, die einen angegebenen Zeitraum.
  
## <a name="quick-info"></a>QuickInfo

Finden Sie unter [IEnumFBBlock](ienumfbblock.md).
  
```cpp
HRESULT Restrict(  
    FILETIME ftmStart, 
    FILETIME ftmEnd 
);

```

## <a name="parameters"></a>Parameter

_ftmStart_
  
>  [in] Die Anfangszeit die Enumeration einschränken. 
    
_ftmEnd_
  
> [in] Die Endzeit die Enumeration einschränken.
    
## <a name="return-values"></a>Rückgabewerte

S_OK zurück, wenn der Aufruf erfolgreich war; andernfalls einen Fehlercode.
  
## <a name="remarks"></a>Anmerkungen

Diese Methode wird auch die-Aufzählung.
  
## <a name="see-also"></a>Siehe auch

- [IEnumFBBlock::Clone](ienumfbblock-clone.md)  
- [IEnumFBBlock::Next](ienumfbblock-next.md)  
- [IEnumFBBlock::Reset](ienumfbblock-reset.md)  
- [IEnumFBBlock::Skip](ienumfbblock-skip.md)  
- [Verwenden von relativer Zeit zum Zugriff auf Frei/Gebucht-Daten](how-to-use-relative-time-to-access-free-busy-data.md)

