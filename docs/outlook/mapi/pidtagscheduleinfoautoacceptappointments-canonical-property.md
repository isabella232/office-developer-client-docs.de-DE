---
title: PidTagScheduleInfoAutoAcceptAppointments (kanonische Eigenschaft)
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
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 6fe724d70ac86b1c51e72f243ef9255dd452be9c
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32330093"
---
# <a name="pidtagscheduleinfoautoacceptappointments-canonical-property"></a><span data-ttu-id="7e8ef-103">PidTagScheduleInfoAutoAcceptAppointments (kanonische Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="7e8ef-103">PidTagScheduleInfoAutoAcceptAppointments Canonical Property</span></span>

  
  
<span data-ttu-id="7e8ef-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="7e8ef-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="7e8ef-105">Enthält TRUE, wenn ein Client oder Server automatisch auf alle Besprechungsanfragen für den Teilnehmer oder die Ressource reagieren soll.</span><span class="sxs-lookup"><span data-stu-id="7e8ef-105">Contains TRUE if a client or server should automatically respond to all meeting requests for the attendee or resource.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="7e8ef-106">Zugeordnete Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="7e8ef-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="7e8ef-107">PR_SCHDINFO_AUTO_ACCEPT_APPTS</span><span class="sxs-lookup"><span data-stu-id="7e8ef-107">PR_SCHDINFO_AUTO_ACCEPT_APPTS</span></span>  <br/> |
|<span data-ttu-id="7e8ef-108">Kennung:</span><span class="sxs-lookup"><span data-stu-id="7e8ef-108">Identifier:</span></span>  <br/> |<span data-ttu-id="7e8ef-109">0x686D</span><span class="sxs-lookup"><span data-stu-id="7e8ef-109">0x686D</span></span>  <br/> |
|<span data-ttu-id="7e8ef-110">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="7e8ef-110">Data type:</span></span>  <br/> |<span data-ttu-id="7e8ef-111">PT_BOOLEAN</span><span class="sxs-lookup"><span data-stu-id="7e8ef-111">PT_BOOLEAN</span></span>  <br/> |
|<span data-ttu-id="7e8ef-112">Bereich:</span><span class="sxs-lookup"><span data-stu-id="7e8ef-112">Area:</span></span>  <br/> |<span data-ttu-id="7e8ef-113">Frei/Gebucht</span><span class="sxs-lookup"><span data-stu-id="7e8ef-113">Free/Busy</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="7e8ef-114">Hinweise</span><span class="sxs-lookup"><span data-stu-id="7e8ef-114">Remarks</span></span>

<span data-ttu-id="7e8ef-115">Bei der Antwort muss die Antwort akzeptiert werden, es sei denn, für eine zusätzliche Einschränkung, die durch die **Eigenschaften PR_SCHDINFO_DISALLOW_RECURRING_APPTS** ([PidTagScheduleInfoDisallowRecurringAppts](pidtagscheduleinfodisallowrecurringappts-canonical-property.md)) oder **PR_SCHDINFO_DISALLOW_OVERLAPPING_APPTS** ([PidTagScheduleInfoDisallowOverlappingAppts](pidtagscheduleinfodisallowoverlappingappts-canonical-property.md)) angegeben wird, wird die Antwort erfüllt.</span><span class="sxs-lookup"><span data-stu-id="7e8ef-115">When responding, the response must be acceptance, unless for an additional constraint that is specified by the **PR_SCHDINFO_DISALLOW_RECURRING_APPTS** ([PidTagScheduleInfoDisallowRecurringAppts](pidtagscheduleinfodisallowrecurringappts-canonical-property.md)) or **PR_SCHDINFO_DISALLOW_OVERLAPPING_APPTS** ([PidTagScheduleInfoDisallowOverlappingAppts](pidtagscheduleinfodisallowoverlappingappts-canonical-property.md)) properties is met.</span></span> <span data-ttu-id="7e8ef-116">Der Wert FALSE oder das Fehlen dieser Eigenschaft gibt an, dass ein Client oder Server Besprechungsanfragen nicht automatisch annehmen darf.</span><span class="sxs-lookup"><span data-stu-id="7e8ef-116">A value of FALSE or the absence of this property indicates that a client or server must not automatically accept meeting requests.</span></span> <span data-ttu-id="7e8ef-117">Dies ist keine erforderliche Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="7e8ef-117">This is not a required property.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="7e8ef-118">Verwandte Ressourcen</span><span class="sxs-lookup"><span data-stu-id="7e8ef-118">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="7e8ef-119">Protokollspezifikationen</span><span class="sxs-lookup"><span data-stu-id="7e8ef-119">Protocol specifications</span></span>

<span data-ttu-id="7e8ef-120">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="7e8ef-120">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="7e8ef-121">Enthält Verweise auf Exchange Server Protokollspezifikationen.</span><span class="sxs-lookup"><span data-stu-id="7e8ef-121">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="7e8ef-122">[[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="7e8ef-122">[[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="7e8ef-123">Gibt die Eigenschaften und Vorgänge für Termin-, Besprechungs- und Antwortnachrichten an.</span><span class="sxs-lookup"><span data-stu-id="7e8ef-123">Specifies the properties and operations for appointment, meeting request, and response messages.</span></span>
    
<span data-ttu-id="7e8ef-124">[[MS-OXOPFFB]](https://msdn.microsoft.com/library/1a527299-7211-4d27-a74c-b69bd0746320%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="7e8ef-124">[[MS-OXOPFFB]](https://msdn.microsoft.com/library/1a527299-7211-4d27-a74c-b69bd0746320%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="7e8ef-125">Veröffentlicht die Verfügbarkeit eines Benutzers oder einer Ressource.</span><span class="sxs-lookup"><span data-stu-id="7e8ef-125">Publishes the availability of a user or resource.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="7e8ef-126">Headerdateien</span><span class="sxs-lookup"><span data-stu-id="7e8ef-126">Header files</span></span>

<span data-ttu-id="7e8ef-127">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="7e8ef-127">Mapidefs.h</span></span>
  
> <span data-ttu-id="7e8ef-128">Bietet Datentypdefinitionen.</span><span class="sxs-lookup"><span data-stu-id="7e8ef-128">Provides data type definitions.</span></span>
    
<span data-ttu-id="7e8ef-129">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="7e8ef-129">Mapitags.h</span></span>
  
> <span data-ttu-id="7e8ef-130">Enthält Definitionen von Eigenschaften, die als alternative Namen aufgeführt sind.</span><span class="sxs-lookup"><span data-stu-id="7e8ef-130">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="7e8ef-131">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="7e8ef-131">See also</span></span>



[<span data-ttu-id="7e8ef-132">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="7e8ef-132">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="7e8ef-133">KANONISCHE EIGENSCHAFTEN VON MAPI</span><span class="sxs-lookup"><span data-stu-id="7e8ef-133">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="7e8ef-134">Zuordnen kanonischer Eigenschaftsnamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="7e8ef-134">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="7e8ef-135">Zuordnen von MAPI-Namen zu kanonischen Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="7e8ef-135">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

