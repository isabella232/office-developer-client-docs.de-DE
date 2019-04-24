---
title: Kanonische PidTagRuleActions-Eigenschaft
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
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: ab246414f7caaf76f462d9b80e762fe614c77c21
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32278900"
---
# <a name="pidtagruleactions-canonical-property"></a><span data-ttu-id="f0e4f-103">Kanonische PidTagRuleActions-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="f0e4f-103">PidTagRuleActions Canonical Property</span></span>

  
  
<span data-ttu-id="f0e4f-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="f0e4f-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="f0e4f-105">Enthält die mit der Regel verknüpften Aktionen.</span><span class="sxs-lookup"><span data-stu-id="f0e4f-105">Contains the set of actions associated with the rule.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="f0e4f-106">Zugeordnete Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="f0e4f-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="f0e4f-107">PR_RULE_ACTIONS</span><span class="sxs-lookup"><span data-stu-id="f0e4f-107">PR_RULE_ACTIONS</span></span>  <br/> |
|<span data-ttu-id="f0e4f-108">Kennung:</span><span class="sxs-lookup"><span data-stu-id="f0e4f-108">Identifier:</span></span>  <br/> |<span data-ttu-id="f0e4f-109">0x6680</span><span class="sxs-lookup"><span data-stu-id="f0e4f-109">0x6680</span></span>  <br/> |
|<span data-ttu-id="f0e4f-110">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="f0e4f-110">Data type:</span></span>  <br/> |<span data-ttu-id="f0e4f-111">PT_ACTIONS</span><span class="sxs-lookup"><span data-stu-id="f0e4f-111">PT_ACTIONS</span></span>  <br/> |
|<span data-ttu-id="f0e4f-112">Bereich:</span><span class="sxs-lookup"><span data-stu-id="f0e4f-112">Area:</span></span>  <br/> |<span data-ttu-id="f0e4f-113">Server seitige Regeln</span><span class="sxs-lookup"><span data-stu-id="f0e4f-113">Server Side Rules</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="f0e4f-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="f0e4f-114">Remarks</span></span>

<span data-ttu-id="f0e4f-115">Die Aktionen werden als Regelaktion ausgedrückt, und der Wert Puffer der Eigenschaft enthält die in [[MS-OXORULE]](https://msdn.microsoft.com/library/70ac9436-501e-43e2-9163-20d2b546b886%28Office.15%29.aspx)verpackte Datenpuffer Struktur für Regelaktionen.</span><span class="sxs-lookup"><span data-stu-id="f0e4f-115">The actions are expressed as a rule action and the property value buffer contains the rule action data buffer structure packaged as specified in [[MS-OXORULE]](https://msdn.microsoft.com/library/70ac9436-501e-43e2-9163-20d2b546b886%28Office.15%29.aspx).</span></span>
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="f0e4f-116">MFCMAPI-Referenz</span><span class="sxs-lookup"><span data-stu-id="f0e4f-116">MFCMAPI reference</span></span>

<span data-ttu-id="f0e4f-117">Einen MFCMAP-Beispielcode finden Sie in der folgenden Tabelle.</span><span class="sxs-lookup"><span data-stu-id="f0e4f-117">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="f0e4f-118">**Datei**</span><span class="sxs-lookup"><span data-stu-id="f0e4f-118">**File**</span></span>|<span data-ttu-id="f0e4f-119">**Funktion**</span><span class="sxs-lookup"><span data-stu-id="f0e4f-119">**Function**</span></span>|<span data-ttu-id="f0e4f-120">**Comment**</span><span class="sxs-lookup"><span data-stu-id="f0e4f-120">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="f0e4f-121">ImportProcs. cpp</span><span class="sxs-lookup"><span data-stu-id="f0e4f-121">ImportProcs.cpp</span></span>  <br/> |<span data-ttu-id="f0e4f-122">PropCopyMore, HrCopyActions</span><span class="sxs-lookup"><span data-stu-id="f0e4f-122">PropCopyMore, HrCopyActions</span></span>  <br/> |<span data-ttu-id="f0e4f-123">Diese Funktionen veranschaulichen, wie Sie eine PT_ACTIONS-Eigenschaft zum Kopieren in eine andere Eigenschaft analysieren.</span><span class="sxs-lookup"><span data-stu-id="f0e4f-123">These functions demonstrate how to parse a PT_ACTIONS property for the purposes of copying to another property.</span></span>  <br/> |
   
## <a name="related-resources"></a><span data-ttu-id="f0e4f-124">Zugehörige Ressourcen</span><span class="sxs-lookup"><span data-stu-id="f0e4f-124">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="f0e4f-125">Protokollspezifikationen</span><span class="sxs-lookup"><span data-stu-id="f0e4f-125">Protocol specifications</span></span>

<span data-ttu-id="f0e4f-126">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="f0e4f-126">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="f0e4f-127">Enthält Verweise auf zugehörige Exchange Server-Protokollspezifikationen.</span><span class="sxs-lookup"><span data-stu-id="f0e4f-127">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="f0e4f-128">[[MS-OXORULE]](https://msdn.microsoft.com/library/70ac9436-501e-43e2-9163-20d2b546b886%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="f0e4f-128">[[MS-OXORULE]](https://msdn.microsoft.com/library/70ac9436-501e-43e2-9163-20d2b546b886%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="f0e4f-129">Bearbeitet eingehende e-Mail-Nachrichten auf einem Server.</span><span class="sxs-lookup"><span data-stu-id="f0e4f-129">Manipulates incoming email messages on a server.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="f0e4f-130">Header Dateien</span><span class="sxs-lookup"><span data-stu-id="f0e4f-130">Header files</span></span>

<span data-ttu-id="f0e4f-131">Mapidefs. h</span><span class="sxs-lookup"><span data-stu-id="f0e4f-131">Mapidefs.h</span></span>
  
> <span data-ttu-id="f0e4f-132">Stellt Datentypdefinitionen bereit.</span><span class="sxs-lookup"><span data-stu-id="f0e4f-132">Provides data type definitions.</span></span>
    
<span data-ttu-id="f0e4f-133">Mapitags. h</span><span class="sxs-lookup"><span data-stu-id="f0e4f-133">Mapitags.h</span></span>
  
> <span data-ttu-id="f0e4f-134">Enthält Definitionen von Eigenschaften, die als Alternative Namen aufgeführt sind.</span><span class="sxs-lookup"><span data-stu-id="f0e4f-134">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="f0e4f-135">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="f0e4f-135">See also</span></span>



[<span data-ttu-id="f0e4f-136">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="f0e4f-136">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="f0e4f-137">Kanonische MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="f0e4f-137">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="f0e4f-138">Zuordnen von kanonischen Eigenschaftennamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="f0e4f-138">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="f0e4f-139">Zuordnen von MAPI-Namen zu kanonischen Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="f0e4f-139">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

