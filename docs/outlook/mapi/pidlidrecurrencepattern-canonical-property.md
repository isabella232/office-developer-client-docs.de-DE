---
title: PidLidRecurrencePattern (kanonische Eigenschaft)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidRecurrencePattern
api_type:
- COM
ms.assetid: ac21ba98-f16b-4365-9134-bca7748189ee
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: d94ac430df54fc03d96ac761c53ca20201d899c2
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32315932"
---
# <a name="pidlidrecurrencepattern-canonical-property"></a><span data-ttu-id="ca684-103">PidLidRecurrencePattern (kanonische Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="ca684-103">PidLidRecurrencePattern Canonical Property</span></span>

  
  
<span data-ttu-id="ca684-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="ca684-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="ca684-105">Gibt eine Beschreibung des Serienmusters des Kalenderobjekts an.</span><span class="sxs-lookup"><span data-stu-id="ca684-105">Specifies a description of the recurrence pattern of the calendar object.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="ca684-106">Zugeordnete Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="ca684-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="ca684-107">dispidRecurPattern</span><span class="sxs-lookup"><span data-stu-id="ca684-107">dispidRecurPattern</span></span>  <br/> |
|<span data-ttu-id="ca684-108">Eigenschaftensatz:</span><span class="sxs-lookup"><span data-stu-id="ca684-108">Property set:</span></span>  <br/> |<span data-ttu-id="ca684-109">PSETID_Appointment</span><span class="sxs-lookup"><span data-stu-id="ca684-109">PSETID_Appointment</span></span>  <br/> |
|<span data-ttu-id="ca684-110">Lange ID (LID):</span><span class="sxs-lookup"><span data-stu-id="ca684-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="ca684-111">0x00008232</span><span class="sxs-lookup"><span data-stu-id="ca684-111">0x00008232</span></span>  <br/> |
|<span data-ttu-id="ca684-112">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="ca684-112">Data type:</span></span>  <br/> |<span data-ttu-id="ca684-113">PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="ca684-113">PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="ca684-114">Bereich:</span><span class="sxs-lookup"><span data-stu-id="ca684-114">Area:</span></span>  <br/> |<span data-ttu-id="ca684-115">Kalender</span><span class="sxs-lookup"><span data-stu-id="ca684-115">Calendar</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="ca684-116">Hinweise</span><span class="sxs-lookup"><span data-stu-id="ca684-116">Remarks</span></span>

<span data-ttu-id="ca684-117">Wenn diese Eigenschaft festgelegt ist, muss sie auf eine Beschreibung der Wiederholung festgelegt werden, die durch die **dispidApptRecur** ([PidLidAppointmentRecur](pidlidappointmentrecur-canonical-property.md)) -Eigenschaft angegeben wird.</span><span class="sxs-lookup"><span data-stu-id="ca684-117">If this property is set, it must be set to a description of the recurrence that is specified by the **dispidApptRecur** ([PidLidAppointmentRecur](pidlidappointmentrecur-canonical-property.md)) property.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="ca684-118">Verwandte Ressourcen</span><span class="sxs-lookup"><span data-stu-id="ca684-118">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="ca684-119">Protokollspezifikationen</span><span class="sxs-lookup"><span data-stu-id="ca684-119">Protocol specifications</span></span>

<span data-ttu-id="ca684-120">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="ca684-120">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="ca684-121">Stellt Eigenschaftensatzdefinitionen und Verweise auf verwandte Exchange Server zur Verfügung.</span><span class="sxs-lookup"><span data-stu-id="ca684-121">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="ca684-122">[[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="ca684-122">[[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="ca684-123">Gibt die Eigenschaften und Vorgänge für Termin-, Besprechungs- und Antwortnachrichten an.</span><span class="sxs-lookup"><span data-stu-id="ca684-123">Specifies the properties and operations for appointment, meeting request, and response messages.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="ca684-124">Headerdateien</span><span class="sxs-lookup"><span data-stu-id="ca684-124">Header files</span></span>

<span data-ttu-id="ca684-125">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="ca684-125">Mapidefs.h</span></span>
  
> <span data-ttu-id="ca684-126">Bietet Datentypdefinitionen.</span><span class="sxs-lookup"><span data-stu-id="ca684-126">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="ca684-127">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="ca684-127">See also</span></span>



[<span data-ttu-id="ca684-128">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="ca684-128">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="ca684-129">KANONISCHE EIGENSCHAFTEN VON MAPI</span><span class="sxs-lookup"><span data-stu-id="ca684-129">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="ca684-130">Zuordnen kanonischer Eigenschaftsnamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="ca684-130">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="ca684-131">Zuordnen von MAPI-Namen zu kanonischen Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="ca684-131">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

