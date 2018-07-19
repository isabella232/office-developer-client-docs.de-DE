---
title: PidLidFExceptionalAttendees (kanonische Eigenschaft)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidFExceptionalAttendees
api_type:
- COM
ms.assetid: f1f489a3-e83a-4e96-bf9a-d98bc17d29f5
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 7c7f654d42df7856b0e69bf276a763ccd29d1d87
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19793584"
---
# <a name="pidlidfexceptionalattendees-canonical-property"></a><span data-ttu-id="8125b-103">PidLidFExceptionalAttendees (kanonische Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="8125b-103">PidLidFExceptionalAttendees Canonical Property</span></span>

  
  
<span data-ttu-id="8125b-104">**Betrifft**: Outlook</span><span class="sxs-lookup"><span data-stu-id="8125b-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="8125b-105">Gibt an, ob diese Eigenschaft ein wiederkehrendes Calendar-Objekt mit eine oder mehrere Ausnahmen ist und mindestens eines der Ausnahme eingebettete Nachrichten mindestens eine RecipientRow hat.</span><span class="sxs-lookup"><span data-stu-id="8125b-105">Indicates whether this property is a recurring calendar object with one or more exceptions, and at least one of the exception embedded messages has at least one RecipientRow.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="8125b-106">Zugeordneten Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="8125b-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="8125b-107">dispidFExceptionalAttendees</span><span class="sxs-lookup"><span data-stu-id="8125b-107">dispidFExceptionalAttendees</span></span>  <br/> |
|<span data-ttu-id="8125b-108">-Eigenschaft festgelegt:</span><span class="sxs-lookup"><span data-stu-id="8125b-108">Property set:</span></span>  <br/> |<span data-ttu-id="8125b-109">PSETID_Appointment</span><span class="sxs-lookup"><span data-stu-id="8125b-109">PSETID_Appointment</span></span>  <br/> |
|<span data-ttu-id="8125b-110">Long-ID (Abdeckung):</span><span class="sxs-lookup"><span data-stu-id="8125b-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="8125b-111">0x0000822B</span><span class="sxs-lookup"><span data-stu-id="8125b-111">0x0000822B</span></span>  <br/> |
|<span data-ttu-id="8125b-112">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="8125b-112">Data type:</span></span>  <br/> |<span data-ttu-id="8125b-113">PT_BOOLEAN</span><span class="sxs-lookup"><span data-stu-id="8125b-113">PT_BOOLEAN</span></span>  <br/> |
|<span data-ttu-id="8125b-114">Bereich:</span><span class="sxs-lookup"><span data-stu-id="8125b-114">Area:</span></span>  <br/> |<span data-ttu-id="8125b-115">Besprechungen</span><span class="sxs-lookup"><span data-stu-id="8125b-115">Meetings</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="8125b-116">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="8125b-116">Remarks</span></span>

<span data-ttu-id="8125b-117">Der Wert FALSE oder das fehlen diese Eigenschaft gibt an, dass das Calendar-Objekt entweder keine Ausnahmen hat oder keine Ausnahme eingebettete Nachrichten RecipientRows hat.</span><span class="sxs-lookup"><span data-stu-id="8125b-117">A value of FALSE, or the absence of this property, indicates that the calendar object either has no exceptions, or none of the exception embedded messages has RecipientRows.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="8125b-118">Verwandte Ressourcen</span><span class="sxs-lookup"><span data-stu-id="8125b-118">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="8125b-119">Protokollspezifikationen</span><span class="sxs-lookup"><span data-stu-id="8125b-119">Protocol specifications</span></span>

<span data-ttu-id="8125b-120">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="8125b-120">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="8125b-121">Enthält Eigenschaftendefinitionen und Verweise auf Verwandte Exchange Server-Spezifikationen.</span><span class="sxs-lookup"><span data-stu-id="8125b-121">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="8125b-122">[[MS-OXOCAL]](http://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="8125b-122">[[MS-OXOCAL]](http://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="8125b-123">Gibt die Eigenschaften und Vorgänge für den Termin, einer Besprechungsanfrage und Antwortnachrichten.</span><span class="sxs-lookup"><span data-stu-id="8125b-123">Specifies the properties and operations for appointment, meeting request, and response messages.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="8125b-124">Header-Dateien</span><span class="sxs-lookup"><span data-stu-id="8125b-124">Header files</span></span>

<span data-ttu-id="8125b-125">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="8125b-125">Mapidefs.h</span></span>
  
> <span data-ttu-id="8125b-126">Enthält die Datentypdefinitionen.</span><span class="sxs-lookup"><span data-stu-id="8125b-126">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="8125b-127">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="8125b-127">See also</span></span>



[<span data-ttu-id="8125b-128">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="8125b-128">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="8125b-129">Kanonische MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="8125b-129">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="8125b-130">Zuordnen von kanonischen Eigenschaftennamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="8125b-130">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="8125b-131">Zuordnen von MAPI-Namen zu kanonische Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="8125b-131">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

