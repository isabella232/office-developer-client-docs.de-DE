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
ms.openlocfilehash: 074bcf7c051b78bc32caf66502747e7fb1ab6b79
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32355286"
---
# <a name="pidtagrecipienttrackstatus-canonical-property"></a><span data-ttu-id="ef728-103">PidTagRecipientTrackStatus (kanonische Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="ef728-103">PidTagRecipientTrackStatus Canonical Property</span></span>

  
  
<span data-ttu-id="ef728-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="ef728-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="ef728-105">Gibt den vom Teilnehmer zurückgegebenen Antwortstatus an.</span><span class="sxs-lookup"><span data-stu-id="ef728-105">Indicates the response status returned by the attendee.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="ef728-106">Zugeordnete Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="ef728-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="ef728-107">PR_RECIPIENT_TRACKSTATUS</span><span class="sxs-lookup"><span data-stu-id="ef728-107">PR_RECIPIENT_TRACKSTATUS</span></span>  <br/> |
|<span data-ttu-id="ef728-108">Kennung:</span><span class="sxs-lookup"><span data-stu-id="ef728-108">Identifier:</span></span>  <br/> |<span data-ttu-id="ef728-109">0x5FFF</span><span class="sxs-lookup"><span data-stu-id="ef728-109">0x5FFF</span></span>  <br/> |
|<span data-ttu-id="ef728-110">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="ef728-110">Data type:</span></span>  <br/> |<span data-ttu-id="ef728-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="ef728-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="ef728-112">Bereich:</span><span class="sxs-lookup"><span data-stu-id="ef728-112">Area:</span></span>  <br/> |<span data-ttu-id="ef728-113">Transportempfänger</span><span class="sxs-lookup"><span data-stu-id="ef728-113">Transport recipient</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="ef728-114">Hinweise</span><span class="sxs-lookup"><span data-stu-id="ef728-114">Remarks</span></span>

<span data-ttu-id="ef728-115">Wenn dieser Wert nicht festgelegt ist, muss davon ausgegangen werden, dass er respNone ist.</span><span class="sxs-lookup"><span data-stu-id="ef728-115">If this value is not set, it must be assumed to be respNone.</span></span> <span data-ttu-id="ef728-116">Andernfalls muss es eine der folgenden Sein:</span><span class="sxs-lookup"><span data-stu-id="ef728-116">Otherwise, it must be one of the following:</span></span>
  
