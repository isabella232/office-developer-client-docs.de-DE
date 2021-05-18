---
title: PidTagContainerContents (kanonische Eigenschaft)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagContainerContents
api_type:
- HeaderDef
ms.assetid: 66dbe65a-b9fd-41d5-946f-ec8888363043
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 5f0717c2a6def6f99f1e53217764e8820125b79d
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32283128"
---
# <a name="pidtagcontainercontents-canonical-property"></a><span data-ttu-id="24074-103">PidTagContainerContents (kanonische Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="24074-103">PidTagContainerContents Canonical Property</span></span>

  
  
<span data-ttu-id="24074-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="24074-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="24074-105">Enthält ein eingebettetes Inhalts-Tabellenobjekt, das Informationen zu einem Container enthält.</span><span class="sxs-lookup"><span data-stu-id="24074-105">Contains an embedded contents table object that provides information about a container.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="24074-106">Zugeordnete Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="24074-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="24074-107">PR_CONTAINER_CONTENTS</span><span class="sxs-lookup"><span data-stu-id="24074-107">PR_CONTAINER_CONTENTS</span></span>  <br/> |
|<span data-ttu-id="24074-108">Kennung:</span><span class="sxs-lookup"><span data-stu-id="24074-108">Identifier:</span></span>  <br/> |<span data-ttu-id="24074-109">0x360F</span><span class="sxs-lookup"><span data-stu-id="24074-109">0x360F</span></span>  <br/> |
|<span data-ttu-id="24074-110">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="24074-110">Data type:</span></span>  <br/> |<span data-ttu-id="24074-111">PT_OBJECT</span><span class="sxs-lookup"><span data-stu-id="24074-111">PT_OBJECT</span></span>  <br/> |
|<span data-ttu-id="24074-112">Bereich:</span><span class="sxs-lookup"><span data-stu-id="24074-112">Area:</span></span>  <br/> |<span data-ttu-id="24074-113">Container</span><span class="sxs-lookup"><span data-stu-id="24074-113">Container</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="24074-114">Hinweise</span><span class="sxs-lookup"><span data-stu-id="24074-114">Remarks</span></span>

<span data-ttu-id="24074-115">Diese Eigenschaft kann in [IMAPIProp::CopyTo-Vorgängen](imapiprop-copyto.md) ausgeschlossen oder in [IMAPIProp::CopyProps-Vorgängen enthalten](imapiprop-copyprops.md) sein.</span><span class="sxs-lookup"><span data-stu-id="24074-115">This property can be excluded in [IMAPIProp::CopyTo](imapiprop-copyto.md) operations or included in [IMAPIProp::CopyProps](imapiprop-copyprops.md) operations.</span></span> <span data-ttu-id="24074-116">Als Eigenschaft vom Typ PT_OBJECT kann sie nicht erfolgreich von der [IMAPIProp::GetProps-Methode abgerufen](imapiprop-getprops.md) werden. Der Zugriff auf den Inhalt sollte über die [IMAPIProp::OpenProperty-Methode](imapiprop-openproperty.md) erfolgen, die den IID_IMAPITable anfordert.</span><span class="sxs-lookup"><span data-stu-id="24074-116">As a property of type PT_OBJECT, it cannot be successfully retrieved by the [IMAPIProp::GetProps](imapiprop-getprops.md) method; its contents should be accessed by the [IMAPIProp::OpenProperty](imapiprop-openproperty.md) method, requesting the IID_IMAPITable interface identifier.</span></span> <span data-ttu-id="24074-117">Dienstanbieter müssen sie der [IMAPIProp::GetPropList-Methode](imapiprop-getproplist.md) melden, wenn sie festgelegt ist, können sie jedoch optional melden oder nicht, wenn sie nicht festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="24074-117">Service providers must report it to the [IMAPIProp::GetPropList](imapiprop-getproplist.md) method if it is set, but can optionally report it or not if it is not set.</span></span> 
  
<span data-ttu-id="24074-118">Zum Abrufen von Tabelleninhalten sollte eine Clientanwendung die [IMAPIContainer::GetContentsTable-Methode](imapicontainer-getcontentstable.md) aufrufen.</span><span class="sxs-lookup"><span data-stu-id="24074-118">To retrieve table contents, a client application should call the [IMAPIContainer::GetContentsTable](imapicontainer-getcontentstable.md) method.</span></span> <span data-ttu-id="24074-119">For more information, see [Inhalt von Tabellen](contents-tables.md).</span><span class="sxs-lookup"><span data-stu-id="24074-119">For more information, see [Contents Tables](contents-tables.md).</span></span> 
  
<span data-ttu-id="24074-120">Diese Eigenschaft, **PR_CONTAINER_HIERARCHY** ([PidTagContainerHierarchy](pidtagcontainerhierarchy-canonical-property.md)) und **PR_FOLDER_ASSOCIATED_CONTENTS** ([PidTagFolderAssociatedContents](pidtagfolderassociatedcontents-canonical-property.md)) sind in der Verwendung ähnlich.</span><span class="sxs-lookup"><span data-stu-id="24074-120">This property, **PR_CONTAINER_HIERARCHY** ([PidTagContainerHierarchy](pidtagcontainerhierarchy-canonical-property.md)) , and **PR_FOLDER_ASSOCIATED_CONTENTS** ([PidTagFolderAssociatedContents](pidtagfolderassociatedcontents-canonical-property.md)) are similar in usage.</span></span> <span data-ttu-id="24074-121">Mehrere MAPI-Eigenschaften bieten Zugriff auf Tabellen:</span><span class="sxs-lookup"><span data-stu-id="24074-121">Several MAPI properties provide access to tables:</span></span> 
  
