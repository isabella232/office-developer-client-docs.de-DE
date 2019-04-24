---
title: Kanonische Pidtagrecipienttype (-Eigenschaft
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
ms.openlocfilehash: 9d74fdb3acb6db94078d6090f0def050fb564cd9
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32355258"
---
# <a name="pidtagrecipienttype-canonical-property"></a><span data-ttu-id="5fbaf-103">Kanonische Pidtagrecipienttype (-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="5fbaf-103">PidTagRecipientType Canonical Property</span></span>

  
  
<span data-ttu-id="5fbaf-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="5fbaf-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="5fbaf-105">Enthält den Empfängertyp für einen Nachrichtenempfänger.</span><span class="sxs-lookup"><span data-stu-id="5fbaf-105">Contains the recipient type for a message recipient.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="5fbaf-106">Zugeordnete Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="5fbaf-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="5fbaf-107">PR_RECIPIENT_TYPE</span><span class="sxs-lookup"><span data-stu-id="5fbaf-107">PR_RECIPIENT_TYPE</span></span>  <br/> |
|<span data-ttu-id="5fbaf-108">Kennung:</span><span class="sxs-lookup"><span data-stu-id="5fbaf-108">Identifier:</span></span>  <br/> |<span data-ttu-id="5fbaf-109">0x0C15</span><span class="sxs-lookup"><span data-stu-id="5fbaf-109">0x0C15</span></span>  <br/> |
|<span data-ttu-id="5fbaf-110">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="5fbaf-110">Data type:</span></span>  <br/> |<span data-ttu-id="5fbaf-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="5fbaf-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="5fbaf-112">Bereich:</span><span class="sxs-lookup"><span data-stu-id="5fbaf-112">Area:</span></span>  <br/> |<span data-ttu-id="5fbaf-113">MAPI-Empfänger</span><span class="sxs-lookup"><span data-stu-id="5fbaf-113">MAPI recipient</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="5fbaf-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="5fbaf-114">Remarks</span></span>

<span data-ttu-id="5fbaf-115">Der in dieser Eigenschaft enthaltene Empfängertyp besteht aus einem erforderlichen Wert und einem optionalen Flag.</span><span class="sxs-lookup"><span data-stu-id="5fbaf-115">The recipient type contained in this property consists of one required value and one optional flag.</span></span>
  
<span data-ttu-id="5fbaf-116">Diese Eigenschaft muss genau einen der folgenden Werte enthalten:</span><span class="sxs-lookup"><span data-stu-id="5fbaf-116">This property must contain exactly one of the following values:</span></span>
  
<span data-ttu-id="5fbaf-117">MAPI_TO</span><span class="sxs-lookup"><span data-stu-id="5fbaf-117">MAPI_TO</span></span> 
  
> <span data-ttu-id="5fbaf-118">Der Empfänger ist ein primärer Empfänger (an).</span><span class="sxs-lookup"><span data-stu-id="5fbaf-118">The recipient is a primary (To) recipient.</span></span> <span data-ttu-id="5fbaf-119">Clients müssen primäre Empfänger verarbeiten.</span><span class="sxs-lookup"><span data-stu-id="5fbaf-119">Clients are required to handle primary recipients.</span></span> <span data-ttu-id="5fbaf-120">Alle anderen Typen sind optional.</span><span class="sxs-lookup"><span data-stu-id="5fbaf-120">All other types are optional.</span></span>
    
<span data-ttu-id="5fbaf-121">MAPI_CC</span><span class="sxs-lookup"><span data-stu-id="5fbaf-121">MAPI_CC</span></span> 
  
> <span data-ttu-id="5fbaf-122">Der Empfänger ist ein CC-Empfänger (Carbon Copy), ein Empfänger, der zusätzlich zu den primären Empfängern eine Nachricht empfängt.</span><span class="sxs-lookup"><span data-stu-id="5fbaf-122">The recipient is a carbon copy (CC) recipient, a recipient that receives a message in addition to the primary recipients.</span></span>
    
<span data-ttu-id="5fbaf-123">MAPI_BCC</span><span class="sxs-lookup"><span data-stu-id="5fbaf-123">MAPI_BCC</span></span> 
  
> <span data-ttu-id="5fbaf-124">Der Empfänger ist ein BCC-Empfänger (Blind Carbon Copy).</span><span class="sxs-lookup"><span data-stu-id="5fbaf-124">The recipient is a blind carbon copy (BCC) recipient.</span></span> <span data-ttu-id="5fbaf-125">Primäre und Carbon Copy-Empfänger wissen nicht, dass BCC-Empfänger vorhanden sind.</span><span class="sxs-lookup"><span data-stu-id="5fbaf-125">Primary and carbon copy recipients are unaware of the existence of BCC recipients.</span></span> 
    
<span data-ttu-id="5fbaf-126">MAPI_P1</span><span class="sxs-lookup"><span data-stu-id="5fbaf-126">MAPI_P1</span></span> 
  
> <span data-ttu-id="5fbaf-127">Der Empfänger hat die Nachricht beim vorherigen Versuch nicht erfolgreich empfangen.</span><span class="sxs-lookup"><span data-stu-id="5fbaf-127">The recipient did not successfully receive the message on the previous attempt.</span></span> <span data-ttu-id="5fbaf-128">Dies ist eine erneute Übermittlung einer früheren Übertragung.</span><span class="sxs-lookup"><span data-stu-id="5fbaf-128">This is a resend of an earlier transmission.</span></span>
    
<span data-ttu-id="5fbaf-129">Darüber hinaus kann das folgende Flag festgelegt werden:</span><span class="sxs-lookup"><span data-stu-id="5fbaf-129">In addition, the following flag can be set:</span></span>
  
<span data-ttu-id="5fbaf-130">MAPI_SUBMITTED</span><span class="sxs-lookup"><span data-stu-id="5fbaf-130">MAPI_SUBMITTED</span></span> 
  
> <span data-ttu-id="5fbaf-131">Der Empfänger hat die Nachricht bereits empfangen und muss ihn nicht erneut empfangen.</span><span class="sxs-lookup"><span data-stu-id="5fbaf-131">The recipient has already received the message and does not need to receive it again.</span></span> <span data-ttu-id="5fbaf-132">Dies ist eine erneute Übermittlung einer früheren Übertragung.</span><span class="sxs-lookup"><span data-stu-id="5fbaf-132">This is a resend of an earlier transmission.</span></span> <span data-ttu-id="5fbaf-133">Dieses Flag wird in Verbindung mit den **MAPI_TO**-, **MAPI_CC**-und **MAPI_BCC** -Werten festgelegt.</span><span class="sxs-lookup"><span data-stu-id="5fbaf-133">This flag is set in conjunction with the **MAPI_TO**, **MAPI_CC**, and **MAPI_BCC** values.</span></span> 
    
<span data-ttu-id="5fbaf-134">Der MAPI_P1-Wert und das **MAPI_SUBMITTED** -Flag werden verwendet, wenn eine Nachricht aufgrund einer Nichtübermittlung an einen oder mehrere der vorgesehenen Empfänger erneut übermittelt wird.</span><span class="sxs-lookup"><span data-stu-id="5fbaf-134">The MAPI_P1 value and the **MAPI_SUBMITTED** flag are used when a message is being retransmitted due to nondelivery to one or more of the intended recipients.</span></span> <span data-ttu-id="5fbaf-135">Bei dieser erneuten Übertragung legt der Client **MAPI_SUBMITTED** für jeden Empfänger fest, der die Nachricht nicht erneut benötigt, sondern in der Empfängerliste angezeigt werden soll.</span><span class="sxs-lookup"><span data-stu-id="5fbaf-135">For this retransmission, the client sets **MAPI_SUBMITTED** on every recipient that does not need the message again but should be displayed in the recipient list.</span></span> <span data-ttu-id="5fbaf-136">Für jeden Empfänger, der die Nachricht zuvor nicht erhalten hat, behält der Client den ursprünglichen Empfänger mit dem **PR_RECIPIENT_TYPE** -Wert unverändert bei, gibt aber zusätzlich eine Kopie des Empfängers mit MAPI_P1 anstelle des ursprünglichen Werts aus.</span><span class="sxs-lookup"><span data-stu-id="5fbaf-136">For every recipient that did not receive the message previously, the client retains the original recipient with its **PR_RECIPIENT_TYPE** value unchanged, but additionally submits a copy of the recipient with MAPI_P1 in place of the original value.</span></span> <span data-ttu-id="5fbaf-137">Diese Kopie, die vor der tatsächlichen Übermittlung verworfen wird, zwingt den Empfänger in den P1-Umschlag und garantiert eine physische erneute Übermittlung an diesen Empfänger.</span><span class="sxs-lookup"><span data-stu-id="5fbaf-137">This copy, which is discarded before actual delivery, forces the recipient into the P1 envelope and guarantees physical retransmission to that recipient.</span></span> <span data-ttu-id="5fbaf-138">Die **PR_RESPONSIBILITY** ([pidtagresponsibility (](pidtagresponsibility-canonical-property.md))-Eigenschaft ist für MAPI_P1-Empfänger auf false festgelegt.</span><span class="sxs-lookup"><span data-stu-id="5fbaf-138">The **PR_RESPONSIBILITY** ([PidTagResponsibility](pidtagresponsibility-canonical-property.md)) property is set to FALSE for MAPI_P1 recipients.</span></span>
  
<span data-ttu-id="5fbaf-139">Wenn ein Client ein Resend-Formular anzeigt, sind nur die MAPI_P1-Empfänger sichtbar.</span><span class="sxs-lookup"><span data-stu-id="5fbaf-139">When a client displays a resend form, only the MAPI_P1 recipients are visible.</span></span> <span data-ttu-id="5fbaf-140">Wenn der Benutzer keine weiteren Empfänger eingibt, wird die Empfängerliste genau wie beim ersten Senden der Nachricht angezeigt.</span><span class="sxs-lookup"><span data-stu-id="5fbaf-140">Unless the user enters additional recipients, when the message is delivered, the recipient list appears exactly as it did when the message was sent for the first time.</span></span> 
  
<span data-ttu-id="5fbaf-141">Die Eigenschaften **PR_DISPLAY_TO** ([PidTagDisplayTo](pidtagdisplayto-canonical-property.md)) **, PR_DISPLAY_CC** ([PidTagDisplayCc](pidtagdisplaycc-canonical-property.md)) und **PR_DISPLAY_BCC** ([pidtagdisplaybcc (](pidtagdisplaybcc-canonical-property.md)) beziehen sich auf den Empfängertyp.</span><span class="sxs-lookup"><span data-stu-id="5fbaf-141">The **PR_DISPLAY_TO** ([PidTagDisplayTo](pidtagdisplayto-canonical-property.md)), **PR_DISPLAY_CC** ([PidTagDisplayCc](pidtagdisplaycc-canonical-property.md)) and **PR_DISPLAY_BCC** ([PidTagDisplayBcc](pidtagdisplaybcc-canonical-property.md)) properties are related to recipient type.</span></span> <span data-ttu-id="5fbaf-142">Wenn ein Client die **IMAPIProp:: SaveChanges** einer Nachricht aufruft und mindestens ein Empfänger in der Empfängerliste vorhanden ist, werden diese Eigenschaften vom Nachrichtenspeicher Anbieter wie folgt festgelegt:</span><span class="sxs-lookup"><span data-stu-id="5fbaf-142">When a client calls a message's **IMAPIProp::SaveChanges** and there is at least one recipient in the recipient list, the message store provider sets these properties as follows:</span></span> 
  
|<span data-ttu-id="5fbaf-143">**Eigenschaft**</span><span class="sxs-lookup"><span data-stu-id="5fbaf-143">**Property**</span></span>|<span data-ttu-id="5fbaf-144">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="5fbaf-144">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="5fbaf-145">PR_DISPLAY_TO</span><span class="sxs-lookup"><span data-stu-id="5fbaf-145">PR_DISPLAY_TO</span></span>  <br/> |<span data-ttu-id="5fbaf-146">Legen Sie den Wert auf TRUE fest, wenn mindestens einer der Empfänger **MAPI_TO** Empfänger ist.</span><span class="sxs-lookup"><span data-stu-id="5fbaf-146">Set to TRUE if one or more of the recipients are **MAPI_TO** recipients.</span></span>  <br/> |
|<span data-ttu-id="5fbaf-147">PR_DISPLAY_CC</span><span class="sxs-lookup"><span data-stu-id="5fbaf-147">PR_DISPLAY_CC</span></span>  <br/> |<span data-ttu-id="5fbaf-148">Legen Sie den Wert auf TRUE fest, wenn mindestens einer der Empfänger **MAPI_CC** Empfänger ist.</span><span class="sxs-lookup"><span data-stu-id="5fbaf-148">Set to TRUE if one or more of the recipients are **MAPI_CC** recipients.</span></span>  <br/> |
| <span data-ttu-id="5fbaf-149">PR_DISPLAY_BCC</span><span class="sxs-lookup"><span data-stu-id="5fbaf-149">PR_DISPLAY_BCC</span></span>  <br/> |<span data-ttu-id="5fbaf-150">Legen Sie den Wert auf TRUE fest, wenn mindestens einer der Empfänger **MAPI_BCC** Empfänger ist.</span><span class="sxs-lookup"><span data-stu-id="5fbaf-150">Set to TRUE if one or more of the recipients are **MAPI_BCC** recipients.</span></span>  <br/> |
   
<span data-ttu-id="5fbaf-151">In X. 400 ist der P1-oder Zustellungs Umschlag die Informationen, die für die Zustellung einer Nachricht erforderlich sind, einschließlich der Adresseigenschaften des Empfängers und beliebiger Options Fahnen zur Steuerung der Zustellung und der Antworten.</span><span class="sxs-lookup"><span data-stu-id="5fbaf-151">In X.400, the P1 or delivery envelope is the information needed to deliver a message, including the recipient's address properties and any option flags controlling delivery and replies.</span></span> <span data-ttu-id="5fbaf-152">Der P2-oder Anzeige Umschlag stellt die Informationen dar, die in der Regel jedem anderen Empfänger als dem Nachrichtentext angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="5fbaf-152">The P2 or display envelope is the information usually displayed to each recipient other than the message text itself.</span></span> <span data-ttu-id="5fbaf-153">Sie umfasst in der Regel den Betreff, die Wichtigkeit, die Priorität, die Vertraulichkeit und die Übermittlungszeit sowie die primären und kopierten Empfängernamen.</span><span class="sxs-lookup"><span data-stu-id="5fbaf-153">It typically includes the subject, importance, priority, sensitivity, and submission time, as well as the primary and copied recipient names.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="5fbaf-154">Zugehörige Ressourcen</span><span class="sxs-lookup"><span data-stu-id="5fbaf-154">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="5fbaf-155">Protokollspezifikationen</span><span class="sxs-lookup"><span data-stu-id="5fbaf-155">Protocol specifications</span></span>

<span data-ttu-id="5fbaf-156">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="5fbaf-156">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="5fbaf-157">Enthält Verweise auf zugehörige Exchange Server-Protokollspezifikationen.</span><span class="sxs-lookup"><span data-stu-id="5fbaf-157">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="5fbaf-158">[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="5fbaf-158">[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="5fbaf-159">Verarbeitet Nachrichten-und Anlagenobjekte.</span><span class="sxs-lookup"><span data-stu-id="5fbaf-159">Handles message and attachment objects.</span></span>
    
<span data-ttu-id="5fbaf-160">[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="5fbaf-160">[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="5fbaf-161">Gibt die Eigenschaften und Vorgänge an, die für e-Mail-Nachrichtenobjekte zulässig sind.</span><span class="sxs-lookup"><span data-stu-id="5fbaf-161">Specifies the properties and operations that are permissible for email message objects.</span></span>
    
<span data-ttu-id="5fbaf-162">[[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="5fbaf-162">[[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="5fbaf-163">Gibt die Eigenschaften und Vorgänge für Termin-, Besprechungs-und Antwortnachrichten an.</span><span class="sxs-lookup"><span data-stu-id="5fbaf-163">Specifies the properties and operations for appointment, meeting request, and response messages.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="5fbaf-164">Header Dateien</span><span class="sxs-lookup"><span data-stu-id="5fbaf-164">Header files</span></span>

<span data-ttu-id="5fbaf-165">Mapidefs. h</span><span class="sxs-lookup"><span data-stu-id="5fbaf-165">Mapidefs.h</span></span>
  
> <span data-ttu-id="5fbaf-166">Stellt Datentypdefinitionen bereit.</span><span class="sxs-lookup"><span data-stu-id="5fbaf-166">Provides data type definitions.</span></span>
    
<span data-ttu-id="5fbaf-167">Mapitags. h</span><span class="sxs-lookup"><span data-stu-id="5fbaf-167">Mapitags.h</span></span>
  
> <span data-ttu-id="5fbaf-168">Enthält Definitionen von Eigenschaften, die als Alternative Namen aufgeführt sind.</span><span class="sxs-lookup"><span data-stu-id="5fbaf-168">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="5fbaf-169">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="5fbaf-169">See also</span></span>



[<span data-ttu-id="5fbaf-170">Kanonische Pidtagrecipientstatus (-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="5fbaf-170">PidTagRecipientStatus Canonical Property</span></span>](pidtagrecipientstatus-canonical-property.md)
  
[<span data-ttu-id="5fbaf-171">Kanonische PidTagDisplayTo-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="5fbaf-171">PidTagDisplayTo Canonical Property</span></span>](pidtagdisplayto-canonical-property.md)
  
[<span data-ttu-id="5fbaf-172">Kanonische Pidtagdisplaybcc (-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="5fbaf-172">PidTagDisplayBcc Canonical Property</span></span>](pidtagdisplaybcc-canonical-property.md)
  
[<span data-ttu-id="5fbaf-173">Kanonische PidTagDisplayCc-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="5fbaf-173">PidTagDisplayCc Canonical Property</span></span>](pidtagdisplaycc-canonical-property.md)


[<span data-ttu-id="5fbaf-174">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="5fbaf-174">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="5fbaf-175">Kanonische MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="5fbaf-175">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="5fbaf-176">Zuordnen von kanonischen Eigenschaftennamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="5fbaf-176">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="5fbaf-177">Zuordnen von MAPI-Namen zu kanonischen Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="5fbaf-177">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

