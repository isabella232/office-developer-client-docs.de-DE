---
title: PidTagOriginatorRequestedAlternateRecipient (kanonische Eigenschaft)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagOriginatorRequestedAlternateRecipient
api_type:
- COM
ms.assetid: c85b7862-18bc-4e17-94db-9097e0ac4a02
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 463f2eb6e730c9250861ce50515a7f662bb75d23
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2018
ms.locfileid: "22588867"
---
# <a name="pidtagoriginatorrequestedalternaterecipient-canonical-property"></a><span data-ttu-id="f8fc8-103">PidTagOriginatorRequestedAlternateRecipient (kanonische Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="f8fc8-103">PidTagOriginatorRequestedAlternateRecipient Canonical Property</span></span>

  
  
<span data-ttu-id="f8fc8-104">**Betrifft**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="f8fc8-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="f8fc8-105">Enthält die Eintrags-ID für einen alternativen Empfänger vom Absender festgelegt.</span><span class="sxs-lookup"><span data-stu-id="f8fc8-105">Contains an entry identifier for an alternate recipient designated by the sender.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="f8fc8-106">Zugeordnete Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="f8fc8-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="f8fc8-107">PR_ORIGINATOR_REQUESTED_ALTERNATE_RECIPIENT</span><span class="sxs-lookup"><span data-stu-id="f8fc8-107">PR_ORIGINATOR_REQUESTED_ALTERNATE_RECIPIENT</span></span>  <br/> |
|<span data-ttu-id="f8fc8-108">Kennung:</span><span class="sxs-lookup"><span data-stu-id="f8fc8-108">Identifier:</span></span>  <br/> |<span data-ttu-id="f8fc8-109">0x0C09</span><span class="sxs-lookup"><span data-stu-id="f8fc8-109">0x0C09</span></span>  <br/> |
|<span data-ttu-id="f8fc8-110">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="f8fc8-110">Data type:</span></span>  <br/> |<span data-ttu-id="f8fc8-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="f8fc8-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="f8fc8-112">Bereich:</span><span class="sxs-lookup"><span data-stu-id="f8fc8-112">Area:</span></span>  <br/> |<span data-ttu-id="f8fc8-113">MIME</span><span class="sxs-lookup"><span data-stu-id="f8fc8-113">MIME</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="f8fc8-114">HinwBemerkungeneise</span><span class="sxs-lookup"><span data-stu-id="f8fc8-114">Remarks</span></span>

<span data-ttu-id="f8fc8-115">Diese Eigenschaft wird in Autoforwarded Nachrichten verwendet.</span><span class="sxs-lookup"><span data-stu-id="f8fc8-115">This property is used in autoforwarded messages.</span></span> <span data-ttu-id="f8fc8-116">Wenn die automatische Weiterleitung nicht zulässig ist oder keine alternativer Empfänger vorgesehen ist, sollte ein Unzustellbarkeitsbericht generiert werden.</span><span class="sxs-lookup"><span data-stu-id="f8fc8-116">If autoforwarding is not permitted or if no alternate recipient has been designated, a nondelivery report should be generated.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="f8fc8-117">Verwandte Ressourcen</span><span class="sxs-lookup"><span data-stu-id="f8fc8-117">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="f8fc8-118">Header-Dateien</span><span class="sxs-lookup"><span data-stu-id="f8fc8-118">Header files</span></span>

<span data-ttu-id="f8fc8-119">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="f8fc8-119">Mapidefs.h</span></span>
  
> <span data-ttu-id="f8fc8-120">Enthält die Datentypdefinitionen.</span><span class="sxs-lookup"><span data-stu-id="f8fc8-120">Provides data type definitions.</span></span>
    
<span data-ttu-id="f8fc8-121">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="f8fc8-121">Mapitags.h</span></span>
  
> <span data-ttu-id="f8fc8-122">Enthält Definitionen von Eigenschaften, die als Alternative Namen aufgelistet.</span><span class="sxs-lookup"><span data-stu-id="f8fc8-122">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="f8fc8-123">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="f8fc8-123">See also</span></span>



[<span data-ttu-id="f8fc8-124">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="f8fc8-124">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="f8fc8-125">Kanonische MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="f8fc8-125">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="f8fc8-126">Zuordnen von kanonischen Eigenschaftennamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="f8fc8-126">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="f8fc8-127">Zuordnen von MAPI-Namen zu kanonische Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="f8fc8-127">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

