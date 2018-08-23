---
title: PidTagOriginalDisplayBcc (kanonische Eigenschaft)
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
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 20f70f9e7bfecd955eb6bfb1c05c6b2010cb52cd
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2018
ms.locfileid: "22563408"
---
# <a name="pidtagoriginaldisplaybcc-canonical-property"></a><span data-ttu-id="71b0c-103">PidTagOriginalDisplayBcc (kanonische Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="71b0c-103">PidTagOriginalDisplayBcc Canonical Property</span></span>

  
  
<span data-ttu-id="71b0c-104">**Betrifft**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="71b0c-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="71b0c-105">Enthält die Anzeigenamen der Empfänger blind Carbon Copy, Blindkopie (BCC) der ursprünglichen Nachricht.</span><span class="sxs-lookup"><span data-stu-id="71b0c-105">Contains the display names of any blind carbon copy (BCC) recipients of the original message.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="71b0c-106">Zugeordnete Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="71b0c-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="71b0c-107">PR_ORIGINAL_DISPLAY_BCC, PR_ORIGINAL_DISPLAY_BCC_A, PR_ORIGINAL_DISPLAY_BCC_W</span><span class="sxs-lookup"><span data-stu-id="71b0c-107">PR_ORIGINAL_DISPLAY_BCC, PR_ORIGINAL_DISPLAY_BCC_A, PR_ORIGINAL_DISPLAY_BCC_W</span></span>  <br/> |
|<span data-ttu-id="71b0c-108">Kennung:</span><span class="sxs-lookup"><span data-stu-id="71b0c-108">Identifier:</span></span>  <br/> |<span data-ttu-id="71b0c-109">0x0072</span><span class="sxs-lookup"><span data-stu-id="71b0c-109">0x0072</span></span>  <br/> |
|<span data-ttu-id="71b0c-110">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="71b0c-110">Data type:</span></span>  <br/> |<span data-ttu-id="71b0c-111">PT_STRING8, PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="71b0c-111">PT_STRING8, PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="71b0c-112">Bereich:</span><span class="sxs-lookup"><span data-stu-id="71b0c-112">Area:</span></span>  <br/> |<span data-ttu-id="71b0c-113">Allgemeine messaging</span><span class="sxs-lookup"><span data-stu-id="71b0c-113">General messaging</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="71b0c-114">HinwBemerkungeneise</span><span class="sxs-lookup"><span data-stu-id="71b0c-114">Remarks</span></span>

<span data-ttu-id="71b0c-115">Diese Eigenschaften enthalten eine durch Semikolons getrennte Liste.</span><span class="sxs-lookup"><span data-stu-id="71b0c-115">These properties contain a list separated by semicolons.</span></span> <span data-ttu-id="71b0c-116">Sie MAPI bereitgestellten und direkt aus **PR_DISPLAY_BCC** ([PidTagDisplayBcc](pidtagdisplaybcc-canonical-property.md)) kopiert werden, wenn eine Lieferung oder Unzustellbarkeitsbericht oder einem Lese- oder nonread Bericht generiert wird.</span><span class="sxs-lookup"><span data-stu-id="71b0c-116">They is furnished by MAPI and are copied directly from **PR_DISPLAY_BCC** ([PidTagDisplayBcc](pidtagdisplaybcc-canonical-property.md)) when a delivery or nondelivery report or a read or nonread report is generated.</span></span> <span data-ttu-id="71b0c-117">Diese Eigenschaften können für andere Nachrichten durch ihre Nachrichtenklassen definierten vorhanden sein.</span><span class="sxs-lookup"><span data-stu-id="71b0c-117">These properties may be present on other messages as defined by their message classes.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="71b0c-118">Verwandte Ressourcen</span><span class="sxs-lookup"><span data-stu-id="71b0c-118">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="71b0c-119">Protokollspezifikationen</span><span class="sxs-lookup"><span data-stu-id="71b0c-119">Protocol specifications</span></span>

<span data-ttu-id="71b0c-120">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="71b0c-120">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="71b0c-121">Bietet Verweise auf Verwandte Exchange Server-Spezifikationen.</span><span class="sxs-lookup"><span data-stu-id="71b0c-121">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="71b0c-122">[[MS-OXOMSG]](http://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="71b0c-122">[[MS-OXOMSG]](http://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="71b0c-123">Gibt die Eigenschaften und Operationen, die für Objekte, die e-Mail-Nachricht zulässig sind.</span><span class="sxs-lookup"><span data-stu-id="71b0c-123">Specifies the properties and operations that are permissible on email message objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="71b0c-124">Header-Dateien</span><span class="sxs-lookup"><span data-stu-id="71b0c-124">Header files</span></span>

<span data-ttu-id="71b0c-125">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="71b0c-125">Mapidefs.h</span></span>
  
> <span data-ttu-id="71b0c-126">Enthält die Datentypdefinitionen.</span><span class="sxs-lookup"><span data-stu-id="71b0c-126">Provides data type definitions.</span></span>
    
<span data-ttu-id="71b0c-127">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="71b0c-127">Mapitags.h</span></span>
  
> <span data-ttu-id="71b0c-128">Enthält Definitionen von Eigenschaften, die als Alternative Namen aufgelistet.</span><span class="sxs-lookup"><span data-stu-id="71b0c-128">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="71b0c-129">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="71b0c-129">See also</span></span>



[<span data-ttu-id="71b0c-130">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="71b0c-130">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="71b0c-131">Kanonische MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="71b0c-131">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="71b0c-132">Zuordnen von kanonischen Eigenschaftennamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="71b0c-132">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="71b0c-133">Zuordnen von MAPI-Namen zu kanonische Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="71b0c-133">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

