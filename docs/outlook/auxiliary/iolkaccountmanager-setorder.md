---
title: IOlkAccountManagerSetOrder
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: e219adf6-e591-72e6-b9bd-2fc62eb5142d
description: Ändert die Reihenfolge der angegebenen Kategorie von Konten.
ms.openlocfilehash: fcb27404471c9b551320027b0ed6979926ad3d58
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19791095"
---
# <a name="iolkaccountmanagersetorder"></a>IOlkAccountManager::SetOrder

Ändert die Reihenfolge der angegebenen Kategorie von Konten.
  
## <a name="quick-info"></a>QuickInfo

See [IOlkAccountManager](iolkaccountmanager.md).
  
```cpp
HRESULT SetOrder(
    const CLSID * pclsidCategory,
    DWORD cAccts,
    DWORD rgAccts[]
);

```

## <a name="parameters"></a>Parameter

_pclsidCategory_
  
> [in] Die Kategorie Klassen-ID für die die Reihenfolge festgelegt. Der Wert muss eine der folgenden sein:
    
   - CLSID_OlkAddressBook
    
   - CLSID_OlkStore
    
_cAccts_
  
> [in] Die Anzahl der Konten.
    
_rgAccts_
  
> [in] Ein Array von Konto-IDs. Die Größe des Arrays ist _cAccts_.
    
## <a name="return-values"></a>Rückgabewerte

|**[HRESULT]**|**Beschreibung**|
|:-----|:-----|
|S_OK  <br/> |Der Aufruf war erfolgreich.  <br/> |
|E_ACCT_WRONG_SORT_ORDER  <br/> |Der Sortierreihenfolge bei neuer verfügt über eine unterschiedliche Anzahl von Konten als die alte Sortierreihenfolge.  <br/> |
|E_INVALIDARG  <br/> |Mindestens ein Argument ist ungültig.  <br/> |
|E_OLK_NOT_INITIALIZED  <br/> |Konto-Manager wurde nicht für die Verwendung initialisiert.  <br/> |
   
## <a name="remarks"></a>Hinweise

Der Aufrufer reserviert Speicher für das Array Zeiger _PrgAccts_ ebenso wie für das Array an welche _PrgAccts_ Punkten. 
  
## <a name="see-also"></a>Siehe auch

- [Konstanten (Account Management API)](constants-account-management-api.md)  
- [IOlkAccountManager::GetOrder](iolkaccountmanager-getorder.md)

