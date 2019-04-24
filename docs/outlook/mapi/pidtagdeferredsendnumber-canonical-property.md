---
title: Kanonische Pidtagdeferredsendnumber (-Eigenschaft
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
ms.openlocfilehash: 9e3a30dad433b255573e4e3f041e6475b9227a54
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32357736"
---
# <a name="pidtagdeferredsendnumber-canonical-property"></a><span data-ttu-id="7b0b7-103">Kanonische Pidtagdeferredsendnumber (-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="7b0b7-103">PidTagDeferredSendNumber Canonical Property</span></span>

  
  
<span data-ttu-id="7b0b7-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="7b0b7-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="7b0b7-105">Enthält eine Zahl, die zum Berechnen der Verschiebung des Sendens einer Nachricht verwendet werden kann.</span><span class="sxs-lookup"><span data-stu-id="7b0b7-105">Contains a number that can be used to compute the deferment of sending a message.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="7b0b7-106">Zugeordnete Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="7b0b7-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="7b0b7-107">PR_DEFERRED_SEND_NUMBER</span><span class="sxs-lookup"><span data-stu-id="7b0b7-107">PR_DEFERRED_SEND_NUMBER</span></span>  <br/> |
|<span data-ttu-id="7b0b7-108">Kennung:</span><span class="sxs-lookup"><span data-stu-id="7b0b7-108">Identifier:</span></span>  <br/> |<span data-ttu-id="7b0b7-109">0x3FEB</span><span class="sxs-lookup"><span data-stu-id="7b0b7-109">0x3FEB</span></span>  <br/> |
|<span data-ttu-id="7b0b7-110">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="7b0b7-110">Data type:</span></span>  <br/> |<span data-ttu-id="7b0b7-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="7b0b7-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="7b0b7-112">Bereich:</span><span class="sxs-lookup"><span data-stu-id="7b0b7-112">Area:</span></span>  <br/> |<span data-ttu-id="7b0b7-113">MAPI-Status</span><span class="sxs-lookup"><span data-stu-id="7b0b7-113">MAPI status</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="7b0b7-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="7b0b7-114">Remarks</span></span>

<span data-ttu-id="7b0b7-115">Diese Eigenschaft wird zum Berechnen der **PR_DEFERRED_SEND_TIME** ([pidtagdeferredsendtime (](pidtagdeferredsendtime-canonical-property.md))-Eigenschaft verwendet, wenn Sie nicht vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="7b0b7-115">This property is used for computing the **PR_DEFERRED_SEND_TIME** ([PidTagDeferredSendTime](pidtagdeferredsendtime-canonical-property.md)) property when it is not present.</span></span> <span data-ttu-id="7b0b7-116">Wenn eine Nachricht verzögert wird, sollte die **PR_DEFERRED_SEND_NUMBER** -Eigenschaft zusammen mit der **PR_DEFERRED_SEND_UNITS** ([pidtagdeferredsendunits (](pidtagdeferredsendunits-canonical-property.md))-Eigenschaft festgelegt werden, wenn die **PR_DEFERRED_SEND_TIME** -Eigenschaft nicht vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="7b0b7-116">When sending a message is deferred, the **PR_DEFERRED_SEND_NUMBER** property should be set along with the **PR_DEFERRED_SEND_UNITS** ([PidTagDeferredSendUnits](pidtagdeferredsendunits-canonical-property.md)) property, if the **PR_DEFERRED_SEND_TIME** property is absent.</span></span> 
  
<span data-ttu-id="7b0b7-117">Der **PR_DEFERRED_SEND_NUMBER** -Wert muss zwischen 0 und 999 festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="7b0b7-117">The **PR_DEFERRED_SEND_NUMBER** value must be set between 0 and 999.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="7b0b7-118">Zugehörige Ressourcen</span><span class="sxs-lookup"><span data-stu-id="7b0b7-118">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="7b0b7-119">Protokollspezifikationen</span><span class="sxs-lookup"><span data-stu-id="7b0b7-119">Protocol specifications</span></span>

<span data-ttu-id="7b0b7-120">[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="7b0b7-120">[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="7b0b7-121">Gibt die Eigenschaften und Vorgänge an, die für e-Mail-Nachrichtenobjekte zulässig sind.</span><span class="sxs-lookup"><span data-stu-id="7b0b7-121">Specifies the properties and operations that are permissible for email message objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="7b0b7-122">Header Dateien</span><span class="sxs-lookup"><span data-stu-id="7b0b7-122">Header files</span></span>

<span data-ttu-id="7b0b7-123">Mapidefs. h</span><span class="sxs-lookup"><span data-stu-id="7b0b7-123">Mapidefs.h</span></span>
  
> <span data-ttu-id="7b0b7-124">Stellt Datentypdefinitionen bereit.</span><span class="sxs-lookup"><span data-stu-id="7b0b7-124">Provides data type definitions.</span></span>
    
<span data-ttu-id="7b0b7-125">Mapitags. h</span><span class="sxs-lookup"><span data-stu-id="7b0b7-125">Mapitags.h</span></span>
  
> <span data-ttu-id="7b0b7-126">Enthält Definitionen von Eigenschaften, die als Alternative Namen aufgeführt sind.</span><span class="sxs-lookup"><span data-stu-id="7b0b7-126">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="7b0b7-127">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="7b0b7-127">See also</span></span>



[<span data-ttu-id="7b0b7-128">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="7b0b7-128">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="7b0b7-129">Kanonische MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="7b0b7-129">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="7b0b7-130">Zuordnen von kanonischen Eigenschaftennamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="7b0b7-130">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="7b0b7-131">Zuordnen von MAPI-Namen zu kanonischen Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="7b0b7-131">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

