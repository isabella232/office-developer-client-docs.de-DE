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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32321234"
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
  
> in Das Property-Tag der abzurufenden Account-Eigenschaft.
    
_pVar_
  
> Out Der Wert der angegebenen Eigenschaft.
    
## <a name="return-values"></a>Rückgabewerte

|**[HRESULT]**|**Description**|
|:-----|:-----|
|S_OK  <br/> |Der Aufruf war erfolgreich.  <br/> |
|E_ACCT_NOT_FOUND  <br/> |Die Eigenschaft wurde für das angegebene Konto nicht gefunden.  <br/> |
|E_INVALIDARG  <br/> |Es wurde ein ungültiges Property-Tag angegeben.  <br/> |
   
## <a name="remarks"></a>Bemerkungen

Nachdem diese Methode zurückgegeben hat, müssen Sie, wenn der Wert der Account-Eigenschaft ein binary-oder String-Typ ist, *pVar* mit [IOlkAccount:: freier Arbeitsspeicher](iolkaccount-freememory.md)freigeben.
  
## <a name="see-also"></a>Siehe auch

- [Konstanten (Account Management API)](constants-account-management-api.md) 
- [IOlkAccount::FreeMemory](iolkaccount-freememory.md)  
- [IOlkAccount::SetProp](iolkaccount-setprop.md)

