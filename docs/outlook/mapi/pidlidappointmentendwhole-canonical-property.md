---
title: PidLidAppointmentEndWhole (kanonische Eigenschaft)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidAppointmentEndWhole
api_type:
- COM
ms.assetid: f6fd33d6-04fb-4801-a004-fb80a14ca79d
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 21d1ee071aa5df24d0ddf641ff6f458a7de1cb3d
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2018
ms.locfileid: "22594278"
---
# <a name="pidlidappointmentendwhole-canonical-property"></a><span data-ttu-id="4a0ae-103">PidLidAppointmentEndWhole (kanonische Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="4a0ae-103">PidLidAppointmentEndWhole Canonical Property</span></span>

  
  
<span data-ttu-id="4a0ae-104">**Betrifft**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="4a0ae-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="4a0ae-105">Das Datum und die Zeit, die am Ende des Termins darstellt.</span><span class="sxs-lookup"><span data-stu-id="4a0ae-105">Represents the date and time that an appointment ends.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="4a0ae-106">Zugeordnete Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="4a0ae-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="4a0ae-107">dispidApptEndWhole</span><span class="sxs-lookup"><span data-stu-id="4a0ae-107">dispidApptEndWhole</span></span>  <br/> |
|<span data-ttu-id="4a0ae-108">-Eigenschaft festgelegt:</span><span class="sxs-lookup"><span data-stu-id="4a0ae-108">Property set:</span></span>  <br/> |<span data-ttu-id="4a0ae-109">PSETID_Appointment</span><span class="sxs-lookup"><span data-stu-id="4a0ae-109">PSETID_Appointment</span></span>  <br/> |
|<span data-ttu-id="4a0ae-110">Long-ID (Abdeckung):</span><span class="sxs-lookup"><span data-stu-id="4a0ae-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="4a0ae-111">0x0000820E</span><span class="sxs-lookup"><span data-stu-id="4a0ae-111">0x0000820E</span></span>  <br/> |
|<span data-ttu-id="4a0ae-112">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="4a0ae-112">Data type:</span></span>  <br/> |<span data-ttu-id="4a0ae-113">PT_SYSTIME</span><span class="sxs-lookup"><span data-stu-id="4a0ae-113">PT_SYSTIME</span></span>  <br/> |
|<span data-ttu-id="4a0ae-114">Bereich:</span><span class="sxs-lookup"><span data-stu-id="4a0ae-114">Area:</span></span>  <br/> |<span data-ttu-id="4a0ae-115">Kalender</span><span class="sxs-lookup"><span data-stu-id="4a0ae-115">Calendar</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="4a0ae-116">HinwBemerkungeneise</span><span class="sxs-lookup"><span data-stu-id="4a0ae-116">Remarks</span></span>

<span data-ttu-id="4a0ae-117">Diese Eigenschaft entspricht der **DispidApptEndWhole** -Eigenschaft des Termins in Microsoft Office Outlook-Objektmodell.</span><span class="sxs-lookup"><span data-stu-id="4a0ae-117">This property corresponds to the **dispidApptEndWhole** property of the appointment in the Microsoft Office Outlook object model.</span></span> 
  
<span data-ttu-id="4a0ae-118">Dies gibt an, das Enddatum und die Uhrzeit für das Ereignis. Es muss in koordinierter Weltzeit (UTC) und muss größer sein als der Wert der Eigenschaft **DispidApptStartWhole** ([PidLidAppointmentStartWhole](pidlidappointmentstartwhole-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="4a0ae-118">This specifies the end date and time for the event; it must be in Coordinated Universal Time (UTC) and must be greater than the value of the **dispidApptStartWhole** ([PidLidAppointmentStartWhole](pidlidappointmentstartwhole-canonical-property.md)) property.</span></span> <span data-ttu-id="4a0ae-119">Für eine Besprechungsserie wird die **DispidApptEndWhole** -Eigenschaft das Enddatum und die Uhrzeit der ersten Instanz entsprechend das Serienmuster.</span><span class="sxs-lookup"><span data-stu-id="4a0ae-119">For a recurring series, the **dispidApptEndWhole** property is the end date and time of the first instance according to the recurrence pattern.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="4a0ae-120">Verwandte Ressourcen</span><span class="sxs-lookup"><span data-stu-id="4a0ae-120">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="4a0ae-121">Protokollspezifikationen</span><span class="sxs-lookup"><span data-stu-id="4a0ae-121">Protocol specifications</span></span>

<span data-ttu-id="4a0ae-122">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="4a0ae-122">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="4a0ae-123">Enthält Eigenschaftendefinitionen und Verweise auf Verwandte Exchange Server-Spezifikationen.</span><span class="sxs-lookup"><span data-stu-id="4a0ae-123">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="4a0ae-124">[[MS-OXOCAL]](http://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="4a0ae-124">[[MS-OXOCAL]](http://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="4a0ae-125">Gibt die Eigenschaften und Vorgänge für den Termin, einer Besprechungsanfrage und Antwortnachrichten.</span><span class="sxs-lookup"><span data-stu-id="4a0ae-125">Specifies the properties and operations for appointment, meeting request, and response messages.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="4a0ae-126">Header-Dateien</span><span class="sxs-lookup"><span data-stu-id="4a0ae-126">Header files</span></span>

<span data-ttu-id="4a0ae-127">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="4a0ae-127">Mapidefs.h</span></span>
  
> <span data-ttu-id="4a0ae-128">Enthält die Datentypdefinitionen.</span><span class="sxs-lookup"><span data-stu-id="4a0ae-128">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="4a0ae-129">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="4a0ae-129">See also</span></span>



[<span data-ttu-id="4a0ae-130">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="4a0ae-130">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="4a0ae-131">Kanonische MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="4a0ae-131">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="4a0ae-132">Zuordnen von kanonischen Eigenschaftennamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="4a0ae-132">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="4a0ae-133">Zuordnen von MAPI-Namen zu kanonische Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="4a0ae-133">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

