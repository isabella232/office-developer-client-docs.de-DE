---
title: SOrRestriction
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.SOrRestriction
api_type:
- COM
ms.assetid: 6fee29ce-9a34-4e0c-bb71-03120c3f1117
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 054625601b496a8ec8f7745aa4cbc4715eed81a7
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2018
ms.locfileid: "22585059"
---
# <a name="sorrestriction"></a><span data-ttu-id="07817-103">SOrRestriction</span><span class="sxs-lookup"><span data-stu-id="07817-103">SOrRestriction</span></span>

  
  
<span data-ttu-id="07817-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="07817-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="07817-105">Beschreibt eine Einschränkung **oder** die verwendet wird, um eine logische **OR** -Operation, die eine Einschränkung anzuwenden.</span><span class="sxs-lookup"><span data-stu-id="07817-105">Describes an **OR** restriction which is used to apply a logical **OR** operation to a restriction.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="07817-106">Headerdatei</span><span class="sxs-lookup"><span data-stu-id="07817-106">Header file:</span></span>  <br/> |<span data-ttu-id="07817-107">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="07817-107">Mapidefs.h</span></span>  <br/> |
   
```cpp
typedef struct _SOrRestriction
{
  ULONG cRes;
  LPSRestriction lpRes;
} SOrRestriction;

```

## <a name="members"></a><span data-ttu-id="07817-108">Elemente</span><span class="sxs-lookup"><span data-stu-id="07817-108">Members</span></span>

 <span data-ttu-id="07817-109">**cRes**</span><span class="sxs-lookup"><span data-stu-id="07817-109">**cRes**</span></span>
  
> <span data-ttu-id="07817-110">Anzahl der im Array Strukturen auf der **LpRes** Member zeigt.</span><span class="sxs-lookup"><span data-stu-id="07817-110">Count of structures in the array pointed to by the **lpRes** member.</span></span> 
    
 <span data-ttu-id="07817-111">**lpRes**</span><span class="sxs-lookup"><span data-stu-id="07817-111">**lpRes**</span></span>
  
> <span data-ttu-id="07817-112">Zeiger auf die [SRestriction](srestriction.md) -Struktur, beschreibt die Einschränkung mithilfe des logischen Operators **OR** verknüpft werden.</span><span class="sxs-lookup"><span data-stu-id="07817-112">Pointer to the [SRestriction](srestriction.md) structure describing the restriction to be joined using the logical **OR** operation.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="07817-113">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="07817-113">Remarks</span></span>

<span data-ttu-id="07817-114">Weitere Informationen zur Struktur **SOrRestriction** finden Sie unter [Informationen zu Einschränkungen](about-restrictions.md).</span><span class="sxs-lookup"><span data-stu-id="07817-114">For more information about the **SOrRestriction** structure, see [About Restrictions](about-restrictions.md).</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="07817-115">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="07817-115">See also</span></span>



[<span data-ttu-id="07817-116">SRestriction</span><span class="sxs-lookup"><span data-stu-id="07817-116">SRestriction</span></span>](srestriction.md)


[<span data-ttu-id="07817-117">MAPI-Strukturen</span><span class="sxs-lookup"><span data-stu-id="07817-117">MAPI Structures</span></span>](mapi-structures.md)

