---
title: Kanonische PidTagOriginalDisplayTo-Eigenschaft
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagOriginalDisplayTo
api_type:
- COM
ms.assetid: 8c1cf14c-0339-4ced-8f68-4bfaa1e4d3e9
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: 68bb9a25131a07cf482a39cef70eb08a2b5a1756
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19794687"
---
# <a name="pidtagoriginaldisplayto-canonical-property"></a><span data-ttu-id="4fb6b-103">Kanonische PidTagOriginalDisplayTo-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="4fb6b-103">PidTagOriginalDisplayTo Canonical Property</span></span>

  
  
<span data-ttu-id="4fb6b-104">**Betrifft**: Outlook</span><span class="sxs-lookup"><span data-stu-id="4fb6b-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="4fb6b-105">Enthält die Anzeigenamen der primären (Empfänger der ursprünglichen Nachricht To).</span><span class="sxs-lookup"><span data-stu-id="4fb6b-105">Contains the display names of the primary (To) recipients of the original message.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="4fb6b-106">Zugeordneten Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="4fb6b-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="4fb6b-107">PR_ORIGINAL_DISPLAY_TO, PR_ORIGINAL_DISPLAY_TO_A, PR_ORIGINAL_DISPLAY_TO_W</span><span class="sxs-lookup"><span data-stu-id="4fb6b-107">PR_ORIGINAL_DISPLAY_TO, PR_ORIGINAL_DISPLAY_TO_A, PR_ORIGINAL_DISPLAY_TO_W</span></span>  <br/> |
|<span data-ttu-id="4fb6b-108">Bezeichner:</span><span class="sxs-lookup"><span data-stu-id="4fb6b-108">Identifier:</span></span>  <br/> |<span data-ttu-id="4fb6b-109">0x0074</span><span class="sxs-lookup"><span data-stu-id="4fb6b-109">0x0074</span></span>  <br/> |
|<span data-ttu-id="4fb6b-110">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="4fb6b-110">Data type:</span></span>  <br/> |<span data-ttu-id="4fb6b-111">PT_STRING8, PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="4fb6b-111">PT_STRING8, PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="4fb6b-112">Bereich:</span><span class="sxs-lookup"><span data-stu-id="4fb6b-112">Area:</span></span>  <br/> |<span data-ttu-id="4fb6b-113">Allgemeine messaging</span><span class="sxs-lookup"><span data-stu-id="4fb6b-113">General messaging</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="4fb6b-114">Hinweise</span><span class="sxs-lookup"><span data-stu-id="4fb6b-114">Remarks</span></span>

<span data-ttu-id="4fb6b-115">Diese Eigenschaften enthalten eine durch Semikolons getrennte ASCII-Liste.</span><span class="sxs-lookup"><span data-stu-id="4fb6b-115">These properties contain an ASCII list separated by semicolons.</span></span> <span data-ttu-id="4fb6b-116">Es MAPI bereitgestellten und wird direkt aus **PR_DISPLAY_TO** ([PidTagDisplayTo](pidtagdisplayto-canonical-property.md)) bei einer Übermittlung kopiert oder Unzustellbarkeitsbericht oder einem Lese- oder nonread Bericht wird generiert.</span><span class="sxs-lookup"><span data-stu-id="4fb6b-116">It is furnished by MAPI and is copied directly from **PR_DISPLAY_TO** ([PidTagDisplayTo](pidtagdisplayto-canonical-property.md)) when a delivery or nondelivery report or a read or nonread report is generated.</span></span> <span data-ttu-id="4fb6b-117">Diese Eigenschaft kann auf andere Nachrichten durch ihre Nachrichtenklassen definierten vorhanden sein.</span><span class="sxs-lookup"><span data-stu-id="4fb6b-117">This property may be present on other messages as defined by their message classes.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="4fb6b-118">Verwandte Ressourcen</span><span class="sxs-lookup"><span data-stu-id="4fb6b-118">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="4fb6b-119">Protokollspezifikationen</span><span class="sxs-lookup"><span data-stu-id="4fb6b-119">Protocol specifications</span></span>

<span data-ttu-id="4fb6b-120">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="4fb6b-120">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="4fb6b-121">Bietet Verweise auf Verwandte Exchange Server-Spezifikationen.</span><span class="sxs-lookup"><span data-stu-id="4fb6b-121">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="4fb6b-122">[[MS-OXOMSG]](http://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="4fb6b-122">[[MS-OXOMSG]](http://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="4fb6b-123">Gibt die Eigenschaften und Operationen, die für Objekte, die e-Mail-Nachricht zulässig sind.</span><span class="sxs-lookup"><span data-stu-id="4fb6b-123">Specifies the properties and operations that are permissible on email message objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="4fb6b-124">Header-Dateien</span><span class="sxs-lookup"><span data-stu-id="4fb6b-124">Header files</span></span>

<span data-ttu-id="4fb6b-125">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="4fb6b-125">Mapidefs.h</span></span>
  
> <span data-ttu-id="4fb6b-126">Enthält die Datentypdefinitionen.</span><span class="sxs-lookup"><span data-stu-id="4fb6b-126">Provides data type definitions.</span></span>
    
<span data-ttu-id="4fb6b-127">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="4fb6b-127">Mapitags.h</span></span>
  
> <span data-ttu-id="4fb6b-128">Enthält Definitionen von Eigenschaften, die als Alternative Namen aufgelistet.</span><span class="sxs-lookup"><span data-stu-id="4fb6b-128">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="4fb6b-129">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="4fb6b-129">See also</span></span>



[<span data-ttu-id="4fb6b-130">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="4fb6b-130">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="4fb6b-131">Kanonische MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="4fb6b-131">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="4fb6b-132">Zuordnen von kanonischen Eigenschaftennamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="4fb6b-132">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="4fb6b-133">Zuordnen von MAPI-Namen zu kanonische Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="4fb6b-133">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)
