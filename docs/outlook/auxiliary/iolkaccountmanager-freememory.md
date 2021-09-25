---
title: IOlkAccountManagerFreeMemory
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.localizationpriority: medium
ms.assetid: acb67186-ab38-e918-5402-2526307a5bd0
description: Gibt von der IOlkAccountManager-Schnittstelle zugewiesenen Speicher frei.
ms.openlocfilehash: e51aa8dd165e9cf1d1498386387b422404c7a5d1
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59561929"
---
# <a name="iolkaccountmanagerfreememory"></a>IOlkAccountManager::FreeMemory

Gibt von der [IOlkAccountManager-Schnittstelle](iolkaccountmanager.md) zugewiesenen Speicher frei. 
  
## <a name="quick-info"></a>QuickInfo

See [IOlkAccountManager](iolkaccountmanager.md).
  
```cpp
HRESULT IOlkAccountManager::FreeMemory (  
    BYTE *pv, 
);
```

## <a name="parameters"></a>Parameter

_pv_
  
> [in] Ein Zeiger auf den freizugebenden Speicher.
    
## <a name="return-values"></a>Rückgabewerte

S_OK zurück, wenn der Aufruf erfolgreich war; andernfalls einen Fehlercode.
  
## <a name="remarks"></a>HinwBemerkungeneise

Verwenden Sie diese Methode, um von [IOlkAccountManager](iolkaccountmanager-getorder.md)zugewiesenen Arbeitsspeicher freizugeben::GetOrder .
  
## <a name="see-also"></a>Siehe auch

- [IOlkAccountManager::GetOrder](iolkaccountmanager-getorder.md)

