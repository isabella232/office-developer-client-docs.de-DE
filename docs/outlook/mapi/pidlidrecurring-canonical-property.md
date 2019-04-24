---
title: Kanonische Pidlidrecurring (-Eigenschaft
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
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: 85e78695a7c4fca5a1e5cd28b0254d4559be0c13
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32315918"
---
# <a name="pidlidrecurring-canonical-property"></a><span data-ttu-id="7d63d-103">Kanonische Pidlidrecurring (-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="7d63d-103">PidLidRecurring Canonical Property</span></span>

  
  
<span data-ttu-id="7d63d-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="7d63d-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="7d63d-105">Gibt an, ob eine Termin Nachricht recurrent ist.</span><span class="sxs-lookup"><span data-stu-id="7d63d-105">Specifies whether an appointment message is recurrent.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="7d63d-106">Zugeordnete Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="7d63d-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="7d63d-107">dispidRecurring</span><span class="sxs-lookup"><span data-stu-id="7d63d-107">dispidRecurring</span></span>  <br/> |
|<span data-ttu-id="7d63d-108">Eigenschaftensatz:</span><span class="sxs-lookup"><span data-stu-id="7d63d-108">Property set:</span></span>  <br/> |<span data-ttu-id="7d63d-109">PSETID_Appointment</span><span class="sxs-lookup"><span data-stu-id="7d63d-109">PSETID_Appointment</span></span>  <br/> |
|<span data-ttu-id="7d63d-110">Long-ID (Deckel):</span><span class="sxs-lookup"><span data-stu-id="7d63d-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="7d63d-111">0x00008223</span><span class="sxs-lookup"><span data-stu-id="7d63d-111">0x00008223</span></span>  <br/> |
|<span data-ttu-id="7d63d-112">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="7d63d-112">Data type:</span></span>  <br/> |<span data-ttu-id="7d63d-113">PT_BOOLEAN</span><span class="sxs-lookup"><span data-stu-id="7d63d-113">PT_BOOLEAN</span></span>  <br/> |
|<span data-ttu-id="7d63d-114">Bereich:</span><span class="sxs-lookup"><span data-stu-id="7d63d-114">Area:</span></span>  <br/> |<span data-ttu-id="7d63d-115">Kalender</span><span class="sxs-lookup"><span data-stu-id="7d63d-115">Calendar</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="7d63d-116">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="7d63d-116">Remarks</span></span>

<span data-ttu-id="7d63d-117">Diese Eigenschaft ist TRUE, wenn der Termin eine Terminserie ist und FALSE, wenn es nicht wiederholt wird.</span><span class="sxs-lookup"><span data-stu-id="7d63d-117">This property is TRUE if the appointment is a recurring appointment, and is FALSE if it is not recurring.</span></span>
  
<span data-ttu-id="7d63d-118">Diese Eigenschaft gibt an, ob das Objekt eine wiederkehrende Datenreihe darstellt.</span><span class="sxs-lookup"><span data-stu-id="7d63d-118">This property specifies whether or not the object represents a recurring series.</span></span> <span data-ttu-id="7d63d-119">Der Wert TRUE gibt an, dass das Objekt eine wiederkehrende Datenreihe darstellt.</span><span class="sxs-lookup"><span data-stu-id="7d63d-119">A value of TRUE indicates that the object represents a recurring series.</span></span> <span data-ttu-id="7d63d-120">Der Wert FALSE oder das Fehlen dieser Eigenschaft gibt an, dass das Objekt entweder eine einzelne Instanz oder eine Ausnahme (einschließlich einer verwaisten Instanz) darstellt.</span><span class="sxs-lookup"><span data-stu-id="7d63d-120">A value of FALSE, or the absence of this property, indicates that the object represents either a single instance or an exception (including an orphan instance).</span></span> <span data-ttu-id="7d63d-121">Beachten Sie den Unterschied zwischen dieser Eigenschaft und der **LID_IS_RECURRING** ([pidlidisrecurring (](pidlidisrecurring-canonical-property.md))-Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="7d63d-121">Note the difference between this property and the **LID_IS_RECURRING** ([PidLidIsRecurring](pidlidisrecurring-canonical-property.md)) property.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="7d63d-122">Zugehörige Ressourcen</span><span class="sxs-lookup"><span data-stu-id="7d63d-122">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="7d63d-123">Protokollspezifikationen</span><span class="sxs-lookup"><span data-stu-id="7d63d-123">Protocol specifications</span></span>

<span data-ttu-id="7d63d-124">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="7d63d-124">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="7d63d-125">Stellt Eigenschaftensatz Definitionen und Verweise auf zugehörige Exchange Server-Protokollspezifikationen bereit.</span><span class="sxs-lookup"><span data-stu-id="7d63d-125">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="7d63d-126">[[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="7d63d-126">[[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="7d63d-127">Gibt die Eigenschaften und Vorgänge für Termin-, Besprechungs-und Antwortnachrichten an.</span><span class="sxs-lookup"><span data-stu-id="7d63d-127">Specifies the properties and operations for appointment, meeting request, and response messages.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="7d63d-128">Header Dateien</span><span class="sxs-lookup"><span data-stu-id="7d63d-128">Header files</span></span>

<span data-ttu-id="7d63d-129">Mapidefs. h</span><span class="sxs-lookup"><span data-stu-id="7d63d-129">Mapidefs.h</span></span>
  
> <span data-ttu-id="7d63d-130">Stellt Datentypdefinitionen bereit.</span><span class="sxs-lookup"><span data-stu-id="7d63d-130">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="7d63d-131">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="7d63d-131">See also</span></span>



[<span data-ttu-id="7d63d-132">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="7d63d-132">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="7d63d-133">Kanonische MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="7d63d-133">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="7d63d-134">Zuordnen von kanonischen Eigenschaftennamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="7d63d-134">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="7d63d-135">Zuordnen von MAPI-Namen zu kanonischen Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="7d63d-135">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

