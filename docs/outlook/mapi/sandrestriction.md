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
ms.openlocfilehash: da35c9c72f4cf3f076715a7a35a3e3514c672ceb
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32344660"
---
# <a name="sandrestriction"></a><span data-ttu-id="b8d1a-103">SAndRestriction</span><span class="sxs-lookup"><span data-stu-id="b8d1a-103">SAndRestriction</span></span>

  
  
<span data-ttu-id="b8d1a-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="b8d1a-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="b8d1a-105">Beschreibt eine **und-** Einschränkung, die verwendet wird, um einer Gruppe von Einschränkungen mithilfe einer logischen **and-** Operation beizutreten.</span><span class="sxs-lookup"><span data-stu-id="b8d1a-105">Describes an **AND** restriction, which is used to join a group of restrictions using a logical **AND** operation.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="b8d1a-106">Headerdatei</span><span class="sxs-lookup"><span data-stu-id="b8d1a-106">Header file:</span></span>  <br/> |<span data-ttu-id="b8d1a-107">Mapidefs. h</span><span class="sxs-lookup"><span data-stu-id="b8d1a-107">Mapidefs.h</span></span>  <br/> |
   
```cpp
typedef struct _SAndRestriction
{
  ULONG cRes;
  LPSRestriction lpRes;
} SAndRestriction;

```

## <a name="members"></a><span data-ttu-id="b8d1a-108">Elemente</span><span class="sxs-lookup"><span data-stu-id="b8d1a-108">Members</span></span>

 <span data-ttu-id="b8d1a-109">**cRes**</span><span class="sxs-lookup"><span data-stu-id="b8d1a-109">**cRes**</span></span>
  
> <span data-ttu-id="b8d1a-110">Die Anzahl der Sucheinschränkungen im Array, auf die durch das **lpRes** -Element verwiesen wird.</span><span class="sxs-lookup"><span data-stu-id="b8d1a-110">Count of search restrictions in the array pointed to by the **lpRes** member.</span></span> 
    
 <span data-ttu-id="b8d1a-111">**lpRes**</span><span class="sxs-lookup"><span data-stu-id="b8d1a-111">**lpRes**</span></span>
  
> <span data-ttu-id="b8d1a-112">Zeiger auf ein Array von [SRestriction](srestriction.md) -Strukturen, die mit einer logischen **and-** Operation kombiniert werden.</span><span class="sxs-lookup"><span data-stu-id="b8d1a-112">Pointer to an array of [SRestriction](srestriction.md) structures that will be combined with a logical **AND** operation.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="b8d1a-113">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="b8d1a-113">Remarks</span></span>

<span data-ttu-id="b8d1a-114">Das Ergebnis des **SAndRestriction** ist true, wenn alle untergeordneten Einschränkungen zu true ausgewertet werden.</span><span class="sxs-lookup"><span data-stu-id="b8d1a-114">The result of the **SAndRestriction** is TRUE if all its child restrictions evaluate to TRUE.</span></span> <span data-ttu-id="b8d1a-115">Er ist FALSE, wenn eine untergeordnete Einschränkung als FALSE ausgewertet wird.</span><span class="sxs-lookup"><span data-stu-id="b8d1a-115">It is FALSE if any child restriction evaluates to FALSE.</span></span> 
  
<span data-ttu-id="b8d1a-116">Eine Beschreibung der Einschränkungen, ihre Erstellung und Beispielcode finden Sie unter [Informationen zu Einschränkungen](about-restrictions.md).</span><span class="sxs-lookup"><span data-stu-id="b8d1a-116">For a description of types of restrictions, how to build them, and sample code, see [About Restrictions](about-restrictions.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="b8d1a-117">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="b8d1a-117">See also</span></span>



[<span data-ttu-id="b8d1a-118">SRestriction</span><span class="sxs-lookup"><span data-stu-id="b8d1a-118">SRestriction</span></span>](srestriction.md)


[<span data-ttu-id="b8d1a-119">MAPI-Strukturen</span><span class="sxs-lookup"><span data-stu-id="b8d1a-119">MAPI Structures</span></span>](mapi-structures.md)

