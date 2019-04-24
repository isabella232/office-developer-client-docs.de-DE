---
title: Kanonische Pidtagextendedrulemessagecondition (-Eigenschaft
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagExtendedRuleMessageCondition
api_type:
- HeaderDef
ms.assetid: 891851e1-e4a4-4c20-a26c-7223bcca35f7
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: 7c444485c3a443694e2902343a02da5605bde39f
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32316331"
---
# <a name="pidtagextendedrulemessagecondition-canonical-property"></a><span data-ttu-id="45914-103">Kanonische Pidtagextendedrulemessagecondition (-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="45914-103">PidTagExtendedRuleMessageCondition Canonical Property</span></span>

  
  
<span data-ttu-id="45914-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="45914-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="45914-105">Enthält Informationen zu allen benannten Eigenschaften, die in erweiterten Regelbedingungen enthalten sind.</span><span class="sxs-lookup"><span data-stu-id="45914-105">Contains information about any named properties that are contained inside of extended rule conditions.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="45914-106">Zugeordnete Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="45914-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="45914-107">PR_EXTENDED_RULE_MSG_CONDITION</span><span class="sxs-lookup"><span data-stu-id="45914-107">PR_EXTENDED_RULE_MSG_CONDITION</span></span>  <br/> |
|<span data-ttu-id="45914-108">Kennung:</span><span class="sxs-lookup"><span data-stu-id="45914-108">Identifier:</span></span>  <br/> |<span data-ttu-id="45914-109">0x0E9A</span><span class="sxs-lookup"><span data-stu-id="45914-109">0x0E9A</span></span>  <br/> |
|<span data-ttu-id="45914-110">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="45914-110">Data type:</span></span>  <br/> |<span data-ttu-id="45914-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="45914-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="45914-112">Bereich:</span><span class="sxs-lookup"><span data-stu-id="45914-112">Area:</span></span>  <br/> |<span data-ttu-id="45914-113">Regeln</span><span class="sxs-lookup"><span data-stu-id="45914-113">Rules</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="45914-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="45914-114">Remarks</span></span>

<span data-ttu-id="45914-115">Diese Eigenschaft muss für eine FAI-Nachricht festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="45914-115">This property must be set on an FAI message.</span></span> <span data-ttu-id="45914-116">Sie dient dem gleichen Zweck wie **PR_RULE_CONDITION** ([pidtagrulecondition (](pidtagrulecondition-canonical-property.md)), enthält aber zusätzliche Informationen zu den verwendeten benannten Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="45914-116">It serves the same purpose as **PR_RULE_CONDITION** ([PidTagRuleCondition](pidtagrulecondition-canonical-property.md)), but contains additional information about the named properties used.</span></span> <span data-ttu-id="45914-117">Alle Zeichenfolgenwerte, die in einem beliebigen Teil dieses Condition-Eigenschaftswerts enthalten sind, müssen im Unicode-Format vorliegen.</span><span class="sxs-lookup"><span data-stu-id="45914-117">All string values contained in any part of this condition property value must be in Unicode format.</span></span>
  
<span data-ttu-id="45914-118">Informationen zum Format dieser Binary-Eigenschaft finden Sie unter [[MS-OXORULE]](https://msdn.microsoft.com/library/70ac9436-501e-43e2-9163-20d2b546b886%28Office.15%29.aspx).</span><span class="sxs-lookup"><span data-stu-id="45914-118">For information about the format of this binary property, see [[MS-OXORULE]](https://msdn.microsoft.com/library/70ac9436-501e-43e2-9163-20d2b546b886%28Office.15%29.aspx).</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="45914-119">Zugehörige Ressourcen</span><span class="sxs-lookup"><span data-stu-id="45914-119">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="45914-120">Protokollspezifikationen</span><span class="sxs-lookup"><span data-stu-id="45914-120">Protocol specifications</span></span>

<span data-ttu-id="45914-121">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="45914-121">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="45914-122">Enthält Verweise auf zugehörige Exchange Server-Protokollspezifikationen.</span><span class="sxs-lookup"><span data-stu-id="45914-122">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="45914-123">[[MS-OXORULE]](https://msdn.microsoft.com/library/70ac9436-501e-43e2-9163-20d2b546b886%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="45914-123">[[MS-OXORULE]](https://msdn.microsoft.com/library/70ac9436-501e-43e2-9163-20d2b546b886%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="45914-124">Bearbeitet eingehende e-Mail-Nachrichten auf einem Server.</span><span class="sxs-lookup"><span data-stu-id="45914-124">Manipulates incoming email messages on a server.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="45914-125">Header Dateien</span><span class="sxs-lookup"><span data-stu-id="45914-125">Header files</span></span>

<span data-ttu-id="45914-126">Mapidefs. h</span><span class="sxs-lookup"><span data-stu-id="45914-126">Mapidefs.h</span></span>
  
> <span data-ttu-id="45914-127">Stellt Datentypdefinitionen bereit.</span><span class="sxs-lookup"><span data-stu-id="45914-127">Provides data type definitions.</span></span>
    
<span data-ttu-id="45914-128">Mapitags. h</span><span class="sxs-lookup"><span data-stu-id="45914-128">Mapitags.h</span></span>
  
> <span data-ttu-id="45914-129">Enthält Definitionen von Eigenschaften, die als Alternative Namen aufgeführt sind.</span><span class="sxs-lookup"><span data-stu-id="45914-129">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="45914-130">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="45914-130">See also</span></span>



[<span data-ttu-id="45914-131">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="45914-131">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="45914-132">Kanonische MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="45914-132">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="45914-133">Zuordnen von kanonischen Eigenschaftennamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="45914-133">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="45914-134">Zuordnen von MAPI-Namen zu kanonischen Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="45914-134">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

