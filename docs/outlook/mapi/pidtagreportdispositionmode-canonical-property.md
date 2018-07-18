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
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: bc2d577ad6c6b430c2339dfb0567ca56de0a7f8e
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19794963"
---
# <a name="pidtagreportdispositionmode-canonical-property"></a><span data-ttu-id="737e1-103">PidTagReportDispositionMode (kanonische Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="737e1-103">PidTagReportDispositionMode Canonical Property</span></span>

  
  
<span data-ttu-id="737e1-104">**Betrifft**: Outlook</span><span class="sxs-lookup"><span data-stu-id="737e1-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="737e1-105">Zeigt die Disposition des Eingangs für Nachrichten, die Empfangsbestätigungen anfordern.</span><span class="sxs-lookup"><span data-stu-id="737e1-105">Indicates the disposition of the receipt for messages that request receipts.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="737e1-106">Zugeordneten Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="737e1-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="737e1-107">PR_REPORT_DISPOSITION_MODE, PR_REPORT_DISPOSITION_MODE_A, PR_REPORT_DISPOSITION_MODE_W</span><span class="sxs-lookup"><span data-stu-id="737e1-107">PR_REPORT_DISPOSITION_MODE, PR_REPORT_DISPOSITION_MODE_A, PR_REPORT_DISPOSITION_MODE_W</span></span>  <br/> |
|<span data-ttu-id="737e1-108">Bezeichner:</span><span class="sxs-lookup"><span data-stu-id="737e1-108">Identifier:</span></span>  <br/> |<span data-ttu-id="737e1-109">0x0081</span><span class="sxs-lookup"><span data-stu-id="737e1-109">0x0081</span></span>  <br/> |
|<span data-ttu-id="737e1-110">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="737e1-110">Data type:</span></span>  <br/> |<span data-ttu-id="737e1-111">PT_STRING8, PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="737e1-111">PT_STRING8, PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="737e1-112">Bereich:</span><span class="sxs-lookup"><span data-stu-id="737e1-112">Area:</span></span>  <br/> |<span data-ttu-id="737e1-113">MAPI-Umschlag</span><span class="sxs-lookup"><span data-stu-id="737e1-113">MAPI envelope</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="737e1-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="737e1-114">Remarks</span></span>

<span data-ttu-id="737e1-115">Die möglichen Werte für diese Eigenschaft sind "manuell-Aktion/MDN-gesendet-automatisch" und "manuell-Aktion/MDN-gesendet-manuell".</span><span class="sxs-lookup"><span data-stu-id="737e1-115">The possible values for this property are "manual-action/MDN-sent-automatically" and "manual-action/MDN-sent-manually".</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="737e1-116">Verwandte Ressourcen</span><span class="sxs-lookup"><span data-stu-id="737e1-116">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="737e1-117">Protokollspezifikationen</span><span class="sxs-lookup"><span data-stu-id="737e1-117">Protocol specifications</span></span>

<span data-ttu-id="737e1-118">[[MS-OXPROPS]]</span><span class="sxs-lookup"><span data-stu-id="737e1-118">[[MS-OXPROPS]]</span></span> 
  
> <span data-ttu-id="737e1-119">Bietet Verweise auf Verwandte Exchange Server-Spezifikationen.</span><span class="sxs-lookup"><span data-stu-id="737e1-119">Provides references to related Exchange Server protocol specifications.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="737e1-120">Header-Dateien</span><span class="sxs-lookup"><span data-stu-id="737e1-120">Header files</span></span>

<span data-ttu-id="737e1-121">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="737e1-121">Mapidefs.h</span></span>
  
> <span data-ttu-id="737e1-122">Enthält die Datentypdefinitionen.</span><span class="sxs-lookup"><span data-stu-id="737e1-122">Provides data type definitions.</span></span>
    
<span data-ttu-id="737e1-123">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="737e1-123">Mapitags.h</span></span>
  
> <span data-ttu-id="737e1-124">Enthält Definitionen von Eigenschaften, die als zugeordneten Eigenschaften aufgelistet.</span><span class="sxs-lookup"><span data-stu-id="737e1-124">Contains definitions of properties listed as associated properties.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="737e1-125">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="737e1-125">See also</span></span>



[<span data-ttu-id="737e1-126">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="737e1-126">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="737e1-127">Kanonische MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="737e1-127">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="737e1-128">Zuordnen von kanonischen Eigenschaftennamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="737e1-128">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="737e1-129">Zuordnen von MAPI-Namen zu kanonische Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="737e1-129">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

