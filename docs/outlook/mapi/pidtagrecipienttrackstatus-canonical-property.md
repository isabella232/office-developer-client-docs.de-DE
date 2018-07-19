---
title: PidTagRecipientTrackStatus (kanonische Eigenschaft)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagRecipientTrackStatus
api_type:
- COM
ms.assetid: d619b5e7-2867-44fc-9b42-123bb1bf7bde
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: cbc934eec5331a0302ba222108ee92a0dc696b1f
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19794930"
---
# <a name="pidtagrecipienttrackstatus-canonical-property"></a><span data-ttu-id="802a5-103">PidTagRecipientTrackStatus (kanonische Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="802a5-103">PidTagRecipientTrackStatus Canonical Property</span></span>

  
  
<span data-ttu-id="802a5-104">**Betrifft**: Outlook</span><span class="sxs-lookup"><span data-stu-id="802a5-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="802a5-105">Gibt den Status der Antwort vom Teilnehmer zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="802a5-105">Indicates the response status returned by the attendee.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="802a5-106">Zugeordneten Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="802a5-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="802a5-107">PR_RECIPIENT_TRACKSTATUS</span><span class="sxs-lookup"><span data-stu-id="802a5-107">PR_RECIPIENT_TRACKSTATUS</span></span>  <br/> |
|<span data-ttu-id="802a5-108">Bezeichner:</span><span class="sxs-lookup"><span data-stu-id="802a5-108">Identifier:</span></span>  <br/> |<span data-ttu-id="802a5-109">0x5FFF</span><span class="sxs-lookup"><span data-stu-id="802a5-109">0x5FFF</span></span>  <br/> |
|<span data-ttu-id="802a5-110">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="802a5-110">Data type:</span></span>  <br/> |<span data-ttu-id="802a5-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="802a5-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="802a5-112">Bereich:</span><span class="sxs-lookup"><span data-stu-id="802a5-112">Area:</span></span>  <br/> |<span data-ttu-id="802a5-113">Transport-Empfänger</span><span class="sxs-lookup"><span data-stu-id="802a5-113">Transport recipient</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="802a5-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="802a5-114">Remarks</span></span>

<span data-ttu-id="802a5-115">Wenn dieser Wert nicht festgelegt ist, muss angenommen werden RespNone werden.</span><span class="sxs-lookup"><span data-stu-id="802a5-115">If this value is not set, it must be assumed to be respNone.</span></span> <span data-ttu-id="802a5-116">Anderenfalls müssen sie eine der folgenden sein:</span><span class="sxs-lookup"><span data-stu-id="802a5-116">Otherwise, it must be one of the following:</span></span>
  
