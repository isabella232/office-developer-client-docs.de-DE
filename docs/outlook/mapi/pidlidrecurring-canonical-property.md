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
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/04/2018
ms.locfileid: "25399480"
---
# <a name="pidlidrecurring-canonical-property"></a><span data-ttu-id="13ff6-103">PidLidRecurring (kanonische Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="13ff6-103">PidLidRecurring Canonical Property</span></span>

  
  
<span data-ttu-id="13ff6-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="13ff6-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="13ff6-105">Gibt an, ob eine Nachricht Termin eine Serie ist.</span><span class="sxs-lookup"><span data-stu-id="13ff6-105">Specifies whether an appointment message is recurrent.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="13ff6-106">Zugeordnete Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="13ff6-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="13ff6-107">dispidRecurring</span><span class="sxs-lookup"><span data-stu-id="13ff6-107">dispidRecurring</span></span>  <br/> |
|<span data-ttu-id="13ff6-108">-Eigenschaft festgelegt:</span><span class="sxs-lookup"><span data-stu-id="13ff6-108">Property set:</span></span>  <br/> |<span data-ttu-id="13ff6-109">PSETID_Appointment</span><span class="sxs-lookup"><span data-stu-id="13ff6-109">PSETID_Appointment</span></span>  <br/> |
|<span data-ttu-id="13ff6-110">Long-ID (Abdeckung):</span><span class="sxs-lookup"><span data-stu-id="13ff6-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="13ff6-111">0x00008223</span><span class="sxs-lookup"><span data-stu-id="13ff6-111">0x00008223</span></span>  <br/> |
|<span data-ttu-id="13ff6-112">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="13ff6-112">Data type:</span></span>  <br/> |<span data-ttu-id="13ff6-113">PT_BOOLEAN</span><span class="sxs-lookup"><span data-stu-id="13ff6-113">PT_BOOLEAN</span></span>  <br/> |
|<span data-ttu-id="13ff6-114">Bereich:</span><span class="sxs-lookup"><span data-stu-id="13ff6-114">Area:</span></span>  <br/> |<span data-ttu-id="13ff6-115">Kalender</span><span class="sxs-lookup"><span data-stu-id="13ff6-115">Calendar</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="13ff6-116">Hinweise</span><span class="sxs-lookup"><span data-stu-id="13ff6-116">Remarks</span></span>

<span data-ttu-id="13ff6-117">Diese Eigenschaft ist TRUE, wenn der Termin einer Terminserie ist, und ist FALSE, wenn es nicht wiederholt wird.</span><span class="sxs-lookup"><span data-stu-id="13ff6-117">This property is TRUE if the appointment is a recurring appointment, and is FALSE if it is not recurring.</span></span>
  
<span data-ttu-id="13ff6-118">Diese Eigenschaft gibt an, ob das Objekt einer Terminserie darstellt.</span><span class="sxs-lookup"><span data-stu-id="13ff6-118">This property specifies whether or not the object represents a recurring series.</span></span> <span data-ttu-id="13ff6-119">Der Wert TRUE gibt an, dass das Objekt einer Terminserie darstellt.</span><span class="sxs-lookup"><span data-stu-id="13ff6-119">A value of TRUE indicates that the object represents a recurring series.</span></span> <span data-ttu-id="13ff6-120">Den Wert FALSE oder das fehlen diese Eigenschaft gibt an, dass das Objekt eine einzelne Instanz oder eine Ausnahme (einschließlich einer verwaisten Instanz) darstellt.</span><span class="sxs-lookup"><span data-stu-id="13ff6-120">A value of FALSE, or the absence of this property, indicates that the object represents either a single instance or an exception (including an orphan instance).</span></span> <span data-ttu-id="13ff6-121">Beachten Sie den Unterschied zwischen dieser Eigenschaft und die **LID_IS_RECURRING** ([PidLidIsRecurring](pidlidisrecurring-canonical-property.md))-Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="13ff6-121">Note the difference between this property and the **LID_IS_RECURRING** ([PidLidIsRecurring](pidlidisrecurring-canonical-property.md)) property.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="13ff6-122">Verwandte Ressourcen</span><span class="sxs-lookup"><span data-stu-id="13ff6-122">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="13ff6-123">Protokollspezifikationen</span><span class="sxs-lookup"><span data-stu-id="13ff6-123">Protocol specifications</span></span>

<span data-ttu-id="13ff6-124">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="13ff6-124">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="13ff6-125">Enthält Eigenschaftendefinitionen und Verweise auf Verwandte Exchange Server-Spezifikationen.</span><span class="sxs-lookup"><span data-stu-id="13ff6-125">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="13ff6-126">[[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="13ff6-126">[[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="13ff6-127">Gibt die Eigenschaften und Vorgänge für den Termin, einer Besprechungsanfrage und Antwortnachrichten.</span><span class="sxs-lookup"><span data-stu-id="13ff6-127">Specifies the properties and operations for appointment, meeting request, and response messages.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="13ff6-128">Header-Dateien</span><span class="sxs-lookup"><span data-stu-id="13ff6-128">Header files</span></span>

<span data-ttu-id="13ff6-129">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="13ff6-129">Mapidefs.h</span></span>
  
> <span data-ttu-id="13ff6-130">Enthält die Datentypdefinitionen.</span><span class="sxs-lookup"><span data-stu-id="13ff6-130">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="13ff6-131">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="13ff6-131">See also</span></span>



[<span data-ttu-id="13ff6-132">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="13ff6-132">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="13ff6-133">Kanonische MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="13ff6-133">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="13ff6-134">Zuordnen von kanonischen Eigenschaftennamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="13ff6-134">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="13ff6-135">Zuordnen von MAPI-Namen zu kanonische Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="13ff6-135">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

