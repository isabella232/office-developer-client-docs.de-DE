---
title: Kanonische Pidtagoriginatorrequestedalternaterecipient (-Eigenschaft
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
ms.openlocfilehash: 45cd0e8a95f908d7ef56d03b3ecab5d5df5bcae1
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33437861"
---
# <a name="pidtagoriginatorrequestedalternaterecipient-canonical-property"></a><span data-ttu-id="9ca43-103">Kanonische Pidtagoriginatorrequestedalternaterecipient (-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="9ca43-103">PidTagOriginatorRequestedAlternateRecipient Canonical Property</span></span>

  
  
<span data-ttu-id="9ca43-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="9ca43-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="9ca43-105">Enthält eine Eintrags-ID für einen vom Absender angegebenen alternativen Empfänger.</span><span class="sxs-lookup"><span data-stu-id="9ca43-105">Contains an entry identifier for an alternate recipient designated by the sender.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="9ca43-106">Zugeordnete Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="9ca43-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="9ca43-107">PR_ORIGINATOR_REQUESTED_ALTERNATE_RECIPIENT</span><span class="sxs-lookup"><span data-stu-id="9ca43-107">PR_ORIGINATOR_REQUESTED_ALTERNATE_RECIPIENT</span></span>  <br/> |
|<span data-ttu-id="9ca43-108">Kennung:</span><span class="sxs-lookup"><span data-stu-id="9ca43-108">Identifier:</span></span>  <br/> |<span data-ttu-id="9ca43-109">0x0C09</span><span class="sxs-lookup"><span data-stu-id="9ca43-109">0x0C09</span></span>  <br/> |
|<span data-ttu-id="9ca43-110">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="9ca43-110">Data type:</span></span>  <br/> |<span data-ttu-id="9ca43-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="9ca43-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="9ca43-112">Bereich:</span><span class="sxs-lookup"><span data-stu-id="9ca43-112">Area:</span></span>  <br/> |<span data-ttu-id="9ca43-113">MIME</span><span class="sxs-lookup"><span data-stu-id="9ca43-113">MIME</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="9ca43-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="9ca43-114">Remarks</span></span>

<span data-ttu-id="9ca43-115">Diese Eigenschaft wird in Nachrichten mit Auto Weiterleitung verwendet.</span><span class="sxs-lookup"><span data-stu-id="9ca43-115">This property is used in autoforwarded messages.</span></span> <span data-ttu-id="9ca43-116">Wenn die Auto Weiterleitung nicht zulässig ist oder kein alternativer Empfänger festgelegt wurde, sollte ein Unzustellbarkeitsbericht generiert werden.</span><span class="sxs-lookup"><span data-stu-id="9ca43-116">If autoforwarding is not permitted or if no alternate recipient has been designated, a nondelivery report should be generated.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="9ca43-117">Verwandte Ressourcen</span><span class="sxs-lookup"><span data-stu-id="9ca43-117">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="9ca43-118">Header Dateien</span><span class="sxs-lookup"><span data-stu-id="9ca43-118">Header files</span></span>

<span data-ttu-id="9ca43-119">Mapidefs. h</span><span class="sxs-lookup"><span data-stu-id="9ca43-119">Mapidefs.h</span></span>
  
> <span data-ttu-id="9ca43-120">Stellt Datentypdefinitionen bereit.</span><span class="sxs-lookup"><span data-stu-id="9ca43-120">Provides data type definitions.</span></span>
    
<span data-ttu-id="9ca43-121">Mapitags. h</span><span class="sxs-lookup"><span data-stu-id="9ca43-121">Mapitags.h</span></span>
  
> <span data-ttu-id="9ca43-122">Enthält Definitionen von Eigenschaften, die als Alternative Namen aufgeführt sind.</span><span class="sxs-lookup"><span data-stu-id="9ca43-122">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="9ca43-123">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="9ca43-123">See also</span></span>



[<span data-ttu-id="9ca43-124">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="9ca43-124">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="9ca43-125">Kanonische MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="9ca43-125">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="9ca43-126">Zuordnen von kanonischen Eigenschaftennamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="9ca43-126">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="9ca43-127">Zuordnen von MAPI-Namen zu kanonischen Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="9ca43-127">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

