---
title: SLPSTRArray
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.SLPSTRArray
api_type:
- COM
ms.assetid: 5f570d9b-eb3d-4fc7-bcbe-348a0b8fe9e9
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: 6d2bb6bdb934e0b02831b813b1246a3df4193e0d
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19795572"
---
# <a name="slpstrarray"></a><span data-ttu-id="d62bc-103">SLPSTRArray</span><span class="sxs-lookup"><span data-stu-id="d62bc-103">SLPSTRArray</span></span>

  
  
<span data-ttu-id="d62bc-104">**Betrifft**: Outlook</span><span class="sxs-lookup"><span data-stu-id="d62bc-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="d62bc-105">Enthält ein Array mit String-Werten, mit denen eine Eigenschaft vom Typ PT_MV_STRING8 beschrieben.</span><span class="sxs-lookup"><span data-stu-id="d62bc-105">Contains an array of string values that are used to describe a property of type PT_MV_STRING8.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="d62bc-106">Headerdatei</span><span class="sxs-lookup"><span data-stu-id="d62bc-106">Header file:</span></span>  <br/> |<span data-ttu-id="d62bc-107">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="d62bc-107">Mapidefs.h</span></span>  <br/> |
   
```cpp
typedef struct _SLPSTRArray
{
  ULONG cValues;
  LPSTR FAR *lppszA;
} SLPSTRArray;

```

## <a name="members"></a><span data-ttu-id="d62bc-108">Members</span><span class="sxs-lookup"><span data-stu-id="d62bc-108">Members</span></span>

 <span data-ttu-id="d62bc-109">**cValues**</span><span class="sxs-lookup"><span data-stu-id="d62bc-109">**cValues**</span></span>
  
> <span data-ttu-id="d62bc-110">Anzahl der Werte im Array auf den Member **LppszA** zeigt.</span><span class="sxs-lookup"><span data-stu-id="d62bc-110">Count of values in the array pointed to by the **lppszA** member.</span></span> 
    
 <span data-ttu-id="d62bc-111">**lppszA**</span><span class="sxs-lookup"><span data-stu-id="d62bc-111">**lppszA**</span></span>
  
> <span data-ttu-id="d62bc-112">Zeiger auf ein Array von Zeichenfolgen mit Null beendet 8-Bit-Zeichen.</span><span class="sxs-lookup"><span data-stu-id="d62bc-112">Pointer to an array of null-ended 8-bit character strings.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="d62bc-113">Hinweise</span><span class="sxs-lookup"><span data-stu-id="d62bc-113">Remarks</span></span>

<span data-ttu-id="d62bc-114">Weitere Informationen zu PT_MV_STRING8 finden Sie unter [Liste der Eigenschaftentypen](property-types.md).</span><span class="sxs-lookup"><span data-stu-id="d62bc-114">For more information about PT_MV_STRING8, see [List of Property Types](property-types.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="d62bc-115">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="d62bc-115">See also</span></span>



[<span data-ttu-id="d62bc-116">SPropValue</span><span class="sxs-lookup"><span data-stu-id="d62bc-116">SPropValue</span></span>](spropvalue.md)


[<span data-ttu-id="d62bc-117">MAPI-Strukturen</span><span class="sxs-lookup"><span data-stu-id="d62bc-117">MAPI Structures</span></span>](mapi-structures.md)

