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
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: d30088ba7398669228a18be825323afa800ec536
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32355685"
---
# <a name="pidtagmessagerecipients-canonical-property"></a><span data-ttu-id="7af1d-103">PidTagMessageRecipients (kanonische Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="7af1d-103">PidTagMessageRecipients Canonical Property</span></span>

  
  
<span data-ttu-id="7af1d-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="7af1d-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="7af1d-105">Enthält eine Tabelle mit Einschränkungen, die auf eine Inhaltstabelle angewendet werden können, um alle Nachrichten zu finden, die Empfängerunterobjekte enthalten, die die Einschränkungen erfüllen.</span><span class="sxs-lookup"><span data-stu-id="7af1d-105">Contains a table of restrictions that can be applied to a contents table to find all messages that contain recipient subobjects that meet the restrictions.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="7af1d-106">Zugeordnete Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="7af1d-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="7af1d-107">PR_MESSAGE_RECIPIENTS</span><span class="sxs-lookup"><span data-stu-id="7af1d-107">PR_MESSAGE_RECIPIENTS</span></span>  <br/> |
|<span data-ttu-id="7af1d-108">Kennung:</span><span class="sxs-lookup"><span data-stu-id="7af1d-108">Identifier:</span></span>  <br/> |<span data-ttu-id="7af1d-109">0x0E12</span><span class="sxs-lookup"><span data-stu-id="7af1d-109">0x0E12</span></span>  <br/> |
|<span data-ttu-id="7af1d-110">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="7af1d-110">Data type:</span></span>  <br/> |<span data-ttu-id="7af1d-111">PT_OBJECT</span><span class="sxs-lookup"><span data-stu-id="7af1d-111">PT_OBJECT</span></span>  <br/> |
|<span data-ttu-id="7af1d-112">Bereich:</span><span class="sxs-lookup"><span data-stu-id="7af1d-112">Area:</span></span>  <br/> |<span data-ttu-id="7af1d-113">Allgemeines Messaging</span><span class="sxs-lookup"><span data-stu-id="7af1d-113">General messaging</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="7af1d-114">Hinweise</span><span class="sxs-lookup"><span data-stu-id="7af1d-114">Remarks</span></span>

<span data-ttu-id="7af1d-115">Diese Eigenschaft kann in [IMAPIProp::CopyTo-Vorgängen](imapiprop-copyto.md) ausgeschlossen oder in [IMAPIProp::CopyProps-Vorgängen enthalten](imapiprop-copyprops.md) sein.</span><span class="sxs-lookup"><span data-stu-id="7af1d-115">This property can be excluded in [IMAPIProp::CopyTo](imapiprop-copyto.md) operations or included in [IMAPIProp::CopyProps](imapiprop-copyprops.md) operations.</span></span> <span data-ttu-id="7af1d-116">Als Eigenschaft vom Typ **PT_OBJECT** kann sie nicht erfolgreich von der [IMAPIProp::GetProps-Methode abgerufen](imapiprop-getprops.md) werden.</span><span class="sxs-lookup"><span data-stu-id="7af1d-116">As a property of type **PT_OBJECT**, it cannot be successfully retrieved by the [IMAPIProp::GetProps](imapiprop-getprops.md) method.</span></span> <span data-ttu-id="7af1d-117">Der Zugriff auf den Inhalt sollte über die [IMAPIProp::OpenProperty-Methode](imapiprop-openproperty.md) erfolgen, die den IID_IMAPITable  anfordert.</span><span class="sxs-lookup"><span data-stu-id="7af1d-117">Its contents should be accessed by the [IMAPIProp::OpenProperty](imapiprop-openproperty.md) method, requesting the **IID_IMAPITable** interface identifier.</span></span> <span data-ttu-id="7af1d-118">Dienstanbieter müssen sie der [IMAPIProp::GetPropList-Methode](imapiprop-getproplist.md) melden, wenn sie festgelegt ist, kann sie jedoch optional melden oder nicht, wenn sie nicht festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="7af1d-118">Service providers must report it to the [IMAPIProp::GetPropList](imapiprop-getproplist.md) method if it is set, but may optionally report it or not if it is not set.</span></span> 
  
<span data-ttu-id="7af1d-119">Zum Abrufen von Tabelleninhalten sollte eine Clientanwendung die [IMessage::GetRecipientTable-Methode](imessage-getrecipienttable.md) aufrufen.</span><span class="sxs-lookup"><span data-stu-id="7af1d-119">To retrieve table contents, a client application should call the [IMessage::GetRecipientTable](imessage-getrecipienttable.md) method.</span></span> 
  
