---
title: PidLidClipEnd (kanonische Eigenschaft)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidClipEnd
api_type:
- COM
ms.assetid: 17c8db96-80dd-4a7a-9a1b-ab1b37ba616c
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 71a0a50f26b26d65ed34f38c2a0c7f930e6082a8
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32349182"
---
# <a name="pidlidclipend-canonical-property"></a><span data-ttu-id="b0da1-103">PidLidClipEnd (kanonische Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="b0da1-103">PidLidClipEnd Canonical Property</span></span>

  
  
<span data-ttu-id="b0da1-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="b0da1-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="b0da1-105">Gibt das Enddatum und die Uhrzeit des Ereignisses in koordinierter Weltzeit (Coordinated Universal Time, UTC) für Kalenderobjekte einzelner Instanzen an.</span><span class="sxs-lookup"><span data-stu-id="b0da1-105">Specifies the end date and time of the event in Coordinated Universal Time (UTC) for single instance calendar objects.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="b0da1-106">Zugeordnete Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="b0da1-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="b0da1-107">dispidClipEnd</span><span class="sxs-lookup"><span data-stu-id="b0da1-107">dispidClipEnd</span></span>  <br/> |
|<span data-ttu-id="b0da1-108">Eigenschaftensatz:</span><span class="sxs-lookup"><span data-stu-id="b0da1-108">Property set:</span></span>  <br/> |<span data-ttu-id="b0da1-109">PSETID_Appointment</span><span class="sxs-lookup"><span data-stu-id="b0da1-109">PSETID_Appointment</span></span>  <br/> |
|<span data-ttu-id="b0da1-110">Lange ID (LID):</span><span class="sxs-lookup"><span data-stu-id="b0da1-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="b0da1-111">0x00008236</span><span class="sxs-lookup"><span data-stu-id="b0da1-111">0x00008236</span></span>  <br/> |
|<span data-ttu-id="b0da1-112">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="b0da1-112">Data type:</span></span>  <br/> |<span data-ttu-id="b0da1-113">PT_SYSTIME</span><span class="sxs-lookup"><span data-stu-id="b0da1-113">PT_SYSTIME</span></span>  <br/> |
|<span data-ttu-id="b0da1-114">Bereich:</span><span class="sxs-lookup"><span data-stu-id="b0da1-114">Area:</span></span>  <br/> |<span data-ttu-id="b0da1-115">Kalender</span><span class="sxs-lookup"><span data-stu-id="b0da1-115">Calendar</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="b0da1-116">Hinweise</span><span class="sxs-lookup"><span data-stu-id="b0da1-116">Remarks</span></span>

<span data-ttu-id="b0da1-117">Bei Kalenderobjekten mit einer einzelnen Instanz wird das Enddatum und die Uhrzeit des Ereignisses in UTC angegeben.</span><span class="sxs-lookup"><span data-stu-id="b0da1-117">For single instance calendar objects, it specifies the end date and time of the event in UTC.</span></span> <span data-ttu-id="b0da1-118">Für eine Serienserie gibt diese Eigenschaft Mitternacht am Datum der letzten Instanz der Serienserie in UTC an, es sei denn, die Serienserie hat kein Ende, in diesem Fall muss der Wert 31. August 4500, 23:59 Uhr, sein.</span><span class="sxs-lookup"><span data-stu-id="b0da1-118">For a recurring series, this property specifies midnight on the date of the last instance of the recurring series in UTC, unless the recurring series has no end, in which case the value must be 31 August 4500, 11:59 p.m.</span></span>
  
<span data-ttu-id="b0da1-119">Der Wert dieser Eigenschaft muss auf den Wert des **dispidApptEndWhole** ([PidLidAppointmentEndWhole](pidlidappointmentendwhole-canonical-property.md)) festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="b0da1-119">The value of this property must be set to the value of the **dispidApptEndWhole** ([PidLidAppointmentEndWhole](pidlidappointmentendwhole-canonical-property.md)).</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="b0da1-120">Verwandte Ressourcen</span><span class="sxs-lookup"><span data-stu-id="b0da1-120">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="b0da1-121">Protokollspezifikationen</span><span class="sxs-lookup"><span data-stu-id="b0da1-121">Protocol specifications</span></span>

<span data-ttu-id="b0da1-122">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="b0da1-122">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="b0da1-123">Stellt Eigenschaftensatzdefinitionen und Verweise auf verwandte Exchange Server zur Verfügung.</span><span class="sxs-lookup"><span data-stu-id="b0da1-123">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="b0da1-124">[[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="b0da1-124">[[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="b0da1-125">Gibt die Eigenschaften und Vorgänge für Termin-, Besprechungs- und Antwortnachrichten an.</span><span class="sxs-lookup"><span data-stu-id="b0da1-125">Specifies the properties and operations for appointment, meeting request, and response messages.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="b0da1-126">Headerdateien</span><span class="sxs-lookup"><span data-stu-id="b0da1-126">Header files</span></span>

<span data-ttu-id="b0da1-127">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="b0da1-127">Mapidefs.h</span></span>
  
> <span data-ttu-id="b0da1-128">Bietet Datentypdefinitionen.</span><span class="sxs-lookup"><span data-stu-id="b0da1-128">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="b0da1-129">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="b0da1-129">See also</span></span>



[<span data-ttu-id="b0da1-130">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="b0da1-130">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="b0da1-131">KANONISCHE EIGENSCHAFTEN VON MAPI</span><span class="sxs-lookup"><span data-stu-id="b0da1-131">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="b0da1-132">Zuordnen kanonischer Eigenschaftsnamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="b0da1-132">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="b0da1-133">Zuordnen von MAPI-Namen zu kanonischen Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="b0da1-133">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

