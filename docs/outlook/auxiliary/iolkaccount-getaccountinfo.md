---
title: IOlkAccountGetAccountInfo
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.localizationpriority: medium
ms.assetid: 97f08cde-d6e4-8935-1758-4018a3baf682
description: Ruft die Typ- und Kategorieninformationen für das angegebene Konto ab.
ms.openlocfilehash: 7d5abc2126ff3aa9c66f82d1c104c030f9e029a6
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59567942"
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
  
> [out] Der Klassenbezeichner für den Kontotyp. Der Wert muss eine der folgenden sein:
    
   - CLSID_OlkPOP3Account 
    
   - CLSID_OlkIMAP4Account 
    
   - CLSID_OlkMAPIAccount 
    
   - CLSID_OlkHotmailAccount 
    
   - CLSID_OlkLDAPAccount
    
_pcCategories_
  
> [out] Die Anzahl der Kategorien in  _prgclsidCategory_.
    
_prgclsidCategory_
  
> [out] Ein Array von Kategorien, denen dieses Konto zugeordnet ist. Das Array hat die Größe * _pcCategories_. Der Wert jeder Kategorie im Array muss einer der folgenden Werte sein:
    
   - CLSID_OlkMail
    
   - CLSID_OlkAddressBook
    
   - CLSID_OlkStore
    
## <a name="return-values"></a>Rückgabewerte

S_OK zurück, wenn der Aufruf erfolgreich war; andernfalls einen Fehlercode.
  
## <a name="remarks"></a>HinwBemerkungeneise

Nachdem diese Methode zurückgegeben wurde, müssen Sie  *prgclsidCategory*  mithilfe von [IOlkAccount::FreeMemory](iolkaccount-freememory.md)freigeben.
  
**IOlkAccount::GetAccountInfo** unterstützt die Adressbuchkategorie für ein Exchange Konto nicht. Wenn es sich bei dem Konto um ein Exchange Konto handelt (*pclsidType* ist **CLSID_OlkMAPIAccount** ), und das Konto das Adressbuch implementiert, gibt das Aufrufen von **IOlkAccount::GetAccountInfo** **CLSID_OlkAddressBook** nicht als Kategorie in *prgclsidCategory* zurück. 
  
## <a name="see-also"></a>Siehe auch

- [Konstanten (Account Management API)](constants-account-management-api.md)  
- [IOlkAccount::FreeMemory](iolkaccount-freememory.md)

