---
title: Kanonische Pidtagrtfsyncprefixcount (-Eigenschaft
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
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: 61683534504b7451f126591af149d11306cff1bd
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32357862"
---
# <a name="pidtagrtfsyncprefixcount-canonical-property"></a><span data-ttu-id="0dd91-103">Kanonische Pidtagrtfsyncprefixcount (-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="0dd91-103">PidTagRtfSyncPrefixCount Canonical Property</span></span>

  
  
<span data-ttu-id="0dd91-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="0dd91-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="0dd91-105">Enthält die Anzahl der ignorierten Zeichen, die vor den signifikanten Zeichen der Nachricht angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="0dd91-105">Contains a count of the ignorable characters that appear before the significant characters of the message.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="0dd91-106">Zugeordnete Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="0dd91-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="0dd91-107">PR_RTF_SYNC_PREFIX_COUNT</span><span class="sxs-lookup"><span data-stu-id="0dd91-107">PR_RTF_SYNC_PREFIX_COUNT</span></span>  <br/> |
|<span data-ttu-id="0dd91-108">Kennung:</span><span class="sxs-lookup"><span data-stu-id="0dd91-108">Identifier:</span></span>  <br/> |<span data-ttu-id="0dd91-109">0x1010</span><span class="sxs-lookup"><span data-stu-id="0dd91-109">0x1010</span></span>  <br/> |
|<span data-ttu-id="0dd91-110">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="0dd91-110">Data type:</span></span>  <br/> |<span data-ttu-id="0dd91-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="0dd91-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="0dd91-112">Bereich:</span><span class="sxs-lookup"><span data-stu-id="0dd91-112">Area:</span></span>  <br/> |<span data-ttu-id="0dd91-113">MAPI-Nachricht</span><span class="sxs-lookup"><span data-stu-id="0dd91-113">MAPI message</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="0dd91-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="0dd91-114">Remarks</span></span>

<span data-ttu-id="0dd91-115">Die Anzahl der Präfixzeichen enthält keinen Leerraum.</span><span class="sxs-lookup"><span data-stu-id="0dd91-115">The count of prefix characters does not include white space.</span></span>
  
<span data-ttu-id="0dd91-116">Diese Eigenschaft ist eine Hilfseigenschaft für Rich-Text-Format (RTF).</span><span class="sxs-lookup"><span data-stu-id="0dd91-116">This property is a Rich Text Format (RTF) auxiliary property.</span></span> <span data-ttu-id="0dd91-117">RTF-Hilfseigenschaften werden von der [RTFSync](rtfsync.md) -Funktion verwendet und sind nicht für die direkte Verwendung durch Clientanwendungen vorgesehen.</span><span class="sxs-lookup"><span data-stu-id="0dd91-117">RTF auxiliary properties are used by the [RTFSync](rtfsync.md) function and are not intended to be used directly by client applications.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="0dd91-118">Zugehörige Ressourcen</span><span class="sxs-lookup"><span data-stu-id="0dd91-118">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="0dd91-119">Protokollspezifikationen</span><span class="sxs-lookup"><span data-stu-id="0dd91-119">Protocol specifications</span></span>

<span data-ttu-id="0dd91-120">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="0dd91-120">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="0dd91-121">Enthält Verweise auf zugehörige Exchange Server-Protokollspezifikationen.</span><span class="sxs-lookup"><span data-stu-id="0dd91-121">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="0dd91-122">[[MS-OXTNEF]](https://msdn.microsoft.com/library/1f0544d7-30b7-4194-b58f-adc82f3763bb%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="0dd91-122">[[MS-OXTNEF]](https://msdn.microsoft.com/library/1f0544d7-30b7-4194-b58f-adc82f3763bb%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="0dd91-123">Codiert und dekodiert Message-und Attachment-Objekte in einer effizienten Datenstrom Darstellung.</span><span class="sxs-lookup"><span data-stu-id="0dd91-123">Encodes and decodes message and attachment objects to an efficient stream representation.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="0dd91-124">Header Dateien</span><span class="sxs-lookup"><span data-stu-id="0dd91-124">Header files</span></span>

<span data-ttu-id="0dd91-125">Mapidefs. h</span><span class="sxs-lookup"><span data-stu-id="0dd91-125">Mapidefs.h</span></span>
  
> <span data-ttu-id="0dd91-126">Stellt Datentypdefinitionen bereit.</span><span class="sxs-lookup"><span data-stu-id="0dd91-126">Provides data type definitions.</span></span>
    
<span data-ttu-id="0dd91-127">Mapitags. h</span><span class="sxs-lookup"><span data-stu-id="0dd91-127">Mapitags.h</span></span>
  
> <span data-ttu-id="0dd91-128">Enthält Definitionen von Eigenschaften, die als Alternative Namen aufgeführt sind.</span><span class="sxs-lookup"><span data-stu-id="0dd91-128">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="0dd91-129">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="0dd91-129">See also</span></span>



[<span data-ttu-id="0dd91-130">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="0dd91-130">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="0dd91-131">Kanonische MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="0dd91-131">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="0dd91-132">Zuordnen von kanonischen Eigenschaftennamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="0dd91-132">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="0dd91-133">Zuordnen von MAPI-Namen zu kanonischen Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="0dd91-133">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

