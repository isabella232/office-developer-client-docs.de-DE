---
title: Kanonische PidTagRequestedDeliveryMethod-Eigenschaft
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
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: 8a2199ee2bba8b3b41af7bf26de6cdd3d8d0956e
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19794983"
---
# <a name="pidtagrequesteddeliverymethod-canonical-property"></a><span data-ttu-id="8fa53-103">Kanonische PidTagRequestedDeliveryMethod-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="8fa53-103">PidTagRequestedDeliveryMethod Canonical Property</span></span>

  
  
<span data-ttu-id="8fa53-104">**Betrifft**: Outlook</span><span class="sxs-lookup"><span data-stu-id="8fa53-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="8fa53-105">Diese Eigenschaft enthält ein binäres Array der Übermittlungsmethoden (Dienstanbieter) Rangfolge des Nachrichtenabsenders einer.</span><span class="sxs-lookup"><span data-stu-id="8fa53-105">This property contains a binary array of delivery methods (service providers), in the order of a message sender's preference.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="8fa53-106">Zugeordneten Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="8fa53-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="8fa53-107">PR_REQUESTED_DELIVERY_METHOD</span><span class="sxs-lookup"><span data-stu-id="8fa53-107">PR_REQUESTED_DELIVERY_METHOD</span></span>  <br/> |
|<span data-ttu-id="8fa53-108">Bezeichner:</span><span class="sxs-lookup"><span data-stu-id="8fa53-108">Identifier:</span></span>  <br/> |<span data-ttu-id="8fa53-109">0x0C18</span><span class="sxs-lookup"><span data-stu-id="8fa53-109">0x0C18</span></span>  <br/> |
|<span data-ttu-id="8fa53-110">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="8fa53-110">Data type:</span></span>  <br/> |<span data-ttu-id="8fa53-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="8fa53-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="8fa53-112">Bereich:</span><span class="sxs-lookup"><span data-stu-id="8fa53-112">Area:</span></span>  <br/> |<span data-ttu-id="8fa53-113">MAPI-Empfänger</span><span class="sxs-lookup"><span data-stu-id="8fa53-113">MAPI Recipient</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="8fa53-114">Hinweise</span><span class="sxs-lookup"><span data-stu-id="8fa53-114">Remarks</span></span>

<span data-ttu-id="8fa53-115">Die in diesem Objekt enthaltenen Arrays Eigenschaft besteht aus ASN. 1-IDs für die einzelnen-Dienstanbieter.</span><span class="sxs-lookup"><span data-stu-id="8fa53-115">The array contained in the this property consists of ASN.1 identifiers for each of the service providers.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="8fa53-116">Verwandte Ressourcen</span><span class="sxs-lookup"><span data-stu-id="8fa53-116">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="8fa53-117">Header-Dateien</span><span class="sxs-lookup"><span data-stu-id="8fa53-117">Header files</span></span>

<span data-ttu-id="8fa53-118">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="8fa53-118">Mapidefs.h</span></span>
  
> <span data-ttu-id="8fa53-119">Enthält die Datentypdefinitionen.</span><span class="sxs-lookup"><span data-stu-id="8fa53-119">Provides data type definitions.</span></span>
    
<span data-ttu-id="8fa53-120">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="8fa53-120">Mapitags.h</span></span>
  
> <span data-ttu-id="8fa53-121">Enthält Definitionen von Eigenschaften, die als zugeordneten Eigenschaften aufgelistet.</span><span class="sxs-lookup"><span data-stu-id="8fa53-121">Contains definitions of properties listed as associated properties.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="8fa53-122">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="8fa53-122">See also</span></span>



[<span data-ttu-id="8fa53-123">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="8fa53-123">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="8fa53-124">Kanonische MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="8fa53-124">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="8fa53-125">Zuordnen von kanonischen Eigenschaftennamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="8fa53-125">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="8fa53-126">Zuordnen von MAPI-Namen zu kanonische Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="8fa53-126">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

