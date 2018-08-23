---
title: PidTagFolderAssociatedContents (kanonische Eigenschaft)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagFolderAssociatedContents
api_type:
- HeaderDef
ms.assetid: d1f3f589-dc2d-4538-a13f-278dad29bcc7
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: ae09488b99cd55e5cfca23f504d81ac5919633d3
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2018
ms.locfileid: "22574153"
---
# <a name="pidtagfolderassociatedcontents-canonical-property"></a><span data-ttu-id="1f79c-103">PidTagFolderAssociatedContents (kanonische Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="1f79c-103">PidTagFolderAssociatedContents Canonical Property</span></span>

  
  
<span data-ttu-id="1f79c-104">**Betrifft**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="1f79c-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="1f79c-105">Enthält eine eingebettete Inhalt Table-Objekt, das Informationen über die Inhaltstabelle zugeordneten bereitstellt.</span><span class="sxs-lookup"><span data-stu-id="1f79c-105">Contains an embedded contents table object that provides information about the associated contents table.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="1f79c-106">Zugeordnete Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="1f79c-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="1f79c-107">PR_FOLDER_ASSOCIATED_CONTENTS</span><span class="sxs-lookup"><span data-stu-id="1f79c-107">PR_FOLDER_ASSOCIATED_CONTENTS</span></span>  <br/> |
|<span data-ttu-id="1f79c-108">Kennung:</span><span class="sxs-lookup"><span data-stu-id="1f79c-108">Identifier:</span></span>  <br/> |<span data-ttu-id="1f79c-109">0x3610</span><span class="sxs-lookup"><span data-stu-id="1f79c-109">0x3610</span></span>  <br/> |
|<span data-ttu-id="1f79c-110">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="1f79c-110">Data type:</span></span>  <br/> |<span data-ttu-id="1f79c-111">PT_OBJECT</span><span class="sxs-lookup"><span data-stu-id="1f79c-111">PT_OBJECT</span></span>  <br/> |
|<span data-ttu-id="1f79c-112">Bereich:</span><span class="sxs-lookup"><span data-stu-id="1f79c-112">Area:</span></span>  <br/> |<span data-ttu-id="1f79c-113">MAPI-container</span><span class="sxs-lookup"><span data-stu-id="1f79c-113">MAPI container</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="1f79c-114">HinwBemerkungeneise</span><span class="sxs-lookup"><span data-stu-id="1f79c-114">Remarks</span></span>

<span data-ttu-id="1f79c-115">Der zugehörige Inhaltstabelle stellt einen Unterordner, der nicht in der Inhaltstabelle standard angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="1f79c-115">The associated contents table represents a subfolder that does not appear in the standard contents table.</span></span> <span data-ttu-id="1f79c-116">Sie enthält den Ordner verknüpft oder ausgeblendet, Nachrichten.</span><span class="sxs-lookup"><span data-stu-id="1f79c-116">It contains the folder's associated, or hidden, messages.</span></span> 
  
<span data-ttu-id="1f79c-117">Diese Eigenschaft kann in [IMAPIProp::CopyTo](imapiprop-copyto.md) Vorgänge aus- oder in [IMAPIProp::CopyProps](imapiprop-copyprops.md) Vorgänge eingeschlossen werden.</span><span class="sxs-lookup"><span data-stu-id="1f79c-117">This property can be excluded in [IMAPIProp::CopyTo](imapiprop-copyto.md) operations or included in [IMAPIProp::CopyProps](imapiprop-copyprops.md) operations.</span></span> <span data-ttu-id="1f79c-118">Als Eigenschaft vom Typ **PT_OBJECT**kann nicht es erfolgreich von der [IMAPIProp::GetProps](imapiprop-getprops.md) -Methode abgerufen werden. von der [IMAPIProp::OpenProperty](imapiprop-openproperty.md) -Methode der **IID_IMAPITable** Identifier anfordern sollte seinen Inhalt zugegriffen werden.</span><span class="sxs-lookup"><span data-stu-id="1f79c-118">As a property of type **PT_OBJECT**, it cannot be successfully retrieved by the [IMAPIProp::GetProps](imapiprop-getprops.md) method; its contents should be accessed by the [IMAPIProp::OpenProperty](imapiprop-openproperty.md) method, requesting the **IID_IMAPITable** interface identifier.</span></span> <span data-ttu-id="1f79c-119">Dienstanbieter müssen es an die [IMAPIProp::GetPropList](imapiprop-getproplist.md) -Methode melden, wenn er festgelegt ist, aber optional meldet oder nicht, wenn sie nicht festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="1f79c-119">Service providers must report it to the [IMAPIProp::GetPropList](imapiprop-getproplist.md) method if it is set, but may optionally report it or not if it is not set.</span></span> 
  
