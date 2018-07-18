---
title: IOlkAccountManagerFindAccount
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 31004aec-7bd2-6e12-83eb-1a32da121c54
description: Gibt ein Konto mit Eigenschaftswert ist.
ms.openlocfilehash: a7d016ab7e265e547b33940c16f96979bd5fa87a
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19791092"
---
# <a name="iolkaccountmanagerfindaccount"></a><span data-ttu-id="0ee16-103">IOlkAccountManager::FindAccount</span><span class="sxs-lookup"><span data-stu-id="0ee16-103">IOlkAccountManager::FindAccount</span></span>

<span data-ttu-id="0ee16-104">Gibt ein Konto mit Eigenschaftswert ist.</span><span class="sxs-lookup"><span data-stu-id="0ee16-104">Finds an account by property value.</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="0ee16-105">QuickInfo</span><span class="sxs-lookup"><span data-stu-id="0ee16-105">Quick info</span></span>

<span data-ttu-id="0ee16-106">See [IOlkAccountManager](iolkaccountmanager.md).</span><span class="sxs-lookup"><span data-stu-id="0ee16-106">See [IOlkAccountManager](iolkaccountmanager.md).</span></span>
  
```cpp
HRESULT IOlkAccountManager::FindAccount (  
    DWORD dwProp, 
    ACCT_VARIANT *pVar, 
    IOlkAccount **ppAccount 
);
```

## <a name="parameters"></a><span data-ttu-id="0ee16-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="0ee16-107">Parameters</span></span>

<span data-ttu-id="0ee16-108">_dwProp_</span><span class="sxs-lookup"><span data-stu-id="0ee16-108">_dwProp_</span></span>
  
> <span data-ttu-id="0ee16-109">[in] Die Eigenschaft für die Suche.</span><span class="sxs-lookup"><span data-stu-id="0ee16-109">[in] The property to search on.</span></span> <span data-ttu-id="0ee16-110">[PROP_ACCT_ID](prop_acct_id.md) oder [PROP_ACCT_IS_EXCH](prop_acct_is_exch.md)muss sein.</span><span class="sxs-lookup"><span data-stu-id="0ee16-110">Must be [PROP_ACCT_ID](prop_acct_id.md) or [PROP_ACCT_IS_EXCH](prop_acct_is_exch.md).</span></span>
    
<span data-ttu-id="0ee16-111">_pVar_</span><span class="sxs-lookup"><span data-stu-id="0ee16-111">_pVar_</span></span>
  
> <span data-ttu-id="0ee16-112">[in] Der Wert übereinstimmen.</span><span class="sxs-lookup"><span data-stu-id="0ee16-112">[in] The value to match.</span></span>
    
<span data-ttu-id="0ee16-113">_ppAccount_</span><span class="sxs-lookup"><span data-stu-id="0ee16-113">_ppAccount_</span></span>
  
> <span data-ttu-id="0ee16-114">[out] Das Konto gefunden.</span><span class="sxs-lookup"><span data-stu-id="0ee16-114">[out] The account found.</span></span> <span data-ttu-id="0ee16-115">Dieses Objekt unterstützt eine [IOlkAccount](iolkaccount.md) -Schnittstelle.</span><span class="sxs-lookup"><span data-stu-id="0ee16-115">This object supports an [IOlkAccount](iolkaccount.md) interface.</span></span> 
    
## <a name="return-values"></a><span data-ttu-id="0ee16-116">Rückgabewerte</span><span class="sxs-lookup"><span data-stu-id="0ee16-116">Return values</span></span>

|<span data-ttu-id="0ee16-117">**[HRESULT]**</span><span class="sxs-lookup"><span data-stu-id="0ee16-117">**HRESULT**</span></span>|<span data-ttu-id="0ee16-118">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="0ee16-118">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="0ee16-119">S_OK</span><span class="sxs-lookup"><span data-stu-id="0ee16-119">S_OK</span></span>  <br/> |<span data-ttu-id="0ee16-120">Der Aufruf war erfolgreich.</span><span class="sxs-lookup"><span data-stu-id="0ee16-120">The call succeeded.</span></span>  <br/> |
|<span data-ttu-id="0ee16-121">E_ACCT_NOT_FOUND</span><span class="sxs-lookup"><span data-stu-id="0ee16-121">E_ACCT_NOT_FOUND</span></span>  <br/> |<span data-ttu-id="0ee16-122">Das angegebene Konto kann nicht gefunden werden.</span><span class="sxs-lookup"><span data-stu-id="0ee16-122">The specified account cannot be found.</span></span>  <br/> |
|<span data-ttu-id="0ee16-123">E_OLK_NOT_INITIALIZED</span><span class="sxs-lookup"><span data-stu-id="0ee16-123">E_OLK_NOT_INITIALIZED</span></span>  <br/> |<span data-ttu-id="0ee16-124">Konto-Manager wurde nicht für die Verwendung initialisiert.</span><span class="sxs-lookup"><span data-stu-id="0ee16-124">The account manager has not been initialized for use.</span></span>  <br/> |
|<span data-ttu-id="0ee16-125">E_OLK_PARAM_NOT_SUPPORTED</span><span class="sxs-lookup"><span data-stu-id="0ee16-125">E_OLK_PARAM_NOT_SUPPORTED</span></span>  <br/> |<span data-ttu-id="0ee16-126">Ein oder mehrere Parameter sind ungültig.</span><span class="sxs-lookup"><span data-stu-id="0ee16-126">One or more parameters are invalid.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="0ee16-127">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="0ee16-127">See also</span></span>

- [<span data-ttu-id="0ee16-128">ACCT_VARIANT</span><span class="sxs-lookup"><span data-stu-id="0ee16-128">ACCT_VARIANT</span></span>](acct_variant.md)  
- [<span data-ttu-id="0ee16-129">Konstanten (Account Management API)</span><span class="sxs-lookup"><span data-stu-id="0ee16-129">Constants (Account management API)</span></span>](constants-account-management-api.md)  
- [<span data-ttu-id="0ee16-130">IOlkAccountHelper</span><span class="sxs-lookup"><span data-stu-id="0ee16-130">IOlkAccountHelper</span></span>](iolkaccounthelper.md)

