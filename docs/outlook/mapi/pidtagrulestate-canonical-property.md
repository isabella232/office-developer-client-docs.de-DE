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
ms.openlocfilehash: 9d1adb6dd1fc151c9a599ea44391c2ca5b2fe2aa
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2018
ms.locfileid: "22580565"
---
# <a name="pidtagrulestate-canonical-property"></a><span data-ttu-id="a1171-103">PidTagRuleState (kanonische Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="a1171-103">PidTagRuleState Canonical Property</span></span>

  
  
<span data-ttu-id="a1171-104">**Betrifft**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="a1171-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="a1171-105">Ein Wert, der als eine Bitmaske Kombination von Flags, die angeben, den Status der Regel interpretiert.</span><span class="sxs-lookup"><span data-stu-id="a1171-105">A value interpreted as a bitmask combination of flags that specify the state of the rule.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="a1171-106">Zugeordnete Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="a1171-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="a1171-107">PR_RULE_STATE</span><span class="sxs-lookup"><span data-stu-id="a1171-107">PR_RULE_STATE</span></span>  <br/> |
|<span data-ttu-id="a1171-108">Kennung:</span><span class="sxs-lookup"><span data-stu-id="a1171-108">Identifier:</span></span>  <br/> |<span data-ttu-id="a1171-109">0x6677</span><span class="sxs-lookup"><span data-stu-id="a1171-109">0x6677</span></span>  <br/> |
|<span data-ttu-id="a1171-110">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="a1171-110">Data type:</span></span>  <br/> |<span data-ttu-id="a1171-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="a1171-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="a1171-112">Bereich:</span><span class="sxs-lookup"><span data-stu-id="a1171-112">Area:</span></span>  <br/> |<span data-ttu-id="a1171-113">Serverseitige Regeln</span><span class="sxs-lookup"><span data-stu-id="a1171-113">Server Side Rules</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="a1171-114">HinwBemerkungeneise</span><span class="sxs-lookup"><span data-stu-id="a1171-114">Remarks</span></span>

<span data-ttu-id="a1171-115">Die folgende Tabelle zeigt die möglichen Werte dieser Eigenschaft an.</span><span class="sxs-lookup"><span data-stu-id="a1171-115">The following table defines the possible values of this property.</span></span>
  
<span data-ttu-id="a1171-116">De-de (ST_ENABLED, 0 x 00000001 Bitmaske)</span><span class="sxs-lookup"><span data-stu-id="a1171-116">EN (ST_ENABLED, bitmask 0x00000001)</span></span>
  
> <span data-ttu-id="a1171-117">Die Regel ist für die Ausführung aktiviert.</span><span class="sxs-lookup"><span data-stu-id="a1171-117">The rule is enabled for execution.</span></span> <span data-ttu-id="a1171-118">Wenn dieses Flag nicht festgelegt ist, muss der Server diese Regel überspringen, beim Auswerten der Regeln.</span><span class="sxs-lookup"><span data-stu-id="a1171-118">If this flag is not set, the server must skip this rule when evaluating rules.</span></span>
    
<span data-ttu-id="a1171-119">ER (ST_ERROR, 0 x 00000002 Bitmaske)</span><span class="sxs-lookup"><span data-stu-id="a1171-119">ER (ST_ERROR, bitmask 0x00000002)</span></span>
  
> <span data-ttu-id="a1171-120">Der Server ist Verarbeitung der Regel einen Fehler aufgetreten.</span><span class="sxs-lookup"><span data-stu-id="a1171-120">The server has encountered an error processing the rule.</span></span>
    
<span data-ttu-id="a1171-121">DER (ST_ONLY_WHEN_OOF, 0 x 00000004 Bitmaske)</span><span class="sxs-lookup"><span data-stu-id="a1171-121">OF (ST_ONLY_WHEN_OOF, bitmask 0x00000004)</span></span>
  
