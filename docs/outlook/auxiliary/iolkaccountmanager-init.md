---
title: IOlkAccountManagerInit
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 0e5ffb61-1469-bc91-f237-27d1156179cd
description: Initialisiert den Kontomanager für die Verwendung.
ms.openlocfilehash: 621c6a73ab2bcbdff17b87ce15af8b4e0c2e1e24
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19791089"
---
# <a name="iolkaccountmanagerinit"></a>IOlkAccountManager::Init

Initialisiert den Kontomanager für die Verwendung.
  
## <a name="quick-info"></a>QuickInfo

See [IOlkAccountManager](iolkaccountmanager.md).
  
```cpp
HRESULT IOlkAccountManager::Init (  
    IOlkAccountHelper *pAcctHelper, 
    DWORD dwFlags 
);

```

## <a name="parameters"></a>Parameter

_pAcctHelper_
  
> [in] Eine [IOlkAccountHelper](iolkaccounthelper.md) -Schnittstelle, die Konto Hilfsfunktionen bereitstellt. 
    
_dwFlags_
  
> [in] Flags, die Verhalten ändern.
    
   - **ACCT_INIT_NO_STORES_CHECK** – verhindert, dass ein Konto (beispielsweise ein IMAP-Konto) synchronisieren mit einer zugeordneten Informationsspeicher. 
    
   - **ACCT_INIT_NOSYNCH_MAPI_ACCTS** – verhindert, dass MAPI-Dienste nicht mit Konten synchronisiert. 
    
   - **OLK_ACCOUNT_NO_FLAGS** – synchronisiert MAPI-Dienste mit Konten. 
    
## <a name="return-values"></a>Rückgabewerte

|**[HRESULT]**|**Beschreibung**|
|:-----|:-----|
|S_OK  <br/> |Der Aufruf war erfolgreich.  <br/> |
|E_OLK_ALREADY_INITIALIZED  <br/> |**"Init"** wurde bereits aufgerufen.  <br/> |
|E_OLK_REGISTRY  <br/> |Konto-Manager konnte die erforderlichen Registrierungseinträge nicht zugegriffen werden.  <br/> |
   
## <a name="remarks"></a>Hinweise

Der Client muss **IOlkAccountManager::Init** zum Initialisieren des Kontos aufrufen Manager vor der Nutzung des Konto-Managers auf Konten zugreifen oder Benachrichtigungen einrichten. Da MAPI-Dienste mit Konten beim Starten von Outlook automatisch synchronisiert werden, verwenden Sie **ACCT_INIT_NOSYNCH_MAPI_ACCTS** , es sei denn, es eine bestimmte Ursache ist zu synchronisieren. 
  
## <a name="see-also"></a>Siehe auch

- [Konstanten (Account Management API)](constants-account-management-api.md)

