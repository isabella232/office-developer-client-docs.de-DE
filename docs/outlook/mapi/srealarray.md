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
ms.openlocfilehash: 8439d6609ebece75699a1150a9d0c1a41277fd52
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33429873"
---
# <a name="srealarray"></a><span data-ttu-id="3dd1d-103">SRealArray</span><span class="sxs-lookup"><span data-stu-id="3dd1d-103">SRealArray</span></span>

  
  
<span data-ttu-id="3dd1d-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="3dd1d-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="3dd1d-105">Enthält ein Array von Gleitkommawerten, die zum Beschreiben einer Eigenschaft vom Typ PT_MV_R4.</span><span class="sxs-lookup"><span data-stu-id="3dd1d-105">Contains an array of float values that are used to describe a property of type PT_MV_R4.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="3dd1d-106">Headerdatei</span><span class="sxs-lookup"><span data-stu-id="3dd1d-106">Header file:</span></span>  <br/> |<span data-ttu-id="3dd1d-107">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="3dd1d-107">Mapidefs.h</span></span>  <br/> |
   
```cpp
typedef struct _SRealArray
{
  ULONG cValues;
  float FAR *lpflt;
} SRealArray;

```

## <a name="members"></a><span data-ttu-id="3dd1d-108">Elemente</span><span class="sxs-lookup"><span data-stu-id="3dd1d-108">Members</span></span>

 <span data-ttu-id="3dd1d-109">**cValues**</span><span class="sxs-lookup"><span data-stu-id="3dd1d-109">**cValues**</span></span>
  
> <span data-ttu-id="3dd1d-110">Anzahl der Werte im Array, auf das das **lpflt-Element** verweist.</span><span class="sxs-lookup"><span data-stu-id="3dd1d-110">Count of values in the array pointed to by the **lpflt** member.</span></span> 
    
 <span data-ttu-id="3dd1d-111">**lpflt**</span><span class="sxs-lookup"><span data-stu-id="3dd1d-111">**lpflt**</span></span>
  
> <span data-ttu-id="3dd1d-112">Zeiger auf ein Array von Gleitkommawerten.</span><span class="sxs-lookup"><span data-stu-id="3dd1d-112">Pointer to an array of float values.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="3dd1d-113">Hinweise</span><span class="sxs-lookup"><span data-stu-id="3dd1d-113">Remarks</span></span>

<span data-ttu-id="3dd1d-114">Weitere Informationen zum eigenschaftentyp PT_MV_R4 finden Sie unter [Property Types](property-types.md).</span><span class="sxs-lookup"><span data-stu-id="3dd1d-114">For more information about the PT_MV_R4 property type, see [Property Types](property-types.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="3dd1d-115">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="3dd1d-115">See also</span></span>



[<span data-ttu-id="3dd1d-116">SPropValue</span><span class="sxs-lookup"><span data-stu-id="3dd1d-116">SPropValue</span></span>](spropvalue.md)


[<span data-ttu-id="3dd1d-117">MAPI-Strukturen</span><span class="sxs-lookup"><span data-stu-id="3dd1d-117">MAPI Structures</span></span>](mapi-structures.md)

