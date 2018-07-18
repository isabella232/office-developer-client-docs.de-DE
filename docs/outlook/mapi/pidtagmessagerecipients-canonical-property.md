---
title: PidTagMessageRecipients (kanonische Eigenschaft)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagMessageRecipients
api_type:
- HeaderDef
ms.assetid: 7f8b0d96-99d6-4f1c-8ac4-4dbb83626382
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: 980b1b81a0afbfe05fee915ddd730aad31811132
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19794615"
---
# <a name="pidtagmessagerecipients-canonical-property"></a><span data-ttu-id="c800f-103">PidTagMessageRecipients (kanonische Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="c800f-103">PidTagMessageRecipients Canonical Property</span></span>

  
  
<span data-ttu-id="c800f-104">**Betrifft**: Outlook</span><span class="sxs-lookup"><span data-stu-id="c800f-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="c800f-105">Enthält eine Tabelle mit Einschränkungen, die auf einer Inhaltstabelle, erhalten alle Nachrichten, die Empfänger Unterobjekte enthalten, die die Suchkriterien erfüllen angewendet werden kann.</span><span class="sxs-lookup"><span data-stu-id="c800f-105">Contains a table of restrictions that can be applied to a contents table to find all messages that contain recipient subobjects that meet the restrictions.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="c800f-106">Zugeordneten Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="c800f-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="c800f-107">PR_MESSAGE_RECIPIENTS</span><span class="sxs-lookup"><span data-stu-id="c800f-107">PR_MESSAGE_RECIPIENTS</span></span>  <br/> |
|<span data-ttu-id="c800f-108">Bezeichner:</span><span class="sxs-lookup"><span data-stu-id="c800f-108">Identifier:</span></span>  <br/> |<span data-ttu-id="c800f-109">0x0E12</span><span class="sxs-lookup"><span data-stu-id="c800f-109">0x0E12</span></span>  <br/> |
|<span data-ttu-id="c800f-110">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="c800f-110">Data type:</span></span>  <br/> |<span data-ttu-id="c800f-111">PT_OBJECT</span><span class="sxs-lookup"><span data-stu-id="c800f-111">PT_OBJECT</span></span>  <br/> |
|<span data-ttu-id="c800f-112">Bereich:</span><span class="sxs-lookup"><span data-stu-id="c800f-112">Area:</span></span>  <br/> |<span data-ttu-id="c800f-113">Allgemeine messaging</span><span class="sxs-lookup"><span data-stu-id="c800f-113">General messaging</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="c800f-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="c800f-114">Remarks</span></span>

<span data-ttu-id="c800f-115">Diese Eigenschaft kann in [IMAPIProp::CopyTo](imapiprop-copyto.md) Vorgänge aus- oder in [IMAPIProp::CopyProps](imapiprop-copyprops.md) Vorgänge eingeschlossen werden.</span><span class="sxs-lookup"><span data-stu-id="c800f-115">This property can be excluded in [IMAPIProp::CopyTo](imapiprop-copyto.md) operations or included in [IMAPIProp::CopyProps](imapiprop-copyprops.md) operations.</span></span> <span data-ttu-id="c800f-116">Als Eigenschaft vom Typ **PT_OBJECT**kann es erfolgreich von der [IMAPIProp::GetProps](imapiprop-getprops.md) -Methode abgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="c800f-116">As a property of type **PT_OBJECT**, it cannot be successfully retrieved by the [IMAPIProp::GetProps](imapiprop-getprops.md) method.</span></span> <span data-ttu-id="c800f-117">Von der [IMAPIProp::OpenProperty](imapiprop-openproperty.md) -Methode der **IID_IMAPITable** Identifier anfordern sollte seinen Inhalt zugegriffen werden.</span><span class="sxs-lookup"><span data-stu-id="c800f-117">Its contents should be accessed by the [IMAPIProp::OpenProperty](imapiprop-openproperty.md) method, requesting the **IID_IMAPITable** interface identifier.</span></span> <span data-ttu-id="c800f-118">Dienstanbieter müssen es an die [IMAPIProp::GetPropList](imapiprop-getproplist.md) -Methode melden, wenn er festgelegt ist, aber optional meldet oder nicht, wenn sie nicht festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="c800f-118">Service providers must report it to the [IMAPIProp::GetPropList](imapiprop-getproplist.md) method if it is set, but may optionally report it or not if it is not set.</span></span> 
  
<span data-ttu-id="c800f-119">Zum Abrufen von Inhaltsverzeichnisses sollte eine Clientanwendung die [IMessage::GetRecipientTable](imessage-getrecipienttable.md) -Methode aufrufen.</span><span class="sxs-lookup"><span data-stu-id="c800f-119">To retrieve table contents, a client application should call the [IMessage::GetRecipientTable](imessage-getrecipienttable.md) method.</span></span> 
  
