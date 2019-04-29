---
title: IOlkAccountManagerSaveChanges
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 32a5d4b7-ead7-24e7-58f2-750232263a0d
description: Speichert Änderungen am angegebenen Konto.
ms.openlocfilehash: dbb1dffa1725e96bd2ab635341718ce53738b864
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33429607"
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

_dwAcctID_
  
> in Die zu speichernde Konto-ID. 
    
_dwFlags_
  
> [in] Flags, die Verhalten ändern. OLK_ACCOUNT_NO_FLAGS ist der einzige unterstützte Wert.
    
## <a name="return-values"></a>Rückgabewerte

|**[HRESULT]**|**Description**|
|:-----|:-----|
|S_OK  <br/> |Der Aufruf war erfolgreich.  <br/> |
|E_ACCT_NOT_FOUND  <br/> |Das angegebene Konto wurde nicht gefunden.  <br/> |
|E_OLK_NOT_INITIALIZED  <br/> |Konto-Manager wurde nicht für die Verwendung initialisiert.  <br/> |
   
## <a name="remarks"></a>Bemerkungen

Nachdem Sie den Wert der Kontoeigenschaften mithilfe von [IOlkAccount:: setprop](iolkaccount-setprop.md)geändert haben, verwenden Sie **IOlkAccountManager:: SaveChanges** oder [IOlkAccount:: SaveChanges](iolkaccount-savechanges.md) , um solche Änderungen zu speichern. 
  
## <a name="see-also"></a>Siehe auch

- [Konstanten (Account Management API)](constants-account-management-api.md) 
- [IOlkAccount::SaveChanges](iolkaccount-savechanges.md)

