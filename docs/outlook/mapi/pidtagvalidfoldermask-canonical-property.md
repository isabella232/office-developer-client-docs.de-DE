---
title: PidTagValidFolderMask (kanonische Eigenschaft)
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
# <a name="pidtagvalidfoldermask-canonical-property"></a><span data-ttu-id="89547-103">PidTagValidFolderMask (kanonische Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="89547-103">PidTagValidFolderMask Canonical Property</span></span>

  
  
<span data-ttu-id="89547-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="89547-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="89547-105">Enthält eine Bitmaske mit Flags, die die Gültigkeit der Eintragsbezeichner der Ordner in einem Nachrichtenspeicher angeben.</span><span class="sxs-lookup"><span data-stu-id="89547-105">Contains a bitmask of flags that indicate the validity of the entry identifiers of the folders in a message store.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="89547-106">Zugeordnete Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="89547-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="89547-107">PR_VALID_FOLDER_MASK</span><span class="sxs-lookup"><span data-stu-id="89547-107">PR_VALID_FOLDER_MASK</span></span>  <br/> |
|<span data-ttu-id="89547-108">Kennung:</span><span class="sxs-lookup"><span data-stu-id="89547-108">Identifier:</span></span>  <br/> |<span data-ttu-id="89547-109">0x35DF</span><span class="sxs-lookup"><span data-stu-id="89547-109">0x35DF</span></span>  <br/> |
|<span data-ttu-id="89547-110">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="89547-110">Data type:</span></span>  <br/> |<span data-ttu-id="89547-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="89547-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="89547-112">Bereich:</span><span class="sxs-lookup"><span data-stu-id="89547-112">Area:</span></span>  <br/> |<span data-ttu-id="89547-113">MAPI-Nachrichtenspeicher</span><span class="sxs-lookup"><span data-stu-id="89547-113">MAPI message store</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="89547-114">Hinweise</span><span class="sxs-lookup"><span data-stu-id="89547-114">Remarks</span></span>

<span data-ttu-id="89547-115">Der Eintragsbezeichner eines Ordners kann ungültig werden, wenn ein Benutzer den Ordner löscht oder wenn der Nachrichtenspeicher beschädigt wird.</span><span class="sxs-lookup"><span data-stu-id="89547-115">A folder's entry identifier can become invalid if a user deletes the folder or if the message store becomes corrupted.</span></span>
  
<span data-ttu-id="89547-116">Mindestens eines der folgenden Flags kann für die Bitmaske festgelegt werden:</span><span class="sxs-lookup"><span data-stu-id="89547-116">One or more of the following flags can be set for the bitmask:</span></span> 
  
<span data-ttu-id="89547-117">FOLDER_COMMON_VIEWS_VALID</span><span class="sxs-lookup"><span data-stu-id="89547-117">FOLDER_COMMON_VIEWS_VALID</span></span> 
  
