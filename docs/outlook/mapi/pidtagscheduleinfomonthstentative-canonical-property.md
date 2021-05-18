---
title: PidTagScheduleInfoMonthsTentative (kanonische Eigenschaft)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagScheduleInfoMonthsTentative
api_type:
- COM
ms.assetid: 3179442c-6499-464a-93af-eb0a7a5b0d30
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 6fa0579dcd98a0d819e58e62d8a42cb2972a9d1e
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32359759"
---
# <a name="pidtagscheduleinfomonthstentative-canonical-property"></a><span data-ttu-id="de9a2-103">PidTagScheduleInfoMonthsTentative (kanonische Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="de9a2-103">PidTagScheduleInfoMonthsTentative Canonical Property</span></span>

  
  
<span data-ttu-id="de9a2-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="de9a2-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="de9a2-105">Enthält die Monate, die in der Frei/Gebucht-Nachricht mit Zag markiert sind.</span><span class="sxs-lookup"><span data-stu-id="de9a2-105">Contains the months marked tentative in the free/busy message.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="de9a2-106">Zugeordnete Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="de9a2-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="de9a2-107">PR_SCHDINFO_MONTHS_TENTATIVE</span><span class="sxs-lookup"><span data-stu-id="de9a2-107">PR_SCHDINFO_MONTHS_TENTATIVE</span></span>  <br/> |
|<span data-ttu-id="de9a2-108">Kennung:</span><span class="sxs-lookup"><span data-stu-id="de9a2-108">Identifier:</span></span>  <br/> |<span data-ttu-id="de9a2-109">0x6851</span><span class="sxs-lookup"><span data-stu-id="de9a2-109">0x6851</span></span>  <br/> |
|<span data-ttu-id="de9a2-110">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="de9a2-110">Data type:</span></span>  <br/> |<span data-ttu-id="de9a2-111">PT_MV_LONG</span><span class="sxs-lookup"><span data-stu-id="de9a2-111">PT_MV_LONG</span></span>  <br/> |
|<span data-ttu-id="de9a2-112">Bereich:</span><span class="sxs-lookup"><span data-stu-id="de9a2-112">Area:</span></span>  <br/> |<span data-ttu-id="de9a2-113">Frei/Gebucht</span><span class="sxs-lookup"><span data-stu-id="de9a2-113">Free/Busy</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="de9a2-114">Hinweise</span><span class="sxs-lookup"><span data-stu-id="de9a2-114">Remarks</span></span>

