---
title: PidLidCalendarType (kanonische Eigenschaft)
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
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 6a33559a3e047890153f6a8e0ab40e49c2bf80cb
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/04/2018
ms.locfileid: "25396519"
---
# <a name="pidlidcalendartype-canonical-property"></a><span data-ttu-id="18213-103">PidLidCalendarType (kanonische Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="18213-103">PidLidCalendarType Canonical Property</span></span>

  
  
<span data-ttu-id="18213-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="18213-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="18213-105">Gibt den Wert des Felds CalendarType aus der Eigenschaft **DispidApptRecur** ([PidLidAppointmentRecur](pidlidappointmentrecur-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="18213-105">Specifies the value of the CalendarType field from the **dispidApptRecur** ([PidLidAppointmentRecur](pidlidappointmentrecur-canonical-property.md)) property.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="18213-106">Zugeordnete Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="18213-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="18213-107">LID_CALENDAR_TYPE</span><span class="sxs-lookup"><span data-stu-id="18213-107">LID_CALENDAR_TYPE</span></span>  <br/> |
|<span data-ttu-id="18213-108">-Eigenschaft festgelegt:</span><span class="sxs-lookup"><span data-stu-id="18213-108">Property set:</span></span>  <br/> |<span data-ttu-id="18213-109">PSETID_Meeting</span><span class="sxs-lookup"><span data-stu-id="18213-109">PSETID_Meeting</span></span>  <br/> |
|<span data-ttu-id="18213-110">Long-ID (Abdeckung):</span><span class="sxs-lookup"><span data-stu-id="18213-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="18213-111">0x0000001C</span><span class="sxs-lookup"><span data-stu-id="18213-111">0x0000001C</span></span>  <br/> |
|<span data-ttu-id="18213-112">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="18213-112">Data type:</span></span>  <br/> |<span data-ttu-id="18213-113">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="18213-113">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="18213-114">Bereich:</span><span class="sxs-lookup"><span data-stu-id="18213-114">Area:</span></span>  <br/> |<span data-ttu-id="18213-115">Besprechungen</span><span class="sxs-lookup"><span data-stu-id="18213-115">Meetings</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="18213-116">Hinweise</span><span class="sxs-lookup"><span data-stu-id="18213-116">Remarks</span></span>

<span data-ttu-id="18213-117">Wenn die Besprechungsanfrage eine Terminserie oder eine Ausnahme darstellt, ist dies der Wert des Felds CalendarType aus der **DispidApptRecur** -Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="18213-117">When the meeting request represents a recurring series or an exception, this is the value of the CalendarType field from the **dispidApptRecur** property.</span></span> <span data-ttu-id="18213-118">Anderenfalls diese Eigenschaft nicht festlegen und davon ausgegangen, dass 0 sein.</span><span class="sxs-lookup"><span data-stu-id="18213-118">Otherwise, this property is not set and assumed to be 0.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="18213-119">Verwandte Ressourcen</span><span class="sxs-lookup"><span data-stu-id="18213-119">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="18213-120">Protokollspezifikationen</span><span class="sxs-lookup"><span data-stu-id="18213-120">Protocol specifications</span></span>

<span data-ttu-id="18213-121">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="18213-121">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="18213-122">Enthält Eigenschaftendefinitionen und Verweise auf Verwandte Exchange Server-Spezifikationen.</span><span class="sxs-lookup"><span data-stu-id="18213-122">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="18213-123">[[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="18213-123">[[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="18213-124">Gibt die Eigenschaften und Vorgänge für den Termin, einer Besprechungsanfrage und Antwortnachrichten.</span><span class="sxs-lookup"><span data-stu-id="18213-124">Specifies the properties and operations for appointment, meeting request, and response messages.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="18213-125">Header-Dateien</span><span class="sxs-lookup"><span data-stu-id="18213-125">Header files</span></span>

<span data-ttu-id="18213-126">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="18213-126">Mapidefs.h</span></span>
  
> <span data-ttu-id="18213-127">Enthält die Datentypdefinitionen.</span><span class="sxs-lookup"><span data-stu-id="18213-127">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="18213-128">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="18213-128">See also</span></span>



[<span data-ttu-id="18213-129">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="18213-129">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="18213-130">Kanonische MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="18213-130">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="18213-131">Zuordnen von kanonischen Eigenschaftennamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="18213-131">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="18213-132">Zuordnen von MAPI-Namen zu kanonische Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="18213-132">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

