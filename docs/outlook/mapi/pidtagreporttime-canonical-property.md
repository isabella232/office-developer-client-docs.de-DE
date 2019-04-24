---
title: Kanonische Pidtagreporttime (-Eigenschaft
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagReportTime
api_type:
- COM
ms.assetid: b3646505-a9f0-4a72-8277-b238c909f66f
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: 298c53e537819f800a3acc5cf07c01a7b9f978ec
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32330149"
---
# <a name="pidtagreporttime-canonical-property"></a><span data-ttu-id="53ed4-103">Kanonische Pidtagreporttime (-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="53ed4-103">PidTagReportTime Canonical Property</span></span>

  
  
<span data-ttu-id="53ed4-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="53ed4-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="53ed4-105">Enthält das Datum und die Uhrzeit, zu denen das Messagingsystem einen Bericht generiert hat.</span><span class="sxs-lookup"><span data-stu-id="53ed4-105">Contains the date and time when the messaging system generated a report.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="53ed4-106">Zugeordnete Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="53ed4-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="53ed4-107">PR_REPORT_TIME</span><span class="sxs-lookup"><span data-stu-id="53ed4-107">PR_REPORT_TIME</span></span>  <br/> |
|<span data-ttu-id="53ed4-108">Kennung:</span><span class="sxs-lookup"><span data-stu-id="53ed4-108">Identifier:</span></span>  <br/> |<span data-ttu-id="53ed4-109">0x0032</span><span class="sxs-lookup"><span data-stu-id="53ed4-109">0x0032</span></span>  <br/> |
|<span data-ttu-id="53ed4-110">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="53ed4-110">Data type:</span></span>  <br/> |<span data-ttu-id="53ed4-111">PT_SYSTIME</span><span class="sxs-lookup"><span data-stu-id="53ed4-111">PT_SYSTIME</span></span>  <br/> |
|<span data-ttu-id="53ed4-112">Bereich:</span><span class="sxs-lookup"><span data-stu-id="53ed4-112">Area:</span></span>  <br/> |<span data-ttu-id="53ed4-113">MAPI-Umschlag</span><span class="sxs-lookup"><span data-stu-id="53ed4-113">MAPI envelope</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="53ed4-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="53ed4-114">Remarks</span></span>

<span data-ttu-id="53ed4-115">Diese Eigenschaft stellt eine Eigenschaft pro Empfänger für Übermittlungs-und Unzustellbarkeitsberichte und eine Eigenschaft pro Nachricht für Lese-und nonread-Berichte dar.</span><span class="sxs-lookup"><span data-stu-id="53ed4-115">This property represents a per-recipient property on delivery and nondelivery reports and a per-message property on read and nonread reports.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="53ed4-116">Zugehörige Ressourcen</span><span class="sxs-lookup"><span data-stu-id="53ed4-116">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="53ed4-117">Protokollspezifikationen</span><span class="sxs-lookup"><span data-stu-id="53ed4-117">Protocol specifications</span></span>

<span data-ttu-id="53ed4-118">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="53ed4-118">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="53ed4-119">Enthält Verweise auf zugehörige Exchange Server-Protokollspezifikationen.</span><span class="sxs-lookup"><span data-stu-id="53ed4-119">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="53ed4-120">[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="53ed4-120">[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="53ed4-121">Gibt die Eigenschaften und Vorgänge an, die für e-Mail-Nachrichten zulässig sind.</span><span class="sxs-lookup"><span data-stu-id="53ed4-121">Specifies the properties and operations that are permissible on email messages.</span></span>
    
<span data-ttu-id="53ed4-122">[[MS-OXCSPAM]](https://msdn.microsoft.com/library/522f8587-4aed-4cd6-831b-40bd87862189%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="53ed4-122">[[MS-OXCSPAM]](https://msdn.microsoft.com/library/522f8587-4aed-4cd6-831b-40bd87862189%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="53ed4-123">Ermöglicht die Behandlung von Allow/Block-Listen und die Bestimmung von Junk-e-Mails.</span><span class="sxs-lookup"><span data-stu-id="53ed4-123">Enables the handling of allow/block lists and the determination of junk email messages.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="53ed4-124">Header Dateien</span><span class="sxs-lookup"><span data-stu-id="53ed4-124">Header files</span></span>

<span data-ttu-id="53ed4-125">Mapidefs. h</span><span class="sxs-lookup"><span data-stu-id="53ed4-125">Mapidefs.h</span></span>
  
> <span data-ttu-id="53ed4-126">Stellt Datentypdefinitionen bereit.</span><span class="sxs-lookup"><span data-stu-id="53ed4-126">Provides data type definitions.</span></span>
    
<span data-ttu-id="53ed4-127">Mapitags. h</span><span class="sxs-lookup"><span data-stu-id="53ed4-127">Mapitags.h</span></span>
  
> <span data-ttu-id="53ed4-128">Enthält Definitionen von Eigenschaften, die als Alternative Namen aufgeführt sind.</span><span class="sxs-lookup"><span data-stu-id="53ed4-128">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="53ed4-129">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="53ed4-129">See also</span></span>



[<span data-ttu-id="53ed4-130">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="53ed4-130">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="53ed4-131">Kanonische MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="53ed4-131">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="53ed4-132">Zuordnen von kanonischen Eigenschaftennamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="53ed4-132">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="53ed4-133">Zuordnen von MAPI-Namen zu kanonischen Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="53ed4-133">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

