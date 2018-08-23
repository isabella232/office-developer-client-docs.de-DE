---
title: PidLidTimeZone (kanonische Eigenschaft)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidTimeZone
api_type:
- COM
ms.assetid: ffbab371-1a1d-4aa4-ad31-17549a74513c
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 90dc35e72fc863ab12d9d6df9c54def7af788efd
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2018
ms.locfileid: "22568889"
---
# <a name="pidlidtimezone-canonical-property"></a><span data-ttu-id="3c757-103">PidLidTimeZone (kanonische Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="3c757-103">PidLidTimeZone Canonical Property</span></span>

  
  
<span data-ttu-id="3c757-104">**Betrifft**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="3c757-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="3c757-105">Gibt Informationen über die Zeitzone einer Besprechungsserie.</span><span class="sxs-lookup"><span data-stu-id="3c757-105">Specifies information about the time zone of a recurring meeting.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="3c757-106">Zugeordnete Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="3c757-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="3c757-107">LID_TIME_ZONE</span><span class="sxs-lookup"><span data-stu-id="3c757-107">LID_TIME_ZONE</span></span>  <br/> |
|<span data-ttu-id="3c757-108">-Eigenschaft festgelegt:</span><span class="sxs-lookup"><span data-stu-id="3c757-108">Property set:</span></span>  <br/> |<span data-ttu-id="3c757-109">PSETID_Meeting</span><span class="sxs-lookup"><span data-stu-id="3c757-109">PSETID_Meeting</span></span>  <br/> |
|<span data-ttu-id="3c757-110">Long-ID (Abdeckung):</span><span class="sxs-lookup"><span data-stu-id="3c757-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="3c757-111">0x0000000C</span><span class="sxs-lookup"><span data-stu-id="3c757-111">0x0000000C</span></span>  <br/> |
|<span data-ttu-id="3c757-112">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="3c757-112">Data type:</span></span>  <br/> |<span data-ttu-id="3c757-113">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="3c757-113">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="3c757-114">Bereich:</span><span class="sxs-lookup"><span data-stu-id="3c757-114">Area:</span></span>  <br/> |<span data-ttu-id="3c757-115">Besprechungen</span><span class="sxs-lookup"><span data-stu-id="3c757-115">Meetings</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="3c757-116">HinwBemerkungeneise</span><span class="sxs-lookup"><span data-stu-id="3c757-116">Remarks</span></span>

<span data-ttu-id="3c757-117">Diese Eigenschaft ist schreibgeschützt, wenn die **DispidApptRecur** ([PidLidAppointmentRecur](pidlidappointmentrecur-canonical-property.md))-Eigenschaft nicht festgelegt ist, aber die **LID_IS_RECURRING** ([PidLidIsRecurring](pidlidisrecurring-canonical-property.md))-Eigenschaft ist TRUE und **LID_IS_EXCEPTION** ([ PidLidIsException](pidlidisexception-canonical-property.md))-Eigenschaft lautet FALSE.</span><span class="sxs-lookup"><span data-stu-id="3c757-117">This property is only read if the **dispidApptRecur** ([PidLidAppointmentRecur](pidlidappointmentrecur-canonical-property.md)) property is not set, but if the **LID_IS_RECURRING** ([PidLidIsRecurring](pidlidisrecurring-canonical-property.md)) property is TRUE and the **LID_IS_EXCEPTION** ([PidLidIsException](pidlidisexception-canonical-property.md)) property is FALSE.</span></span> <span data-ttu-id="3c757-118">Das untere Wort gibt einen Index in einer Tabelle, die Informationen zur Zeitzone enthält.</span><span class="sxs-lookup"><span data-stu-id="3c757-118">The lower WORD specifies an index into a table that contains time zone information.</span></span> <span data-ttu-id="3c757-119">Die obere Wort ist nur das höchste Bit gelesen werden.</span><span class="sxs-lookup"><span data-stu-id="3c757-119">From the upper WORD, only the highest bit is read.</span></span> <span data-ttu-id="3c757-120">Wenn dieses Bit gesetzt ist, klicken Sie dann berücksichtigt die Zeitzone auf die verwiesen wird nicht, dass Sommerzeit (Ziel), andernfalls die neuen Sommerzeitregeln Datumsangaben in [[MS-OXOCAL]](http://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx) beschrieben ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="3c757-120">If that bit is set, then the time zone referenced will not observe daylight saving time (DST), otherwise the DST dates detailed in [[MS-OXOCAL]](http://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx) will be followed.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="3c757-121">Verwandte Ressourcen</span><span class="sxs-lookup"><span data-stu-id="3c757-121">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="3c757-122">Protokollspezifikationen</span><span class="sxs-lookup"><span data-stu-id="3c757-122">Protocol specifications</span></span>

<span data-ttu-id="3c757-123">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="3c757-123">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="3c757-124">Enthält Eigenschaftendefinitionen und Verweise auf Verwandte Exchange Server-Spezifikationen.</span><span class="sxs-lookup"><span data-stu-id="3c757-124">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="3c757-125">[[MS-OXOCAL]](http://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="3c757-125">[[MS-OXOCAL]](http://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="3c757-126">Gibt die Eigenschaften und Vorgänge für den Termin, einer Besprechungsanfrage und Antwortnachrichten.</span><span class="sxs-lookup"><span data-stu-id="3c757-126">Specifies the properties and operations for appointment, meeting request, and response messages.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="3c757-127">Header-Dateien</span><span class="sxs-lookup"><span data-stu-id="3c757-127">Header files</span></span>

<span data-ttu-id="3c757-128">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="3c757-128">Mapidefs.h</span></span>
  
> <span data-ttu-id="3c757-129">Enthält die Datentypdefinitionen.</span><span class="sxs-lookup"><span data-stu-id="3c757-129">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="3c757-130">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="3c757-130">See also</span></span>



[<span data-ttu-id="3c757-131">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="3c757-131">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="3c757-132">Kanonische MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="3c757-132">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="3c757-133">Zuordnen von kanonischen Eigenschaftennamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="3c757-133">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="3c757-134">Zuordnen von MAPI-Namen zu kanonische Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="3c757-134">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

