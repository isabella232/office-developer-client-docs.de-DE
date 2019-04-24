---
title: IOlkAccountSaveChanges
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 8f1ab61e-7d1c-50d5-ae21-8cb4b08d729c
description: Übergibt Änderungen am Account-Objekt, indem er in den Registrierungsspeicher schreibt.
ms.openlocfilehash: c23cefbbda62de9b7e159e500d95b8db5ff34ef4
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32322260"
---
# <a name="iolkaccountsavechanges"></a>IOlkAccount::SaveChanges

Übergibt Änderungen am Account-Objekt, indem er in den Registrierungsspeicher schreibt.
  
## <a name="quick-info"></a>QuickInfo

Siehe [IOlkAccount](iolkaccount.md).
  
```cpp
HRESULT IOlkAccount::SaveChanges (  
    DWORD dwFlags 
); 
```

## <a name="parameters"></a>Parameter

_dwFlags_
  
> [in] Flags, die Verhalten ändern. OLK_ACCOUNT_NO_FLAGS ist der einzige unterstützte Wert.
    
## <a name="return-values"></a>Rückgabewerte

|**[HRESULT]**|**Description**|
|:-----|:-----|
|S_OK  <br/> |Die Methode war erfolgreich.  <br/> |
|E_ACCT_NOT_FOUND  <br/> |Das angegebene Konto wurde nicht gefunden.  <br/> |
|E_OLK_NOT_INITIALIZED  <br/> |Konto-Manager wurde nicht für die Verwendung initialisiert.  <br/> |
   
## <a name="remarks"></a>Bemerkungen

Nachdem Sie den Wert der Kontoeigenschaften mithilfe von [IOlkAccount:: setprop](iolkaccount-setprop.md)geändert haben, verwenden Sie **IOlkAccount:: SaveChanges** , um solche Änderungen zu speichern. 
  
## <a name="see-also"></a>Siehe auch

- [Konstanten (Account Management API)](constants-account-management-api.md) 
- [IOlkAccountManager::SaveChanges](iolkaccountmanager-savechanges.md)

