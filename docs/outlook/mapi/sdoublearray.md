---
title: SDoubleArray
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.SDoubleArray
api_type:
- COM
ms.assetid: b63b26de-faf9-453c-ab8b-fb703ed09ae8
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 91440d619c8ad8a64b2bac7463a26d9c196a3c0f
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33439268"
---
# <a name="sdoublearray"></a><span data-ttu-id="a3957-103">SDoubleArray</span><span class="sxs-lookup"><span data-stu-id="a3957-103">SDoubleArray</span></span>

  
  
<span data-ttu-id="a3957-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="a3957-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="a3957-105">Enthält ein Array von Doubles, die zum Beschreiben einer Eigenschaft vom Typ PT_MV_DOUBLE verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="a3957-105">Contains an array of doubles used to describe a property of type PT_MV_DOUBLE.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="a3957-106">Headerdatei</span><span class="sxs-lookup"><span data-stu-id="a3957-106">Header file:</span></span>  <br/> |<span data-ttu-id="a3957-107">Mapidefs. h</span><span class="sxs-lookup"><span data-stu-id="a3957-107">Mapidefs.h</span></span>  <br/> |
   
```cpp
typedef struct _SDoubleArray
{
  ULONG cValues;
  double FAR *lpdbl;
} SDoubleArray;

```

## <a name="members"></a><span data-ttu-id="a3957-108">Members</span><span class="sxs-lookup"><span data-stu-id="a3957-108">Members</span></span>

 <span data-ttu-id="a3957-109">**cValues**</span><span class="sxs-lookup"><span data-stu-id="a3957-109">**cValues**</span></span>
  
> <span data-ttu-id="a3957-110">Die Anzahl der Werte im Array, auf die durch das **lpdbl** -Element verwiesen wird.</span><span class="sxs-lookup"><span data-stu-id="a3957-110">Count of values in the array pointed to by the **lpdbl** member.</span></span> 
    
 <span data-ttu-id="a3957-111">**lpdbl**</span><span class="sxs-lookup"><span data-stu-id="a3957-111">**lpdbl**</span></span>
  
> <span data-ttu-id="a3957-112">Zeiger auf ein Array von Double-Werten.</span><span class="sxs-lookup"><span data-stu-id="a3957-112">Pointer to an array of double values.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="a3957-113">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="a3957-113">Remarks</span></span>

<span data-ttu-id="a3957-114">Weitere Informationen zu PT_MV_DOUBLE finden Sie unter [Liste der Eigenschaftstypen](property-types.md).</span><span class="sxs-lookup"><span data-stu-id="a3957-114">For more information about PT_MV_DOUBLE, see [List of Property Types](property-types.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="a3957-115">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="a3957-115">See also</span></span>



[<span data-ttu-id="a3957-116">SPropValue</span><span class="sxs-lookup"><span data-stu-id="a3957-116">SPropValue</span></span>](spropvalue.md)


[<span data-ttu-id="a3957-117">MAPI-Strukturen</span><span class="sxs-lookup"><span data-stu-id="a3957-117">MAPI Structures</span></span>](mapi-structures.md)

