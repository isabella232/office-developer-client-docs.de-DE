---
title: Kanonische PidTagValidFolderMask-Eigenschaft
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
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: ae09723c78fe4e333fb5c46e8c79da4b77c0b331
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19795289"
---
# <a name="pidtagvalidfoldermask-canonical-property"></a><span data-ttu-id="06d01-103">Kanonische PidTagValidFolderMask-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="06d01-103">PidTagValidFolderMask Canonical Property</span></span>

  
  
<span data-ttu-id="06d01-104">**Betrifft**: Outlook</span><span class="sxs-lookup"><span data-stu-id="06d01-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="06d01-105">Enthält eine Bitmaske der Flags, die die Gültigkeit der Eintragsbezeichner der Ordner in einem Nachrichtenspeicher angeben.</span><span class="sxs-lookup"><span data-stu-id="06d01-105">Contains a bitmask of flags that indicate the validity of the entry identifiers of the folders in a message store.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="06d01-106">Zugeordneten Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="06d01-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="06d01-107">PR_VALID_FOLDER_MASK</span><span class="sxs-lookup"><span data-stu-id="06d01-107">PR_VALID_FOLDER_MASK</span></span>  <br/> |
|<span data-ttu-id="06d01-108">Bezeichner:</span><span class="sxs-lookup"><span data-stu-id="06d01-108">Identifier:</span></span>  <br/> |<span data-ttu-id="06d01-109">0x35DF</span><span class="sxs-lookup"><span data-stu-id="06d01-109">0x35DF</span></span>  <br/> |
|<span data-ttu-id="06d01-110">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="06d01-110">Data type:</span></span>  <br/> |<span data-ttu-id="06d01-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="06d01-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="06d01-112">Bereich:</span><span class="sxs-lookup"><span data-stu-id="06d01-112">Area:</span></span>  <br/> |<span data-ttu-id="06d01-113">MAPI-Nachrichtenspeicher</span><span class="sxs-lookup"><span data-stu-id="06d01-113">MAPI message store</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="06d01-114">Hinweise</span><span class="sxs-lookup"><span data-stu-id="06d01-114">Remarks</span></span>

<span data-ttu-id="06d01-115">Eintrags-ID für einen Ordner werden ungültig, wenn ein Benutzer auf den Ordner löscht oder der Nachrichtenspeicher beschädigt.</span><span class="sxs-lookup"><span data-stu-id="06d01-115">A folder's entry identifier can become invalid if a user deletes the folder or if the message store becomes corrupted.</span></span>
  
<span data-ttu-id="06d01-116">Für die Bitmaske kann eine oder mehrere der folgenden Werte festgelegt werden:</span><span class="sxs-lookup"><span data-stu-id="06d01-116">One or more of the following flags can be set for the bitmask:</span></span> 
  
<span data-ttu-id="06d01-117">FOLDER_COMMON_VIEWS_VALID</span><span class="sxs-lookup"><span data-stu-id="06d01-117">FOLDER_COMMON_VIEWS_VALID</span></span> 
  
