---
title: Kanonische PidTagOriginalDisplayBcc-Eigenschaft
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagOriginalDisplayBcc
api_type:
- COM
ms.assetid: 7bf66f0c-3095-4b4a-a32e-db278e1adc5a
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: 15615a2de54cf42399007268cc07cbe2ab776ee8
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19794677"
---
# <a name="pidtagoriginaldisplaybcc-canonical-property"></a><span data-ttu-id="655f2-103">Kanonische PidTagOriginalDisplayBcc-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="655f2-103">PidTagOriginalDisplayBcc Canonical Property</span></span>

  
  
<span data-ttu-id="655f2-104">**Betrifft**: Outlook</span><span class="sxs-lookup"><span data-stu-id="655f2-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="655f2-105">Enthält die Anzeigenamen der Empfänger blind Carbon Copy, Blindkopie (BCC) der ursprünglichen Nachricht.</span><span class="sxs-lookup"><span data-stu-id="655f2-105">Contains the display names of any blind carbon copy (BCC) recipients of the original message.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="655f2-106">Zugeordneten Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="655f2-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="655f2-107">PR_ORIGINAL_DISPLAY_BCC, PR_ORIGINAL_DISPLAY_BCC_A, PR_ORIGINAL_DISPLAY_BCC_W</span><span class="sxs-lookup"><span data-stu-id="655f2-107">PR_ORIGINAL_DISPLAY_BCC, PR_ORIGINAL_DISPLAY_BCC_A, PR_ORIGINAL_DISPLAY_BCC_W</span></span>  <br/> |
|<span data-ttu-id="655f2-108">Bezeichner:</span><span class="sxs-lookup"><span data-stu-id="655f2-108">Identifier:</span></span>  <br/> |<span data-ttu-id="655f2-109">0x0072</span><span class="sxs-lookup"><span data-stu-id="655f2-109">0x0072</span></span>  <br/> |
|<span data-ttu-id="655f2-110">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="655f2-110">Data type:</span></span>  <br/> |<span data-ttu-id="655f2-111">PT_STRING8, PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="655f2-111">PT_STRING8, PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="655f2-112">Bereich:</span><span class="sxs-lookup"><span data-stu-id="655f2-112">Area:</span></span>  <br/> |<span data-ttu-id="655f2-113">Allgemeine messaging</span><span class="sxs-lookup"><span data-stu-id="655f2-113">General messaging</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="655f2-114">Hinweise</span><span class="sxs-lookup"><span data-stu-id="655f2-114">Remarks</span></span>

<span data-ttu-id="655f2-115">Diese Eigenschaften enthalten eine durch Semikolons getrennte Liste.</span><span class="sxs-lookup"><span data-stu-id="655f2-115">These properties contain a list separated by semicolons.</span></span> <span data-ttu-id="655f2-116">Sie MAPI bereitgestellten und direkt aus **PR_DISPLAY_BCC** ([PidTagDisplayBcc](pidtagdisplaybcc-canonical-property.md)) kopiert werden, wenn eine Lieferung oder Unzustellbarkeitsbericht oder einem Lese- oder nonread Bericht generiert wird.</span><span class="sxs-lookup"><span data-stu-id="655f2-116">They is furnished by MAPI and are copied directly from **PR_DISPLAY_BCC** ([PidTagDisplayBcc](pidtagdisplaybcc-canonical-property.md)) when a delivery or nondelivery report or a read or nonread report is generated.</span></span> <span data-ttu-id="655f2-117">Diese Eigenschaften können für andere Nachrichten durch ihre Nachrichtenklassen definierten vorhanden sein.</span><span class="sxs-lookup"><span data-stu-id="655f2-117">These properties may be present on other messages as defined by their message classes.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="655f2-118">Verwandte Ressourcen</span><span class="sxs-lookup"><span data-stu-id="655f2-118">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="655f2-119">Protokollspezifikationen</span><span class="sxs-lookup"><span data-stu-id="655f2-119">Protocol specifications</span></span>

<span data-ttu-id="655f2-120">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="655f2-120">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="655f2-121">Bietet Verweise auf Verwandte Exchange Server-Spezifikationen.</span><span class="sxs-lookup"><span data-stu-id="655f2-121">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="655f2-122">[[MS-OXOMSG]](http://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="655f2-122">[[MS-OXOMSG]](http://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="655f2-123">Gibt die Eigenschaften und Operationen, die für Objekte, die e-Mail-Nachricht zulässig sind.</span><span class="sxs-lookup"><span data-stu-id="655f2-123">Specifies the properties and operations that are permissible on email message objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="655f2-124">Header-Dateien</span><span class="sxs-lookup"><span data-stu-id="655f2-124">Header files</span></span>

<span data-ttu-id="655f2-125">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="655f2-125">Mapidefs.h</span></span>
  
> <span data-ttu-id="655f2-126">Enthält die Datentypdefinitionen.</span><span class="sxs-lookup"><span data-stu-id="655f2-126">Provides data type definitions.</span></span>
    
<span data-ttu-id="655f2-127">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="655f2-127">Mapitags.h</span></span>
  
> <span data-ttu-id="655f2-128">Enthält Definitionen von Eigenschaften, die als Alternative Namen aufgelistet.</span><span class="sxs-lookup"><span data-stu-id="655f2-128">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="655f2-129">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="655f2-129">See also</span></span>



[<span data-ttu-id="655f2-130">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="655f2-130">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="655f2-131">Kanonische MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="655f2-131">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="655f2-132">Zuordnen von kanonischen Eigenschaftennamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="655f2-132">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="655f2-133">Zuordnen von MAPI-Namen zu kanonische Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="655f2-133">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

