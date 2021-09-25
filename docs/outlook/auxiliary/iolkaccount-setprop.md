---
title: IOlkAccountSetProp
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.localizationpriority: medium
ms.assetid: 883b1c5d-47dd-a006-b5f1-130691bdd019
description: Legt den Wert der angegebenen Kontoeigenschaft fest.
ms.openlocfilehash: 8fd8eb0acc51d457911799e751451e7600202d5d
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59617146"
---
# <a name="iolkaccountsetprop"></a>IOlkAccount::SetProp

Legt den Wert der angegebenen Kontoeigenschaft fest.
  
## <a name="quick-info"></a>QuickInfo

Siehe [IOlkAccount](iolkaccount.md).
  
```cpp
HRESULT IOlkAccount::SetProp(  
    DWORD dwProp, 
    ACCT_VARIANT *pVar 
);
```

## <a name="parameters"></a>Parameter

_für "wetterprop"_
  
> [in] Das Eigenschaftstag der festzulegenden Kontoeigenschaft.
    
_pVar_
  
> [in] Der Wert der angegebenen Eigenschaft.
    
## <a name="return-values"></a>Rückgabewerte

|**[HRESULT]**|**Description**|
|:-----|:-----|
|S_OK  <br/> |Der Methodenaufruf war erfolgreich.  <br/> |
|E_INVALIDARG  <br/> |Es wurde ein ungültiges Eigenschaftstag angegeben.  <br/> |
   
## <a name="remarks"></a>Bemerkungen

Verwenden Sie [IOlkAccount::SaveChanges,](iolkaccount-savechanges.md) um Änderungen am Wert der Kontoeigenschaften zu speichern. 
  
## <a name="see-also"></a>Siehe auch

- [Konstanten (Account Management API)](constants-account-management-api.md) 
- [IOlkAccount::GetProp](iolkaccount-getprop.md)

