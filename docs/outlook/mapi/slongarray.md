---
title: SLongArray
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.SLongArray
api_type:
- COM
ms.assetid: 57435634-202d-4998-9931-4562f1a66f5f
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: c207b1db6a24cc60967735e2f4b1a4aa97007750
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19795566"
---
# <a name="slongarray"></a><span data-ttu-id="b103d-103">SLongArray</span><span class="sxs-lookup"><span data-stu-id="b103d-103">SLongArray</span></span>

  
  
<span data-ttu-id="b103d-104">**Betrifft**: Outlook</span><span class="sxs-lookup"><span data-stu-id="b103d-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="b103d-105">Enthält ein Array von LONG-Werttypen, mit denen eine Eigenschaft vom Typ PT_MV_LONG beschrieben.</span><span class="sxs-lookup"><span data-stu-id="b103d-105">Contains an array of LONG value types that are used to describe a property of type PT_MV_LONG.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="b103d-106">Headerdatei</span><span class="sxs-lookup"><span data-stu-id="b103d-106">Header file:</span></span>  <br/> |<span data-ttu-id="b103d-107">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="b103d-107">Mapidefs.h</span></span>  <br/> |
   
```cpp
typedef struct _SLongArray
{
  ULONG cValues;
  LONG FAR *lpl;
} SLongArray;

```

## <a name="members"></a><span data-ttu-id="b103d-108">Elemente</span><span class="sxs-lookup"><span data-stu-id="b103d-108">Members</span></span>

 <span data-ttu-id="b103d-109">**cValues**</span><span class="sxs-lookup"><span data-stu-id="b103d-109">**cValues**</span></span>
  
> <span data-ttu-id="b103d-110">Anzahl der Werte im Array auf den Member **Lpl** zeigt.</span><span class="sxs-lookup"><span data-stu-id="b103d-110">Count of values in the array pointed to by the **lpl** member.</span></span> 
    
 <span data-ttu-id="b103d-111">**LPL**</span><span class="sxs-lookup"><span data-stu-id="b103d-111">**lpl**</span></span>
  
> <span data-ttu-id="b103d-112">Zeiger auf ein Array von LONG-Werte.</span><span class="sxs-lookup"><span data-stu-id="b103d-112">Pointer to an array of LONG values.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="b103d-113">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="b103d-113">Remarks</span></span>

<span data-ttu-id="b103d-114">Weitere Informationen zu PT_MV_LONG finden Sie unter [Liste der Eigenschaftentypen](property-types.md).</span><span class="sxs-lookup"><span data-stu-id="b103d-114">For more information about PT_MV_LONG, see [List of Property Types](property-types.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="b103d-115">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="b103d-115">See also</span></span>



[<span data-ttu-id="b103d-116">SPropValue</span><span class="sxs-lookup"><span data-stu-id="b103d-116">SPropValue</span></span>](spropvalue.md)


[<span data-ttu-id="b103d-117">MAPI-Strukturen</span><span class="sxs-lookup"><span data-stu-id="b103d-117">MAPI Structures</span></span>](mapi-structures.md)

