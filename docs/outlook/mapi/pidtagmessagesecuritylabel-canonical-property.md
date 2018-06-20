---
title: Kanonische PidTagMessageSecurityLabel-Eigenschaft
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagMessageSecurityLabel
api_type:
- HeaderDef
ms.assetid: aae41f1b-19bb-40c7-8564-0c87a5a4e47c
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: 24cf7d8d7b025e5a013ce3a5c1bb03da5ae8a6a3
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19794612"
---
# <a name="pidtagmessagesecuritylabel-canonical-property"></a><span data-ttu-id="90b65-103">Kanonische PidTagMessageSecurityLabel-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="90b65-103">PidTagMessageSecurityLabel Canonical Property</span></span>

  
  
<span data-ttu-id="90b65-104">**Betrifft**: Outlook</span><span class="sxs-lookup"><span data-stu-id="90b65-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="90b65-105">Enthält ein Sicherheitskennzeichen für eine Nachricht an.</span><span class="sxs-lookup"><span data-stu-id="90b65-105">Contains a security label for a message.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="90b65-106">Zugeordneten Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="90b65-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="90b65-107">PR_MESSAGE_SECURITY_LABEL</span><span class="sxs-lookup"><span data-stu-id="90b65-107">PR_MESSAGE_SECURITY_LABEL</span></span>  <br/> |
|<span data-ttu-id="90b65-108">Bezeichner:</span><span class="sxs-lookup"><span data-stu-id="90b65-108">Identifier:</span></span>  <br/> |<span data-ttu-id="90b65-109">0x001E</span><span class="sxs-lookup"><span data-stu-id="90b65-109">0x001E</span></span>  <br/> |
|<span data-ttu-id="90b65-110">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="90b65-110">Data type:</span></span>  <br/> |<span data-ttu-id="90b65-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="90b65-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="90b65-112">Bereich:</span><span class="sxs-lookup"><span data-stu-id="90b65-112">Area:</span></span>  <br/> |<span data-ttu-id="90b65-113">Server</span><span class="sxs-lookup"><span data-stu-id="90b65-113">Server</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="90b65-114">Hinweise</span><span class="sxs-lookup"><span data-stu-id="90b65-114">Remarks</span></span>

<span data-ttu-id="90b65-115">Diese Eigenschaft bietet die Grundlage, auf der die **PR_MESSAGE_TOKEN** ([PidTagMessageToken](pidtagmessagetoken-canonical-property.md))-Eigenschaft eine Nachricht schützt.</span><span class="sxs-lookup"><span data-stu-id="90b65-115">This property provides the basis on which the **PR_MESSAGE_TOKEN** ([PidTagMessageToken](pidtagmessagetoken-canonical-property.md)) property protects a message.</span></span> <span data-ttu-id="90b65-116">Die Verknüpfung mit den Nachrichteninhalt wird durch das Token garantiert.</span><span class="sxs-lookup"><span data-stu-id="90b65-116">Its association with the message content is guaranteed by the token.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="90b65-117">Verwandte Ressourcen</span><span class="sxs-lookup"><span data-stu-id="90b65-117">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="90b65-118">Header-Dateien</span><span class="sxs-lookup"><span data-stu-id="90b65-118">Header files</span></span>

<span data-ttu-id="90b65-119">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="90b65-119">Mapidefs.h</span></span>
  
> <span data-ttu-id="90b65-120">Enthält die Datentypdefinitionen.</span><span class="sxs-lookup"><span data-stu-id="90b65-120">Provides data type definitions.</span></span>
    
<span data-ttu-id="90b65-121">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="90b65-121">Mapitags.h</span></span>
  
> <span data-ttu-id="90b65-122">Enthält Definitionen von Eigenschaften, die als zugeordneten Eigenschaften aufgelistet.</span><span class="sxs-lookup"><span data-stu-id="90b65-122">Contains definitions of properties listed as associated properties.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="90b65-123">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="90b65-123">See also</span></span>



[<span data-ttu-id="90b65-124">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="90b65-124">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="90b65-125">Kanonische MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="90b65-125">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="90b65-126">Zuordnen von kanonischen Eigenschaftennamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="90b65-126">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="90b65-127">Zuordnen von MAPI-Namen zu kanonische Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="90b65-127">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

