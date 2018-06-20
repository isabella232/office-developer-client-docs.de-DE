---
title: IOlkAccountManagerFindAccount
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 31004aec-7bd2-6e12-83eb-1a32da121c54
description: Gibt ein Konto mit Eigenschaftswert ist.
ms.openlocfilehash: a7d016ab7e265e547b33940c16f96979bd5fa87a
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19791092"
---
# <a name="iolkaccountmanagerfindaccount"></a>IOlkAccountManager::FindAccount

Gibt ein Konto mit Eigenschaftswert ist.
  
## <a name="quick-info"></a>QuickInfo

See [IOlkAccountManager](iolkaccountmanager.md).
  
```cpp
HRESULT IOlkAccountManager::FindAccount (  
    DWORD dwProp, 
    ACCT_VARIANT *pVar, 
    IOlkAccount **ppAccount 
);
```

## <a name="parameters"></a>Parameter

_dwProp_
  
> [in] Die Eigenschaft für die Suche. [PROP_ACCT_ID](prop_acct_id.md) oder [PROP_ACCT_IS_EXCH](prop_acct_is_exch.md)muss sein.
    
_pVar_
  
> [in] Der Wert übereinstimmen.
    
_ppAccount_
  
> [out] Das Konto gefunden. Dieses Objekt unterstützt eine [IOlkAccount](iolkaccount.md) -Schnittstelle. 
    
## <a name="return-values"></a>Rückgabewerte

|**[HRESULT]**|**Beschreibung**|
|:-----|:-----|
|S_OK  <br/> |Der Aufruf war erfolgreich.  <br/> |
|E_ACCT_NOT_FOUND  <br/> |Das angegebene Konto kann nicht gefunden werden.  <br/> |
|E_OLK_NOT_INITIALIZED  <br/> |Konto-Manager wurde nicht für die Verwendung initialisiert.  <br/> |
|E_OLK_PARAM_NOT_SUPPORTED  <br/> |Ein oder mehrere Parameter sind ungültig.  <br/> |
   
## <a name="see-also"></a>Siehe auch

- [ACCT_VARIANT](acct_variant.md)  
- [Konstanten (Account Management API)](constants-account-management-api.md)  
- [IOlkAccountHelper](iolkaccounthelper.md)

