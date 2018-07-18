---
title: PidTagContainerHierarchy (kanonische Eigenschaft)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagContainerHierarchy
api_type:
- HeaderDef
ms.assetid: 6917510d-ca1e-4049-9eab-09313753ecf0
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: 691c5977092b5e2ca6b453209982dd1333a6df89
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19794228"
---
# <a name="pidtagcontainerhierarchy-canonical-property"></a><span data-ttu-id="ac3e5-103">PidTagContainerHierarchy (kanonische Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="ac3e5-103">PidTagContainerHierarchy Canonical Property</span></span>

  
  
<span data-ttu-id="ac3e5-104">**Betrifft**: Outlook</span><span class="sxs-lookup"><span data-stu-id="ac3e5-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="ac3e5-105">Enthält eine eingebettete Hierarchie Table-Objekt, das Informationen über das untergeordnete Container bereitstellt.</span><span class="sxs-lookup"><span data-stu-id="ac3e5-105">Contains an embedded hierarchy table object that provides information about the child containers.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="ac3e5-106">Zugeordneten Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="ac3e5-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="ac3e5-107">PR_CONTAINER_HIERARCHY</span><span class="sxs-lookup"><span data-stu-id="ac3e5-107">PR_CONTAINER_HIERARCHY</span></span>  <br/> |
|<span data-ttu-id="ac3e5-108">Bezeichner:</span><span class="sxs-lookup"><span data-stu-id="ac3e5-108">Identifier:</span></span>  <br/> |<span data-ttu-id="ac3e5-109">0x360E</span><span class="sxs-lookup"><span data-stu-id="ac3e5-109">0x360E</span></span>  <br/> |
|<span data-ttu-id="ac3e5-110">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="ac3e5-110">Data type:</span></span>  <br/> |<span data-ttu-id="ac3e5-111">PT_OBJECT</span><span class="sxs-lookup"><span data-stu-id="ac3e5-111">PT_OBJECT</span></span>  <br/> |
|<span data-ttu-id="ac3e5-112">Bereich:</span><span class="sxs-lookup"><span data-stu-id="ac3e5-112">Area:</span></span>  <br/> |<span data-ttu-id="ac3e5-113">Container</span><span class="sxs-lookup"><span data-stu-id="ac3e5-113">Container</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="ac3e5-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="ac3e5-114">Remarks</span></span>

<span data-ttu-id="ac3e5-115">Diese Eigenschaft kann in [IMAPIProp::CopyTo](imapiprop-copyto.md) Vorgänge aus- oder in [IMAPIProp::CopyProps](imapiprop-copyprops.md) Vorgänge eingeschlossen werden.</span><span class="sxs-lookup"><span data-stu-id="ac3e5-115">This property can be excluded in [IMAPIProp::CopyTo](imapiprop-copyto.md) operations or included in [IMAPIProp::CopyProps](imapiprop-copyprops.md) operations.</span></span> <span data-ttu-id="ac3e5-116">Als Eigenschaft vom Typ **PT_OBJECT**kann nicht es erfolgreich von der [IMAPIProp::GetProps](imapiprop-getprops.md) -Methode abgerufen werden. von der [IMAPIProp::OpenProperty](imapiprop-openproperty.md) -Methode der IID_IMAPITable Identifier anfordern sollte seinen Inhalt zugegriffen werden.</span><span class="sxs-lookup"><span data-stu-id="ac3e5-116">As a property of type **PT_OBJECT**, it cannot be successfully retrieved by the [IMAPIProp::GetProps](imapiprop-getprops.md) method; its contents should be accessed by the [IMAPIProp::OpenProperty](imapiprop-openproperty.md) method, requesting the IID_IMAPITable interface identifier.</span></span> <span data-ttu-id="ac3e5-117">Dienstanbieter müssen es an die [IMAPIProp::GetPropList](imapiprop-getproplist.md) -Methode melden, wenn er festgelegt ist, jedoch kann positives oder nicht, wenn sie nicht festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="ac3e5-117">Service providers must report it to the [IMAPIProp::GetPropList](imapiprop-getproplist.md) method if it is set, but can optionally report it or not if it is not set.</span></span> 
  
