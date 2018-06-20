---
title: FBBlock_1
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: da67171d-d25f-3424-1409-33189ac63a12
description: Definiert einen Datenblock Frei/Gebucht-Informationen. Dies ist ein Element in einem Kalender, dargestellt durch ein Termin oder einer Besprechungsanfrage.
ms.openlocfilehash: 93418e3777e9d9f0a016822ea5897b8fccc37ac3
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19790928"
---
# <a name="fbblock1"></a><span data-ttu-id="bce73-104">FBBlock_1</span><span class="sxs-lookup"><span data-stu-id="bce73-104">FBBlock_1</span></span>

<span data-ttu-id="bce73-105">Definiert einen Datenblock Frei/Gebucht-Informationen.</span><span class="sxs-lookup"><span data-stu-id="bce73-105">Defines a free/busy block of data.</span></span> <span data-ttu-id="bce73-106">Dies ist ein Element in einem Kalender, dargestellt durch ein Termin oder einer Besprechungsanfrage.</span><span class="sxs-lookup"><span data-stu-id="bce73-106">This is an item on a calendar represented by an appointment or meeting request.</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="bce73-107">QuickInfo</span><span class="sxs-lookup"><span data-stu-id="bce73-107">Quick info</span></span>

```cpp
typedef struct  tagFBBlock_1 
    { 
    long m_tmStart; 
    long m_tmEnd; 
    FBStatus m_fbstatus; 
    }FBBlock_1; 

```

## <a name="members"></a><span data-ttu-id="bce73-108">Members</span><span class="sxs-lookup"><span data-stu-id="bce73-108">Members</span></span>

<span data-ttu-id="bce73-109">_m_tmStart_</span><span class="sxs-lookup"><span data-stu-id="bce73-109">_m_tmStart_</span></span>
  
> <span data-ttu-id="bce73-110">Die Startzeit für den Block, ausgedrückt als relative Zeit.</span><span class="sxs-lookup"><span data-stu-id="bce73-110">The start time for the block, expressed in relative time.</span></span> <span data-ttu-id="bce73-111">Weitere Informationen finden Sie unter [Verwendung relative Zeit auf Frei/Gebucht-Daten zugreifen](how-to-use-relative-time-to-access-free-busy-data.md).</span><span class="sxs-lookup"><span data-stu-id="bce73-111">For more information, see [Use relative time to access free/busy data](how-to-use-relative-time-to-access-free-busy-data.md).</span></span>
    
<span data-ttu-id="bce73-112">_m_tmEnd_</span><span class="sxs-lookup"><span data-stu-id="bce73-112">_m_tmEnd_</span></span>
  
> <span data-ttu-id="bce73-113">Die Endzeit für das blockieren, ausgedrückt als relative Zeit.</span><span class="sxs-lookup"><span data-stu-id="bce73-113">The end time for the block, expressed in relative time.</span></span>
    
<span data-ttu-id="bce73-114">_m_fbStatus_</span><span class="sxs-lookup"><span data-stu-id="bce73-114">_m_fbStatus_</span></span>
  
> <span data-ttu-id="bce73-115">Der Frei/Gebucht-Status für diese-Blocks ungültig; zurück, der angibt, ob der Benutzer während des Zeitraums zwischen _M_tmStart_ und _M_tmEnd_Abwesenheits, gebucht, mit Vorbehalt oder frei ist.</span><span class="sxs-lookup"><span data-stu-id="bce73-115">The free/busy status for this block, indicating whether the user is out-of-office, busy, tentative, or free, during the time period between  _m_tmStart_ and  _m_tmEnd_.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="bce73-116">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="bce73-116">See also</span></span>

- [<span data-ttu-id="bce73-117">FBStatus</span><span class="sxs-lookup"><span data-stu-id="bce73-117">FBStatus</span></span>](fbstatus.md)
- [<span data-ttu-id="bce73-118">IEnumFBBlock::Next</span><span class="sxs-lookup"><span data-stu-id="bce73-118">IEnumFBBlock::Next</span></span>](ienumfbblock-next.md)
- [<span data-ttu-id="bce73-119">Verwenden Sie relative Zeit Zugriff auf Frei/Gebucht-Daten</span><span class="sxs-lookup"><span data-stu-id="bce73-119">Use relative time to access free/busy data</span></span>](how-to-use-relative-time-to-access-free-busy-data.md)

