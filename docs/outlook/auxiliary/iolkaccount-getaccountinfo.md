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
# <a name="iolkaccountgetaccountinfo"></a><span data-ttu-id="ee552-103">IOlkAccount::GetAccountInfo</span><span class="sxs-lookup"><span data-stu-id="ee552-103">IOlkAccount::GetAccountInfo</span></span>

<span data-ttu-id="ee552-104">Ruft die Typ- und Kategorieninformationen für das angegebene Konto ab.</span><span class="sxs-lookup"><span data-stu-id="ee552-104">Gets the type and categories information for the specified account.</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="ee552-105">QuickInfo</span><span class="sxs-lookup"><span data-stu-id="ee552-105">Quick info</span></span>

<span data-ttu-id="ee552-106">Siehe [IOlkAccount](iolkaccount.md).</span><span class="sxs-lookup"><span data-stu-id="ee552-106">See [IOlkAccount](iolkaccount.md).</span></span>
  
```cpp
HRESULT IOlkAccount::GetAccountInfo(  
    CLSID *pclsidType, 
    DWORD *pcCategories, 
    CLSID **prgclsidCategory 
);

```

## <a name="parameters"></a><span data-ttu-id="ee552-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="ee552-107">Parameters</span></span>

<span data-ttu-id="ee552-108">_pclsidType_</span><span class="sxs-lookup"><span data-stu-id="ee552-108">_pclsidType_</span></span>
  
> <span data-ttu-id="ee552-109">[out] Die Klassen-ID für den Kontotyp.</span><span class="sxs-lookup"><span data-stu-id="ee552-109">[out] The class identifier for the account type.</span></span> <span data-ttu-id="ee552-110">Der Wert muss eine der folgenden sein:</span><span class="sxs-lookup"><span data-stu-id="ee552-110">The value must be one of the following:</span></span>
    
   - <span data-ttu-id="ee552-111">CLSID_OlkPOP3Account</span><span class="sxs-lookup"><span data-stu-id="ee552-111">CLSID_OlkPOP3Account</span></span> 
    
   - <span data-ttu-id="ee552-112">CLSID_OlkIMAP4Account</span><span class="sxs-lookup"><span data-stu-id="ee552-112">CLSID_OlkIMAP4Account</span></span> 
    
   - <span data-ttu-id="ee552-113">CLSID_OlkMAPIAccount</span><span class="sxs-lookup"><span data-stu-id="ee552-113">CLSID_OlkMAPIAccount</span></span> 
    
   - <span data-ttu-id="ee552-114">CLSID_OlkHotmailAccount</span><span class="sxs-lookup"><span data-stu-id="ee552-114">CLSID_OlkHotmailAccount</span></span> 
    
   - <span data-ttu-id="ee552-115">CLSID_OlkLDAPAccount</span><span class="sxs-lookup"><span data-stu-id="ee552-115">CLSID_OlkLDAPAccount</span></span>
    
<span data-ttu-id="ee552-116">_pcCategories_</span><span class="sxs-lookup"><span data-stu-id="ee552-116">_pcCategories_</span></span>
  
> <span data-ttu-id="ee552-117">[out] Die Anzahl der Kategorien in  _prgclsidCategory_.</span><span class="sxs-lookup"><span data-stu-id="ee552-117">[out] The number of categories in  _prgclsidCategory_.</span></span>
    
<span data-ttu-id="ee552-118">_prgclsidCategory_</span><span class="sxs-lookup"><span data-stu-id="ee552-118">_prgclsidCategory_</span></span>
  
> <span data-ttu-id="ee552-119">[out] Ein Array von Kategorien, dem dieses Konto zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="ee552-119">[out] An array of categories that this account is associated with.</span></span> <span data-ttu-id="ee552-120">Das Array hat die Größe \* _pcCategories_.</span><span class="sxs-lookup"><span data-stu-id="ee552-120">The array is of size \* _pcCategories_.</span></span> <span data-ttu-id="ee552-121">Der Wert jeder Kategorie im Array muss einer der folgenden Sein:</span><span class="sxs-lookup"><span data-stu-id="ee552-121">The value of each category in the array must be one of the following:</span></span>
    
   - <span data-ttu-id="ee552-122">CLSID_OlkMail</span><span class="sxs-lookup"><span data-stu-id="ee552-122">CLSID_OlkMail</span></span>
    
   - <span data-ttu-id="ee552-123">CLSID_OlkAddressBook</span><span class="sxs-lookup"><span data-stu-id="ee552-123">CLSID_OlkAddressBook</span></span>
    
   - <span data-ttu-id="ee552-124">CLSID_OlkStore</span><span class="sxs-lookup"><span data-stu-id="ee552-124">CLSID_OlkStore</span></span>
    
## <a name="return-values"></a><span data-ttu-id="ee552-125">Rückgabewerte</span><span class="sxs-lookup"><span data-stu-id="ee552-125">Return values</span></span>

<span data-ttu-id="ee552-126">S_OK zurück, wenn der Aufruf erfolgreich war; andernfalls einen Fehlercode.</span><span class="sxs-lookup"><span data-stu-id="ee552-126">S_OK if the call succeeded; otherwise, an error code.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="ee552-127">Hinweise</span><span class="sxs-lookup"><span data-stu-id="ee552-127">Remarks</span></span>

<span data-ttu-id="ee552-128">Nachdem diese Methode zurückgegeben wurde, müssen Sie *prgclsidCategory* mithilfe von [IOlkAccount::FreeMemory frei machen.](iolkaccount-freememory.md)</span><span class="sxs-lookup"><span data-stu-id="ee552-128">After this method returns, you must free  *prgclsidCategory*  by using [IOlkAccount::FreeMemory](iolkaccount-freememory.md).</span></span>
  
<span data-ttu-id="ee552-129">**IOlkAccount::GetAccountInfo** unterstützt die Adressbuchkategorie für ein Exchange Konto.</span><span class="sxs-lookup"><span data-stu-id="ee552-129">**IOlkAccount::GetAccountInfo** does not support the address book category for an Exchange account.</span></span> <span data-ttu-id="ee552-130">Wenn es sich bei dem Konto um ein Exchange-Konto handelt (*pclsidType* ist **CLSID_OlkMAPIAccount** ), und das Konto das Adressbuch implementiert, gibt der Aufruf von **IOlkAccount::GetAccountInfo** **CLSID_OlkAddressBook** als Kategorie in *prgclsidCategory* nicht zurück.</span><span class="sxs-lookup"><span data-stu-id="ee552-130">If the account is an Exchange account (*pclsidType*  is **CLSID_OlkMAPIAccount** ), and the account implements the address book, calling **IOlkAccount::GetAccountInfo** will not return **CLSID_OlkAddressBook** as a category in  *prgclsidCategory*  .</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="ee552-131">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="ee552-131">See also</span></span>

- [<span data-ttu-id="ee552-132">Konstanten (Account Management API)</span><span class="sxs-lookup"><span data-stu-id="ee552-132">Constants (Account management API)</span></span>](constants-account-management-api.md)  
- [<span data-ttu-id="ee552-133">IOlkAccount::FreeMemory</span><span class="sxs-lookup"><span data-stu-id="ee552-133">IOlkAccount::FreeMemory</span></span>](iolkaccount-freememory.md)

