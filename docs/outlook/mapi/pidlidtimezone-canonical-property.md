---
title: Kanonische Pidlidtimezone (-Eigenschaft
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
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: b62779567a7dbd298fdd313e90b13fb223e4e47e
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32319271"
---
# <a name="pidlidtimezone-canonical-property"></a><span data-ttu-id="c49f3-103">Kanonische Pidlidtimezone (-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="c49f3-103">PidLidTimeZone Canonical Property</span></span>

  
  
<span data-ttu-id="c49f3-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="c49f3-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="c49f3-105">Gibt Informationen zur Zeitzone einer Besprechungsserie an.</span><span class="sxs-lookup"><span data-stu-id="c49f3-105">Specifies information about the time zone of a recurring meeting.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="c49f3-106">Zugeordnete Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="c49f3-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="c49f3-107">LID_TIME_ZONE</span><span class="sxs-lookup"><span data-stu-id="c49f3-107">LID_TIME_ZONE</span></span>  <br/> |
|<span data-ttu-id="c49f3-108">Eigenschaftensatz:</span><span class="sxs-lookup"><span data-stu-id="c49f3-108">Property set:</span></span>  <br/> |<span data-ttu-id="c49f3-109">PSETID_Meeting</span><span class="sxs-lookup"><span data-stu-id="c49f3-109">PSETID_Meeting</span></span>  <br/> |
|<span data-ttu-id="c49f3-110">Long-ID (Deckel):</span><span class="sxs-lookup"><span data-stu-id="c49f3-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="c49f3-111">0x0000000C</span><span class="sxs-lookup"><span data-stu-id="c49f3-111">0x0000000C</span></span>  <br/> |
|<span data-ttu-id="c49f3-112">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="c49f3-112">Data type:</span></span>  <br/> |<span data-ttu-id="c49f3-113">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="c49f3-113">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="c49f3-114">Bereich:</span><span class="sxs-lookup"><span data-stu-id="c49f3-114">Area:</span></span>  <br/> |<span data-ttu-id="c49f3-115">Meetings</span><span class="sxs-lookup"><span data-stu-id="c49f3-115">Meetings</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="c49f3-116">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="c49f3-116">Remarks</span></span>

<span data-ttu-id="c49f3-117">Diese Eigenschaft wird nur dann gelesen, wenn die **dispidApptRecur** ([pidlidappointmentrecur (](pidlidappointmentrecur-canonical-property.md))-Eigenschaft nicht festgelegt ist, aber wenn die **LID_IS_RECURRING** ([pidlidisrecurring (](pidlidisrecurring-canonical-property.md))-Eigenschaft true ist und die **LID_IS_EXCEPTION** ([ Pidlidisexception (](pidlidisexception-canonical-property.md))-Eigenschaft ist false.</span><span class="sxs-lookup"><span data-stu-id="c49f3-117">This property is only read if the **dispidApptRecur** ([PidLidAppointmentRecur](pidlidappointmentrecur-canonical-property.md)) property is not set, but if the **LID_IS_RECURRING** ([PidLidIsRecurring](pidlidisrecurring-canonical-property.md)) property is TRUE and the **LID_IS_EXCEPTION** ([PidLidIsException](pidlidisexception-canonical-property.md)) property is FALSE.</span></span> <span data-ttu-id="c49f3-118">Das untere Wort gibt einen Index in einer Tabelle an, die Zeitzoneninformationen enthält.</span><span class="sxs-lookup"><span data-stu-id="c49f3-118">The lower WORD specifies an index into a table that contains time zone information.</span></span> <span data-ttu-id="c49f3-119">Aus dem oberen Wort wird nur das höchste Bit gelesen.</span><span class="sxs-lookup"><span data-stu-id="c49f3-119">From the upper WORD, only the highest bit is read.</span></span> <span data-ttu-id="c49f3-120">Wenn dieses Bit festgelegt ist, wird in der Zeitzone, auf die verwiesen wird, keine Sommerzeit (DST) beobachtet, da andernfalls die in [[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx) ausführlich erläuterten DST-Daten befolgt werden.</span><span class="sxs-lookup"><span data-stu-id="c49f3-120">If that bit is set, then the time zone referenced will not observe daylight saving time (DST), otherwise the DST dates detailed in [[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx) will be followed.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="c49f3-121">Zugehörige Ressourcen</span><span class="sxs-lookup"><span data-stu-id="c49f3-121">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="c49f3-122">Protokollspezifikationen</span><span class="sxs-lookup"><span data-stu-id="c49f3-122">Protocol specifications</span></span>

<span data-ttu-id="c49f3-123">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="c49f3-123">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="c49f3-124">Stellt Eigenschaftensatz Definitionen und Verweise auf zugehörige Exchange Server-Protokollspezifikationen bereit.</span><span class="sxs-lookup"><span data-stu-id="c49f3-124">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="c49f3-125">[[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="c49f3-125">[[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="c49f3-126">Gibt die Eigenschaften und Vorgänge für Termin-, Besprechungs-und Antwortnachrichten an.</span><span class="sxs-lookup"><span data-stu-id="c49f3-126">Specifies the properties and operations for appointment, meeting request, and response messages.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="c49f3-127">Header Dateien</span><span class="sxs-lookup"><span data-stu-id="c49f3-127">Header files</span></span>

<span data-ttu-id="c49f3-128">Mapidefs. h</span><span class="sxs-lookup"><span data-stu-id="c49f3-128">Mapidefs.h</span></span>
  
> <span data-ttu-id="c49f3-129">Stellt Datentypdefinitionen bereit.</span><span class="sxs-lookup"><span data-stu-id="c49f3-129">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="c49f3-130">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="c49f3-130">See also</span></span>



[<span data-ttu-id="c49f3-131">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="c49f3-131">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="c49f3-132">Kanonische MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="c49f3-132">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="c49f3-133">Zuordnen von kanonischen Eigenschaftennamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="c49f3-133">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="c49f3-134">Zuordnen von MAPI-Namen zu kanonischen Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="c49f3-134">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

