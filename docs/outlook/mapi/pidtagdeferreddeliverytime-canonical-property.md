---
title: Kanonische PidTagDeferredDeliveryTime-Eigenschaft
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagDeferredDeliveryTime
api_type:
- HeaderDef
ms.assetid: 263ac923-692f-40d4-bdd5-116dc5c49766
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: 7197159fd55016454de3fa806fc30d0700ef5f3d
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32359927"
---
# <a name="pidtagdeferreddeliverytime-canonical-property"></a><span data-ttu-id="c6e8b-103">Kanonische PidTagDeferredDeliveryTime-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="c6e8b-103">PidTagDeferredDeliveryTime Canonical Property</span></span>

  
  
<span data-ttu-id="c6e8b-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="c6e8b-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="c6e8b-105">Enthält das Datum und die Uhrzeit, zu denen ein Nachrichtenabsender eine Nachricht zugestellt wünscht.</span><span class="sxs-lookup"><span data-stu-id="c6e8b-105">Contains the date and time when a message sender wants a message delivered.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="c6e8b-106">Zugeordnete Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="c6e8b-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="c6e8b-107">PR_DEFERRED_DELIVERY_TIME</span><span class="sxs-lookup"><span data-stu-id="c6e8b-107">PR_DEFERRED_DELIVERY_TIME</span></span>  <br/> |
|<span data-ttu-id="c6e8b-108">Kennung:</span><span class="sxs-lookup"><span data-stu-id="c6e8b-108">Identifier:</span></span>  <br/> |<span data-ttu-id="c6e8b-109">0x000F</span><span class="sxs-lookup"><span data-stu-id="c6e8b-109">0x000F</span></span>  <br/> |
|<span data-ttu-id="c6e8b-110">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="c6e8b-110">Data type:</span></span>  <br/> |<span data-ttu-id="c6e8b-111">PT_SYSTIME</span><span class="sxs-lookup"><span data-stu-id="c6e8b-111">PT_SYSTIME</span></span>  <br/> |
|<span data-ttu-id="c6e8b-112">Bereich:</span><span class="sxs-lookup"><span data-stu-id="c6e8b-112">Area:</span></span>  <br/> |<span data-ttu-id="c6e8b-113">MAPI-Umschlag</span><span class="sxs-lookup"><span data-stu-id="c6e8b-113">MAPI envelope</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="c6e8b-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="c6e8b-114">Remarks</span></span>

<span data-ttu-id="c6e8b-115">Die verzögerte Übertragung wird von MAPI nicht ausgeführt; Es ist eine Option des zugrunde liegenden Messagingsystems, um die verzögerte Übermittlung zu behandeln.</span><span class="sxs-lookup"><span data-stu-id="c6e8b-115">MAPI does not perform the deferred delivery; it is an option of the underlying messaging system to handle deferred delivery.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="c6e8b-116">Zugehörige Ressourcen</span><span class="sxs-lookup"><span data-stu-id="c6e8b-116">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="c6e8b-117">Protokollspezifikationen</span><span class="sxs-lookup"><span data-stu-id="c6e8b-117">Protocol specifications</span></span>

<span data-ttu-id="c6e8b-118">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="c6e8b-118">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="c6e8b-119">Enthält Verweise auf zugehörige Exchange Server-Protokollspezifikationen.</span><span class="sxs-lookup"><span data-stu-id="c6e8b-119">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="c6e8b-120">[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="c6e8b-120">[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="c6e8b-121">Gibt die Eigenschaften und Vorgänge an, die für e-Mail-Nachrichten zulässig sind.</span><span class="sxs-lookup"><span data-stu-id="c6e8b-121">Specifies the properties and operations that are permissible on email messages.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="c6e8b-122">Header Dateien</span><span class="sxs-lookup"><span data-stu-id="c6e8b-122">Header files</span></span>

<span data-ttu-id="c6e8b-123">Mapidefs. h</span><span class="sxs-lookup"><span data-stu-id="c6e8b-123">Mapidefs.h</span></span>
  
> <span data-ttu-id="c6e8b-124">Stellt Datentypdefinitionen bereit.</span><span class="sxs-lookup"><span data-stu-id="c6e8b-124">Provides data type definitions.</span></span>
    
<span data-ttu-id="c6e8b-125">Mapitags. h</span><span class="sxs-lookup"><span data-stu-id="c6e8b-125">Mapitags.h</span></span>
  
> <span data-ttu-id="c6e8b-126">Enthält Definitionen von Eigenschaften, die als Alternative Namen aufgeführt sind.</span><span class="sxs-lookup"><span data-stu-id="c6e8b-126">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="c6e8b-127">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="c6e8b-127">See also</span></span>



[<span data-ttu-id="c6e8b-128">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="c6e8b-128">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="c6e8b-129">Kanonische MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="c6e8b-129">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="c6e8b-130">Zuordnen von kanonischen Eigenschaftennamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="c6e8b-130">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="c6e8b-131">Zuordnen von MAPI-Namen zu kanonischen Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="c6e8b-131">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

