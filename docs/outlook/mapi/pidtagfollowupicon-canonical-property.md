---
title: PidTagFollowupIcon (kanonische Eigenschaft)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagFollowupIcon
api_type:
- HeaderDef
ms.assetid: 374cef41-141a-491b-8dd1-eaf1a2044204
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 8fa96736b5404d84c6ab48851b916c5ab987ae2a
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2018
ms.locfileid: "22593921"
---
# <a name="pidtagfollowupicon-canonical-property"></a><span data-ttu-id="6202b-103">PidTagFollowupIcon (kanonische Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="6202b-103">PidTagFollowupIcon Canonical Property</span></span>

  
  
<span data-ttu-id="6202b-104">**Betrifft**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="6202b-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="6202b-105">Gibt die Kennzeichnungsfarbe des Message-Objekts.</span><span class="sxs-lookup"><span data-stu-id="6202b-105">Specifies the flag color of the message object.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="6202b-106">Zugeordnete Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="6202b-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="6202b-107">PR_FOLLOWUP_ICON</span><span class="sxs-lookup"><span data-stu-id="6202b-107">PR_FOLLOWUP_ICON</span></span>  <br/> |
|<span data-ttu-id="6202b-108">Kennung:</span><span class="sxs-lookup"><span data-stu-id="6202b-108">Identifier:</span></span>  <br/> |<span data-ttu-id="6202b-109">0x1095</span><span class="sxs-lookup"><span data-stu-id="6202b-109">0x1095</span></span>  <br/> |
|<span data-ttu-id="6202b-110">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="6202b-110">Data type:</span></span>  <br/> |<span data-ttu-id="6202b-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="6202b-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="6202b-112">Bereich:</span><span class="sxs-lookup"><span data-stu-id="6202b-112">Area:</span></span>  <br/> |<span data-ttu-id="6202b-113">Benennen Sie Nachrichtenordner</span><span class="sxs-lookup"><span data-stu-id="6202b-113">Rename message folder</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="6202b-114">HinwBemerkungeneise</span><span class="sxs-lookup"><span data-stu-id="6202b-114">Remarks</span></span>

<span data-ttu-id="6202b-115">Diese Eigenschaft darf nicht vorhanden sein, es sei denn, der Wert der **PR_FLAG_STATUS** ([PidTagFlagStatus](pidtagflagstatus-canonical-property.md))-Eigenschaft auf "FollowupFlagged" festgelegt ist, oder Message-Objekts ein bezüglich Besprechungen-Objekt ist.</span><span class="sxs-lookup"><span data-stu-id="6202b-115">This property must not exist unless the value of the **PR_FLAG_STATUS** ([PidTagFlagStatus](pidtagflagstatus-canonical-property.md)) property is set to "followupFlagged", or the message object is a meeting-related object.</span></span> <span data-ttu-id="6202b-116">Diese Eigenschaft sollte auf ein Task-Objekt nicht vorhanden.</span><span class="sxs-lookup"><span data-stu-id="6202b-116">This property should not exist on a task object.</span></span> <span data-ttu-id="6202b-117">Bei Festlegung auf andere Nachrichtenobjekte, muss diese Eigenschaft auf einen der folgenden Werte festgelegt sein.</span><span class="sxs-lookup"><span data-stu-id="6202b-117">When set on other message objects, this property must be set to one of the following values.</span></span>
  
