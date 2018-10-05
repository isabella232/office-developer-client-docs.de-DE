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
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/04/2018
ms.locfileid: "25399872"
---
# <a name="pidlidappointmentcolor-canonical-property"></a><span data-ttu-id="a24a8-103">PidLidAppointmentColor (kanonische Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="a24a8-103">PidLidAppointmentColor Canonical Property</span></span>

  
  
<span data-ttu-id="a24a8-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="a24a8-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="a24a8-105">Gibt die Designfarbe zu verwenden, wenn im Kalender anzeigen.</span><span class="sxs-lookup"><span data-stu-id="a24a8-105">Specifies the color to use when displaying the calendar.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="a24a8-106">Zugeordnete Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="a24a8-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="a24a8-107">dispidApptColor</span><span class="sxs-lookup"><span data-stu-id="a24a8-107">dispidApptColor</span></span>  <br/> |
|<span data-ttu-id="a24a8-108">-Eigenschaft festgelegt:</span><span class="sxs-lookup"><span data-stu-id="a24a8-108">Property set:</span></span>  <br/> |<span data-ttu-id="a24a8-109">PSETID_Appointment</span><span class="sxs-lookup"><span data-stu-id="a24a8-109">PSETID_Appointment</span></span>  <br/> |
|<span data-ttu-id="a24a8-110">Long-ID (Abdeckung):</span><span class="sxs-lookup"><span data-stu-id="a24a8-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="a24a8-111">0x00008214</span><span class="sxs-lookup"><span data-stu-id="a24a8-111">0x00008214</span></span>  <br/> |
|<span data-ttu-id="a24a8-112">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="a24a8-112">Data type:</span></span>  <br/> |<span data-ttu-id="a24a8-113">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="a24a8-113">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="a24a8-114">Bereich:</span><span class="sxs-lookup"><span data-stu-id="a24a8-114">Area:</span></span>  <br/> |<span data-ttu-id="a24a8-115">Kalender</span><span class="sxs-lookup"><span data-stu-id="a24a8-115">Calendar</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="a24a8-116">Hinweise</span><span class="sxs-lookup"><span data-stu-id="a24a8-116">Remarks</span></span>