|<span data-ttu-id="ef728-117">**Antwortstatus**</span><span class="sxs-lookup"><span data-stu-id="ef728-117">**Response status**</span></span>|<span data-ttu-id="ef728-118">**Wert**</span><span class="sxs-lookup"><span data-stu-id="ef728-118">**Value**</span></span>|<span data-ttu-id="ef728-119">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="ef728-119">**Description**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="ef728-120">respNone</span><span class="sxs-lookup"><span data-stu-id="ef728-120">respNone</span></span>  <br/> |<span data-ttu-id="ef728-121">0x00000000</span><span class="sxs-lookup"><span data-stu-id="ef728-121">0x00000000</span></span>  <br/> |<span data-ttu-id="ef728-122">Für dieses Objekt ist keine Antwort erforderlich.</span><span class="sxs-lookup"><span data-stu-id="ef728-122">No response is required for this object.</span></span> <span data-ttu-id="ef728-123">Dies ist bei Terminobjekten und Besprechungsantwortobjekten der Fall.</span><span class="sxs-lookup"><span data-stu-id="ef728-123">This is the case for appointment objects and meeting response objects.</span></span>  <br/> |
|<span data-ttu-id="ef728-124">respTentative</span><span class="sxs-lookup"><span data-stu-id="ef728-124">respTentative</span></span>  <br/> |<span data-ttu-id="ef728-125">0x00000002</span><span class="sxs-lookup"><span data-stu-id="ef728-125">0x00000002</span></span>  <br/> |<span data-ttu-id="ef728-126">Dieser Wert für das Besprechungsobjekt des Teilnehmers gibt an, dass der Teilnehmer das Besprechungsanforderungsobjekt mit Zag angenommen hat.</span><span class="sxs-lookup"><span data-stu-id="ef728-126">This value on the attendee's meeting object indicates that the attendee has tentatively accepted the meeting request object.</span></span>  <br/> |
|<span data-ttu-id="ef728-127">respAccepted</span><span class="sxs-lookup"><span data-stu-id="ef728-127">respAccepted</span></span>  <br/> |<span data-ttu-id="ef728-128">0x00000003</span><span class="sxs-lookup"><span data-stu-id="ef728-128">0x00000003</span></span>  <br/> |<span data-ttu-id="ef728-129">Dieser Wert für das Besprechungsobjekt des Teilnehmers gibt an, dass der Teilnehmer das Besprechungsanforderungsobjekt akzeptiert hat.</span><span class="sxs-lookup"><span data-stu-id="ef728-129">This value on the attendee's meeting object indicates that the attendee has accepted the meeting request object.</span></span>  <br/> |
|<span data-ttu-id="ef728-130">respDeclined</span><span class="sxs-lookup"><span data-stu-id="ef728-130">respDeclined</span></span>  <br/> |<span data-ttu-id="ef728-131">0x00000004</span><span class="sxs-lookup"><span data-stu-id="ef728-131">0x00000004</span></span>  <br/> |<span data-ttu-id="ef728-132">Dieser Wert für das Besprechungsobjekt des Teilnehmers gibt an, dass der Teilnehmer das Besprechungsanforderungsobjekt abgelehnt hat.</span><span class="sxs-lookup"><span data-stu-id="ef728-132">This value on the attendee's meeting object indicates that the attendee has declined the meeting request object.</span></span>  <br/> |
   
## <a name="related-resources"></a><span data-ttu-id="ef728-133">Verwandte Ressourcen</span><span class="sxs-lookup"><span data-stu-id="ef728-133">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="ef728-134">Protokollspezifikationen</span><span class="sxs-lookup"><span data-stu-id="ef728-134">Protocol specifications</span></span>

<span data-ttu-id="ef728-135">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="ef728-135">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="ef728-136">Enthält Verweise auf Exchange Server Protokollspezifikationen.</span><span class="sxs-lookup"><span data-stu-id="ef728-136">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="ef728-137">[[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="ef728-137">[[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="ef728-138">Gibt die Eigenschaften und Vorgänge für Termin-, Besprechungs- und Antwortnachrichten an.</span><span class="sxs-lookup"><span data-stu-id="ef728-138">Specifies the properties and operations for appointment, meeting request, and response messages.</span></span>
    
<span data-ttu-id="ef728-139">[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="ef728-139">[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="ef728-140">Behandelt Nachrichten- und Anlagenobjekte.</span><span class="sxs-lookup"><span data-stu-id="ef728-140">Handles message and attachment objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="ef728-141">Headerdateien</span><span class="sxs-lookup"><span data-stu-id="ef728-141">Header files</span></span>

<span data-ttu-id="ef728-142">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="ef728-142">Mapidefs.h</span></span>
  
> <span data-ttu-id="ef728-143">Bietet Datentypdefinitionen.</span><span class="sxs-lookup"><span data-stu-id="ef728-143">Provides data type definitions.</span></span>
    
<span data-ttu-id="ef728-144">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="ef728-144">Mapitags.h</span></span>
  
> <span data-ttu-id="ef728-145">Enthält Definitionen von Eigenschaften, die als alternative Namen aufgeführt sind.</span><span class="sxs-lookup"><span data-stu-id="ef728-145">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="ef728-146">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="ef728-146">See also</span></span>



[<span data-ttu-id="ef728-147">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="ef728-147">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="ef728-148">KANONISCHE EIGENSCHAFTEN VON MAPI</span><span class="sxs-lookup"><span data-stu-id="ef728-148">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="ef728-149">Zuordnen kanonischer Eigenschaftsnamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="ef728-149">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="ef728-150">Zuordnen von MAPI-Namen zu kanonischen Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="ef728-150">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