|<span data-ttu-id="6202b-118">**Numerischen Wert**</span><span class="sxs-lookup"><span data-stu-id="6202b-118">**Numeric value**</span></span>|<span data-ttu-id="6202b-119">**Name**</span><span class="sxs-lookup"><span data-stu-id="6202b-119">**Name**</span></span>|<span data-ttu-id="6202b-120">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="6202b-120">**Description**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="6202b-121">Nicht vorhanden</span><span class="sxs-lookup"><span data-stu-id="6202b-121">Not present</span></span>  <br/> |<span data-ttu-id="6202b-122">–</span><span class="sxs-lookup"><span data-stu-id="6202b-122">N/A</span></span>  <br/> |<span data-ttu-id="6202b-123">Keine Farbe</span><span class="sxs-lookup"><span data-stu-id="6202b-123">No color</span></span>  <br/> |
|<span data-ttu-id="6202b-124">1</span><span class="sxs-lookup"><span data-stu-id="6202b-124">1</span></span>  <br/> |<span data-ttu-id="6202b-125">followupIcon1</span><span class="sxs-lookup"><span data-stu-id="6202b-125">followupIcon1</span></span>  <br/> |<span data-ttu-id="6202b-126">Lila Kennzeichnung</span><span class="sxs-lookup"><span data-stu-id="6202b-126">Purple flag</span></span>  <br/> |
|<span data-ttu-id="6202b-127">2</span><span class="sxs-lookup"><span data-stu-id="6202b-127">2</span></span>  <br/> |<span data-ttu-id="6202b-128">followupIcon2</span><span class="sxs-lookup"><span data-stu-id="6202b-128">followupIcon2</span></span>  <br/> |<span data-ttu-id="6202b-129">Orange Kennzeichnung</span><span class="sxs-lookup"><span data-stu-id="6202b-129">Orange flag</span></span>  <br/> |
|<span data-ttu-id="6202b-130">3</span><span class="sxs-lookup"><span data-stu-id="6202b-130">3</span></span>  <br/> |<span data-ttu-id="6202b-131">followupIcon3</span><span class="sxs-lookup"><span data-stu-id="6202b-131">followupIcon3</span></span>  <br/> |<span data-ttu-id="6202b-132">Grüne Kennzeichnung</span><span class="sxs-lookup"><span data-stu-id="6202b-132">Green flag</span></span>  <br/> |
|<span data-ttu-id="6202b-133">4</span><span class="sxs-lookup"><span data-stu-id="6202b-133">4</span></span>  <br/> |<span data-ttu-id="6202b-134">followupIcon4</span><span class="sxs-lookup"><span data-stu-id="6202b-134">followupIcon4</span></span>  <br/> |<span data-ttu-id="6202b-135">Gelbe Kennzeichnung</span><span class="sxs-lookup"><span data-stu-id="6202b-135">Yellow flag</span></span>  <br/> |
|<span data-ttu-id="6202b-136">5</span><span class="sxs-lookup"><span data-stu-id="6202b-136">5</span></span>  <br/> |<span data-ttu-id="6202b-137">followupIcon5</span><span class="sxs-lookup"><span data-stu-id="6202b-137">followupIcon5</span></span>  <br/> |<span data-ttu-id="6202b-138">Blaue Kennzeichnung</span><span class="sxs-lookup"><span data-stu-id="6202b-138">Blue flag</span></span>  <br/> |
|<span data-ttu-id="6202b-139">6</span><span class="sxs-lookup"><span data-stu-id="6202b-139">6</span></span>  <br/> |<span data-ttu-id="6202b-140">followupIcon6</span><span class="sxs-lookup"><span data-stu-id="6202b-140">followupIcon6</span></span>  <br/> |<span data-ttu-id="6202b-141">Rote Kennzeichnung</span><span class="sxs-lookup"><span data-stu-id="6202b-141">Red flag</span></span>  <br/> |
   
## <a name="related-resources"></a><span data-ttu-id="6202b-142">Verwandte Ressourcen</span><span class="sxs-lookup"><span data-stu-id="6202b-142">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="6202b-143">Protokollspezifikationen</span><span class="sxs-lookup"><span data-stu-id="6202b-143">Protocol specifications</span></span>

<span data-ttu-id="6202b-144">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="6202b-144">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="6202b-145">Bietet Verweise auf Verwandte Exchange Server-Spezifikationen.</span><span class="sxs-lookup"><span data-stu-id="6202b-145">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="6202b-146">[[MS-OXOFLAG]](http://msdn.microsoft.com/library/f1e50be4-ed30-4c2a-b5cb-8ff3aaaf9b91%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="6202b-146">[[MS-OXOFLAG]](http://msdn.microsoft.com/library/f1e50be4-ed30-4c2a-b5cb-8ff3aaaf9b91%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="6202b-147">Gibt die Eigenschaften und Vorgänge im Zusammenhang mit kennzeichnen.</span><span class="sxs-lookup"><span data-stu-id="6202b-147">Specifies the properties and operations related to flagging.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="6202b-148">Header-Dateien</span><span class="sxs-lookup"><span data-stu-id="6202b-148">Header files</span></span>

<span data-ttu-id="6202b-149">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="6202b-149">Mapidefs.h</span></span>
  
> <span data-ttu-id="6202b-150">Enthält die Datentypdefinitionen.</span><span class="sxs-lookup"><span data-stu-id="6202b-150">Provides data type definitions.</span></span>
    
<span data-ttu-id="6202b-151">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="6202b-151">Mapitags.h</span></span>
  
> <span data-ttu-id="6202b-152">Enthält Definitionen von Eigenschaften, die als Alternative Namen aufgelistet.</span><span class="sxs-lookup"><span data-stu-id="6202b-152">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="6202b-153">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="6202b-153">See also</span></span>



[<span data-ttu-id="6202b-154">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="6202b-154">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="6202b-155">Kanonische MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="6202b-155">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="6202b-156">Zuordnen von kanonischen Eigenschaftennamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="6202b-156">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="6202b-157">Zuordnen von MAPI-Namen zu kanonische Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="6202b-157">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

