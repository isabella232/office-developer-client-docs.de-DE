---
title: PidTagScheduleInfoDisallowOverlappingAppts (kanonische Eigenschaft)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagScheduleInfoDisallowOverlappingAppts
api_type:
- COM
ms.assetid: 27978a09-daf7-4a50-927a-96d9c4a97d02
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 5ead258c056ec2204ddab92e9b99e1b17fe98092
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32330086"
---
# <a name="pidtagscheduleinfodisallowoverlappingappts-canonical-property"></a><span data-ttu-id="2de8e-103">PidTagScheduleInfoDisallowOverlappingAppts (kanonische Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="2de8e-103">PidTagScheduleInfoDisallowOverlappingAppts Canonical Property</span></span>

  
  
<span data-ttu-id="2de8e-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="2de8e-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="2de8e-105">Enthält TRUE, wenn überlappende Termine nicht zulässig sind.</span><span class="sxs-lookup"><span data-stu-id="2de8e-105">Contains TRUE if overlapping appointments are disallowed.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="2de8e-106">Zugeordnete Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="2de8e-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="2de8e-107">PR_SCHDINFO_DISALLOW_OVERLAPPING_APPTS</span><span class="sxs-lookup"><span data-stu-id="2de8e-107">PR_SCHDINFO_DISALLOW_OVERLAPPING_APPTS</span></span>  <br/> |
|<span data-ttu-id="2de8e-108">Kennung:</span><span class="sxs-lookup"><span data-stu-id="2de8e-108">Identifier:</span></span>  <br/> |<span data-ttu-id="2de8e-109">0x686F</span><span class="sxs-lookup"><span data-stu-id="2de8e-109">0x686F</span></span>  <br/> |
|<span data-ttu-id="2de8e-110">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="2de8e-110">Data type:</span></span>  <br/> |<span data-ttu-id="2de8e-111">PT_BOOLEAN</span><span class="sxs-lookup"><span data-stu-id="2de8e-111">PT_BOOLEAN</span></span>  <br/> |
|<span data-ttu-id="2de8e-112">Bereich:</span><span class="sxs-lookup"><span data-stu-id="2de8e-112">Area:</span></span>  <br/> |<span data-ttu-id="2de8e-113">Frei/Gebucht</span><span class="sxs-lookup"><span data-stu-id="2de8e-113">Free/Busy</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="2de8e-114">Hinweise</span><span class="sxs-lookup"><span data-stu-id="2de8e-114">Remarks</span></span>

<span data-ttu-id="2de8e-115">Diese Eigenschaft ist nur dann sinnvoll, wenn der Wert **der PR_SCHDINFO_AUTO_ACCEPT_APPTS** ([PidTagScheduleInfoAutoAcceptAppointments](pidtagscheduleinfoautoacceptappointments-canonical-property.md)) -Eigenschaft TRUE ist.</span><span class="sxs-lookup"><span data-stu-id="2de8e-115">This property is only meaningful when the value of the **PR_SCHDINFO_AUTO_ACCEPT_APPTS** ([PidTagScheduleInfoAutoAcceptAppointments](pidtagscheduleinfoautoacceptappointments-canonical-property.md)) property is TRUE.</span></span> <span data-ttu-id="2de8e-116">Der Wert TRUE gibt an, dass ein Client oder Server instanzen ablehnen muss, die zuvor geplante Ereignisse überlappen, wenn sie automatisch auf Besprechungsanfragen reagieren.</span><span class="sxs-lookup"><span data-stu-id="2de8e-116">A value of TRUE indicates that when automatically responding to meeting requests, a client or server must decline instances that overlap previously scheduled events.</span></span> <span data-ttu-id="2de8e-117">Der Wert FALSE oder das Fehlen dieser Eigenschaft gibt an, dass überlappende Instanzen akzeptiert werden müssen.</span><span class="sxs-lookup"><span data-stu-id="2de8e-117">A value of FALSE or the absence of this property indicates that overlapping instances must be accepted.</span></span> <span data-ttu-id="2de8e-118">Dies ist keine erforderliche Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="2de8e-118">This is not a required property.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="2de8e-119">Verwandte Ressourcen</span><span class="sxs-lookup"><span data-stu-id="2de8e-119">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="2de8e-120">Protokollspezifikationen</span><span class="sxs-lookup"><span data-stu-id="2de8e-120">Protocol specifications</span></span>

<span data-ttu-id="2de8e-121">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="2de8e-121">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="2de8e-122">Enthält Verweise auf Exchange Server Protokollspezifikationen.</span><span class="sxs-lookup"><span data-stu-id="2de8e-122">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="2de8e-123">[[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="2de8e-123">[[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="2de8e-124">Gibt die Eigenschaften und Vorgänge für Termin-, Besprechungs- und Antwortnachrichten an.</span><span class="sxs-lookup"><span data-stu-id="2de8e-124">Specifies the properties and operations for appointment, meeting request, and response messages.</span></span>
    
<span data-ttu-id="2de8e-125">[[MS-OXOPFFB]](https://msdn.microsoft.com/library/1a527299-7211-4d27-a74c-b69bd0746320%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="2de8e-125">[[MS-OXOPFFB]](https://msdn.microsoft.com/library/1a527299-7211-4d27-a74c-b69bd0746320%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="2de8e-126">Veröffentlicht die Verfügbarkeit eines Benutzers oder einer Ressource.</span><span class="sxs-lookup"><span data-stu-id="2de8e-126">Publishes the availability of a user or resource.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="2de8e-127">Headerdateien</span><span class="sxs-lookup"><span data-stu-id="2de8e-127">Header files</span></span>

<span data-ttu-id="2de8e-128">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="2de8e-128">Mapidefs.h</span></span>
  
> <span data-ttu-id="2de8e-129">Bietet Datentypdefinitionen.</span><span class="sxs-lookup"><span data-stu-id="2de8e-129">Provides data type definitions.</span></span>
    
<span data-ttu-id="2de8e-130">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="2de8e-130">Mapitags.h</span></span>
  
> <span data-ttu-id="2de8e-131">Enthält Definitionen von Eigenschaften, die als alternative Namen aufgeführt sind.</span><span class="sxs-lookup"><span data-stu-id="2de8e-131">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="2de8e-132">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="2de8e-132">See also</span></span>



[<span data-ttu-id="2de8e-133">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="2de8e-133">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="2de8e-134">KANONISCHE EIGENSCHAFTEN VON MAPI</span><span class="sxs-lookup"><span data-stu-id="2de8e-134">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="2de8e-135">Zuordnen kanonischer Eigenschaftsnamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="2de8e-135">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="2de8e-136">Zuordnen von MAPI-Namen zu kanonischen Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="2de8e-136">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

