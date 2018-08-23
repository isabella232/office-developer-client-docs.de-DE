---
title: PidTagNonReceiptNotificationRequested (kanonische Eigenschaft)
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
ms.openlocfilehash: 896cfa2bf8a1b33fd6dee09649853b71618f31be
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2018
ms.locfileid: "22582784"
---
# <a name="pidtagnonreceiptnotificationrequested-canonical-property"></a><span data-ttu-id="721b3-103">PidTagNonReceiptNotificationRequested (kanonische Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="721b3-103">PidTagNonReceiptNotificationRequested Canonical Property</span></span>

  
  
<span data-ttu-id="721b3-104">**Betrifft**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="721b3-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="721b3-105">Enthält True, wenn der Absender einer Nachricht nicht Eingang nach einem bestimmten Empfänger möchte.</span><span class="sxs-lookup"><span data-stu-id="721b3-105">Contains TRUE if a message sender wants notification of non-receipt for a specified recipient.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="721b3-106">Zugeordnete Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="721b3-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="721b3-107">PR_NON_RECEIPT_NOTIFICATION_REQUESTED</span><span class="sxs-lookup"><span data-stu-id="721b3-107">PR_NON_RECEIPT_NOTIFICATION_REQUESTED</span></span>  <br/> |
|<span data-ttu-id="721b3-108">Kennung:</span><span class="sxs-lookup"><span data-stu-id="721b3-108">Identifier:</span></span>  <br/> |<span data-ttu-id="721b3-109">0x0C06</span><span class="sxs-lookup"><span data-stu-id="721b3-109">0x0C06</span></span>  <br/> |
|<span data-ttu-id="721b3-110">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="721b3-110">Data type:</span></span>  <br/> |<span data-ttu-id="721b3-111">PT_BOOLEAN</span><span class="sxs-lookup"><span data-stu-id="721b3-111">PT_BOOLEAN</span></span>  <br/> |
|<span data-ttu-id="721b3-112">Bereich:</span><span class="sxs-lookup"><span data-stu-id="721b3-112">Area:</span></span>  <br/> |<span data-ttu-id="721b3-113">Exchange</span><span class="sxs-lookup"><span data-stu-id="721b3-113">Exchange</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="721b3-114">HinwBemerkungeneise</span><span class="sxs-lookup"><span data-stu-id="721b3-114">Remarks</span></span>

<span data-ttu-id="721b3-115">Wenn diese Eigenschaft FALSE enthält und die **PR_READ_RECEIPT_REQUESTED** ([PidTagReadReceiptRequested](pidtagreadreceiptrequested-canonical-property.md))-Eigenschaft TRUE enthält, der Dienstanbieter überschreiben Sie die Eigenschaft **PR_NON_RECEIPT_NOTIFICATION_REQUESTED** und generieren kann ein Unzustellbarkeitsbericht.</span><span class="sxs-lookup"><span data-stu-id="721b3-115">If this property contains FALSE and the **PR_READ_RECEIPT_REQUESTED** ([PidTagReadReceiptRequested](pidtagreadreceiptrequested-canonical-property.md)) property contains TRUE, the service provider can override the **PR_NON_RECEIPT_NOTIFICATION_REQUESTED** property and generate a non-delivery report.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="721b3-116">Verwandte Ressourcen</span><span class="sxs-lookup"><span data-stu-id="721b3-116">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="721b3-117">Header-Dateien</span><span class="sxs-lookup"><span data-stu-id="721b3-117">Header files</span></span>

<span data-ttu-id="721b3-118">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="721b3-118">Mapidefs.h</span></span>
  
> <span data-ttu-id="721b3-119">Enthält die Datentypdefinitionen.</span><span class="sxs-lookup"><span data-stu-id="721b3-119">Provides data type definitions.</span></span>
    
<span data-ttu-id="721b3-120">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="721b3-120">Mapitags.h</span></span>
  
> <span data-ttu-id="721b3-121">Enthält Definitionen von Eigenschaften, die als zugeordneten Eigenschaften aufgelistet.</span><span class="sxs-lookup"><span data-stu-id="721b3-121">Contains definitions of properties listed as associated properties.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="721b3-122">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="721b3-122">See also</span></span>



[<span data-ttu-id="721b3-123">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="721b3-123">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="721b3-124">Kanonische MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="721b3-124">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="721b3-125">Zuordnen von kanonischen Eigenschaftennamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="721b3-125">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="721b3-126">Zuordnen von MAPI-Namen zu kanonische Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="721b3-126">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

