---
title: Kanonische PidTagReportTag-Eigenschaft
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
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: c832842568ea3d64d50b56d226b66d551402ba6e
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19794975"
---
# <a name="pidtagreporttag-canonical-property"></a><span data-ttu-id="82ad6-103">Kanonische PidTagReportTag-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="82ad6-103">PidTagReportTag Canonical Property</span></span>

  
  
<span data-ttu-id="82ad6-104">**Betrifft**: Outlook</span><span class="sxs-lookup"><span data-stu-id="82ad6-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="82ad6-105">Enthält einen binären Tagwert, den das messaging-System auf einen Bericht für die Nachricht generierte kopieren soll.</span><span class="sxs-lookup"><span data-stu-id="82ad6-105">Contains a binary tag value that the messaging system should copy to any report generated for the message.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="82ad6-106">Zugeordneten Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="82ad6-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="82ad6-107">PR_REPORT_TAG</span><span class="sxs-lookup"><span data-stu-id="82ad6-107">PR_REPORT_TAG</span></span>  <br/> |
|<span data-ttu-id="82ad6-108">Bezeichner:</span><span class="sxs-lookup"><span data-stu-id="82ad6-108">Identifier:</span></span>  <br/> |<span data-ttu-id="82ad6-109">0x0031</span><span class="sxs-lookup"><span data-stu-id="82ad6-109">0x0031</span></span>  <br/> |
|<span data-ttu-id="82ad6-110">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="82ad6-110">Data type:</span></span>  <br/> |<span data-ttu-id="82ad6-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="82ad6-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="82ad6-112">Bereich:</span><span class="sxs-lookup"><span data-stu-id="82ad6-112">Area:</span></span>  <br/> |<span data-ttu-id="82ad6-113">MAPI-Umschlag</span><span class="sxs-lookup"><span data-stu-id="82ad6-113">MAPI envelope</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="82ad6-114">Hinweise</span><span class="sxs-lookup"><span data-stu-id="82ad6-114">Remarks</span></span>

<span data-ttu-id="82ad6-115">Diese Eigenschaft, wie die Eigenschaft **PR_SUBJECT_IPM** ([PidTagSubjectMessageId](pidtagsubjectmessageid-canonical-property.md)) wird verwendet, um einen Bericht mit der ursprünglichen Nachricht zu korrelieren.</span><span class="sxs-lookup"><span data-stu-id="82ad6-115">This property, like the **PR_SUBJECT_IPM** ([PidTagSubjectMessageId](pidtagsubjectmessageid-canonical-property.md)) property, is used to correlate a report with the original message.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="82ad6-116">Verwandte Ressourcen</span><span class="sxs-lookup"><span data-stu-id="82ad6-116">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="82ad6-117">Protokollspezifikationen</span><span class="sxs-lookup"><span data-stu-id="82ad6-117">Protocol specifications</span></span>

<span data-ttu-id="82ad6-118">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="82ad6-118">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="82ad6-119">Bietet Verweise auf Verwandte Exchange Server-Spezifikationen.</span><span class="sxs-lookup"><span data-stu-id="82ad6-119">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="82ad6-120">[[MS-OXOMSG]](http://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="82ad6-120">[[MS-OXOMSG]](http://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="82ad6-121">Gibt die Eigenschaften und Operationen, die für e-Mail-Nachrichten zulässig sind.</span><span class="sxs-lookup"><span data-stu-id="82ad6-121">Specifies the properties and operations that are permissible on email messages.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="82ad6-122">Header-Dateien</span><span class="sxs-lookup"><span data-stu-id="82ad6-122">Header files</span></span>

<span data-ttu-id="82ad6-123">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="82ad6-123">Mapidefs.h</span></span>
  
> <span data-ttu-id="82ad6-124">Enthält die Datentypdefinitionen.</span><span class="sxs-lookup"><span data-stu-id="82ad6-124">Provides data type definitions.</span></span>
    
<span data-ttu-id="82ad6-125">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="82ad6-125">Mapitags.h</span></span>
  
> <span data-ttu-id="82ad6-126">Enthält Definitionen von Eigenschaften, die als Alternative Namen aufgelistet.</span><span class="sxs-lookup"><span data-stu-id="82ad6-126">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="82ad6-127">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="82ad6-127">See also</span></span>



[<span data-ttu-id="82ad6-128">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="82ad6-128">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="82ad6-129">Kanonische MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="82ad6-129">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="82ad6-130">Zuordnen von kanonischen Eigenschaftennamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="82ad6-130">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="82ad6-131">Zuordnen von MAPI-Namen zu kanonische Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="82ad6-131">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

