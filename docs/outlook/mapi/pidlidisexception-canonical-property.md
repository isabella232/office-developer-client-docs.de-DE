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
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/04/2018
ms.locfileid: "25386250"
---
# <a name="pidlidisexception-canonical-property"></a><span data-ttu-id="77dd7-103">PidLidIsException (kanonische Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="77dd7-103">PidLidIsException Canonical Property</span></span>

  
  
<span data-ttu-id="77dd7-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="77dd7-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="77dd7-105">Gibt an, dass das Objekt, das eine Ausnahme (einschließlich einer verwaisten Instanz) darstellt.</span><span class="sxs-lookup"><span data-stu-id="77dd7-105">Indicates that the object that represents an exception (including an orphan instance).</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="77dd7-106">Zugeordnete Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="77dd7-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="77dd7-107">LID_IS_EXCEPTION</span><span class="sxs-lookup"><span data-stu-id="77dd7-107">LID_IS_EXCEPTION</span></span>  <br/> |
|<span data-ttu-id="77dd7-108">-Eigenschaft festgelegt:</span><span class="sxs-lookup"><span data-stu-id="77dd7-108">Property set:</span></span>  <br/> |<span data-ttu-id="77dd7-109">PSETID_Meeting</span><span class="sxs-lookup"><span data-stu-id="77dd7-109">PSETID_Meeting</span></span>  <br/> |
|<span data-ttu-id="77dd7-110">Long-ID (Abdeckung):</span><span class="sxs-lookup"><span data-stu-id="77dd7-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="77dd7-111">0x0000000A</span><span class="sxs-lookup"><span data-stu-id="77dd7-111">0x0000000A</span></span>  <br/> |
|<span data-ttu-id="77dd7-112">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="77dd7-112">Data type:</span></span>  <br/> |<span data-ttu-id="77dd7-113">PT_BOOLEAN</span><span class="sxs-lookup"><span data-stu-id="77dd7-113">PT_BOOLEAN</span></span>  <br/> |
|<span data-ttu-id="77dd7-114">Bereich:</span><span class="sxs-lookup"><span data-stu-id="77dd7-114">Area:</span></span>  <br/> |<span data-ttu-id="77dd7-115">Besprechungen</span><span class="sxs-lookup"><span data-stu-id="77dd7-115">Meetings</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="77dd7-116">Hinweise</span><span class="sxs-lookup"><span data-stu-id="77dd7-116">Remarks</span></span>

<span data-ttu-id="77dd7-117">Gibt der Wert FALSE an, dass das Objekt, das eine Terminserie oder eine einzelne Instanz darstellt.</span><span class="sxs-lookup"><span data-stu-id="77dd7-117">A value of FALSE indicates that the object that represents a recurring series or a single instance.</span></span> <span data-ttu-id="77dd7-118">Das Fehlen dieser Eigenschaft für jedes Objekt gilt gibt einen Wert false mit Ausnahme der Ausnahme eingebettete Nachricht, die Wert TRUE wird davon ausgegangen.</span><span class="sxs-lookup"><span data-stu-id="77dd7-118">The absence of this property for any object indicates a value of FALSE except for the exception embedded message, which assumes a value of TRUE.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="77dd7-119">Verwandte Ressourcen</span><span class="sxs-lookup"><span data-stu-id="77dd7-119">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="77dd7-120">Protokollspezifikationen</span><span class="sxs-lookup"><span data-stu-id="77dd7-120">Protocol specifications</span></span>

<span data-ttu-id="77dd7-121">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="77dd7-121">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="77dd7-122">Enthält Eigenschaftendefinitionen und Verweise auf Verwandte Exchange Server-Spezifikationen.</span><span class="sxs-lookup"><span data-stu-id="77dd7-122">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="77dd7-123">[[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="77dd7-123">[[MS-OXOCAL] ](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="77dd7-124">Gibt die Eigenschaften und Vorgänge für den Termin, einer Besprechungsanfrage und Antwortnachrichten.</span><span class="sxs-lookup"><span data-stu-id="77dd7-124">Specifies the properties and operations for appointment, meeting request, and response messages.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="77dd7-125">Header-Dateien</span><span class="sxs-lookup"><span data-stu-id="77dd7-125">Header files</span></span>

<span data-ttu-id="77dd7-126">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="77dd7-126">Mapidefs.h</span></span>
  
> <span data-ttu-id="77dd7-127">Enthält die Datentypdefinitionen.</span><span class="sxs-lookup"><span data-stu-id="77dd7-127">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="77dd7-128">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="77dd7-128">See also</span></span>



[<span data-ttu-id="77dd7-129">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="77dd7-129">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="77dd7-130">Kanonische MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="77dd7-130">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="77dd7-131">Zuordnen von kanonischen Eigenschaftennamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="77dd7-131">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="77dd7-132">Zuordnen von MAPI-Namen zu kanonische Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="77dd7-132">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

