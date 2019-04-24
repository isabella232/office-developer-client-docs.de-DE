---
title: IOlkAccountFreeMemory
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 3b2ee5aa-7639-d86d-447e-50bda54aa3ec
description: Gibt von der IOlkAccount-Schnittstelle zugewiesene Arbeitsspeicher frei.
ms.openlocfilehash: a7f763ba4fc260a517f8b7df4d3791f4a8fd23b0
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32321336"
---
# <a name="iolkaccountfreememory"></a>IOlkAccount::FreeMemory

Gibt von der [IOlkAccount](iolkaccount.md) -Schnittstelle zugewiesene Arbeitsspeicher frei. 
  
## <a name="quick-info"></a>QuickInfo

Siehe [IOlkAccount](iolkaccount.md).
  
```cpp
HRESULT IOlkAccount::FreeMemory (  
    BYTE *pv, 
); 

```

## <a name="parameters"></a>Parameter

_pv_
  
> in Ein Zeiger auf den zu speichernden Speicher.
    
## <a name="return-values"></a>Rückgabewerte

S_OK zurück, wenn der Aufruf erfolgreich war; andernfalls einen Fehlercode.
  
## <a name="remarks"></a>Bemerkungen

Verwenden Sie diese Methode, um den von [IOlkAccount:: getprop](iolkaccount-getprop.md) reservierten Arbeitsspeicher freizugeben (wenn der Wert der angegebenen Account-Eigenschaft ein binary-oder String-Typ ist) und [IOlkAccount:: GetAccountInfo](iolkaccount-getaccountinfo.md).
  
## <a name="see-also"></a>Siehe auch

- [IOlkAccount::GetAccountInfo](iolkaccount-getaccountinfo.md)  
- [IOlkAccount::GetProp](iolkaccount-getprop.md)

