---
title: IOlkAccountNotifyNotify
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: dbce1c47-1252-ddeb-64ae-d52118e6821f
description: Benachrichtigt den Client über Änderungen am angegebenen Konto.
ms.openlocfilehash: 269d8a8bd605c9d8a0a4057e87895522d8587ee9
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32321966"
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

_dwNotify_
  
> in Der Benachrichtigungstyp. Bei dem Wert muss es sich um Folgendes handeln:
    
   - NOTIFY_ACCT_CHANGED 
    
   - NOTIFY_ACCT_CREATED 
    
   - NOTIFY_ACCT_DELETED
    
   - NOTIFY_ACCT_ORDER_CHANGED 
    
   - NOTIFY_ACCT_PREDELETED 
    
 _dwAcctID_
  
> in Die Konto-ID des Kontos, das erstellt, geändert, gelöscht oder vorab gelöscht wurde.
    
 _dwFlags_
  
>  in Nicht verwendet. OLK_ACCOUNT_NO_FLAGS ist der einzige unterstützte Wert. 
    
## <a name="return-values"></a>Rückgabewerte

S_OK zurück, wenn der Aufruf erfolgreich war; andernfalls einen Fehlercode.
  
## <a name="see-also"></a>Siehe auch

- [Konstanten (Account Management API)](constants-account-management-api.md)  
- [IOlkAccountManager](iolkaccountmanager.md)

