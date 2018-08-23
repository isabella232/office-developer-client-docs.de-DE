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
ms.openlocfilehash: 8dba5906a00beb6d38e4f3e375a9c57db79d42f1
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2018
ms.locfileid: "22575959"
---
# <a name="pidtagflagstatus-canonical-property"></a><span data-ttu-id="838bc-103">PidTagFlagStatus (kanonische Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="838bc-103">PidTagFlagStatus Canonical Property</span></span>

  
  
<span data-ttu-id="838bc-104">**Betrifft**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="838bc-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="838bc-105">Gibt den Status der Kennzeichnung des Message-Objekts.</span><span class="sxs-lookup"><span data-stu-id="838bc-105">Specifies the flag state of the message object.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="838bc-106">Zugeordnete Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="838bc-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="838bc-107">PR_FLAG_STATUS</span><span class="sxs-lookup"><span data-stu-id="838bc-107">PR_FLAG_STATUS</span></span>  <br/> |
|<span data-ttu-id="838bc-108">Kennung:</span><span class="sxs-lookup"><span data-stu-id="838bc-108">Identifier:</span></span>  <br/> |<span data-ttu-id="838bc-109">0x1090</span><span class="sxs-lookup"><span data-stu-id="838bc-109">0x1090</span></span>  <br/> |
|<span data-ttu-id="838bc-110">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="838bc-110">Data type:</span></span>  <br/> |<span data-ttu-id="838bc-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="838bc-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="838bc-112">Bereich:</span><span class="sxs-lookup"><span data-stu-id="838bc-112">Area:</span></span>  <br/> |<span data-ttu-id="838bc-113">Verschiedenes</span><span class="sxs-lookup"><span data-stu-id="838bc-113">Miscellaneous</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="838bc-114">HinwBemerkungeneise</span><span class="sxs-lookup"><span data-stu-id="838bc-114">Remarks</span></span>

<span data-ttu-id="838bc-115">Diese Eigenschaft muss auf ein Objekt bezüglich Besprechungen nicht vorhanden, und sollte nicht auf ein Task-Objekt vorhanden sein.</span><span class="sxs-lookup"><span data-stu-id="838bc-115">This property must not exist on a meeting-related object, and it should not exist on a task object.</span></span> <span data-ttu-id="838bc-116">Bei Festlegung auf andere Nachrichtenobjekte, muss diese Eigenschaft auf einen der folgenden Werte festgelegt werden:</span><span class="sxs-lookup"><span data-stu-id="838bc-116">When set on other message objects, this property must be set to one of the following values:</span></span>
  
|<span data-ttu-id="838bc-117">**Numerischen Wert**</span><span class="sxs-lookup"><span data-stu-id="838bc-117">**Numeric value**</span></span>|<span data-ttu-id="838bc-118">**Name**</span><span class="sxs-lookup"><span data-stu-id="838bc-118">**Name**</span></span>|<span data-ttu-id="838bc-119">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="838bc-119">**Description**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="838bc-120">Nicht vorhanden</span><span class="sxs-lookup"><span data-stu-id="838bc-120">Not present</span></span>  <br/> |<span data-ttu-id="838bc-121">–</span><span class="sxs-lookup"><span data-stu-id="838bc-121">N/A</span></span>  <br/> |<span data-ttu-id="838bc-122">Nicht gekennzeichnet</span><span class="sxs-lookup"><span data-stu-id="838bc-122">Unflagged</span></span>  <br/> |
|<span data-ttu-id="838bc-123">0x00000001</span><span class="sxs-lookup"><span data-stu-id="838bc-123">0x00000001</span></span>  <br/> |<span data-ttu-id="838bc-124">followupComplete</span><span class="sxs-lookup"><span data-stu-id="838bc-124">followupComplete</span></span>  <br/> |<span data-ttu-id="838bc-125">Abgeschlossen gekennzeichnet</span><span class="sxs-lookup"><span data-stu-id="838bc-125">Flagged complete</span></span>  <br/> |
|<span data-ttu-id="838bc-126">0x00000002</span><span class="sxs-lookup"><span data-stu-id="838bc-126">0x00000002</span></span>  <br/> |<span data-ttu-id="838bc-127">followupFlagged</span><span class="sxs-lookup"><span data-stu-id="838bc-127">followupFlagged</span></span>  <br/> |<span data-ttu-id="838bc-128">Gekennzeichnet</span><span class="sxs-lookup"><span data-stu-id="838bc-128">Flagged</span></span>  <br/> |
   
## <a name="related-resources"></a><span data-ttu-id="838bc-129">Verwandte Ressourcen</span><span class="sxs-lookup"><span data-stu-id="838bc-129">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="838bc-130">Protokollspezifikationen</span><span class="sxs-lookup"><span data-stu-id="838bc-130">Protocol specifications</span></span>

<span data-ttu-id="838bc-131">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="838bc-131">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="838bc-132">Bietet Verweise auf Verwandte Exchange Server-Spezifikationen.</span><span class="sxs-lookup"><span data-stu-id="838bc-132">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="838bc-133">[[MS-OXOFLAG]](http://msdn.microsoft.com/library/f1e50be4-ed30-4c2a-b5cb-8ff3aaaf9b91%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="838bc-133">[[MS-OXOFLAG]](http://msdn.microsoft.com/library/f1e50be4-ed30-4c2a-b5cb-8ff3aaaf9b91%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="838bc-134">Gibt die Eigenschaften und Vorgänge im Zusammenhang mit kennzeichnen.</span><span class="sxs-lookup"><span data-stu-id="838bc-134">Specifies the properties and operations related to flagging.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="838bc-135">Header-Dateien</span><span class="sxs-lookup"><span data-stu-id="838bc-135">Header files</span></span>

<span data-ttu-id="838bc-136">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="838bc-136">Mapidefs.h</span></span>
  
> <span data-ttu-id="838bc-137">Enthält die Datentypdefinitionen.</span><span class="sxs-lookup"><span data-stu-id="838bc-137">Provides data type definitions.</span></span>
    
<span data-ttu-id="838bc-138">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="838bc-138">Mapitags.h</span></span>
  
> <span data-ttu-id="838bc-139">Enthält Definitionen von Eigenschaften, die als Alternative Namen aufgelistet.</span><span class="sxs-lookup"><span data-stu-id="838bc-139">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="838bc-140">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="838bc-140">See also</span></span>



[<span data-ttu-id="838bc-141">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="838bc-141">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="838bc-142">Kanonische MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="838bc-142">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="838bc-143">Zuordnen von kanonischen Eigenschaftennamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="838bc-143">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="838bc-144">Zuordnen von MAPI-Namen zu kanonische Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="838bc-144">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

