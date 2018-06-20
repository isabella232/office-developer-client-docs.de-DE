---
title: Kanonische PidTagDeliverTime-Eigenschaft
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagDeliverTime
api_type:
- HeaderDef
ms.assetid: da0ad17b-08ac-4c50-ac1d-13062b890dfd
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: 40839e34a61b5e5fdd3d7b69d8c553d7e469cd22
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19794298"
---
# <a name="pidtagdelivertime-canonical-property"></a><span data-ttu-id="5529d-103">Kanonische PidTagDeliverTime-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="5529d-103">PidTagDeliverTime Canonical Property</span></span>

  
  
<span data-ttu-id="5529d-104">**Betrifft**: Outlook</span><span class="sxs-lookup"><span data-stu-id="5529d-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="5529d-105">Enthält Datum und Uhrzeit, wann die ursprüngliche Nachricht übermittelt wurde.</span><span class="sxs-lookup"><span data-stu-id="5529d-105">Contains the date and time when the original message was delivered.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="5529d-106">Zugeordneten Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="5529d-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="5529d-107">PR_DELIVER_TIME</span><span class="sxs-lookup"><span data-stu-id="5529d-107">PR_DELIVER_TIME</span></span>  <br/> |
|<span data-ttu-id="5529d-108">Bezeichner:</span><span class="sxs-lookup"><span data-stu-id="5529d-108">Identifier:</span></span>  <br/> |<span data-ttu-id="5529d-109">0x0010</span><span class="sxs-lookup"><span data-stu-id="5529d-109">0x0010</span></span>  <br/> |
|<span data-ttu-id="5529d-110">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="5529d-110">Data type:</span></span>  <br/> |<span data-ttu-id="5529d-111">PT_SYSTIME</span><span class="sxs-lookup"><span data-stu-id="5529d-111">PT_SYSTIME</span></span>  <br/> |
|<span data-ttu-id="5529d-112">Bereich:</span><span class="sxs-lookup"><span data-stu-id="5529d-112">Area:</span></span>  <br/> |<span data-ttu-id="5529d-113">MAPI-Umschlag</span><span class="sxs-lookup"><span data-stu-id="5529d-113">MAPI envelope</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="5529d-114">Hinweise</span><span class="sxs-lookup"><span data-stu-id="5529d-114">Remarks</span></span>

<span data-ttu-id="5529d-115">Diese Eigenschaft ist eine pro Empfänger-Eigenschaft für einen Delivery Report, der die angibt, die die ursprüngliche Nachricht an die messaging-Benutzer übermittelt wurde für die der Übermittlungsbericht generiert wird.</span><span class="sxs-lookup"><span data-stu-id="5529d-115">This property is a per-recipient property on a delivery report that indicates the time the original message was delivered to the messaging user for which the delivery report is being generated.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="5529d-116">Verwandte Ressourcen</span><span class="sxs-lookup"><span data-stu-id="5529d-116">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="5529d-117">Header-Dateien</span><span class="sxs-lookup"><span data-stu-id="5529d-117">Header files</span></span>

<span data-ttu-id="5529d-118">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="5529d-118">Mapidefs.h</span></span>
  
> <span data-ttu-id="5529d-119">Enthält die Datentypdefinitionen.</span><span class="sxs-lookup"><span data-stu-id="5529d-119">Provides data type definitions.</span></span>
    
<span data-ttu-id="5529d-120">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="5529d-120">Mapitags.h</span></span>
  
> <span data-ttu-id="5529d-121">Enthält Definitionen von Eigenschaften, die als Alternative Namen aufgelistet.</span><span class="sxs-lookup"><span data-stu-id="5529d-121">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="5529d-122">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="5529d-122">See also</span></span>



[<span data-ttu-id="5529d-123">IMAPISupport::StatusRecips</span><span class="sxs-lookup"><span data-stu-id="5529d-123">IMAPISupport::StatusRecips</span></span>](imapisupport-statusrecips.md)


[<span data-ttu-id="5529d-124">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="5529d-124">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="5529d-125">Kanonische MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="5529d-125">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="5529d-126">Zuordnen von kanonischen Eigenschaftennamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="5529d-126">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="5529d-127">Zuordnen von MAPI-Namen zu kanonische Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="5529d-127">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

