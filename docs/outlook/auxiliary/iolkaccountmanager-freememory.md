---
title: IOlkAccountManagerFreeMemory
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: acb67186-ab38-e918-5402-2526307a5bd0
description: Gibt von der IOlkAccountManager-Schnittstelle zugewiesene Arbeitsspeicher frei.
ms.openlocfilehash: 3e680e1e26d6c9b12c2dd4a7d48df4dbeae14154
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33408488"
---
# <a name="iolkaccountmanagerfreememory"></a>IOlkAccountManager::FreeMemory

Gibt von der [IOlkAccountManager](iolkaccountmanager.md) -Schnittstelle zugewiesene Arbeitsspeicher frei. 
  
## <a name="quick-info"></a>QuickInfo

See [IOlkAccountManager](iolkaccountmanager.md).
  
```cpp
HRESULT IOlkAccountManager::FreeMemory (  
    BYTE *pv, 
);
```

## <a name="parameters"></a>Parameter

_pv_
  
> in Ein Zeiger auf den zu befreienden Arbeitsspeicher.
    
## <a name="return-values"></a>Rückgabewerte

S_OK zurück, wenn der Aufruf erfolgreich war; andernfalls einen Fehlercode.
  
## <a name="remarks"></a>Bemerkungen

Verwenden Sie diese Methode, um den von [IOlkAccountManager:: GetOrder](iolkaccountmanager-getorder.md)reservierten Arbeitsspeicher freizugeben.
  
## <a name="see-also"></a>Siehe auch

- [IOlkAccountManager::GetOrder](iolkaccountmanager-getorder.md)

