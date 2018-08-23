---
title: PidTagStartDate (kanonische Eigenschaft)
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
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 82d9060513814b5011e33ca00d849a75f9defbf6
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2018
ms.locfileid: "22577373"
---
# <a name="pidtagstartdate-canonical-property"></a><span data-ttu-id="43d08-103">PidTagStartDate (kanonische Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="43d08-103">PidTagStartDate Canonical Property</span></span>

  
  
<span data-ttu-id="43d08-104">**Betrifft**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="43d08-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="43d08-105">Enthält das Datum und die Uhrzeit eines Termins als durch eine Anwendung zur terminplanung verwaltet.</span><span class="sxs-lookup"><span data-stu-id="43d08-105">Contains the starting date and time of an appointment as managed by a scheduling application.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="43d08-106">Zugeordnete Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="43d08-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="43d08-107">PR_START_DATE</span><span class="sxs-lookup"><span data-stu-id="43d08-107">PR_START_DATE</span></span>  <br/> |
|<span data-ttu-id="43d08-108">Kennung:</span><span class="sxs-lookup"><span data-stu-id="43d08-108">Identifier:</span></span>  <br/> |<span data-ttu-id="43d08-109">0x0060</span><span class="sxs-lookup"><span data-stu-id="43d08-109">0x0060</span></span>  <br/> |
|<span data-ttu-id="43d08-110">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="43d08-110">Data type:</span></span>  <br/> |<span data-ttu-id="43d08-111">PT_SYSTIME</span><span class="sxs-lookup"><span data-stu-id="43d08-111">PT_SYSTIME</span></span>  <br/> |
|<span data-ttu-id="43d08-112">Bereich:</span><span class="sxs-lookup"><span data-stu-id="43d08-112">Area:</span></span>  <br/> |<span data-ttu-id="43d08-113">MAPI-Umschlag</span><span class="sxs-lookup"><span data-stu-id="43d08-113">MAPI envelope</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="43d08-114">HinwBemerkungeneise</span><span class="sxs-lookup"><span data-stu-id="43d08-114">Remarks</span></span>

<span data-ttu-id="43d08-115">Planen von Anwendungen sollte diese Eigenschaft und die Eigenschaften des **PR_END_DATE** ([PidTagEndDate](pidtagenddate-canonical-property.md)) festgelegt, wenn Senden von Besprechungsanfragen.</span><span class="sxs-lookup"><span data-stu-id="43d08-115">Scheduling applications should set both this property and **PR_END_DATE** ([PidTagEndDate](pidtagenddate-canonical-property.md)) properties when sending meeting requests.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="43d08-116">Verwandte Ressourcen</span><span class="sxs-lookup"><span data-stu-id="43d08-116">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="43d08-117">Protokollspezifikationen</span><span class="sxs-lookup"><span data-stu-id="43d08-117">Protocol specifications</span></span>

<span data-ttu-id="43d08-118">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="43d08-118">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="43d08-119">Bietet Verweise auf Verwandte Exchange Server-Spezifikationen.</span><span class="sxs-lookup"><span data-stu-id="43d08-119">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="43d08-120">[[MS-OXOCAL]](http://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="43d08-120">[[MS-OXOCAL]](http://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="43d08-121">Gibt die Eigenschaften und Vorgänge für den Termin, einer Besprechungsanfrage und Antwortnachrichten.</span><span class="sxs-lookup"><span data-stu-id="43d08-121">Specifies the properties and operations for appointment, meeting request, and response messages.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="43d08-122">Header-Dateien</span><span class="sxs-lookup"><span data-stu-id="43d08-122">Header files</span></span>

<span data-ttu-id="43d08-123">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="43d08-123">Mapidefs.h</span></span>
  
> <span data-ttu-id="43d08-124">Enthält die Datentypdefinitionen.</span><span class="sxs-lookup"><span data-stu-id="43d08-124">Provides data type definitions.</span></span>
    
<span data-ttu-id="43d08-125">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="43d08-125">Mapitags.h</span></span>
  
> <span data-ttu-id="43d08-126">Enthält Definitionen von Eigenschaften, die als Alternative Namen aufgelistet.</span><span class="sxs-lookup"><span data-stu-id="43d08-126">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="43d08-127">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="43d08-127">See also</span></span>



[<span data-ttu-id="43d08-128">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="43d08-128">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="43d08-129">Kanonische MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="43d08-129">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="43d08-130">Zuordnen von kanonischen Eigenschaftennamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="43d08-130">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="43d08-131">Zuordnen von MAPI-Namen zu kanonische Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="43d08-131">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

