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
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/04/2018
ms.locfileid: "25391556"
---
# <a name="pidtagscheduleinfomonthstentative-canonical-property"></a><span data-ttu-id="1390a-103">PidTagScheduleInfoMonthsTentative (kanonische Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="1390a-103">PidTagScheduleInfoMonthsTentative Canonical Property</span></span>

  
  
<span data-ttu-id="1390a-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="1390a-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="1390a-105">Enthält die Monate in der Nachricht Frei/Gebucht-Informationen mit Vorbehalt markiert.</span><span class="sxs-lookup"><span data-stu-id="1390a-105">Contains the months marked tentative in the free/busy message.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="1390a-106">Zugeordnete Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="1390a-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="1390a-107">PR_SCHDINFO_MONTHS_TENTATIVE</span><span class="sxs-lookup"><span data-stu-id="1390a-107">PR_SCHDINFO_MONTHS_TENTATIVE</span></span>  <br/> |
|<span data-ttu-id="1390a-108">Kennung:</span><span class="sxs-lookup"><span data-stu-id="1390a-108">Identifier:</span></span>  <br/> |<span data-ttu-id="1390a-109">0x6851</span><span class="sxs-lookup"><span data-stu-id="1390a-109">0x6851</span></span>  <br/> |
|<span data-ttu-id="1390a-110">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="1390a-110">Data type:</span></span>  <br/> |<span data-ttu-id="1390a-111">PT_MV_LONG</span><span class="sxs-lookup"><span data-stu-id="1390a-111">PT_MV_LONG</span></span>  <br/> |
|<span data-ttu-id="1390a-112">Bereich:</span><span class="sxs-lookup"><span data-stu-id="1390a-112">Area:</span></span>  <br/> |<span data-ttu-id="1390a-113">Frei/Gebucht-Informationen</span><span class="sxs-lookup"><span data-stu-id="1390a-113">Free/Busy</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="1390a-114">Hinweise</span><span class="sxs-lookup"><span data-stu-id="1390a-114">Remarks</span></span>

<span data-ttu-id="1390a-115">Die Anzahl von Werten in dieser Eigenschaft muss zwischen 0 (null) und die Anzahl der Monate nach der Veröffentlichung der Zeitraum zwischen dem **PR_FREEBUSY_PUBLISH_START** ([PidTagFreeBusyPublishStart](pidtagfreebusypublishstart-canonical-property.md)) und \*\*PR_FREEBUSY_PUBLISH_END ist Bereich abgedeckt \*\*([PidTagFreeBusyPublishEnd](pidtagfreebusypublishend-canonical-property.md))-Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="1390a-115">The number of values in this property must be between zero and the number of months covered by the publishing range, which is the period between the **PR_FREEBUSY_PUBLISH_START** ([PidTagFreeBusyPublishStart](pidtagfreebusypublishstart-canonical-property.md)) and **PR_FREEBUSY_PUBLISH_END** ([PidTagFreeBusyPublishEnd](pidtagfreebusypublishend-canonical-property.md)) properties.</span></span>
  
<span data-ttu-id="1390a-116">Jeder Wert in dieser Eigenschaft hat einen Monat und Jahr, die in dem er codiert.</span><span class="sxs-lookup"><span data-stu-id="1390a-116">Each value in this property, has a month and year encoded in it.</span></span> <span data-ttu-id="1390a-117">Dies wird mithilfe des Ausdrucks "Jahr × 16 + Monat", in dem Jahr und Monat der gregorianische Kalender basieren auf berechnet.</span><span class="sxs-lookup"><span data-stu-id="1390a-117">This is calculated by using the expression "year × 16 + month" where year and month are based on the Gregorian calendar.</span></span> <span data-ttu-id="1390a-118">Die Werte in aufsteigender Reihenfolge sortiert sind und in little-Endian-Format codiert werden.</span><span class="sxs-lookup"><span data-stu-id="1390a-118">The values are sorted in ascending order and are encoded in little-endian format.</span></span> <span data-ttu-id="1390a-119">Wenn ein Ereignis über mehrere Monate oder Jahre mehrere verteilt ist, muss ein Wert für die Monate, die in der Veröffentlichung Bereich fallen vorhanden sein.</span><span class="sxs-lookup"><span data-stu-id="1390a-119">If an event is spread across multiple months, or multiple years, there must be one value for each of the months that fall in the publishing range.</span></span> <span data-ttu-id="1390a-120">Wenn keine mit Vorbehalt Ereignisse in der Veröffentlichung Bereich vorhanden sind, hat diese Eigenschaft und die **PR_SCHDINFO_FREEBUSY_TENTATIVE** ([PidTagScheduleInfoFreeBusyTentative](pidtagscheduleinfofreebusytentative-canonical-property.md)) muss nicht festgelegt werden oder gelöscht werden müssen, wenn sie bereits vorhanden.</span><span class="sxs-lookup"><span data-stu-id="1390a-120">If there are no tentative events in the publishing range, then this property and **PR_SCHDINFO_FREEBUSY_TENTATIVE** ([PidTagScheduleInfoFreeBusyTentative](pidtagscheduleinfofreebusytentative-canonical-property.md)) must not be set or must be deleted if they already exist.</span></span> <span data-ttu-id="1390a-121">Andernfalls muss diese Eigenschaft festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="1390a-121">Otherwise, this property must be set.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="1390a-122">Verwandte Ressourcen</span><span class="sxs-lookup"><span data-stu-id="1390a-122">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="1390a-123">Protokollspezifikationen</span><span class="sxs-lookup"><span data-stu-id="1390a-123">Protocol specifications</span></span>

<span data-ttu-id="1390a-124">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="1390a-124">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="1390a-125">Bietet Verweise auf Verwandte Exchange Server-Spezifikationen.</span><span class="sxs-lookup"><span data-stu-id="1390a-125">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="1390a-126">[[MS-OXOPFFB]](https://msdn.microsoft.com/library/1a527299-7211-4d27-a74c-b69bd0746320%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="1390a-126">[[MS-OXOPFFB]](https://msdn.microsoft.com/library/1a527299-7211-4d27-a74c-b69bd0746320%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="1390a-127">Veröffentlicht die Verfügbarkeit eines Benutzers oder einer Ressource.</span><span class="sxs-lookup"><span data-stu-id="1390a-127">Publishes the availability of a user or resource.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="1390a-128">Header-Dateien</span><span class="sxs-lookup"><span data-stu-id="1390a-128">Header files</span></span>

<span data-ttu-id="1390a-129">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="1390a-129">Mapidefs.h</span></span>
  
> <span data-ttu-id="1390a-130">Enthält die Datentypdefinitionen.</span><span class="sxs-lookup"><span data-stu-id="1390a-130">Provides data type definitions.</span></span>
    
<span data-ttu-id="1390a-131">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="1390a-131">Mapitags.h</span></span>
  
> <span data-ttu-id="1390a-132">Enthält Definitionen von Eigenschaften, die als Alternative Namen aufgelistet.</span><span class="sxs-lookup"><span data-stu-id="1390a-132">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="1390a-133">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="1390a-133">See also</span></span>



[<span data-ttu-id="1390a-134">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="1390a-134">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="1390a-135">Kanonische MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="1390a-135">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="1390a-136">Zuordnen von kanonischen Eigenschaftennamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="1390a-136">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="1390a-137">Zuordnen von MAPI-Namen zu kanonische Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="1390a-137">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

