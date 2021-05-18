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
ms.openlocfilehash: c85c5d7c3e80508c4d328f69ac4ad15f0f2c355a
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32316303"
---
# <a name="pidtagfolderassociatedcontents-canonical-property"></a><span data-ttu-id="121df-103">PidTagFolderAssociatedContents (kanonische Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="121df-103">PidTagFolderAssociatedContents Canonical Property</span></span>

  
  
<span data-ttu-id="121df-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="121df-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="121df-105">Enthält ein eingebettetes Inhaltstabellesobjekt, das Informationen zur zugeordneten Inhaltstabelle enthält.</span><span class="sxs-lookup"><span data-stu-id="121df-105">Contains an embedded contents table object that provides information about the associated contents table.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="121df-106">Zugeordnete Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="121df-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="121df-107">PR_FOLDER_ASSOCIATED_CONTENTS</span><span class="sxs-lookup"><span data-stu-id="121df-107">PR_FOLDER_ASSOCIATED_CONTENTS</span></span>  <br/> |
|<span data-ttu-id="121df-108">Kennung:</span><span class="sxs-lookup"><span data-stu-id="121df-108">Identifier:</span></span>  <br/> |<span data-ttu-id="121df-109">0x3610</span><span class="sxs-lookup"><span data-stu-id="121df-109">0x3610</span></span>  <br/> |
|<span data-ttu-id="121df-110">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="121df-110">Data type:</span></span>  <br/> |<span data-ttu-id="121df-111">PT_OBJECT</span><span class="sxs-lookup"><span data-stu-id="121df-111">PT_OBJECT</span></span>  <br/> |
|<span data-ttu-id="121df-112">Bereich:</span><span class="sxs-lookup"><span data-stu-id="121df-112">Area:</span></span>  <br/> |<span data-ttu-id="121df-113">MAPI-Container</span><span class="sxs-lookup"><span data-stu-id="121df-113">MAPI container</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="121df-114">Hinweise</span><span class="sxs-lookup"><span data-stu-id="121df-114">Remarks</span></span>

<span data-ttu-id="121df-115">Die zugeordnete Inhaltstabelle stellt einen Unterordner dar, der nicht in der Standardinhaltstabelle angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="121df-115">The associated contents table represents a subfolder that does not appear in the standard contents table.</span></span> <span data-ttu-id="121df-116">Er enthält die zugeordneten oder ausgeblendeten Nachrichten des Ordners.</span><span class="sxs-lookup"><span data-stu-id="121df-116">It contains the folder's associated, or hidden, messages.</span></span> 
  
<span data-ttu-id="121df-117">Diese Eigenschaft kann in [IMAPIProp::CopyTo-Vorgängen](imapiprop-copyto.md) ausgeschlossen oder in [IMAPIProp::CopyProps-Vorgängen enthalten](imapiprop-copyprops.md) sein.</span><span class="sxs-lookup"><span data-stu-id="121df-117">This property can be excluded in [IMAPIProp::CopyTo](imapiprop-copyto.md) operations or included in [IMAPIProp::CopyProps](imapiprop-copyprops.md) operations.</span></span> <span data-ttu-id="121df-118">Als Eigenschaft vom Typ **PT_OBJECT** kann sie nicht erfolgreich von der [IMAPIProp::GetProps-Methode abgerufen](imapiprop-getprops.md) werden. Der Zugriff auf den Inhalt sollte über die [IMAPIProp::OpenProperty-Methode](imapiprop-openproperty.md) erfolgen, die den IID_IMAPITable  anfordert.</span><span class="sxs-lookup"><span data-stu-id="121df-118">As a property of type **PT_OBJECT**, it cannot be successfully retrieved by the [IMAPIProp::GetProps](imapiprop-getprops.md) method; its contents should be accessed by the [IMAPIProp::OpenProperty](imapiprop-openproperty.md) method, requesting the **IID_IMAPITable** interface identifier.</span></span> <span data-ttu-id="121df-119">Dienstanbieter müssen sie der [IMAPIProp::GetPropList-Methode](imapiprop-getproplist.md) melden, wenn sie festgelegt ist, kann sie jedoch optional melden oder nicht, wenn sie nicht festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="121df-119">Service providers must report it to the [IMAPIProp::GetPropList](imapiprop-getproplist.md) method if it is set, but may optionally report it or not if it is not set.</span></span> 
  
