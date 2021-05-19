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
ms.openlocfilehash: d2b00c67984d090274a17028ee74e46bee482e2b
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32331577"
---
# <a name="pidlidmeetingtype-canonical-property"></a><span data-ttu-id="d41e5-103">PidLidMeetingType (kanonische Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="d41e5-103">PidLidMeetingType Canonical Property</span></span>

  
  
<span data-ttu-id="d41e5-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="d41e5-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="d41e5-105">Gibt den Typ der Besprechungsanfrage oder Besprechungsaktualisierung an.</span><span class="sxs-lookup"><span data-stu-id="d41e5-105">Indicates the type of meeting request or meeting update.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="d41e5-106">Zugeordnete Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="d41e5-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="d41e5-107">dispidMeetingType</span><span class="sxs-lookup"><span data-stu-id="d41e5-107">dispidMeetingType</span></span>  <br/> |
|<span data-ttu-id="d41e5-108">Eigenschaftensatz:</span><span class="sxs-lookup"><span data-stu-id="d41e5-108">Property set:</span></span>  <br/> |<span data-ttu-id="d41e5-109">PSETID_Meeting</span><span class="sxs-lookup"><span data-stu-id="d41e5-109">PSETID_Meeting</span></span>  <br/> |
|<span data-ttu-id="d41e5-110">Lange ID (LID):</span><span class="sxs-lookup"><span data-stu-id="d41e5-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="d41e5-111">0x00000026</span><span class="sxs-lookup"><span data-stu-id="d41e5-111">0x00000026</span></span>  <br/> |
|<span data-ttu-id="d41e5-112">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="d41e5-112">Data type:</span></span>  <br/> |<span data-ttu-id="d41e5-113">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="d41e5-113">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="d41e5-114">Bereich:</span><span class="sxs-lookup"><span data-stu-id="d41e5-114">Area:</span></span>  <br/> |<span data-ttu-id="d41e5-115">Besprechungen</span><span class="sxs-lookup"><span data-stu-id="d41e5-115">Meetings</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="d41e5-116">Hinweise</span><span class="sxs-lookup"><span data-stu-id="d41e5-116">Remarks</span></span>

<span data-ttu-id="d41e5-117">Der Wert dieser Eigenschaft muss auf eine der folgenden Werte festgelegt werden:</span><span class="sxs-lookup"><span data-stu-id="d41e5-117">The value of this property must be set to one of the following:</span></span>
  
