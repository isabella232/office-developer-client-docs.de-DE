---
title: IOlkAccountManagerFreeMemory
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: acb67186-ab38-e918-5402-2526307a5bd0
description: Durch die Schnittstelle IOlkAccountManager Arbeitsspeicher frei.
ms.openlocfilehash: 85ba4d0d47eb5c879fa562e3147860533ef59f23
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19791087"
---
# <a name="iolkaccountmanagerfreememory"></a><span data-ttu-id="27274-103">IOlkAccountManager::FreeMemory</span><span class="sxs-lookup"><span data-stu-id="27274-103">IOlkAccountManager::FreeMemory</span></span>

<span data-ttu-id="27274-104">Durch die Schnittstelle [IOlkAccountManager](iolkaccountmanager.md) Arbeitsspeicher frei.</span><span class="sxs-lookup"><span data-stu-id="27274-104">Frees memory allocated by the [IOlkAccountManager](iolkaccountmanager.md) interface.</span></span> 
  
## <a name="quick-info"></a><span data-ttu-id="27274-105">QuickInfo</span><span class="sxs-lookup"><span data-stu-id="27274-105">Quick info</span></span>

<span data-ttu-id="27274-106">See [IOlkAccountManager](iolkaccountmanager.md).</span><span class="sxs-lookup"><span data-stu-id="27274-106">See [IOlkAccountManager](iolkaccountmanager.md).</span></span>
  
```cpp
HRESULT IOlkAccountManager::FreeMemory (  
    BYTE *pv, 
);
```

## <a name="parameters"></a><span data-ttu-id="27274-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="27274-107">Parameters</span></span>

<span data-ttu-id="27274-108">_PV_</span><span class="sxs-lookup"><span data-stu-id="27274-108">_pv_</span></span>
  
> <span data-ttu-id="27274-109">[in] Ein Zeiger auf den Speicher frei.</span><span class="sxs-lookup"><span data-stu-id="27274-109">[in] A pointer to the memory to free.</span></span>
    
## <a name="return-values"></a><span data-ttu-id="27274-110">Rückgabewerte</span><span class="sxs-lookup"><span data-stu-id="27274-110">Return values</span></span>

<span data-ttu-id="27274-111">S_OK zurück, wenn der Aufruf erfolgreich war; andernfalls einen Fehlercode.</span><span class="sxs-lookup"><span data-stu-id="27274-111">S_OK if the call succeeded; otherwise, an error code.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="27274-112">Anmerkungen</span><span class="sxs-lookup"><span data-stu-id="27274-112">Remarks</span></span>

<span data-ttu-id="27274-113">Verwenden Sie diese Methode, um durch [IOlkAccountManager::GetOrder](iolkaccountmanager-getorder.md)Arbeitsspeicher freizugeben.</span><span class="sxs-lookup"><span data-stu-id="27274-113">Use this method to release memory allocated by [IOlkAccountManager::GetOrder](iolkaccountmanager-getorder.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="27274-114">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="27274-114">See also</span></span>

- [<span data-ttu-id="27274-115">IOlkAccountManager::GetOrder</span><span class="sxs-lookup"><span data-stu-id="27274-115">IOlkAccountManager::GetOrder</span></span>](iolkaccountmanager-getorder.md)

