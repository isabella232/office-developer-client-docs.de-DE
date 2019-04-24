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
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: 9b1c5a09a60240efa9d4fa117f0d8fe8113169d5
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32361166"
---
# <a name="slongarray"></a><span data-ttu-id="f03a5-103">SLongArray</span><span class="sxs-lookup"><span data-stu-id="f03a5-103">SLongArray</span></span>

  
  
<span data-ttu-id="f03a5-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="f03a5-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="f03a5-105">Enthält ein Array von LONG-Werttypen, die zum Beschreiben einer Eigenschaft vom Typ PT_MV_LONG verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="f03a5-105">Contains an array of LONG value types that are used to describe a property of type PT_MV_LONG.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="f03a5-106">Headerdatei</span><span class="sxs-lookup"><span data-stu-id="f03a5-106">Header file:</span></span>  <br/> |<span data-ttu-id="f03a5-107">Mapidefs. h</span><span class="sxs-lookup"><span data-stu-id="f03a5-107">Mapidefs.h</span></span>  <br/> |
   
```cpp
typedef struct _SLongArray
{
  ULONG cValues;
  LONG FAR *lpl;
} SLongArray;

```

## <a name="members"></a><span data-ttu-id="f03a5-108">Elemente</span><span class="sxs-lookup"><span data-stu-id="f03a5-108">Members</span></span>

 <span data-ttu-id="f03a5-109">**cValues**</span><span class="sxs-lookup"><span data-stu-id="f03a5-109">**cValues**</span></span>
  
> <span data-ttu-id="f03a5-110">Die Anzahl der Werte im Array, auf die durch das **LPL** -Element verwiesen wird.</span><span class="sxs-lookup"><span data-stu-id="f03a5-110">Count of values in the array pointed to by the **lpl** member.</span></span> 
    
 <span data-ttu-id="f03a5-111">**LPL**</span><span class="sxs-lookup"><span data-stu-id="f03a5-111">**lpl**</span></span>
  
> <span data-ttu-id="f03a5-112">Zeiger auf ein Array von LONG-Werten.</span><span class="sxs-lookup"><span data-stu-id="f03a5-112">Pointer to an array of LONG values.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="f03a5-113">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="f03a5-113">Remarks</span></span>

<span data-ttu-id="f03a5-114">Weitere Informationen zu PT_MV_LONG finden Sie unter [Liste der Eigenschaftstypen](property-types.md).</span><span class="sxs-lookup"><span data-stu-id="f03a5-114">For more information about PT_MV_LONG, see [List of Property Types](property-types.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="f03a5-115">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="f03a5-115">See also</span></span>



[<span data-ttu-id="f03a5-116">SPropValue</span><span class="sxs-lookup"><span data-stu-id="f03a5-116">SPropValue</span></span>](spropvalue.md)


[<span data-ttu-id="f03a5-117">MAPI-Strukturen</span><span class="sxs-lookup"><span data-stu-id="f03a5-117">MAPI Structures</span></span>](mapi-structures.md)

