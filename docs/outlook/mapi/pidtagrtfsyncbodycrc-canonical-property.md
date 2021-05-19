---
title: PidTagRtfSyncBodyCrc (kanonische Eigenschaft)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagRtfSyncBodyCrc
api_type:
- COM
ms.assetid: 95db4837-400f-476f-b313-60e8baa1c6d1
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 85ac61d968243283e5ad9283730941adcd87cd5e
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32357869"
---
# <a name="pidtagrtfsyncbodycrc-canonical-property"></a><span data-ttu-id="80660-103">PidTagRtfSyncBodyCrc (kanonische Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="80660-103">PidTagRtfSyncBodyCrc Canonical Property</span></span>

  
  
<span data-ttu-id="80660-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="80660-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="80660-105">Enthält die zyklische Redundanzprüfung (CrC), die für den Nachrichtentext berechnet wurde.</span><span class="sxs-lookup"><span data-stu-id="80660-105">Contains the cyclical redundancy check (CRC) computed for the message text.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="80660-106">Zugeordnete Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="80660-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="80660-107">PR_RTF_SYNC_BODY_CRC</span><span class="sxs-lookup"><span data-stu-id="80660-107">PR_RTF_SYNC_BODY_CRC</span></span>  <br/> |
|<span data-ttu-id="80660-108">Kennung:</span><span class="sxs-lookup"><span data-stu-id="80660-108">Identifier:</span></span>  <br/> |<span data-ttu-id="80660-109">0x1006</span><span class="sxs-lookup"><span data-stu-id="80660-109">0x1006</span></span>  <br/> |
|<span data-ttu-id="80660-110">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="80660-110">Data type:</span></span>  <br/> |<span data-ttu-id="80660-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="80660-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="80660-112">Bereich:</span><span class="sxs-lookup"><span data-stu-id="80660-112">Area:</span></span>  <br/> |<span data-ttu-id="80660-113">MAPI-Nachricht</span><span class="sxs-lookup"><span data-stu-id="80660-113">MAPI message</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="80660-114">Hinweise</span><span class="sxs-lookup"><span data-stu-id="80660-114">Remarks</span></span>

<span data-ttu-id="80660-115">Die [RTFSync-Funktion](rtfsync.md) berechnet den CRC, indem nur die Zeichen verwendet werden, die sie für die Nachricht als wichtig erachtet.</span><span class="sxs-lookup"><span data-stu-id="80660-115">The [RTFSync](rtfsync.md) function computes the CRC by using only the characters that it considers to be significant to the message.</span></span> <span data-ttu-id="80660-116">Beispielsweise werden einige Leerzeichen und andere nicht ignorierbare Zeichen aus der CRC weggelassen.</span><span class="sxs-lookup"><span data-stu-id="80660-116">For example, some white space and other ignorable characters are omitted from the CRC.</span></span> 
  
<span data-ttu-id="80660-117">Diese Eigenschaft ist eine Rich Text Format (RTF)-Hilfseigenschaft.</span><span class="sxs-lookup"><span data-stu-id="80660-117">This property is a Rich Text Format (RTF) auxiliary property.</span></span> <span data-ttu-id="80660-118">Diese Eigenschaften werden von der **RTFSync-Funktion** verwendet und sind nicht für die direkte Verwendung durch Clientanwendungen vorgesehen.</span><span class="sxs-lookup"><span data-stu-id="80660-118">These properties are used by the **RTFSync** function and are not intended to be used directly by client applications.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="80660-119">Verwandte Ressourcen</span><span class="sxs-lookup"><span data-stu-id="80660-119">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="80660-120">Protokollspezifikationen</span><span class="sxs-lookup"><span data-stu-id="80660-120">Protocol specifications</span></span>

<span data-ttu-id="80660-121">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="80660-121">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="80660-122">Enthält Verweise auf Exchange Server Protokollspezifikationen.</span><span class="sxs-lookup"><span data-stu-id="80660-122">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="80660-123">[[MS-OXTNEF]](https://msdn.microsoft.com/library/1f0544d7-30b7-4194-b58f-adc82f3763bb%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="80660-123">[[MS-OXTNEF]](https://msdn.microsoft.com/library/1f0544d7-30b7-4194-b58f-adc82f3763bb%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="80660-124">Codiert und decodiert Nachrichten- und Anlagenobjekte in eine effiziente Streamdarstellung.</span><span class="sxs-lookup"><span data-stu-id="80660-124">Encodes and decodes message and attachment objects to an efficient stream representation.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="80660-125">Headerdateien</span><span class="sxs-lookup"><span data-stu-id="80660-125">Header files</span></span>

<span data-ttu-id="80660-126">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="80660-126">Mapidefs.h</span></span>
  
> <span data-ttu-id="80660-127">Bietet Datentypdefinitionen.</span><span class="sxs-lookup"><span data-stu-id="80660-127">Provides data type definitions.</span></span>
    
<span data-ttu-id="80660-128">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="80660-128">Mapitags.h</span></span>
  
> <span data-ttu-id="80660-129">Enthält Definitionen von Eigenschaften, die als alternative Namen aufgeführt sind.</span><span class="sxs-lookup"><span data-stu-id="80660-129">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="80660-130">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="80660-130">See also</span></span>



[<span data-ttu-id="80660-131">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="80660-131">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="80660-132">KANONISCHE EIGENSCHAFTEN VON MAPI</span><span class="sxs-lookup"><span data-stu-id="80660-132">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="80660-133">Zuordnen kanonischer Eigenschaftsnamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="80660-133">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="80660-134">Zuordnen von MAPI-Namen zu kanonischen Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="80660-134">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

