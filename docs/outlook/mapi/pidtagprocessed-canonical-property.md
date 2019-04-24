---
title: Kanonische Pidtagprocessed (-Eigenschaft
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagProcessed
api_type:
- COM
ms.assetid: 44884f60-7e36-45b2-9712-4f9821a0dc1f
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: 5d84e9cb693cbe732295ee1891b4219450eb09ae
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32351436"
---
# <a name="pidtagprocessed-canonical-property"></a><span data-ttu-id="944b6-103">Kanonische Pidtagprocessed (-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="944b6-103">PidTagProcessed Canonical Property</span></span>

  
  
<span data-ttu-id="944b6-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="944b6-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="944b6-105">Wird auf TRUE festgelegt, wenn die Besprechungsanfrage verarbeitet wurde.</span><span class="sxs-lookup"><span data-stu-id="944b6-105">Set to TRUE when the meeting request has been processed.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="944b6-106">Zugeordnete Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="944b6-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="944b6-107">PR_PROCESSED</span><span class="sxs-lookup"><span data-stu-id="944b6-107">PR_PROCESSED</span></span>  <br/> |
|<span data-ttu-id="944b6-108">Kennung:</span><span class="sxs-lookup"><span data-stu-id="944b6-108">Identifier:</span></span>  <br/> |<span data-ttu-id="944b6-109">0x7D01</span><span class="sxs-lookup"><span data-stu-id="944b6-109">0x7D01</span></span>  <br/> |
|<span data-ttu-id="944b6-110">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="944b6-110">Data type:</span></span>  <br/> |<span data-ttu-id="944b6-111">PT_BOOLEAN</span><span class="sxs-lookup"><span data-stu-id="944b6-111">PT_BOOLEAN</span></span>  <br/> |
|<span data-ttu-id="944b6-112">Bereich:</span><span class="sxs-lookup"><span data-stu-id="944b6-112">Area:</span></span>  <br/> |<span data-ttu-id="944b6-113">Kalender</span><span class="sxs-lookup"><span data-stu-id="944b6-113">Calendar</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="944b6-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="944b6-114">Remarks</span></span>

<span data-ttu-id="944b6-115">Diese Eigenschaft stellt sicher, dass Besprechungsanfragen einmal verarbeitet werden.</span><span class="sxs-lookup"><span data-stu-id="944b6-115">This property ensures that meeting requests get processed once.</span></span> <span data-ttu-id="944b6-116">Der Ersteller der Anforderung sollte diese Eigenschaft auf FALSE festlegen, und der Empfänger sollte ihn auf TRUE festlegen, wenn sich die Anforderung im Kalender befindet.</span><span class="sxs-lookup"><span data-stu-id="944b6-116">The creator of the request should set this property to FALSE and the receiver should set it to TRUE once the request is in the calendar.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="944b6-117">Zugehörige Ressourcen</span><span class="sxs-lookup"><span data-stu-id="944b6-117">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="944b6-118">Protokollspezifikationen</span><span class="sxs-lookup"><span data-stu-id="944b6-118">Protocol specifications</span></span>

<span data-ttu-id="944b6-119">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="944b6-119">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="944b6-120">Enthält Verweise auf zugehörige Exchange Server-Protokollspezifikationen.</span><span class="sxs-lookup"><span data-stu-id="944b6-120">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="944b6-121">[[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="944b6-121">[[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="944b6-122">Gibt die Eigenschaften und Vorgänge für Termin-, Besprechungs-und Antwortnachrichten an.</span><span class="sxs-lookup"><span data-stu-id="944b6-122">Specifies the properties and operations for appointment, meeting request, and response messages.</span></span>
    
<span data-ttu-id="944b6-123">[[MS-OXOTASK]](https://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="944b6-123">[[MS-OXOTASK]](https://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="944b6-124">Gibt die Eigenschaften und Vorgänge an, die für Kontakt-und persönliche Verteilerlistenobjekte zulässig sind.</span><span class="sxs-lookup"><span data-stu-id="944b6-124">Specifies the properties and operations that are permissible for contact and personal distribution list objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="944b6-125">Header Dateien</span><span class="sxs-lookup"><span data-stu-id="944b6-125">Header files</span></span>

<span data-ttu-id="944b6-126">Mapidefs. h</span><span class="sxs-lookup"><span data-stu-id="944b6-126">Mapidefs.h</span></span>
  
> <span data-ttu-id="944b6-127">Stellt Datentypdefinitionen bereit.</span><span class="sxs-lookup"><span data-stu-id="944b6-127">Provides data type definitions.</span></span>
    
<span data-ttu-id="944b6-128">Mapitags. h</span><span class="sxs-lookup"><span data-stu-id="944b6-128">Mapitags.h</span></span>
  
> <span data-ttu-id="944b6-129">Enthält Definitionen von Eigenschaften, die als zugeordnete Eigenschaften aufgelistet sind.</span><span class="sxs-lookup"><span data-stu-id="944b6-129">Contains definitions of properties listed as associated properties.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="944b6-130">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="944b6-130">See also</span></span>



[<span data-ttu-id="944b6-131">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="944b6-131">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="944b6-132">Kanonische MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="944b6-132">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="944b6-133">Zuordnen von kanonischen Eigenschaftennamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="944b6-133">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="944b6-134">Zuordnen von MAPI-Namen zu kanonischen Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="944b6-134">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

