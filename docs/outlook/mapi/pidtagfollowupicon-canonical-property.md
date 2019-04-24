---
title: Kanonische Pidtagfollowupicon (-Eigenschaft
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
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: 205b6ddc2b65297d69a2223aab7b745b223ee553
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32316282"
---
# <a name="pidtagfollowupicon-canonical-property"></a><span data-ttu-id="336b5-103">Kanonische Pidtagfollowupicon (-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="336b5-103">PidTagFollowupIcon Canonical Property</span></span>

  
  
<span data-ttu-id="336b5-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="336b5-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="336b5-105">Gibt die flagfarbe des Message-Objekts an.</span><span class="sxs-lookup"><span data-stu-id="336b5-105">Specifies the flag color of the message object.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="336b5-106">Zugeordnete Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="336b5-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="336b5-107">PR_FOLLOWUP_ICON</span><span class="sxs-lookup"><span data-stu-id="336b5-107">PR_FOLLOWUP_ICON</span></span>  <br/> |
|<span data-ttu-id="336b5-108">Kennung:</span><span class="sxs-lookup"><span data-stu-id="336b5-108">Identifier:</span></span>  <br/> |<span data-ttu-id="336b5-109">0x1095</span><span class="sxs-lookup"><span data-stu-id="336b5-109">0x1095</span></span>  <br/> |
|<span data-ttu-id="336b5-110">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="336b5-110">Data type:</span></span>  <br/> |<span data-ttu-id="336b5-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="336b5-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="336b5-112">Bereich:</span><span class="sxs-lookup"><span data-stu-id="336b5-112">Area:</span></span>  <br/> |<span data-ttu-id="336b5-113">Nachrichten Ordner umbenennen</span><span class="sxs-lookup"><span data-stu-id="336b5-113">Rename message folder</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="336b5-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="336b5-114">Remarks</span></span>

<span data-ttu-id="336b5-115">Diese Eigenschaft darf nur vorhanden sein, wenn der Wert der **PR_FLAG_STATUS** ([pidtagflagstatus (](pidtagflagstatus-canonical-property.md))-Eigenschaft auf "followupFlagged" festgelegt ist oder das Message-Objekt ein Besprechungs bezogenes Objekt ist.</span><span class="sxs-lookup"><span data-stu-id="336b5-115">This property must not exist unless the value of the **PR_FLAG_STATUS** ([PidTagFlagStatus](pidtagflagstatus-canonical-property.md)) property is set to "followupFlagged", or the message object is a meeting-related object.</span></span> <span data-ttu-id="336b5-116">Diese Eigenschaft sollte in einem Task-Objekt nicht vorhanden sein.</span><span class="sxs-lookup"><span data-stu-id="336b5-116">This property should not exist on a task object.</span></span> <span data-ttu-id="336b5-117">Wenn diese Eigenschaft für andere Nachrichtenobjekte festgelegt ist, muss Sie auf einen der folgenden Werte festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="336b5-117">When set on other message objects, this property must be set to one of the following values.</span></span>
  
|<span data-ttu-id="336b5-118">**Numerischer Wert**</span><span class="sxs-lookup"><span data-stu-id="336b5-118">**Numeric value**</span></span>|<span data-ttu-id="336b5-119">**Name**</span><span class="sxs-lookup"><span data-stu-id="336b5-119">**Name**</span></span>|<span data-ttu-id="336b5-120">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="336b5-120">**Description**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="336b5-121">Nicht vorhanden</span><span class="sxs-lookup"><span data-stu-id="336b5-121">Not present</span></span>  <br/> |<span data-ttu-id="336b5-122">Nicht zutreffend</span><span class="sxs-lookup"><span data-stu-id="336b5-122">N/A</span></span>  <br/> |<span data-ttu-id="336b5-123">Keine Farbe</span><span class="sxs-lookup"><span data-stu-id="336b5-123">No color</span></span>  <br/> |
|<span data-ttu-id="336b5-124">1</span><span class="sxs-lookup"><span data-stu-id="336b5-124">1</span></span>  <br/> |<span data-ttu-id="336b5-125">followupIcon1</span><span class="sxs-lookup"><span data-stu-id="336b5-125">followupIcon1</span></span>  <br/> |<span data-ttu-id="336b5-126">Violette Kennzeichnung</span><span class="sxs-lookup"><span data-stu-id="336b5-126">Purple flag</span></span>  <br/> |
|<span data-ttu-id="336b5-127">2</span><span class="sxs-lookup"><span data-stu-id="336b5-127">2</span></span>  <br/> |<span data-ttu-id="336b5-128">followupIcon2</span><span class="sxs-lookup"><span data-stu-id="336b5-128">followupIcon2</span></span>  <br/> |<span data-ttu-id="336b5-129">Orangefarbene Kennzeichnung</span><span class="sxs-lookup"><span data-stu-id="336b5-129">Orange flag</span></span>  <br/> |
|<span data-ttu-id="336b5-130">3</span><span class="sxs-lookup"><span data-stu-id="336b5-130">3</span></span>  <br/> |<span data-ttu-id="336b5-131">followupIcon3</span><span class="sxs-lookup"><span data-stu-id="336b5-131">followupIcon3</span></span>  <br/> |<span data-ttu-id="336b5-132">Grüne Kennzeichnung</span><span class="sxs-lookup"><span data-stu-id="336b5-132">Green flag</span></span>  <br/> |
|<span data-ttu-id="336b5-133">4</span><span class="sxs-lookup"><span data-stu-id="336b5-133">4</span></span>  <br/> |<span data-ttu-id="336b5-134">followupIcon4</span><span class="sxs-lookup"><span data-stu-id="336b5-134">followupIcon4</span></span>  <br/> |<span data-ttu-id="336b5-135">Gelbe Kennzeichnung</span><span class="sxs-lookup"><span data-stu-id="336b5-135">Yellow flag</span></span>  <br/> |
|<span data-ttu-id="336b5-136">5</span><span class="sxs-lookup"><span data-stu-id="336b5-136">5</span></span>  <br/> |<span data-ttu-id="336b5-137">followupIcon5</span><span class="sxs-lookup"><span data-stu-id="336b5-137">followupIcon5</span></span>  <br/> |<span data-ttu-id="336b5-138">Blaue Kennzeichnung</span><span class="sxs-lookup"><span data-stu-id="336b5-138">Blue flag</span></span>  <br/> |
|<span data-ttu-id="336b5-139">6</span><span class="sxs-lookup"><span data-stu-id="336b5-139">6</span></span>  <br/> |<span data-ttu-id="336b5-140">followupIcon6</span><span class="sxs-lookup"><span data-stu-id="336b5-140">followupIcon6</span></span>  <br/> |<span data-ttu-id="336b5-141">Rote Kennzeichnung</span><span class="sxs-lookup"><span data-stu-id="336b5-141">Red flag</span></span>  <br/> |
   
## <a name="related-resources"></a><span data-ttu-id="336b5-142">Zugehörige Ressourcen</span><span class="sxs-lookup"><span data-stu-id="336b5-142">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="336b5-143">Protokollspezifikationen</span><span class="sxs-lookup"><span data-stu-id="336b5-143">Protocol specifications</span></span>

<span data-ttu-id="336b5-144">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="336b5-144">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="336b5-145">Enthält Verweise auf zugehörige Exchange Server-Protokollspezifikationen.</span><span class="sxs-lookup"><span data-stu-id="336b5-145">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="336b5-146">[[MS-OXOFLAG]](https://msdn.microsoft.com/library/f1e50be4-ed30-4c2a-b5cb-8ff3aaaf9b91%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="336b5-146">[[MS-OXOFLAG]](https://msdn.microsoft.com/library/f1e50be4-ed30-4c2a-b5cb-8ff3aaaf9b91%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="336b5-147">Gibt die Eigenschaften und Vorgänge im Zusammenhang mit der Markierung an.</span><span class="sxs-lookup"><span data-stu-id="336b5-147">Specifies the properties and operations related to flagging.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="336b5-148">Header Dateien</span><span class="sxs-lookup"><span data-stu-id="336b5-148">Header files</span></span>

<span data-ttu-id="336b5-149">Mapidefs. h</span><span class="sxs-lookup"><span data-stu-id="336b5-149">Mapidefs.h</span></span>
  
> <span data-ttu-id="336b5-150">Stellt Datentypdefinitionen bereit.</span><span class="sxs-lookup"><span data-stu-id="336b5-150">Provides data type definitions.</span></span>
    
<span data-ttu-id="336b5-151">Mapitags. h</span><span class="sxs-lookup"><span data-stu-id="336b5-151">Mapitags.h</span></span>
  
> <span data-ttu-id="336b5-152">Enthält Definitionen von Eigenschaften, die als Alternative Namen aufgeführt sind.</span><span class="sxs-lookup"><span data-stu-id="336b5-152">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="336b5-153">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="336b5-153">See also</span></span>



[<span data-ttu-id="336b5-154">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="336b5-154">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="336b5-155">Kanonische MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="336b5-155">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="336b5-156">Zuordnen von kanonischen Eigenschaftennamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="336b5-156">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="336b5-157">Zuordnen von MAPI-Namen zu kanonischen Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="336b5-157">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

