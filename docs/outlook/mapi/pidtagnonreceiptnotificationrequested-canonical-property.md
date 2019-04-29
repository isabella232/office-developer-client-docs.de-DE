---
title: Kanonische Pidtagnonreceiptnotificationrequested (-Eigenschaft
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagNonReceiptNotificationRequested
api_type:
- HeaderDef
ms.assetid: 747f7ba8-42d3-4be3-9908-269e9a347c7f
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 0c6b56a786ea794587e140c9555cc88cd862b489
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33419751"
---
# <a name="pidtagnonreceiptnotificationrequested-canonical-property"></a><span data-ttu-id="fc032-103">Kanonische Pidtagnonreceiptnotificationrequested (-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="fc032-103">PidTagNonReceiptNotificationRequested Canonical Property</span></span>

  
  
<span data-ttu-id="fc032-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="fc032-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="fc032-105">Enthält TRUE, wenn ein Nachrichtenabsender eine Benachrichtigung über den nicht Empfang eines bestimmten Empfängers wünscht.</span><span class="sxs-lookup"><span data-stu-id="fc032-105">Contains TRUE if a message sender wants notification of non-receipt for a specified recipient.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="fc032-106">Zugeordnete Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="fc032-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="fc032-107">PR_NON_RECEIPT_NOTIFICATION_REQUESTED</span><span class="sxs-lookup"><span data-stu-id="fc032-107">PR_NON_RECEIPT_NOTIFICATION_REQUESTED</span></span>  <br/> |
|<span data-ttu-id="fc032-108">Kennung:</span><span class="sxs-lookup"><span data-stu-id="fc032-108">Identifier:</span></span>  <br/> |<span data-ttu-id="fc032-109">0x0C06</span><span class="sxs-lookup"><span data-stu-id="fc032-109">0x0C06</span></span>  <br/> |
|<span data-ttu-id="fc032-110">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="fc032-110">Data type:</span></span>  <br/> |<span data-ttu-id="fc032-111">PT_BOOLEAN</span><span class="sxs-lookup"><span data-stu-id="fc032-111">PT_BOOLEAN</span></span>  <br/> |
|<span data-ttu-id="fc032-112">Bereich:</span><span class="sxs-lookup"><span data-stu-id="fc032-112">Area:</span></span>  <br/> |<span data-ttu-id="fc032-113">Exchange</span><span class="sxs-lookup"><span data-stu-id="fc032-113">Exchange</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="fc032-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="fc032-114">Remarks</span></span>

<span data-ttu-id="fc032-115">Wenn diese Eigenschaft FALSE enthält und die **PR_READ_RECEIPT_REQUESTED** ([pidtagreadreceiptrequested (](pidtagreadreceiptrequested-canonical-property.md))-Eigenschaft true enthält, kann der Dienstanbieter die **PR_NON_RECEIPT_NOTIFICATION_REQUESTED** -Eigenschaft überschreiben und eine Unzustellbarkeitsbericht.</span><span class="sxs-lookup"><span data-stu-id="fc032-115">If this property contains FALSE and the **PR_READ_RECEIPT_REQUESTED** ([PidTagReadReceiptRequested](pidtagreadreceiptrequested-canonical-property.md)) property contains TRUE, the service provider can override the **PR_NON_RECEIPT_NOTIFICATION_REQUESTED** property and generate a non-delivery report.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="fc032-116">Verwandte Ressourcen</span><span class="sxs-lookup"><span data-stu-id="fc032-116">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="fc032-117">Header Dateien</span><span class="sxs-lookup"><span data-stu-id="fc032-117">Header files</span></span>

<span data-ttu-id="fc032-118">Mapidefs. h</span><span class="sxs-lookup"><span data-stu-id="fc032-118">Mapidefs.h</span></span>
  
> <span data-ttu-id="fc032-119">Stellt Datentypdefinitionen bereit.</span><span class="sxs-lookup"><span data-stu-id="fc032-119">Provides data type definitions.</span></span>
    
<span data-ttu-id="fc032-120">Mapitags. h</span><span class="sxs-lookup"><span data-stu-id="fc032-120">Mapitags.h</span></span>
  
> <span data-ttu-id="fc032-121">Enthält Definitionen von Eigenschaften, die als zugeordnete Eigenschaften aufgelistet sind.</span><span class="sxs-lookup"><span data-stu-id="fc032-121">Contains definitions of properties listed as associated properties.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="fc032-122">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="fc032-122">See also</span></span>



[<span data-ttu-id="fc032-123">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="fc032-123">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="fc032-124">Kanonische MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="fc032-124">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="fc032-125">Zuordnen von kanonischen Eigenschaftennamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="fc032-125">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="fc032-126">Zuordnen von MAPI-Namen zu kanonischen Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="fc032-126">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

