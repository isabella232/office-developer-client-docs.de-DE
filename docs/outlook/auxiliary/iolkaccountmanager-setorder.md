---
title: IOlkAccountManagerSetOrder
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: e219adf6-e591-72e6-b9bd-2fc62eb5142d
description: Ändert die Reihenfolge der angegebenen Kontenkategorie.
ms.openlocfilehash: 29dfe4fd1bda9e323481297167361650c3b3a173
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33422859"
---
# <a name="iolkaccountmanagersetorder"></a><span data-ttu-id="b487b-103">IOlkAccountManager::SetOrder</span><span class="sxs-lookup"><span data-stu-id="b487b-103">IOlkAccountManager::SetOrder</span></span>

<span data-ttu-id="b487b-104">Ändert die Reihenfolge der angegebenen Kontenkategorie.</span><span class="sxs-lookup"><span data-stu-id="b487b-104">Modifies the ordering of the specified category of accounts.</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="b487b-105">QuickInfo</span><span class="sxs-lookup"><span data-stu-id="b487b-105">Quick info</span></span>

<span data-ttu-id="b487b-106">See [IOlkAccountManager](iolkaccountmanager.md).</span><span class="sxs-lookup"><span data-stu-id="b487b-106">See [IOlkAccountManager](iolkaccountmanager.md).</span></span>
  
```cpp
HRESULT SetOrder(
    const CLSID * pclsidCategory,
    DWORD cAccts,
    DWORD rgAccts[]
);

```

## <a name="parameters"></a><span data-ttu-id="b487b-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="b487b-107">Parameters</span></span>

<span data-ttu-id="b487b-108">_pclsidCategory_</span><span class="sxs-lookup"><span data-stu-id="b487b-108">_pclsidCategory_</span></span>
  
> <span data-ttu-id="b487b-109">in Die Kategorie-Klassen-ID, für die die Reihenfolge festgelegt werden soll.</span><span class="sxs-lookup"><span data-stu-id="b487b-109">[in] The category class ID for which to set the order.</span></span> <span data-ttu-id="b487b-110">Bei dem Wert muss es sich um Folgendes handeln:</span><span class="sxs-lookup"><span data-stu-id="b487b-110">The value must be one of the following:</span></span>
    
   - <span data-ttu-id="b487b-111">CLSID_OlkAddressBook</span><span class="sxs-lookup"><span data-stu-id="b487b-111">CLSID_OlkAddressBook</span></span>
    
   - <span data-ttu-id="b487b-112">CLSID_OlkStore</span><span class="sxs-lookup"><span data-stu-id="b487b-112">CLSID_OlkStore</span></span>
    
<span data-ttu-id="b487b-113">_cAccts_</span><span class="sxs-lookup"><span data-stu-id="b487b-113">_cAccts_</span></span>
  
> <span data-ttu-id="b487b-114">in Die Anzahl der Konten.</span><span class="sxs-lookup"><span data-stu-id="b487b-114">[in] The number of accounts.</span></span>
    
<span data-ttu-id="b487b-115">_rgAccts_</span><span class="sxs-lookup"><span data-stu-id="b487b-115">_rgAccts_</span></span>
  
> <span data-ttu-id="b487b-116">in Ein Array von Konto-IDs.</span><span class="sxs-lookup"><span data-stu-id="b487b-116">[in] An array of account IDs.</span></span> <span data-ttu-id="b487b-117">Die Größe des Arrays ist _cAccts_.</span><span class="sxs-lookup"><span data-stu-id="b487b-117">The size of the array is  _cAccts_.</span></span>
    
## <a name="return-values"></a><span data-ttu-id="b487b-118">Rückgabewerte</span><span class="sxs-lookup"><span data-stu-id="b487b-118">Return values</span></span>

|<span data-ttu-id="b487b-119">**[HRESULT]**</span><span class="sxs-lookup"><span data-stu-id="b487b-119">**HRESULT**</span></span>|<span data-ttu-id="b487b-120">**Description**</span><span class="sxs-lookup"><span data-stu-id="b487b-120">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="b487b-121">S_OK</span><span class="sxs-lookup"><span data-stu-id="b487b-121">S_OK</span></span>  <br/> |<span data-ttu-id="b487b-122">Der Aufruf war erfolgreich.</span><span class="sxs-lookup"><span data-stu-id="b487b-122">The call succeeded.</span></span>  <br/> |
|<span data-ttu-id="b487b-123">E_ACCT_WRONG_SORT_ORDER</span><span class="sxs-lookup"><span data-stu-id="b487b-123">E_ACCT_WRONG_SORT_ORDER</span></span>  <br/> |<span data-ttu-id="b487b-124">Die neue Sortierreihenfolge hat eine unterschiedliche Anzahl von Konten als die alte Sortierreihenfolge.</span><span class="sxs-lookup"><span data-stu-id="b487b-124">The new sort order has a different number of accounts than the old sort order.</span></span>  <br/> |
|<span data-ttu-id="b487b-125">E_INVALIDARG</span><span class="sxs-lookup"><span data-stu-id="b487b-125">E_INVALIDARG</span></span>  <br/> |<span data-ttu-id="b487b-126">Mindestens ein Argument ist ungültig.</span><span class="sxs-lookup"><span data-stu-id="b487b-126">One or more arguments are invalid.</span></span>  <br/> |
|<span data-ttu-id="b487b-127">E_OLK_NOT_INITIALIZED</span><span class="sxs-lookup"><span data-stu-id="b487b-127">E_OLK_NOT_INITIALIZED</span></span>  <br/> |<span data-ttu-id="b487b-128">Konto-Manager wurde nicht für die Verwendung initialisiert.</span><span class="sxs-lookup"><span data-stu-id="b487b-128">The account manager has not been initialized for use.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="b487b-129">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="b487b-129">Remarks</span></span>

<span data-ttu-id="b487b-130">Der Aufrufer reserviert Speicher für den Array Zeiger _prgAccts_ sowie für das Array, an dem _prgAccts_ zeigt.</span><span class="sxs-lookup"><span data-stu-id="b487b-130">The caller allocates memory for the array pointer  _prgAccts_ as well as for the array at which  _prgAccts_ points.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="b487b-131">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="b487b-131">See also</span></span>

- [<span data-ttu-id="b487b-132">Konstanten (Account Management API)</span><span class="sxs-lookup"><span data-stu-id="b487b-132">Constants (Account management API)</span></span>](constants-account-management-api.md)  
- [<span data-ttu-id="b487b-133">IOlkAccountManager::GetOrder</span><span class="sxs-lookup"><span data-stu-id="b487b-133">IOlkAccountManager::GetOrder</span></span>](iolkaccountmanager-getorder.md)