<span data-ttu-id="7af1d-120">Diese Eigenschaft kann für die Unterobjekteinschränkung verwendet werden, indem sie in der [SSubRestriction-Struktur angegeben](ssubrestriction.md) wird.</span><span class="sxs-lookup"><span data-stu-id="7af1d-120">This property can be used for subobject restriction by specifying it in the [SSubRestriction](ssubrestriction.md) structure.</span></span> <span data-ttu-id="7af1d-121">Dadurch kann ein Client die Ansicht eines Containers auf Nachrichten beschränken, deren Empfänger bestimmte Kriterien erfüllen.</span><span class="sxs-lookup"><span data-stu-id="7af1d-121">This enables a client to limit the view of a container to messages with recipients meeting given criteria.</span></span> <span data-ttu-id="7af1d-122">Eine Nachricht kann angezeigt werden, wenn mindestens eine Zeile in der Empfängertabelle, d. h. ein Empfänger die Unterobjekteinschränkung erfüllt.</span><span class="sxs-lookup"><span data-stu-id="7af1d-122">A message qualifies for viewing if at least one row in its recipient table, that is, one recipient satisfies the subobject restriction.</span></span> 
  
 <span data-ttu-id="7af1d-123">**Hinweis** Die Verwendung von Ergebnissen der Unterobjekteinschränkung entspricht einem [IMAPISession::OpenEntry-Aufruf](imapisession-openentry.md) für jede Nachricht in der Tabelle.</span><span class="sxs-lookup"><span data-stu-id="7af1d-123">**Note** Using subobject restriction results is the equivalent of an [IMAPISession::OpenEntry](imapisession-openentry.md) call on every message in the table.</span></span> <span data-ttu-id="7af1d-124">Abhängig von der Clientanwendung und der Anzahl der zu durchsuchende Nachrichten kann sich dies auf die Leistung auswirken.</span><span class="sxs-lookup"><span data-stu-id="7af1d-124">Depending on the client application and the number of messages to be searched, it can affect performance.</span></span> 
  
<span data-ttu-id="7af1d-125">Die **PR_MESSAGE_ATTACHMENTS** ([PidTagMessageAttachments](pidtagmessageattachments-canonical-property.md)) -Eigenschaft und diese Eigenschaft sind in der Verwendung ähnlich.</span><span class="sxs-lookup"><span data-stu-id="7af1d-125">The **PR_MESSAGE_ATTACHMENTS** ([PidTagMessageAttachments](pidtagmessageattachments-canonical-property.md)) property and this property are similar in usage.</span></span> <span data-ttu-id="7af1d-126">Mehrere MAPI-Eigenschaften bieten Zugriff auf Tabellen:</span><span class="sxs-lookup"><span data-stu-id="7af1d-126">Several MAPI properties provide access to tables:</span></span> 
  
