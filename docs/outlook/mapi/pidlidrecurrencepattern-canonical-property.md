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
ms.openlocfilehash: 12a55ec4dfe0fb53a07aef73cb4e96771379e483
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2018
ms.locfileid: "22589224"
---
# <a name="pidlidrecurrencepattern-canonical-property"></a><span data-ttu-id="4248f-103">PidLidRecurrencePattern (kanonische Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="4248f-103">PidLidRecurrencePattern Canonical Property</span></span>

  
  
<span data-ttu-id="4248f-104">**Betrifft**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="4248f-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="4248f-105">Gibt eine Beschreibung des Serienmusters des Calendar-Objekts.</span><span class="sxs-lookup"><span data-stu-id="4248f-105">Specifies a description of the recurrence pattern of the calendar object.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="4248f-106">Zugeordnete Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="4248f-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="4248f-107">dispidRecurPattern</span><span class="sxs-lookup"><span data-stu-id="4248f-107">dispidRecurPattern</span></span>  <br/> |
|<span data-ttu-id="4248f-108">-Eigenschaft festgelegt:</span><span class="sxs-lookup"><span data-stu-id="4248f-108">Property set:</span></span>  <br/> |<span data-ttu-id="4248f-109">PSETID_Appointment</span><span class="sxs-lookup"><span data-stu-id="4248f-109">PSETID_Appointment</span></span>  <br/> |
|<span data-ttu-id="4248f-110">Long-ID (Abdeckung):</span><span class="sxs-lookup"><span data-stu-id="4248f-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="4248f-111">0x00008232</span><span class="sxs-lookup"><span data-stu-id="4248f-111">0x00008232</span></span>  <br/> |
|<span data-ttu-id="4248f-112">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="4248f-112">Data type:</span></span>  <br/> |<span data-ttu-id="4248f-113">PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="4248f-113">PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="4248f-114">Bereich:</span><span class="sxs-lookup"><span data-stu-id="4248f-114">Area:</span></span>  <br/> |<span data-ttu-id="4248f-115">Kalender</span><span class="sxs-lookup"><span data-stu-id="4248f-115">Calendar</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="4248f-116">HinwBemerkungeneise</span><span class="sxs-lookup"><span data-stu-id="4248f-116">Remarks</span></span>

<span data-ttu-id="4248f-117">Wenn diese Eigenschaft festgelegt ist, muss er auf eine Beschreibung für die Serie festgelegt sein, die von der **DispidApptRecur** ([PidLidAppointmentRecur](pidlidappointmentrecur-canonical-property.md))-Eigenschaft angegeben wird.</span><span class="sxs-lookup"><span data-stu-id="4248f-117">If this property is set, it must be set to a description of the recurrence that is specified by the **dispidApptRecur** ([PidLidAppointmentRecur](pidlidappointmentrecur-canonical-property.md)) property.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="4248f-118">Verwandte Ressourcen</span><span class="sxs-lookup"><span data-stu-id="4248f-118">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="4248f-119">Protokollspezifikationen</span><span class="sxs-lookup"><span data-stu-id="4248f-119">Protocol specifications</span></span>

<span data-ttu-id="4248f-120">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="4248f-120">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="4248f-121">Enthält Eigenschaftendefinitionen und Verweise auf Verwandte Exchange Server-Spezifikationen.</span><span class="sxs-lookup"><span data-stu-id="4248f-121">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="4248f-122">[[MS-OXOCAL]](http://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="4248f-122">[[MS-OXOCAL]](http://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="4248f-123">Gibt die Eigenschaften und Vorgänge für den Termin, einer Besprechungsanfrage und Antwortnachrichten.</span><span class="sxs-lookup"><span data-stu-id="4248f-123">Specifies the properties and operations for appointment, meeting request, and response messages.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="4248f-124">Header-Dateien</span><span class="sxs-lookup"><span data-stu-id="4248f-124">Header files</span></span>

<span data-ttu-id="4248f-125">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="4248f-125">Mapidefs.h</span></span>
  
> <span data-ttu-id="4248f-126">Enthält die Datentypdefinitionen.</span><span class="sxs-lookup"><span data-stu-id="4248f-126">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="4248f-127">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="4248f-127">See also</span></span>



[<span data-ttu-id="4248f-128">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="4248f-128">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="4248f-129">Kanonische MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="4248f-129">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="4248f-130">Zuordnen von kanonischen Eigenschaftennamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="4248f-130">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="4248f-131">Zuordnen von MAPI-Namen zu kanonische Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="4248f-131">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

