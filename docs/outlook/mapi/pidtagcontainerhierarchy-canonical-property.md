---
title: Kanonische Pidtagcontainerhierarchy (-Eigenschaft
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
ms.openlocfilehash: f009d7ce5cd1856ccff1e00953188c8edde7a6bc
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32332858"
---
# <a name="pidtagcontainerhierarchy-canonical-property"></a><span data-ttu-id="5dc44-103">Kanonische Pidtagcontainerhierarchy (-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="5dc44-103">PidTagContainerHierarchy Canonical Property</span></span>

  
  
<span data-ttu-id="5dc44-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="5dc44-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="5dc44-105">Enthält ein eingebettetes Hierarchie Table-Objekt, das Informationen zu den untergeordneten Containern bereitstellt.</span><span class="sxs-lookup"><span data-stu-id="5dc44-105">Contains an embedded hierarchy table object that provides information about the child containers.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="5dc44-106">Zugeordnete Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="5dc44-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="5dc44-107">PR_CONTAINER_HIERARCHY</span><span class="sxs-lookup"><span data-stu-id="5dc44-107">PR_CONTAINER_HIERARCHY</span></span>  <br/> |
|<span data-ttu-id="5dc44-108">Kennung:</span><span class="sxs-lookup"><span data-stu-id="5dc44-108">Identifier:</span></span>  <br/> |<span data-ttu-id="5dc44-109">0x360E</span><span class="sxs-lookup"><span data-stu-id="5dc44-109">0x360E</span></span>  <br/> |
|<span data-ttu-id="5dc44-110">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="5dc44-110">Data type:</span></span>  <br/> |<span data-ttu-id="5dc44-111">PT_OBJECT</span><span class="sxs-lookup"><span data-stu-id="5dc44-111">PT_OBJECT</span></span>  <br/> |
|<span data-ttu-id="5dc44-112">Bereich:</span><span class="sxs-lookup"><span data-stu-id="5dc44-112">Area:</span></span>  <br/> |<span data-ttu-id="5dc44-113">Container</span><span class="sxs-lookup"><span data-stu-id="5dc44-113">Container</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="5dc44-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="5dc44-114">Remarks</span></span>

<span data-ttu-id="5dc44-115">Diese Eigenschaft kann in [IMAPIProp:: CopyTo](imapiprop-copyto.md) -Vorgängen oder in [IMAPIProp:: CopyProps](imapiprop-copyprops.md) -Vorgängen ausgeschlossen werden.</span><span class="sxs-lookup"><span data-stu-id="5dc44-115">This property can be excluded in [IMAPIProp::CopyTo](imapiprop-copyto.md) operations or included in [IMAPIProp::CopyProps](imapiprop-copyprops.md) operations.</span></span> <span data-ttu-id="5dc44-116">Als Eigenschaft vom Typ **PT_OBJECT**kann Sie nicht erfolgreich von der [IMAPIProp::](imapiprop-getprops.md) GetProps-Methode abgerufen werden; auf den Inhalt sollte von der [IMAPIProp:: OpenProperty](imapiprop-openproperty.md) -Methode zugegriffen werden, um den IID_IMAPITable-Schnittstellenbezeichner anzufordern.</span><span class="sxs-lookup"><span data-stu-id="5dc44-116">As a property of type **PT_OBJECT**, it cannot be successfully retrieved by the [IMAPIProp::GetProps](imapiprop-getprops.md) method; its contents should be accessed by the [IMAPIProp::OpenProperty](imapiprop-openproperty.md) method, requesting the IID_IMAPITable interface identifier.</span></span> <span data-ttu-id="5dc44-117">Dienstanbieter müssen Sie an die [IMAPIProp::](imapiprop-getproplist.md) getproplist-Methode melden, wenn Sie festgelegt ist, aber optional melden können, wenn Sie nicht festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="5dc44-117">Service providers must report it to the [IMAPIProp::GetPropList](imapiprop-getproplist.md) method if it is set, but can optionally report it or not if it is not set.</span></span> 
  
<span data-ttu-id="5dc44-118">Zum Abrufen von Tabelleninhalten sollte eine Clientanwendung die [IMAPIContainer:: gethierarchyid](imapicontainer-gethierarchytable.md) -Methode aufrufen.</span><span class="sxs-lookup"><span data-stu-id="5dc44-118">To retrieve table contents, a client application should call the [IMAPIContainer::GetHierarchyTable](imapicontainer-gethierarchytable.md) method.</span></span> <span data-ttu-id="5dc44-119">Weitere Informationen finden Sie unter [Hierarchietabellen](hierarchy-tables.md).</span><span class="sxs-lookup"><span data-stu-id="5dc44-119">For more information, see [Hierarchy Tables](hierarchy-tables.md).</span></span> 
  
 <span data-ttu-id="5dc44-120">**PR_CONTAINER_CONTENTS** ([Pidtagcontainercontents (](pidtagcontainercontents-canonical-property.md)), **PR_FOLDER_ASSOCIATED_CONTENTS** ([pidtagfolderassociatedcontents (](pidtagfolderassociatedcontents-canonical-property.md)) und diese Eigenschaft ähneln der Verwendung.</span><span class="sxs-lookup"><span data-stu-id="5dc44-120">**PR_CONTAINER_CONTENTS** ([PidTagContainerContents](pidtagcontainercontents-canonical-property.md)), **PR_FOLDER_ASSOCIATED_CONTENTS** ([PidTagFolderAssociatedContents](pidtagfolderassociatedcontents-canonical-property.md)), and this property are similar in usage.</span></span> <span data-ttu-id="5dc44-121">Mehrere MAPI-Eigenschaften bieten Zugriff auf Tabellen:</span><span class="sxs-lookup"><span data-stu-id="5dc44-121">Several MAPI properties provide access to tables:</span></span> 
  
|<span data-ttu-id="5dc44-122">**Eigenschaft**</span><span class="sxs-lookup"><span data-stu-id="5dc44-122">**Property**</span></span>|<span data-ttu-id="5dc44-123">**Table**</span><span class="sxs-lookup"><span data-stu-id="5dc44-123">**Table**</span></span>|
|:-----|:-----|
|<span data-ttu-id="5dc44-124">**PR_CONTAINER_CONTENTS** ([Pidtagcontainercontents (](pidtagcontainercontents-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="5dc44-124">**PR_CONTAINER_CONTENTS** ([PidTagContainerContents](pidtagcontainercontents-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="5dc44-125">Inhaltstabelle</span><span class="sxs-lookup"><span data-stu-id="5dc44-125">Contents table</span></span>  <br/> |
|<span data-ttu-id="5dc44-126">**PR_CONTAINER_HIERARCHY**</span><span class="sxs-lookup"><span data-stu-id="5dc44-126">**PR_CONTAINER_HIERARCHY**</span></span> <br/> |<span data-ttu-id="5dc44-127">Hierarchietabelle</span><span class="sxs-lookup"><span data-stu-id="5dc44-127">Hierarchy table</span></span>  <br/> |
|<span data-ttu-id="5dc44-128">**PR_FOLDER_ASSOCIATED_CONTENTS** ([Pidtagfolderassociatedcontents (](pidtagfolderassociatedcontents-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="5dc44-128">**PR_FOLDER_ASSOCIATED_CONTENTS** ([PidTagFolderAssociatedContents](pidtagfolderassociatedcontents-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="5dc44-129">Tabelle mit zugeordneten Inhalten</span><span class="sxs-lookup"><span data-stu-id="5dc44-129">Associated contents table</span></span>  <br/> |
|<span data-ttu-id="5dc44-130">**PR_MESSAGE_ATTACHMENTS** ([Pidtagmessageattachments (](pidtagmessageattachments-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="5dc44-130">**PR_MESSAGE_ATTACHMENTS** ([PidTagMessageAttachments](pidtagmessageattachments-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="5dc44-131">Attachment-Tabelle</span><span class="sxs-lookup"><span data-stu-id="5dc44-131">Attachment table</span></span>  <br/> |
|<span data-ttu-id="5dc44-132">**PR_MESSAGE_RECIPIENTS** ([Pidtagmessagerecipients (](pidtagmessagerecipients-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="5dc44-132">**PR_MESSAGE_RECIPIENTS** ([PidTagMessageRecipients](pidtagmessagerecipients-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="5dc44-133">Empfängertabelle</span><span class="sxs-lookup"><span data-stu-id="5dc44-133">Recipient table</span></span>  <br/> |
   
## <a name="related-resources"></a><span data-ttu-id="5dc44-134">Zugehörige Ressourcen</span><span class="sxs-lookup"><span data-stu-id="5dc44-134">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="5dc44-135">Protokollspezifikationen</span><span class="sxs-lookup"><span data-stu-id="5dc44-135">Protocol specifications</span></span>

<span data-ttu-id="5dc44-136">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="5dc44-136">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="5dc44-137">Enthält Verweise auf zugehörige Exchange Server-Protokollspezifikationen.</span><span class="sxs-lookup"><span data-stu-id="5dc44-137">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="5dc44-138">[[MS-OXCFXICS]](https://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="5dc44-138">[[MS-OXCFXICS]](https://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="5dc44-139">Verarbeitet die Reihenfolge und den Ablauf für die Datenübertragung zwischen einem Client und einem Server.</span><span class="sxs-lookup"><span data-stu-id="5dc44-139">Handles the order and flow for data transfers between a client and server.</span></span>
    
<span data-ttu-id="5dc44-140">[[MS-OXCICAL]](https://msdn.microsoft.com/library/a685a040-5b69-4c84-b084-795113fb4012%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="5dc44-140">[[MS-OXCICAL]](https://msdn.microsoft.com/library/a685a040-5b69-4c84-b084-795113fb4012%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="5dc44-141">Konvertiert zwischen IETF-RFC2445, RFC2446 und RFC2447 sowie Termin-und Besprechungs Objekten.</span><span class="sxs-lookup"><span data-stu-id="5dc44-141">Converts between IETF RFC2445, RFC2446, and RFC2447, and appointment and meeting objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="5dc44-142">Header Dateien</span><span class="sxs-lookup"><span data-stu-id="5dc44-142">Header files</span></span>

<span data-ttu-id="5dc44-143">Mapidefs. h</span><span class="sxs-lookup"><span data-stu-id="5dc44-143">Mapidefs.h</span></span>
  
> <span data-ttu-id="5dc44-144">Stellt Datentypdefinitionen bereit.</span><span class="sxs-lookup"><span data-stu-id="5dc44-144">Provides data type definitions.</span></span>
    
<span data-ttu-id="5dc44-145">Mapitags. h</span><span class="sxs-lookup"><span data-stu-id="5dc44-145">Mapitags.h</span></span>
  
> <span data-ttu-id="5dc44-146">Enthält Definitionen von Eigenschaften, die als Alternative Namen aufgeführt sind.</span><span class="sxs-lookup"><span data-stu-id="5dc44-146">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="5dc44-147">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="5dc44-147">See also</span></span>



[<span data-ttu-id="5dc44-148">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="5dc44-148">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="5dc44-149">Kanonische MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="5dc44-149">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="5dc44-150">Zuordnen von kanonischen Eigenschaftennamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="5dc44-150">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="5dc44-151">Zuordnen von MAPI-Namen zu kanonischen Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="5dc44-151">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

