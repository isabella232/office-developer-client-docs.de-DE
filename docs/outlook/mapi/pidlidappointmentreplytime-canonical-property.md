---
title: PidLidAppointmentReplyTime (kanonische Eigenschaft)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidAppointmentReplyTime
api_type:
- COM
ms.assetid: 80a2608b-fc44-455a-86be-d6235caba99e
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 755342da4bc280241e313fbb7efb818ab29b829f
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2018
ms.locfileid: "22571626"
---
# <a name="pidlidappointmentreplytime-canonical-property"></a><span data-ttu-id="ba53b-103">PidLidAppointmentReplyTime (kanonische Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="ba53b-103">PidLidAppointmentReplyTime Canonical Property</span></span>

  
  
<span data-ttu-id="ba53b-104">**Betrifft**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="ba53b-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="ba53b-105">Gibt das Datum und Uhrzeit, als der Teilnehmer zu einer empfangenen einer Besprechungsanfrage oder Update meeting geantwortet hat.</span><span class="sxs-lookup"><span data-stu-id="ba53b-105">Specifies the date and time when the attendee responded to a received meeting request or meeting update.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="ba53b-106">Zugeordnete Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="ba53b-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="ba53b-107">dispidApptReplyTime</span><span class="sxs-lookup"><span data-stu-id="ba53b-107">dispidApptReplyTime</span></span>  <br/> |
|<span data-ttu-id="ba53b-108">-Eigenschaft festgelegt:</span><span class="sxs-lookup"><span data-stu-id="ba53b-108">Property set:</span></span>  <br/> |<span data-ttu-id="ba53b-109">PSETID_Appointment</span><span class="sxs-lookup"><span data-stu-id="ba53b-109">PSETID_Appointment</span></span>  <br/> |
|<span data-ttu-id="ba53b-110">Long-ID (Abdeckung):</span><span class="sxs-lookup"><span data-stu-id="ba53b-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="ba53b-111">0x00008220</span><span class="sxs-lookup"><span data-stu-id="ba53b-111">0x00008220</span></span>  <br/> |
|<span data-ttu-id="ba53b-112">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="ba53b-112">Data type:</span></span>  <br/> |<span data-ttu-id="ba53b-113">PT_SYSTIME</span><span class="sxs-lookup"><span data-stu-id="ba53b-113">PT_SYSTIME</span></span>  <br/> |
|<span data-ttu-id="ba53b-114">Bereich:</span><span class="sxs-lookup"><span data-stu-id="ba53b-114">Area:</span></span>  <br/> |<span data-ttu-id="ba53b-115">Besprechungen</span><span class="sxs-lookup"><span data-stu-id="ba53b-115">Meetings</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="ba53b-116">HinwBemerkungeneise</span><span class="sxs-lookup"><span data-stu-id="ba53b-116">Remarks</span></span>

<span data-ttu-id="ba53b-117">Der Wert muss in koordinierter Weltzeit (UTC) angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="ba53b-117">The value must be specified in Coordinated Universal Time (UTC).</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="ba53b-118">Verwandte Ressourcen</span><span class="sxs-lookup"><span data-stu-id="ba53b-118">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="ba53b-119">Protokollspezifikationen</span><span class="sxs-lookup"><span data-stu-id="ba53b-119">Protocol specifications</span></span>

<span data-ttu-id="ba53b-120">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="ba53b-120">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="ba53b-121">Enthält Eigenschaftendefinitionen und Verweise auf Verwandte Exchange Server-Spezifikationen.</span><span class="sxs-lookup"><span data-stu-id="ba53b-121">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="ba53b-122">[[MS-OXOCAL]](http://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="ba53b-122">[[MS-OXOCAL]](http://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="ba53b-123">Gibt die Eigenschaften und Vorgänge für den Termin, einer Besprechungsanfrage und Antwortnachrichten.</span><span class="sxs-lookup"><span data-stu-id="ba53b-123">Specifies the properties and operations for appointment, meeting request, and response messages.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="ba53b-124">Header-Dateien</span><span class="sxs-lookup"><span data-stu-id="ba53b-124">Header files</span></span>

<span data-ttu-id="ba53b-125">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="ba53b-125">Mapidefs.h</span></span>
  
> <span data-ttu-id="ba53b-126">Enthält die Datentypdefinitionen.</span><span class="sxs-lookup"><span data-stu-id="ba53b-126">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="ba53b-127">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="ba53b-127">See also</span></span>



[<span data-ttu-id="ba53b-128">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="ba53b-128">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="ba53b-129">Kanonische MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="ba53b-129">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="ba53b-130">Zuordnen von kanonischen Eigenschaftennamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="ba53b-130">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="ba53b-131">Zuordnen von MAPI-Namen zu kanonische Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="ba53b-131">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

