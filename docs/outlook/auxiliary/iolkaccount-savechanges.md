---
title: IOlkAccountSaveChanges
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 8f1ab61e-7d1c-50d5-ae21-8cb4b08d729c
description: Führt ein Commit für Änderungen an das Account-Objekt durch Schreiben der Registrierung gespeichert.
ms.openlocfilehash: ebff8af8af8a7512b577b36a2c31f76f3297a19d
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19791037"
---
# <a name="iolkaccountsavechanges"></a>IOlkAccount::SaveChanges

Führt ein Commit für Änderungen an das Account-Objekt durch Schreiben der Registrierung gespeichert.
  
## <a name="quick-info"></a>QuickInfo

Finden Sie unter [IOlkAccount](iolkaccount.md).
  
```cpp
HRESULT IOlkAccount::SaveChanges (  
    DWORD dwFlags 
); 
```

## <a name="parameters"></a>Parameter

_dwFlags_
  
> [in] Flags, die Verhalten ändern. OLK_ACCOUNT_NO_FLAGS ist der einzige unterstützte Wert.
    
## <a name="return-values"></a>Rückgabewerte

|**[HRESULT]**|**Beschreibung**|
|:-----|:-----|
|S_OK  <br/> |Die Methode erfolgreich war.  <br/> |
|E_ACCT_NOT_FOUND  <br/> |Das angegebene Konto nicht gefunden werden.  <br/> |
|E_OLK_NOT_INITIALIZED  <br/> |Konto-Manager wurde nicht für die Verwendung initialisiert.  <br/> |
   
## <a name="remarks"></a>Hinweise

Verwenden Sie nach dem Ändern des Werts der Eigenschaften von Benutzerkonten mithilfe von [IOlkAccount::SetProp](iolkaccount-setprop.md), **IOlkAccount::SaveChanges** , um derartige Änderungen zu speichern. 
  
## <a name="see-also"></a>Siehe auch

- [Konstanten (Account Management API)](constants-account-management-api.md) 
- [IOlkAccountManager::SaveChanges](iolkaccountmanager-savechanges.md)

