---
title: PidTagRecipientType (kanonische Eigenschaft)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagRecipientType
api_type:
- COM
ms.assetid: 67e31027-6bc2-4a40-9b00-d61baef4ab0f
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: 0218ff558e9dfca2f73bbad2dc42cdb7bd7121fc
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19794940"
---
# <a name="pidtagrecipienttype-canonical-property"></a><span data-ttu-id="34de7-103">PidTagRecipientType (kanonische Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="34de7-103">PidTagRecipientType Canonical Property</span></span>

  
  
<span data-ttu-id="34de7-104">**Betrifft**: Outlook</span><span class="sxs-lookup"><span data-stu-id="34de7-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="34de7-105">Enthält den Empfängertyp für einen Nachrichtenempfänger.</span><span class="sxs-lookup"><span data-stu-id="34de7-105">Contains the recipient type for a message recipient.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="34de7-106">Zugeordneten Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="34de7-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="34de7-107">PR_RECIPIENT_TYPE</span><span class="sxs-lookup"><span data-stu-id="34de7-107">PR_RECIPIENT_TYPE</span></span>  <br/> |
|<span data-ttu-id="34de7-108">Bezeichner:</span><span class="sxs-lookup"><span data-stu-id="34de7-108">Identifier:</span></span>  <br/> |<span data-ttu-id="34de7-109">0x0C15</span><span class="sxs-lookup"><span data-stu-id="34de7-109">0x0C15</span></span>  <br/> |
|<span data-ttu-id="34de7-110">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="34de7-110">Data type:</span></span>  <br/> |<span data-ttu-id="34de7-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="34de7-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="34de7-112">Bereich:</span><span class="sxs-lookup"><span data-stu-id="34de7-112">Area:</span></span>  <br/> |<span data-ttu-id="34de7-113">MAPI-Empfänger</span><span class="sxs-lookup"><span data-stu-id="34de7-113">MAPI recipient</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="34de7-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="34de7-114">Remarks</span></span>

<span data-ttu-id="34de7-115">Der in dieser Eigenschaft enthaltenen Empfängertyp besteht aus ein erforderlicher Wert und eine optionale Kennzeichnung.</span><span class="sxs-lookup"><span data-stu-id="34de7-115">The recipient type contained in this property consists of one required value and one optional flag.</span></span>
  
<span data-ttu-id="34de7-116">Diese Eigenschaft muss genau einen der folgenden Werte enthalten:</span><span class="sxs-lookup"><span data-stu-id="34de7-116">This property must contain exactly one of the following values:</span></span>
  
<span data-ttu-id="34de7-117">MAPI_TO</span><span class="sxs-lookup"><span data-stu-id="34de7-117">MAPI_TO</span></span> 
  
> <span data-ttu-id="34de7-118">Der Empfänger ist ein primärer (Empfänger To).</span><span class="sxs-lookup"><span data-stu-id="34de7-118">The recipient is a primary (To) recipient.</span></span> <span data-ttu-id="34de7-119">Clients sind erforderlich, um die primären Empfänger zu behandeln.</span><span class="sxs-lookup"><span data-stu-id="34de7-119">Clients are required to handle primary recipients.</span></span> <span data-ttu-id="34de7-120">Alle anderen Typen sind optional.</span><span class="sxs-lookup"><span data-stu-id="34de7-120">All other types are optional.</span></span>
    
<span data-ttu-id="34de7-121">MAPI_CC</span><span class="sxs-lookup"><span data-stu-id="34de7-121">MAPI_CC</span></span> 
  
> <span data-ttu-id="34de7-122">Beim Empfänger handelt es sich um einen Empfänger Carbon Copy, Kopie (CC), einen Empfänger an, die zusätzlich zu den primären Empfänger eine Nachricht empfängt.</span><span class="sxs-lookup"><span data-stu-id="34de7-122">The recipient is a carbon copy (CC) recipient, a recipient that receives a message in addition to the primary recipients.</span></span>
    
<span data-ttu-id="34de7-123">MAPI_BCC</span><span class="sxs-lookup"><span data-stu-id="34de7-123">MAPI_BCC</span></span> 
  
> <span data-ttu-id="34de7-124">Beim Empfänger handelt es sich um einen Empfänger blind Carbon Copy, Blindkopie (BCC).</span><span class="sxs-lookup"><span data-stu-id="34de7-124">The recipient is a blind carbon copy (BCC) recipient.</span></span> <span data-ttu-id="34de7-125">Primäre und Carbon Copy, Blindkopie Empfänger ist wissen das Vorhandensein der BCC-Empfänger.</span><span class="sxs-lookup"><span data-stu-id="34de7-125">Primary and carbon copy recipients are unaware of the existence of BCC recipients.</span></span> 
    
