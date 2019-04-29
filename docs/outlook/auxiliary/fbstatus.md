---
title: FBStatus
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: f2d6a11e-847d-6bbe-cd77-e78ee961cb12
description: Eine Enumeration für den Frei/Gebucht-Status von Frei/Gebucht-Blöcken.
ms.openlocfilehash: 2a08ef142f9baddd453166c0ebcb989e69a51ceb
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33424091"
---
# <a name="fbstatus"></a><span data-ttu-id="a8ab1-103">FBStatus</span><span class="sxs-lookup"><span data-stu-id="a8ab1-103">FBStatus</span></span>

<span data-ttu-id="a8ab1-104">Eine Enumeration für den Frei/Gebucht-Status von Frei/Gebucht-Blöcken.</span><span class="sxs-lookup"><span data-stu-id="a8ab1-104">An enumeration for the free/busy status of free/busy blocks.</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="a8ab1-105">QuickInfo</span><span class="sxs-lookup"><span data-stu-id="a8ab1-105">Quick info</span></span>

```cpp
enum  
    { 
      fbFree      = 0, 
      fbTentative = fbFree + 1, 
      fbBusy      = fbTentative + 1, 
      fbOutOfOffice = fbBusy + 1 
    }

```

## <a name="remarks"></a><span data-ttu-id="a8ab1-106">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="a8ab1-106">Remarks</span></span>

<span data-ttu-id="a8ab1-107">Der Frei/Gebucht-Status eines Zeitblocks bestimmt, wie er in einem Kalender angezeigt wird: **frei**, **beschäftigt**, mit **Vorbehalt**oder \*\*\*\* Abwesenheit.</span><span class="sxs-lookup"><span data-stu-id="a8ab1-107">The free/busy status of a block of time determines how it is displayed on a calendar: **Free**, **Busy**, **Tentative**, or **Out of Office**.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="a8ab1-108">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="a8ab1-108">See also</span></span>

- [<span data-ttu-id="a8ab1-109">FBBlock_1</span><span class="sxs-lookup"><span data-stu-id="a8ab1-109">FBBlock_1</span></span>](fbblock_1.md)
- [<span data-ttu-id="a8ab1-110">IEnumFBBlock::Next</span><span class="sxs-lookup"><span data-stu-id="a8ab1-110">IEnumFBBlock::Next</span></span>](ienumfbblock-next.md)

