---
title: Kanonische Pidtagscheduleinfofreebusytentative (-Eigenschaft
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
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: 18bc41d9038113b5b813f1cfd02d90b8e982703c
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32359774"
---
# <a name="pidtagscheduleinfofreebusytentative-canonical-property"></a><span data-ttu-id="f9c77-103">Kanonische Pidtagscheduleinfofreebusytentative (-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="f9c77-103">PidTagScheduleInfoFreeBusyTentative Canonical Property</span></span>

  
  
<span data-ttu-id="f9c77-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="f9c77-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="f9c77-105">Enthält die Zeitblöcke, für die der Frei/Gebucht-Status vorläufig ist.</span><span class="sxs-lookup"><span data-stu-id="f9c77-105">Contains the blocks of times for which the free/busy status is tentative.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="f9c77-106">Zugeordnete Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="f9c77-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="f9c77-107">PR_SCHDINFO_FREEBUSY_TENTATIVE</span><span class="sxs-lookup"><span data-stu-id="f9c77-107">PR_SCHDINFO_FREEBUSY_TENTATIVE</span></span>  <br/> |
|<span data-ttu-id="f9c77-108">Kennung:</span><span class="sxs-lookup"><span data-stu-id="f9c77-108">Identifier:</span></span>  <br/> |<span data-ttu-id="f9c77-109">0x6852</span><span class="sxs-lookup"><span data-stu-id="f9c77-109">0x6852</span></span>  <br/> |
|<span data-ttu-id="f9c77-110">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="f9c77-110">Data type:</span></span>  <br/> |<span data-ttu-id="f9c77-111">PT_MV_BINARY</span><span class="sxs-lookup"><span data-stu-id="f9c77-111">PT_MV_BINARY</span></span>  <br/> |
|<span data-ttu-id="f9c77-112">Bereich:</span><span class="sxs-lookup"><span data-stu-id="f9c77-112">Area:</span></span>  <br/> |<span data-ttu-id="f9c77-113">Frei/Gebucht</span><span class="sxs-lookup"><span data-stu-id="f9c77-113">Free/Busy</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="f9c77-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="f9c77-114">Remarks</span></span>

<span data-ttu-id="f9c77-115">Diese Eigenschaft hat so viele Werte wie die Anzahl der Werte in **PR_SCHDINFO_MONTHS_TENTATIVE** ([pidtagscheduleinfomonthstentative (](pidtagscheduleinfomonthstentative-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="f9c77-115">This property has as many values as the number of values in **PR_SCHDINFO_MONTHS_TENTATIVE** ([PidTagScheduleInfoMonthsTentative](pidtagscheduleinfomonthstentative-canonical-property.md)).</span></span> <span data-ttu-id="f9c77-116">Jeder binäre Wert stellt einen Monat dar und entspricht dem Wert am gleichen Index in **PR_SCHDINFO_MONTHS_TENTATIVE**.</span><span class="sxs-lookup"><span data-stu-id="f9c77-116">Each binary value represents a month and corresponds to the value at the same index in **PR_SCHDINFO_MONTHS_TENTATIVE**.</span></span> <span data-ttu-id="f9c77-117">Die binären Werte werden in der gleichen Reihenfolge sortiert wie die Werte in **PR_SCHDINFO_MONTHS_TENTATIVE**.</span><span class="sxs-lookup"><span data-stu-id="f9c77-117">The binary values are sorted in the same order as the values in **PR_SCHDINFO_MONTHS_TENTATIVE**.</span></span>
  
<span data-ttu-id="f9c77-118">Jeder Binärwert weist einen oder mehrere 4-BYTE-Blöcke auf, und jede dieser Elemente enthält die Startzeit in den ersten beiden Bytes und die Endzeit in den zweiten zwei Bytes im Little-Endian-Format.</span><span class="sxs-lookup"><span data-stu-id="f9c77-118">Each binary value has one or more 4-BYTE blocks and each of them contains the start time in the first two bytes and end time in the second two bytes in little-endian format.</span></span> <span data-ttu-id="f9c77-119">Die Startzeit ist die Anzahl der Minuten zwischen Mitternachts koordinierter weltZeit (UTC) vom ersten Tag des Monats und der Startzeit des Ereignisses in UTC.</span><span class="sxs-lookup"><span data-stu-id="f9c77-119">The start time is the number of minutes between midnight Coordinated Universal Time (UTC) of the first day of the month and the start time of the event in UTC.</span></span> <span data-ttu-id="f9c77-120">Die Endzeit ist die Anzahl der Minuten zwischen Mitternacht UTC des ersten Tags des Monats und der Endzeit des Ereignisses in UTC.</span><span class="sxs-lookup"><span data-stu-id="f9c77-120">The end time is the number of minutes between midnight UTC of the first day of the month and the end time of the event in UTC.</span></span> <span data-ttu-id="f9c77-121">Die 4-BYTE-Blöcke werden in aufsteigender Reihenfolge sortiert.</span><span class="sxs-lookup"><span data-stu-id="f9c77-121">The 4-BYTE blocks are sorted in ascending order.</span></span>
  
<span data-ttu-id="f9c77-122">Aufeinanderfolgende oder überlappende Zeitblöcke werden zu einem Block mit der Startzeit als Startzeit des ersten Blocks und Endzeit als Endzeit des letzten Blocks zusammengeführt.</span><span class="sxs-lookup"><span data-stu-id="f9c77-122">Consecutive or overlapping blocks of time are merged into one block with start time as the start time of the first block and end time as the end time of the last block.</span></span> <span data-ttu-id="f9c77-123">Wenn ein Ereignis über mehrere Monate oder Jahre verteilt ist, wird das Ereignis in mehrere Blöcke aufgeteilt, eine für jeden Monat.</span><span class="sxs-lookup"><span data-stu-id="f9c77-123">If an event is spread across multiple months or years, the event is split into multiple blocks, one for each month.</span></span> <span data-ttu-id="f9c77-124">Wenn im Veröffentlichungszeitraum keine zaghaften Ereignisse vorhanden sind, dürfen diese Eigenschaft und **PR_SCHDINFO_MONTHS_TENTATIVE** nicht festgelegt oder gelöscht werden, wenn Sie bereits vorhanden sind.</span><span class="sxs-lookup"><span data-stu-id="f9c77-124">If there are no tentative events in the publishing range, then this property and **PR_SCHDINFO_MONTHS_TENTATIVE** must not be set or must be deleted if they already exist.</span></span> <span data-ttu-id="f9c77-125">Andernfalls muss diese Eigenschaft festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="f9c77-125">Otherwise, this property must be set.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="f9c77-126">Zugehörige Ressourcen</span><span class="sxs-lookup"><span data-stu-id="f9c77-126">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="f9c77-127">Protokollspezifikationen</span><span class="sxs-lookup"><span data-stu-id="f9c77-127">Protocol specifications</span></span>

<span data-ttu-id="f9c77-128">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="f9c77-128">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="f9c77-129">Enthält Verweise auf zugehörige Exchange Server-Protokollspezifikationen.</span><span class="sxs-lookup"><span data-stu-id="f9c77-129">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="f9c77-130">[[MS-OXOPFFB]](https://msdn.microsoft.com/library/1a527299-7211-4d27-a74c-b69bd0746320%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="f9c77-130">[[MS-OXOPFFB]](https://msdn.microsoft.com/library/1a527299-7211-4d27-a74c-b69bd0746320%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="f9c77-131">Veröffentlicht die Verfügbarkeit eines Benutzers oder einer Ressource.</span><span class="sxs-lookup"><span data-stu-id="f9c77-131">Publishes the availability of a user or resource.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="f9c77-132">Header Dateien</span><span class="sxs-lookup"><span data-stu-id="f9c77-132">Header files</span></span>

<span data-ttu-id="f9c77-133">Mapidefs. h</span><span class="sxs-lookup"><span data-stu-id="f9c77-133">Mapidefs.h</span></span>
  
> <span data-ttu-id="f9c77-134">Stellt Datentypdefinitionen bereit.</span><span class="sxs-lookup"><span data-stu-id="f9c77-134">Provides data type definitions.</span></span>
    
<span data-ttu-id="f9c77-135">Mapitags. h</span><span class="sxs-lookup"><span data-stu-id="f9c77-135">Mapitags.h</span></span>
  
> <span data-ttu-id="f9c77-136">Enthält Definitionen von Eigenschaften, die als Alternative Namen aufgeführt sind.</span><span class="sxs-lookup"><span data-stu-id="f9c77-136">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="f9c77-137">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="f9c77-137">See also</span></span>



[<span data-ttu-id="f9c77-138">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="f9c77-138">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="f9c77-139">Kanonische MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="f9c77-139">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="f9c77-140">Zuordnen von kanonischen Eigenschaftennamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="f9c77-140">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="f9c77-141">Zuordnen von MAPI-Namen zu kanonischen Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="f9c77-141">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