|<span data-ttu-id="d41e5-118">**Eigenschaft**</span><span class="sxs-lookup"><span data-stu-id="d41e5-118">**Property**</span></span>|<span data-ttu-id="d41e5-119">**Wert**</span><span class="sxs-lookup"><span data-stu-id="d41e5-119">**Value**</span></span>|<span data-ttu-id="d41e5-120">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="d41e5-120">**Description**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="d41e5-121">mtgEmpty</span><span class="sxs-lookup"><span data-stu-id="d41e5-121">mtgEmpty</span></span>  <br/> |<span data-ttu-id="d41e5-122">0x00000000</span><span class="sxs-lookup"><span data-stu-id="d41e5-122">0x00000000</span></span>  <br/> |<span data-ttu-id="d41e5-123">Nicht angegeben.</span><span class="sxs-lookup"><span data-stu-id="d41e5-123">Unspecified.</span></span>  <br/> |
|<span data-ttu-id="d41e5-124">mtgRequest</span><span class="sxs-lookup"><span data-stu-id="d41e5-124">mtgRequest</span></span>  <br/> |<span data-ttu-id="d41e5-125">0x00000001</span><span class="sxs-lookup"><span data-stu-id="d41e5-125">0x00000001</span></span>  <br/> |<span data-ttu-id="d41e5-126">Erste Besprechungsanfrage.</span><span class="sxs-lookup"><span data-stu-id="d41e5-126">Initial meeting request.</span></span>  <br/> |
|<span data-ttu-id="d41e5-127">mtgFull</span><span class="sxs-lookup"><span data-stu-id="d41e5-127">mtgFull</span></span>  <br/> |<span data-ttu-id="d41e5-128">0x00010000</span><span class="sxs-lookup"><span data-stu-id="d41e5-128">0x00010000</span></span>  <br/> |<span data-ttu-id="d41e5-129">Vollständige Aktualisierung.</span><span class="sxs-lookup"><span data-stu-id="d41e5-129">Full update.</span></span>  <br/> |
|<span data-ttu-id="d41e5-130">mtgInfo</span><span class="sxs-lookup"><span data-stu-id="d41e5-130">mtgInfo</span></span>  <br/> |<span data-ttu-id="d41e5-131">0x00020000</span><span class="sxs-lookup"><span data-stu-id="d41e5-131">0x00020000</span></span>  <br/> |<span data-ttu-id="d41e5-132">Informationsupdate.</span><span class="sxs-lookup"><span data-stu-id="d41e5-132">Informational update.</span></span>  <br/> |
|<span data-ttu-id="d41e5-133">mtgOutOfDate</span><span class="sxs-lookup"><span data-stu-id="d41e5-133">mtgOutOfDate</span></span>  <br/> |<span data-ttu-id="d41e5-134">0x00080000</span><span class="sxs-lookup"><span data-stu-id="d41e5-134">0x00080000</span></span>  <br/> |<span data-ttu-id="d41e5-135">Eine neuere Besprechungsanfrage oder Besprechungsaktualisierung wurde nach dieser empfangen.</span><span class="sxs-lookup"><span data-stu-id="d41e5-135">A newer meeting request or meeting update was received after this one.</span></span>  <br/> |
|<span data-ttu-id="d41e5-136">mtgDelegatorCopy</span><span class="sxs-lookup"><span data-stu-id="d41e5-136">mtgDelegatorCopy</span></span>  <br/> |<span data-ttu-id="d41e5-137">0x00100000</span><span class="sxs-lookup"><span data-stu-id="d41e5-137">0x00100000</span></span>  <br/> |<span data-ttu-id="d41e5-138">Dies wird für die Kopie des Delegators festgelegt, wenn eine Stellvertretung besprechungsbezogene Objekte behandelt.</span><span class="sxs-lookup"><span data-stu-id="d41e5-138">This is set on the delegator's copy when a delegate handles meeting-related objects.</span></span>  <br/> |
   
## <a name="related-resources"></a><span data-ttu-id="d41e5-139">Verwandte Ressourcen</span><span class="sxs-lookup"><span data-stu-id="d41e5-139">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="d41e5-140">Protokollspezifikationen</span><span class="sxs-lookup"><span data-stu-id="d41e5-140">Protocol specifications</span></span>

<span data-ttu-id="d41e5-141">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="d41e5-141">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="d41e5-142">Stellt Eigenschaftensatzdefinitionen und Verweise auf verwandte Exchange Server zur Verfügung.</span><span class="sxs-lookup"><span data-stu-id="d41e5-142">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="d41e5-143">[[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="d41e5-143">[[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="d41e5-144">Gibt die Eigenschaften und Vorgänge für Termin-, Besprechungs- und Antwortnachrichten an.</span><span class="sxs-lookup"><span data-stu-id="d41e5-144">Specifies the properties and operations for appointment, meeting request, and response messages.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="d41e5-145">Headerdateien</span><span class="sxs-lookup"><span data-stu-id="d41e5-145">Header files</span></span>

<span data-ttu-id="d41e5-146">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="d41e5-146">Mapidefs.h</span></span>
  
> <span data-ttu-id="d41e5-147">Bietet Datentypdefinitionen.</span><span class="sxs-lookup"><span data-stu-id="d41e5-147">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="d41e5-148">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="d41e5-148">See also</span></span>



[<span data-ttu-id="d41e5-149">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="d41e5-149">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="d41e5-150">KANONISCHE EIGENSCHAFTEN VON MAPI</span><span class="sxs-lookup"><span data-stu-id="d41e5-150">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="d41e5-151">Zuordnen kanonischer Eigenschaftsnamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="d41e5-151">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="d41e5-152">Zuordnen von MAPI-Namen zu kanonischen Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="d41e5-152">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

