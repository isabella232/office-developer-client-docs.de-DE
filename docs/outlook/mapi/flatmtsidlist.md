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
# <a name="flatmtsidlist"></a><span data-ttu-id="03645-103">FLATMTSIDLIST</span><span class="sxs-lookup"><span data-stu-id="03645-103">FLATMTSIDLIST</span></span>

  
  
<span data-ttu-id="03645-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="03645-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="03645-105">Enthält ein Array von [MTSID-Strukturen,](mtsid.md) von denen jede einen X.400 Message Transport System (MTS)-Eintragsbezeichner enthält.</span><span class="sxs-lookup"><span data-stu-id="03645-105">Contains an array of [MTSID](mtsid.md) structures, each of which contains an X.400 message transport system (MTS) entry identifier.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="03645-106">Headerdatei</span><span class="sxs-lookup"><span data-stu-id="03645-106">Header file:</span></span>  <br/> |<span data-ttu-id="03645-107">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="03645-107">Mapidefs.h</span></span>  <br/> |
|<span data-ttu-id="03645-108">Verwandte Makros:</span><span class="sxs-lookup"><span data-stu-id="03645-108">Related macros:</span></span>  <br/> |<span data-ttu-id="03645-109">[CbFLATMTSIDLIST](cbflatmtsidlist.md), [CbNewFLATMTSIDLIST](cbnewflatmtsidlist.md)</span><span class="sxs-lookup"><span data-stu-id="03645-109">[CbFLATMTSIDLIST](cbflatmtsidlist.md), [CbNewFLATMTSIDLIST](cbnewflatmtsidlist.md)</span></span> <br/> |
   
```cpp
typedef struct
{
  ULONG cMTSIDs;
  ULONG cbMTSIDs;
  BYTE abMTSIDs[MAPI_DIM];
} FLATMTSIDLIST, FAR *LPFLATMTSIDLIST;

```

## <a name="members"></a><span data-ttu-id="03645-110">Elemente</span><span class="sxs-lookup"><span data-stu-id="03645-110">Members</span></span>

 <span data-ttu-id="03645-111">**cMTSIDs**</span><span class="sxs-lookup"><span data-stu-id="03645-111">**cMTSIDs**</span></span>
  
> <span data-ttu-id="03645-112">Anzahl der **MTSID-Strukturen** im array, das vom **abMTSIDs-Element beschrieben** wird.</span><span class="sxs-lookup"><span data-stu-id="03645-112">Count of **MTSID** structures in the array described by the **abMTSIDs** member.</span></span> 
    
 <span data-ttu-id="03645-113">**cbMTSIDs**</span><span class="sxs-lookup"><span data-stu-id="03645-113">**cbMTSIDs**</span></span>
  
> <span data-ttu-id="03645-114">Anzahl der Byte im Array, das von **abMTSIDs beschrieben wird.**</span><span class="sxs-lookup"><span data-stu-id="03645-114">Count of bytes in the array described by **abMTSIDs**.</span></span>
    
 <span data-ttu-id="03645-115">**abMTSIDs**</span><span class="sxs-lookup"><span data-stu-id="03645-115">**abMTSIDs**</span></span>
  
> <span data-ttu-id="03645-116">Bytearray, das eine oder mehrere **MTSID-Strukturen** enthält.</span><span class="sxs-lookup"><span data-stu-id="03645-116">Byte array that contains one or more **MTSID** structures.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="03645-117">Hinweise</span><span class="sxs-lookup"><span data-stu-id="03645-117">Remarks</span></span>

<span data-ttu-id="03645-118">Die **Verwendung der FLATMTSIDLIST-Struktur** in X.400-Messaging entspricht der Verwendung der [FLATENTRYLIST-Struktur](flatentrylist.md) in MAPI-Messaging.</span><span class="sxs-lookup"><span data-stu-id="03645-118">The **FLATMTSIDLIST** structure's use in X.400 messaging corresponds to the [FLATENTRYLIST](flatentrylist.md) structure's use in MAPI messaging.</span></span> <span data-ttu-id="03645-119">MAPI verwendet **FLATMTSIDLIST-Strukturen,** um X.400-Eigenschaften während der Nachrichtenverarbeitung zu verwalten.</span><span class="sxs-lookup"><span data-stu-id="03645-119">MAPI uses **FLATMTSIDLIST** structures to maintain X.400 properties during message handling.</span></span> <span data-ttu-id="03645-120">Dienstanbieter verwenden **FLATMTSIDLIST-Strukturen** beim Behandeln eingehender und ausgehender X.400-Nachrichten.</span><span class="sxs-lookup"><span data-stu-id="03645-120">Service providers use **FLATMTSIDLIST** structures when handling incoming and outgoing X.400 messages.</span></span> 
  
<span data-ttu-id="03645-121">Im **abMTSIDs-Array** wird jede **MTSID-Struktur** an einer natürlich ausgerichteten Grenze ausgerichtet.</span><span class="sxs-lookup"><span data-stu-id="03645-121">In the **abMTSIDs** array, each **MTSID** structure is aligned on a naturally aligned boundary.</span></span> <span data-ttu-id="03645-122">Zusätzliche Bytes sind als Abstand enthalten, um die natürliche Ausrichtung zwischen zwei **MTSID-Strukturen sicherzustellen.**</span><span class="sxs-lookup"><span data-stu-id="03645-122">Extra bytes are included as padding to make sure natural alignment between any two **MTSID** structures.</span></span> <span data-ttu-id="03645-123">Die erste **MTSID-Struktur** im Array wird immer richtig ausgerichtet, da der Offset des **abMTSIDs-Mitglieds** 8 ist.</span><span class="sxs-lookup"><span data-stu-id="03645-123">The first **MTSID** structure in the array is always aligned correctly because the offset of the **abMTSIDs** member is 8.</span></span> <span data-ttu-id="03645-124">Verwenden Sie zum Berechnen des Offsets der nächsten Struktur die Größe des ersten Eintrags, der auf das nächste Vielfache von 4 aufgerundet wurde.</span><span class="sxs-lookup"><span data-stu-id="03645-124">To compute the offset of the next structure, use the size of the first entry rounded up to the next multiple of 4.</span></span> <span data-ttu-id="03645-125">Verwenden Sie [das CbNewMTSID-Makro,](cbnewmtsid.md) um die Größe einer **MTSID-Struktur zu** berechnen.</span><span class="sxs-lookup"><span data-stu-id="03645-125">Use the [CbNewMTSID](cbnewmtsid.md) macro to compute the size of an **MTSID** structure.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="03645-126">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="03645-126">See also</span></span>



[<span data-ttu-id="03645-127">CbNewFLATMTSIDLIST</span><span class="sxs-lookup"><span data-stu-id="03645-127">CbNewFLATMTSIDLIST</span></span>](cbnewflatmtsidlist.md)
  
[<span data-ttu-id="03645-128">FLATENTRYLIST</span><span class="sxs-lookup"><span data-stu-id="03645-128">FLATENTRYLIST</span></span>](flatentrylist.md)
  
[<span data-ttu-id="03645-129">MTSID</span><span class="sxs-lookup"><span data-stu-id="03645-129">MTSID</span></span>](mtsid.md)


[<span data-ttu-id="03645-130">MAPI-Strukturen</span><span class="sxs-lookup"><span data-stu-id="03645-130">MAPI Structures</span></span>](mapi-structures.md)

