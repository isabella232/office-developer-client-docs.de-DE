---
title: FBBlock_1
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: da67171d-d25f-3424-1409-33189ac63a12
description: Definiert einen Frei/Gebucht-Block von Daten. Dies ist ein Element in einem Kalender, der durch eine Termin- oder Besprechungsanfrage dargestellt wird.
ms.openlocfilehash: 60d2ff50081a8950a397df6f2f6bbfd37d3bdb61
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33413199"
---
# <a name="fbblock_1"></a><span data-ttu-id="04fe2-104">FBBlock_1</span><span class="sxs-lookup"><span data-stu-id="04fe2-104">FBBlock_1</span></span>

<span data-ttu-id="04fe2-105">Definiert einen Frei/Gebucht-Block von Daten.</span><span class="sxs-lookup"><span data-stu-id="04fe2-105">Defines a free/busy block of data.</span></span> <span data-ttu-id="04fe2-106">Dies ist ein Element in einem Kalender, der durch eine Termin- oder Besprechungsanfrage dargestellt wird.</span><span class="sxs-lookup"><span data-stu-id="04fe2-106">This is an item on a calendar represented by an appointment or meeting request.</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="04fe2-107">QuickInfo</span><span class="sxs-lookup"><span data-stu-id="04fe2-107">Quick info</span></span>

```cpp
typedef struct  tagFBBlock_1 
    { 
    long m_tmStart; 
    long m_tmEnd; 
    FBStatus m_fbstatus; 
    }FBBlock_1; 

```

## <a name="members"></a><span data-ttu-id="04fe2-108">Elemente</span><span class="sxs-lookup"><span data-stu-id="04fe2-108">Members</span></span>

<span data-ttu-id="04fe2-109">_m_tmStart_</span><span class="sxs-lookup"><span data-stu-id="04fe2-109">_m_tmStart_</span></span>
  
> <span data-ttu-id="04fe2-110">Die Startzeit für den Block, ausgedrückt in relativer Zeit.</span><span class="sxs-lookup"><span data-stu-id="04fe2-110">The start time for the block, expressed in relative time.</span></span> <span data-ttu-id="04fe2-111">Weitere Informationen finden Sie unter [Verwenden der relativen Zeit für den Zugriff auf Frei/Gebucht-Daten.](how-to-use-relative-time-to-access-free-busy-data.md)</span><span class="sxs-lookup"><span data-stu-id="04fe2-111">For more information, see [Use relative time to access free/busy data](how-to-use-relative-time-to-access-free-busy-data.md).</span></span>
    
<span data-ttu-id="04fe2-112">_m_tmEnd_</span><span class="sxs-lookup"><span data-stu-id="04fe2-112">_m_tmEnd_</span></span>
  
> <span data-ttu-id="04fe2-113">Die Endzeit für den Block, ausgedrückt in relativer Zeit.</span><span class="sxs-lookup"><span data-stu-id="04fe2-113">The end time for the block, expressed in relative time.</span></span>
    
<span data-ttu-id="04fe2-114">_m_fbStatus_</span><span class="sxs-lookup"><span data-stu-id="04fe2-114">_m_fbStatus_</span></span>
  
> <span data-ttu-id="04fe2-115">Der Frei/Gebucht-Status für diesen Block, der angibt, ob der Benutzer im Zeitraum zwischen  m_tmStart und m_tmEnd ist.</span><span class="sxs-lookup"><span data-stu-id="04fe2-115">The free/busy status for this block, indicating whether the user is out-of-office, busy, tentative, or free, during the time period between  _m_tmStart_ and  _m_tmEnd_.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="04fe2-116">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="04fe2-116">See also</span></span>

- [<span data-ttu-id="04fe2-117">FBStatus</span><span class="sxs-lookup"><span data-stu-id="04fe2-117">FBStatus</span></span>](fbstatus.md)
- [<span data-ttu-id="04fe2-118">IEnumFBBlock::Next</span><span class="sxs-lookup"><span data-stu-id="04fe2-118">IEnumFBBlock::Next</span></span>](ienumfbblock-next.md)
- [<span data-ttu-id="04fe2-119">Verwenden von relativer Zeit zum Zugriff auf Frei/Gebucht-Daten</span><span class="sxs-lookup"><span data-stu-id="04fe2-119">Use relative time to access free/busy data</span></span>](how-to-use-relative-time-to-access-free-busy-data.md)