> <span data-ttu-id="06d01-118">Die gemeinsamen Ordner "Ansichten" besitzt eine gültige Eingabe-ID.</span><span class="sxs-lookup"><span data-stu-id="06d01-118">The common views folder has a valid entry identifier.</span></span> <span data-ttu-id="06d01-119">Finden Sie unter **PR_COMMON_VIEWS_ENTRYID** ([PidTagCommonViewsEntryId](pidtagcommonviewsentryid-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="06d01-119">See **PR_COMMON_VIEWS_ENTRYID** ([PidTagCommonViewsEntryId](pidtagcommonviewsentryid-canonical-property.md)).</span></span>
    
<span data-ttu-id="06d01-120">FOLDER_FINDER_VALID</span><span class="sxs-lookup"><span data-stu-id="06d01-120">FOLDER_FINDER_VALID</span></span> 
  
> <span data-ttu-id="06d01-121">Der Finder-Ordner verfügt über eine gültige Eingabe-Bezeichner.</span><span class="sxs-lookup"><span data-stu-id="06d01-121">The finder folder has a valid entry identifier.</span></span> <span data-ttu-id="06d01-122">Finden Sie unter **PR_FINDER_ENTRYID** ([PidTagFinderEntryId](pidtagfinderentryid-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="06d01-122">See **PR_FINDER_ENTRYID** ([PidTagFinderEntryId](pidtagfinderentryid-canonical-property.md)).</span></span> 
    
<span data-ttu-id="06d01-123">FOLDER_IPM_INBOX_VALID</span><span class="sxs-lookup"><span data-stu-id="06d01-123">FOLDER_IPM_INBOX_VALID</span></span> 
  
> <span data-ttu-id="06d01-124">Die zwischen Personen angezeigt (IPM) Ordner verfügt über eine gültige Eingabe-Bezeichner.</span><span class="sxs-lookup"><span data-stu-id="06d01-124">The interpersonal message (IPM) receive folder has a valid entry identifier.</span></span> <span data-ttu-id="06d01-125">Finden Sie unter [IMsgStore::GetReceiveFolder](imsgstore-getreceivefolder.md).</span><span class="sxs-lookup"><span data-stu-id="06d01-125">See [IMsgStore::GetReceiveFolder](imsgstore-getreceivefolder.md).</span></span> 
    
<span data-ttu-id="06d01-126">FOLDER_IPM_OUTBOX_VALID</span><span class="sxs-lookup"><span data-stu-id="06d01-126">FOLDER_IPM_OUTBOX_VALID</span></span> 
  
> <span data-ttu-id="06d01-127">Der Ordner Postausgang IPM besitzt eine gültige Eingabe-ID.</span><span class="sxs-lookup"><span data-stu-id="06d01-127">The IPM Outbox folder has a valid entry identifier.</span></span> <span data-ttu-id="06d01-128">Finden Sie unter **PR_IPM_OUTBOX_ENTRYID** ([PidTagIpmOutboxEntryId](pidtagipmoutboxentryid-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="06d01-128">See **PR_IPM_OUTBOX_ENTRYID** ([PidTagIpmOutboxEntryId](pidtagipmoutboxentryid-canonical-property.md)).</span></span> 
    
<span data-ttu-id="06d01-129">FOLDER_IPM_SENTMAIL_VALID</span><span class="sxs-lookup"><span data-stu-id="06d01-129">FOLDER_IPM_SENTMAIL_VALID</span></span> 
  
> <span data-ttu-id="06d01-130">Ordner Gesendete Objekte IPM verfügt über eine gültige Eingabe-Bezeichner.</span><span class="sxs-lookup"><span data-stu-id="06d01-130">The IPM Sent Items folder has a valid entry identifier.</span></span> <span data-ttu-id="06d01-131">Finden Sie unter **PR_IPM_SENTMAIL_ENTRYID** ([PidTagIpmSentMailEntryId](pidtagipmsentmailentryid-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="06d01-131">See **PR_IPM_SENTMAIL_ENTRYID** ([PidTagIpmSentMailEntryId](pidtagipmsentmailentryid-canonical-property.md)).</span></span>
    
<span data-ttu-id="06d01-132">FOLDER_IPM_SUBTREE_VALID</span><span class="sxs-lookup"><span data-stu-id="06d01-132">FOLDER_IPM_SUBTREE_VALID</span></span> 
  
> <span data-ttu-id="06d01-133">Die IPM Ordner Unterstruktur verfügt über eine gültige Eingabe Bezeichner.</span><span class="sxs-lookup"><span data-stu-id="06d01-133">The IPM folder subtree has a valid entry identifier.</span></span> <span data-ttu-id="06d01-134">Finden Sie unter **PR_IPM_SUBTREE_ENTRYID** ([PidTagIpmSubtreeEntryId](pidtagipmsubtreeentryid-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="06d01-134">See **PR_IPM_SUBTREE_ENTRYID** ([PidTagIpmSubtreeEntryId](pidtagipmsubtreeentryid-canonical-property.md)).</span></span>
    
<span data-ttu-id="06d01-135">FOLDER_IPM_WASTEBASKET_VALID</span><span class="sxs-lookup"><span data-stu-id="06d01-135">FOLDER_IPM_WASTEBASKET_VALID</span></span> 
  
> <span data-ttu-id="06d01-136">Der Ordner Gelöschte Objekte IPM verfügt über eine gültige Eingabe-Bezeichner.</span><span class="sxs-lookup"><span data-stu-id="06d01-136">The IPM Deleted Items folder has a valid entry identifier.</span></span> <span data-ttu-id="06d01-137">Finden Sie unter **PR_IPM_WASTEBASKET_ENTRYID** ([PidTagIpmWastebasketEntryId](pidtagipmwastebasketentryid-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="06d01-137">See **PR_IPM_WASTEBASKET_ENTRYID** ([PidTagIpmWastebasketEntryId](pidtagipmwastebasketentryid-canonical-property.md)).</span></span>
    
<span data-ttu-id="06d01-138">FOLDER_VIEWS_VALID</span><span class="sxs-lookup"><span data-stu-id="06d01-138">FOLDER_VIEWS_VALID</span></span> 
  
> <span data-ttu-id="06d01-139">Ordner "Ansichten" verfügt über eine gültige Eingabe-Bezeichner.</span><span class="sxs-lookup"><span data-stu-id="06d01-139">The views folder has a valid entry identifier.</span></span> <span data-ttu-id="06d01-140">Finden Sie unter **PR_VIEWS_ENTRYID** ([PidTagViewsEntryId](pidtagviewsentryid-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="06d01-140">See **PR_VIEWS_ENTRYID** ([PidTagViewsEntryId](pidtagviewsentryid-canonical-property.md)).</span></span>
    
## <a name="related-resources"></a><span data-ttu-id="06d01-141">Verwandte Ressourcen</span><span class="sxs-lookup"><span data-stu-id="06d01-141">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="06d01-142">Header-Dateien</span><span class="sxs-lookup"><span data-stu-id="06d01-142">Header files</span></span>

<span data-ttu-id="06d01-143">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="06d01-143">Mapidefs.h</span></span>
  
> <span data-ttu-id="06d01-144">Enthält die Datentypdefinitionen.</span><span class="sxs-lookup"><span data-stu-id="06d01-144">Provides data type definitions.</span></span>
    
<span data-ttu-id="06d01-145">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="06d01-145">Mapitags.h</span></span>
  
> <span data-ttu-id="06d01-146">Enthält Definitionen von Eigenschaften, die als Alternative Namen aufgelistet.</span><span class="sxs-lookup"><span data-stu-id="06d01-146">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="06d01-147">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="06d01-147">See also</span></span>



[<span data-ttu-id="06d01-148">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="06d01-148">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="06d01-149">Kanonische MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="06d01-149">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="06d01-150">Zuordnen von kanonischen Eigenschaftennamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="06d01-150">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="06d01-151">Zuordnen von MAPI-Namen zu kanonische Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="06d01-151">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

