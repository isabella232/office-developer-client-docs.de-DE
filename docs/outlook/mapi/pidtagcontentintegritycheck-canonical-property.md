---
title: Kanonische PidTagContentIntegrityCheck-Eigenschaft
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagContentIntegrityCheck
api_type:
- HeaderDef
ms.assetid: c7f10b8a-6b20-44cf-bde6-8d2b711c1c14
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: 2082db4ccd107fcd02e37882707e4e3ee697695d
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19794235"
---
# <a name="pidtagcontentintegritycheck-canonical-property"></a><span data-ttu-id="fc11d-103">Kanonische PidTagContentIntegrityCheck-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="fc11d-103">PidTagContentIntegrityCheck Canonical Property</span></span>

  
  
<span data-ttu-id="fc11d-104">**Betrifft**: Outlook</span><span class="sxs-lookup"><span data-stu-id="fc11d-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="fc11d-105">Enthält einen ASN. 1 Content-Integrität Kontrollkästchen Wert, der einem Absender der Nachricht um Nachrichteninhalt Offenlegung an nicht autorisierte Empfänger schützen kann.</span><span class="sxs-lookup"><span data-stu-id="fc11d-105">Contains an ASN.1 content integrity check value that allows a message sender to protect message content from disclosure to unauthorized recipients.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="fc11d-106">Zugeordneten Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="fc11d-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="fc11d-107">PR_CONTENT_INTEGRITY_CHECK</span><span class="sxs-lookup"><span data-stu-id="fc11d-107">PR_CONTENT_INTEGRITY_CHECK</span></span>  <br/> |
|<span data-ttu-id="fc11d-108">Bezeichner:</span><span class="sxs-lookup"><span data-stu-id="fc11d-108">Identifier:</span></span>  <br/> |<span data-ttu-id="fc11d-109">0x0c00</span><span class="sxs-lookup"><span data-stu-id="fc11d-109">0x0C00</span></span>  <br/> |
|<span data-ttu-id="fc11d-110">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="fc11d-110">Data type:</span></span>  <br/> |<span data-ttu-id="fc11d-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="fc11d-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="fc11d-112">Bereich:</span><span class="sxs-lookup"><span data-stu-id="fc11d-112">Area:</span></span>  <br/> |<span data-ttu-id="fc11d-113">Exchange</span><span class="sxs-lookup"><span data-stu-id="fc11d-113">Exchange</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="fc11d-114">Hinweise</span><span class="sxs-lookup"><span data-stu-id="fc11d-114">Remarks</span></span>

<span data-ttu-id="fc11d-115">Diese Eigenschaft bietet Nichtabstreitbarkeit des Nachrichteninhalts.</span><span class="sxs-lookup"><span data-stu-id="fc11d-115">This property provides for non-repudiation of message content.</span></span> <span data-ttu-id="fc11d-116">In Verbindung mit **PR_MESSAGE_TOKEN** ([PidTagMessageToken](pidtagmessagetoken-canonical-property.md)) wird sichergestellt, dass der Inhalt einer Nachricht ihr Ziel unverändert erreicht.</span><span class="sxs-lookup"><span data-stu-id="fc11d-116">In conjunction with **PR_MESSAGE_TOKEN** ([PidTagMessageToken](pidtagmessagetoken-canonical-property.md)), it ensures that the content of a message arrives at its destination unchanged.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="fc11d-117">Verwandte Ressourcen</span><span class="sxs-lookup"><span data-stu-id="fc11d-117">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="fc11d-118">Header-Dateien</span><span class="sxs-lookup"><span data-stu-id="fc11d-118">Header files</span></span>

<span data-ttu-id="fc11d-119">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="fc11d-119">Mapidefs.h</span></span>
  
> <span data-ttu-id="fc11d-120">Enthält die Datentypdefinitionen.</span><span class="sxs-lookup"><span data-stu-id="fc11d-120">Provides data type definitions.</span></span>
    
<span data-ttu-id="fc11d-121">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="fc11d-121">Mapitags.h</span></span>
  
> <span data-ttu-id="fc11d-122">Enthält Definitionen von Eigenschaften, die als zugeordneten Eigenschaften aufgelistet.</span><span class="sxs-lookup"><span data-stu-id="fc11d-122">Contains definitions of properties listed as associated properties.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="fc11d-123">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="fc11d-123">See also</span></span>



[<span data-ttu-id="fc11d-124">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="fc11d-124">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="fc11d-125">Kanonische MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="fc11d-125">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="fc11d-126">Zuordnen von kanonischen Eigenschaftennamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="fc11d-126">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="fc11d-127">Zuordnen von MAPI-Namen zu kanonische Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="fc11d-127">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

