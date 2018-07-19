---
title: PidLidRecurrenceType (kanonische Eigenschaft)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidRecurrenceType
api_type:
- COM
ms.assetid: 81ad2e8a-661f-4fc7-bee4-848db3285e31
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 9fecd67c370333064fd593634ad2a924a3005d28
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19793725"
---
# <a name="pidlidrecurrencetype-canonical-property"></a><span data-ttu-id="91bb7-103">PidLidRecurrenceType (kanonische Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="91bb7-103">PidLidRecurrenceType Canonical Property</span></span>

  
  
<span data-ttu-id="91bb7-104">**Betrifft**: Outlook</span><span class="sxs-lookup"><span data-stu-id="91bb7-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="91bb7-105">Gibt den Serientyp von sich wiederholenden Reihe.</span><span class="sxs-lookup"><span data-stu-id="91bb7-105">Specifies the recurrence type of the recurring series.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="91bb7-106">Zugeordneten Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="91bb7-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="91bb7-107">dispidRecurType</span><span class="sxs-lookup"><span data-stu-id="91bb7-107">dispidRecurType</span></span>  <br/> |
|<span data-ttu-id="91bb7-108">-Eigenschaft festgelegt:</span><span class="sxs-lookup"><span data-stu-id="91bb7-108">Property set:</span></span>  <br/> |<span data-ttu-id="91bb7-109">PSETID_Appointment</span><span class="sxs-lookup"><span data-stu-id="91bb7-109">PSETID_Appointment</span></span>  <br/> |
|<span data-ttu-id="91bb7-110">Long-ID (Abdeckung):</span><span class="sxs-lookup"><span data-stu-id="91bb7-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="91bb7-111">0x00008231</span><span class="sxs-lookup"><span data-stu-id="91bb7-111">0x00008231</span></span>  <br/> |
|<span data-ttu-id="91bb7-112">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="91bb7-112">Data type:</span></span>  <br/> |<span data-ttu-id="91bb7-113">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="91bb7-113">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="91bb7-114">Bereich:</span><span class="sxs-lookup"><span data-stu-id="91bb7-114">Area:</span></span>  <br/> |<span data-ttu-id="91bb7-115">Kalender</span><span class="sxs-lookup"><span data-stu-id="91bb7-115">Calendar</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="91bb7-116">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="91bb7-116">Remarks</span></span>

<span data-ttu-id="91bb7-117">Diese Eigenschaft gibt an, welche Serie von sich wiederholenden Reihe mithilfe der unten aufgeführten Werte.</span><span class="sxs-lookup"><span data-stu-id="91bb7-117">This property specifies the recurrence type of the recurring series by using one of the values listed below.</span></span>
  
|<span data-ttu-id="91bb7-118">**Status**</span><span class="sxs-lookup"><span data-stu-id="91bb7-118">**Status**</span></span>|<span data-ttu-id="91bb7-119">**Wert**</span><span class="sxs-lookup"><span data-stu-id="91bb7-119">**Value**</span></span>|<span data-ttu-id="91bb7-120">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="91bb7-120">**Description**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="91bb7-121">rectypeNone</span><span class="sxs-lookup"><span data-stu-id="91bb7-121">rectypeNone</span></span>  <br/> |<span data-ttu-id="91bb7-122">0</span><span class="sxs-lookup"><span data-stu-id="91bb7-122">0</span></span>  <br/> |<span data-ttu-id="91bb7-123">Eine einzelne Instanz eines Termins.</span><span class="sxs-lookup"><span data-stu-id="91bb7-123">A single instance appointment.</span></span>  <br/> |
|<span data-ttu-id="91bb7-124">rectypeDaily</span><span class="sxs-lookup"><span data-stu-id="91bb7-124">rectypeDaily</span></span>  <br/> |<span data-ttu-id="91bb7-125">1</span><span class="sxs-lookup"><span data-stu-id="91bb7-125">1</span></span>  <br/> |<span data-ttu-id="91bb7-126">Ein tägliches Serienmuster.</span><span class="sxs-lookup"><span data-stu-id="91bb7-126">A daily recurrence pattern.</span></span>  <br/> |
|<span data-ttu-id="91bb7-127">rectypeWeekly</span><span class="sxs-lookup"><span data-stu-id="91bb7-127">rectypeWeekly</span></span>  <br/> |<span data-ttu-id="91bb7-128">2</span><span class="sxs-lookup"><span data-stu-id="91bb7-128">2</span></span>  <br/> |<span data-ttu-id="91bb7-129">Ein wöchentliches Serienmuster.</span><span class="sxs-lookup"><span data-stu-id="91bb7-129">A weekly recurrence pattern.</span></span>  <br/> |
|<span data-ttu-id="91bb7-130">rectypeMonthly</span><span class="sxs-lookup"><span data-stu-id="91bb7-130">rectypeMonthly</span></span>  <br/> |<span data-ttu-id="91bb7-131">3</span><span class="sxs-lookup"><span data-stu-id="91bb7-131">3</span></span>  <br/> |<span data-ttu-id="91bb7-132">Ein monatliches Serienmuster.</span><span class="sxs-lookup"><span data-stu-id="91bb7-132">A monthly recurrence pattern.</span></span>  <br/> |
|<span data-ttu-id="91bb7-133">rectypeYearly</span><span class="sxs-lookup"><span data-stu-id="91bb7-133">rectypeYearly</span></span>  <br/> |<span data-ttu-id="91bb7-134">4</span><span class="sxs-lookup"><span data-stu-id="91bb7-134">4</span></span>  <br/> |<span data-ttu-id="91bb7-135">Ein jährliches Serienmuster.</span><span class="sxs-lookup"><span data-stu-id="91bb7-135">A yearly recurrence pattern.</span></span>  <br/> |
   
## <a name="related-resources"></a><span data-ttu-id="91bb7-136">Verwandte Ressourcen</span><span class="sxs-lookup"><span data-stu-id="91bb7-136">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="91bb7-137">Protokollspezifikationen</span><span class="sxs-lookup"><span data-stu-id="91bb7-137">Protocol specifications</span></span>

<span data-ttu-id="91bb7-138">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="91bb7-138">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="91bb7-139">Enthält Eigenschaftendefinitionen und Verweise auf Verwandte Exchange Server-Spezifikationen.</span><span class="sxs-lookup"><span data-stu-id="91bb7-139">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="91bb7-140">[[MS-OXOCAL]](http://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="91bb7-140">[[MS-OXOCAL]](http://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="91bb7-141">Gibt die Eigenschaften und Vorgänge für den Termin, einer Besprechungsanfrage und Antwortnachrichten.</span><span class="sxs-lookup"><span data-stu-id="91bb7-141">Specifies the properties and operations for appointment, meeting request, and response messages.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="91bb7-142">Header-Dateien</span><span class="sxs-lookup"><span data-stu-id="91bb7-142">Header files</span></span>

<span data-ttu-id="91bb7-143">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="91bb7-143">Mapidefs.h</span></span>
  
> <span data-ttu-id="91bb7-144">Enthält die Datentypdefinitionen.</span><span class="sxs-lookup"><span data-stu-id="91bb7-144">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="91bb7-145">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="91bb7-145">See also</span></span>



[<span data-ttu-id="91bb7-146">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="91bb7-146">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="91bb7-147">Kanonische MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="91bb7-147">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="91bb7-148">Zuordnen von kanonischen Eigenschaftennamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="91bb7-148">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="91bb7-149">Zuordnen von MAPI-Namen zu kanonische Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="91bb7-149">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

