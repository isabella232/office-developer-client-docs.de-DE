---
title: PidTagOriginallyIntendedRecipEmailAddress (kanonische Eigenschaft)
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
ms.openlocfilehash: f4adbdfc041ebe5213c384db98343baa82af5b05
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2018
ms.locfileid: "22572725"
---
# <a name="pidtagoriginallyintendedrecipemailaddress-canonical-property"></a><span data-ttu-id="e8764-103">PidTagOriginallyIntendedRecipEmailAddress (kanonische Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="e8764-103">PidTagOriginallyIntendedRecipEmailAddress Canonical Property</span></span>

  
  
<span data-ttu-id="e8764-104">**Betrifft**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="e8764-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="e8764-105">Enthält die e-Mail-Adresse des ursprünglich beabsichtigten Empfänger einer Nachricht Autoforwarded.</span><span class="sxs-lookup"><span data-stu-id="e8764-105">Contains the email address of the originally intended recipient of an autoforwarded message.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="e8764-106">Zugeordnete Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="e8764-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="e8764-107">PR_ORIGINALLY_INTENDED_RECIP_EMAIL_ADDRESS, PR_ORIGINALLY_INTENDED_RECIP_EMAIL_ADDRESS_A, PR_ORIGINALLY_INTENDED_RECIP_EMAIL_ADDRESS_W</span><span class="sxs-lookup"><span data-stu-id="e8764-107">PR_ORIGINALLY_INTENDED_RECIP_EMAIL_ADDRESS, PR_ORIGINALLY_INTENDED_RECIP_EMAIL_ADDRESS_A, PR_ORIGINALLY_INTENDED_RECIP_EMAIL_ADDRESS_W</span></span>  <br/> |
|<span data-ttu-id="e8764-108">Kennung:</span><span class="sxs-lookup"><span data-stu-id="e8764-108">Identifier:</span></span>  <br/> |<span data-ttu-id="e8764-109">0x007C</span><span class="sxs-lookup"><span data-stu-id="e8764-109">0x007C</span></span>  <br/> |
|<span data-ttu-id="e8764-110">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="e8764-110">Data type:</span></span>  <br/> |<span data-ttu-id="e8764-111">PT_STRING8, PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="e8764-111">PT_STRING8, PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="e8764-112">Bereich:</span><span class="sxs-lookup"><span data-stu-id="e8764-112">Area:</span></span>  <br/> |<span data-ttu-id="e8764-113">Server</span><span class="sxs-lookup"><span data-stu-id="e8764-113">Server</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="e8764-114">HinwBemerkungeneise</span><span class="sxs-lookup"><span data-stu-id="e8764-114">Remarks</span></span>

<span data-ttu-id="e8764-115">Diese Eigenschaften sind Beispiele für die Adresseigenschaften für der ursprünglich beabsichtigten Empfänger.</span><span class="sxs-lookup"><span data-stu-id="e8764-115">These properties are examples of the address properties for the originally intended message recipient.</span></span> <span data-ttu-id="e8764-116">Sie müssen vom automatische Agent festgelegt werden, die die Nachricht weitergeleitet hat.</span><span class="sxs-lookup"><span data-stu-id="e8764-116">They must be set by the automatic agent that has forwarded the message.</span></span>
  
<span data-ttu-id="e8764-117">Diese Eigenschaften entsprechen dem x. 400-Bericht pro Empfänger-Attribut.</span><span class="sxs-lookup"><span data-stu-id="e8764-117">These properties correspond to the X.400 report per-recipient attribute.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="e8764-118">Verwandte Ressourcen</span><span class="sxs-lookup"><span data-stu-id="e8764-118">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="e8764-119">Header-Dateien</span><span class="sxs-lookup"><span data-stu-id="e8764-119">Header files</span></span>

<span data-ttu-id="e8764-120">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="e8764-120">Mapidefs.h</span></span>
  
> <span data-ttu-id="e8764-121">Enthält die Datentypdefinitionen.</span><span class="sxs-lookup"><span data-stu-id="e8764-121">Provides data type definitions.</span></span>
    
<span data-ttu-id="e8764-122">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="e8764-122">Mapitags.h</span></span>
  
> <span data-ttu-id="e8764-123">Enthält Definitionen von Eigenschaften, die als zugeordneten Eigenschaften aufgelistet.</span><span class="sxs-lookup"><span data-stu-id="e8764-123">Contains definitions of properties listed as associated properties.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="e8764-124">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="e8764-124">See also</span></span>



[<span data-ttu-id="e8764-125">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="e8764-125">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="e8764-126">Kanonische MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="e8764-126">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="e8764-127">Zuordnen von kanonischen Eigenschaftennamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="e8764-127">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="e8764-128">Zuordnen von MAPI-Namen zu kanonische Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="e8764-128">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

