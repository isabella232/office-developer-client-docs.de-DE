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
ms.openlocfilehash: 07a1a0a1953d136da534fbdc6339d326c877bebf
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33426653"
---
# <a name="snotrestriction"></a><span data-ttu-id="2d0ef-103">SNotRestriction</span><span class="sxs-lookup"><span data-stu-id="2d0ef-103">SNotRestriction</span></span>

  
  
<span data-ttu-id="2d0ef-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="2d0ef-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="2d0ef-105">Beschreibt eine **NOT-Einschränkung,** die zum Anwenden eines logischen **NOT-Vorgangs** auf eine Einschränkung verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="2d0ef-105">Describes a **NOT** restriction, which is used to apply a logical **NOT** operation to a restriction.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="2d0ef-106">Headerdatei</span><span class="sxs-lookup"><span data-stu-id="2d0ef-106">Header file:</span></span>  <br/> |<span data-ttu-id="2d0ef-107">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="2d0ef-107">Mapidefs.h</span></span>  <br/> |
   
```cpp
typedef struct _SNotRestriction
{
  ULONG ulReserved;
  LPSRestriction lpRes;
} SNotRestriction;

```

## <a name="members"></a><span data-ttu-id="2d0ef-108">Elemente</span><span class="sxs-lookup"><span data-stu-id="2d0ef-108">Members</span></span>

 <span data-ttu-id="2d0ef-109">**ulReserved**</span><span class="sxs-lookup"><span data-stu-id="2d0ef-109">**ulReserved**</span></span>
  
> <span data-ttu-id="2d0ef-110">[in] Reserviert. NULL muss sein.</span><span class="sxs-lookup"><span data-stu-id="2d0ef-110">[in] Reserved; must be zero.</span></span>
    
 <span data-ttu-id="2d0ef-111">**lpRes**</span><span class="sxs-lookup"><span data-stu-id="2d0ef-111">**lpRes**</span></span>
  
> <span data-ttu-id="2d0ef-112">Zeiger auf eine [SRestriction-Struktur,](srestriction.md) die die Einschränkung beschreibt, die mit dem logischen **NOT-Operator verbunden werden** soll.</span><span class="sxs-lookup"><span data-stu-id="2d0ef-112">Pointer to a [SRestriction](srestriction.md) structure describing the restriction to be joined to the logical **NOT** operator.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="2d0ef-113">Hinweise</span><span class="sxs-lookup"><span data-stu-id="2d0ef-113">Remarks</span></span>

<span data-ttu-id="2d0ef-114">Weitere Informationen zur **SNotRestriction-Struktur** finden Sie unter [Informationen zu Einschränkungen](about-restrictions.md).</span><span class="sxs-lookup"><span data-stu-id="2d0ef-114">For more information about the **SNotRestriction** structure, see [About Restrictions](about-restrictions.md).</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="2d0ef-115">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="2d0ef-115">See also</span></span>



[<span data-ttu-id="2d0ef-116">SRestriction</span><span class="sxs-lookup"><span data-stu-id="2d0ef-116">SRestriction</span></span>](srestriction.md)


[<span data-ttu-id="2d0ef-117">MAPI-Strukturen</span><span class="sxs-lookup"><span data-stu-id="2d0ef-117">MAPI Structures</span></span>](mapi-structures.md)

