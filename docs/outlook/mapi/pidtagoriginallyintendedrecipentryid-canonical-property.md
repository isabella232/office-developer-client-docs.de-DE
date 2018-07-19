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
ms.openlocfilehash: 4745318d5666cc3c138f424c94bc2c5e430a61d0
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19794689"
---
# <a name="pidtagoriginallyintendedrecipentryid-canonical-property"></a><span data-ttu-id="21f1b-103">PidTagOriginallyIntendedRecipEntryId (kanonische Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="21f1b-103">PidTagOriginallyIntendedRecipEntryId Canonical Property</span></span>

  
  
<span data-ttu-id="21f1b-104">**Betrifft**: Outlook</span><span class="sxs-lookup"><span data-stu-id="21f1b-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="21f1b-105">Enthält die Eintrags-ID des ursprünglich beabsichtigten Empfänger einer Nachricht automatisch weitergeleitet.</span><span class="sxs-lookup"><span data-stu-id="21f1b-105">Contains the entry identifier of the originally intended recipient of an auto-forwarded message.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="21f1b-106">Zugeordneten Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="21f1b-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="21f1b-107">PR_ORIGINALLY_INTENDED_RECIP_ENTRYID</span><span class="sxs-lookup"><span data-stu-id="21f1b-107">PR_ORIGINALLY_INTENDED_RECIP_ENTRYID</span></span>  <br/> |
|<span data-ttu-id="21f1b-108">Bezeichner:</span><span class="sxs-lookup"><span data-stu-id="21f1b-108">Identifier:</span></span>  <br/> |<span data-ttu-id="21f1b-109">0x1012</span><span class="sxs-lookup"><span data-stu-id="21f1b-109">0x1012</span></span>  <br/> |
|<span data-ttu-id="21f1b-110">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="21f1b-110">Data type:</span></span>  <br/> |<span data-ttu-id="21f1b-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="21f1b-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="21f1b-112">Bereich:</span><span class="sxs-lookup"><span data-stu-id="21f1b-112">Area:</span></span>  <br/> |<span data-ttu-id="21f1b-113">Server</span><span class="sxs-lookup"><span data-stu-id="21f1b-113">Server</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="21f1b-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="21f1b-114">Remarks</span></span>

<span data-ttu-id="21f1b-115">Diese Eigenschaft ist eine Adresse Eigenschaften der ursprünglich beabsichtigten Empfänger.</span><span class="sxs-lookup"><span data-stu-id="21f1b-115">This property is one of the address properties for the originally intended message recipient.</span></span> <span data-ttu-id="21f1b-116">Vom automatische Agent muss festgelegt werden, die die Nachricht weitergeleitet hat.</span><span class="sxs-lookup"><span data-stu-id="21f1b-116">It must be set by the automatic agent that has forwarded the message.</span></span>
  
<span data-ttu-id="21f1b-117">Diese Eigenschaft entspricht dem x. 400-Bericht pro Empfänger-Attribut.</span><span class="sxs-lookup"><span data-stu-id="21f1b-117">This property corresponds to the X.400 report per-recipient attribute.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="21f1b-118">Verwandte Ressourcen</span><span class="sxs-lookup"><span data-stu-id="21f1b-118">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="21f1b-119">Header-Dateien</span><span class="sxs-lookup"><span data-stu-id="21f1b-119">Header files</span></span>

<span data-ttu-id="21f1b-120">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="21f1b-120">Mapidefs.h</span></span>
  
> <span data-ttu-id="21f1b-121">Enthält die Datentypdefinitionen.</span><span class="sxs-lookup"><span data-stu-id="21f1b-121">Provides data type definitions.</span></span>
    
<span data-ttu-id="21f1b-122">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="21f1b-122">Mapitags.h</span></span>
  
> <span data-ttu-id="21f1b-123">Enthält Definitionen von Eigenschaften, die als zugeordneten Eigenschaften aufgelistet.</span><span class="sxs-lookup"><span data-stu-id="21f1b-123">Contains definitions of properties listed as associated properties.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="21f1b-124">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="21f1b-124">See also</span></span>



[<span data-ttu-id="21f1b-125">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="21f1b-125">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="21f1b-126">Kanonische MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="21f1b-126">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="21f1b-127">Zuordnen von kanonischen Eigenschaftennamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="21f1b-127">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="21f1b-128">Zuordnen von MAPI-Namen zu kanonische Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="21f1b-128">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

