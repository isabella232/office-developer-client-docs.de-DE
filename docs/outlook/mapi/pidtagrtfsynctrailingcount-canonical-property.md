---
title: Kanonische PidTagRtfSyncTrailingCount-Eigenschaft
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagRtfSyncTrailingCount
api_type:
- COM
ms.assetid: 3f0e5b24-767e-46f5-bb3d-e9cb82cb935b
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: 3174ebbcf70104c82305e2a20df1e183d30265d6
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19795012"
---
# <a name="pidtagrtfsynctrailingcount-canonical-property"></a><span data-ttu-id="179d6-103">Kanonische PidTagRtfSyncTrailingCount-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="179d6-103">PidTagRtfSyncTrailingCount Canonical Property</span></span>

  
  
<span data-ttu-id="179d6-104">**Betrifft**: Outlook</span><span class="sxs-lookup"><span data-stu-id="179d6-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="179d6-105">Enthält eine Anzahl von Zeichen, die nach den erheblichen Zeichen der Nachricht angezeigt werden ignoriert.</span><span class="sxs-lookup"><span data-stu-id="179d6-105">Contains a count of the ignorable characters that appear after the significant characters of the message.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="179d6-106">Zugeordneten Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="179d6-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="179d6-107">PR_RTF_SYNC_TRAILING_COUNT</span><span class="sxs-lookup"><span data-stu-id="179d6-107">PR_RTF_SYNC_TRAILING_COUNT</span></span>  <br/> |
|<span data-ttu-id="179d6-108">Bezeichner:</span><span class="sxs-lookup"><span data-stu-id="179d6-108">Identifier:</span></span>  <br/> |<span data-ttu-id="179d6-109">0x1011</span><span class="sxs-lookup"><span data-stu-id="179d6-109">0x1011</span></span>  <br/> |
|<span data-ttu-id="179d6-110">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="179d6-110">Data type:</span></span>  <br/> |<span data-ttu-id="179d6-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="179d6-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="179d6-112">Bereich:</span><span class="sxs-lookup"><span data-stu-id="179d6-112">Area:</span></span>  <br/> |<span data-ttu-id="179d6-113">MAPI-Nachricht</span><span class="sxs-lookup"><span data-stu-id="179d6-113">MAPI message</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="179d6-114">Hinweise</span><span class="sxs-lookup"><span data-stu-id="179d6-114">Remarks</span></span>

<span data-ttu-id="179d6-115">Diese Eigenschaft ist eine zusätzliche Rich Text Format (RTF)-Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="179d6-115">This property is a Rich Text Format (RFT) auxiliary property.</span></span> <span data-ttu-id="179d6-116">Diese Eigenschaften werden von der Funktion [RTFSync](rtfsync.md) verwendet und nicht direkt von Clientanwendungen verwendet werden sollen.</span><span class="sxs-lookup"><span data-stu-id="179d6-116">These properties are used by the [RTFSync](rtfsync.md) function and are not intended to be used directly by client applications.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="179d6-117">Verwandte Ressourcen</span><span class="sxs-lookup"><span data-stu-id="179d6-117">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="179d6-118">Protokollspezifikationen</span><span class="sxs-lookup"><span data-stu-id="179d6-118">Protocol specifications</span></span>

<span data-ttu-id="179d6-119">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="179d6-119">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="179d6-120">Bietet Verweise auf Verwandte Exchange Server-Spezifikationen.</span><span class="sxs-lookup"><span data-stu-id="179d6-120">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="179d6-121">[[MS-OXTNEF]](http://msdn.microsoft.com/library/1f0544d7-30b7-4194-b58f-adc82f3763bb%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="179d6-121">[[MS-OXTNEF]](http://msdn.microsoft.com/library/1f0544d7-30b7-4194-b58f-adc82f3763bb%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="179d6-122">Codiert und decodiert Nachrichten- und Objekte, die auf eine effiziente Streamdarstellung.</span><span class="sxs-lookup"><span data-stu-id="179d6-122">Encodes and decodes message and attachment objects to an efficient stream representation.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="179d6-123">Header-Dateien</span><span class="sxs-lookup"><span data-stu-id="179d6-123">Header files</span></span>

<span data-ttu-id="179d6-124">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="179d6-124">Mapidefs.h</span></span>
  
> <span data-ttu-id="179d6-125">Enthält die Datentypdefinitionen.</span><span class="sxs-lookup"><span data-stu-id="179d6-125">Provides data type definitions.</span></span>
    
<span data-ttu-id="179d6-126">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="179d6-126">Mapitags.h</span></span>
  
> <span data-ttu-id="179d6-127">Enthält Definitionen von Eigenschaften, die als Alternative Namen aufgelistet.</span><span class="sxs-lookup"><span data-stu-id="179d6-127">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="179d6-128">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="179d6-128">See also</span></span>



[<span data-ttu-id="179d6-129">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="179d6-129">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="179d6-130">Kanonische MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="179d6-130">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="179d6-131">Zuordnen von kanonischen Eigenschaftennamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="179d6-131">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="179d6-132">Zuordnen von MAPI-Namen zu kanonische Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="179d6-132">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)