> <span data-ttu-id="89547-118">Der Ordner "Allgemeine Ansichten" verfügt über einen gültigen Eintragsbezeichner.</span><span class="sxs-lookup"><span data-stu-id="89547-118">The common views folder has a valid entry identifier.</span></span> <span data-ttu-id="89547-119">Siehe **PR_COMMON_VIEWS_ENTRYID** ([PidTagCommonViewsEntryId](pidtagcommonviewsentryid-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="89547-119">See **PR_COMMON_VIEWS_ENTRYID** ([PidTagCommonViewsEntryId](pidtagcommonviewsentryid-canonical-property.md)).</span></span>
    
<span data-ttu-id="89547-120">FOLDER_FINDER_VALID</span><span class="sxs-lookup"><span data-stu-id="89547-120">FOLDER_FINDER_VALID</span></span> 
  
> <span data-ttu-id="89547-121">Der Finderordner verfügt über einen gültigen Eintragsbezeichner.</span><span class="sxs-lookup"><span data-stu-id="89547-121">The finder folder has a valid entry identifier.</span></span> <span data-ttu-id="89547-122">Siehe **PR_FINDER_ENTRYID** ([PidTagFinderEntryId](pidtagfinderentryid-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="89547-122">See **PR_FINDER_ENTRYID** ([PidTagFinderEntryId](pidtagfinderentryid-canonical-property.md)).</span></span> 
    
<span data-ttu-id="89547-123">FOLDER_IPM_INBOX_VALID</span><span class="sxs-lookup"><span data-stu-id="89547-123">FOLDER_IPM_INBOX_VALID</span></span> 
  
> <span data-ttu-id="89547-124">Der IpM-Empfangsordner (Interpersonal Message) verfügt über einen gültigen Eintragsbezeichner.</span><span class="sxs-lookup"><span data-stu-id="89547-124">The interpersonal message (IPM) receive folder has a valid entry identifier.</span></span> <span data-ttu-id="89547-125">Weitere [Informationen finden Sie unter IMsgStore::GetReceiveFolder](imsgstore-getreceivefolder.md).</span><span class="sxs-lookup"><span data-stu-id="89547-125">See [IMsgStore::GetReceiveFolder](imsgstore-getreceivefolder.md).</span></span> 
    
<span data-ttu-id="89547-126">FOLDER_IPM_OUTBOX_VALID</span><span class="sxs-lookup"><span data-stu-id="89547-126">FOLDER_IPM_OUTBOX_VALID</span></span> 
  
> <span data-ttu-id="89547-127">Der Ordner "IPM-Posteingang" verfügt über einen gültigen Eintragsbezeichner.</span><span class="sxs-lookup"><span data-stu-id="89547-127">The IPM Outbox folder has a valid entry identifier.</span></span> <span data-ttu-id="89547-128">Siehe **PR_IPM_OUTBOX_ENTRYID** ([PidTagIpmOutboxEntryId](pidtagipmoutboxentryid-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="89547-128">See **PR_IPM_OUTBOX_ENTRYID** ([PidTagIpmOutboxEntryId](pidtagipmoutboxentryid-canonical-property.md)).</span></span> 
    
<span data-ttu-id="89547-129">FOLDER_IPM_SENTMAIL_VALID</span><span class="sxs-lookup"><span data-stu-id="89547-129">FOLDER_IPM_SENTMAIL_VALID</span></span> 
  
> <span data-ttu-id="89547-130">Der Ordner "IPM Gesendete Elemente" verfügt über einen gültigen Eintragsbezeichner.</span><span class="sxs-lookup"><span data-stu-id="89547-130">The IPM Sent Items folder has a valid entry identifier.</span></span> <span data-ttu-id="89547-131">Siehe **PR_IPM_SENTMAIL_ENTRYID** ([PidTagIpmSentMailEntryId](pidtagipmsentmailentryid-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="89547-131">See **PR_IPM_SENTMAIL_ENTRYID** ([PidTagIpmSentMailEntryId](pidtagipmsentmailentryid-canonical-property.md)).</span></span>
    
<span data-ttu-id="89547-132">FOLDER_IPM_SUBTREE_VALID</span><span class="sxs-lookup"><span data-stu-id="89547-132">FOLDER_IPM_SUBTREE_VALID</span></span> 
  
> <span data-ttu-id="89547-133">Die Unterstruktur des IPM-Ordners verfügt über einen gültigen Eintragsbezeichner.</span><span class="sxs-lookup"><span data-stu-id="89547-133">The IPM folder subtree has a valid entry identifier.</span></span> <span data-ttu-id="89547-134">Siehe **PR_IPM_SUBTREE_ENTRYID** ([PidTagIpmSubtreeEntryId](pidtagipmsubtreeentryid-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="89547-134">See **PR_IPM_SUBTREE_ENTRYID** ([PidTagIpmSubtreeEntryId](pidtagipmsubtreeentryid-canonical-property.md)).</span></span>
    
<span data-ttu-id="89547-135">FOLDER_IPM_WASTEBASKET_VALID</span><span class="sxs-lookup"><span data-stu-id="89547-135">FOLDER_IPM_WASTEBASKET_VALID</span></span> 
  
> <span data-ttu-id="89547-136">Der Ordner "Gelöschte Elemente" von IPM verfügt über einen gültigen Eintragsbezeichner.</span><span class="sxs-lookup"><span data-stu-id="89547-136">The IPM Deleted Items folder has a valid entry identifier.</span></span> <span data-ttu-id="89547-137">Siehe **PR_IPM_WASTEBASKET_ENTRYID** ([PidTagIpmWastebasketEntryId](pidtagipmwastebasketentryid-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="89547-137">See **PR_IPM_WASTEBASKET_ENTRYID** ([PidTagIpmWastebasketEntryId](pidtagipmwastebasketentryid-canonical-property.md)).</span></span>
    
<span data-ttu-id="89547-138">FOLDER_VIEWS_VALID</span><span class="sxs-lookup"><span data-stu-id="89547-138">FOLDER_VIEWS_VALID</span></span> 
  
> <span data-ttu-id="89547-139">Der Ordner Ansichten verfügt über einen gültigen Eintragsbezeichner.</span><span class="sxs-lookup"><span data-stu-id="89547-139">The views folder has a valid entry identifier.</span></span> <span data-ttu-id="89547-140">Siehe **PR_VIEWS_ENTRYID** ([PidTagViewsEntryId](pidtagviewsentryid-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="89547-140">See **PR_VIEWS_ENTRYID** ([PidTagViewsEntryId](pidtagviewsentryid-canonical-property.md)).</span></span>
    
## <a name="related-resources"></a><span data-ttu-id="89547-141">Verwandte Ressourcen</span><span class="sxs-lookup"><span data-stu-id="89547-141">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="89547-142">Headerdateien</span><span class="sxs-lookup"><span data-stu-id="89547-142">Header files</span></span>

<span data-ttu-id="89547-143">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="89547-143">Mapidefs.h</span></span>
  
> <span data-ttu-id="89547-144">Bietet Datentypdefinitionen.</span><span class="sxs-lookup"><span data-stu-id="89547-144">Provides data type definitions.</span></span>
    
<span data-ttu-id="89547-145">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="89547-145">Mapitags.h</span></span>
  
> <span data-ttu-id="89547-146">Enthält Definitionen von Eigenschaften, die als alternative Namen aufgeführt sind.</span><span class="sxs-lookup"><span data-stu-id="89547-146">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="89547-147">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="89547-147">See also</span></span>



[<span data-ttu-id="89547-148">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="89547-148">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="89547-149">KANONISCHE EIGENSCHAFTEN VON MAPI</span><span class="sxs-lookup"><span data-stu-id="89547-149">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="89547-150">Zuordnen kanonischer Eigenschaftsnamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="89547-150">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="89547-151">Zuordnen von MAPI-Namen zu kanonischen Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="89547-151">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

