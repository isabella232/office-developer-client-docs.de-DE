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
ms.openlocfilehash: e3f53a894b7f7cdaa68e66530c7bd99bf49b9ed0
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2018
ms.locfileid: "22581356"
---
# <a name="swstringarray"></a><span data-ttu-id="a6d93-103">SWStringArray</span><span class="sxs-lookup"><span data-stu-id="a6d93-103">SWStringArray</span></span>

  
  
<span data-ttu-id="a6d93-104">**Betrifft**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="a6d93-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="a6d93-105">Enthält ein Array von Zeichenfolgen, die verwendet werden, um eine Eigenschaft vom Typ PT_MV_UNICODE zu beschreiben.</span><span class="sxs-lookup"><span data-stu-id="a6d93-105">Contains an array of character strings that are used to describe a property of type PT_MV_UNICODE.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="a6d93-106">Headerdatei</span><span class="sxs-lookup"><span data-stu-id="a6d93-106">Header file:</span></span>  <br/> |<span data-ttu-id="a6d93-107">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="a6d93-107">Mapidefs.h</span></span>  <br/> |
   
```cpp
typedef struct _SWStringArray
{
  ULONG cValues;
  LPWSTR FAR *lppszW;
} SWStringArray;

```

## <a name="members"></a><span data-ttu-id="a6d93-108">Elemente</span><span class="sxs-lookup"><span data-stu-id="a6d93-108">Members</span></span>

 <span data-ttu-id="a6d93-109">**cValues**</span><span class="sxs-lookup"><span data-stu-id="a6d93-109">**cValues**</span></span>
  
> <span data-ttu-id="a6d93-110">Anzahl der Zeichenfolgen im Array auf den Member **LppszW** zeigt.</span><span class="sxs-lookup"><span data-stu-id="a6d93-110">Count of strings in the array pointed to by the **lppszW** member.</span></span> 
    
 <span data-ttu-id="a6d93-111">**lppszW**</span><span class="sxs-lookup"><span data-stu-id="a6d93-111">**lppszW**</span></span>
  
> <span data-ttu-id="a6d93-112">Zeiger auf ein Array von Zeichenfolgen mit Unicode-Zeichen Null beendet.</span><span class="sxs-lookup"><span data-stu-id="a6d93-112">Pointer to an array of null-ended Unicode character strings.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="a6d93-113">HinwBemerkungeneise</span><span class="sxs-lookup"><span data-stu-id="a6d93-113">Remarks</span></span>

<span data-ttu-id="a6d93-114">Weitere Informationen zu PT_MV_UNICODE finden Sie unter [Eigenschaftentypen](property-types.md).</span><span class="sxs-lookup"><span data-stu-id="a6d93-114">For more information about PT_MV_UNICODE, see [Property Types](property-types.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="a6d93-115">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="a6d93-115">See also</span></span>



[<span data-ttu-id="a6d93-116">SPropValue</span><span class="sxs-lookup"><span data-stu-id="a6d93-116">SPropValue</span></span>](spropvalue.md)


[<span data-ttu-id="a6d93-117">MAPI-Strukturen</span><span class="sxs-lookup"><span data-stu-id="a6d93-117">MAPI Structures</span></span>](mapi-structures.md)

