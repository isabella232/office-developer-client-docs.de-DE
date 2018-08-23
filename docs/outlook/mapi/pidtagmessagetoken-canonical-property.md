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
ms.openlocfilehash: 6b5def94096f7664169935a062d3b28171fb2919
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2018
ms.locfileid: "22578430"
---
# <a name="pidtagmessagetoken-canonical-property"></a><span data-ttu-id="1e98d-103">PidTagMessageToken (kanonische Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="1e98d-103">PidTagMessageToken Canonical Property</span></span>

  
  
<span data-ttu-id="1e98d-104">**Betrifft**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="1e98d-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="1e98d-105">Ein ASN. 1-Sicherheitstoken für eine Nachricht enthält.</span><span class="sxs-lookup"><span data-stu-id="1e98d-105">Contains an ASN.1 security token for a message.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="1e98d-106">Zugeordnete Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="1e98d-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="1e98d-107">PR_MESSAGE_TOKEN</span><span class="sxs-lookup"><span data-stu-id="1e98d-107">PR_MESSAGE_TOKEN</span></span>  <br/> |
|<span data-ttu-id="1e98d-108">Kennung:</span><span class="sxs-lookup"><span data-stu-id="1e98d-108">Identifier:</span></span>  <br/> |<span data-ttu-id="1e98d-109">0x0C03</span><span class="sxs-lookup"><span data-stu-id="1e98d-109">0x0C03</span></span>  <br/> |
|<span data-ttu-id="1e98d-110">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="1e98d-110">Data type:</span></span>  <br/> |<span data-ttu-id="1e98d-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="1e98d-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="1e98d-112">Bereich:</span><span class="sxs-lookup"><span data-stu-id="1e98d-112">Area:</span></span>  <br/> |<span data-ttu-id="1e98d-113">Secure Messaging-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="1e98d-113">Secure Messaging Properties</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="1e98d-114">HinwBemerkungeneise</span><span class="sxs-lookup"><span data-stu-id="1e98d-114">Remarks</span></span>

<span data-ttu-id="1e98d-115">Diese Eigenschaft übermittelt geschützte sicherheitsbezogenen Informationen aus den Ersteller an den Empfänger.</span><span class="sxs-lookup"><span data-stu-id="1e98d-115">This property conveys protected security-related information from its originator to its recipient.</span></span> <span data-ttu-id="1e98d-116">In Verbindung mit der **PR_MESSAGE_SECURITY_LABEL** ([PidTagMessageSecurityLabel](pidtagmessagesecuritylabel-canonical-property.md))-Eigenschaft garantiert dies Zuordnung mit den Nachrichteninhalt des Bezeichnungsfelds.</span><span class="sxs-lookup"><span data-stu-id="1e98d-116">In conjunction with the **PR_MESSAGE_SECURITY_LABEL** ([PidTagMessageSecurityLabel](pidtagmessagesecuritylabel-canonical-property.md)) property, it guarantees the label's association with the message content.</span></span> <span data-ttu-id="1e98d-117">In Verbindung mit der **PR_CONTENT_INTEGRITY_CHECK** ([PidTagContentIntegrityCheck](pidtagcontentintegritycheck-canonical-property.md))-Eigenschaft überprüft es, dass der Inhalt der Nachricht unverändert ist.</span><span class="sxs-lookup"><span data-stu-id="1e98d-117">In conjunction with the **PR_CONTENT_INTEGRITY_CHECK** ([PidTagContentIntegrityCheck](pidtagcontentintegritycheck-canonical-property.md)) property, it verifies that the message content is unchanged.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="1e98d-118">Verwandte Ressourcen</span><span class="sxs-lookup"><span data-stu-id="1e98d-118">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="1e98d-119">Header-Dateien</span><span class="sxs-lookup"><span data-stu-id="1e98d-119">Header files</span></span>

<span data-ttu-id="1e98d-120">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="1e98d-120">Mapidefs.h</span></span>
  
> <span data-ttu-id="1e98d-121">Enthält die Datentypdefinitionen.</span><span class="sxs-lookup"><span data-stu-id="1e98d-121">Provides data type definitions.</span></span>
    
<span data-ttu-id="1e98d-122">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="1e98d-122">Mapitags.h</span></span>
  
> <span data-ttu-id="1e98d-123">Enthält Definitionen von Eigenschaften, die als zugeordneten Eigenschaften aufgelistet.</span><span class="sxs-lookup"><span data-stu-id="1e98d-123">Contains definitions of properties listed as associated properties.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="1e98d-124">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="1e98d-124">See also</span></span>



[<span data-ttu-id="1e98d-125">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="1e98d-125">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="1e98d-126">Kanonische MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="1e98d-126">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="1e98d-127">Zuordnen von kanonischen Eigenschaftennamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="1e98d-127">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="1e98d-128">Zuordnen von MAPI-Namen zu kanonische Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="1e98d-128">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

