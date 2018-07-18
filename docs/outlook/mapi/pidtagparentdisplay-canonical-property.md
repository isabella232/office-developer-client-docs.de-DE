---
title: PidTagParentDisplay (kanonische Eigenschaft)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagParentDisplay
api_type:
- COM
ms.assetid: 6a36f4fb-17c0-4271-87d4-a92895f35f23
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: ce9fea80a2dfed25002e5500dd4defaf5ff04421
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19794784"
---
# <a name="pidtagparentdisplay-canonical-property"></a><span data-ttu-id="f9f88-103">PidTagParentDisplay (kanonische Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="f9f88-103">PidTagParentDisplay Canonical Property</span></span>

  
  
<span data-ttu-id="f9f88-104">**Betrifft**: Outlook</span><span class="sxs-lookup"><span data-stu-id="f9f88-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="f9f88-105">Enthält den Anzeigenamen des Ordners, in dem eine Nachricht während eines Suchvorgangs gefunden wurde.</span><span class="sxs-lookup"><span data-stu-id="f9f88-105">Contains the display name of the folder where a message was found during a search.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="f9f88-106">Zugeordneten Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="f9f88-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="f9f88-107">PR_PARENT_DISPLAY, PR_PARENT_DISPLAY_A, PR_PARENT_DISPLAY_W</span><span class="sxs-lookup"><span data-stu-id="f9f88-107">PR_PARENT_DISPLAY, PR_PARENT_DISPLAY_A, PR_PARENT_DISPLAY_W</span></span>  <br/> |
|<span data-ttu-id="f9f88-108">Bezeichner:</span><span class="sxs-lookup"><span data-stu-id="f9f88-108">Identifier:</span></span>  <br/> |<span data-ttu-id="f9f88-109">0x0E05</span><span class="sxs-lookup"><span data-stu-id="f9f88-109">0x0E05</span></span>  <br/> |
|<span data-ttu-id="f9f88-110">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="f9f88-110">Data type:</span></span>  <br/> |<span data-ttu-id="f9f88-111">PT_STRING8, PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="f9f88-111">PT_STRING8, PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="f9f88-112">Bereich:</span><span class="sxs-lookup"><span data-stu-id="f9f88-112">Area:</span></span>  <br/> |<span data-ttu-id="f9f88-113">MAPI Übertragungseinehit</span><span class="sxs-lookup"><span data-stu-id="f9f88-113">MAPI non-transmittable</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="f9f88-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="f9f88-114">Remarks</span></span>

<span data-ttu-id="f9f88-115">Diese Eigenschaften ist nicht für jedes Objekt.</span><span class="sxs-lookup"><span data-stu-id="f9f88-115">These properties is not on any object.</span></span> <span data-ttu-id="f9f88-116">Sie können nur in der Inhaltstabelle eines Ordners Suchergebnisse angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="f9f88-116">They can only appear in the contents table of a search-results folder.</span></span>
  
<span data-ttu-id="f9f88-117">Diese Eigenschaften und **PR_PARENT_ENTRYID** ([PidTagParentEntryId](pidtagparententryid-canonical-property.md)) Eigenschaften sind nicht miteinander verknüpft.</span><span class="sxs-lookup"><span data-stu-id="f9f88-117">These properties and **PR_PARENT_ENTRYID** ([PidTagParentEntryId](pidtagparententryid-canonical-property.md)) properties are not related to each other.</span></span> <span data-ttu-id="f9f88-118">Zielgerichtet auf völlig andere Kontexte.</span><span class="sxs-lookup"><span data-stu-id="f9f88-118">They belong to entirely different contexts.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="f9f88-119">Verwandte Ressourcen</span><span class="sxs-lookup"><span data-stu-id="f9f88-119">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="f9f88-120">Header-Dateien</span><span class="sxs-lookup"><span data-stu-id="f9f88-120">Header files</span></span>

<span data-ttu-id="f9f88-121">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="f9f88-121">Mapidefs.h</span></span>
  
> <span data-ttu-id="f9f88-122">Enthält die Datentypdefinitionen.</span><span class="sxs-lookup"><span data-stu-id="f9f88-122">Provides data type definitions.</span></span>
    
<span data-ttu-id="f9f88-123">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="f9f88-123">Mapitags.h</span></span>
  
> <span data-ttu-id="f9f88-124">Enthält Definitionen von Eigenschaften, die als Alternative Namen aufgelistet.</span><span class="sxs-lookup"><span data-stu-id="f9f88-124">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="f9f88-125">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="f9f88-125">See also</span></span>



[<span data-ttu-id="f9f88-126">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="f9f88-126">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="f9f88-127">Kanonische MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="f9f88-127">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="f9f88-128">Zuordnen von kanonischen Eigenschaftennamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="f9f88-128">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="f9f88-129">Zuordnen von MAPI-Namen zu kanonische Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="f9f88-129">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

