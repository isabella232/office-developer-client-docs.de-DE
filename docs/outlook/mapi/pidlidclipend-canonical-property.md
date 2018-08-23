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
ms.openlocfilehash: b1b18db072cb7c62c10c8ee4ab79dd1d8754388f
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2018
ms.locfileid: "22588020"
---
# <a name="pidlidclipend-canonical-property"></a><span data-ttu-id="c25d8-103">PidLidClipEnd (kanonische Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="c25d8-103">PidLidClipEnd Canonical Property</span></span>

  
  
<span data-ttu-id="c25d8-104">**Betrifft**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="c25d8-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="c25d8-105">Gibt das Enddatum und die Uhrzeit des Ereignisses in koordinierter Weltzeit (UTC) für Einzelinstanz Calendar-Objekten.</span><span class="sxs-lookup"><span data-stu-id="c25d8-105">Specifies the end date and time of the event in Coordinated Universal Time (UTC) for single instance calendar objects.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="c25d8-106">Zugeordnete Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="c25d8-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="c25d8-107">dispidClipEnd</span><span class="sxs-lookup"><span data-stu-id="c25d8-107">dispidClipEnd</span></span>  <br/> |
|<span data-ttu-id="c25d8-108">-Eigenschaft festgelegt:</span><span class="sxs-lookup"><span data-stu-id="c25d8-108">Property set:</span></span>  <br/> |<span data-ttu-id="c25d8-109">PSETID_Appointment</span><span class="sxs-lookup"><span data-stu-id="c25d8-109">PSETID_Appointment</span></span>  <br/> |
|<span data-ttu-id="c25d8-110">Long-ID (Abdeckung):</span><span class="sxs-lookup"><span data-stu-id="c25d8-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="c25d8-111">0x00008236</span><span class="sxs-lookup"><span data-stu-id="c25d8-111">0x00008236</span></span>  <br/> |
|<span data-ttu-id="c25d8-112">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="c25d8-112">Data type:</span></span>  <br/> |<span data-ttu-id="c25d8-113">PT_SYSTIME</span><span class="sxs-lookup"><span data-stu-id="c25d8-113">PT_SYSTIME</span></span>  <br/> |
|<span data-ttu-id="c25d8-114">Bereich:</span><span class="sxs-lookup"><span data-stu-id="c25d8-114">Area:</span></span>  <br/> |<span data-ttu-id="c25d8-115">Kalender</span><span class="sxs-lookup"><span data-stu-id="c25d8-115">Calendar</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="c25d8-116">HinwBemerkungeneise</span><span class="sxs-lookup"><span data-stu-id="c25d8-116">Remarks</span></span>

<span data-ttu-id="c25d8-117">Für einzelne Instanz Calendar-Objekten gibt es das Enddatum und die Uhrzeit des Ereignisses in UTC.</span><span class="sxs-lookup"><span data-stu-id="c25d8-117">For single instance calendar objects, it specifies the end date and time of the event in UTC.</span></span> <span data-ttu-id="c25d8-118">Für eine Besprechungsserie diese Eigenschaft gibt Mitternacht auf das Datum der letzten Instanz von der Terminserie in UTC, es sei denn, der sich wiederholenden Reihe kein Ende der Wert in dem 31. August muss 4500, 23:59 Uhr</span><span class="sxs-lookup"><span data-stu-id="c25d8-118">For a recurring series, this property specifies midnight on the date of the last instance of the recurring series in UTC, unless the recurring series has no end, in which case the value must be 31 August 4500, 11:59 p.m.</span></span>
  
<span data-ttu-id="c25d8-119">Der Wert dieser Eigenschaft muss auf den Wert der **DispidApptEndWhole** ([PidLidAppointmentEndWhole](pidlidappointmentendwhole-canonical-property.md)) festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="c25d8-119">The value of this property must be set to the value of the **dispidApptEndWhole** ([PidLidAppointmentEndWhole](pidlidappointmentendwhole-canonical-property.md)).</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="c25d8-120">Verwandte Ressourcen</span><span class="sxs-lookup"><span data-stu-id="c25d8-120">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="c25d8-121">Protokollspezifikationen</span><span class="sxs-lookup"><span data-stu-id="c25d8-121">Protocol specifications</span></span>

<span data-ttu-id="c25d8-122">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="c25d8-122">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="c25d8-123">Enthält Eigenschaftendefinitionen und Verweise auf Verwandte Exchange Server-Spezifikationen.</span><span class="sxs-lookup"><span data-stu-id="c25d8-123">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="c25d8-124">[[MS-OXOCAL]](http://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="c25d8-124">[[MS-OXOCAL]](http://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="c25d8-125">Gibt die Eigenschaften und Vorgänge für den Termin, einer Besprechungsanfrage und Antwortnachrichten.</span><span class="sxs-lookup"><span data-stu-id="c25d8-125">Specifies the properties and operations for appointment, meeting request, and response messages.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="c25d8-126">Header-Dateien</span><span class="sxs-lookup"><span data-stu-id="c25d8-126">Header files</span></span>

<span data-ttu-id="c25d8-127">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="c25d8-127">Mapidefs.h</span></span>
  
> <span data-ttu-id="c25d8-128">Enthält die Datentypdefinitionen.</span><span class="sxs-lookup"><span data-stu-id="c25d8-128">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="c25d8-129">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="c25d8-129">See also</span></span>



[<span data-ttu-id="c25d8-130">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="c25d8-130">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="c25d8-131">Kanonische MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="c25d8-131">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="c25d8-132">Zuordnen von kanonischen Eigenschaftennamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="c25d8-132">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="c25d8-133">Zuordnen von MAPI-Namen zu kanonische Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="c25d8-133">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

