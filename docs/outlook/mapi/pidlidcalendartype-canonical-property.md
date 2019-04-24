---
title: Kanonische Pidlidcalendartype (-Eigenschaft
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
ms.openlocfilehash: 6a33559a3e047890153f6a8e0ab40e49c2bf80cb
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32341993"
---
# <a name="pidlidcalendartype-canonical-property"></a><span data-ttu-id="dd45b-103">Kanonische Pidlidcalendartype (-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="dd45b-103">PidLidCalendarType Canonical Property</span></span>

  
  
<span data-ttu-id="dd45b-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="dd45b-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="dd45b-105">Gibt den Wert des Felds CalendarType aus der **dispidApptRecur** ([pidlidappointmentrecur (](pidlidappointmentrecur-canonical-property.md))-Eigenschaft an.</span><span class="sxs-lookup"><span data-stu-id="dd45b-105">Specifies the value of the CalendarType field from the **dispidApptRecur** ([PidLidAppointmentRecur](pidlidappointmentrecur-canonical-property.md)) property.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="dd45b-106">Zugeordnete Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="dd45b-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="dd45b-107">LID_CALENDAR_TYPE</span><span class="sxs-lookup"><span data-stu-id="dd45b-107">LID_CALENDAR_TYPE</span></span>  <br/> |
|<span data-ttu-id="dd45b-108">Eigenschaftensatz:</span><span class="sxs-lookup"><span data-stu-id="dd45b-108">Property set:</span></span>  <br/> |<span data-ttu-id="dd45b-109">PSETID_Meeting</span><span class="sxs-lookup"><span data-stu-id="dd45b-109">PSETID_Meeting</span></span>  <br/> |
|<span data-ttu-id="dd45b-110">Long-ID (Deckel):</span><span class="sxs-lookup"><span data-stu-id="dd45b-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="dd45b-111">0x0000001C</span><span class="sxs-lookup"><span data-stu-id="dd45b-111">0x0000001C</span></span>  <br/> |
|<span data-ttu-id="dd45b-112">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="dd45b-112">Data type:</span></span>  <br/> |<span data-ttu-id="dd45b-113">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="dd45b-113">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="dd45b-114">Bereich:</span><span class="sxs-lookup"><span data-stu-id="dd45b-114">Area:</span></span>  <br/> |<span data-ttu-id="dd45b-115">Meetings</span><span class="sxs-lookup"><span data-stu-id="dd45b-115">Meetings</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="dd45b-116">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="dd45b-116">Remarks</span></span>

<span data-ttu-id="dd45b-117">Wenn die Besprechungsanfrage eine wiederkehrende Reihe oder eine Ausnahme darstellt, ist dies der Wert des Felds CalendarType aus der **dispidApptRecur** -Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="dd45b-117">When the meeting request represents a recurring series or an exception, this is the value of the CalendarType field from the **dispidApptRecur** property.</span></span> <span data-ttu-id="dd45b-118">Andernfalls wird diese Eigenschaft nicht festgelegt, und es wird angenommen, dass Sie 0 ist.</span><span class="sxs-lookup"><span data-stu-id="dd45b-118">Otherwise, this property is not set and assumed to be 0.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="dd45b-119">Zugehörige Ressourcen</span><span class="sxs-lookup"><span data-stu-id="dd45b-119">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="dd45b-120">Protokollspezifikationen</span><span class="sxs-lookup"><span data-stu-id="dd45b-120">Protocol specifications</span></span>

<span data-ttu-id="dd45b-121">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="dd45b-121">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="dd45b-122">Stellt Eigenschaftensatz Definitionen und Verweise auf zugehörige Exchange Server-Protokollspezifikationen bereit.</span><span class="sxs-lookup"><span data-stu-id="dd45b-122">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="dd45b-123">[[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="dd45b-123">[[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="dd45b-124">Gibt die Eigenschaften und Vorgänge für Termin-, Besprechungs-und Antwortnachrichten an.</span><span class="sxs-lookup"><span data-stu-id="dd45b-124">Specifies the properties and operations for appointment, meeting request, and response messages.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="dd45b-125">Header Dateien</span><span class="sxs-lookup"><span data-stu-id="dd45b-125">Header files</span></span>

<span data-ttu-id="dd45b-126">Mapidefs. h</span><span class="sxs-lookup"><span data-stu-id="dd45b-126">Mapidefs.h</span></span>
  
> <span data-ttu-id="dd45b-127">Stellt Datentypdefinitionen bereit.</span><span class="sxs-lookup"><span data-stu-id="dd45b-127">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="dd45b-128">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="dd45b-128">See also</span></span>



[<span data-ttu-id="dd45b-129">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="dd45b-129">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="dd45b-130">Kanonische MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="dd45b-130">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="dd45b-131">Zuordnen von kanonischen Eigenschaftennamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="dd45b-131">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="dd45b-132">Zuordnen von MAPI-Namen zu kanonischen Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="dd45b-132">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

