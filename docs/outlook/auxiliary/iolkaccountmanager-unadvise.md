---
title: IOlkAccountManagerUnadvise
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.localizationpriority: medium
ms.assetid: ea5cbf9f-25cc-9cca-9be0-d2deed576153
description: Hebt die Registrierung eines Clients beim Konto-Manager für Benachrichtigungen für alle Konten auf.
ms.openlocfilehash: cc82aa8bc3ba7f550f1f328c12a68802ef34c29c
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59631237"
---
# <a name="iolkaccountmanagerunadvise"></a>IOlkAccountManager::Unadvise

Hebt die Registrierung eines Clients beim Konto-Manager für Benachrichtigungen für alle Konten auf. 
  
## <a name="quick-info"></a>QuickInfo

See [IOlkAccountManager](iolkaccountmanager.md).
  
```cpp
HRESULT Unadvise(
    DWORD dwCookie
);

```

## <a name="parameters"></a>Parameter

_dwCookie_
  
> [in] Das von [IOlkAccountManager::Advise](iolkaccountmanager-advise.md)zurückgegebene Cookie.
    
## <a name="return-values"></a>Rückgabewerte

|**[HRESULT]**|**Description**|
|:-----|:-----|
|S_OK  <br/> |Der Aufruf war erfolgreich.  <br/> |
|E_INVALIDARG  <br/> |Mindestens ein Argument ist ungültig.  <br/> |
|E_OLK_NOT_INITIALIZED  <br/> |Konto-Manager wurde nicht für die Verwendung initialisiert.  <br/> |
   
## <a name="see-also"></a>Siehe auch

- [Konstanten (Account Management API)](constants-account-management-api.md)  
- [IOlkAccountManager::Advise](iolkaccountmanager-advise.md)

