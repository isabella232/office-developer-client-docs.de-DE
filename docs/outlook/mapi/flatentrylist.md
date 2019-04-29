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
ms.openlocfilehash: bc511ea4b3ec4eea9e38f744bcb8f277108085cc
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33413857"
---
# <a name="flatentrylist"></a><span data-ttu-id="f7cc8-103">FLATENTRYLIST</span><span class="sxs-lookup"><span data-stu-id="f7cc8-103">FLATENTRYLIST</span></span>

<span data-ttu-id="f7cc8-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="f7cc8-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="f7cc8-105">Enthält ein Array von [FLATENTRY](flatentry.md) -Strukturen.</span><span class="sxs-lookup"><span data-stu-id="f7cc8-105">Contains an array of [FLATENTRY](flatentry.md) structures.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="f7cc8-106">Headerdatei</span><span class="sxs-lookup"><span data-stu-id="f7cc8-106">Header file:</span></span>  <br/> |<span data-ttu-id="f7cc8-107">Mapidefs. h</span><span class="sxs-lookup"><span data-stu-id="f7cc8-107">Mapidefs.h</span></span>  <br/> |
|<span data-ttu-id="f7cc8-108">Verwandte Makros:</span><span class="sxs-lookup"><span data-stu-id="f7cc8-108">Related macros:</span></span>  <br/> |<span data-ttu-id="f7cc8-109">[CbFLATENTRYLIST](cbflatentrylist.md), [CbNewFLATENTRYLIST](cbnewflatentrylist.md)</span><span class="sxs-lookup"><span data-stu-id="f7cc8-109">[CbFLATENTRYLIST](cbflatentrylist.md), [CbNewFLATENTRYLIST](cbnewflatentrylist.md)</span></span> <br/> |
   
```cpp
typedef struct
{
  ULONG cEntries;
  ULONG cbEntries;
  BYTE abEntries[MAPI_DIM];
} FLATENTRYLIST, FAR *LPFLATENTRYLIST;

```

## <a name="members"></a><span data-ttu-id="f7cc8-110">Members</span><span class="sxs-lookup"><span data-stu-id="f7cc8-110">Members</span></span>

<span data-ttu-id="f7cc8-111">**Zentriert**</span><span class="sxs-lookup"><span data-stu-id="f7cc8-111">**cEntries**</span></span>
  
> <span data-ttu-id="f7cc8-112">Die Anzahl der **FLATENTRY** -Strukturen in dem vom **abEntries** -Element beschriebenen Array.</span><span class="sxs-lookup"><span data-stu-id="f7cc8-112">Count of **FLATENTRY** structures in the array described by the **abEntries** member.</span></span> 
    
<span data-ttu-id="f7cc8-113">**cbEntries**</span><span class="sxs-lookup"><span data-stu-id="f7cc8-113">**cbEntries**</span></span>
  
> <span data-ttu-id="f7cc8-114">Die Anzahl der Bytes im von **abEntries**beschriebenen Array.</span><span class="sxs-lookup"><span data-stu-id="f7cc8-114">Count of bytes in the array described by **abEntries**.</span></span> 
    
<span data-ttu-id="f7cc8-115">**abEntries**</span><span class="sxs-lookup"><span data-stu-id="f7cc8-115">**abEntries**</span></span>
  
> <span data-ttu-id="f7cc8-116">Bytearray, das eine oder mehrere **FLATENTRY** -Strukturen enthält, die bis zum Ende angeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="f7cc8-116">Byte array that contains one or more **FLATENTRY** structures, arranged end to end.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="f7cc8-117">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="f7cc8-117">Remarks</span></span>

