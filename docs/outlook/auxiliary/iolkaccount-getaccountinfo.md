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
# <a name="iolkaccountgetaccountinfo"></a><span data-ttu-id="02ad5-103">IOlkAccount::GetAccountInfo</span><span class="sxs-lookup"><span data-stu-id="02ad5-103">IOlkAccount::GetAccountInfo</span></span>

<span data-ttu-id="02ad5-104">Der Typ und Kategorien für das angegebene Konto abgerufen.</span><span class="sxs-lookup"><span data-stu-id="02ad5-104">Gets the type and categories information for the specified account.</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="02ad5-105">QuickInfo</span><span class="sxs-lookup"><span data-stu-id="02ad5-105">Quick info</span></span>

<span data-ttu-id="02ad5-106">Finden Sie unter [IOlkAccount](iolkaccount.md).</span><span class="sxs-lookup"><span data-stu-id="02ad5-106">See [IOlkAccount](iolkaccount.md).</span></span>
  
```cpp
HRESULT IOlkAccount::GetAccountInfo(  
    CLSID *pclsidType, 
    DWORD *pcCategories, 
    CLSID **prgclsidCategory 
);

```

## <a name="parameters"></a><span data-ttu-id="02ad5-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="02ad5-107">Parameters</span></span>

<span data-ttu-id="02ad5-108">_pclsidType_</span><span class="sxs-lookup"><span data-stu-id="02ad5-108">_pclsidType_</span></span>
  
> <span data-ttu-id="02ad5-109">[out] Die Klassen-ID für die Kontenart an.</span><span class="sxs-lookup"><span data-stu-id="02ad5-109">[out] The class identifier for the account type.</span></span> <span data-ttu-id="02ad5-110">Der Wert muss eine der folgenden sein:</span><span class="sxs-lookup"><span data-stu-id="02ad5-110">The value must be one of the following:</span></span>
    
   - <span data-ttu-id="02ad5-111">CLSID_OlkPOP3Account</span><span class="sxs-lookup"><span data-stu-id="02ad5-111">CLSID_OlkPOP3Account</span></span> 
    
   - <span data-ttu-id="02ad5-112">CLSID_OlkIMAP4Account</span><span class="sxs-lookup"><span data-stu-id="02ad5-112">CLSID_OlkIMAP4Account</span></span> 
    
   - <span data-ttu-id="02ad5-113">CLSID_OlkMAPIAccount</span><span class="sxs-lookup"><span data-stu-id="02ad5-113">CLSID_OlkMAPIAccount</span></span> 
    
   - <span data-ttu-id="02ad5-114">CLSID_OlkHotmailAccount</span><span class="sxs-lookup"><span data-stu-id="02ad5-114">CLSID_OlkHotmailAccount</span></span> 
    
   - <span data-ttu-id="02ad5-115">CLSID_OlkLDAPAccount</span><span class="sxs-lookup"><span data-stu-id="02ad5-115">CLSID_OlkLDAPAccount</span></span>
    
<span data-ttu-id="02ad5-116">_pcCategories_</span><span class="sxs-lookup"><span data-stu-id="02ad5-116">_pcCategories_</span></span>
  
> <span data-ttu-id="02ad5-117">[out] Die Anzahl der Rubriken in _PrgclsidCategory_.</span><span class="sxs-lookup"><span data-stu-id="02ad5-117">[out] The number of categories in  _prgclsidCategory_.</span></span>
    
<span data-ttu-id="02ad5-118">_prgclsidCategory_</span><span class="sxs-lookup"><span data-stu-id="02ad5-118">_prgclsidCategory_</span></span>
  
> <span data-ttu-id="02ad5-119">[out] Ein Array von Kategorien, bei denen dieses Konto zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="02ad5-119">[out] An array of categories that this account is associated with.</span></span> <span data-ttu-id="02ad5-120">Das Array ist Größe \* _PcCategories_.</span><span class="sxs-lookup"><span data-stu-id="02ad5-120">The array is of size \* _pcCategories_.</span></span> <span data-ttu-id="02ad5-121">Der Wert von jeder Kategorie im Array muss eine der folgenden sein:</span><span class="sxs-lookup"><span data-stu-id="02ad5-121">The value of each category in the array must be one of the following:</span></span>
    
   - <span data-ttu-id="02ad5-122">CLSID_OlkMail</span><span class="sxs-lookup"><span data-stu-id="02ad5-122">CLSID_OlkMail</span></span>
    
   - <span data-ttu-id="02ad5-123">CLSID_OlkAddressBook</span><span class="sxs-lookup"><span data-stu-id="02ad5-123">CLSID_OlkAddressBook</span></span>
    
   - <span data-ttu-id="02ad5-124">CLSID_OlkStore</span><span class="sxs-lookup"><span data-stu-id="02ad5-124">CLSID_OlkStore</span></span>
    
## <a name="return-values"></a><span data-ttu-id="02ad5-125">Rückgabewerte</span><span class="sxs-lookup"><span data-stu-id="02ad5-125">Return values</span></span>

<span data-ttu-id="02ad5-126">S_OK zurück, wenn der Aufruf erfolgreich war; andernfalls einen Fehlercode.</span><span class="sxs-lookup"><span data-stu-id="02ad5-126">S_OK if the call succeeded; otherwise, an error code.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="02ad5-127">Anmerkungen</span><span class="sxs-lookup"><span data-stu-id="02ad5-127">Remarks</span></span>

<span data-ttu-id="02ad5-128">Nachdem diese Methode zurückgegeben wird, müssen Sie *PrgclsidCategory* mithilfe von [IOlkAccount::FreeMemory](iolkaccount-freememory.md)freigeben.</span><span class="sxs-lookup"><span data-stu-id="02ad5-128">After this method returns, you must free  *prgclsidCategory*  by using [IOlkAccount::FreeMemory](iolkaccount-freememory.md).</span></span>
  
<span data-ttu-id="02ad5-129">**IOlkAccount::GetAccountInfo** unterstützt nicht die Address Book Kategorie für ein Exchange-Konto.</span><span class="sxs-lookup"><span data-stu-id="02ad5-129">**IOlkAccount::GetAccountInfo** does not support the address book category for an Exchange account.</span></span> <span data-ttu-id="02ad5-130">Das Konto ist ein Exchange-Konto (*PclsidType* lautet **CLSID_OlkMAPIAccount** ) und das Dienstkonto des Adressbuchs implementiert, aufrufende **IOlkAccount::GetAccountInfo** **CLSID_OlkAddressBook** nicht als einer Kategorie in *zurück PrgclsidCategory* .</span><span class="sxs-lookup"><span data-stu-id="02ad5-130">If the account is an Exchange account (*pclsidType*  is **CLSID_OlkMAPIAccount** ), and the account implements the address book, calling **IOlkAccount::GetAccountInfo** will not return **CLSID_OlkAddressBook** as a category in  *prgclsidCategory*  .</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="02ad5-131">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="02ad5-131">See also</span></span>

- [<span data-ttu-id="02ad5-132">Konstanten (Account Management API)</span><span class="sxs-lookup"><span data-stu-id="02ad5-132">Constants (Account management API)</span></span>](constants-account-management-api.md)  
- [<span data-ttu-id="02ad5-133">IOlkAccount::FreeMemory</span><span class="sxs-lookup"><span data-stu-id="02ad5-133">IOlkAccount::FreeMemory</span></span>](iolkaccount-freememory.md)

