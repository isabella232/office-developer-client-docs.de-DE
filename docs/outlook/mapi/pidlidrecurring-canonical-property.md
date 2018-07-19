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
ms.openlocfilehash: 36bf204823711e87ac6250f0997445f2745fbc19
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19793730"
---
# <a name="pidlidrecurring-canonical-property"></a><span data-ttu-id="34a0a-103">PidLidRecurring (kanonische Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="34a0a-103">PidLidRecurring Canonical Property</span></span>

  
  
<span data-ttu-id="34a0a-104">**Betrifft**: Outlook</span><span class="sxs-lookup"><span data-stu-id="34a0a-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="34a0a-105">Gibt an, ob eine Nachricht Termin eine Serie ist.</span><span class="sxs-lookup"><span data-stu-id="34a0a-105">Specifies whether an appointment message is recurrent.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="34a0a-106">Zugeordneten Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="34a0a-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="34a0a-107">dispidRecurring</span><span class="sxs-lookup"><span data-stu-id="34a0a-107">dispidRecurring</span></span>  <br/> |
|<span data-ttu-id="34a0a-108">-Eigenschaft festgelegt:</span><span class="sxs-lookup"><span data-stu-id="34a0a-108">Property set:</span></span>  <br/> |<span data-ttu-id="34a0a-109">PSETID_Appointment</span><span class="sxs-lookup"><span data-stu-id="34a0a-109">PSETID_Appointment</span></span>  <br/> |
|<span data-ttu-id="34a0a-110">Long-ID (Abdeckung):</span><span class="sxs-lookup"><span data-stu-id="34a0a-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="34a0a-111">0x00008223</span><span class="sxs-lookup"><span data-stu-id="34a0a-111">0x00008223</span></span>  <br/> |
|<span data-ttu-id="34a0a-112">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="34a0a-112">Data type:</span></span>  <br/> |<span data-ttu-id="34a0a-113">PT_BOOLEAN</span><span class="sxs-lookup"><span data-stu-id="34a0a-113">PT_BOOLEAN</span></span>  <br/> |
|<span data-ttu-id="34a0a-114">Bereich:</span><span class="sxs-lookup"><span data-stu-id="34a0a-114">Area:</span></span>  <br/> |<span data-ttu-id="34a0a-115">Kalender</span><span class="sxs-lookup"><span data-stu-id="34a0a-115">Calendar</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="34a0a-116">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="34a0a-116">Remarks</span></span>

<span data-ttu-id="34a0a-117">Diese Eigenschaft ist TRUE, wenn der Termin einer Terminserie ist, und ist FALSE, wenn es nicht wiederholt wird.</span><span class="sxs-lookup"><span data-stu-id="34a0a-117">This property is TRUE if the appointment is a recurring appointment, and is FALSE if it is not recurring.</span></span>
  
<span data-ttu-id="34a0a-118">Diese Eigenschaft gibt an, ob das Objekt einer Terminserie darstellt.</span><span class="sxs-lookup"><span data-stu-id="34a0a-118">This property specifies whether or not the object represents a recurring series.</span></span> <span data-ttu-id="34a0a-119">Der Wert TRUE gibt an, dass das Objekt einer Terminserie darstellt.</span><span class="sxs-lookup"><span data-stu-id="34a0a-119">A value of TRUE indicates that the object represents a recurring series.</span></span> <span data-ttu-id="34a0a-120">Den Wert FALSE oder das fehlen diese Eigenschaft gibt an, dass das Objekt eine einzelne Instanz oder eine Ausnahme (einschließlich einer verwaisten Instanz) darstellt.</span><span class="sxs-lookup"><span data-stu-id="34a0a-120">A value of FALSE, or the absence of this property, indicates that the object represents either a single instance or an exception (including an orphan instance).</span></span> <span data-ttu-id="34a0a-121">Beachten Sie den Unterschied zwischen dieser Eigenschaft und die **LID_IS_RECURRING** ([PidLidIsRecurring](pidlidisrecurring-canonical-property.md))-Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="34a0a-121">Note the difference between this property and the **LID_IS_RECURRING** ([PidLidIsRecurring](pidlidisrecurring-canonical-property.md)) property.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="34a0a-122">Verwandte Ressourcen</span><span class="sxs-lookup"><span data-stu-id="34a0a-122">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="34a0a-123">Protokollspezifikationen</span><span class="sxs-lookup"><span data-stu-id="34a0a-123">Protocol specifications</span></span>

<span data-ttu-id="34a0a-124">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="34a0a-124">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="34a0a-125">Enthält Eigenschaftendefinitionen und Verweise auf Verwandte Exchange Server-Spezifikationen.</span><span class="sxs-lookup"><span data-stu-id="34a0a-125">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="34a0a-126">[[MS-OXOCAL]](http://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="34a0a-126">[[MS-OXOCAL]](http://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="34a0a-127">Gibt die Eigenschaften und Vorgänge für den Termin, einer Besprechungsanfrage und Antwortnachrichten.</span><span class="sxs-lookup"><span data-stu-id="34a0a-127">Specifies the properties and operations for appointment, meeting request, and response messages.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="34a0a-128">Header-Dateien</span><span class="sxs-lookup"><span data-stu-id="34a0a-128">Header files</span></span>

<span data-ttu-id="34a0a-129">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="34a0a-129">Mapidefs.h</span></span>
  
> <span data-ttu-id="34a0a-130">Enthält die Datentypdefinitionen.</span><span class="sxs-lookup"><span data-stu-id="34a0a-130">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="34a0a-131">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="34a0a-131">See also</span></span>



[<span data-ttu-id="34a0a-132">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="34a0a-132">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="34a0a-133">Kanonische MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="34a0a-133">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="34a0a-134">Zuordnen von kanonischen Eigenschaftennamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="34a0a-134">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="34a0a-135">Zuordnen von MAPI-Namen zu kanonische Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="34a0a-135">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

