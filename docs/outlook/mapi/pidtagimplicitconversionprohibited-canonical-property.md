---
title: PidTagImplicitConversionProhibited (kanonische Eigenschaft)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagImplicitConversionProhibited
api_type:
- HeaderDef
ms.assetid: c6cb5a86-0105-4743-9f8e-b832e898da52
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 7635dd24f4fbc5128d3d96556802ab2e3fe56e35
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2018
ms.locfileid: "22571843"
---
# <a name="pidtagimplicitconversionprohibited-canonical-property"></a><span data-ttu-id="b9ea8-103">PidTagImplicitConversionProhibited (kanonische Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="b9ea8-103">PidTagImplicitConversionProhibited Canonical Property</span></span>

  
  
<span data-ttu-id="b9ea8-104">**Betrifft**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="b9ea8-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="b9ea8-105">Enthält True, wenn ein Message Transfer Agent (MTA) tätigen implizite Nachricht Text Konvertierungen verboten wird.</span><span class="sxs-lookup"><span data-stu-id="b9ea8-105">Contains TRUE if a message transfer agent (MTA) is prohibited from making implicit message text conversions.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="b9ea8-106">Zugeordnete Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="b9ea8-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="b9ea8-107">PR_IMPLICIT_CONVERSION_PROHIBITED</span><span class="sxs-lookup"><span data-stu-id="b9ea8-107">PR_IMPLICIT_CONVERSION_PROHIBITED</span></span>  <br/> |
|<span data-ttu-id="b9ea8-108">Kennung:</span><span class="sxs-lookup"><span data-stu-id="b9ea8-108">Identifier:</span></span>  <br/> |<span data-ttu-id="b9ea8-109">0x0016</span><span class="sxs-lookup"><span data-stu-id="b9ea8-109">0x0016</span></span>  <br/> |
|<span data-ttu-id="b9ea8-110">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="b9ea8-110">Data type:</span></span>  <br/> |<span data-ttu-id="b9ea8-111">PT_BOOLEAN</span><span class="sxs-lookup"><span data-stu-id="b9ea8-111">PT_BOOLEAN</span></span>  <br/> |
|<span data-ttu-id="b9ea8-112">Bereich:</span><span class="sxs-lookup"><span data-stu-id="b9ea8-112">Area:</span></span>  <br/> |<span data-ttu-id="b9ea8-113">Server</span><span class="sxs-lookup"><span data-stu-id="b9ea8-113">Server</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="b9ea8-114">HinwBemerkungeneise</span><span class="sxs-lookup"><span data-stu-id="b9ea8-114">Remarks</span></span>

<span data-ttu-id="b9ea8-115">Wenn diese Eigenschaft auf true festgelegt ist, muss das messaging-System keine inhaltskonvertierung für die Nachricht ausführen, wenn es für eine einzelne pro Empfänger mit der **PR_EXPLICIT_CONVERSION** ([PidTagExplicitConversion](pidtagexplicitconversion-canonical-property.md))-Eigenschaft explizit angefordert wird.</span><span class="sxs-lookup"><span data-stu-id="b9ea8-115">If this property is TRUE, the messaging system must not perform any content conversion on the message unless it is explicitly requested on a per-recipient basis with the **PR_EXPLICIT_CONVERSION** ([PidTagExplicitConversion](pidtagexplicitconversion-canonical-property.md)) property.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="b9ea8-116">Verwandte Ressourcen</span><span class="sxs-lookup"><span data-stu-id="b9ea8-116">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="b9ea8-117">Header-Dateien</span><span class="sxs-lookup"><span data-stu-id="b9ea8-117">Header files</span></span>

<span data-ttu-id="b9ea8-118">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="b9ea8-118">Mapidefs.h</span></span>
  
> <span data-ttu-id="b9ea8-119">Enthält die Datentypdefinitionen.</span><span class="sxs-lookup"><span data-stu-id="b9ea8-119">Provides data type definitions.</span></span>
    
<span data-ttu-id="b9ea8-120">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="b9ea8-120">Mapitags.h</span></span>
  
> <span data-ttu-id="b9ea8-121">Enthält Definitionen von Eigenschaften, die als zugeordneten Eigenschaften aufgelistet.</span><span class="sxs-lookup"><span data-stu-id="b9ea8-121">Contains definitions of properties listed as associated properties.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="b9ea8-122">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="b9ea8-122">See also</span></span>



[<span data-ttu-id="b9ea8-123">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="b9ea8-123">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="b9ea8-124">Kanonische MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="b9ea8-124">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="b9ea8-125">Zuordnen von kanonischen Eigenschaftennamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="b9ea8-125">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="b9ea8-126">Zuordnen von MAPI-Namen zu kanonische Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="b9ea8-126">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

