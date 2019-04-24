---
title: IOlkAccountGetAccountInfo
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 97f08cde-d6e4-8935-1758-4018a3baf682
description: Ruft den Typ und die Kategorien Informationen für das angegebene Konto ab.
ms.openlocfilehash: 88021537cc7ff4c55759081e6f3619c2a9f10ea3
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32318186"
---
# <a name="iolkaccountgetaccountinfo"></a>IOlkAccount::GetAccountInfo

Ruft den Typ und die Kategorien Informationen für das angegebene Konto ab.
  
## <a name="quick-info"></a>QuickInfo

Siehe [IOlkAccount](iolkaccount.md).
  
```cpp
HRESULT IOlkAccount::GetAccountInfo(  
    CLSID *pclsidType, 
    DWORD *pcCategories, 
    CLSID **prgclsidCategory 
);

```

## <a name="parameters"></a>Parameter

_pclsidType_
  
> Out Der Klassenbezeichner für den Kontotyp. Der Wert muss eine der folgenden sein:
    
   - CLSID_OlkPOP3Account 
    
   - CLSID_OlkIMAP4Account 
    
   - CLSID_OlkMAPIAccount 
    
   - CLSID_OlkHotmailAccount 
    
   - CLSID_OlkLDAPAccount
    
_pcCategories_
  
> Out Die Anzahl der Kategorien in _prgclsidCategory_.
    
_prgclsidCategory_
  
> Out Ein Array von Kategorien, denen dieses Konto zugeordnet ist. Das Array hat die Größe * _pcCategories_. Der Wert jeder Kategorie im Array muss einer der folgenden Werte sein:
    
   - CLSID_OlkMail
    
   - CLSID_OlkAddressBook
    
   - CLSID_OlkStore
    
## <a name="return-values"></a>Rückgabewerte

S_OK zurück, wenn der Aufruf erfolgreich war; andernfalls einen Fehlercode.
  
## <a name="remarks"></a>Bemerkungen

Nachdem diese Methode zurückgegeben wurde, müssen Sie *prgclsidCategory* mit [IOlkAccount:: freier Arbeitsspeicher](iolkaccount-freememory.md)freigeben.
  
**IOlkAccount:: GetAccountInfo** unterstützt die Adressbuch Kategorie für ein Exchange-Konto nicht. Wenn es sich bei dem Konto um ein Exchange-Konto handelt (*pclsidType* ist **CLSID_OlkMAPIAccount** ), und wenn das Konto das Adressbuch implementiert, ruft **IOlkAccount:: GetAccountInfo** nicht **CLSID_OlkAddressBook** als Kategorie in * prgclsidCategory* . 
  
## <a name="see-also"></a>Siehe auch

- [Konstanten (Account Management API)](constants-account-management-api.md)  
- [IOlkAccount::FreeMemory](iolkaccount-freememory.md)

