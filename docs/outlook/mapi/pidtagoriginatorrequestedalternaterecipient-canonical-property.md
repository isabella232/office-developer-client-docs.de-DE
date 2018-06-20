---
title: Kanonische PidTagOriginatorRequestedAlternateRecipient-Eigenschaft
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
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: c7abd0ae93c5b38c756ec0915dda6a4cdfcebaa5
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19794747"
---
# <a name="pidtagoriginatorrequestedalternaterecipient-canonical-property"></a><span data-ttu-id="f2a84-103">Kanonische PidTagOriginatorRequestedAlternateRecipient-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="f2a84-103">PidTagOriginatorRequestedAlternateRecipient Canonical Property</span></span>

  
  
<span data-ttu-id="f2a84-104">**Betrifft**: Outlook</span><span class="sxs-lookup"><span data-stu-id="f2a84-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="f2a84-105">Enthält die Eintrags-ID für einen alternativen Empfänger vom Absender festgelegt.</span><span class="sxs-lookup"><span data-stu-id="f2a84-105">Contains an entry identifier for an alternate recipient designated by the sender.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="f2a84-106">Zugeordneten Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="f2a84-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="f2a84-107">PR_ORIGINATOR_REQUESTED_ALTERNATE_RECIPIENT</span><span class="sxs-lookup"><span data-stu-id="f2a84-107">PR_ORIGINATOR_REQUESTED_ALTERNATE_RECIPIENT</span></span>  <br/> |
|<span data-ttu-id="f2a84-108">Bezeichner:</span><span class="sxs-lookup"><span data-stu-id="f2a84-108">Identifier:</span></span>  <br/> |<span data-ttu-id="f2a84-109">0x0C09</span><span class="sxs-lookup"><span data-stu-id="f2a84-109">0x0C09</span></span>  <br/> |
|<span data-ttu-id="f2a84-110">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="f2a84-110">Data type:</span></span>  <br/> |<span data-ttu-id="f2a84-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="f2a84-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="f2a84-112">Bereich:</span><span class="sxs-lookup"><span data-stu-id="f2a84-112">Area:</span></span>  <br/> |<span data-ttu-id="f2a84-113">MIME</span><span class="sxs-lookup"><span data-stu-id="f2a84-113">MIME</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="f2a84-114">Hinweise</span><span class="sxs-lookup"><span data-stu-id="f2a84-114">Remarks</span></span>

<span data-ttu-id="f2a84-115">Diese Eigenschaft wird in Autoforwarded Nachrichten verwendet.</span><span class="sxs-lookup"><span data-stu-id="f2a84-115">This property is used in autoforwarded messages.</span></span> <span data-ttu-id="f2a84-116">Wenn die automatische Weiterleitung nicht zulässig ist oder keine alternativer Empfänger vorgesehen ist, sollte ein Unzustellbarkeitsbericht generiert werden.</span><span class="sxs-lookup"><span data-stu-id="f2a84-116">If autoforwarding is not permitted or if no alternate recipient has been designated, a nondelivery report should be generated.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="f2a84-117">Verwandte Ressourcen</span><span class="sxs-lookup"><span data-stu-id="f2a84-117">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="f2a84-118">Header-Dateien</span><span class="sxs-lookup"><span data-stu-id="f2a84-118">Header files</span></span>

<span data-ttu-id="f2a84-119">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="f2a84-119">Mapidefs.h</span></span>
  
> <span data-ttu-id="f2a84-120">Enthält die Datentypdefinitionen.</span><span class="sxs-lookup"><span data-stu-id="f2a84-120">Provides data type definitions.</span></span>
    
<span data-ttu-id="f2a84-121">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="f2a84-121">Mapitags.h</span></span>
  
> <span data-ttu-id="f2a84-122">Enthält Definitionen von Eigenschaften, die als Alternative Namen aufgelistet.</span><span class="sxs-lookup"><span data-stu-id="f2a84-122">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="f2a84-123">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="f2a84-123">See also</span></span>



[<span data-ttu-id="f2a84-124">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="f2a84-124">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="f2a84-125">Kanonische MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="f2a84-125">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="f2a84-126">Zuordnen von kanonischen Eigenschaftennamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="f2a84-126">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="f2a84-127">Zuordnen von MAPI-Namen zu kanonische Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="f2a84-127">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