<span data-ttu-id="34de7-126">MAPI_P1</span><span class="sxs-lookup"><span data-stu-id="34de7-126">MAPI_P1</span></span> 
  
> <span data-ttu-id="34de7-127">Der Empfänger nicht die Meldung auf vorherigen Versuch erhalten.</span><span class="sxs-lookup"><span data-stu-id="34de7-127">The recipient did not successfully receive the message on the previous attempt.</span></span> <span data-ttu-id="34de7-128">Hierbei handelt es sich um eine erneute Senden eines eine frühere Übertragung.</span><span class="sxs-lookup"><span data-stu-id="34de7-128">This is a resend of an earlier transmission.</span></span>
    
<span data-ttu-id="34de7-129">Darüber hinaus können die folgenden Kennzeichen festgelegt werden:</span><span class="sxs-lookup"><span data-stu-id="34de7-129">In addition, the following flag can be set:</span></span>
  
<span data-ttu-id="34de7-130">MAPI_SUBMITTED</span><span class="sxs-lookup"><span data-stu-id="34de7-130">MAPI_SUBMITTED</span></span> 
  
> <span data-ttu-id="34de7-131">Der Empfänger die Nachricht wurde bereits empfangen und muss nicht erneut empfangen.</span><span class="sxs-lookup"><span data-stu-id="34de7-131">The recipient has already received the message and does not need to receive it again.</span></span> <span data-ttu-id="34de7-132">Hierbei handelt es sich um eine erneute Senden eines eine frühere Übertragung.</span><span class="sxs-lookup"><span data-stu-id="34de7-132">This is a resend of an earlier transmission.</span></span> <span data-ttu-id="34de7-133">Dieses Kennzeichen werden in Verbindung mit den Werten **MAPI_TO**, **MAPI_CC**und **MAPI_BCC** festgelegt.</span><span class="sxs-lookup"><span data-stu-id="34de7-133">This flag is set in conjunction with the **MAPI_TO**, **MAPI_CC**, and **MAPI_BCC** values.</span></span> 
    
<span data-ttu-id="34de7-134">Der Wert MAPI_P1 und das Flag **MAPI_SUBMITTED** werden verwendet, wenn eine Nachricht aufgrund von Nondelivery an einen oder mehrere der angegebenen Empfänger erneut übertragen wird.</span><span class="sxs-lookup"><span data-stu-id="34de7-134">The MAPI_P1 value and the **MAPI_SUBMITTED** flag are used when a message is being retransmitted due to nondelivery to one or more of the intended recipients.</span></span> <span data-ttu-id="34de7-135">Für diese erneute Übertragung wird der Client **MAPI_SUBMITTED** auf jeden Empfänger, die in der Empfängerliste angezeigt werden sollen, benötigen die Nachricht nicht erneut.</span><span class="sxs-lookup"><span data-stu-id="34de7-135">For this retransmission, the client sets **MAPI_SUBMITTED** on every recipient that does not need the message again but should be displayed in the recipient list.</span></span> <span data-ttu-id="34de7-136">Für jeden Empfänger, die nicht zuvor die Nachricht erhalten haben, wird der Client behält den ursprünglichen Empfänger mit seinem **PR_RECIPIENT_TYPE** Wert unverändert aber darüber sendet eine Kopie des Empfängers mit MAPI_P1 anstelle der ursprüngliche Wert.</span><span class="sxs-lookup"><span data-stu-id="34de7-136">For every recipient that did not receive the message previously, the client retains the original recipient with its **PR_RECIPIENT_TYPE** value unchanged, but additionally submits a copy of the recipient with MAPI_P1 in place of the original value.</span></span> <span data-ttu-id="34de7-137">Diese Kopie, die vor der Zustellung tatsächlichen gelöscht wird, erzwingt, dass den Empfänger in den Umschlag P1 und garantiert physischen erneute Übertragung an diesen Empfänger.</span><span class="sxs-lookup"><span data-stu-id="34de7-137">This copy, which is discarded before actual delivery, forces the recipient into the P1 envelope and guarantees physical retransmission to that recipient.</span></span> <span data-ttu-id="34de7-138">Die **PR_RESPONSIBILITY** ([PidTagResponsibility](pidtagresponsibility-canonical-property.md))-Eigenschaft ist für MAPI_P1 Empfänger auf FALSE festgelegt.</span><span class="sxs-lookup"><span data-stu-id="34de7-138">The **PR_RESPONSIBILITY** ([PidTagResponsibility](pidtagresponsibility-canonical-property.md)) property is set to FALSE for MAPI_P1 recipients.</span></span>
  
