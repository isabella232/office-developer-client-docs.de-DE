---
title: PidTagRuleActions (kanonische Eigenschaft)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagRuleActions
api_type:
- COM
ms.assetid: 3ec4259a-8fe9-46c3-82b8-42c6907b8515
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: ede62c792b1241a150c9d0a05adbe47fe0b6c0e7
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2018
ms.locfileid: "22567461"
---
# <a name="pidtagruleactions-canonical-property"></a><span data-ttu-id="846aa-103">PidTagRuleActions (kanonische Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="846aa-103">PidTagRuleActions Canonical Property</span></span>

  
  
<span data-ttu-id="846aa-104">**Betrifft**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="846aa-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="846aa-105">Enthält den Satz von Aktionen, die die Regel zugeordnet.</span><span class="sxs-lookup"><span data-stu-id="846aa-105">Contains the set of actions associated with the rule.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="846aa-106">Zugeordnete Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="846aa-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="846aa-107">PR_RULE_ACTIONS</span><span class="sxs-lookup"><span data-stu-id="846aa-107">PR_RULE_ACTIONS</span></span>  <br/> |
|<span data-ttu-id="846aa-108">Kennung:</span><span class="sxs-lookup"><span data-stu-id="846aa-108">Identifier:</span></span>  <br/> |<span data-ttu-id="846aa-109">0x6680</span><span class="sxs-lookup"><span data-stu-id="846aa-109">0x6680</span></span>  <br/> |
|<span data-ttu-id="846aa-110">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="846aa-110">Data type:</span></span>  <br/> |<span data-ttu-id="846aa-111">PT_ACTIONS</span><span class="sxs-lookup"><span data-stu-id="846aa-111">PT_ACTIONS</span></span>  <br/> |
|<span data-ttu-id="846aa-112">Bereich:</span><span class="sxs-lookup"><span data-stu-id="846aa-112">Area:</span></span>  <br/> |<span data-ttu-id="846aa-113">Serverseitige Regeln</span><span class="sxs-lookup"><span data-stu-id="846aa-113">Server Side Rules</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="846aa-114">HinwBemerkungeneise</span><span class="sxs-lookup"><span data-stu-id="846aa-114">Remarks</span></span>

<span data-ttu-id="846aa-115">Die Aktionen werden als Regelaktion ausgedrückt, und der Eigenschaft Wert Puffer enthält die Regel Aktion-Puffer Datenstruktur gepackt wie in [[MS-OXORULE]](http://msdn.microsoft.com/library/70ac9436-501e-43e2-9163-20d2b546b886%28Office.15%29.aspx)angegeben.</span><span class="sxs-lookup"><span data-stu-id="846aa-115">The actions are expressed as a rule action and the property value buffer contains the rule action data buffer structure packaged as specified in [[MS-OXORULE]](http://msdn.microsoft.com/library/70ac9436-501e-43e2-9163-20d2b546b886%28Office.15%29.aspx).</span></span>
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="846aa-116">MFCMAPI (engl.) (engl.)</span><span class="sxs-lookup"><span data-stu-id="846aa-116">MFCMAPI reference</span></span>

<span data-ttu-id="846aa-117">Beispielcode MFCMAPI (engl.) finden Sie in der folgenden Tabelle.</span><span class="sxs-lookup"><span data-stu-id="846aa-117">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="846aa-118">**Datei**</span><span class="sxs-lookup"><span data-stu-id="846aa-118">**File**</span></span>|<span data-ttu-id="846aa-119">**Funktion**</span><span class="sxs-lookup"><span data-stu-id="846aa-119">**Function**</span></span>|<span data-ttu-id="846aa-120">**Comment**</span><span class="sxs-lookup"><span data-stu-id="846aa-120">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="846aa-121">ImportProcs.cpp</span><span class="sxs-lookup"><span data-stu-id="846aa-121">ImportProcs.cpp</span></span>  <br/> |<span data-ttu-id="846aa-122">PropCopyMore HrCopyActions</span><span class="sxs-lookup"><span data-stu-id="846aa-122">PropCopyMore, HrCopyActions</span></span>  <br/> |<span data-ttu-id="846aa-123">Diese Funktionen wird gezeigt, wie eine PT_ACTIONS-Eigenschaft im Zusammenhang mit einer anderen Eigenschaft kopieren von analysieren.</span><span class="sxs-lookup"><span data-stu-id="846aa-123">These functions demonstrate how to parse a PT_ACTIONS property for the purposes of copying to another property.</span></span>  <br/> |
   
## <a name="related-resources"></a><span data-ttu-id="846aa-124">Verwandte Ressourcen</span><span class="sxs-lookup"><span data-stu-id="846aa-124">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="846aa-125">Protokollspezifikationen</span><span class="sxs-lookup"><span data-stu-id="846aa-125">Protocol specifications</span></span>

<span data-ttu-id="846aa-126">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="846aa-126">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="846aa-127">Bietet Verweise auf Verwandte Exchange Server-Spezifikationen.</span><span class="sxs-lookup"><span data-stu-id="846aa-127">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="846aa-128">[[MS-OXORULE]](http://msdn.microsoft.com/library/70ac9436-501e-43e2-9163-20d2b546b886%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="846aa-128">[[MS-OXORULE]](http://msdn.microsoft.com/library/70ac9436-501e-43e2-9163-20d2b546b886%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="846aa-129">Eingehende e-Mail-Nachrichten auf einem Server bearbeitet.</span><span class="sxs-lookup"><span data-stu-id="846aa-129">Manipulates incoming email messages on a server.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="846aa-130">Header-Dateien</span><span class="sxs-lookup"><span data-stu-id="846aa-130">Header files</span></span>

<span data-ttu-id="846aa-131">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="846aa-131">Mapidefs.h</span></span>
  
> <span data-ttu-id="846aa-132">Enthält die Datentypdefinitionen.</span><span class="sxs-lookup"><span data-stu-id="846aa-132">Provides data type definitions.</span></span>
    
<span data-ttu-id="846aa-133">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="846aa-133">Mapitags.h</span></span>
  
> <span data-ttu-id="846aa-134">Enthält Definitionen von Eigenschaften, die als Alternative Namen aufgelistet.</span><span class="sxs-lookup"><span data-stu-id="846aa-134">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="846aa-135">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="846aa-135">See also</span></span>



[<span data-ttu-id="846aa-136">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="846aa-136">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="846aa-137">Kanonische MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="846aa-137">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="846aa-138">Zuordnen von kanonischen Eigenschaftennamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="846aa-138">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="846aa-139">Zuordnen von MAPI-Namen zu kanonische Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="846aa-139">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

