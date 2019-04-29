---
title: Kanonische Pidtaglatestdeliverytime (-Eigenschaft
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
ms.openlocfilehash: 77ca51ae5a0e7e1d5a9be8f4ca05a1187fe71694
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33407788"
---
# <a name="pidtaglatestdeliverytime-canonical-property"></a><span data-ttu-id="2060e-103">Kanonische Pidtaglatestdeliverytime (-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="2060e-103">PidTagLatestDeliveryTime Canonical Property</span></span>

  
  
<span data-ttu-id="2060e-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="2060e-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="2060e-105">Enthält das aktuelle Datum und die Uhrzeit, zu der ein MTA (Message Transfer Agent) eine Nachricht übermitteln soll.</span><span class="sxs-lookup"><span data-stu-id="2060e-105">Contains the latest date and time when a message transfer agent (MTA) should deliver a message.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="2060e-106">Zugeordnete Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="2060e-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="2060e-107">PR_LATEST_DELIVERY_TIME</span><span class="sxs-lookup"><span data-stu-id="2060e-107">PR_LATEST_DELIVERY_TIME</span></span>  <br/> |
|<span data-ttu-id="2060e-108">Kennung:</span><span class="sxs-lookup"><span data-stu-id="2060e-108">Identifier:</span></span>  <br/> |<span data-ttu-id="2060e-109">0x0019</span><span class="sxs-lookup"><span data-stu-id="2060e-109">0x0019</span></span>  <br/> |
|<span data-ttu-id="2060e-110">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="2060e-110">Data type:</span></span>  <br/> |<span data-ttu-id="2060e-111">PT_SYSTIME</span><span class="sxs-lookup"><span data-stu-id="2060e-111">PT_SYSTIME</span></span>  <br/> |
|<span data-ttu-id="2060e-112">Bereich:</span><span class="sxs-lookup"><span data-stu-id="2060e-112">Area:</span></span>  <br/> |<span data-ttu-id="2060e-113">Allgemeine Nachrichtenübermittlung</span><span class="sxs-lookup"><span data-stu-id="2060e-113">General messaging</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="2060e-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="2060e-114">Remarks</span></span>

<span data-ttu-id="2060e-115">Wenn ein MTA keine Nachricht übermitteln kann, wenn diese Eigenschaft angibt, wird die Nachricht ohne Übermittlung abgebrochen.</span><span class="sxs-lookup"><span data-stu-id="2060e-115">If an MTA cannot deliver a message by the time this property specifies, it cancels the message without delivery.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="2060e-116">Verwandte Ressourcen</span><span class="sxs-lookup"><span data-stu-id="2060e-116">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="2060e-117">Header Dateien</span><span class="sxs-lookup"><span data-stu-id="2060e-117">Header files</span></span>

<span data-ttu-id="2060e-118">Mapidefs. h</span><span class="sxs-lookup"><span data-stu-id="2060e-118">Mapidefs.h</span></span>
  
> <span data-ttu-id="2060e-119">Stellt Datentypdefinitionen bereit.</span><span class="sxs-lookup"><span data-stu-id="2060e-119">Provides data type definitions.</span></span>
    
<span data-ttu-id="2060e-120">Mapitags. h</span><span class="sxs-lookup"><span data-stu-id="2060e-120">Mapitags.h</span></span>
  
> <span data-ttu-id="2060e-121">Enthält Definitionen von Eigenschaften, die als Alternative Namen aufgeführt sind.</span><span class="sxs-lookup"><span data-stu-id="2060e-121">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="2060e-122">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="2060e-122">See also</span></span>



[<span data-ttu-id="2060e-123">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="2060e-123">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="2060e-124">Kanonische MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="2060e-124">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="2060e-125">Zuordnen von kanonischen Eigenschaftennamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="2060e-125">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="2060e-126">Zuordnen von MAPI-Namen zu kanonischen Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="2060e-126">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