<span data-ttu-id="121df-120">Zum Abrufen von Tabelleninhalten sollten Clientanwendungen die [IMAPIContainer::GetContentsTable-Methode](imapicontainer-getcontentstable.md) aufrufen.</span><span class="sxs-lookup"><span data-stu-id="121df-120">To retrieve table contents, client applications should call the [IMAPIContainer::GetContentsTable](imapicontainer-getcontentstable.md) method.</span></span> <span data-ttu-id="121df-121">Weitere Informationen zu Ordnerinhaltstabellen finden Sie unter [Inhaltstabellen](contents-tables.md) und [Anzeigen einer Ordnerinhaltstabelle](displaying-a-folder-contents-table.md).</span><span class="sxs-lookup"><span data-stu-id="121df-121">For more information on folder contents tables, see [Contents Tables](contents-tables.md) and [Displaying a Folder Contents Table](displaying-a-folder-contents-table.md).</span></span> 
  
<span data-ttu-id="121df-122">Die **PR_CONTAINER_CONTENTS** ([PidTagContainerContents](pidtagcontainercontents-canonical-property.md)), **PR_CONTAINER_HIERARCHY** ([PidTagContainerHierarchy](pidtagcontainerhierarchy-canonical-property.md)) und diese Eigenschaft sind in der Verwendung ähnlich.</span><span class="sxs-lookup"><span data-stu-id="121df-122">The **PR_CONTAINER_CONTENTS** ([PidTagContainerContents](pidtagcontainercontents-canonical-property.md)), **PR_CONTAINER_HIERARCHY** ([PidTagContainerHierarchy](pidtagcontainerhierarchy-canonical-property.md)), and this property are similar in usage.</span></span> <span data-ttu-id="121df-123">Mehrere MAPI-Eigenschaften bieten Zugriff auf Tabellen:</span><span class="sxs-lookup"><span data-stu-id="121df-123">Several MAPI properties provide access to tables:</span></span> 
  
