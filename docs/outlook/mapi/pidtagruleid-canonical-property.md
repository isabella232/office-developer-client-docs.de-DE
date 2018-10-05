---
title: PidTagRuleId (kanonische Eigenschaft)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagRuleId
api_type:
- COM
ms.assetid: 341e8db0-52b7-4ba7-aaa6-eedf2783b4e8
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 8d88838893836c550136be9556299258b44e3e49
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/04/2018
ms.locfileid: "25398059"
---
# <a name="pidtagruleid-canonical-property"></a><span data-ttu-id="ab8c9-103">PidTagRuleId (kanonische Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="ab8c9-103">PidTagRuleId Canonical Property</span></span>

  
  
<span data-ttu-id="ab8c9-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="ab8c9-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="ab8c9-105">Gibt einen eindeutigen Bezeichner, den der messaging-Server für jede Regel generiert wird, wenn die Regel erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="ab8c9-105">Specifies a unique identifier the messaging server generates for each rule when the rule is first created.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="ab8c9-106">Zugeordnete Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="ab8c9-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="ab8c9-107">PR_RULE_ID</span><span class="sxs-lookup"><span data-stu-id="ab8c9-107">PR_RULE_ID</span></span>  <br/> |
|<span data-ttu-id="ab8c9-108">Kennung:</span><span class="sxs-lookup"><span data-stu-id="ab8c9-108">Identifier:</span></span>  <br/> |<span data-ttu-id="ab8c9-109">0x6674</span><span class="sxs-lookup"><span data-stu-id="ab8c9-109">0x6674</span></span>  <br/> |
|<span data-ttu-id="ab8c9-110">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="ab8c9-110">Data type:</span></span>  <br/> |<span data-ttu-id="ab8c9-111">PT_I8</span><span class="sxs-lookup"><span data-stu-id="ab8c9-111">PT_I8</span></span>  <br/> |
|<span data-ttu-id="ab8c9-112">Bereich:</span><span class="sxs-lookup"><span data-stu-id="ab8c9-112">Area:</span></span>  <br/> |<span data-ttu-id="ab8c9-113">Serverseitige Regeln</span><span class="sxs-lookup"><span data-stu-id="ab8c9-113">Server Side Rules</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="ab8c9-114">Hinweise</span><span class="sxs-lookup"><span data-stu-id="ab8c9-114">Remarks</span></span>

<span data-ttu-id="ab8c9-115">Der Client muss diese Eigenschaft nicht angeben, beim Erstellen einer neuen Regel, jedoch müssen sie beim Ändern oder Löschen einer Regel angeben.</span><span class="sxs-lookup"><span data-stu-id="ab8c9-115">The client must not specify this property when creating a new rule but must specify it when modifying or deleting a rule.</span></span>
  
