---
title: Kanonische Pidtagremoteprogress (-Eigenschaft
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagRemoteProgress
api_type:
- COM
ms.assetid: 01cae79e-5b56-4cd4-83a6-f0956ff539fb
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: a5a9d0796bc92514ae6d990b7328364b85bc55cd
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33439842"
---
# <a name="pidtagremoteprogress-canonical-property"></a><span data-ttu-id="a49bb-103">Kanonische Pidtagremoteprogress (-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="a49bb-103">PidTagRemoteProgress Canonical Property</span></span>

  
  
<span data-ttu-id="a49bb-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="a49bb-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="a49bb-105">Diese Eigenschaft enthält eine Zahl, die den Status einer Remoteübertragung angibt.</span><span class="sxs-lookup"><span data-stu-id="a49bb-105">This property contains a number that indicates the status of a remote transfer.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="a49bb-106">Zugeordnete Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="a49bb-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="a49bb-107">PR_REMOTE_PROGRESS</span><span class="sxs-lookup"><span data-stu-id="a49bb-107">PR_REMOTE_PROGRESS</span></span>  <br/> |
|<span data-ttu-id="a49bb-108">Kennung:</span><span class="sxs-lookup"><span data-stu-id="a49bb-108">Identifier:</span></span>  <br/> |<span data-ttu-id="a49bb-109">0x3E0B</span><span class="sxs-lookup"><span data-stu-id="a49bb-109">0x3E0B</span></span>  <br/> |
|<span data-ttu-id="a49bb-110">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="a49bb-110">Data type:</span></span>  <br/> |<span data-ttu-id="a49bb-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="a49bb-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="a49bb-112">Bereich:</span><span class="sxs-lookup"><span data-stu-id="a49bb-112">Area:</span></span>  <br/> |<span data-ttu-id="a49bb-113">MAPI-Status</span><span class="sxs-lookup"><span data-stu-id="a49bb-113">MAPI Status</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="a49bb-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="a49bb-114">Remarks</span></span>

<span data-ttu-id="a49bb-115">Wenn keine Übertragung ausgeführt wird, sollte diese Eigenschaft auf 1 festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="a49bb-115">If no transfer is in progress, this property should be set to 1.</span></span> <span data-ttu-id="a49bb-116">Wenn eine Übertragung ausgeführt wird, sollte Sie auf einen Wert zwischen 0 und 100 festgelegt werden, der den Prozentsatz der Fertigstellung des Transfers angibt.</span><span class="sxs-lookup"><span data-stu-id="a49bb-116">If a transfer is in progress, it should be set to a value from 0 to 100 indicating the transfer's percent of completion.</span></span>
  
<span data-ttu-id="a49bb-117">Der mit dem numerischen Statuscode verknüpfte Text wird in der **PR_REMOTE_PROGRESS_TEXT** ([pidtagremoteprogresstext (](pidtagremoteprogresstext-canonical-property.md))-Eigenschaft angezeigt.</span><span class="sxs-lookup"><span data-stu-id="a49bb-117">The text associated with the numeric status code appears in the **PR_REMOTE_PROGRESS_TEXT** ([PidTagRemoteProgressText](pidtagremoteprogresstext-canonical-property.md)) property.</span></span>
  
<span data-ttu-id="a49bb-118">Für diese Eigenschaft können die folgenden Flags festgelegt werden:</span><span class="sxs-lookup"><span data-stu-id="a49bb-118">The following flags can be set for this property:</span></span>
  
<span data-ttu-id="a49bb-119">MSGSTATUS_REMOTE_DELETE</span><span class="sxs-lookup"><span data-stu-id="a49bb-119">MSGSTATUS_REMOTE_DELETE</span></span>
  
> <span data-ttu-id="a49bb-120">Die Nachrichtenübertragung wird gelöscht.</span><span class="sxs-lookup"><span data-stu-id="a49bb-120">The message transfer is deleted.</span></span>
    
<span data-ttu-id="a49bb-121">MSGSTATUS_REMOTE_DOWNLOAD</span><span class="sxs-lookup"><span data-stu-id="a49bb-121">MSGSTATUS_REMOTE_DOWNLOAD</span></span>
  
> <span data-ttu-id="a49bb-122">Die Nachrichtenübertragung wird ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="a49bb-122">The message transfer is in progress.</span></span>
    
## <a name="related-resources"></a><span data-ttu-id="a49bb-123">Verwandte Ressourcen</span><span class="sxs-lookup"><span data-stu-id="a49bb-123">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="a49bb-124">Header Dateien</span><span class="sxs-lookup"><span data-stu-id="a49bb-124">Header files</span></span>

<span data-ttu-id="a49bb-125">Mapidefs. h</span><span class="sxs-lookup"><span data-stu-id="a49bb-125">Mapidefs.h</span></span>
  
> <span data-ttu-id="a49bb-126">Stellt Datentypdefinitionen bereit.</span><span class="sxs-lookup"><span data-stu-id="a49bb-126">Provides data type definitions.</span></span>
    
<span data-ttu-id="a49bb-127">Mapitags. h</span><span class="sxs-lookup"><span data-stu-id="a49bb-127">Mapitags.h</span></span>
  
> <span data-ttu-id="a49bb-128">Enthält Definitionen von Eigenschaften, die als zugeordnete Eigenschaften aufgelistet sind.</span><span class="sxs-lookup"><span data-stu-id="a49bb-128">Contains definitions of properties listed as associated properties.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="a49bb-129">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="a49bb-129">See also</span></span>



[<span data-ttu-id="a49bb-130">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="a49bb-130">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="a49bb-131">Kanonische MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="a49bb-131">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="a49bb-132">Zuordnen von kanonischen Eigenschaftennamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="a49bb-132">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="a49bb-133">Zuordnen von MAPI-Namen zu kanonischen Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="a49bb-133">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

