---
title: IOlkAccountGetProp
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 5725eb52-3a78-897d-f9e3-c5a494fb78c0
description: Ruft den Wert der angegebenen Account-Eigenschaft ab.
ms.openlocfilehash: d24df8cfa9d54bee4614c1f31e12268748b8c986
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33433738"
---
# <a name="iolkaccountgetprop"></a>IOlkAccount::GetProp

Ruft den Wert der angegebenen Account-Eigenschaft ab.
  
## <a name="quick-info"></a>QuickInfo

Siehe [IOlkAccount](iolkaccount.md).
  
```cpp
HRESULT IOlkAccount::GetProp(  
DWORD dwProp, 
ACCT_VARIANT *pVar 
);
```

## <a name="parameters"></a>Parameter

_dwProp_
  
> [in] Das Eigenschaftstag der zu erhaltende Account-Eigenschaft.
    
_pVar_
  
> [out] Der Wert der angegebenen Eigenschaft.
    
## <a name="return-values"></a>Rückgabewerte

|**[HRESULT]**|**Description**|
|:-----|:-----|
|S_OK  <br/> |Der Aufruf war erfolgreich.  <br/> |
|E_ACCT_NOT_FOUND  <br/> |Die Eigenschaft wird für das angegebene Konto nicht gefunden.  <br/> |
|E_INVALIDARG  <br/> |Ein ungültiges Eigenschaftstag wurde angegeben.  <br/> |
   
## <a name="remarks"></a>Hinweise

Nachdem diese Methode zurückgegeben wurde, müssen Sie  *pVar*  mithilfe von [IOlkAccount::FreeMemory](iolkaccount-freememory.md)frei geben, wenn der Wert der Account-Eigenschaft ein Binär- oder Zeichenfolgentyp ist.
  
## <a name="see-also"></a>Siehe auch

- [Konstanten (Account Management API)](constants-account-management-api.md) 
- [IOlkAccount::FreeMemory](iolkaccount-freememory.md)  
- [IOlkAccount::SetProp](iolkaccount-setprop.md)

