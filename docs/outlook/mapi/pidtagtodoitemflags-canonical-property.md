---
title: Kanonische Pidtagtodoitemflags (-Eigenschaft
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagToDoItemFlags
api_type:
- COM
ms.assetid: bb7ccb45-ce08-4d22-9259-db15cd267e34
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: 6ddc7231afef0a224b92be7fe86216e56200ab70
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32284483"
---
# <a name="pidtagtodoitemflags-canonical-property"></a><span data-ttu-id="73b66-103">Kanonische Pidtagtodoitemflags (-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="73b66-103">PidTagToDoItemFlags Canonical Property</span></span>

  
  
<span data-ttu-id="73b66-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="73b66-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="73b66-105">Stellt die gekennzeichnete Bedingung eines Aufgabenelements dar.</span><span class="sxs-lookup"><span data-stu-id="73b66-105">Represents a To-Do item's flagged condition.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="73b66-106">Zugeordnete Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="73b66-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="73b66-107">PR_TODO_ITEM_FLAGS</span><span class="sxs-lookup"><span data-stu-id="73b66-107">PR_TODO_ITEM_FLAGS</span></span>  <br/> |
|<span data-ttu-id="73b66-108">Kennung:</span><span class="sxs-lookup"><span data-stu-id="73b66-108">Identifier:</span></span>  <br/> |<span data-ttu-id="73b66-109">0x0E2B</span><span class="sxs-lookup"><span data-stu-id="73b66-109">0x0E2B</span></span>  <br/> |
|<span data-ttu-id="73b66-110">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="73b66-110">Data type:</span></span>  <br/> |<span data-ttu-id="73b66-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="73b66-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="73b66-112">Bereich:</span><span class="sxs-lookup"><span data-stu-id="73b66-112">Area:</span></span>  <br/> |<span data-ttu-id="73b66-113">Nicht transmitable MAPI</span><span class="sxs-lookup"><span data-stu-id="73b66-113">MAPI non-transmittable</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="73b66-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="73b66-114">Remarks</span></span>

<span data-ttu-id="73b66-115">Diese Eigenschaft ist ein Bitfeld, in dem jedes Bit auf 1 festgelegt werden sollte, wenn die zugeordnete Bedingung in der folgenden Tabelle gilt, andernfalls 0.</span><span class="sxs-lookup"><span data-stu-id="73b66-115">This property is a bit field in which each bit should be set to 1 if the associated condition in the following table applies, otherwise 0.</span></span>
  
||||
|:-----|:-----|:-----|
|<span data-ttu-id="73b66-116">Numerischer Wert</span><span class="sxs-lookup"><span data-stu-id="73b66-116">Numeric value</span></span>  <br/> |<span data-ttu-id="73b66-117">Name</span><span class="sxs-lookup"><span data-stu-id="73b66-117">Name</span></span>  <br/> |<span data-ttu-id="73b66-118">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="73b66-118">Description</span></span>  <br/> |
|<span data-ttu-id="73b66-119">Nicht vorhanden</span><span class="sxs-lookup"><span data-stu-id="73b66-119">Not present</span></span>  <br/> |<span data-ttu-id="73b66-120">Nicht zutreffend</span><span class="sxs-lookup"><span data-stu-id="73b66-120">N/A</span></span>  <br/> |<span data-ttu-id="73b66-121">Unflagged</span><span class="sxs-lookup"><span data-stu-id="73b66-121">Unflagged</span></span>  <br/> |
|<span data-ttu-id="73b66-122">1</span><span class="sxs-lookup"><span data-stu-id="73b66-122">1</span></span>  <br/> |<span data-ttu-id="73b66-123">todoTimeFlagged</span><span class="sxs-lookup"><span data-stu-id="73b66-123">todoTimeFlagged</span></span>  <br/> |<span data-ttu-id="73b66-124">Objekt ist Zeit gekennzeichnet</span><span class="sxs-lookup"><span data-stu-id="73b66-124">Object is time flagged</span></span>  <br/> |
|<span data-ttu-id="73b66-125">8</span><span class="sxs-lookup"><span data-stu-id="73b66-125">8</span></span>  <br/> |<span data-ttu-id="73b66-126">todoRecipientFlagged</span><span class="sxs-lookup"><span data-stu-id="73b66-126">todoRecipientFlagged</span></span>  <br/> |<span data-ttu-id="73b66-127">Sollte nur für ein Entwurfsnachrichten Objekt festgelegt werden, und es bedeutet, dass das Objekt für Empfänger gekennzeichnet ist.</span><span class="sxs-lookup"><span data-stu-id="73b66-127">Should only be set on a draft message object, and it means that the object is flagged for recipients.</span></span>  <br/> |
   
<span data-ttu-id="73b66-128">Alle Bits, die nicht in der Tabelle angegeben sind, sind reserviert.</span><span class="sxs-lookup"><span data-stu-id="73b66-128">All bits that are not specified in the table are reserved.</span></span> <span data-ttu-id="73b66-129">Sie müssen ignoriert werden, Sie sollten jedoch beibehalten werden, wenn Sie festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="73b66-129">They must be ignored, but should be preserved if they are set.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="73b66-130">Zugehörige Ressourcen</span><span class="sxs-lookup"><span data-stu-id="73b66-130">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="73b66-131">Protokollspezifikationen</span><span class="sxs-lookup"><span data-stu-id="73b66-131">Protocol specifications</span></span>

<span data-ttu-id="73b66-132">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="73b66-132">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="73b66-133">Enthält Verweise auf zugehörige Exchange Server-Protokollspezifikationen.</span><span class="sxs-lookup"><span data-stu-id="73b66-133">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="73b66-134">[[MS-OXOFLAG]](https://msdn.microsoft.com/library/f1e50be4-ed30-4c2a-b5cb-8ff3aaaf9b91%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="73b66-134">[[MS-OXOFLAG]](https://msdn.microsoft.com/library/f1e50be4-ed30-4c2a-b5cb-8ff3aaaf9b91%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="73b66-135">Gibt die Eigenschaften und Vorgänge im Zusammenhang mit der Markierung an.</span><span class="sxs-lookup"><span data-stu-id="73b66-135">Specifies the properties and operations related to flagging.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="73b66-136">Header Dateien</span><span class="sxs-lookup"><span data-stu-id="73b66-136">Header files</span></span>

<span data-ttu-id="73b66-137">Mapidefs. h</span><span class="sxs-lookup"><span data-stu-id="73b66-137">Mapidefs.h</span></span>
  
> <span data-ttu-id="73b66-138">Stellt Datentypdefinitionen bereit.</span><span class="sxs-lookup"><span data-stu-id="73b66-138">Provides data type definitions.</span></span>
    
<span data-ttu-id="73b66-139">Mapitags. h</span><span class="sxs-lookup"><span data-stu-id="73b66-139">Mapitags.h</span></span>
  
> <span data-ttu-id="73b66-140">Enthält Definitionen von Eigenschaften, die als Alternative Namen aufgeführt sind.</span><span class="sxs-lookup"><span data-stu-id="73b66-140">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="73b66-141">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="73b66-141">See also</span></span>



[<span data-ttu-id="73b66-142">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="73b66-142">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="73b66-143">Kanonische MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="73b66-143">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="73b66-144">Zuordnen von kanonischen Eigenschaftennamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="73b66-144">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="73b66-145">Zuordnen von MAPI-Namen zu kanonischen Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="73b66-145">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

