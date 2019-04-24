---
title: Kanonische Pidtagfolderassociatedcontents (-Eigenschaft
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
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: c85c5d7c3e80508c4d328f69ac4ad15f0f2c355a
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32316303"
---
# <a name="pidtagfolderassociatedcontents-canonical-property"></a><span data-ttu-id="e7204-103">Kanonische Pidtagfolderassociatedcontents (-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="e7204-103">PidTagFolderAssociatedContents Canonical Property</span></span>

  
  
<span data-ttu-id="e7204-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="e7204-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="e7204-105">Enthält ein Table-Objekt mit eingebetteten Inhalten, das Informationen zur zugeordneten Inhaltstabelle bereitstellt.</span><span class="sxs-lookup"><span data-stu-id="e7204-105">Contains an embedded contents table object that provides information about the associated contents table.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="e7204-106">Zugeordnete Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="e7204-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="e7204-107">PR_FOLDER_ASSOCIATED_CONTENTS</span><span class="sxs-lookup"><span data-stu-id="e7204-107">PR_FOLDER_ASSOCIATED_CONTENTS</span></span>  <br/> |
|<span data-ttu-id="e7204-108">Kennung:</span><span class="sxs-lookup"><span data-stu-id="e7204-108">Identifier:</span></span>  <br/> |<span data-ttu-id="e7204-109">0x3610</span><span class="sxs-lookup"><span data-stu-id="e7204-109">0x3610</span></span>  <br/> |
|<span data-ttu-id="e7204-110">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="e7204-110">Data type:</span></span>  <br/> |<span data-ttu-id="e7204-111">PT_OBJECT</span><span class="sxs-lookup"><span data-stu-id="e7204-111">PT_OBJECT</span></span>  <br/> |
|<span data-ttu-id="e7204-112">Bereich:</span><span class="sxs-lookup"><span data-stu-id="e7204-112">Area:</span></span>  <br/> |<span data-ttu-id="e7204-113">MAPI-Container</span><span class="sxs-lookup"><span data-stu-id="e7204-113">MAPI container</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="e7204-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="e7204-114">Remarks</span></span>

<span data-ttu-id="e7204-115">Die Tabelle zugeordnete Inhalte stellt einen Unterordner dar, der nicht in der Tabelle mit den Standardinhalten angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="e7204-115">The associated contents table represents a subfolder that does not appear in the standard contents table.</span></span> <span data-ttu-id="e7204-116">Sie enthält die zugeordneten oder ausgeblendeten Nachrichten des Ordners.</span><span class="sxs-lookup"><span data-stu-id="e7204-116">It contains the folder's associated, or hidden, messages.</span></span> 
  
<span data-ttu-id="e7204-117">Diese Eigenschaft kann in [IMAPIProp:: CopyTo](imapiprop-copyto.md) -Vorgängen oder in [IMAPIProp:: CopyProps](imapiprop-copyprops.md) -Vorgängen ausgeschlossen werden.</span><span class="sxs-lookup"><span data-stu-id="e7204-117">This property can be excluded in [IMAPIProp::CopyTo](imapiprop-copyto.md) operations or included in [IMAPIProp::CopyProps](imapiprop-copyprops.md) operations.</span></span> <span data-ttu-id="e7204-118">Als Eigenschaft vom Typ **PT_OBJECT**kann Sie nicht erfolgreich von der [IMAPIProp::](imapiprop-getprops.md) GetProps-Methode abgerufen werden; auf den Inhalt sollte von der [IMAPIProp:: OpenProperty](imapiprop-openproperty.md) -Methode zugegriffen werden, um den **IID_IMAPITable** -Schnittstellenbezeichner anzufordern.</span><span class="sxs-lookup"><span data-stu-id="e7204-118">As a property of type **PT_OBJECT**, it cannot be successfully retrieved by the [IMAPIProp::GetProps](imapiprop-getprops.md) method; its contents should be accessed by the [IMAPIProp::OpenProperty](imapiprop-openproperty.md) method, requesting the **IID_IMAPITable** interface identifier.</span></span> <span data-ttu-id="e7204-119">Dienstanbieter müssen Sie an die [IMAPIProp::](imapiprop-getproplist.md) getproplist-Methode melden, wenn Sie festgelegt ist, aber Sie kann Sie optional melden oder nicht, wenn Sie nicht festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="e7204-119">Service providers must report it to the [IMAPIProp::GetPropList](imapiprop-getproplist.md) method if it is set, but may optionally report it or not if it is not set.</span></span> 
  
<span data-ttu-id="e7204-120">Zum Abrufen von Tabelleninhalten sollten Clientanwendungen die [IMAPIContainer::](imapicontainer-getcontentstable.md) getcontentable-Methode aufrufen.</span><span class="sxs-lookup"><span data-stu-id="e7204-120">To retrieve table contents, client applications should call the [IMAPIContainer::GetContentsTable](imapicontainer-getcontentstable.md) method.</span></span> <span data-ttu-id="e7204-121">Weitere Informationen zu Ordnerinhaltstabellen finden Sie unter [Inhaltstabellen](contents-tables.md) und [Anzeigen einer Ordnerinhaltstabelle](displaying-a-folder-contents-table.md).</span><span class="sxs-lookup"><span data-stu-id="e7204-121">For more information on folder contents tables, see [Contents Tables](contents-tables.md) and [Displaying a Folder Contents Table](displaying-a-folder-contents-table.md).</span></span> 
  
<span data-ttu-id="e7204-122">Die **PR_CONTAINER_CONTENTS** ([Pidtagcontainercontents (](pidtagcontainercontents-canonical-property.md)), **PR_CONTAINER_HIERARCHY** ([Pidtagcontainerhierarchy (](pidtagcontainerhierarchy-canonical-property.md)) und diese Eigenschaft ähneln der Verwendung.</span><span class="sxs-lookup"><span data-stu-id="e7204-122">The **PR_CONTAINER_CONTENTS** ([PidTagContainerContents](pidtagcontainercontents-canonical-property.md)), **PR_CONTAINER_HIERARCHY** ([PidTagContainerHierarchy](pidtagcontainerhierarchy-canonical-property.md)), and this property are similar in usage.</span></span> <span data-ttu-id="e7204-123">Mehrere MAPI-Eigenschaften bieten Zugriff auf Tabellen:</span><span class="sxs-lookup"><span data-stu-id="e7204-123">Several MAPI properties provide access to tables:</span></span> 
  
|<span data-ttu-id="e7204-124">**Eigenschaft**</span><span class="sxs-lookup"><span data-stu-id="e7204-124">**Property**</span></span>|<span data-ttu-id="e7204-125">**Table**</span><span class="sxs-lookup"><span data-stu-id="e7204-125">**Table**</span></span>|
|:-----|:-----|
|<span data-ttu-id="e7204-126">**PR_CONTAINER_CONTENTS** ([Pidtagcontainercontents (](pidtagcontainercontents-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="e7204-126">**PR_CONTAINER_CONTENTS** ([PidTagContainerContents](pidtagcontainercontents-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="e7204-127">Inhaltstabelle</span><span class="sxs-lookup"><span data-stu-id="e7204-127">Contents table</span></span>  <br/> |
|<span data-ttu-id="e7204-128">**PR_CONTAINER_HIERARCHY** ([Pidtagcontainerhierarchy (](pidtagcontainerhierarchy-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="e7204-128">**PR_CONTAINER_HIERARCHY** ([PidTagContainerHierarchy](pidtagcontainerhierarchy-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="e7204-129">Hierarchietabelle</span><span class="sxs-lookup"><span data-stu-id="e7204-129">Hierarchy table</span></span>  <br/> |
|<span data-ttu-id="e7204-130">**PR_FOLDER_ASSOCIATED_CONTENTS**</span><span class="sxs-lookup"><span data-stu-id="e7204-130">**PR_FOLDER_ASSOCIATED_CONTENTS**</span></span> <br/> |<span data-ttu-id="e7204-131">Tabelle mit zugeordneten Inhalten</span><span class="sxs-lookup"><span data-stu-id="e7204-131">Associated contents table</span></span>  <br/> |
|<span data-ttu-id="e7204-132">**PR_MESSAGE_ATTACHMENTS** ([Pidtagmessageattachments (](pidtagmessageattachments-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="e7204-132">**PR_MESSAGE_ATTACHMENTS** ([PidTagMessageAttachments](pidtagmessageattachments-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="e7204-133">Attachment-Tabelle</span><span class="sxs-lookup"><span data-stu-id="e7204-133">Attachment table</span></span>  <br/> |
|<span data-ttu-id="e7204-134">**PR_MESSAGE_RECIPIENTS** ([Pidtagmessagerecipients (](pidtagmessagerecipients-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="e7204-134">**PR_MESSAGE_RECIPIENTS** ([PidTagMessageRecipients](pidtagmessagerecipients-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="e7204-135">Empfängertabelle</span><span class="sxs-lookup"><span data-stu-id="e7204-135">Recipient table</span></span>  <br/> |
   
## <a name="related-resources"></a><span data-ttu-id="e7204-136">Zugehörige Ressourcen</span><span class="sxs-lookup"><span data-stu-id="e7204-136">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="e7204-137">Protokollspezifikationen</span><span class="sxs-lookup"><span data-stu-id="e7204-137">Protocol specifications</span></span>

<span data-ttu-id="e7204-138">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="e7204-138">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="e7204-139">Enthält Verweise auf zugehörige Exchange Server-Protokollspezifikationen.</span><span class="sxs-lookup"><span data-stu-id="e7204-139">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="e7204-140">[[MS-OXCFXICS]](https://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="e7204-140">[[MS-OXCFXICS]](https://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="e7204-141">Verarbeitet die Reihenfolge und den Ablauf für die Datenübertragung zwischen einem Client und einem Server.</span><span class="sxs-lookup"><span data-stu-id="e7204-141">Handles the order and flow for data transfers between a client and server.</span></span>
    
<span data-ttu-id="e7204-142">[[MS-OXCICAL]](https://msdn.microsoft.com/library/a685a040-5b69-4c84-b084-795113fb4012%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="e7204-142">[[MS-OXCICAL]](https://msdn.microsoft.com/library/a685a040-5b69-4c84-b084-795113fb4012%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="e7204-143">Konvertiert zwischen IETF-RFC2445, RFC2446 und RFC2447 sowie Termin-und Besprechungselementen.</span><span class="sxs-lookup"><span data-stu-id="e7204-143">Converts between IETF RFC2445, RFC2446, and RFC2447, and appointment and meeting items.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="e7204-144">Header Dateien</span><span class="sxs-lookup"><span data-stu-id="e7204-144">Header files</span></span>

<span data-ttu-id="e7204-145">Mapidefs. h</span><span class="sxs-lookup"><span data-stu-id="e7204-145">Mapidefs.h</span></span>
  
> <span data-ttu-id="e7204-146">Stellt Datentypdefinitionen bereit.</span><span class="sxs-lookup"><span data-stu-id="e7204-146">Provides data type definitions.</span></span>
    
<span data-ttu-id="e7204-147">Mapitags. h</span><span class="sxs-lookup"><span data-stu-id="e7204-147">Mapitags.h</span></span>
  
> <span data-ttu-id="e7204-148">Enthält Definitionen von Eigenschaften, die als Alternative Namen aufgeführt sind.</span><span class="sxs-lookup"><span data-stu-id="e7204-148">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="e7204-149">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="e7204-149">See also</span></span>



[<span data-ttu-id="e7204-150">Kanonische Pidtagassociatedcontentcount (-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="e7204-150">PidTagAssociatedContentCount Canonical Property</span></span>](pidtagassociatedcontentcount-canonical-property.md)


[<span data-ttu-id="e7204-151">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="e7204-151">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="e7204-152">Kanonische MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="e7204-152">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="e7204-153">Zuordnen von kanonischen Eigenschaftennamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="e7204-153">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="e7204-154">Zuordnen von MAPI-Namen zu kanonischen Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="e7204-154">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

