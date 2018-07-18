---
title: IOlkAccountManagerEnumerateAccounts
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: dbb8342b-e4e0-f89d-3e14-b4c7049095ef
description: Ruft einen Enumerator für die Konten, die bestimmte Kategorie oder Typ ab.
ms.openlocfilehash: f9b332c0bbc90b1a8f5f944492448055f23c0668
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19791094"
---
# <a name="iolkaccountmanagerenumerateaccounts"></a>IOlkAccountManager::EnumerateAccounts

Ruft einen Enumerator für die Konten, die bestimmte Kategorie oder Typ ab.
  
## <a name="quick-info"></a>QuickInfo

See [IOlkAccountManager](iolkaccountmanager.md).
  
```cpp
HRESULT IOlkAccountManager::EnumerateAccounts (  
    const CLSID *pclsidCategory, 
    const CLSID *pclsidType, 
    DWORD dwFlags, 
    IOlkEnum **ppEnum 
);

```

## <a name="parameters"></a>Parameter

_pclsidCategory_
  
> [in] Die Klassen-ID der Kategorie aufgelistet werden. Der Wert muss eine der folgenden sein:
    
   - CLSID_OlkMail 
    
   -  CLSID_OlkAddressBook 
    
   - CLSID_OlkStore 
    
_pclsidType_
  
> [in] Die Klassen-ID der Kontenart aufgelistet werden. Der Wert muss eine der folgenden sein:
    
   - CLSID_OlkPOP3Account
    
   - CLSID_OlkIMAP4Account
    
   - CLSID_OlkMAPIAccount
    
   - CLSID_OlkHotmailAccount
    
   - CLSID_OlkLDAPAccount
    
_dwFlags_
  
> [in] Flags, die Verhalten ändern. Der einzige unterstützte Wert ist OLK_ACCOUNT_NO_FLAGS.
    
_ppEnum_
  
> [out] An enumerator that supports the [IOlkEnum](iolkenum.md) interface. 
    
## <a name="return-values"></a>Rückgabewerte

|**[HRESULT]**|**Beschreibung**|
|:-----|:-----|
|S_OK  <br/> |Der Aufruf war erfolgreich.  <br/> |
|E_OLK_NOT_INITIALIZED  <br/> |Konto-Manager wurde nicht für die Verwendung initialisiert.  <br/> |
   
## <a name="remarks"></a>Hinweise

Angeben von NULL für die Kategorie gibt einen Enumerator aller Konten des angegebenen Typs zurück. Entsprechend gibt die Angabe von NULL für Typ einen Enumerator aller Konten der angegebenen Kategorie.
  
 **IOlkAccountManager::EnumerateAccounts** unterstützt nicht die Address Book Kategorie für ein Exchange-Konto. Wenn das Konto ein Exchange-Konto ist (*PclsidType* ist **CLSID_OlkMAPIAccount** ), und Sie versuchen, Aufzählen von Konten, die im Adressbuch implementieren (*PrgclsidCategory* ist **CLSID_OlkAddressBook** ), **aufrufen IOlkAccountManager::EnumerateAccounts** des Exchange-Kontos wird nicht in der Konten Enumerator *PpEnum* zurück. 
  
## <a name="see-also"></a>Siehe auch

- [Konstanten (Account Management API)](constants-account-management-api.md)  
- [IOlkEnum](iolkenum.md)

