---
title: PidTagMessageToken (kanonische Eigenschaft)
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
# <a name="pidtagmessagetoken-canonical-property"></a><span data-ttu-id="b4152-103">PidTagMessageToken (kanonische Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="b4152-103">PidTagMessageToken Canonical Property</span></span>

  
  
<span data-ttu-id="b4152-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="b4152-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="b4152-105">Enthält ein ASN.1-Sicherheitstoken für eine Nachricht.</span><span class="sxs-lookup"><span data-stu-id="b4152-105">Contains an ASN.1 security token for a message.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="b4152-106">Zugeordnete Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="b4152-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="b4152-107">PR_MESSAGE_TOKEN</span><span class="sxs-lookup"><span data-stu-id="b4152-107">PR_MESSAGE_TOKEN</span></span>  <br/> |
|<span data-ttu-id="b4152-108">Kennung:</span><span class="sxs-lookup"><span data-stu-id="b4152-108">Identifier:</span></span>  <br/> |<span data-ttu-id="b4152-109">0x0C03</span><span class="sxs-lookup"><span data-stu-id="b4152-109">0x0C03</span></span>  <br/> |
|<span data-ttu-id="b4152-110">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="b4152-110">Data type:</span></span>  <br/> |<span data-ttu-id="b4152-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="b4152-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="b4152-112">Bereich:</span><span class="sxs-lookup"><span data-stu-id="b4152-112">Area:</span></span>  <br/> |<span data-ttu-id="b4152-113">Secure Messaging-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="b4152-113">Secure Messaging Properties</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="b4152-114">Hinweise</span><span class="sxs-lookup"><span data-stu-id="b4152-114">Remarks</span></span>

<span data-ttu-id="b4152-115">Diese Eigenschaft übermittelt geschützte sicherheitsrelevante Informationen vom Urheber an den Empfänger.</span><span class="sxs-lookup"><span data-stu-id="b4152-115">This property conveys protected security-related information from its originator to its recipient.</span></span> <span data-ttu-id="b4152-116">In Verbindung mit der **PR_MESSAGE_SECURITY_LABEL** ([PidTagMessageSecurityLabel](pidtagmessagesecuritylabel-canonical-property.md)) -Eigenschaft garantiert sie die Zuordnung der Bezeichnung mit dem Nachrichteninhalt.</span><span class="sxs-lookup"><span data-stu-id="b4152-116">In conjunction with the **PR_MESSAGE_SECURITY_LABEL** ([PidTagMessageSecurityLabel](pidtagmessagesecuritylabel-canonical-property.md)) property, it guarantees the label's association with the message content.</span></span> <span data-ttu-id="b4152-117">In Verbindung mit der **PR_CONTENT_INTEGRITY_CHECK** ([PidTagContentIntegrityCheck](pidtagcontentintegritycheck-canonical-property.md))-Eigenschaft wird überprüft, ob der Nachrichteninhalt unverändert ist.</span><span class="sxs-lookup"><span data-stu-id="b4152-117">In conjunction with the **PR_CONTENT_INTEGRITY_CHECK** ([PidTagContentIntegrityCheck](pidtagcontentintegritycheck-canonical-property.md)) property, it verifies that the message content is unchanged.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="b4152-118">Verwandte Ressourcen</span><span class="sxs-lookup"><span data-stu-id="b4152-118">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="b4152-119">Headerdateien</span><span class="sxs-lookup"><span data-stu-id="b4152-119">Header files</span></span>

<span data-ttu-id="b4152-120">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="b4152-120">Mapidefs.h</span></span>
  
> <span data-ttu-id="b4152-121">Bietet Datentypdefinitionen.</span><span class="sxs-lookup"><span data-stu-id="b4152-121">Provides data type definitions.</span></span>
    
<span data-ttu-id="b4152-122">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="b4152-122">Mapitags.h</span></span>
  
> <span data-ttu-id="b4152-123">Enthält Definitionen von Eigenschaften, die als zugeordnete Eigenschaften aufgeführt sind.</span><span class="sxs-lookup"><span data-stu-id="b4152-123">Contains definitions of properties listed as associated properties.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="b4152-124">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="b4152-124">See also</span></span>



[<span data-ttu-id="b4152-125">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="b4152-125">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="b4152-126">KANONISCHE EIGENSCHAFTEN VON MAPI</span><span class="sxs-lookup"><span data-stu-id="b4152-126">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="b4152-127">Zuordnen kanonischer Eigenschaftsnamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="b4152-127">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="b4152-128">Zuordnen von MAPI-Namen zu kanonischen Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="b4152-128">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

