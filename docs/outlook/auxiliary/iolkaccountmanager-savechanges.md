---
title: IOlkAccountManagerSaveChanges
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 32a5d4b7-ead7-24e7-58f2-750232263a0d
description: Speichert Änderungen an das angegebene Konto.
ms.openlocfilehash: 87b513659b632e88697fb63d1aeccccb77ed9fd1
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19791107"
---
# <a name="iolkaccountmanagersavechanges"></a>IOlkAccountManager::SaveChanges

Speichert Änderungen an das angegebene Konto.
  
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
  
> [in] Die Konto-ID zu speichern. 
    
_dwFlags_
  
> [in] Flags, die Verhalten ändern. OLK_ACCOUNT_NO_FLAGS ist der einzige unterstützte Wert.
    
## <a name="return-values"></a>Rückgabewerte

|**[HRESULT]**|**Beschreibung**|
|:-----|:-----|
|S_OK  <br/> |Der Aufruf war erfolgreich  <br/> |
|E_ACCT_NOT_FOUND  <br/> |Das angegebene Konto kann nicht gefunden werden.  <br/> |
|E_OLK_NOT_INITIALIZED  <br/> |Konto-Manager wurde nicht für die Verwendung initialisiert.  <br/> |
   
## <a name="remarks"></a>Hinweise

Verwenden Sie nach dem Ändern des Werts der Eigenschaften von Benutzerkonten mithilfe von [IOlkAccount::SetProp](iolkaccount-setprop.md), **IOlkAccountManager::SaveChanges** oder [IOlkAccount::SaveChanges](iolkaccount-savechanges.md) , um derartige Änderungen zu speichern. 
  
## <a name="see-also"></a>Siehe auch

- [Konstanten (Account Management API)](constants-account-management-api.md) 
- [IOlkAccount::SaveChanges](iolkaccount-savechanges.md)