<span data-ttu-id="c800f-120">Diese Eigenschaft kann durch Festlegen in der Struktur [SSubRestriction](ssubrestriction.md) für Unterobjekts Einschränkung verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="c800f-120">This property can be used for subobject restriction by specifying it in the [SSubRestriction](ssubrestriction.md) structure.</span></span> <span data-ttu-id="c800f-121">Auf diese Weise können einen Client zur Begrenzung der Ansicht eines Containers für Nachrichten mit meeting Empfänger bestimmte Kriterien erfüllen.</span><span class="sxs-lookup"><span data-stu-id="c800f-121">This enables a client to limit the view of a container to messages with recipients meeting given criteria.</span></span> <span data-ttu-id="c800f-122">Eine Nachricht qualifiziert für anzeigen, wenn mindestens eine Zeile in der Empfänger Tabelle, d. h., ein Empfänger die Einschränkung Unterobjekts erfüllt.</span><span class="sxs-lookup"><span data-stu-id="c800f-122">A message qualifies for viewing if at least one row in its recipient table, that is, one recipient satisfies the subobject restriction.</span></span> 
  
 <span data-ttu-id="c800f-123">**Hinweis** Verwendung von Unterobjekts Einschränkung Ergebnisse ist das Äquivalent von einer [IMAPISession::OpenEntry](imapisession-openentry.md) rufen Sie für jede Nachricht in der Tabelle.</span><span class="sxs-lookup"><span data-stu-id="c800f-123">**Note** Using subobject restriction results is the equivalent of an [IMAPISession::OpenEntry](imapisession-openentry.md) call on every message in the table.</span></span> <span data-ttu-id="c800f-124">Je nach der Clientanwendung und die Anzahl der Nachrichten an, die durchsucht werden können sie die Leistung beeinträchtigen.</span><span class="sxs-lookup"><span data-stu-id="c800f-124">Depending on the client application and the number of messages to be searched, it can affect performance.</span></span> 
  
<span data-ttu-id="c800f-125">Die Eigenschaft **PR_MESSAGE_ATTACHMENTS** ([PidTagMessageAttachments](pidtagmessageattachments-canonical-property.md)) und diese Eigenschaft ähneln in Verwendung.</span><span class="sxs-lookup"><span data-stu-id="c800f-125">The **PR_MESSAGE_ATTACHMENTS** ([PidTagMessageAttachments](pidtagmessageattachments-canonical-property.md)) property and this property are similar in usage.</span></span> <span data-ttu-id="c800f-126">Mehrere MAPI-Eigenschaften bieten Zugriff auf Tabellen:</span><span class="sxs-lookup"><span data-stu-id="c800f-126">Several MAPI properties provide access to tables:</span></span> 
  
