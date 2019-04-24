---
title: Kanonische Pidtagrecipienttrackstatus (-Eigenschaft
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
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: 074bcf7c051b78bc32caf66502747e7fb1ab6b79
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32355286"
---
# <a name="pidtagrecipienttrackstatus-canonical-property"></a><span data-ttu-id="bfc01-103">Kanonische Pidtagrecipienttrackstatus (-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="bfc01-103">PidTagRecipientTrackStatus Canonical Property</span></span>

  
  
<span data-ttu-id="bfc01-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="bfc01-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="bfc01-105">Gibt den vom Teilnehmer zurückgegebenen Antwortstatus an.</span><span class="sxs-lookup"><span data-stu-id="bfc01-105">Indicates the response status returned by the attendee.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="bfc01-106">Zugeordnete Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="bfc01-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="bfc01-107">PR_RECIPIENT_TRACKSTATUS</span><span class="sxs-lookup"><span data-stu-id="bfc01-107">PR_RECIPIENT_TRACKSTATUS</span></span>  <br/> |
|<span data-ttu-id="bfc01-108">Kennung:</span><span class="sxs-lookup"><span data-stu-id="bfc01-108">Identifier:</span></span>  <br/> |<span data-ttu-id="bfc01-109">0x5FFF</span><span class="sxs-lookup"><span data-stu-id="bfc01-109">0x5FFF</span></span>  <br/> |
|<span data-ttu-id="bfc01-110">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="bfc01-110">Data type:</span></span>  <br/> |<span data-ttu-id="bfc01-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="bfc01-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="bfc01-112">Bereich:</span><span class="sxs-lookup"><span data-stu-id="bfc01-112">Area:</span></span>  <br/> |<span data-ttu-id="bfc01-113">Transport Empfänger</span><span class="sxs-lookup"><span data-stu-id="bfc01-113">Transport recipient</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="bfc01-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="bfc01-114">Remarks</span></span>

<span data-ttu-id="bfc01-115">Wenn dieser Wert nicht festgelegt ist, muss davon ausgegangen werden, dass respNone.</span><span class="sxs-lookup"><span data-stu-id="bfc01-115">If this value is not set, it must be assumed to be respNone.</span></span> <span data-ttu-id="bfc01-116">Andernfalls muss es eine der folgenden sein:</span><span class="sxs-lookup"><span data-stu-id="bfc01-116">Otherwise, it must be one of the following:</span></span>
  
|<span data-ttu-id="bfc01-117">**Antwortstatus**</span><span class="sxs-lookup"><span data-stu-id="bfc01-117">**Response status**</span></span>|<span data-ttu-id="bfc01-118">**Wert**</span><span class="sxs-lookup"><span data-stu-id="bfc01-118">**Value**</span></span>|<span data-ttu-id="bfc01-119">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="bfc01-119">**Description**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="bfc01-120">respNone</span><span class="sxs-lookup"><span data-stu-id="bfc01-120">respNone</span></span>  <br/> |<span data-ttu-id="bfc01-121">0x00000000</span><span class="sxs-lookup"><span data-stu-id="bfc01-121">0x00000000</span></span>  <br/> |<span data-ttu-id="bfc01-122">Für dieses Objekt ist keine Antwort erforderlich.</span><span class="sxs-lookup"><span data-stu-id="bfc01-122">No response is required for this object.</span></span> <span data-ttu-id="bfc01-123">Dies gilt für Terminobjekte und Besprechungsantwort Objekte.</span><span class="sxs-lookup"><span data-stu-id="bfc01-123">This is the case for appointment objects and meeting response objects.</span></span>  <br/> |
|<span data-ttu-id="bfc01-124">respTentative</span><span class="sxs-lookup"><span data-stu-id="bfc01-124">respTentative</span></span>  <br/> |<span data-ttu-id="bfc01-125">0x00000002</span><span class="sxs-lookup"><span data-stu-id="bfc01-125">0x00000002</span></span>  <br/> |<span data-ttu-id="bfc01-126">Dieser Wert im Meeting-Objekt des Teilnehmers gibt an, dass der Teilnehmer das Besprechungsanfrage Objekt vorläufig akzeptiert hat.</span><span class="sxs-lookup"><span data-stu-id="bfc01-126">This value on the attendee's meeting object indicates that the attendee has tentatively accepted the meeting request object.</span></span>  <br/> |
|<span data-ttu-id="bfc01-127">respAccepted</span><span class="sxs-lookup"><span data-stu-id="bfc01-127">respAccepted</span></span>  <br/> |<span data-ttu-id="bfc01-128">0x00000003</span><span class="sxs-lookup"><span data-stu-id="bfc01-128">0x00000003</span></span>  <br/> |<span data-ttu-id="bfc01-129">Dieser Wert im Meeting-Objekt des Teilnehmers gibt an, dass der Teilnehmer das Besprechungsanfrage Objekt akzeptiert hat.</span><span class="sxs-lookup"><span data-stu-id="bfc01-129">This value on the attendee's meeting object indicates that the attendee has accepted the meeting request object.</span></span>  <br/> |
|<span data-ttu-id="bfc01-130">respDeclined</span><span class="sxs-lookup"><span data-stu-id="bfc01-130">respDeclined</span></span>  <br/> |<span data-ttu-id="bfc01-131">0x00000004</span><span class="sxs-lookup"><span data-stu-id="bfc01-131">0x00000004</span></span>  <br/> |<span data-ttu-id="bfc01-132">Dieser Wert im Meeting-Objekt des Teilnehmers gibt an, dass der Teilnehmer das Besprechungsanfrage Objekt abgelehnt hat.</span><span class="sxs-lookup"><span data-stu-id="bfc01-132">This value on the attendee's meeting object indicates that the attendee has declined the meeting request object.</span></span>  <br/> |
   
## <a name="related-resources"></a><span data-ttu-id="bfc01-133">Zugehörige Ressourcen</span><span class="sxs-lookup"><span data-stu-id="bfc01-133">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="bfc01-134">Protokollspezifikationen</span><span class="sxs-lookup"><span data-stu-id="bfc01-134">Protocol specifications</span></span>

<span data-ttu-id="bfc01-135">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="bfc01-135">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="bfc01-136">Enthält Verweise auf zugehörige Exchange Server-Protokollspezifikationen.</span><span class="sxs-lookup"><span data-stu-id="bfc01-136">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="bfc01-137">[[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="bfc01-137">[[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="bfc01-138">Gibt die Eigenschaften und Vorgänge für Termin-, Besprechungs-und Antwortnachrichten an.</span><span class="sxs-lookup"><span data-stu-id="bfc01-138">Specifies the properties and operations for appointment, meeting request, and response messages.</span></span>
    
<span data-ttu-id="bfc01-139">[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="bfc01-139">[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="bfc01-140">Verarbeitet Nachrichten-und Anlagenobjekte.</span><span class="sxs-lookup"><span data-stu-id="bfc01-140">Handles message and attachment objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="bfc01-141">Header Dateien</span><span class="sxs-lookup"><span data-stu-id="bfc01-141">Header files</span></span>

<span data-ttu-id="bfc01-142">Mapidefs. h</span><span class="sxs-lookup"><span data-stu-id="bfc01-142">Mapidefs.h</span></span>
  
> <span data-ttu-id="bfc01-143">Stellt Datentypdefinitionen bereit.</span><span class="sxs-lookup"><span data-stu-id="bfc01-143">Provides data type definitions.</span></span>
    
<span data-ttu-id="bfc01-144">Mapitags. h</span><span class="sxs-lookup"><span data-stu-id="bfc01-144">Mapitags.h</span></span>
  
> <span data-ttu-id="bfc01-145">Enthält Definitionen von Eigenschaften, die als Alternative Namen aufgeführt sind.</span><span class="sxs-lookup"><span data-stu-id="bfc01-145">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="bfc01-146">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="bfc01-146">See also</span></span>



[<span data-ttu-id="bfc01-147">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="bfc01-147">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="bfc01-148">Kanonische MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="bfc01-148">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="bfc01-149">Zuordnen von kanonischen Eigenschaftennamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="bfc01-149">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="bfc01-150">Zuordnen von MAPI-Namen zu kanonischen Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="bfc01-150">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

