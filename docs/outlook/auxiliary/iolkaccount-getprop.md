---
title: IOlkAccountGetProp
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.localizationpriority: medium
ms.assetid: 5725eb52-3a78-897d-f9e3-c5a494fb78c0
description: Ruft den Wert der angegebenen Kontoeigenschaft ab.
ms.openlocfilehash: 2ab86eeaf18374a28159c6f0743e55d1664a1b31
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59561950"
---
# <a name="iolkaccountgetprop"></a>IOlkAccount::GetProp

Ruft den Wert der angegebenen Kontoeigenschaft ab.
  
## <a name="quick-info"></a>QuickInfo

Siehe [IOlkAccount](iolkaccount.md).
  
```cpp
HRESULT IOlkAccount::GetProp(  
DWORD dwProp, 
ACCT_VARIANT *pVar 
);
```

## <a name="parameters"></a>Parameter

_für "wetterprop"_
  
> [in] Das Eigenschaftstag der abzurufenden Kontoeigenschaft.
    
_pVar_
  
> [out] Der Wert der angegebenen Eigenschaft.
    
## <a name="return-values"></a>Rückgabewerte

|**[HRESULT]**|**Description**|
|:-----|:-----|
|S_OK  <br/> |Der Aufruf war erfolgreich.  <br/> |
|E_ACCT_NOT_FOUND  <br/> |Die Eigenschaft für das angegebene Konto wurde nicht gefunden.  <br/> |
|E_INVALIDARG  <br/> |Ein ungültiges Eigenschaftstag wurde angegeben.  <br/> |
   
## <a name="remarks"></a>HinwBemerkungeneise

Wenn der Wert der Kontoeigenschaft ein Binär- oder Zeichenfolgentyp ist, müssen Sie nach der Rückgabe dieser Methode  *pVar*  mithilfe von [IOlkAccount::FreeMemory](iolkaccount-freememory.md)freigeben.
  
## <a name="see-also"></a>Siehe auch

- [Konstanten (Account Management API)](constants-account-management-api.md) 
- [IOlkAccount::FreeMemory](iolkaccount-freememory.md)  
- [IOlkAccount::SetProp](iolkaccount-setprop.md)

