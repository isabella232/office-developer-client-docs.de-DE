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
ms.openlocfilehash: ebc7ed4563040e16c71e1df1094667f87a4c09b2
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2018
ms.locfileid: "22572368"
---
# <a name="pidlidmeetingtype-canonical-property"></a><span data-ttu-id="4a7cd-103">PidLidMeetingType (kanonische Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="4a7cd-103">PidLidMeetingType Canonical Property</span></span>

  
  
<span data-ttu-id="4a7cd-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="4a7cd-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="4a7cd-105">Gibt den Typ des einer Besprechungsanfrage oder meeting-Update an.</span><span class="sxs-lookup"><span data-stu-id="4a7cd-105">Indicates the type of meeting request or meeting update.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="4a7cd-106">Zugeordnete Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="4a7cd-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="4a7cd-107">dispidMeetingType</span><span class="sxs-lookup"><span data-stu-id="4a7cd-107">dispidMeetingType</span></span>  <br/> |
|<span data-ttu-id="4a7cd-108">-Eigenschaft festgelegt:</span><span class="sxs-lookup"><span data-stu-id="4a7cd-108">Property set:</span></span>  <br/> |<span data-ttu-id="4a7cd-109">PSETID_Meeting</span><span class="sxs-lookup"><span data-stu-id="4a7cd-109">PSETID_Meeting</span></span>  <br/> |
|<span data-ttu-id="4a7cd-110">Long-ID (Abdeckung):</span><span class="sxs-lookup"><span data-stu-id="4a7cd-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="4a7cd-111">0x00000026</span><span class="sxs-lookup"><span data-stu-id="4a7cd-111">0x00000026</span></span>  <br/> |
|<span data-ttu-id="4a7cd-112">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="4a7cd-112">Data type:</span></span>  <br/> |<span data-ttu-id="4a7cd-113">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="4a7cd-113">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="4a7cd-114">Bereich:</span><span class="sxs-lookup"><span data-stu-id="4a7cd-114">Area:</span></span>  <br/> |<span data-ttu-id="4a7cd-115">Besprechungen</span><span class="sxs-lookup"><span data-stu-id="4a7cd-115">Meetings</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="4a7cd-116">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="4a7cd-116">Remarks</span></span>

<span data-ttu-id="4a7cd-117">Der Wert dieser Eigenschaft muss auf einen der folgenden festgelegt werden:</span><span class="sxs-lookup"><span data-stu-id="4a7cd-117">The value of this property must be set to one of the following:</span></span>
  
