---
title: IEnumFBBlockSkip
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 70fbdb41-46ea-d016-25a2-37e94962095d
description: Überspringt eine angegebene Anzahl von Blöcken von Frei/Gebucht-Daten.
ms.openlocfilehash: cf8ae18b5ed2c24a48d44d9e8d461da7d95054d2
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33425722"
---
# <a name="ienumfbblockskip"></a><span data-ttu-id="ee356-103">IEnumFBBlock::Skip</span><span class="sxs-lookup"><span data-stu-id="ee356-103">IEnumFBBlock::Skip</span></span>

<span data-ttu-id="ee356-104">Überspringt eine angegebene Anzahl von Blöcken von Frei/Gebucht-Daten.</span><span class="sxs-lookup"><span data-stu-id="ee356-104">Skips a specified number of blocks of free/busy data.</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="ee356-105">QuickInfo</span><span class="sxs-lookup"><span data-stu-id="ee356-105">Quick info</span></span>

<span data-ttu-id="ee356-106">Weitere [Informationen finden Sie unter IEnumFBBlock](ienumfbblock.md).</span><span class="sxs-lookup"><span data-stu-id="ee356-106">See [IEnumFBBlock](ienumfbblock.md).</span></span>
  
```cpp
HRESULT Skip(  
    LONG celt 
);
```

## <a name="parameters"></a><span data-ttu-id="ee356-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="ee356-107">Parameters</span></span>

<span data-ttu-id="ee356-108">_sellert_</span><span class="sxs-lookup"><span data-stu-id="ee356-108">_celt_</span></span>
  
>  <span data-ttu-id="ee356-109">[in] Die Anzahl der zu überspringende Frei/Gebucht-Blöcke.</span><span class="sxs-lookup"><span data-stu-id="ee356-109">[in] The number of free/busy blocks to skip.</span></span> 
    
## <a name="return-values"></a><span data-ttu-id="ee356-110">Rückgabewerte</span><span class="sxs-lookup"><span data-stu-id="ee356-110">Return values</span></span>

<span data-ttu-id="ee356-111">S_OK zurück, wenn der Aufruf erfolgreich war; andernfalls einen Fehlercode.</span><span class="sxs-lookup"><span data-stu-id="ee356-111">S_OK if the call succeeded; otherwise, an error code.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="ee356-112">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="ee356-112">See also</span></span>

- [<span data-ttu-id="ee356-113">IEnumFBBlock::Clone</span><span class="sxs-lookup"><span data-stu-id="ee356-113">IEnumFBBlock::Clone</span></span>](ienumfbblock-clone.md)  
- [<span data-ttu-id="ee356-114">IEnumFBBlock::Next</span><span class="sxs-lookup"><span data-stu-id="ee356-114">IEnumFBBlock::Next</span></span>](ienumfbblock-next.md)  
- [<span data-ttu-id="ee356-115">IEnumFBBlock::Reset</span><span class="sxs-lookup"><span data-stu-id="ee356-115">IEnumFBBlock::Reset</span></span>](ienumfbblock-reset.md)  
- [<span data-ttu-id="ee356-116">IEnumFBBlock::Restrict</span><span class="sxs-lookup"><span data-stu-id="ee356-116">IEnumFBBlock::Restrict</span></span>](ienumfbblock-restrict.md)

