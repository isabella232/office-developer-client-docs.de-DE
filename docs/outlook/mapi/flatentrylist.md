---
title: FLATENTRYLIST
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.FLATENTRYLIST
api_type:
- COM
ms.assetid: b465d015-9b62-4986-b0df-118121f60602
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: a8f17c3cf3d3d00930f87acd004b24f683a3fc8c
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19791694"
---
# <a name="flatentrylist"></a><span data-ttu-id="0df52-103">FLATENTRYLIST</span><span class="sxs-lookup"><span data-stu-id="0df52-103">FLATENTRYLIST</span></span>

<span data-ttu-id="0df52-104">**Betrifft**: Outlook</span><span class="sxs-lookup"><span data-stu-id="0df52-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="0df52-105">Enthält ein Array von [FLATENTRY](flatentry.md) -Strukturen.</span><span class="sxs-lookup"><span data-stu-id="0df52-105">Contains an array of [FLATENTRY](flatentry.md) structures.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="0df52-106">Headerdatei</span><span class="sxs-lookup"><span data-stu-id="0df52-106">Header file:</span></span>  <br/> |<span data-ttu-id="0df52-107">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="0df52-107">Mapidefs.h</span></span>  <br/> |
|<span data-ttu-id="0df52-108">Verwandte Makros:</span><span class="sxs-lookup"><span data-stu-id="0df52-108">Related macros:</span></span>  <br/> |<span data-ttu-id="0df52-109">[CbFLATENTRYLIST](cbflatentrylist.md), [CbNewFLATENTRYLIST](cbnewflatentrylist.md)</span><span class="sxs-lookup"><span data-stu-id="0df52-109">[CbFLATENTRYLIST](cbflatentrylist.md), [CbNewFLATENTRYLIST](cbnewflatentrylist.md)</span></span> <br/> |
   
```cpp
typedef struct
{
  ULONG cEntries;
  ULONG cbEntries;
  BYTE abEntries[MAPI_DIM];
} FLATENTRYLIST, FAR *LPFLATENTRYLIST;

```

## <a name="members"></a><span data-ttu-id="0df52-110">Elemente</span><span class="sxs-lookup"><span data-stu-id="0df52-110">Members</span></span>

<span data-ttu-id="0df52-111">**cEntries**</span><span class="sxs-lookup"><span data-stu-id="0df52-111">**cEntries**</span></span>
  
> <span data-ttu-id="0df52-112">Anzahl der **FLATENTRY** Strukturen in das Array von **AbEntries** -Elements beschrieben.</span><span class="sxs-lookup"><span data-stu-id="0df52-112">Count of **FLATENTRY** structures in the array described by the **abEntries** member.</span></span> 
    
<span data-ttu-id="0df52-113">**cbEntries**</span><span class="sxs-lookup"><span data-stu-id="0df52-113">**cbEntries**</span></span>
  
> <span data-ttu-id="0df52-114">Die Anzahl von Bytes im Array von **AbEntries**beschrieben.</span><span class="sxs-lookup"><span data-stu-id="0df52-114">Count of bytes in the array described by **abEntries**.</span></span> 
    
<span data-ttu-id="0df52-115">**abEntries**</span><span class="sxs-lookup"><span data-stu-id="0df52-115">**abEntries**</span></span>
  
> <span data-ttu-id="0df52-116">Byte-Array, das ein oder mehrere **FLATENTRY** Strukturen enthält angeordnete Ende zu Ende.</span><span class="sxs-lookup"><span data-stu-id="0df52-116">Byte array that contains one or more **FLATENTRY** structures, arranged end to end.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="0df52-117">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="0df52-117">Remarks</span></span>

