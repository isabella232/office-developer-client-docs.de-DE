---
title: Kanonische Pidlidappointmentcolor (-Eigenschaft
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
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: 1ea0830a06f303da8243f927e4a07cc744951ca9
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32345437"
---
# <a name="pidlidappointmentcolor-canonical-property"></a><span data-ttu-id="dd048-103">Kanonische Pidlidappointmentcolor (-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="dd048-103">PidLidAppointmentColor Canonical Property</span></span>

  
  
<span data-ttu-id="dd048-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="dd048-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="dd048-105">Gibt die Farbe an, die beim Anzeigen des Kalenders verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="dd048-105">Specifies the color to use when displaying the calendar.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="dd048-106">Zugeordnete Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="dd048-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="dd048-107">dispidApptColor</span><span class="sxs-lookup"><span data-stu-id="dd048-107">dispidApptColor</span></span>  <br/> |
|<span data-ttu-id="dd048-108">Eigenschaftensatz:</span><span class="sxs-lookup"><span data-stu-id="dd048-108">Property set:</span></span>  <br/> |<span data-ttu-id="dd048-109">PSETID_Appointment</span><span class="sxs-lookup"><span data-stu-id="dd048-109">PSETID_Appointment</span></span>  <br/> |
|<span data-ttu-id="dd048-110">Long-ID (Deckel):</span><span class="sxs-lookup"><span data-stu-id="dd048-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="dd048-111">0x00008214</span><span class="sxs-lookup"><span data-stu-id="dd048-111">0x00008214</span></span>  <br/> |
|<span data-ttu-id="dd048-112">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="dd048-112">Data type:</span></span>  <br/> |<span data-ttu-id="dd048-113">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="dd048-113">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="dd048-114">Bereich:</span><span class="sxs-lookup"><span data-stu-id="dd048-114">Area:</span></span>  <br/> |<span data-ttu-id="dd048-115">Kalender</span><span class="sxs-lookup"><span data-stu-id="dd048-115">Calendar</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="dd048-116">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="dd048-116">Remarks</span></span>

<span data-ttu-id="dd048-117">Diese Eigenschaft gibt die Farbe an, die beim Anzeigen des Kalenders verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="dd048-117">This property specifies the color to use when displaying the calendar.</span></span> <span data-ttu-id="dd048-118">Ein Client oder Server sollte diesen Wert für die Abwärtskompatibilität mit älteren Clients festlegen.</span><span class="sxs-lookup"><span data-stu-id="dd048-118">A client or server should set this value for backward compatibility with older clients.</span></span> <span data-ttu-id="dd048-119">Stattdessen kann der Kalender basierend auf dem Wert der **Schlüsselwörter** ([pidnamekeywords (](pidnamekeywords-canonical-property.md))-Eigenschaft gemäß [[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="dd048-119">It may instead display the calendar based on the value of the **Keywords** ([PidNameKeywords](pidnamekeywords-canonical-property.md)) property as specified in [[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx).</span></span> <span data-ttu-id="dd048-120">Bei Festlegung muss es sich um einen der folgenden Werte handeln.</span><span class="sxs-lookup"><span data-stu-id="dd048-120">When set, the value must be one of the following.</span></span>
  
|<span data-ttu-id="dd048-121">**Wert**</span><span class="sxs-lookup"><span data-stu-id="dd048-121">**Value**</span></span>|<span data-ttu-id="dd048-122">**Color**</span><span class="sxs-lookup"><span data-stu-id="dd048-122">**Color**</span></span>|
|:-----|:-----|
|<span data-ttu-id="dd048-123">0x00000000</span><span class="sxs-lookup"><span data-stu-id="dd048-123">0x00000000</span></span>  <br/> |<span data-ttu-id="dd048-124">Keine</span><span class="sxs-lookup"><span data-stu-id="dd048-124">None</span></span>  <br/> |
|<span data-ttu-id="dd048-125">0x00000001</span><span class="sxs-lookup"><span data-stu-id="dd048-125">0x00000001</span></span>  <br/> |<span data-ttu-id="dd048-126">Rot</span><span class="sxs-lookup"><span data-stu-id="dd048-126">Red</span></span>  <br/> |
|<span data-ttu-id="dd048-127">0x00000002</span><span class="sxs-lookup"><span data-stu-id="dd048-127">0x00000002</span></span>  <br/> |<span data-ttu-id="dd048-128">Blau</span><span class="sxs-lookup"><span data-stu-id="dd048-128">Blue</span></span>  <br/> |
|<span data-ttu-id="dd048-129">0x00000003</span><span class="sxs-lookup"><span data-stu-id="dd048-129">0x00000003</span></span>  <br/> |<span data-ttu-id="dd048-130">Grün</span><span class="sxs-lookup"><span data-stu-id="dd048-130">Green</span></span>  <br/> |
|<span data-ttu-id="dd048-131">0x00000004</span><span class="sxs-lookup"><span data-stu-id="dd048-131">0x00000004</span></span>  <br/> |<span data-ttu-id="dd048-132">Grau</span><span class="sxs-lookup"><span data-stu-id="dd048-132">Grey</span></span>  <br/> |
|<span data-ttu-id="dd048-133">0x00000005</span><span class="sxs-lookup"><span data-stu-id="dd048-133">0x00000005</span></span>  <br/> |<span data-ttu-id="dd048-134">Orange</span><span class="sxs-lookup"><span data-stu-id="dd048-134">Orange</span></span>  <br/> |
|<span data-ttu-id="dd048-135">0x00000006</span><span class="sxs-lookup"><span data-stu-id="dd048-135">0x00000006</span></span>  <br/> |<span data-ttu-id="dd048-136">Cyan</span><span class="sxs-lookup"><span data-stu-id="dd048-136">Cyan</span></span>  <br/> |
|<span data-ttu-id="dd048-137">0x00000007</span><span class="sxs-lookup"><span data-stu-id="dd048-137">0x00000007</span></span>  <br/> |<span data-ttu-id="dd048-138">Olive</span><span class="sxs-lookup"><span data-stu-id="dd048-138">Olive</span></span>  <br/> |
|<span data-ttu-id="dd048-139">0x00000008</span><span class="sxs-lookup"><span data-stu-id="dd048-139">0x00000008</span></span>  <br/> |<span data-ttu-id="dd048-140">Purpur</span><span class="sxs-lookup"><span data-stu-id="dd048-140">Purple</span></span>  <br/> |
|<span data-ttu-id="dd048-141">0x00000009</span><span class="sxs-lookup"><span data-stu-id="dd048-141">0x00000009</span></span>  <br/> |<span data-ttu-id="dd048-142">Teal</span><span class="sxs-lookup"><span data-stu-id="dd048-142">Teal</span></span>  <br/> |
|<span data-ttu-id="dd048-143">0x0000000A</span><span class="sxs-lookup"><span data-stu-id="dd048-143">0x0000000A</span></span>  <br/> |<span data-ttu-id="dd048-144">Gelb</span><span class="sxs-lookup"><span data-stu-id="dd048-144">Yellow</span></span>  <br/> |
   
## <a name="related-resources"></a><span data-ttu-id="dd048-145">Zugehörige Ressourcen</span><span class="sxs-lookup"><span data-stu-id="dd048-145">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="dd048-146">Protokollspezifikationen</span><span class="sxs-lookup"><span data-stu-id="dd048-146">Protocol specifications</span></span>

<span data-ttu-id="dd048-147">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="dd048-147">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="dd048-148">Stellt Eigenschaftensatz Definitionen und Verweise auf zugehörige Exchange Server-Protokollspezifikationen bereit.</span><span class="sxs-lookup"><span data-stu-id="dd048-148">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="dd048-149">[[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="dd048-149">[[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="dd048-150">Gibt die Eigenschaften und Vorgänge für Termin-, Besprechungs-und Antwortnachrichten an.</span><span class="sxs-lookup"><span data-stu-id="dd048-150">Specifies the properties and operations for appointment, meeting request, and response messages.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="dd048-151">Header Dateien</span><span class="sxs-lookup"><span data-stu-id="dd048-151">Header files</span></span>

<span data-ttu-id="dd048-152">Mapidefs. h</span><span class="sxs-lookup"><span data-stu-id="dd048-152">Mapidefs.h</span></span>
  
> <span data-ttu-id="dd048-153">Stellt Datentypdefinitionen bereit.</span><span class="sxs-lookup"><span data-stu-id="dd048-153">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="dd048-154">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="dd048-154">See also</span></span>



[<span data-ttu-id="dd048-155">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="dd048-155">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="dd048-156">Kanonische MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="dd048-156">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="dd048-157">Zuordnen von kanonischen Eigenschaftennamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="dd048-157">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="dd048-158">Zuordnen von MAPI-Namen zu kanonischen Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="dd048-158">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

