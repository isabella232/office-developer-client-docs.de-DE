---
title: PidTagEndDate (kanonische Eigenschaft)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagEndDate
api_type:
- HeaderDef
ms.assetid: d7ec5c79-1287-4364-b5e5-5d1d6f0ea0f1
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 2688e1764b6e4e31a47aeee306987caa66c709a6
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/04/2018
ms.locfileid: "25382715"
---
# <a name="pidtagenddate-canonical-property"></a><span data-ttu-id="81f5d-103">PidTagEndDate (kanonische Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="81f5d-103">PidTagEndDate Canonical Property</span></span>

  
  
<span data-ttu-id="81f5d-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="81f5d-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="81f5d-105">Enthält das Enddatum und die Uhrzeit eines Termins als durch eine Anwendung zur terminplanung verwaltet.</span><span class="sxs-lookup"><span data-stu-id="81f5d-105">Contains the ending date and time of an appointment as managed by a scheduling application.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="81f5d-106">Zugeordnete Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="81f5d-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="81f5d-107">PR_END_DATE</span><span class="sxs-lookup"><span data-stu-id="81f5d-107">PR_END_DATE</span></span>  <br/> |
|<span data-ttu-id="81f5d-108">Kennung:</span><span class="sxs-lookup"><span data-stu-id="81f5d-108">Identifier:</span></span>  <br/> |<span data-ttu-id="81f5d-109">0x0061</span><span class="sxs-lookup"><span data-stu-id="81f5d-109">0x0061</span></span>  <br/> |
|<span data-ttu-id="81f5d-110">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="81f5d-110">Data type:</span></span>  <br/> |<span data-ttu-id="81f5d-111">PT_SYSTIME</span><span class="sxs-lookup"><span data-stu-id="81f5d-111">PT_SYSTIME</span></span>  <br/> |
|<span data-ttu-id="81f5d-112">Bereich:</span><span class="sxs-lookup"><span data-stu-id="81f5d-112">Area:</span></span>  <br/> |<span data-ttu-id="81f5d-113">MAPI-Umschlag</span><span class="sxs-lookup"><span data-stu-id="81f5d-113">MAPI envelope</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="81f5d-114">Hinweise</span><span class="sxs-lookup"><span data-stu-id="81f5d-114">Remarks</span></span>

<span data-ttu-id="81f5d-115">Planen von Anwendungen sollte die **PR_START_DATE** ([PidTagStartDate](pidtagstartdate-canonical-property.md)) und diese Eigenschaft festgelegt, wenn Senden von Besprechungsanfragen.</span><span class="sxs-lookup"><span data-stu-id="81f5d-115">Scheduling applications should set both the **PR_START_DATE** ([PidTagStartDate](pidtagstartdate-canonical-property.md)) and this property when sending meeting requests.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="81f5d-116">Verwandte Ressourcen</span><span class="sxs-lookup"><span data-stu-id="81f5d-116">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="81f5d-117">Protokollspezifikationen</span><span class="sxs-lookup"><span data-stu-id="81f5d-117">Protocol specifications</span></span>

<span data-ttu-id="81f5d-118">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="81f5d-118">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="81f5d-119">Bietet Verweise auf Verwandte Exchange Server-Spezifikationen.</span><span class="sxs-lookup"><span data-stu-id="81f5d-119">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="81f5d-120">[[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="81f5d-120">[[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="81f5d-121">Gibt die Eigenschaften und Vorgänge für den Termin, einer Besprechungsanfrage und Antwortnachrichten.</span><span class="sxs-lookup"><span data-stu-id="81f5d-121">Specifies the properties and operations for appointment, meeting request, and response messages.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="81f5d-122">Header-Dateien</span><span class="sxs-lookup"><span data-stu-id="81f5d-122">Header files</span></span>

<span data-ttu-id="81f5d-123">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="81f5d-123">Mapidefs.h</span></span>
  
> <span data-ttu-id="81f5d-124">Enthält die Datentypdefinitionen.</span><span class="sxs-lookup"><span data-stu-id="81f5d-124">Provides data type definitions.</span></span>
    
<span data-ttu-id="81f5d-125">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="81f5d-125">Mapitags.h</span></span>
  
> <span data-ttu-id="81f5d-126">Enthält Definitionen von Eigenschaften, die als Alternative Namen aufgelistet.</span><span class="sxs-lookup"><span data-stu-id="81f5d-126">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="81f5d-127">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="81f5d-127">See also</span></span>



[<span data-ttu-id="81f5d-128">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="81f5d-128">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="81f5d-129">Kanonische MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="81f5d-129">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="81f5d-130">Zuordnen von kanonischen Eigenschaftennamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="81f5d-130">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="81f5d-131">Zuordnen von MAPI-Namen zu kanonische Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="81f5d-131">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

