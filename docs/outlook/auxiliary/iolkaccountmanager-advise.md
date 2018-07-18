---
title: IOlkAccountManagerAdvise
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: c88f087e-4ff4-0837-186d-b6e761468a4d
description: Registriert einen Client mit dem Kontomanager für Benachrichtigungen bezüglich alle Konten.
ms.openlocfilehash: 1fb697fef44b9ed32888527c3c9e467be69ba4c7
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19791085"
---
# <a name="iolkaccountmanageradvise"></a>IOlkAccountManager::Advise

Registriert einen Client mit dem Kontomanager für Benachrichtigungen bezüglich alle Konten.
  
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
  
> [in] Eine [IOlkAccountNotify](iolkaccountnotify.md) -Schnittstelle, die der Konto-Manager zum Senden von Benachrichtigungen an den Client verwenden. 
    
_pdwCookie_
  
> [out] Ein Cookie, das [IOlkAccountManager::Unadvise](iolkaccountmanager-unadvise.md) verwendet wird, wenn Sie die Registrierung für das Konto zu entfernen. 
    
## <a name="return-values"></a>Rückgabewerte

|**[HRESULT]**|**Beschreibung**|
|:-----|:-----|
|S_OK  <br/> |Der Aufruf war erfolgreich.  <br/> |
|E_INVALIDARG  <br/> |Ein ungültiges Argument wurde bereitgestellt.  <br/> |
|E_OLK_NOT_INITIALIZED  <br/> |Konto-Manager wurde nicht für die Verwendung initialisiert.  <br/> |
   
## <a name="see-also"></a>Siehe auch

- [Konstanten (Account Management API)](constants-account-management-api.md)  
- [IOlkAccountManager::Unadvise](iolkaccountmanager-unadvise.md)

