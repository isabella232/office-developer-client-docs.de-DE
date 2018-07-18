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
ms.openlocfilehash: c64e9a7497a70ea34dc09a5749dd281a24f9413d
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19795615"
---
# <a name="srealarray"></a><span data-ttu-id="58909-103">SRealArray</span><span class="sxs-lookup"><span data-stu-id="58909-103">SRealArray</span></span>

  
  
<span data-ttu-id="58909-104">**Betrifft**: Outlook</span><span class="sxs-lookup"><span data-stu-id="58909-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="58909-105">Enthält ein Array von Float-Werten, mit denen eine Eigenschaft vom Typ PT_MV_R4 beschrieben.</span><span class="sxs-lookup"><span data-stu-id="58909-105">Contains an array of float values that are used to describe a property of type PT_MV_R4.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="58909-106">Headerdatei</span><span class="sxs-lookup"><span data-stu-id="58909-106">Header file:</span></span>  <br/> |<span data-ttu-id="58909-107">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="58909-107">Mapidefs.h</span></span>  <br/> |
   
```cpp
typedef struct _SRealArray
{
  ULONG cValues;
  float FAR *lpflt;
} SRealArray;

```

## <a name="members"></a><span data-ttu-id="58909-108">Elemente</span><span class="sxs-lookup"><span data-stu-id="58909-108">Members</span></span>

 <span data-ttu-id="58909-109">**cValues**</span><span class="sxs-lookup"><span data-stu-id="58909-109">**cValues**</span></span>
  
> <span data-ttu-id="58909-110">Anzahl der Werte im Array auf den Member **Lpflt** zeigt.</span><span class="sxs-lookup"><span data-stu-id="58909-110">Count of values in the array pointed to by the **lpflt** member.</span></span> 
    
 <span data-ttu-id="58909-111">**lpflt**</span><span class="sxs-lookup"><span data-stu-id="58909-111">**lpflt**</span></span>
  
> <span data-ttu-id="58909-112">Zeiger auf ein Array von Float-Werten.</span><span class="sxs-lookup"><span data-stu-id="58909-112">Pointer to an array of float values.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="58909-113">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="58909-113">Remarks</span></span>

<span data-ttu-id="58909-114">Weitere Informationen zu den Eigenschaftentyp PT_MV_R4 finden Sie unter [Eigenschaftentypen](property-types.md).</span><span class="sxs-lookup"><span data-stu-id="58909-114">For more information about the PT_MV_R4 property type, see [Property Types](property-types.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="58909-115">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="58909-115">See also</span></span>



[<span data-ttu-id="58909-116">SPropValue</span><span class="sxs-lookup"><span data-stu-id="58909-116">SPropValue</span></span>](spropvalue.md)


[<span data-ttu-id="58909-117">MAPI-Strukturen</span><span class="sxs-lookup"><span data-stu-id="58909-117">MAPI Structures</span></span>](mapi-structures.md)

