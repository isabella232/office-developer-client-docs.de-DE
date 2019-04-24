---
title: Kanonische Pidtagoriginaldeliverytime (-Eigenschaft
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagOriginalDeliveryTime
api_type:
- COM
ms.assetid: 700ccfc9-493a-483b-aca0-aa2d7f6bb229
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: bbe277092b450a4254e02d00d2cf54e35ec6be44
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32355657"
---
# <a name="pidtagoriginaldeliverytime-canonical-property"></a><span data-ttu-id="250e1-103">Kanonische Pidtagoriginaldeliverytime (-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="250e1-103">PidTagOriginalDeliveryTime Canonical Property</span></span>

  
  
<span data-ttu-id="250e1-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="250e1-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="250e1-105">Enthält eine Kopie der Übermittlungsdatum und-Uhrzeit der ursprünglichen Nachricht in einem Thread.</span><span class="sxs-lookup"><span data-stu-id="250e1-105">Contains a copy of the original message's delivery date and time in a thread.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="250e1-106">Zugeordnete Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="250e1-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="250e1-107">PR_ORIGINAL_DELIVERY_TIME</span><span class="sxs-lookup"><span data-stu-id="250e1-107">PR_ORIGINAL_DELIVERY_TIME</span></span>  <br/> |
|<span data-ttu-id="250e1-108">Kennung:</span><span class="sxs-lookup"><span data-stu-id="250e1-108">Identifier:</span></span>  <br/> |<span data-ttu-id="250e1-109">0x0055</span><span class="sxs-lookup"><span data-stu-id="250e1-109">0x0055</span></span>  <br/> |
|<span data-ttu-id="250e1-110">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="250e1-110">Data type:</span></span>  <br/> |<span data-ttu-id="250e1-111">PT_SYSTIME</span><span class="sxs-lookup"><span data-stu-id="250e1-111">PT_SYSTIME</span></span>  <br/> |
|<span data-ttu-id="250e1-112">Bereich:</span><span class="sxs-lookup"><span data-stu-id="250e1-112">Area:</span></span>  <br/> |<span data-ttu-id="250e1-113">Allgemeine Nachrichtenübermittlung</span><span class="sxs-lookup"><span data-stu-id="250e1-113">General messaging</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="250e1-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="250e1-114">Remarks</span></span>

<span data-ttu-id="250e1-115">Diese Eigenschaft wird von der ursprünglichen **PR_MESSAGE_DELIVERY_TIME** ([pidtagmessagedeliverytime (](pidtagmessagedeliverytime-canonical-property.md))-Eigenschaft in nachfolgenden Reply-oder Forward-Vorgängen kopiert und in Lese-und nonread-Berichten verwendet.</span><span class="sxs-lookup"><span data-stu-id="250e1-115">This property is copied from the original **PR_MESSAGE_DELIVERY_TIME** ([PidTagMessageDeliveryTime](pidtagmessagedeliverytime-canonical-property.md)) property in subsequent reply or forward operations and used in read and nonread reports.</span></span> <span data-ttu-id="250e1-116">Zuzustellenden Berichte verwenden Sie stattdessen die **PR_DELIVER_TIME** ([pidtagdelivertime (](pidtagdelivertime-canonical-property.md))-Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="250e1-116">Delivery reports use the **PR_DELIVER_TIME** ([PidTagDeliverTime](pidtagdelivertime-canonical-property.md)) property instead.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="250e1-117">Zugehörige Ressourcen</span><span class="sxs-lookup"><span data-stu-id="250e1-117">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="250e1-118">Protokollspezifikationen</span><span class="sxs-lookup"><span data-stu-id="250e1-118">Protocol specifications</span></span>

<span data-ttu-id="250e1-119">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="250e1-119">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="250e1-120">Enthält Verweise auf zugehörige Exchange Server-Protokollspezifikationen.</span><span class="sxs-lookup"><span data-stu-id="250e1-120">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="250e1-121">[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="250e1-121">[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="250e1-122">Gibt die Eigenschaften und Vorgänge an, die für e-Mail-Nachrichtenobjekte zulässig sind.</span><span class="sxs-lookup"><span data-stu-id="250e1-122">Specifies the properties and operations that are permissible on email message objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="250e1-123">Header Dateien</span><span class="sxs-lookup"><span data-stu-id="250e1-123">Header files</span></span>

<span data-ttu-id="250e1-124">Mapidefs. h</span><span class="sxs-lookup"><span data-stu-id="250e1-124">Mapidefs.h</span></span>
  
> <span data-ttu-id="250e1-125">Stellt Datentypdefinitionen bereit.</span><span class="sxs-lookup"><span data-stu-id="250e1-125">Provides data type definitions.</span></span>
    
<span data-ttu-id="250e1-126">Mapitags. h</span><span class="sxs-lookup"><span data-stu-id="250e1-126">Mapitags.h</span></span>
  
> <span data-ttu-id="250e1-127">Enthält Definitionen von Eigenschaften, die als Alternative Namen aufgeführt sind.</span><span class="sxs-lookup"><span data-stu-id="250e1-127">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="250e1-128">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="250e1-128">See also</span></span>



[<span data-ttu-id="250e1-129">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="250e1-129">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="250e1-130">Kanonische MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="250e1-130">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="250e1-131">Zuordnen von kanonischen Eigenschaftennamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="250e1-131">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="250e1-132">Zuordnen von MAPI-Namen zu kanonischen Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="250e1-132">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

