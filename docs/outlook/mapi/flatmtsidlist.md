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
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: bd9bfe4d1411b84a7811235aa68728afaefe64ab
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33439219"
---
# <a name="flatmtsidlist"></a><span data-ttu-id="16d3b-103">FLATMTSIDLIST</span><span class="sxs-lookup"><span data-stu-id="16d3b-103">FLATMTSIDLIST</span></span>

  
  
<span data-ttu-id="16d3b-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="16d3b-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="16d3b-105">Enthält ein Array von [MTSID](mtsid.md) -Strukturen, die jeweils eine MTS-Eintrags-ID (X. 400-Nachrichtentransportsystem) enthalten.</span><span class="sxs-lookup"><span data-stu-id="16d3b-105">Contains an array of [MTSID](mtsid.md) structures, each of which contains an X.400 message transport system (MTS) entry identifier.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="16d3b-106">Headerdatei</span><span class="sxs-lookup"><span data-stu-id="16d3b-106">Header file:</span></span>  <br/> |<span data-ttu-id="16d3b-107">Mapidefs. h</span><span class="sxs-lookup"><span data-stu-id="16d3b-107">Mapidefs.h</span></span>  <br/> |
|<span data-ttu-id="16d3b-108">Verwandte Makros:</span><span class="sxs-lookup"><span data-stu-id="16d3b-108">Related macros:</span></span>  <br/> |<span data-ttu-id="16d3b-109">[CbFLATMTSIDLIST](cbflatmtsidlist.md), [CbNewFLATMTSIDLIST](cbnewflatmtsidlist.md)</span><span class="sxs-lookup"><span data-stu-id="16d3b-109">[CbFLATMTSIDLIST](cbflatmtsidlist.md), [CbNewFLATMTSIDLIST](cbnewflatmtsidlist.md)</span></span> <br/> |
   
```cpp
typedef struct
{
  ULONG cMTSIDs;
  ULONG cbMTSIDs;
  BYTE abMTSIDs[MAPI_DIM];
} FLATMTSIDLIST, FAR *LPFLATMTSIDLIST;

```

## <a name="members"></a><span data-ttu-id="16d3b-110">Members</span><span class="sxs-lookup"><span data-stu-id="16d3b-110">Members</span></span>

 <span data-ttu-id="16d3b-111">**cMTSIDs**</span><span class="sxs-lookup"><span data-stu-id="16d3b-111">**cMTSIDs**</span></span>
  
> <span data-ttu-id="16d3b-112">Die Anzahl der **MTSID** -Strukturen in dem vom **abMTSIDs** -Element beschriebenen Array.</span><span class="sxs-lookup"><span data-stu-id="16d3b-112">Count of **MTSID** structures in the array described by the **abMTSIDs** member.</span></span> 
    
 <span data-ttu-id="16d3b-113">**cbMTSIDs**</span><span class="sxs-lookup"><span data-stu-id="16d3b-113">**cbMTSIDs**</span></span>
  
> <span data-ttu-id="16d3b-114">Die Anzahl der Bytes im von **abMTSIDs**beschriebenen Array.</span><span class="sxs-lookup"><span data-stu-id="16d3b-114">Count of bytes in the array described by **abMTSIDs**.</span></span>
    
 <span data-ttu-id="16d3b-115">**abMTSIDs**</span><span class="sxs-lookup"><span data-stu-id="16d3b-115">**abMTSIDs**</span></span>
  
> <span data-ttu-id="16d3b-116">Bytearray, das eine oder mehrere **MTSID** -Strukturen enthält.</span><span class="sxs-lookup"><span data-stu-id="16d3b-116">Byte array that contains one or more **MTSID** structures.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="16d3b-117">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="16d3b-117">Remarks</span></span>

