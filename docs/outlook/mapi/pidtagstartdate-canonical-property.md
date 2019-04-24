---
title: Kanonische Pidtagstartdate (-Eigenschaft
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagStartDate
api_type:
- COM
ms.assetid: 908c2d9f-53f4-4aa8-b309-2f3ac2dca5b5
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: fd799a3dc5ba91d388285f649cccfeec188b6143
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32278820"
---
# <a name="pidtagstartdate-canonical-property"></a><span data-ttu-id="b5b58-103">Kanonische Pidtagstartdate (-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="b5b58-103">PidTagStartDate Canonical Property</span></span>

  
  
<span data-ttu-id="b5b58-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="b5b58-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="b5b58-105">Enthält das Startdatum und die Startzeit eines Termins, der von einer Planungsanwendung verwaltet wird.</span><span class="sxs-lookup"><span data-stu-id="b5b58-105">Contains the starting date and time of an appointment as managed by a scheduling application.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="b5b58-106">Zugeordnete Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="b5b58-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="b5b58-107">PR_START_DATE</span><span class="sxs-lookup"><span data-stu-id="b5b58-107">PR_START_DATE</span></span>  <br/> |
|<span data-ttu-id="b5b58-108">Kennung:</span><span class="sxs-lookup"><span data-stu-id="b5b58-108">Identifier:</span></span>  <br/> |<span data-ttu-id="b5b58-109">0x0060</span><span class="sxs-lookup"><span data-stu-id="b5b58-109">0x0060</span></span>  <br/> |
|<span data-ttu-id="b5b58-110">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="b5b58-110">Data type:</span></span>  <br/> |<span data-ttu-id="b5b58-111">PT_SYSTIME</span><span class="sxs-lookup"><span data-stu-id="b5b58-111">PT_SYSTIME</span></span>  <br/> |
|<span data-ttu-id="b5b58-112">Bereich:</span><span class="sxs-lookup"><span data-stu-id="b5b58-112">Area:</span></span>  <br/> |<span data-ttu-id="b5b58-113">MAPI-Umschlag</span><span class="sxs-lookup"><span data-stu-id="b5b58-113">MAPI envelope</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="b5b58-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="b5b58-114">Remarks</span></span>

<span data-ttu-id="b5b58-115">Bei der Planung von Anwendungen sollten diese Eigenschaften und **PR_END_DATE** ([pidtagenddate (](pidtagenddate-canonical-property.md)) beim Senden von Besprechungsanfragen festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="b5b58-115">Scheduling applications should set both this property and **PR_END_DATE** ([PidTagEndDate](pidtagenddate-canonical-property.md)) properties when sending meeting requests.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="b5b58-116">Zugehörige Ressourcen</span><span class="sxs-lookup"><span data-stu-id="b5b58-116">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="b5b58-117">Protokollspezifikationen</span><span class="sxs-lookup"><span data-stu-id="b5b58-117">Protocol specifications</span></span>

<span data-ttu-id="b5b58-118">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="b5b58-118">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="b5b58-119">Enthält Verweise auf zugehörige Exchange Server-Protokollspezifikationen.</span><span class="sxs-lookup"><span data-stu-id="b5b58-119">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="b5b58-120">[[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="b5b58-120">[[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="b5b58-121">Gibt die Eigenschaften und Vorgänge für Termin-, Besprechungs-und Antwortnachrichten an.</span><span class="sxs-lookup"><span data-stu-id="b5b58-121">Specifies the properties and operations for appointment, meeting request, and response messages.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="b5b58-122">Header Dateien</span><span class="sxs-lookup"><span data-stu-id="b5b58-122">Header files</span></span>

<span data-ttu-id="b5b58-123">Mapidefs. h</span><span class="sxs-lookup"><span data-stu-id="b5b58-123">Mapidefs.h</span></span>
  
> <span data-ttu-id="b5b58-124">Stellt Datentypdefinitionen bereit.</span><span class="sxs-lookup"><span data-stu-id="b5b58-124">Provides data type definitions.</span></span>
    
<span data-ttu-id="b5b58-125">Mapitags. h</span><span class="sxs-lookup"><span data-stu-id="b5b58-125">Mapitags.h</span></span>
  
> <span data-ttu-id="b5b58-126">Enthält Definitionen von Eigenschaften, die als Alternative Namen aufgeführt sind.</span><span class="sxs-lookup"><span data-stu-id="b5b58-126">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="b5b58-127">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="b5b58-127">See also</span></span>



[<span data-ttu-id="b5b58-128">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="b5b58-128">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="b5b58-129">Kanonische MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="b5b58-129">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="b5b58-130">Zuordnen von kanonischen Eigenschaftennamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="b5b58-130">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="b5b58-131">Zuordnen von MAPI-Namen zu kanonischen Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="b5b58-131">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