|<span data-ttu-id="802a5-117">**Antwortstatus**</span><span class="sxs-lookup"><span data-stu-id="802a5-117">**Response status**</span></span>|<span data-ttu-id="802a5-118">**Wert**</span><span class="sxs-lookup"><span data-stu-id="802a5-118">**Value**</span></span>|<span data-ttu-id="802a5-119">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="802a5-119">**Description**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="802a5-120">respNone</span><span class="sxs-lookup"><span data-stu-id="802a5-120">respNone</span></span>  <br/> |<span data-ttu-id="802a5-121">0x00000000</span><span class="sxs-lookup"><span data-stu-id="802a5-121">0x00000000</span></span>  <br/> |<span data-ttu-id="802a5-122">Keine Antwort ist erforderlich für dieses Objekt.</span><span class="sxs-lookup"><span data-stu-id="802a5-122">No response is required for this object.</span></span> <span data-ttu-id="802a5-123">Dies ist die Groß-/Kleinschreibung für Terminobjekte und Antwortobjekte meeting.</span><span class="sxs-lookup"><span data-stu-id="802a5-123">This is the case for appointment objects and meeting response objects.</span></span>  <br/> |
|<span data-ttu-id="802a5-124">respTentative</span><span class="sxs-lookup"><span data-stu-id="802a5-124">respTentative</span></span>  <br/> |<span data-ttu-id="802a5-125">0x00000002</span><span class="sxs-lookup"><span data-stu-id="802a5-125">0x00000002</span></span>  <br/> |<span data-ttu-id="802a5-126">Dieser Wert auf den Teilnehmer Besprechung-Objekt gibt an, dass der Teilnehmer die Besprechung mit Vorbehalt angenommen hat Request-Objekt.</span><span class="sxs-lookup"><span data-stu-id="802a5-126">This value on the attendee's meeting object indicates that the attendee has tentatively accepted the meeting request object.</span></span>  <br/> |
|<span data-ttu-id="802a5-127">respAccepted</span><span class="sxs-lookup"><span data-stu-id="802a5-127">respAccepted</span></span>  <br/> |<span data-ttu-id="802a5-128">0 x 00000003</span><span class="sxs-lookup"><span data-stu-id="802a5-128">0x00000003</span></span>  <br/> |<span data-ttu-id="802a5-129">Dieser Wert auf den Teilnehmer Besprechung-Objekt gibt an, dass der Teilnehmer die Besprechung angenommen hat Request-Objekt.</span><span class="sxs-lookup"><span data-stu-id="802a5-129">This value on the attendee's meeting object indicates that the attendee has accepted the meeting request object.</span></span>  <br/> |
|<span data-ttu-id="802a5-130">respDeclined</span><span class="sxs-lookup"><span data-stu-id="802a5-130">respDeclined</span></span>  <br/> |<span data-ttu-id="802a5-131">0 x 00000004</span><span class="sxs-lookup"><span data-stu-id="802a5-131">0x00000004</span></span>  <br/> |<span data-ttu-id="802a5-132">Dieser Wert auf den Teilnehmer Besprechung-Objekt gibt an, dass der Teilnehmer die Besprechung abgelehnt wurde Request-Objekt.</span><span class="sxs-lookup"><span data-stu-id="802a5-132">This value on the attendee's meeting object indicates that the attendee has declined the meeting request object.</span></span>  <br/> |
   
## <a name="related-resources"></a><span data-ttu-id="802a5-133">Verwandte Ressourcen</span><span class="sxs-lookup"><span data-stu-id="802a5-133">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="802a5-134">Protokollspezifikationen</span><span class="sxs-lookup"><span data-stu-id="802a5-134">Protocol specifications</span></span>

<span data-ttu-id="802a5-135">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="802a5-135">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="802a5-136">Bietet Verweise auf Verwandte Exchange Server-Spezifikationen.</span><span class="sxs-lookup"><span data-stu-id="802a5-136">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="802a5-137">[[MS-OXOCAL]](http://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="802a5-137">[[MS-OXOCAL]](http://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="802a5-138">Gibt die Eigenschaften und Vorgänge für den Termin, einer Besprechungsanfrage und Antwortnachrichten.</span><span class="sxs-lookup"><span data-stu-id="802a5-138">Specifies the properties and operations for appointment, meeting request, and response messages.</span></span>
    
<span data-ttu-id="802a5-139">[[MS-OXCMSG]](http://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="802a5-139">[[MS-OXCMSG]](http://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="802a5-140">Nachrichten und Anlagen Objekte behandelt.</span><span class="sxs-lookup"><span data-stu-id="802a5-140">Handles message and attachment objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="802a5-141">Header-Dateien</span><span class="sxs-lookup"><span data-stu-id="802a5-141">Header files</span></span>

<span data-ttu-id="802a5-142">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="802a5-142">Mapidefs.h</span></span>
  
> <span data-ttu-id="802a5-143">Enthält die Datentypdefinitionen.</span><span class="sxs-lookup"><span data-stu-id="802a5-143">Provides data type definitions.</span></span>
    
<span data-ttu-id="802a5-144">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="802a5-144">Mapitags.h</span></span>
  
> <span data-ttu-id="802a5-145">Enthält Definitionen von Eigenschaften, die als Alternative Namen aufgelistet.</span><span class="sxs-lookup"><span data-stu-id="802a5-145">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="802a5-146">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="802a5-146">See also</span></span>



[<span data-ttu-id="802a5-147">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="802a5-147">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="802a5-148">Kanonische MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="802a5-148">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="802a5-149">Zuordnen von kanonischen Eigenschaftennamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="802a5-149">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="802a5-150">Zuordnen von MAPI-Namen zu kanonische Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="802a5-150">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

