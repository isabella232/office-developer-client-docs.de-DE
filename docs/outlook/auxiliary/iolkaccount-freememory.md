---
title: IOlkAccountFreeMemory
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.localizationpriority: medium
ms.assetid: 3b2ee5aa-7639-d86d-447e-50bda54aa3ec
description: Gibt von der IOlkAccount-Schnittstelle zugewiesenen Speicher frei.
ms.openlocfilehash: 5c8c0952c3014e3088e30565fdfed377d943f126
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59576558"
---
# <a name="iolkaccountfreememory"></a>IOlkAccount::FreeMemory

Gibt von der [IOlkAccount-Schnittstelle](iolkaccount.md) zugewiesenen Speicher frei. 
  
## <a name="quick-info"></a>QuickInfo

Siehe [IOlkAccount](iolkaccount.md).
  
```cpp
HRESULT IOlkAccount::FreeMemory (  
    BYTE *pv, 
); 

```

## <a name="parameters"></a>Parameter

_pv_
  
> [in] Ein Zeiger auf den freizugebenden Speicher.
    
## <a name="return-values"></a>Rückgabewerte

S_OK zurück, wenn der Aufruf erfolgreich war; andernfalls einen Fehlercode.
  
## <a name="remarks"></a>HinwBemerkungeneise

Verwenden Sie diese Methode, um von [IOlkAccount::GetProp](iolkaccount-getprop.md) zugewiesenen Speicher freizugeben (wenn der Wert der angegebenen Kontoeigenschaft ein Binär- oder Zeichenfolgentyp ist) und [IOlkAccount::GetAccountInfo](iolkaccount-getaccountinfo.md).
  
## <a name="see-also"></a>Siehe auch

- [IOlkAccount::GetAccountInfo](iolkaccount-getaccountinfo.md)  
- [IOlkAccount::GetProp](iolkaccount-getprop.md)

