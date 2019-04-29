---
title: Kanonische Pidtagvalidfoldermask (-Eigenschaft
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagValidFolderMask
api_type:
- COM
ms.assetid: 83a44aee-5269-42a8-8078-4bc063bb6e29
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 925e0eb60d55349ded114b827b6ca67e3b5ac1ce
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33427794"
---
# <a name="pidtagvalidfoldermask-canonical-property"></a><span data-ttu-id="03ec6-103">Kanonische Pidtagvalidfoldermask (-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="03ec6-103">PidTagValidFolderMask Canonical Property</span></span>

  
  
<span data-ttu-id="03ec6-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="03ec6-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="03ec6-105">Enthält eine Bitmaske von Flags, die die Gültigkeit der Eintragsbezeichner der Ordner in einem Nachrichtenspeicher kennzeichnen.</span><span class="sxs-lookup"><span data-stu-id="03ec6-105">Contains a bitmask of flags that indicate the validity of the entry identifiers of the folders in a message store.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="03ec6-106">Zugeordnete Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="03ec6-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="03ec6-107">PR_VALID_FOLDER_MASK</span><span class="sxs-lookup"><span data-stu-id="03ec6-107">PR_VALID_FOLDER_MASK</span></span>  <br/> |
|<span data-ttu-id="03ec6-108">Kennung:</span><span class="sxs-lookup"><span data-stu-id="03ec6-108">Identifier:</span></span>  <br/> |<span data-ttu-id="03ec6-109">0x35DF</span><span class="sxs-lookup"><span data-stu-id="03ec6-109">0x35DF</span></span>  <br/> |
|<span data-ttu-id="03ec6-110">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="03ec6-110">Data type:</span></span>  <br/> |<span data-ttu-id="03ec6-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="03ec6-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="03ec6-112">Bereich:</span><span class="sxs-lookup"><span data-stu-id="03ec6-112">Area:</span></span>  <br/> |<span data-ttu-id="03ec6-113">MAPI-Nachrichtenspeicher</span><span class="sxs-lookup"><span data-stu-id="03ec6-113">MAPI message store</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="03ec6-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="03ec6-114">Remarks</span></span>

<span data-ttu-id="03ec6-115">Die Eintrags-ID eines Ordners kann ungültig werden, wenn ein Benutzer den Ordner löscht oder wenn der Nachrichtenspeicher beschädigt wird.</span><span class="sxs-lookup"><span data-stu-id="03ec6-115">A folder's entry identifier can become invalid if a user deletes the folder or if the message store becomes corrupted.</span></span>
  
<span data-ttu-id="03ec6-116">Mindestens eines der folgenden Flags kann für die Bitmaske festgelegt werden:</span><span class="sxs-lookup"><span data-stu-id="03ec6-116">One or more of the following flags can be set for the bitmask:</span></span> 
  
<span data-ttu-id="03ec6-117">FOLDER_COMMON_VIEWS_VALID</span><span class="sxs-lookup"><span data-stu-id="03ec6-117">FOLDER_COMMON_VIEWS_VALID</span></span> 
  
> <span data-ttu-id="03ec6-118">Der Ordner Allgemeine Ansichten hat einen gültigen Eintragsbezeichner.</span><span class="sxs-lookup"><span data-stu-id="03ec6-118">The common views folder has a valid entry identifier.</span></span> <span data-ttu-id="03ec6-119">Siehe **PR_COMMON_VIEWS_ENTRYID** ([pidtagcommonviewsentryid (](pidtagcommonviewsentryid-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="03ec6-119">See **PR_COMMON_VIEWS_ENTRYID** ([PidTagCommonViewsEntryId](pidtagcommonviewsentryid-canonical-property.md)).</span></span>
    
<span data-ttu-id="03ec6-120">FOLDER_FINDER_VALID</span><span class="sxs-lookup"><span data-stu-id="03ec6-120">FOLDER_FINDER_VALID</span></span> 
  
> <span data-ttu-id="03ec6-121">Der Finder-Ordner verfügt über eine gültige Eintrags-ID.</span><span class="sxs-lookup"><span data-stu-id="03ec6-121">The finder folder has a valid entry identifier.</span></span> <span data-ttu-id="03ec6-122">Siehe **PR_FINDER_ENTRYID** ([pidtagfinderentryid (](pidtagfinderentryid-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="03ec6-122">See **PR_FINDER_ENTRYID** ([PidTagFinderEntryId](pidtagfinderentryid-canonical-property.md)).</span></span> 
    
<span data-ttu-id="03ec6-123">FOLDER_IPM_INBOX_VALID</span><span class="sxs-lookup"><span data-stu-id="03ec6-123">FOLDER_IPM_INBOX_VALID</span></span> 
  
> <span data-ttu-id="03ec6-124">Der Empfänger Ordner für die zwischenmenschlichen Nachrichten (IPM) verfügt über eine gültige Eintrags-ID.</span><span class="sxs-lookup"><span data-stu-id="03ec6-124">The interpersonal message (IPM) receive folder has a valid entry identifier.</span></span> <span data-ttu-id="03ec6-125">Weitere Informationen finden Sie unter [IMsgStore:: GetReceiveFolder](imsgstore-getreceivefolder.md).</span><span class="sxs-lookup"><span data-stu-id="03ec6-125">See [IMsgStore::GetReceiveFolder](imsgstore-getreceivefolder.md).</span></span> 
    
<span data-ttu-id="03ec6-126">FOLDER_IPM_OUTBOX_VALID</span><span class="sxs-lookup"><span data-stu-id="03ec6-126">FOLDER_IPM_OUTBOX_VALID</span></span> 
  
> <span data-ttu-id="03ec6-127">Der IPM-Ausgangsordner hat einen gültigen Eintragsbezeichner.</span><span class="sxs-lookup"><span data-stu-id="03ec6-127">The IPM Outbox folder has a valid entry identifier.</span></span> <span data-ttu-id="03ec6-128">Siehe **PR_IPM_OUTBOX_ENTRYID** ([pidtagipmoutboxentryid (](pidtagipmoutboxentryid-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="03ec6-128">See **PR_IPM_OUTBOX_ENTRYID** ([PidTagIpmOutboxEntryId](pidtagipmoutboxentryid-canonical-property.md)).</span></span> 
    
<span data-ttu-id="03ec6-129">FOLDER_IPM_SENTMAIL_VALID</span><span class="sxs-lookup"><span data-stu-id="03ec6-129">FOLDER_IPM_SENTMAIL_VALID</span></span> 
  
> <span data-ttu-id="03ec6-130">Der Ordner "IPM Sent Items" hat einen gültigen Eintragsbezeichner.</span><span class="sxs-lookup"><span data-stu-id="03ec6-130">The IPM Sent Items folder has a valid entry identifier.</span></span> <span data-ttu-id="03ec6-131">Siehe **PR_IPM_SENTMAIL_ENTRYID** ([pidtagipmsentmailentryid (](pidtagipmsentmailentryid-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="03ec6-131">See **PR_IPM_SENTMAIL_ENTRYID** ([PidTagIpmSentMailEntryId](pidtagipmsentmailentryid-canonical-property.md)).</span></span>
    
<span data-ttu-id="03ec6-132">FOLDER_IPM_SUBTREE_VALID</span><span class="sxs-lookup"><span data-stu-id="03ec6-132">FOLDER_IPM_SUBTREE_VALID</span></span> 
  
> <span data-ttu-id="03ec6-133">Die Unterstruktur des IPM-Ordners verfügt über eine gültige Eintrags-ID.</span><span class="sxs-lookup"><span data-stu-id="03ec6-133">The IPM folder subtree has a valid entry identifier.</span></span> <span data-ttu-id="03ec6-134">Siehe **PR_IPM_SUBTREE_ENTRYID** ([pidtagipmsubtreeentryid (](pidtagipmsubtreeentryid-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="03ec6-134">See **PR_IPM_SUBTREE_ENTRYID** ([PidTagIpmSubtreeEntryId](pidtagipmsubtreeentryid-canonical-property.md)).</span></span>
    
<span data-ttu-id="03ec6-135">FOLDER_IPM_WASTEBASKET_VALID</span><span class="sxs-lookup"><span data-stu-id="03ec6-135">FOLDER_IPM_WASTEBASKET_VALID</span></span> 
  
> <span data-ttu-id="03ec6-136">Der Ordner "IPM Deleted Items" hat einen gültigen Eintragsbezeichner.</span><span class="sxs-lookup"><span data-stu-id="03ec6-136">The IPM Deleted Items folder has a valid entry identifier.</span></span> <span data-ttu-id="03ec6-137">Siehe **PR_IPM_WASTEBASKET_ENTRYID** ([pidtagipmwastebasketentryid (](pidtagipmwastebasketentryid-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="03ec6-137">See **PR_IPM_WASTEBASKET_ENTRYID** ([PidTagIpmWastebasketEntryId](pidtagipmwastebasketentryid-canonical-property.md)).</span></span>
    
<span data-ttu-id="03ec6-138">FOLDER_VIEWS_VALID</span><span class="sxs-lookup"><span data-stu-id="03ec6-138">FOLDER_VIEWS_VALID</span></span> 
  
> <span data-ttu-id="03ec6-139">Der Ordner views hat eine gültige Eintrags-ID.</span><span class="sxs-lookup"><span data-stu-id="03ec6-139">The views folder has a valid entry identifier.</span></span> <span data-ttu-id="03ec6-140">Siehe **PR_VIEWS_ENTRYID** ([pidtagviewsentryid (](pidtagviewsentryid-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="03ec6-140">See **PR_VIEWS_ENTRYID** ([PidTagViewsEntryId](pidtagviewsentryid-canonical-property.md)).</span></span>
    
## <a name="related-resources"></a><span data-ttu-id="03ec6-141">Verwandte Ressourcen</span><span class="sxs-lookup"><span data-stu-id="03ec6-141">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="03ec6-142">Header Dateien</span><span class="sxs-lookup"><span data-stu-id="03ec6-142">Header files</span></span>

<span data-ttu-id="03ec6-143">Mapidefs. h</span><span class="sxs-lookup"><span data-stu-id="03ec6-143">Mapidefs.h</span></span>
  
> <span data-ttu-id="03ec6-144">Stellt Datentypdefinitionen bereit.</span><span class="sxs-lookup"><span data-stu-id="03ec6-144">Provides data type definitions.</span></span>
    
<span data-ttu-id="03ec6-145">Mapitags. h</span><span class="sxs-lookup"><span data-stu-id="03ec6-145">Mapitags.h</span></span>
  
> <span data-ttu-id="03ec6-146">Enthält Definitionen von Eigenschaften, die als Alternative Namen aufgeführt sind.</span><span class="sxs-lookup"><span data-stu-id="03ec6-146">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="03ec6-147">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="03ec6-147">See also</span></span>



[<span data-ttu-id="03ec6-148">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="03ec6-148">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="03ec6-149">Kanonische MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="03ec6-149">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="03ec6-150">Zuordnen von kanonischen Eigenschaftennamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="03ec6-150">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="03ec6-151">Zuordnen von MAPI-Namen zu kanonischen Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="03ec6-151">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

