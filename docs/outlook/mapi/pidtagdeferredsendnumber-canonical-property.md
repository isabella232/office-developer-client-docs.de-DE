---
title: PidTagDeferredSendNumber (kanonische Eigenschaft)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagDeferredSendNumber
api_type:
- HeaderDef
ms.assetid: 8ada5c9b-bec5-42d8-bc58-f0411ec4e88b
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: f2ccd004415bcbd42b56b1269fbdb4622ef1f8c5
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19794322"
---
# <a name="pidtagdeferredsendnumber-canonical-property"></a><span data-ttu-id="41182-103">PidTagDeferredSendNumber (kanonische Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="41182-103">PidTagDeferredSendNumber Canonical Property</span></span>

  
  
<span data-ttu-id="41182-104">**Betrifft**: Outlook</span><span class="sxs-lookup"><span data-stu-id="41182-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="41182-105">Enthält eine Zahl, die zum Berechnen der Aufgeschobene Senden einer Nachricht verwendet werden kann.</span><span class="sxs-lookup"><span data-stu-id="41182-105">Contains a number that can be used to compute the deferment of sending a message.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="41182-106">Zugeordneten Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="41182-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="41182-107">PR_DEFERRED_SEND_NUMBER</span><span class="sxs-lookup"><span data-stu-id="41182-107">PR_DEFERRED_SEND_NUMBER</span></span>  <br/> |
|<span data-ttu-id="41182-108">Bezeichner:</span><span class="sxs-lookup"><span data-stu-id="41182-108">Identifier:</span></span>  <br/> |<span data-ttu-id="41182-109">0x3FEB</span><span class="sxs-lookup"><span data-stu-id="41182-109">0x3FEB</span></span>  <br/> |
|<span data-ttu-id="41182-110">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="41182-110">Data type:</span></span>  <br/> |<span data-ttu-id="41182-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="41182-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="41182-112">Bereich:</span><span class="sxs-lookup"><span data-stu-id="41182-112">Area:</span></span>  <br/> |<span data-ttu-id="41182-113">MAPI-status</span><span class="sxs-lookup"><span data-stu-id="41182-113">MAPI status</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="41182-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="41182-114">Remarks</span></span>

<span data-ttu-id="41182-115">Diese Eigenschaft wird verwendet, für die Eigenschaft **PR_DEFERRED_SEND_TIME** ([PidTagDeferredSendTime](pidtagdeferredsendtime-canonical-property.md)) computing, wenn er nicht vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="41182-115">This property is used for computing the **PR_DEFERRED_SEND_TIME** ([PidTagDeferredSendTime](pidtagdeferredsendtime-canonical-property.md)) property when it is not present.</span></span> <span data-ttu-id="41182-116">Beim Senden einer Nachricht verzögert ist, sollte die **PR_DEFERRED_SEND_NUMBER** -Eigenschaft zusammen mit der Eigenschaft **PR_DEFERRED_SEND_UNITS** ([PidTagDeferredSendUnits](pidtagdeferredsendunits-canonical-property.md)) festgelegt werden, wenn die **PR_DEFERRED_SEND_TIME** -Eigenschaft nicht vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="41182-116">When sending a message is deferred, the **PR_DEFERRED_SEND_NUMBER** property should be set along with the **PR_DEFERRED_SEND_UNITS** ([PidTagDeferredSendUnits](pidtagdeferredsendunits-canonical-property.md)) property, if the **PR_DEFERRED_SEND_TIME** property is absent.</span></span> 
  
<span data-ttu-id="41182-117">Der Wert **PR_DEFERRED_SEND_NUMBER** muss zwischen 0 und 999 festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="41182-117">The **PR_DEFERRED_SEND_NUMBER** value must be set between 0 and 999.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="41182-118">Verwandte Ressourcen</span><span class="sxs-lookup"><span data-stu-id="41182-118">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="41182-119">Protokollspezifikationen</span><span class="sxs-lookup"><span data-stu-id="41182-119">Protocol specifications</span></span>

<span data-ttu-id="41182-120">[[MS-OXOMSG]](http://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="41182-120">[[MS-OXOMSG]](http://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="41182-121">Gibt die Eigenschaften und Operationen, die für e-Mail-Nachrichtenobjekte zulässig sind.</span><span class="sxs-lookup"><span data-stu-id="41182-121">Specifies the properties and operations that are permissible for email message objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="41182-122">Header-Dateien</span><span class="sxs-lookup"><span data-stu-id="41182-122">Header files</span></span>

<span data-ttu-id="41182-123">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="41182-123">Mapidefs.h</span></span>
  
> <span data-ttu-id="41182-124">Enthält die Datentypdefinitionen.</span><span class="sxs-lookup"><span data-stu-id="41182-124">Provides data type definitions.</span></span>
    
<span data-ttu-id="41182-125">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="41182-125">Mapitags.h</span></span>
  
> <span data-ttu-id="41182-126">Enthält Definitionen von Eigenschaften, die als Alternative Namen aufgelistet.</span><span class="sxs-lookup"><span data-stu-id="41182-126">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="41182-127">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="41182-127">See also</span></span>



[<span data-ttu-id="41182-128">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="41182-128">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="41182-129">Kanonische MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="41182-129">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="41182-130">Zuordnen von kanonischen Eigenschaftennamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="41182-130">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="41182-131">Zuordnen von MAPI-Namen zu kanonische Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="41182-131">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

