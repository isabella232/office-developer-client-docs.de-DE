---
title: IOlkErrorUnknownGetLastError
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 3f332de3-470d-9bc2-0c65-684bb58bcd7a
description: Ruft eine Meldungszeichenfolge für den angegebenen Fehler.
ms.openlocfilehash: 7b00392cdf65d1d4990f2231769e5126c9ae26dc
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19791120"
---
# <a name="iolkerrorunknowngetlasterror"></a><span data-ttu-id="e74e4-103">IOlkErrorUnknown::GetLastError</span><span class="sxs-lookup"><span data-stu-id="e74e4-103">IOlkErrorUnknown::GetLastError</span></span>

<span data-ttu-id="e74e4-104">Ruft eine Meldungszeichenfolge für den angegebenen Fehler.</span><span class="sxs-lookup"><span data-stu-id="e74e4-104">Gets a message string for the specified error.</span></span> 
  
## <a name="quick-info"></a><span data-ttu-id="e74e4-105">QuickInfo</span><span class="sxs-lookup"><span data-stu-id="e74e4-105">Quick info</span></span>

<span data-ttu-id="e74e4-106">Finden Sie unter [IOlkErrorUnknown](iolkerrorunknown.md).</span><span class="sxs-lookup"><span data-stu-id="e74e4-106">See [IOlkErrorUnknown](iolkerrorunknown.md).</span></span>
  
```cpp
HRESULT IOlkErrorUnknown::GetLastError(  
    HRESULT hr, 
    LPWSTR *ppwszError 
); 

```

## <a name="parameters"></a><span data-ttu-id="e74e4-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="e74e4-107">Parameters</span></span>

<span data-ttu-id="e74e4-108">_Personalwesen_</span><span class="sxs-lookup"><span data-stu-id="e74e4-108">_hr_</span></span>
  
> <span data-ttu-id="e74e4-109">[in] Der Fehlercode nachzuschlagen.</span><span class="sxs-lookup"><span data-stu-id="e74e4-109">[in] The error code to look up.</span></span>
    
<span data-ttu-id="e74e4-110">_ppwszError_</span><span class="sxs-lookup"><span data-stu-id="e74e4-110">_ppwszError_</span></span>
  
> <span data-ttu-id="e74e4-111">[out] Die Fehlermeldung, die entspricht, *hr* .</span><span class="sxs-lookup"><span data-stu-id="e74e4-111">[out] The error message that corresponds to  *hr*  .</span></span> 
    
## <a name="return-values"></a><span data-ttu-id="e74e4-112">Rückgabewerte</span><span class="sxs-lookup"><span data-stu-id="e74e4-112">Return values</span></span>

|<span data-ttu-id="e74e4-113">**[HRESULT]**</span><span class="sxs-lookup"><span data-stu-id="e74e4-113">**HRESULT**</span></span>|<span data-ttu-id="e74e4-114">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="e74e4-114">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="e74e4-115">S_OK</span><span class="sxs-lookup"><span data-stu-id="e74e4-115">S_OK</span></span>  <br/> |<span data-ttu-id="e74e4-116">Der Aufruf war erfolgreich.</span><span class="sxs-lookup"><span data-stu-id="e74e4-116">The call succeeded.</span></span>  <br/> |
|<span data-ttu-id="e74e4-117">E_INVALIDARG</span><span class="sxs-lookup"><span data-stu-id="e74e4-117">E_INVALIDARG</span></span>  <br/> |<span data-ttu-id="e74e4-118">Mindestens ein Argument ist ungültig.</span><span class="sxs-lookup"><span data-stu-id="e74e4-118">One or more arguments are invalid.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="e74e4-119">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="e74e4-119">See also</span></span>

- [<span data-ttu-id="e74e4-120">Konstanten (Account Management API)</span><span class="sxs-lookup"><span data-stu-id="e74e4-120">Constants (Account management API)</span></span>](constants-account-management-api.md)