> <span data-ttu-id="a1171-122">Die Regel wird ausgeführt, nur, wenn der Benutzer den Status von Office (OOF) für das Postfach festlegt.</span><span class="sxs-lookup"><span data-stu-id="a1171-122">The rule is executed only when the user sets the Out of Office (OOF) state on the mailbox.</span></span> <span data-ttu-id="a1171-123">Dieses Kennzeichen müssen in einer Regel für Öffentliche Ordner nicht festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="a1171-123">This flag must not be set in a public folder rule.</span></span>
    
<span data-ttu-id="a1171-124">HI (ST_KEEP_OOF_HIST, 0 x 00000008 Bitmaske)</span><span class="sxs-lookup"><span data-stu-id="a1171-124">HI (ST_KEEP_OOF_HIST, bitmask 0x00000008)</span></span>
  
> <span data-ttu-id="a1171-125">Dieses Kennzeichen müssen in einer Regel für Öffentliche Ordner nicht festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="a1171-125">This flag must not be set in a public folder rule.</span></span>
    
<span data-ttu-id="a1171-126">EL (ST_EXIT_LEVEL, 0 x 00000010 Bitmaske)</span><span class="sxs-lookup"><span data-stu-id="a1171-126">EL (ST_EXIT_LEVEL, bitmask 0x00000010)</span></span>
  
> <span data-ttu-id="a1171-127">Auswertung der Regel werden nach dem Ausführen dieser Regel, mit Ausnahme der Auswertung von Abwesenheitsnotizen Regeln beendet.</span><span class="sxs-lookup"><span data-stu-id="a1171-127">Rule evaluation will end after executing this rule, except for evaluation of Out of Office rules.</span></span>
    
<span data-ttu-id="a1171-128">SCL-Bewertung (ST_SKIP_IF_SCL_IS_SAFE, 0 x 00000020 Bitmaske)</span><span class="sxs-lookup"><span data-stu-id="a1171-128">SCL (ST_SKIP_IF_SCL_IS_SAFE, bitmask 0x00000020)</span></span>
  
> <span data-ttu-id="a1171-129">Auswertung dieser Regel möglicherweise übersprungen werden.</span><span class="sxs-lookup"><span data-stu-id="a1171-129">Evaluation of this rule may be skipped.</span></span>
    
<span data-ttu-id="a1171-130">PE (ST_RULE_PARSE_ERROR, 0 x 00000040 Bitmaske)</span><span class="sxs-lookup"><span data-stu-id="a1171-130">PE (ST_RULE_PARSE_ERROR, bitmask 0x00000040)</span></span>
  
> <span data-ttu-id="a1171-131">Der Server ist ein Fehler, die Analyse der Regeldaten vom Client aufgetreten.</span><span class="sxs-lookup"><span data-stu-id="a1171-131">The server has encountered an error parsing the rule data provided by the client.</span></span>
    
<span data-ttu-id="a1171-132">X</span><span class="sxs-lookup"><span data-stu-id="a1171-132">X</span></span>
  
> <span data-ttu-id="a1171-133">Von dieses Protokoll nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="a1171-133">Unused by this protocol.</span></span> <span data-ttu-id="a1171-134">Dieses Bit muss vom Client nicht geändert werden.</span><span class="sxs-lookup"><span data-stu-id="a1171-134">This bit must not be modified by the client.</span></span>
    
<span data-ttu-id="a1171-135">Beachten Sie auf die Interaktion zwischen ST_ONLY_WHEN_OOF und ST_EXIT_LEVEL Flags:</span><span class="sxs-lookup"><span data-stu-id="a1171-135">Note on the interaction between ST_ONLY_WHEN_OOF and ST_EXIT_LEVEL flags:</span></span> 
  
<span data-ttu-id="a1171-136">Wenn der Status "Abwesend" für das Postfach festgelegt ist, und eine Bedingung TRUE ergibt,</span><span class="sxs-lookup"><span data-stu-id="a1171-136">When the "Out of Office" state is set on the mailbox, and a rule condition evaluates to TRUE,</span></span> 
  
<span data-ttu-id="a1171-137">UND:</span><span class="sxs-lookup"><span data-stu-id="a1171-137">AND:</span></span>
  
