---
title: Kanonische Pidtagflagstatus (-Eigenschaft
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagFlagStatus
api_type:
- HeaderDef
ms.assetid: b5117360-0939-4535-83fe-3b4a240b5217
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: bca8fccaa43bb3157b3d4e2af7d6aafa64972b41
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32316296"
---
# <a name="pidtagflagstatus-canonical-property"></a><span data-ttu-id="faece-103">Kanonische Pidtagflagstatus (-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="faece-103">PidTagFlagStatus Canonical Property</span></span>

  
  
<span data-ttu-id="faece-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="faece-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="faece-105">Gibt den FlagStatus des Message-Objekts an.</span><span class="sxs-lookup"><span data-stu-id="faece-105">Specifies the flag state of the message object.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="faece-106">Zugeordnete Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="faece-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="faece-107">PR_FLAG_STATUS</span><span class="sxs-lookup"><span data-stu-id="faece-107">PR_FLAG_STATUS</span></span>  <br/> |
|<span data-ttu-id="faece-108">Kennung:</span><span class="sxs-lookup"><span data-stu-id="faece-108">Identifier:</span></span>  <br/> |<span data-ttu-id="faece-109">0x1090</span><span class="sxs-lookup"><span data-stu-id="faece-109">0x1090</span></span>  <br/> |
|<span data-ttu-id="faece-110">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="faece-110">Data type:</span></span>  <br/> |<span data-ttu-id="faece-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="faece-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="faece-112">Bereich:</span><span class="sxs-lookup"><span data-stu-id="faece-112">Area:</span></span>  <br/> |<span data-ttu-id="faece-113">Sonstiges</span><span class="sxs-lookup"><span data-stu-id="faece-113">Miscellaneous</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="faece-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="faece-114">Remarks</span></span>

<span data-ttu-id="faece-115">Diese Eigenschaft darf in einem Besprechungs bezogenen Objekt nicht vorhanden sein und sollte in einem Task-Objekt nicht vorhanden sein.</span><span class="sxs-lookup"><span data-stu-id="faece-115">This property must not exist on a meeting-related object, and it should not exist on a task object.</span></span> <span data-ttu-id="faece-116">Bei Festlegung für andere Nachrichtenobjekte muss diese Eigenschaft auf einen der folgenden Werte festgelegt werden:</span><span class="sxs-lookup"><span data-stu-id="faece-116">When set on other message objects, this property must be set to one of the following values:</span></span>
  
|<span data-ttu-id="faece-117">**Numerischer Wert**</span><span class="sxs-lookup"><span data-stu-id="faece-117">**Numeric value**</span></span>|<span data-ttu-id="faece-118">**Name**</span><span class="sxs-lookup"><span data-stu-id="faece-118">**Name**</span></span>|<span data-ttu-id="faece-119">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="faece-119">**Description**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="faece-120">Nicht vorhanden</span><span class="sxs-lookup"><span data-stu-id="faece-120">Not present</span></span>  <br/> |<span data-ttu-id="faece-121">Nicht zutreffend</span><span class="sxs-lookup"><span data-stu-id="faece-121">N/A</span></span>  <br/> |<span data-ttu-id="faece-122">Unflagged</span><span class="sxs-lookup"><span data-stu-id="faece-122">Unflagged</span></span>  <br/> |
|<span data-ttu-id="faece-123">0x00000001</span><span class="sxs-lookup"><span data-stu-id="faece-123">0x00000001</span></span>  <br/> |<span data-ttu-id="faece-124">followupComplete</span><span class="sxs-lookup"><span data-stu-id="faece-124">followupComplete</span></span>  <br/> |<span data-ttu-id="faece-125">Gekennzeichnet abgeschlossen</span><span class="sxs-lookup"><span data-stu-id="faece-125">Flagged complete</span></span>  <br/> |
|<span data-ttu-id="faece-126">0x00000002</span><span class="sxs-lookup"><span data-stu-id="faece-126">0x00000002</span></span>  <br/> |<span data-ttu-id="faece-127">followupFlagged</span><span class="sxs-lookup"><span data-stu-id="faece-127">followupFlagged</span></span>  <br/> |<span data-ttu-id="faece-128">Gekennzeichnet</span><span class="sxs-lookup"><span data-stu-id="faece-128">Flagged</span></span>  <br/> |
   
## <a name="related-resources"></a><span data-ttu-id="faece-129">Zugehörige Ressourcen</span><span class="sxs-lookup"><span data-stu-id="faece-129">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="faece-130">Protokollspezifikationen</span><span class="sxs-lookup"><span data-stu-id="faece-130">Protocol specifications</span></span>

<span data-ttu-id="faece-131">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="faece-131">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="faece-132">Enthält Verweise auf zugehörige Exchange Server-Protokollspezifikationen.</span><span class="sxs-lookup"><span data-stu-id="faece-132">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="faece-133">[[MS-OXOFLAG]](https://msdn.microsoft.com/library/f1e50be4-ed30-4c2a-b5cb-8ff3aaaf9b91%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="faece-133">[[MS-OXOFLAG]](https://msdn.microsoft.com/library/f1e50be4-ed30-4c2a-b5cb-8ff3aaaf9b91%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="faece-134">Gibt die Eigenschaften und Vorgänge im Zusammenhang mit der Markierung an.</span><span class="sxs-lookup"><span data-stu-id="faece-134">Specifies the properties and operations related to flagging.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="faece-135">Header Dateien</span><span class="sxs-lookup"><span data-stu-id="faece-135">Header files</span></span>

<span data-ttu-id="faece-136">Mapidefs. h</span><span class="sxs-lookup"><span data-stu-id="faece-136">Mapidefs.h</span></span>
  
> <span data-ttu-id="faece-137">Stellt Datentypdefinitionen bereit.</span><span class="sxs-lookup"><span data-stu-id="faece-137">Provides data type definitions.</span></span>
    
<span data-ttu-id="faece-138">Mapitags. h</span><span class="sxs-lookup"><span data-stu-id="faece-138">Mapitags.h</span></span>
  
> <span data-ttu-id="faece-139">Enthält Definitionen von Eigenschaften, die als Alternative Namen aufgeführt sind.</span><span class="sxs-lookup"><span data-stu-id="faece-139">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="faece-140">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="faece-140">See also</span></span>



[<span data-ttu-id="faece-141">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="faece-141">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="faece-142">Kanonische MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="faece-142">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="faece-143">Zuordnen von kanonischen Eigenschaftennamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="faece-143">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="faece-144">Zuordnen von MAPI-Namen zu kanonischen Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="faece-144">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

