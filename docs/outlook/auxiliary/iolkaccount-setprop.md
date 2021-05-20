---
title: IOlkAccountSetProp
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 883b1c5d-47dd-a006-b5f1-130691bdd019
description: Legt den Wert der angegebenen Account-Eigenschaft fest.
ms.openlocfilehash: 94134cee7886177ab840a6caff7d70d65bf9d4cb
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33431988"
---
# <a name="iolkaccountsetprop"></a><span data-ttu-id="86bab-103">IOlkAccount::SetProp</span><span class="sxs-lookup"><span data-stu-id="86bab-103">IOlkAccount::SetProp</span></span>

<span data-ttu-id="86bab-104">Legt den Wert der angegebenen Account-Eigenschaft fest.</span><span class="sxs-lookup"><span data-stu-id="86bab-104">Sets the value of the specified account property.</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="86bab-105">QuickInfo</span><span class="sxs-lookup"><span data-stu-id="86bab-105">Quick info</span></span>

<span data-ttu-id="86bab-106">Siehe [IOlkAccount](iolkaccount.md).</span><span class="sxs-lookup"><span data-stu-id="86bab-106">See [IOlkAccount](iolkaccount.md).</span></span>
  
```cpp
HRESULT IOlkAccount::SetProp(  
    DWORD dwProp, 
    ACCT_VARIANT *pVar 
);
```

## <a name="parameters"></a><span data-ttu-id="86bab-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="86bab-107">Parameters</span></span>

<span data-ttu-id="86bab-108">_dwProp_</span><span class="sxs-lookup"><span data-stu-id="86bab-108">_dwProp_</span></span>
  
> <span data-ttu-id="86bab-109">[in] Das Eigenschaftstag der festgelegten Account-Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="86bab-109">[in] The property tag of the account property to set.</span></span>
    
<span data-ttu-id="86bab-110">_pVar_</span><span class="sxs-lookup"><span data-stu-id="86bab-110">_pVar_</span></span>
  
> <span data-ttu-id="86bab-111">[in] Der Wert der angegebenen Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="86bab-111">[in] The value of the specified property.</span></span>
    
## <a name="return-values"></a><span data-ttu-id="86bab-112">Rückgabewerte</span><span class="sxs-lookup"><span data-stu-id="86bab-112">Return values</span></span>

|<span data-ttu-id="86bab-113">**[HRESULT]**</span><span class="sxs-lookup"><span data-stu-id="86bab-113">**HRESULT**</span></span>|<span data-ttu-id="86bab-114">**Description**</span><span class="sxs-lookup"><span data-stu-id="86bab-114">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="86bab-115">S_OK</span><span class="sxs-lookup"><span data-stu-id="86bab-115">S_OK</span></span>  <br/> |<span data-ttu-id="86bab-116">Der Methodenaufruf war erfolgreich.</span><span class="sxs-lookup"><span data-stu-id="86bab-116">The method call was successful.</span></span>  <br/> |
|<span data-ttu-id="86bab-117">E_INVALIDARG</span><span class="sxs-lookup"><span data-stu-id="86bab-117">E_INVALIDARG</span></span>  <br/> |<span data-ttu-id="86bab-118">Ein ungültiges Eigenschaftstag wurde angegeben.</span><span class="sxs-lookup"><span data-stu-id="86bab-118">An invalid property tag was specified.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="86bab-119">Hinweise</span><span class="sxs-lookup"><span data-stu-id="86bab-119">Remarks</span></span>

<span data-ttu-id="86bab-120">Verwenden [Sie IOlkAccount::SaveChanges,](iolkaccount-savechanges.md) um Änderungen am Wert der Kontoeigenschaften zu speichern.</span><span class="sxs-lookup"><span data-stu-id="86bab-120">Use [IOlkAccount::SaveChanges](iolkaccount-savechanges.md) to save changes to the value of account properties.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="86bab-121">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="86bab-121">See also</span></span>

- [<span data-ttu-id="86bab-122">Konstanten (Account Management API)</span><span class="sxs-lookup"><span data-stu-id="86bab-122">Constants (Account management API)</span></span>](constants-account-management-api.md) 
- [<span data-ttu-id="86bab-123">IOlkAccount::GetProp</span><span class="sxs-lookup"><span data-stu-id="86bab-123">IOlkAccount::GetProp</span></span>](iolkaccount-getprop.md)

