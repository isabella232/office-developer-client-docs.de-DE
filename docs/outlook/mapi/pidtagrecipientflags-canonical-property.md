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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32356700"
---
# <a name="pidtagrecipientflags-canonical-property"></a><span data-ttu-id="f5cfa-103">PidTagRecipientFlags (kanonische Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="f5cfa-103">PidTagRecipientFlags Canonical Property</span></span>

  
  
<span data-ttu-id="f5cfa-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="f5cfa-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="f5cfa-105">Gibt ein Bitfeld an, das den Empfängerstatus beschreibt.</span><span class="sxs-lookup"><span data-stu-id="f5cfa-105">Specifies a bit field that describes the recipient status.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="f5cfa-106">Zugeordnete Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="f5cfa-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="f5cfa-107">PR_RECIPIENT_FLAGS</span><span class="sxs-lookup"><span data-stu-id="f5cfa-107">PR_RECIPIENT_FLAGS</span></span>  <br/> |
|<span data-ttu-id="f5cfa-108">Kennung:</span><span class="sxs-lookup"><span data-stu-id="f5cfa-108">Identifier:</span></span>  <br/> |<span data-ttu-id="f5cfa-109">0x5FFD</span><span class="sxs-lookup"><span data-stu-id="f5cfa-109">0x5FFD</span></span>  <br/> |
|<span data-ttu-id="f5cfa-110">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="f5cfa-110">Data type:</span></span>  <br/> |<span data-ttu-id="f5cfa-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="f5cfa-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="f5cfa-112">Bereich:</span><span class="sxs-lookup"><span data-stu-id="f5cfa-112">Area:</span></span>  <br/> |<span data-ttu-id="f5cfa-113">Transportempfänger</span><span class="sxs-lookup"><span data-stu-id="f5cfa-113">Transport recipient</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="f5cfa-114">Hinweise</span><span class="sxs-lookup"><span data-stu-id="f5cfa-114">Remarks</span></span>

<span data-ttu-id="f5cfa-115">Diese Eigenschaft ist nicht erforderlich.</span><span class="sxs-lookup"><span data-stu-id="f5cfa-115">This property is not required.</span></span> <span data-ttu-id="f5cfa-116">Im Folgenden finden Sie die einzelnen Flags, die festgelegt werden können.</span><span class="sxs-lookup"><span data-stu-id="f5cfa-116">The following are the individual flags that can be set.</span></span>
  
