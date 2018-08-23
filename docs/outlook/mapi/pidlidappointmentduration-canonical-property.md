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
ms.openlocfilehash: cfe5ad9a088fb4c02842e8be9d11a3623be749e3
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2018
ms.locfileid: "22574908"
---
# <a name="pidlidappointmentduration-canonical-property"></a><span data-ttu-id="1a1df-103">PidLidAppointmentDuration (kanonische Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="1a1df-103">PidLidAppointmentDuration Canonical Property</span></span>

  
  
<span data-ttu-id="1a1df-104">**Betrifft**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="1a1df-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="1a1df-105">Stellt die Zeitdauer in Minuten ein, wenn ein Termin geplant ist.</span><span class="sxs-lookup"><span data-stu-id="1a1df-105">Represents the length of time, in minutes, when an appointment is scheduled.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="1a1df-106">Zugeordnete Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="1a1df-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="1a1df-107">dispidApptDuration</span><span class="sxs-lookup"><span data-stu-id="1a1df-107">dispidApptDuration</span></span>  <br/> |
|<span data-ttu-id="1a1df-108">-Eigenschaft festgelegt:</span><span class="sxs-lookup"><span data-stu-id="1a1df-108">Property set:</span></span>  <br/> |<span data-ttu-id="1a1df-109">PSETID_Appointment</span><span class="sxs-lookup"><span data-stu-id="1a1df-109">PSETID_Appointment</span></span>  <br/> |
|<span data-ttu-id="1a1df-110">Long-ID (Abdeckung):</span><span class="sxs-lookup"><span data-stu-id="1a1df-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="1a1df-111">0x00008213</span><span class="sxs-lookup"><span data-stu-id="1a1df-111">0x00008213</span></span>  <br/> |
|<span data-ttu-id="1a1df-112">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="1a1df-112">Data type:</span></span>  <br/> |<span data-ttu-id="1a1df-113">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="1a1df-113">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="1a1df-114">Bereich:</span><span class="sxs-lookup"><span data-stu-id="1a1df-114">Area:</span></span>  <br/> |<span data-ttu-id="1a1df-115">Kalender</span><span class="sxs-lookup"><span data-stu-id="1a1df-115">Calendar</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="1a1df-116">HinwBemerkungeneise</span><span class="sxs-lookup"><span data-stu-id="1a1df-116">Remarks</span></span>

<span data-ttu-id="1a1df-117">Der Wert muss die Anzahl der Minuten zwischen Eigenschaften **DispidApptEndWhole** ([PidLidAppointmentEndWhole](pidlidappointmentendwhole-canonical-property.md)) und der Wert der **DispidApptStartWhole** ([PidLidAppointmentStartWhole](pidlidappointmentstartwhole-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="1a1df-117">The value must be the number of minutes between the value of the **dispidApptStartWhole** ([PidLidAppointmentStartWhole](pidlidappointmentstartwhole-canonical-property.md)) and the **dispidApptEndWhole** ([PidLidAppointmentEndWhole](pidlidappointmentendwhole-canonical-property.md)) properties.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="1a1df-118">Verwandte Ressourcen</span><span class="sxs-lookup"><span data-stu-id="1a1df-118">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="1a1df-119">Protokollspezifikationen</span><span class="sxs-lookup"><span data-stu-id="1a1df-119">Protocol specifications</span></span>

<span data-ttu-id="1a1df-120">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="1a1df-120">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="1a1df-121">Enthält Eigenschaftendefinitionen und Verweise auf Verwandte Exchange Server-Spezifikationen.</span><span class="sxs-lookup"><span data-stu-id="1a1df-121">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="1a1df-122">[[MS-OXOCAL]](http://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="1a1df-122">[[MS-OXOCAL]](http://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="1a1df-123">Gibt die Eigenschaften und Vorgänge für den Termin, einer Besprechungsanfrage und Antwortnachrichten.</span><span class="sxs-lookup"><span data-stu-id="1a1df-123">Specifies the properties and operations for appointment, meeting request, and response messages.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="1a1df-124">Header-Dateien</span><span class="sxs-lookup"><span data-stu-id="1a1df-124">Header files</span></span>

<span data-ttu-id="1a1df-125">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="1a1df-125">Mapidefs.h</span></span>
  
> <span data-ttu-id="1a1df-126">Enthält die Datentypdefinitionen.</span><span class="sxs-lookup"><span data-stu-id="1a1df-126">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="1a1df-127">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="1a1df-127">See also</span></span>



[<span data-ttu-id="1a1df-128">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="1a1df-128">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="1a1df-129">Kanonische MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="1a1df-129">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="1a1df-130">Zuordnen von kanonischen Eigenschaftennamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="1a1df-130">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="1a1df-131">Zuordnen von MAPI-Namen zu kanonische Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="1a1df-131">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

