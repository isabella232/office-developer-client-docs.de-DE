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
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 6ddc7231afef0a224b92be7fe86216e56200ab70
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32284483"
---
# <a name="pidtagtodoitemflags-canonical-property"></a><span data-ttu-id="d7aac-103">PidTagToDoItemFlags (kanonische Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="d7aac-103">PidTagToDoItemFlags Canonical Property</span></span>

  
  
<span data-ttu-id="d7aac-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="d7aac-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="d7aac-105">Represents a To-Do item's flagged condition.</span><span class="sxs-lookup"><span data-stu-id="d7aac-105">Represents a To-Do item's flagged condition.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="d7aac-106">Zugeordnete Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="d7aac-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="d7aac-107">PR_TODO_ITEM_FLAGS</span><span class="sxs-lookup"><span data-stu-id="d7aac-107">PR_TODO_ITEM_FLAGS</span></span>  <br/> |
|<span data-ttu-id="d7aac-108">Kennung:</span><span class="sxs-lookup"><span data-stu-id="d7aac-108">Identifier:</span></span>  <br/> |<span data-ttu-id="d7aac-109">0x0E2B</span><span class="sxs-lookup"><span data-stu-id="d7aac-109">0x0E2B</span></span>  <br/> |
|<span data-ttu-id="d7aac-110">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="d7aac-110">Data type:</span></span>  <br/> |<span data-ttu-id="d7aac-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="d7aac-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="d7aac-112">Bereich:</span><span class="sxs-lookup"><span data-stu-id="d7aac-112">Area:</span></span>  <br/> |<span data-ttu-id="d7aac-113">MAPI nicht durchlässig</span><span class="sxs-lookup"><span data-stu-id="d7aac-113">MAPI non-transmittable</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="d7aac-114">Hinweise</span><span class="sxs-lookup"><span data-stu-id="d7aac-114">Remarks</span></span>

<span data-ttu-id="d7aac-115">Diese Eigenschaft ist ein Bitfeld, in dem jedes Bit auf 1 festgelegt werden sollte, wenn die zugeordnete Bedingung in der folgenden Tabelle zutrifft, andernfalls 0.</span><span class="sxs-lookup"><span data-stu-id="d7aac-115">This property is a bit field in which each bit should be set to 1 if the associated condition in the following table applies, otherwise 0.</span></span>
  
||||
|:-----|:-----|:-----|
|<span data-ttu-id="d7aac-116">Numerischer Wert</span><span class="sxs-lookup"><span data-stu-id="d7aac-116">Numeric value</span></span>  <br/> |<span data-ttu-id="d7aac-117">Name</span><span class="sxs-lookup"><span data-stu-id="d7aac-117">Name</span></span>  <br/> |<span data-ttu-id="d7aac-118">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="d7aac-118">Description</span></span>  <br/> |
|<span data-ttu-id="d7aac-119">Nicht vorhanden</span><span class="sxs-lookup"><span data-stu-id="d7aac-119">Not present</span></span>  <br/> |<span data-ttu-id="d7aac-120">Nicht zutreffend</span><span class="sxs-lookup"><span data-stu-id="d7aac-120">N/A</span></span>  <br/> |<span data-ttu-id="d7aac-121">Unflagged</span><span class="sxs-lookup"><span data-stu-id="d7aac-121">Unflagged</span></span>  <br/> |
|<span data-ttu-id="d7aac-122">1</span><span class="sxs-lookup"><span data-stu-id="d7aac-122">1</span></span>  <br/> |<span data-ttu-id="d7aac-123">todoTimeFlagged</span><span class="sxs-lookup"><span data-stu-id="d7aac-123">todoTimeFlagged</span></span>  <br/> |<span data-ttu-id="d7aac-124">Objekt ist zeitflagt</span><span class="sxs-lookup"><span data-stu-id="d7aac-124">Object is time flagged</span></span>  <br/> |
|<span data-ttu-id="d7aac-125">8 </span><span class="sxs-lookup"><span data-stu-id="d7aac-125">8</span></span>  <br/> |<span data-ttu-id="d7aac-126">todoRecipientFlagged</span><span class="sxs-lookup"><span data-stu-id="d7aac-126">todoRecipientFlagged</span></span>  <br/> |<span data-ttu-id="d7aac-127">Sollte nur für ein Nachrichtenentwurfsobjekt festgelegt werden, was bedeutet, dass das Objekt für Empfänger gekennzeichnet ist.</span><span class="sxs-lookup"><span data-stu-id="d7aac-127">Should only be set on a draft message object, and it means that the object is flagged for recipients.</span></span>  <br/> |
   
<span data-ttu-id="d7aac-128">Alle Bits, die nicht in der Tabelle angegeben sind, sind reserviert.</span><span class="sxs-lookup"><span data-stu-id="d7aac-128">All bits that are not specified in the table are reserved.</span></span> <span data-ttu-id="d7aac-129">Sie müssen ignoriert werden, sollten jedoch beibehalten werden, wenn sie festgelegt sind.</span><span class="sxs-lookup"><span data-stu-id="d7aac-129">They must be ignored, but should be preserved if they are set.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="d7aac-130">Verwandte Ressourcen</span><span class="sxs-lookup"><span data-stu-id="d7aac-130">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="d7aac-131">Protokollspezifikationen</span><span class="sxs-lookup"><span data-stu-id="d7aac-131">Protocol specifications</span></span>

<span data-ttu-id="d7aac-132">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="d7aac-132">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="d7aac-133">Enthält Verweise auf Exchange Server Protokollspezifikationen.</span><span class="sxs-lookup"><span data-stu-id="d7aac-133">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="d7aac-134">[[MS-OXOFLAG]](https://msdn.microsoft.com/library/f1e50be4-ed30-4c2a-b5cb-8ff3aaaf9b91%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="d7aac-134">[[MS-OXOFLAG]](https://msdn.microsoft.com/library/f1e50be4-ed30-4c2a-b5cb-8ff3aaaf9b91%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="d7aac-135">Gibt die Eigenschaften und Vorgänge im Zusammenhang mit der Kennzeichnung an.</span><span class="sxs-lookup"><span data-stu-id="d7aac-135">Specifies the properties and operations related to flagging.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="d7aac-136">Headerdateien</span><span class="sxs-lookup"><span data-stu-id="d7aac-136">Header files</span></span>

<span data-ttu-id="d7aac-137">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="d7aac-137">Mapidefs.h</span></span>
  
> <span data-ttu-id="d7aac-138">Bietet Datentypdefinitionen.</span><span class="sxs-lookup"><span data-stu-id="d7aac-138">Provides data type definitions.</span></span>
    
<span data-ttu-id="d7aac-139">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="d7aac-139">Mapitags.h</span></span>
  
> <span data-ttu-id="d7aac-140">Enthält Definitionen von Eigenschaften, die als alternative Namen aufgeführt sind.</span><span class="sxs-lookup"><span data-stu-id="d7aac-140">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="d7aac-141">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="d7aac-141">See also</span></span>



[<span data-ttu-id="d7aac-142">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="d7aac-142">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="d7aac-143">KANONISCHE EIGENSCHAFTEN VON MAPI</span><span class="sxs-lookup"><span data-stu-id="d7aac-143">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="d7aac-144">Zuordnen kanonischer Eigenschaftsnamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="d7aac-144">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="d7aac-145">Zuordnen von MAPI-Namen zu kanonischen Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="d7aac-145">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

