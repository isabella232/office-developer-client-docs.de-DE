---
title: Kanonische Pidtagmessagesecuritylabel (-Eigenschaft
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
ms.openlocfilehash: b6900cbacc2bea6c5519efdc4281ca98629b23bf
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33425673"
---
# <a name="pidtagmessagesecuritylabel-canonical-property"></a><span data-ttu-id="e4b0b-103">Kanonische Pidtagmessagesecuritylabel (-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="e4b0b-103">PidTagMessageSecurityLabel Canonical Property</span></span>

  
  
<span data-ttu-id="e4b0b-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="e4b0b-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="e4b0b-105">Enthält eine Sicherheitsbezeichnung für eine Nachricht.</span><span class="sxs-lookup"><span data-stu-id="e4b0b-105">Contains a security label for a message.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="e4b0b-106">Zugeordnete Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="e4b0b-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="e4b0b-107">PR_MESSAGE_SECURITY_LABEL</span><span class="sxs-lookup"><span data-stu-id="e4b0b-107">PR_MESSAGE_SECURITY_LABEL</span></span>  <br/> |
|<span data-ttu-id="e4b0b-108">Kennung:</span><span class="sxs-lookup"><span data-stu-id="e4b0b-108">Identifier:</span></span>  <br/> |<span data-ttu-id="e4b0b-109">0x001E</span><span class="sxs-lookup"><span data-stu-id="e4b0b-109">0x001E</span></span>  <br/> |
|<span data-ttu-id="e4b0b-110">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="e4b0b-110">Data type:</span></span>  <br/> |<span data-ttu-id="e4b0b-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="e4b0b-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="e4b0b-112">Bereich:</span><span class="sxs-lookup"><span data-stu-id="e4b0b-112">Area:</span></span>  <br/> |<span data-ttu-id="e4b0b-113">Server</span><span class="sxs-lookup"><span data-stu-id="e4b0b-113">Server</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="e4b0b-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="e4b0b-114">Remarks</span></span>

<span data-ttu-id="e4b0b-115">Diese Eigenschaft bietet die Grundlage, auf der die **PR_MESSAGE_TOKEN** ([pidtagmessagetoken (](pidtagmessagetoken-canonical-property.md))-Eigenschaft eine Nachricht schützt.</span><span class="sxs-lookup"><span data-stu-id="e4b0b-115">This property provides the basis on which the **PR_MESSAGE_TOKEN** ([PidTagMessageToken](pidtagmessagetoken-canonical-property.md)) property protects a message.</span></span> <span data-ttu-id="e4b0b-116">Die Zuordnung zum Nachrichteninhalt wird durch das Token gewährleistet.</span><span class="sxs-lookup"><span data-stu-id="e4b0b-116">Its association with the message content is guaranteed by the token.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="e4b0b-117">Verwandte Ressourcen</span><span class="sxs-lookup"><span data-stu-id="e4b0b-117">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="e4b0b-118">Header Dateien</span><span class="sxs-lookup"><span data-stu-id="e4b0b-118">Header files</span></span>

<span data-ttu-id="e4b0b-119">Mapidefs. h</span><span class="sxs-lookup"><span data-stu-id="e4b0b-119">Mapidefs.h</span></span>
  
> <span data-ttu-id="e4b0b-120">Stellt Datentypdefinitionen bereit.</span><span class="sxs-lookup"><span data-stu-id="e4b0b-120">Provides data type definitions.</span></span>
    
<span data-ttu-id="e4b0b-121">Mapitags. h</span><span class="sxs-lookup"><span data-stu-id="e4b0b-121">Mapitags.h</span></span>
  
> <span data-ttu-id="e4b0b-122">Enthält Definitionen von Eigenschaften, die als zugeordnete Eigenschaften aufgelistet sind.</span><span class="sxs-lookup"><span data-stu-id="e4b0b-122">Contains definitions of properties listed as associated properties.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="e4b0b-123">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="e4b0b-123">See also</span></span>



[<span data-ttu-id="e4b0b-124">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="e4b0b-124">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="e4b0b-125">Kanonische MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="e4b0b-125">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="e4b0b-126">Zuordnen von kanonischen Eigenschaftennamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="e4b0b-126">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="e4b0b-127">Zuordnen von MAPI-Namen zu kanonischen Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="e4b0b-127">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

