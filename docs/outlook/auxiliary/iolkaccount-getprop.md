---
title: IOlkAccountGetProp
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 5725eb52-3a78-897d-f9e3-c5a494fb78c0
description: Ruft den Wert der Eigenschaft angegebene Konto.
ms.openlocfilehash: 2c0756f416a209d37eff2209a82c298837f85f3d
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19791039"
---
# <a name="iolkaccountgetprop"></a><span data-ttu-id="20cdd-103">IOlkAccount::GetProp</span><span class="sxs-lookup"><span data-stu-id="20cdd-103">IOlkAccount::GetProp</span></span>

<span data-ttu-id="20cdd-104">Ruft den Wert der Eigenschaft angegebene Konto.</span><span class="sxs-lookup"><span data-stu-id="20cdd-104">Gets the value of the specified account property.</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="20cdd-105">QuickInfo</span><span class="sxs-lookup"><span data-stu-id="20cdd-105">Quick info</span></span>

<span data-ttu-id="20cdd-106">Finden Sie unter [IOlkAccount](iolkaccount.md).</span><span class="sxs-lookup"><span data-stu-id="20cdd-106">See [IOlkAccount](iolkaccount.md).</span></span>
  
```cpp
HRESULT IOlkAccount::GetProp(  
DWORD dwProp, 
ACCT_VARIANT *pVar 
);
```

## <a name="parameters"></a><span data-ttu-id="20cdd-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="20cdd-107">Parameters</span></span>

<span data-ttu-id="20cdd-108">_dwProp_</span><span class="sxs-lookup"><span data-stu-id="20cdd-108">_dwProp_</span></span>
  
> <span data-ttu-id="20cdd-109">[in] Die Eigenschaftstag der Konto-Eigenschaft abrufen.</span><span class="sxs-lookup"><span data-stu-id="20cdd-109">[in] The property tag of the account property to get.</span></span>
    
<span data-ttu-id="20cdd-110">_pVar_</span><span class="sxs-lookup"><span data-stu-id="20cdd-110">_pVar_</span></span>
  
> <span data-ttu-id="20cdd-111">[out] Der Wert der angegebenen Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="20cdd-111">[out] The value of the specified property.</span></span>
    
## <a name="return-values"></a><span data-ttu-id="20cdd-112">Rückgabewerte</span><span class="sxs-lookup"><span data-stu-id="20cdd-112">Return values</span></span>

|<span data-ttu-id="20cdd-113">**[HRESULT]**</span><span class="sxs-lookup"><span data-stu-id="20cdd-113">**HRESULT**</span></span>|<span data-ttu-id="20cdd-114">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="20cdd-114">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="20cdd-115">S_OK</span><span class="sxs-lookup"><span data-stu-id="20cdd-115">S_OK</span></span>  <br/> |<span data-ttu-id="20cdd-116">Der Aufruf war erfolgreich.</span><span class="sxs-lookup"><span data-stu-id="20cdd-116">The call succeeded.</span></span>  <br/> |
|<span data-ttu-id="20cdd-117">E_ACCT_NOT_FOUND</span><span class="sxs-lookup"><span data-stu-id="20cdd-117">E_ACCT_NOT_FOUND</span></span>  <br/> |<span data-ttu-id="20cdd-118">Die Eigenschaft ist für das angegebene Konto nicht gefunden.</span><span class="sxs-lookup"><span data-stu-id="20cdd-118">The property is not found for the given account.</span></span>  <br/> |
|<span data-ttu-id="20cdd-119">E_INVALIDARG</span><span class="sxs-lookup"><span data-stu-id="20cdd-119">E_INVALIDARG</span></span>  <br/> |<span data-ttu-id="20cdd-120">Ein ungültiger Eigenschafts-Tag es wurde angegeben.</span><span class="sxs-lookup"><span data-stu-id="20cdd-120">An invalid property tag has been specified.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="20cdd-121">Hinweise</span><span class="sxs-lookup"><span data-stu-id="20cdd-121">Remarks</span></span>

<span data-ttu-id="20cdd-122">Nachdem diese Methode zurückgegeben, wenn der Wert der Eigenschaft Konto einen Typ Binär oder eine Zeichenfolge handelt, müssen Sie *pVar* mithilfe von [IOlkAccount::FreeMemory](iolkaccount-freememory.md)freigeben.</span><span class="sxs-lookup"><span data-stu-id="20cdd-122">After this method returns, if the value of the account property is a binary or string type, you must free  *pVar*  by using [IOlkAccount::FreeMemory](iolkaccount-freememory.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="20cdd-123">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="20cdd-123">See also</span></span>

- [<span data-ttu-id="20cdd-124">Konstanten (Account Management API)</span><span class="sxs-lookup"><span data-stu-id="20cdd-124">Constants (Account management API)</span></span>](constants-account-management-api.md) 
- [<span data-ttu-id="20cdd-125">IOlkAccount::FreeMemory</span><span class="sxs-lookup"><span data-stu-id="20cdd-125">IOlkAccount::FreeMemory</span></span>](iolkaccount-freememory.md)  
- [<span data-ttu-id="20cdd-126">IOlkAccount::SetProp</span><span class="sxs-lookup"><span data-stu-id="20cdd-126">IOlkAccount::SetProp</span></span>](iolkaccount-setprop.md)

