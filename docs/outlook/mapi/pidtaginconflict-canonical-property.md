---
title: Kanonische PidTagInConflict-Eigenschaft
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagInConflict
api_type:
- HeaderDef
ms.assetid: e83c05c6-a7c0-486c-a112-58a39255767a
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: 573e0ba37d4117d85193933a3a5045b5060fbd3d
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19794481"
---
# <a name="pidtaginconflict-canonical-property"></a><span data-ttu-id="51274-103">Kanonische PidTagInConflict-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="51274-103">PidTagInConflict Canonical Property</span></span>

  
  
<span data-ttu-id="51274-104">**Betrifft**: Outlook</span><span class="sxs-lookup"><span data-stu-id="51274-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="51274-105">Enthält True, wenn die Anlage eine alternative Replikat darstellt.</span><span class="sxs-lookup"><span data-stu-id="51274-105">Contains TRUE when the attachment represents an alternate replica.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="51274-106">Zugeordneten Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="51274-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="51274-107">PR_IN_CONFLICT</span><span class="sxs-lookup"><span data-stu-id="51274-107">PR_IN_CONFLICT</span></span>  <br/> |
|<span data-ttu-id="51274-108">Bezeichner:</span><span class="sxs-lookup"><span data-stu-id="51274-108">Identifier:</span></span>  <br/> |<span data-ttu-id="51274-109">0x666C</span><span class="sxs-lookup"><span data-stu-id="51274-109">0x666C</span></span>  <br/> |
|<span data-ttu-id="51274-110">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="51274-110">Data type:</span></span>  <br/> |<span data-ttu-id="51274-111">PT_BOOLEAN</span><span class="sxs-lookup"><span data-stu-id="51274-111">PT_BOOLEAN</span></span>  <br/> |
|<span data-ttu-id="51274-112">Bereich:</span><span class="sxs-lookup"><span data-stu-id="51274-112">Area:</span></span>  <br/> |<span data-ttu-id="51274-113">Conflict-Hinweis</span><span class="sxs-lookup"><span data-stu-id="51274-113">Conflict note</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="51274-114">Hinweise</span><span class="sxs-lookup"><span data-stu-id="51274-114">Remarks</span></span>

<span data-ttu-id="51274-115">Die e-Mail-Client und Server müssen eine Konflikt auflösen Nachricht generieren, wenn einen Konflikt mit der aktuellen Version einer Nachricht in das Replikat während der Synchronisierung zu erkennen.</span><span class="sxs-lookup"><span data-stu-id="51274-115">The email client and server must generate a conflict resolve message when detecting a conflict against the current version of a message in the replica during synchronization.</span></span> <span data-ttu-id="51274-116">Es ist wichtig zu verstehen, dass es möglich ist, dass die aktuelle Version der Nachricht in dem lokalen Replikat während der aktuellen Synchronisierungsvorgang übermittelt wurde.</span><span class="sxs-lookup"><span data-stu-id="51274-116">It is important to understand that it is possible that the current version of the message in the local replica was transmitted during the current synchronization operation.</span></span> <span data-ttu-id="51274-117">Das passiert, wenn Sie der Konflikt bereits auf dem Server vorhanden ist, bevor in einer miteinander in Konflikt stehende auf dem lokalen Replikat heruntergeladen wurden.</span><span class="sxs-lookup"><span data-stu-id="51274-117">This will happen when the conflict already exists on the server before any of the conflicting messages were downloaded to the local replica.</span></span> <span data-ttu-id="51274-118">Ein Konflikt beheben, dass die Nachricht als unabhängiger Replikate mit miteinander in Konflikt stehende PCLs synchronisiert werden muss.</span><span class="sxs-lookup"><span data-stu-id="51274-118">A conflict resolve message must be synchronized as independent replicas with conflicting PCLs.</span></span> <span data-ttu-id="51274-119">Der Konflikt aufgelöst werden kann, dass die Nachricht selbst nicht zwischen Client und Server synchronisiert werden muss. nur die unabhängige Replikate sollte ausgetauscht werden.</span><span class="sxs-lookup"><span data-stu-id="51274-119">The conflict resolve message itself must not be synchronized between client and server; only the independent replicas should be exchanged.</span></span> <span data-ttu-id="51274-120">Der Synchronisierungspartner muss dann eine neue Nachricht generieren, die die Struktur der Konfliktnachricht entspricht.</span><span class="sxs-lookup"><span data-stu-id="51274-120">The synchronization partner must then generate a new message that matches the structure of the conflict message.</span></span> <span data-ttu-id="51274-121">Aus diesem Grund ist es wichtig, dass Client und Server den gleichen Algorithmus verwenden, um das Element "Gewinner" zu erkennen.</span><span class="sxs-lookup"><span data-stu-id="51274-121">Therefore, it is important that client and server use the same algorithm to detect the "winner" item.</span></span> <span data-ttu-id="51274-122">Die folgenden Regeln müssen angewendet werden, um zu ermitteln, den "Gewinner":</span><span class="sxs-lookup"><span data-stu-id="51274-122">The following rules must be applied to detect the "winner":</span></span>
  
1. <span data-ttu-id="51274-123">Zeitpunkt der letzten Änderung.</span><span class="sxs-lookup"><span data-stu-id="51274-123">Last modification time.</span></span>
    
2. <span data-ttu-id="51274-124">Höhere CN GUID (Verwendung von Arbeitsspeicher Compare) Tie unterbrochen.</span><span class="sxs-lookup"><span data-stu-id="51274-124">Higher CN GUID (using memory compare) to break tie.</span></span>
    
## <a name="related-resources"></a><span data-ttu-id="51274-125">Verwandte Ressourcen</span><span class="sxs-lookup"><span data-stu-id="51274-125">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="51274-126">Protokollspezifikationen</span><span class="sxs-lookup"><span data-stu-id="51274-126">Protocol specifications</span></span>

<span data-ttu-id="51274-127">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="51274-127">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="51274-128">Bietet Verweise auf Verwandte Exchange Server-Spezifikationen.</span><span class="sxs-lookup"><span data-stu-id="51274-128">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="51274-129">[[MS-OXCFXICS]](http://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="51274-129">[[MS-OXCFXICS]](http://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="51274-130">Synchronisieren von messaging Objektdaten zwischen einem Server und einem Client behandelt.</span><span class="sxs-lookup"><span data-stu-id="51274-130">Handles synchronizing messaging object data between a server and a client.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="51274-131">Header-Dateien</span><span class="sxs-lookup"><span data-stu-id="51274-131">Header files</span></span>

<span data-ttu-id="51274-132">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="51274-132">Mapidefs.h</span></span>
  
> <span data-ttu-id="51274-133">Enthält die Datentypdefinitionen.</span><span class="sxs-lookup"><span data-stu-id="51274-133">Provides data type definitions.</span></span>
    
<span data-ttu-id="51274-134">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="51274-134">Mapitags.h</span></span>
  
> <span data-ttu-id="51274-135">Enthält Definitionen von Eigenschaften, die als zugeordneten Eigenschaften aufgelistet.</span><span class="sxs-lookup"><span data-stu-id="51274-135">Contains definitions of properties listed as associated properties.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="51274-136">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="51274-136">See also</span></span>



[<span data-ttu-id="51274-137">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="51274-137">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="51274-138">Kanonische MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="51274-138">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="51274-139">Zuordnen von kanonischen Eigenschaftennamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="51274-139">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="51274-140">Zuordnen von MAPI-Namen zu kanonische Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="51274-140">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

