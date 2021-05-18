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
ms.openlocfilehash: 205b6ddc2b65297d69a2223aab7b745b223ee553
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32316282"
---
# <a name="pidtagfollowupicon-canonical-property"></a><span data-ttu-id="ee9f1-103">PidTagFollowupIcon (kanonische Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="ee9f1-103">PidTagFollowupIcon Canonical Property</span></span>

  
  
<span data-ttu-id="ee9f1-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="ee9f1-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="ee9f1-105">Gibt die Kennzeichenfarbe des Message-Objekts an.</span><span class="sxs-lookup"><span data-stu-id="ee9f1-105">Specifies the flag color of the message object.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="ee9f1-106">Zugeordnete Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="ee9f1-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="ee9f1-107">PR_FOLLOWUP_ICON</span><span class="sxs-lookup"><span data-stu-id="ee9f1-107">PR_FOLLOWUP_ICON</span></span>  <br/> |
|<span data-ttu-id="ee9f1-108">Kennung:</span><span class="sxs-lookup"><span data-stu-id="ee9f1-108">Identifier:</span></span>  <br/> |<span data-ttu-id="ee9f1-109">0x1095</span><span class="sxs-lookup"><span data-stu-id="ee9f1-109">0x1095</span></span>  <br/> |
|<span data-ttu-id="ee9f1-110">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="ee9f1-110">Data type:</span></span>  <br/> |<span data-ttu-id="ee9f1-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="ee9f1-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="ee9f1-112">Bereich:</span><span class="sxs-lookup"><span data-stu-id="ee9f1-112">Area:</span></span>  <br/> |<span data-ttu-id="ee9f1-113">Umbenennen des Nachrichtenordners</span><span class="sxs-lookup"><span data-stu-id="ee9f1-113">Rename message folder</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="ee9f1-114">Hinweise</span><span class="sxs-lookup"><span data-stu-id="ee9f1-114">Remarks</span></span>

<span data-ttu-id="ee9f1-115">Diese Eigenschaft darf nur vorhanden sein, wenn der Wert der **PR_FLAG_STATUS** ([PidTagFlagStatus](pidtagflagstatus-canonical-property.md))-Eigenschaft auf "followupFlagged" festgelegt ist oder das Message-Objekt ein besprechungsbezogenes Objekt ist.</span><span class="sxs-lookup"><span data-stu-id="ee9f1-115">This property must not exist unless the value of the **PR_FLAG_STATUS** ([PidTagFlagStatus](pidtagflagstatus-canonical-property.md)) property is set to "followupFlagged", or the message object is a meeting-related object.</span></span> <span data-ttu-id="ee9f1-116">Diese Eigenschaft sollte für ein Aufgabenobjekt nicht vorhanden sein.</span><span class="sxs-lookup"><span data-stu-id="ee9f1-116">This property should not exist on a task object.</span></span> <span data-ttu-id="ee9f1-117">Wenn sie für andere Nachrichtenobjekte festgelegt ist, muss diese Eigenschaft auf einen der folgenden Werte festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="ee9f1-117">When set on other message objects, this property must be set to one of the following values.</span></span>
  
