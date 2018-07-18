---
title: IOlkAccountManagerSaveChanges
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 32a5d4b7-ead7-24e7-58f2-750232263a0d
description: Speichert Änderungen an das angegebene Konto.
ms.openlocfilehash: 87b513659b632e88697fb63d1aeccccb77ed9fd1
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19791107"
---
# <a name="iolkaccountmanagersavechanges"></a><span data-ttu-id="606af-103">IOlkAccountManager::SaveChanges</span><span class="sxs-lookup"><span data-stu-id="606af-103">IOlkAccountManager::SaveChanges</span></span>

<span data-ttu-id="606af-104">Speichert Änderungen an das angegebene Konto.</span><span class="sxs-lookup"><span data-stu-id="606af-104">Saves changes to the specified account.</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="606af-105">QuickInfo</span><span class="sxs-lookup"><span data-stu-id="606af-105">Quick info</span></span>

<span data-ttu-id="606af-106">See [IOlkAccountManager](iolkaccountmanager.md).</span><span class="sxs-lookup"><span data-stu-id="606af-106">See [IOlkAccountManager](iolkaccountmanager.md).</span></span>
  
```cpp
HRESULT IOlkAccountManager::SaveChanges (  
    DWORD dwAcctID, 
    DWORD dwFlags 
); 
```

## <a name="parameters"></a><span data-ttu-id="606af-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="606af-107">Parameters</span></span>

<span data-ttu-id="606af-108">_dwAcctID_</span><span class="sxs-lookup"><span data-stu-id="606af-108">_dwAcctID_</span></span>
  
> <span data-ttu-id="606af-109">[in] Die Konto-ID zu speichern.</span><span class="sxs-lookup"><span data-stu-id="606af-109">[in] The account ID to save.</span></span> 
    
<span data-ttu-id="606af-110">_dwFlags_</span><span class="sxs-lookup"><span data-stu-id="606af-110">_dwFlags_</span></span>
  
> <span data-ttu-id="606af-111">[in] Flags, die Verhalten ändern.</span><span class="sxs-lookup"><span data-stu-id="606af-111">[in] Flags to modify behavior.</span></span> <span data-ttu-id="606af-112">OLK_ACCOUNT_NO_FLAGS ist der einzige unterstützte Wert.</span><span class="sxs-lookup"><span data-stu-id="606af-112">OLK_ACCOUNT_NO_FLAGS is the only supported value.</span></span>
    
## <a name="return-values"></a><span data-ttu-id="606af-113">Rückgabewerte</span><span class="sxs-lookup"><span data-stu-id="606af-113">Return values</span></span>

|<span data-ttu-id="606af-114">**[HRESULT]**</span><span class="sxs-lookup"><span data-stu-id="606af-114">**HRESULT**</span></span>|<span data-ttu-id="606af-115">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="606af-115">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="606af-116">S_OK</span><span class="sxs-lookup"><span data-stu-id="606af-116">S_OK</span></span>  <br/> |<span data-ttu-id="606af-117">Der Aufruf war erfolgreich</span><span class="sxs-lookup"><span data-stu-id="606af-117">The call succeeded</span></span>  <br/> |
|<span data-ttu-id="606af-118">E_ACCT_NOT_FOUND</span><span class="sxs-lookup"><span data-stu-id="606af-118">E_ACCT_NOT_FOUND</span></span>  <br/> |<span data-ttu-id="606af-119">Das angegebene Konto kann nicht gefunden werden.</span><span class="sxs-lookup"><span data-stu-id="606af-119">The specified account cannot be found.</span></span>  <br/> |
|<span data-ttu-id="606af-120">E_OLK_NOT_INITIALIZED</span><span class="sxs-lookup"><span data-stu-id="606af-120">E_OLK_NOT_INITIALIZED</span></span>  <br/> |<span data-ttu-id="606af-121">Konto-Manager wurde nicht für die Verwendung initialisiert.</span><span class="sxs-lookup"><span data-stu-id="606af-121">The account manager has not been initialized for use.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="606af-122">Hinweise</span><span class="sxs-lookup"><span data-stu-id="606af-122">Remarks</span></span>

<span data-ttu-id="606af-123">Verwenden Sie nach dem Ändern des Werts der Eigenschaften von Benutzerkonten mithilfe von [IOlkAccount::SetProp](iolkaccount-setprop.md), **IOlkAccountManager::SaveChanges** oder [IOlkAccount::SaveChanges](iolkaccount-savechanges.md) , um derartige Änderungen zu speichern.</span><span class="sxs-lookup"><span data-stu-id="606af-123">After changing the value of account properties by using [IOlkAccount::SetProp](iolkaccount-setprop.md), use **IOlkAccountManager::SaveChanges** or [IOlkAccount::SaveChanges](iolkaccount-savechanges.md) to save such changes.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="606af-124">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="606af-124">See also</span></span>

- [<span data-ttu-id="606af-125">Konstanten (Account Management API)</span><span class="sxs-lookup"><span data-stu-id="606af-125">Constants (Account management API)</span></span>](constants-account-management-api.md) 
- [<span data-ttu-id="606af-126">IOlkAccount::SaveChanges</span><span class="sxs-lookup"><span data-stu-id="606af-126">IOlkAccount::SaveChanges</span></span>](iolkaccount-savechanges.md)

