---
title: Kanonische PidTagExtendedRuleMessageActions-Eigenschaft
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
ms.openlocfilehash: 5425496a5b7845daabf736978e6ed24518451fe0
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19794378"
---
# <a name="pidtagextendedrulemessageactions-canonical-property"></a><span data-ttu-id="4f956-103">Kanonische PidTagExtendedRuleMessageActions-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="4f956-103">PidTagExtendedRuleMessageActions Canonical Property</span></span>

  
  
<span data-ttu-id="4f956-104">**Betrifft**: Outlook</span><span class="sxs-lookup"><span data-stu-id="4f956-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="4f956-105">Enthält zusätzliche Informationen zu den benannten Eigenschaften in einer Nachricht Ordner verknüpften Informationen (FAI) verwendet.</span><span class="sxs-lookup"><span data-stu-id="4f956-105">Contains additional information about the named properties used in a Folder Associated Information (FAI) message.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="4f956-106">Zugeordneten Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="4f956-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="4f956-107">PR_EXTENDED_RULE_MSG_ACTIONS</span><span class="sxs-lookup"><span data-stu-id="4f956-107">PR_EXTENDED_RULE_MSG_ACTIONS</span></span>  <br/> |
|<span data-ttu-id="4f956-108">Bezeichner:</span><span class="sxs-lookup"><span data-stu-id="4f956-108">Identifier:</span></span>  <br/> |<span data-ttu-id="4f956-109">0x0E99</span><span class="sxs-lookup"><span data-stu-id="4f956-109">0x0E99</span></span>  <br/> |
|<span data-ttu-id="4f956-110">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="4f956-110">Data type:</span></span>  <br/> |<span data-ttu-id="4f956-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="4f956-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="4f956-112">Bereich:</span><span class="sxs-lookup"><span data-stu-id="4f956-112">Area:</span></span>  <br/> |<span data-ttu-id="4f956-113">Regeln</span><span class="sxs-lookup"><span data-stu-id="4f956-113">Rules</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="4f956-114">Hinweise</span><span class="sxs-lookup"><span data-stu-id="4f956-114">Remarks</span></span>

<span data-ttu-id="4f956-115">Diese Eigenschaft muss auf eine Nachricht FAI festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="4f956-115">This property must be set on an FAI message.</span></span> <span data-ttu-id="4f956-116">Diese Eigenschaft dient dem gleichen Zweck als **PR_RULE_ACTIONS** ([PidTagRuleActions](pidtagruleactions-canonical-property.md)), jedoch enthält zusätzliche Informationen zur Version der benannten Eigenschaften in die Regelaktion gespeichert und die Regel sowie Informationen zu den Aktionen werden Durch diese Regel ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="4f956-116">This property serves the same purpose as **PR_RULE_ACTIONS** ([PidTagRuleActions](pidtagruleactions-canonical-property.md)), but contains additional information about the version of the rule and the named properties stored in the rule action, as well as information about the actions to be performed by this rule.</span></span> <span data-ttu-id="4f956-117">Alle String-Werten, die in einem beliebigen Teil des Puffers Aktion verwendet, um Aktionen enthalten enthalten sind, muss im Unicode-Format.</span><span class="sxs-lookup"><span data-stu-id="4f956-117">All string values contained in any part of the action buffer used to contain actions must be in Unicode format.</span></span>
  
<span data-ttu-id="4f956-118">Informationen zum Format dieser binäre Eigenschaft finden Sie unter [[MS-OXORULE]](http://msdn.microsoft.com/library/70ac9436-501e-43e2-9163-20d2b546b886%28Office.15%29.aspx).</span><span class="sxs-lookup"><span data-stu-id="4f956-118">For information about the format of this binary property, see [[MS-OXORULE]](http://msdn.microsoft.com/library/70ac9436-501e-43e2-9163-20d2b546b886%28Office.15%29.aspx).</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="4f956-119">Verwandte Ressourcen</span><span class="sxs-lookup"><span data-stu-id="4f956-119">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="4f956-120">Protokollspezifikationen</span><span class="sxs-lookup"><span data-stu-id="4f956-120">Protocol specifications</span></span>

<span data-ttu-id="4f956-121">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="4f956-121">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="4f956-122">Bietet Verweise auf Verwandte Exchange Server-Spezifikationen.</span><span class="sxs-lookup"><span data-stu-id="4f956-122">Provides references to related Exchange Server protocol specifications..</span></span>
    
<span data-ttu-id="4f956-123">[[MS-OXORULE]](http://msdn.microsoft.com/library/70ac9436-501e-43e2-9163-20d2b546b886%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="4f956-123">[[MS-OXORULE]](http://msdn.microsoft.com/library/70ac9436-501e-43e2-9163-20d2b546b886%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="4f956-124">Eingehende e-Mail-Nachrichten auf einem Server bearbeitet.</span><span class="sxs-lookup"><span data-stu-id="4f956-124">Manipulates incoming email messages on a server.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="4f956-125">Header-Dateien</span><span class="sxs-lookup"><span data-stu-id="4f956-125">Header files</span></span>

<span data-ttu-id="4f956-126">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="4f956-126">Mapidefs.h</span></span>
  
> <span data-ttu-id="4f956-127">Enthält die Datentypdefinitionen.</span><span class="sxs-lookup"><span data-stu-id="4f956-127">Provides data type definitions.</span></span>
    
<span data-ttu-id="4f956-128">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="4f956-128">Mapitags.h</span></span>
  
> <span data-ttu-id="4f956-129">Enthält Definitionen von Eigenschaften, die als Alternative Namen aufgelistet.</span><span class="sxs-lookup"><span data-stu-id="4f956-129">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="4f956-130">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="4f956-130">See also</span></span>



[<span data-ttu-id="4f956-131">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="4f956-131">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="4f956-132">Kanonische MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="4f956-132">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="4f956-133">Zuordnen von kanonischen Eigenschaftennamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="4f956-133">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="4f956-134">Zuordnen von MAPI-Namen zu kanonische Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="4f956-134">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