<span data-ttu-id="f7cc8-118">Im **abEntries** -Array wird jede **FLATENTRY** -Struktur an einer natürlich ausgerichteten Grenze ausgerichtet.</span><span class="sxs-lookup"><span data-stu-id="f7cc8-118">In the **abEntries** array, each **FLATENTRY** structure is aligned on a naturally aligned boundary.</span></span> <span data-ttu-id="f7cc8-119">Zusätzliche Bytes sind als Padding enthalten, um eine natürliche Ausrichtung zwischen zwei **FLATENTRY** -Strukturen sicherzustellen.</span><span class="sxs-lookup"><span data-stu-id="f7cc8-119">Extra bytes are included as padding to make sure natural alignment between any two **FLATENTRY** structures.</span></span> <span data-ttu-id="f7cc8-120">Die erste **FLATENTRY** -Struktur im Array wird immer korrekt ausgerichtet, da der Offset des **abEntries** -Elements 8 ist.</span><span class="sxs-lookup"><span data-stu-id="f7cc8-120">The first **FLATENTRY** structure in the array is always aligned correctly because the offset of the **abEntries** member is 8.</span></span> <span data-ttu-id="f7cc8-121">Um den Offset der nächsten Struktur zu berechnen, verwenden Sie die Größe des ersten Eintrags, aufgerundet auf das nächste Vielfache von 4.</span><span class="sxs-lookup"><span data-stu-id="f7cc8-121">To compute the offset of the next structure, use the size of the first entry rounded up to the next multiple of 4.</span></span> <span data-ttu-id="f7cc8-122">Verwenden Sie das [CbFLATENTRY](cbflatentry.md) -Makro, um die Größe einer **FLATENTRY** -Struktur zu berechnen.</span><span class="sxs-lookup"><span data-stu-id="f7cc8-122">Use the [CbFLATENTRY](cbflatentry.md) macro to compute the size of a **FLATENTRY** structure.</span></span> 
  
<span data-ttu-id="f7cc8-123">Beispielsweise beginnt die zweite **FLATENTRY** -Struktur mit einem Offset, der aus dem Offset des ersten Eintrags und der Länge des ersten Eintrags besteht, gerundet auf die nächsten vier Bytes.</span><span class="sxs-lookup"><span data-stu-id="f7cc8-123">For example, the second **FLATENTRY** structure starts at an offset that consists of the offset of the first entry plus the length of the first entry rounded to the next four bytes.</span></span> <span data-ttu-id="f7cc8-124">Die Länge des ersten Eintrags entspricht der Länge des **CB** -Elements sowie der Länge des **abEntry** -Elements.</span><span class="sxs-lookup"><span data-stu-id="f7cc8-124">The length of the first entry is the length of its **cb** member plus the length of its **abEntry** member.</span></span> 
  
<span data-ttu-id="f7cc8-125">Das folgende Codebeispiel gibt an, wie Offsets in einer **FLATENTRYLIST** -Struktur berechnet werden.</span><span class="sxs-lookup"><span data-stu-id="f7cc8-125">The following code sample indicates how to compute offsets in a **FLATENTRYLIST** structure.</span></span> <span data-ttu-id="f7cc8-126">Gehen Sie davon aus, dass _lpFlatEntry_ ein Zeiger auf die erste Struktur in der Liste ist.</span><span class="sxs-lookup"><span data-stu-id="f7cc8-126">Assume that  _lpFlatEntry_ is a pointer to the first structure in the list.</span></span> 
  
```cpp
(offsetof(lpFlatEntry->ab) // for example, 4
+ lpFlatEntry->cb // size of lpFlatEntry->ab 
+ 4) & ~3 // round to next 4 byte boundary
```

## <a name="see-also"></a><span data-ttu-id="f7cc8-127">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="f7cc8-127">See also</span></span>

- [<span data-ttu-id="f7cc8-128">FLATENTRY</span><span class="sxs-lookup"><span data-stu-id="f7cc8-128">FLATENTRY</span></span>](flatentry.md)
- [<span data-ttu-id="f7cc8-129">Kanonische Pidtagreplyrecipiententries (-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="f7cc8-129">PidTagReplyRecipientEntries Canonical Property</span></span>](pidtagreplyrecipiententries-canonical-property.md)
- [<span data-ttu-id="f7cc8-130">MAPI-Strukturen</span><span class="sxs-lookup"><span data-stu-id="f7cc8-130">MAPI Structures</span></span>](mapi-structures.md)

