---
title: IOlkAccountManagerSetOrder
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: e219adf6-e591-72e6-b9bd-2fc62eb5142d
description: Ändert die Reihenfolge der angegebenen Kontenkategorie.
ms.openlocfilehash: 29dfe4fd1bda9e323481297167361650c3b3a173
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33422859"
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
  
> in Die Kategorie-Klassen-ID, für die die Reihenfolge festgelegt werden soll. Bei dem Wert muss es sich um Folgendes handeln:
    
   - CLSID_OlkAddressBook
    
   - CLSID_OlkStore
    
_cAccts_
  
> in Die Anzahl der Konten.
    
_rgAccts_
  
> in Ein Array von Konto-IDs. Die Größe des Arrays ist _cAccts_.
    
## <a name="return-values"></a>Rückgabewerte

|**[HRESULT]**|**Description**|
|:-----|:-----|
|S_OK  <br/> |Der Aufruf war erfolgreich.  <br/> |
|E_ACCT_WRONG_SORT_ORDER  <br/> |Die neue Sortierreihenfolge hat eine unterschiedliche Anzahl von Konten als die alte Sortierreihenfolge.  <br/> |
|E_INVALIDARG  <br/> |Mindestens ein Argument ist ungültig.  <br/> |
|E_OLK_NOT_INITIALIZED  <br/> |Konto-Manager wurde nicht für die Verwendung initialisiert.  <br/> |
   
## <a name="remarks"></a>Bemerkungen

Der Aufrufer reserviert Speicher für den Array Zeiger _prgAccts_ sowie für das Array, an dem _prgAccts_ zeigt. 
  
## <a name="see-also"></a>Siehe auch

- [Konstanten (Account Management API)](constants-account-management-api.md)  
- [IOlkAccountManager::GetOrder](iolkaccountmanager-getorder.md)