|<span data-ttu-id="7af1d-127">**Eigenschaft**</span><span class="sxs-lookup"><span data-stu-id="7af1d-127">**Property**</span></span>|<span data-ttu-id="7af1d-128">**Table**</span><span class="sxs-lookup"><span data-stu-id="7af1d-128">**Table**</span></span>|
|:-----|:-----|
|<span data-ttu-id="7af1d-129">**PR_CONTAINER_CONTENTS** ([PidTagContainerContents](pidtagcontainercontents-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="7af1d-129">**PR_CONTAINER_CONTENTS** ([PidTagContainerContents](pidtagcontainercontents-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="7af1d-130">Inhaltstabelle</span><span class="sxs-lookup"><span data-stu-id="7af1d-130">Contents table</span></span>  <br/> |
|<span data-ttu-id="7af1d-131">**PR_CONTAINER_HIERARCHY** ([PidTagContainerHierarchy](pidtagcontainerhierarchy-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="7af1d-131">**PR_CONTAINER_HIERARCHY** ([PidTagContainerHierarchy](pidtagcontainerhierarchy-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="7af1d-132">Hierarchietabelle</span><span class="sxs-lookup"><span data-stu-id="7af1d-132">Hierarchy table</span></span>  <br/> |
|<span data-ttu-id="7af1d-133">**PR_FOLDER_ASSOCIATED_CONTENTS** ([PidTagFolderAssociatedContents](pidtagfolderassociatedcontents-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="7af1d-133">**PR_FOLDER_ASSOCIATED_CONTENTS** ([PidTagFolderAssociatedContents](pidtagfolderassociatedcontents-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="7af1d-134">Tabelle "Zugeordnete Inhalte"</span><span class="sxs-lookup"><span data-stu-id="7af1d-134">Associated contents table</span></span>  <br/> |
|<span data-ttu-id="7af1d-135">**PR_MESSAGE_ATTACHMENTS** ([PidTagMessageAttachments](pidtagmessageattachments-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="7af1d-135">**PR_MESSAGE_ATTACHMENTS** ([PidTagMessageAttachments](pidtagmessageattachments-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="7af1d-136">Anlagentabelle</span><span class="sxs-lookup"><span data-stu-id="7af1d-136">Attachment table</span></span>  <br/> |
|<span data-ttu-id="7af1d-137">PR_MESSAGE_RECIPIENTS</span><span class="sxs-lookup"><span data-stu-id="7af1d-137">PR_MESSAGE_RECIPIENTS</span></span>  <br/> |<span data-ttu-id="7af1d-138">Empfängertabelle</span><span class="sxs-lookup"><span data-stu-id="7af1d-138">Recipient table</span></span>  <br/> |
   
## <a name="related-resources"></a><span data-ttu-id="7af1d-139">Verwandte Ressourcen</span><span class="sxs-lookup"><span data-stu-id="7af1d-139">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="7af1d-140">Protokollspezifikationen</span><span class="sxs-lookup"><span data-stu-id="7af1d-140">Protocol specifications</span></span>

<span data-ttu-id="7af1d-141">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="7af1d-141">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="7af1d-142">Enthält Verweise auf Exchange Server Protokollspezifikationen.</span><span class="sxs-lookup"><span data-stu-id="7af1d-142">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="7af1d-143">[[MS-OXCFXICS]](https://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="7af1d-143">[[MS-OXCFXICS]](https://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="7af1d-144">Verarbeitet die Reihenfolge und den Fluss für Datenübertragungen zwischen einem Client und einem Server.</span><span class="sxs-lookup"><span data-stu-id="7af1d-144">Handles the order and flow for data transfers between a client and server.</span></span>
    
<span data-ttu-id="7af1d-145">[[MS-OXCICAL]](https://msdn.microsoft.com/library/a685a040-5b69-4c84-b084-795113fb4012%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="7af1d-145">[[MS-OXCICAL]](https://msdn.microsoft.com/library/a685a040-5b69-4c84-b084-795113fb4012%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="7af1d-146">Konvertiert zwischen IETF RFC2445, RFC2446 und RFC2447 sowie Termin- und Besprechungsobjekten.</span><span class="sxs-lookup"><span data-stu-id="7af1d-146">Converts between IETF RFC2445, RFC2446, and RFC2447, and appointment and meeting objects.</span></span>
    
<span data-ttu-id="7af1d-147">[[MS-OXCSPAM]](https://msdn.microsoft.com/library/522f8587-4aed-4cd6-831b-40bd87862189%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="7af1d-147">[[MS-OXCSPAM]](https://msdn.microsoft.com/library/522f8587-4aed-4cd6-831b-40bd87862189%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="7af1d-148">Ermöglicht die Behandlung von Zulässig-/Sperrlisten und die Ermittlung von Junk-E-Mail-Nachrichten.</span><span class="sxs-lookup"><span data-stu-id="7af1d-148">Enables the handling of allow/block lists and the determination of junk email messages.</span></span>
    
<span data-ttu-id="7af1d-149">[[MS-OXTNEF]](https://msdn.microsoft.com/library/1f0544d7-30b7-4194-b58f-adc82f3763bb%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="7af1d-149">[[MS-OXTNEF]](https://msdn.microsoft.com/library/1f0544d7-30b7-4194-b58f-adc82f3763bb%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="7af1d-150">Codiert und decodiert Nachrichten- und Anlagenobjekte in eine effiziente Streamdarstellung.</span><span class="sxs-lookup"><span data-stu-id="7af1d-150">Encodes and decodes message and attachment objects to an efficient stream representation.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="7af1d-151">Headerdateien</span><span class="sxs-lookup"><span data-stu-id="7af1d-151">Header files</span></span>

<span data-ttu-id="7af1d-152">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="7af1d-152">Mapidefs.h</span></span>
  
> <span data-ttu-id="7af1d-153">Bietet Datentypdefinitionen.</span><span class="sxs-lookup"><span data-stu-id="7af1d-153">Provides data type definitions.</span></span>
    
<span data-ttu-id="7af1d-154">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="7af1d-154">Mapitags.h</span></span>
  
> <span data-ttu-id="7af1d-155">Enthält Definitionen von Eigenschaften, die als alternative Namen aufgeführt sind.</span><span class="sxs-lookup"><span data-stu-id="7af1d-155">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="7af1d-156">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="7af1d-156">See also</span></span>



[<span data-ttu-id="7af1d-157">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="7af1d-157">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="7af1d-158">KANONISCHE EIGENSCHAFTEN VON MAPI</span><span class="sxs-lookup"><span data-stu-id="7af1d-158">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="7af1d-159">Zuordnen kanonischer Eigenschaftsnamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="7af1d-159">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="7af1d-160">Zuordnen von MAPI-Namen zu kanonischen Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="7af1d-160">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

