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
ms.openlocfilehash: 07cea7606654bf32c1fe70e49254afeeb04f0e98
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19794749"
---
# <a name="pidtagoriginatordeliveryreportrequested-canonical-property"></a><span data-ttu-id="bfc80-103">PidTagOriginatorDeliveryReportRequested (kanonische Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="bfc80-103">PidTagOriginatorDeliveryReportRequested Canonical Property</span></span>

  
  
<span data-ttu-id="bfc80-104">**Betrifft**: Outlook</span><span class="sxs-lookup"><span data-stu-id="bfc80-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="bfc80-105">Enthält True, wenn den Absender einer Nachricht ein Zustellungsberichts für einen bestimmten Empfänger von messaging-System anfordert, bevor die Nachricht im Nachrichtenspeicher abgelegt wird.</span><span class="sxs-lookup"><span data-stu-id="bfc80-105">Contains TRUE if a message sender requests a delivery report for a particular recipient from the messaging system before the message is placed in the message store.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="bfc80-106">Zugeordneten Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="bfc80-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="bfc80-107">PR_ORIGINATOR_DELIVERY_REPORT_REQUESTED</span><span class="sxs-lookup"><span data-stu-id="bfc80-107">PR_ORIGINATOR_DELIVERY_REPORT_REQUESTED</span></span>  <br/> |
|<span data-ttu-id="bfc80-108">Bezeichner:</span><span class="sxs-lookup"><span data-stu-id="bfc80-108">Identifier:</span></span>  <br/> |<span data-ttu-id="bfc80-109">0x0023</span><span class="sxs-lookup"><span data-stu-id="bfc80-109">0x0023</span></span>  <br/> |
|<span data-ttu-id="bfc80-110">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="bfc80-110">Data type:</span></span>  <br/> |<span data-ttu-id="bfc80-111">PT_BOOLEAN</span><span class="sxs-lookup"><span data-stu-id="bfc80-111">PT_BOOLEAN</span></span>  <br/> |
|<span data-ttu-id="bfc80-112">Bereich:</span><span class="sxs-lookup"><span data-stu-id="bfc80-112">Area:</span></span>  <br/> |<span data-ttu-id="bfc80-113">MIME</span><span class="sxs-lookup"><span data-stu-id="bfc80-113">MIME</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="bfc80-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="bfc80-114">Remarks</span></span>

<span data-ttu-id="bfc80-115">Diese Eigenschaft wird verwendet, um Nachrichtensystem Umgang mit Nachrichten zu leiten.</span><span class="sxs-lookup"><span data-stu-id="bfc80-115">This property is used to direct the messaging system in handling delivered messages.</span></span> <span data-ttu-id="bfc80-116">In diesem Fall muss die Nachricht auch die **PR_ORIGINATOR_NON_DELIVERY_REPORT_REQUESTED** ([PidTagOriginatorNonDeliveryReportRequested](pidtagoriginatornondeliveryreportrequested-canonical-property.md))-Eigenschaft auf FALSE festgelegt sind.</span><span class="sxs-lookup"><span data-stu-id="bfc80-116">In this case, the message must also furnish the **PR_ORIGINATOR_NON_DELIVERY_REPORT_REQUESTED** ([PidTagOriginatorNonDeliveryReportRequested](pidtagoriginatornondeliveryreportrequested-canonical-property.md)) property set to FALSE.</span></span>
  
<span data-ttu-id="bfc80-117">Festlegen der **PR_ORIGINATOR_DELIVERY_REPORT_REQUESTED** -Eigenschaft auf eine Nachricht ist eine Möglichkeit zum Status Übermittlungsberichte für alle Empfänger.</span><span class="sxs-lookup"><span data-stu-id="bfc80-117">Setting the **PR_ORIGINATOR_DELIVERY_REPORT_REQUESTED** property on a message is a way to request delivery status reports for all recipients.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="bfc80-118">Verwandte Ressourcen</span><span class="sxs-lookup"><span data-stu-id="bfc80-118">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="bfc80-119">Protokollspezifikationen</span><span class="sxs-lookup"><span data-stu-id="bfc80-119">Protocol specifications</span></span>

<span data-ttu-id="bfc80-120">[[MS-OXOMSG]](http://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="bfc80-120">[[MS-OXOMSG]](http://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="bfc80-121">Gibt die Eigenschaften und Operationen, die für e-Mail-Nachrichtenobjekte zulässig sind.</span><span class="sxs-lookup"><span data-stu-id="bfc80-121">Specifies the properties and operations that are permissible for email message objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="bfc80-122">Header-Dateien</span><span class="sxs-lookup"><span data-stu-id="bfc80-122">Header files</span></span>

<span data-ttu-id="bfc80-123">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="bfc80-123">Mapidefs.h</span></span>
  
> <span data-ttu-id="bfc80-124">Enthält die Datentypdefinitionen.</span><span class="sxs-lookup"><span data-stu-id="bfc80-124">Provides data type definitions.</span></span>
    
<span data-ttu-id="bfc80-125">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="bfc80-125">Mapitags.h</span></span>
  
> <span data-ttu-id="bfc80-126">Enthält Definitionen von Eigenschaften, die als Alternative Namen aufgelistet.</span><span class="sxs-lookup"><span data-stu-id="bfc80-126">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="bfc80-127">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="bfc80-127">See also</span></span>



[<span data-ttu-id="bfc80-128">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="bfc80-128">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="bfc80-129">Kanonische MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="bfc80-129">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="bfc80-130">Zuordnen von kanonischen Eigenschaftennamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="bfc80-130">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="bfc80-131">Zuordnen von MAPI-Namen zu kanonische Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="bfc80-131">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

