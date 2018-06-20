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
ms.openlocfilehash: 635a4a872b83a2996b1a0198975a0ecd2cd906eb
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19792826"
---
# <a name="isequalmapiuid"></a><span data-ttu-id="67e3c-103">IsEqualMAPIUID</span><span class="sxs-lookup"><span data-stu-id="67e3c-103">IsEqualMAPIUID</span></span>

  
  
<span data-ttu-id="67e3c-104">**Betrifft**: Outlook</span><span class="sxs-lookup"><span data-stu-id="67e3c-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="67e3c-105">Testet zwei [MAPIUID](mapiuid.md) -Strukturen, um zu bestimmen, ob sie den gleichen Bezeichner enthalten.</span><span class="sxs-lookup"><span data-stu-id="67e3c-105">Tests two [MAPIUID](mapiuid.md) structures to determine whether they contain the same identifier.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="67e3c-106">Headerdatei</span><span class="sxs-lookup"><span data-stu-id="67e3c-106">Header file:</span></span>  <br/> |<span data-ttu-id="67e3c-107">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="67e3c-107">Mapidefs.h</span></span>  <br/> |
|<span data-ttu-id="67e3c-108">Verwandte Struktur:</span><span class="sxs-lookup"><span data-stu-id="67e3c-108">Related structure:</span></span>  <br/> |<span data-ttu-id="67e3c-109">**MAPIUID**</span><span class="sxs-lookup"><span data-stu-id="67e3c-109">**MAPIUID**</span></span> <br/> |
   
```cpp
IsEqualMAPIUID(lpuid1, lpuid2)
```

## <a name="parameters"></a><span data-ttu-id="67e3c-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="67e3c-110">Parameters</span></span>

 <span data-ttu-id="67e3c-111">_lpuid1_</span><span class="sxs-lookup"><span data-stu-id="67e3c-111">_lpuid1_</span></span>
  
> <span data-ttu-id="67e3c-112">Zeiger auf die erste **MAPIUID** Struktur auf getestet werden soll.</span><span class="sxs-lookup"><span data-stu-id="67e3c-112">Pointer to the first **MAPIUID** structure to be tested.</span></span> 
    
 <span data-ttu-id="67e3c-113">_lpuid2_</span><span class="sxs-lookup"><span data-stu-id="67e3c-113">_lpuid2_</span></span>
  
> <span data-ttu-id="67e3c-114">Zeiger auf die zweite **MAPIUID** Struktur auf getestet werden soll.</span><span class="sxs-lookup"><span data-stu-id="67e3c-114">Pointer to the second **MAPIUID** structure to be tested.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="67e3c-115">Hinweise</span><span class="sxs-lookup"><span data-stu-id="67e3c-115">Remarks</span></span>

<span data-ttu-id="67e3c-116">Das Makro **IsEqualMAPIUID** gibt TRUE zurück, wenn die zwei **MAPIUID** -Strukturen, die dieselbe ID und FALSE enthalten, wenn nicht der Fall ist.</span><span class="sxs-lookup"><span data-stu-id="67e3c-116">The **IsEqualMAPIUID** macro returns TRUE if the two **MAPIUID** structures contain the same identifier and FALSE if they do not.</span></span> 
  
<span data-ttu-id="67e3c-117">Das Makro **IsEqualMAPIUID** erfordert, dass die Headerdatei Memory.h enthalten sein.</span><span class="sxs-lookup"><span data-stu-id="67e3c-117">The **IsEqualMAPIUID** macro requires that the header file Memory.h be included.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="67e3c-118">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="67e3c-118">See also</span></span>



[<span data-ttu-id="67e3c-119">MAPIUID</span><span class="sxs-lookup"><span data-stu-id="67e3c-119">MAPIUID</span></span>](mapiuid.md)


[<span data-ttu-id="67e3c-120">Makros im Zusammenhang mit Strukturen</span><span class="sxs-lookup"><span data-stu-id="67e3c-120">Macros Related to Structures</span></span>](macros-related-to-structures.md)

