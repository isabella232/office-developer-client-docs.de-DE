---
title: PidTagLatestDeliveryTime (kanonische Eigenschaft)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagLatestDeliveryTime
api_type:
- HeaderDef
ms.assetid: 6c2e64bc-786e-4867-a504-46f4d1214337
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 3640ec4471b72dea81d56cc2c462ef145095480f
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2018
ms.locfileid: "22590925"
---
# <a name="pidtaglatestdeliverytime-canonical-property"></a><span data-ttu-id="7aabc-103">PidTagLatestDeliveryTime (kanonische Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="7aabc-103">PidTagLatestDeliveryTime Canonical Property</span></span>

  
  
<span data-ttu-id="7aabc-104">**Betrifft**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="7aabc-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="7aabc-105">Enthält das späteste Datum und Uhrzeit, wann ein Message Transfer Agent (MTA) eine Nachricht übermitteln soll.</span><span class="sxs-lookup"><span data-stu-id="7aabc-105">Contains the latest date and time when a message transfer agent (MTA) should deliver a message.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="7aabc-106">Zugeordnete Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="7aabc-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="7aabc-107">PR_LATEST_DELIVERY_TIME</span><span class="sxs-lookup"><span data-stu-id="7aabc-107">PR_LATEST_DELIVERY_TIME</span></span>  <br/> |
|<span data-ttu-id="7aabc-108">Kennung:</span><span class="sxs-lookup"><span data-stu-id="7aabc-108">Identifier:</span></span>  <br/> |<span data-ttu-id="7aabc-109">0x0019</span><span class="sxs-lookup"><span data-stu-id="7aabc-109">0x0019</span></span>  <br/> |
|<span data-ttu-id="7aabc-110">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="7aabc-110">Data type:</span></span>  <br/> |<span data-ttu-id="7aabc-111">PT_SYSTIME</span><span class="sxs-lookup"><span data-stu-id="7aabc-111">PT_SYSTIME</span></span>  <br/> |
|<span data-ttu-id="7aabc-112">Bereich:</span><span class="sxs-lookup"><span data-stu-id="7aabc-112">Area:</span></span>  <br/> |<span data-ttu-id="7aabc-113">Allgemeine messaging</span><span class="sxs-lookup"><span data-stu-id="7aabc-113">General messaging</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="7aabc-114">HinwBemerkungeneise</span><span class="sxs-lookup"><span data-stu-id="7aabc-114">Remarks</span></span>

<span data-ttu-id="7aabc-115">Wenn ein MTA jeweils Zustellungsversuche ist nicht möglich, den diese Eigenschaft gibt an, abbricht die Nachricht ohne Übermittlung.</span><span class="sxs-lookup"><span data-stu-id="7aabc-115">If an MTA cannot deliver a message by the time this property specifies, it cancels the message without delivery.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="7aabc-116">Verwandte Ressourcen</span><span class="sxs-lookup"><span data-stu-id="7aabc-116">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="7aabc-117">Header-Dateien</span><span class="sxs-lookup"><span data-stu-id="7aabc-117">Header files</span></span>

<span data-ttu-id="7aabc-118">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="7aabc-118">Mapidefs.h</span></span>
  
> <span data-ttu-id="7aabc-119">Enthält die Datentypdefinitionen.</span><span class="sxs-lookup"><span data-stu-id="7aabc-119">Provides data type definitions.</span></span>
    
<span data-ttu-id="7aabc-120">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="7aabc-120">Mapitags.h</span></span>
  
> <span data-ttu-id="7aabc-121">Enthält Definitionen von Eigenschaften, die als Alternative Namen aufgelistet.</span><span class="sxs-lookup"><span data-stu-id="7aabc-121">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="7aabc-122">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="7aabc-122">See also</span></span>



[<span data-ttu-id="7aabc-123">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="7aabc-123">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="7aabc-124">Kanonische MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="7aabc-124">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="7aabc-125">Zuordnen von kanonischen Eigenschaftennamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="7aabc-125">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="7aabc-126">Zuordnen von MAPI-Namen zu kanonische Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="7aabc-126">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

