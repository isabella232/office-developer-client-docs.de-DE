---
title: PidTagRequestedDeliveryMethod (kanonische Eigenschaft)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagRequestedDeliveryMethod
api_type:
- COM
ms.assetid: cc55089b-e389-405e-8174-f5b5ec352f78
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: f18d726c1b06a6fb7f79964165bbdb9074a6d4d7
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2018
ms.locfileid: "22571367"
---
# <a name="pidtagrequesteddeliverymethod-canonical-property"></a><span data-ttu-id="081a4-103">PidTagRequestedDeliveryMethod (kanonische Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="081a4-103">PidTagRequestedDeliveryMethod Canonical Property</span></span>

  
  
<span data-ttu-id="081a4-104">**Betrifft**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="081a4-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="081a4-105">Diese Eigenschaft enthält ein binäres Array der Übermittlungsmethoden (Dienstanbieter) Rangfolge des Nachrichtenabsenders einer.</span><span class="sxs-lookup"><span data-stu-id="081a4-105">This property contains a binary array of delivery methods (service providers), in the order of a message sender's preference.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="081a4-106">Zugeordnete Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="081a4-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="081a4-107">PR_REQUESTED_DELIVERY_METHOD</span><span class="sxs-lookup"><span data-stu-id="081a4-107">PR_REQUESTED_DELIVERY_METHOD</span></span>  <br/> |
|<span data-ttu-id="081a4-108">Kennung:</span><span class="sxs-lookup"><span data-stu-id="081a4-108">Identifier:</span></span>  <br/> |<span data-ttu-id="081a4-109">0x0C18</span><span class="sxs-lookup"><span data-stu-id="081a4-109">0x0C18</span></span>  <br/> |
|<span data-ttu-id="081a4-110">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="081a4-110">Data type:</span></span>  <br/> |<span data-ttu-id="081a4-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="081a4-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="081a4-112">Bereich:</span><span class="sxs-lookup"><span data-stu-id="081a4-112">Area:</span></span>  <br/> |<span data-ttu-id="081a4-113">MAPI-Empfänger</span><span class="sxs-lookup"><span data-stu-id="081a4-113">MAPI Recipient</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="081a4-114">HinwBemerkungeneise</span><span class="sxs-lookup"><span data-stu-id="081a4-114">Remarks</span></span>

<span data-ttu-id="081a4-115">Die in diesem Objekt enthaltenen Arrays Eigenschaft besteht aus ASN. 1-IDs für die einzelnen-Dienstanbieter.</span><span class="sxs-lookup"><span data-stu-id="081a4-115">The array contained in the this property consists of ASN.1 identifiers for each of the service providers.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="081a4-116">Verwandte Ressourcen</span><span class="sxs-lookup"><span data-stu-id="081a4-116">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="081a4-117">Header-Dateien</span><span class="sxs-lookup"><span data-stu-id="081a4-117">Header files</span></span>

<span data-ttu-id="081a4-118">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="081a4-118">Mapidefs.h</span></span>
  
> <span data-ttu-id="081a4-119">Enthält die Datentypdefinitionen.</span><span class="sxs-lookup"><span data-stu-id="081a4-119">Provides data type definitions.</span></span>
    
<span data-ttu-id="081a4-120">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="081a4-120">Mapitags.h</span></span>
  
> <span data-ttu-id="081a4-121">Enthält Definitionen von Eigenschaften, die als zugeordneten Eigenschaften aufgelistet.</span><span class="sxs-lookup"><span data-stu-id="081a4-121">Contains definitions of properties listed as associated properties.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="081a4-122">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="081a4-122">See also</span></span>



[<span data-ttu-id="081a4-123">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="081a4-123">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="081a4-124">Kanonische MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="081a4-124">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="081a4-125">Zuordnen von kanonischen Eigenschaftennamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="081a4-125">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="081a4-126">Zuordnen von MAPI-Namen zu kanonische Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="081a4-126">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

