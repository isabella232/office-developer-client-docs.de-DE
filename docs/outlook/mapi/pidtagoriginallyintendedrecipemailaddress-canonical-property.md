---
title: Kanonische Pidtagoriginallyintendedrecipemailaddress (-Eigenschaft
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagOriginallyIntendedRecipEmailAddress
api_type:
- COM
ms.assetid: 6a85b695-731a-4401-9c9c-fda6bc308558
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 4a0e7325618a38addefe562c8207066dfea620f9
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33411372"
---
# <a name="pidtagoriginallyintendedrecipemailaddress-canonical-property"></a><span data-ttu-id="31dd9-103">Kanonische Pidtagoriginallyintendedrecipemailaddress (-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="31dd9-103">PidTagOriginallyIntendedRecipEmailAddress Canonical Property</span></span>

  
  
<span data-ttu-id="31dd9-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="31dd9-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="31dd9-105">Enthält die e-Mail-Adresse des ursprünglich vorgesehenen Empfängers einer AutoForwarded-Nachricht.</span><span class="sxs-lookup"><span data-stu-id="31dd9-105">Contains the email address of the originally intended recipient of an autoforwarded message.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="31dd9-106">Zugeordnete Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="31dd9-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="31dd9-107">PR_ORIGINALLY_INTENDED_RECIP_EMAIL_ADDRESS, PR_ORIGINALLY_INTENDED_RECIP_EMAIL_ADDRESS_A, PR_ORIGINALLY_INTENDED_RECIP_EMAIL_ADDRESS_W</span><span class="sxs-lookup"><span data-stu-id="31dd9-107">PR_ORIGINALLY_INTENDED_RECIP_EMAIL_ADDRESS, PR_ORIGINALLY_INTENDED_RECIP_EMAIL_ADDRESS_A, PR_ORIGINALLY_INTENDED_RECIP_EMAIL_ADDRESS_W</span></span>  <br/> |
|<span data-ttu-id="31dd9-108">Kennung:</span><span class="sxs-lookup"><span data-stu-id="31dd9-108">Identifier:</span></span>  <br/> |<span data-ttu-id="31dd9-109">0x007C</span><span class="sxs-lookup"><span data-stu-id="31dd9-109">0x007C</span></span>  <br/> |
|<span data-ttu-id="31dd9-110">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="31dd9-110">Data type:</span></span>  <br/> |<span data-ttu-id="31dd9-111">PT_STRING8, PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="31dd9-111">PT_STRING8, PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="31dd9-112">Bereich:</span><span class="sxs-lookup"><span data-stu-id="31dd9-112">Area:</span></span>  <br/> |<span data-ttu-id="31dd9-113">Server</span><span class="sxs-lookup"><span data-stu-id="31dd9-113">Server</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="31dd9-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="31dd9-114">Remarks</span></span>

<span data-ttu-id="31dd9-115">Diese Eigenschaften sind Beispiele für die Adresseigenschaften für den ursprünglich beabsichtigten Nachrichtenempfänger.</span><span class="sxs-lookup"><span data-stu-id="31dd9-115">These properties are examples of the address properties for the originally intended message recipient.</span></span> <span data-ttu-id="31dd9-116">Sie müssen vom automatischen Agent festgelegt werden, der die Nachricht weitergeleitet hat.</span><span class="sxs-lookup"><span data-stu-id="31dd9-116">They must be set by the automatic agent that has forwarded the message.</span></span>
  
<span data-ttu-id="31dd9-117">Diese Eigenschaften entsprechen dem Attribut X. 400 pro Empfänger.</span><span class="sxs-lookup"><span data-stu-id="31dd9-117">These properties correspond to the X.400 report per-recipient attribute.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="31dd9-118">Verwandte Ressourcen</span><span class="sxs-lookup"><span data-stu-id="31dd9-118">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="31dd9-119">Header Dateien</span><span class="sxs-lookup"><span data-stu-id="31dd9-119">Header files</span></span>

<span data-ttu-id="31dd9-120">Mapidefs. h</span><span class="sxs-lookup"><span data-stu-id="31dd9-120">Mapidefs.h</span></span>
  
> <span data-ttu-id="31dd9-121">Stellt Datentypdefinitionen bereit.</span><span class="sxs-lookup"><span data-stu-id="31dd9-121">Provides data type definitions.</span></span>
    
<span data-ttu-id="31dd9-122">Mapitags. h</span><span class="sxs-lookup"><span data-stu-id="31dd9-122">Mapitags.h</span></span>
  
> <span data-ttu-id="31dd9-123">Enthält Definitionen von Eigenschaften, die als zugeordnete Eigenschaften aufgelistet sind.</span><span class="sxs-lookup"><span data-stu-id="31dd9-123">Contains definitions of properties listed as associated properties.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="31dd9-124">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="31dd9-124">See also</span></span>



[<span data-ttu-id="31dd9-125">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="31dd9-125">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="31dd9-126">Kanonische MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="31dd9-126">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="31dd9-127">Zuordnen von kanonischen Eigenschaftennamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="31dd9-127">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="31dd9-128">Zuordnen von MAPI-Namen zu kanonischen Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="31dd9-128">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

