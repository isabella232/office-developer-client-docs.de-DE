---
title: Kanonische Pidlidappointmentduration (-Eigenschaft
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
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: 8ce9df6290fe6e50e52c632f0a14f226c4d715d7
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32345395"
---
# <a name="pidlidappointmentduration-canonical-property"></a><span data-ttu-id="4ad54-103">Kanonische Pidlidappointmentduration (-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="4ad54-103">PidLidAppointmentDuration Canonical Property</span></span>

  
  
<span data-ttu-id="4ad54-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="4ad54-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="4ad54-105">Stellt die Zeitdauer (in Minuten) dar, in der ein Termin geplant wird.</span><span class="sxs-lookup"><span data-stu-id="4ad54-105">Represents the length of time, in minutes, when an appointment is scheduled.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="4ad54-106">Zugeordnete Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="4ad54-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="4ad54-107">dispidApptDuration</span><span class="sxs-lookup"><span data-stu-id="4ad54-107">dispidApptDuration</span></span>  <br/> |
|<span data-ttu-id="4ad54-108">Eigenschaftensatz:</span><span class="sxs-lookup"><span data-stu-id="4ad54-108">Property set:</span></span>  <br/> |<span data-ttu-id="4ad54-109">PSETID_Appointment</span><span class="sxs-lookup"><span data-stu-id="4ad54-109">PSETID_Appointment</span></span>  <br/> |
|<span data-ttu-id="4ad54-110">Long-ID (Deckel):</span><span class="sxs-lookup"><span data-stu-id="4ad54-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="4ad54-111">0x00008213</span><span class="sxs-lookup"><span data-stu-id="4ad54-111">0x00008213</span></span>  <br/> |
|<span data-ttu-id="4ad54-112">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="4ad54-112">Data type:</span></span>  <br/> |<span data-ttu-id="4ad54-113">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="4ad54-113">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="4ad54-114">Bereich:</span><span class="sxs-lookup"><span data-stu-id="4ad54-114">Area:</span></span>  <br/> |<span data-ttu-id="4ad54-115">Kalender</span><span class="sxs-lookup"><span data-stu-id="4ad54-115">Calendar</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="4ad54-116">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="4ad54-116">Remarks</span></span>

<span data-ttu-id="4ad54-117">Der Wert muss die Anzahl der Minuten zwischen dem Wert der **dispidApptStartWhole** ([pidlidappointmentstartwhole (](pidlidappointmentstartwhole-canonical-property.md)) und der **dispidApptEndWhole** ([pidlidappointmentendwhole (](pidlidappointmentendwhole-canonical-property.md))-Eigenschaft sein.</span><span class="sxs-lookup"><span data-stu-id="4ad54-117">The value must be the number of minutes between the value of the **dispidApptStartWhole** ([PidLidAppointmentStartWhole](pidlidappointmentstartwhole-canonical-property.md)) and the **dispidApptEndWhole** ([PidLidAppointmentEndWhole](pidlidappointmentendwhole-canonical-property.md)) properties.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="4ad54-118">Zugehörige Ressourcen</span><span class="sxs-lookup"><span data-stu-id="4ad54-118">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="4ad54-119">Protokollspezifikationen</span><span class="sxs-lookup"><span data-stu-id="4ad54-119">Protocol specifications</span></span>

<span data-ttu-id="4ad54-120">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="4ad54-120">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="4ad54-121">Stellt Eigenschaftensatz Definitionen und Verweise auf zugehörige Exchange Server-Protokollspezifikationen bereit.</span><span class="sxs-lookup"><span data-stu-id="4ad54-121">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="4ad54-122">[[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="4ad54-122">[[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="4ad54-123">Gibt die Eigenschaften und Vorgänge für Termin-, Besprechungs-und Antwortnachrichten an.</span><span class="sxs-lookup"><span data-stu-id="4ad54-123">Specifies the properties and operations for appointment, meeting request, and response messages.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="4ad54-124">Header Dateien</span><span class="sxs-lookup"><span data-stu-id="4ad54-124">Header files</span></span>

<span data-ttu-id="4ad54-125">Mapidefs. h</span><span class="sxs-lookup"><span data-stu-id="4ad54-125">Mapidefs.h</span></span>
  
> <span data-ttu-id="4ad54-126">Stellt Datentypdefinitionen bereit.</span><span class="sxs-lookup"><span data-stu-id="4ad54-126">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="4ad54-127">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="4ad54-127">See also</span></span>



[<span data-ttu-id="4ad54-128">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="4ad54-128">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="4ad54-129">Kanonische MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="4ad54-129">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="4ad54-130">Zuordnen von kanonischen Eigenschaftennamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="4ad54-130">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="4ad54-131">Zuordnen von MAPI-Namen zu kanonischen Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="4ad54-131">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