- <span data-ttu-id="a1171-138">Die Regel muss das ST_EXIT_LEVEL-Flag festlegen und keinen ST_ONLY_WHEN_OOF-Flag festlegen.</span><span class="sxs-lookup"><span data-stu-id="a1171-138">The rule has the ST_EXIT_LEVEL flag set and does not have ST_ONLY_WHEN_OOF flag set.</span></span> <span data-ttu-id="a1171-139">Klicken Sie dann der Server muss nicht ausgewertet werden nachfolgende Regeln, die keine ST_ONLY_WHEN_OOF flag festgelegt und nachfolgende Regeln, die ST_ONLY_WHEN_OOF gekennzeichnet sind ausgewertet werden.</span><span class="sxs-lookup"><span data-stu-id="a1171-139">Then, the server must not evaluate subsequent rules that do not have ST_ONLY_WHEN_OOF flag set, and must evaluate subsequent rules that have ST_ONLY_WHEN_OOF flag set.</span></span>
    
<span data-ttu-id="a1171-140">ODER:</span><span class="sxs-lookup"><span data-stu-id="a1171-140">OR:</span></span>
  
- <span data-ttu-id="a1171-141">Die Regel verwendet den ST_EXIT_LEVEL und die ST_ONLY_WHEN_OOF Flags festgelegt.</span><span class="sxs-lookup"><span data-stu-id="a1171-141">The rule has both the ST_EXIT_LEVEL and ST_ONLY_WHEN_OOF flags set.</span></span> <span data-ttu-id="a1171-142">Klicken Sie dann, muss der Server nicht ausgewertet werden alle nachfolgenden Regeln.</span><span class="sxs-lookup"><span data-stu-id="a1171-142">Then, the server must not evaluate any subsequent rules.</span></span>
    
## <a name="related-resources"></a><span data-ttu-id="a1171-143">Verwandte Ressourcen</span><span class="sxs-lookup"><span data-stu-id="a1171-143">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="a1171-144">Protokollspezifikationen</span><span class="sxs-lookup"><span data-stu-id="a1171-144">Protocol specifications</span></span>

<span data-ttu-id="a1171-145">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="a1171-145">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="a1171-146">Bietet Verweise auf Verwandte Exchange Server-Spezifikationen.</span><span class="sxs-lookup"><span data-stu-id="a1171-146">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="a1171-147">[[MS-OXORULE]](http://msdn.microsoft.com/library/70ac9436-501e-43e2-9163-20d2b546b886%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="a1171-147">[[MS-OXORULE]](http://msdn.microsoft.com/library/70ac9436-501e-43e2-9163-20d2b546b886%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="a1171-148">Eingehende e-Mail-Nachrichten auf einem Server bearbeitet.</span><span class="sxs-lookup"><span data-stu-id="a1171-148">Manipulates incoming email messages on a server.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="a1171-149">Header-Dateien</span><span class="sxs-lookup"><span data-stu-id="a1171-149">Header files</span></span>

<span data-ttu-id="a1171-150">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="a1171-150">Mapidefs.h</span></span>
  
> <span data-ttu-id="a1171-151">Enthält die Datentypdefinitionen.</span><span class="sxs-lookup"><span data-stu-id="a1171-151">Provides data type definitions.</span></span>
    
<span data-ttu-id="a1171-152">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="a1171-152">Mapitags.h</span></span>
  
> <span data-ttu-id="a1171-153">Enthält Definitionen von Eigenschaften, die als Alternative Namen aufgelistet.</span><span class="sxs-lookup"><span data-stu-id="a1171-153">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="a1171-154">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="a1171-154">See also</span></span>



[<span data-ttu-id="a1171-155">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="a1171-155">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="a1171-156">Kanonische MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="a1171-156">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="a1171-157">Zuordnen von kanonischen Eigenschaftennamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="a1171-157">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="a1171-158">Zuordnen von MAPI-Namen zu kanonische Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="a1171-158">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

