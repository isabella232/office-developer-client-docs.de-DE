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
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 8c7ce2805248bf91ce7da071c67ece28a5b8ca07
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2018
ms.locfileid: "22564283"
---
# <a name="srealarray"></a><span data-ttu-id="7247c-103">SRealArray</span><span class="sxs-lookup"><span data-stu-id="7247c-103">SRealArray</span></span>

  
  
<span data-ttu-id="7247c-104">**Betrifft**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="7247c-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="7247c-105">Enthält ein Array von Float-Werten, mit denen eine Eigenschaft vom Typ PT_MV_R4 beschrieben.</span><span class="sxs-lookup"><span data-stu-id="7247c-105">Contains an array of float values that are used to describe a property of type PT_MV_R4.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="7247c-106">Headerdatei</span><span class="sxs-lookup"><span data-stu-id="7247c-106">Header file:</span></span>  <br/> |<span data-ttu-id="7247c-107">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="7247c-107">Mapidefs.h</span></span>  <br/> |
   
```cpp
typedef struct _SRealArray
{
  ULONG cValues;
  float FAR *lpflt;
} SRealArray;

```

## <a name="members"></a><span data-ttu-id="7247c-108">Elemente</span><span class="sxs-lookup"><span data-stu-id="7247c-108">Members</span></span>

 <span data-ttu-id="7247c-109">**cValues**</span><span class="sxs-lookup"><span data-stu-id="7247c-109">**cValues**</span></span>
  
> <span data-ttu-id="7247c-110">Anzahl der Werte im Array auf den Member **Lpflt** zeigt.</span><span class="sxs-lookup"><span data-stu-id="7247c-110">Count of values in the array pointed to by the **lpflt** member.</span></span> 
    
 <span data-ttu-id="7247c-111">**lpflt**</span><span class="sxs-lookup"><span data-stu-id="7247c-111">**lpflt**</span></span>
  
> <span data-ttu-id="7247c-112">Zeiger auf ein Array von Float-Werten.</span><span class="sxs-lookup"><span data-stu-id="7247c-112">Pointer to an array of float values.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="7247c-113">HinwBemerkungeneise</span><span class="sxs-lookup"><span data-stu-id="7247c-113">Remarks</span></span>

<span data-ttu-id="7247c-114">Weitere Informationen zu den Eigenschaftentyp PT_MV_R4 finden Sie unter [Eigenschaftentypen](property-types.md).</span><span class="sxs-lookup"><span data-stu-id="7247c-114">For more information about the PT_MV_R4 property type, see [Property Types](property-types.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="7247c-115">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="7247c-115">See also</span></span>



[<span data-ttu-id="7247c-116">SPropValue</span><span class="sxs-lookup"><span data-stu-id="7247c-116">SPropValue</span></span>](spropvalue.md)


[<span data-ttu-id="7247c-117">MAPI-Strukturen</span><span class="sxs-lookup"><span data-stu-id="7247c-117">MAPI Structures</span></span>](mapi-structures.md)

