---
title: PidTagRoamingBinary (kanonische Eigenschaft)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: f06bf063-fc95-46f9-b5fa-3f127a59ebda
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 717c456024dd98495550f1377edc6a53f82ee042
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2018
ms.locfileid: "22572410"
---
# <a name="pidtagroamingbinary-canonical-property"></a><span data-ttu-id="bd1d6-103">PidTagRoamingBinary (kanonische Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="bd1d6-103">PidTagRoamingBinary Canonical Property</span></span>

  
  
<span data-ttu-id="bd1d6-104">**Betrifft**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="bd1d6-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="bd1d6-105">Enthält eine Nachrichtendatenstrom eine Unterklasse der der **IPM zugeordnet. Konfiguration** Klasse.</span><span class="sxs-lookup"><span data-stu-id="bd1d6-105">Contains a message stream associated with a subclass of the **IPM.Configuration** class.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="bd1d6-106">Zugeordnete Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="bd1d6-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="bd1d6-107">PR_ROAMING_BINARYSTREAM</span><span class="sxs-lookup"><span data-stu-id="bd1d6-107">PR_ROAMING_BINARYSTREAM</span></span>  <br/> |
|<span data-ttu-id="bd1d6-108">Kennung:</span><span class="sxs-lookup"><span data-stu-id="bd1d6-108">Identifier:</span></span>  <br/> |<span data-ttu-id="bd1d6-109">0x7C09</span><span class="sxs-lookup"><span data-stu-id="bd1d6-109">0x7C09</span></span>  <br/> |
|<span data-ttu-id="bd1d6-110">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="bd1d6-110">Data type:</span></span>  <br/> |<span data-ttu-id="bd1d6-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="bd1d6-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="bd1d6-112">Bereich:</span><span class="sxs-lookup"><span data-stu-id="bd1d6-112">Area:</span></span>  <br/> |<span data-ttu-id="bd1d6-113">Konfiguration</span><span class="sxs-lookup"><span data-stu-id="bd1d6-113">Configuration</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="bd1d6-114">HinwBemerkungeneise</span><span class="sxs-lookup"><span data-stu-id="bd1d6-114">Remarks</span></span>

<span data-ttu-id="bd1d6-115">Diese Eigenschaft enthält den Datenstrom ein **IPM zugeordnet. Konfiguration** Nachricht-Klasse.</span><span class="sxs-lookup"><span data-stu-id="bd1d6-115">This property contains the data stream associated with an **IPM.Configuration** message class message.</span></span> <span data-ttu-id="bd1d6-116">Das Format des Stream-Objekts hängt von der Nachrichtenklasse ab.</span><span class="sxs-lookup"><span data-stu-id="bd1d6-116">The format of the stream depends on the message class.</span></span> <span data-ttu-id="bd1d6-117">Beispielsweise eine Nachricht vom Typ der Klasse **IPM. Configuration.Autocomplete** als [AutoVervollständigen Stream](autocomplete-stream.md)formatiert.</span><span class="sxs-lookup"><span data-stu-id="bd1d6-117">For instance, a message of class type **IPM.Configuration.Autocomplete** would be formatted as an [Autocomplete Stream](autocomplete-stream.md).</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="bd1d6-118">Verwandte Ressourcen</span><span class="sxs-lookup"><span data-stu-id="bd1d6-118">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="bd1d6-119">Protokollspezifikationen</span><span class="sxs-lookup"><span data-stu-id="bd1d6-119">Protocol specifications</span></span>

<span data-ttu-id="bd1d6-120">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="bd1d6-120">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="bd1d6-121">Bietet Verweise auf Verwandte Spezifikationen von Microsoft Exchange Server-Protokoll.</span><span class="sxs-lookup"><span data-stu-id="bd1d6-121">Provides references to related Microsoft Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="bd1d6-122">[[MS-OXOCFG]](http://msdn.microsoft.com/library/7d466dd5-c156-4da9-9a01-75c78e7e1a67%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="bd1d6-122">[[MS-OXOCFG]](http://msdn.microsoft.com/library/7d466dd5-c156-4da9-9a01-75c78e7e1a67%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="bd1d6-123">Gibt den Speicherort und die Eigenschaften von Client- und Konfigurationsdaten, wie etwa freigegebene Kategorielisten und Arbeitszeiten.</span><span class="sxs-lookup"><span data-stu-id="bd1d6-123">Specifies the location and properties of client and server configuration data, such as shared category lists and working hours.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="bd1d6-124">Header-Dateien</span><span class="sxs-lookup"><span data-stu-id="bd1d6-124">Header files</span></span>

<span data-ttu-id="bd1d6-125">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="bd1d6-125">Mapidefs.h</span></span>
  
> <span data-ttu-id="bd1d6-126">Enthält die Datentypdefinitionen.</span><span class="sxs-lookup"><span data-stu-id="bd1d6-126">Provides data type definitions.</span></span>
    
<span data-ttu-id="bd1d6-127">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="bd1d6-127">Mapitags.h</span></span>
  
> <span data-ttu-id="bd1d6-128">Enthält Definitionen von Eigenschaften, die als zugeordneten Eigenschaften aufgelistet.</span><span class="sxs-lookup"><span data-stu-id="bd1d6-128">Contains definitions of properties listed as associated properties.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="bd1d6-129">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="bd1d6-129">See also</span></span>



[<span data-ttu-id="bd1d6-130">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="bd1d6-130">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="bd1d6-131">Kanonische MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="bd1d6-131">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="bd1d6-132">Zuordnen von kanonischen Eigenschaftennamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="bd1d6-132">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="bd1d6-133">Zuordnen von MAPI-Namen zu kanonische Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="bd1d6-133">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

