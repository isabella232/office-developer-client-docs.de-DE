---
title: PidTagOriginatorDeliveryReportRequested (kanonische Eigenschaft)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagOriginatorDeliveryReportRequested
api_type:
- COM
ms.assetid: 4461b35d-e2b9-41ff-b079-31bfef02e2bb
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: a92ee13e571032c050f69677d9daba8dad7aea3c
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32356301"
---
# <a name="pidtagoriginatordeliveryreportrequested-canonical-property"></a><span data-ttu-id="8cb83-103">PidTagOriginatorDeliveryReportRequested (kanonische Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="8cb83-103">PidTagOriginatorDeliveryReportRequested Canonical Property</span></span>

  
  
<span data-ttu-id="8cb83-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="8cb83-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="8cb83-105">Enthält TRUE, wenn ein Nachrichtensender einen Zustellungsbericht für einen bestimmten Empfänger vom Messagingsystem anfordert, bevor die Nachricht im Nachrichtenspeicher platziert wird.</span><span class="sxs-lookup"><span data-stu-id="8cb83-105">Contains TRUE if a message sender requests a delivery report for a particular recipient from the messaging system before the message is placed in the message store.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="8cb83-106">Zugeordnete Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="8cb83-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="8cb83-107">PR_ORIGINATOR_DELIVERY_REPORT_REQUESTED</span><span class="sxs-lookup"><span data-stu-id="8cb83-107">PR_ORIGINATOR_DELIVERY_REPORT_REQUESTED</span></span>  <br/> |
|<span data-ttu-id="8cb83-108">Kennung:</span><span class="sxs-lookup"><span data-stu-id="8cb83-108">Identifier:</span></span>  <br/> |<span data-ttu-id="8cb83-109">0x0023</span><span class="sxs-lookup"><span data-stu-id="8cb83-109">0x0023</span></span>  <br/> |
|<span data-ttu-id="8cb83-110">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="8cb83-110">Data type:</span></span>  <br/> |<span data-ttu-id="8cb83-111">PT_BOOLEAN</span><span class="sxs-lookup"><span data-stu-id="8cb83-111">PT_BOOLEAN</span></span>  <br/> |
|<span data-ttu-id="8cb83-112">Bereich:</span><span class="sxs-lookup"><span data-stu-id="8cb83-112">Area:</span></span>  <br/> |<span data-ttu-id="8cb83-113">MIME</span><span class="sxs-lookup"><span data-stu-id="8cb83-113">MIME</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="8cb83-114">Hinweise</span><span class="sxs-lookup"><span data-stu-id="8cb83-114">Remarks</span></span>

<span data-ttu-id="8cb83-115">Diese Eigenschaft wird verwendet, um das Messagingsystem bei der Verarbeitung von zugestellten Nachrichten an das Messagingsystem weiter zu senden.</span><span class="sxs-lookup"><span data-stu-id="8cb83-115">This property is used to direct the messaging system in handling delivered messages.</span></span> <span data-ttu-id="8cb83-116">In diesem Fall muss die Nachricht auch die **eigenschaft PR_ORIGINATOR_NON_DELIVERY_REPORT_REQUESTED** ([PidTagOriginatorNonDeliveryReportRequested](pidtagoriginatornondeliveryreportrequested-canonical-property.md)) auf FALSE festlegen.</span><span class="sxs-lookup"><span data-stu-id="8cb83-116">In this case, the message must also furnish the **PR_ORIGINATOR_NON_DELIVERY_REPORT_REQUESTED** ([PidTagOriginatorNonDeliveryReportRequested](pidtagoriginatornondeliveryreportrequested-canonical-property.md)) property set to FALSE.</span></span>
  
<span data-ttu-id="8cb83-117">Das Festlegen **PR_ORIGINATOR_DELIVERY_REPORT_REQUESTED** -Eigenschaft für eine Nachricht ist eine Möglichkeit zum Anfordern von Übermittlungsstatusberichten für alle Empfänger.</span><span class="sxs-lookup"><span data-stu-id="8cb83-117">Setting the **PR_ORIGINATOR_DELIVERY_REPORT_REQUESTED** property on a message is a way to request delivery status reports for all recipients.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="8cb83-118">Verwandte Ressourcen</span><span class="sxs-lookup"><span data-stu-id="8cb83-118">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="8cb83-119">Protokollspezifikationen</span><span class="sxs-lookup"><span data-stu-id="8cb83-119">Protocol specifications</span></span>

<span data-ttu-id="8cb83-120">[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="8cb83-120">[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="8cb83-121">Gibt die Eigenschaften und Vorgänge an, die für E-Mail-Nachrichtenobjekte zulässig sind.</span><span class="sxs-lookup"><span data-stu-id="8cb83-121">Specifies the properties and operations that are permissible for email message objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="8cb83-122">Headerdateien</span><span class="sxs-lookup"><span data-stu-id="8cb83-122">Header files</span></span>

<span data-ttu-id="8cb83-123">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="8cb83-123">Mapidefs.h</span></span>
  
> <span data-ttu-id="8cb83-124">Bietet Datentypdefinitionen.</span><span class="sxs-lookup"><span data-stu-id="8cb83-124">Provides data type definitions.</span></span>
    
<span data-ttu-id="8cb83-125">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="8cb83-125">Mapitags.h</span></span>
  
> <span data-ttu-id="8cb83-126">Enthält Definitionen von Eigenschaften, die als alternative Namen aufgeführt sind.</span><span class="sxs-lookup"><span data-stu-id="8cb83-126">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="8cb83-127">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="8cb83-127">See also</span></span>



[<span data-ttu-id="8cb83-128">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="8cb83-128">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="8cb83-129">KANONISCHE EIGENSCHAFTEN VON MAPI</span><span class="sxs-lookup"><span data-stu-id="8cb83-129">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="8cb83-130">Zuordnen kanonischer Eigenschaftsnamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="8cb83-130">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="8cb83-131">Zuordnen von MAPI-Namen zu kanonischen Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="8cb83-131">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

