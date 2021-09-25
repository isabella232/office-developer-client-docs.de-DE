---
title: IOlkAccountManagerDeleteAccount
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.localizationpriority: medium
ms.assetid: df210364-fe20-8e33-a455-9902f04ec739
description: Löscht das angegebene Konto.
ms.openlocfilehash: fd4c7570241db450e05ed8394d8360ead3c68451
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59552024"
---
# <a name="iolkaccountmanagerdeleteaccount"></a>IOlkAccountManager::DeleteAccount

Löscht das angegebene Konto.
  
## <a name="quick-info"></a>QuickInfo

See [IOlkAccountManager](iolkaccountmanager.md).
  
```cpp
HRESULT IOlkAccountManager::DeleteAccount (  
    DWORD dwAcctID, 
);
```

## <a name="parameters"></a>Parameter

_invalidAcctID_
  
> [in] Die Konto-ID des zu löschenden Kontos.
    
## <a name="return-values"></a>Rückgabewerte

|**[HRESULT]**|**Description**|
|:-----|:-----|
|S_OK  <br/> |Der Aufruf war erfolgreich.  <br/> |
|E_ACCT_NOT_FOUND  <br/> |Das angegebene Konto konnte nicht gefunden werden.  <br/> |
|E_OLK_NOT_INITIALIZED  <br/> |Konto-Manager wurde nicht für die Verwendung initialisiert.  <br/> |
   
## <a name="see-also"></a>Siehe auch

- [Konstanten (Account Management API)](constants-account-management-api.md)  
- [IOlkAccountManager::FindAccount](iolkaccountmanager-findaccount.md)

