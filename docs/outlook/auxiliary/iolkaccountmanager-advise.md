---
title: IOlkAccountManagerAdvise
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.localizationpriority: medium
ms.assetid: c88f087e-4ff4-0837-186d-b6e761468a4d
description: Registriert einen Client beim Konto-Manager für Benachrichtigungen zu allen Konten.
ms.openlocfilehash: e17bd2b2f07761b8e381913a1de6113dd8133cad
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59625665"
---
# <a name="iolkaccountmanageradvise"></a>IOlkAccountManager::Advise

Registriert einen Client beim Konto-Manager für Benachrichtigungen zu allen Konten.
  
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
  
> [in] Eine [IOlkAccountNotify-Schnittstelle,](iolkaccountnotify.md) die der Konto-Manager zum Senden von Benachrichtigungen an den Client verwendet. 
    
_pdwCookie_
  
> [out] Ein Cookie, das [IOlkAccountManager::Unadvise](iolkaccountmanager-unadvise.md) beim Entfernen der Registrierung für das Konto verwendet. 
    
## <a name="return-values"></a>Rückgabewerte

|**[HRESULT]**|**Description**|
|:-----|:-----|
|S_OK  <br/> |Der Aufruf war erfolgreich.  <br/> |
|E_INVALIDARG  <br/> |Es wurde ein ungültiges Argument angegeben.  <br/> |
|E_OLK_NOT_INITIALIZED  <br/> |Konto-Manager wurde nicht für die Verwendung initialisiert.  <br/> |
   
## <a name="see-also"></a>Siehe auch

- [Konstanten (Account Management API)](constants-account-management-api.md)  
- [IOlkAccountManager::Unadvise](iolkaccountmanager-unadvise.md)

