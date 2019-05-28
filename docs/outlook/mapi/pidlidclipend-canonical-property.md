---
title: Kanonische pidlidclipend (-Eigenschaft
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
# <a name="pidlidclipend-canonical-property"></a><span data-ttu-id="83a60-103">Kanonische pidlidclipend (-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="83a60-103">PidLidClipEnd Canonical Property</span></span>

  
  
<span data-ttu-id="83a60-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="83a60-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="83a60-105">Gibt das Enddatum und die Uhrzeit des Ereignisses in koordinierter Weltzeit (Coordinated Universal Time, UTC) für Kalenderobjekte mit einzelnen Instanzen an.</span><span class="sxs-lookup"><span data-stu-id="83a60-105">Specifies the end date and time of the event in Coordinated Universal Time (UTC) for single instance calendar objects.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="83a60-106">Zugeordnete Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="83a60-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="83a60-107">dispidClipEnd</span><span class="sxs-lookup"><span data-stu-id="83a60-107">dispidClipEnd</span></span>  <br/> |
|<span data-ttu-id="83a60-108">Eigenschaftengruppe:</span><span class="sxs-lookup"><span data-stu-id="83a60-108">Property set:</span></span>  <br/> |<span data-ttu-id="83a60-109">PSETID_Appointment</span><span class="sxs-lookup"><span data-stu-id="83a60-109">PSETID_Appointment</span></span>  <br/> |
|<span data-ttu-id="83a60-110">Lange ID (LID):</span><span class="sxs-lookup"><span data-stu-id="83a60-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="83a60-111">0x00008236</span><span class="sxs-lookup"><span data-stu-id="83a60-111">0x00008236</span></span>  <br/> |
|<span data-ttu-id="83a60-112">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="83a60-112">Data type:</span></span>  <br/> |<span data-ttu-id="83a60-113">PT_SYSTIME</span><span class="sxs-lookup"><span data-stu-id="83a60-113">PT_SYSTIME</span></span>  <br/> |
|<span data-ttu-id="83a60-114">Bereich:</span><span class="sxs-lookup"><span data-stu-id="83a60-114">Area:</span></span>  <br/> |<span data-ttu-id="83a60-115">Kalender</span><span class="sxs-lookup"><span data-stu-id="83a60-115">Calendar</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="83a60-116">Hinweise</span><span class="sxs-lookup"><span data-stu-id="83a60-116">Remarks</span></span>

<span data-ttu-id="83a60-117">Für Kalenderobjekte mit einer Instanz gibt er das Enddatum und die Uhrzeit des Ereignisses in UTC an.</span><span class="sxs-lookup"><span data-stu-id="83a60-117">For single instance calendar objects, it specifies the end date and time of the event in UTC.</span></span> <span data-ttu-id="83a60-118">Bei einer Terminserie gibt diese Eigenschaft Mitternacht am Datum der letzten Instanz der Terminserie in UTC an, es sei denn, die wiederkehrende Reihe hat kein Ende, in diesem Fall muss der Wert 31 August 4500, 11:59 Uhr sein.</span><span class="sxs-lookup"><span data-stu-id="83a60-118">For a recurring series, this property specifies midnight on the date of the last instance of the recurring series in UTC, unless the recurring series has no end, in which case the value must be 31 August 4500, 11:59 p.m.</span></span>
  
<span data-ttu-id="83a60-119">Der Wert dieser Eigenschaft muss auf den Wert der **dispidApptEndWhole** ([pidlidappointmentendwhole (](pidlidappointmentendwhole-canonical-property.md)) festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="83a60-119">The value of this property must be set to the value of the **dispidApptEndWhole** ([PidLidAppointmentEndWhole](pidlidappointmentendwhole-canonical-property.md)).</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="83a60-120">Verwandte Ressourcen</span><span class="sxs-lookup"><span data-stu-id="83a60-120">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="83a60-121">Protokollspezifikationen</span><span class="sxs-lookup"><span data-stu-id="83a60-121">Protocol specifications</span></span>

<span data-ttu-id="83a60-122">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="83a60-122">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="83a60-123">Stellt Eigenschaftenmengen Definitionen und Verweise auf zugehörige Exchange Server Protokollspezifikationen bereit.</span><span class="sxs-lookup"><span data-stu-id="83a60-123">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="83a60-124">[[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="83a60-124">[[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="83a60-125">Gibt die Eigenschaften und Vorgänge für Termin-, Besprechungsanfrage-und Antwortnachrichten an.</span><span class="sxs-lookup"><span data-stu-id="83a60-125">Specifies the properties and operations for appointment, meeting request, and response messages.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="83a60-126">Header Dateien</span><span class="sxs-lookup"><span data-stu-id="83a60-126">Header files</span></span>

<span data-ttu-id="83a60-127">Mapidefs. h</span><span class="sxs-lookup"><span data-stu-id="83a60-127">Mapidefs.h</span></span>
  
> <span data-ttu-id="83a60-128">Stellt Definitionen von Datentypen bereit.</span><span class="sxs-lookup"><span data-stu-id="83a60-128">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="83a60-129">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="83a60-129">See also</span></span>



[<span data-ttu-id="83a60-130">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="83a60-130">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="83a60-131">Kanonische MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="83a60-131">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="83a60-132">Zuordnen von kanonischen Eigenschaftennamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="83a60-132">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="83a60-133">Zuordnen von MAPI-Namen zu kanonischen Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="83a60-133">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

