---
title: Kanonische Pidtagmessagetoken (-Eigenschaft
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagMessageToken
api_type:
- HeaderDef
ms.assetid: fcb93346-db92-44b5-a447-59fd95f98f45
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 2d832b3a53f8056c034b5e87f1f309fa3058173d
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33408187"
---
# <a name="pidtagmessagetoken-canonical-property"></a><span data-ttu-id="7c1a7-103">Kanonische Pidtagmessagetoken (-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="7c1a7-103">PidTagMessageToken Canonical Property</span></span>

  
  
<span data-ttu-id="7c1a7-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="7c1a7-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="7c1a7-105">Enthält ein ASN. 1-Sicherheitstoken für eine Nachricht.</span><span class="sxs-lookup"><span data-stu-id="7c1a7-105">Contains an ASN.1 security token for a message.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="7c1a7-106">Zugeordnete Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="7c1a7-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="7c1a7-107">PR_MESSAGE_TOKEN</span><span class="sxs-lookup"><span data-stu-id="7c1a7-107">PR_MESSAGE_TOKEN</span></span>  <br/> |
|<span data-ttu-id="7c1a7-108">Kennung:</span><span class="sxs-lookup"><span data-stu-id="7c1a7-108">Identifier:</span></span>  <br/> |<span data-ttu-id="7c1a7-109">0x0C03</span><span class="sxs-lookup"><span data-stu-id="7c1a7-109">0x0C03</span></span>  <br/> |
|<span data-ttu-id="7c1a7-110">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="7c1a7-110">Data type:</span></span>  <br/> |<span data-ttu-id="7c1a7-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="7c1a7-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="7c1a7-112">Bereich:</span><span class="sxs-lookup"><span data-stu-id="7c1a7-112">Area:</span></span>  <br/> |<span data-ttu-id="7c1a7-113">Eigenschaften für sichere Nachrichtenübermittlung</span><span class="sxs-lookup"><span data-stu-id="7c1a7-113">Secure Messaging Properties</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="7c1a7-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="7c1a7-114">Remarks</span></span>

<span data-ttu-id="7c1a7-115">Diese Eigenschaft übermittelt geschützte sicherheitsbezogene Informationen vom Absender an den Empfänger.</span><span class="sxs-lookup"><span data-stu-id="7c1a7-115">This property conveys protected security-related information from its originator to its recipient.</span></span> <span data-ttu-id="7c1a7-116">In Verbindung mit der **PR_MESSAGE_SECURITY_LABEL** ([pidtagmessagesecuritylabel (](pidtagmessagesecuritylabel-canonical-property.md))-Eigenschaft wird die Zuordnung der Bezeichnung zum Nachrichteninhalt garantiert.</span><span class="sxs-lookup"><span data-stu-id="7c1a7-116">In conjunction with the **PR_MESSAGE_SECURITY_LABEL** ([PidTagMessageSecurityLabel](pidtagmessagesecuritylabel-canonical-property.md)) property, it guarantees the label's association with the message content.</span></span> <span data-ttu-id="7c1a7-117">In Verbindung mit der **PR_CONTENT_INTEGRITY_CHECK** ([pidtagcontentintegritycheck (](pidtagcontentintegritycheck-canonical-property.md))-Eigenschaft wird überprüft, ob der Nachrichteninhalt unverändert ist.</span><span class="sxs-lookup"><span data-stu-id="7c1a7-117">In conjunction with the **PR_CONTENT_INTEGRITY_CHECK** ([PidTagContentIntegrityCheck](pidtagcontentintegritycheck-canonical-property.md)) property, it verifies that the message content is unchanged.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="7c1a7-118">Verwandte Ressourcen</span><span class="sxs-lookup"><span data-stu-id="7c1a7-118">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="7c1a7-119">Header Dateien</span><span class="sxs-lookup"><span data-stu-id="7c1a7-119">Header files</span></span>

<span data-ttu-id="7c1a7-120">Mapidefs. h</span><span class="sxs-lookup"><span data-stu-id="7c1a7-120">Mapidefs.h</span></span>
  
> <span data-ttu-id="7c1a7-121">Stellt Datentypdefinitionen bereit.</span><span class="sxs-lookup"><span data-stu-id="7c1a7-121">Provides data type definitions.</span></span>
    
<span data-ttu-id="7c1a7-122">Mapitags. h</span><span class="sxs-lookup"><span data-stu-id="7c1a7-122">Mapitags.h</span></span>
  
> <span data-ttu-id="7c1a7-123">Enthält Definitionen von Eigenschaften, die als zugeordnete Eigenschaften aufgelistet sind.</span><span class="sxs-lookup"><span data-stu-id="7c1a7-123">Contains definitions of properties listed as associated properties.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="7c1a7-124">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="7c1a7-124">See also</span></span>



[<span data-ttu-id="7c1a7-125">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="7c1a7-125">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="7c1a7-126">Kanonische MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="7c1a7-126">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="7c1a7-127">Zuordnen von kanonischen Eigenschaftennamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="7c1a7-127">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="7c1a7-128">Zuordnen von MAPI-Namen zu kanonischen Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="7c1a7-128">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

