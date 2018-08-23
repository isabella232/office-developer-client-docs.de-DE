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
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 9f8da0902ea4c4a862d279ee80ba566c0473c44e
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2018
ms.locfileid: "22592325"
---
# <a name="sandrestriction"></a><span data-ttu-id="d6051-103">SAndRestriction</span><span class="sxs-lookup"><span data-stu-id="d6051-103">SAndRestriction</span></span>

  
  
<span data-ttu-id="d6051-104">**Betrifft**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="d6051-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="d6051-105">Beschreibt eine Einschränkung **und** , die zur Teilnahme an einer Gruppe von Einschränkungen, die mit einer logischen **AND** -Operation verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="d6051-105">Describes an **AND** restriction, which is used to join a group of restrictions using a logical **AND** operation.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="d6051-106">Headerdatei</span><span class="sxs-lookup"><span data-stu-id="d6051-106">Header file:</span></span>  <br/> |<span data-ttu-id="d6051-107">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="d6051-107">Mapidefs.h</span></span>  <br/> |
   
```cpp
typedef struct _SAndRestriction
{
  ULONG cRes;
  LPSRestriction lpRes;
} SAndRestriction;

```

## <a name="members"></a><span data-ttu-id="d6051-108">Elemente</span><span class="sxs-lookup"><span data-stu-id="d6051-108">Members</span></span>

 <span data-ttu-id="d6051-109">**cRes**</span><span class="sxs-lookup"><span data-stu-id="d6051-109">**cRes**</span></span>
  
> <span data-ttu-id="d6051-110">Anzahl der Suche Einschränkungen im Array auf das Element **LpRes** zeigt.</span><span class="sxs-lookup"><span data-stu-id="d6051-110">Count of search restrictions in the array pointed to by the **lpRes** member.</span></span> 
    
 <span data-ttu-id="d6051-111">**lpRes**</span><span class="sxs-lookup"><span data-stu-id="d6051-111">**lpRes**</span></span>
  
> <span data-ttu-id="d6051-112">Zeiger auf ein Array von [SRestriction](srestriction.md) -Strukturen, die mit **eine Operation** kombiniert werden.</span><span class="sxs-lookup"><span data-stu-id="d6051-112">Pointer to an array of [SRestriction](srestriction.md) structures that will be combined with a logical **AND** operation.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="d6051-113">HinwBemerkungeneise</span><span class="sxs-lookup"><span data-stu-id="d6051-113">Remarks</span></span>

<span data-ttu-id="d6051-114">Das Ergebnis der **SAndRestriction** ist TRUE, wenn alle seine untergeordneten Einschränkungen zu TRUE ausgewertet werden.</span><span class="sxs-lookup"><span data-stu-id="d6051-114">The result of the **SAndRestriction** is TRUE if all its child restrictions evaluate to TRUE.</span></span> <span data-ttu-id="d6051-115">Es ist FALSE, wenn alle untergeordneten Beschränkung auf "false" ausgewertet wird.</span><span class="sxs-lookup"><span data-stu-id="d6051-115">It is FALSE if any child restriction evaluates to FALSE.</span></span> 
  
<span data-ttu-id="d6051-116">Eine Beschreibung der Einschränkungstypen zum Erstellen, und Beispielcode finden Sie unter [Informationen zu Einschränkungen](about-restrictions.md).</span><span class="sxs-lookup"><span data-stu-id="d6051-116">For a description of types of restrictions, how to build them, and sample code, see [About Restrictions](about-restrictions.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="d6051-117">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="d6051-117">See also</span></span>



[<span data-ttu-id="d6051-118">SRestriction</span><span class="sxs-lookup"><span data-stu-id="d6051-118">SRestriction</span></span>](srestriction.md)


[<span data-ttu-id="d6051-119">MAPI-Strukturen</span><span class="sxs-lookup"><span data-stu-id="d6051-119">MAPI Structures</span></span>](mapi-structures.md)

