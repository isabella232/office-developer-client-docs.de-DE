---
title: PidTagOriginallyIntendedRecipEntryId (kanonische Eigenschaft)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagOriginallyIntendedRecipEntryId
api_type:
- COM
ms.assetid: fc288a7a-1927-484e-b860-9cc118672ed2
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 4e7d97f4b2043c9ca08e487e52d58fb534c7abef
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2018
ms.locfileid: "22572655"
---
# <a name="pidtagoriginallyintendedrecipentryid-canonical-property"></a><span data-ttu-id="16a63-103">PidTagOriginallyIntendedRecipEntryId (kanonische Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="16a63-103">PidTagOriginallyIntendedRecipEntryId Canonical Property</span></span>

  
  
<span data-ttu-id="16a63-104">**Betrifft**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="16a63-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="16a63-105">Enthält die Eintrags-ID des ursprünglich beabsichtigten Empfänger einer Nachricht automatisch weitergeleitet.</span><span class="sxs-lookup"><span data-stu-id="16a63-105">Contains the entry identifier of the originally intended recipient of an auto-forwarded message.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="16a63-106">Zugeordnete Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="16a63-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="16a63-107">PR_ORIGINALLY_INTENDED_RECIP_ENTRYID</span><span class="sxs-lookup"><span data-stu-id="16a63-107">PR_ORIGINALLY_INTENDED_RECIP_ENTRYID</span></span>  <br/> |
|<span data-ttu-id="16a63-108">Kennung:</span><span class="sxs-lookup"><span data-stu-id="16a63-108">Identifier:</span></span>  <br/> |<span data-ttu-id="16a63-109">0x1012</span><span class="sxs-lookup"><span data-stu-id="16a63-109">0x1012</span></span>  <br/> |
|<span data-ttu-id="16a63-110">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="16a63-110">Data type:</span></span>  <br/> |<span data-ttu-id="16a63-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="16a63-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="16a63-112">Bereich:</span><span class="sxs-lookup"><span data-stu-id="16a63-112">Area:</span></span>  <br/> |<span data-ttu-id="16a63-113">Server</span><span class="sxs-lookup"><span data-stu-id="16a63-113">Server</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="16a63-114">HinwBemerkungeneise</span><span class="sxs-lookup"><span data-stu-id="16a63-114">Remarks</span></span>

<span data-ttu-id="16a63-115">Diese Eigenschaft ist eine Adresse Eigenschaften der ursprünglich beabsichtigten Empfänger.</span><span class="sxs-lookup"><span data-stu-id="16a63-115">This property is one of the address properties for the originally intended message recipient.</span></span> <span data-ttu-id="16a63-116">Vom automatische Agent muss festgelegt werden, die die Nachricht weitergeleitet hat.</span><span class="sxs-lookup"><span data-stu-id="16a63-116">It must be set by the automatic agent that has forwarded the message.</span></span>
  
<span data-ttu-id="16a63-117">Diese Eigenschaft entspricht dem x. 400-Bericht pro Empfänger-Attribut.</span><span class="sxs-lookup"><span data-stu-id="16a63-117">This property corresponds to the X.400 report per-recipient attribute.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="16a63-118">Verwandte Ressourcen</span><span class="sxs-lookup"><span data-stu-id="16a63-118">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="16a63-119">Header-Dateien</span><span class="sxs-lookup"><span data-stu-id="16a63-119">Header files</span></span>

<span data-ttu-id="16a63-120">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="16a63-120">Mapidefs.h</span></span>
  
> <span data-ttu-id="16a63-121">Enthält die Datentypdefinitionen.</span><span class="sxs-lookup"><span data-stu-id="16a63-121">Provides data type definitions.</span></span>
    
<span data-ttu-id="16a63-122">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="16a63-122">Mapitags.h</span></span>
  
> <span data-ttu-id="16a63-123">Enthält Definitionen von Eigenschaften, die als zugeordneten Eigenschaften aufgelistet.</span><span class="sxs-lookup"><span data-stu-id="16a63-123">Contains definitions of properties listed as associated properties.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="16a63-124">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="16a63-124">See also</span></span>



[<span data-ttu-id="16a63-125">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="16a63-125">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="16a63-126">Kanonische MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="16a63-126">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="16a63-127">Zuordnen von kanonischen Eigenschaftennamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="16a63-127">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="16a63-128">Zuordnen von MAPI-Namen zu kanonische Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="16a63-128">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

