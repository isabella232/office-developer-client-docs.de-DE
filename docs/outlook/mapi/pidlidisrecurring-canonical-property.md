---
title: PidLidIsRecurring (kanonische Eigenschaft)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidIsRecurring
api_type:
- COM
ms.assetid: 1f8ecc22-badc-4278-a3c6-fcd398f5bf24
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: c920cd42a27c03ffcff63bbd2e0049ddb6f81158
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32315435"
---
# <a name="pidlidisrecurring-canonical-property"></a><span data-ttu-id="86f0b-103">PidLidIsRecurring (kanonische Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="86f0b-103">PidLidIsRecurring Canonical Property</span></span>

  
  
<span data-ttu-id="86f0b-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="86f0b-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="86f0b-105">Gibt an, ob das Objekt einer Serienserie zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="86f0b-105">Specifies whether or not the object is associated with a recurring series.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="86f0b-106">Zugeordnete Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="86f0b-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="86f0b-107">LID_IS_RECURRING</span><span class="sxs-lookup"><span data-stu-id="86f0b-107">LID_IS_RECURRING</span></span>  <br/> |
|<span data-ttu-id="86f0b-108">Eigenschaftensatz:</span><span class="sxs-lookup"><span data-stu-id="86f0b-108">Property set:</span></span>  <br/> |<span data-ttu-id="86f0b-109">PSETID_Meeting</span><span class="sxs-lookup"><span data-stu-id="86f0b-109">PSETID_Meeting</span></span>  <br/> |
|<span data-ttu-id="86f0b-110">Lange ID (LID):</span><span class="sxs-lookup"><span data-stu-id="86f0b-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="86f0b-111">0x00000005</span><span class="sxs-lookup"><span data-stu-id="86f0b-111">0x00000005</span></span>  <br/> |
|<span data-ttu-id="86f0b-112">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="86f0b-112">Data type:</span></span>  <br/> |<span data-ttu-id="86f0b-113">PT_BOOLEAN</span><span class="sxs-lookup"><span data-stu-id="86f0b-113">PT_BOOLEAN</span></span>  <br/> |
|<span data-ttu-id="86f0b-114">Bereich:</span><span class="sxs-lookup"><span data-stu-id="86f0b-114">Area:</span></span>  <br/> |<span data-ttu-id="86f0b-115">Besprechungen</span><span class="sxs-lookup"><span data-stu-id="86f0b-115">Meetings</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="86f0b-116">Hinweise</span><span class="sxs-lookup"><span data-stu-id="86f0b-116">Remarks</span></span>

<span data-ttu-id="86f0b-117">Der Wert TRUE gibt an, dass das Objekt entweder eine Serienserie oder eine Ausnahme darstellt (einschließlich einer verwaisten Instanz).</span><span class="sxs-lookup"><span data-stu-id="86f0b-117">A value of TRUE indicates that the object represents either a recurring series or an exception (including an orphan instance).</span></span> <span data-ttu-id="86f0b-118">Der Wert FALSE oder das Fehlen dieser Eigenschaft gibt an, dass das Objekt eine einzelne Instanz darstellt.</span><span class="sxs-lookup"><span data-stu-id="86f0b-118">A value of FALSE, or the absence of this property, indicates that the object represents a single instance.</span></span> <span data-ttu-id="86f0b-119">Beachten Sie den Unterschied zwischen dieser Eigenschaft und **der PR_RECURRING** ([PidLidRecurring](pidlidrecurring-canonical-property.md)) -Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="86f0b-119">Note the difference between this property and the **PR_RECURRING** ([PidLidRecurring](pidlidrecurring-canonical-property.md)) property.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="86f0b-120">Verwandte Ressourcen</span><span class="sxs-lookup"><span data-stu-id="86f0b-120">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="86f0b-121">Protokollspezifikationen</span><span class="sxs-lookup"><span data-stu-id="86f0b-121">Protocol specifications</span></span>

<span data-ttu-id="86f0b-122">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="86f0b-122">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="86f0b-123">Stellt Eigenschaftensatzdefinitionen und Verweise auf verwandte Exchange Server zur Verfügung.</span><span class="sxs-lookup"><span data-stu-id="86f0b-123">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="86f0b-124">[[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="86f0b-124">[[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="86f0b-125">Gibt die Eigenschaften und Vorgänge für Termin-, Besprechungs- und Antwortnachrichten an.</span><span class="sxs-lookup"><span data-stu-id="86f0b-125">Specifies the properties and operations for appointment, meeting request, and response messages.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="86f0b-126">Headerdateien</span><span class="sxs-lookup"><span data-stu-id="86f0b-126">Header files</span></span>

<span data-ttu-id="86f0b-127">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="86f0b-127">Mapidefs.h</span></span>
  
> <span data-ttu-id="86f0b-128">Bietet Datentypdefinitionen.</span><span class="sxs-lookup"><span data-stu-id="86f0b-128">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="86f0b-129">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="86f0b-129">See also</span></span>



[<span data-ttu-id="86f0b-130">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="86f0b-130">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="86f0b-131">KANONISCHE EIGENSCHAFTEN VON MAPI</span><span class="sxs-lookup"><span data-stu-id="86f0b-131">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="86f0b-132">Zuordnen kanonischer Eigenschaftsnamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="86f0b-132">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="86f0b-133">Zuordnen von MAPI-Namen zu kanonischen Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="86f0b-133">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

