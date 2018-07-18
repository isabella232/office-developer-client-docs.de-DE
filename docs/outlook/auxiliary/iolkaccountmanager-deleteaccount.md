---
title: IOlkAccountManagerDeleteAccount
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: df210364-fe20-8e33-a455-9902f04ec739
description: Löscht das angegebene Konto.
ms.openlocfilehash: 1c0b246af10dac1af9c61f368d082a92c7b3616a
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19791093"
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

_dwAcctID_
  
> [in] Die Konto-ID des Kontos gelöscht werden soll.
    
## <a name="return-values"></a>Rückgabewerte

|**[HRESULT]**|**Beschreibung**|
|:-----|:-----|
|S_OK  <br/> |Der Aufruf war erfolgreich  <br/> |
|E_ACCT_NOT_FOUND  <br/> |Das angegebene Konto kann nicht gefunden werden.  <br/> |
|E_OLK_NOT_INITIALIZED  <br/> |Konto-Manager wurde nicht für die Verwendung initialisiert.  <br/> |
   
## <a name="see-also"></a>Siehe auch

- [Konstanten (Account Management API)](constants-account-management-api.md)  
- [IOlkAccountManager::FindAccount](iolkaccountmanager-findaccount.md)

