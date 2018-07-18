---
title: PidTagRemoteProgress (kanonische Eigenschaft)
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
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: 4e6495d5521e0f277ac4d501a987de0142d0960d
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19794939"
---
# <a name="pidtagremoteprogress-canonical-property"></a><span data-ttu-id="ae282-103">PidTagRemoteProgress (kanonische Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="ae282-103">PidTagRemoteProgress Canonical Property</span></span>

  
  
<span data-ttu-id="ae282-104">**Betrifft**: Outlook</span><span class="sxs-lookup"><span data-stu-id="ae282-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="ae282-105">Diese Eigenschaft enthält eine Zahl, die den Status einer remote Übertragungstyp angibt.</span><span class="sxs-lookup"><span data-stu-id="ae282-105">This property contains a number that indicates the status of a remote transfer.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="ae282-106">Zugeordneten Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="ae282-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="ae282-107">PR_REMOTE_PROGRESS</span><span class="sxs-lookup"><span data-stu-id="ae282-107">PR_REMOTE_PROGRESS</span></span>  <br/> |
|<span data-ttu-id="ae282-108">Bezeichner:</span><span class="sxs-lookup"><span data-stu-id="ae282-108">Identifier:</span></span>  <br/> |<span data-ttu-id="ae282-109">0x3E0B</span><span class="sxs-lookup"><span data-stu-id="ae282-109">0x3E0B</span></span>  <br/> |
|<span data-ttu-id="ae282-110">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="ae282-110">Data type:</span></span>  <br/> |<span data-ttu-id="ae282-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="ae282-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="ae282-112">Bereich:</span><span class="sxs-lookup"><span data-stu-id="ae282-112">Area:</span></span>  <br/> |<span data-ttu-id="ae282-113">MAPI-Status</span><span class="sxs-lookup"><span data-stu-id="ae282-113">MAPI Status</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="ae282-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="ae282-114">Remarks</span></span>

<span data-ttu-id="ae282-115">Wenn Sie keine Übertragung ausgeführt wird, sollten diese Eigenschaft auf 1 festgelegt.</span><span class="sxs-lookup"><span data-stu-id="ae282-115">If no transfer is in progress, this property should be set to 1.</span></span> <span data-ttu-id="ae282-116">Wenn eine Übertragung ausgeführt wird, sollte es auf einen anderen Wert zwischen 0 und 100, der angibt, die Übertragung Prozent der Fertigstellung festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="ae282-116">If a transfer is in progress, it should be set to a value from 0 to 100 indicating the transfer's percent of completion.</span></span>
  
<span data-ttu-id="ae282-117">Der numerische Statuscode zugeordnete Text wird in der Eigenschaft **PR_REMOTE_PROGRESS_TEXT** ([PidTagRemoteProgressText](pidtagremoteprogresstext-canonical-property.md)) angezeigt.</span><span class="sxs-lookup"><span data-stu-id="ae282-117">The text associated with the numeric status code appears in the **PR_REMOTE_PROGRESS_TEXT** ([PidTagRemoteProgressText](pidtagremoteprogresstext-canonical-property.md)) property.</span></span>
  
<span data-ttu-id="ae282-118">Die folgenden Kennzeichen können für diese Eigenschaft festgelegt werden:</span><span class="sxs-lookup"><span data-stu-id="ae282-118">The following flags can be set for this property:</span></span>
  
<span data-ttu-id="ae282-119">MSGSTATUS_REMOTE_DELETE</span><span class="sxs-lookup"><span data-stu-id="ae282-119">MSGSTATUS_REMOTE_DELETE</span></span>
  
> <span data-ttu-id="ae282-120">Übertragung der Nachricht wird gelöscht.</span><span class="sxs-lookup"><span data-stu-id="ae282-120">The message transfer is deleted.</span></span>
    
<span data-ttu-id="ae282-121">MSGSTATUS_REMOTE_DOWNLOAD</span><span class="sxs-lookup"><span data-stu-id="ae282-121">MSGSTATUS_REMOTE_DOWNLOAD</span></span>
  
> <span data-ttu-id="ae282-122">Die Nachrichtenübermittlung wird gerade durchgeführt.</span><span class="sxs-lookup"><span data-stu-id="ae282-122">The message transfer is in progress.</span></span>
    
## <a name="related-resources"></a><span data-ttu-id="ae282-123">Verwandte Ressourcen</span><span class="sxs-lookup"><span data-stu-id="ae282-123">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="ae282-124">Header-Dateien</span><span class="sxs-lookup"><span data-stu-id="ae282-124">Header files</span></span>

<span data-ttu-id="ae282-125">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="ae282-125">Mapidefs.h</span></span>
  
> <span data-ttu-id="ae282-126">Enthält die Datentypdefinitionen.</span><span class="sxs-lookup"><span data-stu-id="ae282-126">Provides data type definitions.</span></span>
    
<span data-ttu-id="ae282-127">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="ae282-127">Mapitags.h</span></span>
  
> <span data-ttu-id="ae282-128">Enthält Definitionen von Eigenschaften, die als zugeordneten Eigenschaften aufgelistet.</span><span class="sxs-lookup"><span data-stu-id="ae282-128">Contains definitions of properties listed as associated properties.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="ae282-129">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="ae282-129">See also</span></span>



[<span data-ttu-id="ae282-130">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="ae282-130">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="ae282-131">Kanonische MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="ae282-131">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="ae282-132">Zuordnen von kanonischen Eigenschaftennamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="ae282-132">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="ae282-133">Zuordnen von MAPI-Namen zu kanonische Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="ae282-133">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

