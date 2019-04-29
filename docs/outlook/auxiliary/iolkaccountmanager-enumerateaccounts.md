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
# <a name="iolkaccountmanagerenumerateaccounts"></a><span data-ttu-id="16f0c-103">IOlkAccountManager::EnumerateAccounts</span><span class="sxs-lookup"><span data-stu-id="16f0c-103">IOlkAccountManager::EnumerateAccounts</span></span>

<span data-ttu-id="16f0c-104">Ruft einen Enumerator für die Konten, die bestimmte Kategorie oder Typ ab.</span><span class="sxs-lookup"><span data-stu-id="16f0c-104">Gets an enumerator for the accounts of the specific category or type.</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="16f0c-105">QuickInfo</span><span class="sxs-lookup"><span data-stu-id="16f0c-105">Quick info</span></span>

<span data-ttu-id="16f0c-106">See [IOlkAccountManager](iolkaccountmanager.md).</span><span class="sxs-lookup"><span data-stu-id="16f0c-106">See [IOlkAccountManager](iolkaccountmanager.md).</span></span>
  
```cpp
HRESULT IOlkAccountManager::EnumerateAccounts (  
    const CLSID *pclsidCategory, 
    const CLSID *pclsidType, 
    DWORD dwFlags, 
    IOlkEnum **ppEnum 
);

```

## <a name="parameters"></a><span data-ttu-id="16f0c-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="16f0c-107">Parameters</span></span>

<span data-ttu-id="16f0c-108">_pclsidCategory_</span><span class="sxs-lookup"><span data-stu-id="16f0c-108">_pclsidCategory_</span></span>
  
> <span data-ttu-id="16f0c-p101">[in] Die Klassen-ID der Kategorie aufgelistet werden. Der Wert muss eine der folgenden sein:</span><span class="sxs-lookup"><span data-stu-id="16f0c-p101">[in] The class identifier of the category to enumerate. The value must be one of the following:</span></span>
    
   - <span data-ttu-id="16f0c-111">CLSID_OlkMail</span><span class="sxs-lookup"><span data-stu-id="16f0c-111">CLSID_OlkMail</span></span> 
    
   -  <span data-ttu-id="16f0c-112">CLSID_OlkAddressBook</span><span class="sxs-lookup"><span data-stu-id="16f0c-112">CLSID_OlkAddressBook</span></span> 
    
   - <span data-ttu-id="16f0c-113">CLSID_OlkStore</span><span class="sxs-lookup"><span data-stu-id="16f0c-113">CLSID_OlkStore</span></span> 
    
<span data-ttu-id="16f0c-114">_pclsidType_</span><span class="sxs-lookup"><span data-stu-id="16f0c-114">_pclsidType_</span></span>
  
> <span data-ttu-id="16f0c-p102">[in] Die Klassen-ID der Kontenart aufgelistet werden. Der Wert muss eine der folgenden sein:</span><span class="sxs-lookup"><span data-stu-id="16f0c-p102">[in] The class identifier of the account type to enumerate. The value must be one of the following:</span></span>
    
   - <span data-ttu-id="16f0c-117">CLSID_OlkPOP3Account</span><span class="sxs-lookup"><span data-stu-id="16f0c-117">CLSID_OlkPOP3Account</span></span>
    
   - <span data-ttu-id="16f0c-118">CLSID_OlkIMAP4Account</span><span class="sxs-lookup"><span data-stu-id="16f0c-118">CLSID_OlkIMAP4Account</span></span>
    
   - <span data-ttu-id="16f0c-119">CLSID_OlkMAPIAccount</span><span class="sxs-lookup"><span data-stu-id="16f0c-119">CLSID_OlkMAPIAccount</span></span>
    
   - <span data-ttu-id="16f0c-120">CLSID_OlkHotmailAccount</span><span class="sxs-lookup"><span data-stu-id="16f0c-120">CLSID_OlkHotmailAccount</span></span>
    
   - <span data-ttu-id="16f0c-121">CLSID_OlkLDAPAccount</span><span class="sxs-lookup"><span data-stu-id="16f0c-121">CLSID_OlkLDAPAccount</span></span>
    
<span data-ttu-id="16f0c-122">_dwFlags_</span><span class="sxs-lookup"><span data-stu-id="16f0c-122">_dwFlags_</span></span>
  
