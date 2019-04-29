---
title: IOlkAccountManagerFindAccount
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 31004aec-7bd2-6e12-83eb-1a32da121c54
description: Sucht nach einem Eigenschaftswert.
ms.openlocfilehash: d09bce88413f85ee3ccc332c3cb88bb545a0ccaf
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33428802"
---
# <a name="iolkaccountmanagerfindaccount"></a><span data-ttu-id="76931-103">IOlkAccountManager::FindAccount</span><span class="sxs-lookup"><span data-stu-id="76931-103">IOlkAccountManager::FindAccount</span></span>

<span data-ttu-id="76931-104">Sucht nach einem Eigenschaftswert.</span><span class="sxs-lookup"><span data-stu-id="76931-104">Finds an account by property value.</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="76931-105">QuickInfo</span><span class="sxs-lookup"><span data-stu-id="76931-105">Quick info</span></span>

<span data-ttu-id="76931-106">See [IOlkAccountManager](iolkaccountmanager.md).</span><span class="sxs-lookup"><span data-stu-id="76931-106">See [IOlkAccountManager](iolkaccountmanager.md).</span></span>
  
```cpp
HRESULT IOlkAccountManager::FindAccount (  
    DWORD dwProp, 
    ACCT_VARIANT *pVar, 
    IOlkAccount **ppAccount 
);
```

## <a name="parameters"></a><span data-ttu-id="76931-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="76931-107">Parameters</span></span>

<span data-ttu-id="76931-108">_dwProp_</span><span class="sxs-lookup"><span data-stu-id="76931-108">_dwProp_</span></span>
  
> <span data-ttu-id="76931-109">in Die Eigenschaft, nach der gesucht werden soll.</span><span class="sxs-lookup"><span data-stu-id="76931-109">[in] The property to search on.</span></span> <span data-ttu-id="76931-110">Muss [PROP_ACCT_ID](prop_acct_id.md) oder [PROP_ACCT_IS_EXCH](prop_acct_is_exch.md)sein.</span><span class="sxs-lookup"><span data-stu-id="76931-110">Must be [PROP_ACCT_ID](prop_acct_id.md) or [PROP_ACCT_IS_EXCH](prop_acct_is_exch.md).</span></span>
    
<span data-ttu-id="76931-111">_pVar_</span><span class="sxs-lookup"><span data-stu-id="76931-111">_pVar_</span></span>
  
> <span data-ttu-id="76931-112">in Der Wert, der abgeglichen werden soll.</span><span class="sxs-lookup"><span data-stu-id="76931-112">[in] The value to match.</span></span>
    
<span data-ttu-id="76931-113">_ppAccount_</span><span class="sxs-lookup"><span data-stu-id="76931-113">_ppAccount_</span></span>
  
> <span data-ttu-id="76931-114">Out Das Konto wurde gefunden.</span><span class="sxs-lookup"><span data-stu-id="76931-114">[out] The account found.</span></span> <span data-ttu-id="76931-115">Dieses Objekt unterstützt eine [IOlkAccount](iolkaccount.md) -Schnittstelle.</span><span class="sxs-lookup"><span data-stu-id="76931-115">This object supports an [IOlkAccount](iolkaccount.md) interface.</span></span> 
    
## <a name="return-values"></a><span data-ttu-id="76931-116">Rückgabewerte</span><span class="sxs-lookup"><span data-stu-id="76931-116">Return values</span></span>

|<span data-ttu-id="76931-117">**[HRESULT]**</span><span class="sxs-lookup"><span data-stu-id="76931-117">**HRESULT**</span></span>|<span data-ttu-id="76931-118">**Description**</span><span class="sxs-lookup"><span data-stu-id="76931-118">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="76931-119">S_OK</span><span class="sxs-lookup"><span data-stu-id="76931-119">S_OK</span></span>  <br/> |<span data-ttu-id="76931-120">Der Aufruf war erfolgreich.</span><span class="sxs-lookup"><span data-stu-id="76931-120">The call succeeded.</span></span>  <br/> |
|<span data-ttu-id="76931-121">E_ACCT_NOT_FOUND</span><span class="sxs-lookup"><span data-stu-id="76931-121">E_ACCT_NOT_FOUND</span></span>  <br/> |<span data-ttu-id="76931-122">Das angegebene Konto wurde nicht gefunden.</span><span class="sxs-lookup"><span data-stu-id="76931-122">The specified account cannot be found.</span></span>  <br/> |
|<span data-ttu-id="76931-123">E_OLK_NOT_INITIALIZED</span><span class="sxs-lookup"><span data-stu-id="76931-123">E_OLK_NOT_INITIALIZED</span></span>  <br/> |<span data-ttu-id="76931-124">Konto-Manager wurde nicht für die Verwendung initialisiert.</span><span class="sxs-lookup"><span data-stu-id="76931-124">The account manager has not been initialized for use.</span></span>  <br/> |
|<span data-ttu-id="76931-125">E_OLK_PARAM_NOT_SUPPORTED</span><span class="sxs-lookup"><span data-stu-id="76931-125">E_OLK_PARAM_NOT_SUPPORTED</span></span>  <br/> |<span data-ttu-id="76931-126">Mindestens ein Parameter ist ungültig.</span><span class="sxs-lookup"><span data-stu-id="76931-126">One or more parameters are invalid.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="76931-127">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="76931-127">See also</span></span>

- [<span data-ttu-id="76931-128">ACCT_VARIANT</span><span class="sxs-lookup"><span data-stu-id="76931-128">ACCT_VARIANT</span></span>](acct_variant.md)  
- [<span data-ttu-id="76931-129">Konstanten (Account Management API)</span><span class="sxs-lookup"><span data-stu-id="76931-129">Constants (Account management API)</span></span>](constants-account-management-api.md)  
- [<span data-ttu-id="76931-130">IOlkAccountHelper</span><span class="sxs-lookup"><span data-stu-id="76931-130">IOlkAccountHelper</span></span>](iolkaccounthelper.md)

