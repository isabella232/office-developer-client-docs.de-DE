---
title: Kanonische pidlidappointmentsubtype (-Eigenschaft
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
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 921d7d8defbdae66bc48072d757f4f58b7d656f0
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32345416"
---
# <a name="pidlidappointmentsubtype-canonical-property"></a><span data-ttu-id="8a4c4-103">Kanonische pidlidappointmentsubtype (-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="8a4c4-103">PidLidAppointmentSubType Canonical Property</span></span>

  
  
<span data-ttu-id="8a4c4-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="8a4c4-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="8a4c4-105">Gibt an, ob das Ereignis den ganzen Tag ist.</span><span class="sxs-lookup"><span data-stu-id="8a4c4-105">Specifies whether or not the event is all day.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="8a4c4-106">Zugeordnete Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="8a4c4-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="8a4c4-107">dispidApptSubType</span><span class="sxs-lookup"><span data-stu-id="8a4c4-107">dispidApptSubType</span></span>  <br/> |
|<span data-ttu-id="8a4c4-108">Eigenschaftengruppe:</span><span class="sxs-lookup"><span data-stu-id="8a4c4-108">Property set:</span></span>  <br/> |<span data-ttu-id="8a4c4-109">PSETID_Appointment</span><span class="sxs-lookup"><span data-stu-id="8a4c4-109">PSETID_Appointment</span></span>  <br/> |
|<span data-ttu-id="8a4c4-110">Lange ID (LID):</span><span class="sxs-lookup"><span data-stu-id="8a4c4-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="8a4c4-111">0x00008215</span><span class="sxs-lookup"><span data-stu-id="8a4c4-111">0x00008215</span></span>  <br/> |
|<span data-ttu-id="8a4c4-112">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="8a4c4-112">Data type:</span></span>  <br/> |<span data-ttu-id="8a4c4-113">PT_BOOLEAN</span><span class="sxs-lookup"><span data-stu-id="8a4c4-113">PT_BOOLEAN</span></span>  <br/> |
|<span data-ttu-id="8a4c4-114">Bereich:</span><span class="sxs-lookup"><span data-stu-id="8a4c4-114">Area:</span></span>  <br/> |<span data-ttu-id="8a4c4-115">Kalender</span><span class="sxs-lookup"><span data-stu-id="8a4c4-115">Calendar</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="8a4c4-116">Hinweise</span><span class="sxs-lookup"><span data-stu-id="8a4c4-116">Remarks</span></span>

<span data-ttu-id="8a4c4-117">Diese Eigenschaft gibt an, ob das Ereignis ein ganztägiges Ereignis ist, wie vom Benutzer angegeben.</span><span class="sxs-lookup"><span data-stu-id="8a4c4-117">This property specifies whether or not the event is an all-day event, as specified by the user.</span></span> <span data-ttu-id="8a4c4-118">Der Wert true gibt an, dass das Ereignis ein ganztägiges Ereignis ist, in diesem Fall müssen die Startzeit und die Endzeit Mitternacht sein, damit die Dauer ein Vielfaches von 24 Stunden und mindestens 24 Stunden ist.</span><span class="sxs-lookup"><span data-stu-id="8a4c4-118">A value of TRUE indicates that the event is an all-day event, in which case the start time and end time must be midnight so that the duration is a multiple of 24 hours and is at least 24 hours.</span></span> <span data-ttu-id="8a4c4-119">Der Wert false oder das Fehlen dieser Eigenschaft gibt an, dass das Ereignis kein ganztägiges Ereignis ist.</span><span class="sxs-lookup"><span data-stu-id="8a4c4-119">A value of FALSE or the absence of this property indicates the event is not an all-day event.</span></span> <span data-ttu-id="8a4c4-120">Der Client oder Server darf den Wert nicht als true ableiten, wenn ein Benutzer ein Ereignis erstellt, das 24 Stunden dauert, selbst wenn das Ereignis beginnt und um Mitternacht endet.</span><span class="sxs-lookup"><span data-stu-id="8a4c4-120">The client or server must not infer the value as TRUE when a user happens to create an event that is 24 hours, even if the event starts and ends at midnight.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="8a4c4-121">Verwandte Ressourcen</span><span class="sxs-lookup"><span data-stu-id="8a4c4-121">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="8a4c4-122">Protokollspezifikationen</span><span class="sxs-lookup"><span data-stu-id="8a4c4-122">Protocol specifications</span></span>

<span data-ttu-id="8a4c4-123">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="8a4c4-123">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="8a4c4-124">Stellt Eigenschaftenmengen Definitionen und Verweise auf zugehörige Exchange Server Protokollspezifikationen bereit.</span><span class="sxs-lookup"><span data-stu-id="8a4c4-124">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="8a4c4-125">[[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="8a4c4-125">[[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="8a4c4-126">Gibt die Eigenschaften und Vorgänge für Termin-, Besprechungsanfrage-und Antwortnachrichten an.</span><span class="sxs-lookup"><span data-stu-id="8a4c4-126">Specifies the properties and operations for appointment, meeting request, and response messages.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="8a4c4-127">Header Dateien</span><span class="sxs-lookup"><span data-stu-id="8a4c4-127">Header files</span></span>

<span data-ttu-id="8a4c4-128">Mapidefs. h</span><span class="sxs-lookup"><span data-stu-id="8a4c4-128">Mapidefs.h</span></span>
  
> <span data-ttu-id="8a4c4-129">Stellt Definitionen von Datentypen bereit.</span><span class="sxs-lookup"><span data-stu-id="8a4c4-129">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="8a4c4-130">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="8a4c4-130">See also</span></span>



[<span data-ttu-id="8a4c4-131">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="8a4c4-131">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="8a4c4-132">Kanonische MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="8a4c4-132">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="8a4c4-133">Zuordnen von kanonischen Eigenschaftennamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="8a4c4-133">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="8a4c4-134">Zuordnen von MAPI-Namen zu kanonischen Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="8a4c4-134">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

