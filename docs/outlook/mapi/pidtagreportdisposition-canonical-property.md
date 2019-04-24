---
title: Kanonische Pidtagreportdisposition (-Eigenschaft
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
ms.openlocfilehash: dae31959cddad7ad61ea32f2372ea34bdbff658e
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32346354"
---
# <a name="pidtagreportdisposition-canonical-property"></a><span data-ttu-id="29cf6-103">Kanonische Pidtagreportdisposition (-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="29cf6-103">PidTagReportDisposition Canonical Property</span></span>

  
  
<span data-ttu-id="29cf6-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="29cf6-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="29cf6-105">Gibt den Bestätigungsstatus für Nachrichten an, die Empfangsbestätigungen anfordern.</span><span class="sxs-lookup"><span data-stu-id="29cf6-105">Indicates the receipt status for messages that request receipts.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="29cf6-106">Zugeordnete Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="29cf6-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="29cf6-107">PR_REPORT_DISPOSITION, PR_REPORT_DISPOSITION_A, PR_REPORT_DISPOSITION_W</span><span class="sxs-lookup"><span data-stu-id="29cf6-107">PR_REPORT_DISPOSITION, PR_REPORT_DISPOSITION_A, PR_REPORT_DISPOSITION_W</span></span>  <br/> |
|<span data-ttu-id="29cf6-108">Kennung:</span><span class="sxs-lookup"><span data-stu-id="29cf6-108">Identifier:</span></span>  <br/> |<span data-ttu-id="29cf6-109">0x0080</span><span class="sxs-lookup"><span data-stu-id="29cf6-109">0x0080</span></span>  <br/> |
|<span data-ttu-id="29cf6-110">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="29cf6-110">Data type:</span></span>  <br/> |<span data-ttu-id="29cf6-111">PT_STRING8, PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="29cf6-111">PT_STRING8, PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="29cf6-112">Bereich:</span><span class="sxs-lookup"><span data-stu-id="29cf6-112">Area:</span></span>  <br/> |<span data-ttu-id="29cf6-113">MAPI-Umschlag</span><span class="sxs-lookup"><span data-stu-id="29cf6-113">MAPI envelope</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="29cf6-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="29cf6-114">Remarks</span></span>

<span data-ttu-id="29cf6-115">Die gültigen Werte lauten:</span><span class="sxs-lookup"><span data-stu-id="29cf6-115">The following are valid values:</span></span>
  
- <span data-ttu-id="29cf6-116">gelöscht</span><span class="sxs-lookup"><span data-stu-id="29cf6-116">"deleted"</span></span>
    
- <span data-ttu-id="29cf6-117">verarbeitet</span><span class="sxs-lookup"><span data-stu-id="29cf6-117">"processed"</span></span>
    
- <span data-ttu-id="29cf6-118">versandt</span><span class="sxs-lookup"><span data-stu-id="29cf6-118">"dispatched"</span></span>
    
- <span data-ttu-id="29cf6-119">verweigert</span><span class="sxs-lookup"><span data-stu-id="29cf6-119">"denied"</span></span>
    
- <span data-ttu-id="29cf6-120">"failed"</span><span class="sxs-lookup"><span data-stu-id="29cf6-120">"failed"</span></span>
    
## <a name="related-resources"></a><span data-ttu-id="29cf6-121">Zugehörige Ressourcen</span><span class="sxs-lookup"><span data-stu-id="29cf6-121">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="29cf6-122">Protokollspezifikationen</span><span class="sxs-lookup"><span data-stu-id="29cf6-122">Protocol specifications</span></span>

<span data-ttu-id="29cf6-123">[[MS-OXPROPS]]</span><span class="sxs-lookup"><span data-stu-id="29cf6-123">[[MS-OXPROPS]]</span></span> 
  
> <span data-ttu-id="29cf6-124">Enthält Verweise auf zugehörige Exchange Server-Protokollspezifikationen.</span><span class="sxs-lookup"><span data-stu-id="29cf6-124">Provides references to related Exchange Server protocol specifications.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="29cf6-125">Header Dateien</span><span class="sxs-lookup"><span data-stu-id="29cf6-125">Header files</span></span>

<span data-ttu-id="29cf6-126">Mapidefs. h</span><span class="sxs-lookup"><span data-stu-id="29cf6-126">Mapidefs.h</span></span>
  
> <span data-ttu-id="29cf6-127">Stellt Datentypdefinitionen bereit.</span><span class="sxs-lookup"><span data-stu-id="29cf6-127">Provides data type definitions.</span></span>
    
<span data-ttu-id="29cf6-128">Mapitags. h</span><span class="sxs-lookup"><span data-stu-id="29cf6-128">Mapitags.h</span></span>
  
> <span data-ttu-id="29cf6-129">Enthält Definitionen von Eigenschaften, die als zugeordnete Eigenschaften aufgelistet sind.</span><span class="sxs-lookup"><span data-stu-id="29cf6-129">Contains definitions of properties listed as associated properties.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="29cf6-130">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="29cf6-130">See also</span></span>



[<span data-ttu-id="29cf6-131">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="29cf6-131">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="29cf6-132">Kanonische MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="29cf6-132">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="29cf6-133">Zuordnen von kanonischen Eigenschaftennamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="29cf6-133">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="29cf6-134">Zuordnen von MAPI-Namen zu kanonischen Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="29cf6-134">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

