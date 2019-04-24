---
title: IOlkAccountManagerAdvise
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: c88f087e-4ff4-0837-186d-b6e761468a4d
description: Registriert einen Client mit dem Kontomanager für Benachrichtigungen zu allen Konten.
ms.openlocfilehash: 5460d55d906d382ce40ecd3fd9277cf370295680
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32322197"
---
# <a name="iolkaccountmanageradvise"></a>IOlkAccountManager::Advise

Registriert einen Client mit dem Kontomanager für Benachrichtigungen zu allen Konten.
  
## <a name="quick-info"></a>QuickInfo

See [IOlkAccountManager](iolkaccountmanager.md).
  
```cpp
HRESULT IOlkAccountManager::Advise (  
    IOlkAccountNotify *pNotify, 
    DWORD *pdwCookie 
);
```

## <a name="parameters"></a>Parameter

_pNotify_
  
> in Eine [IOlkAccountNotify](iolkaccountnotify.md) -Schnittstelle, die der Kontomanager zum Senden von Benachrichtigungen an den Client verwendet. 
    
_pdwCookie_
  
> Out Ein Cookie, das [IOlkAccountManager:: Unadvise](iolkaccountmanager-unadvise.md) verwendet, wenn die Registrierung für das Konto entfernt wird. 
    
## <a name="return-values"></a>Rückgabewerte

|**[HRESULT]**|**Description**|
|:-----|:-----|
|S_OK  <br/> |Der Aufruf war erfolgreich.  <br/> |
|E_INVALIDARG  <br/> |Es wurde ein ungültiges Argument bereitgestellt.  <br/> |
|E_OLK_NOT_INITIALIZED  <br/> |Konto-Manager wurde nicht für die Verwendung initialisiert.  <br/> |
   
## <a name="see-also"></a>Siehe auch

- [Konstanten (Account Management API)](constants-account-management-api.md)  
- [IOlkAccountManager::Unadvise](iolkaccountmanager-unadvise.md)

