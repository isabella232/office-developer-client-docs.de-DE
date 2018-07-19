---
title: PidTagScheduleInfoFreeBusyTentative (kanonische Eigenschaft)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagScheduleInfoFreeBusyTentative
api_type:
- COM
ms.assetid: 28453d29-30c5-405b-84d2-5bb5f281756c
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: a00505b765abdcb7b8fe9d68052774b30bbdf692
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19795103"
---
# <a name="pidtagscheduleinfofreebusytentative-canonical-property"></a><span data-ttu-id="dc75d-103">PidTagScheduleInfoFreeBusyTentative (kanonische Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="dc75d-103">PidTagScheduleInfoFreeBusyTentative Canonical Property</span></span>

  
  
<span data-ttu-id="dc75d-104">**Betrifft**: Outlook</span><span class="sxs-lookup"><span data-stu-id="dc75d-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="dc75d-105">Enthält die Blöcke von Zeiten für die der Frei/Gebucht-Status mit Vorbehalt ist.</span><span class="sxs-lookup"><span data-stu-id="dc75d-105">Contains the blocks of times for which the free/busy status is tentative.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="dc75d-106">Zugeordneten Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="dc75d-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="dc75d-107">PR_SCHDINFO_FREEBUSY_TENTATIVE</span><span class="sxs-lookup"><span data-stu-id="dc75d-107">PR_SCHDINFO_FREEBUSY_TENTATIVE</span></span>  <br/> |
|<span data-ttu-id="dc75d-108">Bezeichner:</span><span class="sxs-lookup"><span data-stu-id="dc75d-108">Identifier:</span></span>  <br/> |<span data-ttu-id="dc75d-109">0x6852</span><span class="sxs-lookup"><span data-stu-id="dc75d-109">0x6852</span></span>  <br/> |
|<span data-ttu-id="dc75d-110">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="dc75d-110">Data type:</span></span>  <br/> |<span data-ttu-id="dc75d-111">PT_MV_BINARY</span><span class="sxs-lookup"><span data-stu-id="dc75d-111">PT_MV_BINARY</span></span>  <br/> |
|<span data-ttu-id="dc75d-112">Bereich:</span><span class="sxs-lookup"><span data-stu-id="dc75d-112">Area:</span></span>  <br/> |<span data-ttu-id="dc75d-113">Frei/Gebucht-Informationen</span><span class="sxs-lookup"><span data-stu-id="dc75d-113">Free/Busy</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="dc75d-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="dc75d-114">Remarks</span></span>

