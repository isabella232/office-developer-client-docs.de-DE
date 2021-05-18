---
title: PidTagFlagStatus (kanonische Eigenschaft)
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
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: bca8fccaa43bb3157b3d4e2af7d6aafa64972b41
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32316296"
---
# <a name="pidtagflagstatus-canonical-property"></a><span data-ttu-id="ec0f6-103">PidTagFlagStatus (kanonische Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="ec0f6-103">PidTagFlagStatus Canonical Property</span></span>

  
  
<span data-ttu-id="ec0f6-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="ec0f6-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="ec0f6-105">Gibt den Flagstatus des Message-Objekts an.</span><span class="sxs-lookup"><span data-stu-id="ec0f6-105">Specifies the flag state of the message object.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="ec0f6-106">Zugeordnete Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="ec0f6-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="ec0f6-107">PR_FLAG_STATUS</span><span class="sxs-lookup"><span data-stu-id="ec0f6-107">PR_FLAG_STATUS</span></span>  <br/> |
|<span data-ttu-id="ec0f6-108">Kennung:</span><span class="sxs-lookup"><span data-stu-id="ec0f6-108">Identifier:</span></span>  <br/> |<span data-ttu-id="ec0f6-109">0x1090</span><span class="sxs-lookup"><span data-stu-id="ec0f6-109">0x1090</span></span>  <br/> |
|<span data-ttu-id="ec0f6-110">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="ec0f6-110">Data type:</span></span>  <br/> |<span data-ttu-id="ec0f6-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="ec0f6-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="ec0f6-112">Bereich:</span><span class="sxs-lookup"><span data-stu-id="ec0f6-112">Area:</span></span>  <br/> |<span data-ttu-id="ec0f6-113">Sonstiges</span><span class="sxs-lookup"><span data-stu-id="ec0f6-113">Miscellaneous</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="ec0f6-114">Hinweise</span><span class="sxs-lookup"><span data-stu-id="ec0f6-114">Remarks</span></span>

<span data-ttu-id="ec0f6-115">Diese Eigenschaft darf in einem besprechungsbezogenen Objekt nicht vorhanden sein und sollte nicht für ein Aufgabenobjekt vorhanden sein.</span><span class="sxs-lookup"><span data-stu-id="ec0f6-115">This property must not exist on a meeting-related object, and it should not exist on a task object.</span></span> <span data-ttu-id="ec0f6-116">Wenn diese Eigenschaft für andere Nachrichtenobjekte festgelegt ist, muss sie auf einen der folgenden Werte festgelegt werden:</span><span class="sxs-lookup"><span data-stu-id="ec0f6-116">When set on other message objects, this property must be set to one of the following values:</span></span>
  
|<span data-ttu-id="ec0f6-117">**Numerischer Wert**</span><span class="sxs-lookup"><span data-stu-id="ec0f6-117">**Numeric value**</span></span>|<span data-ttu-id="ec0f6-118">**Name**</span><span class="sxs-lookup"><span data-stu-id="ec0f6-118">**Name**</span></span>|<span data-ttu-id="ec0f6-119">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="ec0f6-119">**Description**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="ec0f6-120">Nicht vorhanden</span><span class="sxs-lookup"><span data-stu-id="ec0f6-120">Not present</span></span>  <br/> |<span data-ttu-id="ec0f6-121">Nicht zutreffend</span><span class="sxs-lookup"><span data-stu-id="ec0f6-121">N/A</span></span>  <br/> |<span data-ttu-id="ec0f6-122">Unflagged</span><span class="sxs-lookup"><span data-stu-id="ec0f6-122">Unflagged</span></span>  <br/> |
|<span data-ttu-id="ec0f6-123">0x00000001</span><span class="sxs-lookup"><span data-stu-id="ec0f6-123">0x00000001</span></span>  <br/> |<span data-ttu-id="ec0f6-124">followupComplete</span><span class="sxs-lookup"><span data-stu-id="ec0f6-124">followupComplete</span></span>  <br/> |<span data-ttu-id="ec0f6-125">Gekennzeichnet abgeschlossen</span><span class="sxs-lookup"><span data-stu-id="ec0f6-125">Flagged complete</span></span>  <br/> |
|<span data-ttu-id="ec0f6-126">0x00000002</span><span class="sxs-lookup"><span data-stu-id="ec0f6-126">0x00000002</span></span>  <br/> |<span data-ttu-id="ec0f6-127">followupFlagged</span><span class="sxs-lookup"><span data-stu-id="ec0f6-127">followupFlagged</span></span>  <br/> |<span data-ttu-id="ec0f6-128">Gekennzeichnet</span><span class="sxs-lookup"><span data-stu-id="ec0f6-128">Flagged</span></span>  <br/> |
   
## <a name="related-resources"></a><span data-ttu-id="ec0f6-129">Verwandte Ressourcen</span><span class="sxs-lookup"><span data-stu-id="ec0f6-129">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="ec0f6-130">Protokollspezifikationen</span><span class="sxs-lookup"><span data-stu-id="ec0f6-130">Protocol specifications</span></span>

<span data-ttu-id="ec0f6-131">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="ec0f6-131">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="ec0f6-132">Enthält Verweise auf Exchange Server Protokollspezifikationen.</span><span class="sxs-lookup"><span data-stu-id="ec0f6-132">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="ec0f6-133">[[MS-OXOFLAG]](https://msdn.microsoft.com/library/f1e50be4-ed30-4c2a-b5cb-8ff3aaaf9b91%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="ec0f6-133">[[MS-OXOFLAG]](https://msdn.microsoft.com/library/f1e50be4-ed30-4c2a-b5cb-8ff3aaaf9b91%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="ec0f6-134">Gibt die Eigenschaften und Vorgänge im Zusammenhang mit der Kennzeichnung an.</span><span class="sxs-lookup"><span data-stu-id="ec0f6-134">Specifies the properties and operations related to flagging.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="ec0f6-135">Headerdateien</span><span class="sxs-lookup"><span data-stu-id="ec0f6-135">Header files</span></span>

<span data-ttu-id="ec0f6-136">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="ec0f6-136">Mapidefs.h</span></span>
  
> <span data-ttu-id="ec0f6-137">Bietet Datentypdefinitionen.</span><span class="sxs-lookup"><span data-stu-id="ec0f6-137">Provides data type definitions.</span></span>
    
<span data-ttu-id="ec0f6-138">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="ec0f6-138">Mapitags.h</span></span>
  
> <span data-ttu-id="ec0f6-139">Enthält Definitionen von Eigenschaften, die als alternative Namen aufgeführt sind.</span><span class="sxs-lookup"><span data-stu-id="ec0f6-139">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="ec0f6-140">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="ec0f6-140">See also</span></span>



[<span data-ttu-id="ec0f6-141">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="ec0f6-141">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="ec0f6-142">KANONISCHE EIGENSCHAFTEN VON MAPI</span><span class="sxs-lookup"><span data-stu-id="ec0f6-142">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="ec0f6-143">Zuordnen kanonischer Eigenschaftsnamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="ec0f6-143">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="ec0f6-144">Zuordnen von MAPI-Namen zu kanonischen Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="ec0f6-144">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

