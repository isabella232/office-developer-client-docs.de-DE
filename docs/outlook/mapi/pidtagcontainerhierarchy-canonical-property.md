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
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: f009d7ce5cd1856ccff1e00953188c8edde7a6bc
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32332858"
---
# <a name="pidtagcontainerhierarchy-canonical-property"></a><span data-ttu-id="38ca7-103">PidTagContainerHierarchy (kanonische Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="38ca7-103">PidTagContainerHierarchy Canonical Property</span></span>

  
  
<span data-ttu-id="38ca7-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="38ca7-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="38ca7-105">Enthält ein eingebettetes Hierarchietabelle-Objekt, das Informationen zu den untergeordneten Containern enthält.</span><span class="sxs-lookup"><span data-stu-id="38ca7-105">Contains an embedded hierarchy table object that provides information about the child containers.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="38ca7-106">Zugeordnete Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="38ca7-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="38ca7-107">PR_CONTAINER_HIERARCHY</span><span class="sxs-lookup"><span data-stu-id="38ca7-107">PR_CONTAINER_HIERARCHY</span></span>  <br/> |
|<span data-ttu-id="38ca7-108">Kennung:</span><span class="sxs-lookup"><span data-stu-id="38ca7-108">Identifier:</span></span>  <br/> |<span data-ttu-id="38ca7-109">0x360E</span><span class="sxs-lookup"><span data-stu-id="38ca7-109">0x360E</span></span>  <br/> |
|<span data-ttu-id="38ca7-110">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="38ca7-110">Data type:</span></span>  <br/> |<span data-ttu-id="38ca7-111">PT_OBJECT</span><span class="sxs-lookup"><span data-stu-id="38ca7-111">PT_OBJECT</span></span>  <br/> |
|<span data-ttu-id="38ca7-112">Bereich:</span><span class="sxs-lookup"><span data-stu-id="38ca7-112">Area:</span></span>  <br/> |<span data-ttu-id="38ca7-113">Container</span><span class="sxs-lookup"><span data-stu-id="38ca7-113">Container</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="38ca7-114">Hinweise</span><span class="sxs-lookup"><span data-stu-id="38ca7-114">Remarks</span></span>

<span data-ttu-id="38ca7-115">Diese Eigenschaft kann in [IMAPIProp::CopyTo-Vorgängen](imapiprop-copyto.md) ausgeschlossen oder in [IMAPIProp::CopyProps-Vorgängen enthalten](imapiprop-copyprops.md) sein.</span><span class="sxs-lookup"><span data-stu-id="38ca7-115">This property can be excluded in [IMAPIProp::CopyTo](imapiprop-copyto.md) operations or included in [IMAPIProp::CopyProps](imapiprop-copyprops.md) operations.</span></span> <span data-ttu-id="38ca7-116">Als Eigenschaft vom Typ **PT_OBJECT** kann sie nicht erfolgreich von der [IMAPIProp::GetProps-Methode abgerufen](imapiprop-getprops.md) werden. Der Zugriff auf den Inhalt sollte über die [IMAPIProp::OpenProperty-Methode](imapiprop-openproperty.md) erfolgen, die den IID_IMAPITable anfordert.</span><span class="sxs-lookup"><span data-stu-id="38ca7-116">As a property of type **PT_OBJECT**, it cannot be successfully retrieved by the [IMAPIProp::GetProps](imapiprop-getprops.md) method; its contents should be accessed by the [IMAPIProp::OpenProperty](imapiprop-openproperty.md) method, requesting the IID_IMAPITable interface identifier.</span></span> <span data-ttu-id="38ca7-117">Dienstanbieter müssen sie der [IMAPIProp::GetPropList-Methode](imapiprop-getproplist.md) melden, wenn sie festgelegt ist, können sie jedoch optional melden oder nicht, wenn sie nicht festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="38ca7-117">Service providers must report it to the [IMAPIProp::GetPropList](imapiprop-getproplist.md) method if it is set, but can optionally report it or not if it is not set.</span></span> 
  
<span data-ttu-id="38ca7-118">Zum Abrufen von Tabelleninhalten sollte eine Clientanwendung die [IMAPIContainer::GetHierarchyTable-Methode](imapicontainer-gethierarchytable.md) aufrufen.</span><span class="sxs-lookup"><span data-stu-id="38ca7-118">To retrieve table contents, a client application should call the [IMAPIContainer::GetHierarchyTable](imapicontainer-gethierarchytable.md) method.</span></span> <span data-ttu-id="38ca7-119">Weitere Informationen finden Sie unter [Hierarchietabellen](hierarchy-tables.md).</span><span class="sxs-lookup"><span data-stu-id="38ca7-119">For more information, see [Hierarchy Tables](hierarchy-tables.md).</span></span> 
  
 <span data-ttu-id="38ca7-120">**PR_CONTAINER_CONTENTS** ([PidTagContainerContents](pidtagcontainercontents-canonical-property.md)), **PR_FOLDER_ASSOCIATED_CONTENTS** ([PidTagFolderAssociatedContents](pidtagfolderassociatedcontents-canonical-property.md)), und diese Eigenschaft ist in der Verwendung ähnlich.</span><span class="sxs-lookup"><span data-stu-id="38ca7-120">**PR_CONTAINER_CONTENTS** ([PidTagContainerContents](pidtagcontainercontents-canonical-property.md)), **PR_FOLDER_ASSOCIATED_CONTENTS** ([PidTagFolderAssociatedContents](pidtagfolderassociatedcontents-canonical-property.md)), and this property are similar in usage.</span></span> <span data-ttu-id="38ca7-121">Mehrere MAPI-Eigenschaften bieten Zugriff auf Tabellen:</span><span class="sxs-lookup"><span data-stu-id="38ca7-121">Several MAPI properties provide access to tables:</span></span> 
  
