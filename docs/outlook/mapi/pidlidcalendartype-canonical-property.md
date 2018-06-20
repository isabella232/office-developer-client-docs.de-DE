---
title: Kanonische PidLidCalendarType-Eigenschaft
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidCalendarType
api_type:
- COM
ms.assetid: 06e066f1-2b7d-4a6b-b88c-85a9bfa83bd3
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: 8e3017d18491fde6b66c3173c43b8b9d0ee37ea8
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19793457"
---
# <a name="pidlidcalendartype-canonical-property"></a><span data-ttu-id="4684e-103">Kanonische PidLidCalendarType-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="4684e-103">PidLidCalendarType Canonical Property</span></span>

  
  
<span data-ttu-id="4684e-104">**Betrifft**: Outlook</span><span class="sxs-lookup"><span data-stu-id="4684e-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="4684e-105">Gibt den Wert des Felds CalendarType aus der Eigenschaft **DispidApptRecur** ([PidLidAppointmentRecur](pidlidappointmentrecur-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="4684e-105">Specifies the value of the CalendarType field from the **dispidApptRecur** ([PidLidAppointmentRecur](pidlidappointmentrecur-canonical-property.md)) property.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="4684e-106">Zugeordneten Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="4684e-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="4684e-107">LID_CALENDAR_TYPE</span><span class="sxs-lookup"><span data-stu-id="4684e-107">LID_CALENDAR_TYPE</span></span>  <br/> |
|<span data-ttu-id="4684e-108">-Eigenschaft festgelegt:</span><span class="sxs-lookup"><span data-stu-id="4684e-108">Property set:</span></span>  <br/> |<span data-ttu-id="4684e-109">PSETID_Meeting</span><span class="sxs-lookup"><span data-stu-id="4684e-109">PSETID_Meeting</span></span>  <br/> |
|<span data-ttu-id="4684e-110">Long-ID (Abdeckung):</span><span class="sxs-lookup"><span data-stu-id="4684e-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="4684e-111">0x0000001C</span><span class="sxs-lookup"><span data-stu-id="4684e-111">0x0000001C</span></span>  <br/> |
|<span data-ttu-id="4684e-112">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="4684e-112">Data type:</span></span>  <br/> |<span data-ttu-id="4684e-113">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="4684e-113">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="4684e-114">Bereich:</span><span class="sxs-lookup"><span data-stu-id="4684e-114">Area:</span></span>  <br/> |<span data-ttu-id="4684e-115">Besprechungen</span><span class="sxs-lookup"><span data-stu-id="4684e-115">Meetings</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="4684e-116">Hinweise</span><span class="sxs-lookup"><span data-stu-id="4684e-116">Remarks</span></span>

<span data-ttu-id="4684e-117">Wenn die Besprechungsanfrage eine Terminserie oder eine Ausnahme darstellt, ist dies der Wert des Felds CalendarType aus der **DispidApptRecur** -Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="4684e-117">When the meeting request represents a recurring series or an exception, this is the value of the CalendarType field from the **dispidApptRecur** property.</span></span> <span data-ttu-id="4684e-118">Anderenfalls diese Eigenschaft nicht festlegen und davon ausgegangen, dass 0 sein.</span><span class="sxs-lookup"><span data-stu-id="4684e-118">Otherwise, this property is not set and assumed to be 0.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="4684e-119">Verwandte Ressourcen</span><span class="sxs-lookup"><span data-stu-id="4684e-119">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="4684e-120">Protokollspezifikationen</span><span class="sxs-lookup"><span data-stu-id="4684e-120">Protocol specifications</span></span>

<span data-ttu-id="4684e-121">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="4684e-121">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="4684e-122">Enthält Eigenschaftendefinitionen und Verweise auf Verwandte Exchange Server-Spezifikationen.</span><span class="sxs-lookup"><span data-stu-id="4684e-122">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="4684e-123">[[MS-OXOCAL]](http://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="4684e-123">[[MS-OXOCAL]](http://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="4684e-124">Gibt die Eigenschaften und Vorgänge für den Termin, einer Besprechungsanfrage und Antwortnachrichten.</span><span class="sxs-lookup"><span data-stu-id="4684e-124">Specifies the properties and operations for appointment, meeting request, and response messages.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="4684e-125">Header-Dateien</span><span class="sxs-lookup"><span data-stu-id="4684e-125">Header files</span></span>

<span data-ttu-id="4684e-126">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="4684e-126">Mapidefs.h</span></span>
  
> <span data-ttu-id="4684e-127">Enthält die Datentypdefinitionen.</span><span class="sxs-lookup"><span data-stu-id="4684e-127">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="4684e-128">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="4684e-128">See also</span></span>



[<span data-ttu-id="4684e-129">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="4684e-129">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="4684e-130">Kanonische MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="4684e-130">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="4684e-131">Zuordnen von kanonischen Eigenschaftennamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="4684e-131">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="4684e-132">Zuordnen von MAPI-Namen zu kanonische Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="4684e-132">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

