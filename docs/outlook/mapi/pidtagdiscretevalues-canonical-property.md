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
ms.openlocfilehash: 6d6974302e3413db3590abbbd3e6567976c6ac72
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33404841"
---
# <a name="pidtagdiscretevalues-canonical-property"></a><span data-ttu-id="6d01b-103">PidTagDiscreteValues (kanonische Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="6d01b-103">PidTagDiscreteValues Canonical Property</span></span>

  
  
<span data-ttu-id="6d01b-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="6d01b-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="6d01b-105">Enthält TRUE, wenn ein Nicht-Verteilerbericht nur für einzelne Mitglieder einer Verteilerliste und nicht für die gesamte Liste gilt.</span><span class="sxs-lookup"><span data-stu-id="6d01b-105">Contains TRUE if a nondelivery report applies only to discrete members of a distribution list rather than the entire list.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="6d01b-106">Zugeordnete Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="6d01b-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="6d01b-107">PR_DISCRETE_VALUES</span><span class="sxs-lookup"><span data-stu-id="6d01b-107">PR_DISCRETE_VALUES</span></span>  <br/> |
|<span data-ttu-id="6d01b-108">Kennung:</span><span class="sxs-lookup"><span data-stu-id="6d01b-108">Identifier:</span></span>  <br/> |<span data-ttu-id="6d01b-109">0x0E0E</span><span class="sxs-lookup"><span data-stu-id="6d01b-109">0x0E0E</span></span>  <br/> |
|<span data-ttu-id="6d01b-110">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="6d01b-110">Data type:</span></span>  <br/> |<span data-ttu-id="6d01b-111">PT_BOOLEAN</span><span class="sxs-lookup"><span data-stu-id="6d01b-111">PT_BOOLEAN</span></span>  <br/> |
|<span data-ttu-id="6d01b-112">Bereich:</span><span class="sxs-lookup"><span data-stu-id="6d01b-112">Area:</span></span>  <br/> |<span data-ttu-id="6d01b-113">MAPI nicht durchlässig</span><span class="sxs-lookup"><span data-stu-id="6d01b-113">MAPI non-transmittable</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="6d01b-114">Hinweise</span><span class="sxs-lookup"><span data-stu-id="6d01b-114">Remarks</span></span>

<span data-ttu-id="6d01b-115">Diese Eigenschaft wird innerhalb eines Nicht-Verteilerberichts verwendet, wenn die Nachricht nicht an ein oder mehrere Mitglieder einer Verteilerliste zugestellt werden konnte.</span><span class="sxs-lookup"><span data-stu-id="6d01b-115">This property is used within a nondelivery report when the message could not be delivered to one or more members of a distribution list.</span></span> <span data-ttu-id="6d01b-116">Ihr Zweck besteht in der Beschränkung der Erneutübertragungsversuche auf die einzelnen Mitglieder und nicht auf die Verteilerliste als Ganzes.</span><span class="sxs-lookup"><span data-stu-id="6d01b-116">Its purpose is to limit retransmission attempts to only those individual members and not the distribution list as a whole.</span></span> 
  
<span data-ttu-id="6d01b-117">Die Empfängertabelle eines Unzustellbarberichts enthält Einträge für alle Empfänger, denen die Nachricht nicht zugestellt werden konnte, sowie für die Verteilerlisten, zu denen sie gehören.</span><span class="sxs-lookup"><span data-stu-id="6d01b-117">The recipient table of a nondelivery report contains entries for all recipients to whom the message could not be delivered, and also for the distribution lists, if any, to which they belong.</span></span> <span data-ttu-id="6d01b-118">Der Transportanbieter sollte diese Eigenschaft für jeden Verteilerlisteneintrag auf TRUE festlegen und die **Eigenschaften PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)), **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)) und **PR_SEARCH_KEY** ( PidTagSearchKey ) aus der Verteilerliste in **PR_ORIGINAL_DISPLAY_NAME** ([PidTagOriginalDisplayName](pidtagoriginaldisplayname-canonical-property.md)), **PR_ORIGINAL_ENTRYID** ([PidTagOriginalEntryId](pidtagoriginalentryid-canonical-property.md)) und **PR_ORIGINAL_SEARCH_KEY** ([PidTagOriginalSearchKey](pidtagoriginalsearchkey-canonical-property.md)) für jedes Mitglied dieser Verteilerliste kopieren.[](pidtagsearchkey-canonical-property.md)</span><span class="sxs-lookup"><span data-stu-id="6d01b-118">The transport provider should set this property to TRUE for each distribution list entry, and it should copy the **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)), **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)), and **PR_SEARCH_KEY** ([PidTagSearchKey](pidtagsearchkey-canonical-property.md)) from the distribution list to **PR_ORIGINAL_DISPLAY_NAME** ([PidTagOriginalDisplayName](pidtagoriginaldisplayname-canonical-property.md)), **PR_ORIGINAL_ENTRYID** ([PidTagOriginalEntryId](pidtagoriginalentryid-canonical-property.md)), and **PR_ORIGINAL_SEARCH_KEY** ([PidTagOriginalSearchKey](pidtagoriginalsearchkey-canonical-property.md)) properties for each member of that distribution list.</span></span> 
  
 <span data-ttu-id="6d01b-119">**PR_DISCRETE_VALUES** sollte nicht für einen anderen Empfängereintrag als eine Verteilerliste festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="6d01b-119">**PR_DISCRETE_VALUES** should not be set for any nondelivery report recipient entry other than a distribution list.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="6d01b-120">Verwandte Ressourcen</span><span class="sxs-lookup"><span data-stu-id="6d01b-120">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="6d01b-121">Headerdateien</span><span class="sxs-lookup"><span data-stu-id="6d01b-121">Header files</span></span>

<span data-ttu-id="6d01b-122">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="6d01b-122">Mapidefs.h</span></span>
  
> <span data-ttu-id="6d01b-123">Bietet Datentypdefinitionen.</span><span class="sxs-lookup"><span data-stu-id="6d01b-123">Provides data type definitions.</span></span>
    
<span data-ttu-id="6d01b-124">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="6d01b-124">Mapitags.h</span></span>
  
> <span data-ttu-id="6d01b-125">Enthält Definitionen von Eigenschaften, die als zugeordnete Eigenschaften aufgeführt sind.</span><span class="sxs-lookup"><span data-stu-id="6d01b-125">Contains definitions of properties listed as associated properties.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="6d01b-126">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="6d01b-126">See also</span></span>



[<span data-ttu-id="6d01b-127">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="6d01b-127">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="6d01b-128">KANONISCHE EIGENSCHAFTEN VON MAPI</span><span class="sxs-lookup"><span data-stu-id="6d01b-128">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="6d01b-129">Zuordnen kanonischer Eigenschaftsnamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="6d01b-129">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="6d01b-130">Zuordnen von MAPI-Namen zu kanonischen Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="6d01b-130">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

