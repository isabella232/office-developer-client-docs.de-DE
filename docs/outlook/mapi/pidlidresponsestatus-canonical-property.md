---
title: Kanonische PidLidResponseStatus-Eigenschaft
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
ms.openlocfilehash: 0bfa3a01613c49b122e92e4ac281e5b20b5f07ae
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19793762"
---
# <a name="pidlidresponsestatus-canonical-property"></a><span data-ttu-id="178ca-103">Kanonische PidLidResponseStatus-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="178ca-103">PidLidResponseStatus Canonical Property</span></span>

  
  
<span data-ttu-id="178ca-104">**Betrifft**: Outlook</span><span class="sxs-lookup"><span data-stu-id="178ca-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="178ca-105">Gibt den Antwortstatus eines Teilnehmers.</span><span class="sxs-lookup"><span data-stu-id="178ca-105">Specifies the response status of an attendee.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="178ca-106">Zugeordneten Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="178ca-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="178ca-107">dispidResponseStatus</span><span class="sxs-lookup"><span data-stu-id="178ca-107">dispidResponseStatus</span></span>  <br/> |
|<span data-ttu-id="178ca-108">-Eigenschaft festgelegt:</span><span class="sxs-lookup"><span data-stu-id="178ca-108">Property set:</span></span>  <br/> |<span data-ttu-id="178ca-109">PSETID_Appointment</span><span class="sxs-lookup"><span data-stu-id="178ca-109">PSETID_Appointment</span></span>  <br/> |
|<span data-ttu-id="178ca-110">Long-ID (Abdeckung):</span><span class="sxs-lookup"><span data-stu-id="178ca-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="178ca-111">0x00008218</span><span class="sxs-lookup"><span data-stu-id="178ca-111">0x00008218</span></span>  <br/> |
|<span data-ttu-id="178ca-112">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="178ca-112">Data type:</span></span>  <br/> |<span data-ttu-id="178ca-113">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="178ca-113">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="178ca-114">Bereich:</span><span class="sxs-lookup"><span data-stu-id="178ca-114">Area:</span></span>  <br/> |<span data-ttu-id="178ca-115">Besprechungen</span><span class="sxs-lookup"><span data-stu-id="178ca-115">Meetings</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="178ca-116">Hinweise</span><span class="sxs-lookup"><span data-stu-id="178ca-116">Remarks</span></span>

<span data-ttu-id="178ca-117">Der Antwortstatus muss einen der Werte in der folgenden Tabelle.</span><span class="sxs-lookup"><span data-stu-id="178ca-117">The response status must be one of the values in the table below.</span></span>
  
