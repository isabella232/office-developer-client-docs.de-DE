---
title: PidTagRtfSyncBodyCount (kanonische Eigenschaft)
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
ms.openlocfilehash: 09274c21df3a93abc19aa8158da976e2d16f3e7c
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19795030"
---
# <a name="pidtagrtfsyncbodycount-canonical-property"></a><span data-ttu-id="e0846-103">PidTagRtfSyncBodyCount (kanonische Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="e0846-103">PidTagRtfSyncBodyCount Canonical Property</span></span>

  
  
<span data-ttu-id="e0846-104">**Betrifft**: Outlook</span><span class="sxs-lookup"><span data-stu-id="e0846-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="e0846-105">Anzahl der signifikanten Zeichen des Nachrichtentexts enthält.</span><span class="sxs-lookup"><span data-stu-id="e0846-105">Contains a count of the significant characters of the message text.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="e0846-106">Zugeordneten Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="e0846-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="e0846-107">PR_RTF_SYNC_BODY_COUNT</span><span class="sxs-lookup"><span data-stu-id="e0846-107">PR_RTF_SYNC_BODY_COUNT</span></span>  <br/> |
|<span data-ttu-id="e0846-108">Bezeichner:</span><span class="sxs-lookup"><span data-stu-id="e0846-108">Identifier:</span></span>  <br/> |<span data-ttu-id="e0846-109">0 x 1007</span><span class="sxs-lookup"><span data-stu-id="e0846-109">0x1007</span></span>  <br/> |
|<span data-ttu-id="e0846-110">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="e0846-110">Data type:</span></span>  <br/> |<span data-ttu-id="e0846-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="e0846-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="e0846-112">Bereich:</span><span class="sxs-lookup"><span data-stu-id="e0846-112">Area:</span></span>  <br/> |<span data-ttu-id="e0846-113">MAPI-Nachricht</span><span class="sxs-lookup"><span data-stu-id="e0846-113">MAPI message</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="e0846-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="e0846-114">Remarks</span></span>

<span data-ttu-id="e0846-115">Die [RTFSync](rtfsync.md) -Funktion berechnet die Anzahl der Zeichen im Text nur diejenigen, die sie für die Nachricht erzielt werden hält verwenden.</span><span class="sxs-lookup"><span data-stu-id="e0846-115">The [RTFSync](rtfsync.md) function computes the count of characters in the text using only those that it considers to be significant to the message.</span></span> <span data-ttu-id="e0846-116">Beispielsweise sind einige Leerzeichen und Sonderzeichen ignoriert die Anzahl der ausgelassen.</span><span class="sxs-lookup"><span data-stu-id="e0846-116">For example, some white space and other ignorable characters are omitted from the count.</span></span> 
  
<span data-ttu-id="e0846-117">Diese Eigenschaft ist eine zusätzliche Rich Text Format (RTF)-Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="e0846-117">This property is a Rich Text Format (RTF) auxiliary property.</span></span> <span data-ttu-id="e0846-118">Diese Eigenschaften werden von der Funktion **RTFSync** verwendet und nicht direkt von Clientanwendungen verwendet werden sollen.</span><span class="sxs-lookup"><span data-stu-id="e0846-118">These properties are used by the **RTFSync** function and are not intended to be used directly by client applications.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="e0846-119">Verwandte Ressourcen</span><span class="sxs-lookup"><span data-stu-id="e0846-119">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="e0846-120">Protokollspezifikationen</span><span class="sxs-lookup"><span data-stu-id="e0846-120">Protocol specifications</span></span>

<span data-ttu-id="e0846-121">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="e0846-121">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="e0846-122">Bietet Verweise auf Verwandte Exchange Server-Spezifikationen.</span><span class="sxs-lookup"><span data-stu-id="e0846-122">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="e0846-123">[[MS-OXTNEF]](http://msdn.microsoft.com/library/1f0544d7-30b7-4194-b58f-adc82f3763bb%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="e0846-123">[[MS-OXTNEF]](http://msdn.microsoft.com/library/1f0544d7-30b7-4194-b58f-adc82f3763bb%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="e0846-124">Codiert und decodiert Nachrichten- und Objekte, die auf eine effiziente Streamdarstellung.</span><span class="sxs-lookup"><span data-stu-id="e0846-124">Encodes and decodes message and attachment objects to an efficient stream representation.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="e0846-125">Header-Dateien</span><span class="sxs-lookup"><span data-stu-id="e0846-125">Header files</span></span>

<span data-ttu-id="e0846-126">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="e0846-126">Mapidefs.h</span></span>
  
> <span data-ttu-id="e0846-127">Enthält die Datentypdefinitionen.</span><span class="sxs-lookup"><span data-stu-id="e0846-127">Provides data type definitions.</span></span>
    
<span data-ttu-id="e0846-128">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="e0846-128">Mapitags.h</span></span>
  
> <span data-ttu-id="e0846-129">Enthält Definitionen von Eigenschaften, die als Alternative Namen aufgelistet.</span><span class="sxs-lookup"><span data-stu-id="e0846-129">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="e0846-130">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="e0846-130">See also</span></span>



[<span data-ttu-id="e0846-131">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="e0846-131">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="e0846-132">Kanonische MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="e0846-132">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="e0846-133">Zuordnen von kanonischen Eigenschaftennamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="e0846-133">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="e0846-134">Zuordnen von MAPI-Namen zu kanonische Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="e0846-134">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

