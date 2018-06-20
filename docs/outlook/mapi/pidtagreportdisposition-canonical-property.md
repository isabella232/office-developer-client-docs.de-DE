---
title: Kanonische PidTagReportDisposition-Eigenschaft
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_type:
- COM
ms.assetid: 56b9e7bd-eece-4264-8ee5-a1bcbec4f35c
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: 62d5b04086e45b6b3d2cfa960472010827d60d6b
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19794967"
---
# <a name="pidtagreportdisposition-canonical-property"></a><span data-ttu-id="4f141-103">Kanonische PidTagReportDisposition-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="4f141-103">PidTagReportDisposition Canonical Property</span></span>

  
  
<span data-ttu-id="4f141-104">**Betrifft**: Outlook</span><span class="sxs-lookup"><span data-stu-id="4f141-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="4f141-105">Gibt den Empfangsbestätigungsstatus für Nachrichten, die Empfangsbestätigungen anfordern.</span><span class="sxs-lookup"><span data-stu-id="4f141-105">Indicates the receipt status for messages that request receipts.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="4f141-106">Zugeordneten Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="4f141-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="4f141-107">PR_REPORT_DISPOSITION, PR_REPORT_DISPOSITION_A, PR_REPORT_DISPOSITION_W</span><span class="sxs-lookup"><span data-stu-id="4f141-107">PR_REPORT_DISPOSITION, PR_REPORT_DISPOSITION_A, PR_REPORT_DISPOSITION_W</span></span>  <br/> |
|<span data-ttu-id="4f141-108">Bezeichner:</span><span class="sxs-lookup"><span data-stu-id="4f141-108">Identifier:</span></span>  <br/> |<span data-ttu-id="4f141-109">0 x 0080</span><span class="sxs-lookup"><span data-stu-id="4f141-109">0x0080</span></span>  <br/> |
|<span data-ttu-id="4f141-110">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="4f141-110">Data type:</span></span>  <br/> |<span data-ttu-id="4f141-111">PT_STRING8, PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="4f141-111">PT_STRING8, PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="4f141-112">Bereich:</span><span class="sxs-lookup"><span data-stu-id="4f141-112">Area:</span></span>  <br/> |<span data-ttu-id="4f141-113">MAPI-Umschlag</span><span class="sxs-lookup"><span data-stu-id="4f141-113">MAPI envelope</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="4f141-114">Hinweise</span><span class="sxs-lookup"><span data-stu-id="4f141-114">Remarks</span></span>

<span data-ttu-id="4f141-115">Die folgenden Werte sind gültig:</span><span class="sxs-lookup"><span data-stu-id="4f141-115">The following are valid values:</span></span>
  
- <span data-ttu-id="4f141-116">"gelöscht"</span><span class="sxs-lookup"><span data-stu-id="4f141-116">"deleted"</span></span>
    
- <span data-ttu-id="4f141-117">"verarbeitet"</span><span class="sxs-lookup"><span data-stu-id="4f141-117">"processed"</span></span>
    
- <span data-ttu-id="4f141-118">"verteilt"</span><span class="sxs-lookup"><span data-stu-id="4f141-118">"dispatched"</span></span>
    
- <span data-ttu-id="4f141-119">"verweigert."</span><span class="sxs-lookup"><span data-stu-id="4f141-119">"denied"</span></span>
    
- <span data-ttu-id="4f141-120">"failed"</span><span class="sxs-lookup"><span data-stu-id="4f141-120">"failed"</span></span>
    
## <a name="related-resources"></a><span data-ttu-id="4f141-121">Verwandte Ressourcen</span><span class="sxs-lookup"><span data-stu-id="4f141-121">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="4f141-122">Protokollspezifikationen</span><span class="sxs-lookup"><span data-stu-id="4f141-122">Protocol specifications</span></span>

<span data-ttu-id="4f141-123">[[MS-OXPROPS]]</span><span class="sxs-lookup"><span data-stu-id="4f141-123">[[MS-OXPROPS]]</span></span> 
  
> <span data-ttu-id="4f141-124">Bietet Verweise auf Verwandte Exchange Server-Spezifikationen.</span><span class="sxs-lookup"><span data-stu-id="4f141-124">Provides references to related Exchange Server protocol specifications.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="4f141-125">Header-Dateien</span><span class="sxs-lookup"><span data-stu-id="4f141-125">Header files</span></span>

<span data-ttu-id="4f141-126">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="4f141-126">Mapidefs.h</span></span>
  
> <span data-ttu-id="4f141-127">Enthält die Datentypdefinitionen.</span><span class="sxs-lookup"><span data-stu-id="4f141-127">Provides data type definitions.</span></span>
    
<span data-ttu-id="4f141-128">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="4f141-128">Mapitags.h</span></span>
  
> <span data-ttu-id="4f141-129">Enthält Definitionen von Eigenschaften, die als zugeordneten Eigenschaften aufgelistet.</span><span class="sxs-lookup"><span data-stu-id="4f141-129">Contains definitions of properties listed as associated properties.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="4f141-130">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="4f141-130">See also</span></span>



[<span data-ttu-id="4f141-131">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="4f141-131">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="4f141-132">Kanonische MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="4f141-132">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="4f141-133">Zuordnen von kanonischen Eigenschaftennamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="4f141-133">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="4f141-134">Zuordnen von MAPI-Namen zu kanonische Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="4f141-134">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

