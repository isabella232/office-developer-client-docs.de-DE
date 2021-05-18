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
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: ff69981e83d42e439936a3e4be47eabfd811b310
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33413605"
---
# <a name="swstringarray"></a><span data-ttu-id="b22bf-103">SWStringArray</span><span class="sxs-lookup"><span data-stu-id="b22bf-103">SWStringArray</span></span>

  
  
<span data-ttu-id="b22bf-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="b22bf-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="b22bf-105">Enthält ein Array von Zeichenzeichenfolgen, die zum Beschreiben einer Eigenschaft vom Typ PT_MV_UNICODE.</span><span class="sxs-lookup"><span data-stu-id="b22bf-105">Contains an array of character strings that are used to describe a property of type PT_MV_UNICODE.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="b22bf-106">Headerdatei</span><span class="sxs-lookup"><span data-stu-id="b22bf-106">Header file:</span></span>  <br/> |<span data-ttu-id="b22bf-107">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="b22bf-107">Mapidefs.h</span></span>  <br/> |
   
```cpp
typedef struct _SWStringArray
{
  ULONG cValues;
  LPWSTR FAR *lppszW;
} SWStringArray;

```

## <a name="members"></a><span data-ttu-id="b22bf-108">Elemente</span><span class="sxs-lookup"><span data-stu-id="b22bf-108">Members</span></span>

 <span data-ttu-id="b22bf-109">**cValues**</span><span class="sxs-lookup"><span data-stu-id="b22bf-109">**cValues**</span></span>
  
> <span data-ttu-id="b22bf-110">Anzahl der Zeichenfolgen im Array, auf die das **lppszW-Element** verweist.</span><span class="sxs-lookup"><span data-stu-id="b22bf-110">Count of strings in the array pointed to by the **lppszW** member.</span></span> 
    
 <span data-ttu-id="b22bf-111">**lppszW**</span><span class="sxs-lookup"><span data-stu-id="b22bf-111">**lppszW**</span></span>
  
> <span data-ttu-id="b22bf-112">Zeiger auf ein Array mit Nullend-Unicode-Zeichenzeichenfolgen.</span><span class="sxs-lookup"><span data-stu-id="b22bf-112">Pointer to an array of null-ended Unicode character strings.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="b22bf-113">Hinweise</span><span class="sxs-lookup"><span data-stu-id="b22bf-113">Remarks</span></span>

<span data-ttu-id="b22bf-114">Weitere Informationen zu PT_MV_UNICODE finden Sie unter [Property Types](property-types.md).</span><span class="sxs-lookup"><span data-stu-id="b22bf-114">For more information about PT_MV_UNICODE, see [Property Types](property-types.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="b22bf-115">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="b22bf-115">See also</span></span>



[<span data-ttu-id="b22bf-116">SPropValue</span><span class="sxs-lookup"><span data-stu-id="b22bf-116">SPropValue</span></span>](spropvalue.md)


[<span data-ttu-id="b22bf-117">MAPI-Strukturen</span><span class="sxs-lookup"><span data-stu-id="b22bf-117">MAPI Structures</span></span>](mapi-structures.md)

