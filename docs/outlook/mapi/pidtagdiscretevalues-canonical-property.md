---
title: PidTagDiscreteValues (kanonische Eigenschaft)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagDiscreteValues
api_type:
- HeaderDef
ms.assetid: 958f3cf7-953a-43f4-9102-ad35edf5e813
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 9911d6cee40637a69dfaf432be0e6d42bf38bccd
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19794331"
---
# <a name="pidtagdiscretevalues-canonical-property"></a><span data-ttu-id="89797-103">PidTagDiscreteValues (kanonische Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="89797-103">PidTagDiscreteValues Canonical Property</span></span>

  
  
<span data-ttu-id="89797-104">**Betrifft**: Outlook</span><span class="sxs-lookup"><span data-stu-id="89797-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="89797-105">Enthält True, wenn ein Unzustellbarkeitsbericht zu nur einzelne Mitglieder einer Verteilerliste, anstatt die gesamte Liste angewendet wird.</span><span class="sxs-lookup"><span data-stu-id="89797-105">Contains TRUE if a nondelivery report applies only to discrete members of a distribution list rather than the entire list.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="89797-106">Zugeordneten Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="89797-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="89797-107">PR_DISCRETE_VALUES</span><span class="sxs-lookup"><span data-stu-id="89797-107">PR_DISCRETE_VALUES</span></span>  <br/> |
|<span data-ttu-id="89797-108">Bezeichner:</span><span class="sxs-lookup"><span data-stu-id="89797-108">Identifier:</span></span>  <br/> |<span data-ttu-id="89797-109">0x0E0E</span><span class="sxs-lookup"><span data-stu-id="89797-109">0x0E0E</span></span>  <br/> |
|<span data-ttu-id="89797-110">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="89797-110">Data type:</span></span>  <br/> |<span data-ttu-id="89797-111">PT_BOOLEAN</span><span class="sxs-lookup"><span data-stu-id="89797-111">PT_BOOLEAN</span></span>  <br/> |
|<span data-ttu-id="89797-112">Bereich:</span><span class="sxs-lookup"><span data-stu-id="89797-112">Area:</span></span>  <br/> |<span data-ttu-id="89797-113">MAPI Übertragungseinehit</span><span class="sxs-lookup"><span data-stu-id="89797-113">MAPI non-transmittable</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="89797-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="89797-114">Remarks</span></span>

<span data-ttu-id="89797-115">Diese Eigenschaft wird in einen Unzustellbarkeitsbericht verwendet, wenn die Nachricht an einen oder mehrere Mitglieder von Verteilerlisten nicht übermittelt werden konnte.</span><span class="sxs-lookup"><span data-stu-id="89797-115">This property is used within a nondelivery report when the message could not be delivered to one or more members of a distribution list.</span></span> <span data-ttu-id="89797-116">Dient zur erneuten Begrenzung nur die einzelnen Elemente und nicht die Verteilerliste als Ganzes versucht, ein.</span><span class="sxs-lookup"><span data-stu-id="89797-116">Its purpose is to limit retransmission attempts to only those individual members and not the distribution list as a whole.</span></span> 
  
<span data-ttu-id="89797-117">Die Empfänger ein Unzustellbarkeitsbericht-Tabelle enthält Einträge für alle Empfänger auf denen die Nachricht nicht übermittelt werden konnte und für die Verteilerlisten, falls vorhanden, zu denen sie gehören.</span><span class="sxs-lookup"><span data-stu-id="89797-117">The recipient table of a nondelivery report contains entries for all recipients to whom the message could not be delivered, and also for the distribution lists, if any, to which they belong.</span></span> <span data-ttu-id="89797-118">Der Adressbuchhierarchie sollte diese Eigenschaft für jeden Listeneintrag Verteilung auf TRUE festgelegt, und es sollten die **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) sowie die **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)) und **PR_SEARCH_KEY** ([ Kopieren PidTagSearchKey](pidtagsearchkey-canonical-property.md)) aus der Verteilerliste **PR_ORIGINAL_DISPLAY_NAME** ([PidTagOriginalDisplayName](pidtagoriginaldisplayname-canonical-property.md)), **PR_ORIGINAL_ENTRYID** ([PidTagOriginalEntryId](pidtagoriginalentryid-canonical-property.md)) und **PR_ORIGINAL_SEARCH_KEY** ([ PidTagOriginalSearchKey](pidtagoriginalsearchkey-canonical-property.md)) Eigenschaften für jedes Mitglied der gewünschten Verteilerliste.</span><span class="sxs-lookup"><span data-stu-id="89797-118">The transport provider should set this property to TRUE for each distribution list entry, and it should copy the **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)), **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)), and **PR_SEARCH_KEY** ([PidTagSearchKey](pidtagsearchkey-canonical-property.md)) from the distribution list to **PR_ORIGINAL_DISPLAY_NAME** ([PidTagOriginalDisplayName](pidtagoriginaldisplayname-canonical-property.md)), **PR_ORIGINAL_ENTRYID** ([PidTagOriginalEntryId](pidtagoriginalentryid-canonical-property.md)), and **PR_ORIGINAL_SEARCH_KEY** ([PidTagOriginalSearchKey](pidtagoriginalsearchkey-canonical-property.md)) properties for each member of that distribution list.</span></span> 
  
 <span data-ttu-id="89797-119">**PR_DISCRETE_VALUES** sollte nicht für alle Empfänger Nondelivery Bericht-Eintrag keiner Verteilerliste festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="89797-119">**PR_DISCRETE_VALUES** should not be set for any nondelivery report recipient entry other than a distribution list.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="89797-120">Verwandte Ressourcen</span><span class="sxs-lookup"><span data-stu-id="89797-120">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="89797-121">Header-Dateien</span><span class="sxs-lookup"><span data-stu-id="89797-121">Header files</span></span>

<span data-ttu-id="89797-122">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="89797-122">Mapidefs.h</span></span>
  
> <span data-ttu-id="89797-123">Enthält die Datentypdefinitionen.</span><span class="sxs-lookup"><span data-stu-id="89797-123">Provides data type definitions.</span></span>
    
<span data-ttu-id="89797-124">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="89797-124">Mapitags.h</span></span>
  
> <span data-ttu-id="89797-125">Enthält Definitionen von Eigenschaften, die als zugeordneten Eigenschaften aufgelistet.</span><span class="sxs-lookup"><span data-stu-id="89797-125">Contains definitions of properties listed as associated properties.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="89797-126">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="89797-126">See also</span></span>



[<span data-ttu-id="89797-127">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="89797-127">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="89797-128">Kanonische MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="89797-128">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="89797-129">Zuordnen von kanonischen Eigenschaftennamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="89797-129">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="89797-130">Zuordnen von MAPI-Namen zu kanonische Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="89797-130">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

