---
title: PidTagDeferredDeliveryTime (kanonische Eigenschaft)
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
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 7197159fd55016454de3fa806fc30d0700ef5f3d
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32359927"
---
# <a name="pidtagdeferreddeliverytime-canonical-property"></a><span data-ttu-id="e4490-103">PidTagDeferredDeliveryTime (kanonische Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="e4490-103">PidTagDeferredDeliveryTime Canonical Property</span></span>

  
  
<span data-ttu-id="e4490-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="e4490-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="e4490-105">Enthält das Datum und die Uhrzeit, zu der ein Nachrichtensender eine Nachricht zugestellt haben möchte.</span><span class="sxs-lookup"><span data-stu-id="e4490-105">Contains the date and time when a message sender wants a message delivered.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="e4490-106">Zugeordnete Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="e4490-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="e4490-107">PR_DEFERRED_DELIVERY_TIME</span><span class="sxs-lookup"><span data-stu-id="e4490-107">PR_DEFERRED_DELIVERY_TIME</span></span>  <br/> |
|<span data-ttu-id="e4490-108">Kennung:</span><span class="sxs-lookup"><span data-stu-id="e4490-108">Identifier:</span></span>  <br/> |<span data-ttu-id="e4490-109">0x000F</span><span class="sxs-lookup"><span data-stu-id="e4490-109">0x000F</span></span>  <br/> |
|<span data-ttu-id="e4490-110">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="e4490-110">Data type:</span></span>  <br/> |<span data-ttu-id="e4490-111">PT_SYSTIME</span><span class="sxs-lookup"><span data-stu-id="e4490-111">PT_SYSTIME</span></span>  <br/> |
|<span data-ttu-id="e4490-112">Bereich:</span><span class="sxs-lookup"><span data-stu-id="e4490-112">Area:</span></span>  <br/> |<span data-ttu-id="e4490-113">MAPI-Umschlag</span><span class="sxs-lookup"><span data-stu-id="e4490-113">MAPI envelope</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="e4490-114">Hinweise</span><span class="sxs-lookup"><span data-stu-id="e4490-114">Remarks</span></span>

<span data-ttu-id="e4490-115">MAPI führt die verzögerte Zustellung nicht aus. Es ist eine Option des zugrunde liegenden Messagingsystems, die verzögerte Zustellung zu verarbeiten.</span><span class="sxs-lookup"><span data-stu-id="e4490-115">MAPI does not perform the deferred delivery; it is an option of the underlying messaging system to handle deferred delivery.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="e4490-116">Verwandte Ressourcen</span><span class="sxs-lookup"><span data-stu-id="e4490-116">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="e4490-117">Protokollspezifikationen</span><span class="sxs-lookup"><span data-stu-id="e4490-117">Protocol specifications</span></span>

<span data-ttu-id="e4490-118">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="e4490-118">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="e4490-119">Enthält Verweise auf Exchange Server Protokollspezifikationen.</span><span class="sxs-lookup"><span data-stu-id="e4490-119">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="e4490-120">[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="e4490-120">[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="e4490-121">Gibt die Eigenschaften und Vorgänge an, die für E-Mail-Nachrichten zulässig sind.</span><span class="sxs-lookup"><span data-stu-id="e4490-121">Specifies the properties and operations that are permissible on email messages.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="e4490-122">Headerdateien</span><span class="sxs-lookup"><span data-stu-id="e4490-122">Header files</span></span>

<span data-ttu-id="e4490-123">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="e4490-123">Mapidefs.h</span></span>
  
> <span data-ttu-id="e4490-124">Bietet Datentypdefinitionen.</span><span class="sxs-lookup"><span data-stu-id="e4490-124">Provides data type definitions.</span></span>
    
<span data-ttu-id="e4490-125">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="e4490-125">Mapitags.h</span></span>
  
> <span data-ttu-id="e4490-126">Enthält Definitionen von Eigenschaften, die als alternative Namen aufgeführt sind.</span><span class="sxs-lookup"><span data-stu-id="e4490-126">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="e4490-127">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="e4490-127">See also</span></span>



[<span data-ttu-id="e4490-128">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="e4490-128">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="e4490-129">KANONISCHE EIGENSCHAFTEN VON MAPI</span><span class="sxs-lookup"><span data-stu-id="e4490-129">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="e4490-130">Zuordnen kanonischer Eigenschaftsnamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="e4490-130">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="e4490-131">Zuordnen von MAPI-Namen zu kanonischen Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="e4490-131">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

