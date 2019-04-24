---
title: IOlkAccountGetProp
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 5725eb52-3a78-897d-f9e3-c5a494fb78c0
description: Ruft den Wert der angegebenen Account-Eigenschaft ab.
ms.openlocfilehash: d24df8cfa9d54bee4614c1f31e12268748b8c986
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32321234"
---
# <a name="iolkaccountgetprop"></a><span data-ttu-id="d2a05-103">IOlkAccount::GetProp</span><span class="sxs-lookup"><span data-stu-id="d2a05-103">IOlkAccount::GetProp</span></span>

<span data-ttu-id="d2a05-104">Ruft den Wert der angegebenen Account-Eigenschaft ab.</span><span class="sxs-lookup"><span data-stu-id="d2a05-104">Gets the value of the specified account property.</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="d2a05-105">QuickInfo</span><span class="sxs-lookup"><span data-stu-id="d2a05-105">Quick info</span></span>

<span data-ttu-id="d2a05-106">Siehe [IOlkAccount](iolkaccount.md).</span><span class="sxs-lookup"><span data-stu-id="d2a05-106">See [IOlkAccount](iolkaccount.md).</span></span>
  
```cpp
HRESULT IOlkAccount::GetProp(  
DWORD dwProp, 
ACCT_VARIANT *pVar 
);
```

## <a name="parameters"></a><span data-ttu-id="d2a05-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="d2a05-107">Parameters</span></span>

<span data-ttu-id="d2a05-108">_dwProp_</span><span class="sxs-lookup"><span data-stu-id="d2a05-108">_dwProp_</span></span>
  
> <span data-ttu-id="d2a05-109">in Das Property-Tag der abzurufenden Account-Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="d2a05-109">[in] The property tag of the account property to get.</span></span>
    
<span data-ttu-id="d2a05-110">_pVar_</span><span class="sxs-lookup"><span data-stu-id="d2a05-110">_pVar_</span></span>
  
> <span data-ttu-id="d2a05-111">Out Der Wert der angegebenen Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="d2a05-111">[out] The value of the specified property.</span></span>
    
## <a name="return-values"></a><span data-ttu-id="d2a05-112">Rückgabewerte</span><span class="sxs-lookup"><span data-stu-id="d2a05-112">Return values</span></span>

|<span data-ttu-id="d2a05-113">**[HRESULT]**</span><span class="sxs-lookup"><span data-stu-id="d2a05-113">**HRESULT**</span></span>|<span data-ttu-id="d2a05-114">**Description**</span><span class="sxs-lookup"><span data-stu-id="d2a05-114">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="d2a05-115">S_OK</span><span class="sxs-lookup"><span data-stu-id="d2a05-115">S_OK</span></span>  <br/> |<span data-ttu-id="d2a05-116">Der Aufruf war erfolgreich.</span><span class="sxs-lookup"><span data-stu-id="d2a05-116">The call succeeded.</span></span>  <br/> |
|<span data-ttu-id="d2a05-117">E_ACCT_NOT_FOUND</span><span class="sxs-lookup"><span data-stu-id="d2a05-117">E_ACCT_NOT_FOUND</span></span>  <br/> |<span data-ttu-id="d2a05-118">Die Eigenschaft wurde für das angegebene Konto nicht gefunden.</span><span class="sxs-lookup"><span data-stu-id="d2a05-118">The property is not found for the given account.</span></span>  <br/> |
|<span data-ttu-id="d2a05-119">E_INVALIDARG</span><span class="sxs-lookup"><span data-stu-id="d2a05-119">E_INVALIDARG</span></span>  <br/> |<span data-ttu-id="d2a05-120">Es wurde ein ungültiges Property-Tag angegeben.</span><span class="sxs-lookup"><span data-stu-id="d2a05-120">An invalid property tag has been specified.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="d2a05-121">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="d2a05-121">Remarks</span></span>

<span data-ttu-id="d2a05-122">Nachdem diese Methode zurückgegeben hat, müssen Sie, wenn der Wert der Account-Eigenschaft ein binary-oder String-Typ ist, *pVar* mit [IOlkAccount:: freier Arbeitsspeicher](iolkaccount-freememory.md)freigeben.</span><span class="sxs-lookup"><span data-stu-id="d2a05-122">After this method returns, if the value of the account property is a binary or string type, you must free  *pVar*  by using [IOlkAccount::FreeMemory](iolkaccount-freememory.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="d2a05-123">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="d2a05-123">See also</span></span>

- [<span data-ttu-id="d2a05-124">Konstanten (Account Management API)</span><span class="sxs-lookup"><span data-stu-id="d2a05-124">Constants (Account management API)</span></span>](constants-account-management-api.md) 
- [<span data-ttu-id="d2a05-125">IOlkAccount::FreeMemory</span><span class="sxs-lookup"><span data-stu-id="d2a05-125">IOlkAccount::FreeMemory</span></span>](iolkaccount-freememory.md)  
- [<span data-ttu-id="d2a05-126">IOlkAccount::SetProp</span><span class="sxs-lookup"><span data-stu-id="d2a05-126">IOlkAccount::SetProp</span></span>](iolkaccount-setprop.md)

