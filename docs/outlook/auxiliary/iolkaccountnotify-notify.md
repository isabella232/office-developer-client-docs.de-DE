---
title: IOlkAccountNotifyNotify
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: dbce1c47-1252-ddeb-64ae-d52118e6821f
description: Benachrichtigt den Client von Änderungen an das angegebene Konto.
ms.openlocfilehash: ea4cab8cb8571cf5f34637c08935c78c657e5503
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19791112"
---
# <a name="iolkaccountnotifynotify"></a>IOlkAccountNotify::Notify

Benachrichtigt den Client von Änderungen an das angegebene Konto.
  
## <a name="quick-info"></a>QuickInfo

Finden Sie unter [IOlkAccountNotify](iolkaccountnotify.md).
  
```cpp
HRESULT IOlkAccount::Notify(  
    DWORD dwNotify, 
    DWORD dwAcctID, 
    DWORD dwFlags 
);

```

## <a name="parameters"></a>Parameter

_dwNotify_
  
> [in] Der Typ der Benachrichtigung. Der Wert muss eine der folgenden sein:
    
   - NOTIFY_ACCT_CHANGED 
    
   - NOTIFY_ACCT_CREATED 
    
   - NOTIFY_ACCT_DELETED
    
   - NOTIFY_ACCT_ORDER_CHANGED 
    
   - NOTIFY_ACCT_PREDELETED 
    
 _dwAcctID_
  
> [in] Die Konto-ID des Kontos, das geändert, erstellt worden ist, gelöscht oder vor dem gelöscht werden.
    
 _dwFlags_
  
>  [in] Nicht verwendet. OLK_ACCOUNT_NO_FLAGS ist der einzige unterstützte Wert. 
    
## <a name="return-values"></a>Rückgabewerte

S_OK zurück, wenn der Aufruf erfolgreich war; andernfalls einen Fehlercode.
  
## <a name="see-also"></a>Siehe auch

- [Konstanten (Account Management API)](constants-account-management-api.md)  
- [IOlkAccountManager](iolkaccountmanager.md)

