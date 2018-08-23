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
ms.openlocfilehash: 9b16cf3b8d0281ba8995058af6b18dbe22dcf592
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2018
ms.locfileid: "22566117"
---
# <a name="pidtagreportdispositionmode-canonical-property"></a><span data-ttu-id="41b7a-103">PidTagReportDispositionMode (kanonische Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="41b7a-103">PidTagReportDispositionMode Canonical Property</span></span>

  
  
<span data-ttu-id="41b7a-104">**Betrifft**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="41b7a-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="41b7a-105">Zeigt die Disposition des Eingangs für Nachrichten, die Empfangsbestätigungen anfordern.</span><span class="sxs-lookup"><span data-stu-id="41b7a-105">Indicates the disposition of the receipt for messages that request receipts.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="41b7a-106">Zugeordnete Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="41b7a-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="41b7a-107">PR_REPORT_DISPOSITION_MODE, PR_REPORT_DISPOSITION_MODE_A, PR_REPORT_DISPOSITION_MODE_W</span><span class="sxs-lookup"><span data-stu-id="41b7a-107">PR_REPORT_DISPOSITION_MODE, PR_REPORT_DISPOSITION_MODE_A, PR_REPORT_DISPOSITION_MODE_W</span></span>  <br/> |
|<span data-ttu-id="41b7a-108">Kennung:</span><span class="sxs-lookup"><span data-stu-id="41b7a-108">Identifier:</span></span>  <br/> |<span data-ttu-id="41b7a-109">0x0081</span><span class="sxs-lookup"><span data-stu-id="41b7a-109">0x0081</span></span>  <br/> |
|<span data-ttu-id="41b7a-110">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="41b7a-110">Data type:</span></span>  <br/> |<span data-ttu-id="41b7a-111">PT_STRING8, PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="41b7a-111">PT_STRING8, PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="41b7a-112">Bereich:</span><span class="sxs-lookup"><span data-stu-id="41b7a-112">Area:</span></span>  <br/> |<span data-ttu-id="41b7a-113">MAPI-Umschlag</span><span class="sxs-lookup"><span data-stu-id="41b7a-113">MAPI envelope</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="41b7a-114">HinwBemerkungeneise</span><span class="sxs-lookup"><span data-stu-id="41b7a-114">Remarks</span></span>

<span data-ttu-id="41b7a-115">Die möglichen Werte für diese Eigenschaft sind "manuell-Aktion/MDN-gesendet-automatisch" und "manuell-Aktion/MDN-gesendet-manuell".</span><span class="sxs-lookup"><span data-stu-id="41b7a-115">The possible values for this property are "manual-action/MDN-sent-automatically" and "manual-action/MDN-sent-manually".</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="41b7a-116">Verwandte Ressourcen</span><span class="sxs-lookup"><span data-stu-id="41b7a-116">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="41b7a-117">Protokollspezifikationen</span><span class="sxs-lookup"><span data-stu-id="41b7a-117">Protocol specifications</span></span>

<span data-ttu-id="41b7a-118">[[MS-OXPROPS]]</span><span class="sxs-lookup"><span data-stu-id="41b7a-118">[[MS-OXPROPS]]</span></span> 
  
> <span data-ttu-id="41b7a-119">Bietet Verweise auf Verwandte Exchange Server-Spezifikationen.</span><span class="sxs-lookup"><span data-stu-id="41b7a-119">Provides references to related Exchange Server protocol specifications.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="41b7a-120">Header-Dateien</span><span class="sxs-lookup"><span data-stu-id="41b7a-120">Header files</span></span>

<span data-ttu-id="41b7a-121">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="41b7a-121">Mapidefs.h</span></span>
  
> <span data-ttu-id="41b7a-122">Enthält die Datentypdefinitionen.</span><span class="sxs-lookup"><span data-stu-id="41b7a-122">Provides data type definitions.</span></span>
    
<span data-ttu-id="41b7a-123">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="41b7a-123">Mapitags.h</span></span>
  
> <span data-ttu-id="41b7a-124">Enthält Definitionen von Eigenschaften, die als zugeordneten Eigenschaften aufgelistet.</span><span class="sxs-lookup"><span data-stu-id="41b7a-124">Contains definitions of properties listed as associated properties.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="41b7a-125">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="41b7a-125">See also</span></span>



[<span data-ttu-id="41b7a-126">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="41b7a-126">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="41b7a-127">Kanonische MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="41b7a-127">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="41b7a-128">Zuordnen von kanonischen Eigenschaftennamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="41b7a-128">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="41b7a-129">Zuordnen von MAPI-Namen zu kanonische Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="41b7a-129">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

