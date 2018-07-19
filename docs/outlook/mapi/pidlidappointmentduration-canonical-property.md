---
title: PidLidAppointmentDuration (kanonische Eigenschaft)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidAppointmentDuration
api_type:
- COM
ms.assetid: 92c07a81-9dec-4118-af1f-02ecad340f07
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 0d124bd3aa4350863351284a9e4b19ca4533e382
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19793355"
---
# <a name="pidlidappointmentduration-canonical-property"></a><span data-ttu-id="578af-103">PidLidAppointmentDuration (kanonische Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="578af-103">PidLidAppointmentDuration Canonical Property</span></span>

  
  
<span data-ttu-id="578af-104">**Betrifft**: Outlook</span><span class="sxs-lookup"><span data-stu-id="578af-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="578af-105">Stellt die Zeitdauer in Minuten ein, wenn ein Termin geplant ist.</span><span class="sxs-lookup"><span data-stu-id="578af-105">Represents the length of time, in minutes, when an appointment is scheduled.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="578af-106">Zugeordneten Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="578af-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="578af-107">dispidApptDuration</span><span class="sxs-lookup"><span data-stu-id="578af-107">dispidApptDuration</span></span>  <br/> |
|<span data-ttu-id="578af-108">-Eigenschaft festgelegt:</span><span class="sxs-lookup"><span data-stu-id="578af-108">Property set:</span></span>  <br/> |<span data-ttu-id="578af-109">PSETID_Appointment</span><span class="sxs-lookup"><span data-stu-id="578af-109">PSETID_Appointment</span></span>  <br/> |
|<span data-ttu-id="578af-110">Long-ID (Abdeckung):</span><span class="sxs-lookup"><span data-stu-id="578af-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="578af-111">0x00008213</span><span class="sxs-lookup"><span data-stu-id="578af-111">0x00008213</span></span>  <br/> |
|<span data-ttu-id="578af-112">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="578af-112">Data type:</span></span>  <br/> |<span data-ttu-id="578af-113">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="578af-113">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="578af-114">Bereich:</span><span class="sxs-lookup"><span data-stu-id="578af-114">Area:</span></span>  <br/> |<span data-ttu-id="578af-115">Kalender</span><span class="sxs-lookup"><span data-stu-id="578af-115">Calendar</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="578af-116">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="578af-116">Remarks</span></span>

<span data-ttu-id="578af-117">Der Wert muss die Anzahl der Minuten zwischen Eigenschaften **DispidApptEndWhole** ([PidLidAppointmentEndWhole](pidlidappointmentendwhole-canonical-property.md)) und der Wert der **DispidApptStartWhole** ([PidLidAppointmentStartWhole](pidlidappointmentstartwhole-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="578af-117">The value must be the number of minutes between the value of the **dispidApptStartWhole** ([PidLidAppointmentStartWhole](pidlidappointmentstartwhole-canonical-property.md)) and the **dispidApptEndWhole** ([PidLidAppointmentEndWhole](pidlidappointmentendwhole-canonical-property.md)) properties.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="578af-118">Verwandte Ressourcen</span><span class="sxs-lookup"><span data-stu-id="578af-118">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="578af-119">Protokollspezifikationen</span><span class="sxs-lookup"><span data-stu-id="578af-119">Protocol specifications</span></span>

<span data-ttu-id="578af-120">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="578af-120">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="578af-121">Enthält Eigenschaftendefinitionen und Verweise auf Verwandte Exchange Server-Spezifikationen.</span><span class="sxs-lookup"><span data-stu-id="578af-121">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="578af-122">[[MS-OXOCAL]](http://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="578af-122">[[MS-OXOCAL]](http://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="578af-123">Gibt die Eigenschaften und Vorgänge für den Termin, einer Besprechungsanfrage und Antwortnachrichten.</span><span class="sxs-lookup"><span data-stu-id="578af-123">Specifies the properties and operations for appointment, meeting request, and response messages.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="578af-124">Header-Dateien</span><span class="sxs-lookup"><span data-stu-id="578af-124">Header files</span></span>

<span data-ttu-id="578af-125">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="578af-125">Mapidefs.h</span></span>
  
> <span data-ttu-id="578af-126">Enthält die Datentypdefinitionen.</span><span class="sxs-lookup"><span data-stu-id="578af-126">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="578af-127">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="578af-127">See also</span></span>



[<span data-ttu-id="578af-128">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="578af-128">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="578af-129">Kanonische MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="578af-129">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="578af-130">Zuordnen von kanonischen Eigenschaftennamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="578af-130">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="578af-131">Zuordnen von MAPI-Namen zu kanonische Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="578af-131">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

