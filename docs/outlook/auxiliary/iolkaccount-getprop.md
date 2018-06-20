---
title: IOlkAccountGetProp
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 5725eb52-3a78-897d-f9e3-c5a494fb78c0
description: Ruft den Wert der Eigenschaft angegebene Konto.
ms.openlocfilehash: 2c0756f416a209d37eff2209a82c298837f85f3d
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19791039"
---
# <a name="iolkaccountgetprop"></a>IOlkAccount::GetProp

Ruft den Wert der Eigenschaft angegebene Konto.
  
## <a name="quick-info"></a>QuickInfo

Finden Sie unter [IOlkAccount](iolkaccount.md).
  
```cpp
HRESULT IOlkAccount::GetProp(  
DWORD dwProp, 
ACCT_VARIANT *pVar 
);
```

## <a name="parameters"></a>Parameter

_dwProp_
  
> [in] Die Eigenschaftstag der Konto-Eigenschaft abrufen.
    
_pVar_
  
> [out] Der Wert der angegebenen Eigenschaft.
    
## <a name="return-values"></a>Rückgabewerte

|**[HRESULT]**|**Beschreibung**|
|:-----|:-----|
|S_OK  <br/> |Der Aufruf war erfolgreich.  <br/> |
|E_ACCT_NOT_FOUND  <br/> |Die Eigenschaft ist für das angegebene Konto nicht gefunden.  <br/> |
|E_INVALIDARG  <br/> |Ein ungültiger Eigenschafts-Tag es wurde angegeben.  <br/> |
   
## <a name="remarks"></a>Hinweise

Nachdem diese Methode zurückgegeben, wenn der Wert der Eigenschaft Konto einen Typ Binär oder eine Zeichenfolge handelt, müssen Sie *pVar* mithilfe von [IOlkAccount::FreeMemory](iolkaccount-freememory.md)freigeben.
  
## <a name="see-also"></a>Siehe auch

- [Konstanten (Account Management API)](constants-account-management-api.md) 
- [IOlkAccount::FreeMemory](iolkaccount-freememory.md)  
- [IOlkAccount::SetProp](iolkaccount-setprop.md)

