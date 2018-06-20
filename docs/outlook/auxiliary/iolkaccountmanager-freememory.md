---
title: IOlkAccountManagerFreeMemory
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: acb67186-ab38-e918-5402-2526307a5bd0
description: Durch die Schnittstelle IOlkAccountManager Arbeitsspeicher frei.
ms.openlocfilehash: 85ba4d0d47eb5c879fa562e3147860533ef59f23
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19791087"
---
# <a name="iolkaccountmanagerfreememory"></a>IOlkAccountManager::FreeMemory

Durch die Schnittstelle [IOlkAccountManager](iolkaccountmanager.md) Arbeitsspeicher frei. 
  
## <a name="quick-info"></a>QuickInfo

See [IOlkAccountManager](iolkaccountmanager.md).
  
```cpp
HRESULT IOlkAccountManager::FreeMemory (  
    BYTE *pv, 
);
```

## <a name="parameters"></a>Parameter

_PV_
  
> [in] Ein Zeiger auf den Speicher frei.
    
## <a name="return-values"></a>Rückgabewerte

S_OK zurück, wenn der Aufruf erfolgreich war; andernfalls einen Fehlercode.
  
## <a name="remarks"></a>Anmerkungen

Verwenden Sie diese Methode, um durch [IOlkAccountManager::GetOrder](iolkaccountmanager-getorder.md)Arbeitsspeicher freizugeben.
  
## <a name="see-also"></a>Siehe auch

- [IOlkAccountManager::GetOrder](iolkaccountmanager-getorder.md)

