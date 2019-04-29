---
title: IOlkAccountManagerSaveChanges
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 32a5d4b7-ead7-24e7-58f2-750232263a0d
description: Speichert Änderungen am angegebenen Konto.
ms.openlocfilehash: dbb1dffa1725e96bd2ab635341718ce53738b864
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33429607"
---
# <a name="iolkaccountmanagersavechanges"></a><span data-ttu-id="44b15-103">IOlkAccountManager::SaveChanges</span><span class="sxs-lookup"><span data-stu-id="44b15-103">IOlkAccountManager::SaveChanges</span></span>

<span data-ttu-id="44b15-104">Speichert Änderungen am angegebenen Konto.</span><span class="sxs-lookup"><span data-stu-id="44b15-104">Saves changes to the specified account.</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="44b15-105">QuickInfo</span><span class="sxs-lookup"><span data-stu-id="44b15-105">Quick info</span></span>

<span data-ttu-id="44b15-106">See [IOlkAccountManager](iolkaccountmanager.md).</span><span class="sxs-lookup"><span data-stu-id="44b15-106">See [IOlkAccountManager](iolkaccountmanager.md).</span></span>
  
```cpp
HRESULT IOlkAccountManager::SaveChanges (  
    DWORD dwAcctID, 
    DWORD dwFlags 
); 
```

## <a name="parameters"></a><span data-ttu-id="44b15-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="44b15-107">Parameters</span></span>

<span data-ttu-id="44b15-108">_dwAcctID_</span><span class="sxs-lookup"><span data-stu-id="44b15-108">_dwAcctID_</span></span>
  
> <span data-ttu-id="44b15-109">in Die zu speichernde Konto-ID.</span><span class="sxs-lookup"><span data-stu-id="44b15-109">[in] The account ID to save.</span></span> 
    
<span data-ttu-id="44b15-110">_dwFlags_</span><span class="sxs-lookup"><span data-stu-id="44b15-110">_dwFlags_</span></span>
  
> <span data-ttu-id="44b15-111">[in] Flags, die Verhalten ändern.</span><span class="sxs-lookup"><span data-stu-id="44b15-111">[in] Flags to modify behavior.</span></span> <span data-ttu-id="44b15-112">OLK_ACCOUNT_NO_FLAGS ist der einzige unterstützte Wert.</span><span class="sxs-lookup"><span data-stu-id="44b15-112">OLK_ACCOUNT_NO_FLAGS is the only supported value.</span></span>
    
## <a name="return-values"></a><span data-ttu-id="44b15-113">Rückgabewerte</span><span class="sxs-lookup"><span data-stu-id="44b15-113">Return values</span></span>

|<span data-ttu-id="44b15-114">**[HRESULT]**</span><span class="sxs-lookup"><span data-stu-id="44b15-114">**HRESULT**</span></span>|<span data-ttu-id="44b15-115">**Description**</span><span class="sxs-lookup"><span data-stu-id="44b15-115">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="44b15-116">S_OK</span><span class="sxs-lookup"><span data-stu-id="44b15-116">S_OK</span></span>  <br/> |<span data-ttu-id="44b15-117">Der Aufruf war erfolgreich.</span><span class="sxs-lookup"><span data-stu-id="44b15-117">The call succeeded</span></span>  <br/> |
|<span data-ttu-id="44b15-118">E_ACCT_NOT_FOUND</span><span class="sxs-lookup"><span data-stu-id="44b15-118">E_ACCT_NOT_FOUND</span></span>  <br/> |<span data-ttu-id="44b15-119">Das angegebene Konto wurde nicht gefunden.</span><span class="sxs-lookup"><span data-stu-id="44b15-119">The specified account cannot be found.</span></span>  <br/> |
|<span data-ttu-id="44b15-120">E_OLK_NOT_INITIALIZED</span><span class="sxs-lookup"><span data-stu-id="44b15-120">E_OLK_NOT_INITIALIZED</span></span>  <br/> |<span data-ttu-id="44b15-121">Konto-Manager wurde nicht für die Verwendung initialisiert.</span><span class="sxs-lookup"><span data-stu-id="44b15-121">The account manager has not been initialized for use.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="44b15-122">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="44b15-122">Remarks</span></span>

<span data-ttu-id="44b15-123">Nachdem Sie den Wert der Kontoeigenschaften mithilfe von [IOlkAccount:: setprop](iolkaccount-setprop.md)geändert haben, verwenden Sie **IOlkAccountManager:: SaveChanges** oder [IOlkAccount:: SaveChanges](iolkaccount-savechanges.md) , um solche Änderungen zu speichern.</span><span class="sxs-lookup"><span data-stu-id="44b15-123">After changing the value of account properties by using [IOlkAccount::SetProp](iolkaccount-setprop.md), use **IOlkAccountManager::SaveChanges** or [IOlkAccount::SaveChanges](iolkaccount-savechanges.md) to save such changes.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="44b15-124">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="44b15-124">See also</span></span>

- [<span data-ttu-id="44b15-125">Konstanten (Account Management API)</span><span class="sxs-lookup"><span data-stu-id="44b15-125">Constants (Account management API)</span></span>](constants-account-management-api.md) 
- [<span data-ttu-id="44b15-126">IOlkAccount::SaveChanges</span><span class="sxs-lookup"><span data-stu-id="44b15-126">IOlkAccount::SaveChanges</span></span>](iolkaccount-savechanges.md)

