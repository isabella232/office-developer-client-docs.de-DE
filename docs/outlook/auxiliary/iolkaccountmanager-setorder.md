---
title: IOlkAccountManagerSetOrder
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.localizationpriority: medium
ms.assetid: e219adf6-e591-72e6-b9bd-2fc62eb5142d
description: Ändert die Reihenfolge der angegebenen Kontenkategorie.
ms.openlocfilehash: 5197cc484d0c410367c06d8c28dce9b62c73411d
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59617097"
---
# <a name="iolkaccountmanagersetorder"></a>IOlkAccountManager::SetOrder

Ändert die Reihenfolge der angegebenen Kontenkategorie.
  
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
  
> [in] Die Kategorieklassen-ID, für die die Reihenfolge festgelegt werden soll. Bei dem Wert muss es sich um Folgendes handeln:
    
   - CLSID_OlkAddressBook
    
   - CLSID_OlkStore
    
_cAccts_
  
> [in] Die Anzahl der Konten.
    
_rgAccts_
  
> [in] Ein Array von Konto-IDs. Die Größe des  _Arrays ist cAccts_.
    
## <a name="return-values"></a>Rückgabewerte

|**[HRESULT]**|**Description**|
|:-----|:-----|
|S_OK  <br/> |Der Aufruf war erfolgreich.  <br/> |
|E_ACCT_WRONG_SORT_ORDER  <br/> |Die neue Sortierreihenfolge hat eine andere Anzahl von Konten als die alte Sortierreihenfolge.  <br/> |
|E_INVALIDARG  <br/> |Mindestens ein Argument ist ungültig.  <br/> |
|E_OLK_NOT_INITIALIZED  <br/> |Konto-Manager wurde nicht für die Verwendung initialisiert.  <br/> |
   
## <a name="remarks"></a>Bemerkungen

Der Aufrufer weist Speicher für die  _Arrayzeiger-PrgAccts_ sowie für das Array zu, auf das  _prgAccts_ zeigt. 
  
## <a name="see-also"></a>Siehe auch

- [Konstanten (Account Management API)](constants-account-management-api.md)  
- [IOlkAccountManager::GetOrder](iolkaccountmanager-getorder.md)

