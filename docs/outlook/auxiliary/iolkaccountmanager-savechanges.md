---
title: IOlkAccountManagerSaveChanges
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.localizationpriority: medium
ms.assetid: 32a5d4b7-ead7-24e7-58f2-750232263a0d
description: Speichert Änderungen am angegebenen Konto.
ms.openlocfilehash: 48df3b07e9b98a277d0dfe7a210f88a8e3dbbc2f
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59551996"
---
# <a name="iolkaccountmanagersavechanges"></a>IOlkAccountManager::SaveChanges

Speichert Änderungen am angegebenen Konto.
  
## <a name="quick-info"></a>QuickInfo

See [IOlkAccountManager](iolkaccountmanager.md).
  
```cpp
HRESULT IOlkAccountManager::SaveChanges (  
    DWORD dwAcctID, 
    DWORD dwFlags 
); 
```

## <a name="parameters"></a>Parameter

_invalidAcctID_
  
> [in] Die zu speichernde Konto-ID. 
    
_Dwflags_
  
> [in] Flags, die Verhalten ändern. OLK_ACCOUNT_NO_FLAGS ist der einzige unterstützte Wert.
    
## <a name="return-values"></a>Rückgabewerte

|**[HRESULT]**|**Description**|
|:-----|:-----|
|S_OK  <br/> |Der Aufruf war erfolgreich.  <br/> |
|E_ACCT_NOT_FOUND  <br/> |Das angegebene Konto konnte nicht gefunden werden.  <br/> |
|E_OLK_NOT_INITIALIZED  <br/> |Konto-Manager wurde nicht für die Verwendung initialisiert.  <br/> |
   
## <a name="remarks"></a>HinwBemerkungeneise

Nachdem Sie den Wert der Kontoeigenschaften mithilfe von [IOlkAccount::SetProp](iolkaccount-setprop.md)geändert haben, verwenden Sie **IOlkAccountManager::SaveChanges** oder [IOlkAccount::SaveChanges,](iolkaccount-savechanges.md) um solche Änderungen zu speichern. 
  
## <a name="see-also"></a>Siehe auch

- [Konstanten (Account Management API)](constants-account-management-api.md) 
- [IOlkAccount::SaveChanges](iolkaccount-savechanges.md)

