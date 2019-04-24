---
title: Kanonische Pidlidresponsestatus (-Eigenschaft
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidResponseStatus
api_type:
- COM
ms.assetid: e56142fd-204b-497e-83b9-59f9acda6cb4
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: 8c8e284752c6fd47eb7a8f227e2dbfeceebea596
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32345759"
---
# <a name="pidlidresponsestatus-canonical-property"></a><span data-ttu-id="0c04e-103">Kanonische Pidlidresponsestatus (-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="0c04e-103">PidLidResponseStatus Canonical Property</span></span>

  
  
<span data-ttu-id="0c04e-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="0c04e-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="0c04e-105">Gibt den Antwortstatus eines Teilnehmers an.</span><span class="sxs-lookup"><span data-stu-id="0c04e-105">Specifies the response status of an attendee.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="0c04e-106">Zugeordnete Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="0c04e-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="0c04e-107">dispidResponseStatus</span><span class="sxs-lookup"><span data-stu-id="0c04e-107">dispidResponseStatus</span></span>  <br/> |
|<span data-ttu-id="0c04e-108">Eigenschaftensatz:</span><span class="sxs-lookup"><span data-stu-id="0c04e-108">Property set:</span></span>  <br/> |<span data-ttu-id="0c04e-109">PSETID_Appointment</span><span class="sxs-lookup"><span data-stu-id="0c04e-109">PSETID_Appointment</span></span>  <br/> |
|<span data-ttu-id="0c04e-110">Long-ID (Deckel):</span><span class="sxs-lookup"><span data-stu-id="0c04e-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="0c04e-111">0x00008218</span><span class="sxs-lookup"><span data-stu-id="0c04e-111">0x00008218</span></span>  <br/> |
|<span data-ttu-id="0c04e-112">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="0c04e-112">Data type:</span></span>  <br/> |<span data-ttu-id="0c04e-113">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="0c04e-113">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="0c04e-114">Bereich:</span><span class="sxs-lookup"><span data-stu-id="0c04e-114">Area:</span></span>  <br/> |<span data-ttu-id="0c04e-115">Meetings</span><span class="sxs-lookup"><span data-stu-id="0c04e-115">Meetings</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="0c04e-116">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="0c04e-116">Remarks</span></span>

<span data-ttu-id="0c04e-117">Der Antwortstatus muss einer der Werte in der folgenden Tabelle sein.</span><span class="sxs-lookup"><span data-stu-id="0c04e-117">The response status must be one of the values in the table below.</span></span>
  
|<span data-ttu-id="0c04e-118">**Antwortstatus**</span><span class="sxs-lookup"><span data-stu-id="0c04e-118">**Response status**</span></span>|<span data-ttu-id="0c04e-119">**Wert**</span><span class="sxs-lookup"><span data-stu-id="0c04e-119">**Value**</span></span>|<span data-ttu-id="0c04e-120">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="0c04e-120">**Description**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="0c04e-121">respNone</span><span class="sxs-lookup"><span data-stu-id="0c04e-121">respNone</span></span>  <br/> |<span data-ttu-id="0c04e-122">0x00000000</span><span class="sxs-lookup"><span data-stu-id="0c04e-122">0x00000000</span></span>  <br/> |<span data-ttu-id="0c04e-123">Für dieses Objekt ist keine Antwort erforderlich.</span><span class="sxs-lookup"><span data-stu-id="0c04e-123">No response is required for this object.</span></span> <span data-ttu-id="0c04e-124">Dies gilt für Terminobjekte und Besprechungsantwort Objekte.</span><span class="sxs-lookup"><span data-stu-id="0c04e-124">This is the case for appointment objects and meeting response objects.</span></span>  <br/> |
|<span data-ttu-id="0c04e-125">respOrganized</span><span class="sxs-lookup"><span data-stu-id="0c04e-125">respOrganized</span></span>  <br/> |<span data-ttu-id="0c04e-126">0x00000001</span><span class="sxs-lookup"><span data-stu-id="0c04e-126">0x00000001</span></span>  <br/> |<span data-ttu-id="0c04e-127">Diese Besprechung gehört zum Organisator.</span><span class="sxs-lookup"><span data-stu-id="0c04e-127">This meeting belongs to the organizer.</span></span>  <br/> |
|<span data-ttu-id="0c04e-128">respTentative</span><span class="sxs-lookup"><span data-stu-id="0c04e-128">respTentative</span></span>  <br/> |<span data-ttu-id="0c04e-129">0x00000002</span><span class="sxs-lookup"><span data-stu-id="0c04e-129">0x00000002</span></span>  <br/> |<span data-ttu-id="0c04e-130">Dieser Wert in der Besprechung des Teilnehmers gibt an, dass der Teilnehmer die Besprechungsanfrage vorläufig akzeptiert hat.</span><span class="sxs-lookup"><span data-stu-id="0c04e-130">This value on the attendee's meeting indicates that the attendee has tentatively accepted the meeting request.</span></span>  <br/> |
|<span data-ttu-id="0c04e-131">respAccepted</span><span class="sxs-lookup"><span data-stu-id="0c04e-131">respAccepted</span></span>  <br/> |<span data-ttu-id="0c04e-132">0x00000003</span><span class="sxs-lookup"><span data-stu-id="0c04e-132">0x00000003</span></span>  <br/> |<span data-ttu-id="0c04e-133">Dieser Wert in der Besprechung t des Teilnehmers gibt an, dass der Teilnehmer die Besprechungsanfrage akzeptiert hat.</span><span class="sxs-lookup"><span data-stu-id="0c04e-133">This value on the attendee's meeting t indicates that the attendee has accepted the meeting request.</span></span>  <br/> |
|<span data-ttu-id="0c04e-134">respDeclined</span><span class="sxs-lookup"><span data-stu-id="0c04e-134">respDeclined</span></span>  <br/> |<span data-ttu-id="0c04e-135">0x00000004</span><span class="sxs-lookup"><span data-stu-id="0c04e-135">0x00000004</span></span>  <br/> |<span data-ttu-id="0c04e-136">Dieser Wert in der Besprechung des Teilnehmers gibt an, dass der Teilnehmer die Besprechungsanfrage abgelehnt hat.</span><span class="sxs-lookup"><span data-stu-id="0c04e-136">This value on the attendee's meeting indicates that the attendee has declined the meeting request.</span></span>  <br/> |
|<span data-ttu-id="0c04e-137">respNotResponded</span><span class="sxs-lookup"><span data-stu-id="0c04e-137">respNotResponded</span></span>  <br/> |<span data-ttu-id="0c04e-138">0x00000005</span><span class="sxs-lookup"><span data-stu-id="0c04e-138">0x00000005</span></span>  <br/> |<span data-ttu-id="0c04e-139">Dieser Wert in der Besprechung des Teilnehmers gibt an, dass der Teilnehmer noch nicht geantwortet hat.</span><span class="sxs-lookup"><span data-stu-id="0c04e-139">This value on the attendee's meeting indicates the attendee has not yet responded.</span></span> <span data-ttu-id="0c04e-140">Dieser Wert befindet sich in der Besprechungs-, Besprechungs-und Besprechungs Abbruch.</span><span class="sxs-lookup"><span data-stu-id="0c04e-140">This value is on the meeting request, meeting update, and meeting cancelation.</span></span>  <br/> |
   
## <a name="related-resources"></a><span data-ttu-id="0c04e-141">Zugehörige Ressourcen</span><span class="sxs-lookup"><span data-stu-id="0c04e-141">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="0c04e-142">Protokollspezifikationen</span><span class="sxs-lookup"><span data-stu-id="0c04e-142">Protocol specifications</span></span>

<span data-ttu-id="0c04e-143">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="0c04e-143">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="0c04e-144">Stellt Eigenschaftensatz Definitionen und Verweise auf zugehörige Exchange Server-Protokollspezifikationen bereit.</span><span class="sxs-lookup"><span data-stu-id="0c04e-144">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="0c04e-145">[[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="0c04e-145">[[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="0c04e-146">Gibt die Eigenschaften und Vorgänge für Termin-, Besprechungs-und Antwortnachrichten an.</span><span class="sxs-lookup"><span data-stu-id="0c04e-146">Specifies the properties and operations for appointment, meeting request, and response messages.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="0c04e-147">Header Dateien</span><span class="sxs-lookup"><span data-stu-id="0c04e-147">Header files</span></span>

<span data-ttu-id="0c04e-148">Mapidefs. h</span><span class="sxs-lookup"><span data-stu-id="0c04e-148">Mapidefs.h</span></span>
  
> <span data-ttu-id="0c04e-149">Stellt Datentypdefinitionen bereit.</span><span class="sxs-lookup"><span data-stu-id="0c04e-149">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="0c04e-150">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="0c04e-150">See also</span></span>



[<span data-ttu-id="0c04e-151">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="0c04e-151">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="0c04e-152">Kanonische MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="0c04e-152">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="0c04e-153">Zuordnen von kanonischen Eigenschaftennamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="0c04e-153">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="0c04e-154">Zuordnen von MAPI-Namen zu kanonischen Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="0c04e-154">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

