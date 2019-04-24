---
title: Kanonische Pidtagrtfsyncbodycount (-Eigenschaft
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagRtfSyncBodyCount
api_type:
- COM
ms.assetid: b7267be4-8d5c-4dc7-86b2-651e03e84f9b
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: 6f6e687412dfce1e5fcee6b4a4d64f3e5106455f
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32331255"
---
# <a name="pidtagrtfsyncbodycount-canonical-property"></a><span data-ttu-id="01c2b-103">Kanonische Pidtagrtfsyncbodycount (-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="01c2b-103">PidTagRtfSyncBodyCount Canonical Property</span></span>

  
  
<span data-ttu-id="01c2b-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="01c2b-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="01c2b-105">Enthält die Anzahl der signifikanten Zeichen des Nachrichtentexts.</span><span class="sxs-lookup"><span data-stu-id="01c2b-105">Contains a count of the significant characters of the message text.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="01c2b-106">Zugeordnete Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="01c2b-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="01c2b-107">PR_RTF_SYNC_BODY_COUNT</span><span class="sxs-lookup"><span data-stu-id="01c2b-107">PR_RTF_SYNC_BODY_COUNT</span></span>  <br/> |
|<span data-ttu-id="01c2b-108">Kennung:</span><span class="sxs-lookup"><span data-stu-id="01c2b-108">Identifier:</span></span>  <br/> |<span data-ttu-id="01c2b-109">0x1007</span><span class="sxs-lookup"><span data-stu-id="01c2b-109">0x1007</span></span>  <br/> |
|<span data-ttu-id="01c2b-110">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="01c2b-110">Data type:</span></span>  <br/> |<span data-ttu-id="01c2b-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="01c2b-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="01c2b-112">Bereich:</span><span class="sxs-lookup"><span data-stu-id="01c2b-112">Area:</span></span>  <br/> |<span data-ttu-id="01c2b-113">MAPI-Nachricht</span><span class="sxs-lookup"><span data-stu-id="01c2b-113">MAPI message</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="01c2b-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="01c2b-114">Remarks</span></span>

<span data-ttu-id="01c2b-115">Die [RTFSync](rtfsync.md) -Funktion berechnet die Anzahl der Zeichen im Text nur mit denjenigen, die für die Nachricht als bedeutsam erachtet werden.</span><span class="sxs-lookup"><span data-stu-id="01c2b-115">The [RTFSync](rtfsync.md) function computes the count of characters in the text using only those that it considers to be significant to the message.</span></span> <span data-ttu-id="01c2b-116">Beispielsweise werden einige Leerraum und andere ignorierte Zeichen aus der Anzahl weggelassen.</span><span class="sxs-lookup"><span data-stu-id="01c2b-116">For example, some white space and other ignorable characters are omitted from the count.</span></span> 
  
<span data-ttu-id="01c2b-117">Diese Eigenschaft ist eine Hilfseigenschaft für Rich-Text-Format (RTF).</span><span class="sxs-lookup"><span data-stu-id="01c2b-117">This property is a Rich Text Format (RTF) auxiliary property.</span></span> <span data-ttu-id="01c2b-118">Diese Eigenschaften werden von der **RTFSync** -Funktion verwendet und sind nicht für die direkte Verwendung durch Clientanwendungen vorgesehen.</span><span class="sxs-lookup"><span data-stu-id="01c2b-118">These properties are used by the **RTFSync** function and are not intended to be used directly by client applications.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="01c2b-119">Zugehörige Ressourcen</span><span class="sxs-lookup"><span data-stu-id="01c2b-119">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="01c2b-120">Protokollspezifikationen</span><span class="sxs-lookup"><span data-stu-id="01c2b-120">Protocol specifications</span></span>

<span data-ttu-id="01c2b-121">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="01c2b-121">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="01c2b-122">Enthält Verweise auf zugehörige Exchange Server-Protokollspezifikationen.</span><span class="sxs-lookup"><span data-stu-id="01c2b-122">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="01c2b-123">[[MS-OXTNEF]](https://msdn.microsoft.com/library/1f0544d7-30b7-4194-b58f-adc82f3763bb%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="01c2b-123">[[MS-OXTNEF]](https://msdn.microsoft.com/library/1f0544d7-30b7-4194-b58f-adc82f3763bb%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="01c2b-124">Codiert und dekodiert Message-und Attachment-Objekte in einer effizienten Datenstrom Darstellung.</span><span class="sxs-lookup"><span data-stu-id="01c2b-124">Encodes and decodes message and attachment objects to an efficient stream representation.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="01c2b-125">Header Dateien</span><span class="sxs-lookup"><span data-stu-id="01c2b-125">Header files</span></span>

<span data-ttu-id="01c2b-126">Mapidefs. h</span><span class="sxs-lookup"><span data-stu-id="01c2b-126">Mapidefs.h</span></span>
  
> <span data-ttu-id="01c2b-127">Stellt Datentypdefinitionen bereit.</span><span class="sxs-lookup"><span data-stu-id="01c2b-127">Provides data type definitions.</span></span>
    
<span data-ttu-id="01c2b-128">Mapitags. h</span><span class="sxs-lookup"><span data-stu-id="01c2b-128">Mapitags.h</span></span>
  
> <span data-ttu-id="01c2b-129">Enthält Definitionen von Eigenschaften, die als Alternative Namen aufgeführt sind.</span><span class="sxs-lookup"><span data-stu-id="01c2b-129">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="01c2b-130">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="01c2b-130">See also</span></span>



[<span data-ttu-id="01c2b-131">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="01c2b-131">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="01c2b-132">Kanonische MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="01c2b-132">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="01c2b-133">Zuordnen von kanonischen Eigenschaftennamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="01c2b-133">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="01c2b-134">Zuordnen von MAPI-Namen zu kanonischen Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="01c2b-134">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