<span data-ttu-id="1f79c-120">Zum Abrufen von Inhaltsverzeichnisses sollte Clientanwendungen die [IMAPIContainer::GetContentsTable](imapicontainer-getcontentstable.md) -Methode aufrufen.</span><span class="sxs-lookup"><span data-stu-id="1f79c-120">To retrieve table contents, client applications should call the [IMAPIContainer::GetContentsTable](imapicontainer-getcontentstable.md) method.</span></span> <span data-ttu-id="1f79c-121">Weitere Informationen zum Ordner Inhalt Tabellen finden Sie unter [Inhalt Tabellen](contents-tables.md) und [eine Tabelle der Ordner-Inhalt angezeigt](displaying-a-folder-contents-table.md).</span><span class="sxs-lookup"><span data-stu-id="1f79c-121">For more information on folder contents tables, see [Contents Tables](contents-tables.md) and [Displaying a Folder Contents Table](displaying-a-folder-contents-table.md).</span></span> 
  
<span data-ttu-id="1f79c-122">**PR_CONTAINER_CONTENTS** ([PidTagContainerContents](pidtagcontainercontents-canonical-property.md)), **PR_CONTAINER_HIERARCHY** ([PidTagContainerHierarchy](pidtagcontainerhierarchy-canonical-property.md)) und diese Eigenschaft ähneln in Verwendung.</span><span class="sxs-lookup"><span data-stu-id="1f79c-122">The **PR_CONTAINER_CONTENTS** ([PidTagContainerContents](pidtagcontainercontents-canonical-property.md)), **PR_CONTAINER_HIERARCHY** ([PidTagContainerHierarchy](pidtagcontainerhierarchy-canonical-property.md)), and this property are similar in usage.</span></span> <span data-ttu-id="1f79c-123">Mehrere MAPI-Eigenschaften bieten Zugriff auf Tabellen:</span><span class="sxs-lookup"><span data-stu-id="1f79c-123">Several MAPI properties provide access to tables:</span></span> 
  
