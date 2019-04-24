---
title: Kanonische Pidtaginconflict (-Eigenschaft
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
ms.openlocfilehash: fc2774efed1a15fe79e167149f2cb162bae7642c
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32358534"
---
# <a name="pidtaginconflict-canonical-property"></a><span data-ttu-id="6719d-103">Kanonische Pidtaginconflict (-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="6719d-103">PidTagInConflict Canonical Property</span></span>

  
  
<span data-ttu-id="6719d-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="6719d-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="6719d-105">Enthält TRUE, wenn die Anlage ein alternatives Replikat darstellt.</span><span class="sxs-lookup"><span data-stu-id="6719d-105">Contains TRUE when the attachment represents an alternate replica.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="6719d-106">Zugeordnete Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="6719d-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="6719d-107">PR_IN_CONFLICT</span><span class="sxs-lookup"><span data-stu-id="6719d-107">PR_IN_CONFLICT</span></span>  <br/> |
|<span data-ttu-id="6719d-108">Kennung:</span><span class="sxs-lookup"><span data-stu-id="6719d-108">Identifier:</span></span>  <br/> |<span data-ttu-id="6719d-109">0x666C</span><span class="sxs-lookup"><span data-stu-id="6719d-109">0x666C</span></span>  <br/> |
|<span data-ttu-id="6719d-110">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="6719d-110">Data type:</span></span>  <br/> |<span data-ttu-id="6719d-111">PT_BOOLEAN</span><span class="sxs-lookup"><span data-stu-id="6719d-111">PT_BOOLEAN</span></span>  <br/> |
|<span data-ttu-id="6719d-112">Bereich:</span><span class="sxs-lookup"><span data-stu-id="6719d-112">Area:</span></span>  <br/> |<span data-ttu-id="6719d-113">Konflikt Hinweis</span><span class="sxs-lookup"><span data-stu-id="6719d-113">Conflict note</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="6719d-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="6719d-114">Remarks</span></span>

<span data-ttu-id="6719d-115">Der e-Mail-Client und der Server müssen eine Konflikt Lösungs Meldung generieren, wenn ein Konflikt mit der aktuellen Version einer Nachricht im Replikat während der Synchronisierung ermittelt wird.</span><span class="sxs-lookup"><span data-stu-id="6719d-115">The email client and server must generate a conflict resolve message when detecting a conflict against the current version of a message in the replica during synchronization.</span></span> <span data-ttu-id="6719d-116">Es ist wichtig zu wissen, dass es möglich ist, dass die aktuelle Version der Nachricht im lokalen Replikat während des aktuellen Synchronisierungsvorgangs übertragen wurde.</span><span class="sxs-lookup"><span data-stu-id="6719d-116">It is important to understand that it is possible that the current version of the message in the local replica was transmitted during the current synchronization operation.</span></span> <span data-ttu-id="6719d-117">Dies geschieht, wenn der Konflikt bereits auf dem Server vorhanden ist, bevor eine der Konflikt verursachenden Nachrichten in das lokale Replikat heruntergeladen wurde.</span><span class="sxs-lookup"><span data-stu-id="6719d-117">This will happen when the conflict already exists on the server before any of the conflicting messages were downloaded to the local replica.</span></span> <span data-ttu-id="6719d-118">Eine Nachricht zur Konfliktbehebung muss als unabhängige Replikate mit widersprüchlichen PCLs synchronisiert werden.</span><span class="sxs-lookup"><span data-stu-id="6719d-118">A conflict resolve message must be synchronized as independent replicas with conflicting PCLs.</span></span> <span data-ttu-id="6719d-119">Die Nachricht zur Konfliktlösung selbst darf nicht zwischen Client und Server synchronisiert werden. nur die unabhängigen Replikate sollten ausgetauscht werden.</span><span class="sxs-lookup"><span data-stu-id="6719d-119">The conflict resolve message itself must not be synchronized between client and server; only the independent replicas should be exchanged.</span></span> <span data-ttu-id="6719d-120">Der Synchronisierungspartner muss dann eine neue Nachricht generieren, die mit der Struktur der Konfliktmeldung übereinstimmt.</span><span class="sxs-lookup"><span data-stu-id="6719d-120">The synchronization partner must then generate a new message that matches the structure of the conflict message.</span></span> <span data-ttu-id="6719d-121">Daher ist es wichtig, dass Client und Server den gleichen Algorithmus verwenden, um das Element "Winner" zu identifizieren.</span><span class="sxs-lookup"><span data-stu-id="6719d-121">Therefore, it is important that client and server use the same algorithm to detect the "winner" item.</span></span> <span data-ttu-id="6719d-122">Die folgenden Regeln müssen angewendet werden, um den "Gewinner" zu erfassen:</span><span class="sxs-lookup"><span data-stu-id="6719d-122">The following rules must be applied to detect the "winner":</span></span>
  
1. <span data-ttu-id="6719d-123">Zeitpunkt der letzten Änderung.</span><span class="sxs-lookup"><span data-stu-id="6719d-123">Last modification time.</span></span>
    
2. <span data-ttu-id="6719d-124">Höhere CN-GUID (mit Arbeitsspeicher Vergleich), um Tie zu unterbrechen.</span><span class="sxs-lookup"><span data-stu-id="6719d-124">Higher CN GUID (using memory compare) to break tie.</span></span>
    
## <a name="related-resources"></a><span data-ttu-id="6719d-125">Zugehörige Ressourcen</span><span class="sxs-lookup"><span data-stu-id="6719d-125">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="6719d-126">Protokollspezifikationen</span><span class="sxs-lookup"><span data-stu-id="6719d-126">Protocol specifications</span></span>

<span data-ttu-id="6719d-127">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="6719d-127">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="6719d-128">Enthält Verweise auf zugehörige Exchange Server-Protokollspezifikationen.</span><span class="sxs-lookup"><span data-stu-id="6719d-128">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="6719d-129">[[MS-OXCFXICS]](https://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="6719d-129">[[MS-OXCFXICS]](https://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="6719d-130">Behandelt das Synchronisieren von Messagingobjekt Daten zwischen einem Server und einem Client.</span><span class="sxs-lookup"><span data-stu-id="6719d-130">Handles synchronizing messaging object data between a server and a client.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="6719d-131">Header Dateien</span><span class="sxs-lookup"><span data-stu-id="6719d-131">Header files</span></span>

<span data-ttu-id="6719d-132">Mapidefs. h</span><span class="sxs-lookup"><span data-stu-id="6719d-132">Mapidefs.h</span></span>
  
> <span data-ttu-id="6719d-133">Stellt Datentypdefinitionen bereit.</span><span class="sxs-lookup"><span data-stu-id="6719d-133">Provides data type definitions.</span></span>
    
<span data-ttu-id="6719d-134">Mapitags. h</span><span class="sxs-lookup"><span data-stu-id="6719d-134">Mapitags.h</span></span>
  
> <span data-ttu-id="6719d-135">Enthält Definitionen von Eigenschaften, die als zugeordnete Eigenschaften aufgelistet sind.</span><span class="sxs-lookup"><span data-stu-id="6719d-135">Contains definitions of properties listed as associated properties.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="6719d-136">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="6719d-136">See also</span></span>



[<span data-ttu-id="6719d-137">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="6719d-137">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="6719d-138">Kanonische MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="6719d-138">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="6719d-139">Zuordnen von kanonischen Eigenschaftennamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="6719d-139">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="6719d-140">Zuordnen von MAPI-Namen zu kanonischen Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="6719d-140">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

