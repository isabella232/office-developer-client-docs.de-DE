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
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/04/2018
ms.locfileid: "25401755"
---
# <a name="pidtagdeferreddeliverytime-canonical-property"></a><span data-ttu-id="fca07-103">PidTagDeferredDeliveryTime (kanonische Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="fca07-103">PidTagDeferredDeliveryTime Canonical Property</span></span>

  
  
<span data-ttu-id="fca07-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="fca07-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="fca07-105">Enthält Datum und Uhrzeit, wenn ein Absender eine Nachricht zugestellt möchte.</span><span class="sxs-lookup"><span data-stu-id="fca07-105">Contains the date and time when a message sender wants a message delivered.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="fca07-106">Zugeordnete Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="fca07-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="fca07-107">PR_DEFERRED_DELIVERY_TIME</span><span class="sxs-lookup"><span data-stu-id="fca07-107">PR_DEFERRED_DELIVERY_TIME</span></span>  <br/> |
|<span data-ttu-id="fca07-108">Kennung:</span><span class="sxs-lookup"><span data-stu-id="fca07-108">Identifier:</span></span>  <br/> |<span data-ttu-id="fca07-109">0x000F</span><span class="sxs-lookup"><span data-stu-id="fca07-109">0x000F</span></span>  <br/> |
|<span data-ttu-id="fca07-110">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="fca07-110">Data type:</span></span>  <br/> |<span data-ttu-id="fca07-111">PT_SYSTIME</span><span class="sxs-lookup"><span data-stu-id="fca07-111">PT_SYSTIME</span></span>  <br/> |
|<span data-ttu-id="fca07-112">Bereich:</span><span class="sxs-lookup"><span data-stu-id="fca07-112">Area:</span></span>  <br/> |<span data-ttu-id="fca07-113">MAPI-Umschlag</span><span class="sxs-lookup"><span data-stu-id="fca07-113">MAPI envelope</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="fca07-114">Hinweise</span><span class="sxs-lookup"><span data-stu-id="fca07-114">Remarks</span></span>

<span data-ttu-id="fca07-115">MAPI keine verzögerte Übermittlung ausgeführt wird; Es ist eine Option des zugrunde liegenden Nachrichtensystem verzögerte Übermittlung zu behandeln.</span><span class="sxs-lookup"><span data-stu-id="fca07-115">MAPI does not perform the deferred delivery; it is an option of the underlying messaging system to handle deferred delivery.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="fca07-116">Verwandte Ressourcen</span><span class="sxs-lookup"><span data-stu-id="fca07-116">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="fca07-117">Protokollspezifikationen</span><span class="sxs-lookup"><span data-stu-id="fca07-117">Protocol specifications</span></span>

<span data-ttu-id="fca07-118">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="fca07-118">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="fca07-119">Bietet Verweise auf Verwandte Exchange Server-Spezifikationen.</span><span class="sxs-lookup"><span data-stu-id="fca07-119">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="fca07-120">[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="fca07-120">[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="fca07-121">Gibt die Eigenschaften und Operationen, die für e-Mail-Nachrichten zulässig sind.</span><span class="sxs-lookup"><span data-stu-id="fca07-121">Specifies the properties and operations that are permissible on email messages.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="fca07-122">Header-Dateien</span><span class="sxs-lookup"><span data-stu-id="fca07-122">Header files</span></span>

<span data-ttu-id="fca07-123">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="fca07-123">Mapidefs.h</span></span>
  
> <span data-ttu-id="fca07-124">Enthält die Datentypdefinitionen.</span><span class="sxs-lookup"><span data-stu-id="fca07-124">Provides data type definitions.</span></span>
    
<span data-ttu-id="fca07-125">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="fca07-125">Mapitags.h</span></span>
  
> <span data-ttu-id="fca07-126">Enthält Definitionen von Eigenschaften, die als Alternative Namen aufgelistet.</span><span class="sxs-lookup"><span data-stu-id="fca07-126">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="fca07-127">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="fca07-127">See also</span></span>



[<span data-ttu-id="fca07-128">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="fca07-128">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="fca07-129">Kanonische MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="fca07-129">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="fca07-130">Zuordnen von kanonischen Eigenschaftennamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="fca07-130">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="fca07-131">Zuordnen von MAPI-Namen zu kanonische Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="fca07-131">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

