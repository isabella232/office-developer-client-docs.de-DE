---
title: PidTagReportDisposition (kanonische Eigenschaft)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_type:
- COM
ms.assetid: 56b9e7bd-eece-4264-8ee5-a1bcbec4f35c
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 1e84308f3a9f9457c5db23c1ad9d42d6e856519e
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2018
ms.locfileid: "22583631"
---
# <a name="pidtagreportdisposition-canonical-property"></a><span data-ttu-id="bffbd-103">PidTagReportDisposition (kanonische Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="bffbd-103">PidTagReportDisposition Canonical Property</span></span>

  
  
<span data-ttu-id="bffbd-104">**Betrifft**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="bffbd-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="bffbd-105">Gibt den Empfangsbestätigungsstatus für Nachrichten, die Empfangsbestätigungen anfordern.</span><span class="sxs-lookup"><span data-stu-id="bffbd-105">Indicates the receipt status for messages that request receipts.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="bffbd-106">Zugeordnete Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="bffbd-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="bffbd-107">PR_REPORT_DISPOSITION, PR_REPORT_DISPOSITION_A, PR_REPORT_DISPOSITION_W</span><span class="sxs-lookup"><span data-stu-id="bffbd-107">PR_REPORT_DISPOSITION, PR_REPORT_DISPOSITION_A, PR_REPORT_DISPOSITION_W</span></span>  <br/> |
|<span data-ttu-id="bffbd-108">Kennung:</span><span class="sxs-lookup"><span data-stu-id="bffbd-108">Identifier:</span></span>  <br/> |<span data-ttu-id="bffbd-109">0 x 0080</span><span class="sxs-lookup"><span data-stu-id="bffbd-109">0x0080</span></span>  <br/> |
|<span data-ttu-id="bffbd-110">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="bffbd-110">Data type:</span></span>  <br/> |<span data-ttu-id="bffbd-111">PT_STRING8, PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="bffbd-111">PT_STRING8, PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="bffbd-112">Bereich:</span><span class="sxs-lookup"><span data-stu-id="bffbd-112">Area:</span></span>  <br/> |<span data-ttu-id="bffbd-113">MAPI-Umschlag</span><span class="sxs-lookup"><span data-stu-id="bffbd-113">MAPI envelope</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="bffbd-114">HinwBemerkungeneise</span><span class="sxs-lookup"><span data-stu-id="bffbd-114">Remarks</span></span>

<span data-ttu-id="bffbd-115">Die folgenden Werte sind gültig:</span><span class="sxs-lookup"><span data-stu-id="bffbd-115">The following are valid values:</span></span>
  
- <span data-ttu-id="bffbd-116">"gelöscht"</span><span class="sxs-lookup"><span data-stu-id="bffbd-116">"deleted"</span></span>
    
- <span data-ttu-id="bffbd-117">"verarbeitet"</span><span class="sxs-lookup"><span data-stu-id="bffbd-117">"processed"</span></span>
    
- <span data-ttu-id="bffbd-118">"verteilt"</span><span class="sxs-lookup"><span data-stu-id="bffbd-118">"dispatched"</span></span>
    
- <span data-ttu-id="bffbd-119">"verweigert."</span><span class="sxs-lookup"><span data-stu-id="bffbd-119">"denied"</span></span>
    
- <span data-ttu-id="bffbd-120">"failed"</span><span class="sxs-lookup"><span data-stu-id="bffbd-120">"failed"</span></span>
    
## <a name="related-resources"></a><span data-ttu-id="bffbd-121">Verwandte Ressourcen</span><span class="sxs-lookup"><span data-stu-id="bffbd-121">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="bffbd-122">Protokollspezifikationen</span><span class="sxs-lookup"><span data-stu-id="bffbd-122">Protocol specifications</span></span>

<span data-ttu-id="bffbd-123">[[MS-OXPROPS]]</span><span class="sxs-lookup"><span data-stu-id="bffbd-123">[[MS-OXPROPS]]</span></span> 
  
> <span data-ttu-id="bffbd-124">Bietet Verweise auf Verwandte Exchange Server-Spezifikationen.</span><span class="sxs-lookup"><span data-stu-id="bffbd-124">Provides references to related Exchange Server protocol specifications.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="bffbd-125">Header-Dateien</span><span class="sxs-lookup"><span data-stu-id="bffbd-125">Header files</span></span>

<span data-ttu-id="bffbd-126">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="bffbd-126">Mapidefs.h</span></span>
  
> <span data-ttu-id="bffbd-127">Enthält die Datentypdefinitionen.</span><span class="sxs-lookup"><span data-stu-id="bffbd-127">Provides data type definitions.</span></span>
    
<span data-ttu-id="bffbd-128">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="bffbd-128">Mapitags.h</span></span>
  
> <span data-ttu-id="bffbd-129">Enthält Definitionen von Eigenschaften, die als zugeordneten Eigenschaften aufgelistet.</span><span class="sxs-lookup"><span data-stu-id="bffbd-129">Contains definitions of properties listed as associated properties.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="bffbd-130">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="bffbd-130">See also</span></span>



[<span data-ttu-id="bffbd-131">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="bffbd-131">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="bffbd-132">Kanonische MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="bffbd-132">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="bffbd-133">Zuordnen von kanonischen Eigenschaftennamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="bffbd-133">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="bffbd-134">Zuordnen von MAPI-Namen zu kanonische Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="bffbd-134">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

