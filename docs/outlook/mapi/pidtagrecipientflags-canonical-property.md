---
title: Kanonische PidTagRecipientFlags-Eigenschaft
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagRecipientFlags
api_type:
- COM
ms.assetid: 9fbe537f-b5fe-48a2-803c-653c50c82efd
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: a93e5a44768cd99512189f800bf98ab6e30b575d
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19794894"
---
# <a name="pidtagrecipientflags-canonical-property"></a><span data-ttu-id="713a4-103">Kanonische PidTagRecipientFlags-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="713a4-103">PidTagRecipientFlags Canonical Property</span></span>

  
  
<span data-ttu-id="713a4-104">**Betrifft**: Outlook</span><span class="sxs-lookup"><span data-stu-id="713a4-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="713a4-105">Gibt ein Bitfeld, das der Empfängerstatus beschreibt.</span><span class="sxs-lookup"><span data-stu-id="713a4-105">Specifies a bit field that describes the recipient status.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="713a4-106">Zugeordneten Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="713a4-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="713a4-107">PR_RECIPIENT_FLAGS</span><span class="sxs-lookup"><span data-stu-id="713a4-107">PR_RECIPIENT_FLAGS</span></span>  <br/> |
|<span data-ttu-id="713a4-108">Bezeichner:</span><span class="sxs-lookup"><span data-stu-id="713a4-108">Identifier:</span></span>  <br/> |<span data-ttu-id="713a4-109">0x5FFD</span><span class="sxs-lookup"><span data-stu-id="713a4-109">0x5FFD</span></span>  <br/> |
|<span data-ttu-id="713a4-110">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="713a4-110">Data type:</span></span>  <br/> |<span data-ttu-id="713a4-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="713a4-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="713a4-112">Bereich:</span><span class="sxs-lookup"><span data-stu-id="713a4-112">Area:</span></span>  <br/> |<span data-ttu-id="713a4-113">Transport-Empfänger</span><span class="sxs-lookup"><span data-stu-id="713a4-113">Transport recipient</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="713a4-114">Hinweise</span><span class="sxs-lookup"><span data-stu-id="713a4-114">Remarks</span></span>

<span data-ttu-id="713a4-115">Diese Eigenschaft ist nicht erforderlich.</span><span class="sxs-lookup"><span data-stu-id="713a4-115">This property is not required.</span></span> <span data-ttu-id="713a4-116">Im folgenden werden die einzelnen Flags, die festgelegt werden können.</span><span class="sxs-lookup"><span data-stu-id="713a4-116">The following are the individual flags that can be set.</span></span>
  
