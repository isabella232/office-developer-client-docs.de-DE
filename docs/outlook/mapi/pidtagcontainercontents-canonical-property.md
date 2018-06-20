---
title: Kanonische PidTagContainerContents-Eigenschaft
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
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: c2979a0825ad6c62dbbb7931255501e90d8450a5
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19794216"
---
# <a name="pidtagcontainercontents-canonical-property"></a><span data-ttu-id="488ec-103">Kanonische PidTagContainerContents-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="488ec-103">PidTagContainerContents Canonical Property</span></span>

  
  
<span data-ttu-id="488ec-104">**Betrifft**: Outlook</span><span class="sxs-lookup"><span data-stu-id="488ec-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="488ec-105">Enthält eine eingebettete Inhalt Table-Objekt, das Informationen über einem Container bereitstellt.</span><span class="sxs-lookup"><span data-stu-id="488ec-105">Contains an embedded contents table object that provides information about a container.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="488ec-106">Zugeordneten Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="488ec-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="488ec-107">PR_CONTAINER_CONTENTS</span><span class="sxs-lookup"><span data-stu-id="488ec-107">PR_CONTAINER_CONTENTS</span></span>  <br/> |
|<span data-ttu-id="488ec-108">Bezeichner:</span><span class="sxs-lookup"><span data-stu-id="488ec-108">Identifier:</span></span>  <br/> |<span data-ttu-id="488ec-109">0x360F</span><span class="sxs-lookup"><span data-stu-id="488ec-109">0x360F</span></span>  <br/> |
|<span data-ttu-id="488ec-110">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="488ec-110">Data type:</span></span>  <br/> |<span data-ttu-id="488ec-111">PT_OBJECT</span><span class="sxs-lookup"><span data-stu-id="488ec-111">PT_OBJECT</span></span>  <br/> |
|<span data-ttu-id="488ec-112">Bereich:</span><span class="sxs-lookup"><span data-stu-id="488ec-112">Area:</span></span>  <br/> |<span data-ttu-id="488ec-113">Container</span><span class="sxs-lookup"><span data-stu-id="488ec-113">Container</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="488ec-114">Hinweise</span><span class="sxs-lookup"><span data-stu-id="488ec-114">Remarks</span></span>

<span data-ttu-id="488ec-115">Diese Eigenschaft kann in [IMAPIProp::CopyTo](imapiprop-copyto.md) Vorgänge aus- oder in [IMAPIProp::CopyProps](imapiprop-copyprops.md) Vorgänge eingeschlossen werden.</span><span class="sxs-lookup"><span data-stu-id="488ec-115">This property can be excluded in [IMAPIProp::CopyTo](imapiprop-copyto.md) operations or included in [IMAPIProp::CopyProps](imapiprop-copyprops.md) operations.</span></span> <span data-ttu-id="488ec-116">Als Eigenschaft vom Typ PT_OBJECT kann nicht es erfolgreich von der [IMAPIProp::GetProps](imapiprop-getprops.md) -Methode abgerufen werden. von der [IMAPIProp::OpenProperty](imapiprop-openproperty.md) -Methode der IID_IMAPITable Identifier anfordern sollte seinen Inhalt zugegriffen werden.</span><span class="sxs-lookup"><span data-stu-id="488ec-116">As a property of type PT_OBJECT, it cannot be successfully retrieved by the [IMAPIProp::GetProps](imapiprop-getprops.md) method; its contents should be accessed by the [IMAPIProp::OpenProperty](imapiprop-openproperty.md) method, requesting the IID_IMAPITable interface identifier.</span></span> <span data-ttu-id="488ec-117">Dienstanbieter müssen es an die [IMAPIProp::GetPropList](imapiprop-getproplist.md) -Methode melden, wenn er festgelegt ist, jedoch kann positives oder nicht, wenn sie nicht festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="488ec-117">Service providers must report it to the [IMAPIProp::GetPropList](imapiprop-getproplist.md) method if it is set, but can optionally report it or not if it is not set.</span></span> 
  
<span data-ttu-id="488ec-118">Zum Abrufen von Inhaltsverzeichnisses sollte eine Clientanwendung die [IMAPIContainer::GetContentsTable](imapicontainer-getcontentstable.md) -Methode aufrufen.</span><span class="sxs-lookup"><span data-stu-id="488ec-118">To retrieve table contents, a client application should call the [IMAPIContainer::GetContentsTable](imapicontainer-getcontentstable.md) method.</span></span> <span data-ttu-id="488ec-119">For more information, see [Inhalt von Tabellen](contents-tables.md).</span><span class="sxs-lookup"><span data-stu-id="488ec-119">For more information, see [Contents Tables](contents-tables.md).</span></span> 
  
<span data-ttu-id="488ec-120">Diese Eigenschaft, **PR_CONTAINER_HIERARCHY** ([PidTagContainerHierarchy](pidtagcontainerhierarchy-canonical-property.md)) und **PR_FOLDER_ASSOCIATED_CONTENTS** ([PidTagFolderAssociatedContents](pidtagfolderassociatedcontents-canonical-property.md)) ähneln in Verwendung.</span><span class="sxs-lookup"><span data-stu-id="488ec-120">This property, **PR_CONTAINER_HIERARCHY** ([PidTagContainerHierarchy](pidtagcontainerhierarchy-canonical-property.md)) , and **PR_FOLDER_ASSOCIATED_CONTENTS** ([PidTagFolderAssociatedContents](pidtagfolderassociatedcontents-canonical-property.md)) are similar in usage.</span></span> <span data-ttu-id="488ec-121">Mehrere MAPI-Eigenschaften bieten Zugriff auf Tabellen:</span><span class="sxs-lookup"><span data-stu-id="488ec-121">Several MAPI properties provide access to tables:</span></span> 
  
