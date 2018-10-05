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
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 2dec706252eb6aa1b28f68f6f46473df04f3fbe7
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/04/2018
ms.locfileid: "25382792"
---
# <a name="pidtagrecipienttrackstatustime-canonical-property"></a><span data-ttu-id="1c58c-103">PidTagRecipientTrackStatusTime (kanonische Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="1c58c-103">PidTagRecipientTrackStatusTime Canonical Property</span></span>

  
  
<span data-ttu-id="1c58c-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="1c58c-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="1c58c-105">Enthält das Datum und die Uhrzeit, als der Teilnehmer geantwortet hat.</span><span class="sxs-lookup"><span data-stu-id="1c58c-105">Contains the date and time when the attendee responded.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="1c58c-106">Zugeordnete Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="1c58c-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="1c58c-107">PR_RECIPIENT_TRACKSTATUS_TIME</span><span class="sxs-lookup"><span data-stu-id="1c58c-107">PR_RECIPIENT_TRACKSTATUS_TIME</span></span>  <br/> |
|<span data-ttu-id="1c58c-108">Kennung:</span><span class="sxs-lookup"><span data-stu-id="1c58c-108">Identifier:</span></span>  <br/> |<span data-ttu-id="1c58c-109">0x5FFB</span><span class="sxs-lookup"><span data-stu-id="1c58c-109">0x5FFB</span></span>  <br/> |
|<span data-ttu-id="1c58c-110">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="1c58c-110">Data type:</span></span>  <br/> |<span data-ttu-id="1c58c-111">PT_SYSTIME</span><span class="sxs-lookup"><span data-stu-id="1c58c-111">PT_SYSTIME</span></span>  <br/> |
|<span data-ttu-id="1c58c-112">Bereich:</span><span class="sxs-lookup"><span data-stu-id="1c58c-112">Area:</span></span>  <br/> |<span data-ttu-id="1c58c-113">Transport-Empfänger</span><span class="sxs-lookup"><span data-stu-id="1c58c-113">Transport recipient</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="1c58c-114">Hinweise</span><span class="sxs-lookup"><span data-stu-id="1c58c-114">Remarks</span></span>

<span data-ttu-id="1c58c-115">Der Wert muss in koordinierter Weltzeit (UTC) angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="1c58c-115">The value must be specified in Coordinated Universal Time (UTC).</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="1c58c-116">Verwandte Ressourcen</span><span class="sxs-lookup"><span data-stu-id="1c58c-116">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="1c58c-117">Protokollspezifikationen</span><span class="sxs-lookup"><span data-stu-id="1c58c-117">Protocol specifications</span></span>

<span data-ttu-id="1c58c-118">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="1c58c-118">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="1c58c-119">Bietet Verweise auf Verwandte Exchange Server-Spezifikationen.</span><span class="sxs-lookup"><span data-stu-id="1c58c-119">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="1c58c-120">[[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="1c58c-120">[[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="1c58c-121">Gibt die Eigenschaften und Vorgänge für den Termin, einer Besprechungsanfrage und Antwortnachrichten.</span><span class="sxs-lookup"><span data-stu-id="1c58c-121">Specifies the properties and operations for appointment, meeting request, and response messages.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="1c58c-122">Header-Dateien</span><span class="sxs-lookup"><span data-stu-id="1c58c-122">Header files</span></span>

<span data-ttu-id="1c58c-123">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="1c58c-123">Mapidefs.h</span></span>
  
> <span data-ttu-id="1c58c-124">Enthält die Datentypdefinitionen.</span><span class="sxs-lookup"><span data-stu-id="1c58c-124">Provides data type definitions.</span></span>
    
<span data-ttu-id="1c58c-125">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="1c58c-125">Mapitags.h</span></span>
  
> <span data-ttu-id="1c58c-126">Enthält Definitionen von Eigenschaften, die als Alternative Namen aufgelistet.</span><span class="sxs-lookup"><span data-stu-id="1c58c-126">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="1c58c-127">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="1c58c-127">See also</span></span>



[<span data-ttu-id="1c58c-128">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="1c58c-128">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="1c58c-129">Kanonische MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="1c58c-129">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="1c58c-130">Zuordnen von kanonischen Eigenschaftennamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="1c58c-130">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="1c58c-131">Zuordnen von MAPI-Namen zu kanonische Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="1c58c-131">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