<span data-ttu-id="0df52-118">Im Array **AbEntries** wird jede **FLATENTRY** Struktur auf einer vertrauten ausgerichtete Grenze ausgerichtet.</span><span class="sxs-lookup"><span data-stu-id="0df52-118">In the **abEntries** array, each **FLATENTRY** structure is aligned on a naturally aligned boundary.</span></span> <span data-ttu-id="0df52-119">Zusätzliche Bytes sind als Abstand, stellen Sie sicher, dass natürlichen Ausrichtung alle zweier **FLATENTRY** Strukturen enthalten.</span><span class="sxs-lookup"><span data-stu-id="0df52-119">Extra bytes are included as padding to make sure natural alignment between any two **FLATENTRY** structures.</span></span> <span data-ttu-id="0df52-120">Die erste **FLATENTRY** Struktur im Array ist immer ordnungsgemäß ausgerichtet werden, da der Versatz des Elements **AbEntries** 8 ist.</span><span class="sxs-lookup"><span data-stu-id="0df52-120">The first **FLATENTRY** structure in the array is always aligned correctly because the offset of the **abEntries** member is 8.</span></span> <span data-ttu-id="0df52-121">Berechnen Sie den Offset der nächsten Struktur, verwenden Sie die Größe des ersten Eintrags aufgerundet auf das nächste Vielfache von 4.</span><span class="sxs-lookup"><span data-stu-id="0df52-121">To compute the offset of the next structure, use the size of the first entry rounded up to the next multiple of 4.</span></span> <span data-ttu-id="0df52-122">Verwenden Sie das Makro [CbFLATENTRY](cbflatentry.md) , um die Größe einer **FLATENTRY** -Struktur zu berechnen.</span><span class="sxs-lookup"><span data-stu-id="0df52-122">Use the [CbFLATENTRY](cbflatentry.md) macro to compute the size of a **FLATENTRY** structure.</span></span> 
  
<span data-ttu-id="0df52-123">Die zweite **FLATENTRY** -Struktur beginnt mit einem Offset, der den Offset des ersten Eintrags plus die Länge des ersten Eintrags gerundet auf die nächsten vier Bytes besteht.</span><span class="sxs-lookup"><span data-stu-id="0df52-123">For example, the second **FLATENTRY** structure starts at an offset that consists of the offset of the first entry plus the length of the first entry rounded to the next four bytes.</span></span> <span data-ttu-id="0df52-124">Die Länge des ersten Eintrags beträgt die Länge der **Cb** Mitglied plus die Länge des **AbEntry** Mitglied.</span><span class="sxs-lookup"><span data-stu-id="0df52-124">The length of the first entry is the length of its **cb** member plus the length of its **abEntry** member.</span></span> 
  
<span data-ttu-id="0df52-125">Im folgenden Codebeispiel gibt an, wie Offsets in einer **FLATENTRYLIST** -Struktur zu berechnen.</span><span class="sxs-lookup"><span data-stu-id="0df52-125">The following code sample indicates how to compute offsets in a **FLATENTRYLIST** structure.</span></span> <span data-ttu-id="0df52-126">Wird davon ausgegangen Sie, dass diese _LpFlatEntry_ einen Zeiger auf die erste Struktur in der Liste ist.</span><span class="sxs-lookup"><span data-stu-id="0df52-126">Assume that  _lpFlatEntry_ is a pointer to the first structure in the list.</span></span> 
  
```cpp
(offsetof(lpFlatEntry->ab) // for example, 4
+ lpFlatEntry->cb // size of lpFlatEntry->ab 
+ 4) & ~3 // round to next 4 byte boundary
```

## <a name="see-also"></a><span data-ttu-id="0df52-127">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="0df52-127">See also</span></span>

- [<span data-ttu-id="0df52-128">FLATENTRY</span><span class="sxs-lookup"><span data-stu-id="0df52-128">FLATENTRY</span></span>](flatentry.md)
- [<span data-ttu-id="0df52-129">PidTagReplyRecipientEntries (kanonische Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="0df52-129">PidTagReplyRecipientEntries Canonical Property</span></span>](pidtagreplyrecipiententries-canonical-property.md)
- [<span data-ttu-id="0df52-130">MAPI-Strukturen</span><span class="sxs-lookup"><span data-stu-id="0df52-130">MAPI Structures</span></span>](mapi-structures.md)