|<span data-ttu-id="f5cfa-117">**Wert**</span><span class="sxs-lookup"><span data-stu-id="f5cfa-117">**Value**</span></span>|<span data-ttu-id="f5cfa-118">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="f5cfa-118">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="f5cfa-119">S (recipSendable, 0x00000001)</span><span class="sxs-lookup"><span data-stu-id="f5cfa-119">S (recipSendable, 0x00000001)</span></span>  <br/> |<span data-ttu-id="f5cfa-120">Der Empfänger ist ein **sendefähiger** Teilnehmer.</span><span class="sxs-lookup"><span data-stu-id="f5cfa-120">The recipient is a **Sendable** Attendee.</span></span> <span data-ttu-id="f5cfa-121">Dieses Flag wird nur in der **eigenschaft dispidApptUnsendableRecips** ([PidLidAppointmentUnsendableRecipients](pidlidappointmentunsendablerecipients-canonical-property.md)) verwendet.</span><span class="sxs-lookup"><span data-stu-id="f5cfa-121">This flag is only used in the **dispidApptUnsendableRecips** ([PidLidAppointmentUnsendableRecipients](pidlidappointmentunsendablerecipients-canonical-property.md)) property.</span></span>  <br/> |
|<span data-ttu-id="f5cfa-122">O (recipOrganizer, 0x0000002)</span><span class="sxs-lookup"><span data-stu-id="f5cfa-122">O (recipOrganizer, 0x0000002)</span></span>  <br/> |<span data-ttu-id="f5cfa-123">Der **RecipientRow-Wert,** auf dem dieses Flag festgelegt ist, stellt den Besprechungsorganisator dar.</span><span class="sxs-lookup"><span data-stu-id="f5cfa-123">The **RecipientRow** on which this flag is set represents the meeting Organizer.</span></span>  <br/> |
|<span data-ttu-id="f5cfa-124">ER (recipExceptionalResponse, 0x00000010)</span><span class="sxs-lookup"><span data-stu-id="f5cfa-124">ER (recipExceptionalResponse, 0x00000010)</span></span>  <br/> |<span data-ttu-id="f5cfa-125">Gibt an, dass der Teilnehmer eine Antwort für die Ausnahme gegeben hat, in der sich dieses **RecipientRow** befindet.</span><span class="sxs-lookup"><span data-stu-id="f5cfa-125">Indicates that the attendee gave a response for the exception on which this **RecipientRow** resides.</span></span> <span data-ttu-id="f5cfa-126">Dieses Flag wird nur in einem **RecipientRow-Objekt eines** eingebetteten Nachrichtenobjekts der Ausnahme des Besprechungsobjekts des Organisators verwendet.</span><span class="sxs-lookup"><span data-stu-id="f5cfa-126">This flag is only used in a **RecipientRow** of an exception embedded message object of the organizer's meeting object.</span></span>  <br/> |
|<span data-ttu-id="f5cfa-127">ED (recipExceptionalDeleted, 0x00000020)</span><span class="sxs-lookup"><span data-stu-id="f5cfa-127">ED (recipExceptionalDeleted, 0x00000020)</span></span>  <br/> |<span data-ttu-id="f5cfa-128">Gibt an, dass **der RecipientRow** zwar vorhanden ist, aber so behandelt werden sollte, als ob der entsprechende Empfänger dies nicht tut.</span><span class="sxs-lookup"><span data-stu-id="f5cfa-128">Indicates that although the **RecipientRow** exists, it should be treated as if the corresponding recipient does not.</span></span> <span data-ttu-id="f5cfa-129">Dieses Flag wird nur in einem **RecipientRow-Objekt eines** eingebetteten Nachrichtenobjekts der Ausnahme des Besprechungsobjekts des Organisators verwendet.</span><span class="sxs-lookup"><span data-stu-id="f5cfa-129">This flag is only used in a **RecipientRow** of an exception embedded message object of the organizer's meeting object.</span></span>  <br/> |
|<span data-ttu-id="f5cfa-130">X (reserviert, 0x00000040)</span><span class="sxs-lookup"><span data-stu-id="f5cfa-130">X (reserved, 0x00000040)</span></span>  <br/> |<span data-ttu-id="f5cfa-131">Darf nicht festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="f5cfa-131">Must not be set.</span></span>  <br/> |
|<span data-ttu-id="f5cfa-132">X (reserviert, 0x00000080)</span><span class="sxs-lookup"><span data-stu-id="f5cfa-132">X (reserved, 0x00000080)</span></span>  <br/> |<span data-ttu-id="f5cfa-133">Darf nicht festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="f5cfa-133">Must not be set.</span></span>  <br/> |
|<span data-ttu-id="f5cfa-134">G (recipOriginal, 0x00000100)</span><span class="sxs-lookup"><span data-stu-id="f5cfa-134">G (recipOriginal, 0x00000100)</span></span>  <br/> |<span data-ttu-id="f5cfa-135">Gibt an, dass der Empfänger ein ursprünglicher Teilnehmer ist.</span><span class="sxs-lookup"><span data-stu-id="f5cfa-135">Indicates the recipient is an original attendee.</span></span> <span data-ttu-id="f5cfa-136">Dieses Flag wird nur in der **eigenschaft dispidApptUnsendableRecips** verwendet.</span><span class="sxs-lookup"><span data-stu-id="f5cfa-136">This flag is only used in the **dispidApptUnsendableRecips** property.</span></span>  <br/> |
|<span data-ttu-id="f5cfa-137">X (reserviert, 0x00000200)</span><span class="sxs-lookup"><span data-stu-id="f5cfa-137">X (reserved, 0x00000200)</span></span>  <br/> |<span data-ttu-id="f5cfa-138">Reserviert.</span><span class="sxs-lookup"><span data-stu-id="f5cfa-138">Reserved.</span></span>  <br/> |
   
## <a name="related-resources"></a><span data-ttu-id="f5cfa-139">Verwandte Ressourcen</span><span class="sxs-lookup"><span data-stu-id="f5cfa-139">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="f5cfa-140">Protokollspezifikationen</span><span class="sxs-lookup"><span data-stu-id="f5cfa-140">Protocol specifications</span></span>

<span data-ttu-id="f5cfa-141">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="f5cfa-141">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="f5cfa-142">Enthält Verweise auf Exchange Server Protokollspezifikationen.</span><span class="sxs-lookup"><span data-stu-id="f5cfa-142">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="f5cfa-143">[[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="f5cfa-143">[[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="f5cfa-144">Gibt die Eigenschaften und Vorgänge für Termin-, Besprechungs- und Antwortnachrichten an.</span><span class="sxs-lookup"><span data-stu-id="f5cfa-144">Specifies the properties and operations for appointment, meeting request, and response messages.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="f5cfa-145">Headerdateien</span><span class="sxs-lookup"><span data-stu-id="f5cfa-145">Header files</span></span>

<span data-ttu-id="f5cfa-146">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="f5cfa-146">Mapidefs.h</span></span>
  
> <span data-ttu-id="f5cfa-147">Bietet Datentypdefinitionen.</span><span class="sxs-lookup"><span data-stu-id="f5cfa-147">Provides data type definitions.</span></span>
    
<span data-ttu-id="f5cfa-148">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="f5cfa-148">Mapitags.h</span></span>
  
> <span data-ttu-id="f5cfa-149">Enthält Definitionen von Eigenschaften, die als alternative Namen aufgeführt sind.</span><span class="sxs-lookup"><span data-stu-id="f5cfa-149">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="f5cfa-150">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="f5cfa-150">See also</span></span>



[<span data-ttu-id="f5cfa-151">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="f5cfa-151">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="f5cfa-152">KANONISCHE EIGENSCHAFTEN VON MAPI</span><span class="sxs-lookup"><span data-stu-id="f5cfa-152">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="f5cfa-153">Zuordnen kanonischer Eigenschaftsnamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="f5cfa-153">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="f5cfa-154">Zuordnen von MAPI-Namen zu kanonischen Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="f5cfa-154">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

