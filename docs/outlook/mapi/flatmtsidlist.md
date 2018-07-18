---
title: FLATMTSIDLIST
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.FLATMTSIDLIST
api_type:
- COM
ms.assetid: b66c2815-72bc-4535-b34c-899bb830f29e
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: ea841ef4bc551581fb2d9ca90201b4615e67f134
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19791698"
---
# <a name="flatmtsidlist"></a><span data-ttu-id="986f2-103">FLATMTSIDLIST</span><span class="sxs-lookup"><span data-stu-id="986f2-103">FLATMTSIDLIST</span></span>

  
  
<span data-ttu-id="986f2-104">**Betrifft**: Outlook</span><span class="sxs-lookup"><span data-stu-id="986f2-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="986f2-105">Enthält ein Array von [MTSID](mtsid.md) -Strukturen, von denen jedes einen x. 400-Nachricht Transport System (MTS) Eintrag Bezeichner enthält.</span><span class="sxs-lookup"><span data-stu-id="986f2-105">Contains an array of [MTSID](mtsid.md) structures, each of which contains an X.400 message transport system (MTS) entry identifier.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="986f2-106">Headerdatei</span><span class="sxs-lookup"><span data-stu-id="986f2-106">Header file:</span></span>  <br/> |<span data-ttu-id="986f2-107">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="986f2-107">Mapidefs.h</span></span>  <br/> |
|<span data-ttu-id="986f2-108">Verwandte Makros:</span><span class="sxs-lookup"><span data-stu-id="986f2-108">Related macros:</span></span>  <br/> |<span data-ttu-id="986f2-109">[CbFLATMTSIDLIST](cbflatmtsidlist.md), [CbNewFLATMTSIDLIST](cbnewflatmtsidlist.md)</span><span class="sxs-lookup"><span data-stu-id="986f2-109">[CbFLATMTSIDLIST](cbflatmtsidlist.md), [CbNewFLATMTSIDLIST](cbnewflatmtsidlist.md)</span></span> <br/> |
   
```cpp
typedef struct
{
  ULONG cMTSIDs;
  ULONG cbMTSIDs;
  BYTE abMTSIDs[MAPI_DIM];
} FLATMTSIDLIST, FAR *LPFLATMTSIDLIST;

```

## <a name="members"></a><span data-ttu-id="986f2-110">Elemente</span><span class="sxs-lookup"><span data-stu-id="986f2-110">Members</span></span>

 <span data-ttu-id="986f2-111">**cMTSIDs**</span><span class="sxs-lookup"><span data-stu-id="986f2-111">**cMTSIDs**</span></span>
  
> <span data-ttu-id="986f2-112">Anzahl der **MTSID** Strukturen in das Array von **AbMTSIDs** -Elements beschrieben.</span><span class="sxs-lookup"><span data-stu-id="986f2-112">Count of **MTSID** structures in the array described by the **abMTSIDs** member.</span></span> 
    
 <span data-ttu-id="986f2-113">**cbMTSIDs**</span><span class="sxs-lookup"><span data-stu-id="986f2-113">**cbMTSIDs**</span></span>
  
> <span data-ttu-id="986f2-114">Die Anzahl von Bytes im Array von **AbMTSIDs**beschrieben.</span><span class="sxs-lookup"><span data-stu-id="986f2-114">Count of bytes in the array described by **abMTSIDs**.</span></span>
    
 <span data-ttu-id="986f2-115">**abMTSIDs**</span><span class="sxs-lookup"><span data-stu-id="986f2-115">**abMTSIDs**</span></span>
  
> <span data-ttu-id="986f2-116">Bytearray, das eine oder mehrere **MTSID** Strukturen enthält.</span><span class="sxs-lookup"><span data-stu-id="986f2-116">Byte array that contains one or more **MTSID** structures.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="986f2-117">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="986f2-117">Remarks</span></span>

