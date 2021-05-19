---
title: PidTagDiscardReason (kanonische Eigenschaft)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagDiscardReason
api_type:
- HeaderDef
ms.assetid: 5004dc1f-6bd3-4764-b83c-d04d83161dba
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 32c81474580dbe4948c40390dadd0445776ab825
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33434802"
---
# <a name="pidtagdiscardreason-canonical-property"></a><span data-ttu-id="00311-103">PidTagDiscardReason (kanonische Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="00311-103">PidTagDiscardReason Canonical Property</span></span>

  
  
<span data-ttu-id="00311-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="00311-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="00311-105">Enthält einen Grund, warum ein Nachrichtenübertragungs-Agent (Message Transfer Agent, MTA) eine Nachricht verworfen hat.</span><span class="sxs-lookup"><span data-stu-id="00311-105">Contains a reason why a message transfer agent (MTA) has discarded a message.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="00311-106">Zugeordnete Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="00311-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="00311-107">PR_DISCARD_REASON</span><span class="sxs-lookup"><span data-stu-id="00311-107">PR_DISCARD_REASON</span></span>  <br/> |
|<span data-ttu-id="00311-108">Kennung:</span><span class="sxs-lookup"><span data-stu-id="00311-108">Identifier:</span></span>  <br/> |<span data-ttu-id="00311-109">0x0011</span><span class="sxs-lookup"><span data-stu-id="00311-109">0x0011</span></span>  <br/> |
|<span data-ttu-id="00311-110">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="00311-110">Data type:</span></span>  <br/> |<span data-ttu-id="00311-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="00311-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="00311-112">Bereich:</span><span class="sxs-lookup"><span data-stu-id="00311-112">Area:</span></span>  <br/> |<span data-ttu-id="00311-113">MAPI-Umschlag</span><span class="sxs-lookup"><span data-stu-id="00311-113">MAPI envelope</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="00311-114">Hinweise</span><span class="sxs-lookup"><span data-stu-id="00311-114">Remarks</span></span>

<span data-ttu-id="00311-115">Der in dieser Eigenschaft enthaltene Grund wird in einem Nicht-Löschbericht für die Nachricht verwendet.</span><span class="sxs-lookup"><span data-stu-id="00311-115">The reason contained in this property is used in a nondelivery report for the message.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="00311-116">Verwandte Ressourcen</span><span class="sxs-lookup"><span data-stu-id="00311-116">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="00311-117">Headerdateien</span><span class="sxs-lookup"><span data-stu-id="00311-117">Header files</span></span>

<span data-ttu-id="00311-118">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="00311-118">Mapidefs.h</span></span>
  
> <span data-ttu-id="00311-119">Bietet Datentypdefinitionen.</span><span class="sxs-lookup"><span data-stu-id="00311-119">Provides data type definitions.</span></span>
    
<span data-ttu-id="00311-120">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="00311-120">Mapitags.h</span></span>
  
> <span data-ttu-id="00311-121">Enthält Definitionen von Eigenschaften, die als alternative Namen aufgeführt sind.</span><span class="sxs-lookup"><span data-stu-id="00311-121">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="00311-122">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="00311-122">See also</span></span>



[<span data-ttu-id="00311-123">PidTagNonDeliveryReportReasonCode (kanonische Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="00311-123">PidTagNonDeliveryReportReasonCode Canonical Property</span></span>](pidtagnondeliveryreportreasoncode-canonical-property.md)


[<span data-ttu-id="00311-124">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="00311-124">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="00311-125">KANONISCHE EIGENSCHAFTEN VON MAPI</span><span class="sxs-lookup"><span data-stu-id="00311-125">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="00311-126">Zuordnen kanonischer Eigenschaftsnamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="00311-126">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="00311-127">Zuordnen von MAPI-Namen zu kanonischen Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="00311-127">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

