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
ms.openlocfilehash: dae31959cddad7ad61ea32f2372ea34bdbff658e
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33423706"
---
# <a name="pidtagreportdisposition-canonical-property"></a><span data-ttu-id="5345b-103">PidTagReportDisposition (kanonische Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="5345b-103">PidTagReportDisposition Canonical Property</span></span>

  
  
<span data-ttu-id="5345b-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="5345b-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="5345b-105">Gibt den Empfangsstatus für Nachrichten an, die Quittungen anfordern.</span><span class="sxs-lookup"><span data-stu-id="5345b-105">Indicates the receipt status for messages that request receipts.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="5345b-106">Zugeordnete Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="5345b-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="5345b-107">PR_REPORT_DISPOSITION, PR_REPORT_DISPOSITION_A, PR_REPORT_DISPOSITION_W</span><span class="sxs-lookup"><span data-stu-id="5345b-107">PR_REPORT_DISPOSITION, PR_REPORT_DISPOSITION_A, PR_REPORT_DISPOSITION_W</span></span>  <br/> |
|<span data-ttu-id="5345b-108">Kennung:</span><span class="sxs-lookup"><span data-stu-id="5345b-108">Identifier:</span></span>  <br/> |<span data-ttu-id="5345b-109">0x0080</span><span class="sxs-lookup"><span data-stu-id="5345b-109">0x0080</span></span>  <br/> |
|<span data-ttu-id="5345b-110">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="5345b-110">Data type:</span></span>  <br/> |<span data-ttu-id="5345b-111">PT_STRING8, PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="5345b-111">PT_STRING8, PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="5345b-112">Bereich:</span><span class="sxs-lookup"><span data-stu-id="5345b-112">Area:</span></span>  <br/> |<span data-ttu-id="5345b-113">MAPI-Umschlag</span><span class="sxs-lookup"><span data-stu-id="5345b-113">MAPI envelope</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="5345b-114">Hinweise</span><span class="sxs-lookup"><span data-stu-id="5345b-114">Remarks</span></span>

<span data-ttu-id="5345b-115">Die folgenden Werte sind gültig:</span><span class="sxs-lookup"><span data-stu-id="5345b-115">The following are valid values:</span></span>
  
- <span data-ttu-id="5345b-116">"gelöscht"</span><span class="sxs-lookup"><span data-stu-id="5345b-116">"deleted"</span></span>
    
- <span data-ttu-id="5345b-117">"verarbeitet"</span><span class="sxs-lookup"><span data-stu-id="5345b-117">"processed"</span></span>
    
- <span data-ttu-id="5345b-118">"Dispatched"</span><span class="sxs-lookup"><span data-stu-id="5345b-118">"dispatched"</span></span>
    
- <span data-ttu-id="5345b-119">"Verweigert"</span><span class="sxs-lookup"><span data-stu-id="5345b-119">"denied"</span></span>
    
- <span data-ttu-id="5345b-120">"failed"</span><span class="sxs-lookup"><span data-stu-id="5345b-120">"failed"</span></span>
    
## <a name="related-resources"></a><span data-ttu-id="5345b-121">Verwandte Ressourcen</span><span class="sxs-lookup"><span data-stu-id="5345b-121">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="5345b-122">Protokollspezifikationen</span><span class="sxs-lookup"><span data-stu-id="5345b-122">Protocol specifications</span></span>

<span data-ttu-id="5345b-123">[[MS-OXPROPS]]</span><span class="sxs-lookup"><span data-stu-id="5345b-123">[[MS-OXPROPS]]</span></span> 
  
> <span data-ttu-id="5345b-124">Enthält Verweise auf Exchange Server Protokollspezifikationen.</span><span class="sxs-lookup"><span data-stu-id="5345b-124">Provides references to related Exchange Server protocol specifications.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="5345b-125">Headerdateien</span><span class="sxs-lookup"><span data-stu-id="5345b-125">Header files</span></span>

<span data-ttu-id="5345b-126">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="5345b-126">Mapidefs.h</span></span>
  
> <span data-ttu-id="5345b-127">Bietet Datentypdefinitionen.</span><span class="sxs-lookup"><span data-stu-id="5345b-127">Provides data type definitions.</span></span>
    
<span data-ttu-id="5345b-128">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="5345b-128">Mapitags.h</span></span>
  
> <span data-ttu-id="5345b-129">Enthält Definitionen von Eigenschaften, die als zugeordnete Eigenschaften aufgeführt sind.</span><span class="sxs-lookup"><span data-stu-id="5345b-129">Contains definitions of properties listed as associated properties.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="5345b-130">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="5345b-130">See also</span></span>



[<span data-ttu-id="5345b-131">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="5345b-131">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="5345b-132">KANONISCHE EIGENSCHAFTEN VON MAPI</span><span class="sxs-lookup"><span data-stu-id="5345b-132">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="5345b-133">Zuordnen kanonischer Eigenschaftsnamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="5345b-133">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="5345b-134">Zuordnen von MAPI-Namen zu kanonischen Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="5345b-134">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

