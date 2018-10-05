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
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/04/2018
ms.locfileid: "25391899"
---
# <a name="pidtagscheduleinfodisallowoverlappingappts-canonical-property"></a><span data-ttu-id="1af24-103">PidTagScheduleInfoDisallowOverlappingAppts (kanonische Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="1af24-103">PidTagScheduleInfoDisallowOverlappingAppts Canonical Property</span></span>

  
  
<span data-ttu-id="1af24-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="1af24-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="1af24-105">Enthält True, wenn keine überlappenden Termine zulässig sind.</span><span class="sxs-lookup"><span data-stu-id="1af24-105">Contains TRUE if overlapping appointments are disallowed.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="1af24-106">Zugeordnete Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="1af24-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="1af24-107">PR_SCHDINFO_DISALLOW_OVERLAPPING_APPTS</span><span class="sxs-lookup"><span data-stu-id="1af24-107">PR_SCHDINFO_DISALLOW_OVERLAPPING_APPTS</span></span>  <br/> |
|<span data-ttu-id="1af24-108">Kennung:</span><span class="sxs-lookup"><span data-stu-id="1af24-108">Identifier:</span></span>  <br/> |<span data-ttu-id="1af24-109">0x686F</span><span class="sxs-lookup"><span data-stu-id="1af24-109">0x686F</span></span>  <br/> |
|<span data-ttu-id="1af24-110">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="1af24-110">Data type:</span></span>  <br/> |<span data-ttu-id="1af24-111">PT_BOOLEAN</span><span class="sxs-lookup"><span data-stu-id="1af24-111">PT_BOOLEAN</span></span>  <br/> |
|<span data-ttu-id="1af24-112">Bereich:</span><span class="sxs-lookup"><span data-stu-id="1af24-112">Area:</span></span>  <br/> |<span data-ttu-id="1af24-113">Frei/Gebucht-Informationen</span><span class="sxs-lookup"><span data-stu-id="1af24-113">Free/Busy</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="1af24-114">Hinweise</span><span class="sxs-lookup"><span data-stu-id="1af24-114">Remarks</span></span>

<span data-ttu-id="1af24-115">Diese Eigenschaft ist nur sinnvoll, wenn der Wert der **PR_SCHDINFO_AUTO_ACCEPT_APPTS** ([PidTagScheduleInfoAutoAcceptAppointments](pidtagscheduleinfoautoacceptappointments-canonical-property.md))-Eigenschaft auf true festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="1af24-115">This property is only meaningful when the value of the **PR_SCHDINFO_AUTO_ACCEPT_APPTS** ([PidTagScheduleInfoAutoAcceptAppointments](pidtagscheduleinfoautoacceptappointments-canonical-property.md)) property is TRUE.</span></span> <span data-ttu-id="1af24-116">Der Wert gibt TRUE an, dass beim automatisch Antworten auf Besprechungsanfragen, ein Client oder Server Instanzen ablehnen muss, die zuvor geplanten Ereignisse überlappen.</span><span class="sxs-lookup"><span data-stu-id="1af24-116">A value of TRUE indicates that when automatically responding to meeting requests, a client or server must decline instances that overlap previously scheduled events.</span></span> <span data-ttu-id="1af24-117">Den Wert FALSE oder das Fehlen dieser Eigenschaft gibt an, dass überlappende Instanzen akzeptiert werden muss.</span><span class="sxs-lookup"><span data-stu-id="1af24-117">A value of FALSE or the absence of this property indicates that overlapping instances must be accepted.</span></span> <span data-ttu-id="1af24-118">Dies ist keine erforderliche Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="1af24-118">This is not a required property.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="1af24-119">Verwandte Ressourcen</span><span class="sxs-lookup"><span data-stu-id="1af24-119">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="1af24-120">Protokollspezifikationen</span><span class="sxs-lookup"><span data-stu-id="1af24-120">Protocol specifications</span></span>

<span data-ttu-id="1af24-121">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="1af24-121">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="1af24-122">Bietet Verweise auf Verwandte Exchange Server-Spezifikationen.</span><span class="sxs-lookup"><span data-stu-id="1af24-122">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="1af24-123">[[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="1af24-123">[[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="1af24-124">Gibt die Eigenschaften und Vorgänge für den Termin, einer Besprechungsanfrage und Antwortnachrichten.</span><span class="sxs-lookup"><span data-stu-id="1af24-124">Specifies the properties and operations for appointment, meeting request, and response messages.</span></span>
    
<span data-ttu-id="1af24-125">[[MS-OXOPFFB]](https://msdn.microsoft.com/library/1a527299-7211-4d27-a74c-b69bd0746320%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="1af24-125">[[MS-OXOPFFB]](https://msdn.microsoft.com/library/1a527299-7211-4d27-a74c-b69bd0746320%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="1af24-126">Veröffentlicht die Verfügbarkeit eines Benutzers oder einer Ressource.</span><span class="sxs-lookup"><span data-stu-id="1af24-126">Publishes the availability of a user or resource.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="1af24-127">Header-Dateien</span><span class="sxs-lookup"><span data-stu-id="1af24-127">Header files</span></span>

<span data-ttu-id="1af24-128">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="1af24-128">Mapidefs.h</span></span>
  
> <span data-ttu-id="1af24-129">Enthält die Datentypdefinitionen.</span><span class="sxs-lookup"><span data-stu-id="1af24-129">Provides data type definitions.</span></span>
    
<span data-ttu-id="1af24-130">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="1af24-130">Mapitags.h</span></span>
  
> <span data-ttu-id="1af24-131">Enthält Definitionen von Eigenschaften, die als Alternative Namen aufgelistet.</span><span class="sxs-lookup"><span data-stu-id="1af24-131">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="1af24-132">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="1af24-132">See also</span></span>



[<span data-ttu-id="1af24-133">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="1af24-133">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="1af24-134">Kanonische MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="1af24-134">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="1af24-135">Zuordnen von kanonischen Eigenschaftennamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="1af24-135">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="1af24-136">Zuordnen von MAPI-Namen zu kanonische Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="1af24-136">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

