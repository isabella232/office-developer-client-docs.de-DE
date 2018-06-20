---
title: Kanonische PidLidAppointmentSubType-Eigenschaft
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidAppointmentSubType
api_type:
- COM
ms.assetid: e2e00af3-1fb3-4314-936a-f480674d3d83
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: cb9f4e0f58ea27d36ba911ed60527a2e53f23727
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19793427"
---
# <a name="pidlidappointmentsubtype-canonical-property"></a><span data-ttu-id="214f3-103">Kanonische PidLidAppointmentSubType-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="214f3-103">PidLidAppointmentSubType Canonical Property</span></span>

  
  
<span data-ttu-id="214f3-104">**Betrifft**: Outlook</span><span class="sxs-lookup"><span data-stu-id="214f3-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="214f3-105">Gibt an, ob das Ereignis den ganzen Tag ist.</span><span class="sxs-lookup"><span data-stu-id="214f3-105">Specifies whether or not the event is all day.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="214f3-106">Zugeordneten Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="214f3-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="214f3-107">dispidApptSubType</span><span class="sxs-lookup"><span data-stu-id="214f3-107">dispidApptSubType</span></span>  <br/> |
|<span data-ttu-id="214f3-108">-Eigenschaft festgelegt:</span><span class="sxs-lookup"><span data-stu-id="214f3-108">Property set:</span></span>  <br/> |<span data-ttu-id="214f3-109">PSETID_Appointment</span><span class="sxs-lookup"><span data-stu-id="214f3-109">PSETID_Appointment</span></span>  <br/> |
|<span data-ttu-id="214f3-110">Long-ID (Abdeckung):</span><span class="sxs-lookup"><span data-stu-id="214f3-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="214f3-111">0x00008215</span><span class="sxs-lookup"><span data-stu-id="214f3-111">0x00008215</span></span>  <br/> |
|<span data-ttu-id="214f3-112">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="214f3-112">Data type:</span></span>  <br/> |<span data-ttu-id="214f3-113">PT_BOOLEAN</span><span class="sxs-lookup"><span data-stu-id="214f3-113">PT_BOOLEAN</span></span>  <br/> |
|<span data-ttu-id="214f3-114">Bereich:</span><span class="sxs-lookup"><span data-stu-id="214f3-114">Area:</span></span>  <br/> |<span data-ttu-id="214f3-115">Kalender</span><span class="sxs-lookup"><span data-stu-id="214f3-115">Calendar</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="214f3-116">Hinweise</span><span class="sxs-lookup"><span data-stu-id="214f3-116">Remarks</span></span>

<span data-ttu-id="214f3-117">Diese Eigenschaft gibt an, ob das Ereignis ein ganztägiges Ereignis, wie vom Benutzer angegeben ist oder nicht.</span><span class="sxs-lookup"><span data-stu-id="214f3-117">This property specifies whether or not the event is an all-day event, as specified by the user.</span></span> <span data-ttu-id="214f3-118">Der Wert gibt TRUE an, dass das Ereignis als ganztägiges Ereignis in diesem Fall müssen der Start- und Endzeit Mitternacht sein ist, damit die Dauer ein Vielfaches von 24 Stunden ist und mindestens 24 Stunden ist.</span><span class="sxs-lookup"><span data-stu-id="214f3-118">A value of TRUE indicates that the event is an all-day event, in which case the start time and end time must be midnight so that the duration is a multiple of 24 hours and is at least 24 hours.</span></span> <span data-ttu-id="214f3-119">Den Wert FALSE oder Abwesenheit dieser Eigenschaft wird angegeben, dass das Ereignis nicht um ein ganztägiges Ereignis ist.</span><span class="sxs-lookup"><span data-stu-id="214f3-119">A value of FALSE or the absence of this property indicates the event is not an all-day event.</span></span> <span data-ttu-id="214f3-120">Der Client oder Server müssen Sie nicht den Wert true ableiten, wenn ein Benutzer ein Ereignis zu erstellen, ist von 24 Stunden, geschieht, auch wenn das Ereignis beginnt und um Mitternacht endet.</span><span class="sxs-lookup"><span data-stu-id="214f3-120">The client or server must not infer the value as TRUE when a user happens to create an event that is 24 hours, even if the event starts and ends at midnight.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="214f3-121">Verwandte Ressourcen</span><span class="sxs-lookup"><span data-stu-id="214f3-121">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="214f3-122">Protokollspezifikationen</span><span class="sxs-lookup"><span data-stu-id="214f3-122">Protocol specifications</span></span>

<span data-ttu-id="214f3-123">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="214f3-123">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="214f3-124">Enthält Eigenschaftendefinitionen und Verweise auf Verwandte Exchange Server-Spezifikationen.</span><span class="sxs-lookup"><span data-stu-id="214f3-124">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="214f3-125">[[MS-OXOCAL]](http://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="214f3-125">[[MS-OXOCAL]](http://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="214f3-126">Gibt die Eigenschaften und Vorgänge für den Termin, einer Besprechungsanfrage und Antwortnachrichten.</span><span class="sxs-lookup"><span data-stu-id="214f3-126">Specifies the properties and operations for appointment, meeting request, and response messages.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="214f3-127">Header-Dateien</span><span class="sxs-lookup"><span data-stu-id="214f3-127">Header files</span></span>

<span data-ttu-id="214f3-128">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="214f3-128">Mapidefs.h</span></span>
  
> <span data-ttu-id="214f3-129">Enthält die Datentypdefinitionen.</span><span class="sxs-lookup"><span data-stu-id="214f3-129">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="214f3-130">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="214f3-130">See also</span></span>



[<span data-ttu-id="214f3-131">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="214f3-131">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="214f3-132">Kanonische MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="214f3-132">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="214f3-133">Zuordnen von kanonischen Eigenschaftennamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="214f3-133">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="214f3-134">Zuordnen von MAPI-Namen zu kanonische Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="214f3-134">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

