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
ms.openlocfilehash: 8ce9df6290fe6e50e52c632f0a14f226c4d715d7
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32345395"
---
# <a name="pidlidappointmentduration-canonical-property"></a><span data-ttu-id="37add-103">PidLidAppointmentDuration (kanonische Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="37add-103">PidLidAppointmentDuration Canonical Property</span></span>

  
  
<span data-ttu-id="37add-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="37add-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="37add-105">Stellt den Zeitraum (in Minuten) dar, für den ein Termin geplant wird.</span><span class="sxs-lookup"><span data-stu-id="37add-105">Represents the length of time, in minutes, when an appointment is scheduled.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="37add-106">Zugeordnete Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="37add-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="37add-107">dispidApptDuration</span><span class="sxs-lookup"><span data-stu-id="37add-107">dispidApptDuration</span></span>  <br/> |
|<span data-ttu-id="37add-108">Eigenschaftensatz:</span><span class="sxs-lookup"><span data-stu-id="37add-108">Property set:</span></span>  <br/> |<span data-ttu-id="37add-109">PSETID_Appointment</span><span class="sxs-lookup"><span data-stu-id="37add-109">PSETID_Appointment</span></span>  <br/> |
|<span data-ttu-id="37add-110">Lange ID (LID):</span><span class="sxs-lookup"><span data-stu-id="37add-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="37add-111">0x00008213</span><span class="sxs-lookup"><span data-stu-id="37add-111">0x00008213</span></span>  <br/> |
|<span data-ttu-id="37add-112">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="37add-112">Data type:</span></span>  <br/> |<span data-ttu-id="37add-113">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="37add-113">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="37add-114">Bereich:</span><span class="sxs-lookup"><span data-stu-id="37add-114">Area:</span></span>  <br/> |<span data-ttu-id="37add-115">Kalender</span><span class="sxs-lookup"><span data-stu-id="37add-115">Calendar</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="37add-116">Hinweise</span><span class="sxs-lookup"><span data-stu-id="37add-116">Remarks</span></span>

<span data-ttu-id="37add-117">Der Wert muss die Anzahl der Minuten zwischen dem Wert der **eigenschaften dispidApptStartWhole** ([PidLidAppointmentStartWhole](pidlidappointmentstartwhole-canonical-property.md)) und **dispidApptEndWhole** ([PidLidAppointmentEndWhole](pidlidappointmentendwhole-canonical-property.md)) sein.</span><span class="sxs-lookup"><span data-stu-id="37add-117">The value must be the number of minutes between the value of the **dispidApptStartWhole** ([PidLidAppointmentStartWhole](pidlidappointmentstartwhole-canonical-property.md)) and the **dispidApptEndWhole** ([PidLidAppointmentEndWhole](pidlidappointmentendwhole-canonical-property.md)) properties.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="37add-118">Verwandte Ressourcen</span><span class="sxs-lookup"><span data-stu-id="37add-118">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="37add-119">Protokollspezifikationen</span><span class="sxs-lookup"><span data-stu-id="37add-119">Protocol specifications</span></span>

<span data-ttu-id="37add-120">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="37add-120">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="37add-121">Stellt Eigenschaftensatzdefinitionen und Verweise auf verwandte Exchange Server zur Verfügung.</span><span class="sxs-lookup"><span data-stu-id="37add-121">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="37add-122">[[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="37add-122">[[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="37add-123">Gibt die Eigenschaften und Vorgänge für Termin-, Besprechungs- und Antwortnachrichten an.</span><span class="sxs-lookup"><span data-stu-id="37add-123">Specifies the properties and operations for appointment, meeting request, and response messages.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="37add-124">Headerdateien</span><span class="sxs-lookup"><span data-stu-id="37add-124">Header files</span></span>

<span data-ttu-id="37add-125">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="37add-125">Mapidefs.h</span></span>
  
> <span data-ttu-id="37add-126">Bietet Datentypdefinitionen.</span><span class="sxs-lookup"><span data-stu-id="37add-126">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="37add-127">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="37add-127">See also</span></span>



[<span data-ttu-id="37add-128">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="37add-128">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="37add-129">KANONISCHE EIGENSCHAFTEN VON MAPI</span><span class="sxs-lookup"><span data-stu-id="37add-129">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="37add-130">Zuordnen kanonischer Eigenschaftsnamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="37add-130">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="37add-131">Zuordnen von MAPI-Namen zu kanonischen Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="37add-131">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

