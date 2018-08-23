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
ms.openlocfilehash: b1d4600810d4f773896f1880b7309c1f818c7dc1
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2018
ms.locfileid: "22575777"
---
# <a name="pidlidisexception-canonical-property"></a><span data-ttu-id="9d4bd-103">PidLidIsException (kanonische Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="9d4bd-103">PidLidIsException Canonical Property</span></span>

  
  
<span data-ttu-id="9d4bd-104">**Betrifft**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="9d4bd-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="9d4bd-105">Gibt an, dass das Objekt, das eine Ausnahme (einschließlich einer verwaisten Instanz) darstellt.</span><span class="sxs-lookup"><span data-stu-id="9d4bd-105">Indicates that the object that represents an exception (including an orphan instance).</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="9d4bd-106">Zugeordnete Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="9d4bd-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="9d4bd-107">LID_IS_EXCEPTION</span><span class="sxs-lookup"><span data-stu-id="9d4bd-107">LID_IS_EXCEPTION</span></span>  <br/> |
|<span data-ttu-id="9d4bd-108">-Eigenschaft festgelegt:</span><span class="sxs-lookup"><span data-stu-id="9d4bd-108">Property set:</span></span>  <br/> |<span data-ttu-id="9d4bd-109">PSETID_Meeting</span><span class="sxs-lookup"><span data-stu-id="9d4bd-109">PSETID_Meeting</span></span>  <br/> |
|<span data-ttu-id="9d4bd-110">Long-ID (Abdeckung):</span><span class="sxs-lookup"><span data-stu-id="9d4bd-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="9d4bd-111">0x0000000A</span><span class="sxs-lookup"><span data-stu-id="9d4bd-111">0x0000000A</span></span>  <br/> |
|<span data-ttu-id="9d4bd-112">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="9d4bd-112">Data type:</span></span>  <br/> |<span data-ttu-id="9d4bd-113">PT_BOOLEAN</span><span class="sxs-lookup"><span data-stu-id="9d4bd-113">PT_BOOLEAN</span></span>  <br/> |
|<span data-ttu-id="9d4bd-114">Bereich:</span><span class="sxs-lookup"><span data-stu-id="9d4bd-114">Area:</span></span>  <br/> |<span data-ttu-id="9d4bd-115">Besprechungen</span><span class="sxs-lookup"><span data-stu-id="9d4bd-115">Meetings</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="9d4bd-116">HinwBemerkungeneise</span><span class="sxs-lookup"><span data-stu-id="9d4bd-116">Remarks</span></span>

<span data-ttu-id="9d4bd-117">Gibt der Wert FALSE an, dass das Objekt, das eine Terminserie oder eine einzelne Instanz darstellt.</span><span class="sxs-lookup"><span data-stu-id="9d4bd-117">A value of FALSE indicates that the object that represents a recurring series or a single instance.</span></span> <span data-ttu-id="9d4bd-118">Das Fehlen dieser Eigenschaft für jedes Objekt gilt gibt einen Wert false mit Ausnahme der Ausnahme eingebettete Nachricht, die Wert TRUE wird davon ausgegangen.</span><span class="sxs-lookup"><span data-stu-id="9d4bd-118">The absence of this property for any object indicates a value of FALSE except for the exception embedded message, which assumes a value of TRUE.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="9d4bd-119">Verwandte Ressourcen</span><span class="sxs-lookup"><span data-stu-id="9d4bd-119">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="9d4bd-120">Protokollspezifikationen</span><span class="sxs-lookup"><span data-stu-id="9d4bd-120">Protocol specifications</span></span>

<span data-ttu-id="9d4bd-121">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="9d4bd-121">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="9d4bd-122">Enthält Eigenschaftendefinitionen und Verweise auf Verwandte Exchange Server-Spezifikationen.</span><span class="sxs-lookup"><span data-stu-id="9d4bd-122">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="9d4bd-123">[[MS-OXOCAL]](http://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="9d4bd-123">[[MS-OXOCAL] ](http://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="9d4bd-124">Gibt die Eigenschaften und Vorgänge für den Termin, einer Besprechungsanfrage und Antwortnachrichten.</span><span class="sxs-lookup"><span data-stu-id="9d4bd-124">Specifies the properties and operations for appointment, meeting request, and response messages.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="9d4bd-125">Header-Dateien</span><span class="sxs-lookup"><span data-stu-id="9d4bd-125">Header files</span></span>

<span data-ttu-id="9d4bd-126">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="9d4bd-126">Mapidefs.h</span></span>
  
> <span data-ttu-id="9d4bd-127">Enthält die Datentypdefinitionen.</span><span class="sxs-lookup"><span data-stu-id="9d4bd-127">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="9d4bd-128">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="9d4bd-128">See also</span></span>



[<span data-ttu-id="9d4bd-129">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="9d4bd-129">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="9d4bd-130">Kanonische MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="9d4bd-130">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="9d4bd-131">Zuordnen von kanonischen Eigenschaftennamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="9d4bd-131">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="9d4bd-132">Zuordnen von MAPI-Namen zu kanonische Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="9d4bd-132">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

