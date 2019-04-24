---
title: Kanonische Pidlidappointmentsubtype (-Eigenschaft
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
ms.openlocfilehash: 921d7d8defbdae66bc48072d757f4f58b7d656f0
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32345416"
---
# <a name="pidlidappointmentsubtype-canonical-property"></a><span data-ttu-id="310df-103">Kanonische Pidlidappointmentsubtype (-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="310df-103">PidLidAppointmentSubType Canonical Property</span></span>

  
  
<span data-ttu-id="310df-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="310df-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="310df-105">Gibt an, ob das Ereignis ganztägig ist.</span><span class="sxs-lookup"><span data-stu-id="310df-105">Specifies whether or not the event is all day.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="310df-106">Zugeordnete Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="310df-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="310df-107">dispidApptSubType</span><span class="sxs-lookup"><span data-stu-id="310df-107">dispidApptSubType</span></span>  <br/> |
|<span data-ttu-id="310df-108">Eigenschaftensatz:</span><span class="sxs-lookup"><span data-stu-id="310df-108">Property set:</span></span>  <br/> |<span data-ttu-id="310df-109">PSETID_Appointment</span><span class="sxs-lookup"><span data-stu-id="310df-109">PSETID_Appointment</span></span>  <br/> |
|<span data-ttu-id="310df-110">Long-ID (Deckel):</span><span class="sxs-lookup"><span data-stu-id="310df-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="310df-111">0x00008215</span><span class="sxs-lookup"><span data-stu-id="310df-111">0x00008215</span></span>  <br/> |
|<span data-ttu-id="310df-112">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="310df-112">Data type:</span></span>  <br/> |<span data-ttu-id="310df-113">PT_BOOLEAN</span><span class="sxs-lookup"><span data-stu-id="310df-113">PT_BOOLEAN</span></span>  <br/> |
|<span data-ttu-id="310df-114">Bereich:</span><span class="sxs-lookup"><span data-stu-id="310df-114">Area:</span></span>  <br/> |<span data-ttu-id="310df-115">Kalender</span><span class="sxs-lookup"><span data-stu-id="310df-115">Calendar</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="310df-116">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="310df-116">Remarks</span></span>

<span data-ttu-id="310df-117">Diese Eigenschaft gibt an, ob das Ereignis ein ganztägiges Ereignis ist, wie vom Benutzer angegeben.</span><span class="sxs-lookup"><span data-stu-id="310df-117">This property specifies whether or not the event is an all-day event, as specified by the user.</span></span> <span data-ttu-id="310df-118">Der Wert TRUE gibt an, dass das Ereignis ein ganztägiges Ereignis ist, in dem die Startzeit und die Endzeit Mitternacht sein müssen, damit die Dauer ein Vielfaches von 24 Stunden ist und mindestens 24 Stunden beträgt.</span><span class="sxs-lookup"><span data-stu-id="310df-118">A value of TRUE indicates that the event is an all-day event, in which case the start time and end time must be midnight so that the duration is a multiple of 24 hours and is at least 24 hours.</span></span> <span data-ttu-id="310df-119">Der Wert FALSE oder das Fehlen dieser Eigenschaft gibt an, dass das Ereignis kein ganztägiges Ereignis ist.</span><span class="sxs-lookup"><span data-stu-id="310df-119">A value of FALSE or the absence of this property indicates the event is not an all-day event.</span></span> <span data-ttu-id="310df-120">Der Client oder Server darf den Wert nicht als TRUE ableiten, wenn ein Benutzer ein Ereignis erstellt, das 24 Stunden dauert, auch wenn das Ereignis um Mitternacht beginnt und endet.</span><span class="sxs-lookup"><span data-stu-id="310df-120">The client or server must not infer the value as TRUE when a user happens to create an event that is 24 hours, even if the event starts and ends at midnight.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="310df-121">Zugehörige Ressourcen</span><span class="sxs-lookup"><span data-stu-id="310df-121">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="310df-122">Protokollspezifikationen</span><span class="sxs-lookup"><span data-stu-id="310df-122">Protocol specifications</span></span>

<span data-ttu-id="310df-123">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="310df-123">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="310df-124">Stellt Eigenschaftensatz Definitionen und Verweise auf zugehörige Exchange Server-Protokollspezifikationen bereit.</span><span class="sxs-lookup"><span data-stu-id="310df-124">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="310df-125">[[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="310df-125">[[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="310df-126">Gibt die Eigenschaften und Vorgänge für Termin-, Besprechungs-und Antwortnachrichten an.</span><span class="sxs-lookup"><span data-stu-id="310df-126">Specifies the properties and operations for appointment, meeting request, and response messages.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="310df-127">Header Dateien</span><span class="sxs-lookup"><span data-stu-id="310df-127">Header files</span></span>

<span data-ttu-id="310df-128">Mapidefs. h</span><span class="sxs-lookup"><span data-stu-id="310df-128">Mapidefs.h</span></span>
  
> <span data-ttu-id="310df-129">Stellt Datentypdefinitionen bereit.</span><span class="sxs-lookup"><span data-stu-id="310df-129">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="310df-130">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="310df-130">See also</span></span>



[<span data-ttu-id="310df-131">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="310df-131">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="310df-132">Kanonische MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="310df-132">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="310df-133">Zuordnen von kanonischen Eigenschaftennamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="310df-133">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="310df-134">Zuordnen von MAPI-Namen zu kanonischen Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="310df-134">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

