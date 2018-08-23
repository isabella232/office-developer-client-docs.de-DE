---
title: SBinary
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.SBinary
api_type:
- COM
ms.assetid: f21b5e6c-7a63-46bf-acbf-0e042e3519f7
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: f54ef96443e5c9fc5fb587f5a9c25388c1ff9cdb
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2018
ms.locfileid: "22577422"
---
# <a name="sbinary"></a><span data-ttu-id="c71ae-103">SBinary</span><span class="sxs-lookup"><span data-stu-id="c71ae-103">SBinary</span></span>

  
  
<span data-ttu-id="c71ae-104">**Betrifft**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="c71ae-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="c71ae-105">Beschreibt eine Eigenschaft vom Typ PT_BINARY.</span><span class="sxs-lookup"><span data-stu-id="c71ae-105">Describes a property of type PT_BINARY.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="c71ae-106">Headerdatei</span><span class="sxs-lookup"><span data-stu-id="c71ae-106">Header file:</span></span>  <br/> |<span data-ttu-id="c71ae-107">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="c71ae-107">Mapidefs.h</span></span>  <br/> |
   
```cpp
typedef struct _SBinary
{
  ULONG      cb;
  LPBYTE     lpb;
} SBinary, FAR *LPSBinary;

```

## <a name="members"></a><span data-ttu-id="c71ae-108">Elemente</span><span class="sxs-lookup"><span data-stu-id="c71ae-108">Members</span></span>

 <span data-ttu-id="c71ae-109">**cb**</span><span class="sxs-lookup"><span data-stu-id="c71ae-109">**cb**</span></span>
  
> <span data-ttu-id="c71ae-110">Anzahl der Bytes im **Lpb** -Member.</span><span class="sxs-lookup"><span data-stu-id="c71ae-110">Count of bytes in the **lpb** member.</span></span> 
    
 <span data-ttu-id="c71ae-111">**lpb**</span><span class="sxs-lookup"><span data-stu-id="c71ae-111">**lpb**</span></span>
  
> <span data-ttu-id="c71ae-112">Zeiger auf den Wert der PT_BINARY-Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="c71ae-112">Pointer to the PT_BINARY property value.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="c71ae-113">HinwBemerkungeneise</span><span class="sxs-lookup"><span data-stu-id="c71ae-113">Remarks</span></span>

<span data-ttu-id="c71ae-114">Informationen zu Eigenschaftstypen finden Sie unter [MAPI-Eigenschaft Type Overview](mapi-property-type-overview.md).</span><span class="sxs-lookup"><span data-stu-id="c71ae-114">For information about property types, see [MAPI Property Type Overview](mapi-property-type-overview.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="c71ae-115">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="c71ae-115">See also</span></span>



[<span data-ttu-id="c71ae-116">SPropValue</span><span class="sxs-lookup"><span data-stu-id="c71ae-116">SPropValue</span></span>](spropvalue.md)


[<span data-ttu-id="c71ae-117">MAPI-Strukturen</span><span class="sxs-lookup"><span data-stu-id="c71ae-117">MAPI Structures</span></span>](mapi-structures.md)

