---
title: PidLidMeetingType (kanonische Eigenschaft)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidMeetingType
api_type:
- COM
ms.assetid: 290b290c-7836-4a7e-bf1a-8d0225a07e56
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: e61ce7798c9e41dbb707d0d5773b116f7cce02d6
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19793662"
---
# <a name="pidlidmeetingtype-canonical-property"></a><span data-ttu-id="d3a85-103">PidLidMeetingType (kanonische Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="d3a85-103">PidLidMeetingType Canonical Property</span></span>

  
  
<span data-ttu-id="d3a85-104">**Betrifft**: Outlook</span><span class="sxs-lookup"><span data-stu-id="d3a85-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="d3a85-105">Gibt den Typ des einer Besprechungsanfrage oder meeting-Update an.</span><span class="sxs-lookup"><span data-stu-id="d3a85-105">Indicates the type of meeting request or meeting update.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="d3a85-106">Zugeordneten Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="d3a85-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="d3a85-107">dispidMeetingType</span><span class="sxs-lookup"><span data-stu-id="d3a85-107">dispidMeetingType</span></span>  <br/> |
|<span data-ttu-id="d3a85-108">-Eigenschaft festgelegt:</span><span class="sxs-lookup"><span data-stu-id="d3a85-108">Property set:</span></span>  <br/> |<span data-ttu-id="d3a85-109">PSETID_Meeting</span><span class="sxs-lookup"><span data-stu-id="d3a85-109">PSETID_Meeting</span></span>  <br/> |
|<span data-ttu-id="d3a85-110">Long-ID (Abdeckung):</span><span class="sxs-lookup"><span data-stu-id="d3a85-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="d3a85-111">0x00000026</span><span class="sxs-lookup"><span data-stu-id="d3a85-111">0x00000026</span></span>  <br/> |
|<span data-ttu-id="d3a85-112">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="d3a85-112">Data type:</span></span>  <br/> |<span data-ttu-id="d3a85-113">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="d3a85-113">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="d3a85-114">Bereich:</span><span class="sxs-lookup"><span data-stu-id="d3a85-114">Area:</span></span>  <br/> |<span data-ttu-id="d3a85-115">Besprechungen</span><span class="sxs-lookup"><span data-stu-id="d3a85-115">Meetings</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="d3a85-116">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="d3a85-116">Remarks</span></span>

<span data-ttu-id="d3a85-117">Der Wert dieser Eigenschaft muss auf einen der folgenden festgelegt werden:</span><span class="sxs-lookup"><span data-stu-id="d3a85-117">The value of this property must be set to one of the following:</span></span>
  
