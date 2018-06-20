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
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: cde59b73381458533910dc8f0a728cc4e6ca0c01
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19795476"
---
# <a name="sdoublearray"></a><span data-ttu-id="a9d49-103">SDoubleArray</span><span class="sxs-lookup"><span data-stu-id="a9d49-103">SDoubleArray</span></span>

  
  
<span data-ttu-id="a9d49-104">**Betrifft**: Outlook</span><span class="sxs-lookup"><span data-stu-id="a9d49-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="a9d49-105">Enthält ein Array von Double-Werte verwendet, um eine Eigenschaft vom Typ PT_MV_DOUBLE beschrieben.</span><span class="sxs-lookup"><span data-stu-id="a9d49-105">Contains an array of doubles used to describe a property of type PT_MV_DOUBLE.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="a9d49-106">Headerdatei</span><span class="sxs-lookup"><span data-stu-id="a9d49-106">Header file:</span></span>  <br/> |<span data-ttu-id="a9d49-107">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="a9d49-107">Mapidefs.h</span></span>  <br/> |
   
```cpp
typedef struct _SDoubleArray
{
  ULONG cValues;
  double FAR *lpdbl;
} SDoubleArray;

```

## <a name="members"></a><span data-ttu-id="a9d49-108">Members</span><span class="sxs-lookup"><span data-stu-id="a9d49-108">Members</span></span>

 <span data-ttu-id="a9d49-109">**cValues**</span><span class="sxs-lookup"><span data-stu-id="a9d49-109">**cValues**</span></span>
  
> <span data-ttu-id="a9d49-110">Anzahl der Werte im Array auf den Member **Lpdbl** zeigt.</span><span class="sxs-lookup"><span data-stu-id="a9d49-110">Count of values in the array pointed to by the **lpdbl** member.</span></span> 
    
 <span data-ttu-id="a9d49-111">**lpdbl**</span><span class="sxs-lookup"><span data-stu-id="a9d49-111">**lpdbl**</span></span>
  
> <span data-ttu-id="a9d49-112">Zeiger auf ein Array von double-Werte.</span><span class="sxs-lookup"><span data-stu-id="a9d49-112">Pointer to an array of double values.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="a9d49-113">Hinweise</span><span class="sxs-lookup"><span data-stu-id="a9d49-113">Remarks</span></span>

<span data-ttu-id="a9d49-114">Weitere Informationen zu PT_MV_DOUBLE finden Sie unter [Liste der Eigenschaftentypen](property-types.md).</span><span class="sxs-lookup"><span data-stu-id="a9d49-114">For more information about PT_MV_DOUBLE, see [List of Property Types](property-types.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="a9d49-115">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="a9d49-115">See also</span></span>



[<span data-ttu-id="a9d49-116">SPropValue</span><span class="sxs-lookup"><span data-stu-id="a9d49-116">SPropValue</span></span>](spropvalue.md)


[<span data-ttu-id="a9d49-117">MAPI-Strukturen</span><span class="sxs-lookup"><span data-stu-id="a9d49-117">MAPI Structures</span></span>](mapi-structures.md)