<span data-ttu-id="986f2-118">Die **FLATMTSIDLIST** Struktur Verwendung in x. 400-messaging entspricht der [FLATENTRYLIST](flatentrylist.md) -Struktur Verwendung in MAPI messaging.</span><span class="sxs-lookup"><span data-stu-id="986f2-118">The **FLATMTSIDLIST** structure's use in X.400 messaging corresponds to the [FLATENTRYLIST](flatentrylist.md) structure's use in MAPI messaging.</span></span> <span data-ttu-id="986f2-119">MAPI verwendet **FLATMTSIDLIST** Strukturen zum Verwalten von x. 400-Eigenschaften während der Verarbeitung der Nachricht.</span><span class="sxs-lookup"><span data-stu-id="986f2-119">MAPI uses **FLATMTSIDLIST** structures to maintain X.400 properties during message handling.</span></span> <span data-ttu-id="986f2-120">Dienstanbieter verwenden **FLATMTSIDLIST** Strukturen beim Verarbeiten von eingehender und ausgehender x. 400-Nachrichten.</span><span class="sxs-lookup"><span data-stu-id="986f2-120">Service providers use **FLATMTSIDLIST** structures when handling incoming and outgoing X.400 messages.</span></span> 
  
<span data-ttu-id="986f2-121">Im Array **AbMTSIDs** wird jede **MTSID** Struktur auf einer vertrauten ausgerichtete Grenze ausgerichtet.</span><span class="sxs-lookup"><span data-stu-id="986f2-121">In the **abMTSIDs** array, each **MTSID** structure is aligned on a naturally aligned boundary.</span></span> <span data-ttu-id="986f2-122">Zusätzliche Bytes sind als Abstand, stellen Sie sicher, dass natürlichen Ausrichtung alle zweier **MTSID** Strukturen enthalten.</span><span class="sxs-lookup"><span data-stu-id="986f2-122">Extra bytes are included as padding to make sure natural alignment between any two **MTSID** structures.</span></span> <span data-ttu-id="986f2-123">Die erste **MTSID** Struktur im Array ist immer ordnungsgemäß ausgerichtet werden, da der Versatz des Elements **AbMTSIDs** 8 ist.</span><span class="sxs-lookup"><span data-stu-id="986f2-123">The first **MTSID** structure in the array is always aligned correctly because the offset of the **abMTSIDs** member is 8.</span></span> <span data-ttu-id="986f2-124">Berechnen Sie den Offset der nächsten Struktur, verwenden Sie die Größe des ersten Eintrags aufgerundet auf das nächste Vielfache von 4.</span><span class="sxs-lookup"><span data-stu-id="986f2-124">To compute the offset of the next structure, use the size of the first entry rounded up to the next multiple of 4.</span></span> <span data-ttu-id="986f2-125">Verwenden Sie das Makro [CbNewMTSID](cbnewmtsid.md) , um die Größe einer **MTSID** -Struktur zu berechnen.</span><span class="sxs-lookup"><span data-stu-id="986f2-125">Use the [CbNewMTSID](cbnewmtsid.md) macro to compute the size of an **MTSID** structure.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="986f2-126">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="986f2-126">See also</span></span>



[<span data-ttu-id="986f2-127">CbNewFLATMTSIDLIST</span><span class="sxs-lookup"><span data-stu-id="986f2-127">CbNewFLATMTSIDLIST</span></span>](cbnewflatmtsidlist.md)
  
[<span data-ttu-id="986f2-128">FLATENTRYLIST</span><span class="sxs-lookup"><span data-stu-id="986f2-128">FLATENTRYLIST</span></span>](flatentrylist.md)
  
[<span data-ttu-id="986f2-129">MTSID</span><span class="sxs-lookup"><span data-stu-id="986f2-129">MTSID</span></span>](mtsid.md)


[<span data-ttu-id="986f2-130">MAPI-Strukturen</span><span class="sxs-lookup"><span data-stu-id="986f2-130">MAPI Structures</span></span>](mapi-structures.md)

