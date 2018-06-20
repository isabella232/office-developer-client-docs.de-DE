---
title: Kanonische PidTagScheduleInfoAutoAcceptAppointments-Eigenschaft
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
ms.openlocfilehash: 4f2cab31d6eed19a262bd0e667166bc79f428877
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19795071"
---
# <a name="pidtagscheduleinfoautoacceptappointments-canonical-property"></a><span data-ttu-id="b5d6b-103">Kanonische PidTagScheduleInfoAutoAcceptAppointments-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="b5d6b-103">PidTagScheduleInfoAutoAcceptAppointments Canonical Property</span></span>

  
  
<span data-ttu-id="b5d6b-104">**Betrifft**: Outlook</span><span class="sxs-lookup"><span data-stu-id="b5d6b-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="b5d6b-105">Enthält True, wenn ein Client oder Server automatisch alle Besprechungsanfragen für die Teilnehmer oder eine Ressource beantworten sollten.</span><span class="sxs-lookup"><span data-stu-id="b5d6b-105">Contains TRUE if a client or server should automatically respond to all meeting requests for the attendee or resource.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="b5d6b-106">Zugeordneten Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="b5d6b-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="b5d6b-107">PR_SCHDINFO_AUTO_ACCEPT_APPTS</span><span class="sxs-lookup"><span data-stu-id="b5d6b-107">PR_SCHDINFO_AUTO_ACCEPT_APPTS</span></span>  <br/> |
|<span data-ttu-id="b5d6b-108">Bezeichner:</span><span class="sxs-lookup"><span data-stu-id="b5d6b-108">Identifier:</span></span>  <br/> |<span data-ttu-id="b5d6b-109">0x686D</span><span class="sxs-lookup"><span data-stu-id="b5d6b-109">0x686D</span></span>  <br/> |
|<span data-ttu-id="b5d6b-110">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="b5d6b-110">Data type:</span></span>  <br/> |<span data-ttu-id="b5d6b-111">PT_BOOLEAN</span><span class="sxs-lookup"><span data-stu-id="b5d6b-111">PT_BOOLEAN</span></span>  <br/> |
|<span data-ttu-id="b5d6b-112">Bereich:</span><span class="sxs-lookup"><span data-stu-id="b5d6b-112">Area:</span></span>  <br/> |<span data-ttu-id="b5d6b-113">Frei/Gebucht-Informationen</span><span class="sxs-lookup"><span data-stu-id="b5d6b-113">Free/Busy</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="b5d6b-114">Hinweise</span><span class="sxs-lookup"><span data-stu-id="b5d6b-114">Remarks</span></span>

<span data-ttu-id="b5d6b-115">Die Antwort, muss die Antwort Annahme, wenn für eine zusätzliche Einschränkung, die durch das **PR_SCHDINFO_DISALLOW_RECURRING_APPTS** ([PidTagScheduleInfoDisallowRecurringAppts](pidtagscheduleinfodisallowrecurringappts-canonical-property.md)) oder **PR_SCHDINFO_DISALLOW_ angegeben wird OVERLAPPING_APPTS** ([PidTagScheduleInfoDisallowOverlappingAppts](pidtagscheduleinfodisallowoverlappingappts-canonical-property.md)) Eigenschaften erfüllt ist.</span><span class="sxs-lookup"><span data-stu-id="b5d6b-115">When responding, the response must be acceptance, unless for an additional constraint that is specified by the **PR_SCHDINFO_DISALLOW_RECURRING_APPTS** ([PidTagScheduleInfoDisallowRecurringAppts](pidtagscheduleinfodisallowrecurringappts-canonical-property.md)) or **PR_SCHDINFO_DISALLOW_OVERLAPPING_APPTS** ([PidTagScheduleInfoDisallowOverlappingAppts](pidtagscheduleinfodisallowoverlappingappts-canonical-property.md)) properties is met.</span></span> <span data-ttu-id="b5d6b-116">Den Wert FALSE oder Abwesenheit dieser Eigenschaft wird angegeben, dass ein Client oder Server nicht automatisch annehmen von Besprechungsanfragen muss.</span><span class="sxs-lookup"><span data-stu-id="b5d6b-116">A value of FALSE or the absence of this property indicates that a client or server must not automatically accept meeting requests.</span></span> <span data-ttu-id="b5d6b-117">Dies ist keine erforderliche Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="b5d6b-117">This is not a required property.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="b5d6b-118">Verwandte Ressourcen</span><span class="sxs-lookup"><span data-stu-id="b5d6b-118">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="b5d6b-119">Protokollspezifikationen</span><span class="sxs-lookup"><span data-stu-id="b5d6b-119">Protocol specifications</span></span>

<span data-ttu-id="b5d6b-120">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="b5d6b-120">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="b5d6b-121">Bietet Verweise auf Verwandte Exchange Server-Spezifikationen.</span><span class="sxs-lookup"><span data-stu-id="b5d6b-121">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="b5d6b-122">[[MS-OXOCAL]](http://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="b5d6b-122">[[MS-OXOCAL]](http://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="b5d6b-123">Gibt die Eigenschaften und Vorgänge für den Termin, einer Besprechungsanfrage und Antwortnachrichten.</span><span class="sxs-lookup"><span data-stu-id="b5d6b-123">Specifies the properties and operations for appointment, meeting request, and response messages.</span></span>
    
<span data-ttu-id="b5d6b-124">[[MS-OXOPFFB]](http://msdn.microsoft.com/library/1a527299-7211-4d27-a74c-b69bd0746320%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="b5d6b-124">[[MS-OXOPFFB]](http://msdn.microsoft.com/library/1a527299-7211-4d27-a74c-b69bd0746320%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="b5d6b-125">Veröffentlicht die Verfügbarkeit eines Benutzers oder einer Ressource.</span><span class="sxs-lookup"><span data-stu-id="b5d6b-125">Publishes the availability of a user or resource.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="b5d6b-126">Header-Dateien</span><span class="sxs-lookup"><span data-stu-id="b5d6b-126">Header files</span></span>

<span data-ttu-id="b5d6b-127">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="b5d6b-127">Mapidefs.h</span></span>
  
> <span data-ttu-id="b5d6b-128">Enthält die Datentypdefinitionen.</span><span class="sxs-lookup"><span data-stu-id="b5d6b-128">Provides data type definitions.</span></span>
    
<span data-ttu-id="b5d6b-129">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="b5d6b-129">Mapitags.h</span></span>
  
> <span data-ttu-id="b5d6b-130">Enthält Definitionen von Eigenschaften, die als Alternative Namen aufgelistet.</span><span class="sxs-lookup"><span data-stu-id="b5d6b-130">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="b5d6b-131">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="b5d6b-131">See also</span></span>



[<span data-ttu-id="b5d6b-132">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="b5d6b-132">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="b5d6b-133">Kanonische MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="b5d6b-133">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="b5d6b-134">Zuordnen von kanonischen Eigenschaftennamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="b5d6b-134">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="b5d6b-135">Zuordnen von MAPI-Namen zu kanonische Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="b5d6b-135">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

