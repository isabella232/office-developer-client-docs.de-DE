---
title: IEnumFBBlockSkip
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 70fbdb41-46ea-d016-25a2-37e94962095d
description: Überspringt eine angegebene Anzahl von Frei/Gebucht-Datenblöcken.
ms.openlocfilehash: cf8ae18b5ed2c24a48d44d9e8d461da7d95054d2
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32317549"
---
# <a name="ienumfbblockskip"></a><span data-ttu-id="c28f1-103">IEnumFBBlock::Skip</span><span class="sxs-lookup"><span data-stu-id="c28f1-103">IEnumFBBlock::Skip</span></span>

<span data-ttu-id="c28f1-104">Überspringt eine angegebene Anzahl von Frei/Gebucht-Datenblöcken.</span><span class="sxs-lookup"><span data-stu-id="c28f1-104">Skips a specified number of blocks of free/busy data.</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="c28f1-105">QuickInfo</span><span class="sxs-lookup"><span data-stu-id="c28f1-105">Quick info</span></span>

<span data-ttu-id="c28f1-106">Siehe [IEnumFBBlock](ienumfbblock.md).</span><span class="sxs-lookup"><span data-stu-id="c28f1-106">See [IEnumFBBlock](ienumfbblock.md).</span></span>
  
```cpp
HRESULT Skip(  
    LONG celt 
);
```

## <a name="parameters"></a><span data-ttu-id="c28f1-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="c28f1-107">Parameters</span></span>

<span data-ttu-id="c28f1-108">_celt_</span><span class="sxs-lookup"><span data-stu-id="c28f1-108">_celt_</span></span>
  
>  <span data-ttu-id="c28f1-109">in Die Anzahl der frei/gebucht-Blöcke, die übersprungen werden sollen.</span><span class="sxs-lookup"><span data-stu-id="c28f1-109">[in] The number of free/busy blocks to skip.</span></span> 
    
## <a name="return-values"></a><span data-ttu-id="c28f1-110">Rückgabewerte</span><span class="sxs-lookup"><span data-stu-id="c28f1-110">Return values</span></span>

<span data-ttu-id="c28f1-111">S_OK zurück, wenn der Aufruf erfolgreich war; andernfalls einen Fehlercode.</span><span class="sxs-lookup"><span data-stu-id="c28f1-111">S_OK if the call succeeded; otherwise, an error code.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="c28f1-112">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="c28f1-112">See also</span></span>

- [<span data-ttu-id="c28f1-113">IEnumFBBlock::Clone</span><span class="sxs-lookup"><span data-stu-id="c28f1-113">IEnumFBBlock::Clone</span></span>](ienumfbblock-clone.md)  
- [<span data-ttu-id="c28f1-114">IEnumFBBlock::Next</span><span class="sxs-lookup"><span data-stu-id="c28f1-114">IEnumFBBlock::Next</span></span>](ienumfbblock-next.md)  
- [<span data-ttu-id="c28f1-115">IEnumFBBlock::Reset</span><span class="sxs-lookup"><span data-stu-id="c28f1-115">IEnumFBBlock::Reset</span></span>](ienumfbblock-reset.md)  
- [<span data-ttu-id="c28f1-116">IEnumFBBlock::Restrict</span><span class="sxs-lookup"><span data-stu-id="c28f1-116">IEnumFBBlock::Restrict</span></span>](ienumfbblock-restrict.md)

