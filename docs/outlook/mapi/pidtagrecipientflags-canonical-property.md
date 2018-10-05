---
title: PidTagRecipientFlags (kanonische Eigenschaft)
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
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 7b791d75c2a76ea1a504c0d8862dd20f5365b475
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/04/2018
ms.locfileid: "25394041"
---
# <a name="pidtagrecipientflags-canonical-property"></a><span data-ttu-id="6c960-103">PidTagRecipientFlags (kanonische Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="6c960-103">PidTagRecipientFlags Canonical Property</span></span>

  
  
<span data-ttu-id="6c960-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="6c960-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="6c960-105">Gibt ein Bitfeld, das der Empfängerstatus beschreibt.</span><span class="sxs-lookup"><span data-stu-id="6c960-105">Specifies a bit field that describes the recipient status.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="6c960-106">Zugeordnete Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="6c960-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="6c960-107">PR_RECIPIENT_FLAGS</span><span class="sxs-lookup"><span data-stu-id="6c960-107">PR_RECIPIENT_FLAGS</span></span>  <br/> |
|<span data-ttu-id="6c960-108">Kennung:</span><span class="sxs-lookup"><span data-stu-id="6c960-108">Identifier:</span></span>  <br/> |<span data-ttu-id="6c960-109">0x5FFD</span><span class="sxs-lookup"><span data-stu-id="6c960-109">0x5FFD</span></span>  <br/> |
|<span data-ttu-id="6c960-110">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="6c960-110">Data type:</span></span>  <br/> |<span data-ttu-id="6c960-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="6c960-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="6c960-112">Bereich:</span><span class="sxs-lookup"><span data-stu-id="6c960-112">Area:</span></span>  <br/> |<span data-ttu-id="6c960-113">Transport-Empfänger</span><span class="sxs-lookup"><span data-stu-id="6c960-113">Transport recipient</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="6c960-114">Hinweise</span><span class="sxs-lookup"><span data-stu-id="6c960-114">Remarks</span></span>

<span data-ttu-id="6c960-115">Diese Eigenschaft ist nicht erforderlich.</span><span class="sxs-lookup"><span data-stu-id="6c960-115">This property is not required.</span></span> <span data-ttu-id="6c960-116">Im folgenden werden die einzelnen Flags, die festgelegt werden können.</span><span class="sxs-lookup"><span data-stu-id="6c960-116">The following are the individual flags that can be set.</span></span>
  