<span data-ttu-id="34de7-139">Wenn ein Client ein Formular erneut angezeigt wird, werden nur die MAPI_P1 Empfänger angezeigt.</span><span class="sxs-lookup"><span data-stu-id="34de7-139">When a client displays a resend form, only the MAPI_P1 recipients are visible.</span></span> <span data-ttu-id="34de7-140">Wenn der Benutzer weitere Empfänger eingibt, wenn die Nachricht gesendet wird, wird die Empfängerliste angezeigt, genau wie beim zum ersten Mal die Nachricht gesendet wurde.</span><span class="sxs-lookup"><span data-stu-id="34de7-140">Unless the user enters additional recipients, when the message is delivered, the recipient list appears exactly as it did when the message was sent for the first time.</span></span> 
  
<span data-ttu-id="34de7-141">Die **PR_DISPLAY_TO** ([PidTagDisplayTo](pidtagdisplayto-canonical-property.md)) sowie die **PR_DISPLAY_CC** ([PidTagDisplayCc](pidtagdisplaycc-canonical-property.md)) und **PR_DISPLAY_BCC** ([PidTagDisplayBcc](pidtagdisplaybcc-canonical-property.md)) Eigenschaften sind Empfängertyp relevant.</span><span class="sxs-lookup"><span data-stu-id="34de7-141">The **PR_DISPLAY_TO** ([PidTagDisplayTo](pidtagdisplayto-canonical-property.md)), **PR_DISPLAY_CC** ([PidTagDisplayCc](pidtagdisplaycc-canonical-property.md)) and **PR_DISPLAY_BCC** ([PidTagDisplayBcc](pidtagdisplaybcc-canonical-property.md)) properties are related to recipient type.</span></span> <span data-ttu-id="34de7-142">Wenn ein Client eine Nachricht **IMAPIProp::SaveChanges ruft** und mindestens einen Empfänger in der Empfängerliste ist, legt der Nachricht Informationsdienst diese Eigenschaften wie folgt fest:</span><span class="sxs-lookup"><span data-stu-id="34de7-142">When a client calls a message's **IMAPIProp::SaveChanges** and there is at least one recipient in the recipient list, the message store provider sets these properties as follows:</span></span> 
  
|<span data-ttu-id="34de7-143">**Eigenschaft**</span><span class="sxs-lookup"><span data-stu-id="34de7-143">**Property**</span></span>|<span data-ttu-id="34de7-144">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="34de7-144">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="34de7-145">PR_DISPLAY_TO</span><span class="sxs-lookup"><span data-stu-id="34de7-145">PR_DISPLAY_TO</span></span>  <br/> |<span data-ttu-id="34de7-146">Auf TRUE festgelegt, wenn ein oder mehrere Empfänger **MAPI_TO** Empfänger sind.</span><span class="sxs-lookup"><span data-stu-id="34de7-146">Set to TRUE if one or more of the recipients are **MAPI_TO** recipients.</span></span>  <br/> |
|<span data-ttu-id="34de7-147">PR_DISPLAY_CC</span><span class="sxs-lookup"><span data-stu-id="34de7-147">PR_DISPLAY_CC</span></span>  <br/> |<span data-ttu-id="34de7-148">Auf TRUE festgelegt, wenn ein oder mehrere Empfänger **MAPI_CC** Empfänger sind.</span><span class="sxs-lookup"><span data-stu-id="34de7-148">Set to TRUE if one or more of the recipients are **MAPI_CC** recipients.</span></span>  <br/> |
| <span data-ttu-id="34de7-149">PR_DISPLAY_BCC</span><span class="sxs-lookup"><span data-stu-id="34de7-149">PR_DISPLAY_BCC</span></span>  <br/> |<span data-ttu-id="34de7-150">Auf TRUE festgelegt, wenn ein oder mehrere Empfänger **MAPI_BCC** Empfänger sind.</span><span class="sxs-lookup"><span data-stu-id="34de7-150">Set to TRUE if one or more of the recipients are **MAPI_BCC** recipients.</span></span>  <br/> |
   
