---
title: IOlkErrorUnknownGetLastError
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 3f332de3-470d-9bc2-0c65-684bb58bcd7a
description: Ruft eine Nachrichtenzeichenfolge für den angegebenen Fehler ab.
ms.openlocfilehash: 4d2aa3a7513687484988921734eb4c0e6f91226b
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33431701"
---
# <a name="iolkerrorunknowngetlasterror"></a><span data-ttu-id="b4eb4-103">IOlkErrorUnknown::GetLastError</span><span class="sxs-lookup"><span data-stu-id="b4eb4-103">IOlkErrorUnknown::GetLastError</span></span>

<span data-ttu-id="b4eb4-104">Ruft eine Nachrichtenzeichenfolge für den angegebenen Fehler ab.</span><span class="sxs-lookup"><span data-stu-id="b4eb4-104">Gets a message string for the specified error.</span></span> 
  
## <a name="quick-info"></a><span data-ttu-id="b4eb4-105">QuickInfo</span><span class="sxs-lookup"><span data-stu-id="b4eb4-105">Quick info</span></span>

<span data-ttu-id="b4eb4-106">Weitere Informationen finden Sie unter [IOlkErrorUnknown](iolkerrorunknown.md).</span><span class="sxs-lookup"><span data-stu-id="b4eb4-106">See [IOlkErrorUnknown](iolkerrorunknown.md).</span></span>
  
```cpp
HRESULT IOlkErrorUnknown::GetLastError(  
    HRESULT hr, 
    LPWSTR *ppwszError 
); 

```

## <a name="parameters"></a><span data-ttu-id="b4eb4-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="b4eb4-107">Parameters</span></span>

<span data-ttu-id="b4eb4-108">_hr_</span><span class="sxs-lookup"><span data-stu-id="b4eb4-108">_hr_</span></span>
  
> <span data-ttu-id="b4eb4-109">[in] Der zu suchende Fehlercode.</span><span class="sxs-lookup"><span data-stu-id="b4eb4-109">[in] The error code to look up.</span></span>
    
<span data-ttu-id="b4eb4-110">_ppwszError_</span><span class="sxs-lookup"><span data-stu-id="b4eb4-110">_ppwszError_</span></span>
  
> <span data-ttu-id="b4eb4-111">[out] Die Fehlermeldung, die hr *entspricht.*</span><span class="sxs-lookup"><span data-stu-id="b4eb4-111">[out] The error message that corresponds to  *hr*  .</span></span> 
    
## <a name="return-values"></a><span data-ttu-id="b4eb4-112">Rückgabewerte</span><span class="sxs-lookup"><span data-stu-id="b4eb4-112">Return values</span></span>

|<span data-ttu-id="b4eb4-113">**[HRESULT]**</span><span class="sxs-lookup"><span data-stu-id="b4eb4-113">**HRESULT**</span></span>|<span data-ttu-id="b4eb4-114">**Description**</span><span class="sxs-lookup"><span data-stu-id="b4eb4-114">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="b4eb4-115">S_OK</span><span class="sxs-lookup"><span data-stu-id="b4eb4-115">S_OK</span></span>  <br/> |<span data-ttu-id="b4eb4-116">Der Aufruf war erfolgreich.</span><span class="sxs-lookup"><span data-stu-id="b4eb4-116">The call succeeded.</span></span>  <br/> |
|<span data-ttu-id="b4eb4-117">E_INVALIDARG</span><span class="sxs-lookup"><span data-stu-id="b4eb4-117">E_INVALIDARG</span></span>  <br/> |<span data-ttu-id="b4eb4-118">Mindestens ein Argument ist ungültig.</span><span class="sxs-lookup"><span data-stu-id="b4eb4-118">One or more arguments are invalid.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="b4eb4-119">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="b4eb4-119">See also</span></span>

- [<span data-ttu-id="b4eb4-120">Konstanten (Account Management API)</span><span class="sxs-lookup"><span data-stu-id="b4eb4-120">Constants (Account management API)</span></span>](constants-account-management-api.md)

