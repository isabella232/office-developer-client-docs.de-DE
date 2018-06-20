---
title: IOlkAccountGetAccountInfo
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 97f08cde-d6e4-8935-1758-4018a3baf682
description: Der Typ und Kategorien für das angegebene Konto abgerufen.
ms.openlocfilehash: 85f27d1d5f47a372090b208821b52656a56559ad
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19791022"
---
# <a name="iolkaccountgetaccountinfo"></a>IOlkAccount::GetAccountInfo

Der Typ und Kategorien für das angegebene Konto abgerufen.
  
## <a name="quick-info"></a>QuickInfo

Finden Sie unter [IOlkAccount](iolkaccount.md).
  
```cpp
HRESULT IOlkAccount::GetAccountInfo(  
    CLSID *pclsidType, 
    DWORD *pcCategories, 
    CLSID **prgclsidCategory 
);

```

## <a name="parameters"></a>Parameter

_pclsidType_
  
> [out] Die Klassen-ID für die Kontenart an. Der Wert muss eine der folgenden sein:
    
   - CLSID_OlkPOP3Account 
    
   - CLSID_OlkIMAP4Account 
    
   - CLSID_OlkMAPIAccount 
    
   - CLSID_OlkHotmailAccount 
    
   - CLSID_OlkLDAPAccount
    
_pcCategories_
  
> [out] Die Anzahl der Rubriken in _PrgclsidCategory_.
    
_prgclsidCategory_
  
> [out] Ein Array von Kategorien, bei denen dieses Konto zugeordnet ist. Das Array ist Größe * _PcCategories_. Der Wert von jeder Kategorie im Array muss eine der folgenden sein:
    
   - CLSID_OlkMail
    
   - CLSID_OlkAddressBook
    
   - CLSID_OlkStore
    
## <a name="return-values"></a>Rückgabewerte

S_OK zurück, wenn der Aufruf erfolgreich war; andernfalls einen Fehlercode.
  
## <a name="remarks"></a>Anmerkungen

Nachdem diese Methode zurückgegeben wird, müssen Sie *PrgclsidCategory* mithilfe von [IOlkAccount::FreeMemory](iolkaccount-freememory.md)freigeben.
  
**IOlkAccount::GetAccountInfo** unterstützt nicht die Address Book Kategorie für ein Exchange-Konto. Das Konto ist ein Exchange-Konto (*PclsidType* lautet **CLSID_OlkMAPIAccount** ) und das Dienstkonto des Adressbuchs implementiert, aufrufende **IOlkAccount::GetAccountInfo** **CLSID_OlkAddressBook** nicht als einer Kategorie in *zurück PrgclsidCategory* . 
  
## <a name="see-also"></a>Siehe auch

- [Konstanten (Account Management API)](constants-account-management-api.md)  
- [IOlkAccount::FreeMemory](iolkaccount-freememory.md)