|<span data-ttu-id="178ca-118">**Antwortstatus**</span><span class="sxs-lookup"><span data-stu-id="178ca-118">**Response status**</span></span>|<span data-ttu-id="178ca-119">**Wert**</span><span class="sxs-lookup"><span data-stu-id="178ca-119">**Value**</span></span>|<span data-ttu-id="178ca-120">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="178ca-120">**Description**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="178ca-121">respNone</span><span class="sxs-lookup"><span data-stu-id="178ca-121">respNone</span></span>  <br/> |<span data-ttu-id="178ca-122">0x00000000</span><span class="sxs-lookup"><span data-stu-id="178ca-122">0x00000000</span></span>  <br/> |<span data-ttu-id="178ca-123">Keine Antwort ist erforderlich für dieses Objekt.</span><span class="sxs-lookup"><span data-stu-id="178ca-123">No response is required for this object.</span></span> <span data-ttu-id="178ca-124">Dies ist die Groß-/Kleinschreibung für Terminobjekte und Antwortobjekte meeting.</span><span class="sxs-lookup"><span data-stu-id="178ca-124">This is the case for appointment objects and meeting response objects.</span></span>  <br/> |
|<span data-ttu-id="178ca-125">respOrganized</span><span class="sxs-lookup"><span data-stu-id="178ca-125">respOrganized</span></span>  <br/> |<span data-ttu-id="178ca-126">0x00000001</span><span class="sxs-lookup"><span data-stu-id="178ca-126">0x00000001</span></span>  <br/> |<span data-ttu-id="178ca-127">Diese Besprechung gehört zu organisieren.</span><span class="sxs-lookup"><span data-stu-id="178ca-127">This meeting belongs to the organizer.</span></span>  <br/> |
|<span data-ttu-id="178ca-128">respTentative</span><span class="sxs-lookup"><span data-stu-id="178ca-128">respTentative</span></span>  <br/> |<span data-ttu-id="178ca-129">0x00000002</span><span class="sxs-lookup"><span data-stu-id="178ca-129">0x00000002</span></span>  <br/> |<span data-ttu-id="178ca-130">Dieser Wert auf den Attendee-Besprechung gibt an, dass der Teilnehmer die Besprechungsanfrage mit Vorbehalt angenommen hat.</span><span class="sxs-lookup"><span data-stu-id="178ca-130">This value on the attendee's meeting indicates that the attendee has tentatively accepted the meeting request.</span></span>  <br/> |
|<span data-ttu-id="178ca-131">respAccepted</span><span class="sxs-lookup"><span data-stu-id="178ca-131">respAccepted</span></span>  <br/> |<span data-ttu-id="178ca-132">0 x 00000003</span><span class="sxs-lookup"><span data-stu-id="178ca-132">0x00000003</span></span>  <br/> |<span data-ttu-id="178ca-133">Dieser Wert auf den Teilnehmer Besprechung t gibt an, dass der Teilnehmer die Besprechungsanfrage angenommen hat.</span><span class="sxs-lookup"><span data-stu-id="178ca-133">This value on the attendee's meeting t indicates that the attendee has accepted the meeting request.</span></span>  <br/> |
|<span data-ttu-id="178ca-134">respDeclined</span><span class="sxs-lookup"><span data-stu-id="178ca-134">respDeclined</span></span>  <br/> |<span data-ttu-id="178ca-135">0 x 00000004</span><span class="sxs-lookup"><span data-stu-id="178ca-135">0x00000004</span></span>  <br/> |<span data-ttu-id="178ca-136">Dieser Wert auf den Attendee-Besprechung gibt an, dass der Teilnehmer die Besprechungsanfrage wurde abgelehnt wurde.</span><span class="sxs-lookup"><span data-stu-id="178ca-136">This value on the attendee's meeting indicates that the attendee has declined the meeting request.</span></span>  <br/> |
|<span data-ttu-id="178ca-137">respNotResponded</span><span class="sxs-lookup"><span data-stu-id="178ca-137">respNotResponded</span></span>  <br/> |<span data-ttu-id="178ca-138">0 x 00000005</span><span class="sxs-lookup"><span data-stu-id="178ca-138">0x00000005</span></span>  <br/> |<span data-ttu-id="178ca-139">Dieser Wert auf den Attendee-Besprechung gibt an, dass der Teilnehmer noch nicht geantwortet hat.</span><span class="sxs-lookup"><span data-stu-id="178ca-139">This value on the attendee's meeting indicates the attendee has not yet responded.</span></span> <span data-ttu-id="178ca-140">Dieser Wert ist auf die Besprechungsanfrage, besprechungsaktualisierung und Besprechungsabsage.</span><span class="sxs-lookup"><span data-stu-id="178ca-140">This value is on the meeting request, meeting update, and meeting cancelation.</span></span>  <br/> |
   
## <a name="related-resources"></a><span data-ttu-id="178ca-141">Verwandte Ressourcen</span><span class="sxs-lookup"><span data-stu-id="178ca-141">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="178ca-142">Protokollspezifikationen</span><span class="sxs-lookup"><span data-stu-id="178ca-142">Protocol specifications</span></span>

<span data-ttu-id="178ca-143">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="178ca-143">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="178ca-144">Enthält Eigenschaftendefinitionen und Verweise auf Verwandte Exchange Server-Spezifikationen.</span><span class="sxs-lookup"><span data-stu-id="178ca-144">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="178ca-145">[[MS-OXOCAL]](http://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="178ca-145">[[MS-OXOCAL]](http://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="178ca-146">Gibt die Eigenschaften und Vorgänge für den Termin, einer Besprechungsanfrage und Antwortnachrichten.</span><span class="sxs-lookup"><span data-stu-id="178ca-146">Specifies the properties and operations for appointment, meeting request, and response messages.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="178ca-147">Header-Dateien</span><span class="sxs-lookup"><span data-stu-id="178ca-147">Header files</span></span>

<span data-ttu-id="178ca-148">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="178ca-148">Mapidefs.h</span></span>
  
> <span data-ttu-id="178ca-149">Enthält die Datentypdefinitionen.</span><span class="sxs-lookup"><span data-stu-id="178ca-149">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="178ca-150">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="178ca-150">See also</span></span>



[<span data-ttu-id="178ca-151">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="178ca-151">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="178ca-152">Kanonische MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="178ca-152">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="178ca-153">Zuordnen von kanonischen Eigenschaftennamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="178ca-153">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="178ca-154">Zuordnen von MAPI-Namen zu kanonische Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="178ca-154">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