|<span data-ttu-id="121df-124">**Eigenschaft**</span><span class="sxs-lookup"><span data-stu-id="121df-124">**Property**</span></span>|<span data-ttu-id="121df-125">**Table**</span><span class="sxs-lookup"><span data-stu-id="121df-125">**Table**</span></span>|
|:-----|:-----|
|<span data-ttu-id="121df-126">**PR_CONTAINER_CONTENTS** ([PidTagContainerContents](pidtagcontainercontents-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="121df-126">**PR_CONTAINER_CONTENTS** ([PidTagContainerContents](pidtagcontainercontents-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="121df-127">Inhaltstabelle</span><span class="sxs-lookup"><span data-stu-id="121df-127">Contents table</span></span>  <br/> |
|<span data-ttu-id="121df-128">**PR_CONTAINER_HIERARCHY** ([PidTagContainerHierarchy](pidtagcontainerhierarchy-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="121df-128">**PR_CONTAINER_HIERARCHY** ([PidTagContainerHierarchy](pidtagcontainerhierarchy-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="121df-129">Hierarchietabelle</span><span class="sxs-lookup"><span data-stu-id="121df-129">Hierarchy table</span></span>  <br/> |
|<span data-ttu-id="121df-130">**PR_FOLDER_ASSOCIATED_CONTENTS**</span><span class="sxs-lookup"><span data-stu-id="121df-130">**PR_FOLDER_ASSOCIATED_CONTENTS**</span></span> <br/> |<span data-ttu-id="121df-131">Tabelle "Zugeordnete Inhalte"</span><span class="sxs-lookup"><span data-stu-id="121df-131">Associated contents table</span></span>  <br/> |
|<span data-ttu-id="121df-132">**PR_MESSAGE_ATTACHMENTS** ([PidTagMessageAttachments](pidtagmessageattachments-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="121df-132">**PR_MESSAGE_ATTACHMENTS** ([PidTagMessageAttachments](pidtagmessageattachments-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="121df-133">Anlagentabelle</span><span class="sxs-lookup"><span data-stu-id="121df-133">Attachment table</span></span>  <br/> |
|<span data-ttu-id="121df-134">**PR_MESSAGE_RECIPIENTS** ([PidTagMessageRecipients](pidtagmessagerecipients-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="121df-134">**PR_MESSAGE_RECIPIENTS** ([PidTagMessageRecipients](pidtagmessagerecipients-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="121df-135">Empfängertabelle</span><span class="sxs-lookup"><span data-stu-id="121df-135">Recipient table</span></span>  <br/> |
   
## <a name="related-resources"></a><span data-ttu-id="121df-136">Verwandte Ressourcen</span><span class="sxs-lookup"><span data-stu-id="121df-136">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="121df-137">Protokollspezifikationen</span><span class="sxs-lookup"><span data-stu-id="121df-137">Protocol specifications</span></span>

<span data-ttu-id="121df-138">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="121df-138">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="121df-139">Enthält Verweise auf Exchange Server Protokollspezifikationen.</span><span class="sxs-lookup"><span data-stu-id="121df-139">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="121df-140">[[MS-OXCFXICS]](https://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="121df-140">[[MS-OXCFXICS]](https://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="121df-141">Verarbeitet die Reihenfolge und den Fluss für Datenübertragungen zwischen einem Client und einem Server.</span><span class="sxs-lookup"><span data-stu-id="121df-141">Handles the order and flow for data transfers between a client and server.</span></span>
    
<span data-ttu-id="121df-142">[[MS-OXCICAL]](https://msdn.microsoft.com/library/a685a040-5b69-4c84-b084-795113fb4012%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="121df-142">[[MS-OXCICAL]](https://msdn.microsoft.com/library/a685a040-5b69-4c84-b084-795113fb4012%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="121df-143">Konvertiert zwischen IETF RFC2445, RFC2446 und RFC2447 sowie Termin- und Besprechungselementen.</span><span class="sxs-lookup"><span data-stu-id="121df-143">Converts between IETF RFC2445, RFC2446, and RFC2447, and appointment and meeting items.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="121df-144">Headerdateien</span><span class="sxs-lookup"><span data-stu-id="121df-144">Header files</span></span>

<span data-ttu-id="121df-145">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="121df-145">Mapidefs.h</span></span>
  
> <span data-ttu-id="121df-146">Bietet Datentypdefinitionen.</span><span class="sxs-lookup"><span data-stu-id="121df-146">Provides data type definitions.</span></span>
    
<span data-ttu-id="121df-147">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="121df-147">Mapitags.h</span></span>
  
> <span data-ttu-id="121df-148">Enthält Definitionen von Eigenschaften, die als alternative Namen aufgeführt sind.</span><span class="sxs-lookup"><span data-stu-id="121df-148">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="121df-149">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="121df-149">See also</span></span>



[<span data-ttu-id="121df-150">PidTagAssociatedContentCount (kanonische Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="121df-150">PidTagAssociatedContentCount Canonical Property</span></span>](pidtagassociatedcontentcount-canonical-property.md)


[<span data-ttu-id="121df-151">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="121df-151">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="121df-152">KANONISCHE EIGENSCHAFTEN VON MAPI</span><span class="sxs-lookup"><span data-stu-id="121df-152">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="121df-153">Zuordnen kanonischer Eigenschaftsnamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="121df-153">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="121df-154">Zuordnen von MAPI-Namen zu kanonischen Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="121df-154">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

