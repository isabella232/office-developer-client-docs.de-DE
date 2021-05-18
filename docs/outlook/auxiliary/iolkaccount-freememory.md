---
title: IOlkAccountFreeMemory
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 3b2ee5aa-7639-d86d-447e-50bda54aa3ec
description: Gibt den von der IOlkAccount-Schnittstelle zugewiesenen Arbeitsspeicher frei.
ms.openlocfilehash: a7f763ba4fc260a517f8b7df4d3791f4a8fd23b0
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33406199"
---
# <a name="iolkaccountfreememory"></a>IOlkAccount::FreeMemory

Gibt den von der [IOlkAccount-Schnittstelle zugewiesenen Arbeitsspeicher](iolkaccount.md) frei. 
  
## <a name="quick-info"></a>QuickInfo

Siehe [IOlkAccount](iolkaccount.md).
  
```cpp
HRESULT IOlkAccount::FreeMemory (  
    BYTE *pv, 
); 

```

## <a name="parameters"></a>Parameter

_pv_
  
> [in] Ein Zeiger auf den speicher, der frei werden soll.
    
## <a name="return-values"></a>Rückgabewerte

S_OK zurück, wenn der Aufruf erfolgreich war; andernfalls einen Fehlercode.
  
## <a name="remarks"></a>Hinweise

Verwenden Sie diese Methode, um von [IOlkAccount::GetProp](iolkaccount-getprop.md) zugewiesenen Arbeitsspeicher frei zu geben (wenn der Wert der angegebenen Kontoeigenschaft ein Binär- oder Zeichenfolgentyp ist) und [IOlkAccount::GetAccountInfo](iolkaccount-getaccountinfo.md).
  
## <a name="see-also"></a>Siehe auch

- [IOlkAccount::GetAccountInfo](iolkaccount-getaccountinfo.md)  
- [IOlkAccount::GetProp](iolkaccount-getprop.md)

