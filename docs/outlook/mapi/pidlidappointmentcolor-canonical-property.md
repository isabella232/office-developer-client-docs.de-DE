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
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: 251377a7b9118437aff3fbb6b2b9376cbf70375c
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19793340"
---
# <a name="pidlidappointmentcolor-canonical-property"></a><span data-ttu-id="8592d-103">PidLidAppointmentColor (kanonische Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="8592d-103">PidLidAppointmentColor Canonical Property</span></span>

  
  
<span data-ttu-id="8592d-104">**Betrifft**: Outlook</span><span class="sxs-lookup"><span data-stu-id="8592d-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="8592d-105">Gibt die Designfarbe zu verwenden, wenn im Kalender anzeigen.</span><span class="sxs-lookup"><span data-stu-id="8592d-105">Specifies the color to use when displaying the calendar.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="8592d-106">Zugeordneten Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="8592d-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="8592d-107">dispidApptColor</span><span class="sxs-lookup"><span data-stu-id="8592d-107">dispidApptColor</span></span>  <br/> |
|<span data-ttu-id="8592d-108">-Eigenschaft festgelegt:</span><span class="sxs-lookup"><span data-stu-id="8592d-108">Property set:</span></span>  <br/> |<span data-ttu-id="8592d-109">PSETID_Appointment</span><span class="sxs-lookup"><span data-stu-id="8592d-109">PSETID_Appointment</span></span>  <br/> |
|<span data-ttu-id="8592d-110">Long-ID (Abdeckung):</span><span class="sxs-lookup"><span data-stu-id="8592d-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="8592d-111">0x00008214</span><span class="sxs-lookup"><span data-stu-id="8592d-111">0x00008214</span></span>  <br/> |
|<span data-ttu-id="8592d-112">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="8592d-112">Data type:</span></span>  <br/> |<span data-ttu-id="8592d-113">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="8592d-113">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="8592d-114">Bereich:</span><span class="sxs-lookup"><span data-stu-id="8592d-114">Area:</span></span>  <br/> |<span data-ttu-id="8592d-115">Kalender</span><span class="sxs-lookup"><span data-stu-id="8592d-115">Calendar</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="8592d-116">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="8592d-116">Remarks</span></span>

