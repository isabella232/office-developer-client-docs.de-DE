---
title: PidTagRecipientTrackStatusTime (kanonische Eigenschaft)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagRecipientTrackStatusTime
api_type:
- COM
ms.assetid: f14dfe47-a9f8-4475-bb26-7da3411d8c6f
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: 0db4efcf1e05536ee7abb3459caa0159f84ef798
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19794916"
---
# <a name="pidtagrecipienttrackstatustime-canonical-property"></a><span data-ttu-id="950a6-103">PidTagRecipientTrackStatusTime (kanonische Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="950a6-103">PidTagRecipientTrackStatusTime Canonical Property</span></span>

  
  
<span data-ttu-id="950a6-104">**Betrifft**: Outlook</span><span class="sxs-lookup"><span data-stu-id="950a6-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="950a6-105">Enthält das Datum und die Uhrzeit, als der Teilnehmer geantwortet hat.</span><span class="sxs-lookup"><span data-stu-id="950a6-105">Contains the date and time when the attendee responded.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="950a6-106">Zugeordneten Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="950a6-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="950a6-107">PR_RECIPIENT_TRACKSTATUS_TIME</span><span class="sxs-lookup"><span data-stu-id="950a6-107">PR_RECIPIENT_TRACKSTATUS_TIME</span></span>  <br/> |
|<span data-ttu-id="950a6-108">Bezeichner:</span><span class="sxs-lookup"><span data-stu-id="950a6-108">Identifier:</span></span>  <br/> |<span data-ttu-id="950a6-109">0x5FFB</span><span class="sxs-lookup"><span data-stu-id="950a6-109">0x5FFB</span></span>  <br/> |
|<span data-ttu-id="950a6-110">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="950a6-110">Data type:</span></span>  <br/> |<span data-ttu-id="950a6-111">PT_SYSTIME</span><span class="sxs-lookup"><span data-stu-id="950a6-111">PT_SYSTIME</span></span>  <br/> |
|<span data-ttu-id="950a6-112">Bereich:</span><span class="sxs-lookup"><span data-stu-id="950a6-112">Area:</span></span>  <br/> |<span data-ttu-id="950a6-113">Transport-Empfänger</span><span class="sxs-lookup"><span data-stu-id="950a6-113">Transport recipient</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="950a6-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="950a6-114">Remarks</span></span>

<span data-ttu-id="950a6-115">Der Wert muss in koordinierter Weltzeit (UTC) angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="950a6-115">The value must be specified in Coordinated Universal Time (UTC).</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="950a6-116">Verwandte Ressourcen</span><span class="sxs-lookup"><span data-stu-id="950a6-116">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="950a6-117">Protokollspezifikationen</span><span class="sxs-lookup"><span data-stu-id="950a6-117">Protocol specifications</span></span>

<span data-ttu-id="950a6-118">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="950a6-118">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="950a6-119">Bietet Verweise auf Verwandte Exchange Server-Spezifikationen.</span><span class="sxs-lookup"><span data-stu-id="950a6-119">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="950a6-120">[[MS-OXOCAL]](http://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="950a6-120">[[MS-OXOCAL]](http://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="950a6-121">Gibt die Eigenschaften und Vorgänge für den Termin, einer Besprechungsanfrage und Antwortnachrichten.</span><span class="sxs-lookup"><span data-stu-id="950a6-121">Specifies the properties and operations for appointment, meeting request, and response messages.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="950a6-122">Header-Dateien</span><span class="sxs-lookup"><span data-stu-id="950a6-122">Header files</span></span>

<span data-ttu-id="950a6-123">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="950a6-123">Mapidefs.h</span></span>
  
> <span data-ttu-id="950a6-124">Enthält die Datentypdefinitionen.</span><span class="sxs-lookup"><span data-stu-id="950a6-124">Provides data type definitions.</span></span>
    
<span data-ttu-id="950a6-125">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="950a6-125">Mapitags.h</span></span>
  
> <span data-ttu-id="950a6-126">Enthält Definitionen von Eigenschaften, die als Alternative Namen aufgelistet.</span><span class="sxs-lookup"><span data-stu-id="950a6-126">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="950a6-127">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="950a6-127">See also</span></span>



[<span data-ttu-id="950a6-128">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="950a6-128">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="950a6-129">Kanonische MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="950a6-129">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="950a6-130">Zuordnen von kanonischen Eigenschaftennamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="950a6-130">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="950a6-131">Zuordnen von MAPI-Namen zu kanonische Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="950a6-131">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

