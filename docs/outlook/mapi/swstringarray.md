---
title: SWStringArray
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.SWStringArray
api_type:
- COM
ms.assetid: c1ae24ad-1bbb-4dee-b414-b5226593b6fa
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: ff69981e83d42e439936a3e4be47eabfd811b310
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32349553"
---
# <a name="swstringarray"></a><span data-ttu-id="ce058-103">SWStringArray</span><span class="sxs-lookup"><span data-stu-id="ce058-103">SWStringArray</span></span>

  
  
<span data-ttu-id="ce058-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="ce058-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="ce058-105">Enthält ein Array von Zeichenfolgen, die zum Beschreiben einer Eigenschaft vom Typ PT_MV_UNICODE verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="ce058-105">Contains an array of character strings that are used to describe a property of type PT_MV_UNICODE.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="ce058-106">Headerdatei</span><span class="sxs-lookup"><span data-stu-id="ce058-106">Header file:</span></span>  <br/> |<span data-ttu-id="ce058-107">Mapidefs. h</span><span class="sxs-lookup"><span data-stu-id="ce058-107">Mapidefs.h</span></span>  <br/> |
   
```cpp
typedef struct _SWStringArray
{
  ULONG cValues;
  LPWSTR FAR *lppszW;
} SWStringArray;

```

## <a name="members"></a><span data-ttu-id="ce058-108">Elemente</span><span class="sxs-lookup"><span data-stu-id="ce058-108">Members</span></span>

 <span data-ttu-id="ce058-109">**cValues**</span><span class="sxs-lookup"><span data-stu-id="ce058-109">**cValues**</span></span>
  
> <span data-ttu-id="ce058-110">Anzahl der Zeichenfolgen im Array, auf die durch das **lppszW** -Element verwiesen wird.</span><span class="sxs-lookup"><span data-stu-id="ce058-110">Count of strings in the array pointed to by the **lppszW** member.</span></span> 
    
 <span data-ttu-id="ce058-111">**lppszW**</span><span class="sxs-lookup"><span data-stu-id="ce058-111">**lppszW**</span></span>
  
> <span data-ttu-id="ce058-112">Zeiger auf ein Array von Zeichenfolgen mit NULL-Zeichenfolge.</span><span class="sxs-lookup"><span data-stu-id="ce058-112">Pointer to an array of null-ended Unicode character strings.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="ce058-113">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="ce058-113">Remarks</span></span>

<span data-ttu-id="ce058-114">Weitere Informationen zu PT_MV_UNICODE finden Sie unter [Property Types](property-types.md).</span><span class="sxs-lookup"><span data-stu-id="ce058-114">For more information about PT_MV_UNICODE, see [Property Types](property-types.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="ce058-115">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="ce058-115">See also</span></span>



[<span data-ttu-id="ce058-116">SPropValue</span><span class="sxs-lookup"><span data-stu-id="ce058-116">SPropValue</span></span>](spropvalue.md)


[<span data-ttu-id="ce058-117">MAPI-Strukturen</span><span class="sxs-lookup"><span data-stu-id="ce058-117">MAPI Structures</span></span>](mapi-structures.md)

