---
title: PidTagRuleState (kanonische Eigenschaft)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagRuleState
api_type:
- COM
ms.assetid: f62f3055-b855-4203-aa5c-6ba28b58c6f7
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: a0e15462cd3dc14c93155e34e47b7caac2c04087
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32338612"
---
# <a name="pidtagrulestate-canonical-property"></a><span data-ttu-id="a7dad-103">PidTagRuleState (kanonische Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="a7dad-103">PidTagRuleState Canonical Property</span></span>

  
  
<span data-ttu-id="a7dad-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="a7dad-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="a7dad-105">Ein Wert, der als Bitmaskenkombination von Flags interpretiert wird, die den Status der Regel angeben.</span><span class="sxs-lookup"><span data-stu-id="a7dad-105">A value interpreted as a bitmask combination of flags that specify the state of the rule.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="a7dad-106">Zugeordnete Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="a7dad-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="a7dad-107">PR_RULE_STATE</span><span class="sxs-lookup"><span data-stu-id="a7dad-107">PR_RULE_STATE</span></span>  <br/> |
|<span data-ttu-id="a7dad-108">Kennung:</span><span class="sxs-lookup"><span data-stu-id="a7dad-108">Identifier:</span></span>  <br/> |<span data-ttu-id="a7dad-109">0x6677</span><span class="sxs-lookup"><span data-stu-id="a7dad-109">0x6677</span></span>  <br/> |
|<span data-ttu-id="a7dad-110">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="a7dad-110">Data type:</span></span>  <br/> |<span data-ttu-id="a7dad-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="a7dad-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="a7dad-112">Bereich:</span><span class="sxs-lookup"><span data-stu-id="a7dad-112">Area:</span></span>  <br/> |<span data-ttu-id="a7dad-113">Serverseitige Regeln</span><span class="sxs-lookup"><span data-stu-id="a7dad-113">Server Side Rules</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="a7dad-114">Hinweise</span><span class="sxs-lookup"><span data-stu-id="a7dad-114">Remarks</span></span>

<span data-ttu-id="a7dad-115">In der folgenden Tabelle werden die möglichen Werte dieser Eigenschaft definiert.</span><span class="sxs-lookup"><span data-stu-id="a7dad-115">The following table defines the possible values of this property.</span></span>
  
<span data-ttu-id="a7dad-116">EN (ST_ENABLED, bitmask 0x00000001)</span><span class="sxs-lookup"><span data-stu-id="a7dad-116">EN (ST_ENABLED, bitmask 0x00000001)</span></span>
  
> <span data-ttu-id="a7dad-117">Die Regel ist für die Ausführung aktiviert.</span><span class="sxs-lookup"><span data-stu-id="a7dad-117">The rule is enabled for execution.</span></span> <span data-ttu-id="a7dad-118">Wenn dieses Flag nicht festgelegt ist, muss der Server diese Regel beim Auswerten von Regeln überspringen.</span><span class="sxs-lookup"><span data-stu-id="a7dad-118">If this flag is not set, the server must skip this rule when evaluating rules.</span></span>
    
<span data-ttu-id="a7dad-119">ER (ST_ERROR, bitmask 0x00000002)</span><span class="sxs-lookup"><span data-stu-id="a7dad-119">ER (ST_ERROR, bitmask 0x00000002)</span></span>
  
> <span data-ttu-id="a7dad-120">Auf dem Server ist ein Fehler bei der Verarbeitung der Regel aufgetreten.</span><span class="sxs-lookup"><span data-stu-id="a7dad-120">The server has encountered an error processing the rule.</span></span>
    
<span data-ttu-id="a7dad-121">OF (ST_ONLY_WHEN_OOF, bitmask 0x00000004)</span><span class="sxs-lookup"><span data-stu-id="a7dad-121">OF (ST_ONLY_WHEN_OOF, bitmask 0x00000004)</span></span>
  
