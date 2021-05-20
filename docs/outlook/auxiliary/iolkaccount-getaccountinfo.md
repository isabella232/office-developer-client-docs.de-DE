---
title: IOlkAccountGetAccountInfo
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 97f08cde-d6e4-8935-1758-4018a3baf682
description: Ruft die Typ- und Kategorieninformationen für das angegebene Konto ab.
ms.openlocfilehash: 88021537cc7ff4c55759081e6f3619c2a9f10ea3
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33437903"
---
# <a name="iolkaccountgetaccountinfo"></a>IOlkAccount::GetAccountInfo

Ruft die Typ- und Kategorieninformationen für das angegebene Konto ab.
  
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
  
> [out] Die Klassen-ID für den Kontotyp. Der Wert muss eine der folgenden sein:
    
   - CLSID_OlkPOP3Account 
    
   - CLSID_OlkIMAP4Account 
    
   - CLSID_OlkMAPIAccount 
    
   - CLSID_OlkHotmailAccount 
    
   - CLSID_OlkLDAPAccount
    
_pcCategories_
  
> [out] Die Anzahl der Kategorien in  _prgclsidCategory_.
    
_prgclsidCategory_
  
> [out] Ein Array von Kategorien, dem dieses Konto zugeordnet ist. Das Array hat die Größe * _pcCategories_. Der Wert jeder Kategorie im Array muss einer der folgenden Sein:
    
   - CLSID_OlkMail
    
   - CLSID_OlkAddressBook
    
   - CLSID_OlkStore
    
## <a name="return-values"></a>Rückgabewerte

S_OK zurück, wenn der Aufruf erfolgreich war; andernfalls einen Fehlercode.
  
## <a name="remarks"></a>Hinweise

Nachdem diese Methode zurückgegeben wurde, müssen Sie *prgclsidCategory* mithilfe von [IOlkAccount::FreeMemory frei machen.](iolkaccount-freememory.md)
  
**IOlkAccount::GetAccountInfo** unterstützt die Adressbuchkategorie für ein Exchange Konto. Wenn es sich bei dem Konto um ein Exchange-Konto handelt (*pclsidType* ist **CLSID_OlkMAPIAccount** ), und das Konto das Adressbuch implementiert, gibt der Aufruf von **IOlkAccount::GetAccountInfo** **CLSID_OlkAddressBook** als Kategorie in *prgclsidCategory* nicht zurück. 
  
## <a name="see-also"></a>Siehe auch

- [Konstanten (Account Management API)](constants-account-management-api.md)  
- [IOlkAccount::FreeMemory](iolkaccount-freememory.md)

