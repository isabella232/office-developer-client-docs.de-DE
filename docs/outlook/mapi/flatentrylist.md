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
# <a name="flatentrylist"></a><span data-ttu-id="78d46-103">FLATENTRYLIST</span><span class="sxs-lookup"><span data-stu-id="78d46-103">FLATENTRYLIST</span></span>

<span data-ttu-id="78d46-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="78d46-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="78d46-105">Enthält ein Array von [FLATENTRY-Strukturen.](flatentry.md)</span><span class="sxs-lookup"><span data-stu-id="78d46-105">Contains an array of [FLATENTRY](flatentry.md) structures.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="78d46-106">Headerdatei</span><span class="sxs-lookup"><span data-stu-id="78d46-106">Header file:</span></span>  <br/> |<span data-ttu-id="78d46-107">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="78d46-107">Mapidefs.h</span></span>  <br/> |
|<span data-ttu-id="78d46-108">Verwandte Makros:</span><span class="sxs-lookup"><span data-stu-id="78d46-108">Related macros:</span></span>  <br/> |<span data-ttu-id="78d46-109">[CbFLATENTRYLIST](cbflatentrylist.md), [CbNewFLATENTRYLIST](cbnewflatentrylist.md)</span><span class="sxs-lookup"><span data-stu-id="78d46-109">[CbFLATENTRYLIST](cbflatentrylist.md), [CbNewFLATENTRYLIST](cbnewflatentrylist.md)</span></span> <br/> |
   
```cpp
typedef struct
{
  ULONG cEntries;
  ULONG cbEntries;
  BYTE abEntries[MAPI_DIM];
} FLATENTRYLIST, FAR *LPFLATENTRYLIST;

```

## <a name="members"></a><span data-ttu-id="78d46-110">Elemente</span><span class="sxs-lookup"><span data-stu-id="78d46-110">Members</span></span>

<span data-ttu-id="78d46-111">**cEntries**</span><span class="sxs-lookup"><span data-stu-id="78d46-111">**cEntries**</span></span>
  
> <span data-ttu-id="78d46-112">Anzahl der **FLATENTRY-Strukturen** im Array, das vom **abEntries-Element beschrieben** wird.</span><span class="sxs-lookup"><span data-stu-id="78d46-112">Count of **FLATENTRY** structures in the array described by the **abEntries** member.</span></span> 
    
<span data-ttu-id="78d46-113">**cbEntries**</span><span class="sxs-lookup"><span data-stu-id="78d46-113">**cbEntries**</span></span>
  
> <span data-ttu-id="78d46-114">Anzahl der Byte im array, das von **abEntries beschrieben wird.**</span><span class="sxs-lookup"><span data-stu-id="78d46-114">Count of bytes in the array described by **abEntries**.</span></span> 
    
<span data-ttu-id="78d46-115">**abEntries**</span><span class="sxs-lookup"><span data-stu-id="78d46-115">**abEntries**</span></span>
  
> <span data-ttu-id="78d46-116">Bytearray, das eine oder mehrere **FLATENTRY-Strukturen** enthält, zwischen Ende und Ende angeordnet.</span><span class="sxs-lookup"><span data-stu-id="78d46-116">Byte array that contains one or more **FLATENTRY** structures, arranged end to end.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="78d46-117">Hinweise</span><span class="sxs-lookup"><span data-stu-id="78d46-117">Remarks</span></span>

