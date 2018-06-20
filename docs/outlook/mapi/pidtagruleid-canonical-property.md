---
title: Kanonische PidTagRuleId-Eigenschaft
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
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: 52a6132dcd6aa2c3a2951f3d1a6458808364dccb
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19795026"
---
# <a name="pidtagruleid-canonical-property"></a><span data-ttu-id="d9af1-103">Kanonische PidTagRuleId-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="d9af1-103">PidTagRuleId Canonical Property</span></span>

  
  
<span data-ttu-id="d9af1-104">**Betrifft**: Outlook</span><span class="sxs-lookup"><span data-stu-id="d9af1-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="d9af1-105">Gibt einen eindeutigen Bezeichner, den der messaging-Server für jede Regel generiert wird, wenn die Regel erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="d9af1-105">Specifies a unique identifier the messaging server generates for each rule when the rule is first created.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="d9af1-106">Zugeordneten Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="d9af1-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="d9af1-107">PR_RULE_ID</span><span class="sxs-lookup"><span data-stu-id="d9af1-107">PR_RULE_ID</span></span>  <br/> |
|<span data-ttu-id="d9af1-108">Bezeichner:</span><span class="sxs-lookup"><span data-stu-id="d9af1-108">Identifier:</span></span>  <br/> |<span data-ttu-id="d9af1-109">0x6674</span><span class="sxs-lookup"><span data-stu-id="d9af1-109">0x6674</span></span>  <br/> |
|<span data-ttu-id="d9af1-110">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="d9af1-110">Data type:</span></span>  <br/> |<span data-ttu-id="d9af1-111">PT_I8</span><span class="sxs-lookup"><span data-stu-id="d9af1-111">PT_I8</span></span>  <br/> |
|<span data-ttu-id="d9af1-112">Bereich:</span><span class="sxs-lookup"><span data-stu-id="d9af1-112">Area:</span></span>  <br/> |<span data-ttu-id="d9af1-113">Serverseitige Regeln</span><span class="sxs-lookup"><span data-stu-id="d9af1-113">Server Side Rules</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="d9af1-114">Hinweise</span><span class="sxs-lookup"><span data-stu-id="d9af1-114">Remarks</span></span>

<span data-ttu-id="d9af1-115">Der Client muss diese Eigenschaft nicht angeben, beim Erstellen einer neuen Regel, jedoch müssen sie beim Ändern oder Löschen einer Regel angeben.</span><span class="sxs-lookup"><span data-stu-id="d9af1-115">The client must not specify this property when creating a new rule but must specify it when modifying or deleting a rule.</span></span>
  
<span data-ttu-id="d9af1-116">Wenn eine Regel zu löschen, die einzige Eigenschaft, die der Client weitergeben muss **PR_RULE_ID** und sollte nicht in anderen-Eigenschaft übergeben.</span><span class="sxs-lookup"><span data-stu-id="d9af1-116">When deleting a rule, the only property the client must pass is **PR_RULE_ID** and should not pass in any other property.</span></span> <span data-ttu-id="d9af1-117">Der Server muss Eigenschaften als diese Eigenschaft ignoriert.</span><span class="sxs-lookup"><span data-stu-id="d9af1-117">The server must ignore properties other than this property.</span></span> <span data-ttu-id="d9af1-118">Hinzufügen einer Regel der Client muss nicht **PR_RULE_ID**übergeben, müssen sie in der **PR_RULE_CONDITION** ([PidTagRuleCondition](pidtagrulecondition-canonical-property.md)), **PR_RULE_ACTIONS** ([PidTagRuleActions](pidtagruleactions-canonical-property.md)) und **PR_RULE_PROVIDER** ([ übergeben PidTagRuleProvider](pidtagruleprovider-canonical-property.md)) Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="d9af1-118">When adding a rule, the client must not pass in **PR_RULE_ID**, it must pass in the **PR_RULE_CONDITION** ([PidTagRuleCondition](pidtagrulecondition-canonical-property.md)), **PR_RULE_ACTIONS** ([PidTagRuleActions](pidtagruleactions-canonical-property.md)) and **PR_RULE_PROVIDER** ([PidTagRuleProvider](pidtagruleprovider-canonical-property.md)) properties.</span></span> <span data-ttu-id="d9af1-119">Beim Ändern einer Regel wird der Client muss **PR_RULE_ID** übergeben und übergeben sollten Sie den Rest der Eigenschaften, die geändert werden müssen.</span><span class="sxs-lookup"><span data-stu-id="d9af1-119">When modifying a rule, the client must pass in **PR_RULE_ID** and should pass in the rest of the properties that need to be modified.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="d9af1-120">Verwandte Ressourcen</span><span class="sxs-lookup"><span data-stu-id="d9af1-120">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="d9af1-121">Protokollspezifikationen</span><span class="sxs-lookup"><span data-stu-id="d9af1-121">Protocol specifications</span></span>

<span data-ttu-id="d9af1-122">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="d9af1-122">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="d9af1-123">Bietet Verweise auf Verwandte Exchange Server-Spezifikationen.</span><span class="sxs-lookup"><span data-stu-id="d9af1-123">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="d9af1-124">[[MS-OXORULE]](http://msdn.microsoft.com/library/70ac9436-501e-43e2-9163-20d2b546b886%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="d9af1-124">[[MS-OXORULE]](http://msdn.microsoft.com/library/70ac9436-501e-43e2-9163-20d2b546b886%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="d9af1-125">Eingehende e-Mail-Nachrichten auf einem Server bearbeitet.</span><span class="sxs-lookup"><span data-stu-id="d9af1-125">Manipulates incoming email messages on a server.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="d9af1-126">Header-Dateien</span><span class="sxs-lookup"><span data-stu-id="d9af1-126">Header files</span></span>

<span data-ttu-id="d9af1-127">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="d9af1-127">Mapidefs.h</span></span>
  
> <span data-ttu-id="d9af1-128">Enthält die Datentypdefinitionen.</span><span class="sxs-lookup"><span data-stu-id="d9af1-128">Provides data type definitions.</span></span>
    
<span data-ttu-id="d9af1-129">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="d9af1-129">Mapitags.h</span></span>
  
> <span data-ttu-id="d9af1-130">Enthält Definitionen von Eigenschaften, die als Alternative Namen aufgelistet.</span><span class="sxs-lookup"><span data-stu-id="d9af1-130">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="d9af1-131">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="d9af1-131">See also</span></span>



[<span data-ttu-id="d9af1-132">Kanonische PidTagRuleCondition-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="d9af1-132">PidTagRuleCondition Canonical Property</span></span>](pidtagrulecondition-canonical-property.md)
  
[<span data-ttu-id="d9af1-133">Kanonische PidTagRuleActions-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="d9af1-133">PidTagRuleActions Canonical Property</span></span>](pidtagruleactions-canonical-property.md)
  
[<span data-ttu-id="d9af1-134">Kanonische PidTagRuleProvider-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="d9af1-134">PidTagRuleProvider Canonical Property</span></span>](pidtagruleprovider-canonical-property.md)


[<span data-ttu-id="d9af1-135">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="d9af1-135">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="d9af1-136">Kanonische MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="d9af1-136">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="d9af1-137">Zuordnen von kanonischen Eigenschaftennamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="d9af1-137">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="d9af1-138">Zuordnen von MAPI-Namen zu kanonische Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="d9af1-138">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