|<span data-ttu-id="1f79c-124">**Eigenschaft**</span><span class="sxs-lookup"><span data-stu-id="1f79c-124">**Property**</span></span>|<span data-ttu-id="1f79c-125">**Table**</span><span class="sxs-lookup"><span data-stu-id="1f79c-125">**Table**</span></span>|
|:-----|:-----|
|<span data-ttu-id="1f79c-126">**PR_CONTAINER_CONTENTS** ([PidTagContainerContents](pidtagcontainercontents-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="1f79c-126">**PR_CONTAINER_CONTENTS** ([PidTagContainerContents](pidtagcontainercontents-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="1f79c-127">Inhaltstabelle</span><span class="sxs-lookup"><span data-stu-id="1f79c-127">Contents table</span></span>  <br/> |
|<span data-ttu-id="1f79c-128">**PR_CONTAINER_HIERARCHY** ([PidTagContainerHierarchy](pidtagcontainerhierarchy-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="1f79c-128">**PR_CONTAINER_HIERARCHY** ([PidTagContainerHierarchy](pidtagcontainerhierarchy-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="1f79c-129">Hierarchietabelle</span><span class="sxs-lookup"><span data-stu-id="1f79c-129">Hierarchy table</span></span>  <br/> |
|<span data-ttu-id="1f79c-130">**PR_FOLDER_ASSOCIATED_CONTENTS**</span><span class="sxs-lookup"><span data-stu-id="1f79c-130">**PR_FOLDER_ASSOCIATED_CONTENTS**</span></span> <br/> |<span data-ttu-id="1f79c-131">Zugehörige Inhaltstabelle</span><span class="sxs-lookup"><span data-stu-id="1f79c-131">Associated contents table</span></span>  <br/> |
|<span data-ttu-id="1f79c-132">**PR_MESSAGE_ATTACHMENTS** ([PidTagMessageAttachments](pidtagmessageattachments-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="1f79c-132">**PR_MESSAGE_ATTACHMENTS** ([PidTagMessageAttachments](pidtagmessageattachments-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="1f79c-133">Anlagentabelle</span><span class="sxs-lookup"><span data-stu-id="1f79c-133">Attachment table</span></span>  <br/> |
|<span data-ttu-id="1f79c-134">**PR_MESSAGE_RECIPIENTS** ([PidTagMessageRecipients](pidtagmessagerecipients-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="1f79c-134">**PR_MESSAGE_RECIPIENTS** ([PidTagMessageRecipients](pidtagmessagerecipients-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="1f79c-135">Empfänger-Tabelle</span><span class="sxs-lookup"><span data-stu-id="1f79c-135">Recipient table</span></span>  <br/> |
   
## <a name="related-resources"></a><span data-ttu-id="1f79c-136">Verwandte Ressourcen</span><span class="sxs-lookup"><span data-stu-id="1f79c-136">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="1f79c-137">Protokollspezifikationen</span><span class="sxs-lookup"><span data-stu-id="1f79c-137">Protocol specifications</span></span>

<span data-ttu-id="1f79c-138">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="1f79c-138">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="1f79c-139">Bietet Verweise auf Verwandte Exchange Server-Spezifikationen.</span><span class="sxs-lookup"><span data-stu-id="1f79c-139">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="1f79c-140">[[MS-OXCFXICS]](http://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="1f79c-140">[[MS-OXCFXICS]](http://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="1f79c-141">Verarbeitet die Reihenfolge und den Fluss für Datenübertragungen zwischen einem Client und Server.</span><span class="sxs-lookup"><span data-stu-id="1f79c-141">Handles the order and flow for data transfers between a client and server.</span></span>
    
<span data-ttu-id="1f79c-142">[[MS-OXCICAL]](http://msdn.microsoft.com/library/a685a040-5b69-4c84-b084-795113fb4012%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="1f79c-142">[[MS-OXCICAL]](http://msdn.microsoft.com/library/a685a040-5b69-4c84-b084-795113fb4012%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="1f79c-143">Konvertiert zwischen IETF RFC2445, RFC2446, RFC2447, und Termine und Besprechungsanfragen.</span><span class="sxs-lookup"><span data-stu-id="1f79c-143">Converts between IETF RFC2445, RFC2446, and RFC2447, and appointment and meeting items.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="1f79c-144">Header-Dateien</span><span class="sxs-lookup"><span data-stu-id="1f79c-144">Header files</span></span>

<span data-ttu-id="1f79c-145">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="1f79c-145">Mapidefs.h</span></span>
  
> <span data-ttu-id="1f79c-146">Enthält die Datentypdefinitionen.</span><span class="sxs-lookup"><span data-stu-id="1f79c-146">Provides data type definitions.</span></span>
    
<span data-ttu-id="1f79c-147">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="1f79c-147">Mapitags.h</span></span>
  
> <span data-ttu-id="1f79c-148">Enthält Definitionen von Eigenschaften, die als Alternative Namen aufgelistet.</span><span class="sxs-lookup"><span data-stu-id="1f79c-148">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="1f79c-149">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="1f79c-149">See also</span></span>



[<span data-ttu-id="1f79c-150">PidTagAssociatedContentCount (kanonische Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="1f79c-150">PidTagAssociatedContentCount Canonical Property</span></span>](pidtagassociatedcontentcount-canonical-property.md)


[<span data-ttu-id="1f79c-151">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="1f79c-151">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="1f79c-152">Kanonische MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="1f79c-152">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="1f79c-153">Zuordnen von kanonischen Eigenschaftennamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="1f79c-153">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="1f79c-154">Zuordnen von MAPI-Namen zu kanonische Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="1f79c-154">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

