---
title: SLargeIntegerArray
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.SLargeIntegerArray
api_type:
- COM
ms.assetid: 9ec9a674-c1a2-4137-856f-6cabe6f0eb9f
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: ab82fff2645a5e1861523eb3f1866e0ddc7d13a5
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/04/2018
ms.locfileid: "25382729"
---
# <a name="slargeintegerarray"></a><span data-ttu-id="c1945-103">SLargeIntegerArray</span><span class="sxs-lookup"><span data-stu-id="c1945-103">SLargeIntegerArray</span></span>

  
  
<span data-ttu-id="c1945-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="c1945-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="c1945-105">Enthält ein Array von [LARGE_INTEGER](https://go.microsoft.com/fwlink/?LinkId=132130) -Strukturen, die verwendet werden, um eine Eigenschaft vom Typ PT_MV_I8 beschrieben.</span><span class="sxs-lookup"><span data-stu-id="c1945-105">Contains an array of [LARGE_INTEGER](https://go.microsoft.com/fwlink/?LinkId=132130) structures that are used to describe a property of type PT_MV_I8.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="c1945-106">Headerdatei:</span><span class="sxs-lookup"><span data-stu-id="c1945-106">Header file:</span></span>  <br/> |<span data-ttu-id="c1945-107">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="c1945-107">Mapidefs.h</span></span>  <br/> |
   
```cpp
typedef struct _SLargeIntegerArray
{
  ULONG cValues;
  LARGE_INTEGER FAR *lpli;
} SLargeIntegerArray;

```

## <a name="members"></a><span data-ttu-id="c1945-108">Elemente</span><span class="sxs-lookup"><span data-stu-id="c1945-108">Members</span></span>

 <span data-ttu-id="c1945-109">**cValues**</span><span class="sxs-lookup"><span data-stu-id="c1945-109">**cValues**</span></span>
  
> <span data-ttu-id="c1945-110">Anzahl der Werte im Array auf den Member **Lpli** zeigt.</span><span class="sxs-lookup"><span data-stu-id="c1945-110">Count of values in the array pointed to by the **lpli** member.</span></span> 
    
 <span data-ttu-id="c1945-111">**lpli**</span><span class="sxs-lookup"><span data-stu-id="c1945-111">**lpli**</span></span>
  
> <span data-ttu-id="c1945-112">Zeiger auf ein Array von **LARGE_INTEGER** Strukturen, indem Sie die Werte für ganze Zahl.</span><span class="sxs-lookup"><span data-stu-id="c1945-112">Pointer to an array of **LARGE_INTEGER** structures holding the integer values.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="c1945-113">Hinweise</span><span class="sxs-lookup"><span data-stu-id="c1945-113">Remarks</span></span>

<span data-ttu-id="c1945-114">Weitere Informationen zu PT_MV_18 finden Sie unter [Liste der Eigenschaftentypen](property-types.md).</span><span class="sxs-lookup"><span data-stu-id="c1945-114">For more information about PT_MV_18, see [List of Property Types](property-types.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="c1945-115">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="c1945-115">See also</span></span>



[<span data-ttu-id="c1945-116">SPropValue</span><span class="sxs-lookup"><span data-stu-id="c1945-116">SPropValue</span></span>](spropvalue.md)


[<span data-ttu-id="c1945-117">MAPI-Strukturen</span><span class="sxs-lookup"><span data-stu-id="c1945-117">MAPI Structures</span></span>](mapi-structures.md)

