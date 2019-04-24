---
title: Kanonische Pidtagcontentintegritycheck (-Eigenschaft
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
ms.openlocfilehash: 30ed8053c9c3d77f4831da37ddd2456ad0564a5a
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32331892"
---
# <a name="pidtagcontentintegritycheck-canonical-property"></a><span data-ttu-id="8f100-103">Kanonische Pidtagcontentintegritycheck (-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="8f100-103">PidTagContentIntegrityCheck Canonical Property</span></span>

  
  
<span data-ttu-id="8f100-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="8f100-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="8f100-105">Enthält den Wert "ASN. 1 Content Integrity Check", der es einem Nachrichtenabsender ermöglicht, den Nachrichteninhalt vor der Weitergabe an unbefugte Empfänger zu schützen.</span><span class="sxs-lookup"><span data-stu-id="8f100-105">Contains an ASN.1 content integrity check value that allows a message sender to protect message content from disclosure to unauthorized recipients.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="8f100-106">Zugeordnete Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="8f100-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="8f100-107">PR_CONTENT_INTEGRITY_CHECK</span><span class="sxs-lookup"><span data-stu-id="8f100-107">PR_CONTENT_INTEGRITY_CHECK</span></span>  <br/> |
|<span data-ttu-id="8f100-108">Kennung:</span><span class="sxs-lookup"><span data-stu-id="8f100-108">Identifier:</span></span>  <br/> |<span data-ttu-id="8f100-109">0x0C00</span><span class="sxs-lookup"><span data-stu-id="8f100-109">0x0C00</span></span>  <br/> |
|<span data-ttu-id="8f100-110">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="8f100-110">Data type:</span></span>  <br/> |<span data-ttu-id="8f100-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="8f100-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="8f100-112">Bereich:</span><span class="sxs-lookup"><span data-stu-id="8f100-112">Area:</span></span>  <br/> |<span data-ttu-id="8f100-113">Exchange</span><span class="sxs-lookup"><span data-stu-id="8f100-113">Exchange</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="8f100-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="8f100-114">Remarks</span></span>

<span data-ttu-id="8f100-115">Diese Eigenschaft ermöglicht die nicht Ablehnung des Nachrichteninhalts.</span><span class="sxs-lookup"><span data-stu-id="8f100-115">This property provides for non-repudiation of message content.</span></span> <span data-ttu-id="8f100-116">In Verbindung mit **PR_MESSAGE_TOKEN** ([pidtagmessagetoken (](pidtagmessagetoken-canonical-property.md)) wird sichergestellt, dass der Inhalt einer Nachricht unverändert an seinem Ziel eintrifft.</span><span class="sxs-lookup"><span data-stu-id="8f100-116">In conjunction with **PR_MESSAGE_TOKEN** ([PidTagMessageToken](pidtagmessagetoken-canonical-property.md)), it ensures that the content of a message arrives at its destination unchanged.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="8f100-117">Zugehörige Ressourcen</span><span class="sxs-lookup"><span data-stu-id="8f100-117">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="8f100-118">Header Dateien</span><span class="sxs-lookup"><span data-stu-id="8f100-118">Header files</span></span>

<span data-ttu-id="8f100-119">Mapidefs. h</span><span class="sxs-lookup"><span data-stu-id="8f100-119">Mapidefs.h</span></span>
  
> <span data-ttu-id="8f100-120">Stellt Datentypdefinitionen bereit.</span><span class="sxs-lookup"><span data-stu-id="8f100-120">Provides data type definitions.</span></span>
    
<span data-ttu-id="8f100-121">Mapitags. h</span><span class="sxs-lookup"><span data-stu-id="8f100-121">Mapitags.h</span></span>
  
> <span data-ttu-id="8f100-122">Enthält Definitionen von Eigenschaften, die als zugeordnete Eigenschaften aufgelistet sind.</span><span class="sxs-lookup"><span data-stu-id="8f100-122">Contains definitions of properties listed as associated properties.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="8f100-123">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="8f100-123">See also</span></span>



[<span data-ttu-id="8f100-124">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="8f100-124">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="8f100-125">Kanonische MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="8f100-125">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="8f100-126">Zuordnen von kanonischen Eigenschaftennamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="8f100-126">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="8f100-127">Zuordnen von MAPI-Namen zu kanonischen Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="8f100-127">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

