---
title: Kanonische PidTagNonReceiptNotificationRequested-Eigenschaft
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
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: 80c76242df409dbea1b60e423629b5b219e1d57d
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19794644"
---
# <a name="pidtagnonreceiptnotificationrequested-canonical-property"></a><span data-ttu-id="047ee-103">Kanonische PidTagNonReceiptNotificationRequested-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="047ee-103">PidTagNonReceiptNotificationRequested Canonical Property</span></span>

  
  
<span data-ttu-id="047ee-104">**Betrifft**: Outlook</span><span class="sxs-lookup"><span data-stu-id="047ee-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="047ee-105">Enthält True, wenn der Absender einer Nachricht nicht Eingang nach einem bestimmten Empfänger möchte.</span><span class="sxs-lookup"><span data-stu-id="047ee-105">Contains TRUE if a message sender wants notification of non-receipt for a specified recipient.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="047ee-106">Zugeordneten Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="047ee-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="047ee-107">PR_NON_RECEIPT_NOTIFICATION_REQUESTED</span><span class="sxs-lookup"><span data-stu-id="047ee-107">PR_NON_RECEIPT_NOTIFICATION_REQUESTED</span></span>  <br/> |
|<span data-ttu-id="047ee-108">Bezeichner:</span><span class="sxs-lookup"><span data-stu-id="047ee-108">Identifier:</span></span>  <br/> |<span data-ttu-id="047ee-109">0x0C06</span><span class="sxs-lookup"><span data-stu-id="047ee-109">0x0C06</span></span>  <br/> |
|<span data-ttu-id="047ee-110">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="047ee-110">Data type:</span></span>  <br/> |<span data-ttu-id="047ee-111">PT_BOOLEAN</span><span class="sxs-lookup"><span data-stu-id="047ee-111">PT_BOOLEAN</span></span>  <br/> |
|<span data-ttu-id="047ee-112">Bereich:</span><span class="sxs-lookup"><span data-stu-id="047ee-112">Area:</span></span>  <br/> |<span data-ttu-id="047ee-113">Exchange</span><span class="sxs-lookup"><span data-stu-id="047ee-113">Exchange</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="047ee-114">Hinweise</span><span class="sxs-lookup"><span data-stu-id="047ee-114">Remarks</span></span>

<span data-ttu-id="047ee-115">Wenn diese Eigenschaft FALSE enthält und die **PR_READ_RECEIPT_REQUESTED** ([PidTagReadReceiptRequested](pidtagreadreceiptrequested-canonical-property.md))-Eigenschaft TRUE enthält, der Dienstanbieter überschreiben Sie die Eigenschaft **PR_NON_RECEIPT_NOTIFICATION_REQUESTED** und generieren kann ein Unzustellbarkeitsbericht.</span><span class="sxs-lookup"><span data-stu-id="047ee-115">If this property contains FALSE and the **PR_READ_RECEIPT_REQUESTED** ([PidTagReadReceiptRequested](pidtagreadreceiptrequested-canonical-property.md)) property contains TRUE, the service provider can override the **PR_NON_RECEIPT_NOTIFICATION_REQUESTED** property and generate a non-delivery report.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="047ee-116">Verwandte Ressourcen</span><span class="sxs-lookup"><span data-stu-id="047ee-116">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="047ee-117">Header-Dateien</span><span class="sxs-lookup"><span data-stu-id="047ee-117">Header files</span></span>

<span data-ttu-id="047ee-118">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="047ee-118">Mapidefs.h</span></span>
  
> <span data-ttu-id="047ee-119">Enthält die Datentypdefinitionen.</span><span class="sxs-lookup"><span data-stu-id="047ee-119">Provides data type definitions.</span></span>
    
<span data-ttu-id="047ee-120">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="047ee-120">Mapitags.h</span></span>
  
> <span data-ttu-id="047ee-121">Enthält Definitionen von Eigenschaften, die als zugeordneten Eigenschaften aufgelistet.</span><span class="sxs-lookup"><span data-stu-id="047ee-121">Contains definitions of properties listed as associated properties.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="047ee-122">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="047ee-122">See also</span></span>



[<span data-ttu-id="047ee-123">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="047ee-123">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="047ee-124">Kanonische MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="047ee-124">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="047ee-125">Zuordnen von kanonischen Eigenschaftennamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="047ee-125">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="047ee-126">Zuordnen von MAPI-Namen zu kanonische Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="047ee-126">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

