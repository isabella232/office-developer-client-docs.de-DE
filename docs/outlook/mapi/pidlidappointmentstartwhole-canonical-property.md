---
title: PidLidAppointmentStartWhole (kanonische Eigenschaft)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidAppointmentStartWhole
api_type:
- COM
ms.assetid: e5e8ed98-57af-40d0-85c4-9d9832626e6b
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 6f9fb9c3f02e66fd01e89742edcfba7391c36e3e
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32345374"
---
# <a name="pidlidappointmentstartwhole-canonical-property"></a><span data-ttu-id="04cd1-103">PidLidAppointmentStartWhole (kanonische Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="04cd1-103">PidLidAppointmentStartWhole Canonical Property</span></span>

  
  
<span data-ttu-id="04cd1-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="04cd1-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="04cd1-105">Stellt das Datum und die Uhrzeit dar, zu der ein Termin beginnt.</span><span class="sxs-lookup"><span data-stu-id="04cd1-105">Represents the date and time when an appointment begins.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="04cd1-106">Zugeordnete Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="04cd1-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="04cd1-107">dispidApptStartWhole</span><span class="sxs-lookup"><span data-stu-id="04cd1-107">dispidApptStartWhole</span></span>  <br/> |
|<span data-ttu-id="04cd1-108">Eigenschaftensatz:</span><span class="sxs-lookup"><span data-stu-id="04cd1-108">Property set:</span></span>  <br/> |<span data-ttu-id="04cd1-109">PSETID_Appointment</span><span class="sxs-lookup"><span data-stu-id="04cd1-109">PSETID_Appointment</span></span>  <br/> |
|<span data-ttu-id="04cd1-110">Lange ID (LID):</span><span class="sxs-lookup"><span data-stu-id="04cd1-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="04cd1-111">0x0000820D</span><span class="sxs-lookup"><span data-stu-id="04cd1-111">0x0000820D</span></span>  <br/> |
|<span data-ttu-id="04cd1-112">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="04cd1-112">Data type:</span></span>  <br/> |<span data-ttu-id="04cd1-113">PT_SYSTIME</span><span class="sxs-lookup"><span data-stu-id="04cd1-113">PT_SYSTIME</span></span>  <br/> |
|<span data-ttu-id="04cd1-114">Bereich:</span><span class="sxs-lookup"><span data-stu-id="04cd1-114">Area:</span></span>  <br/> |<span data-ttu-id="04cd1-115">Kalender</span><span class="sxs-lookup"><span data-stu-id="04cd1-115">Calendar</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="04cd1-116">Hinweise</span><span class="sxs-lookup"><span data-stu-id="04cd1-116">Remarks</span></span>

<span data-ttu-id="04cd1-117">Diese Eigenschaft gibt das Startdatum und die Startzeit des Ereignisses an.</span><span class="sxs-lookup"><span data-stu-id="04cd1-117">This property specifies the start date and time of the event.</span></span> <span data-ttu-id="04cd1-118">Diese Eigenschaft muss sich in koordinierter Weltzeit (Coordinated Universal Time, UTC) und kleiner als der Wert der **eigenschaft dispidApptEndWhole** ([PidLidAppointmentEndWhole](pidlidappointmentendwhole-canonical-property.md)) sein.</span><span class="sxs-lookup"><span data-stu-id="04cd1-118">This property must be in Coordinated Universal Time (UTC) and must be less than the value of the **dispidApptEndWhole** ([PidLidAppointmentEndWhole](pidlidappointmentendwhole-canonical-property.md)) property.</span></span> <span data-ttu-id="04cd1-119">Bei einer Serienserie ist diese Eigenschaft das Startdatum und die Uhrzeit der ersten Instanz gemäß dem Serienmuster.</span><span class="sxs-lookup"><span data-stu-id="04cd1-119">For a recurring series, this property is the start date and time of the first instance according to the recurrence pattern.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="04cd1-120">Verwandte Ressourcen</span><span class="sxs-lookup"><span data-stu-id="04cd1-120">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="04cd1-121">Protokollspezifikationen</span><span class="sxs-lookup"><span data-stu-id="04cd1-121">Protocol specifications</span></span>

<span data-ttu-id="04cd1-122">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="04cd1-122">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="04cd1-123">Stellt Eigenschaftensatzdefinitionen und Verweise auf verwandte Exchange Server zur Verfügung.</span><span class="sxs-lookup"><span data-stu-id="04cd1-123">Provides property set definition and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="04cd1-124">[[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="04cd1-124">[[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="04cd1-125">Gibt die Eigenschaften und Vorgänge für Termin-, Besprechungs- und Antwortnachrichten an.</span><span class="sxs-lookup"><span data-stu-id="04cd1-125">Specifies the properties and operations for appointment, meeting request, and response messages.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="04cd1-126">Headerdateien</span><span class="sxs-lookup"><span data-stu-id="04cd1-126">Header files</span></span>

<span data-ttu-id="04cd1-127">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="04cd1-127">Mapidefs.h</span></span>
  
> <span data-ttu-id="04cd1-128">Bietet Datentypdefinitionen.</span><span class="sxs-lookup"><span data-stu-id="04cd1-128">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="04cd1-129">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="04cd1-129">See also</span></span>



[<span data-ttu-id="04cd1-130">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="04cd1-130">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="04cd1-131">KANONISCHE EIGENSCHAFTEN VON MAPI</span><span class="sxs-lookup"><span data-stu-id="04cd1-131">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="04cd1-132">Zuordnen kanonischer Eigenschaftsnamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="04cd1-132">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="04cd1-133">Zuordnen von MAPI-Namen zu kanonischen Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="04cd1-133">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

