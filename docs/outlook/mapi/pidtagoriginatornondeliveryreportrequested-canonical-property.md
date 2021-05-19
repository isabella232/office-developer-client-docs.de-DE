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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32341958"
---
# <a name="pidtagoriginatornondeliveryreportrequested-canonical-property"></a><span data-ttu-id="fad81-103">PidTagOriginatorNonDeliveryReportRequested (kanonische Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="fad81-103">PidTagOriginatorNonDeliveryReportRequested Canonical Property</span></span>

  
  
<span data-ttu-id="fad81-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="fad81-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="fad81-105">Enthält TRUE, wenn ein Nachrichtensender einen Unauslöschungsbericht für einen bestimmten Empfänger anfordert.</span><span class="sxs-lookup"><span data-stu-id="fad81-105">Contains TRUE if a message sender requests a nondelivery report for a particular recipient.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="fad81-106">Zugeordnete Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="fad81-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="fad81-107">PR_ORIGINATOR_NON_DELIVERY_REPORT_REQUESTED</span><span class="sxs-lookup"><span data-stu-id="fad81-107">PR_ORIGINATOR_NON_DELIVERY_REPORT_REQUESTED</span></span>  <br/> |
|<span data-ttu-id="fad81-108">Kennung:</span><span class="sxs-lookup"><span data-stu-id="fad81-108">Identifier:</span></span>  <br/> |<span data-ttu-id="fad81-109">0x0C08</span><span class="sxs-lookup"><span data-stu-id="fad81-109">0x0C08</span></span>  <br/> |
|<span data-ttu-id="fad81-110">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="fad81-110">Data type:</span></span>  <br/> |<span data-ttu-id="fad81-111">PT_BOOLEAN</span><span class="sxs-lookup"><span data-stu-id="fad81-111">PT_BOOLEAN</span></span>  <br/> |
|<span data-ttu-id="fad81-112">Bereich:</span><span class="sxs-lookup"><span data-stu-id="fad81-112">Area:</span></span>  <br/> |<span data-ttu-id="fad81-113">MIME</span><span class="sxs-lookup"><span data-stu-id="fad81-113">MIME</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="fad81-114">Hinweise</span><span class="sxs-lookup"><span data-stu-id="fad81-114">Remarks</span></span>

<span data-ttu-id="fad81-115">Diese Eigenschaft wird verwendet, um das Messagingsystem bei der Verarbeitung nicht zugestellter Nachrichten anzufeinen.</span><span class="sxs-lookup"><span data-stu-id="fad81-115">This property is used to direct the messaging system in handling undelivered messages.</span></span> <span data-ttu-id="fad81-116">In diesem Fall muss die Nachricht auch die **eigenschaft PR_ORIGINATOR_DELIVERY_REPORT_REQUESTED** ([PidTagOriginatorDeliveryReportRequested](pidtagoriginatordeliveryreportrequested-canonical-property.md)) auf FALSE festlegen.</span><span class="sxs-lookup"><span data-stu-id="fad81-116">In this case, the message must also furnish the **PR_ORIGINATOR_DELIVERY_REPORT_REQUESTED** ([PidTagOriginatorDeliveryReportRequested](pidtagoriginatordeliveryreportrequested-canonical-property.md)) property set to FALSE.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="fad81-117">Verwandte Ressourcen</span><span class="sxs-lookup"><span data-stu-id="fad81-117">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="fad81-118">Protokollspezifikationen</span><span class="sxs-lookup"><span data-stu-id="fad81-118">Protocol specifications</span></span>

<span data-ttu-id="fad81-119">[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="fad81-119">[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="fad81-120">Gibt die Eigenschaften und Vorgänge an, die für E-Mail-Nachrichtenobjekte zulässig sind.</span><span class="sxs-lookup"><span data-stu-id="fad81-120">Specifies the properties and operations that are permissible for email message objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="fad81-121">Headerdateien</span><span class="sxs-lookup"><span data-stu-id="fad81-121">Header files</span></span>

<span data-ttu-id="fad81-122">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="fad81-122">Mapidefs.h</span></span>
  
> <span data-ttu-id="fad81-123">Bietet Datentypdefinitionen.</span><span class="sxs-lookup"><span data-stu-id="fad81-123">Provides data type definitions.</span></span>
    
<span data-ttu-id="fad81-124">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="fad81-124">Mapitags.h</span></span>
  
> <span data-ttu-id="fad81-125">Enthält Definitionen von Eigenschaften, die als alternative Namen aufgeführt sind.</span><span class="sxs-lookup"><span data-stu-id="fad81-125">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="fad81-126">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="fad81-126">See also</span></span>



[<span data-ttu-id="fad81-127">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="fad81-127">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="fad81-128">KANONISCHE EIGENSCHAFTEN VON MAPI</span><span class="sxs-lookup"><span data-stu-id="fad81-128">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="fad81-129">Zuordnen kanonischer Eigenschaftsnamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="fad81-129">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="fad81-130">Zuordnen von MAPI-Namen zu kanonischen Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="fad81-130">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

