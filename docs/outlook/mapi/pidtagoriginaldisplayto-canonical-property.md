---
title: PidTagOriginalDisplayTo (kanonische Eigenschaft)
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
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 5a2f60051e5cb0717926a5c3e2f878a49919b04c
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32342701"
---
# <a name="pidtagoriginaldisplayto-canonical-property"></a><span data-ttu-id="bc7ab-103">PidTagOriginalDisplayTo (kanonische Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="bc7ab-103">PidTagOriginalDisplayTo Canonical Property</span></span>

  
  
<span data-ttu-id="bc7ab-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="bc7ab-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="bc7ab-105">Enthält die Anzeigenamen der primären Empfänger (An) der ursprünglichen Nachricht.</span><span class="sxs-lookup"><span data-stu-id="bc7ab-105">Contains the display names of the primary (To) recipients of the original message.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="bc7ab-106">Zugeordnete Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="bc7ab-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="bc7ab-107">PR_ORIGINAL_DISPLAY_TO, PR_ORIGINAL_DISPLAY_TO_A, PR_ORIGINAL_DISPLAY_TO_W</span><span class="sxs-lookup"><span data-stu-id="bc7ab-107">PR_ORIGINAL_DISPLAY_TO, PR_ORIGINAL_DISPLAY_TO_A, PR_ORIGINAL_DISPLAY_TO_W</span></span>  <br/> |
|<span data-ttu-id="bc7ab-108">Kennung:</span><span class="sxs-lookup"><span data-stu-id="bc7ab-108">Identifier:</span></span>  <br/> |<span data-ttu-id="bc7ab-109">0x0074</span><span class="sxs-lookup"><span data-stu-id="bc7ab-109">0x0074</span></span>  <br/> |
|<span data-ttu-id="bc7ab-110">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="bc7ab-110">Data type:</span></span>  <br/> |<span data-ttu-id="bc7ab-111">PT_STRING8, PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="bc7ab-111">PT_STRING8, PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="bc7ab-112">Bereich:</span><span class="sxs-lookup"><span data-stu-id="bc7ab-112">Area:</span></span>  <br/> |<span data-ttu-id="bc7ab-113">Allgemeines Messaging</span><span class="sxs-lookup"><span data-stu-id="bc7ab-113">General messaging</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="bc7ab-114">Hinweise</span><span class="sxs-lookup"><span data-stu-id="bc7ab-114">Remarks</span></span>

<span data-ttu-id="bc7ab-115">Diese Eigenschaften enthalten eine DURCH Semikolons getrennte ASCII-Liste.</span><span class="sxs-lookup"><span data-stu-id="bc7ab-115">These properties contain an ASCII list separated by semicolons.</span></span> <span data-ttu-id="bc7ab-116">Sie wird von MAPI eingerichtet und direkt aus **PR_DISPLAY_TO** ([PidTagDisplayTo](pidtagdisplayto-canonical-property.md)) kopiert, wenn ein Zustellungs- oder Nichtablagebericht oder ein Lese- oder Ungelesenbericht generiert wird.</span><span class="sxs-lookup"><span data-stu-id="bc7ab-116">It is furnished by MAPI and is copied directly from **PR_DISPLAY_TO** ([PidTagDisplayTo](pidtagdisplayto-canonical-property.md)) when a delivery or nondelivery report or a read or nonread report is generated.</span></span> <span data-ttu-id="bc7ab-117">Diese Eigenschaft kann für andere Nachrichten vorhanden sein, wie durch ihre Nachrichtenklassen definiert.</span><span class="sxs-lookup"><span data-stu-id="bc7ab-117">This property may be present on other messages as defined by their message classes.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="bc7ab-118">Verwandte Ressourcen</span><span class="sxs-lookup"><span data-stu-id="bc7ab-118">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="bc7ab-119">Protokollspezifikationen</span><span class="sxs-lookup"><span data-stu-id="bc7ab-119">Protocol specifications</span></span>

<span data-ttu-id="bc7ab-120">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="bc7ab-120">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="bc7ab-121">Enthält Verweise auf Exchange Server Protokollspezifikationen.</span><span class="sxs-lookup"><span data-stu-id="bc7ab-121">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="bc7ab-122">[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="bc7ab-122">[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="bc7ab-123">Gibt die Eigenschaften und Vorgänge an, die für E-Mail-Nachrichtenobjekte zulässig sind.</span><span class="sxs-lookup"><span data-stu-id="bc7ab-123">Specifies the properties and operations that are permissible on email message objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="bc7ab-124">Headerdateien</span><span class="sxs-lookup"><span data-stu-id="bc7ab-124">Header files</span></span>

<span data-ttu-id="bc7ab-125">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="bc7ab-125">Mapidefs.h</span></span>
  
> <span data-ttu-id="bc7ab-126">Bietet Datentypdefinitionen.</span><span class="sxs-lookup"><span data-stu-id="bc7ab-126">Provides data type definitions.</span></span>
    
<span data-ttu-id="bc7ab-127">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="bc7ab-127">Mapitags.h</span></span>
  
> <span data-ttu-id="bc7ab-128">Enthält Definitionen von Eigenschaften, die als alternative Namen aufgeführt sind.</span><span class="sxs-lookup"><span data-stu-id="bc7ab-128">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="bc7ab-129">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="bc7ab-129">See also</span></span>



[<span data-ttu-id="bc7ab-130">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="bc7ab-130">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="bc7ab-131">KANONISCHE EIGENSCHAFTEN VON MAPI</span><span class="sxs-lookup"><span data-stu-id="bc7ab-131">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="bc7ab-132">Zuordnen kanonischer Eigenschaftsnamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="bc7ab-132">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="bc7ab-133">Zuordnen von MAPI-Namen zu kanonischen Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="bc7ab-133">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

