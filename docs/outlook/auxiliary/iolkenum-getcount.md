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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32322015"
---
# <a name="iolkenumgetcount"></a><span data-ttu-id="6bc78-103">IOlkEnum::GetCount</span><span class="sxs-lookup"><span data-stu-id="6bc78-103">IOlkEnum::GetCount</span></span>

<span data-ttu-id="6bc78-104">Ruft die Anzahl der Konten im Enumerator ab.</span><span class="sxs-lookup"><span data-stu-id="6bc78-104">Gets the number of accounts in the enumerator.</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="6bc78-105">QuickInfo</span><span class="sxs-lookup"><span data-stu-id="6bc78-105">Quick info</span></span>

<span data-ttu-id="6bc78-106">Siehe [IOlkEnum](iolkenum.md).</span><span class="sxs-lookup"><span data-stu-id="6bc78-106">See [IOlkEnum](iolkenum.md).</span></span>
  
```cpp
HRESULT IOlkEnum::GetCount ( 
    DWORD *pulCount 
);

```

## <a name="parameters"></a><span data-ttu-id="6bc78-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="6bc78-107">Parameters</span></span>

<span data-ttu-id="6bc78-108">_pulCount_</span><span class="sxs-lookup"><span data-stu-id="6bc78-108">_pulCount_</span></span>
  
> <span data-ttu-id="6bc78-109">Out Ein Zeiger auf die Anzahl der Objekte, die aufgezählt werden.</span><span class="sxs-lookup"><span data-stu-id="6bc78-109">[out] A pointer to the number of objects being enumerated.</span></span>
    
## <a name="return-values"></a><span data-ttu-id="6bc78-110">Rückgabewerte</span><span class="sxs-lookup"><span data-stu-id="6bc78-110">Return values</span></span>

<span data-ttu-id="6bc78-111">S_OK zurück, wenn der Aufruf erfolgreich war; andernfalls einen Fehlercode.</span><span class="sxs-lookup"><span data-stu-id="6bc78-111">S_OK if the call succeeded; otherwise, an error code.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="6bc78-112">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="6bc78-112">See also</span></span>

- [<span data-ttu-id="6bc78-113">IOlkEnum::GetNext</span><span class="sxs-lookup"><span data-stu-id="6bc78-113">IOlkEnum::GetNext</span></span>](iolkenum-getnext.md)  
- [<span data-ttu-id="6bc78-114">IOlkEnum::Reset</span><span class="sxs-lookup"><span data-stu-id="6bc78-114">IOlkEnum::Reset</span></span>](iolkenum-reset.md) 
- [<span data-ttu-id="6bc78-115">IOlkEnum::Skip</span><span class="sxs-lookup"><span data-stu-id="6bc78-115">IOlkEnum::Skip</span></span>](iolkenum-skip.md)

