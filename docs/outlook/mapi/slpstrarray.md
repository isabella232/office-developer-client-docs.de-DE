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
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: ccad74a9f2553bf29af124821c6d6a87dcde3303
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2018
ms.locfileid: "22572872"
---
# <a name="slpstrarray"></a><span data-ttu-id="6bed6-103">SLPSTRArray</span><span class="sxs-lookup"><span data-stu-id="6bed6-103">SLPSTRArray</span></span>

  
  
<span data-ttu-id="6bed6-104">**Betrifft**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="6bed6-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="6bed6-105">Enthält ein Array mit String-Werten, mit denen eine Eigenschaft vom Typ PT_MV_STRING8 beschrieben.</span><span class="sxs-lookup"><span data-stu-id="6bed6-105">Contains an array of string values that are used to describe a property of type PT_MV_STRING8.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="6bed6-106">Headerdatei</span><span class="sxs-lookup"><span data-stu-id="6bed6-106">Header file:</span></span>  <br/> |<span data-ttu-id="6bed6-107">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="6bed6-107">Mapidefs.h</span></span>  <br/> |
   
```cpp
typedef struct _SLPSTRArray
{
  ULONG cValues;
  LPSTR FAR *lppszA;
} SLPSTRArray;

```

## <a name="members"></a><span data-ttu-id="6bed6-108">Elemente</span><span class="sxs-lookup"><span data-stu-id="6bed6-108">Members</span></span>

 <span data-ttu-id="6bed6-109">**cValues**</span><span class="sxs-lookup"><span data-stu-id="6bed6-109">**cValues**</span></span>
  
> <span data-ttu-id="6bed6-110">Anzahl der Werte im Array auf den Member **LppszA** zeigt.</span><span class="sxs-lookup"><span data-stu-id="6bed6-110">Count of values in the array pointed to by the **lppszA** member.</span></span> 
    
 <span data-ttu-id="6bed6-111">**lppszA**</span><span class="sxs-lookup"><span data-stu-id="6bed6-111">**lppszA**</span></span>
  
> <span data-ttu-id="6bed6-112">Zeiger auf ein Array von Zeichenfolgen mit Null beendet 8-Bit-Zeichen.</span><span class="sxs-lookup"><span data-stu-id="6bed6-112">Pointer to an array of null-ended 8-bit character strings.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="6bed6-113">HinwBemerkungeneise</span><span class="sxs-lookup"><span data-stu-id="6bed6-113">Remarks</span></span>

<span data-ttu-id="6bed6-114">Weitere Informationen zu PT_MV_STRING8 finden Sie unter [Liste der Eigenschaftentypen](property-types.md).</span><span class="sxs-lookup"><span data-stu-id="6bed6-114">For more information about PT_MV_STRING8, see [List of Property Types](property-types.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="6bed6-115">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="6bed6-115">See also</span></span>



[<span data-ttu-id="6bed6-116">SPropValue</span><span class="sxs-lookup"><span data-stu-id="6bed6-116">SPropValue</span></span>](spropvalue.md)


[<span data-ttu-id="6bed6-117">MAPI-Strukturen</span><span class="sxs-lookup"><span data-stu-id="6bed6-117">MAPI Structures</span></span>](mapi-structures.md)

