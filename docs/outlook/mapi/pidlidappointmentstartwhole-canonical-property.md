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
ms.openlocfilehash: 05cd1428966f6c61e2f5e13e574a0bbcb253f7ea
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2018
ms.locfileid: "22582602"
---
# <a name="pidlidappointmentstartwhole-canonical-property"></a><span data-ttu-id="79f18-103">PidLidAppointmentStartWhole (kanonische Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="79f18-103">PidLidAppointmentStartWhole Canonical Property</span></span>

  
  
<span data-ttu-id="79f18-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="79f18-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="79f18-105">Stellt das Datum und die Uhrzeit ein Termins beginnt.</span><span class="sxs-lookup"><span data-stu-id="79f18-105">Represents the date and time when an appointment begins.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="79f18-106">Zugeordnete Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="79f18-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="79f18-107">dispidApptStartWhole</span><span class="sxs-lookup"><span data-stu-id="79f18-107">dispidApptStartWhole</span></span>  <br/> |
|<span data-ttu-id="79f18-108">-Eigenschaft festgelegt:</span><span class="sxs-lookup"><span data-stu-id="79f18-108">Property set:</span></span>  <br/> |<span data-ttu-id="79f18-109">PSETID_Appointment</span><span class="sxs-lookup"><span data-stu-id="79f18-109">PSETID_Appointment</span></span>  <br/> |
|<span data-ttu-id="79f18-110">Long-ID (Abdeckung):</span><span class="sxs-lookup"><span data-stu-id="79f18-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="79f18-111">0x0000820D</span><span class="sxs-lookup"><span data-stu-id="79f18-111">0x0000820D</span></span>  <br/> |
|<span data-ttu-id="79f18-112">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="79f18-112">Data type:</span></span>  <br/> |<span data-ttu-id="79f18-113">PT_SYSTIME</span><span class="sxs-lookup"><span data-stu-id="79f18-113">PT_SYSTIME</span></span>  <br/> |
|<span data-ttu-id="79f18-114">Bereich:</span><span class="sxs-lookup"><span data-stu-id="79f18-114">Area:</span></span>  <br/> |<span data-ttu-id="79f18-115">Kalender</span><span class="sxs-lookup"><span data-stu-id="79f18-115">Calendar</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="79f18-116">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="79f18-116">Remarks</span></span>

<span data-ttu-id="79f18-117">Diese Eigenschaft gibt das Startdatum und die Uhrzeit des Ereignisses.</span><span class="sxs-lookup"><span data-stu-id="79f18-117">This property specifies the start date and time of the event.</span></span> <span data-ttu-id="79f18-118">Diese Eigenschaft muss in koordinierter Weltzeit (UTC) und muss kleiner als der Wert der Eigenschaft **DispidApptEndWhole** ([PidLidAppointmentEndWhole](pidlidappointmentendwhole-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="79f18-118">This property must be in Coordinated Universal Time (UTC) and must be less than the value of the **dispidApptEndWhole** ([PidLidAppointmentEndWhole](pidlidappointmentendwhole-canonical-property.md)) property.</span></span> <span data-ttu-id="79f18-119">Für eine Besprechungsserie wird diese Eigenschaft das Startdatum und die Uhrzeit der ersten Instanz entsprechend das Serienmuster.</span><span class="sxs-lookup"><span data-stu-id="79f18-119">For a recurring series, this property is the start date and time of the first instance according to the recurrence pattern.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="79f18-120">Verwandte Ressourcen</span><span class="sxs-lookup"><span data-stu-id="79f18-120">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="79f18-121">Protokollspezifikationen</span><span class="sxs-lookup"><span data-stu-id="79f18-121">Protocol specifications</span></span>

<span data-ttu-id="79f18-122">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="79f18-122">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="79f18-123">Enthält Set Eigenschaftendefinition und Verweise auf Verwandte Exchange Server-Spezifikationen.</span><span class="sxs-lookup"><span data-stu-id="79f18-123">Provides property set definition and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="79f18-124">[[MS-OXOCAL]](http://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="79f18-124">[[MS-OXOCAL]](http://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="79f18-125">Gibt die Eigenschaften und Vorgänge für den Termin, einer Besprechungsanfrage und Antwortnachrichten.</span><span class="sxs-lookup"><span data-stu-id="79f18-125">Specifies the properties and operations for appointment, meeting request, and response messages.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="79f18-126">Header-Dateien</span><span class="sxs-lookup"><span data-stu-id="79f18-126">Header files</span></span>

<span data-ttu-id="79f18-127">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="79f18-127">Mapidefs.h</span></span>
  
> <span data-ttu-id="79f18-128">Enthält die Datentypdefinitionen.</span><span class="sxs-lookup"><span data-stu-id="79f18-128">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="79f18-129">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="79f18-129">See also</span></span>



[<span data-ttu-id="79f18-130">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="79f18-130">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="79f18-131">Kanonische MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="79f18-131">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="79f18-132">Zuordnen von kanonischen Eigenschaftennamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="79f18-132">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="79f18-133">Zuordnen von MAPI-Namen zu kanonische Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="79f18-133">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

