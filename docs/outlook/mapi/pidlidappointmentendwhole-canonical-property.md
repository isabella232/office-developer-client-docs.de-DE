---
title: Kanonische pidlidappointmentendwhole (-Eigenschaft
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
ms.openlocfilehash: eaff90de919c1bdc04983bce32a2aa808ae56013
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32358898"
---
# <a name="pidlidappointmentendwhole-canonical-property"></a><span data-ttu-id="a5a56-103">Kanonische pidlidappointmentendwhole (-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="a5a56-103">PidLidAppointmentEndWhole Canonical Property</span></span>

  
  
<span data-ttu-id="a5a56-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="a5a56-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="a5a56-105">Stellt das Datum und die Uhrzeit der Beendigung eines Termins dar.</span><span class="sxs-lookup"><span data-stu-id="a5a56-105">Represents the date and time that an appointment ends.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="a5a56-106">Zugeordnete Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="a5a56-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="a5a56-107">dispidApptEndWhole</span><span class="sxs-lookup"><span data-stu-id="a5a56-107">dispidApptEndWhole</span></span>  <br/> |
|<span data-ttu-id="a5a56-108">Eigenschaftengruppe:</span><span class="sxs-lookup"><span data-stu-id="a5a56-108">Property set:</span></span>  <br/> |<span data-ttu-id="a5a56-109">PSETID_Appointment</span><span class="sxs-lookup"><span data-stu-id="a5a56-109">PSETID_Appointment</span></span>  <br/> |
|<span data-ttu-id="a5a56-110">Lange ID (LID):</span><span class="sxs-lookup"><span data-stu-id="a5a56-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="a5a56-111">0x0000820E</span><span class="sxs-lookup"><span data-stu-id="a5a56-111">0x0000820E</span></span>  <br/> |
|<span data-ttu-id="a5a56-112">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="a5a56-112">Data type:</span></span>  <br/> |<span data-ttu-id="a5a56-113">PT_SYSTIME</span><span class="sxs-lookup"><span data-stu-id="a5a56-113">PT_SYSTIME</span></span>  <br/> |
|<span data-ttu-id="a5a56-114">Bereich:</span><span class="sxs-lookup"><span data-stu-id="a5a56-114">Area:</span></span>  <br/> |<span data-ttu-id="a5a56-115">Kalender</span><span class="sxs-lookup"><span data-stu-id="a5a56-115">Calendar</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="a5a56-116">Hinweise</span><span class="sxs-lookup"><span data-stu-id="a5a56-116">Remarks</span></span>

<span data-ttu-id="a5a56-117">Diese Eigenschaft entspricht der **dispidApptEndWhole** -Eigenschaft des Termins im Microsoft Office Outlook-Objektmodell.</span><span class="sxs-lookup"><span data-stu-id="a5a56-117">This property corresponds to the **dispidApptEndWhole** property of the appointment in the Microsoft Office Outlook object model.</span></span> 
  
<span data-ttu-id="a5a56-118">Dies gibt das Enddatum und die Endzeit für das Ereignis an; Er muss sich in UTC (Coordinated Universal Time) und größer als der Wert der **dispidApptStartWhole** ([pidlidappointmentstartwhole (](pidlidappointmentstartwhole-canonical-property.md))-Eigenschaft befinden.</span><span class="sxs-lookup"><span data-stu-id="a5a56-118">This specifies the end date and time for the event; it must be in Coordinated Universal Time (UTC) and must be greater than the value of the **dispidApptStartWhole** ([PidLidAppointmentStartWhole](pidlidappointmentstartwhole-canonical-property.md)) property.</span></span> <span data-ttu-id="a5a56-119">Bei einer Terminserie ist die **dispidApptEndWhole** -Eigenschaft das Enddatum und die Uhrzeit der ersten Instanz entsprechend dem Serienmuster.</span><span class="sxs-lookup"><span data-stu-id="a5a56-119">For a recurring series, the **dispidApptEndWhole** property is the end date and time of the first instance according to the recurrence pattern.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="a5a56-120">Verwandte Ressourcen</span><span class="sxs-lookup"><span data-stu-id="a5a56-120">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="a5a56-121">Protokollspezifikationen</span><span class="sxs-lookup"><span data-stu-id="a5a56-121">Protocol specifications</span></span>

<span data-ttu-id="a5a56-122">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="a5a56-122">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="a5a56-123">Stellt Eigenschaftenmengen Definitionen und Verweise auf zugehörige Exchange Server Protokollspezifikationen bereit.</span><span class="sxs-lookup"><span data-stu-id="a5a56-123">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="a5a56-124">[[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="a5a56-124">[[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="a5a56-125">Gibt die Eigenschaften und Vorgänge für Termin-, Besprechungsanfrage-und Antwortnachrichten an.</span><span class="sxs-lookup"><span data-stu-id="a5a56-125">Specifies the properties and operations for appointment, meeting request, and response messages.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="a5a56-126">Header Dateien</span><span class="sxs-lookup"><span data-stu-id="a5a56-126">Header files</span></span>

<span data-ttu-id="a5a56-127">Mapidefs. h</span><span class="sxs-lookup"><span data-stu-id="a5a56-127">Mapidefs.h</span></span>
  
> <span data-ttu-id="a5a56-128">Stellt Definitionen von Datentypen bereit.</span><span class="sxs-lookup"><span data-stu-id="a5a56-128">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="a5a56-129">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="a5a56-129">See also</span></span>



[<span data-ttu-id="a5a56-130">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="a5a56-130">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="a5a56-131">Kanonische MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="a5a56-131">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="a5a56-132">Zuordnen von kanonischen Eigenschaftennamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="a5a56-132">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="a5a56-133">Zuordnen von MAPI-Namen zu kanonischen Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="a5a56-133">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

