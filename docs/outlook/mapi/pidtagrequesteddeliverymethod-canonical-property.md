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
ms.openlocfilehash: ecfed5684ba2166c1c00c1fd07fa074b4ce9fd79
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33434074"
---
# <a name="pidtagrequesteddeliverymethod-canonical-property"></a><span data-ttu-id="19355-103">PidTagRequestedDeliveryMethod (kanonische Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="19355-103">PidTagRequestedDeliveryMethod Canonical Property</span></span>

  
  
<span data-ttu-id="19355-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="19355-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="19355-105">Diese Eigenschaft enthält ein binäres Array von Zustellungsmethoden (Dienstanbietern) in der Reihenfolge der Einstellung eines Nachrichtensenders.</span><span class="sxs-lookup"><span data-stu-id="19355-105">This property contains a binary array of delivery methods (service providers), in the order of a message sender's preference.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="19355-106">Zugeordnete Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="19355-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="19355-107">PR_REQUESTED_DELIVERY_METHOD</span><span class="sxs-lookup"><span data-stu-id="19355-107">PR_REQUESTED_DELIVERY_METHOD</span></span>  <br/> |
|<span data-ttu-id="19355-108">Kennung:</span><span class="sxs-lookup"><span data-stu-id="19355-108">Identifier:</span></span>  <br/> |<span data-ttu-id="19355-109">0x0C18</span><span class="sxs-lookup"><span data-stu-id="19355-109">0x0C18</span></span>  <br/> |
|<span data-ttu-id="19355-110">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="19355-110">Data type:</span></span>  <br/> |<span data-ttu-id="19355-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="19355-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="19355-112">Bereich:</span><span class="sxs-lookup"><span data-stu-id="19355-112">Area:</span></span>  <br/> |<span data-ttu-id="19355-113">MAPI-Empfänger</span><span class="sxs-lookup"><span data-stu-id="19355-113">MAPI Recipient</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="19355-114">Hinweise</span><span class="sxs-lookup"><span data-stu-id="19355-114">Remarks</span></span>

<span data-ttu-id="19355-115">Das array, das in dieser Eigenschaft enthalten ist, besteht aus ASN.1-Bezeichnern für jeden Dienstanbieter.</span><span class="sxs-lookup"><span data-stu-id="19355-115">The array contained in the this property consists of ASN.1 identifiers for each of the service providers.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="19355-116">Verwandte Ressourcen</span><span class="sxs-lookup"><span data-stu-id="19355-116">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="19355-117">Headerdateien</span><span class="sxs-lookup"><span data-stu-id="19355-117">Header files</span></span>

<span data-ttu-id="19355-118">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="19355-118">Mapidefs.h</span></span>
  
> <span data-ttu-id="19355-119">Bietet Datentypdefinitionen.</span><span class="sxs-lookup"><span data-stu-id="19355-119">Provides data type definitions.</span></span>
    
<span data-ttu-id="19355-120">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="19355-120">Mapitags.h</span></span>
  
> <span data-ttu-id="19355-121">Enthält Definitionen von Eigenschaften, die als zugeordnete Eigenschaften aufgeführt sind.</span><span class="sxs-lookup"><span data-stu-id="19355-121">Contains definitions of properties listed as associated properties.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="19355-122">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="19355-122">See also</span></span>



[<span data-ttu-id="19355-123">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="19355-123">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="19355-124">KANONISCHE EIGENSCHAFTEN VON MAPI</span><span class="sxs-lookup"><span data-stu-id="19355-124">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="19355-125">Zuordnen kanonischer Eigenschaftsnamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="19355-125">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="19355-126">Zuordnen von MAPI-Namen zu kanonischen Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="19355-126">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

