---
title: IOlkAccountManagerSetOrder
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: e219adf6-e591-72e6-b9bd-2fc62eb5142d
description: Ändert die Reihenfolge der angegebenen Kategorie von Konten.
ms.openlocfilehash: 29dfe4fd1bda9e323481297167361650c3b3a173
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33422859"
---
# <a name="iolkaccountmanagersetorder"></a><span data-ttu-id="8b18a-103">IOlkAccountManager::SetOrder</span><span class="sxs-lookup"><span data-stu-id="8b18a-103">IOlkAccountManager::SetOrder</span></span>

<span data-ttu-id="8b18a-104">Ändert die Reihenfolge der angegebenen Kategorie von Konten.</span><span class="sxs-lookup"><span data-stu-id="8b18a-104">Modifies the ordering of the specified category of accounts.</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="8b18a-105">QuickInfo</span><span class="sxs-lookup"><span data-stu-id="8b18a-105">Quick info</span></span>

<span data-ttu-id="8b18a-106">See [IOlkAccountManager](iolkaccountmanager.md).</span><span class="sxs-lookup"><span data-stu-id="8b18a-106">See [IOlkAccountManager](iolkaccountmanager.md).</span></span>
  
```cpp
HRESULT SetOrder(
    const CLSID * pclsidCategory,
    DWORD cAccts,
    DWORD rgAccts[]
);

```

## <a name="parameters"></a><span data-ttu-id="8b18a-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="8b18a-107">Parameters</span></span>

<span data-ttu-id="8b18a-108">_pclsidCategory_</span><span class="sxs-lookup"><span data-stu-id="8b18a-108">_pclsidCategory_</span></span>
  
> <span data-ttu-id="8b18a-109">[in] Die Kategorieklassen-ID, für die die Reihenfolge festgelegt werden soll.</span><span class="sxs-lookup"><span data-stu-id="8b18a-109">[in] The category class ID for which to set the order.</span></span> <span data-ttu-id="8b18a-110">Bei dem Wert muss es sich um Folgendes handeln:</span><span class="sxs-lookup"><span data-stu-id="8b18a-110">The value must be one of the following:</span></span>
    
   - <span data-ttu-id="8b18a-111">CLSID_OlkAddressBook</span><span class="sxs-lookup"><span data-stu-id="8b18a-111">CLSID_OlkAddressBook</span></span>
    
   - <span data-ttu-id="8b18a-112">CLSID_OlkStore</span><span class="sxs-lookup"><span data-stu-id="8b18a-112">CLSID_OlkStore</span></span>
    
<span data-ttu-id="8b18a-113">_cAccts_</span><span class="sxs-lookup"><span data-stu-id="8b18a-113">_cAccts_</span></span>
  
> <span data-ttu-id="8b18a-114">[in] Die Anzahl der Konten.</span><span class="sxs-lookup"><span data-stu-id="8b18a-114">[in] The number of accounts.</span></span>
    
<span data-ttu-id="8b18a-115">_rgAccts_</span><span class="sxs-lookup"><span data-stu-id="8b18a-115">_rgAccts_</span></span>
  
> <span data-ttu-id="8b18a-116">[in] Ein Array von Konto-IDs.</span><span class="sxs-lookup"><span data-stu-id="8b18a-116">[in] An array of account IDs.</span></span> <span data-ttu-id="8b18a-117">Die Größe des Arrays ist  _cAccts_.</span><span class="sxs-lookup"><span data-stu-id="8b18a-117">The size of the array is  _cAccts_.</span></span>
    
## <a name="return-values"></a><span data-ttu-id="8b18a-118">Rückgabewerte</span><span class="sxs-lookup"><span data-stu-id="8b18a-118">Return values</span></span>

|<span data-ttu-id="8b18a-119">**[HRESULT]**</span><span class="sxs-lookup"><span data-stu-id="8b18a-119">**HRESULT**</span></span>|<span data-ttu-id="8b18a-120">**Description**</span><span class="sxs-lookup"><span data-stu-id="8b18a-120">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="8b18a-121">S_OK</span><span class="sxs-lookup"><span data-stu-id="8b18a-121">S_OK</span></span>  <br/> |<span data-ttu-id="8b18a-122">Der Aufruf war erfolgreich.</span><span class="sxs-lookup"><span data-stu-id="8b18a-122">The call succeeded.</span></span>  <br/> |
|<span data-ttu-id="8b18a-123">E_ACCT_WRONG_SORT_ORDER</span><span class="sxs-lookup"><span data-stu-id="8b18a-123">E_ACCT_WRONG_SORT_ORDER</span></span>  <br/> |<span data-ttu-id="8b18a-124">Die neue Sortierreihenfolge hat eine andere Anzahl von Konten als die alte Sortierreihenfolge.</span><span class="sxs-lookup"><span data-stu-id="8b18a-124">The new sort order has a different number of accounts than the old sort order.</span></span>  <br/> |
|<span data-ttu-id="8b18a-125">E_INVALIDARG</span><span class="sxs-lookup"><span data-stu-id="8b18a-125">E_INVALIDARG</span></span>  <br/> |<span data-ttu-id="8b18a-126">Mindestens ein Argument ist ungültig.</span><span class="sxs-lookup"><span data-stu-id="8b18a-126">One or more arguments are invalid.</span></span>  <br/> |
|<span data-ttu-id="8b18a-127">E_OLK_NOT_INITIALIZED</span><span class="sxs-lookup"><span data-stu-id="8b18a-127">E_OLK_NOT_INITIALIZED</span></span>  <br/> |<span data-ttu-id="8b18a-128">Konto-Manager wurde nicht für die Verwendung initialisiert.</span><span class="sxs-lookup"><span data-stu-id="8b18a-128">The account manager has not been initialized for use.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="8b18a-129">Hinweise</span><span class="sxs-lookup"><span data-stu-id="8b18a-129">Remarks</span></span>

<span data-ttu-id="8b18a-130">Der Aufrufer weist Speicher für den Arrayzeiger _prgAccts_ sowie für das Array zu, auf das _prgAccts verweist._</span><span class="sxs-lookup"><span data-stu-id="8b18a-130">The caller allocates memory for the array pointer  _prgAccts_ as well as for the array at which  _prgAccts_ points.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="8b18a-131">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="8b18a-131">See also</span></span>

- [<span data-ttu-id="8b18a-132">Konstanten (Account Management API)</span><span class="sxs-lookup"><span data-stu-id="8b18a-132">Constants (Account management API)</span></span>](constants-account-management-api.md)  
- [<span data-ttu-id="8b18a-133">IOlkAccountManager::GetOrder</span><span class="sxs-lookup"><span data-stu-id="8b18a-133">IOlkAccountManager::GetOrder</span></span>](iolkaccountmanager-getorder.md)

