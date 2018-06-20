---
title: Kanonische PidTagProcessed-Eigenschaft
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
ms.openlocfilehash: 0918f079769a70aa11e4f26551ec232308e5eef0
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19794810"
---
# <a name="pidtagprocessed-canonical-property"></a><span data-ttu-id="5141e-103">Kanonische PidTagProcessed-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="5141e-103">PidTagProcessed Canonical Property</span></span>

  
  
<span data-ttu-id="5141e-104">**Betrifft**: Outlook</span><span class="sxs-lookup"><span data-stu-id="5141e-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="5141e-105">Auf TRUE festgelegt, wenn die Besprechungsanfrage verarbeitet wurden.</span><span class="sxs-lookup"><span data-stu-id="5141e-105">Set to TRUE when the meeting request has been processed.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="5141e-106">Zugeordneten Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="5141e-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="5141e-107">PR_PROCESSED</span><span class="sxs-lookup"><span data-stu-id="5141e-107">PR_PROCESSED</span></span>  <br/> |
|<span data-ttu-id="5141e-108">Bezeichner:</span><span class="sxs-lookup"><span data-stu-id="5141e-108">Identifier:</span></span>  <br/> |<span data-ttu-id="5141e-109">0x7D01</span><span class="sxs-lookup"><span data-stu-id="5141e-109">0x7D01</span></span>  <br/> |
|<span data-ttu-id="5141e-110">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="5141e-110">Data type:</span></span>  <br/> |<span data-ttu-id="5141e-111">PT_BOOLEAN</span><span class="sxs-lookup"><span data-stu-id="5141e-111">PT_BOOLEAN</span></span>  <br/> |
|<span data-ttu-id="5141e-112">Bereich:</span><span class="sxs-lookup"><span data-stu-id="5141e-112">Area:</span></span>  <br/> |<span data-ttu-id="5141e-113">Kalender</span><span class="sxs-lookup"><span data-stu-id="5141e-113">Calendar</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="5141e-114">Hinweise</span><span class="sxs-lookup"><span data-stu-id="5141e-114">Remarks</span></span>

<span data-ttu-id="5141e-115">Diese Eigenschaft wird sichergestellt, dass Besprechungsanfragen einmal verarbeitet.</span><span class="sxs-lookup"><span data-stu-id="5141e-115">This property ensures that meeting requests get processed once.</span></span> <span data-ttu-id="5141e-116">Der Ersteller der Anforderung sollte diese Eigenschaft auf FALSE festgelegt, und der Empfänger sollte es auf TRUE festgelegt, nachdem die Anforderung im Kalender ist.</span><span class="sxs-lookup"><span data-stu-id="5141e-116">The creator of the request should set this property to FALSE and the receiver should set it to TRUE once the request is in the calendar.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="5141e-117">Verwandte Ressourcen</span><span class="sxs-lookup"><span data-stu-id="5141e-117">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="5141e-118">Protokollspezifikationen</span><span class="sxs-lookup"><span data-stu-id="5141e-118">Protocol specifications</span></span>

<span data-ttu-id="5141e-119">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="5141e-119">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="5141e-120">Bietet Verweise auf Verwandte Exchange Server-Spezifikationen.</span><span class="sxs-lookup"><span data-stu-id="5141e-120">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="5141e-121">[[MS-OXOCAL]](http://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="5141e-121">[[MS-OXOCAL]](http://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="5141e-122">Gibt die Eigenschaften und Vorgänge für den Termin, einer Besprechungsanfrage und Antwortnachrichten.</span><span class="sxs-lookup"><span data-stu-id="5141e-122">Specifies the properties and operations for appointment, meeting request, and response messages.</span></span>
    
<span data-ttu-id="5141e-123">[[MS-OXOTASK]](http://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="5141e-123">[[MS-OXOTASK]](http://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="5141e-124">Gibt die Eigenschaften und Operationen, die für Kontakt- und Objekte in der persönlichen Verteilerliste Liste zulässig sind.</span><span class="sxs-lookup"><span data-stu-id="5141e-124">Specifies the properties and operations that are permissible for contact and personal distribution list objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="5141e-125">Header-Dateien</span><span class="sxs-lookup"><span data-stu-id="5141e-125">Header files</span></span>

<span data-ttu-id="5141e-126">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="5141e-126">Mapidefs.h</span></span>
  
> <span data-ttu-id="5141e-127">Enthält die Datentypdefinitionen.</span><span class="sxs-lookup"><span data-stu-id="5141e-127">Provides data type definitions.</span></span>
    
<span data-ttu-id="5141e-128">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="5141e-128">Mapitags.h</span></span>
  
> <span data-ttu-id="5141e-129">Enthält Definitionen von Eigenschaften, die als zugeordneten Eigenschaften aufgelistet.</span><span class="sxs-lookup"><span data-stu-id="5141e-129">Contains definitions of properties listed as associated properties.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="5141e-130">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="5141e-130">See also</span></span>



[<span data-ttu-id="5141e-131">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="5141e-131">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="5141e-132">Kanonische MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="5141e-132">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="5141e-133">Zuordnen von kanonischen Eigenschaftennamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="5141e-133">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="5141e-134">Zuordnen von MAPI-Namen zu kanonische Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="5141e-134">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

