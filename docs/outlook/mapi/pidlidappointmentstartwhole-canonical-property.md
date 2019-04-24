---
title: Kanonische Pidlidappointmentstartwhole (-Eigenschaft
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
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: 6f9fb9c3f02e66fd01e89742edcfba7391c36e3e
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32345374"
---
# <a name="pidlidappointmentstartwhole-canonical-property"></a><span data-ttu-id="f1285-103">Kanonische Pidlidappointmentstartwhole (-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="f1285-103">PidLidAppointmentStartWhole Canonical Property</span></span>

  
  
<span data-ttu-id="f1285-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="f1285-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="f1285-105">Stellt das Datum und die Uhrzeit des Beginns eines Termins dar.</span><span class="sxs-lookup"><span data-stu-id="f1285-105">Represents the date and time when an appointment begins.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="f1285-106">Zugeordnete Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="f1285-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="f1285-107">dispidApptStartWhole</span><span class="sxs-lookup"><span data-stu-id="f1285-107">dispidApptStartWhole</span></span>  <br/> |
|<span data-ttu-id="f1285-108">Eigenschaftensatz:</span><span class="sxs-lookup"><span data-stu-id="f1285-108">Property set:</span></span>  <br/> |<span data-ttu-id="f1285-109">PSETID_Appointment</span><span class="sxs-lookup"><span data-stu-id="f1285-109">PSETID_Appointment</span></span>  <br/> |
|<span data-ttu-id="f1285-110">Long-ID (Deckel):</span><span class="sxs-lookup"><span data-stu-id="f1285-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="f1285-111">0x0000820D</span><span class="sxs-lookup"><span data-stu-id="f1285-111">0x0000820D</span></span>  <br/> |
|<span data-ttu-id="f1285-112">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="f1285-112">Data type:</span></span>  <br/> |<span data-ttu-id="f1285-113">PT_SYSTIME</span><span class="sxs-lookup"><span data-stu-id="f1285-113">PT_SYSTIME</span></span>  <br/> |
|<span data-ttu-id="f1285-114">Bereich:</span><span class="sxs-lookup"><span data-stu-id="f1285-114">Area:</span></span>  <br/> |<span data-ttu-id="f1285-115">Kalender</span><span class="sxs-lookup"><span data-stu-id="f1285-115">Calendar</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="f1285-116">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="f1285-116">Remarks</span></span>

<span data-ttu-id="f1285-117">Diese Eigenschaft gibt das Startdatum und die Uhrzeit des Ereignisses an.</span><span class="sxs-lookup"><span data-stu-id="f1285-117">This property specifies the start date and time of the event.</span></span> <span data-ttu-id="f1285-118">Diese Eigenschaft muss in koordinierter weltZeit (UTC) und kleiner als der Wert der **dispidApptEndWhole** ([pidlidappointmentendwhole (](pidlidappointmentendwhole-canonical-property.md))-Eigenschaft sein.</span><span class="sxs-lookup"><span data-stu-id="f1285-118">This property must be in Coordinated Universal Time (UTC) and must be less than the value of the **dispidApptEndWhole** ([PidLidAppointmentEndWhole](pidlidappointmentendwhole-canonical-property.md)) property.</span></span> <span data-ttu-id="f1285-119">Bei einer wiederkehrenden Reihe ist diese Eigenschaft das Startdatum und die Uhrzeit der ersten Instanz entsprechend dem Serienmuster.</span><span class="sxs-lookup"><span data-stu-id="f1285-119">For a recurring series, this property is the start date and time of the first instance according to the recurrence pattern.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="f1285-120">Zugehörige Ressourcen</span><span class="sxs-lookup"><span data-stu-id="f1285-120">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="f1285-121">Protokollspezifikationen</span><span class="sxs-lookup"><span data-stu-id="f1285-121">Protocol specifications</span></span>

<span data-ttu-id="f1285-122">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="f1285-122">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="f1285-123">Stellt die Eigenschaftensatz Definition und Verweise auf zugehörige Exchange Server-Protokollspezifikationen bereit.</span><span class="sxs-lookup"><span data-stu-id="f1285-123">Provides property set definition and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="f1285-124">[[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="f1285-124">[[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="f1285-125">Gibt die Eigenschaften und Vorgänge für Termin-, Besprechungs-und Antwortnachrichten an.</span><span class="sxs-lookup"><span data-stu-id="f1285-125">Specifies the properties and operations for appointment, meeting request, and response messages.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="f1285-126">Header Dateien</span><span class="sxs-lookup"><span data-stu-id="f1285-126">Header files</span></span>

<span data-ttu-id="f1285-127">Mapidefs. h</span><span class="sxs-lookup"><span data-stu-id="f1285-127">Mapidefs.h</span></span>
  
> <span data-ttu-id="f1285-128">Stellt Datentypdefinitionen bereit.</span><span class="sxs-lookup"><span data-stu-id="f1285-128">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="f1285-129">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="f1285-129">See also</span></span>



[<span data-ttu-id="f1285-130">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="f1285-130">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="f1285-131">Kanonische MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="f1285-131">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="f1285-132">Zuordnen von kanonischen Eigenschaftennamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="f1285-132">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="f1285-133">Zuordnen von MAPI-Namen zu kanonischen Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="f1285-133">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

