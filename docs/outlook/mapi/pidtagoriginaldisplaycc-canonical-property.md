---
title: PidTagOriginalDisplayCc (kanonische Eigenschaft)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagOriginalDisplayCc
api_type:
- COM
ms.assetid: f48d723c-3ad8-4617-952a-ba5216b2129c
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 9eb90d353705434803ff617ff2b355c7c96359b7
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32355622"
---
# <a name="pidtagoriginaldisplaycc-canonical-property"></a><span data-ttu-id="8df2c-103">PidTagOriginalDisplayCc (kanonische Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="8df2c-103">PidTagOriginalDisplayCc Canonical Property</span></span>

  
  
<span data-ttu-id="8df2c-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="8df2c-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="8df2c-105">Enthält die Anzeigenamen aller Carbon Copy (CC)-Empfänger der ursprünglichen Nachricht.</span><span class="sxs-lookup"><span data-stu-id="8df2c-105">Contains the display names of any carbon copy (CC) recipients of the original message.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="8df2c-106">Zugeordnete Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="8df2c-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="8df2c-107">PR_ORIGINAL_DISPLAY_CC, PR_ORIGINAL_DISPLAY_CC_A, PR_ORIGINAL_DISPLAY_CC_W</span><span class="sxs-lookup"><span data-stu-id="8df2c-107">PR_ORIGINAL_DISPLAY_CC, PR_ORIGINAL_DISPLAY_CC_A, PR_ORIGINAL_DISPLAY_CC_W</span></span>  <br/> |
|<span data-ttu-id="8df2c-108">Kennung:</span><span class="sxs-lookup"><span data-stu-id="8df2c-108">Identifier:</span></span>  <br/> |<span data-ttu-id="8df2c-109">0x0073</span><span class="sxs-lookup"><span data-stu-id="8df2c-109">0x0073</span></span>  <br/> |
|<span data-ttu-id="8df2c-110">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="8df2c-110">Data type:</span></span>  <br/> |<span data-ttu-id="8df2c-111">PT_STRING8, PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="8df2c-111">PT_STRING8, PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="8df2c-112">Bereich:</span><span class="sxs-lookup"><span data-stu-id="8df2c-112">Area:</span></span>  <br/> |<span data-ttu-id="8df2c-113">Allgemeines Messaging</span><span class="sxs-lookup"><span data-stu-id="8df2c-113">General messaging</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="8df2c-114">Hinweise</span><span class="sxs-lookup"><span data-stu-id="8df2c-114">Remarks</span></span>

<span data-ttu-id="8df2c-115">Diese Eigenschaften enthalten eine Durch Semikolons getrennte Liste.</span><span class="sxs-lookup"><span data-stu-id="8df2c-115">These properties contain a list separated by semicolons.</span></span> <span data-ttu-id="8df2c-116">Sie wird von MAPI eingerichtet und direkt aus **PR_DISPLAY_CC** ([PidTagDisplayCc](pidtagdisplaycc-canonical-property.md)) kopiert, wenn ein Zustellungs- oder Nichtablagebericht oder ein Lese- oder Ungelesenbericht generiert wird.</span><span class="sxs-lookup"><span data-stu-id="8df2c-116">It is furnished by MAPI and is copied directly from **PR_DISPLAY_CC** ([PidTagDisplayCc](pidtagdisplaycc-canonical-property.md)) when a delivery or nondelivery report or a read or nonread report is generated.</span></span> <span data-ttu-id="8df2c-117">Diese Eigenschaft kann für andere Nachrichten vorhanden sein, wie durch ihre Nachrichtenklassen definiert.</span><span class="sxs-lookup"><span data-stu-id="8df2c-117">This property may be present on other messages as defined by their message classes.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="8df2c-118">Verwandte Ressourcen</span><span class="sxs-lookup"><span data-stu-id="8df2c-118">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="8df2c-119">Protokollspezifikationen</span><span class="sxs-lookup"><span data-stu-id="8df2c-119">Protocol specifications</span></span>

<span data-ttu-id="8df2c-120">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="8df2c-120">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="8df2c-121">Enthält Verweise auf Exchange Server Protokollspezifikationen.</span><span class="sxs-lookup"><span data-stu-id="8df2c-121">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="8df2c-122">[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="8df2c-122">[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="8df2c-123">Gibt die Eigenschaften und Vorgänge an, die für E-Mail-Nachrichtenobjekte zulässig sind.</span><span class="sxs-lookup"><span data-stu-id="8df2c-123">Specifies the properties and operations that are permissible on email message objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="8df2c-124">Headerdateien</span><span class="sxs-lookup"><span data-stu-id="8df2c-124">Header files</span></span>

<span data-ttu-id="8df2c-125">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="8df2c-125">Mapidefs.h</span></span>
  
> <span data-ttu-id="8df2c-126">Bietet Datentypdefinitionen.</span><span class="sxs-lookup"><span data-stu-id="8df2c-126">Provides data type definitions.</span></span>
    
<span data-ttu-id="8df2c-127">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="8df2c-127">Mapitags.h</span></span>
  
> <span data-ttu-id="8df2c-128">Enthält Definitionen von Eigenschaften, die als alternative Namen aufgeführt sind.</span><span class="sxs-lookup"><span data-stu-id="8df2c-128">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="8df2c-129">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="8df2c-129">See also</span></span>



[<span data-ttu-id="8df2c-130">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="8df2c-130">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="8df2c-131">KANONISCHE EIGENSCHAFTEN VON MAPI</span><span class="sxs-lookup"><span data-stu-id="8df2c-131">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="8df2c-132">Zuordnen kanonischer Eigenschaftsnamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="8df2c-132">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="8df2c-133">Zuordnen von MAPI-Namen zu kanonischen Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="8df2c-133">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