<span data-ttu-id="8592d-117">Diese Eigenschaft gibt die Farbe zu verwenden, wenn im Kalender anzeigen.</span><span class="sxs-lookup"><span data-stu-id="8592d-117">This property specifies the color to use when displaying the calendar.</span></span> <span data-ttu-id="8592d-118">Ein Client oder Server sollte diesen Wert für die Abwärtskompatibilität mit älteren Clients festlegen.</span><span class="sxs-lookup"><span data-stu-id="8592d-118">A client or server should set this value for backward compatibility with older clients.</span></span> <span data-ttu-id="8592d-119">Sie können stattdessen im Kalender basierend auf dem Wert der Eigenschaft **Schlüsselwörter** ([PidNameKeywords](pidnamekeywords-canonical-property.md)) als angegebenen in [[MS-OXCMSG]](http://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)angezeigt.</span><span class="sxs-lookup"><span data-stu-id="8592d-119">It may instead display the calendar based on the value of the **Keywords** ([PidNameKeywords](pidnamekeywords-canonical-property.md)) property as specified in [[MS-OXCMSG]](http://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx).</span></span> <span data-ttu-id="8592d-120">Bei Festlegung muss der Wert eine der folgenden sein:</span><span class="sxs-lookup"><span data-stu-id="8592d-120">When set, the value must be one of the following.</span></span>
  
|<span data-ttu-id="8592d-121">**Wert**</span><span class="sxs-lookup"><span data-stu-id="8592d-121">**Value**</span></span>|<span data-ttu-id="8592d-122">**Color**</span><span class="sxs-lookup"><span data-stu-id="8592d-122">**Color**</span></span>|
|:-----|:-----|
|<span data-ttu-id="8592d-123">0x00000000</span><span class="sxs-lookup"><span data-stu-id="8592d-123">0x00000000</span></span>  <br/> |<span data-ttu-id="8592d-124">Keine</span><span class="sxs-lookup"><span data-stu-id="8592d-124">None</span></span>  <br/> |
|<span data-ttu-id="8592d-125">0x00000001</span><span class="sxs-lookup"><span data-stu-id="8592d-125">0x00000001</span></span>  <br/> |<span data-ttu-id="8592d-126">Red</span><span class="sxs-lookup"><span data-stu-id="8592d-126">Red</span></span>  <br/> |
|<span data-ttu-id="8592d-127">0x00000002</span><span class="sxs-lookup"><span data-stu-id="8592d-127">0x00000002</span></span>  <br/> |<span data-ttu-id="8592d-128">Blau</span><span class="sxs-lookup"><span data-stu-id="8592d-128">Blue</span></span>  <br/> |
|<span data-ttu-id="8592d-129">0 x 00000003</span><span class="sxs-lookup"><span data-stu-id="8592d-129">0x00000003</span></span>  <br/> |<span data-ttu-id="8592d-130">Green</span><span class="sxs-lookup"><span data-stu-id="8592d-130">Green</span></span>  <br/> |
|<span data-ttu-id="8592d-131">0 x 00000004</span><span class="sxs-lookup"><span data-stu-id="8592d-131">0x00000004</span></span>  <br/> |<span data-ttu-id="8592d-132">Grau</span><span class="sxs-lookup"><span data-stu-id="8592d-132">Grey</span></span>  <br/> |
|<span data-ttu-id="8592d-133">0 x 00000005</span><span class="sxs-lookup"><span data-stu-id="8592d-133">0x00000005</span></span>  <br/> |<span data-ttu-id="8592d-134">Orange</span><span class="sxs-lookup"><span data-stu-id="8592d-134">Orange</span></span>  <br/> |
|<span data-ttu-id="8592d-135">0 x 00000006</span><span class="sxs-lookup"><span data-stu-id="8592d-135">0x00000006</span></span>  <br/> |<span data-ttu-id="8592d-136">Cyan</span><span class="sxs-lookup"><span data-stu-id="8592d-136">Cyan</span></span>  <br/> |
|<span data-ttu-id="8592d-137">0 x 00000007</span><span class="sxs-lookup"><span data-stu-id="8592d-137">0x00000007</span></span>  <br/> |<span data-ttu-id="8592d-138">Olive</span><span class="sxs-lookup"><span data-stu-id="8592d-138">Olive</span></span>  <br/> |
|<span data-ttu-id="8592d-139">0 x 00000008</span><span class="sxs-lookup"><span data-stu-id="8592d-139">0x00000008</span></span>  <br/> |<span data-ttu-id="8592d-140">Purple</span><span class="sxs-lookup"><span data-stu-id="8592d-140">Purple</span></span>  <br/> |
|<span data-ttu-id="8592d-141">0x00000009</span><span class="sxs-lookup"><span data-stu-id="8592d-141">0x00000009</span></span>  <br/> |<span data-ttu-id="8592d-142">Teal</span><span class="sxs-lookup"><span data-stu-id="8592d-142">Teal</span></span>  <br/> |
|<span data-ttu-id="8592d-143">0x0000000A</span><span class="sxs-lookup"><span data-stu-id="8592d-143">0x0000000A</span></span>  <br/> |<span data-ttu-id="8592d-144">Yellow</span><span class="sxs-lookup"><span data-stu-id="8592d-144">Yellow</span></span>  <br/> |
   
## <a name="related-resources"></a><span data-ttu-id="8592d-145">Verwandte Ressourcen</span><span class="sxs-lookup"><span data-stu-id="8592d-145">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="8592d-146">Protokollspezifikationen</span><span class="sxs-lookup"><span data-stu-id="8592d-146">Protocol specifications</span></span>

<span data-ttu-id="8592d-147">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="8592d-147">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="8592d-148">Enthält Eigenschaftendefinitionen und Verweise auf Verwandte Exchange Server-Spezifikationen.</span><span class="sxs-lookup"><span data-stu-id="8592d-148">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="8592d-149">[[MS-OXOCAL]](http://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="8592d-149">[[MS-OXOCAL]](http://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="8592d-150">Gibt die Eigenschaften und Vorgänge für den Termin, einer Besprechungsanfrage und Antwortnachrichten.</span><span class="sxs-lookup"><span data-stu-id="8592d-150">Specifies the properties and operations for appointment, meeting request, and response messages.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="8592d-151">Header-Dateien</span><span class="sxs-lookup"><span data-stu-id="8592d-151">Header files</span></span>

<span data-ttu-id="8592d-152">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="8592d-152">Mapidefs.h</span></span>
  
> <span data-ttu-id="8592d-153">Enthält die Datentypdefinitionen.</span><span class="sxs-lookup"><span data-stu-id="8592d-153">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="8592d-154">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="8592d-154">See also</span></span>



[<span data-ttu-id="8592d-155">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="8592d-155">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="8592d-156">Kanonische MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="8592d-156">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="8592d-157">Zuordnen von kanonischen Eigenschaftennamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="8592d-157">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="8592d-158">Zuordnen von MAPI-Namen zu kanonische Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="8592d-158">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

