---
title: SNotRestriction
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.SNotRestriction
api_type:
- COM
ms.assetid: e86ca032-d973-4b79-976e-5240ab38a0da
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 174da93e7682246565b12c4fc4ffa6d1a9de065c
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2018
ms.locfileid: "22575063"
---
# <a name="snotrestriction"></a><span data-ttu-id="9bacc-103">SNotRestriction</span><span class="sxs-lookup"><span data-stu-id="9bacc-103">SNotRestriction</span></span>

  
  
<span data-ttu-id="9bacc-104">**Betrifft**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="9bacc-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="9bacc-105">Beschreibt eine **keine** Einschränkung, die mit der eine logische **NOT** -Operation, die eine Einschränkung angewendet.</span><span class="sxs-lookup"><span data-stu-id="9bacc-105">Describes a **NOT** restriction, which is used to apply a logical **NOT** operation to a restriction.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="9bacc-106">Headerdatei</span><span class="sxs-lookup"><span data-stu-id="9bacc-106">Header file:</span></span>  <br/> |<span data-ttu-id="9bacc-107">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="9bacc-107">Mapidefs.h</span></span>  <br/> |
   
```cpp
typedef struct _SNotRestriction
{
  ULONG ulReserved;
  LPSRestriction lpRes;
} SNotRestriction;

```

## <a name="members"></a><span data-ttu-id="9bacc-108">Elemente</span><span class="sxs-lookup"><span data-stu-id="9bacc-108">Members</span></span>

 <span data-ttu-id="9bacc-109">**ulReserved**</span><span class="sxs-lookup"><span data-stu-id="9bacc-109">**ulReserved**</span></span>
  
> <span data-ttu-id="9bacc-110">[in] Reserviert. NULL muss sein.</span><span class="sxs-lookup"><span data-stu-id="9bacc-110">[in] Reserved; must be zero.</span></span>
    
 <span data-ttu-id="9bacc-111">**lpRes**</span><span class="sxs-lookup"><span data-stu-id="9bacc-111">**lpRes**</span></span>
  
> <span data-ttu-id="9bacc-112">Zeiger auf eine [SRestriction](srestriction.md) -Struktur, beschreibt die Einschränkung wieder in den logischen Operator **NOT** aufgenommen werden.</span><span class="sxs-lookup"><span data-stu-id="9bacc-112">Pointer to a [SRestriction](srestriction.md) structure describing the restriction to be joined to the logical **NOT** operator.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="9bacc-113">HinwBemerkungeneise</span><span class="sxs-lookup"><span data-stu-id="9bacc-113">Remarks</span></span>

<span data-ttu-id="9bacc-114">Weitere Informationen zur Struktur **SNotRestriction** finden Sie unter [Informationen zu Einschränkungen](about-restrictions.md).</span><span class="sxs-lookup"><span data-stu-id="9bacc-114">For more information about the **SNotRestriction** structure, see [About Restrictions](about-restrictions.md).</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="9bacc-115">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="9bacc-115">See also</span></span>



[<span data-ttu-id="9bacc-116">SRestriction</span><span class="sxs-lookup"><span data-stu-id="9bacc-116">SRestriction</span></span>](srestriction.md)


[<span data-ttu-id="9bacc-117">MAPI-Strukturen</span><span class="sxs-lookup"><span data-stu-id="9bacc-117">MAPI Structures</span></span>](mapi-structures.md)

