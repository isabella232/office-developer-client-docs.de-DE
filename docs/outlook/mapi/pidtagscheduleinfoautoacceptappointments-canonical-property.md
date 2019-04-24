---
title: Kanonische Pidtagscheduleinfoautoacceptappointments (-Eigenschaft
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagScheduleInfoAutoAcceptAppointments
api_type:
- COM
ms.assetid: 79505b29-2706-472b-b084-ab74be7b3405
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: 6fe724d70ac86b1c51e72f243ef9255dd452be9c
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32330093"
---
# <a name="pidtagscheduleinfoautoacceptappointments-canonical-property"></a><span data-ttu-id="38711-103">Kanonische Pidtagscheduleinfoautoacceptappointments (-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="38711-103">PidTagScheduleInfoAutoAcceptAppointments Canonical Property</span></span>

  
  
<span data-ttu-id="38711-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="38711-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="38711-105">Enthält TRUE, wenn ein Client oder Server automatisch auf alle Besprechungsanfragen für den Teilnehmer oder die Ressource reagieren soll.</span><span class="sxs-lookup"><span data-stu-id="38711-105">Contains TRUE if a client or server should automatically respond to all meeting requests for the attendee or resource.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="38711-106">Zugeordnete Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="38711-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="38711-107">PR_SCHDINFO_AUTO_ACCEPT_APPTS</span><span class="sxs-lookup"><span data-stu-id="38711-107">PR_SCHDINFO_AUTO_ACCEPT_APPTS</span></span>  <br/> |
|<span data-ttu-id="38711-108">Kennung:</span><span class="sxs-lookup"><span data-stu-id="38711-108">Identifier:</span></span>  <br/> |<span data-ttu-id="38711-109">0x686D</span><span class="sxs-lookup"><span data-stu-id="38711-109">0x686D</span></span>  <br/> |
|<span data-ttu-id="38711-110">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="38711-110">Data type:</span></span>  <br/> |<span data-ttu-id="38711-111">PT_BOOLEAN</span><span class="sxs-lookup"><span data-stu-id="38711-111">PT_BOOLEAN</span></span>  <br/> |
|<span data-ttu-id="38711-112">Bereich:</span><span class="sxs-lookup"><span data-stu-id="38711-112">Area:</span></span>  <br/> |<span data-ttu-id="38711-113">Frei/Gebucht</span><span class="sxs-lookup"><span data-stu-id="38711-113">Free/Busy</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="38711-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="38711-114">Remarks</span></span>

<span data-ttu-id="38711-115">Wenn Sie Antworten, muss die Antwort akzeptiert werden, es sei denn, eine zusätzliche Einschränkung, die von der **PR_SCHDINFO_DISALLOW_RECURRING_APPTS** ([Pidtagscheduleinfodisallowrecurringappts (](pidtagscheduleinfodisallowrecurringappts-canonical-property.md)) oder PR_SCHDINFO_DISALLOW_ angegeben wird \*\* OVERLAPPING_APPTS\*\* ([pidtagscheduleinfodisallowoverlappingappts (](pidtagscheduleinfodisallowoverlappingappts-canonical-property.md))-Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="38711-115">When responding, the response must be acceptance, unless for an additional constraint that is specified by the **PR_SCHDINFO_DISALLOW_RECURRING_APPTS** ([PidTagScheduleInfoDisallowRecurringAppts](pidtagscheduleinfodisallowrecurringappts-canonical-property.md)) or **PR_SCHDINFO_DISALLOW_OVERLAPPING_APPTS** ([PidTagScheduleInfoDisallowOverlappingAppts](pidtagscheduleinfodisallowoverlappingappts-canonical-property.md)) properties is met.</span></span> <span data-ttu-id="38711-116">Der Wert FALSE oder das Fehlen dieser Eigenschaft gibt an, dass ein Client oder Server nicht automatisch Besprechungsanfragen annehmen darf.</span><span class="sxs-lookup"><span data-stu-id="38711-116">A value of FALSE or the absence of this property indicates that a client or server must not automatically accept meeting requests.</span></span> <span data-ttu-id="38711-117">Dies ist keine erforderliche Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="38711-117">This is not a required property.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="38711-118">Zugehörige Ressourcen</span><span class="sxs-lookup"><span data-stu-id="38711-118">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="38711-119">Protokollspezifikationen</span><span class="sxs-lookup"><span data-stu-id="38711-119">Protocol specifications</span></span>

<span data-ttu-id="38711-120">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="38711-120">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="38711-121">Enthält Verweise auf zugehörige Exchange Server-Protokollspezifikationen.</span><span class="sxs-lookup"><span data-stu-id="38711-121">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="38711-122">[[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="38711-122">[[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="38711-123">Gibt die Eigenschaften und Vorgänge für Termin-, Besprechungs-und Antwortnachrichten an.</span><span class="sxs-lookup"><span data-stu-id="38711-123">Specifies the properties and operations for appointment, meeting request, and response messages.</span></span>
    
<span data-ttu-id="38711-124">[[MS-OXOPFFB]](https://msdn.microsoft.com/library/1a527299-7211-4d27-a74c-b69bd0746320%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="38711-124">[[MS-OXOPFFB]](https://msdn.microsoft.com/library/1a527299-7211-4d27-a74c-b69bd0746320%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="38711-125">Veröffentlicht die Verfügbarkeit eines Benutzers oder einer Ressource.</span><span class="sxs-lookup"><span data-stu-id="38711-125">Publishes the availability of a user or resource.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="38711-126">Header Dateien</span><span class="sxs-lookup"><span data-stu-id="38711-126">Header files</span></span>

<span data-ttu-id="38711-127">Mapidefs. h</span><span class="sxs-lookup"><span data-stu-id="38711-127">Mapidefs.h</span></span>
  
> <span data-ttu-id="38711-128">Stellt Datentypdefinitionen bereit.</span><span class="sxs-lookup"><span data-stu-id="38711-128">Provides data type definitions.</span></span>
    
<span data-ttu-id="38711-129">Mapitags. h</span><span class="sxs-lookup"><span data-stu-id="38711-129">Mapitags.h</span></span>
  
> <span data-ttu-id="38711-130">Enthält Definitionen von Eigenschaften, die als Alternative Namen aufgeführt sind.</span><span class="sxs-lookup"><span data-stu-id="38711-130">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="38711-131">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="38711-131">See also</span></span>



[<span data-ttu-id="38711-132">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="38711-132">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="38711-133">Kanonische MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="38711-133">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="38711-134">Zuordnen von kanonischen Eigenschaftennamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="38711-134">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="38711-135">Zuordnen von MAPI-Namen zu kanonischen Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="38711-135">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

