---
title: PidTagReportTime (kanonische Eigenschaft)
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
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 4efe68745c10521de243677c10a9ca32debd7122
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2018
ms.locfileid: "22577800"
---
# <a name="pidtagreporttime-canonical-property"></a><span data-ttu-id="1fd01-103">PidTagReportTime (kanonische Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="1fd01-103">PidTagReportTime Canonical Property</span></span>

  
  
<span data-ttu-id="1fd01-104">**Betrifft**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="1fd01-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="1fd01-105">Enthält Datum und Uhrzeit, wann das messaging-System ein Bericht erstellt.</span><span class="sxs-lookup"><span data-stu-id="1fd01-105">Contains the date and time when the messaging system generated a report.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="1fd01-106">Zugeordnete Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="1fd01-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="1fd01-107">PR_REPORT_TIME</span><span class="sxs-lookup"><span data-stu-id="1fd01-107">PR_REPORT_TIME</span></span>  <br/> |
|<span data-ttu-id="1fd01-108">Kennung:</span><span class="sxs-lookup"><span data-stu-id="1fd01-108">Identifier:</span></span>  <br/> |<span data-ttu-id="1fd01-109">0x0032</span><span class="sxs-lookup"><span data-stu-id="1fd01-109">0x0032</span></span>  <br/> |
|<span data-ttu-id="1fd01-110">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="1fd01-110">Data type:</span></span>  <br/> |<span data-ttu-id="1fd01-111">PT_SYSTIME</span><span class="sxs-lookup"><span data-stu-id="1fd01-111">PT_SYSTIME</span></span>  <br/> |
|<span data-ttu-id="1fd01-112">Bereich:</span><span class="sxs-lookup"><span data-stu-id="1fd01-112">Area:</span></span>  <br/> |<span data-ttu-id="1fd01-113">MAPI-Umschlag</span><span class="sxs-lookup"><span data-stu-id="1fd01-113">MAPI envelope</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="1fd01-114">HinwBemerkungeneise</span><span class="sxs-lookup"><span data-stu-id="1fd01-114">Remarks</span></span>

<span data-ttu-id="1fd01-115">Diese Eigenschaft stellt eine Eigenschaft pro Empfänger zur Übermittlung und Nondelivery Berichte und eine-Message-Eigenschaft für Berichte lesen und nonread dar.</span><span class="sxs-lookup"><span data-stu-id="1fd01-115">This property represents a per-recipient property on delivery and nondelivery reports and a per-message property on read and nonread reports.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="1fd01-116">Verwandte Ressourcen</span><span class="sxs-lookup"><span data-stu-id="1fd01-116">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="1fd01-117">Protokollspezifikationen</span><span class="sxs-lookup"><span data-stu-id="1fd01-117">Protocol specifications</span></span>

<span data-ttu-id="1fd01-118">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="1fd01-118">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="1fd01-119">Bietet Verweise auf Verwandte Exchange Server-Spezifikationen.</span><span class="sxs-lookup"><span data-stu-id="1fd01-119">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="1fd01-120">[[MS-OXOMSG]](http://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="1fd01-120">[[MS-OXOMSG]](http://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="1fd01-121">Gibt die Eigenschaften und Operationen, die für e-Mail-Nachrichten zulässig sind.</span><span class="sxs-lookup"><span data-stu-id="1fd01-121">Specifies the properties and operations that are permissible on email messages.</span></span>
    
<span data-ttu-id="1fd01-122">[[MS-OXCSPAM]](http://msdn.microsoft.com/library/522f8587-4aed-4cd6-831b-40bd87862189%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="1fd01-122">[[MS-OXCSPAM]](http://msdn.microsoft.com/library/522f8587-4aed-4cd6-831b-40bd87862189%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="1fd01-123">Ermöglicht die Behandlung von zulassen/blockieren-Listen und die Bestimmung des junk-e-Mail-Nachrichten.</span><span class="sxs-lookup"><span data-stu-id="1fd01-123">Enables the handling of allow/block lists and the determination of junk email messages.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="1fd01-124">Header-Dateien</span><span class="sxs-lookup"><span data-stu-id="1fd01-124">Header files</span></span>

<span data-ttu-id="1fd01-125">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="1fd01-125">Mapidefs.h</span></span>
  
> <span data-ttu-id="1fd01-126">Enthält die Datentypdefinitionen.</span><span class="sxs-lookup"><span data-stu-id="1fd01-126">Provides data type definitions.</span></span>
    
<span data-ttu-id="1fd01-127">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="1fd01-127">Mapitags.h</span></span>
  
> <span data-ttu-id="1fd01-128">Enthält Definitionen von Eigenschaften, die als Alternative Namen aufgelistet.</span><span class="sxs-lookup"><span data-stu-id="1fd01-128">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="1fd01-129">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="1fd01-129">See also</span></span>



[<span data-ttu-id="1fd01-130">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="1fd01-130">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="1fd01-131">Kanonische MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="1fd01-131">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="1fd01-132">Zuordnen von kanonischen Eigenschaftennamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="1fd01-132">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="1fd01-133">Zuordnen von MAPI-Namen zu kanonische Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="1fd01-133">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