<span data-ttu-id="16d3b-118">Die Verwendung der **FLATMTSIDLIST** -Struktur in X. 400-Messaging entspricht der Verwendung der [FLATENTRYLIST](flatentrylist.md) -Struktur in MAPI-Messaging.</span><span class="sxs-lookup"><span data-stu-id="16d3b-118">The **FLATMTSIDLIST** structure's use in X.400 messaging corresponds to the [FLATENTRYLIST](flatentrylist.md) structure's use in MAPI messaging.</span></span> <span data-ttu-id="16d3b-119">MAPI verwendet **FLATMTSIDLIST** -Strukturen, um X. 400-Eigenschaften während der Nachrichtenverarbeitung zu verwalten.</span><span class="sxs-lookup"><span data-stu-id="16d3b-119">MAPI uses **FLATMTSIDLIST** structures to maintain X.400 properties during message handling.</span></span> <span data-ttu-id="16d3b-120">Dienstanbieter verwenden **FLATMTSIDLIST** -Strukturen, wenn Sie eingehende und ausgehende X. 400-Nachrichten verarbeiten.</span><span class="sxs-lookup"><span data-stu-id="16d3b-120">Service providers use **FLATMTSIDLIST** structures when handling incoming and outgoing X.400 messages.</span></span> 
  
<span data-ttu-id="16d3b-121">Im **abMTSIDs** -Array wird jede **MTSID** -Struktur an einer natürlich ausgerichteten Grenze ausgerichtet.</span><span class="sxs-lookup"><span data-stu-id="16d3b-121">In the **abMTSIDs** array, each **MTSID** structure is aligned on a naturally aligned boundary.</span></span> <span data-ttu-id="16d3b-122">Zusätzliche Bytes sind als Padding enthalten, um eine natürliche Ausrichtung zwischen zwei **MTSID** -Strukturen sicherzustellen.</span><span class="sxs-lookup"><span data-stu-id="16d3b-122">Extra bytes are included as padding to make sure natural alignment between any two **MTSID** structures.</span></span> <span data-ttu-id="16d3b-123">Die erste **MTSID** -Struktur im Array wird immer korrekt ausgerichtet, da der Offset des **abMTSIDs** -Elements 8 ist.</span><span class="sxs-lookup"><span data-stu-id="16d3b-123">The first **MTSID** structure in the array is always aligned correctly because the offset of the **abMTSIDs** member is 8.</span></span> <span data-ttu-id="16d3b-124">Um den Offset der nächsten Struktur zu berechnen, verwenden Sie die Größe des ersten Eintrags, aufgerundet auf das nächste Vielfache von 4.</span><span class="sxs-lookup"><span data-stu-id="16d3b-124">To compute the offset of the next structure, use the size of the first entry rounded up to the next multiple of 4.</span></span> <span data-ttu-id="16d3b-125">Verwenden Sie das [CbNewMTSID](cbnewmtsid.md) -Makro, um die Größe einer **MTSID** -Struktur zu berechnen.</span><span class="sxs-lookup"><span data-stu-id="16d3b-125">Use the [CbNewMTSID](cbnewmtsid.md) macro to compute the size of an **MTSID** structure.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="16d3b-126">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="16d3b-126">See also</span></span>



[<span data-ttu-id="16d3b-127">CbNewFLATMTSIDLIST</span><span class="sxs-lookup"><span data-stu-id="16d3b-127">CbNewFLATMTSIDLIST</span></span>](cbnewflatmtsidlist.md)
  
[<span data-ttu-id="16d3b-128">FLATENTRYLIST</span><span class="sxs-lookup"><span data-stu-id="16d3b-128">FLATENTRYLIST</span></span>](flatentrylist.md)
  
[<span data-ttu-id="16d3b-129">MTSID</span><span class="sxs-lookup"><span data-stu-id="16d3b-129">MTSID</span></span>](mtsid.md)


[<span data-ttu-id="16d3b-130">MAPI-Strukturen</span><span class="sxs-lookup"><span data-stu-id="16d3b-130">MAPI Structures</span></span>](mapi-structures.md)