<span data-ttu-id="a24a8-117">Diese Eigenschaft gibt die Farbe zu verwenden, wenn im Kalender anzeigen.</span><span class="sxs-lookup"><span data-stu-id="a24a8-117">This property specifies the color to use when displaying the calendar.</span></span> <span data-ttu-id="a24a8-118">Ein Client oder Server sollte diesen Wert für die Abwärtskompatibilität mit älteren Clients festlegen.</span><span class="sxs-lookup"><span data-stu-id="a24a8-118">A client or server should set this value for backward compatibility with older clients.</span></span> <span data-ttu-id="a24a8-119">Sie können stattdessen im Kalender basierend auf dem Wert der Eigenschaft **Schlüsselwörter** ([PidNameKeywords](pidnamekeywords-canonical-property.md)) als angegebenen in [[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)angezeigt.</span><span class="sxs-lookup"><span data-stu-id="a24a8-119">It may instead display the calendar based on the value of the **Keywords** ([PidNameKeywords](pidnamekeywords-canonical-property.md)) property as specified in [[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx).</span></span> <span data-ttu-id="a24a8-120">Bei Festlegung muss der Wert eine der folgenden sein:</span><span class="sxs-lookup"><span data-stu-id="a24a8-120">When set, the value must be one of the following.</span></span>
  
|<span data-ttu-id="a24a8-121">**Wert**</span><span class="sxs-lookup"><span data-stu-id="a24a8-121">**Value**</span></span>|<span data-ttu-id="a24a8-122">**Color**</span><span class="sxs-lookup"><span data-stu-id="a24a8-122">**Color**</span></span>|
|:-----|:-----|
|<span data-ttu-id="a24a8-123">0x00000000</span><span class="sxs-lookup"><span data-stu-id="a24a8-123">0x00000000</span></span>  <br/> |<span data-ttu-id="a24a8-124">Keine</span><span class="sxs-lookup"><span data-stu-id="a24a8-124">None</span></span>  <br/> |
|<span data-ttu-id="a24a8-125">0x00000001</span><span class="sxs-lookup"><span data-stu-id="a24a8-125">0x00000001</span></span>  <br/> |<span data-ttu-id="a24a8-126">Red</span><span class="sxs-lookup"><span data-stu-id="a24a8-126">Red</span></span>  <br/> |
|<span data-ttu-id="a24a8-127">0x00000002</span><span class="sxs-lookup"><span data-stu-id="a24a8-127">0x00000002</span></span>  <br/> |<span data-ttu-id="a24a8-128">Blau</span><span class="sxs-lookup"><span data-stu-id="a24a8-128">Blue</span></span>  <br/> |
|<span data-ttu-id="a24a8-129">0 x 00000003</span><span class="sxs-lookup"><span data-stu-id="a24a8-129">0x00000003</span></span>  <br/> |<span data-ttu-id="a24a8-130">Green</span><span class="sxs-lookup"><span data-stu-id="a24a8-130">Green</span></span>  <br/> |
|<span data-ttu-id="a24a8-131">0 x 00000004</span><span class="sxs-lookup"><span data-stu-id="a24a8-131">0x00000004</span></span>  <br/> |<span data-ttu-id="a24a8-132">Grau</span><span class="sxs-lookup"><span data-stu-id="a24a8-132">Grey</span></span>  <br/> |
|<span data-ttu-id="a24a8-133">0 x 00000005</span><span class="sxs-lookup"><span data-stu-id="a24a8-133">0x00000005</span></span>  <br/> |<span data-ttu-id="a24a8-134">Orange</span><span class="sxs-lookup"><span data-stu-id="a24a8-134">Orange</span></span>  <br/> |
|<span data-ttu-id="a24a8-135">0 x 00000006</span><span class="sxs-lookup"><span data-stu-id="a24a8-135">0x00000006</span></span>  <br/> |<span data-ttu-id="a24a8-136">Cyan</span><span class="sxs-lookup"><span data-stu-id="a24a8-136">Cyan</span></span>  <br/> |
|<span data-ttu-id="a24a8-137">0 x 00000007</span><span class="sxs-lookup"><span data-stu-id="a24a8-137">0x00000007</span></span>  <br/> |<span data-ttu-id="a24a8-138">Olive</span><span class="sxs-lookup"><span data-stu-id="a24a8-138">Olive</span></span>  <br/> |
|<span data-ttu-id="a24a8-139">0 x 00000008</span><span class="sxs-lookup"><span data-stu-id="a24a8-139">0x00000008</span></span>  <br/> |<span data-ttu-id="a24a8-140">Purple</span><span class="sxs-lookup"><span data-stu-id="a24a8-140">Purple</span></span>  <br/> |
|<span data-ttu-id="a24a8-141">0x00000009</span><span class="sxs-lookup"><span data-stu-id="a24a8-141">0x00000009</span></span>  <br/> |<span data-ttu-id="a24a8-142">Teal</span><span class="sxs-lookup"><span data-stu-id="a24a8-142">Teal</span></span>  <br/> |
|<span data-ttu-id="a24a8-143">0x0000000A</span><span class="sxs-lookup"><span data-stu-id="a24a8-143">0x0000000A</span></span>  <br/> |<span data-ttu-id="a24a8-144">Yellow</span><span class="sxs-lookup"><span data-stu-id="a24a8-144">Yellow</span></span>  <br/> |
   
## <a name="related-resources"></a><span data-ttu-id="a24a8-145">Verwandte Ressourcen</span><span class="sxs-lookup"><span data-stu-id="a24a8-145">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="a24a8-146">Protokollspezifikationen</span><span class="sxs-lookup"><span data-stu-id="a24a8-146">Protocol specifications</span></span>

<span data-ttu-id="a24a8-147">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="a24a8-147">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="a24a8-148">Enthält Eigenschaftendefinitionen und Verweise auf Verwandte Exchange Server-Spezifikationen.</span><span class="sxs-lookup"><span data-stu-id="a24a8-148">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="a24a8-149">[[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="a24a8-149">[[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="a24a8-150">Gibt die Eigenschaften und Vorgänge für den Termin, einer Besprechungsanfrage und Antwortnachrichten.</span><span class="sxs-lookup"><span data-stu-id="a24a8-150">Specifies the properties and operations for appointment, meeting request, and response messages.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="a24a8-151">Header-Dateien</span><span class="sxs-lookup"><span data-stu-id="a24a8-151">Header files</span></span>

<span data-ttu-id="a24a8-152">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="a24a8-152">Mapidefs.h</span></span>
  
> <span data-ttu-id="a24a8-153">Enthält die Datentypdefinitionen.</span><span class="sxs-lookup"><span data-stu-id="a24a8-153">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="a24a8-154">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="a24a8-154">See also</span></span>



[<span data-ttu-id="a24a8-155">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="a24a8-155">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="a24a8-156">Kanonische MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="a24a8-156">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="a24a8-157">Zuordnen von kanonischen Eigenschaftennamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="a24a8-157">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="a24a8-158">Zuordnen von MAPI-Namen zu kanonische Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="a24a8-158">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

