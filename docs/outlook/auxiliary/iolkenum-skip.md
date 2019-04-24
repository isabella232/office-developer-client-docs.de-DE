---
title: IOlkEnumSkip
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: e83e409c-f201-df9d-5e30-879adf15318d
description: Überspringt eine angegebene Anzahl von Konten im Enumerator.
ms.openlocfilehash: d4063b0ff4852e6932cf50789eea3caa81d4d586
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32321987"
---
# <a name="iolkenumskip"></a><span data-ttu-id="2670d-103">IOlkEnum::Skip</span><span class="sxs-lookup"><span data-stu-id="2670d-103">IOlkEnum::Skip</span></span>

<span data-ttu-id="2670d-104">Überspringt eine angegebene Anzahl von Konten im Enumerator.</span><span class="sxs-lookup"><span data-stu-id="2670d-104">Skips a specified number of accounts in the enumerator.</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="2670d-105">QuickInfo</span><span class="sxs-lookup"><span data-stu-id="2670d-105">Quick info</span></span>

<span data-ttu-id="2670d-106">Siehe [IOlkEnum](iolkenum.md).</span><span class="sxs-lookup"><span data-stu-id="2670d-106">See [IOlkEnum](iolkenum.md).</span></span>
  
```cpp
HRESULT IOlkEnum::Skip(  
    DWORD cSkip 
);
```

## <a name="parameters"></a><span data-ttu-id="2670d-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="2670d-107">Parameters</span></span>

<span data-ttu-id="2670d-108">_cSkip_</span><span class="sxs-lookup"><span data-stu-id="2670d-108">_cSkip_</span></span>
  
> <span data-ttu-id="2670d-109">in Die Anzahl der zu überspringenden Konten.</span><span class="sxs-lookup"><span data-stu-id="2670d-109">[in] The number of accounts to be skipped.</span></span>
    
## <a name="return-values"></a><span data-ttu-id="2670d-110">Rückgabewerte</span><span class="sxs-lookup"><span data-stu-id="2670d-110">Return values</span></span>

<span data-ttu-id="2670d-111">S_OK zurück, wenn der Aufruf erfolgreich war; andernfalls einen Fehlercode.</span><span class="sxs-lookup"><span data-stu-id="2670d-111">S_OK if the call succeeded; otherwise, an error code.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="2670d-112">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="2670d-112">See also</span></span>

- [<span data-ttu-id="2670d-113">IOlkEnum::GetCount</span><span class="sxs-lookup"><span data-stu-id="2670d-113">IOlkEnum::GetCount</span></span>](iolkenum-getcount.md) 
- [<span data-ttu-id="2670d-114">IOlkEnum::GetNext</span><span class="sxs-lookup"><span data-stu-id="2670d-114">IOlkEnum::GetNext</span></span>](iolkenum-getnext.md)  
- [<span data-ttu-id="2670d-115">IOlkEnum::Reset</span><span class="sxs-lookup"><span data-stu-id="2670d-115">IOlkEnum::Reset</span></span>](iolkenum-reset.md)

