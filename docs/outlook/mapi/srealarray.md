---
title: SRealArray
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.SRealArray
api_type:
- COM
ms.assetid: 95be07bf-5732-4775-9e0f-fec47e99d9b7
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: 8439d6609ebece75699a1150a9d0c1a41277fd52
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32344380"
---
# <a name="srealarray"></a><span data-ttu-id="7a926-103">SRealArray</span><span class="sxs-lookup"><span data-stu-id="7a926-103">SRealArray</span></span>

  
  
<span data-ttu-id="7a926-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="7a926-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="7a926-105">Enthält ein Array von float-Werten, die zum Beschreiben einer Eigenschaft vom Typ PT_MV_R4 verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="7a926-105">Contains an array of float values that are used to describe a property of type PT_MV_R4.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="7a926-106">Headerdatei</span><span class="sxs-lookup"><span data-stu-id="7a926-106">Header file:</span></span>  <br/> |<span data-ttu-id="7a926-107">Mapidefs. h</span><span class="sxs-lookup"><span data-stu-id="7a926-107">Mapidefs.h</span></span>  <br/> |
   
```cpp
typedef struct _SRealArray
{
  ULONG cValues;
  float FAR *lpflt;
} SRealArray;

```

## <a name="members"></a><span data-ttu-id="7a926-108">Elemente</span><span class="sxs-lookup"><span data-stu-id="7a926-108">Members</span></span>

 <span data-ttu-id="7a926-109">**cValues**</span><span class="sxs-lookup"><span data-stu-id="7a926-109">**cValues**</span></span>
  
> <span data-ttu-id="7a926-110">Die Anzahl der Werte im Array, auf die durch das **lpflt** -Element verwiesen wird.</span><span class="sxs-lookup"><span data-stu-id="7a926-110">Count of values in the array pointed to by the **lpflt** member.</span></span> 
    
 <span data-ttu-id="7a926-111">**lpflt**</span><span class="sxs-lookup"><span data-stu-id="7a926-111">**lpflt**</span></span>
  
> <span data-ttu-id="7a926-112">Zeiger auf ein Array von float-Werten.</span><span class="sxs-lookup"><span data-stu-id="7a926-112">Pointer to an array of float values.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="7a926-113">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="7a926-113">Remarks</span></span>

<span data-ttu-id="7a926-114">Weitere Informationen zum PT_MV_R4-Eigenschaftentyp finden Sie unter [Property](property-types.md)Types.</span><span class="sxs-lookup"><span data-stu-id="7a926-114">For more information about the PT_MV_R4 property type, see [Property Types](property-types.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="7a926-115">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="7a926-115">See also</span></span>



[<span data-ttu-id="7a926-116">SPropValue</span><span class="sxs-lookup"><span data-stu-id="7a926-116">SPropValue</span></span>](spropvalue.md)


[<span data-ttu-id="7a926-117">MAPI-Strukturen</span><span class="sxs-lookup"><span data-stu-id="7a926-117">MAPI Structures</span></span>](mapi-structures.md)

