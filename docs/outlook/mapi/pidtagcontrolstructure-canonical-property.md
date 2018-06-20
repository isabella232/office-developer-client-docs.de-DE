---
title: Kanonische PidTagControlStructure-Eigenschaft
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagControlStructure
api_type:
- HeaderDef
ms.assetid: 02910389-b346-431c-a282-dedbc9f7dfc6
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: e531c986ef6de2eccca446f5d560290fed831c21
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19794252"
---
# <a name="pidtagcontrolstructure-canonical-property"></a><span data-ttu-id="ce8a1-103">Kanonische PidTagControlStructure-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="ce8a1-103">PidTagControlStructure Canonical Property</span></span>

  
  
<span data-ttu-id="ce8a1-104">**Betrifft**: Outlook</span><span class="sxs-lookup"><span data-stu-id="ce8a1-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="ce8a1-105">Enthält einen Zeiger auf eine Struktur für ein Steuerelement in einem Dialogfeld verwendet.</span><span class="sxs-lookup"><span data-stu-id="ce8a1-105">Contains a pointer to a structure for a control used in a dialog box.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="ce8a1-106">Zugeordneten Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="ce8a1-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="ce8a1-107">PR_CONTROL_STRUCTURE</span><span class="sxs-lookup"><span data-stu-id="ce8a1-107">PR_CONTROL_STRUCTURE</span></span>  <br/> |
|<span data-ttu-id="ce8a1-108">Bezeichner:</span><span class="sxs-lookup"><span data-stu-id="ce8a1-108">Identifier:</span></span>  <br/> |<span data-ttu-id="ce8a1-109">0x3F01</span><span class="sxs-lookup"><span data-stu-id="ce8a1-109">0x3F01</span></span>  <br/> |
|<span data-ttu-id="ce8a1-110">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="ce8a1-110">Data type:</span></span>  <br/> |<span data-ttu-id="ce8a1-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="ce8a1-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="ce8a1-112">Bereich:</span><span class="sxs-lookup"><span data-stu-id="ce8a1-112">Area:</span></span>  <br/> |<span data-ttu-id="ce8a1-113">Zeigt die MAPI-Tabelle</span><span class="sxs-lookup"><span data-stu-id="ce8a1-113">MAPI display table</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="ce8a1-114">Hinweise</span><span class="sxs-lookup"><span data-stu-id="ce8a1-114">Remarks</span></span>

<span data-ttu-id="ce8a1-115">Diese Eigenschaft stellt einen langen Zeiger, der auf eine der Steuerelement-Strukturen umgewandelt wird.</span><span class="sxs-lookup"><span data-stu-id="ce8a1-115">This property represents a long pointer that is cast to one of the control structures.</span></span> <span data-ttu-id="ce8a1-116">Die Steuerstrukturen umfassen:</span><span class="sxs-lookup"><span data-stu-id="ce8a1-116">The control structures include:</span></span>
  
|||
|:-----|:-----|
|[<span data-ttu-id="ce8a1-117">DTBLBUTTON</span><span class="sxs-lookup"><span data-stu-id="ce8a1-117">DTBLBUTTON</span></span>](dtblbutton.md) <br/> |[<span data-ttu-id="ce8a1-118">DTBLCHECKBOX</span><span class="sxs-lookup"><span data-stu-id="ce8a1-118">DTBLCHECKBOX</span></span>](dtblcheckbox.md) <br/> |
|[<span data-ttu-id="ce8a1-119">DTBLCOMBOBOX</span><span class="sxs-lookup"><span data-stu-id="ce8a1-119">DTBLCOMBOBOX</span></span>](dtblcombobox.md) <br/> |[<span data-ttu-id="ce8a1-120">DTBLDDLBX</span><span class="sxs-lookup"><span data-stu-id="ce8a1-120">DTBLDDLBX</span></span>](dtblddlbx.md) <br/> |
|[<span data-ttu-id="ce8a1-121">DTBLEDIT</span><span class="sxs-lookup"><span data-stu-id="ce8a1-121">DTBLEDIT</span></span>](dtbledit.md) <br/> |[<span data-ttu-id="ce8a1-122">DTBLGROUPBOX</span><span class="sxs-lookup"><span data-stu-id="ce8a1-122">DTBLGROUPBOX</span></span>](dtblgroupbox.md) <br/> |
|[<span data-ttu-id="ce8a1-123">DTBLLABEL</span><span class="sxs-lookup"><span data-stu-id="ce8a1-123">DTBLLABEL</span></span>](dtbllabel.md) <br/> |[<span data-ttu-id="ce8a1-124">DTBLLBX</span><span class="sxs-lookup"><span data-stu-id="ce8a1-124">DTBLLBX</span></span>](dtbllbx.md) <br/> |
|[<span data-ttu-id="ce8a1-125">DTBLMVDDLBOX</span><span class="sxs-lookup"><span data-stu-id="ce8a1-125">DTBLMVDDLBOX</span></span>](dtblmvddlbox.md) <br/> |[<span data-ttu-id="ce8a1-126">DTBLMVLISTBOX</span><span class="sxs-lookup"><span data-stu-id="ce8a1-126">DTBLMVLISTBOX</span></span>](dtblmvlistbox.md) <br/> |
|[<span data-ttu-id="ce8a1-127">DTBLPAGE</span><span class="sxs-lookup"><span data-stu-id="ce8a1-127">DTBLPAGE</span></span>](dtblpage.md) <br/> |[<span data-ttu-id="ce8a1-128">DTBLRADIOBUTTON</span><span class="sxs-lookup"><span data-stu-id="ce8a1-128">DTBLRADIOBUTTON</span></span>](dtblradiobutton.md) <br/> |
   
## <a name="related-resources"></a><span data-ttu-id="ce8a1-129">Verwandte Ressourcen</span><span class="sxs-lookup"><span data-stu-id="ce8a1-129">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="ce8a1-130">Header-Dateien</span><span class="sxs-lookup"><span data-stu-id="ce8a1-130">Header files</span></span>

<span data-ttu-id="ce8a1-131">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="ce8a1-131">Mapidefs.h</span></span>
  
> <span data-ttu-id="ce8a1-132">Enthält die Datentypdefinitionen.</span><span class="sxs-lookup"><span data-stu-id="ce8a1-132">Provides data type definitions.</span></span>
    
<span data-ttu-id="ce8a1-133">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="ce8a1-133">Mapitags.h</span></span>
  
> <span data-ttu-id="ce8a1-134">Enthält Definitionen von Eigenschaften, die als Alternative Namen aufgelistet.</span><span class="sxs-lookup"><span data-stu-id="ce8a1-134">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="ce8a1-135">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="ce8a1-135">See also</span></span>



[<span data-ttu-id="ce8a1-136">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="ce8a1-136">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="ce8a1-137">Kanonische MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="ce8a1-137">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="ce8a1-138">Zuordnen von kanonischen Eigenschaftennamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="ce8a1-138">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="ce8a1-139">Zuordnen von MAPI-Namen zu kanonische Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="ce8a1-139">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

