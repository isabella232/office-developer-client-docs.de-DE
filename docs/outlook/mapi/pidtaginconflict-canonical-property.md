---
title: PidTagInConflict (kanonische Eigenschaft)
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
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: fc2774efed1a15fe79e167149f2cb162bae7642c
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32358534"
---
# <a name="pidtaginconflict-canonical-property"></a><span data-ttu-id="52c35-103">PidTagInConflict (kanonische Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="52c35-103">PidTagInConflict Canonical Property</span></span>

  
  
<span data-ttu-id="52c35-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="52c35-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="52c35-105">Enthält TRUE, wenn die Anlage ein alternatives Replikat darstellt.</span><span class="sxs-lookup"><span data-stu-id="52c35-105">Contains TRUE when the attachment represents an alternate replica.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="52c35-106">Zugeordnete Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="52c35-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="52c35-107">PR_IN_CONFLICT</span><span class="sxs-lookup"><span data-stu-id="52c35-107">PR_IN_CONFLICT</span></span>  <br/> |
|<span data-ttu-id="52c35-108">Kennung:</span><span class="sxs-lookup"><span data-stu-id="52c35-108">Identifier:</span></span>  <br/> |<span data-ttu-id="52c35-109">0x666C</span><span class="sxs-lookup"><span data-stu-id="52c35-109">0x666C</span></span>  <br/> |
|<span data-ttu-id="52c35-110">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="52c35-110">Data type:</span></span>  <br/> |<span data-ttu-id="52c35-111">PT_BOOLEAN</span><span class="sxs-lookup"><span data-stu-id="52c35-111">PT_BOOLEAN</span></span>  <br/> |
|<span data-ttu-id="52c35-112">Bereich:</span><span class="sxs-lookup"><span data-stu-id="52c35-112">Area:</span></span>  <br/> |<span data-ttu-id="52c35-113">Konflikthinweis</span><span class="sxs-lookup"><span data-stu-id="52c35-113">Conflict note</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="52c35-114">Hinweise</span><span class="sxs-lookup"><span data-stu-id="52c35-114">Remarks</span></span>

<span data-ttu-id="52c35-115">Der E-Mail-Client und der Server müssen eine Konfliktlösungsnachricht generieren, wenn während der Synchronisierung ein Konflikt mit der aktuellen Version einer Nachricht im Replikat erkannt wird.</span><span class="sxs-lookup"><span data-stu-id="52c35-115">The email client and server must generate a conflict resolve message when detecting a conflict against the current version of a message in the replica during synchronization.</span></span> <span data-ttu-id="52c35-116">Es ist wichtig zu wissen, dass es möglich ist, dass die aktuelle Version der Nachricht im lokalen Replikat während des aktuellen Synchronisierungsvorgangs übertragen wurde.</span><span class="sxs-lookup"><span data-stu-id="52c35-116">It is important to understand that it is possible that the current version of the message in the local replica was transmitted during the current synchronization operation.</span></span> <span data-ttu-id="52c35-117">Dies geschieht, wenn der Konflikt bereits auf dem Server vorhanden ist, bevor eine der widersprüchlichen Nachrichten in das lokale Replikat heruntergeladen wurde.</span><span class="sxs-lookup"><span data-stu-id="52c35-117">This will happen when the conflict already exists on the server before any of the conflicting messages were downloaded to the local replica.</span></span> <span data-ttu-id="52c35-118">Eine Nachricht zur Konfliktlösung muss als unabhängige Replikate mit in Konflikt enden PCLs synchronisiert werden.</span><span class="sxs-lookup"><span data-stu-id="52c35-118">A conflict resolve message must be synchronized as independent replicas with conflicting PCLs.</span></span> <span data-ttu-id="52c35-119">Die Konfliktlösungsnachricht selbst darf nicht zwischen Client und Server synchronisiert werden. Nur die unabhängigen Replikate sollten ausgetauscht werden.</span><span class="sxs-lookup"><span data-stu-id="52c35-119">The conflict resolve message itself must not be synchronized between client and server; only the independent replicas should be exchanged.</span></span> <span data-ttu-id="52c35-120">Der Synchronisierungspartner muss dann eine neue Nachricht generieren, die der Struktur der Konfliktnachricht entspricht.</span><span class="sxs-lookup"><span data-stu-id="52c35-120">The synchronization partner must then generate a new message that matches the structure of the conflict message.</span></span> <span data-ttu-id="52c35-121">Daher ist es wichtig, dass Client und Server denselben Algorithmus verwenden, um das "Winner"-Element zu erkennen.</span><span class="sxs-lookup"><span data-stu-id="52c35-121">Therefore, it is important that client and server use the same algorithm to detect the "winner" item.</span></span> <span data-ttu-id="52c35-122">Die folgenden Regeln müssen angewendet werden, um den "Gewinner" zu erkennen:</span><span class="sxs-lookup"><span data-stu-id="52c35-122">The following rules must be applied to detect the "winner":</span></span>
  
1. <span data-ttu-id="52c35-123">Zeitpunkt der letzten Änderung.</span><span class="sxs-lookup"><span data-stu-id="52c35-123">Last modification time.</span></span>
    
2. <span data-ttu-id="52c35-124">Höhere #A0 (mit Arbeitsspeichervergleich), um den Gleichstand zu brechen.</span><span class="sxs-lookup"><span data-stu-id="52c35-124">Higher CN GUID (using memory compare) to break tie.</span></span>
    
## <a name="related-resources"></a><span data-ttu-id="52c35-125">Verwandte Ressourcen</span><span class="sxs-lookup"><span data-stu-id="52c35-125">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="52c35-126">Protokollspezifikationen</span><span class="sxs-lookup"><span data-stu-id="52c35-126">Protocol specifications</span></span>

<span data-ttu-id="52c35-127">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="52c35-127">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="52c35-128">Enthält Verweise auf Exchange Server Protokollspezifikationen.</span><span class="sxs-lookup"><span data-stu-id="52c35-128">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="52c35-129">[[MS-OXCFXICS]](https://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="52c35-129">[[MS-OXCFXICS]](https://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="52c35-130">Behandelt die Synchronisierung von Messagingobjektdaten zwischen einem Server und einem Client.</span><span class="sxs-lookup"><span data-stu-id="52c35-130">Handles synchronizing messaging object data between a server and a client.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="52c35-131">Headerdateien</span><span class="sxs-lookup"><span data-stu-id="52c35-131">Header files</span></span>

<span data-ttu-id="52c35-132">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="52c35-132">Mapidefs.h</span></span>
  
> <span data-ttu-id="52c35-133">Bietet Datentypdefinitionen.</span><span class="sxs-lookup"><span data-stu-id="52c35-133">Provides data type definitions.</span></span>
    
<span data-ttu-id="52c35-134">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="52c35-134">Mapitags.h</span></span>
  
> <span data-ttu-id="52c35-135">Enthält Definitionen von Eigenschaften, die als zugeordnete Eigenschaften aufgeführt sind.</span><span class="sxs-lookup"><span data-stu-id="52c35-135">Contains definitions of properties listed as associated properties.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="52c35-136">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="52c35-136">See also</span></span>



[<span data-ttu-id="52c35-137">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="52c35-137">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="52c35-138">KANONISCHE EIGENSCHAFTEN VON MAPI</span><span class="sxs-lookup"><span data-stu-id="52c35-138">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="52c35-139">Zuordnen kanonischer Eigenschaftsnamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="52c35-139">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="52c35-140">Zuordnen von MAPI-Namen zu kanonischen Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="52c35-140">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

