---
title: PidLidRecurring (kanonische Eigenschaft)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidRecurring
api_type:
- COM
ms.assetid: 3d39a053-277f-4d59-ab2e-cee81710f2ab
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 85e78695a7c4fca5a1e5cd28b0254d4559be0c13
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32315918"
---
# <a name="pidlidrecurring-canonical-property"></a><span data-ttu-id="e1c82-103">PidLidRecurring (kanonische Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="e1c82-103">PidLidRecurring Canonical Property</span></span>

  
  
<span data-ttu-id="e1c82-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="e1c82-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="e1c82-105">Gibt an, ob eine Terminnachricht wiederholt wird.</span><span class="sxs-lookup"><span data-stu-id="e1c82-105">Specifies whether an appointment message is recurrent.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="e1c82-106">Zugeordnete Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="e1c82-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="e1c82-107">dispidRecurring</span><span class="sxs-lookup"><span data-stu-id="e1c82-107">dispidRecurring</span></span>  <br/> |
|<span data-ttu-id="e1c82-108">Eigenschaftensatz:</span><span class="sxs-lookup"><span data-stu-id="e1c82-108">Property set:</span></span>  <br/> |<span data-ttu-id="e1c82-109">PSETID_Appointment</span><span class="sxs-lookup"><span data-stu-id="e1c82-109">PSETID_Appointment</span></span>  <br/> |
|<span data-ttu-id="e1c82-110">Lange ID (LID):</span><span class="sxs-lookup"><span data-stu-id="e1c82-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="e1c82-111">0x00008223</span><span class="sxs-lookup"><span data-stu-id="e1c82-111">0x00008223</span></span>  <br/> |
|<span data-ttu-id="e1c82-112">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="e1c82-112">Data type:</span></span>  <br/> |<span data-ttu-id="e1c82-113">PT_BOOLEAN</span><span class="sxs-lookup"><span data-stu-id="e1c82-113">PT_BOOLEAN</span></span>  <br/> |
|<span data-ttu-id="e1c82-114">Bereich:</span><span class="sxs-lookup"><span data-stu-id="e1c82-114">Area:</span></span>  <br/> |<span data-ttu-id="e1c82-115">Kalender</span><span class="sxs-lookup"><span data-stu-id="e1c82-115">Calendar</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="e1c82-116">Hinweise</span><span class="sxs-lookup"><span data-stu-id="e1c82-116">Remarks</span></span>

<span data-ttu-id="e1c82-117">Diese Eigenschaft ist TRUE, wenn es sich bei dem Termin um einen Termin mit Terminserie handelt, und false, wenn er nicht wiederholt wird.</span><span class="sxs-lookup"><span data-stu-id="e1c82-117">This property is TRUE if the appointment is a recurring appointment, and is FALSE if it is not recurring.</span></span>
  
<span data-ttu-id="e1c82-118">Diese Eigenschaft gibt an, ob das Objekt eine Serienserie darstellt.</span><span class="sxs-lookup"><span data-stu-id="e1c82-118">This property specifies whether or not the object represents a recurring series.</span></span> <span data-ttu-id="e1c82-119">Der Wert TRUE gibt an, dass das Objekt eine Serienserie darstellt.</span><span class="sxs-lookup"><span data-stu-id="e1c82-119">A value of TRUE indicates that the object represents a recurring series.</span></span> <span data-ttu-id="e1c82-120">Der Wert FALSE oder das Fehlen dieser Eigenschaft gibt an, dass das Objekt entweder eine einzelne Instanz oder eine Ausnahme darstellt (einschließlich einer verwaisten Instanz).</span><span class="sxs-lookup"><span data-stu-id="e1c82-120">A value of FALSE, or the absence of this property, indicates that the object represents either a single instance or an exception (including an orphan instance).</span></span> <span data-ttu-id="e1c82-121">Beachten Sie den Unterschied zwischen dieser Eigenschaft und **der LID_IS_RECURRING** ([PidLidIsRecurring](pidlidisrecurring-canonical-property.md)) -Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="e1c82-121">Note the difference between this property and the **LID_IS_RECURRING** ([PidLidIsRecurring](pidlidisrecurring-canonical-property.md)) property.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="e1c82-122">Verwandte Ressourcen</span><span class="sxs-lookup"><span data-stu-id="e1c82-122">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="e1c82-123">Protokollspezifikationen</span><span class="sxs-lookup"><span data-stu-id="e1c82-123">Protocol specifications</span></span>

<span data-ttu-id="e1c82-124">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="e1c82-124">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="e1c82-125">Stellt Eigenschaftensatzdefinitionen und Verweise auf verwandte Exchange Server zur Verfügung.</span><span class="sxs-lookup"><span data-stu-id="e1c82-125">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="e1c82-126">[[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="e1c82-126">[[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="e1c82-127">Gibt die Eigenschaften und Vorgänge für Termin-, Besprechungs- und Antwortnachrichten an.</span><span class="sxs-lookup"><span data-stu-id="e1c82-127">Specifies the properties and operations for appointment, meeting request, and response messages.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="e1c82-128">Headerdateien</span><span class="sxs-lookup"><span data-stu-id="e1c82-128">Header files</span></span>

<span data-ttu-id="e1c82-129">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="e1c82-129">Mapidefs.h</span></span>
  
> <span data-ttu-id="e1c82-130">Bietet Datentypdefinitionen.</span><span class="sxs-lookup"><span data-stu-id="e1c82-130">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="e1c82-131">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="e1c82-131">See also</span></span>



[<span data-ttu-id="e1c82-132">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="e1c82-132">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="e1c82-133">KANONISCHE EIGENSCHAFTEN VON MAPI</span><span class="sxs-lookup"><span data-stu-id="e1c82-133">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="e1c82-134">Zuordnen kanonischer Eigenschaftsnamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="e1c82-134">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="e1c82-135">Zuordnen von MAPI-Namen zu kanonischen Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="e1c82-135">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