|<span data-ttu-id="c800f-127">**Eigenschaft**</span><span class="sxs-lookup"><span data-stu-id="c800f-127">**Property**</span></span>|<span data-ttu-id="c800f-128">**Table**</span><span class="sxs-lookup"><span data-stu-id="c800f-128">**Table**</span></span>|
|:-----|:-----|
|<span data-ttu-id="c800f-129">**PR_CONTAINER_CONTENTS** ([PidTagContainerContents](pidtagcontainercontents-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="c800f-129">**PR_CONTAINER_CONTENTS** ([PidTagContainerContents](pidtagcontainercontents-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="c800f-130">Inhaltstabelle</span><span class="sxs-lookup"><span data-stu-id="c800f-130">Contents table</span></span>  <br/> |
|<span data-ttu-id="c800f-131">**PR_CONTAINER_HIERARCHY** ([PidTagContainerHierarchy](pidtagcontainerhierarchy-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="c800f-131">**PR_CONTAINER_HIERARCHY** ([PidTagContainerHierarchy](pidtagcontainerhierarchy-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="c800f-132">Hierarchietabelle</span><span class="sxs-lookup"><span data-stu-id="c800f-132">Hierarchy table</span></span>  <br/> |
|<span data-ttu-id="c800f-133">**PR_FOLDER_ASSOCIATED_CONTENTS** ([PidTagFolderAssociatedContents](pidtagfolderassociatedcontents-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="c800f-133">**PR_FOLDER_ASSOCIATED_CONTENTS** ([PidTagFolderAssociatedContents](pidtagfolderassociatedcontents-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="c800f-134">Zugehörige Inhaltstabelle</span><span class="sxs-lookup"><span data-stu-id="c800f-134">Associated contents table</span></span>  <br/> |
|<span data-ttu-id="c800f-135">**PR_MESSAGE_ATTACHMENTS** ([PidTagMessageAttachments](pidtagmessageattachments-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="c800f-135">**PR_MESSAGE_ATTACHMENTS** ([PidTagMessageAttachments](pidtagmessageattachments-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="c800f-136">Anlagentabelle</span><span class="sxs-lookup"><span data-stu-id="c800f-136">Attachment table</span></span>  <br/> |
|<span data-ttu-id="c800f-137">PR_MESSAGE_RECIPIENTS</span><span class="sxs-lookup"><span data-stu-id="c800f-137">PR_MESSAGE_RECIPIENTS</span></span>  <br/> |<span data-ttu-id="c800f-138">Empfänger-Tabelle</span><span class="sxs-lookup"><span data-stu-id="c800f-138">Recipient table</span></span>  <br/> |
   
## <a name="related-resources"></a><span data-ttu-id="c800f-139">Verwandte Ressourcen</span><span class="sxs-lookup"><span data-stu-id="c800f-139">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="c800f-140">Protokollspezifikationen</span><span class="sxs-lookup"><span data-stu-id="c800f-140">Protocol specifications</span></span>

<span data-ttu-id="c800f-141">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="c800f-141">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="c800f-142">Bietet Verweise auf Verwandte Exchange Server-Spezifikationen.</span><span class="sxs-lookup"><span data-stu-id="c800f-142">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="c800f-143">[[MS-OXCFXICS]](http://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="c800f-143">[[MS-OXCFXICS]](http://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="c800f-144">Verarbeitet die Reihenfolge und den Fluss für Datenübertragungen zwischen einem Client und Server.</span><span class="sxs-lookup"><span data-stu-id="c800f-144">Handles the order and flow for data transfers between a client and server.</span></span>
    
<span data-ttu-id="c800f-145">[[MS-OXCICAL]](http://msdn.microsoft.com/library/a685a040-5b69-4c84-b084-795113fb4012%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="c800f-145">[[MS-OXCICAL]](http://msdn.microsoft.com/library/a685a040-5b69-4c84-b084-795113fb4012%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="c800f-146">Konvertiert zwischen IETF RFC2445, RFC2446, RFC2447, und Termine und meeting-Objekte.</span><span class="sxs-lookup"><span data-stu-id="c800f-146">Converts between IETF RFC2445, RFC2446, and RFC2447, and appointment and meeting objects.</span></span>
    
<span data-ttu-id="c800f-147">[[MS-OXCSPAM]](http://msdn.microsoft.com/library/522f8587-4aed-4cd6-831b-40bd87862189%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="c800f-147">[[MS-OXCSPAM]](http://msdn.microsoft.com/library/522f8587-4aed-4cd6-831b-40bd87862189%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="c800f-148">Ermöglicht die Behandlung von zulassen/blockieren-Listen und die Bestimmung des junk-e-Mail-Nachrichten.</span><span class="sxs-lookup"><span data-stu-id="c800f-148">Enables the handling of allow/block lists and the determination of junk email messages.</span></span>
    
<span data-ttu-id="c800f-149">[[MS-OXTNEF]](http://msdn.microsoft.com/library/1f0544d7-30b7-4194-b58f-adc82f3763bb%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="c800f-149">[[MS-OXTNEF]](http://msdn.microsoft.com/library/1f0544d7-30b7-4194-b58f-adc82f3763bb%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="c800f-150">Codiert und decodiert Nachrichten- und Objekte, die auf eine effiziente Streamdarstellung.</span><span class="sxs-lookup"><span data-stu-id="c800f-150">Encodes and decodes message and attachment objects to an efficient stream representation.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="c800f-151">Header-Dateien</span><span class="sxs-lookup"><span data-stu-id="c800f-151">Header files</span></span>

<span data-ttu-id="c800f-152">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="c800f-152">Mapidefs.h</span></span>
  
> <span data-ttu-id="c800f-153">Enthält die Datentypdefinitionen.</span><span class="sxs-lookup"><span data-stu-id="c800f-153">Provides data type definitions.</span></span>
    
<span data-ttu-id="c800f-154">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="c800f-154">Mapitags.h</span></span>
  
> <span data-ttu-id="c800f-155">Enthält Definitionen von Eigenschaften, die als Alternative Namen aufgelistet.</span><span class="sxs-lookup"><span data-stu-id="c800f-155">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="c800f-156">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="c800f-156">See also</span></span>



[<span data-ttu-id="c800f-157">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="c800f-157">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="c800f-158">Kanonische MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="c800f-158">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="c800f-159">Zuordnen von kanonischen Eigenschaftennamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="c800f-159">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="c800f-160">Zuordnen von MAPI-Namen zu kanonische Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="c800f-160">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

