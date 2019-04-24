---
title: Kanonische Pidlidisrecurring (-Eigenschaft
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
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: c920cd42a27c03ffcff63bbd2e0049ddb6f81158
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32315435"
---
# <a name="pidlidisrecurring-canonical-property"></a><span data-ttu-id="8672a-103">Kanonische Pidlidisrecurring (-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="8672a-103">PidLidIsRecurring Canonical Property</span></span>

  
  
<span data-ttu-id="8672a-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="8672a-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="8672a-105">Gibt an, ob das Objekt einer wiederkehrenden Reihe zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="8672a-105">Specifies whether or not the object is associated with a recurring series.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="8672a-106">Zugeordnete Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="8672a-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="8672a-107">LID_IS_RECURRING</span><span class="sxs-lookup"><span data-stu-id="8672a-107">LID_IS_RECURRING</span></span>  <br/> |
|<span data-ttu-id="8672a-108">Eigenschaftensatz:</span><span class="sxs-lookup"><span data-stu-id="8672a-108">Property set:</span></span>  <br/> |<span data-ttu-id="8672a-109">PSETID_Meeting</span><span class="sxs-lookup"><span data-stu-id="8672a-109">PSETID_Meeting</span></span>  <br/> |
|<span data-ttu-id="8672a-110">Long-ID (Deckel):</span><span class="sxs-lookup"><span data-stu-id="8672a-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="8672a-111">0x00000005</span><span class="sxs-lookup"><span data-stu-id="8672a-111">0x00000005</span></span>  <br/> |
|<span data-ttu-id="8672a-112">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="8672a-112">Data type:</span></span>  <br/> |<span data-ttu-id="8672a-113">PT_BOOLEAN</span><span class="sxs-lookup"><span data-stu-id="8672a-113">PT_BOOLEAN</span></span>  <br/> |
|<span data-ttu-id="8672a-114">Bereich:</span><span class="sxs-lookup"><span data-stu-id="8672a-114">Area:</span></span>  <br/> |<span data-ttu-id="8672a-115">Meetings</span><span class="sxs-lookup"><span data-stu-id="8672a-115">Meetings</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="8672a-116">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="8672a-116">Remarks</span></span>

<span data-ttu-id="8672a-117">Der Wert TRUE gibt an, dass das Objekt eine wiederkehrende Datenreihe oder eine Ausnahme (einschließlich einer verwaisten Instanz) darstellt.</span><span class="sxs-lookup"><span data-stu-id="8672a-117">A value of TRUE indicates that the object represents either a recurring series or an exception (including an orphan instance).</span></span> <span data-ttu-id="8672a-118">Der Wert FALSE oder das Fehlen dieser Eigenschaft gibt an, dass das Objekt eine einzelne Instanz darstellt.</span><span class="sxs-lookup"><span data-stu-id="8672a-118">A value of FALSE, or the absence of this property, indicates that the object represents a single instance.</span></span> <span data-ttu-id="8672a-119">Beachten Sie den Unterschied zwischen dieser Eigenschaft und der **PR_RECURRING** ([pidlidrecurring (](pidlidrecurring-canonical-property.md))-Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="8672a-119">Note the difference between this property and the **PR_RECURRING** ([PidLidRecurring](pidlidrecurring-canonical-property.md)) property.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="8672a-120">Zugehörige Ressourcen</span><span class="sxs-lookup"><span data-stu-id="8672a-120">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="8672a-121">Protokollspezifikationen</span><span class="sxs-lookup"><span data-stu-id="8672a-121">Protocol specifications</span></span>

<span data-ttu-id="8672a-122">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="8672a-122">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="8672a-123">Stellt Eigenschaftensatz Definitionen und Verweise auf zugehörige Exchange Server-Protokollspezifikationen bereit.</span><span class="sxs-lookup"><span data-stu-id="8672a-123">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="8672a-124">[[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="8672a-124">[[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="8672a-125">Gibt die Eigenschaften und Vorgänge für Termin-, Besprechungs-und Antwortnachrichten an.</span><span class="sxs-lookup"><span data-stu-id="8672a-125">Specifies the properties and operations for appointment, meeting request, and response messages.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="8672a-126">Header Dateien</span><span class="sxs-lookup"><span data-stu-id="8672a-126">Header files</span></span>

<span data-ttu-id="8672a-127">Mapidefs. h</span><span class="sxs-lookup"><span data-stu-id="8672a-127">Mapidefs.h</span></span>
  
> <span data-ttu-id="8672a-128">Stellt Datentypdefinitionen bereit.</span><span class="sxs-lookup"><span data-stu-id="8672a-128">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="8672a-129">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="8672a-129">See also</span></span>



[<span data-ttu-id="8672a-130">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="8672a-130">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="8672a-131">Kanonische MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="8672a-131">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="8672a-132">Zuordnen von kanonischen Eigenschaftennamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="8672a-132">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="8672a-133">Zuordnen von MAPI-Namen zu kanonischen Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="8672a-133">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

