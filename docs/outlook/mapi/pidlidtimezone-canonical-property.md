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
ms.openlocfilehash: 5eb9842da78541bc8c73cd5b2c52abeb927f9031
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19793884"
---
# <a name="pidlidtimezone-canonical-property"></a><span data-ttu-id="91ec0-103">PidLidTimeZone (kanonische Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="91ec0-103">PidLidTimeZone Canonical Property</span></span>

  
  
<span data-ttu-id="91ec0-104">**Betrifft**: Outlook</span><span class="sxs-lookup"><span data-stu-id="91ec0-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="91ec0-105">Gibt Informationen über die Zeitzone einer Besprechungsserie.</span><span class="sxs-lookup"><span data-stu-id="91ec0-105">Specifies information about the time zone of a recurring meeting.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="91ec0-106">Zugeordneten Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="91ec0-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="91ec0-107">LID_TIME_ZONE</span><span class="sxs-lookup"><span data-stu-id="91ec0-107">LID_TIME_ZONE</span></span>  <br/> |
|<span data-ttu-id="91ec0-108">-Eigenschaft festgelegt:</span><span class="sxs-lookup"><span data-stu-id="91ec0-108">Property set:</span></span>  <br/> |<span data-ttu-id="91ec0-109">PSETID_Meeting</span><span class="sxs-lookup"><span data-stu-id="91ec0-109">PSETID_Meeting</span></span>  <br/> |
|<span data-ttu-id="91ec0-110">Long-ID (Abdeckung):</span><span class="sxs-lookup"><span data-stu-id="91ec0-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="91ec0-111">0x0000000C</span><span class="sxs-lookup"><span data-stu-id="91ec0-111">0x0000000C</span></span>  <br/> |
|<span data-ttu-id="91ec0-112">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="91ec0-112">Data type:</span></span>  <br/> |<span data-ttu-id="91ec0-113">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="91ec0-113">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="91ec0-114">Bereich:</span><span class="sxs-lookup"><span data-stu-id="91ec0-114">Area:</span></span>  <br/> |<span data-ttu-id="91ec0-115">Besprechungen</span><span class="sxs-lookup"><span data-stu-id="91ec0-115">Meetings</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="91ec0-116">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="91ec0-116">Remarks</span></span>

<span data-ttu-id="91ec0-117">Diese Eigenschaft ist schreibgeschützt, wenn die **DispidApptRecur** ([PidLidAppointmentRecur](pidlidappointmentrecur-canonical-property.md))-Eigenschaft nicht festgelegt ist, aber die **LID_IS_RECURRING** ([PidLidIsRecurring](pidlidisrecurring-canonical-property.md))-Eigenschaft ist TRUE und **LID_IS_EXCEPTION** ([ PidLidIsException](pidlidisexception-canonical-property.md))-Eigenschaft lautet FALSE.</span><span class="sxs-lookup"><span data-stu-id="91ec0-117">This property is only read if the **dispidApptRecur** ([PidLidAppointmentRecur](pidlidappointmentrecur-canonical-property.md)) property is not set, but if the **LID_IS_RECURRING** ([PidLidIsRecurring](pidlidisrecurring-canonical-property.md)) property is TRUE and the **LID_IS_EXCEPTION** ([PidLidIsException](pidlidisexception-canonical-property.md)) property is FALSE.</span></span> <span data-ttu-id="91ec0-118">Das untere Wort gibt einen Index in einer Tabelle, die Informationen zur Zeitzone enthält.</span><span class="sxs-lookup"><span data-stu-id="91ec0-118">The lower WORD specifies an index into a table that contains time zone information.</span></span> <span data-ttu-id="91ec0-119">Die obere Wort ist nur das höchste Bit gelesen werden.</span><span class="sxs-lookup"><span data-stu-id="91ec0-119">From the upper WORD, only the highest bit is read.</span></span> <span data-ttu-id="91ec0-120">Wenn dieses Bit gesetzt ist, klicken Sie dann berücksichtigt die Zeitzone auf die verwiesen wird nicht, dass Sommerzeit (Ziel), andernfalls die neuen Sommerzeitregeln Datumsangaben in [[MS-OXOCAL]](http://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx) beschrieben ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="91ec0-120">If that bit is set, then the time zone referenced will not observe daylight saving time (DST), otherwise the DST dates detailed in [[MS-OXOCAL]](http://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx) will be followed.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="91ec0-121">Verwandte Ressourcen</span><span class="sxs-lookup"><span data-stu-id="91ec0-121">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="91ec0-122">Protokollspezifikationen</span><span class="sxs-lookup"><span data-stu-id="91ec0-122">Protocol specifications</span></span>

<span data-ttu-id="91ec0-123">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="91ec0-123">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="91ec0-124">Enthält Eigenschaftendefinitionen und Verweise auf Verwandte Exchange Server-Spezifikationen.</span><span class="sxs-lookup"><span data-stu-id="91ec0-124">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="91ec0-125">[[MS-OXOCAL]](http://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="91ec0-125">[[MS-OXOCAL]](http://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="91ec0-126">Gibt die Eigenschaften und Vorgänge für den Termin, einer Besprechungsanfrage und Antwortnachrichten.</span><span class="sxs-lookup"><span data-stu-id="91ec0-126">Specifies the properties and operations for appointment, meeting request, and response messages.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="91ec0-127">Header-Dateien</span><span class="sxs-lookup"><span data-stu-id="91ec0-127">Header files</span></span>

<span data-ttu-id="91ec0-128">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="91ec0-128">Mapidefs.h</span></span>
  
> <span data-ttu-id="91ec0-129">Enthält die Datentypdefinitionen.</span><span class="sxs-lookup"><span data-stu-id="91ec0-129">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="91ec0-130">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="91ec0-130">See also</span></span>



[<span data-ttu-id="91ec0-131">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="91ec0-131">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="91ec0-132">Kanonische MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="91ec0-132">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="91ec0-133">Zuordnen von kanonischen Eigenschaftennamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="91ec0-133">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="91ec0-134">Zuordnen von MAPI-Namen zu kanonische Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="91ec0-134">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

