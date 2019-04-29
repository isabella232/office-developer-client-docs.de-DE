---
title: IOlkAccountManagerFindAccount
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 31004aec-7bd2-6e12-83eb-1a32da121c54
description: Sucht nach einem Eigenschaftswert.
ms.openlocfilehash: d09bce88413f85ee3ccc332c3cb88bb545a0ccaf
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33428802"
---
# <a name="iolkaccountmanagerfindaccount"></a>IOlkAccountManager::FindAccount

Sucht nach einem Eigenschaftswert.
  
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
  
> in Die Eigenschaft, nach der gesucht werden soll. Muss [PROP_ACCT_ID](prop_acct_id.md) oder [PROP_ACCT_IS_EXCH](prop_acct_is_exch.md)sein.
    
_pVar_
  
> in Der Wert, der abgeglichen werden soll.
    
_ppAccount_
  
> Out Das Konto wurde gefunden. Dieses Objekt unterstützt eine [IOlkAccount](iolkaccount.md) -Schnittstelle. 
    
## <a name="return-values"></a>Rückgabewerte

|**[HRESULT]**|**Description**|
|:-----|:-----|
|S_OK  <br/> |Der Aufruf war erfolgreich.  <br/> |
|E_ACCT_NOT_FOUND  <br/> |Das angegebene Konto wurde nicht gefunden.  <br/> |
|E_OLK_NOT_INITIALIZED  <br/> |Konto-Manager wurde nicht für die Verwendung initialisiert.  <br/> |
|E_OLK_PARAM_NOT_SUPPORTED  <br/> |Mindestens ein Parameter ist ungültig.  <br/> |
   
## <a name="see-also"></a>Siehe auch

- [ACCT_VARIANT](acct_variant.md)  
- [Konstanten (Account Management API)](constants-account-management-api.md)  
- [IOlkAccountHelper](iolkaccounthelper.md)

