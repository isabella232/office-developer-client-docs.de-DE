---
title: PidTagToDoItemFlags (kanonische Eigenschaft)
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
ms.openlocfilehash: cae4ef6e4d7634ca2b429eb946aa948f5d90cd92
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19795295"
---
# <a name="pidtagtodoitemflags-canonical-property"></a><span data-ttu-id="856a0-103">PidTagToDoItemFlags (kanonische Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="856a0-103">PidTagToDoItemFlags Canonical Property</span></span>

  
  
<span data-ttu-id="856a0-104">**Betrifft**: Outlook</span><span class="sxs-lookup"><span data-stu-id="856a0-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="856a0-105">Stellt ein Aufgabenelement gekennzeichnete Bedingung dar.</span><span class="sxs-lookup"><span data-stu-id="856a0-105">Represents a To-Do item's flagged condition.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="856a0-106">Zugeordneten Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="856a0-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="856a0-107">PR_TODO_ITEM_FLAGS</span><span class="sxs-lookup"><span data-stu-id="856a0-107">PR_TODO_ITEM_FLAGS</span></span>  <br/> |
|<span data-ttu-id="856a0-108">Bezeichner:</span><span class="sxs-lookup"><span data-stu-id="856a0-108">Identifier:</span></span>  <br/> |<span data-ttu-id="856a0-109">0x0E2B</span><span class="sxs-lookup"><span data-stu-id="856a0-109">0x0E2B</span></span>  <br/> |
|<span data-ttu-id="856a0-110">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="856a0-110">Data type:</span></span>  <br/> |<span data-ttu-id="856a0-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="856a0-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="856a0-112">Bereich:</span><span class="sxs-lookup"><span data-stu-id="856a0-112">Area:</span></span>  <br/> |<span data-ttu-id="856a0-113">MAPI Übertragungseinehit</span><span class="sxs-lookup"><span data-stu-id="856a0-113">MAPI non-transmittable</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="856a0-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="856a0-114">Remarks</span></span>

<span data-ttu-id="856a0-115">Diese Eigenschaft ist ein Bitfeld, in dem jedes Bit auf 1 festgelegt werden sollte, wenn die zugeordnete Bedingung in der folgenden Tabelle angewendet wird, sonst 0.</span><span class="sxs-lookup"><span data-stu-id="856a0-115">This property is a bit field in which each bit should be set to 1 if the associated condition in the following table applies, otherwise 0.</span></span>
  
||||
|:-----|:-----|:-----|
|<span data-ttu-id="856a0-116">Numerischen Wert</span><span class="sxs-lookup"><span data-stu-id="856a0-116">Numeric value</span></span>  <br/> |<span data-ttu-id="856a0-117">Name</span><span class="sxs-lookup"><span data-stu-id="856a0-117">Name</span></span>  <br/> |<span data-ttu-id="856a0-118">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="856a0-118">Description</span></span>  <br/> |
|<span data-ttu-id="856a0-119">Nicht vorhanden</span><span class="sxs-lookup"><span data-stu-id="856a0-119">Not present</span></span>  <br/> |<span data-ttu-id="856a0-120">n/v</span><span class="sxs-lookup"><span data-stu-id="856a0-120">N/A</span></span>  <br/> |<span data-ttu-id="856a0-121">Nicht gekennzeichnet</span><span class="sxs-lookup"><span data-stu-id="856a0-121">Unflagged</span></span>  <br/> |
|<span data-ttu-id="856a0-122">1</span><span class="sxs-lookup"><span data-stu-id="856a0-122">1</span></span>  <br/> |<span data-ttu-id="856a0-123">todoTimeFlagged</span><span class="sxs-lookup"><span data-stu-id="856a0-123">todoTimeFlagged</span></span>  <br/> |<span data-ttu-id="856a0-124">Objekt ist Zeit gekennzeichnet</span><span class="sxs-lookup"><span data-stu-id="856a0-124">Object is time flagged</span></span>  <br/> |
|<span data-ttu-id="856a0-125">8</span><span class="sxs-lookup"><span data-stu-id="856a0-125">8</span></span>  <br/> |<span data-ttu-id="856a0-126">todoRecipientFlagged</span><span class="sxs-lookup"><span data-stu-id="856a0-126">todoRecipientFlagged</span></span>  <br/> |<span data-ttu-id="856a0-127">Sollte nur auf einem Objekt "Message" Entwurf festgelegt werden, und das bedeutet, dass das Objekt für die Empfänger gekennzeichnet ist.</span><span class="sxs-lookup"><span data-stu-id="856a0-127">Should only be set on a draft message object, and it means that the object is flagged for recipients.</span></span>  <br/> |
   
<span data-ttu-id="856a0-128">Alle Bits an, die nicht in der Tabelle angegeben wurden, sind reserviert.</span><span class="sxs-lookup"><span data-stu-id="856a0-128">All bits that are not specified in the table are reserved.</span></span> <span data-ttu-id="856a0-129">Sie müssen ignoriert werden, aber Sie erhalten bleiben sollen, wenn sie festgelegt sind.</span><span class="sxs-lookup"><span data-stu-id="856a0-129">They must be ignored, but should be preserved if they are set.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="856a0-130">Verwandte Ressourcen</span><span class="sxs-lookup"><span data-stu-id="856a0-130">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="856a0-131">Protokollspezifikationen</span><span class="sxs-lookup"><span data-stu-id="856a0-131">Protocol specifications</span></span>

<span data-ttu-id="856a0-132">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="856a0-132">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="856a0-133">Bietet Verweise auf Verwandte Exchange Server-Spezifikationen.</span><span class="sxs-lookup"><span data-stu-id="856a0-133">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="856a0-134">[[MS-OXOFLAG]](http://msdn.microsoft.com/library/f1e50be4-ed30-4c2a-b5cb-8ff3aaaf9b91%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="856a0-134">[[MS-OXOFLAG]](http://msdn.microsoft.com/library/f1e50be4-ed30-4c2a-b5cb-8ff3aaaf9b91%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="856a0-135">Gibt die Eigenschaften und Vorgänge im Zusammenhang mit kennzeichnen.</span><span class="sxs-lookup"><span data-stu-id="856a0-135">Specifies the properties and operations related to flagging.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="856a0-136">Header-Dateien</span><span class="sxs-lookup"><span data-stu-id="856a0-136">Header files</span></span>

<span data-ttu-id="856a0-137">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="856a0-137">Mapidefs.h</span></span>
  
> <span data-ttu-id="856a0-138">Enthält die Datentypdefinitionen.</span><span class="sxs-lookup"><span data-stu-id="856a0-138">Provides data type definitions.</span></span>
    
<span data-ttu-id="856a0-139">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="856a0-139">Mapitags.h</span></span>
  
> <span data-ttu-id="856a0-140">Enthält Definitionen von Eigenschaften, die als Alternative Namen aufgelistet.</span><span class="sxs-lookup"><span data-stu-id="856a0-140">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="856a0-141">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="856a0-141">See also</span></span>



[<span data-ttu-id="856a0-142">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="856a0-142">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="856a0-143">Kanonische MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="856a0-143">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="856a0-144">Zuordnen von kanonischen Eigenschaftennamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="856a0-144">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="856a0-145">Zuordnen von MAPI-Namen zu kanonische Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="856a0-145">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

