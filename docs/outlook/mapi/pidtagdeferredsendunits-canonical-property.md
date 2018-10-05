---
title: PidTagDeferredSendUnits (kanonische Eigenschaft)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagDeferredSendUnits
api_type:
- HeaderDef
ms.assetid: 2386be9f-18c9-4949-a2aa-efc8e212801c
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: becc076efe0f4f805eb2a8db071b70ad731ee256
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/04/2018
ms.locfileid: "25385685"
---
# <a name="pidtagdeferredsendunits-canonical-property"></a><span data-ttu-id="80868-103">PidTagDeferredSendUnits (kanonische Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="80868-103">PidTagDeferredSendUnits Canonical Property</span></span>

  
  
<span data-ttu-id="80868-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="80868-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="80868-105">Gibt die Zeiteinheit, von denen der Eigenschaftswert **PR_DEFERRED_SEND_NUMBER** ([PidTagDeferredSendNumber](pidtagdeferredsendnumber-canonical-property.md)) multipliziert werden soll.</span><span class="sxs-lookup"><span data-stu-id="80868-105">Specifies the unit of time by which the **PR_DEFERRED_SEND_NUMBER** ([PidTagDeferredSendNumber](pidtagdeferredsendnumber-canonical-property.md)) property value should be multiplied.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="80868-106">Zugeordnete Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="80868-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="80868-107">PR_DEFERRED_SEND_UNITS</span><span class="sxs-lookup"><span data-stu-id="80868-107">PR_DEFERRED_SEND_UNITS</span></span>  <br/> |
|<span data-ttu-id="80868-108">Kennung:</span><span class="sxs-lookup"><span data-stu-id="80868-108">Identifier:</span></span>  <br/> |<span data-ttu-id="80868-109">0x3FEC</span><span class="sxs-lookup"><span data-stu-id="80868-109">0x3FEC</span></span>  <br/> |
|<span data-ttu-id="80868-110">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="80868-110">Data type:</span></span>  <br/> |<span data-ttu-id="80868-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="80868-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="80868-112">Bereich:</span><span class="sxs-lookup"><span data-stu-id="80868-112">Area:</span></span>  <br/> |<span data-ttu-id="80868-113">MAPI-status</span><span class="sxs-lookup"><span data-stu-id="80868-113">MAPI status</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="80868-114">Hinweise</span><span class="sxs-lookup"><span data-stu-id="80868-114">Remarks</span></span>

<span data-ttu-id="80868-115">Wenn festgelegt, diese Eigenschaft einen der folgenden Werte aufweisen muss:</span><span class="sxs-lookup"><span data-stu-id="80868-115">If set, this property must have one of the following values:</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="80868-116">**PidTagDeferredSendUnits**</span><span class="sxs-lookup"><span data-stu-id="80868-116">**PidTagDeferredSendUnits**</span></span> <br/> |<span data-ttu-id="80868-117">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="80868-117">Description</span></span>  <br/> |
|<span data-ttu-id="80868-118">0</span><span class="sxs-lookup"><span data-stu-id="80868-118">0</span></span>  <br/> |<span data-ttu-id="80868-119">Minuten, beispielsweise 60 Sekunden</span><span class="sxs-lookup"><span data-stu-id="80868-119">Minutes, for example 60 seconds</span></span>  <br/> |
|<span data-ttu-id="80868-120">1</span><span class="sxs-lookup"><span data-stu-id="80868-120">1</span></span>  <br/> |<span data-ttu-id="80868-121">Stunden, beispielsweise 60 x 60 Sekunden</span><span class="sxs-lookup"><span data-stu-id="80868-121">Hours, for example 60x60 seconds</span></span>  <br/> |
|<span data-ttu-id="80868-122">2</span><span class="sxs-lookup"><span data-stu-id="80868-122">2</span></span>  <br/> |<span data-ttu-id="80868-123">Am Tag, beispielsweise 24 x 60 x 60 Sekunden</span><span class="sxs-lookup"><span data-stu-id="80868-123">Day, for example 24x60x60 seconds</span></span>  <br/> |
|<span data-ttu-id="80868-124">3</span><span class="sxs-lookup"><span data-stu-id="80868-124">3</span></span>  <br/> |<span data-ttu-id="80868-125">Woche, beispielsweise 7x24x60x60 Sekunden</span><span class="sxs-lookup"><span data-stu-id="80868-125">Week, for example 7x24x60x60 seconds</span></span>  <br/> |
   
## <a name="related-resources"></a><span data-ttu-id="80868-126">Verwandte Ressourcen</span><span class="sxs-lookup"><span data-stu-id="80868-126">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="80868-127">Protokollspezifikationen</span><span class="sxs-lookup"><span data-stu-id="80868-127">Protocol specifications</span></span>

<span data-ttu-id="80868-128">[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="80868-128">[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="80868-129">Gibt die Eigenschaften und Operationen, die für e-Mail-Nachrichtenobjekte zulässig sind.</span><span class="sxs-lookup"><span data-stu-id="80868-129">Specifies the properties and operations that are permissible for email message objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="80868-130">Header-Dateien</span><span class="sxs-lookup"><span data-stu-id="80868-130">Header files</span></span>

<span data-ttu-id="80868-131">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="80868-131">Mapidefs.h</span></span>
  
> <span data-ttu-id="80868-132">Enthält die Datentypdefinitionen.</span><span class="sxs-lookup"><span data-stu-id="80868-132">Provides data type definitions.</span></span>
    
<span data-ttu-id="80868-133">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="80868-133">Mapitags.h</span></span>
  
> <span data-ttu-id="80868-134">Enthält Definitionen von Eigenschaften, die als Alternative Namen aufgelistet.</span><span class="sxs-lookup"><span data-stu-id="80868-134">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="80868-135">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="80868-135">See also</span></span>



[<span data-ttu-id="80868-136">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="80868-136">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="80868-137">Kanonische MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="80868-137">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="80868-138">Zuordnen von kanonischen Eigenschaftennamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="80868-138">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="80868-139">Zuordnen von MAPI-Namen zu kanonische Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="80868-139">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

