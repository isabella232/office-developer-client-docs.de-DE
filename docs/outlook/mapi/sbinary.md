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
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: fe07ed7c7f9c76f82b54732c019b9b5f8beb5db2
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19795422"
---
# <a name="sbinary"></a><span data-ttu-id="95c02-103">SBinary</span><span class="sxs-lookup"><span data-stu-id="95c02-103">SBinary</span></span>

  
  
<span data-ttu-id="95c02-104">**Betrifft**: Outlook</span><span class="sxs-lookup"><span data-stu-id="95c02-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="95c02-105">Beschreibt eine Eigenschaft vom Typ PT_BINARY.</span><span class="sxs-lookup"><span data-stu-id="95c02-105">Describes a property of type PT_BINARY.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="95c02-106">Headerdatei</span><span class="sxs-lookup"><span data-stu-id="95c02-106">Header file:</span></span>  <br/> |<span data-ttu-id="95c02-107">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="95c02-107">Mapidefs.h</span></span>  <br/> |
   
```cpp
typedef struct _SBinary
{
  ULONG      cb;
  LPBYTE     lpb;
} SBinary, FAR *LPSBinary;

```

## <a name="members"></a><span data-ttu-id="95c02-108">Members</span><span class="sxs-lookup"><span data-stu-id="95c02-108">Members</span></span>

 <span data-ttu-id="95c02-109">**cb**</span><span class="sxs-lookup"><span data-stu-id="95c02-109">**cb**</span></span>
  
> <span data-ttu-id="95c02-110">Anzahl der Bytes im **Lpb** -Member.</span><span class="sxs-lookup"><span data-stu-id="95c02-110">Count of bytes in the **lpb** member.</span></span> 
    
 <span data-ttu-id="95c02-111">**lpb**</span><span class="sxs-lookup"><span data-stu-id="95c02-111">**lpb**</span></span>
  
> <span data-ttu-id="95c02-112">Zeiger auf den Wert der PT_BINARY-Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="95c02-112">Pointer to the PT_BINARY property value.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="95c02-113">Hinweise</span><span class="sxs-lookup"><span data-stu-id="95c02-113">Remarks</span></span>

<span data-ttu-id="95c02-114">Informationen zu Eigenschaftstypen finden Sie unter [MAPI-Eigenschaft Type Overview](mapi-property-type-overview.md).</span><span class="sxs-lookup"><span data-stu-id="95c02-114">For information about property types, see [MAPI Property Type Overview](mapi-property-type-overview.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="95c02-115">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="95c02-115">See also</span></span>



[<span data-ttu-id="95c02-116">SPropValue</span><span class="sxs-lookup"><span data-stu-id="95c02-116">SPropValue</span></span>](spropvalue.md)


[<span data-ttu-id="95c02-117">MAPI-Strukturen</span><span class="sxs-lookup"><span data-stu-id="95c02-117">MAPI Structures</span></span>](mapi-structures.md)

