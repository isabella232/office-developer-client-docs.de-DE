---
title: IOlkAccountManagerFreeMemory
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: acb67186-ab38-e918-5402-2526307a5bd0
description: Gibt den von der IOlkAccountManager-Schnittstelle zugewiesenen Arbeitsspeicher frei.
ms.openlocfilehash: 3e680e1e26d6c9b12c2dd4a7d48df4dbeae14154
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33408488"
---
# <a name="iolkaccountmanagerfreememory"></a>IOlkAccountManager::FreeMemory

Gibt den von der [IOlkAccountManager-Schnittstelle zugewiesenen Arbeitsspeicher](iolkaccountmanager.md) frei. 
  
## <a name="quick-info"></a>QuickInfo

See [IOlkAccountManager](iolkaccountmanager.md).
  
```cpp
HRESULT IOlkAccountManager::FreeMemory (  
    BYTE *pv, 
);
```

## <a name="parameters"></a>Parameter

_pv_
  
> [in] Ein Zeiger auf den frei zu verwendende Arbeitsspeicher.
    
## <a name="return-values"></a>Rückgabewerte

S_OK zurück, wenn der Aufruf erfolgreich war; andernfalls einen Fehlercode.
  
## <a name="remarks"></a>Hinweise

Verwenden Sie diese Methode, um von [IOlkAccountManager zugewiesenen Arbeitsspeicher frei zu geben::GetOrder](iolkaccountmanager-getorder.md).
  
## <a name="see-also"></a>Siehe auch

- [IOlkAccountManager::GetOrder](iolkaccountmanager-getorder.md)

