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
ms.openlocfilehash: ab246414f7caaf76f462d9b80e762fe614c77c21
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32278900"
---
# <a name="pidtagruleactions-canonical-property"></a><span data-ttu-id="b6d28-103">PidTagRuleActions (kanonische Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="b6d28-103">PidTagRuleActions Canonical Property</span></span>

  
  
<span data-ttu-id="b6d28-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="b6d28-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="b6d28-105">Enthält den Satz von Aktionen, die der Regel zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="b6d28-105">Contains the set of actions associated with the rule.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="b6d28-106">Zugeordnete Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="b6d28-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="b6d28-107">PR_RULE_ACTIONS</span><span class="sxs-lookup"><span data-stu-id="b6d28-107">PR_RULE_ACTIONS</span></span>  <br/> |
|<span data-ttu-id="b6d28-108">Kennung:</span><span class="sxs-lookup"><span data-stu-id="b6d28-108">Identifier:</span></span>  <br/> |<span data-ttu-id="b6d28-109">0x6680</span><span class="sxs-lookup"><span data-stu-id="b6d28-109">0x6680</span></span>  <br/> |
|<span data-ttu-id="b6d28-110">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="b6d28-110">Data type:</span></span>  <br/> |<span data-ttu-id="b6d28-111">PT_ACTIONS</span><span class="sxs-lookup"><span data-stu-id="b6d28-111">PT_ACTIONS</span></span>  <br/> |
|<span data-ttu-id="b6d28-112">Bereich:</span><span class="sxs-lookup"><span data-stu-id="b6d28-112">Area:</span></span>  <br/> |<span data-ttu-id="b6d28-113">Serverseitige Regeln</span><span class="sxs-lookup"><span data-stu-id="b6d28-113">Server Side Rules</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="b6d28-114">Hinweise</span><span class="sxs-lookup"><span data-stu-id="b6d28-114">Remarks</span></span>

<span data-ttu-id="b6d28-115">Die Aktionen werden als Regelaktion ausgedrückt, und der Eigenschaftswertpuffer enthält die Datenpufferstruktur der Regelaktion, die wie in [[MS-OXORULE]](https://msdn.microsoft.com/library/70ac9436-501e-43e2-9163-20d2b546b886%28Office.15%29.aspx)angegeben verpackt ist.</span><span class="sxs-lookup"><span data-stu-id="b6d28-115">The actions are expressed as a rule action and the property value buffer contains the rule action data buffer structure packaged as specified in [[MS-OXORULE]](https://msdn.microsoft.com/library/70ac9436-501e-43e2-9163-20d2b546b886%28Office.15%29.aspx).</span></span>
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="b6d28-116">MFCMAPI-Referenz</span><span class="sxs-lookup"><span data-stu-id="b6d28-116">MFCMAPI reference</span></span>

<span data-ttu-id="b6d28-117">Einen MFCMAP-Beispielcode finden Sie in der folgenden Tabelle.</span><span class="sxs-lookup"><span data-stu-id="b6d28-117">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="b6d28-118">**Datei**</span><span class="sxs-lookup"><span data-stu-id="b6d28-118">**File**</span></span>|<span data-ttu-id="b6d28-119">**Funktion**</span><span class="sxs-lookup"><span data-stu-id="b6d28-119">**Function**</span></span>|<span data-ttu-id="b6d28-120">**Comment**</span><span class="sxs-lookup"><span data-stu-id="b6d28-120">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="b6d28-121">ImportProcs.cpp</span><span class="sxs-lookup"><span data-stu-id="b6d28-121">ImportProcs.cpp</span></span>  <br/> |<span data-ttu-id="b6d28-122">PropCopyMore, HrCopyActions</span><span class="sxs-lookup"><span data-stu-id="b6d28-122">PropCopyMore, HrCopyActions</span></span>  <br/> |<span data-ttu-id="b6d28-123">Diese Funktionen zeigen, wie eine PT_ACTIONS zum Kopieren in eine andere Eigenschaft analysiert wird.</span><span class="sxs-lookup"><span data-stu-id="b6d28-123">These functions demonstrate how to parse a PT_ACTIONS property for the purposes of copying to another property.</span></span>  <br/> |
   
## <a name="related-resources"></a><span data-ttu-id="b6d28-124">Verwandte Ressourcen</span><span class="sxs-lookup"><span data-stu-id="b6d28-124">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="b6d28-125">Protokollspezifikationen</span><span class="sxs-lookup"><span data-stu-id="b6d28-125">Protocol specifications</span></span>

<span data-ttu-id="b6d28-126">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="b6d28-126">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="b6d28-127">Enthält Verweise auf Exchange Server Protokollspezifikationen.</span><span class="sxs-lookup"><span data-stu-id="b6d28-127">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="b6d28-128">[[MS-OXORULE]](https://msdn.microsoft.com/library/70ac9436-501e-43e2-9163-20d2b546b886%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="b6d28-128">[[MS-OXORULE]](https://msdn.microsoft.com/library/70ac9436-501e-43e2-9163-20d2b546b886%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="b6d28-129">Bearbeitet eingehende E-Mail-Nachrichten auf einem Server.</span><span class="sxs-lookup"><span data-stu-id="b6d28-129">Manipulates incoming email messages on a server.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="b6d28-130">Headerdateien</span><span class="sxs-lookup"><span data-stu-id="b6d28-130">Header files</span></span>

<span data-ttu-id="b6d28-131">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="b6d28-131">Mapidefs.h</span></span>
  
> <span data-ttu-id="b6d28-132">Bietet Datentypdefinitionen.</span><span class="sxs-lookup"><span data-stu-id="b6d28-132">Provides data type definitions.</span></span>
    
<span data-ttu-id="b6d28-133">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="b6d28-133">Mapitags.h</span></span>
  
> <span data-ttu-id="b6d28-134">Enthält Definitionen von Eigenschaften, die als alternative Namen aufgeführt sind.</span><span class="sxs-lookup"><span data-stu-id="b6d28-134">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="b6d28-135">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="b6d28-135">See also</span></span>



[<span data-ttu-id="b6d28-136">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="b6d28-136">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="b6d28-137">KANONISCHE EIGENSCHAFTEN VON MAPI</span><span class="sxs-lookup"><span data-stu-id="b6d28-137">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="b6d28-138">Zuordnen kanonischer Eigenschaftsnamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="b6d28-138">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="b6d28-139">Zuordnen von MAPI-Namen zu kanonischen Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="b6d28-139">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

