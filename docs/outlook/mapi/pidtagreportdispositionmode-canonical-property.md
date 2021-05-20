---
title: PidTagReportDispositionMode (kanonische Eigenschaft)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_type:
- COM
ms.assetid: 67b3c76a-f6f7-462b-955c-dc7b53e7e7eb
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 3d598337a4a66b6345b2f7c827b62a2ccd8af366
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33428970"
---
# <a name="pidtagreportdispositionmode-canonical-property"></a><span data-ttu-id="7ca50-103">PidTagReportDispositionMode (kanonische Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="7ca50-103">PidTagReportDispositionMode Canonical Property</span></span>

  
  
<span data-ttu-id="7ca50-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="7ca50-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="7ca50-105">Gibt die Disposition des Belegs für Nachrichten an, die Quittungen anfordern.</span><span class="sxs-lookup"><span data-stu-id="7ca50-105">Indicates the disposition of the receipt for messages that request receipts.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="7ca50-106">Zugeordnete Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="7ca50-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="7ca50-107">PR_REPORT_DISPOSITION_MODE, PR_REPORT_DISPOSITION_MODE_A, PR_REPORT_DISPOSITION_MODE_W</span><span class="sxs-lookup"><span data-stu-id="7ca50-107">PR_REPORT_DISPOSITION_MODE, PR_REPORT_DISPOSITION_MODE_A, PR_REPORT_DISPOSITION_MODE_W</span></span>  <br/> |
|<span data-ttu-id="7ca50-108">Kennung:</span><span class="sxs-lookup"><span data-stu-id="7ca50-108">Identifier:</span></span>  <br/> |<span data-ttu-id="7ca50-109">0x0081</span><span class="sxs-lookup"><span data-stu-id="7ca50-109">0x0081</span></span>  <br/> |
|<span data-ttu-id="7ca50-110">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="7ca50-110">Data type:</span></span>  <br/> |<span data-ttu-id="7ca50-111">PT_STRING8, PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="7ca50-111">PT_STRING8, PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="7ca50-112">Bereich:</span><span class="sxs-lookup"><span data-stu-id="7ca50-112">Area:</span></span>  <br/> |<span data-ttu-id="7ca50-113">MAPI-Umschlag</span><span class="sxs-lookup"><span data-stu-id="7ca50-113">MAPI envelope</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="7ca50-114">Hinweise</span><span class="sxs-lookup"><span data-stu-id="7ca50-114">Remarks</span></span>

<span data-ttu-id="7ca50-115">Die möglichen Werte für diese Eigenschaft sind "manual-action/MDN-sent-automatically" und "manual-action/MDN-sent-manually".</span><span class="sxs-lookup"><span data-stu-id="7ca50-115">The possible values for this property are "manual-action/MDN-sent-automatically" and "manual-action/MDN-sent-manually".</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="7ca50-116">Verwandte Ressourcen</span><span class="sxs-lookup"><span data-stu-id="7ca50-116">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="7ca50-117">Protokollspezifikationen</span><span class="sxs-lookup"><span data-stu-id="7ca50-117">Protocol specifications</span></span>

<span data-ttu-id="7ca50-118">[[MS-OXPROPS]]</span><span class="sxs-lookup"><span data-stu-id="7ca50-118">[[MS-OXPROPS]]</span></span> 
  
> <span data-ttu-id="7ca50-119">Enthält Verweise auf Exchange Server Protokollspezifikationen.</span><span class="sxs-lookup"><span data-stu-id="7ca50-119">Provides references to related Exchange Server protocol specifications.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="7ca50-120">Headerdateien</span><span class="sxs-lookup"><span data-stu-id="7ca50-120">Header files</span></span>

<span data-ttu-id="7ca50-121">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="7ca50-121">Mapidefs.h</span></span>
  
> <span data-ttu-id="7ca50-122">Bietet Datentypdefinitionen.</span><span class="sxs-lookup"><span data-stu-id="7ca50-122">Provides data type definitions.</span></span>
    
<span data-ttu-id="7ca50-123">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="7ca50-123">Mapitags.h</span></span>
  
> <span data-ttu-id="7ca50-124">Enthält Definitionen von Eigenschaften, die als zugeordnete Eigenschaften aufgeführt sind.</span><span class="sxs-lookup"><span data-stu-id="7ca50-124">Contains definitions of properties listed as associated properties.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="7ca50-125">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="7ca50-125">See also</span></span>



[<span data-ttu-id="7ca50-126">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="7ca50-126">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="7ca50-127">KANONISCHE EIGENSCHAFTEN VON MAPI</span><span class="sxs-lookup"><span data-stu-id="7ca50-127">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="7ca50-128">Zuordnen kanonischer Eigenschaftsnamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="7ca50-128">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="7ca50-129">Zuordnen von MAPI-Namen zu kanonischen Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="7ca50-129">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

