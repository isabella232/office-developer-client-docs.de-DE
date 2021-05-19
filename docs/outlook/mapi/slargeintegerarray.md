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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32331388"
---
# <a name="slargeintegerarray"></a><span data-ttu-id="50d5f-103">SLargeIntegerArray</span><span class="sxs-lookup"><span data-stu-id="50d5f-103">SLargeIntegerArray</span></span>

  
  
<span data-ttu-id="50d5f-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="50d5f-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="50d5f-105">Enthält ein Array [von LARGE_INTEGER](https://go.microsoft.com/fwlink/?LinkId=132130) Strukturen, die zum Beschreiben einer Eigenschaft vom Typ PT_MV_I8.</span><span class="sxs-lookup"><span data-stu-id="50d5f-105">Contains an array of [LARGE_INTEGER](https://go.microsoft.com/fwlink/?LinkId=132130) structures that are used to describe a property of type PT_MV_I8.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="50d5f-106">Headerdatei</span><span class="sxs-lookup"><span data-stu-id="50d5f-106">Header file:</span></span>  <br/> |<span data-ttu-id="50d5f-107">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="50d5f-107">Mapidefs.h</span></span>  <br/> |
   
```cpp
typedef struct _SLargeIntegerArray
{
  ULONG cValues;
  LARGE_INTEGER FAR *lpli;
} SLargeIntegerArray;

```

## <a name="members"></a><span data-ttu-id="50d5f-108">Elemente</span><span class="sxs-lookup"><span data-stu-id="50d5f-108">Members</span></span>

 <span data-ttu-id="50d5f-109">**cValues**</span><span class="sxs-lookup"><span data-stu-id="50d5f-109">**cValues**</span></span>
  
> <span data-ttu-id="50d5f-110">Anzahl der Werte im Array, auf das das **lpli-Element verweist.**</span><span class="sxs-lookup"><span data-stu-id="50d5f-110">Count of values in the array pointed to by the **lpli** member.</span></span> 
    
 <span data-ttu-id="50d5f-111">**lpli**</span><span class="sxs-lookup"><span data-stu-id="50d5f-111">**lpli**</span></span>
  
> <span data-ttu-id="50d5f-112">Zeiger auf ein Array von **LARGE_INTEGER,** das die ganzzahligen Werte enthält.</span><span class="sxs-lookup"><span data-stu-id="50d5f-112">Pointer to an array of **LARGE_INTEGER** structures holding the integer values.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="50d5f-113">Hinweise</span><span class="sxs-lookup"><span data-stu-id="50d5f-113">Remarks</span></span>

<span data-ttu-id="50d5f-114">Weitere Informationen zu PT_MV_18 finden Sie [unter List of Property Types](property-types.md).</span><span class="sxs-lookup"><span data-stu-id="50d5f-114">For more information about PT_MV_18, see [List of Property Types](property-types.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="50d5f-115">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="50d5f-115">See also</span></span>



[<span data-ttu-id="50d5f-116">SPropValue</span><span class="sxs-lookup"><span data-stu-id="50d5f-116">SPropValue</span></span>](spropvalue.md)


[<span data-ttu-id="50d5f-117">MAPI-Strukturen</span><span class="sxs-lookup"><span data-stu-id="50d5f-117">MAPI Structures</span></span>](mapi-structures.md)

