---
title: IOlkAccountNotifyNotify
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.localizationpriority: medium
ms.assetid: dbce1c47-1252-ddeb-64ae-d52118e6821f
description: Benachrichtigt den Client über Änderungen am angegebenen Konto.
ms.openlocfilehash: 2e5bd7d6e2f727b7f89bdf6555ad8e123bc8da13
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59557155"
---
# <a name="iolkaccountnotifynotify"></a>IOlkAccountNotify::Notify

Benachrichtigt den Client über Änderungen am angegebenen Konto.
  
## <a name="quick-info"></a>QuickInfo

Siehe [IOlkAccountNotify](iolkaccountnotify.md).
  
```cpp
HRESULT IOlkAccount::Notify(  
    DWORD dwNotify, 
    DWORD dwAcctID, 
    DWORD dwFlags 
);

```

## <a name="parameters"></a>Parameter

_wetterNotify_
  
> [in] Der Typ der Benachrichtigung. Bei dem Wert muss es sich um Folgendes handeln:
    
   - NOTIFY_ACCT_CHANGED 
    
   - NOTIFY_ACCT_CREATED 
    
   - NOTIFY_ACCT_DELETED
    
   - NOTIFY_ACCT_ORDER_CHANGED 
    
   - NOTIFY_ACCT_PREDELETED 
    
 _invalidAcctID_
  
> [in] Die Konto-ID des Kontos, das erstellt, geändert, gelöscht oder vorab gelöscht wurde.
    
 _Dwflags_
  
>  [in] Nicht verwendet. OLK_ACCOUNT_NO_FLAGS ist der einzige unterstützte Wert. 
    
## <a name="return-values"></a>Rückgabewerte

S_OK zurück, wenn der Aufruf erfolgreich war; andernfalls einen Fehlercode.
  
## <a name="see-also"></a>Siehe auch

- [Konstanten (Account Management API)](constants-account-management-api.md)  
- [IOlkAccountManager](iolkaccountmanager.md)

