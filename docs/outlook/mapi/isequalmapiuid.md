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
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 0c72164cac8a37d0372ac93f4ed6d3face966ddb
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2018
ms.locfileid: "22566663"
---
# <a name="isequalmapiuid"></a><span data-ttu-id="8ecb6-103">IsEqualMAPIUID</span><span class="sxs-lookup"><span data-stu-id="8ecb6-103">IsEqualMAPIUID</span></span>

  
  
<span data-ttu-id="8ecb6-104">**Betrifft**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="8ecb6-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="8ecb6-105">Testet zwei [MAPIUID](mapiuid.md) -Strukturen, um zu bestimmen, ob sie den gleichen Bezeichner enthalten.</span><span class="sxs-lookup"><span data-stu-id="8ecb6-105">Tests two [MAPIUID](mapiuid.md) structures to determine whether they contain the same identifier.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="8ecb6-106">Headerdatei</span><span class="sxs-lookup"><span data-stu-id="8ecb6-106">Header file:</span></span>  <br/> |<span data-ttu-id="8ecb6-107">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="8ecb6-107">Mapidefs.h</span></span>  <br/> |
|<span data-ttu-id="8ecb6-108">Verwandte Struktur:</span><span class="sxs-lookup"><span data-stu-id="8ecb6-108">Related structure:</span></span>  <br/> |<span data-ttu-id="8ecb6-109">**MAPIUID**</span><span class="sxs-lookup"><span data-stu-id="8ecb6-109">**MAPIUID**</span></span> <br/> |
   
```cpp
IsEqualMAPIUID(lpuid1, lpuid2)
```

## <a name="parameters"></a><span data-ttu-id="8ecb6-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="8ecb6-110">Parameters</span></span>

 <span data-ttu-id="8ecb6-111">_lpuid1_</span><span class="sxs-lookup"><span data-stu-id="8ecb6-111">_lpuid1_</span></span>
  
> <span data-ttu-id="8ecb6-112">Zeiger auf die erste **MAPIUID** Struktur auf getestet werden soll.</span><span class="sxs-lookup"><span data-stu-id="8ecb6-112">Pointer to the first **MAPIUID** structure to be tested.</span></span> 
    
 <span data-ttu-id="8ecb6-113">_lpuid2_</span><span class="sxs-lookup"><span data-stu-id="8ecb6-113">_lpuid2_</span></span>
  
> <span data-ttu-id="8ecb6-114">Zeiger auf die zweite **MAPIUID** Struktur auf getestet werden soll.</span><span class="sxs-lookup"><span data-stu-id="8ecb6-114">Pointer to the second **MAPIUID** structure to be tested.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="8ecb6-115">HinwBemerkungeneise</span><span class="sxs-lookup"><span data-stu-id="8ecb6-115">Remarks</span></span>

<span data-ttu-id="8ecb6-116">Das Makro **IsEqualMAPIUID** gibt TRUE zurück, wenn die zwei **MAPIUID** -Strukturen, die dieselbe ID und FALSE enthalten, wenn nicht der Fall ist.</span><span class="sxs-lookup"><span data-stu-id="8ecb6-116">The **IsEqualMAPIUID** macro returns TRUE if the two **MAPIUID** structures contain the same identifier and FALSE if they do not.</span></span> 
  
<span data-ttu-id="8ecb6-117">Das Makro **IsEqualMAPIUID** erfordert, dass die Headerdatei Memory.h enthalten sein.</span><span class="sxs-lookup"><span data-stu-id="8ecb6-117">The **IsEqualMAPIUID** macro requires that the header file Memory.h be included.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="8ecb6-118">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="8ecb6-118">See also</span></span>



[<span data-ttu-id="8ecb6-119">MAPIUID</span><span class="sxs-lookup"><span data-stu-id="8ecb6-119">MAPIUID</span></span>](mapiuid.md)


[<span data-ttu-id="8ecb6-120">Makros im Zusammenhang mit Strukturen</span><span class="sxs-lookup"><span data-stu-id="8ecb6-120">Macros Related to Structures</span></span>](macros-related-to-structures.md)