<span data-ttu-id="ab8c9-116">Wenn eine Regel zu löschen, die einzige Eigenschaft, die der Client weitergeben muss **PR_RULE_ID** und sollte nicht in anderen-Eigenschaft übergeben.</span><span class="sxs-lookup"><span data-stu-id="ab8c9-116">When deleting a rule, the only property the client must pass is **PR_RULE_ID** and should not pass in any other property.</span></span> <span data-ttu-id="ab8c9-117">Der Server muss Eigenschaften als diese Eigenschaft ignoriert.</span><span class="sxs-lookup"><span data-stu-id="ab8c9-117">The server must ignore properties other than this property.</span></span> <span data-ttu-id="ab8c9-118">Hinzufügen einer Regel der Client muss nicht **PR_RULE_ID**übergeben, müssen sie in der **PR_RULE_CONDITION** ([PidTagRuleCondition](pidtagrulecondition-canonical-property.md)), **PR_RULE_ACTIONS** ([PidTagRuleActions](pidtagruleactions-canonical-property.md)) und **PR_RULE_PROVIDER** ([ übergeben PidTagRuleProvider](pidtagruleprovider-canonical-property.md)) Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="ab8c9-118">When adding a rule, the client must not pass in **PR_RULE_ID**, it must pass in the **PR_RULE_CONDITION** ([PidTagRuleCondition](pidtagrulecondition-canonical-property.md)), **PR_RULE_ACTIONS** ([PidTagRuleActions](pidtagruleactions-canonical-property.md)) and **PR_RULE_PROVIDER** ([PidTagRuleProvider](pidtagruleprovider-canonical-property.md)) properties.</span></span> <span data-ttu-id="ab8c9-119">Beim Ändern einer Regel wird der Client muss **PR_RULE_ID** übergeben und übergeben sollten Sie den Rest der Eigenschaften, die geändert werden müssen.</span><span class="sxs-lookup"><span data-stu-id="ab8c9-119">When modifying a rule, the client must pass in **PR_RULE_ID** and should pass in the rest of the properties that need to be modified.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="ab8c9-120">Verwandte Ressourcen</span><span class="sxs-lookup"><span data-stu-id="ab8c9-120">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="ab8c9-121">Protokollspezifikationen</span><span class="sxs-lookup"><span data-stu-id="ab8c9-121">Protocol specifications</span></span>

<span data-ttu-id="ab8c9-122">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="ab8c9-122">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="ab8c9-123">Bietet Verweise auf Verwandte Exchange Server-Spezifikationen.</span><span class="sxs-lookup"><span data-stu-id="ab8c9-123">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="ab8c9-124">[[MS-OXORULE]](https://msdn.microsoft.com/library/70ac9436-501e-43e2-9163-20d2b546b886%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="ab8c9-124">[[MS-OXORULE]](https://msdn.microsoft.com/library/70ac9436-501e-43e2-9163-20d2b546b886%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="ab8c9-125">Eingehende e-Mail-Nachrichten auf einem Server bearbeitet.</span><span class="sxs-lookup"><span data-stu-id="ab8c9-125">Manipulates incoming email messages on a server.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="ab8c9-126">Header-Dateien</span><span class="sxs-lookup"><span data-stu-id="ab8c9-126">Header files</span></span>

<span data-ttu-id="ab8c9-127">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="ab8c9-127">Mapidefs.h</span></span>
  
> <span data-ttu-id="ab8c9-128">Enthält die Datentypdefinitionen.</span><span class="sxs-lookup"><span data-stu-id="ab8c9-128">Provides data type definitions.</span></span>
    
<span data-ttu-id="ab8c9-129">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="ab8c9-129">Mapitags.h</span></span>
  
> <span data-ttu-id="ab8c9-130">Enthält Definitionen von Eigenschaften, die als Alternative Namen aufgelistet.</span><span class="sxs-lookup"><span data-stu-id="ab8c9-130">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="ab8c9-131">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="ab8c9-131">See also</span></span>



[<span data-ttu-id="ab8c9-132">PidTagRuleCondition (kanonische Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="ab8c9-132">PidTagRuleCondition Canonical Property</span></span>](pidtagrulecondition-canonical-property.md)
  
[<span data-ttu-id="ab8c9-133">PidTagRuleActions (kanonische Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="ab8c9-133">PidTagRuleActions Canonical Property</span></span>](pidtagruleactions-canonical-property.md)
  
[<span data-ttu-id="ab8c9-134">PidTagRuleProvider (kanonische Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="ab8c9-134">PidTagRuleProvider Canonical Property</span></span>](pidtagruleprovider-canonical-property.md)


[<span data-ttu-id="ab8c9-135">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="ab8c9-135">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="ab8c9-136">Kanonische MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="ab8c9-136">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="ab8c9-137">Zuordnen von kanonischen Eigenschaftennamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="ab8c9-137">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="ab8c9-138">Zuordnen von MAPI-Namen zu kanonische Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="ab8c9-138">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

