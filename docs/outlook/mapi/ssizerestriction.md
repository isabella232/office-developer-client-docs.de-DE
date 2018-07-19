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
ms.openlocfilehash: 134eb844ef7b72d396c300b27a87a3a7ae320cf1
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19795635"
---
# <a name="ssizerestriction"></a><span data-ttu-id="5aadd-103">SSizeRestriction</span><span class="sxs-lookup"><span data-stu-id="5aadd-103">SSizeRestriction</span></span>

  
  
<span data-ttu-id="5aadd-104">**Betrifft**: Outlook</span><span class="sxs-lookup"><span data-stu-id="5aadd-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="5aadd-105">Beschreibt eine Beschränkung der Größe der verwendet wird, um die Größe der Wert einer Eigenschaft zu testen.</span><span class="sxs-lookup"><span data-stu-id="5aadd-105">Describes a size restriction which is used to test the size of a property value.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="5aadd-106">Headerdatei</span><span class="sxs-lookup"><span data-stu-id="5aadd-106">Header file:</span></span>  <br/> |<span data-ttu-id="5aadd-107">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="5aadd-107">Mapidefs.h</span></span>  <br/> |
   
```cpp
typedef struct _SSizeRestriction
{
  ULONG relop;
  ULONG ulPropTag;
  ULONG cb;
} SSizeRestriction;

```

## <a name="members"></a><span data-ttu-id="5aadd-108">Elemente</span><span class="sxs-lookup"><span data-stu-id="5aadd-108">Members</span></span>

 <span data-ttu-id="5aadd-109">**RelOp-Element**</span><span class="sxs-lookup"><span data-stu-id="5aadd-109">**relop**</span></span>
  
> <span data-ttu-id="5aadd-110">Relationale Operator, der in der Größenvergleich verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="5aadd-110">Relational operator that is used in the size comparison.</span></span> <span data-ttu-id="5aadd-111">Mögliche Werte sind wie folgt:</span><span class="sxs-lookup"><span data-stu-id="5aadd-111">Possible values are as follows:</span></span> 
    
<span data-ttu-id="5aadd-112">RELOP_GE</span><span class="sxs-lookup"><span data-stu-id="5aadd-112">RELOP_GE</span></span> 
  
> <span data-ttu-id="5aadd-113">Der Vergleich wird basierend auf der ersten Wert größer oder gleich vorgenommen.</span><span class="sxs-lookup"><span data-stu-id="5aadd-113">The comparison is made based on a greater or equal first value.</span></span>
    
<span data-ttu-id="5aadd-114">RELOP_GT</span><span class="sxs-lookup"><span data-stu-id="5aadd-114">RELOP_GT</span></span> 
  
> <span data-ttu-id="5aadd-115">Der Vergleich wird basierend auf einen höheren Wert für die erste vorgenommen.</span><span class="sxs-lookup"><span data-stu-id="5aadd-115">The comparison is made based on a greater first value.</span></span>
    
<span data-ttu-id="5aadd-116">RELOP_LE</span><span class="sxs-lookup"><span data-stu-id="5aadd-116">RELOP_LE</span></span> 
  
> <span data-ttu-id="5aadd-117">Der Vergleich wird basierend auf dem ersten Wert kleiner oder gleich vorgenommen.</span><span class="sxs-lookup"><span data-stu-id="5aadd-117">The comparison is made based on a lesser or equal first value.</span></span>
    
<span data-ttu-id="5aadd-118">RELOP_LT</span><span class="sxs-lookup"><span data-stu-id="5aadd-118">RELOP_LT</span></span> 
  
> <span data-ttu-id="5aadd-119">Der Vergleich wird basierend auf einen kleineren Wert des ersten vorgenommen.</span><span class="sxs-lookup"><span data-stu-id="5aadd-119">The comparison is made based on a lesser first value.</span></span>
    
<span data-ttu-id="5aadd-120">RELOP_NE</span><span class="sxs-lookup"><span data-stu-id="5aadd-120">RELOP_NE</span></span> 
  
> <span data-ttu-id="5aadd-121">Der Vergleich wird basierend auf Werten mit ungleicher vorgenommen.</span><span class="sxs-lookup"><span data-stu-id="5aadd-121">The comparison is made based on unequal values.</span></span>
    
<span data-ttu-id="5aadd-122">RELOP_RE</span><span class="sxs-lookup"><span data-stu-id="5aadd-122">RELOP_RE</span></span> 
  
> <span data-ttu-id="5aadd-123">Der Vergleich basierend auf wie Werte (reguläre Ausdrücke) erfolgt.</span><span class="sxs-lookup"><span data-stu-id="5aadd-123">The comparison is made based on LIKE (regular expression) values.</span></span>
    
<span data-ttu-id="5aadd-124">RELOP_EQ</span><span class="sxs-lookup"><span data-stu-id="5aadd-124">RELOP_EQ</span></span> 
  
> <span data-ttu-id="5aadd-125">Der Vergleich wird basierend auf gleich große Werte vorgenommen.</span><span class="sxs-lookup"><span data-stu-id="5aadd-125">The comparison is made based on equal values.</span></span>
    
 <span data-ttu-id="5aadd-126">**ulPropTag**</span><span class="sxs-lookup"><span data-stu-id="5aadd-126">**ulPropTag**</span></span>
  
> <span data-ttu-id="5aadd-127">Eigenschafts-Tag, die zu überprüfenden Eigenschaft identifiziert.</span><span class="sxs-lookup"><span data-stu-id="5aadd-127">Property tag identifying the property to test.</span></span>
    
 <span data-ttu-id="5aadd-128">**cb**</span><span class="sxs-lookup"><span data-stu-id="5aadd-128">**cb**</span></span>
  
> <span data-ttu-id="5aadd-129">Anzahl der Bytes in der Eigenschaftswert.</span><span class="sxs-lookup"><span data-stu-id="5aadd-129">Count of bytes in the property value.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="5aadd-130">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="5aadd-130">Remarks</span></span>

<span data-ttu-id="5aadd-131">Eine allgemeine Erläuterung der Funktionsweise von Einschränkungen finden Sie unter [Informationen zu Einschränkungen](about-restrictions.md).</span><span class="sxs-lookup"><span data-stu-id="5aadd-131">For a general discussion of how restrictions work, see [About Restrictions](about-restrictions.md).</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="5aadd-132">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="5aadd-132">See also</span></span>



[<span data-ttu-id="5aadd-133">SRestriction</span><span class="sxs-lookup"><span data-stu-id="5aadd-133">SRestriction</span></span>](srestriction.md)


[<span data-ttu-id="5aadd-134">MAPI-Strukturen</span><span class="sxs-lookup"><span data-stu-id="5aadd-134">MAPI Structures</span></span>](mapi-structures.md)

