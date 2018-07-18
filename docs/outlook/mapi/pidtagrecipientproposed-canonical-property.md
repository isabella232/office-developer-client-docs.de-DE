---
title: PidTagRecipientProposed (kanonische Eigenschaft)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagRecipientProposed
api_type:
- COM
ms.assetid: 8cb0e46c-0937-482f-be78-1f2e5261b210
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: 3b05f33328e9e0b90251a99defa9816f86971337
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19794906"
---
# <a name="pidtagrecipientproposed-canonical-property"></a><span data-ttu-id="38335-103">PidTagRecipientProposed (kanonische Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="38335-103">PidTagRecipientProposed Canonical Property</span></span>

  
  
<span data-ttu-id="38335-104">**Betrifft**: Outlook</span><span class="sxs-lookup"><span data-stu-id="38335-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="38335-105">Gibt an, ob ein Teilnehmer der Besprechung geantwortet hat.</span><span class="sxs-lookup"><span data-stu-id="38335-105">Indicates whether a meeting attendee has responded.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="38335-106">Zugeordneten Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="38335-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="38335-107">PR_RECIPIENT_PROPOSED</span><span class="sxs-lookup"><span data-stu-id="38335-107">PR_RECIPIENT_PROPOSED</span></span>  <br/> |
|<span data-ttu-id="38335-108">Bezeichner:</span><span class="sxs-lookup"><span data-stu-id="38335-108">Identifier:</span></span>  <br/> |<span data-ttu-id="38335-109">0x5FE1</span><span class="sxs-lookup"><span data-stu-id="38335-109">0x5FE1</span></span>  <br/> |
|<span data-ttu-id="38335-110">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="38335-110">Data type:</span></span>  <br/> |<span data-ttu-id="38335-111">PT_BOOLEAN</span><span class="sxs-lookup"><span data-stu-id="38335-111">PT_BOOLEAN</span></span>  <br/> |
|<span data-ttu-id="38335-112">Bereich:</span><span class="sxs-lookup"><span data-stu-id="38335-112">Area:</span></span>  <br/> |<span data-ttu-id="38335-113">Transport-Empfänger</span><span class="sxs-lookup"><span data-stu-id="38335-113">Transport recipient</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="38335-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="38335-114">Remarks</span></span>

<span data-ttu-id="38335-115">Der Wert TRUE für diese Eigenschaft gibt an, dass der Teilnehmer ein neues Datum und/oder eine Uhrzeit vorgeschlagen.</span><span class="sxs-lookup"><span data-stu-id="38335-115">A value of TRUE for this property indicates that the attendee proposed a new date and/or time.</span></span> <span data-ttu-id="38335-116">Der Wert FALSE oder das Fehlen dieser Eigenschaft bedeutet, dass entweder noch, dass der Teilnehmer nicht hat geantwortet, oder die letzte Antwort vom Teilnehmer nicht enthalten ein neues Datum / Uhrzeit Vorschlag.</span><span class="sxs-lookup"><span data-stu-id="38335-116">A value of FALSE, or the absence of this property, means either that the attendee has not yet responded, or the most recent response from the attendee did not include a new date/ time proposal.</span></span> <span data-ttu-id="38335-117">Dieser Wert muss sich nicht auf "true" für die Teilnehmer in einer Terminserie.</span><span class="sxs-lookup"><span data-stu-id="38335-117">This value must not be TRUE for attendees in a recurring series.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="38335-118">Verwandte Ressourcen</span><span class="sxs-lookup"><span data-stu-id="38335-118">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="38335-119">Protokollspezifikationen</span><span class="sxs-lookup"><span data-stu-id="38335-119">Protocol specifications</span></span>

<span data-ttu-id="38335-120">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="38335-120">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="38335-121">Bietet Verweise auf Verwandte Exchange Server-Spezifikationen.</span><span class="sxs-lookup"><span data-stu-id="38335-121">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="38335-122">[[MS-OXOCAL]](http://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="38335-122">[[MS-OXOCAL]](http://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="38335-123">Gibt die Eigenschaften und Vorgänge für den Termin, einer Besprechungsanfrage und Antwortnachrichten.</span><span class="sxs-lookup"><span data-stu-id="38335-123">Specifies the properties and operations for appointment, meeting request, and response messages.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="38335-124">Header-Dateien</span><span class="sxs-lookup"><span data-stu-id="38335-124">Header files</span></span>

<span data-ttu-id="38335-125">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="38335-125">Mapidefs.h</span></span>
  
> <span data-ttu-id="38335-126">Enthält die Datentypdefinitionen.</span><span class="sxs-lookup"><span data-stu-id="38335-126">Provides data type definitions.</span></span>
    
<span data-ttu-id="38335-127">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="38335-127">Mapitags.h</span></span>
  
> <span data-ttu-id="38335-128">Enthält Definitionen von Eigenschaften, die als Alternative Namen aufgelistet.</span><span class="sxs-lookup"><span data-stu-id="38335-128">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="38335-129">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="38335-129">See also</span></span>



[<span data-ttu-id="38335-130">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="38335-130">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="38335-131">Kanonische MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="38335-131">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="38335-132">Zuordnen von kanonischen Eigenschaftennamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="38335-132">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="38335-133">Zuordnen von MAPI-Namen zu kanonische Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="38335-133">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

