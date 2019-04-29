---
title: Kanonische Pidtagimplicitconversionprohibited (-Eigenschaft
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
ms.openlocfilehash: a0e18ef529b65317abd9446408ed73638c792809
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33420668"
---
# <a name="pidtagimplicitconversionprohibited-canonical-property"></a><span data-ttu-id="b694f-103">Kanonische Pidtagimplicitconversionprohibited (-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="b694f-103">PidTagImplicitConversionProhibited Canonical Property</span></span>

  
  
<span data-ttu-id="b694f-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="b694f-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="b694f-105">Enthält TRUE, wenn für einen MTA (Message Transfer Agent) keine impliziten Nachrichtentext Konvertierungen zulässig sind.</span><span class="sxs-lookup"><span data-stu-id="b694f-105">Contains TRUE if a message transfer agent (MTA) is prohibited from making implicit message text conversions.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="b694f-106">Zugeordnete Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="b694f-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="b694f-107">PR_IMPLICIT_CONVERSION_PROHIBITED</span><span class="sxs-lookup"><span data-stu-id="b694f-107">PR_IMPLICIT_CONVERSION_PROHIBITED</span></span>  <br/> |
|<span data-ttu-id="b694f-108">Kennung:</span><span class="sxs-lookup"><span data-stu-id="b694f-108">Identifier:</span></span>  <br/> |<span data-ttu-id="b694f-109">0x0016</span><span class="sxs-lookup"><span data-stu-id="b694f-109">0x0016</span></span>  <br/> |
|<span data-ttu-id="b694f-110">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="b694f-110">Data type:</span></span>  <br/> |<span data-ttu-id="b694f-111">PT_BOOLEAN</span><span class="sxs-lookup"><span data-stu-id="b694f-111">PT_BOOLEAN</span></span>  <br/> |
|<span data-ttu-id="b694f-112">Bereich:</span><span class="sxs-lookup"><span data-stu-id="b694f-112">Area:</span></span>  <br/> |<span data-ttu-id="b694f-113">Server</span><span class="sxs-lookup"><span data-stu-id="b694f-113">Server</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="b694f-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="b694f-114">Remarks</span></span>

<span data-ttu-id="b694f-115">Wenn diese Eigenschaft auf TRUE festgelegt ist, darf das Messagingsystem keine Inhaltskonvertierung für die Nachricht durchführen, es sei denn, Sie wird explizit pro Empfänger mit der **PR_EXPLICIT_CONVERSION** ([pidtagexplicitconversion (](pidtagexplicitconversion-canonical-property.md))-Eigenschaft angefordert.</span><span class="sxs-lookup"><span data-stu-id="b694f-115">If this property is TRUE, the messaging system must not perform any content conversion on the message unless it is explicitly requested on a per-recipient basis with the **PR_EXPLICIT_CONVERSION** ([PidTagExplicitConversion](pidtagexplicitconversion-canonical-property.md)) property.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="b694f-116">Verwandte Ressourcen</span><span class="sxs-lookup"><span data-stu-id="b694f-116">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="b694f-117">Header Dateien</span><span class="sxs-lookup"><span data-stu-id="b694f-117">Header files</span></span>

<span data-ttu-id="b694f-118">Mapidefs. h</span><span class="sxs-lookup"><span data-stu-id="b694f-118">Mapidefs.h</span></span>
  
> <span data-ttu-id="b694f-119">Stellt Datentypdefinitionen bereit.</span><span class="sxs-lookup"><span data-stu-id="b694f-119">Provides data type definitions.</span></span>
    
<span data-ttu-id="b694f-120">Mapitags. h</span><span class="sxs-lookup"><span data-stu-id="b694f-120">Mapitags.h</span></span>
  
> <span data-ttu-id="b694f-121">Enthält Definitionen von Eigenschaften, die als zugeordnete Eigenschaften aufgelistet sind.</span><span class="sxs-lookup"><span data-stu-id="b694f-121">Contains definitions of properties listed as associated properties.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="b694f-122">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="b694f-122">See also</span></span>



[<span data-ttu-id="b694f-123">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="b694f-123">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="b694f-124">Kanonische MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="b694f-124">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="b694f-125">Zuordnen von kanonischen Eigenschaftennamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="b694f-125">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="b694f-126">Zuordnen von MAPI-Namen zu kanonischen Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="b694f-126">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

