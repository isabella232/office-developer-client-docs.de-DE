---
title: Kanonische Pidtagcorrelate (-Eigenschaft
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
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: ea217808a163c7f16bbaa3c5a959fd32c8cbe10c
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33405219"
---
# <a name="pidtagcorrelate-canonical-property"></a><span data-ttu-id="bce81-103">Kanonische Pidtagcorrelate (-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="bce81-103">PidTagCorrelate Canonical Property</span></span>

  
  
<span data-ttu-id="bce81-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="bce81-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="bce81-105">Enthält TRUE, wenn der Absender einer Nachricht das Korrelations Feature des Messagingsystems anfordert.</span><span class="sxs-lookup"><span data-stu-id="bce81-105">Contains TRUE if the sender of a message requests the correlation feature of the messaging system.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="bce81-106">Zugeordnete Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="bce81-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="bce81-107">PR_CORRELATE</span><span class="sxs-lookup"><span data-stu-id="bce81-107">PR_CORRELATE</span></span>  <br/> |
|<span data-ttu-id="bce81-108">Kennung:</span><span class="sxs-lookup"><span data-stu-id="bce81-108">Identifier:</span></span>  <br/> |<span data-ttu-id="bce81-109">0x0E0C</span><span class="sxs-lookup"><span data-stu-id="bce81-109">0x0E0C</span></span>  <br/> |
|<span data-ttu-id="bce81-110">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="bce81-110">Data type:</span></span>  <br/> |<span data-ttu-id="bce81-111">PT_BOOLEAN</span><span class="sxs-lookup"><span data-stu-id="bce81-111">PT_BOOLEAN</span></span>  <br/> |
|<span data-ttu-id="bce81-112">Bereich:</span><span class="sxs-lookup"><span data-stu-id="bce81-112">Area:</span></span>  <br/> |<span data-ttu-id="bce81-113">Exchange</span><span class="sxs-lookup"><span data-stu-id="bce81-113">Exchange</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="bce81-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="bce81-114">Remarks</span></span>

<span data-ttu-id="bce81-115">Diese Eigenschaft wird verwendet, um die Korrelation eingehender Berichte mit der ursprünglichen gesendeten Nachricht anzufordern.</span><span class="sxs-lookup"><span data-stu-id="bce81-115">This property is used to request the correlation of incoming reports with the original sent message.</span></span> <span data-ttu-id="bce81-116">Wenn ein Transportanbieter eine übermittelte Nachricht mit **PR_CORRELATE** auf true trifft, wird die **PR_CORRELATE_MTSID** ([pidtagcorrelatemtsid (](pidtagcorrelatemtsid-canonical-property.md))-Eigenschaft auf den MTS-Bezeichner (Message Transfer System) für diese Nachricht festgelegt.</span><span class="sxs-lookup"><span data-stu-id="bce81-116">When a transport provider encounters a submitted message with **PR_CORRELATE** set to TRUE, it sets the **PR_CORRELATE_MTSID** ([PidTagCorrelateMtsid](pidtagcorrelatemtsid-canonical-property.md)) property to the message transfer system (MTS) identifier for that message.</span></span>
  
 <span data-ttu-id="bce81-117">**PR_CORRELATE** sollte mit Messagingsystemen verwendet werden, die eine Korrelation durch MTS-ID, wie X. 400, unterstützen.</span><span class="sxs-lookup"><span data-stu-id="bce81-117">**PR_CORRELATE** should be used with messaging systems that support correlation by MTS identifier, such as X.400.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="bce81-118">Verwandte Ressourcen</span><span class="sxs-lookup"><span data-stu-id="bce81-118">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="bce81-119">Header Dateien</span><span class="sxs-lookup"><span data-stu-id="bce81-119">Header files</span></span>

<span data-ttu-id="bce81-120">Mapidefs. h</span><span class="sxs-lookup"><span data-stu-id="bce81-120">Mapidefs.h</span></span>
  
> <span data-ttu-id="bce81-121">Stellt Datentypdefinitionen bereit.</span><span class="sxs-lookup"><span data-stu-id="bce81-121">Provides data type definitions.</span></span>
    
<span data-ttu-id="bce81-122">Mapitags. h</span><span class="sxs-lookup"><span data-stu-id="bce81-122">Mapitags.h</span></span>
  
> <span data-ttu-id="bce81-123">Enthält Definitionen von Eigenschaften, die als zugeordnete Eigenschaften aufgelistet sind.</span><span class="sxs-lookup"><span data-stu-id="bce81-123">Contains definitions of properties listed as associated properties.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="bce81-124">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="bce81-124">See also</span></span>



[<span data-ttu-id="bce81-125">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="bce81-125">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="bce81-126">Kanonische MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="bce81-126">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="bce81-127">Zuordnen von kanonischen Eigenschaftennamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="bce81-127">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="bce81-128">Zuordnen von MAPI-Namen zu kanonischen Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="bce81-128">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