|<span data-ttu-id="24074-122">**Eigenschaft**</span><span class="sxs-lookup"><span data-stu-id="24074-122">**Property**</span></span>|<span data-ttu-id="24074-123">**Table**</span><span class="sxs-lookup"><span data-stu-id="24074-123">**Table**</span></span>|
|:-----|:-----|
|<span data-ttu-id="24074-124">PidTagContainerContents</span><span class="sxs-lookup"><span data-stu-id="24074-124">PidTagContainerContents</span></span>  <br/> |<span data-ttu-id="24074-125">Inhaltstabelle</span><span class="sxs-lookup"><span data-stu-id="24074-125">Contents table</span></span>  <br/> |
|<span data-ttu-id="24074-126">**PR_CONTAINER_HIERARCHY** ([PidTagContainerHierarchy](pidtagcontainerhierarchy-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="24074-126">**PR_CONTAINER_HIERARCHY** ([PidTagContainerHierarchy](pidtagcontainerhierarchy-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="24074-127">Hierarchietabelle</span><span class="sxs-lookup"><span data-stu-id="24074-127">Hierarchy table</span></span>  <br/> |
|<span data-ttu-id="24074-128">**PR_FOLDER_ASSOCIATED_CONTENTS** ([PidTagFolderAssociatedContents](pidtagfolderassociatedcontents-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="24074-128">**PR_FOLDER_ASSOCIATED_CONTENTS** ([PidTagFolderAssociatedContents](pidtagfolderassociatedcontents-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="24074-129">Tabelle "Zugeordnete Inhalte"</span><span class="sxs-lookup"><span data-stu-id="24074-129">Associated contents table</span></span>  <br/> |
|<span data-ttu-id="24074-130">**PR_MESSAGE_ATTACHMENTS** ([PidTagMessageAttachments](pidtagmessageattachments-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="24074-130">**PR_MESSAGE_ATTACHMENTS** ([PidTagMessageAttachments](pidtagmessageattachments-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="24074-131">Anlagentabelle</span><span class="sxs-lookup"><span data-stu-id="24074-131">Attachment table</span></span>  <br/> |
|<span data-ttu-id="24074-132">**PR_MESSAGE_RECIPIENTS** ([PidTagMessageRecipients](pidtagmessagerecipients-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="24074-132">**PR_MESSAGE_RECIPIENTS** ([PidTagMessageRecipients](pidtagmessagerecipients-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="24074-133">Empfängertabelle</span><span class="sxs-lookup"><span data-stu-id="24074-133">Recipient table</span></span>  <br/> |
   
## <a name="related-resources"></a><span data-ttu-id="24074-134">Verwandte Ressourcen</span><span class="sxs-lookup"><span data-stu-id="24074-134">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="24074-135">Protokollspezifikationen</span><span class="sxs-lookup"><span data-stu-id="24074-135">Protocol specifications</span></span>

<span data-ttu-id="24074-136">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="24074-136">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="24074-137">Enthält Verweise auf Exchange Server Protokollspezifikationen.</span><span class="sxs-lookup"><span data-stu-id="24074-137">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="24074-138">[[MS-OXOABK]](https://msdn.microsoft.com/library/f4cf9b4c-9232-4506-9e71-2270de217614%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="24074-138">[[MS-OXOABK]](https://msdn.microsoft.com/library/f4cf9b4c-9232-4506-9e71-2270de217614%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="24074-139">Gibt die Eigenschaften und Vorgänge für Listen von Benutzern, Kontakten, Gruppen und Ressourcen an.</span><span class="sxs-lookup"><span data-stu-id="24074-139">Specifies the properties and operations for lists of users, contacts, groups, and resources.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="24074-140">Headerdateien</span><span class="sxs-lookup"><span data-stu-id="24074-140">Header files</span></span>

<span data-ttu-id="24074-141">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="24074-141">Mapidefs.h</span></span>
  
> <span data-ttu-id="24074-142">Bietet Datentypdefinitionen.</span><span class="sxs-lookup"><span data-stu-id="24074-142">Provides data type definitions.</span></span>
    
<span data-ttu-id="24074-143">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="24074-143">Mapitags.h</span></span>
  
> <span data-ttu-id="24074-144">Enthält Definitionen von Eigenschaften, die als alternative Namen aufgeführt sind.</span><span class="sxs-lookup"><span data-stu-id="24074-144">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="24074-145">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="24074-145">See also</span></span>



[<span data-ttu-id="24074-146">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="24074-146">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="24074-147">KANONISCHE EIGENSCHAFTEN VON MAPI</span><span class="sxs-lookup"><span data-stu-id="24074-147">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="24074-148">Zuordnen kanonischer Eigenschaftsnamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="24074-148">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="24074-149">Zuordnen von MAPI-Namen zu kanonischen Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="24074-149">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

