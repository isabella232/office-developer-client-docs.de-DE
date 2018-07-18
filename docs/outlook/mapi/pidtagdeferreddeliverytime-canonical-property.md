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
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: b6b5f5aa5c595fb0c19ca9b8a9f8aeb94a2c2725
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19794309"
---
# <a name="pidtagdeferreddeliverytime-canonical-property"></a><span data-ttu-id="75614-103">PidTagDeferredDeliveryTime (kanonische Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="75614-103">PidTagDeferredDeliveryTime Canonical Property</span></span>

  
  
<span data-ttu-id="75614-104">**Betrifft**: Outlook</span><span class="sxs-lookup"><span data-stu-id="75614-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="75614-105">Enthält Datum und Uhrzeit, wenn ein Absender eine Nachricht zugestellt möchte.</span><span class="sxs-lookup"><span data-stu-id="75614-105">Contains the date and time when a message sender wants a message delivered.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="75614-106">Zugeordneten Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="75614-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="75614-107">PR_DEFERRED_DELIVERY_TIME</span><span class="sxs-lookup"><span data-stu-id="75614-107">PR_DEFERRED_DELIVERY_TIME</span></span>  <br/> |
|<span data-ttu-id="75614-108">Bezeichner:</span><span class="sxs-lookup"><span data-stu-id="75614-108">Identifier:</span></span>  <br/> |<span data-ttu-id="75614-109">0x000F</span><span class="sxs-lookup"><span data-stu-id="75614-109">0x000F</span></span>  <br/> |
|<span data-ttu-id="75614-110">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="75614-110">Data type:</span></span>  <br/> |<span data-ttu-id="75614-111">PT_SYSTIME</span><span class="sxs-lookup"><span data-stu-id="75614-111">PT_SYSTIME</span></span>  <br/> |
|<span data-ttu-id="75614-112">Bereich:</span><span class="sxs-lookup"><span data-stu-id="75614-112">Area:</span></span>  <br/> |<span data-ttu-id="75614-113">MAPI-Umschlag</span><span class="sxs-lookup"><span data-stu-id="75614-113">MAPI envelope</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="75614-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="75614-114">Remarks</span></span>

<span data-ttu-id="75614-115">MAPI keine verzögerte Übermittlung ausgeführt wird; Es ist eine Option des zugrunde liegenden Nachrichtensystem verzögerte Übermittlung zu behandeln.</span><span class="sxs-lookup"><span data-stu-id="75614-115">MAPI does not perform the deferred delivery; it is an option of the underlying messaging system to handle deferred delivery.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="75614-116">Verwandte Ressourcen</span><span class="sxs-lookup"><span data-stu-id="75614-116">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="75614-117">Protokollspezifikationen</span><span class="sxs-lookup"><span data-stu-id="75614-117">Protocol specifications</span></span>

<span data-ttu-id="75614-118">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="75614-118">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="75614-119">Bietet Verweise auf Verwandte Exchange Server-Spezifikationen.</span><span class="sxs-lookup"><span data-stu-id="75614-119">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="75614-120">[[MS-OXOMSG]](http://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="75614-120">[[MS-OXOMSG]](http://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="75614-121">Gibt die Eigenschaften und Operationen, die für e-Mail-Nachrichten zulässig sind.</span><span class="sxs-lookup"><span data-stu-id="75614-121">Specifies the properties and operations that are permissible on email messages.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="75614-122">Header-Dateien</span><span class="sxs-lookup"><span data-stu-id="75614-122">Header files</span></span>

<span data-ttu-id="75614-123">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="75614-123">Mapidefs.h</span></span>
  
> <span data-ttu-id="75614-124">Enthält die Datentypdefinitionen.</span><span class="sxs-lookup"><span data-stu-id="75614-124">Provides data type definitions.</span></span>
    
<span data-ttu-id="75614-125">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="75614-125">Mapitags.h</span></span>
  
> <span data-ttu-id="75614-126">Enthält Definitionen von Eigenschaften, die als Alternative Namen aufgelistet.</span><span class="sxs-lookup"><span data-stu-id="75614-126">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="75614-127">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="75614-127">See also</span></span>



[<span data-ttu-id="75614-128">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="75614-128">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="75614-129">Kanonische MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="75614-129">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="75614-130">Zuordnen von kanonischen Eigenschaftennamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="75614-130">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="75614-131">Zuordnen von MAPI-Namen zu kanonische Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="75614-131">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

