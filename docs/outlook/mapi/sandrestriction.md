---
title: SAndRestriction
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.SAndRestriction
api_type:
- COM
ms.assetid: 1b7dfe87-f87f-43e3-8332-a0d9c3f70d16
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: 1437130caecd57344fc171d234c5391ea92e1d4b
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19795435"
---
# <a name="sandrestriction"></a><span data-ttu-id="9c24d-103">SAndRestriction</span><span class="sxs-lookup"><span data-stu-id="9c24d-103">SAndRestriction</span></span>

  
  
<span data-ttu-id="9c24d-104">**Betrifft**: Outlook</span><span class="sxs-lookup"><span data-stu-id="9c24d-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="9c24d-105">Beschreibt eine Einschränkung **und** , die zur Teilnahme an einer Gruppe von Einschränkungen, die mit einer logischen **AND** -Operation verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="9c24d-105">Describes an **AND** restriction, which is used to join a group of restrictions using a logical **AND** operation.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="9c24d-106">Headerdatei</span><span class="sxs-lookup"><span data-stu-id="9c24d-106">Header file:</span></span>  <br/> |<span data-ttu-id="9c24d-107">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="9c24d-107">Mapidefs.h</span></span>  <br/> |
   
```cpp
typedef struct _SAndRestriction
{
  ULONG cRes;
  LPSRestriction lpRes;
} SAndRestriction;

```

## <a name="members"></a><span data-ttu-id="9c24d-108">Elemente</span><span class="sxs-lookup"><span data-stu-id="9c24d-108">Members</span></span>

 <span data-ttu-id="9c24d-109">**cRes**</span><span class="sxs-lookup"><span data-stu-id="9c24d-109">**cRes**</span></span>
  
> <span data-ttu-id="9c24d-110">Anzahl der Suche Einschränkungen im Array auf das Element **LpRes** zeigt.</span><span class="sxs-lookup"><span data-stu-id="9c24d-110">Count of search restrictions in the array pointed to by the **lpRes** member.</span></span> 
    
 <span data-ttu-id="9c24d-111">**lpRes**</span><span class="sxs-lookup"><span data-stu-id="9c24d-111">**lpRes**</span></span>
  
> <span data-ttu-id="9c24d-112">Zeiger auf ein Array von [SRestriction](srestriction.md) -Strukturen, die mit **eine Operation** kombiniert werden.</span><span class="sxs-lookup"><span data-stu-id="9c24d-112">Pointer to an array of [SRestriction](srestriction.md) structures that will be combined with a logical **AND** operation.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="9c24d-113">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="9c24d-113">Remarks</span></span>

<span data-ttu-id="9c24d-114">Das Ergebnis der **SAndRestriction** ist TRUE, wenn alle seine untergeordneten Einschränkungen zu TRUE ausgewertet werden.</span><span class="sxs-lookup"><span data-stu-id="9c24d-114">The result of the **SAndRestriction** is TRUE if all its child restrictions evaluate to TRUE.</span></span> <span data-ttu-id="9c24d-115">Es ist FALSE, wenn alle untergeordneten Beschränkung auf "false" ausgewertet wird.</span><span class="sxs-lookup"><span data-stu-id="9c24d-115">It is FALSE if any child restriction evaluates to FALSE.</span></span> 
  
<span data-ttu-id="9c24d-116">Eine Beschreibung der Einschränkungstypen zum Erstellen, und Beispielcode finden Sie unter [Informationen zu Einschränkungen](about-restrictions.md).</span><span class="sxs-lookup"><span data-stu-id="9c24d-116">For a description of types of restrictions, how to build them, and sample code, see [About Restrictions](about-restrictions.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="9c24d-117">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="9c24d-117">See also</span></span>



[<span data-ttu-id="9c24d-118">SRestriction</span><span class="sxs-lookup"><span data-stu-id="9c24d-118">SRestriction</span></span>](srestriction.md)


[<span data-ttu-id="9c24d-119">MAPI-Strukturen</span><span class="sxs-lookup"><span data-stu-id="9c24d-119">MAPI Structures</span></span>](mapi-structures.md)

