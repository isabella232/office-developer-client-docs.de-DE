---
title: Kanonische Pidtagrtfsynctrailingcount (-Eigenschaft
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
ms.openlocfilehash: 67093cf456db9df5f9e939bdda9d2e44f248dadc
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32331234"
---
# <a name="pidtagrtfsynctrailingcount-canonical-property"></a><span data-ttu-id="66345-103">Kanonische Pidtagrtfsynctrailingcount (-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="66345-103">PidTagRtfSyncTrailingCount Canonical Property</span></span>

  
  
<span data-ttu-id="66345-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="66345-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="66345-105">Enthält die Anzahl der ignorierten Zeichen, die nach den signifikanten Zeichen der Nachricht angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="66345-105">Contains a count of the ignorable characters that appear after the significant characters of the message.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="66345-106">Zugeordnete Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="66345-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="66345-107">PR_RTF_SYNC_TRAILING_COUNT</span><span class="sxs-lookup"><span data-stu-id="66345-107">PR_RTF_SYNC_TRAILING_COUNT</span></span>  <br/> |
|<span data-ttu-id="66345-108">Kennung:</span><span class="sxs-lookup"><span data-stu-id="66345-108">Identifier:</span></span>  <br/> |<span data-ttu-id="66345-109">0x1011</span><span class="sxs-lookup"><span data-stu-id="66345-109">0x1011</span></span>  <br/> |
|<span data-ttu-id="66345-110">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="66345-110">Data type:</span></span>  <br/> |<span data-ttu-id="66345-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="66345-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="66345-112">Bereich:</span><span class="sxs-lookup"><span data-stu-id="66345-112">Area:</span></span>  <br/> |<span data-ttu-id="66345-113">MAPI-Nachricht</span><span class="sxs-lookup"><span data-stu-id="66345-113">MAPI message</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="66345-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="66345-114">Remarks</span></span>

<span data-ttu-id="66345-115">Diese Eigenschaft ist eine RFT-Eigenschaft (Rich Text Format).</span><span class="sxs-lookup"><span data-stu-id="66345-115">This property is a Rich Text Format (RFT) auxiliary property.</span></span> <span data-ttu-id="66345-116">Diese Eigenschaften werden von der [RTFSync](rtfsync.md) -Funktion verwendet und sind nicht für die direkte Verwendung durch Clientanwendungen vorgesehen.</span><span class="sxs-lookup"><span data-stu-id="66345-116">These properties are used by the [RTFSync](rtfsync.md) function and are not intended to be used directly by client applications.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="66345-117">Zugehörige Ressourcen</span><span class="sxs-lookup"><span data-stu-id="66345-117">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="66345-118">Protokollspezifikationen</span><span class="sxs-lookup"><span data-stu-id="66345-118">Protocol specifications</span></span>

<span data-ttu-id="66345-119">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="66345-119">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="66345-120">Enthält Verweise auf zugehörige Exchange Server-Protokollspezifikationen.</span><span class="sxs-lookup"><span data-stu-id="66345-120">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="66345-121">[[MS-OXTNEF]](https://msdn.microsoft.com/library/1f0544d7-30b7-4194-b58f-adc82f3763bb%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="66345-121">[[MS-OXTNEF]](https://msdn.microsoft.com/library/1f0544d7-30b7-4194-b58f-adc82f3763bb%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="66345-122">Codiert und dekodiert Message-und Attachment-Objekte in einer effizienten Datenstrom Darstellung.</span><span class="sxs-lookup"><span data-stu-id="66345-122">Encodes and decodes message and attachment objects to an efficient stream representation.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="66345-123">Header Dateien</span><span class="sxs-lookup"><span data-stu-id="66345-123">Header files</span></span>

<span data-ttu-id="66345-124">Mapidefs. h</span><span class="sxs-lookup"><span data-stu-id="66345-124">Mapidefs.h</span></span>
  
> <span data-ttu-id="66345-125">Stellt Datentypdefinitionen bereit.</span><span class="sxs-lookup"><span data-stu-id="66345-125">Provides data type definitions.</span></span>
    
<span data-ttu-id="66345-126">Mapitags. h</span><span class="sxs-lookup"><span data-stu-id="66345-126">Mapitags.h</span></span>
  
> <span data-ttu-id="66345-127">Enthält Definitionen von Eigenschaften, die als Alternative Namen aufgeführt sind.</span><span class="sxs-lookup"><span data-stu-id="66345-127">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="66345-128">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="66345-128">See also</span></span>



[<span data-ttu-id="66345-129">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="66345-129">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="66345-130">Kanonische MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="66345-130">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="66345-131">Zuordnen von kanonischen Eigenschaftennamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="66345-131">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="66345-132">Zuordnen von MAPI-Namen zu kanonischen Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="66345-132">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

