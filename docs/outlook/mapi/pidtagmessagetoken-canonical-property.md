---
title: Kanonische PidTagMessageToken-Eigenschaft
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
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: 7357b7b98d90d08f7d14e965458703e4e193f63a
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19794623"
---
# <a name="pidtagmessagetoken-canonical-property"></a><span data-ttu-id="89612-103">Kanonische PidTagMessageToken-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="89612-103">PidTagMessageToken Canonical Property</span></span>

  
  
<span data-ttu-id="89612-104">**Betrifft**: Outlook</span><span class="sxs-lookup"><span data-stu-id="89612-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="89612-105">Ein ASN. 1-Sicherheitstoken für eine Nachricht enthält.</span><span class="sxs-lookup"><span data-stu-id="89612-105">Contains an ASN.1 security token for a message.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="89612-106">Zugeordneten Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="89612-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="89612-107">PR_MESSAGE_TOKEN</span><span class="sxs-lookup"><span data-stu-id="89612-107">PR_MESSAGE_TOKEN</span></span>  <br/> |
|<span data-ttu-id="89612-108">Bezeichner:</span><span class="sxs-lookup"><span data-stu-id="89612-108">Identifier:</span></span>  <br/> |<span data-ttu-id="89612-109">0x0C03</span><span class="sxs-lookup"><span data-stu-id="89612-109">0x0C03</span></span>  <br/> |
|<span data-ttu-id="89612-110">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="89612-110">Data type:</span></span>  <br/> |<span data-ttu-id="89612-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="89612-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="89612-112">Bereich:</span><span class="sxs-lookup"><span data-stu-id="89612-112">Area:</span></span>  <br/> |<span data-ttu-id="89612-113">Secure Messaging-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="89612-113">Secure Messaging Properties</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="89612-114">Hinweise</span><span class="sxs-lookup"><span data-stu-id="89612-114">Remarks</span></span>

<span data-ttu-id="89612-115">Diese Eigenschaft übermittelt geschützte sicherheitsbezogenen Informationen aus den Ersteller an den Empfänger.</span><span class="sxs-lookup"><span data-stu-id="89612-115">This property conveys protected security-related information from its originator to its recipient.</span></span> <span data-ttu-id="89612-116">In Verbindung mit der **PR_MESSAGE_SECURITY_LABEL** ([PidTagMessageSecurityLabel](pidtagmessagesecuritylabel-canonical-property.md))-Eigenschaft garantiert dies Zuordnung mit den Nachrichteninhalt des Bezeichnungsfelds.</span><span class="sxs-lookup"><span data-stu-id="89612-116">In conjunction with the **PR_MESSAGE_SECURITY_LABEL** ([PidTagMessageSecurityLabel](pidtagmessagesecuritylabel-canonical-property.md)) property, it guarantees the label's association with the message content.</span></span> <span data-ttu-id="89612-117">In Verbindung mit der **PR_CONTENT_INTEGRITY_CHECK** ([PidTagContentIntegrityCheck](pidtagcontentintegritycheck-canonical-property.md))-Eigenschaft überprüft es, dass der Inhalt der Nachricht unverändert ist.</span><span class="sxs-lookup"><span data-stu-id="89612-117">In conjunction with the **PR_CONTENT_INTEGRITY_CHECK** ([PidTagContentIntegrityCheck](pidtagcontentintegritycheck-canonical-property.md)) property, it verifies that the message content is unchanged.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="89612-118">Verwandte Ressourcen</span><span class="sxs-lookup"><span data-stu-id="89612-118">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="89612-119">Header-Dateien</span><span class="sxs-lookup"><span data-stu-id="89612-119">Header files</span></span>

<span data-ttu-id="89612-120">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="89612-120">Mapidefs.h</span></span>
  
> <span data-ttu-id="89612-121">Enthält die Datentypdefinitionen.</span><span class="sxs-lookup"><span data-stu-id="89612-121">Provides data type definitions.</span></span>
    
<span data-ttu-id="89612-122">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="89612-122">Mapitags.h</span></span>
  
> <span data-ttu-id="89612-123">Enthält Definitionen von Eigenschaften, die als zugeordneten Eigenschaften aufgelistet.</span><span class="sxs-lookup"><span data-stu-id="89612-123">Contains definitions of properties listed as associated properties.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="89612-124">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="89612-124">See also</span></span>



[<span data-ttu-id="89612-125">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="89612-125">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="89612-126">Kanonische MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="89612-126">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="89612-127">Zuordnen von kanonischen Eigenschaftennamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="89612-127">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="89612-128">Zuordnen von MAPI-Namen zu kanonische Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="89612-128">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