|<span data-ttu-id="d3a85-118">**Eigenschaft**</span><span class="sxs-lookup"><span data-stu-id="d3a85-118">**Property**</span></span>|<span data-ttu-id="d3a85-119">**Wert**</span><span class="sxs-lookup"><span data-stu-id="d3a85-119">**Value**</span></span>|<span data-ttu-id="d3a85-120">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="d3a85-120">**Description**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="d3a85-121">mtgEmpty</span><span class="sxs-lookup"><span data-stu-id="d3a85-121">mtgEmpty</span></span>  <br/> |<span data-ttu-id="d3a85-122">0x00000000</span><span class="sxs-lookup"><span data-stu-id="d3a85-122">0x00000000</span></span>  <br/> |<span data-ttu-id="d3a85-123">Keine Angabe.</span><span class="sxs-lookup"><span data-stu-id="d3a85-123">Unspecified.</span></span>  <br/> |
|<span data-ttu-id="d3a85-124">mtgRequest</span><span class="sxs-lookup"><span data-stu-id="d3a85-124">mtgRequest</span></span>  <br/> |<span data-ttu-id="d3a85-125">0x00000001</span><span class="sxs-lookup"><span data-stu-id="d3a85-125">0x00000001</span></span>  <br/> |<span data-ttu-id="d3a85-126">Anfängliche Besprechungsanfrage.</span><span class="sxs-lookup"><span data-stu-id="d3a85-126">Initial meeting request.</span></span>  <br/> |
|<span data-ttu-id="d3a85-127">mtgFull</span><span class="sxs-lookup"><span data-stu-id="d3a85-127">mtgFull</span></span>  <br/> |<span data-ttu-id="d3a85-128">0 x 00010000</span><span class="sxs-lookup"><span data-stu-id="d3a85-128">0x00010000</span></span>  <br/> |<span data-ttu-id="d3a85-129">Vollständige Aktualisierung.</span><span class="sxs-lookup"><span data-stu-id="d3a85-129">Full update.</span></span>  <br/> |
|<span data-ttu-id="d3a85-130">mtgInfo</span><span class="sxs-lookup"><span data-stu-id="d3a85-130">mtgInfo</span></span>  <br/> |<span data-ttu-id="d3a85-131">0 x 00020000</span><span class="sxs-lookup"><span data-stu-id="d3a85-131">0x00020000</span></span>  <br/> |<span data-ttu-id="d3a85-132">Informative Update.</span><span class="sxs-lookup"><span data-stu-id="d3a85-132">Informational update.</span></span>  <br/> |
|<span data-ttu-id="d3a85-133">mtgOutOfDate</span><span class="sxs-lookup"><span data-stu-id="d3a85-133">mtgOutOfDate</span></span>  <br/> |<span data-ttu-id="d3a85-134">0x00080000</span><span class="sxs-lookup"><span data-stu-id="d3a85-134">0x00080000</span></span>  <br/> |<span data-ttu-id="d3a85-135">Eine neuere Besprechungsanfrage oder die Besprechungsanfrage wurde nach diesem empfangen.</span><span class="sxs-lookup"><span data-stu-id="d3a85-135">A newer meeting request or meeting update was received after this one.</span></span>  <br/> |
|<span data-ttu-id="d3a85-136">mtgDelegatorCopy</span><span class="sxs-lookup"><span data-stu-id="d3a85-136">mtgDelegatorCopy</span></span>  <br/> |<span data-ttu-id="d3a85-137">0x00100000</span><span class="sxs-lookup"><span data-stu-id="d3a85-137">0x00100000</span></span>  <br/> |<span data-ttu-id="d3a85-138">Dies ist für die Delegator Kopie bei einer Stellvertretung Handles bezüglich Besprechungen Objekte festgelegt.</span><span class="sxs-lookup"><span data-stu-id="d3a85-138">This is set on the delegator's copy when a delegate handles meeting-related objects.</span></span>  <br/> |
   
## <a name="related-resources"></a><span data-ttu-id="d3a85-139">Verwandte Ressourcen</span><span class="sxs-lookup"><span data-stu-id="d3a85-139">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="d3a85-140">Protokollspezifikationen</span><span class="sxs-lookup"><span data-stu-id="d3a85-140">Protocol specifications</span></span>

<span data-ttu-id="d3a85-141">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="d3a85-141">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="d3a85-142">Enthält Eigenschaftendefinitionen und Verweise auf Verwandte Exchange Server-Spezifikationen.</span><span class="sxs-lookup"><span data-stu-id="d3a85-142">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="d3a85-143">[[MS-OXOCAL]](http://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="d3a85-143">[[MS-OXOCAL]](http://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="d3a85-144">Gibt die Eigenschaften und Vorgänge für den Termin, einer Besprechungsanfrage und Antwortnachrichten.</span><span class="sxs-lookup"><span data-stu-id="d3a85-144">Specifies the properties and operations for appointment, meeting request, and response messages.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="d3a85-145">Header-Dateien</span><span class="sxs-lookup"><span data-stu-id="d3a85-145">Header files</span></span>

<span data-ttu-id="d3a85-146">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="d3a85-146">Mapidefs.h</span></span>
  
> <span data-ttu-id="d3a85-147">Enthält die Datentypdefinitionen.</span><span class="sxs-lookup"><span data-stu-id="d3a85-147">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="d3a85-148">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="d3a85-148">See also</span></span>



[<span data-ttu-id="d3a85-149">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="d3a85-149">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="d3a85-150">Kanonische MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="d3a85-150">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="d3a85-151">Zuordnen von kanonischen Eigenschaftennamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="d3a85-151">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="d3a85-152">Zuordnen von MAPI-Namen zu kanonische Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="d3a85-152">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

