---
title: IOlkAccountSetProp
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 883b1c5d-47dd-a006-b5f1-130691bdd019
description: Legt den Wert der angegebenen Account-Eigenschaft fest.
ms.openlocfilehash: 94134cee7886177ab840a6caff7d70d65bf9d4cb
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32322253"
---
# <a name="iolkaccountsetprop"></a>IOlkAccount::SetProp

Legt den Wert der angegebenen Account-Eigenschaft fest.
  
## <a name="quick-info"></a>QuickInfo

Siehe [IOlkAccount](iolkaccount.md).
  
```cpp
HRESULT IOlkAccount::SetProp(  
    DWORD dwProp, 
    ACCT_VARIANT *pVar 
);
```

## <a name="parameters"></a>Parameter

_dwProp_
  
> in Das Property-Tag der festzulegenden Account-Eigenschaft.
    
_pVar_
  
> in Der Wert der angegebenen Eigenschaft.
    
## <a name="return-values"></a>Rückgabewerte

|**[HRESULT]**|**Description**|
|:-----|:-----|
|S_OK  <br/> |Der Methodenaufruf war erfolgreich.  <br/> |
|E_INVALIDARG  <br/> |Es wurde ein ungültiges Property-Tag angegeben.  <br/> |
   
## <a name="remarks"></a>Bemerkungen

Verwenden Sie [IOlkAccount:: SaveChanges](iolkaccount-savechanges.md) , um Änderungen am Wert der Kontoeigenschaften zu speichern. 
  
## <a name="see-also"></a>Siehe auch

- [Konstanten (Account Management API)](constants-account-management-api.md) 
- [IOlkAccount::GetProp](iolkaccount-getprop.md)

