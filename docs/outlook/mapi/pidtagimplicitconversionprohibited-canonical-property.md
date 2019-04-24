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
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: a0e18ef529b65317abd9446408ed73638c792809
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32346606"
---
# <a name="pidtagimplicitconversionprohibited-canonical-property"></a><span data-ttu-id="bd6e4-103">Kanonische Pidtagimplicitconversionprohibited (-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="bd6e4-103">PidTagImplicitConversionProhibited Canonical Property</span></span>

  
  
<span data-ttu-id="bd6e4-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="bd6e4-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="bd6e4-105">Enthält TRUE, wenn für einen MTA (Message Transfer Agent) keine impliziten Nachrichtentext Konvertierungen zulässig sind.</span><span class="sxs-lookup"><span data-stu-id="bd6e4-105">Contains TRUE if a message transfer agent (MTA) is prohibited from making implicit message text conversions.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="bd6e4-106">Zugeordnete Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="bd6e4-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="bd6e4-107">PR_IMPLICIT_CONVERSION_PROHIBITED</span><span class="sxs-lookup"><span data-stu-id="bd6e4-107">PR_IMPLICIT_CONVERSION_PROHIBITED</span></span>  <br/> |
|<span data-ttu-id="bd6e4-108">Kennung:</span><span class="sxs-lookup"><span data-stu-id="bd6e4-108">Identifier:</span></span>  <br/> |<span data-ttu-id="bd6e4-109">0x0016</span><span class="sxs-lookup"><span data-stu-id="bd6e4-109">0x0016</span></span>  <br/> |
|<span data-ttu-id="bd6e4-110">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="bd6e4-110">Data type:</span></span>  <br/> |<span data-ttu-id="bd6e4-111">PT_BOOLEAN</span><span class="sxs-lookup"><span data-stu-id="bd6e4-111">PT_BOOLEAN</span></span>  <br/> |
|<span data-ttu-id="bd6e4-112">Bereich:</span><span class="sxs-lookup"><span data-stu-id="bd6e4-112">Area:</span></span>  <br/> |<span data-ttu-id="bd6e4-113">Server</span><span class="sxs-lookup"><span data-stu-id="bd6e4-113">Server</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="bd6e4-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="bd6e4-114">Remarks</span></span>

<span data-ttu-id="bd6e4-115">Wenn diese Eigenschaft auf TRUE festgelegt ist, darf das Messagingsystem keine Inhaltskonvertierung für die Nachricht durchführen, es sei denn, Sie wird explizit pro Empfänger mit der **PR_EXPLICIT_CONVERSION** ([pidtagexplicitconversion (](pidtagexplicitconversion-canonical-property.md))-Eigenschaft angefordert.</span><span class="sxs-lookup"><span data-stu-id="bd6e4-115">If this property is TRUE, the messaging system must not perform any content conversion on the message unless it is explicitly requested on a per-recipient basis with the **PR_EXPLICIT_CONVERSION** ([PidTagExplicitConversion](pidtagexplicitconversion-canonical-property.md)) property.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="bd6e4-116">Zugehörige Ressourcen</span><span class="sxs-lookup"><span data-stu-id="bd6e4-116">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="bd6e4-117">Header Dateien</span><span class="sxs-lookup"><span data-stu-id="bd6e4-117">Header files</span></span>

<span data-ttu-id="bd6e4-118">Mapidefs. h</span><span class="sxs-lookup"><span data-stu-id="bd6e4-118">Mapidefs.h</span></span>
  
> <span data-ttu-id="bd6e4-119">Stellt Datentypdefinitionen bereit.</span><span class="sxs-lookup"><span data-stu-id="bd6e4-119">Provides data type definitions.</span></span>
    
<span data-ttu-id="bd6e4-120">Mapitags. h</span><span class="sxs-lookup"><span data-stu-id="bd6e4-120">Mapitags.h</span></span>
  
> <span data-ttu-id="bd6e4-121">Enthält Definitionen von Eigenschaften, die als zugeordnete Eigenschaften aufgelistet sind.</span><span class="sxs-lookup"><span data-stu-id="bd6e4-121">Contains definitions of properties listed as associated properties.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="bd6e4-122">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="bd6e4-122">See also</span></span>



[<span data-ttu-id="bd6e4-123">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="bd6e4-123">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="bd6e4-124">Kanonische MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="bd6e4-124">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="bd6e4-125">Zuordnen von kanonischen Eigenschaftennamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="bd6e4-125">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="bd6e4-126">Zuordnen von MAPI-Namen zu kanonischen Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="bd6e4-126">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

