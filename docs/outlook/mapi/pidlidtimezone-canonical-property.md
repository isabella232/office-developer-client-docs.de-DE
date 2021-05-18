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
ms.openlocfilehash: b62779567a7dbd298fdd313e90b13fb223e4e47e
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32319271"
---
# <a name="pidlidtimezone-canonical-property"></a><span data-ttu-id="f2f8f-103">PidLidTimeZone (kanonische Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="f2f8f-103">PidLidTimeZone Canonical Property</span></span>

  
  
<span data-ttu-id="f2f8f-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="f2f8f-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="f2f8f-105">Gibt Informationen zur Zeitzone einer Besprechungsserie an.</span><span class="sxs-lookup"><span data-stu-id="f2f8f-105">Specifies information about the time zone of a recurring meeting.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="f2f8f-106">Zugeordnete Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="f2f8f-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="f2f8f-107">LID_TIME_ZONE</span><span class="sxs-lookup"><span data-stu-id="f2f8f-107">LID_TIME_ZONE</span></span>  <br/> |
|<span data-ttu-id="f2f8f-108">Eigenschaftensatz:</span><span class="sxs-lookup"><span data-stu-id="f2f8f-108">Property set:</span></span>  <br/> |<span data-ttu-id="f2f8f-109">PSETID_Meeting</span><span class="sxs-lookup"><span data-stu-id="f2f8f-109">PSETID_Meeting</span></span>  <br/> |
|<span data-ttu-id="f2f8f-110">Lange ID (LID):</span><span class="sxs-lookup"><span data-stu-id="f2f8f-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="f2f8f-111">0x0000000C</span><span class="sxs-lookup"><span data-stu-id="f2f8f-111">0x0000000C</span></span>  <br/> |
|<span data-ttu-id="f2f8f-112">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="f2f8f-112">Data type:</span></span>  <br/> |<span data-ttu-id="f2f8f-113">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="f2f8f-113">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="f2f8f-114">Bereich:</span><span class="sxs-lookup"><span data-stu-id="f2f8f-114">Area:</span></span>  <br/> |<span data-ttu-id="f2f8f-115">Besprechungen</span><span class="sxs-lookup"><span data-stu-id="f2f8f-115">Meetings</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="f2f8f-116">Hinweise</span><span class="sxs-lookup"><span data-stu-id="f2f8f-116">Remarks</span></span>

<span data-ttu-id="f2f8f-117">Diese Eigenschaft wird nur gelesen, wenn die **dispidApptRecur** ([PidLidAppointmentRecur](pidlidappointmentrecur-canonical-property.md)) -Eigenschaft nicht festgelegt ist, aber wenn die **LID_IS_RECURRING** ([PidLidIsRecurring](pidlidisrecurring-canonical-property.md)) -Eigenschaft TRUE und die **LID_IS_EXCEPTION** ([PidLidIsException](pidlidisexception-canonical-property.md)) -Eigenschaft false ist.</span><span class="sxs-lookup"><span data-stu-id="f2f8f-117">This property is only read if the **dispidApptRecur** ([PidLidAppointmentRecur](pidlidappointmentrecur-canonical-property.md)) property is not set, but if the **LID_IS_RECURRING** ([PidLidIsRecurring](pidlidisrecurring-canonical-property.md)) property is TRUE and the **LID_IS_EXCEPTION** ([PidLidIsException](pidlidisexception-canonical-property.md)) property is FALSE.</span></span> <span data-ttu-id="f2f8f-118">Der untere WORD-Wert gibt einen Index in einer Tabelle an, die Zeitzoneninformationen enthält.</span><span class="sxs-lookup"><span data-stu-id="f2f8f-118">The lower WORD specifies an index into a table that contains time zone information.</span></span> <span data-ttu-id="f2f8f-119">Aus dem oberen WORD wird nur das höchste Bit gelesen.</span><span class="sxs-lookup"><span data-stu-id="f2f8f-119">From the upper WORD, only the highest bit is read.</span></span> <span data-ttu-id="f2f8f-120">Wenn dieses Bit festgelegt ist, wird in der referenzierten Zeitzone die Sommerzeit (Sommerzeit, Sommerzeit, Sommerzeit) nicht beobachtet, andernfalls werden die in [[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx) detaillierten Sommerzeitdaten befolgt.</span><span class="sxs-lookup"><span data-stu-id="f2f8f-120">If that bit is set, then the time zone referenced will not observe daylight saving time (DST), otherwise the DST dates detailed in [[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx) will be followed.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="f2f8f-121">Verwandte Ressourcen</span><span class="sxs-lookup"><span data-stu-id="f2f8f-121">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="f2f8f-122">Protokollspezifikationen</span><span class="sxs-lookup"><span data-stu-id="f2f8f-122">Protocol specifications</span></span>

<span data-ttu-id="f2f8f-123">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="f2f8f-123">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="f2f8f-124">Stellt Eigenschaftensatzdefinitionen und Verweise auf verwandte Exchange Server zur Verfügung.</span><span class="sxs-lookup"><span data-stu-id="f2f8f-124">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="f2f8f-125">[[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="f2f8f-125">[[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="f2f8f-126">Gibt die Eigenschaften und Vorgänge für Termin-, Besprechungs- und Antwortnachrichten an.</span><span class="sxs-lookup"><span data-stu-id="f2f8f-126">Specifies the properties and operations for appointment, meeting request, and response messages.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="f2f8f-127">Headerdateien</span><span class="sxs-lookup"><span data-stu-id="f2f8f-127">Header files</span></span>

<span data-ttu-id="f2f8f-128">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="f2f8f-128">Mapidefs.h</span></span>
  
> <span data-ttu-id="f2f8f-129">Bietet Datentypdefinitionen.</span><span class="sxs-lookup"><span data-stu-id="f2f8f-129">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="f2f8f-130">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="f2f8f-130">See also</span></span>



[<span data-ttu-id="f2f8f-131">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="f2f8f-131">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="f2f8f-132">KANONISCHE EIGENSCHAFTEN VON MAPI</span><span class="sxs-lookup"><span data-stu-id="f2f8f-132">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="f2f8f-133">Zuordnen kanonischer Eigenschaftsnamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="f2f8f-133">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="f2f8f-134">Zuordnen von MAPI-Namen zu kanonischen Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="f2f8f-134">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

