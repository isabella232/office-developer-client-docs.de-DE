---
title: PidTagCorrelate (kanonische Eigenschaft)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagCorrelate
api_type:
- HeaderDef
ms.assetid: be34993e-ffcc-47f5-b2d4-95ffa707bc5c
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: ce8573310e17e26b4e2deb4c0a0f835a6569151e
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19794284"
---
# <a name="pidtagcorrelate-canonical-property"></a><span data-ttu-id="55b7c-103">PidTagCorrelate (kanonische Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="55b7c-103">PidTagCorrelate Canonical Property</span></span>

  
  
<span data-ttu-id="55b7c-104">**Betrifft**: Outlook</span><span class="sxs-lookup"><span data-stu-id="55b7c-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="55b7c-105">Enthält True, wenn der Absender einer Nachricht die Korrelations-Funktion von messaging-System anfordert.</span><span class="sxs-lookup"><span data-stu-id="55b7c-105">Contains TRUE if the sender of a message requests the correlation feature of the messaging system.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="55b7c-106">Zugeordneten Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="55b7c-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="55b7c-107">PR_CORRELATE</span><span class="sxs-lookup"><span data-stu-id="55b7c-107">PR_CORRELATE</span></span>  <br/> |
|<span data-ttu-id="55b7c-108">Bezeichner:</span><span class="sxs-lookup"><span data-stu-id="55b7c-108">Identifier:</span></span>  <br/> |<span data-ttu-id="55b7c-109">0x0E0C</span><span class="sxs-lookup"><span data-stu-id="55b7c-109">0x0E0C</span></span>  <br/> |
|<span data-ttu-id="55b7c-110">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="55b7c-110">Data type:</span></span>  <br/> |<span data-ttu-id="55b7c-111">PT_BOOLEAN</span><span class="sxs-lookup"><span data-stu-id="55b7c-111">PT_BOOLEAN</span></span>  <br/> |
|<span data-ttu-id="55b7c-112">Bereich:</span><span class="sxs-lookup"><span data-stu-id="55b7c-112">Area:</span></span>  <br/> |<span data-ttu-id="55b7c-113">Exchange</span><span class="sxs-lookup"><span data-stu-id="55b7c-113">Exchange</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="55b7c-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="55b7c-114">Remarks</span></span>

<span data-ttu-id="55b7c-115">Diese Eigenschaft wird verwendet, um die Korrelation eingehende Berichte mit der ursprünglichen gesendeten Nachrichten anfordern.</span><span class="sxs-lookup"><span data-stu-id="55b7c-115">This property is used to request the correlation of incoming reports with the original sent message.</span></span> <span data-ttu-id="55b7c-116">Stößt ein Transportdienstes eine gesendete Nachricht mit **PR_CORRELATE** Set auf true festgelegt, wird die **PR_CORRELATE_MTSID** ([PidTagCorrelateMtsid](pidtagcorrelatemtsid-canonical-property.md))-Eigenschaft auf die Übertragung System (MTS)-ID für diese Nachricht.</span><span class="sxs-lookup"><span data-stu-id="55b7c-116">When a transport provider encounters a submitted message with **PR_CORRELATE** set to TRUE, it sets the **PR_CORRELATE_MTSID** ([PidTagCorrelateMtsid](pidtagcorrelatemtsid-canonical-property.md)) property to the message transfer system (MTS) identifier for that message.</span></span>
  
 <span data-ttu-id="55b7c-117">**PR_CORRELATE** sollte mit der messaging-Systeme, die Korrelation unterstützen von MTS Bezeichner, z. B. x. 400-verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="55b7c-117">**PR_CORRELATE** should be used with messaging systems that support correlation by MTS identifier, such as X.400.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="55b7c-118">Verwandte Ressourcen</span><span class="sxs-lookup"><span data-stu-id="55b7c-118">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="55b7c-119">Header-Dateien</span><span class="sxs-lookup"><span data-stu-id="55b7c-119">Header files</span></span>

<span data-ttu-id="55b7c-120">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="55b7c-120">Mapidefs.h</span></span>
  
> <span data-ttu-id="55b7c-121">Enthält die Datentypdefinitionen.</span><span class="sxs-lookup"><span data-stu-id="55b7c-121">Provides data type definitions.</span></span>
    
<span data-ttu-id="55b7c-122">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="55b7c-122">Mapitags.h</span></span>
  
> <span data-ttu-id="55b7c-123">Enthält Definitionen von Eigenschaften, die als zugeordneten Eigenschaften aufgelistet.</span><span class="sxs-lookup"><span data-stu-id="55b7c-123">Contains definitions of properties listed as associated properties.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="55b7c-124">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="55b7c-124">See also</span></span>



[<span data-ttu-id="55b7c-125">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="55b7c-125">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="55b7c-126">Kanonische MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="55b7c-126">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="55b7c-127">Zuordnen von kanonischen Eigenschaftennamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="55b7c-127">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="55b7c-128">Zuordnen von MAPI-Namen zu kanonische Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="55b7c-128">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