|<span data-ttu-id="713a4-117">**Wert**</span><span class="sxs-lookup"><span data-stu-id="713a4-117">**Value**</span></span>|<span data-ttu-id="713a4-118">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="713a4-118">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="713a4-119">S (RecipSendable, 0 x 00000001)</span><span class="sxs-lookup"><span data-stu-id="713a4-119">S (recipSendable, 0x00000001)</span></span>  <br/> |<span data-ttu-id="713a4-120">Der Empfänger ist ein **Sendable** Teilnehmer.</span><span class="sxs-lookup"><span data-stu-id="713a4-120">The recipient is a **Sendable** Attendee.</span></span> <span data-ttu-id="713a4-121">Dieses Kennzeichen werden nur in der Eigenschaft **DispidApptUnsendableRecips** ([PidLidAppointmentUnsendableRecipients](pidlidappointmentunsendablerecipients-canonical-property.md)) verwendet.</span><span class="sxs-lookup"><span data-stu-id="713a4-121">This flag is only used in the **dispidApptUnsendableRecips** ([PidLidAppointmentUnsendableRecipients](pidlidappointmentunsendablerecipients-canonical-property.md)) property.</span></span>  <br/> |
|<span data-ttu-id="713a4-122">O (RecipOrganizer 0x0000002)</span><span class="sxs-lookup"><span data-stu-id="713a4-122">O (recipOrganizer, 0x0000002)</span></span>  <br/> |<span data-ttu-id="713a4-123">Die **RecipientRow** , auf denen dieses Flag festgelegt ist, stellt den Besprechungsorganisator.</span><span class="sxs-lookup"><span data-stu-id="713a4-123">The **RecipientRow** on which this flag is set represents the meeting Organizer.</span></span>  <br/> |
|<span data-ttu-id="713a4-124">ER (RecipExceptionalResponse, 0 x 00000010)</span><span class="sxs-lookup"><span data-stu-id="713a4-124">ER (recipExceptionalResponse, 0x00000010)</span></span>  <br/> |<span data-ttu-id="713a4-125">Gibt an, dass der Teilnehmer für die Ausnahme eine Antwort gesendet hat in der sich diese **RecipientRow** befindet.</span><span class="sxs-lookup"><span data-stu-id="713a4-125">Indicates that the attendee gave a response for the exception on which this **RecipientRow** resides.</span></span> <span data-ttu-id="713a4-126">Dieses Kennzeichen werden nur in einer **RecipientRow** eines Objekts eingebettete Nachricht Ausnahme vom Organisator der Besprechung-Objekts verwendet.</span><span class="sxs-lookup"><span data-stu-id="713a4-126">This flag is only used in a **RecipientRow** of an exception embedded message object of the organizer's meeting object.</span></span>  <br/> |
|<span data-ttu-id="713a4-127">ED (RecipExceptionalDeleted, 0 x 00000020)</span><span class="sxs-lookup"><span data-stu-id="713a4-127">ED (recipExceptionalDeleted, 0x00000020)</span></span>  <br/> |<span data-ttu-id="713a4-128">Gibt an, dass zwar die **RecipientRow** vorhanden ist, es behandelt werden soll, als ob der entsprechende Empfänger nicht der Fall ist.</span><span class="sxs-lookup"><span data-stu-id="713a4-128">Indicates that although the **RecipientRow** exists, it should be treated as if the corresponding recipient does not.</span></span> <span data-ttu-id="713a4-129">Dieses Kennzeichen werden nur in einer **RecipientRow** eines Objekts eingebettete Nachricht Ausnahme vom Organisator der Besprechung-Objekts verwendet.</span><span class="sxs-lookup"><span data-stu-id="713a4-129">This flag is only used in a **RecipientRow** of an exception embedded message object of the organizer's meeting object.</span></span>  <br/> |
|<span data-ttu-id="713a4-130">X (reserviert, 0 x 00000040)</span><span class="sxs-lookup"><span data-stu-id="713a4-130">X (reserved, 0x00000040)</span></span>  <br/> |<span data-ttu-id="713a4-131">Muss nicht festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="713a4-131">Must not be set.</span></span>  <br/> |
|<span data-ttu-id="713a4-132">X (reserviert, 0x00000080)</span><span class="sxs-lookup"><span data-stu-id="713a4-132">X (reserved, 0x00000080)</span></span>  <br/> |<span data-ttu-id="713a4-133">Muss nicht festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="713a4-133">Must not be set.</span></span>  <br/> |
|<span data-ttu-id="713a4-134">G (RecipOriginal, 0 x 00000100)</span><span class="sxs-lookup"><span data-stu-id="713a4-134">G (recipOriginal, 0x00000100)</span></span>  <br/> |<span data-ttu-id="713a4-135">Gibt an, dass der Empfänger ursprünglichen teilnimmt.</span><span class="sxs-lookup"><span data-stu-id="713a4-135">Indicates the recipient is an original attendee.</span></span> <span data-ttu-id="713a4-136">Dieses Kennzeichen werden nur in der **DispidApptUnsendableRecips** -Eigenschaft verwendet.</span><span class="sxs-lookup"><span data-stu-id="713a4-136">This flag is only used in the **dispidApptUnsendableRecips** property.</span></span>  <br/> |
|<span data-ttu-id="713a4-137">X (reserviert, 0 x 00000200)</span><span class="sxs-lookup"><span data-stu-id="713a4-137">X (reserved, 0x00000200)</span></span>  <br/> |<span data-ttu-id="713a4-138">Reserviert.</span><span class="sxs-lookup"><span data-stu-id="713a4-138">Reserved.</span></span>  <br/> |
   
## <a name="related-resources"></a><span data-ttu-id="713a4-139">Verwandte Ressourcen</span><span class="sxs-lookup"><span data-stu-id="713a4-139">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="713a4-140">Protokollspezifikationen</span><span class="sxs-lookup"><span data-stu-id="713a4-140">Protocol specifications</span></span>

<span data-ttu-id="713a4-141">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="713a4-141">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="713a4-142">Bietet Verweise auf Verwandte Exchange Server-Spezifikationen.</span><span class="sxs-lookup"><span data-stu-id="713a4-142">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="713a4-143">[[MS-OXOCAL]](http://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="713a4-143">[[MS-OXOCAL]](http://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="713a4-144">Gibt die Eigenschaften und Vorgänge für den Termin, einer Besprechungsanfrage und Antwortnachrichten.</span><span class="sxs-lookup"><span data-stu-id="713a4-144">Specifies the properties and operations for appointment, meeting request, and response messages.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="713a4-145">Header-Dateien</span><span class="sxs-lookup"><span data-stu-id="713a4-145">Header files</span></span>

<span data-ttu-id="713a4-146">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="713a4-146">Mapidefs.h</span></span>
  
> <span data-ttu-id="713a4-147">Enthält die Datentypdefinitionen.</span><span class="sxs-lookup"><span data-stu-id="713a4-147">Provides data type definitions.</span></span>
    
<span data-ttu-id="713a4-148">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="713a4-148">Mapitags.h</span></span>
  
> <span data-ttu-id="713a4-149">Enthält Definitionen von Eigenschaften, die als Alternative Namen aufgelistet.</span><span class="sxs-lookup"><span data-stu-id="713a4-149">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="713a4-150">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="713a4-150">See also</span></span>



[<span data-ttu-id="713a4-151">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="713a4-151">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="713a4-152">Kanonische MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="713a4-152">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="713a4-153">Zuordnen von kanonischen Eigenschaftennamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="713a4-153">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="713a4-154">Zuordnen von MAPI-Namen zu kanonische Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="713a4-154">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

