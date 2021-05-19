---
title: PidLidAppointmentColor (kanonische Eigenschaft)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidAppointmentColor
api_type:
- COM
ms.assetid: 91147e85-f440-4463-850b-efc9bdbd36d1
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 1ea0830a06f303da8243f927e4a07cc744951ca9
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32345437"
---
# <a name="pidlidappointmentcolor-canonical-property"></a><span data-ttu-id="4c7e5-103">PidLidAppointmentColor (kanonische Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="4c7e5-103">PidLidAppointmentColor Canonical Property</span></span>

  
  
<span data-ttu-id="4c7e5-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="4c7e5-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="4c7e5-105">Gibt die Farbe an, die beim Anzeigen des Kalenders verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="4c7e5-105">Specifies the color to use when displaying the calendar.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="4c7e5-106">Zugeordnete Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="4c7e5-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="4c7e5-107">dispidApptColor</span><span class="sxs-lookup"><span data-stu-id="4c7e5-107">dispidApptColor</span></span>  <br/> |
|<span data-ttu-id="4c7e5-108">Eigenschaftensatz:</span><span class="sxs-lookup"><span data-stu-id="4c7e5-108">Property set:</span></span>  <br/> |<span data-ttu-id="4c7e5-109">PSETID_Appointment</span><span class="sxs-lookup"><span data-stu-id="4c7e5-109">PSETID_Appointment</span></span>  <br/> |
|<span data-ttu-id="4c7e5-110">Lange ID (LID):</span><span class="sxs-lookup"><span data-stu-id="4c7e5-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="4c7e5-111">0x00008214</span><span class="sxs-lookup"><span data-stu-id="4c7e5-111">0x00008214</span></span>  <br/> |
|<span data-ttu-id="4c7e5-112">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="4c7e5-112">Data type:</span></span>  <br/> |<span data-ttu-id="4c7e5-113">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="4c7e5-113">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="4c7e5-114">Bereich:</span><span class="sxs-lookup"><span data-stu-id="4c7e5-114">Area:</span></span>  <br/> |<span data-ttu-id="4c7e5-115">Kalender</span><span class="sxs-lookup"><span data-stu-id="4c7e5-115">Calendar</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="4c7e5-116">Hinweise</span><span class="sxs-lookup"><span data-stu-id="4c7e5-116">Remarks</span></span>

