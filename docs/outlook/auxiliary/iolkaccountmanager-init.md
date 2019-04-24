---
title: IOlkAccountManagerInit
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 0e5ffb61-1469-bc91-f237-27d1156179cd
description: Initialisiert den Konto-Manager für die Verwendung.
ms.openlocfilehash: 5a643a4636251afc98750be8acf47cd3bdab3847
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32322036"
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
  
> in Eine [IOlkAccountHelper](iolkaccounthelper.md) -Schnittstelle, die die Konto Hilfsfunktion bereitstellt. 
    
_dwFlags_
  
> [in] Flags, die Verhalten ändern.
    
   - **ACCT_INIT_NO_STORES_CHECK** – verhindert, dass ein Konto (beispielsweise ein IMAP-Konto) mit einem zugeordneten Speicher synchronisiert wird. 
    
   - **ACCT_INIT_NOSYNCH_MAPI_ACCTS** – verhindert, dass MAPI-Dienste mit Konten synchronisiert werden. 
   
   - **ACCT_INIT_NO_NOTIFICATIONS** – verhindert, dass der Konto Manager Broadcastnachrichten abfängt, die für andere Anwendungen vorgesehen sind. 
   
   - **OLK_ACCOUNT_NO_FLAGS** – synchronisiert MAPI-Dienste mit Konten. 
    
## <a name="return-values"></a>Rückgabewerte

|**[HRESULT]**|**Description**|
|:-----|:-----|
|S_OK  <br/> |Der Aufruf war erfolgreich.  <br/> |
|E_OLK_ALREADY_INITIALIZED  <br/> |**Init** wurde bereits aufgerufen.  <br/> |
|E_OLK_REGISTRY  <br/> |Der Konto-Manager konnte nicht auf die erforderlichen Registrierungseinstellungen zugreifen.  <br/> |
   
## <a name="remarks"></a>Bemerkungen

Der Client muss **IOlkAccountManager:: init** aufrufen, um den Kontomanager zu initialisieren, bevor der Konto-Manager zum Zugreifen auf Konten oder zum Einrichten von Benachrichtigungen verwendet wird. Da Outlook MAPI-Dienste automatisch mit Konten beim Start synchronisiert, verwenden Sie **ACCT_INIT_NOSYNCH_MAPI_ACCTS** , es sei denn, es gibt eine bestimmte Ursache für die Synchronisierung. 
  
## <a name="see-also"></a>Siehe auch

- [Konstanten (Account Management API)](constants-account-management-api.md)

