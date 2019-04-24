---
title: IsEqualMAPIUID
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.IsEqualMAPIUID
api_type:
- COM
ms.assetid: 85d71b73-0630-4c5d-b0e3-b48d27a300d0
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: 44e3613338c8932bc80dd1150392033dfa3cd050
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32278736"
---
# <a name="isequalmapiuid"></a><span data-ttu-id="e7687-103">IsEqualMAPIUID</span><span class="sxs-lookup"><span data-stu-id="e7687-103">IsEqualMAPIUID</span></span>

  
  
<span data-ttu-id="e7687-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="e7687-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="e7687-105">Testet zwei [MAPIUID](mapiuid.md) -Strukturen, um zu bestimmen, ob Sie den gleichen Bezeichner enthalten.</span><span class="sxs-lookup"><span data-stu-id="e7687-105">Tests two [MAPIUID](mapiuid.md) structures to determine whether they contain the same identifier.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="e7687-106">Headerdatei</span><span class="sxs-lookup"><span data-stu-id="e7687-106">Header file:</span></span>  <br/> |<span data-ttu-id="e7687-107">Mapidefs. h</span><span class="sxs-lookup"><span data-stu-id="e7687-107">Mapidefs.h</span></span>  <br/> |
|<span data-ttu-id="e7687-108">Zugehörige Struktur:</span><span class="sxs-lookup"><span data-stu-id="e7687-108">Related structure:</span></span>  <br/> |<span data-ttu-id="e7687-109">**MAPIUID**</span><span class="sxs-lookup"><span data-stu-id="e7687-109">**MAPIUID**</span></span> <br/> |
   
```cpp
IsEqualMAPIUID(lpuid1, lpuid2)
```

## <a name="parameters"></a><span data-ttu-id="e7687-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="e7687-110">Parameters</span></span>

 <span data-ttu-id="e7687-111">_lpuid1_</span><span class="sxs-lookup"><span data-stu-id="e7687-111">_lpuid1_</span></span>
  
> <span data-ttu-id="e7687-112">Zeiger auf die erste zu testende **MAPIUID** -Struktur.</span><span class="sxs-lookup"><span data-stu-id="e7687-112">Pointer to the first **MAPIUID** structure to be tested.</span></span> 
    
 <span data-ttu-id="e7687-113">_lpuid2_</span><span class="sxs-lookup"><span data-stu-id="e7687-113">_lpuid2_</span></span>
  
> <span data-ttu-id="e7687-114">Zeiger auf die zweite zu testende **MAPIUID** -Struktur.</span><span class="sxs-lookup"><span data-stu-id="e7687-114">Pointer to the second **MAPIUID** structure to be tested.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="e7687-115">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="e7687-115">Remarks</span></span>

<span data-ttu-id="e7687-116">Das **IsEqualMAPIUID** -Makro gibt true zurück, wenn die beiden **MAPIUID** -Strukturen denselben Bezeichner enthalten, und false, wenn dies nicht der Fall ist.</span><span class="sxs-lookup"><span data-stu-id="e7687-116">The **IsEqualMAPIUID** macro returns TRUE if the two **MAPIUID** structures contain the same identifier and FALSE if they do not.</span></span> 
  
<span data-ttu-id="e7687-117">Das **IsEqualMAPIUID** -Makro erfordert, dass die Headerdatei Memory. h enthalten ist.</span><span class="sxs-lookup"><span data-stu-id="e7687-117">The **IsEqualMAPIUID** macro requires that the header file Memory.h be included.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="e7687-118">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="e7687-118">See also</span></span>



[<span data-ttu-id="e7687-119">MAPIUID</span><span class="sxs-lookup"><span data-stu-id="e7687-119">MAPIUID</span></span>](mapiuid.md)


[<span data-ttu-id="e7687-120">Makros im Zusammenhang mit Strukturen</span><span class="sxs-lookup"><span data-stu-id="e7687-120">Macros Related to Structures</span></span>](macros-related-to-structures.md)

