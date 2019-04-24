---
title: Kanonische Pidtagextendedrulemessageactions (-Eigenschaft
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagExtendedRuleMessageActions
api_type:
- HeaderDef
ms.assetid: 1cf277d4-76ec-4902-9e54-f1780cee49bf
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: 70f09d6db5940fcb9b980cc839988113bd3a3e2e
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32316338"
---
# <a name="pidtagextendedrulemessageactions-canonical-property"></a><span data-ttu-id="038d0-103">Kanonische Pidtagextendedrulemessageactions (-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="038d0-103">PidTagExtendedRuleMessageActions Canonical Property</span></span>

  
  
<span data-ttu-id="038d0-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="038d0-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="038d0-105">Enthält zusätzliche Informationen zu den benannten Eigenschaften, die in einer FAI-Nachricht (Folder Associated Information) verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="038d0-105">Contains additional information about the named properties used in a Folder Associated Information (FAI) message.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="038d0-106">Zugeordnete Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="038d0-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="038d0-107">PR_EXTENDED_RULE_MSG_ACTIONS</span><span class="sxs-lookup"><span data-stu-id="038d0-107">PR_EXTENDED_RULE_MSG_ACTIONS</span></span>  <br/> |
|<span data-ttu-id="038d0-108">Kennung:</span><span class="sxs-lookup"><span data-stu-id="038d0-108">Identifier:</span></span>  <br/> |<span data-ttu-id="038d0-109">0x0E99</span><span class="sxs-lookup"><span data-stu-id="038d0-109">0x0E99</span></span>  <br/> |
|<span data-ttu-id="038d0-110">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="038d0-110">Data type:</span></span>  <br/> |<span data-ttu-id="038d0-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="038d0-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="038d0-112">Bereich:</span><span class="sxs-lookup"><span data-stu-id="038d0-112">Area:</span></span>  <br/> |<span data-ttu-id="038d0-113">Regeln</span><span class="sxs-lookup"><span data-stu-id="038d0-113">Rules</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="038d0-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="038d0-114">Remarks</span></span>

<span data-ttu-id="038d0-115">Diese Eigenschaft muss für eine FAI-Nachricht festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="038d0-115">This property must be set on an FAI message.</span></span> <span data-ttu-id="038d0-116">Diese Eigenschaft dient dem gleichen Zweck wie **PR_RULE_ACTIONS** ([PidTagRuleActions](pidtagruleactions-canonical-property.md)), enthält aber zusätzliche Informationen zur Version der Regel und den benannten Eigenschaften, die in der Regelaktion gespeichert sind, sowie Informationen zu den Aktionen, die durch diese Regel ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="038d0-116">This property serves the same purpose as **PR_RULE_ACTIONS** ([PidTagRuleActions](pidtagruleactions-canonical-property.md)), but contains additional information about the version of the rule and the named properties stored in the rule action, as well as information about the actions to be performed by this rule.</span></span> <span data-ttu-id="038d0-117">Alle in einem beliebigen Teil des Aktions Puffers enthaltenen Zeichenfolgenwerte, die Aktionen enthalten, müssen im Unicode-Format vorliegen.</span><span class="sxs-lookup"><span data-stu-id="038d0-117">All string values contained in any part of the action buffer used to contain actions must be in Unicode format.</span></span>
  
<span data-ttu-id="038d0-118">Informationen zum Format dieser Binary-Eigenschaft finden Sie unter [[MS-OXORULE]](https://msdn.microsoft.com/library/70ac9436-501e-43e2-9163-20d2b546b886%28Office.15%29.aspx).</span><span class="sxs-lookup"><span data-stu-id="038d0-118">For information about the format of this binary property, see [[MS-OXORULE]](https://msdn.microsoft.com/library/70ac9436-501e-43e2-9163-20d2b546b886%28Office.15%29.aspx).</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="038d0-119">Zugehörige Ressourcen</span><span class="sxs-lookup"><span data-stu-id="038d0-119">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="038d0-120">Protokollspezifikationen</span><span class="sxs-lookup"><span data-stu-id="038d0-120">Protocol specifications</span></span>

<span data-ttu-id="038d0-121">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="038d0-121">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="038d0-122">Enthält Verweise auf zugehörige Exchange Server-Protokollspezifikationen.</span><span class="sxs-lookup"><span data-stu-id="038d0-122">Provides references to related Exchange Server protocol specifications..</span></span>
    
<span data-ttu-id="038d0-123">[[MS-OXORULE]](https://msdn.microsoft.com/library/70ac9436-501e-43e2-9163-20d2b546b886%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="038d0-123">[[MS-OXORULE]](https://msdn.microsoft.com/library/70ac9436-501e-43e2-9163-20d2b546b886%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="038d0-124">Bearbeitet eingehende e-Mail-Nachrichten auf einem Server.</span><span class="sxs-lookup"><span data-stu-id="038d0-124">Manipulates incoming email messages on a server.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="038d0-125">Header Dateien</span><span class="sxs-lookup"><span data-stu-id="038d0-125">Header files</span></span>

<span data-ttu-id="038d0-126">Mapidefs. h</span><span class="sxs-lookup"><span data-stu-id="038d0-126">Mapidefs.h</span></span>
  
> <span data-ttu-id="038d0-127">Stellt Datentypdefinitionen bereit.</span><span class="sxs-lookup"><span data-stu-id="038d0-127">Provides data type definitions.</span></span>
    
<span data-ttu-id="038d0-128">Mapitags. h</span><span class="sxs-lookup"><span data-stu-id="038d0-128">Mapitags.h</span></span>
  
> <span data-ttu-id="038d0-129">Enthält Definitionen von Eigenschaften, die als Alternative Namen aufgeführt sind.</span><span class="sxs-lookup"><span data-stu-id="038d0-129">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="038d0-130">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="038d0-130">See also</span></span>



[<span data-ttu-id="038d0-131">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="038d0-131">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="038d0-132">Kanonische MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="038d0-132">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="038d0-133">Zuordnen von kanonischen Eigenschaftennamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="038d0-133">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="038d0-134">Zuordnen von MAPI-Namen zu kanonischen Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="038d0-134">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

