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
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 227ceb468c54cea98519057b2f837a4aee84820c
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/04/2018
ms.locfileid: "25387216"
---
# <a name="pidtagoriginatornondeliveryreportrequested-canonical-property"></a><span data-ttu-id="660ab-103">PidTagOriginatorNonDeliveryReportRequested (kanonische Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="660ab-103">PidTagOriginatorNonDeliveryReportRequested Canonical Property</span></span>

  
  
<span data-ttu-id="660ab-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="660ab-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="660ab-105">Enthält True, wenn der Absender eine Nachricht einen Unzustellbarkeitsbericht für einen bestimmten Empfänger anfordert.</span><span class="sxs-lookup"><span data-stu-id="660ab-105">Contains TRUE if a message sender requests a nondelivery report for a particular recipient.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="660ab-106">Zugeordnete Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="660ab-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="660ab-107">PR_ORIGINATOR_NON_DELIVERY_REPORT_REQUESTED</span><span class="sxs-lookup"><span data-stu-id="660ab-107">PR_ORIGINATOR_NON_DELIVERY_REPORT_REQUESTED</span></span>  <br/> |
|<span data-ttu-id="660ab-108">Kennung:</span><span class="sxs-lookup"><span data-stu-id="660ab-108">Identifier:</span></span>  <br/> |<span data-ttu-id="660ab-109">0x0C08</span><span class="sxs-lookup"><span data-stu-id="660ab-109">0x0C08</span></span>  <br/> |
|<span data-ttu-id="660ab-110">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="660ab-110">Data type:</span></span>  <br/> |<span data-ttu-id="660ab-111">PT_BOOLEAN</span><span class="sxs-lookup"><span data-stu-id="660ab-111">PT_BOOLEAN</span></span>  <br/> |
|<span data-ttu-id="660ab-112">Bereich:</span><span class="sxs-lookup"><span data-stu-id="660ab-112">Area:</span></span>  <br/> |<span data-ttu-id="660ab-113">MIME</span><span class="sxs-lookup"><span data-stu-id="660ab-113">MIME</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="660ab-114">Hinweise</span><span class="sxs-lookup"><span data-stu-id="660ab-114">Remarks</span></span>

<span data-ttu-id="660ab-115">Diese Eigenschaft wird verwendet, um die messaging-System in Bearbeitung nicht zugestellte Nachrichten direkt.</span><span class="sxs-lookup"><span data-stu-id="660ab-115">This property is used to direct the messaging system in handling undelivered messages.</span></span> <span data-ttu-id="660ab-116">In diesem Fall muss die Nachricht auch die **PR_ORIGINATOR_DELIVERY_REPORT_REQUESTED** ([PidTagOriginatorDeliveryReportRequested](pidtagoriginatordeliveryreportrequested-canonical-property.md))-Eigenschaft auf FALSE festgelegt sind.</span><span class="sxs-lookup"><span data-stu-id="660ab-116">In this case, the message must also furnish the **PR_ORIGINATOR_DELIVERY_REPORT_REQUESTED** ([PidTagOriginatorDeliveryReportRequested](pidtagoriginatordeliveryreportrequested-canonical-property.md)) property set to FALSE.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="660ab-117">Verwandte Ressourcen</span><span class="sxs-lookup"><span data-stu-id="660ab-117">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="660ab-118">Protokollspezifikationen</span><span class="sxs-lookup"><span data-stu-id="660ab-118">Protocol specifications</span></span>

<span data-ttu-id="660ab-119">[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="660ab-119">[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="660ab-120">Gibt die Eigenschaften und Operationen, die für e-Mail-Nachrichtenobjekte zulässig sind.</span><span class="sxs-lookup"><span data-stu-id="660ab-120">Specifies the properties and operations that are permissible for email message objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="660ab-121">Header-Dateien</span><span class="sxs-lookup"><span data-stu-id="660ab-121">Header files</span></span>

<span data-ttu-id="660ab-122">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="660ab-122">Mapidefs.h</span></span>
  
> <span data-ttu-id="660ab-123">Enthält die Datentypdefinitionen.</span><span class="sxs-lookup"><span data-stu-id="660ab-123">Provides data type definitions.</span></span>
    
<span data-ttu-id="660ab-124">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="660ab-124">Mapitags.h</span></span>
  
> <span data-ttu-id="660ab-125">Enthält Definitionen von Eigenschaften, die als Alternative Namen aufgelistet.</span><span class="sxs-lookup"><span data-stu-id="660ab-125">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="660ab-126">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="660ab-126">See also</span></span>



[<span data-ttu-id="660ab-127">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="660ab-127">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="660ab-128">Kanonische MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="660ab-128">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="660ab-129">Zuordnen von kanonischen Eigenschaftennamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="660ab-129">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="660ab-130">Zuordnen von MAPI-Namen zu kanonische Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="660ab-130">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

