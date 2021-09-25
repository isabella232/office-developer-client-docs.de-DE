---
title: IEnumFBBlockRestrict
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.localizationpriority: medium
ms.assetid: 887cea55-8f1c-45ec-3100-d03e1213d7c9
description: Schränkt die Aufzählung auf einen angegebenen Zeitraum ein.
ms.openlocfilehash: 0dcb2cb2304323a4d434bb315531190f36e96e96
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59596610"
---
# <a name="ienumfbblockrestrict"></a>IEnumFBBlock::Restrict

Schränkt die Aufzählung auf einen angegebenen Zeitraum ein.
  
## <a name="quick-info"></a>QuickInfo

Siehe [IEnumFBBlock](ienumfbblock.md).
  
```cpp
HRESULT Restrict(  
    FILETIME ftmStart, 
    FILETIME ftmEnd 
);

```

## <a name="parameters"></a>Parameter

_ftmStart_
  
>  [in] Die Startzeit zum Einschränken der Enumeration. 
    
_ftmEnd_
  
> [in] Die Endzeit zum Einschränken der Enumeration.
    
## <a name="return-values"></a>Rückgabewerte

S_OK zurück, wenn der Aufruf erfolgreich war; andernfalls einen Fehlercode.
  
## <a name="remarks"></a>HinwBemerkungeneise

Diese Methode setzt auch die Enumeration zurück.
  
## <a name="see-also"></a>Siehe auch

- [IEnumFBBlock::Clone](ienumfbblock-clone.md)  
- [IEnumFBBlock::Next](ienumfbblock-next.md)  
- [IEnumFBBlock::Reset](ienumfbblock-reset.md)  
- [IEnumFBBlock::Skip](ienumfbblock-skip.md)  
- [Verwenden von relativer Zeit zum Zugriff auf Frei/Gebucht-Daten](how-to-use-relative-time-to-access-free-busy-data.md)

