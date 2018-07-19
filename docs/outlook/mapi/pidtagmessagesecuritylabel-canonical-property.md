---
title: PidTagMessageSecurityLabel (kanonische Eigenschaft)
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
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 24cf7d8d7b025e5a013ce3a5c1bb03da5ae8a6a3
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19794612"
---
# <a name="pidtagmessagesecuritylabel-canonical-property"></a><span data-ttu-id="5f70b-103">PidTagMessageSecurityLabel (kanonische Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="5f70b-103">PidTagMessageSecurityLabel Canonical Property</span></span>

  
  
<span data-ttu-id="5f70b-104">**Betrifft**: Outlook</span><span class="sxs-lookup"><span data-stu-id="5f70b-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="5f70b-105">Enthält ein Sicherheitskennzeichen für eine Nachricht an.</span><span class="sxs-lookup"><span data-stu-id="5f70b-105">Contains a security label for a message.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="5f70b-106">Zugeordneten Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="5f70b-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="5f70b-107">PR_MESSAGE_SECURITY_LABEL</span><span class="sxs-lookup"><span data-stu-id="5f70b-107">PR_MESSAGE_SECURITY_LABEL</span></span>  <br/> |
|<span data-ttu-id="5f70b-108">Bezeichner:</span><span class="sxs-lookup"><span data-stu-id="5f70b-108">Identifier:</span></span>  <br/> |<span data-ttu-id="5f70b-109">0x001E</span><span class="sxs-lookup"><span data-stu-id="5f70b-109">0x001E</span></span>  <br/> |
|<span data-ttu-id="5f70b-110">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="5f70b-110">Data type:</span></span>  <br/> |<span data-ttu-id="5f70b-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="5f70b-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="5f70b-112">Bereich:</span><span class="sxs-lookup"><span data-stu-id="5f70b-112">Area:</span></span>  <br/> |<span data-ttu-id="5f70b-113">Server</span><span class="sxs-lookup"><span data-stu-id="5f70b-113">Server</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="5f70b-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="5f70b-114">Remarks</span></span>

<span data-ttu-id="5f70b-115">Diese Eigenschaft bietet die Grundlage, auf der die **PR_MESSAGE_TOKEN** ([PidTagMessageToken](pidtagmessagetoken-canonical-property.md))-Eigenschaft eine Nachricht schützt.</span><span class="sxs-lookup"><span data-stu-id="5f70b-115">This property provides the basis on which the **PR_MESSAGE_TOKEN** ([PidTagMessageToken](pidtagmessagetoken-canonical-property.md)) property protects a message.</span></span> <span data-ttu-id="5f70b-116">Die Verknüpfung mit den Nachrichteninhalt wird durch das Token garantiert.</span><span class="sxs-lookup"><span data-stu-id="5f70b-116">Its association with the message content is guaranteed by the token.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="5f70b-117">Verwandte Ressourcen</span><span class="sxs-lookup"><span data-stu-id="5f70b-117">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="5f70b-118">Header-Dateien</span><span class="sxs-lookup"><span data-stu-id="5f70b-118">Header files</span></span>

<span data-ttu-id="5f70b-119">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="5f70b-119">Mapidefs.h</span></span>
  
> <span data-ttu-id="5f70b-120">Enthält die Datentypdefinitionen.</span><span class="sxs-lookup"><span data-stu-id="5f70b-120">Provides data type definitions.</span></span>
    
<span data-ttu-id="5f70b-121">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="5f70b-121">Mapitags.h</span></span>
  
> <span data-ttu-id="5f70b-122">Enthält Definitionen von Eigenschaften, die als zugeordneten Eigenschaften aufgelistet.</span><span class="sxs-lookup"><span data-stu-id="5f70b-122">Contains definitions of properties listed as associated properties.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="5f70b-123">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="5f70b-123">See also</span></span>



[<span data-ttu-id="5f70b-124">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="5f70b-124">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="5f70b-125">Kanonische MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="5f70b-125">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="5f70b-126">Zuordnen von kanonischen Eigenschaftennamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="5f70b-126">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="5f70b-127">Zuordnen von MAPI-Namen zu kanonische Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="5f70b-127">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

