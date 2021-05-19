---
title: IOlkAccountSaveChanges
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 8f1ab61e-7d1c-50d5-ae21-8cb4b08d729c
description: Übergeht Änderungen am Kontoobjekt, indem in den Registrierungsspeicher geschrieben wird.
ms.openlocfilehash: c23cefbbda62de9b7e159e500d95b8db5ff34ef4
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33425834"
---
# <a name="iolkaccountsavechanges"></a><span data-ttu-id="43cfc-103">IOlkAccount::SaveChanges</span><span class="sxs-lookup"><span data-stu-id="43cfc-103">IOlkAccount::SaveChanges</span></span>

<span data-ttu-id="43cfc-104">Übergeht Änderungen am Kontoobjekt, indem in den Registrierungsspeicher geschrieben wird.</span><span class="sxs-lookup"><span data-stu-id="43cfc-104">Commits changes to the account object by writing to the registry store.</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="43cfc-105">QuickInfo</span><span class="sxs-lookup"><span data-stu-id="43cfc-105">Quick info</span></span>

<span data-ttu-id="43cfc-106">Siehe [IOlkAccount](iolkaccount.md).</span><span class="sxs-lookup"><span data-stu-id="43cfc-106">See [IOlkAccount](iolkaccount.md).</span></span>
  
```cpp
HRESULT IOlkAccount::SaveChanges (  
    DWORD dwFlags 
); 
```

## <a name="parameters"></a><span data-ttu-id="43cfc-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="43cfc-107">Parameters</span></span>

<span data-ttu-id="43cfc-108">_dwFlags_</span><span class="sxs-lookup"><span data-stu-id="43cfc-108">_dwFlags_</span></span>
  
> <span data-ttu-id="43cfc-109">[in] Flags, die Verhalten ändern.</span><span class="sxs-lookup"><span data-stu-id="43cfc-109">[in] Flags to modify behavior.</span></span> <span data-ttu-id="43cfc-110">OLK_ACCOUNT_NO_FLAGS ist der einzige unterstützte Wert.</span><span class="sxs-lookup"><span data-stu-id="43cfc-110">OLK_ACCOUNT_NO_FLAGS is the only supported value.</span></span>
    
## <a name="return-values"></a><span data-ttu-id="43cfc-111">Rückgabewerte</span><span class="sxs-lookup"><span data-stu-id="43cfc-111">Return values</span></span>

|<span data-ttu-id="43cfc-112">**[HRESULT]**</span><span class="sxs-lookup"><span data-stu-id="43cfc-112">**HRESULT**</span></span>|<span data-ttu-id="43cfc-113">**Description**</span><span class="sxs-lookup"><span data-stu-id="43cfc-113">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="43cfc-114">S_OK</span><span class="sxs-lookup"><span data-stu-id="43cfc-114">S_OK</span></span>  <br/> |<span data-ttu-id="43cfc-115">Die Methode war erfolgreich.</span><span class="sxs-lookup"><span data-stu-id="43cfc-115">The method was successful.</span></span>  <br/> |
|<span data-ttu-id="43cfc-116">E_ACCT_NOT_FOUND</span><span class="sxs-lookup"><span data-stu-id="43cfc-116">E_ACCT_NOT_FOUND</span></span>  <br/> |<span data-ttu-id="43cfc-117">Das angegebene Konto kann nicht finden.</span><span class="sxs-lookup"><span data-stu-id="43cfc-117">Cannot find the specified account.</span></span>  <br/> |
|<span data-ttu-id="43cfc-118">E_OLK_NOT_INITIALIZED</span><span class="sxs-lookup"><span data-stu-id="43cfc-118">E_OLK_NOT_INITIALIZED</span></span>  <br/> |<span data-ttu-id="43cfc-119">Konto-Manager wurde nicht für die Verwendung initialisiert.</span><span class="sxs-lookup"><span data-stu-id="43cfc-119">The account manager has not been initialized for use.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="43cfc-120">Hinweise</span><span class="sxs-lookup"><span data-stu-id="43cfc-120">Remarks</span></span>

<span data-ttu-id="43cfc-121">Nachdem Sie den Wert der Kontoeigenschaften mithilfe von [IOlkAccount::SetProp](iolkaccount-setprop.md)geändert haben, verwenden Sie **IOlkAccount::SaveChanges,** um solche Änderungen zu speichern.</span><span class="sxs-lookup"><span data-stu-id="43cfc-121">After changing the value of account properties by using [IOlkAccount::SetProp](iolkaccount-setprop.md), use **IOlkAccount::SaveChanges** to save such changes.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="43cfc-122">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="43cfc-122">See also</span></span>

- [<span data-ttu-id="43cfc-123">Konstanten (Account Management API)</span><span class="sxs-lookup"><span data-stu-id="43cfc-123">Constants (Account management API)</span></span>](constants-account-management-api.md) 
- [<span data-ttu-id="43cfc-124">IOlkAccountManager::SaveChanges</span><span class="sxs-lookup"><span data-stu-id="43cfc-124">IOlkAccountManager::SaveChanges</span></span>](iolkaccountmanager-savechanges.md)

