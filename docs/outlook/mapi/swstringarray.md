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
ms.openlocfilehash: 1578e26ec96f69975c2304cb185f352193a52c2d
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19795684"
---
# <a name="swstringarray"></a><span data-ttu-id="b2f90-103">SWStringArray</span><span class="sxs-lookup"><span data-stu-id="b2f90-103">SWStringArray</span></span>

  
  
<span data-ttu-id="b2f90-104">**Betrifft**: Outlook</span><span class="sxs-lookup"><span data-stu-id="b2f90-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="b2f90-105">Enthält ein Array von Zeichenfolgen, die verwendet werden, um eine Eigenschaft vom Typ PT_MV_UNICODE zu beschreiben.</span><span class="sxs-lookup"><span data-stu-id="b2f90-105">Contains an array of character strings that are used to describe a property of type PT_MV_UNICODE.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="b2f90-106">Headerdatei</span><span class="sxs-lookup"><span data-stu-id="b2f90-106">Header file:</span></span>  <br/> |<span data-ttu-id="b2f90-107">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="b2f90-107">Mapidefs.h</span></span>  <br/> |
   
```cpp
typedef struct _SWStringArray
{
  ULONG cValues;
  LPWSTR FAR *lppszW;
} SWStringArray;

```

## <a name="members"></a><span data-ttu-id="b2f90-108">Elemente</span><span class="sxs-lookup"><span data-stu-id="b2f90-108">Members</span></span>

 <span data-ttu-id="b2f90-109">**cValues**</span><span class="sxs-lookup"><span data-stu-id="b2f90-109">**cValues**</span></span>
  
> <span data-ttu-id="b2f90-110">Anzahl der Zeichenfolgen im Array auf den Member **LppszW** zeigt.</span><span class="sxs-lookup"><span data-stu-id="b2f90-110">Count of strings in the array pointed to by the **lppszW** member.</span></span> 
    
 <span data-ttu-id="b2f90-111">**lppszW**</span><span class="sxs-lookup"><span data-stu-id="b2f90-111">**lppszW**</span></span>
  
> <span data-ttu-id="b2f90-112">Zeiger auf ein Array von Zeichenfolgen mit Unicode-Zeichen Null beendet.</span><span class="sxs-lookup"><span data-stu-id="b2f90-112">Pointer to an array of null-ended Unicode character strings.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="b2f90-113">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="b2f90-113">Remarks</span></span>

<span data-ttu-id="b2f90-114">Weitere Informationen zu PT_MV_UNICODE finden Sie unter [Eigenschaftentypen](property-types.md).</span><span class="sxs-lookup"><span data-stu-id="b2f90-114">For more information about PT_MV_UNICODE, see [Property Types](property-types.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="b2f90-115">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="b2f90-115">See also</span></span>



[<span data-ttu-id="b2f90-116">SPropValue</span><span class="sxs-lookup"><span data-stu-id="b2f90-116">SPropValue</span></span>](spropvalue.md)


[<span data-ttu-id="b2f90-117">MAPI-Strukturen</span><span class="sxs-lookup"><span data-stu-id="b2f90-117">MAPI Structures</span></span>](mapi-structures.md)

