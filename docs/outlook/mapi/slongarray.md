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
ms.openlocfilehash: 9b1c5a09a60240efa9d4fa117f0d8fe8113169d5
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33414529"
---
# <a name="slongarray"></a><span data-ttu-id="147d0-103">SLongArray</span><span class="sxs-lookup"><span data-stu-id="147d0-103">SLongArray</span></span>

  
  
<span data-ttu-id="147d0-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="147d0-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="147d0-105">Enthält ein Array von LONG-Werttypen, die zum Beschreiben einer Eigenschaft vom Typ PT_MV_LONG.</span><span class="sxs-lookup"><span data-stu-id="147d0-105">Contains an array of LONG value types that are used to describe a property of type PT_MV_LONG.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="147d0-106">Headerdatei</span><span class="sxs-lookup"><span data-stu-id="147d0-106">Header file:</span></span>  <br/> |<span data-ttu-id="147d0-107">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="147d0-107">Mapidefs.h</span></span>  <br/> |
   
```cpp
typedef struct _SLongArray
{
  ULONG cValues;
  LONG FAR *lpl;
} SLongArray;

```

## <a name="members"></a><span data-ttu-id="147d0-108">Elemente</span><span class="sxs-lookup"><span data-stu-id="147d0-108">Members</span></span>

 <span data-ttu-id="147d0-109">**cValues**</span><span class="sxs-lookup"><span data-stu-id="147d0-109">**cValues**</span></span>
  
> <span data-ttu-id="147d0-110">Anzahl der Werte im Array, auf das das **lpl-Element verweist.**</span><span class="sxs-lookup"><span data-stu-id="147d0-110">Count of values in the array pointed to by the **lpl** member.</span></span> 
    
 <span data-ttu-id="147d0-111">**lpl**</span><span class="sxs-lookup"><span data-stu-id="147d0-111">**lpl**</span></span>
  
> <span data-ttu-id="147d0-112">Zeiger auf ein Array von LONG-Werten.</span><span class="sxs-lookup"><span data-stu-id="147d0-112">Pointer to an array of LONG values.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="147d0-113">Hinweise</span><span class="sxs-lookup"><span data-stu-id="147d0-113">Remarks</span></span>

<span data-ttu-id="147d0-114">Weitere Informationen zu PT_MV_LONG finden Sie [unter List of Property Types](property-types.md).</span><span class="sxs-lookup"><span data-stu-id="147d0-114">For more information about PT_MV_LONG, see [List of Property Types](property-types.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="147d0-115">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="147d0-115">See also</span></span>



[<span data-ttu-id="147d0-116">SPropValue</span><span class="sxs-lookup"><span data-stu-id="147d0-116">SPropValue</span></span>](spropvalue.md)


[<span data-ttu-id="147d0-117">MAPI-Strukturen</span><span class="sxs-lookup"><span data-stu-id="147d0-117">MAPI Structures</span></span>](mapi-structures.md)

