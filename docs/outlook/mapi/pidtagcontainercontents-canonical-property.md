---
title: Kanonische Pidtagcontainercontents (-Eigenschaft
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
ms.openlocfilehash: 5f0717c2a6def6f99f1e53217764e8820125b79d
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32283128"
---
# <a name="pidtagcontainercontents-canonical-property"></a><span data-ttu-id="85a04-103">Kanonische Pidtagcontainercontents (-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="85a04-103">PidTagContainerContents Canonical Property</span></span>

  
  
<span data-ttu-id="85a04-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="85a04-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="85a04-105">Enthält ein Table-Objekt mit eingebetteten Inhalten, das Informationen zu einem Container bereitstellt.</span><span class="sxs-lookup"><span data-stu-id="85a04-105">Contains an embedded contents table object that provides information about a container.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="85a04-106">Zugeordnete Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="85a04-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="85a04-107">PR_CONTAINER_CONTENTS</span><span class="sxs-lookup"><span data-stu-id="85a04-107">PR_CONTAINER_CONTENTS</span></span>  <br/> |
|<span data-ttu-id="85a04-108">Kennung:</span><span class="sxs-lookup"><span data-stu-id="85a04-108">Identifier:</span></span>  <br/> |<span data-ttu-id="85a04-109">0x360F</span><span class="sxs-lookup"><span data-stu-id="85a04-109">0x360F</span></span>  <br/> |
|<span data-ttu-id="85a04-110">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="85a04-110">Data type:</span></span>  <br/> |<span data-ttu-id="85a04-111">PT_OBJECT</span><span class="sxs-lookup"><span data-stu-id="85a04-111">PT_OBJECT</span></span>  <br/> |
|<span data-ttu-id="85a04-112">Bereich:</span><span class="sxs-lookup"><span data-stu-id="85a04-112">Area:</span></span>  <br/> |<span data-ttu-id="85a04-113">Container</span><span class="sxs-lookup"><span data-stu-id="85a04-113">Container</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="85a04-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="85a04-114">Remarks</span></span>

<span data-ttu-id="85a04-115">Diese Eigenschaft kann in [IMAPIProp:: CopyTo](imapiprop-copyto.md) -Vorgängen oder in [IMAPIProp:: CopyProps](imapiprop-copyprops.md) -Vorgängen ausgeschlossen werden.</span><span class="sxs-lookup"><span data-stu-id="85a04-115">This property can be excluded in [IMAPIProp::CopyTo](imapiprop-copyto.md) operations or included in [IMAPIProp::CopyProps](imapiprop-copyprops.md) operations.</span></span> <span data-ttu-id="85a04-116">Als Eigenschaft vom Typ PT_OBJECT kann Sie nicht erfolgreich von der [IMAPIProp::](imapiprop-getprops.md) GetProps-Methode abgerufen werden; auf den Inhalt sollte von der [IMAPIProp:: OpenProperty](imapiprop-openproperty.md) -Methode zugegriffen werden, um den IID_IMAPITable-Schnittstellenbezeichner anzufordern.</span><span class="sxs-lookup"><span data-stu-id="85a04-116">As a property of type PT_OBJECT, it cannot be successfully retrieved by the [IMAPIProp::GetProps](imapiprop-getprops.md) method; its contents should be accessed by the [IMAPIProp::OpenProperty](imapiprop-openproperty.md) method, requesting the IID_IMAPITable interface identifier.</span></span> <span data-ttu-id="85a04-117">Dienstanbieter müssen Sie an die [IMAPIProp::](imapiprop-getproplist.md) getproplist-Methode melden, wenn Sie festgelegt ist, aber optional melden können, wenn Sie nicht festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="85a04-117">Service providers must report it to the [IMAPIProp::GetPropList](imapiprop-getproplist.md) method if it is set, but can optionally report it or not if it is not set.</span></span> 
  
<span data-ttu-id="85a04-118">Zum Abrufen von Tabelleninhalten sollte eine Clientanwendung die [IMAPIContainer::](imapicontainer-getcontentstable.md) getcontentable-Methode aufrufen.</span><span class="sxs-lookup"><span data-stu-id="85a04-118">To retrieve table contents, a client application should call the [IMAPIContainer::GetContentsTable](imapicontainer-getcontentstable.md) method.</span></span> <span data-ttu-id="85a04-119">For more information, see [Inhalt von Tabellen](contents-tables.md).</span><span class="sxs-lookup"><span data-stu-id="85a04-119">For more information, see [Contents Tables](contents-tables.md).</span></span> 
  
<span data-ttu-id="85a04-120">Diese Eigenschaft, **PR_CONTAINER_HIERARCHY** ([Pidtagcontainerhierarchy (](pidtagcontainerhierarchy-canonical-property.md)) und **PR_FOLDER_ASSOCIATED_CONTENTS** ([pidtagfolderassociatedcontents (](pidtagfolderassociatedcontents-canonical-property.md)) ähneln der Verwendung.</span><span class="sxs-lookup"><span data-stu-id="85a04-120">This property, **PR_CONTAINER_HIERARCHY** ([PidTagContainerHierarchy](pidtagcontainerhierarchy-canonical-property.md)) , and **PR_FOLDER_ASSOCIATED_CONTENTS** ([PidTagFolderAssociatedContents](pidtagfolderassociatedcontents-canonical-property.md)) are similar in usage.</span></span> <span data-ttu-id="85a04-121">Mehrere MAPI-Eigenschaften bieten Zugriff auf Tabellen:</span><span class="sxs-lookup"><span data-stu-id="85a04-121">Several MAPI properties provide access to tables:</span></span> 
  
|<span data-ttu-id="85a04-122">**Eigenschaft**</span><span class="sxs-lookup"><span data-stu-id="85a04-122">**Property**</span></span>|<span data-ttu-id="85a04-123">**Table**</span><span class="sxs-lookup"><span data-stu-id="85a04-123">**Table**</span></span>|
|:-----|:-----|
|<span data-ttu-id="85a04-124">Pidtagcontainercontents (</span><span class="sxs-lookup"><span data-stu-id="85a04-124">PidTagContainerContents</span></span>  <br/> |<span data-ttu-id="85a04-125">Inhaltstabelle</span><span class="sxs-lookup"><span data-stu-id="85a04-125">Contents table</span></span>  <br/> |
|<span data-ttu-id="85a04-126">**PR_CONTAINER_HIERARCHY** ([Pidtagcontainerhierarchy (](pidtagcontainerhierarchy-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="85a04-126">**PR_CONTAINER_HIERARCHY** ([PidTagContainerHierarchy](pidtagcontainerhierarchy-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="85a04-127">Hierarchietabelle</span><span class="sxs-lookup"><span data-stu-id="85a04-127">Hierarchy table</span></span>  <br/> |
|<span data-ttu-id="85a04-128">**PR_FOLDER_ASSOCIATED_CONTENTS** ([Pidtagfolderassociatedcontents (](pidtagfolderassociatedcontents-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="85a04-128">**PR_FOLDER_ASSOCIATED_CONTENTS** ([PidTagFolderAssociatedContents](pidtagfolderassociatedcontents-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="85a04-129">Tabelle mit zugeordneten Inhalten</span><span class="sxs-lookup"><span data-stu-id="85a04-129">Associated contents table</span></span>  <br/> |
|<span data-ttu-id="85a04-130">**PR_MESSAGE_ATTACHMENTS** ([Pidtagmessageattachments (](pidtagmessageattachments-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="85a04-130">**PR_MESSAGE_ATTACHMENTS** ([PidTagMessageAttachments](pidtagmessageattachments-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="85a04-131">Attachment-Tabelle</span><span class="sxs-lookup"><span data-stu-id="85a04-131">Attachment table</span></span>  <br/> |
|<span data-ttu-id="85a04-132">**PR_MESSAGE_RECIPIENTS** ([Pidtagmessagerecipients (](pidtagmessagerecipients-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="85a04-132">**PR_MESSAGE_RECIPIENTS** ([PidTagMessageRecipients](pidtagmessagerecipients-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="85a04-133">Empfängertabelle</span><span class="sxs-lookup"><span data-stu-id="85a04-133">Recipient table</span></span>  <br/> |
   
## <a name="related-resources"></a><span data-ttu-id="85a04-134">Zugehörige Ressourcen</span><span class="sxs-lookup"><span data-stu-id="85a04-134">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="85a04-135">Protokollspezifikationen</span><span class="sxs-lookup"><span data-stu-id="85a04-135">Protocol specifications</span></span>

<span data-ttu-id="85a04-136">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="85a04-136">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="85a04-137">Enthält Verweise auf zugehörige Exchange Server-Protokollspezifikationen.</span><span class="sxs-lookup"><span data-stu-id="85a04-137">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="85a04-138">[[MS-OXOABK]](https://msdn.microsoft.com/library/f4cf9b4c-9232-4506-9e71-2270de217614%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="85a04-138">[[MS-OXOABK]](https://msdn.microsoft.com/library/f4cf9b4c-9232-4506-9e71-2270de217614%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="85a04-139">Gibt die Eigenschaften und Vorgänge für Listen von Benutzern, Kontakten, Gruppen und Ressourcen an.</span><span class="sxs-lookup"><span data-stu-id="85a04-139">Specifies the properties and operations for lists of users, contacts, groups, and resources.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="85a04-140">Header Dateien</span><span class="sxs-lookup"><span data-stu-id="85a04-140">Header files</span></span>

<span data-ttu-id="85a04-141">Mapidefs. h</span><span class="sxs-lookup"><span data-stu-id="85a04-141">Mapidefs.h</span></span>
  
> <span data-ttu-id="85a04-142">Stellt Datentypdefinitionen bereit.</span><span class="sxs-lookup"><span data-stu-id="85a04-142">Provides data type definitions.</span></span>
    
<span data-ttu-id="85a04-143">Mapitags. h</span><span class="sxs-lookup"><span data-stu-id="85a04-143">Mapitags.h</span></span>
  
> <span data-ttu-id="85a04-144">Enthält Definitionen von Eigenschaften, die als Alternative Namen aufgeführt sind.</span><span class="sxs-lookup"><span data-stu-id="85a04-144">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="85a04-145">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="85a04-145">See also</span></span>



[<span data-ttu-id="85a04-146">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="85a04-146">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="85a04-147">Kanonische MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="85a04-147">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="85a04-148">Zuordnen von kanonischen Eigenschaftennamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="85a04-148">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="85a04-149">Zuordnen von MAPI-Namen zu kanonischen Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="85a04-149">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

