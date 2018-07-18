---
title: PidTagOriginatorNonDeliveryReportRequested (kanonische Eigenschaft)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagOriginatorNonDeliveryReportRequested
api_type:
- COM
ms.assetid: 0a19ba44-abb0-4868-9d7d-75184058d4c0
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: 841d2b14efc781d89727b0c7ed677f527526a4ff
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19794734"
---
# <a name="pidtagoriginatornondeliveryreportrequested-canonical-property"></a><span data-ttu-id="5d9a4-103">PidTagOriginatorNonDeliveryReportRequested (kanonische Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="5d9a4-103">PidTagOriginatorNonDeliveryReportRequested Canonical Property</span></span>

  
  
<span data-ttu-id="5d9a4-104">**Betrifft**: Outlook</span><span class="sxs-lookup"><span data-stu-id="5d9a4-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="5d9a4-105">Enthält True, wenn der Absender eine Nachricht einen Unzustellbarkeitsbericht für einen bestimmten Empfänger anfordert.</span><span class="sxs-lookup"><span data-stu-id="5d9a4-105">Contains TRUE if a message sender requests a nondelivery report for a particular recipient.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="5d9a4-106">Zugeordneten Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="5d9a4-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="5d9a4-107">PR_ORIGINATOR_NON_DELIVERY_REPORT_REQUESTED</span><span class="sxs-lookup"><span data-stu-id="5d9a4-107">PR_ORIGINATOR_NON_DELIVERY_REPORT_REQUESTED</span></span>  <br/> |
|<span data-ttu-id="5d9a4-108">Bezeichner:</span><span class="sxs-lookup"><span data-stu-id="5d9a4-108">Identifier:</span></span>  <br/> |<span data-ttu-id="5d9a4-109">0x0C08</span><span class="sxs-lookup"><span data-stu-id="5d9a4-109">0x0C08</span></span>  <br/> |
|<span data-ttu-id="5d9a4-110">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="5d9a4-110">Data type:</span></span>  <br/> |<span data-ttu-id="5d9a4-111">PT_BOOLEAN</span><span class="sxs-lookup"><span data-stu-id="5d9a4-111">PT_BOOLEAN</span></span>  <br/> |
|<span data-ttu-id="5d9a4-112">Bereich:</span><span class="sxs-lookup"><span data-stu-id="5d9a4-112">Area:</span></span>  <br/> |<span data-ttu-id="5d9a4-113">MIME</span><span class="sxs-lookup"><span data-stu-id="5d9a4-113">MIME</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="5d9a4-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="5d9a4-114">Remarks</span></span>

<span data-ttu-id="5d9a4-115">Diese Eigenschaft wird verwendet, um die messaging-System in Bearbeitung nicht zugestellte Nachrichten direkt.</span><span class="sxs-lookup"><span data-stu-id="5d9a4-115">This property is used to direct the messaging system in handling undelivered messages.</span></span> <span data-ttu-id="5d9a4-116">In diesem Fall muss die Nachricht auch die **PR_ORIGINATOR_DELIVERY_REPORT_REQUESTED** ([PidTagOriginatorDeliveryReportRequested](pidtagoriginatordeliveryreportrequested-canonical-property.md))-Eigenschaft auf FALSE festgelegt sind.</span><span class="sxs-lookup"><span data-stu-id="5d9a4-116">In this case, the message must also furnish the **PR_ORIGINATOR_DELIVERY_REPORT_REQUESTED** ([PidTagOriginatorDeliveryReportRequested](pidtagoriginatordeliveryreportrequested-canonical-property.md)) property set to FALSE.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="5d9a4-117">Verwandte Ressourcen</span><span class="sxs-lookup"><span data-stu-id="5d9a4-117">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="5d9a4-118">Protokollspezifikationen</span><span class="sxs-lookup"><span data-stu-id="5d9a4-118">Protocol specifications</span></span>

<span data-ttu-id="5d9a4-119">[[MS-OXOMSG]](http://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="5d9a4-119">[[MS-OXOMSG]](http://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="5d9a4-120">Gibt die Eigenschaften und Operationen, die für e-Mail-Nachrichtenobjekte zulässig sind.</span><span class="sxs-lookup"><span data-stu-id="5d9a4-120">Specifies the properties and operations that are permissible for email message objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="5d9a4-121">Header-Dateien</span><span class="sxs-lookup"><span data-stu-id="5d9a4-121">Header files</span></span>

<span data-ttu-id="5d9a4-122">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="5d9a4-122">Mapidefs.h</span></span>
  
> <span data-ttu-id="5d9a4-123">Enthält die Datentypdefinitionen.</span><span class="sxs-lookup"><span data-stu-id="5d9a4-123">Provides data type definitions.</span></span>
    
<span data-ttu-id="5d9a4-124">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="5d9a4-124">Mapitags.h</span></span>
  
> <span data-ttu-id="5d9a4-125">Enthält Definitionen von Eigenschaften, die als Alternative Namen aufgelistet.</span><span class="sxs-lookup"><span data-stu-id="5d9a4-125">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="5d9a4-126">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="5d9a4-126">See also</span></span>



[<span data-ttu-id="5d9a4-127">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="5d9a4-127">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="5d9a4-128">Kanonische MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="5d9a4-128">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="5d9a4-129">Zuordnen von kanonischen Eigenschaftennamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="5d9a4-129">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="5d9a4-130">Zuordnen von MAPI-Namen zu kanonische Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="5d9a4-130">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

