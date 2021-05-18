---
title: IOlkEnumGetCount
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: dd7a7e62-4cf2-bdd3-8a00-4fff5ac575d3
description: Ruft die Anzahl der Konten im Enumerator ab.
ms.openlocfilehash: 8571d5ff01501d980c8b6543607a658ad99085ca
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33421823"
---
# <a name="iolkenumgetcount"></a><span data-ttu-id="4ea10-103">IOlkEnum::GetCount</span><span class="sxs-lookup"><span data-stu-id="4ea10-103">IOlkEnum::GetCount</span></span>

<span data-ttu-id="4ea10-104">Ruft die Anzahl der Konten im Enumerator ab.</span><span class="sxs-lookup"><span data-stu-id="4ea10-104">Gets the number of accounts in the enumerator.</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="4ea10-105">QuickInfo</span><span class="sxs-lookup"><span data-stu-id="4ea10-105">Quick info</span></span>

<span data-ttu-id="4ea10-106">Siehe [IOlkEnum](iolkenum.md).</span><span class="sxs-lookup"><span data-stu-id="4ea10-106">See [IOlkEnum](iolkenum.md).</span></span>
  
```cpp
HRESULT IOlkEnum::GetCount ( 
    DWORD *pulCount 
);

```

## <a name="parameters"></a><span data-ttu-id="4ea10-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="4ea10-107">Parameters</span></span>

<span data-ttu-id="4ea10-108">_pulCount_</span><span class="sxs-lookup"><span data-stu-id="4ea10-108">_pulCount_</span></span>
  
> <span data-ttu-id="4ea10-109">[out] Ein Zeiger auf die Anzahl der objekte, die aufgezählt werden.</span><span class="sxs-lookup"><span data-stu-id="4ea10-109">[out] A pointer to the number of objects being enumerated.</span></span>
    
## <a name="return-values"></a><span data-ttu-id="4ea10-110">Rückgabewerte</span><span class="sxs-lookup"><span data-stu-id="4ea10-110">Return values</span></span>

<span data-ttu-id="4ea10-111">S_OK zurück, wenn der Aufruf erfolgreich war; andernfalls einen Fehlercode.</span><span class="sxs-lookup"><span data-stu-id="4ea10-111">S_OK if the call succeeded; otherwise, an error code.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="4ea10-112">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="4ea10-112">See also</span></span>

- [<span data-ttu-id="4ea10-113">IOlkEnum::GetNext</span><span class="sxs-lookup"><span data-stu-id="4ea10-113">IOlkEnum::GetNext</span></span>](iolkenum-getnext.md)  
- [<span data-ttu-id="4ea10-114">IOlkEnum::Reset</span><span class="sxs-lookup"><span data-stu-id="4ea10-114">IOlkEnum::Reset</span></span>](iolkenum-reset.md) 
- [<span data-ttu-id="4ea10-115">IOlkEnum::Skip</span><span class="sxs-lookup"><span data-stu-id="4ea10-115">IOlkEnum::Skip</span></span>](iolkenum-skip.md)

