---
title: PidTagContentIntegrityCheck (kanonische Eigenschaft)
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
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 53226daafd1c0a53f96db5af3432d6f34738fd93
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2018
ms.locfileid: "22585809"
---
# <a name="pidtagcontentintegritycheck-canonical-property"></a><span data-ttu-id="aab6b-103">PidTagContentIntegrityCheck (kanonische Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="aab6b-103">PidTagContentIntegrityCheck Canonical Property</span></span>

  
  
<span data-ttu-id="aab6b-104">**Betrifft**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="aab6b-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="aab6b-105">Enthält einen ASN. 1 Content-Integrität Kontrollkästchen Wert, der einem Absender der Nachricht um Nachrichteninhalt Offenlegung an nicht autorisierte Empfänger schützen kann.</span><span class="sxs-lookup"><span data-stu-id="aab6b-105">Contains an ASN.1 content integrity check value that allows a message sender to protect message content from disclosure to unauthorized recipients.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="aab6b-106">Zugeordnete Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="aab6b-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="aab6b-107">PR_CONTENT_INTEGRITY_CHECK</span><span class="sxs-lookup"><span data-stu-id="aab6b-107">PR_CONTENT_INTEGRITY_CHECK</span></span>  <br/> |
|<span data-ttu-id="aab6b-108">Kennung:</span><span class="sxs-lookup"><span data-stu-id="aab6b-108">Identifier:</span></span>  <br/> |<span data-ttu-id="aab6b-109">0x0c00</span><span class="sxs-lookup"><span data-stu-id="aab6b-109">0x0C00</span></span>  <br/> |
|<span data-ttu-id="aab6b-110">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="aab6b-110">Data type:</span></span>  <br/> |<span data-ttu-id="aab6b-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="aab6b-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="aab6b-112">Bereich:</span><span class="sxs-lookup"><span data-stu-id="aab6b-112">Area:</span></span>  <br/> |<span data-ttu-id="aab6b-113">Exchange</span><span class="sxs-lookup"><span data-stu-id="aab6b-113">Exchange</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="aab6b-114">HinwBemerkungeneise</span><span class="sxs-lookup"><span data-stu-id="aab6b-114">Remarks</span></span>

<span data-ttu-id="aab6b-115">Diese Eigenschaft bietet Nichtabstreitbarkeit des Nachrichteninhalts.</span><span class="sxs-lookup"><span data-stu-id="aab6b-115">This property provides for non-repudiation of message content.</span></span> <span data-ttu-id="aab6b-116">In Verbindung mit **PR_MESSAGE_TOKEN** ([PidTagMessageToken](pidtagmessagetoken-canonical-property.md)) wird sichergestellt, dass der Inhalt einer Nachricht ihr Ziel unverändert erreicht.</span><span class="sxs-lookup"><span data-stu-id="aab6b-116">In conjunction with **PR_MESSAGE_TOKEN** ([PidTagMessageToken](pidtagmessagetoken-canonical-property.md)), it ensures that the content of a message arrives at its destination unchanged.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="aab6b-117">Verwandte Ressourcen</span><span class="sxs-lookup"><span data-stu-id="aab6b-117">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="aab6b-118">Header-Dateien</span><span class="sxs-lookup"><span data-stu-id="aab6b-118">Header files</span></span>

<span data-ttu-id="aab6b-119">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="aab6b-119">Mapidefs.h</span></span>
  
> <span data-ttu-id="aab6b-120">Enthält die Datentypdefinitionen.</span><span class="sxs-lookup"><span data-stu-id="aab6b-120">Provides data type definitions.</span></span>
    
<span data-ttu-id="aab6b-121">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="aab6b-121">Mapitags.h</span></span>
  
> <span data-ttu-id="aab6b-122">Enthält Definitionen von Eigenschaften, die als zugeordneten Eigenschaften aufgelistet.</span><span class="sxs-lookup"><span data-stu-id="aab6b-122">Contains definitions of properties listed as associated properties.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="aab6b-123">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="aab6b-123">See also</span></span>



[<span data-ttu-id="aab6b-124">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="aab6b-124">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="aab6b-125">Kanonische MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="aab6b-125">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="aab6b-126">Zuordnen von kanonischen Eigenschaftennamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="aab6b-126">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="aab6b-127">Zuordnen von MAPI-Namen zu kanonische Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="aab6b-127">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

