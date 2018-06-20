---
title: Kanonische PidLidRecurrencePattern-Eigenschaft
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
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: 94656a1444149efeb6e2e9cd3a239ff14fa46937
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19793718"
---
# <a name="pidlidrecurrencepattern-canonical-property"></a><span data-ttu-id="af257-103">Kanonische PidLidRecurrencePattern-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="af257-103">PidLidRecurrencePattern Canonical Property</span></span>

  
  
<span data-ttu-id="af257-104">**Betrifft**: Outlook</span><span class="sxs-lookup"><span data-stu-id="af257-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="af257-105">Gibt eine Beschreibung des Serienmusters des Calendar-Objekts.</span><span class="sxs-lookup"><span data-stu-id="af257-105">Specifies a description of the recurrence pattern of the calendar object.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="af257-106">Zugeordneten Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="af257-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="af257-107">dispidRecurPattern</span><span class="sxs-lookup"><span data-stu-id="af257-107">dispidRecurPattern</span></span>  <br/> |
|<span data-ttu-id="af257-108">-Eigenschaft festgelegt:</span><span class="sxs-lookup"><span data-stu-id="af257-108">Property set:</span></span>  <br/> |<span data-ttu-id="af257-109">PSETID_Appointment</span><span class="sxs-lookup"><span data-stu-id="af257-109">PSETID_Appointment</span></span>  <br/> |
|<span data-ttu-id="af257-110">Long-ID (Abdeckung):</span><span class="sxs-lookup"><span data-stu-id="af257-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="af257-111">0x00008232</span><span class="sxs-lookup"><span data-stu-id="af257-111">0x00008232</span></span>  <br/> |
|<span data-ttu-id="af257-112">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="af257-112">Data type:</span></span>  <br/> |<span data-ttu-id="af257-113">PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="af257-113">PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="af257-114">Bereich:</span><span class="sxs-lookup"><span data-stu-id="af257-114">Area:</span></span>  <br/> |<span data-ttu-id="af257-115">Kalender</span><span class="sxs-lookup"><span data-stu-id="af257-115">Calendar</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="af257-116">Hinweise</span><span class="sxs-lookup"><span data-stu-id="af257-116">Remarks</span></span>

<span data-ttu-id="af257-117">Wenn diese Eigenschaft festgelegt ist, muss er auf eine Beschreibung für die Serie festgelegt sein, die von der **DispidApptRecur** ([PidLidAppointmentRecur](pidlidappointmentrecur-canonical-property.md))-Eigenschaft angegeben wird.</span><span class="sxs-lookup"><span data-stu-id="af257-117">If this property is set, it must be set to a description of the recurrence that is specified by the **dispidApptRecur** ([PidLidAppointmentRecur](pidlidappointmentrecur-canonical-property.md)) property.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="af257-118">Verwandte Ressourcen</span><span class="sxs-lookup"><span data-stu-id="af257-118">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="af257-119">Protokollspezifikationen</span><span class="sxs-lookup"><span data-stu-id="af257-119">Protocol specifications</span></span>

<span data-ttu-id="af257-120">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="af257-120">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="af257-121">Enthält Eigenschaftendefinitionen und Verweise auf Verwandte Exchange Server-Spezifikationen.</span><span class="sxs-lookup"><span data-stu-id="af257-121">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="af257-122">[[MS-OXOCAL]](http://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="af257-122">[[MS-OXOCAL]](http://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="af257-123">Gibt die Eigenschaften und Vorgänge für den Termin, einer Besprechungsanfrage und Antwortnachrichten.</span><span class="sxs-lookup"><span data-stu-id="af257-123">Specifies the properties and operations for appointment, meeting request, and response messages.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="af257-124">Header-Dateien</span><span class="sxs-lookup"><span data-stu-id="af257-124">Header files</span></span>

<span data-ttu-id="af257-125">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="af257-125">Mapidefs.h</span></span>
  
> <span data-ttu-id="af257-126">Enthält die Datentypdefinitionen.</span><span class="sxs-lookup"><span data-stu-id="af257-126">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="af257-127">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="af257-127">See also</span></span>



[<span data-ttu-id="af257-128">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="af257-128">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="af257-129">Kanonische MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="af257-129">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="af257-130">Zuordnen von kanonischen Eigenschaftennamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="af257-130">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="af257-131">Zuordnen von MAPI-Namen zu kanonische Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="af257-131">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

