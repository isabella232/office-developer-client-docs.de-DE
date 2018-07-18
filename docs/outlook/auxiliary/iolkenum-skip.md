---
title: IOlkEnumSkip
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: e83e409c-f201-df9d-5e30-879adf15318d
description: Überspringt eine angegebene Anzahl von Konten in den Enumerator.
ms.openlocfilehash: 2791f1204cedf5e91d13923e50dfc45b981b7e26
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19791109"
---
# <a name="iolkenumskip"></a><span data-ttu-id="7b340-103">IOlkEnum::Skip</span><span class="sxs-lookup"><span data-stu-id="7b340-103">IOlkEnum::Skip</span></span>

<span data-ttu-id="7b340-104">Überspringt eine angegebene Anzahl von Konten in den Enumerator.</span><span class="sxs-lookup"><span data-stu-id="7b340-104">Skips a specified number of accounts in the enumerator.</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="7b340-105">QuickInfo</span><span class="sxs-lookup"><span data-stu-id="7b340-105">Quick info</span></span>

<span data-ttu-id="7b340-106">Finden Sie unter [IOlkEnum](iolkenum.md).</span><span class="sxs-lookup"><span data-stu-id="7b340-106">See [IOlkEnum](iolkenum.md).</span></span>
  
```cpp
HRESULT IOlkEnum::Skip(  
    DWORD cSkip 
);
```

## <a name="parameters"></a><span data-ttu-id="7b340-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="7b340-107">Parameters</span></span>

<span data-ttu-id="7b340-108">_cSkip_</span><span class="sxs-lookup"><span data-stu-id="7b340-108">_cSkip_</span></span>
  
> <span data-ttu-id="7b340-109">[in] Die Anzahl der Konten übersprungen werden soll.</span><span class="sxs-lookup"><span data-stu-id="7b340-109">[in] The number of accounts to be skipped.</span></span>
    
## <a name="return-values"></a><span data-ttu-id="7b340-110">Rückgabewerte</span><span class="sxs-lookup"><span data-stu-id="7b340-110">Return values</span></span>

<span data-ttu-id="7b340-111">S_OK zurück, wenn der Aufruf erfolgreich war; andernfalls einen Fehlercode.</span><span class="sxs-lookup"><span data-stu-id="7b340-111">S_OK if the call succeeded; otherwise, an error code.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="7b340-112">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="7b340-112">See also</span></span>

- [<span data-ttu-id="7b340-113">IOlkEnum::GetCount</span><span class="sxs-lookup"><span data-stu-id="7b340-113">IOlkEnum::GetCount</span></span>](iolkenum-getcount.md) 
- [<span data-ttu-id="7b340-114">IOlkEnum::GetNext</span><span class="sxs-lookup"><span data-stu-id="7b340-114">IOlkEnum::GetNext</span></span>](iolkenum-getnext.md)  
- [<span data-ttu-id="7b340-115">IOlkEnum::Reset</span><span class="sxs-lookup"><span data-stu-id="7b340-115">IOlkEnum::Reset</span></span>](iolkenum-reset.md)