|<span data-ttu-id="488ec-122">**Eigenschaft**</span><span class="sxs-lookup"><span data-stu-id="488ec-122">**Property**</span></span>|<span data-ttu-id="488ec-123">**Table**</span><span class="sxs-lookup"><span data-stu-id="488ec-123">**Table**</span></span>|
|:-----|:-----|
|<span data-ttu-id="488ec-124">PidTagContainerContents</span><span class="sxs-lookup"><span data-stu-id="488ec-124">PidTagContainerContents</span></span>  <br/> |<span data-ttu-id="488ec-125">Inhaltstabelle</span><span class="sxs-lookup"><span data-stu-id="488ec-125">Contents table</span></span>  <br/> |
|<span data-ttu-id="488ec-126">**PR_CONTAINER_HIERARCHY** ([PidTagContainerHierarchy](pidtagcontainerhierarchy-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="488ec-126">**PR_CONTAINER_HIERARCHY** ([PidTagContainerHierarchy](pidtagcontainerhierarchy-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="488ec-127">Hierarchietabelle</span><span class="sxs-lookup"><span data-stu-id="488ec-127">Hierarchy table</span></span>  <br/> |
|<span data-ttu-id="488ec-128">**PR_FOLDER_ASSOCIATED_CONTENTS** ([PidTagFolderAssociatedContents](pidtagfolderassociatedcontents-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="488ec-128">**PR_FOLDER_ASSOCIATED_CONTENTS** ([PidTagFolderAssociatedContents](pidtagfolderassociatedcontents-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="488ec-129">Zugehörige Inhaltstabelle</span><span class="sxs-lookup"><span data-stu-id="488ec-129">Associated contents table</span></span>  <br/> |
|<span data-ttu-id="488ec-130">**PR_MESSAGE_ATTACHMENTS** ([PidTagMessageAttachments](pidtagmessageattachments-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="488ec-130">**PR_MESSAGE_ATTACHMENTS** ([PidTagMessageAttachments](pidtagmessageattachments-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="488ec-131">Anlagentabelle</span><span class="sxs-lookup"><span data-stu-id="488ec-131">Attachment table</span></span>  <br/> |
|<span data-ttu-id="488ec-132">**PR_MESSAGE_RECIPIENTS** ([PidTagMessageRecipients](pidtagmessagerecipients-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="488ec-132">**PR_MESSAGE_RECIPIENTS** ([PidTagMessageRecipients](pidtagmessagerecipients-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="488ec-133">Empfänger-Tabelle</span><span class="sxs-lookup"><span data-stu-id="488ec-133">Recipient table</span></span>  <br/> |
   
## <a name="related-resources"></a><span data-ttu-id="488ec-134">Verwandte Ressourcen</span><span class="sxs-lookup"><span data-stu-id="488ec-134">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="488ec-135">Protokollspezifikationen</span><span class="sxs-lookup"><span data-stu-id="488ec-135">Protocol specifications</span></span>

<span data-ttu-id="488ec-136">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="488ec-136">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="488ec-137">Bietet Verweise auf Verwandte Exchange Server-Spezifikationen.</span><span class="sxs-lookup"><span data-stu-id="488ec-137">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="488ec-138">[[MS-OXOABK]](http://msdn.microsoft.com/library/f4cf9b4c-9232-4506-9e71-2270de217614%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="488ec-138">[[MS-OXOABK]](http://msdn.microsoft.com/library/f4cf9b4c-9232-4506-9e71-2270de217614%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="488ec-139">Gibt die Eigenschaften und Operationen für Listen der Benutzer, Kontakte, Gruppen und Ressourcen.</span><span class="sxs-lookup"><span data-stu-id="488ec-139">Specifies the properties and operations for lists of users, contacts, groups, and resources.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="488ec-140">Header-Dateien</span><span class="sxs-lookup"><span data-stu-id="488ec-140">Header files</span></span>

<span data-ttu-id="488ec-141">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="488ec-141">Mapidefs.h</span></span>
  
> <span data-ttu-id="488ec-142">Enthält die Datentypdefinitionen.</span><span class="sxs-lookup"><span data-stu-id="488ec-142">Provides data type definitions.</span></span>
    
<span data-ttu-id="488ec-143">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="488ec-143">Mapitags.h</span></span>
  
> <span data-ttu-id="488ec-144">Enthält Definitionen von Eigenschaften, die als Alternative Namen aufgelistet.</span><span class="sxs-lookup"><span data-stu-id="488ec-144">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="488ec-145">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="488ec-145">See also</span></span>



[<span data-ttu-id="488ec-146">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="488ec-146">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="488ec-147">Kanonische MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="488ec-147">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="488ec-148">Zuordnen von kanonischen Eigenschaftennamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="488ec-148">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="488ec-149">Zuordnen von MAPI-Namen zu kanonische Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="488ec-149">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