|<span data-ttu-id="6c960-117">**Wert**</span><span class="sxs-lookup"><span data-stu-id="6c960-117">**Value**</span></span>|<span data-ttu-id="6c960-118">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="6c960-118">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="6c960-119">S (RecipSendable, 0 x 00000001)</span><span class="sxs-lookup"><span data-stu-id="6c960-119">S (recipSendable, 0x00000001)</span></span>  <br/> |<span data-ttu-id="6c960-120">Der Empfänger ist ein **Sendable** Teilnehmer.</span><span class="sxs-lookup"><span data-stu-id="6c960-120">The recipient is a **Sendable** Attendee.</span></span> <span data-ttu-id="6c960-121">Dieses Kennzeichen werden nur in der Eigenschaft **DispidApptUnsendableRecips** ([PidLidAppointmentUnsendableRecipients](pidlidappointmentunsendablerecipients-canonical-property.md)) verwendet.</span><span class="sxs-lookup"><span data-stu-id="6c960-121">This flag is only used in the **dispidApptUnsendableRecips** ([PidLidAppointmentUnsendableRecipients](pidlidappointmentunsendablerecipients-canonical-property.md)) property.</span></span>  <br/> |
|<span data-ttu-id="6c960-122">O (RecipOrganizer 0x0000002)</span><span class="sxs-lookup"><span data-stu-id="6c960-122">O (recipOrganizer, 0x0000002)</span></span>  <br/> |<span data-ttu-id="6c960-123">Die **RecipientRow** , auf denen dieses Flag festgelegt ist, stellt den Besprechungsorganisator.</span><span class="sxs-lookup"><span data-stu-id="6c960-123">The **RecipientRow** on which this flag is set represents the meeting Organizer.</span></span>  <br/> |
|<span data-ttu-id="6c960-124">ER (RecipExceptionalResponse, 0 x 00000010)</span><span class="sxs-lookup"><span data-stu-id="6c960-124">ER (recipExceptionalResponse, 0x00000010)</span></span>  <br/> |<span data-ttu-id="6c960-125">Gibt an, dass der Teilnehmer für die Ausnahme eine Antwort gesendet hat in der sich diese **RecipientRow** befindet.</span><span class="sxs-lookup"><span data-stu-id="6c960-125">Indicates that the attendee gave a response for the exception on which this **RecipientRow** resides.</span></span> <span data-ttu-id="6c960-126">Dieses Kennzeichen werden nur in einer **RecipientRow** eines Objekts eingebettete Nachricht Ausnahme vom Organisator der Besprechung-Objekts verwendet.</span><span class="sxs-lookup"><span data-stu-id="6c960-126">This flag is only used in a **RecipientRow** of an exception embedded message object of the organizer's meeting object.</span></span>  <br/> |
|<span data-ttu-id="6c960-127">ED (RecipExceptionalDeleted, 0 x 00000020)</span><span class="sxs-lookup"><span data-stu-id="6c960-127">ED (recipExceptionalDeleted, 0x00000020)</span></span>  <br/> |<span data-ttu-id="6c960-128">Gibt an, dass zwar die **RecipientRow** vorhanden ist, es behandelt werden soll, als ob der entsprechende Empfänger nicht der Fall ist.</span><span class="sxs-lookup"><span data-stu-id="6c960-128">Indicates that although the **RecipientRow** exists, it should be treated as if the corresponding recipient does not.</span></span> <span data-ttu-id="6c960-129">Dieses Kennzeichen werden nur in einer **RecipientRow** eines Objekts eingebettete Nachricht Ausnahme vom Organisator der Besprechung-Objekts verwendet.</span><span class="sxs-lookup"><span data-stu-id="6c960-129">This flag is only used in a **RecipientRow** of an exception embedded message object of the organizer's meeting object.</span></span>  <br/> |
|<span data-ttu-id="6c960-130">X (reserviert, 0 x 00000040)</span><span class="sxs-lookup"><span data-stu-id="6c960-130">X (reserved, 0x00000040)</span></span>  <br/> |<span data-ttu-id="6c960-131">Muss nicht festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="6c960-131">Must not be set.</span></span>  <br/> |
|<span data-ttu-id="6c960-132">X (reserviert, 0x00000080)</span><span class="sxs-lookup"><span data-stu-id="6c960-132">X (reserved, 0x00000080)</span></span>  <br/> |<span data-ttu-id="6c960-133">Muss nicht festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="6c960-133">Must not be set.</span></span>  <br/> |
|<span data-ttu-id="6c960-134">G (RecipOriginal, 0 x 00000100)</span><span class="sxs-lookup"><span data-stu-id="6c960-134">G (recipOriginal, 0x00000100)</span></span>  <br/> |<span data-ttu-id="6c960-135">Gibt an, dass der Empfänger ursprünglichen teilnimmt.</span><span class="sxs-lookup"><span data-stu-id="6c960-135">Indicates the recipient is an original attendee.</span></span> <span data-ttu-id="6c960-136">Dieses Kennzeichen werden nur in der **DispidApptUnsendableRecips** -Eigenschaft verwendet.</span><span class="sxs-lookup"><span data-stu-id="6c960-136">This flag is only used in the **dispidApptUnsendableRecips** property.</span></span>  <br/> |
|<span data-ttu-id="6c960-137">X (reserviert, 0 x 00000200)</span><span class="sxs-lookup"><span data-stu-id="6c960-137">X (reserved, 0x00000200)</span></span>  <br/> |<span data-ttu-id="6c960-138">Reserviert.</span><span class="sxs-lookup"><span data-stu-id="6c960-138">Reserved.</span></span>  <br/> |
   
## <a name="related-resources"></a><span data-ttu-id="6c960-139">Verwandte Ressourcen</span><span class="sxs-lookup"><span data-stu-id="6c960-139">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="6c960-140">Protokollspezifikationen</span><span class="sxs-lookup"><span data-stu-id="6c960-140">Protocol specifications</span></span>

<span data-ttu-id="6c960-141">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="6c960-141">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="6c960-142">Bietet Verweise auf Verwandte Exchange Server-Spezifikationen.</span><span class="sxs-lookup"><span data-stu-id="6c960-142">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="6c960-143">[[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="6c960-143">[[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="6c960-144">Gibt die Eigenschaften und Vorgänge für den Termin, einer Besprechungsanfrage und Antwortnachrichten.</span><span class="sxs-lookup"><span data-stu-id="6c960-144">Specifies the properties and operations for appointment, meeting request, and response messages.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="6c960-145">Header-Dateien</span><span class="sxs-lookup"><span data-stu-id="6c960-145">Header files</span></span>

<span data-ttu-id="6c960-146">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="6c960-146">Mapidefs.h</span></span>
  
> <span data-ttu-id="6c960-147">Enthält die Datentypdefinitionen.</span><span class="sxs-lookup"><span data-stu-id="6c960-147">Provides data type definitions.</span></span>
    
<span data-ttu-id="6c960-148">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="6c960-148">Mapitags.h</span></span>
  
> <span data-ttu-id="6c960-149">Enthält Definitionen von Eigenschaften, die als Alternative Namen aufgelistet.</span><span class="sxs-lookup"><span data-stu-id="6c960-149">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="6c960-150">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="6c960-150">See also</span></span>



[<span data-ttu-id="6c960-151">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="6c960-151">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="6c960-152">Kanonische MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="6c960-152">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="6c960-153">Zuordnen von kanonischen Eigenschaftennamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="6c960-153">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="6c960-154">Zuordnen von MAPI-Namen zu kanonische Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="6c960-154">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

