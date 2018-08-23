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
ms.openlocfilehash: a8835b7234a209d5cb80a19593632380f6d83826
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2018
ms.locfileid: "22593158"
---
# <a name="pidtagdiscardreason-canonical-property"></a><span data-ttu-id="85fe3-103">PidTagDiscardReason (kanonische Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="85fe3-103">PidTagDiscardReason Canonical Property</span></span>

  
  
<span data-ttu-id="85fe3-104">**Betrifft**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="85fe3-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="85fe3-105">Enthält einen Grund, warum ein Message Transfer Agent (MTA) eine Nachricht gelöscht wurde.</span><span class="sxs-lookup"><span data-stu-id="85fe3-105">Contains a reason why a message transfer agent (MTA) has discarded a message.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="85fe3-106">Zugeordnete Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="85fe3-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="85fe3-107">PR_DISCARD_REASON</span><span class="sxs-lookup"><span data-stu-id="85fe3-107">PR_DISCARD_REASON</span></span>  <br/> |
|<span data-ttu-id="85fe3-108">Kennung:</span><span class="sxs-lookup"><span data-stu-id="85fe3-108">Identifier:</span></span>  <br/> |<span data-ttu-id="85fe3-109">0x0011</span><span class="sxs-lookup"><span data-stu-id="85fe3-109">0x0011</span></span>  <br/> |
|<span data-ttu-id="85fe3-110">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="85fe3-110">Data type:</span></span>  <br/> |<span data-ttu-id="85fe3-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="85fe3-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="85fe3-112">Bereich:</span><span class="sxs-lookup"><span data-stu-id="85fe3-112">Area:</span></span>  <br/> |<span data-ttu-id="85fe3-113">MAPI-Umschlag</span><span class="sxs-lookup"><span data-stu-id="85fe3-113">MAPI envelope</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="85fe3-114">HinwBemerkungeneise</span><span class="sxs-lookup"><span data-stu-id="85fe3-114">Remarks</span></span>

<span data-ttu-id="85fe3-115">Der Grund dafür, die in dieser Eigenschaft enthalten sind, wird in einen Unzustellbarkeitsbericht für die Nachricht verwendet.</span><span class="sxs-lookup"><span data-stu-id="85fe3-115">The reason contained in this property is used in a nondelivery report for the message.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="85fe3-116">Verwandte Ressourcen</span><span class="sxs-lookup"><span data-stu-id="85fe3-116">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="85fe3-117">Header-Dateien</span><span class="sxs-lookup"><span data-stu-id="85fe3-117">Header files</span></span>

<span data-ttu-id="85fe3-118">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="85fe3-118">Mapidefs.h</span></span>
  
> <span data-ttu-id="85fe3-119">Enthält die Datentypdefinitionen.</span><span class="sxs-lookup"><span data-stu-id="85fe3-119">Provides data type definitions.</span></span>
    
<span data-ttu-id="85fe3-120">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="85fe3-120">Mapitags.h</span></span>
  
> <span data-ttu-id="85fe3-121">Enthält Definitionen von Eigenschaften, die als Alternative Namen aufgelistet.</span><span class="sxs-lookup"><span data-stu-id="85fe3-121">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="85fe3-122">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="85fe3-122">See also</span></span>



[<span data-ttu-id="85fe3-123">PidTagNonDeliveryReportReasonCode (kanonische Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="85fe3-123">PidTagNonDeliveryReportReasonCode Canonical Property</span></span>](pidtagnondeliveryreportreasoncode-canonical-property.md)


[<span data-ttu-id="85fe3-124">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="85fe3-124">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="85fe3-125">Kanonische MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="85fe3-125">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="85fe3-126">Zuordnen von kanonischen Eigenschaftennamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="85fe3-126">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="85fe3-127">Zuordnen von MAPI-Namen zu kanonische Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="85fe3-127">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

