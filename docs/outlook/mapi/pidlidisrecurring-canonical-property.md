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
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/04/2018
ms.locfileid: "25390849"
---
# <a name="pidlidisrecurring-canonical-property"></a><span data-ttu-id="7207a-103">PidLidIsRecurring (kanonische Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="7207a-103">PidLidIsRecurring Canonical Property</span></span>

  
  
<span data-ttu-id="7207a-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="7207a-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="7207a-105">Gibt an, ob das Objekt eine Terminserie zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="7207a-105">Specifies whether or not the object is associated with a recurring series.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="7207a-106">Zugeordnete Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="7207a-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="7207a-107">LID_IS_RECURRING</span><span class="sxs-lookup"><span data-stu-id="7207a-107">LID_IS_RECURRING</span></span>  <br/> |
|<span data-ttu-id="7207a-108">-Eigenschaft festgelegt:</span><span class="sxs-lookup"><span data-stu-id="7207a-108">Property set:</span></span>  <br/> |<span data-ttu-id="7207a-109">PSETID_Meeting</span><span class="sxs-lookup"><span data-stu-id="7207a-109">PSETID_Meeting</span></span>  <br/> |
|<span data-ttu-id="7207a-110">Long-ID (Abdeckung):</span><span class="sxs-lookup"><span data-stu-id="7207a-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="7207a-111">0 x 00000005</span><span class="sxs-lookup"><span data-stu-id="7207a-111">0x00000005</span></span>  <br/> |
|<span data-ttu-id="7207a-112">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="7207a-112">Data type:</span></span>  <br/> |<span data-ttu-id="7207a-113">PT_BOOLEAN</span><span class="sxs-lookup"><span data-stu-id="7207a-113">PT_BOOLEAN</span></span>  <br/> |
|<span data-ttu-id="7207a-114">Bereich:</span><span class="sxs-lookup"><span data-stu-id="7207a-114">Area:</span></span>  <br/> |<span data-ttu-id="7207a-115">Besprechungen</span><span class="sxs-lookup"><span data-stu-id="7207a-115">Meetings</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="7207a-116">Hinweise</span><span class="sxs-lookup"><span data-stu-id="7207a-116">Remarks</span></span>

<span data-ttu-id="7207a-117">Der Wert TRUE gibt an, dass das Objekt eine Terminserie oder eine Ausnahme (einschließlich einer verwaisten Instanz) darstellt.</span><span class="sxs-lookup"><span data-stu-id="7207a-117">A value of TRUE indicates that the object represents either a recurring series or an exception (including an orphan instance).</span></span> <span data-ttu-id="7207a-118">Den Wert FALSE oder das fehlen diese Eigenschaft gibt an, dass das Objekt eine einzelne Instanz darstellt.</span><span class="sxs-lookup"><span data-stu-id="7207a-118">A value of FALSE, or the absence of this property, indicates that the object represents a single instance.</span></span> <span data-ttu-id="7207a-119">Beachten Sie den Unterschied zwischen dieser Eigenschaft und die **PR_RECURRING** ([PidLidRecurring](pidlidrecurring-canonical-property.md))-Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="7207a-119">Note the difference between this property and the **PR_RECURRING** ([PidLidRecurring](pidlidrecurring-canonical-property.md)) property.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="7207a-120">Verwandte Ressourcen</span><span class="sxs-lookup"><span data-stu-id="7207a-120">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="7207a-121">Protokollspezifikationen</span><span class="sxs-lookup"><span data-stu-id="7207a-121">Protocol specifications</span></span>

<span data-ttu-id="7207a-122">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="7207a-122">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="7207a-123">Enthält Eigenschaftendefinitionen und Verweise auf Verwandte Exchange Server-Spezifikationen.</span><span class="sxs-lookup"><span data-stu-id="7207a-123">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="7207a-124">[[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="7207a-124">[[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="7207a-125">Gibt die Eigenschaften und Vorgänge für den Termin, einer Besprechungsanfrage und Antwortnachrichten.</span><span class="sxs-lookup"><span data-stu-id="7207a-125">Specifies the properties and operations for appointment, meeting request, and response messages.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="7207a-126">Header-Dateien</span><span class="sxs-lookup"><span data-stu-id="7207a-126">Header files</span></span>

<span data-ttu-id="7207a-127">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="7207a-127">Mapidefs.h</span></span>
  
> <span data-ttu-id="7207a-128">Enthält die Datentypdefinitionen.</span><span class="sxs-lookup"><span data-stu-id="7207a-128">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="7207a-129">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="7207a-129">See also</span></span>



[<span data-ttu-id="7207a-130">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="7207a-130">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="7207a-131">Kanonische MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="7207a-131">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="7207a-132">Zuordnen von kanonischen Eigenschaftennamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="7207a-132">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="7207a-133">Zuordnen von MAPI-Namen zu kanonische Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="7207a-133">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

