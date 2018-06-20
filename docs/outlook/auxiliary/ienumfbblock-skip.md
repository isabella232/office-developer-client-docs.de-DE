---
title: IEnumFBBlockSkip
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 70fbdb41-46ea-d016-25a2-37e94962095d
description: Überspringt eine angegebene Anzahl von Blöcken des Frei/Gebucht-Daten.
ms.openlocfilehash: 63f699d09e143a879702e8dc76beb8a969a77b82
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19790950"
---
# <a name="ienumfbblockskip"></a><span data-ttu-id="fc768-103">IEnumFBBlock::Skip</span><span class="sxs-lookup"><span data-stu-id="fc768-103">IEnumFBBlock::Skip</span></span>

<span data-ttu-id="fc768-104">Überspringt eine angegebene Anzahl von Blöcken des Frei/Gebucht-Daten.</span><span class="sxs-lookup"><span data-stu-id="fc768-104">Skips a specified number of blocks of free/busy data.</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="fc768-105">QuickInfo</span><span class="sxs-lookup"><span data-stu-id="fc768-105">Quick info</span></span>

<span data-ttu-id="fc768-106">Finden Sie unter [IEnumFBBlock](ienumfbblock.md).</span><span class="sxs-lookup"><span data-stu-id="fc768-106">See [IEnumFBBlock](ienumfbblock.md).</span></span>
  
```cpp
HRESULT Skip(  
    LONG celt 
);
```

## <a name="parameters"></a><span data-ttu-id="fc768-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="fc768-107">Parameters</span></span>

<span data-ttu-id="fc768-108">_celt_</span><span class="sxs-lookup"><span data-stu-id="fc768-108">_celt_</span></span>
  
>  <span data-ttu-id="fc768-109">[in] Die Anzahl der Frei/Gebucht-Blöcke überspringen.</span><span class="sxs-lookup"><span data-stu-id="fc768-109">[in] The number of free/busy blocks to skip.</span></span> 
    
## <a name="return-values"></a><span data-ttu-id="fc768-110">Rückgabewerte</span><span class="sxs-lookup"><span data-stu-id="fc768-110">Return values</span></span>

<span data-ttu-id="fc768-111">S_OK zurück, wenn der Aufruf erfolgreich war; andernfalls einen Fehlercode.</span><span class="sxs-lookup"><span data-stu-id="fc768-111">S_OK if the call succeeded; otherwise, an error code.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="fc768-112">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="fc768-112">See also</span></span>

- [<span data-ttu-id="fc768-113">IEnumFBBlock::Clone</span><span class="sxs-lookup"><span data-stu-id="fc768-113">IEnumFBBlock::Clone</span></span>](ienumfbblock-clone.md)  
- [<span data-ttu-id="fc768-114">IEnumFBBlock::Next</span><span class="sxs-lookup"><span data-stu-id="fc768-114">IEnumFBBlock::Next</span></span>](ienumfbblock-next.md)  
- [<span data-ttu-id="fc768-115">IEnumFBBlock::Reset</span><span class="sxs-lookup"><span data-stu-id="fc768-115">IEnumFBBlock::Reset</span></span>](ienumfbblock-reset.md)  
- [<span data-ttu-id="fc768-116">IEnumFBBlock::Restrict</span><span class="sxs-lookup"><span data-stu-id="fc768-116">IEnumFBBlock::Restrict</span></span>](ienumfbblock-restrict.md)

