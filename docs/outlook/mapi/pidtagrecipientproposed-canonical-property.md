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
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 1b09d8d7621121b3652ceb9824f6d36b53844206
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32283135"
---
# <a name="pidtagrecipientproposed-canonical-property"></a><span data-ttu-id="46b9a-103">PidTagRecipientProposed (kanonische Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="46b9a-103">PidTagRecipientProposed Canonical Property</span></span>

  
  
<span data-ttu-id="46b9a-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="46b9a-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="46b9a-105">Gibt an, ob ein Besprechungsteilnehmer geantwortet hat.</span><span class="sxs-lookup"><span data-stu-id="46b9a-105">Indicates whether a meeting attendee has responded.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="46b9a-106">Zugeordnete Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="46b9a-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="46b9a-107">PR_RECIPIENT_PROPOSED</span><span class="sxs-lookup"><span data-stu-id="46b9a-107">PR_RECIPIENT_PROPOSED</span></span>  <br/> |
|<span data-ttu-id="46b9a-108">Kennung:</span><span class="sxs-lookup"><span data-stu-id="46b9a-108">Identifier:</span></span>  <br/> |<span data-ttu-id="46b9a-109">0x5FE1</span><span class="sxs-lookup"><span data-stu-id="46b9a-109">0x5FE1</span></span>  <br/> |
|<span data-ttu-id="46b9a-110">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="46b9a-110">Data type:</span></span>  <br/> |<span data-ttu-id="46b9a-111">PT_BOOLEAN</span><span class="sxs-lookup"><span data-stu-id="46b9a-111">PT_BOOLEAN</span></span>  <br/> |
|<span data-ttu-id="46b9a-112">Bereich:</span><span class="sxs-lookup"><span data-stu-id="46b9a-112">Area:</span></span>  <br/> |<span data-ttu-id="46b9a-113">Transportempfänger</span><span class="sxs-lookup"><span data-stu-id="46b9a-113">Transport recipient</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="46b9a-114">Hinweise</span><span class="sxs-lookup"><span data-stu-id="46b9a-114">Remarks</span></span>

<span data-ttu-id="46b9a-115">Der Wert TRUE für diese Eigenschaft gibt an, dass der Teilnehmer ein neues Datum und/oder eine neue Uhrzeit vorgeschlagen hat.</span><span class="sxs-lookup"><span data-stu-id="46b9a-115">A value of TRUE for this property indicates that the attendee proposed a new date and/or time.</span></span> <span data-ttu-id="46b9a-116">Der Wert FALSE oder das Fehlen dieser Eigenschaft bedeutet, dass der Teilnehmer noch nicht geantwortet hat oder die letzte Antwort des Teilnehmers keinen neuen Datums-/Uhrzeitvorschlag enthält.</span><span class="sxs-lookup"><span data-stu-id="46b9a-116">A value of FALSE, or the absence of this property, means either that the attendee has not yet responded, or the most recent response from the attendee did not include a new date/ time proposal.</span></span> <span data-ttu-id="46b9a-117">Dieser Wert darf für Teilnehmer in einer Serienserie nicht TRUE sein.</span><span class="sxs-lookup"><span data-stu-id="46b9a-117">This value must not be TRUE for attendees in a recurring series.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="46b9a-118">Verwandte Ressourcen</span><span class="sxs-lookup"><span data-stu-id="46b9a-118">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="46b9a-119">Protokollspezifikationen</span><span class="sxs-lookup"><span data-stu-id="46b9a-119">Protocol specifications</span></span>

<span data-ttu-id="46b9a-120">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="46b9a-120">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="46b9a-121">Enthält Verweise auf Exchange Server Protokollspezifikationen.</span><span class="sxs-lookup"><span data-stu-id="46b9a-121">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="46b9a-122">[[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="46b9a-122">[[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="46b9a-123">Gibt die Eigenschaften und Vorgänge für Termin-, Besprechungs- und Antwortnachrichten an.</span><span class="sxs-lookup"><span data-stu-id="46b9a-123">Specifies the properties and operations for appointment, meeting request, and response messages.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="46b9a-124">Headerdateien</span><span class="sxs-lookup"><span data-stu-id="46b9a-124">Header files</span></span>

<span data-ttu-id="46b9a-125">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="46b9a-125">Mapidefs.h</span></span>
  
> <span data-ttu-id="46b9a-126">Bietet Datentypdefinitionen.</span><span class="sxs-lookup"><span data-stu-id="46b9a-126">Provides data type definitions.</span></span>
    
<span data-ttu-id="46b9a-127">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="46b9a-127">Mapitags.h</span></span>
  
> <span data-ttu-id="46b9a-128">Enthält Definitionen von Eigenschaften, die als alternative Namen aufgeführt sind.</span><span class="sxs-lookup"><span data-stu-id="46b9a-128">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="46b9a-129">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="46b9a-129">See also</span></span>



[<span data-ttu-id="46b9a-130">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="46b9a-130">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="46b9a-131">KANONISCHE EIGENSCHAFTEN VON MAPI</span><span class="sxs-lookup"><span data-stu-id="46b9a-131">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="46b9a-132">Zuordnen kanonischer Eigenschaftsnamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="46b9a-132">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="46b9a-133">Zuordnen von MAPI-Namen zu kanonischen Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="46b9a-133">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

