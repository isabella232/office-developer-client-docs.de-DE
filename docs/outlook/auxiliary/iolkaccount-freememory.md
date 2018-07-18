---
title: IOlkAccountFreeMemory
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 3b2ee5aa-7639-d86d-447e-50bda54aa3ec
description: Durch die Schnittstelle IOlkAccount Arbeitsspeicher frei.
ms.openlocfilehash: ce3046db29cb2cac7d7ee72a3e4e9125346a4ac4
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19791031"
---
# <a name="iolkaccountfreememory"></a>IOlkAccount::FreeMemory

Durch die Schnittstelle [IOlkAccount](iolkaccount.md) Arbeitsspeicher frei. 
  
## <a name="quick-info"></a>QuickInfo

Finden Sie unter [IOlkAccount](iolkaccount.md).
  
```cpp
HRESULT IOlkAccount::FreeMemory (  
    BYTE *pv, 
); 

```

## <a name="parameters"></a>Parameter

_PV_
  
> [in] Ein Zeiger auf den Speicher freigegeben werden.
    
## <a name="return-values"></a>Rückgabewerte

S_OK zurück, wenn der Aufruf erfolgreich war; andernfalls einen Fehlercode.
  
## <a name="remarks"></a>Anmerkungen

Verwenden Sie diese Methode, um Arbeitsspeicher freizugeben, die von [IOlkAccount::GetProp](iolkaccount-getprop.md) (wenn der Wert der Eigenschaft angegebene Konto einen Typ Binär oder eine Zeichenfolge ist) und [IOlkAccount::GetAccountInfo](iolkaccount-getaccountinfo.md)zugeordnet.
  
## <a name="see-also"></a>Siehe auch

- [IOlkAccount::GetAccountInfo](iolkaccount-getaccountinfo.md)  
- [IOlkAccount::GetProp](iolkaccount-getprop.md)

