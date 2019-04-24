---
title: Kanonische Pidtagreporttag (-Eigenschaft
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
ms.openlocfilehash: 870fbf2228206253261124907d6bd420f95fb7c1
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32331430"
---
# <a name="pidtagreporttag-canonical-property"></a><span data-ttu-id="8f44a-103">Kanonische Pidtagreporttag (-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="8f44a-103">PidTagReportTag Canonical Property</span></span>

  
  
<span data-ttu-id="8f44a-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="8f44a-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="8f44a-105">Enthält einen Binary-Tag-Wert, den das Messagingsystem in jeden Bericht kopieren sollte, der für die Nachricht generiert wurde.</span><span class="sxs-lookup"><span data-stu-id="8f44a-105">Contains a binary tag value that the messaging system should copy to any report generated for the message.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="8f44a-106">Zugeordnete Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="8f44a-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="8f44a-107">PR_REPORT_TAG</span><span class="sxs-lookup"><span data-stu-id="8f44a-107">PR_REPORT_TAG</span></span>  <br/> |
|<span data-ttu-id="8f44a-108">Kennung:</span><span class="sxs-lookup"><span data-stu-id="8f44a-108">Identifier:</span></span>  <br/> |<span data-ttu-id="8f44a-109">0x0031</span><span class="sxs-lookup"><span data-stu-id="8f44a-109">0x0031</span></span>  <br/> |
|<span data-ttu-id="8f44a-110">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="8f44a-110">Data type:</span></span>  <br/> |<span data-ttu-id="8f44a-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="8f44a-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="8f44a-112">Bereich:</span><span class="sxs-lookup"><span data-stu-id="8f44a-112">Area:</span></span>  <br/> |<span data-ttu-id="8f44a-113">MAPI-Umschlag</span><span class="sxs-lookup"><span data-stu-id="8f44a-113">MAPI envelope</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="8f44a-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="8f44a-114">Remarks</span></span>

<span data-ttu-id="8f44a-115">Diese Eigenschaft wird wie die **PR_SUBJECT_IPM** ([pidtagsubjectmessageid (](pidtagsubjectmessageid-canonical-property.md))-Eigenschaft verwendet, um einen Bericht mit der ursprünglichen Nachricht zu korrelieren.</span><span class="sxs-lookup"><span data-stu-id="8f44a-115">This property, like the **PR_SUBJECT_IPM** ([PidTagSubjectMessageId](pidtagsubjectmessageid-canonical-property.md)) property, is used to correlate a report with the original message.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="8f44a-116">Zugehörige Ressourcen</span><span class="sxs-lookup"><span data-stu-id="8f44a-116">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="8f44a-117">Protokollspezifikationen</span><span class="sxs-lookup"><span data-stu-id="8f44a-117">Protocol specifications</span></span>

<span data-ttu-id="8f44a-118">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="8f44a-118">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="8f44a-119">Enthält Verweise auf zugehörige Exchange Server-Protokollspezifikationen.</span><span class="sxs-lookup"><span data-stu-id="8f44a-119">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="8f44a-120">[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="8f44a-120">[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="8f44a-121">Gibt die Eigenschaften und Vorgänge an, die für e-Mail-Nachrichten zulässig sind.</span><span class="sxs-lookup"><span data-stu-id="8f44a-121">Specifies the properties and operations that are permissible on email messages.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="8f44a-122">Header Dateien</span><span class="sxs-lookup"><span data-stu-id="8f44a-122">Header files</span></span>

<span data-ttu-id="8f44a-123">Mapidefs. h</span><span class="sxs-lookup"><span data-stu-id="8f44a-123">Mapidefs.h</span></span>
  
> <span data-ttu-id="8f44a-124">Stellt Datentypdefinitionen bereit.</span><span class="sxs-lookup"><span data-stu-id="8f44a-124">Provides data type definitions.</span></span>
    
<span data-ttu-id="8f44a-125">Mapitags. h</span><span class="sxs-lookup"><span data-stu-id="8f44a-125">Mapitags.h</span></span>
  
> <span data-ttu-id="8f44a-126">Enthält Definitionen von Eigenschaften, die als Alternative Namen aufgeführt sind.</span><span class="sxs-lookup"><span data-stu-id="8f44a-126">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="8f44a-127">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="8f44a-127">See also</span></span>



[<span data-ttu-id="8f44a-128">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="8f44a-128">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="8f44a-129">Kanonische MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="8f44a-129">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="8f44a-130">Zuordnen von kanonischen Eigenschaftennamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="8f44a-130">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="8f44a-131">Zuordnen von MAPI-Namen zu kanonischen Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="8f44a-131">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

