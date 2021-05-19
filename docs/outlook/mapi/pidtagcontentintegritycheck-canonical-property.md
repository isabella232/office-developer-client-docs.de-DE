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
ms.openlocfilehash: 30ed8053c9c3d77f4831da37ddd2456ad0564a5a
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33415726"
---
# <a name="pidtagcontentintegritycheck-canonical-property"></a><span data-ttu-id="a3b70-103">PidTagContentIntegrityCheck (kanonische Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="a3b70-103">PidTagContentIntegrityCheck Canonical Property</span></span>

  
  
<span data-ttu-id="a3b70-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="a3b70-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="a3b70-105">Enthält einen ASN.1-Wert für die Inhaltsintegritätsprüfung, mit dem ein Nachrichtensender Nachrichteninhalte vor der Offenlegung an nicht autorisierte Empfänger schützen kann.</span><span class="sxs-lookup"><span data-stu-id="a3b70-105">Contains an ASN.1 content integrity check value that allows a message sender to protect message content from disclosure to unauthorized recipients.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="a3b70-106">Zugeordnete Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="a3b70-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="a3b70-107">PR_CONTENT_INTEGRITY_CHECK</span><span class="sxs-lookup"><span data-stu-id="a3b70-107">PR_CONTENT_INTEGRITY_CHECK</span></span>  <br/> |
|<span data-ttu-id="a3b70-108">Kennung:</span><span class="sxs-lookup"><span data-stu-id="a3b70-108">Identifier:</span></span>  <br/> |<span data-ttu-id="a3b70-109">0x0C00</span><span class="sxs-lookup"><span data-stu-id="a3b70-109">0x0C00</span></span>  <br/> |
|<span data-ttu-id="a3b70-110">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="a3b70-110">Data type:</span></span>  <br/> |<span data-ttu-id="a3b70-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="a3b70-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="a3b70-112">Bereich:</span><span class="sxs-lookup"><span data-stu-id="a3b70-112">Area:</span></span>  <br/> |<span data-ttu-id="a3b70-113">Exchange</span><span class="sxs-lookup"><span data-stu-id="a3b70-113">Exchange</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="a3b70-114">Hinweise</span><span class="sxs-lookup"><span data-stu-id="a3b70-114">Remarks</span></span>

<span data-ttu-id="a3b70-115">Diese Eigenschaft ermöglicht die Nicht-Ablehnung von Nachrichteninhalten.</span><span class="sxs-lookup"><span data-stu-id="a3b70-115">This property provides for non-repudiation of message content.</span></span> <span data-ttu-id="a3b70-116">In Verbindung mit **PR_MESSAGE_TOKEN** ([PidTagMessageToken](pidtagmessagetoken-canonical-property.md)) wird sichergestellt, dass der Inhalt einer Nachricht unverändert am Ziel eintrifft.</span><span class="sxs-lookup"><span data-stu-id="a3b70-116">In conjunction with **PR_MESSAGE_TOKEN** ([PidTagMessageToken](pidtagmessagetoken-canonical-property.md)), it ensures that the content of a message arrives at its destination unchanged.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="a3b70-117">Verwandte Ressourcen</span><span class="sxs-lookup"><span data-stu-id="a3b70-117">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="a3b70-118">Headerdateien</span><span class="sxs-lookup"><span data-stu-id="a3b70-118">Header files</span></span>

<span data-ttu-id="a3b70-119">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="a3b70-119">Mapidefs.h</span></span>
  
> <span data-ttu-id="a3b70-120">Bietet Datentypdefinitionen.</span><span class="sxs-lookup"><span data-stu-id="a3b70-120">Provides data type definitions.</span></span>
    
<span data-ttu-id="a3b70-121">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="a3b70-121">Mapitags.h</span></span>
  
> <span data-ttu-id="a3b70-122">Enthält Definitionen von Eigenschaften, die als zugeordnete Eigenschaften aufgeführt sind.</span><span class="sxs-lookup"><span data-stu-id="a3b70-122">Contains definitions of properties listed as associated properties.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="a3b70-123">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="a3b70-123">See also</span></span>



[<span data-ttu-id="a3b70-124">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="a3b70-124">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="a3b70-125">KANONISCHE EIGENSCHAFTEN VON MAPI</span><span class="sxs-lookup"><span data-stu-id="a3b70-125">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="a3b70-126">Zuordnen kanonischer Eigenschaftsnamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="a3b70-126">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="a3b70-127">Zuordnen von MAPI-Namen zu kanonischen Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="a3b70-127">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

