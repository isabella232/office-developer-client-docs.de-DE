---
title: IOlkAccountSaveChanges
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.localizationpriority: medium
ms.assetid: 8f1ab61e-7d1c-50d5-ae21-8cb4b08d729c
description: Führt einen Commit für Änderungen am Kontoobjekt durch Schreiben in den Registrierungsspeicher aus.
ms.openlocfilehash: 2ea5cfaa51ae4fada6d771b8aac774bf309a0335
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59561936"
---
# <a name="iolkaccountsavechanges"></a>IOlkAccount::SaveChanges

Führt einen Commit für Änderungen am Kontoobjekt durch Schreiben in den Registrierungsspeicher aus.
  
## <a name="quick-info"></a>QuickInfo

Siehe [IOlkAccount](iolkaccount.md).
  
```cpp
HRESULT IOlkAccount::SaveChanges (  
    DWORD dwFlags 
); 
```

## <a name="parameters"></a>Parameter

_Dwflags_
  
> [in] Flags, die Verhalten ändern. OLK_ACCOUNT_NO_FLAGS ist der einzige unterstützte Wert.
    
## <a name="return-values"></a>Rückgabewerte

|**[HRESULT]**|**Description**|
|:-----|:-----|
|S_OK  <br/> |Die Methode war erfolgreich.  <br/> |
|E_ACCT_NOT_FOUND  <br/> |Das angegebene Konto kann nicht gefunden werden.  <br/> |
|E_OLK_NOT_INITIALIZED  <br/> |Konto-Manager wurde nicht für die Verwendung initialisiert.  <br/> |
   
## <a name="remarks"></a>HinwBemerkungeneise

Nachdem Sie den Wert der Kontoeigenschaften mithilfe von [IOlkAccount::SetProp](iolkaccount-setprop.md)geändert haben, verwenden Sie **IOlkAccount::SaveChanges,** um solche Änderungen zu speichern. 
  
## <a name="see-also"></a>Siehe auch

- [Konstanten (Account Management API)](constants-account-management-api.md) 
- [IOlkAccountManager::SaveChanges](iolkaccountmanager-savechanges.md)

