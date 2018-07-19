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
ms.openlocfilehash: a07a7737e9b9354514a2d5ac2ec37a393a3cd4e4
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19795589"
---
# <a name="snotrestriction"></a><span data-ttu-id="30a6e-103">SNotRestriction</span><span class="sxs-lookup"><span data-stu-id="30a6e-103">SNotRestriction</span></span>

  
  
<span data-ttu-id="30a6e-104">**Betrifft**: Outlook</span><span class="sxs-lookup"><span data-stu-id="30a6e-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="30a6e-105">Beschreibt eine **keine** Einschränkung, die mit der eine logische **NOT** -Operation, die eine Einschränkung angewendet.</span><span class="sxs-lookup"><span data-stu-id="30a6e-105">Describes a **NOT** restriction, which is used to apply a logical **NOT** operation to a restriction.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="30a6e-106">Headerdatei</span><span class="sxs-lookup"><span data-stu-id="30a6e-106">Header file:</span></span>  <br/> |<span data-ttu-id="30a6e-107">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="30a6e-107">Mapidefs.h</span></span>  <br/> |
   
```cpp
typedef struct _SNotRestriction
{
  ULONG ulReserved;
  LPSRestriction lpRes;
} SNotRestriction;

```

## <a name="members"></a><span data-ttu-id="30a6e-108">Elemente</span><span class="sxs-lookup"><span data-stu-id="30a6e-108">Members</span></span>

 <span data-ttu-id="30a6e-109">**ulReserved**</span><span class="sxs-lookup"><span data-stu-id="30a6e-109">**ulReserved**</span></span>
  
> <span data-ttu-id="30a6e-110">[in] Reserviert. NULL muss sein.</span><span class="sxs-lookup"><span data-stu-id="30a6e-110">[in] Reserved; must be zero.</span></span>
    
 <span data-ttu-id="30a6e-111">**lpRes**</span><span class="sxs-lookup"><span data-stu-id="30a6e-111">**lpRes**</span></span>
  
> <span data-ttu-id="30a6e-112">Zeiger auf eine [SRestriction](srestriction.md) -Struktur, beschreibt die Einschränkung wieder in den logischen Operator **NOT** aufgenommen werden.</span><span class="sxs-lookup"><span data-stu-id="30a6e-112">Pointer to a [SRestriction](srestriction.md) structure describing the restriction to be joined to the logical **NOT** operator.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="30a6e-113">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="30a6e-113">Remarks</span></span>

<span data-ttu-id="30a6e-114">Weitere Informationen zur Struktur **SNotRestriction** finden Sie unter [Informationen zu Einschränkungen](about-restrictions.md).</span><span class="sxs-lookup"><span data-stu-id="30a6e-114">For more information about the **SNotRestriction** structure, see [About Restrictions](about-restrictions.md).</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="30a6e-115">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="30a6e-115">See also</span></span>



[<span data-ttu-id="30a6e-116">SRestriction</span><span class="sxs-lookup"><span data-stu-id="30a6e-116">SRestriction</span></span>](srestriction.md)


[<span data-ttu-id="30a6e-117">MAPI-Strukturen</span><span class="sxs-lookup"><span data-stu-id="30a6e-117">MAPI Structures</span></span>](mapi-structures.md)

