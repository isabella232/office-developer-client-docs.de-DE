---
title: PidTagRtfSyncPrefixCount (kanonische Eigenschaft)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagRtfSyncPrefixCount
api_type:
- COM
ms.assetid: c2b15ac5-9e89-4ee2-812d-102d0b2ac56e
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 61683534504b7451f126591af149d11306cff1bd
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32357862"
---
# <a name="pidtagrtfsyncprefixcount-canonical-property"></a><span data-ttu-id="c55ac-103">PidTagRtfSyncPrefixCount (kanonische Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="c55ac-103">PidTagRtfSyncPrefixCount Canonical Property</span></span>

  
  
<span data-ttu-id="c55ac-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="c55ac-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="c55ac-105">Enthält eine Anzahl der ignorablen Zeichen, die vor den wichtigen Zeichen der Nachricht angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="c55ac-105">Contains a count of the ignorable characters that appear before the significant characters of the message.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="c55ac-106">Zugeordnete Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="c55ac-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="c55ac-107">PR_RTF_SYNC_PREFIX_COUNT</span><span class="sxs-lookup"><span data-stu-id="c55ac-107">PR_RTF_SYNC_PREFIX_COUNT</span></span>  <br/> |
|<span data-ttu-id="c55ac-108">Kennung:</span><span class="sxs-lookup"><span data-stu-id="c55ac-108">Identifier:</span></span>  <br/> |<span data-ttu-id="c55ac-109">0x1010</span><span class="sxs-lookup"><span data-stu-id="c55ac-109">0x1010</span></span>  <br/> |
|<span data-ttu-id="c55ac-110">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="c55ac-110">Data type:</span></span>  <br/> |<span data-ttu-id="c55ac-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="c55ac-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="c55ac-112">Bereich:</span><span class="sxs-lookup"><span data-stu-id="c55ac-112">Area:</span></span>  <br/> |<span data-ttu-id="c55ac-113">MAPI-Nachricht</span><span class="sxs-lookup"><span data-stu-id="c55ac-113">MAPI message</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="c55ac-114">Hinweise</span><span class="sxs-lookup"><span data-stu-id="c55ac-114">Remarks</span></span>

<span data-ttu-id="c55ac-115">Die Anzahl der Präfixzeichen enthält kein Leerzeichen.</span><span class="sxs-lookup"><span data-stu-id="c55ac-115">The count of prefix characters does not include white space.</span></span>
  
<span data-ttu-id="c55ac-116">Diese Eigenschaft ist eine Rich Text Format (RTF)-Hilfseigenschaft.</span><span class="sxs-lookup"><span data-stu-id="c55ac-116">This property is a Rich Text Format (RTF) auxiliary property.</span></span> <span data-ttu-id="c55ac-117">RTF-Hilfseigenschaften werden von der [RTFSync-Funktion](rtfsync.md) verwendet und sind nicht für die direkte Verwendung durch Clientanwendungen vorgesehen.</span><span class="sxs-lookup"><span data-stu-id="c55ac-117">RTF auxiliary properties are used by the [RTFSync](rtfsync.md) function and are not intended to be used directly by client applications.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="c55ac-118">Verwandte Ressourcen</span><span class="sxs-lookup"><span data-stu-id="c55ac-118">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="c55ac-119">Protokollspezifikationen</span><span class="sxs-lookup"><span data-stu-id="c55ac-119">Protocol specifications</span></span>

<span data-ttu-id="c55ac-120">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="c55ac-120">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="c55ac-121">Enthält Verweise auf Exchange Server Protokollspezifikationen.</span><span class="sxs-lookup"><span data-stu-id="c55ac-121">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="c55ac-122">[[MS-OXTNEF]](https://msdn.microsoft.com/library/1f0544d7-30b7-4194-b58f-adc82f3763bb%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="c55ac-122">[[MS-OXTNEF]](https://msdn.microsoft.com/library/1f0544d7-30b7-4194-b58f-adc82f3763bb%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="c55ac-123">Codiert und decodiert Nachrichten- und Anlagenobjekte in eine effiziente Streamdarstellung.</span><span class="sxs-lookup"><span data-stu-id="c55ac-123">Encodes and decodes message and attachment objects to an efficient stream representation.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="c55ac-124">Headerdateien</span><span class="sxs-lookup"><span data-stu-id="c55ac-124">Header files</span></span>

<span data-ttu-id="c55ac-125">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="c55ac-125">Mapidefs.h</span></span>
  
> <span data-ttu-id="c55ac-126">Bietet Datentypdefinitionen.</span><span class="sxs-lookup"><span data-stu-id="c55ac-126">Provides data type definitions.</span></span>
    
<span data-ttu-id="c55ac-127">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="c55ac-127">Mapitags.h</span></span>
  
> <span data-ttu-id="c55ac-128">Enthält Definitionen von Eigenschaften, die als alternative Namen aufgeführt sind.</span><span class="sxs-lookup"><span data-stu-id="c55ac-128">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="c55ac-129">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="c55ac-129">See also</span></span>



[<span data-ttu-id="c55ac-130">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="c55ac-130">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="c55ac-131">KANONISCHE EIGENSCHAFTEN VON MAPI</span><span class="sxs-lookup"><span data-stu-id="c55ac-131">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="c55ac-132">Zuordnen kanonischer Eigenschaftsnamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="c55ac-132">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="c55ac-133">Zuordnen von MAPI-Namen zu kanonischen Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="c55ac-133">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

