---
title: IOlkAccountManagerInit
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.localizationpriority: medium
ms.assetid: 0e5ffb61-1469-bc91-f237-27d1156179cd
description: Initialisiert den Konto-Manager für die Verwendung.
ms.openlocfilehash: 44742fadb2c0c450611370d700ced33173387a02
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59552003"
---
# <a name="iolkaccountmanagerinit"></a>IOlkAccountManager::Init

Initialisiert den Konto-Manager für die Verwendung.
  
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
  
> [in] Eine [IOlkAccountHelper-Schnittstelle,](iolkaccounthelper.md) die Kontohilfsfunktionen bereitstellt. 
    
_Dwflags_
  
> [in] Flags, die Verhalten ändern.
    
   - **ACCT_INIT_NO_STORES_CHECK** : Verhindert, dass ein Konto (z. B. ein IMAP-Konto) mit einem zugeordneten Speicher synchronisiert wird. 
    
   - **ACCT_INIT_NOSYNCH_MAPI_ACCTS** : Verhindert, dass MAPI-Dienste mit Konten synchronisiert werden. 
   
   - **ACCT_INIT_NO_NOTIFICATIONS** : Verhindert, dass der Account Manager Übertragungsnachrichten abfangen kann, die für andere Anwendungen vorgesehen sind. 
   
   - **OLK_ACCOUNT_NO_FLAGS** : Synchronisiert MAPI-Dienste mit Konten. 
    
## <a name="return-values"></a>Rückgabewerte

|**[HRESULT]**|**Description**|
|:-----|:-----|
|S_OK  <br/> |Der Aufruf war erfolgreich.  <br/> |
|E_OLK_ALREADY_INITIALIZED  <br/> |**Init** wurde bereits aufgerufen.  <br/> |
|E_OLK_REGISTRY  <br/> |Der Konto-Manager konnte nicht auf die erforderlichen Registrierungseinstellungen zugreifen.  <br/> |
   
## <a name="remarks"></a>HinwBemerkungeneise

Der Client muss **IOlkAccountManager::Init** aufrufen, um den Konto-Manager zu initialisieren, bevor der Konto-Manager für den Zugriff auf Konten oder das Einrichten von Benachrichtigungen verwendet wird. Da Outlook MAPI-Dienste beim Start automatisch mit Konten synchronisiert, verwenden **Sie ACCT_INIT_NOSYNCH_MAPI_ACCTS,** es sei denn, es gibt eine bestimmte Ursache für die Synchronisierung. 
  
## <a name="see-also"></a>Siehe auch

- [Konstanten (Account Management API)](constants-account-management-api.md)