> <span data-ttu-id="a7dad-122">Die Regel wird nur ausgeführt, wenn der Benutzer den Status Out of Office (OOF) für das Postfach fest legt.</span><span class="sxs-lookup"><span data-stu-id="a7dad-122">The rule is executed only when the user sets the Out of Office (OOF) state on the mailbox.</span></span> <span data-ttu-id="a7dad-123">Dieses Flag darf nicht in einer Regel für öffentliche Ordner festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="a7dad-123">This flag must not be set in a public folder rule.</span></span>
    
<span data-ttu-id="a7dad-124">HI (ST_KEEP_OOF_HIST, bitmask 0x00000008)</span><span class="sxs-lookup"><span data-stu-id="a7dad-124">HI (ST_KEEP_OOF_HIST, bitmask 0x00000008)</span></span>
  
> <span data-ttu-id="a7dad-125">Dieses Flag darf nicht in einer Regel für öffentliche Ordner festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="a7dad-125">This flag must not be set in a public folder rule.</span></span>
    
<span data-ttu-id="a7dad-126">EL (ST_EXIT_LEVEL, bitmask 0x00000010)</span><span class="sxs-lookup"><span data-stu-id="a7dad-126">EL (ST_EXIT_LEVEL, bitmask 0x00000010)</span></span>
  
> <span data-ttu-id="a7dad-127">Die Regelauswertung endet nach der Ausführung dieser Regel, mit Ausnahme der Auswertung von Out of Office Regeln.</span><span class="sxs-lookup"><span data-stu-id="a7dad-127">Rule evaluation will end after executing this rule, except for evaluation of Out of Office rules.</span></span>
    
<span data-ttu-id="a7dad-128">SCL (ST_SKIP_IF_SCL_IS_SAFE, bitmask 0x00000020)</span><span class="sxs-lookup"><span data-stu-id="a7dad-128">SCL (ST_SKIP_IF_SCL_IS_SAFE, bitmask 0x00000020)</span></span>
  
> <span data-ttu-id="a7dad-129">Die Auswertung dieser Regel kann übersprungen werden.</span><span class="sxs-lookup"><span data-stu-id="a7dad-129">Evaluation of this rule may be skipped.</span></span>
    
<span data-ttu-id="a7dad-130">PE (ST_RULE_PARSE_ERROR, bitmask 0x00000040)</span><span class="sxs-lookup"><span data-stu-id="a7dad-130">PE (ST_RULE_PARSE_ERROR, bitmask 0x00000040)</span></span>
  
> <span data-ttu-id="a7dad-131">Auf dem Server ist ein Fehler aufgetreten, bei dem die vom Client bereitgestellten Regeldaten analyset werden.</span><span class="sxs-lookup"><span data-stu-id="a7dad-131">The server has encountered an error parsing the rule data provided by the client.</span></span>
    
<span data-ttu-id="a7dad-132">X</span><span class="sxs-lookup"><span data-stu-id="a7dad-132">X</span></span>
  
> <span data-ttu-id="a7dad-133">Von diesem Protokoll nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="a7dad-133">Unused by this protocol.</span></span> <span data-ttu-id="a7dad-134">Dieses Bit darf vom Client nicht geändert werden.</span><span class="sxs-lookup"><span data-stu-id="a7dad-134">This bit must not be modified by the client.</span></span>
    
<span data-ttu-id="a7dad-135">Hinweis zur Interaktion zwischen ST_ONLY_WHEN_OOF und ST_EXIT_LEVEL Flags:</span><span class="sxs-lookup"><span data-stu-id="a7dad-135">Note on the interaction between ST_ONLY_WHEN_OOF and ST_EXIT_LEVEL flags:</span></span> 
  
<span data-ttu-id="a7dad-136">Wenn der Status "Out of Office" für das Postfach festgelegt ist und eine Regelbedingung auf TRUE ausgewertet wird,</span><span class="sxs-lookup"><span data-stu-id="a7dad-136">When the "Out of Office" state is set on the mailbox, and a rule condition evaluates to TRUE,</span></span> 
  
<span data-ttu-id="a7dad-137">AND:</span><span class="sxs-lookup"><span data-stu-id="a7dad-137">AND:</span></span>
  