<span data-ttu-id="dc75d-115">Diese Eigenschaft hat viele Werte als die Anzahl von Werten in **PR_SCHDINFO_MONTHS_TENTATIVE** ([PidTagScheduleInfoMonthsTentative](pidtagscheduleinfomonthstentative-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="dc75d-115">This property has as many values as the number of values in **PR_SCHDINFO_MONTHS_TENTATIVE** ([PidTagScheduleInfoMonthsTentative](pidtagscheduleinfomonthstentative-canonical-property.md)).</span></span> <span data-ttu-id="dc75d-116">Jede Binärwert stellt einen Monat und entspricht dem Wert der selben Index **PR_SCHDINFO_MONTHS_TENTATIVE**.</span><span class="sxs-lookup"><span data-stu-id="dc75d-116">Each binary value represents a month and corresponds to the value at the same index in **PR_SCHDINFO_MONTHS_TENTATIVE**.</span></span> <span data-ttu-id="dc75d-117">Die binäre Werte werden in der gleichen Reihenfolge wie die Werte in **PR_SCHDINFO_MONTHS_TENTATIVE**sortiert.</span><span class="sxs-lookup"><span data-stu-id="dc75d-117">The binary values are sorted in the same order as the values in **PR_SCHDINFO_MONTHS_TENTATIVE**.</span></span>
  
<span data-ttu-id="dc75d-118">Jede Binärwert hat mindestens 4-BYTE-Blöcken und einzelnen Elementen durch die Start- und Endzeit in der zweiten zwei Bytes in little-Endian-Format in den ersten beiden Bytes enthält.</span><span class="sxs-lookup"><span data-stu-id="dc75d-118">Each binary value has one or more 4-BYTE blocks and each of them contains the start time in the first two bytes and end time in the second two bytes in little-endian format.</span></span> <span data-ttu-id="dc75d-119">Die Anfangszeit ist die Anzahl der Minuten zwischen Mitternacht koordinierte Weltzeit (UTC), der den ersten Tag des Monats und die Startzeit des Ereignisses in UTC.</span><span class="sxs-lookup"><span data-stu-id="dc75d-119">The start time is the number of minutes between midnight Coordinated Universal Time (UTC) of the first day of the month and the start time of the event in UTC.</span></span> <span data-ttu-id="dc75d-120">Die Endzeit ist die Anzahl der Minuten zwischen den ersten Tag des Monats Mitternacht UTC und Zeit für das Ende des Ereignisses in UTC.</span><span class="sxs-lookup"><span data-stu-id="dc75d-120">The end time is the number of minutes between midnight UTC of the first day of the month and the end time of the event in UTC.</span></span> <span data-ttu-id="dc75d-121">Die 4-BYTE-Blöcken werden in aufsteigender Reihenfolge sortiert.</span><span class="sxs-lookup"><span data-stu-id="dc75d-121">The 4-BYTE blocks are sorted in ascending order.</span></span>
  
<span data-ttu-id="dc75d-122">Ein Block mit Startzeit als die Anfangszeit des ersten Blocks und Endzeit als Zeit für das Ende des letzten Blocks werden aufeinander folgende oder überlappende Blöcke Zeitraum zusammengeführt.</span><span class="sxs-lookup"><span data-stu-id="dc75d-122">Consecutive or overlapping blocks of time are merged into one block with start time as the start time of the first block and end time as the end time of the last block.</span></span> <span data-ttu-id="dc75d-123">Wenn ein Ereignis über mehrere Monate oder Jahre verteilt ist, wird das Ereignis in mehrere Blöcke, eine pro Monat geteilt.</span><span class="sxs-lookup"><span data-stu-id="dc75d-123">If an event is spread across multiple months or years, the event is split into multiple blocks, one for each month.</span></span> <span data-ttu-id="dc75d-124">Wenn keine mit Vorbehalt Ereignisse in der Veröffentlichung Bereich vorhanden sind, hat diese Eigenschaft und die **PR_SCHDINFO_MONTHS_TENTATIVE** muss nicht festgelegt werden oder gelöscht werden müssen, wenn sie bereits vorhanden.</span><span class="sxs-lookup"><span data-stu-id="dc75d-124">If there are no tentative events in the publishing range, then this property and **PR_SCHDINFO_MONTHS_TENTATIVE** must not be set or must be deleted if they already exist.</span></span> <span data-ttu-id="dc75d-125">Andernfalls muss diese Eigenschaft festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="dc75d-125">Otherwise, this property must be set.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="dc75d-126">Verwandte Ressourcen</span><span class="sxs-lookup"><span data-stu-id="dc75d-126">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="dc75d-127">Protokollspezifikationen</span><span class="sxs-lookup"><span data-stu-id="dc75d-127">Protocol specifications</span></span>

<span data-ttu-id="dc75d-128">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="dc75d-128">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="dc75d-129">Bietet Verweise auf Verwandte Exchange Server-Spezifikationen.</span><span class="sxs-lookup"><span data-stu-id="dc75d-129">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="dc75d-130">[[MS-OXOPFFB]](http://msdn.microsoft.com/library/1a527299-7211-4d27-a74c-b69bd0746320%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="dc75d-130">[[MS-OXOPFFB]](http://msdn.microsoft.com/library/1a527299-7211-4d27-a74c-b69bd0746320%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="dc75d-131">Veröffentlicht die Verfügbarkeit eines Benutzers oder einer Ressource.</span><span class="sxs-lookup"><span data-stu-id="dc75d-131">Publishes the availability of a user or resource.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="dc75d-132">Header-Dateien</span><span class="sxs-lookup"><span data-stu-id="dc75d-132">Header files</span></span>

<span data-ttu-id="dc75d-133">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="dc75d-133">Mapidefs.h</span></span>
  
> <span data-ttu-id="dc75d-134">Enthält die Datentypdefinitionen.</span><span class="sxs-lookup"><span data-stu-id="dc75d-134">Provides data type definitions.</span></span>
    
<span data-ttu-id="dc75d-135">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="dc75d-135">Mapitags.h</span></span>
  
> <span data-ttu-id="dc75d-136">Enthält Definitionen von Eigenschaften, die als Alternative Namen aufgelistet.</span><span class="sxs-lookup"><span data-stu-id="dc75d-136">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="dc75d-137">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="dc75d-137">See also</span></span>



[<span data-ttu-id="dc75d-138">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="dc75d-138">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="dc75d-139">Kanonische MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="dc75d-139">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="dc75d-140">Zuordnen von kanonischen Eigenschaftennamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="dc75d-140">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="dc75d-141">Zuordnen von MAPI-Namen zu kanonische Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="dc75d-141">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