<span data-ttu-id="de9a2-115">Die Anzahl der Werte in dieser Eigenschaft muss zwischen Null und der Anzahl der Monate liegen, die vom Veröffentlichungsbereich abgedeckt werden. Dabei handelt es sich um den Zeitraum zwischen den **Eigenschaften PR_FREEBUSY_PUBLISH_START** ([PidTagFreeBusyPublishStart](pidtagfreebusypublishstart-canonical-property.md)) und **PR_FREEBUSY_PUBLISH_END** ([PidTagFreeBusyPublishEnd](pidtagfreebusypublishend-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="de9a2-115">The number of values in this property must be between zero and the number of months covered by the publishing range, which is the period between the **PR_FREEBUSY_PUBLISH_START** ([PidTagFreeBusyPublishStart](pidtagfreebusypublishstart-canonical-property.md)) and **PR_FREEBUSY_PUBLISH_END** ([PidTagFreeBusyPublishEnd](pidtagfreebusypublishend-canonical-property.md)) properties.</span></span>
  
<span data-ttu-id="de9a2-116">Jeder Wert in dieser Eigenschaft verfügt über einen Monat und ein Jahr, die codiert sind.</span><span class="sxs-lookup"><span data-stu-id="de9a2-116">Each value in this property, has a month and year encoded in it.</span></span> <span data-ttu-id="de9a2-117">Dies wird mithilfe des Ausdrucks "Jahr × 16 + Monat" berechnet, wobei Jahr und Monat auf dem gregorianischen Kalender basieren.</span><span class="sxs-lookup"><span data-stu-id="de9a2-117">This is calculated by using the expression "year × 16 + month" where year and month are based on the Gregorian calendar.</span></span> <span data-ttu-id="de9a2-118">Die Werte werden in aufsteigender Reihenfolge sortiert und im Little-Endian-Format codiert.</span><span class="sxs-lookup"><span data-stu-id="de9a2-118">The values are sorted in ascending order and are encoded in little-endian format.</span></span> <span data-ttu-id="de9a2-119">Wenn ein Ereignis über mehrere Monate oder mehrere Jahre verteilt ist, muss für jeden der Monate, die in den Veröffentlichungsbereich fallen, ein Wert verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="de9a2-119">If an event is spread across multiple months, or multiple years, there must be one value for each of the months that fall in the publishing range.</span></span> <span data-ttu-id="de9a2-120">Wenn im Veröffentlichungsbereich keine zaghaften Ereignisse vorhanden sind, dürfen diese Eigenschaft und **PR_SCHDINFO_FREEBUSY_TENTATIVE** ([PidTagScheduleInfoFreeBusyTentative](pidtagscheduleinfofreebusytentative-canonical-property.md)) nicht festgelegt oder gelöscht werden, wenn sie bereits vorhanden sind.</span><span class="sxs-lookup"><span data-stu-id="de9a2-120">If there are no tentative events in the publishing range, then this property and **PR_SCHDINFO_FREEBUSY_TENTATIVE** ([PidTagScheduleInfoFreeBusyTentative](pidtagscheduleinfofreebusytentative-canonical-property.md)) must not be set or must be deleted if they already exist.</span></span> <span data-ttu-id="de9a2-121">Andernfalls muss diese Eigenschaft festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="de9a2-121">Otherwise, this property must be set.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="de9a2-122">Verwandte Ressourcen</span><span class="sxs-lookup"><span data-stu-id="de9a2-122">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="de9a2-123">Protokollspezifikationen</span><span class="sxs-lookup"><span data-stu-id="de9a2-123">Protocol specifications</span></span>

<span data-ttu-id="de9a2-124">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="de9a2-124">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="de9a2-125">Enthält Verweise auf Exchange Server Protokollspezifikationen.</span><span class="sxs-lookup"><span data-stu-id="de9a2-125">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="de9a2-126">[[MS-OXOPFFB]](https://msdn.microsoft.com/library/1a527299-7211-4d27-a74c-b69bd0746320%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="de9a2-126">[[MS-OXOPFFB]](https://msdn.microsoft.com/library/1a527299-7211-4d27-a74c-b69bd0746320%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="de9a2-127">Veröffentlicht die Verfügbarkeit eines Benutzers oder einer Ressource.</span><span class="sxs-lookup"><span data-stu-id="de9a2-127">Publishes the availability of a user or resource.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="de9a2-128">Headerdateien</span><span class="sxs-lookup"><span data-stu-id="de9a2-128">Header files</span></span>

<span data-ttu-id="de9a2-129">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="de9a2-129">Mapidefs.h</span></span>
  
> <span data-ttu-id="de9a2-130">Bietet Datentypdefinitionen.</span><span class="sxs-lookup"><span data-stu-id="de9a2-130">Provides data type definitions.</span></span>
    
<span data-ttu-id="de9a2-131">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="de9a2-131">Mapitags.h</span></span>
  
> <span data-ttu-id="de9a2-132">Enthält Definitionen von Eigenschaften, die als alternative Namen aufgeführt sind.</span><span class="sxs-lookup"><span data-stu-id="de9a2-132">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="de9a2-133">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="de9a2-133">See also</span></span>



[<span data-ttu-id="de9a2-134">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="de9a2-134">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="de9a2-135">KANONISCHE EIGENSCHAFTEN VON MAPI</span><span class="sxs-lookup"><span data-stu-id="de9a2-135">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="de9a2-136">Zuordnen kanonischer Eigenschaftsnamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="de9a2-136">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="de9a2-137">Zuordnen von MAPI-Namen zu kanonischen Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="de9a2-137">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

