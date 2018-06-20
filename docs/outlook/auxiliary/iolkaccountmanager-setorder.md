---
title: IOlkAccountManagerSetOrder
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: e219adf6-e591-72e6-b9bd-2fc62eb5142d
description: Ändert die Reihenfolge der angegebenen Kategorie von Konten.
ms.openlocfilehash: fcb27404471c9b551320027b0ed6979926ad3d58
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19791095"
---
# <a name="iolkaccountmanagersetorder"></a><span data-ttu-id="86025-103">IOlkAccountManager::SetOrder</span><span class="sxs-lookup"><span data-stu-id="86025-103">IOlkAccountManager::SetOrder</span></span>

<span data-ttu-id="86025-104">Ändert die Reihenfolge der angegebenen Kategorie von Konten.</span><span class="sxs-lookup"><span data-stu-id="86025-104">Modifies the ordering of the specified category of accounts.</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="86025-105">QuickInfo</span><span class="sxs-lookup"><span data-stu-id="86025-105">Quick info</span></span>

<span data-ttu-id="86025-106">See [IOlkAccountManager](iolkaccountmanager.md).</span><span class="sxs-lookup"><span data-stu-id="86025-106">See [IOlkAccountManager](iolkaccountmanager.md).</span></span>
  
```cpp
HRESULT SetOrder(
    const CLSID * pclsidCategory,
    DWORD cAccts,
    DWORD rgAccts[]
);

```

## <a name="parameters"></a><span data-ttu-id="86025-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="86025-107">Parameters</span></span>

<span data-ttu-id="86025-108">_pclsidCategory_</span><span class="sxs-lookup"><span data-stu-id="86025-108">_pclsidCategory_</span></span>
  
> <span data-ttu-id="86025-109">[in] Die Kategorie Klassen-ID für die die Reihenfolge festgelegt.</span><span class="sxs-lookup"><span data-stu-id="86025-109">[in] The category class ID for which to set the order.</span></span> <span data-ttu-id="86025-110">Der Wert muss eine der folgenden sein:</span><span class="sxs-lookup"><span data-stu-id="86025-110">The value must be one of the following:</span></span>
    
   - <span data-ttu-id="86025-111">CLSID_OlkAddressBook</span><span class="sxs-lookup"><span data-stu-id="86025-111">CLSID_OlkAddressBook</span></span>
    
   - <span data-ttu-id="86025-112">CLSID_OlkStore</span><span class="sxs-lookup"><span data-stu-id="86025-112">CLSID_OlkStore</span></span>
    
<span data-ttu-id="86025-113">_cAccts_</span><span class="sxs-lookup"><span data-stu-id="86025-113">_cAccts_</span></span>
  
> <span data-ttu-id="86025-114">[in] Die Anzahl der Konten.</span><span class="sxs-lookup"><span data-stu-id="86025-114">[in] The number of accounts.</span></span>
    
<span data-ttu-id="86025-115">_rgAccts_</span><span class="sxs-lookup"><span data-stu-id="86025-115">_rgAccts_</span></span>
  
> <span data-ttu-id="86025-116">[in] Ein Array von Konto-IDs.</span><span class="sxs-lookup"><span data-stu-id="86025-116">[in] An array of account IDs.</span></span> <span data-ttu-id="86025-117">Die Größe des Arrays ist _cAccts_.</span><span class="sxs-lookup"><span data-stu-id="86025-117">The size of the array is  _cAccts_.</span></span>
    
## <a name="return-values"></a><span data-ttu-id="86025-118">Rückgabewerte</span><span class="sxs-lookup"><span data-stu-id="86025-118">Return values</span></span>

|<span data-ttu-id="86025-119">**[HRESULT]**</span><span class="sxs-lookup"><span data-stu-id="86025-119">**HRESULT**</span></span>|<span data-ttu-id="86025-120">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="86025-120">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="86025-121">S_OK</span><span class="sxs-lookup"><span data-stu-id="86025-121">S_OK</span></span>  <br/> |<span data-ttu-id="86025-122">Der Aufruf war erfolgreich.</span><span class="sxs-lookup"><span data-stu-id="86025-122">The call succeeded.</span></span>  <br/> |
|<span data-ttu-id="86025-123">E_ACCT_WRONG_SORT_ORDER</span><span class="sxs-lookup"><span data-stu-id="86025-123">E_ACCT_WRONG_SORT_ORDER</span></span>  <br/> |<span data-ttu-id="86025-124">Der Sortierreihenfolge bei neuer verfügt über eine unterschiedliche Anzahl von Konten als die alte Sortierreihenfolge.</span><span class="sxs-lookup"><span data-stu-id="86025-124">The new sort order has a different number of accounts than the old sort order.</span></span>  <br/> |
|<span data-ttu-id="86025-125">E_INVALIDARG</span><span class="sxs-lookup"><span data-stu-id="86025-125">E_INVALIDARG</span></span>  <br/> |<span data-ttu-id="86025-126">Mindestens ein Argument ist ungültig.</span><span class="sxs-lookup"><span data-stu-id="86025-126">One or more arguments are invalid.</span></span>  <br/> |
|<span data-ttu-id="86025-127">E_OLK_NOT_INITIALIZED</span><span class="sxs-lookup"><span data-stu-id="86025-127">E_OLK_NOT_INITIALIZED</span></span>  <br/> |<span data-ttu-id="86025-128">Konto-Manager wurde nicht für die Verwendung initialisiert.</span><span class="sxs-lookup"><span data-stu-id="86025-128">The account manager has not been initialized for use.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="86025-129">Hinweise</span><span class="sxs-lookup"><span data-stu-id="86025-129">Remarks</span></span>

<span data-ttu-id="86025-130">Der Aufrufer reserviert Speicher für das Array Zeiger _PrgAccts_ ebenso wie für das Array an welche _PrgAccts_ Punkten.</span><span class="sxs-lookup"><span data-stu-id="86025-130">The caller allocates memory for the array pointer  _prgAccts_ as well as for the array at which  _prgAccts_ points.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="86025-131">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="86025-131">See also</span></span>

- [<span data-ttu-id="86025-132">Konstanten (Account Management API)</span><span class="sxs-lookup"><span data-stu-id="86025-132">Constants (Account management API)</span></span>](constants-account-management-api.md)  
- [<span data-ttu-id="86025-133">IOlkAccountManager::GetOrder</span><span class="sxs-lookup"><span data-stu-id="86025-133">IOlkAccountManager::GetOrder</span></span>](iolkaccountmanager-getorder.md)

