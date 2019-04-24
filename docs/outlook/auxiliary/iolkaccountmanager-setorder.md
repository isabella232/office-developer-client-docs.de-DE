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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32322043"
---
# <a name="iolkaccountmanagersetorder"></a><span data-ttu-id="ea347-103">IOlkAccountManager::SetOrder</span><span class="sxs-lookup"><span data-stu-id="ea347-103">IOlkAccountManager::SetOrder</span></span>

<span data-ttu-id="ea347-104">Ändert die Reihenfolge der angegebenen Kontenkategorie.</span><span class="sxs-lookup"><span data-stu-id="ea347-104">Modifies the ordering of the specified category of accounts.</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="ea347-105">QuickInfo</span><span class="sxs-lookup"><span data-stu-id="ea347-105">Quick info</span></span>

<span data-ttu-id="ea347-106">See [IOlkAccountManager](iolkaccountmanager.md).</span><span class="sxs-lookup"><span data-stu-id="ea347-106">See [IOlkAccountManager](iolkaccountmanager.md).</span></span>
  
```cpp
HRESULT SetOrder(
    const CLSID * pclsidCategory,
    DWORD cAccts,
    DWORD rgAccts[]
);

```

## <a name="parameters"></a><span data-ttu-id="ea347-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="ea347-107">Parameters</span></span>

<span data-ttu-id="ea347-108">_pclsidCategory_</span><span class="sxs-lookup"><span data-stu-id="ea347-108">_pclsidCategory_</span></span>
  
> <span data-ttu-id="ea347-109">in Die Kategorie-Klassen-ID, für die die Reihenfolge festgelegt werden soll.</span><span class="sxs-lookup"><span data-stu-id="ea347-109">[in] The category class ID for which to set the order.</span></span> <span data-ttu-id="ea347-110">Bei dem Wert muss es sich um Folgendes handeln:</span><span class="sxs-lookup"><span data-stu-id="ea347-110">The value must be one of the following:</span></span>
    
   - <span data-ttu-id="ea347-111">CLSID_OlkAddressBook</span><span class="sxs-lookup"><span data-stu-id="ea347-111">CLSID_OlkAddressBook</span></span>
    
   - <span data-ttu-id="ea347-112">CLSID_OlkStore</span><span class="sxs-lookup"><span data-stu-id="ea347-112">CLSID_OlkStore</span></span>
    
<span data-ttu-id="ea347-113">_cAccts_</span><span class="sxs-lookup"><span data-stu-id="ea347-113">_cAccts_</span></span>
  
> <span data-ttu-id="ea347-114">in Die Anzahl der Konten.</span><span class="sxs-lookup"><span data-stu-id="ea347-114">[in] The number of accounts.</span></span>
    
<span data-ttu-id="ea347-115">_rgAccts_</span><span class="sxs-lookup"><span data-stu-id="ea347-115">_rgAccts_</span></span>
  
> <span data-ttu-id="ea347-116">in Ein Array von Konto-IDs.</span><span class="sxs-lookup"><span data-stu-id="ea347-116">[in] An array of account IDs.</span></span> <span data-ttu-id="ea347-117">Die Größe des Arrays ist _cAccts_.</span><span class="sxs-lookup"><span data-stu-id="ea347-117">The size of the array is  _cAccts_.</span></span>
    
## <a name="return-values"></a><span data-ttu-id="ea347-118">Rückgabewerte</span><span class="sxs-lookup"><span data-stu-id="ea347-118">Return values</span></span>

|<span data-ttu-id="ea347-119">**[HRESULT]**</span><span class="sxs-lookup"><span data-stu-id="ea347-119">**HRESULT**</span></span>|<span data-ttu-id="ea347-120">**Description**</span><span class="sxs-lookup"><span data-stu-id="ea347-120">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="ea347-121">S_OK</span><span class="sxs-lookup"><span data-stu-id="ea347-121">S_OK</span></span>  <br/> |<span data-ttu-id="ea347-122">Der Aufruf war erfolgreich.</span><span class="sxs-lookup"><span data-stu-id="ea347-122">The call succeeded.</span></span>  <br/> |
|<span data-ttu-id="ea347-123">E_ACCT_WRONG_SORT_ORDER</span><span class="sxs-lookup"><span data-stu-id="ea347-123">E_ACCT_WRONG_SORT_ORDER</span></span>  <br/> |<span data-ttu-id="ea347-124">Die neue Sortierreihenfolge hat eine unterschiedliche Anzahl von Konten als die alte Sortierreihenfolge.</span><span class="sxs-lookup"><span data-stu-id="ea347-124">The new sort order has a different number of accounts than the old sort order.</span></span>  <br/> |
|<span data-ttu-id="ea347-125">E_INVALIDARG</span><span class="sxs-lookup"><span data-stu-id="ea347-125">E_INVALIDARG</span></span>  <br/> |<span data-ttu-id="ea347-126">Mindestens ein Argument ist ungültig.</span><span class="sxs-lookup"><span data-stu-id="ea347-126">One or more arguments are invalid.</span></span>  <br/> |
|<span data-ttu-id="ea347-127">E_OLK_NOT_INITIALIZED</span><span class="sxs-lookup"><span data-stu-id="ea347-127">E_OLK_NOT_INITIALIZED</span></span>  <br/> |<span data-ttu-id="ea347-128">Konto-Manager wurde nicht für die Verwendung initialisiert.</span><span class="sxs-lookup"><span data-stu-id="ea347-128">The account manager has not been initialized for use.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="ea347-129">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="ea347-129">Remarks</span></span>

<span data-ttu-id="ea347-130">Der Aufrufer reserviert Speicher für den Array Zeiger _prgAccts_ sowie für das Array, an dem _prgAccts_ zeigt.</span><span class="sxs-lookup"><span data-stu-id="ea347-130">The caller allocates memory for the array pointer  _prgAccts_ as well as for the array at which  _prgAccts_ points.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="ea347-131">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="ea347-131">See also</span></span>

- [<span data-ttu-id="ea347-132">Konstanten (Account Management API)</span><span class="sxs-lookup"><span data-stu-id="ea347-132">Constants (Account management API)</span></span>](constants-account-management-api.md)  
- [<span data-ttu-id="ea347-133">IOlkAccountManager::GetOrder</span><span class="sxs-lookup"><span data-stu-id="ea347-133">IOlkAccountManager::GetOrder</span></span>](iolkaccountmanager-getorder.md)

