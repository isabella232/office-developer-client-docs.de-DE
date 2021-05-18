---
title: PidLidIsException (kanonische Eigenschaft)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidIsException
api_type:
- COM
ms.assetid: 802321fb-4261-4c3e-9de3-8b4f490dae13
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 18dfa8a5936902afe0272274f7a48d01b28f94f3
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32315449"
---
# <a name="pidlidisexception-canonical-property"></a><span data-ttu-id="76ff5-103">PidLidIsException (kanonische Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="76ff5-103">PidLidIsException Canonical Property</span></span>

  
  
<span data-ttu-id="76ff5-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="76ff5-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="76ff5-105">Gibt an, dass das Objekt, das eine Ausnahme darstellt (einschließlich einer verwaisten Instanz).</span><span class="sxs-lookup"><span data-stu-id="76ff5-105">Indicates that the object that represents an exception (including an orphan instance).</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="76ff5-106">Zugeordnete Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="76ff5-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="76ff5-107">LID_IS_EXCEPTION</span><span class="sxs-lookup"><span data-stu-id="76ff5-107">LID_IS_EXCEPTION</span></span>  <br/> |
|<span data-ttu-id="76ff5-108">Eigenschaftensatz:</span><span class="sxs-lookup"><span data-stu-id="76ff5-108">Property set:</span></span>  <br/> |<span data-ttu-id="76ff5-109">PSETID_Meeting</span><span class="sxs-lookup"><span data-stu-id="76ff5-109">PSETID_Meeting</span></span>  <br/> |
|<span data-ttu-id="76ff5-110">Lange ID (LID):</span><span class="sxs-lookup"><span data-stu-id="76ff5-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="76ff5-111">0x0000000A</span><span class="sxs-lookup"><span data-stu-id="76ff5-111">0x0000000A</span></span>  <br/> |
|<span data-ttu-id="76ff5-112">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="76ff5-112">Data type:</span></span>  <br/> |<span data-ttu-id="76ff5-113">PT_BOOLEAN</span><span class="sxs-lookup"><span data-stu-id="76ff5-113">PT_BOOLEAN</span></span>  <br/> |
|<span data-ttu-id="76ff5-114">Bereich:</span><span class="sxs-lookup"><span data-stu-id="76ff5-114">Area:</span></span>  <br/> |<span data-ttu-id="76ff5-115">Besprechungen</span><span class="sxs-lookup"><span data-stu-id="76ff5-115">Meetings</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="76ff5-116">Hinweise</span><span class="sxs-lookup"><span data-stu-id="76ff5-116">Remarks</span></span>

<span data-ttu-id="76ff5-117">Der Wert FALSE gibt an, dass das Objekt, das eine Serienserie oder eine einzelne Instanz darstellt.</span><span class="sxs-lookup"><span data-stu-id="76ff5-117">A value of FALSE indicates that the object that represents a recurring series or a single instance.</span></span> <span data-ttu-id="76ff5-118">Das Fehlen dieser Eigenschaft für jedes Objekt gibt den Wert FALSE an, mit Ausnahme der eingebetteten Ausnahmenachricht, die den Wert TRUE annimmt.</span><span class="sxs-lookup"><span data-stu-id="76ff5-118">The absence of this property for any object indicates a value of FALSE except for the exception embedded message, which assumes a value of TRUE.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="76ff5-119">Verwandte Ressourcen</span><span class="sxs-lookup"><span data-stu-id="76ff5-119">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="76ff5-120">Protokollspezifikationen</span><span class="sxs-lookup"><span data-stu-id="76ff5-120">Protocol specifications</span></span>

<span data-ttu-id="76ff5-121">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="76ff5-121">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="76ff5-122">Stellt Eigenschaftensatzdefinitionen und Verweise auf verwandte Exchange Server zur Verfügung.</span><span class="sxs-lookup"><span data-stu-id="76ff5-122">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="76ff5-123">[[MS-OXOCAL] ](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="76ff5-123">[[MS-OXOCAL] ](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="76ff5-124">Gibt die Eigenschaften und Vorgänge für Termin-, Besprechungs- und Antwortnachrichten an.</span><span class="sxs-lookup"><span data-stu-id="76ff5-124">Specifies the properties and operations for appointment, meeting request, and response messages.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="76ff5-125">Headerdateien</span><span class="sxs-lookup"><span data-stu-id="76ff5-125">Header files</span></span>

<span data-ttu-id="76ff5-126">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="76ff5-126">Mapidefs.h</span></span>
  
> <span data-ttu-id="76ff5-127">Bietet Datentypdefinitionen.</span><span class="sxs-lookup"><span data-stu-id="76ff5-127">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="76ff5-128">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="76ff5-128">See also</span></span>



[<span data-ttu-id="76ff5-129">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="76ff5-129">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="76ff5-130">KANONISCHE EIGENSCHAFTEN VON MAPI</span><span class="sxs-lookup"><span data-stu-id="76ff5-130">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="76ff5-131">Zuordnen kanonischer Eigenschaftsnamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="76ff5-131">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="76ff5-132">Zuordnen von MAPI-Namen zu kanonischen Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="76ff5-132">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

