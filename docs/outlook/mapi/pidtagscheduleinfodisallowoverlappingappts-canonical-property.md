---
title: Kanonische PidTagScheduleInfoDisallowOverlappingAppts-Eigenschaft
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
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: 3719c0d86b0f14324e65b963d2a81a27f6cd52ba
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19795080"
---
# <a name="pidtagscheduleinfodisallowoverlappingappts-canonical-property"></a><span data-ttu-id="875c7-103">Kanonische PidTagScheduleInfoDisallowOverlappingAppts-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="875c7-103">PidTagScheduleInfoDisallowOverlappingAppts Canonical Property</span></span>

  
  
<span data-ttu-id="875c7-104">**Betrifft**: Outlook</span><span class="sxs-lookup"><span data-stu-id="875c7-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="875c7-105">Enthält True, wenn keine überlappenden Termine zulässig sind.</span><span class="sxs-lookup"><span data-stu-id="875c7-105">Contains TRUE if overlapping appointments are disallowed.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="875c7-106">Zugeordneten Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="875c7-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="875c7-107">PR_SCHDINFO_DISALLOW_OVERLAPPING_APPTS</span><span class="sxs-lookup"><span data-stu-id="875c7-107">PR_SCHDINFO_DISALLOW_OVERLAPPING_APPTS</span></span>  <br/> |
|<span data-ttu-id="875c7-108">Bezeichner:</span><span class="sxs-lookup"><span data-stu-id="875c7-108">Identifier:</span></span>  <br/> |<span data-ttu-id="875c7-109">0x686F</span><span class="sxs-lookup"><span data-stu-id="875c7-109">0x686F</span></span>  <br/> |
|<span data-ttu-id="875c7-110">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="875c7-110">Data type:</span></span>  <br/> |<span data-ttu-id="875c7-111">PT_BOOLEAN</span><span class="sxs-lookup"><span data-stu-id="875c7-111">PT_BOOLEAN</span></span>  <br/> |
|<span data-ttu-id="875c7-112">Bereich:</span><span class="sxs-lookup"><span data-stu-id="875c7-112">Area:</span></span>  <br/> |<span data-ttu-id="875c7-113">Frei/Gebucht-Informationen</span><span class="sxs-lookup"><span data-stu-id="875c7-113">Free/Busy</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="875c7-114">Hinweise</span><span class="sxs-lookup"><span data-stu-id="875c7-114">Remarks</span></span>

<span data-ttu-id="875c7-115">Diese Eigenschaft ist nur sinnvoll, wenn der Wert der **PR_SCHDINFO_AUTO_ACCEPT_APPTS** ([PidTagScheduleInfoAutoAcceptAppointments](pidtagscheduleinfoautoacceptappointments-canonical-property.md))-Eigenschaft auf true festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="875c7-115">This property is only meaningful when the value of the **PR_SCHDINFO_AUTO_ACCEPT_APPTS** ([PidTagScheduleInfoAutoAcceptAppointments](pidtagscheduleinfoautoacceptappointments-canonical-property.md)) property is TRUE.</span></span> <span data-ttu-id="875c7-116">Der Wert gibt TRUE an, dass beim automatisch Antworten auf Besprechungsanfragen, ein Client oder Server Instanzen ablehnen muss, die zuvor geplanten Ereignisse überlappen.</span><span class="sxs-lookup"><span data-stu-id="875c7-116">A value of TRUE indicates that when automatically responding to meeting requests, a client or server must decline instances that overlap previously scheduled events.</span></span> <span data-ttu-id="875c7-117">Den Wert FALSE oder das Fehlen dieser Eigenschaft gibt an, dass überlappende Instanzen akzeptiert werden muss.</span><span class="sxs-lookup"><span data-stu-id="875c7-117">A value of FALSE or the absence of this property indicates that overlapping instances must be accepted.</span></span> <span data-ttu-id="875c7-118">Dies ist keine erforderliche Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="875c7-118">This is not a required property.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="875c7-119">Verwandte Ressourcen</span><span class="sxs-lookup"><span data-stu-id="875c7-119">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="875c7-120">Protokollspezifikationen</span><span class="sxs-lookup"><span data-stu-id="875c7-120">Protocol specifications</span></span>

<span data-ttu-id="875c7-121">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="875c7-121">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="875c7-122">Bietet Verweise auf Verwandte Exchange Server-Spezifikationen.</span><span class="sxs-lookup"><span data-stu-id="875c7-122">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="875c7-123">[[MS-OXOCAL]](http://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="875c7-123">[[MS-OXOCAL]](http://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="875c7-124">Gibt die Eigenschaften und Vorgänge für den Termin, einer Besprechungsanfrage und Antwortnachrichten.</span><span class="sxs-lookup"><span data-stu-id="875c7-124">Specifies the properties and operations for appointment, meeting request, and response messages.</span></span>
    
<span data-ttu-id="875c7-125">[[MS-OXOPFFB]](http://msdn.microsoft.com/library/1a527299-7211-4d27-a74c-b69bd0746320%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="875c7-125">[[MS-OXOPFFB]](http://msdn.microsoft.com/library/1a527299-7211-4d27-a74c-b69bd0746320%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="875c7-126">Veröffentlicht die Verfügbarkeit eines Benutzers oder einer Ressource.</span><span class="sxs-lookup"><span data-stu-id="875c7-126">Publishes the availability of a user or resource.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="875c7-127">Header-Dateien</span><span class="sxs-lookup"><span data-stu-id="875c7-127">Header files</span></span>

<span data-ttu-id="875c7-128">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="875c7-128">Mapidefs.h</span></span>
  
> <span data-ttu-id="875c7-129">Enthält die Datentypdefinitionen.</span><span class="sxs-lookup"><span data-stu-id="875c7-129">Provides data type definitions.</span></span>
    
<span data-ttu-id="875c7-130">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="875c7-130">Mapitags.h</span></span>
  
> <span data-ttu-id="875c7-131">Enthält Definitionen von Eigenschaften, die als Alternative Namen aufgelistet.</span><span class="sxs-lookup"><span data-stu-id="875c7-131">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="875c7-132">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="875c7-132">See also</span></span>



[<span data-ttu-id="875c7-133">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="875c7-133">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="875c7-134">Kanonische MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="875c7-134">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="875c7-135">Zuordnen von kanonischen Eigenschaftennamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="875c7-135">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="875c7-136">Zuordnen von MAPI-Namen zu kanonische Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="875c7-136">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