|<span data-ttu-id="4a7cd-118">**Eigenschaft**</span><span class="sxs-lookup"><span data-stu-id="4a7cd-118">**Property**</span></span>|<span data-ttu-id="4a7cd-119">**Wert**</span><span class="sxs-lookup"><span data-stu-id="4a7cd-119">**Value**</span></span>|<span data-ttu-id="4a7cd-120">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="4a7cd-120">**Description**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="4a7cd-121">mtgEmpty</span><span class="sxs-lookup"><span data-stu-id="4a7cd-121">mtgEmpty</span></span>  <br/> |<span data-ttu-id="4a7cd-122">0x00000000</span><span class="sxs-lookup"><span data-stu-id="4a7cd-122">0x00000000</span></span>  <br/> |<span data-ttu-id="4a7cd-123">Keine Angabe.</span><span class="sxs-lookup"><span data-stu-id="4a7cd-123">Unspecified.</span></span>  <br/> |
|<span data-ttu-id="4a7cd-124">mtgRequest</span><span class="sxs-lookup"><span data-stu-id="4a7cd-124">mtgRequest</span></span>  <br/> |<span data-ttu-id="4a7cd-125">0x00000001</span><span class="sxs-lookup"><span data-stu-id="4a7cd-125">0x00000001</span></span>  <br/> |<span data-ttu-id="4a7cd-126">Anfängliche Besprechungsanfrage.</span><span class="sxs-lookup"><span data-stu-id="4a7cd-126">Initial meeting request.</span></span>  <br/> |
|<span data-ttu-id="4a7cd-127">mtgFull</span><span class="sxs-lookup"><span data-stu-id="4a7cd-127">mtgFull</span></span>  <br/> |<span data-ttu-id="4a7cd-128">0 x 00010000</span><span class="sxs-lookup"><span data-stu-id="4a7cd-128">0x00010000</span></span>  <br/> |<span data-ttu-id="4a7cd-129">Vollständige Aktualisierung.</span><span class="sxs-lookup"><span data-stu-id="4a7cd-129">Full update.</span></span>  <br/> |
|<span data-ttu-id="4a7cd-130">mtgInfo</span><span class="sxs-lookup"><span data-stu-id="4a7cd-130">mtgInfo</span></span>  <br/> |<span data-ttu-id="4a7cd-131">0 x 00020000</span><span class="sxs-lookup"><span data-stu-id="4a7cd-131">0x00020000</span></span>  <br/> |<span data-ttu-id="4a7cd-132">Informative Update.</span><span class="sxs-lookup"><span data-stu-id="4a7cd-132">Informational update.</span></span>  <br/> |
|<span data-ttu-id="4a7cd-133">mtgOutOfDate</span><span class="sxs-lookup"><span data-stu-id="4a7cd-133">mtgOutOfDate</span></span>  <br/> |<span data-ttu-id="4a7cd-134">0x00080000</span><span class="sxs-lookup"><span data-stu-id="4a7cd-134">0x00080000</span></span>  <br/> |<span data-ttu-id="4a7cd-135">Eine neuere Besprechungsanfrage oder die Besprechungsanfrage wurde nach diesem empfangen.</span><span class="sxs-lookup"><span data-stu-id="4a7cd-135">A newer meeting request or meeting update was received after this one.</span></span>  <br/> |
|<span data-ttu-id="4a7cd-136">mtgDelegatorCopy</span><span class="sxs-lookup"><span data-stu-id="4a7cd-136">mtgDelegatorCopy</span></span>  <br/> |<span data-ttu-id="4a7cd-137">0x00100000</span><span class="sxs-lookup"><span data-stu-id="4a7cd-137">0x00100000</span></span>  <br/> |<span data-ttu-id="4a7cd-138">Dies ist für die Delegator Kopie bei einer Stellvertretung Handles bezüglich Besprechungen Objekte festgelegt.</span><span class="sxs-lookup"><span data-stu-id="4a7cd-138">This is set on the delegator's copy when a delegate handles meeting-related objects.</span></span>  <br/> |
   
## <a name="related-resources"></a><span data-ttu-id="4a7cd-139">Verwandte Ressourcen</span><span class="sxs-lookup"><span data-stu-id="4a7cd-139">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="4a7cd-140">Protokollspezifikationen</span><span class="sxs-lookup"><span data-stu-id="4a7cd-140">Protocol specifications</span></span>

<span data-ttu-id="4a7cd-141">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="4a7cd-141">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="4a7cd-142">Enthält Eigenschaftendefinitionen und Verweise auf Verwandte Exchange Server-Spezifikationen.</span><span class="sxs-lookup"><span data-stu-id="4a7cd-142">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="4a7cd-143">[[MS-OXOCAL]](http://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="4a7cd-143">[[MS-OXOCAL]](http://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="4a7cd-144">Gibt die Eigenschaften und Vorgänge für den Termin, einer Besprechungsanfrage und Antwortnachrichten.</span><span class="sxs-lookup"><span data-stu-id="4a7cd-144">Specifies the properties and operations for appointment, meeting request, and response messages.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="4a7cd-145">Header-Dateien</span><span class="sxs-lookup"><span data-stu-id="4a7cd-145">Header files</span></span>

<span data-ttu-id="4a7cd-146">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="4a7cd-146">Mapidefs.h</span></span>
  
> <span data-ttu-id="4a7cd-147">Enthält die Datentypdefinitionen.</span><span class="sxs-lookup"><span data-stu-id="4a7cd-147">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="4a7cd-148">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="4a7cd-148">See also</span></span>



[<span data-ttu-id="4a7cd-149">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="4a7cd-149">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="4a7cd-150">Kanonische MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="4a7cd-150">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="4a7cd-151">Zuordnen von kanonischen Eigenschaftennamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="4a7cd-151">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="4a7cd-152">Zuordnen von MAPI-Namen zu kanonische Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="4a7cd-152">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

