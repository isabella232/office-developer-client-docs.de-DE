---
title: SSizeRestriction
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.SSizeRestriction
api_type:
- COM
ms.assetid: 4e7340d1-3cb9-4276-b83f-1c8f94acb909
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 24ceb7b5358447de3a240756227b86224d2c354c
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33439086"
---
# <a name="ssizerestriction"></a><span data-ttu-id="70413-103">SSizeRestriction</span><span class="sxs-lookup"><span data-stu-id="70413-103">SSizeRestriction</span></span>

  
  
<span data-ttu-id="70413-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="70413-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="70413-105">Beschreibt eine Größenbeschränkung, die zum Testen der Größe eines Eigenschaftswerts verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="70413-105">Describes a size restriction which is used to test the size of a property value.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="70413-106">Headerdatei</span><span class="sxs-lookup"><span data-stu-id="70413-106">Header file:</span></span>  <br/> |<span data-ttu-id="70413-107">Mapidefs. h</span><span class="sxs-lookup"><span data-stu-id="70413-107">Mapidefs.h</span></span>  <br/> |
   
```cpp
typedef struct _SSizeRestriction
{
  ULONG relop;
  ULONG ulPropTag;
  ULONG cb;
} SSizeRestriction;

```

## <a name="members"></a><span data-ttu-id="70413-108">Members</span><span class="sxs-lookup"><span data-stu-id="70413-108">Members</span></span>

 <span data-ttu-id="70413-109">**RelOp**</span><span class="sxs-lookup"><span data-stu-id="70413-109">**relop**</span></span>
  
> <span data-ttu-id="70413-110">Relationaler Operator, der im Größenvergleich verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="70413-110">Relational operator that is used in the size comparison.</span></span> <span data-ttu-id="70413-111">Folgende Werte sind möglich:</span><span class="sxs-lookup"><span data-stu-id="70413-111">Possible values are as follows:</span></span> 
    
<span data-ttu-id="70413-112">RELOP_GE</span><span class="sxs-lookup"><span data-stu-id="70413-112">RELOP_GE</span></span> 
  
> <span data-ttu-id="70413-113">Der Vergleich erfolgt basierend auf einem größer oder gleich dem ersten Wert.</span><span class="sxs-lookup"><span data-stu-id="70413-113">The comparison is made based on a greater or equal first value.</span></span>
    
<span data-ttu-id="70413-114">RELOP_GT</span><span class="sxs-lookup"><span data-stu-id="70413-114">RELOP_GT</span></span> 
  
> <span data-ttu-id="70413-115">Der Vergleich erfolgt basierend auf einem höheren ersten Wert.</span><span class="sxs-lookup"><span data-stu-id="70413-115">The comparison is made based on a greater first value.</span></span>
    
<span data-ttu-id="70413-116">RELOP_LE</span><span class="sxs-lookup"><span data-stu-id="70413-116">RELOP_LE</span></span> 
  
> <span data-ttu-id="70413-117">Der Vergleich erfolgt basierend auf einem niedrigeren oder gleichen ersten Wert.</span><span class="sxs-lookup"><span data-stu-id="70413-117">The comparison is made based on a lesser or equal first value.</span></span>
    
<span data-ttu-id="70413-118">RELOP_LT</span><span class="sxs-lookup"><span data-stu-id="70413-118">RELOP_LT</span></span> 
  
> <span data-ttu-id="70413-119">Der Vergleich erfolgt basierend auf einem niedrigeren ersten Wert.</span><span class="sxs-lookup"><span data-stu-id="70413-119">The comparison is made based on a lesser first value.</span></span>
    
<span data-ttu-id="70413-120">RELOP_NE</span><span class="sxs-lookup"><span data-stu-id="70413-120">RELOP_NE</span></span> 
  
> <span data-ttu-id="70413-121">Der Vergleich erfolgt basierend auf ungleich Werten.</span><span class="sxs-lookup"><span data-stu-id="70413-121">The comparison is made based on unequal values.</span></span>
    
<span data-ttu-id="70413-122">RELOP_RE</span><span class="sxs-lookup"><span data-stu-id="70413-122">RELOP_RE</span></span> 
  
> <span data-ttu-id="70413-123">Der Vergleich basiert auf LIKE (Regular Expression)-Werten.</span><span class="sxs-lookup"><span data-stu-id="70413-123">The comparison is made based on LIKE (regular expression) values.</span></span>
    
<span data-ttu-id="70413-124">RELOP_EQ</span><span class="sxs-lookup"><span data-stu-id="70413-124">RELOP_EQ</span></span> 
  
> <span data-ttu-id="70413-125">Der Vergleich erfolgt basierend auf gleichen Werten.</span><span class="sxs-lookup"><span data-stu-id="70413-125">The comparison is made based on equal values.</span></span>
    
 <span data-ttu-id="70413-126">**ulPropTag**</span><span class="sxs-lookup"><span data-stu-id="70413-126">**ulPropTag**</span></span>
  
> <span data-ttu-id="70413-127">Property-Tag, das die zu testende Eigenschaft identifiziert.</span><span class="sxs-lookup"><span data-stu-id="70413-127">Property tag identifying the property to test.</span></span>
    
 <span data-ttu-id="70413-128">**cb**</span><span class="sxs-lookup"><span data-stu-id="70413-128">**cb**</span></span>
  
> <span data-ttu-id="70413-129">Die Anzahl der Bytes im Eigenschaftswert.</span><span class="sxs-lookup"><span data-stu-id="70413-129">Count of bytes in the property value.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="70413-130">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="70413-130">Remarks</span></span>

<span data-ttu-id="70413-131">Eine allgemeine Erläuterung der Funktionsweise von Einschränkungen finden Sie unter [Informationen zu Einschränkungen](about-restrictions.md).</span><span class="sxs-lookup"><span data-stu-id="70413-131">For a general discussion of how restrictions work, see [About Restrictions](about-restrictions.md).</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="70413-132">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="70413-132">See also</span></span>



[<span data-ttu-id="70413-133">SRestriction</span><span class="sxs-lookup"><span data-stu-id="70413-133">SRestriction</span></span>](srestriction.md)


[<span data-ttu-id="70413-134">MAPI-Strukturen</span><span class="sxs-lookup"><span data-stu-id="70413-134">MAPI Structures</span></span>](mapi-structures.md)