> <span data-ttu-id="16f0c-p103">[in] Flags, die Verhalten ändern. Der einzige unterstützte Wert ist OLK_ACCOUNT_NO_FLAGS.</span><span class="sxs-lookup"><span data-stu-id="16f0c-p103">[in] Flags to modify behavior. The only supported value is OLK_ACCOUNT_NO_FLAGS.</span></span>
    
<span data-ttu-id="16f0c-125">_ppEnum_</span><span class="sxs-lookup"><span data-stu-id="16f0c-125">_ppEnum_</span></span>
  
> <span data-ttu-id="16f0c-126">[out] An enumerator that supports the [IOlkEnum](iolkenum.md) interface.</span><span class="sxs-lookup"><span data-stu-id="16f0c-126">[out] An enumerator that supports the [IOlkEnum](iolkenum.md) interface.</span></span> 
    
## <a name="return-values"></a><span data-ttu-id="16f0c-127">Rückgabewerte</span><span class="sxs-lookup"><span data-stu-id="16f0c-127">Return values</span></span>

|<span data-ttu-id="16f0c-128">**[HRESULT]**</span><span class="sxs-lookup"><span data-stu-id="16f0c-128">**HRESULT**</span></span>|<span data-ttu-id="16f0c-129">**Description**</span><span class="sxs-lookup"><span data-stu-id="16f0c-129">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="16f0c-130">S_OK</span><span class="sxs-lookup"><span data-stu-id="16f0c-130">S_OK</span></span>  <br/> |<span data-ttu-id="16f0c-131">Der Aufruf war erfolgreich.</span><span class="sxs-lookup"><span data-stu-id="16f0c-131">The call succeeded.</span></span>  <br/> |
|<span data-ttu-id="16f0c-132">E_OLK_NOT_INITIALIZED</span><span class="sxs-lookup"><span data-stu-id="16f0c-132">E_OLK_NOT_INITIALIZED</span></span>  <br/> |<span data-ttu-id="16f0c-133">Konto-Manager wurde nicht für die Verwendung initialisiert.</span><span class="sxs-lookup"><span data-stu-id="16f0c-133">The account manager has not been initialized for use.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="16f0c-134">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="16f0c-134">Remarks</span></span>

<span data-ttu-id="16f0c-p104">Angeben von NULL für die Kategorie gibt einen Enumerator aller Konten des angegebenen Typs zurück. Entsprechend gibt die Angabe von NULL für Typ einen Enumerator aller Konten der angegebenen Kategorie.</span><span class="sxs-lookup"><span data-stu-id="16f0c-p104">Specifying NULL for category returns an enumerator of all accounts of the specified type. Similarly, specifying NULL for type returns an enumerator of all accounts of the specified category.</span></span>
  
 <span data-ttu-id="16f0c-137">**IOlkAccountManager::EnumerateAccounts** unterstützt nicht die Address Book Kategorie für ein Exchange-Konto.</span><span class="sxs-lookup"><span data-stu-id="16f0c-137">**IOlkAccountManager::EnumerateAccounts** does not support the address book category for an Exchange account.</span></span> <span data-ttu-id="16f0c-138">Wenn es sich bei dem Konto um ein Exchange-Konto handelt (*pclsidType* ist **CLSID_OlkMAPIAccount** ), und Sie versuchen, Konten aufzuzählen, die das Adressbuch implementieren (*prgclsidCategory* ist **CLSID_OlkAddressBook** ), rufen **Sie IOlkAccountManager:: EnumerateAccounts** gibt das Exchange-Konto nicht im Enumerator *ppEnum* für Konten zurück.</span><span class="sxs-lookup"><span data-stu-id="16f0c-138">If the account is an Exchange account (*pclsidType*  is **CLSID_OlkMAPIAccount** ), and you are trying to enumerate accounts that implement the address book (*prgclsidCategory*  is **CLSID_OlkAddressBook** ), calling **IOlkAccountManager::EnumerateAccounts** will not return the Exchange account in the accounts enumerator  *ppEnum*  .</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="16f0c-139">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="16f0c-139">See also</span></span>

- [<span data-ttu-id="16f0c-140">Konstanten (Account Management API)</span><span class="sxs-lookup"><span data-stu-id="16f0c-140">Constants (Account management API)</span></span>](constants-account-management-api.md)  
- [<span data-ttu-id="16f0c-141">IOlkEnum</span><span class="sxs-lookup"><span data-stu-id="16f0c-141">IOlkEnum</span></span>](iolkenum.md)

