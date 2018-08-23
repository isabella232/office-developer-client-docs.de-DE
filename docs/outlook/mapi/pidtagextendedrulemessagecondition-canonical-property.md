---
title: PidTagExtendedRuleMessageCondition (kanonische Eigenschaft)
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
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 92008a387bb0130207af012df209a3aa6881d40e
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2018
ms.locfileid: "22593172"
---
# <a name="pidtagextendedrulemessagecondition-canonical-property"></a><span data-ttu-id="93ac5-103">PidTagExtendedRuleMessageCondition (kanonische Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="93ac5-103">PidTagExtendedRuleMessageCondition Canonical Property</span></span>

  
  
<span data-ttu-id="93ac5-104">**Betrifft**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="93ac5-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="93ac5-105">Enthält Informationen über keine benannten Eigenschaften auf, die in erweiterten regelbedingungen enthalten sind.</span><span class="sxs-lookup"><span data-stu-id="93ac5-105">Contains information about any named properties that are contained inside of extended rule conditions.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="93ac5-106">Zugeordnete Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="93ac5-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="93ac5-107">PR_EXTENDED_RULE_MSG_CONDITION</span><span class="sxs-lookup"><span data-stu-id="93ac5-107">PR_EXTENDED_RULE_MSG_CONDITION</span></span>  <br/> |
|<span data-ttu-id="93ac5-108">Kennung:</span><span class="sxs-lookup"><span data-stu-id="93ac5-108">Identifier:</span></span>  <br/> |<span data-ttu-id="93ac5-109">0x0E9A</span><span class="sxs-lookup"><span data-stu-id="93ac5-109">0x0E9A</span></span>  <br/> |
|<span data-ttu-id="93ac5-110">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="93ac5-110">Data type:</span></span>  <br/> |<span data-ttu-id="93ac5-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="93ac5-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="93ac5-112">Bereich:</span><span class="sxs-lookup"><span data-stu-id="93ac5-112">Area:</span></span>  <br/> |<span data-ttu-id="93ac5-113">Regeln</span><span class="sxs-lookup"><span data-stu-id="93ac5-113">Rules</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="93ac5-114">HinwBemerkungeneise</span><span class="sxs-lookup"><span data-stu-id="93ac5-114">Remarks</span></span>

<span data-ttu-id="93ac5-115">Diese Eigenschaft muss auf eine Nachricht FAI festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="93ac5-115">This property must be set on an FAI message.</span></span> <span data-ttu-id="93ac5-116">Es dient als **PR_RULE_CONDITION** ([PidTagRuleCondition](pidtagrulecondition-canonical-property.md)), aber enthält zusätzliche Informationen zu den benannten Eigenschaften verwendet.</span><span class="sxs-lookup"><span data-stu-id="93ac5-116">It serves the same purpose as **PR_RULE_CONDITION** ([PidTagRuleCondition](pidtagrulecondition-canonical-property.md)), but contains additional information about the named properties used.</span></span> <span data-ttu-id="93ac5-117">Alle String-Werten, die in einem beliebigen Teil des dieser Bedingung-Eigenschaftenwert enthalten sind, muss im Unicode-Format.</span><span class="sxs-lookup"><span data-stu-id="93ac5-117">All string values contained in any part of this condition property value must be in Unicode format.</span></span>
  
<span data-ttu-id="93ac5-118">Informationen zum Format dieser binäre Eigenschaft finden Sie unter [[MS-OXORULE]](http://msdn.microsoft.com/library/70ac9436-501e-43e2-9163-20d2b546b886%28Office.15%29.aspx).</span><span class="sxs-lookup"><span data-stu-id="93ac5-118">For information about the format of this binary property, see [[MS-OXORULE]](http://msdn.microsoft.com/library/70ac9436-501e-43e2-9163-20d2b546b886%28Office.15%29.aspx).</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="93ac5-119">Verwandte Ressourcen</span><span class="sxs-lookup"><span data-stu-id="93ac5-119">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="93ac5-120">Protokollspezifikationen</span><span class="sxs-lookup"><span data-stu-id="93ac5-120">Protocol specifications</span></span>

<span data-ttu-id="93ac5-121">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="93ac5-121">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="93ac5-122">Bietet Verweise auf Verwandte Exchange Server-Spezifikationen.</span><span class="sxs-lookup"><span data-stu-id="93ac5-122">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="93ac5-123">[[MS-OXORULE]](http://msdn.microsoft.com/library/70ac9436-501e-43e2-9163-20d2b546b886%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="93ac5-123">[[MS-OXORULE]](http://msdn.microsoft.com/library/70ac9436-501e-43e2-9163-20d2b546b886%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="93ac5-124">Eingehende e-Mail-Nachrichten auf einem Server bearbeitet.</span><span class="sxs-lookup"><span data-stu-id="93ac5-124">Manipulates incoming email messages on a server.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="93ac5-125">Header-Dateien</span><span class="sxs-lookup"><span data-stu-id="93ac5-125">Header files</span></span>

<span data-ttu-id="93ac5-126">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="93ac5-126">Mapidefs.h</span></span>
  
> <span data-ttu-id="93ac5-127">Enthält die Datentypdefinitionen.</span><span class="sxs-lookup"><span data-stu-id="93ac5-127">Provides data type definitions.</span></span>
    
<span data-ttu-id="93ac5-128">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="93ac5-128">Mapitags.h</span></span>
  
> <span data-ttu-id="93ac5-129">Enthält Definitionen von Eigenschaften, die als Alternative Namen aufgelistet.</span><span class="sxs-lookup"><span data-stu-id="93ac5-129">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="93ac5-130">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="93ac5-130">See also</span></span>



[<span data-ttu-id="93ac5-131">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="93ac5-131">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="93ac5-132">Kanonische MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="93ac5-132">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="93ac5-133">Zuordnen von kanonischen Eigenschaftennamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="93ac5-133">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="93ac5-134">Zuordnen von MAPI-Namen zu kanonische Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="93ac5-134">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

