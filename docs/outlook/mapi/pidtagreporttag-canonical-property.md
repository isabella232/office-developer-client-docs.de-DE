---
title: PidTagReportTag (kanonische Eigenschaft)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagReportTag
api_type:
- COM
ms.assetid: 581bf372-8705-4617-aaa4-a1d761eb9b58
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 870fbf2228206253261124907d6bd420f95fb7c1
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32331430"
---
# <a name="pidtagreporttag-canonical-property"></a><span data-ttu-id="f554d-103">PidTagReportTag (kanonische Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="f554d-103">PidTagReportTag Canonical Property</span></span>

  
  
<span data-ttu-id="f554d-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="f554d-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="f554d-105">Enthält einen binären Tagwert, den das Messagingsystem in einen für die Nachricht generierten Bericht kopieren soll.</span><span class="sxs-lookup"><span data-stu-id="f554d-105">Contains a binary tag value that the messaging system should copy to any report generated for the message.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="f554d-106">Zugeordnete Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="f554d-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="f554d-107">PR_REPORT_TAG</span><span class="sxs-lookup"><span data-stu-id="f554d-107">PR_REPORT_TAG</span></span>  <br/> |
|<span data-ttu-id="f554d-108">Kennung:</span><span class="sxs-lookup"><span data-stu-id="f554d-108">Identifier:</span></span>  <br/> |<span data-ttu-id="f554d-109">0x0031</span><span class="sxs-lookup"><span data-stu-id="f554d-109">0x0031</span></span>  <br/> |
|<span data-ttu-id="f554d-110">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="f554d-110">Data type:</span></span>  <br/> |<span data-ttu-id="f554d-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="f554d-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="f554d-112">Bereich:</span><span class="sxs-lookup"><span data-stu-id="f554d-112">Area:</span></span>  <br/> |<span data-ttu-id="f554d-113">MAPI-Umschlag</span><span class="sxs-lookup"><span data-stu-id="f554d-113">MAPI envelope</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="f554d-114">Hinweise</span><span class="sxs-lookup"><span data-stu-id="f554d-114">Remarks</span></span>

<span data-ttu-id="f554d-115">Diese Eigenschaft, wie die **PR_SUBJECT_IPM** ([PidTagSubjectMessageId](pidtagsubjectmessageid-canonical-property.md)) -Eigenschaft, wird verwendet, um einen Bericht mit der ursprünglichen Nachricht zu korrelieren.</span><span class="sxs-lookup"><span data-stu-id="f554d-115">This property, like the **PR_SUBJECT_IPM** ([PidTagSubjectMessageId](pidtagsubjectmessageid-canonical-property.md)) property, is used to correlate a report with the original message.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="f554d-116">Verwandte Ressourcen</span><span class="sxs-lookup"><span data-stu-id="f554d-116">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="f554d-117">Protokollspezifikationen</span><span class="sxs-lookup"><span data-stu-id="f554d-117">Protocol specifications</span></span>

<span data-ttu-id="f554d-118">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="f554d-118">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="f554d-119">Enthält Verweise auf Exchange Server Protokollspezifikationen.</span><span class="sxs-lookup"><span data-stu-id="f554d-119">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="f554d-120">[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="f554d-120">[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="f554d-121">Gibt die Eigenschaften und Vorgänge an, die für E-Mail-Nachrichten zulässig sind.</span><span class="sxs-lookup"><span data-stu-id="f554d-121">Specifies the properties and operations that are permissible on email messages.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="f554d-122">Headerdateien</span><span class="sxs-lookup"><span data-stu-id="f554d-122">Header files</span></span>

<span data-ttu-id="f554d-123">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="f554d-123">Mapidefs.h</span></span>
  
> <span data-ttu-id="f554d-124">Bietet Datentypdefinitionen.</span><span class="sxs-lookup"><span data-stu-id="f554d-124">Provides data type definitions.</span></span>
    
<span data-ttu-id="f554d-125">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="f554d-125">Mapitags.h</span></span>
  
> <span data-ttu-id="f554d-126">Enthält Definitionen von Eigenschaften, die als alternative Namen aufgeführt sind.</span><span class="sxs-lookup"><span data-stu-id="f554d-126">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="f554d-127">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="f554d-127">See also</span></span>



[<span data-ttu-id="f554d-128">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="f554d-128">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="f554d-129">KANONISCHE EIGENSCHAFTEN VON MAPI</span><span class="sxs-lookup"><span data-stu-id="f554d-129">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="f554d-130">Zuordnen kanonischer Eigenschaftsnamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="f554d-130">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="f554d-131">Zuordnen von MAPI-Namen zu kanonischen Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="f554d-131">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