<span data-ttu-id="34de7-151">In x. 400 wird der Umschlag P1 oder Übermittlung benötigt, eine Nachricht, einschließlich des Empfängers Adresseigenschaften und Steuern der Übermittlung und-Antworten Optionsflags übermitteln.</span><span class="sxs-lookup"><span data-stu-id="34de7-151">In X.400, the P1 or delivery envelope is the information needed to deliver a message, including the recipient's address properties and any option flags controlling delivery and replies.</span></span> <span data-ttu-id="34de7-152">Der P2 oder den Anzeigenamen-Umschlag befindet sich die Informationen in der Regel auf jeden Empfänger als den Nachrichtentext selbst angezeigt.</span><span class="sxs-lookup"><span data-stu-id="34de7-152">The P2 or display envelope is the information usually displayed to each recipient other than the message text itself.</span></span> <span data-ttu-id="34de7-153">Sie umfasst in der Regel den Betreff, Wichtigkeit, Priorität, Vertraulichkeit, und Zeitpunkt der Übermittlung, sowie die primären und die kopierte Empfängernamen.</span><span class="sxs-lookup"><span data-stu-id="34de7-153">It typically includes the subject, importance, priority, sensitivity, and submission time, as well as the primary and copied recipient names.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="34de7-154">Verwandte Ressourcen</span><span class="sxs-lookup"><span data-stu-id="34de7-154">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="34de7-155">Protokollspezifikationen</span><span class="sxs-lookup"><span data-stu-id="34de7-155">Protocol specifications</span></span>

<span data-ttu-id="34de7-156">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="34de7-156">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="34de7-157">Bietet Verweise auf Verwandte Exchange Server-Spezifikationen.</span><span class="sxs-lookup"><span data-stu-id="34de7-157">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="34de7-158">[[MS-OXCMSG]](http://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="34de7-158">[[MS-OXCMSG]](http://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="34de7-159">Nachrichten und Anlagen Objekte behandelt.</span><span class="sxs-lookup"><span data-stu-id="34de7-159">Handles message and attachment objects.</span></span>
    
<span data-ttu-id="34de7-160">[[MS-OXOMSG]](http://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="34de7-160">[[MS-OXOMSG]](http://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="34de7-161">Gibt die Eigenschaften und Operationen, die für e-Mail-Nachrichtenobjekte zulässig sind.</span><span class="sxs-lookup"><span data-stu-id="34de7-161">Specifies the properties and operations that are permissible for email message objects.</span></span>
    
<span data-ttu-id="34de7-162">[[MS-OXOCAL]](http://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="34de7-162">[[MS-OXOCAL]](http://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="34de7-163">Gibt die Eigenschaften und Vorgänge für den Termin, einer Besprechungsanfrage und Antwortnachrichten.</span><span class="sxs-lookup"><span data-stu-id="34de7-163">Specifies the properties and operations for appointment, meeting request, and response messages.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="34de7-164">Header-Dateien</span><span class="sxs-lookup"><span data-stu-id="34de7-164">Header files</span></span>

<span data-ttu-id="34de7-165">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="34de7-165">Mapidefs.h</span></span>
  
> <span data-ttu-id="34de7-166">Enthält die Datentypdefinitionen.</span><span class="sxs-lookup"><span data-stu-id="34de7-166">Provides data type definitions.</span></span>
    
<span data-ttu-id="34de7-167">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="34de7-167">Mapitags.h</span></span>
  
> <span data-ttu-id="34de7-168">Enthält Definitionen von Eigenschaften, die als Alternative Namen aufgelistet.</span><span class="sxs-lookup"><span data-stu-id="34de7-168">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="34de7-169">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="34de7-169">See also</span></span>



[<span data-ttu-id="34de7-170">PidTagRecipientStatus (kanonische Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="34de7-170">PidTagRecipientStatus Canonical Property</span></span>](pidtagrecipientstatus-canonical-property.md)
  
[<span data-ttu-id="34de7-171">PidTagDisplayTo (kanonische Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="34de7-171">PidTagDisplayTo Canonical Property</span></span>](pidtagdisplayto-canonical-property.md)
  
[<span data-ttu-id="34de7-172">PidTagDisplayBcc (kanonische Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="34de7-172">PidTagDisplayBcc Canonical Property</span></span>](pidtagdisplaybcc-canonical-property.md)
  
[<span data-ttu-id="34de7-173">PidTagDisplayCc (kanonische Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="34de7-173">PidTagDisplayCc Canonical Property</span></span>](pidtagdisplaycc-canonical-property.md)


[<span data-ttu-id="34de7-174">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="34de7-174">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="34de7-175">Kanonische MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="34de7-175">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="34de7-176">Zuordnen von kanonischen Eigenschaftennamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="34de7-176">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="34de7-177">Zuordnen von MAPI-Namen zu kanonische Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="34de7-177">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

