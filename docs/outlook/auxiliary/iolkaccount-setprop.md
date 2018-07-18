---
title: IOlkAccountSetProp
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 883b1c5d-47dd-a006-b5f1-130691bdd019
description: Legt den Wert der Eigenschaft angegebene Konto.
ms.openlocfilehash: 2bb8a323f5f3399b9eac1cfdf9ac18faddfdb259
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19791056"
---
# <a name="iolkaccountsetprop"></a>IOlkAccount::SetProp

Legt den Wert der Eigenschaft angegebene Konto.
  
## <a name="quick-info"></a>QuickInfo

Finden Sie unter [IOlkAccount](iolkaccount.md).
  
```cpp
HRESULT IOlkAccount::SetProp(  
    DWORD dwProp, 
    ACCT_VARIANT *pVar 
);
```

## <a name="parameters"></a>Parameter

_dwProp_
  
> [in] Die Eigenschaftstag der Konto-Eigenschaft festgelegt.
    
_pVar_
  
> [in] Der Wert der angegebenen Eigenschaft.
    
## <a name="return-values"></a>Rückgabewerte

|**[HRESULT]**|**Beschreibung**|
|:-----|:-----|
|S_OK  <br/> |Methodenaufruf war erfolgreich.  <br/> |
|E_INVALIDARG  <br/> |Eine ungültige Eigenschafts-Tag angegeben wurde.  <br/> |
   
## <a name="remarks"></a>Bemerkungen

Verwenden Sie [IOlkAccount::SaveChanges](iolkaccount-savechanges.md) , um Änderungen auf den Wert der Eigenschaften von Benutzerkonten zu speichern. 
  
## <a name="see-also"></a>Siehe auch

- [Konstanten (Account Management API)](constants-account-management-api.md) 
- [IOlkAccount::GetProp](iolkaccount-getprop.md)