<span data-ttu-id="ac3e5-118">Zum Abrufen von Inhaltsverzeichnisses sollte eine Clientanwendung die [IMAPIContainer::GetHierarchyTable](imapicontainer-gethierarchytable.md) -Methode aufrufen.</span><span class="sxs-lookup"><span data-stu-id="ac3e5-118">To retrieve table contents, a client application should call the [IMAPIContainer::GetHierarchyTable](imapicontainer-gethierarchytable.md) method.</span></span> <span data-ttu-id="ac3e5-119">Weitere Informationen finden Sie unter [Hierarchietabellen](hierarchy-tables.md).</span><span class="sxs-lookup"><span data-stu-id="ac3e5-119">For more information, see [Hierarchy Tables](hierarchy-tables.md).</span></span> 
  
 <span data-ttu-id="ac3e5-120">**PR_CONTAINER_CONTENTS** ([PidTagContainerContents](pidtagcontainercontents-canonical-property.md)) **PR_FOLDER_ASSOCIATED_CONTENTS** ([PidTagFolderAssociatedContents](pidtagfolderassociatedcontents-canonical-property.md)), und diese Eigenschaft ähneln in Verwendung.</span><span class="sxs-lookup"><span data-stu-id="ac3e5-120">**PR_CONTAINER_CONTENTS** ([PidTagContainerContents](pidtagcontainercontents-canonical-property.md)), **PR_FOLDER_ASSOCIATED_CONTENTS** ([PidTagFolderAssociatedContents](pidtagfolderassociatedcontents-canonical-property.md)), and this property are similar in usage.</span></span> <span data-ttu-id="ac3e5-121">Mehrere MAPI-Eigenschaften bieten Zugriff auf Tabellen:</span><span class="sxs-lookup"><span data-stu-id="ac3e5-121">Several MAPI properties provide access to tables:</span></span> 
  
