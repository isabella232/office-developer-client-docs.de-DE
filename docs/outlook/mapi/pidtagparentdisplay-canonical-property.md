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
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 7aef4c1d83672033662502ad0950b7bac9f58c52
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33429502"
---
# <a name="pidtagparentdisplay-canonical-property"></a><span data-ttu-id="274ae-103">PidTagParentDisplay (kanonische Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="274ae-103">PidTagParentDisplay Canonical Property</span></span>

  
  
<span data-ttu-id="274ae-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="274ae-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="274ae-105">Enthält den Anzeigenamen des Ordners, in dem während einer Suche eine Nachricht gefunden wurde.</span><span class="sxs-lookup"><span data-stu-id="274ae-105">Contains the display name of the folder where a message was found during a search.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="274ae-106">Zugeordnete Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="274ae-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="274ae-107">PR_PARENT_DISPLAY, PR_PARENT_DISPLAY_A, PR_PARENT_DISPLAY_W</span><span class="sxs-lookup"><span data-stu-id="274ae-107">PR_PARENT_DISPLAY, PR_PARENT_DISPLAY_A, PR_PARENT_DISPLAY_W</span></span>  <br/> |
|<span data-ttu-id="274ae-108">Kennung:</span><span class="sxs-lookup"><span data-stu-id="274ae-108">Identifier:</span></span>  <br/> |<span data-ttu-id="274ae-109">0x0E05</span><span class="sxs-lookup"><span data-stu-id="274ae-109">0x0E05</span></span>  <br/> |
|<span data-ttu-id="274ae-110">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="274ae-110">Data type:</span></span>  <br/> |<span data-ttu-id="274ae-111">PT_STRING8, PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="274ae-111">PT_STRING8, PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="274ae-112">Bereich:</span><span class="sxs-lookup"><span data-stu-id="274ae-112">Area:</span></span>  <br/> |<span data-ttu-id="274ae-113">MAPI nicht durchlässig</span><span class="sxs-lookup"><span data-stu-id="274ae-113">MAPI non-transmittable</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="274ae-114">Hinweise</span><span class="sxs-lookup"><span data-stu-id="274ae-114">Remarks</span></span>

<span data-ttu-id="274ae-115">Diese Eigenschaften sind in keinem Objekt enthalten.</span><span class="sxs-lookup"><span data-stu-id="274ae-115">These properties is not on any object.</span></span> <span data-ttu-id="274ae-116">Sie können nur im Inhaltsverzeichnis eines Suchergebnisordners angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="274ae-116">They can only appear in the contents table of a search-results folder.</span></span>
  
<span data-ttu-id="274ae-117">Diese Eigenschaften und **PR_PARENT_ENTRYID** ([PidTagParentEntryId](pidtagparententryid-canonical-property.md)) sind nicht miteinander verknüpft.</span><span class="sxs-lookup"><span data-stu-id="274ae-117">These properties and **PR_PARENT_ENTRYID** ([PidTagParentEntryId](pidtagparententryid-canonical-property.md)) properties are not related to each other.</span></span> <span data-ttu-id="274ae-118">Sie gehören zu völlig unterschiedlichen Kontexten.</span><span class="sxs-lookup"><span data-stu-id="274ae-118">They belong to entirely different contexts.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="274ae-119">Verwandte Ressourcen</span><span class="sxs-lookup"><span data-stu-id="274ae-119">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="274ae-120">Headerdateien</span><span class="sxs-lookup"><span data-stu-id="274ae-120">Header files</span></span>

<span data-ttu-id="274ae-121">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="274ae-121">Mapidefs.h</span></span>
  
> <span data-ttu-id="274ae-122">Bietet Datentypdefinitionen.</span><span class="sxs-lookup"><span data-stu-id="274ae-122">Provides data type definitions.</span></span>
    
<span data-ttu-id="274ae-123">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="274ae-123">Mapitags.h</span></span>
  
> <span data-ttu-id="274ae-124">Enthält Definitionen von Eigenschaften, die als alternative Namen aufgeführt sind.</span><span class="sxs-lookup"><span data-stu-id="274ae-124">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="274ae-125">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="274ae-125">See also</span></span>



[<span data-ttu-id="274ae-126">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="274ae-126">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="274ae-127">KANONISCHE EIGENSCHAFTEN VON MAPI</span><span class="sxs-lookup"><span data-stu-id="274ae-127">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="274ae-128">Zuordnen kanonischer Eigenschaftsnamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="274ae-128">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="274ae-129">Zuordnen von MAPI-Namen zu kanonischen Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="274ae-129">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

