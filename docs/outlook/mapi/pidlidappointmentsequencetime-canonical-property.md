---
title: PidLidAppointmentSequenceTime (kanonische Eigenschaft)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidAppointmentSequenceTime
api_type:
- COM
ms.assetid: 0170bb9b-f43b-4089-9144-b8652c38f43d
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: a36728fc3db2506e7c8d929842de6916b55409c8
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2018
ms.locfileid: "22588258"
---
# <a name="pidlidappointmentsequencetime-canonical-property"></a><span data-ttu-id="d1061-103">PidLidAppointmentSequenceTime (kanonische Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="d1061-103">PidLidAppointmentSequenceTime Canonical Property</span></span>

  
  
<span data-ttu-id="d1061-104">**Betrifft**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="d1061-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="d1061-105">Gibt das Datum und die Uhrzeit der letzten dieser Eigenschaft Änderung an.</span><span class="sxs-lookup"><span data-stu-id="d1061-105">Specifies the date and time at which this property was last modified.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="d1061-106">Zugeordnete Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="d1061-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="d1061-107">dispidApptSeqTime</span><span class="sxs-lookup"><span data-stu-id="d1061-107">dispidApptSeqTime</span></span>  <br/> |
|<span data-ttu-id="d1061-108">-Eigenschaft festgelegt:</span><span class="sxs-lookup"><span data-stu-id="d1061-108">Property set:</span></span>  <br/> |<span data-ttu-id="d1061-109">PSETID_Appointment</span><span class="sxs-lookup"><span data-stu-id="d1061-109">PSETID_Appointment</span></span>  <br/> |
|<span data-ttu-id="d1061-110">Long-ID (Abdeckung):</span><span class="sxs-lookup"><span data-stu-id="d1061-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="d1061-111">0x00008202</span><span class="sxs-lookup"><span data-stu-id="d1061-111">0x00008202</span></span>  <br/> |
|<span data-ttu-id="d1061-112">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="d1061-112">Data type:</span></span>  <br/> |<span data-ttu-id="d1061-113">PT_SYSTIME</span><span class="sxs-lookup"><span data-stu-id="d1061-113">PT_SYSTIME</span></span>  <br/> |
|<span data-ttu-id="d1061-114">Bereich:</span><span class="sxs-lookup"><span data-stu-id="d1061-114">Area:</span></span>  <br/> |<span data-ttu-id="d1061-115">Besprechungen</span><span class="sxs-lookup"><span data-stu-id="d1061-115">Meetings</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="d1061-116">HinwBemerkungeneise</span><span class="sxs-lookup"><span data-stu-id="d1061-116">Remarks</span></span>

<span data-ttu-id="d1061-117">Der Wert muss in koordinierter Weltzeit (UTC) angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="d1061-117">The value must be specified in Coordinated Universal Time (UTC).</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="d1061-118">Verwandte Ressourcen</span><span class="sxs-lookup"><span data-stu-id="d1061-118">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="d1061-119">Protokollspezifikationen</span><span class="sxs-lookup"><span data-stu-id="d1061-119">Protocol specifications</span></span>

<span data-ttu-id="d1061-120">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="d1061-120">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="d1061-121">Enthält Eigenschaftendefinitionen und Verweise auf Verwandte Exchange Server-Spezifikationen.</span><span class="sxs-lookup"><span data-stu-id="d1061-121">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="d1061-122">[[MS-OXOCAL]](http://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="d1061-122">[[MS-OXOCAL]](http://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="d1061-123">Gibt die Eigenschaften und Vorgänge für den Termin, einer Besprechungsanfrage und Antwortnachrichten.</span><span class="sxs-lookup"><span data-stu-id="d1061-123">Specifies the properties and operations for appointment, meeting request, and response messages.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="d1061-124">Header-Dateien</span><span class="sxs-lookup"><span data-stu-id="d1061-124">Header files</span></span>

<span data-ttu-id="d1061-125">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="d1061-125">Mapidefs.h</span></span>
  
> <span data-ttu-id="d1061-126">Enthält die Datentypdefinitionen.</span><span class="sxs-lookup"><span data-stu-id="d1061-126">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="d1061-127">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="d1061-127">See also</span></span>



[<span data-ttu-id="d1061-128">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="d1061-128">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="d1061-129">Kanonische MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="d1061-129">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="d1061-130">Zuordnen von kanonischen Eigenschaftennamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="d1061-130">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="d1061-131">Zuordnen von MAPI-Namen zu kanonische Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="d1061-131">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

