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
ms.openlocfilehash: 987020bd6fd49fcba9453075cd502bd5cea4c3a3
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33435908"
---
# <a name="slpstrarray"></a><span data-ttu-id="8422d-103">SLPSTRArray</span><span class="sxs-lookup"><span data-stu-id="8422d-103">SLPSTRArray</span></span>

  
  
<span data-ttu-id="8422d-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="8422d-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="8422d-105">Enthält ein Array von String-Werten, die zum Beschreiben einer Eigenschaft vom Typ PT_MV_STRING8 verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="8422d-105">Contains an array of string values that are used to describe a property of type PT_MV_STRING8.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="8422d-106">Headerdatei</span><span class="sxs-lookup"><span data-stu-id="8422d-106">Header file:</span></span>  <br/> |<span data-ttu-id="8422d-107">Mapidefs. h</span><span class="sxs-lookup"><span data-stu-id="8422d-107">Mapidefs.h</span></span>  <br/> |
   
```cpp
typedef struct _SLPSTRArray
{
  ULONG cValues;
  LPSTR FAR *lppszA;
} SLPSTRArray;

```

## <a name="members"></a><span data-ttu-id="8422d-108">Members</span><span class="sxs-lookup"><span data-stu-id="8422d-108">Members</span></span>

 <span data-ttu-id="8422d-109">**cValues**</span><span class="sxs-lookup"><span data-stu-id="8422d-109">**cValues**</span></span>
  
> <span data-ttu-id="8422d-110">Die Anzahl der Werte im Array, auf die durch das **lppszA** -Element verwiesen wird.</span><span class="sxs-lookup"><span data-stu-id="8422d-110">Count of values in the array pointed to by the **lppszA** member.</span></span> 
    
 <span data-ttu-id="8422d-111">**lppszA**</span><span class="sxs-lookup"><span data-stu-id="8422d-111">**lppszA**</span></span>
  
> <span data-ttu-id="8422d-112">Zeiger auf ein Array von NULL-beendeten 8-Bit-Zeichenfolgen.</span><span class="sxs-lookup"><span data-stu-id="8422d-112">Pointer to an array of null-ended 8-bit character strings.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="8422d-113">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="8422d-113">Remarks</span></span>

<span data-ttu-id="8422d-114">Weitere Informationen zu PT_MV_STRING8 finden Sie unter [Liste der Eigenschaftstypen](property-types.md).</span><span class="sxs-lookup"><span data-stu-id="8422d-114">For more information about PT_MV_STRING8, see [List of Property Types](property-types.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="8422d-115">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="8422d-115">See also</span></span>



[<span data-ttu-id="8422d-116">SPropValue</span><span class="sxs-lookup"><span data-stu-id="8422d-116">SPropValue</span></span>](spropvalue.md)


[<span data-ttu-id="8422d-117">MAPI-Strukturen</span><span class="sxs-lookup"><span data-stu-id="8422d-117">MAPI Structures</span></span>](mapi-structures.md)