|<span data-ttu-id="ee9f1-118">**Numerischer Wert**</span><span class="sxs-lookup"><span data-stu-id="ee9f1-118">**Numeric value**</span></span>|<span data-ttu-id="ee9f1-119">**Name**</span><span class="sxs-lookup"><span data-stu-id="ee9f1-119">**Name**</span></span>|<span data-ttu-id="ee9f1-120">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="ee9f1-120">**Description**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="ee9f1-121">Nicht vorhanden</span><span class="sxs-lookup"><span data-stu-id="ee9f1-121">Not present</span></span>  <br/> |<span data-ttu-id="ee9f1-122">Nicht zutreffend</span><span class="sxs-lookup"><span data-stu-id="ee9f1-122">N/A</span></span>  <br/> |<span data-ttu-id="ee9f1-123">Keine Farbe</span><span class="sxs-lookup"><span data-stu-id="ee9f1-123">No color</span></span>  <br/> |
|<span data-ttu-id="ee9f1-124">1</span><span class="sxs-lookup"><span data-stu-id="ee9f1-124">1</span></span>  <br/> |<span data-ttu-id="ee9f1-125">followupIcon1</span><span class="sxs-lookup"><span data-stu-id="ee9f1-125">followupIcon1</span></span>  <br/> |<span data-ttu-id="ee9f1-126">Lila-Flag</span><span class="sxs-lookup"><span data-stu-id="ee9f1-126">Purple flag</span></span>  <br/> |
|<span data-ttu-id="ee9f1-127">2</span><span class="sxs-lookup"><span data-stu-id="ee9f1-127">2</span></span>  <br/> |<span data-ttu-id="ee9f1-128">followupIcon2</span><span class="sxs-lookup"><span data-stu-id="ee9f1-128">followupIcon2</span></span>  <br/> |<span data-ttu-id="ee9f1-129">Orangefarbenes Flag</span><span class="sxs-lookup"><span data-stu-id="ee9f1-129">Orange flag</span></span>  <br/> |
|<span data-ttu-id="ee9f1-130">3</span><span class="sxs-lookup"><span data-stu-id="ee9f1-130">3</span></span>  <br/> |<span data-ttu-id="ee9f1-131">followupIcon3</span><span class="sxs-lookup"><span data-stu-id="ee9f1-131">followupIcon3</span></span>  <br/> |<span data-ttu-id="ee9f1-132">Grünes Flag</span><span class="sxs-lookup"><span data-stu-id="ee9f1-132">Green flag</span></span>  <br/> |
|<span data-ttu-id="ee9f1-133">4 </span><span class="sxs-lookup"><span data-stu-id="ee9f1-133">4</span></span>  <br/> |<span data-ttu-id="ee9f1-134">followupIcon4</span><span class="sxs-lookup"><span data-stu-id="ee9f1-134">followupIcon4</span></span>  <br/> |<span data-ttu-id="ee9f1-135">Gelbes Flag</span><span class="sxs-lookup"><span data-stu-id="ee9f1-135">Yellow flag</span></span>  <br/> |
|<span data-ttu-id="ee9f1-136">5 </span><span class="sxs-lookup"><span data-stu-id="ee9f1-136">5</span></span>  <br/> |<span data-ttu-id="ee9f1-137">followupIcon5</span><span class="sxs-lookup"><span data-stu-id="ee9f1-137">followupIcon5</span></span>  <br/> |<span data-ttu-id="ee9f1-138">Blaues Flag</span><span class="sxs-lookup"><span data-stu-id="ee9f1-138">Blue flag</span></span>  <br/> |
|<span data-ttu-id="ee9f1-139">6 </span><span class="sxs-lookup"><span data-stu-id="ee9f1-139">6</span></span>  <br/> |<span data-ttu-id="ee9f1-140">followupIcon6</span><span class="sxs-lookup"><span data-stu-id="ee9f1-140">followupIcon6</span></span>  <br/> |<span data-ttu-id="ee9f1-141">Rotes Flag</span><span class="sxs-lookup"><span data-stu-id="ee9f1-141">Red flag</span></span>  <br/> |
   
## <a name="related-resources"></a><span data-ttu-id="ee9f1-142">Verwandte Ressourcen</span><span class="sxs-lookup"><span data-stu-id="ee9f1-142">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="ee9f1-143">Protokollspezifikationen</span><span class="sxs-lookup"><span data-stu-id="ee9f1-143">Protocol specifications</span></span>

<span data-ttu-id="ee9f1-144">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="ee9f1-144">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="ee9f1-145">Enthält Verweise auf Exchange Server Protokollspezifikationen.</span><span class="sxs-lookup"><span data-stu-id="ee9f1-145">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="ee9f1-146">[[MS-OXOFLAG]](https://msdn.microsoft.com/library/f1e50be4-ed30-4c2a-b5cb-8ff3aaaf9b91%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="ee9f1-146">[[MS-OXOFLAG]](https://msdn.microsoft.com/library/f1e50be4-ed30-4c2a-b5cb-8ff3aaaf9b91%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="ee9f1-147">Gibt die Eigenschaften und Vorgänge im Zusammenhang mit der Kennzeichnung an.</span><span class="sxs-lookup"><span data-stu-id="ee9f1-147">Specifies the properties and operations related to flagging.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="ee9f1-148">Headerdateien</span><span class="sxs-lookup"><span data-stu-id="ee9f1-148">Header files</span></span>

<span data-ttu-id="ee9f1-149">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="ee9f1-149">Mapidefs.h</span></span>
  
> <span data-ttu-id="ee9f1-150">Bietet Datentypdefinitionen.</span><span class="sxs-lookup"><span data-stu-id="ee9f1-150">Provides data type definitions.</span></span>
    
<span data-ttu-id="ee9f1-151">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="ee9f1-151">Mapitags.h</span></span>
  
> <span data-ttu-id="ee9f1-152">Enthält Definitionen von Eigenschaften, die als alternative Namen aufgeführt sind.</span><span class="sxs-lookup"><span data-stu-id="ee9f1-152">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="ee9f1-153">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="ee9f1-153">See also</span></span>



[<span data-ttu-id="ee9f1-154">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="ee9f1-154">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="ee9f1-155">KANONISCHE EIGENSCHAFTEN VON MAPI</span><span class="sxs-lookup"><span data-stu-id="ee9f1-155">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="ee9f1-156">Zuordnen kanonischer Eigenschaftsnamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="ee9f1-156">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="ee9f1-157">Zuordnen von MAPI-Namen zu kanonischen Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="ee9f1-157">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

