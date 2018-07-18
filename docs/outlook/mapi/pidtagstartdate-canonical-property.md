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
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: 14a077dfdb0f0781ab0d9f085c758c7a7d6285af
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19795201"
---
# <a name="pidtagstartdate-canonical-property"></a><span data-ttu-id="35873-103">PidTagStartDate (kanonische Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="35873-103">PidTagStartDate Canonical Property</span></span>

  
  
<span data-ttu-id="35873-104">**Betrifft**: Outlook</span><span class="sxs-lookup"><span data-stu-id="35873-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="35873-105">Enthält das Datum und die Uhrzeit eines Termins als durch eine Anwendung zur terminplanung verwaltet.</span><span class="sxs-lookup"><span data-stu-id="35873-105">Contains the starting date and time of an appointment as managed by a scheduling application.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="35873-106">Zugeordneten Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="35873-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="35873-107">PR_START_DATE</span><span class="sxs-lookup"><span data-stu-id="35873-107">PR_START_DATE</span></span>  <br/> |
|<span data-ttu-id="35873-108">Bezeichner:</span><span class="sxs-lookup"><span data-stu-id="35873-108">Identifier:</span></span>  <br/> |<span data-ttu-id="35873-109">0x0060</span><span class="sxs-lookup"><span data-stu-id="35873-109">0x0060</span></span>  <br/> |
|<span data-ttu-id="35873-110">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="35873-110">Data type:</span></span>  <br/> |<span data-ttu-id="35873-111">PT_SYSTIME</span><span class="sxs-lookup"><span data-stu-id="35873-111">PT_SYSTIME</span></span>  <br/> |
|<span data-ttu-id="35873-112">Bereich:</span><span class="sxs-lookup"><span data-stu-id="35873-112">Area:</span></span>  <br/> |<span data-ttu-id="35873-113">MAPI-Umschlag</span><span class="sxs-lookup"><span data-stu-id="35873-113">MAPI envelope</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="35873-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="35873-114">Remarks</span></span>

<span data-ttu-id="35873-115">Planen von Anwendungen sollte diese Eigenschaft und die Eigenschaften des **PR_END_DATE** ([PidTagEndDate](pidtagenddate-canonical-property.md)) festgelegt, wenn Senden von Besprechungsanfragen.</span><span class="sxs-lookup"><span data-stu-id="35873-115">Scheduling applications should set both this property and **PR_END_DATE** ([PidTagEndDate](pidtagenddate-canonical-property.md)) properties when sending meeting requests.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="35873-116">Verwandte Ressourcen</span><span class="sxs-lookup"><span data-stu-id="35873-116">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="35873-117">Protokollspezifikationen</span><span class="sxs-lookup"><span data-stu-id="35873-117">Protocol specifications</span></span>

<span data-ttu-id="35873-118">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="35873-118">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="35873-119">Bietet Verweise auf Verwandte Exchange Server-Spezifikationen.</span><span class="sxs-lookup"><span data-stu-id="35873-119">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="35873-120">[[MS-OXOCAL]](http://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="35873-120">[[MS-OXOCAL]](http://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="35873-121">Gibt die Eigenschaften und Vorgänge für den Termin, einer Besprechungsanfrage und Antwortnachrichten.</span><span class="sxs-lookup"><span data-stu-id="35873-121">Specifies the properties and operations for appointment, meeting request, and response messages.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="35873-122">Header-Dateien</span><span class="sxs-lookup"><span data-stu-id="35873-122">Header files</span></span>

<span data-ttu-id="35873-123">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="35873-123">Mapidefs.h</span></span>
  
> <span data-ttu-id="35873-124">Enthält die Datentypdefinitionen.</span><span class="sxs-lookup"><span data-stu-id="35873-124">Provides data type definitions.</span></span>
    
<span data-ttu-id="35873-125">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="35873-125">Mapitags.h</span></span>
  
> <span data-ttu-id="35873-126">Enthält Definitionen von Eigenschaften, die als Alternative Namen aufgelistet.</span><span class="sxs-lookup"><span data-stu-id="35873-126">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="35873-127">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="35873-127">See also</span></span>



[<span data-ttu-id="35873-128">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="35873-128">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="35873-129">Kanonische MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="35873-129">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="35873-130">Zuordnen von kanonischen Eigenschaftennamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="35873-130">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="35873-131">Zuordnen von MAPI-Namen zu kanonische Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="35873-131">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