<span data-ttu-id="78d46-118">Im **abEntries-Array** wird jede **FLATENTRY-Struktur** an einer natürlich ausgerichteten Grenze ausgerichtet.</span><span class="sxs-lookup"><span data-stu-id="78d46-118">In the **abEntries** array, each **FLATENTRY** structure is aligned on a naturally aligned boundary.</span></span> <span data-ttu-id="78d46-119">Zusätzliche Bytes sind als Abstand enthalten, um die natürliche Ausrichtung zwischen zwei **FLATENTRY-Strukturen sicherzustellen.**</span><span class="sxs-lookup"><span data-stu-id="78d46-119">Extra bytes are included as padding to make sure natural alignment between any two **FLATENTRY** structures.</span></span> <span data-ttu-id="78d46-120">Die erste **FLATENTRY-Struktur** im Array wird immer richtig ausgerichtet, da der Offset des **abEntries-Mitglieds** 8 ist.</span><span class="sxs-lookup"><span data-stu-id="78d46-120">The first **FLATENTRY** structure in the array is always aligned correctly because the offset of the **abEntries** member is 8.</span></span> <span data-ttu-id="78d46-121">Verwenden Sie zum Berechnen des Offsets der nächsten Struktur die Größe des ersten Eintrags, der auf das nächste Vielfache von 4 aufgerundet wurde.</span><span class="sxs-lookup"><span data-stu-id="78d46-121">To compute the offset of the next structure, use the size of the first entry rounded up to the next multiple of 4.</span></span> <span data-ttu-id="78d46-122">Verwenden Sie das [CbFLATENTRY-Makro,](cbflatentry.md) um die Größe einer **FLATENTRY-Struktur zu** berechnen.</span><span class="sxs-lookup"><span data-stu-id="78d46-122">Use the [CbFLATENTRY](cbflatentry.md) macro to compute the size of a **FLATENTRY** structure.</span></span> 
  
<span data-ttu-id="78d46-123">Die zweite **FLATENTRY-Struktur** beginnt beispielsweise bei einem Offset, der aus dem Offset des ersten Eintrags plus der Länge des ersten Eintrags besteht, der auf die nächsten vier Bytes gerundet wird.</span><span class="sxs-lookup"><span data-stu-id="78d46-123">For example, the second **FLATENTRY** structure starts at an offset that consists of the offset of the first entry plus the length of the first entry rounded to the next four bytes.</span></span> <span data-ttu-id="78d46-124">Die Länge des ersten Eintrags ist die Länge des **cb-Mitglieds** plus die Länge des **abEntry-Mitglieds.**</span><span class="sxs-lookup"><span data-stu-id="78d46-124">The length of the first entry is the length of its **cb** member plus the length of its **abEntry** member.</span></span> 
  
<span data-ttu-id="78d46-125">Das folgende Codebeispiel zeigt, wie Offsets in einer **FLATENTRYLIST-Struktur berechnet** werden.</span><span class="sxs-lookup"><span data-stu-id="78d46-125">The following code sample indicates how to compute offsets in a **FLATENTRYLIST** structure.</span></span> <span data-ttu-id="78d46-126">Angenommen,  _lpFlatEntry_ ist ein Zeiger auf die erste Struktur in der Liste.</span><span class="sxs-lookup"><span data-stu-id="78d46-126">Assume that  _lpFlatEntry_ is a pointer to the first structure in the list.</span></span> 
  
```cpp
(offsetof(lpFlatEntry->ab) // for example, 4
+ lpFlatEntry->cb // size of lpFlatEntry->ab 
+ 4) & ~3 // round to next 4 byte boundary
```

## <a name="see-also"></a><span data-ttu-id="78d46-127">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="78d46-127">See also</span></span>

- [<span data-ttu-id="78d46-128">FLATENTRY</span><span class="sxs-lookup"><span data-stu-id="78d46-128">FLATENTRY</span></span>](flatentry.md)
- [<span data-ttu-id="78d46-129">PidTagReplyRecipientEntries (kanonische Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="78d46-129">PidTagReplyRecipientEntries Canonical Property</span></span>](pidtagreplyrecipiententries-canonical-property.md)
- [<span data-ttu-id="78d46-130">MAPI-Strukturen</span><span class="sxs-lookup"><span data-stu-id="78d46-130">MAPI Structures</span></span>](mapi-structures.md)

