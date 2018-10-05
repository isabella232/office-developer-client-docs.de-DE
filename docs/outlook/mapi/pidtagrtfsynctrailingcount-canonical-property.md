---
title: PidTagRtfSyncTrailingCount (kanonische Eigenschaft)
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
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 67093cf456db9df5f9e939bdda9d2e44f248dadc
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/04/2018
ms.locfileid: "25397919"
---
# <a name="pidtagrtfsynctrailingcount-canonical-property"></a><span data-ttu-id="6c9e4-103">PidTagRtfSyncTrailingCount (kanonische Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="6c9e4-103">PidTagRtfSyncTrailingCount Canonical Property</span></span>

  
  
<span data-ttu-id="6c9e4-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="6c9e4-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="6c9e4-105">Enthält eine Anzahl von Zeichen, die nach den erheblichen Zeichen der Nachricht angezeigt werden ignoriert.</span><span class="sxs-lookup"><span data-stu-id="6c9e4-105">Contains a count of the ignorable characters that appear after the significant characters of the message.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="6c9e4-106">Zugeordnete Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="6c9e4-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="6c9e4-107">PR_RTF_SYNC_TRAILING_COUNT</span><span class="sxs-lookup"><span data-stu-id="6c9e4-107">PR_RTF_SYNC_TRAILING_COUNT</span></span>  <br/> |
|<span data-ttu-id="6c9e4-108">Kennung:</span><span class="sxs-lookup"><span data-stu-id="6c9e4-108">Identifier:</span></span>  <br/> |<span data-ttu-id="6c9e4-109">0x1011</span><span class="sxs-lookup"><span data-stu-id="6c9e4-109">0x1011</span></span>  <br/> |
|<span data-ttu-id="6c9e4-110">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="6c9e4-110">Data type:</span></span>  <br/> |<span data-ttu-id="6c9e4-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="6c9e4-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="6c9e4-112">Bereich:</span><span class="sxs-lookup"><span data-stu-id="6c9e4-112">Area:</span></span>  <br/> |<span data-ttu-id="6c9e4-113">MAPI-Nachricht</span><span class="sxs-lookup"><span data-stu-id="6c9e4-113">MAPI message</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="6c9e4-114">Hinweise</span><span class="sxs-lookup"><span data-stu-id="6c9e4-114">Remarks</span></span>

<span data-ttu-id="6c9e4-115">Diese Eigenschaft ist eine zusätzliche Rich Text Format (RTF)-Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="6c9e4-115">This property is a Rich Text Format (RFT) auxiliary property.</span></span> <span data-ttu-id="6c9e4-116">Diese Eigenschaften werden von der Funktion [RTFSync](rtfsync.md) verwendet und nicht direkt von Clientanwendungen verwendet werden sollen.</span><span class="sxs-lookup"><span data-stu-id="6c9e4-116">These properties are used by the [RTFSync](rtfsync.md) function and are not intended to be used directly by client applications.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="6c9e4-117">Verwandte Ressourcen</span><span class="sxs-lookup"><span data-stu-id="6c9e4-117">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="6c9e4-118">Protokollspezifikationen</span><span class="sxs-lookup"><span data-stu-id="6c9e4-118">Protocol specifications</span></span>

<span data-ttu-id="6c9e4-119">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="6c9e4-119">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="6c9e4-120">Bietet Verweise auf Verwandte Exchange Server-Spezifikationen.</span><span class="sxs-lookup"><span data-stu-id="6c9e4-120">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="6c9e4-121">[[MS-OXTNEF]](https://msdn.microsoft.com/library/1f0544d7-30b7-4194-b58f-adc82f3763bb%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="6c9e4-121">[[MS-OXTNEF]](https://msdn.microsoft.com/library/1f0544d7-30b7-4194-b58f-adc82f3763bb%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="6c9e4-122">Codiert und decodiert Nachrichten- und Objekte, die auf eine effiziente Streamdarstellung.</span><span class="sxs-lookup"><span data-stu-id="6c9e4-122">Encodes and decodes message and attachment objects to an efficient stream representation.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="6c9e4-123">Header-Dateien</span><span class="sxs-lookup"><span data-stu-id="6c9e4-123">Header files</span></span>

<span data-ttu-id="6c9e4-124">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="6c9e4-124">Mapidefs.h</span></span>
  
> <span data-ttu-id="6c9e4-125">Enthält die Datentypdefinitionen.</span><span class="sxs-lookup"><span data-stu-id="6c9e4-125">Provides data type definitions.</span></span>
    
<span data-ttu-id="6c9e4-126">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="6c9e4-126">Mapitags.h</span></span>
  
> <span data-ttu-id="6c9e4-127">Enthält Definitionen von Eigenschaften, die als Alternative Namen aufgelistet.</span><span class="sxs-lookup"><span data-stu-id="6c9e4-127">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="6c9e4-128">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="6c9e4-128">See also</span></span>



[<span data-ttu-id="6c9e4-129">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="6c9e4-129">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="6c9e4-130">Kanonische MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="6c9e4-130">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="6c9e4-131">Zuordnen von kanonischen Eigenschaftennamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="6c9e4-131">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="6c9e4-132">Zuordnen von MAPI-Namen zu kanonische Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="6c9e4-132">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

