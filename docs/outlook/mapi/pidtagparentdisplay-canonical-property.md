---
title: Kanonische Pidtagparentdisplay (-Eigenschaft
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
# <a name="pidtagparentdisplay-canonical-property"></a><span data-ttu-id="892ad-103">Kanonische Pidtagparentdisplay (-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="892ad-103">PidTagParentDisplay Canonical Property</span></span>

  
  
<span data-ttu-id="892ad-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="892ad-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="892ad-105">Enthält den Anzeigenamen des Ordners, in dem eine Nachricht während einer Suche gefunden wurde.</span><span class="sxs-lookup"><span data-stu-id="892ad-105">Contains the display name of the folder where a message was found during a search.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="892ad-106">Zugeordnete Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="892ad-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="892ad-107">PR_PARENT_DISPLAY, PR_PARENT_DISPLAY_A, PR_PARENT_DISPLAY_W</span><span class="sxs-lookup"><span data-stu-id="892ad-107">PR_PARENT_DISPLAY, PR_PARENT_DISPLAY_A, PR_PARENT_DISPLAY_W</span></span>  <br/> |
|<span data-ttu-id="892ad-108">Kennung:</span><span class="sxs-lookup"><span data-stu-id="892ad-108">Identifier:</span></span>  <br/> |<span data-ttu-id="892ad-109">0x0E05</span><span class="sxs-lookup"><span data-stu-id="892ad-109">0x0E05</span></span>  <br/> |
|<span data-ttu-id="892ad-110">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="892ad-110">Data type:</span></span>  <br/> |<span data-ttu-id="892ad-111">PT_STRING8, PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="892ad-111">PT_STRING8, PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="892ad-112">Bereich:</span><span class="sxs-lookup"><span data-stu-id="892ad-112">Area:</span></span>  <br/> |<span data-ttu-id="892ad-113">Nicht transmitable MAPI</span><span class="sxs-lookup"><span data-stu-id="892ad-113">MAPI non-transmittable</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="892ad-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="892ad-114">Remarks</span></span>

<span data-ttu-id="892ad-115">Diese Eigenschaften befinden sich nicht in einem Objekt.</span><span class="sxs-lookup"><span data-stu-id="892ad-115">These properties is not on any object.</span></span> <span data-ttu-id="892ad-116">Sie können nur in der Tabelle Inhalt eines Ordners mit Suchergebnissen angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="892ad-116">They can only appear in the contents table of a search-results folder.</span></span>
  
<span data-ttu-id="892ad-117">Diese Eigenschaften und **PR_PARENT_ENTRYID** ([pidtagparententryid (](pidtagparententryid-canonical-property.md))-Eigenschaften sind nicht miteinander verbunden.</span><span class="sxs-lookup"><span data-stu-id="892ad-117">These properties and **PR_PARENT_ENTRYID** ([PidTagParentEntryId](pidtagparententryid-canonical-property.md)) properties are not related to each other.</span></span> <span data-ttu-id="892ad-118">Sie gehören ganz unterschiedlichen Kontexten.</span><span class="sxs-lookup"><span data-stu-id="892ad-118">They belong to entirely different contexts.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="892ad-119">Verwandte Ressourcen</span><span class="sxs-lookup"><span data-stu-id="892ad-119">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="892ad-120">Header Dateien</span><span class="sxs-lookup"><span data-stu-id="892ad-120">Header files</span></span>

<span data-ttu-id="892ad-121">Mapidefs. h</span><span class="sxs-lookup"><span data-stu-id="892ad-121">Mapidefs.h</span></span>
  
> <span data-ttu-id="892ad-122">Stellt Datentypdefinitionen bereit.</span><span class="sxs-lookup"><span data-stu-id="892ad-122">Provides data type definitions.</span></span>
    
<span data-ttu-id="892ad-123">Mapitags. h</span><span class="sxs-lookup"><span data-stu-id="892ad-123">Mapitags.h</span></span>
  
> <span data-ttu-id="892ad-124">Enthält Definitionen von Eigenschaften, die als Alternative Namen aufgeführt sind.</span><span class="sxs-lookup"><span data-stu-id="892ad-124">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="892ad-125">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="892ad-125">See also</span></span>



[<span data-ttu-id="892ad-126">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="892ad-126">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="892ad-127">Kanonische MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="892ad-127">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="892ad-128">Zuordnen von kanonischen Eigenschaftennamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="892ad-128">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="892ad-129">Zuordnen von MAPI-Namen zu kanonischen Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="892ad-129">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