|<span data-ttu-id="ac3e5-122">**Eigenschaft**</span><span class="sxs-lookup"><span data-stu-id="ac3e5-122">**Property**</span></span>|<span data-ttu-id="ac3e5-123">**Table**</span><span class="sxs-lookup"><span data-stu-id="ac3e5-123">**Table**</span></span>|
|:-----|:-----|
|<span data-ttu-id="ac3e5-124">**PR_CONTAINER_CONTENTS** ([PidTagContainerContents](pidtagcontainercontents-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="ac3e5-124">**PR_CONTAINER_CONTENTS** ([PidTagContainerContents](pidtagcontainercontents-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="ac3e5-125">Inhaltstabelle</span><span class="sxs-lookup"><span data-stu-id="ac3e5-125">Contents table</span></span>  <br/> |
|<span data-ttu-id="ac3e5-126">**PR_CONTAINER_HIERARCHY**</span><span class="sxs-lookup"><span data-stu-id="ac3e5-126">**PR_CONTAINER_HIERARCHY**</span></span> <br/> |<span data-ttu-id="ac3e5-127">Hierarchietabelle</span><span class="sxs-lookup"><span data-stu-id="ac3e5-127">Hierarchy table</span></span>  <br/> |
|<span data-ttu-id="ac3e5-128">**PR_FOLDER_ASSOCIATED_CONTENTS** ([PidTagFolderAssociatedContents](pidtagfolderassociatedcontents-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="ac3e5-128">**PR_FOLDER_ASSOCIATED_CONTENTS** ([PidTagFolderAssociatedContents](pidtagfolderassociatedcontents-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="ac3e5-129">Zugehörige Inhaltstabelle</span><span class="sxs-lookup"><span data-stu-id="ac3e5-129">Associated contents table</span></span>  <br/> |
|<span data-ttu-id="ac3e5-130">**PR_MESSAGE_ATTACHMENTS** ([PidTagMessageAttachments](pidtagmessageattachments-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="ac3e5-130">**PR_MESSAGE_ATTACHMENTS** ([PidTagMessageAttachments](pidtagmessageattachments-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="ac3e5-131">Anlagentabelle</span><span class="sxs-lookup"><span data-stu-id="ac3e5-131">Attachment table</span></span>  <br/> |
|<span data-ttu-id="ac3e5-132">**PR_MESSAGE_RECIPIENTS** ([PidTagMessageRecipients](pidtagmessagerecipients-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="ac3e5-132">**PR_MESSAGE_RECIPIENTS** ([PidTagMessageRecipients](pidtagmessagerecipients-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="ac3e5-133">Empfänger-Tabelle</span><span class="sxs-lookup"><span data-stu-id="ac3e5-133">Recipient table</span></span>  <br/> |
   
## <a name="related-resources"></a><span data-ttu-id="ac3e5-134">Verwandte Ressourcen</span><span class="sxs-lookup"><span data-stu-id="ac3e5-134">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="ac3e5-135">Protokollspezifikationen</span><span class="sxs-lookup"><span data-stu-id="ac3e5-135">Protocol specifications</span></span>

<span data-ttu-id="ac3e5-136">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="ac3e5-136">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="ac3e5-137">Bietet Verweise auf Verwandte Exchange Server-Spezifikationen.</span><span class="sxs-lookup"><span data-stu-id="ac3e5-137">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="ac3e5-138">[[MS-OXCFXICS]](http://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="ac3e5-138">[[MS-OXCFXICS]](http://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="ac3e5-139">Verarbeitet die Reihenfolge und den Fluss für Datenübertragungen zwischen einem Client und Server.</span><span class="sxs-lookup"><span data-stu-id="ac3e5-139">Handles the order and flow for data transfers between a client and server.</span></span>
    
<span data-ttu-id="ac3e5-140">[[MS-OXCICAL]](http://msdn.microsoft.com/library/a685a040-5b69-4c84-b084-795113fb4012%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="ac3e5-140">[[MS-OXCICAL]](http://msdn.microsoft.com/library/a685a040-5b69-4c84-b084-795113fb4012%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="ac3e5-141">Konvertiert zwischen IETF RFC2445, RFC2446, RFC2447, und Termine und meeting-Objekte.</span><span class="sxs-lookup"><span data-stu-id="ac3e5-141">Converts between IETF RFC2445, RFC2446, and RFC2447, and appointment and meeting objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="ac3e5-142">Header-Dateien</span><span class="sxs-lookup"><span data-stu-id="ac3e5-142">Header files</span></span>

<span data-ttu-id="ac3e5-143">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="ac3e5-143">Mapidefs.h</span></span>
  
> <span data-ttu-id="ac3e5-144">Enthält die Datentypdefinitionen.</span><span class="sxs-lookup"><span data-stu-id="ac3e5-144">Provides data type definitions.</span></span>
    
<span data-ttu-id="ac3e5-145">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="ac3e5-145">Mapitags.h</span></span>
  
> <span data-ttu-id="ac3e5-146">Enthält Definitionen von Eigenschaften, die als Alternative Namen aufgelistet.</span><span class="sxs-lookup"><span data-stu-id="ac3e5-146">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="ac3e5-147">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="ac3e5-147">See also</span></span>



[<span data-ttu-id="ac3e5-148">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="ac3e5-148">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="ac3e5-149">Kanonische MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="ac3e5-149">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="ac3e5-150">Zuordnen von kanonischen Eigenschaftennamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="ac3e5-150">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="ac3e5-151">Zuordnen von MAPI-Namen zu kanonische Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="ac3e5-151">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

