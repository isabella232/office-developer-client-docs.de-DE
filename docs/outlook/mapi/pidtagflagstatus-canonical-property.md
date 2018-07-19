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
ms.openlocfilehash: 38df67757082bd12e008e56632ec7e6961ba9d42
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19794370"
---
# <a name="pidtagflagstatus-canonical-property"></a><span data-ttu-id="18ae6-103">PidTagFlagStatus (kanonische Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="18ae6-103">PidTagFlagStatus Canonical Property</span></span>

  
  
<span data-ttu-id="18ae6-104">**Betrifft**: Outlook</span><span class="sxs-lookup"><span data-stu-id="18ae6-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="18ae6-105">Gibt den Status der Kennzeichnung des Message-Objekts.</span><span class="sxs-lookup"><span data-stu-id="18ae6-105">Specifies the flag state of the message object.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="18ae6-106">Zugeordneten Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="18ae6-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="18ae6-107">PR_FLAG_STATUS</span><span class="sxs-lookup"><span data-stu-id="18ae6-107">PR_FLAG_STATUS</span></span>  <br/> |
|<span data-ttu-id="18ae6-108">Bezeichner:</span><span class="sxs-lookup"><span data-stu-id="18ae6-108">Identifier:</span></span>  <br/> |<span data-ttu-id="18ae6-109">0x1090</span><span class="sxs-lookup"><span data-stu-id="18ae6-109">0x1090</span></span>  <br/> |
|<span data-ttu-id="18ae6-110">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="18ae6-110">Data type:</span></span>  <br/> |<span data-ttu-id="18ae6-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="18ae6-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="18ae6-112">Bereich:</span><span class="sxs-lookup"><span data-stu-id="18ae6-112">Area:</span></span>  <br/> |<span data-ttu-id="18ae6-113">Verschiedenes</span><span class="sxs-lookup"><span data-stu-id="18ae6-113">Miscellaneous</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="18ae6-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="18ae6-114">Remarks</span></span>

<span data-ttu-id="18ae6-115">Diese Eigenschaft muss auf ein Objekt bezüglich Besprechungen nicht vorhanden, und sollte nicht auf ein Task-Objekt vorhanden sein.</span><span class="sxs-lookup"><span data-stu-id="18ae6-115">This property must not exist on a meeting-related object, and it should not exist on a task object.</span></span> <span data-ttu-id="18ae6-116">Bei Festlegung auf andere Nachrichtenobjekte, muss diese Eigenschaft auf einen der folgenden Werte festgelegt werden:</span><span class="sxs-lookup"><span data-stu-id="18ae6-116">When set on other message objects, this property must be set to one of the following values:</span></span>
  
|<span data-ttu-id="18ae6-117">**Numerischen Wert**</span><span class="sxs-lookup"><span data-stu-id="18ae6-117">**Numeric value**</span></span>|<span data-ttu-id="18ae6-118">**Name**</span><span class="sxs-lookup"><span data-stu-id="18ae6-118">**Name**</span></span>|<span data-ttu-id="18ae6-119">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="18ae6-119">**Description**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="18ae6-120">Nicht vorhanden</span><span class="sxs-lookup"><span data-stu-id="18ae6-120">Not present</span></span>  <br/> |<span data-ttu-id="18ae6-121">n/v</span><span class="sxs-lookup"><span data-stu-id="18ae6-121">N/A</span></span>  <br/> |<span data-ttu-id="18ae6-122">Nicht gekennzeichnet</span><span class="sxs-lookup"><span data-stu-id="18ae6-122">Unflagged</span></span>  <br/> |
|<span data-ttu-id="18ae6-123">0x00000001</span><span class="sxs-lookup"><span data-stu-id="18ae6-123">0x00000001</span></span>  <br/> |<span data-ttu-id="18ae6-124">followupComplete</span><span class="sxs-lookup"><span data-stu-id="18ae6-124">followupComplete</span></span>  <br/> |<span data-ttu-id="18ae6-125">Abgeschlossen gekennzeichnet</span><span class="sxs-lookup"><span data-stu-id="18ae6-125">Flagged complete</span></span>  <br/> |
|<span data-ttu-id="18ae6-126">0x00000002</span><span class="sxs-lookup"><span data-stu-id="18ae6-126">0x00000002</span></span>  <br/> |<span data-ttu-id="18ae6-127">followupFlagged</span><span class="sxs-lookup"><span data-stu-id="18ae6-127">followupFlagged</span></span>  <br/> |<span data-ttu-id="18ae6-128">Gekennzeichnet</span><span class="sxs-lookup"><span data-stu-id="18ae6-128">Flagged</span></span>  <br/> |
   
## <a name="related-resources"></a><span data-ttu-id="18ae6-129">Verwandte Ressourcen</span><span class="sxs-lookup"><span data-stu-id="18ae6-129">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="18ae6-130">Protokollspezifikationen</span><span class="sxs-lookup"><span data-stu-id="18ae6-130">Protocol specifications</span></span>

<span data-ttu-id="18ae6-131">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="18ae6-131">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="18ae6-132">Bietet Verweise auf Verwandte Exchange Server-Spezifikationen.</span><span class="sxs-lookup"><span data-stu-id="18ae6-132">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="18ae6-133">[[MS-OXOFLAG]](http://msdn.microsoft.com/library/f1e50be4-ed30-4c2a-b5cb-8ff3aaaf9b91%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="18ae6-133">[[MS-OXOFLAG]](http://msdn.microsoft.com/library/f1e50be4-ed30-4c2a-b5cb-8ff3aaaf9b91%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="18ae6-134">Gibt die Eigenschaften und Vorgänge im Zusammenhang mit kennzeichnen.</span><span class="sxs-lookup"><span data-stu-id="18ae6-134">Specifies the properties and operations related to flagging.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="18ae6-135">Header-Dateien</span><span class="sxs-lookup"><span data-stu-id="18ae6-135">Header files</span></span>

<span data-ttu-id="18ae6-136">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="18ae6-136">Mapidefs.h</span></span>
  
> <span data-ttu-id="18ae6-137">Enthält die Datentypdefinitionen.</span><span class="sxs-lookup"><span data-stu-id="18ae6-137">Provides data type definitions.</span></span>
    
<span data-ttu-id="18ae6-138">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="18ae6-138">Mapitags.h</span></span>
  
> <span data-ttu-id="18ae6-139">Enthält Definitionen von Eigenschaften, die als Alternative Namen aufgelistet.</span><span class="sxs-lookup"><span data-stu-id="18ae6-139">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="18ae6-140">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="18ae6-140">See also</span></span>



[<span data-ttu-id="18ae6-141">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="18ae6-141">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="18ae6-142">Kanonische MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="18ae6-142">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="18ae6-143">Zuordnen von kanonischen Eigenschaftennamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="18ae6-143">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="18ae6-144">Zuordnen von MAPI-Namen zu kanonische Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="18ae6-144">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

