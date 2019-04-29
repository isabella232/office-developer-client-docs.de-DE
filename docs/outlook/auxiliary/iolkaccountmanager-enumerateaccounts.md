---
title: IOlkAccountManagerEnumerateAccounts
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: dbb8342b-e4e0-f89d-3e14-b4c7049095ef
description: Ruft einen Enumerator für die Konten, die bestimmte Kategorie oder Typ ab.
ms.openlocfilehash: d0d383dee0e76dd6310d01bd1482e307c2374856
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33423048"
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

|**[HRESULT]**|**Description**|
|:-----|:-----|
|S_OK  <br/> |Der Aufruf war erfolgreich.  <br/> |
|E_OLK_NOT_INITIALIZED  <br/> |Konto-Manager wurde nicht für die Verwendung initialisiert.  <br/> |
   
## <a name="remarks"></a>Bemerkungen

Angeben von NULL für die Kategorie gibt einen Enumerator aller Konten des angegebenen Typs zurück. Entsprechend gibt die Angabe von NULL für Typ einen Enumerator aller Konten der angegebenen Kategorie.
  
 **IOlkAccountManager::EnumerateAccounts** unterstützt nicht die Address Book Kategorie für ein Exchange-Konto. Wenn es sich bei dem Konto um ein Exchange-Konto handelt (*pclsidType* ist **CLSID_OlkMAPIAccount** ), und Sie versuchen, Konten aufzuzählen, die das Adressbuch implementieren (*prgclsidCategory* ist **CLSID_OlkAddressBook** ), rufen **Sie IOlkAccountManager:: EnumerateAccounts** gibt das Exchange-Konto nicht im Enumerator *ppEnum* für Konten zurück. 
  
## <a name="see-also"></a>Siehe auch

- [Konstanten (Account Management API)](constants-account-management-api.md)  
- [IOlkEnum](iolkenum.md)