- <span data-ttu-id="a7dad-138">Für die Regel ist ST_EXIT_LEVEL Flag festgelegt und ST_ONLY_WHEN_OOF festgelegt.</span><span class="sxs-lookup"><span data-stu-id="a7dad-138">The rule has the ST_EXIT_LEVEL flag set and does not have ST_ONLY_WHEN_OOF flag set.</span></span> <span data-ttu-id="a7dad-139">Anschließend darf der Server keine nachfolgenden Regeln auswerten, für die ST_ONLY_WHEN_OOF festgelegt ist, und nachfolgende Regeln mit ST_ONLY_WHEN_OOF auswerten.</span><span class="sxs-lookup"><span data-stu-id="a7dad-139">Then, the server must not evaluate subsequent rules that do not have ST_ONLY_WHEN_OOF flag set, and must evaluate subsequent rules that have ST_ONLY_WHEN_OOF flag set.</span></span>
    
<span data-ttu-id="a7dad-140">OR:</span><span class="sxs-lookup"><span data-stu-id="a7dad-140">OR:</span></span>
  
- <span data-ttu-id="a7dad-141">Für die Regel sind die ST_EXIT_LEVEL und ST_ONLY_WHEN_OOF festgelegt.</span><span class="sxs-lookup"><span data-stu-id="a7dad-141">The rule has both the ST_EXIT_LEVEL and ST_ONLY_WHEN_OOF flags set.</span></span> <span data-ttu-id="a7dad-142">Anschließend darf der Server keine nachfolgenden Regeln auswerten.</span><span class="sxs-lookup"><span data-stu-id="a7dad-142">Then, the server must not evaluate any subsequent rules.</span></span>
    
## <a name="related-resources"></a><span data-ttu-id="a7dad-143">Verwandte Ressourcen</span><span class="sxs-lookup"><span data-stu-id="a7dad-143">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="a7dad-144">Protokollspezifikationen</span><span class="sxs-lookup"><span data-stu-id="a7dad-144">Protocol specifications</span></span>

<span data-ttu-id="a7dad-145">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="a7dad-145">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="a7dad-146">Enthält Verweise auf Exchange Server Protokollspezifikationen.</span><span class="sxs-lookup"><span data-stu-id="a7dad-146">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="a7dad-147">[[MS-OXORULE]](https://msdn.microsoft.com/library/70ac9436-501e-43e2-9163-20d2b546b886%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="a7dad-147">[[MS-OXORULE]](https://msdn.microsoft.com/library/70ac9436-501e-43e2-9163-20d2b546b886%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="a7dad-148">Bearbeitet eingehende E-Mail-Nachrichten auf einem Server.</span><span class="sxs-lookup"><span data-stu-id="a7dad-148">Manipulates incoming email messages on a server.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="a7dad-149">Headerdateien</span><span class="sxs-lookup"><span data-stu-id="a7dad-149">Header files</span></span>

<span data-ttu-id="a7dad-150">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="a7dad-150">Mapidefs.h</span></span>
  
> <span data-ttu-id="a7dad-151">Bietet Datentypdefinitionen.</span><span class="sxs-lookup"><span data-stu-id="a7dad-151">Provides data type definitions.</span></span>
    
<span data-ttu-id="a7dad-152">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="a7dad-152">Mapitags.h</span></span>
  
> <span data-ttu-id="a7dad-153">Enthält Definitionen von Eigenschaften, die als alternative Namen aufgeführt sind.</span><span class="sxs-lookup"><span data-stu-id="a7dad-153">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="a7dad-154">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="a7dad-154">See also</span></span>



[<span data-ttu-id="a7dad-155">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="a7dad-155">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="a7dad-156">KANONISCHE EIGENSCHAFTEN VON MAPI</span><span class="sxs-lookup"><span data-stu-id="a7dad-156">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="a7dad-157">Zuordnen kanonischer Eigenschaftsnamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="a7dad-157">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="a7dad-158">Zuordnen von MAPI-Namen zu kanonischen Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="a7dad-158">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

