---
title: IOlkAccountManagerFindAccount
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.localizationpriority: medium
ms.assetid: 31004aec-7bd2-6e12-83eb-1a32da121c54
description: Sucht ein Konto anhand des Eigenschaftswerts.
ms.openlocfilehash: 2ec221394364ce2c747e7f9aed4ff5d8373c9b96
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59564505"
---
# <a name="iolkaccountmanagerfindaccount"></a>IOlkAccountManager::FindAccount

Sucht ein Konto anhand des Eigenschaftswerts.
  
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

_für "wetterprop"_
  
> [in] Die Eigenschaft, nach der gesucht werden soll. Muss [PROP_ACCT_ID](prop_acct_id.md) oder [PROP_ACCT_IS_EXCH](prop_acct_is_exch.md)sein.
    
_pVar_
  
> [in] Der zuzuordnende Wert.
    
_ppAccount_
  
> [out] Das gefundene Konto. Dieses Objekt unterstützt eine [IOlkAccount-Schnittstelle.](iolkaccount.md) 
    
## <a name="return-values"></a>Rückgabewerte

|**[HRESULT]**|**Description**|
|:-----|:-----|
|S_OK  <br/> |Der Aufruf war erfolgreich.  <br/> |
|E_ACCT_NOT_FOUND  <br/> |Das angegebene Konto konnte nicht gefunden werden.  <br/> |
|E_OLK_NOT_INITIALIZED  <br/> |Konto-Manager wurde nicht für die Verwendung initialisiert.  <br/> |
|E_OLK_PARAM_NOT_SUPPORTED  <br/> |Mindestens ein Parameter ist ungültig.  <br/> |
   
## <a name="see-also"></a>Siehe auch

- [ACCT_VARIANT](acct_variant.md)  
- [Konstanten (Account Management API)](constants-account-management-api.md)  
- [IOlkAccountHelper](iolkaccounthelper.md)