|<span data-ttu-id="38ca7-122">**Eigenschaft**</span><span class="sxs-lookup"><span data-stu-id="38ca7-122">**Property**</span></span>|<span data-ttu-id="38ca7-123">**Table**</span><span class="sxs-lookup"><span data-stu-id="38ca7-123">**Table**</span></span>|
|:-----|:-----|
|<span data-ttu-id="38ca7-124">**PR_CONTAINER_CONTENTS** ([PidTagContainerContents](pidtagcontainercontents-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="38ca7-124">**PR_CONTAINER_CONTENTS** ([PidTagContainerContents](pidtagcontainercontents-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="38ca7-125">Inhaltstabelle</span><span class="sxs-lookup"><span data-stu-id="38ca7-125">Contents table</span></span>  <br/> |
|<span data-ttu-id="38ca7-126">**PR_CONTAINER_HIERARCHY**</span><span class="sxs-lookup"><span data-stu-id="38ca7-126">**PR_CONTAINER_HIERARCHY**</span></span> <br/> |<span data-ttu-id="38ca7-127">Hierarchietabelle</span><span class="sxs-lookup"><span data-stu-id="38ca7-127">Hierarchy table</span></span>  <br/> |
|<span data-ttu-id="38ca7-128">**PR_FOLDER_ASSOCIATED_CONTENTS** ([PidTagFolderAssociatedContents](pidtagfolderassociatedcontents-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="38ca7-128">**PR_FOLDER_ASSOCIATED_CONTENTS** ([PidTagFolderAssociatedContents](pidtagfolderassociatedcontents-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="38ca7-129">Tabelle "Zugeordnete Inhalte"</span><span class="sxs-lookup"><span data-stu-id="38ca7-129">Associated contents table</span></span>  <br/> |
|<span data-ttu-id="38ca7-130">**PR_MESSAGE_ATTACHMENTS** ([PidTagMessageAttachments](pidtagmessageattachments-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="38ca7-130">**PR_MESSAGE_ATTACHMENTS** ([PidTagMessageAttachments](pidtagmessageattachments-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="38ca7-131">Anlagentabelle</span><span class="sxs-lookup"><span data-stu-id="38ca7-131">Attachment table</span></span>  <br/> |
|<span data-ttu-id="38ca7-132">**PR_MESSAGE_RECIPIENTS** ([PidTagMessageRecipients](pidtagmessagerecipients-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="38ca7-132">**PR_MESSAGE_RECIPIENTS** ([PidTagMessageRecipients](pidtagmessagerecipients-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="38ca7-133">Empfängertabelle</span><span class="sxs-lookup"><span data-stu-id="38ca7-133">Recipient table</span></span>  <br/> |
   
## <a name="related-resources"></a><span data-ttu-id="38ca7-134">Verwandte Ressourcen</span><span class="sxs-lookup"><span data-stu-id="38ca7-134">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="38ca7-135">Protokollspezifikationen</span><span class="sxs-lookup"><span data-stu-id="38ca7-135">Protocol specifications</span></span>

<span data-ttu-id="38ca7-136">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="38ca7-136">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="38ca7-137">Enthält Verweise auf Exchange Server Protokollspezifikationen.</span><span class="sxs-lookup"><span data-stu-id="38ca7-137">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="38ca7-138">[[MS-OXCFXICS]](https://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="38ca7-138">[[MS-OXCFXICS]](https://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="38ca7-139">Verarbeitet die Reihenfolge und den Fluss für Datenübertragungen zwischen einem Client und einem Server.</span><span class="sxs-lookup"><span data-stu-id="38ca7-139">Handles the order and flow for data transfers between a client and server.</span></span>
    
<span data-ttu-id="38ca7-140">[[MS-OXCICAL]](https://msdn.microsoft.com/library/a685a040-5b69-4c84-b084-795113fb4012%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="38ca7-140">[[MS-OXCICAL]](https://msdn.microsoft.com/library/a685a040-5b69-4c84-b084-795113fb4012%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="38ca7-141">Konvertiert zwischen IETF RFC2445, RFC2446 und RFC2447 sowie Termin- und Besprechungsobjekten.</span><span class="sxs-lookup"><span data-stu-id="38ca7-141">Converts between IETF RFC2445, RFC2446, and RFC2447, and appointment and meeting objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="38ca7-142">Headerdateien</span><span class="sxs-lookup"><span data-stu-id="38ca7-142">Header files</span></span>

<span data-ttu-id="38ca7-143">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="38ca7-143">Mapidefs.h</span></span>
  
> <span data-ttu-id="38ca7-144">Bietet Datentypdefinitionen.</span><span class="sxs-lookup"><span data-stu-id="38ca7-144">Provides data type definitions.</span></span>
    
<span data-ttu-id="38ca7-145">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="38ca7-145">Mapitags.h</span></span>
  
> <span data-ttu-id="38ca7-146">Enthält Definitionen von Eigenschaften, die als alternative Namen aufgeführt sind.</span><span class="sxs-lookup"><span data-stu-id="38ca7-146">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="38ca7-147">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="38ca7-147">See also</span></span>



[<span data-ttu-id="38ca7-148">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="38ca7-148">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="38ca7-149">KANONISCHE EIGENSCHAFTEN VON MAPI</span><span class="sxs-lookup"><span data-stu-id="38ca7-149">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="38ca7-150">Zuordnen kanonischer Eigenschaftsnamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="38ca7-150">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="38ca7-151">Zuordnen von MAPI-Namen zu kanonischen Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="38ca7-151">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