<span data-ttu-id="4c7e5-117">Diese Eigenschaft gibt die Farbe an, die beim Anzeigen des Kalenders verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="4c7e5-117">This property specifies the color to use when displaying the calendar.</span></span> <span data-ttu-id="4c7e5-118">Ein Client oder Server sollte diesen Wert für die Abwärtskompatibilität mit älteren Clients festlegen.</span><span class="sxs-lookup"><span data-stu-id="4c7e5-118">A client or server should set this value for backward compatibility with older clients.</span></span> <span data-ttu-id="4c7e5-119">Stattdessen kann der Kalender basierend auf dem Wert der **Keywords** ([PidNameKeywords](pidnamekeywords-canonical-property.md)) -Eigenschaft angezeigt werden, wie in [[MS-OXCMSG] angegeben.](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="4c7e5-119">It may instead display the calendar based on the value of the **Keywords** ([PidNameKeywords](pidnamekeywords-canonical-property.md)) property as specified in [[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx).</span></span> <span data-ttu-id="4c7e5-120">Wenn festgelegt, muss der Wert einer der folgenden Werte sein:</span><span class="sxs-lookup"><span data-stu-id="4c7e5-120">When set, the value must be one of the following.</span></span>
  
|<span data-ttu-id="4c7e5-121">**Wert**</span><span class="sxs-lookup"><span data-stu-id="4c7e5-121">**Value**</span></span>|<span data-ttu-id="4c7e5-122">**Color**</span><span class="sxs-lookup"><span data-stu-id="4c7e5-122">**Color**</span></span>|
|:-----|:-----|
|<span data-ttu-id="4c7e5-123">0x00000000</span><span class="sxs-lookup"><span data-stu-id="4c7e5-123">0x00000000</span></span>  <br/> |<span data-ttu-id="4c7e5-124">Keine</span><span class="sxs-lookup"><span data-stu-id="4c7e5-124">None</span></span>  <br/> |
|<span data-ttu-id="4c7e5-125">0x00000001</span><span class="sxs-lookup"><span data-stu-id="4c7e5-125">0x00000001</span></span>  <br/> |<span data-ttu-id="4c7e5-126">Rot</span><span class="sxs-lookup"><span data-stu-id="4c7e5-126">Red</span></span>  <br/> |
|<span data-ttu-id="4c7e5-127">0x00000002</span><span class="sxs-lookup"><span data-stu-id="4c7e5-127">0x00000002</span></span>  <br/> |<span data-ttu-id="4c7e5-128">Blau</span><span class="sxs-lookup"><span data-stu-id="4c7e5-128">Blue</span></span>  <br/> |
|<span data-ttu-id="4c7e5-129">0x00000003</span><span class="sxs-lookup"><span data-stu-id="4c7e5-129">0x00000003</span></span>  <br/> |<span data-ttu-id="4c7e5-130">Grün</span><span class="sxs-lookup"><span data-stu-id="4c7e5-130">Green</span></span>  <br/> |
|<span data-ttu-id="4c7e5-131">0x00000004</span><span class="sxs-lookup"><span data-stu-id="4c7e5-131">0x00000004</span></span>  <br/> |<span data-ttu-id="4c7e5-132">Grau</span><span class="sxs-lookup"><span data-stu-id="4c7e5-132">Grey</span></span>  <br/> |
|<span data-ttu-id="4c7e5-133">0x00000005</span><span class="sxs-lookup"><span data-stu-id="4c7e5-133">0x00000005</span></span>  <br/> |<span data-ttu-id="4c7e5-134">Orange</span><span class="sxs-lookup"><span data-stu-id="4c7e5-134">Orange</span></span>  <br/> |
|<span data-ttu-id="4c7e5-135">0x00000006</span><span class="sxs-lookup"><span data-stu-id="4c7e5-135">0x00000006</span></span>  <br/> |<span data-ttu-id="4c7e5-136">Cyan</span><span class="sxs-lookup"><span data-stu-id="4c7e5-136">Cyan</span></span>  <br/> |
|<span data-ttu-id="4c7e5-137">0x00000007</span><span class="sxs-lookup"><span data-stu-id="4c7e5-137">0x00000007</span></span>  <br/> |<span data-ttu-id="4c7e5-138">Olive</span><span class="sxs-lookup"><span data-stu-id="4c7e5-138">Olive</span></span>  <br/> |
|<span data-ttu-id="4c7e5-139">0x00000008</span><span class="sxs-lookup"><span data-stu-id="4c7e5-139">0x00000008</span></span>  <br/> |<span data-ttu-id="4c7e5-140">Purpur</span><span class="sxs-lookup"><span data-stu-id="4c7e5-140">Purple</span></span>  <br/> |
|<span data-ttu-id="4c7e5-141">0x00000009</span><span class="sxs-lookup"><span data-stu-id="4c7e5-141">0x00000009</span></span>  <br/> |<span data-ttu-id="4c7e5-142">Teal</span><span class="sxs-lookup"><span data-stu-id="4c7e5-142">Teal</span></span>  <br/> |
|<span data-ttu-id="4c7e5-143">0x0000000A</span><span class="sxs-lookup"><span data-stu-id="4c7e5-143">0x0000000A</span></span>  <br/> |<span data-ttu-id="4c7e5-144">Gelb</span><span class="sxs-lookup"><span data-stu-id="4c7e5-144">Yellow</span></span>  <br/> |
   
## <a name="related-resources"></a><span data-ttu-id="4c7e5-145">Verwandte Ressourcen</span><span class="sxs-lookup"><span data-stu-id="4c7e5-145">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="4c7e5-146">Protokollspezifikationen</span><span class="sxs-lookup"><span data-stu-id="4c7e5-146">Protocol specifications</span></span>

<span data-ttu-id="4c7e5-147">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="4c7e5-147">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="4c7e5-148">Stellt Eigenschaftensatzdefinitionen und Verweise auf verwandte Exchange Server zur Verfügung.</span><span class="sxs-lookup"><span data-stu-id="4c7e5-148">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="4c7e5-149">[[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="4c7e5-149">[[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="4c7e5-150">Gibt die Eigenschaften und Vorgänge für Termin-, Besprechungs- und Antwortnachrichten an.</span><span class="sxs-lookup"><span data-stu-id="4c7e5-150">Specifies the properties and operations for appointment, meeting request, and response messages.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="4c7e5-151">Headerdateien</span><span class="sxs-lookup"><span data-stu-id="4c7e5-151">Header files</span></span>

<span data-ttu-id="4c7e5-152">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="4c7e5-152">Mapidefs.h</span></span>
  
> <span data-ttu-id="4c7e5-153">Bietet Datentypdefinitionen.</span><span class="sxs-lookup"><span data-stu-id="4c7e5-153">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="4c7e5-154">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="4c7e5-154">See also</span></span>



[<span data-ttu-id="4c7e5-155">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="4c7e5-155">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="4c7e5-156">KANONISCHE EIGENSCHAFTEN VON MAPI</span><span class="sxs-lookup"><span data-stu-id="4c7e5-156">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="4c7e5-157">Zuordnen kanonischer Eigenschaftsnamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="4c7e5-157">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="4c7e5-158">Zuordnen von MAPI-Namen zu kanonischen Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="4c7e5-158">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

