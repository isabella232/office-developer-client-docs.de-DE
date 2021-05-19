---
title: PidTagDeliverTime (kanonische Eigenschaft)
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
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 3e9318e396bf195ad701b92372a3136dee7fd0d8
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33435278"
---
# <a name="pidtagdelivertime-canonical-property"></a><span data-ttu-id="de737-103">PidTagDeliverTime (kanonische Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="de737-103">PidTagDeliverTime Canonical Property</span></span>

  
  
<span data-ttu-id="de737-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="de737-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="de737-105">Enthält das Datum und die Uhrzeit, zu der die ursprüngliche Nachricht zugestellt wurde.</span><span class="sxs-lookup"><span data-stu-id="de737-105">Contains the date and time when the original message was delivered.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="de737-106">Zugeordnete Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="de737-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="de737-107">PR_DELIVER_TIME</span><span class="sxs-lookup"><span data-stu-id="de737-107">PR_DELIVER_TIME</span></span>  <br/> |
|<span data-ttu-id="de737-108">Kennung:</span><span class="sxs-lookup"><span data-stu-id="de737-108">Identifier:</span></span>  <br/> |<span data-ttu-id="de737-109">0x0010</span><span class="sxs-lookup"><span data-stu-id="de737-109">0x0010</span></span>  <br/> |
|<span data-ttu-id="de737-110">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="de737-110">Data type:</span></span>  <br/> |<span data-ttu-id="de737-111">PT_SYSTIME</span><span class="sxs-lookup"><span data-stu-id="de737-111">PT_SYSTIME</span></span>  <br/> |
|<span data-ttu-id="de737-112">Bereich:</span><span class="sxs-lookup"><span data-stu-id="de737-112">Area:</span></span>  <br/> |<span data-ttu-id="de737-113">MAPI-Umschlag</span><span class="sxs-lookup"><span data-stu-id="de737-113">MAPI envelope</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="de737-114">Hinweise</span><span class="sxs-lookup"><span data-stu-id="de737-114">Remarks</span></span>

<span data-ttu-id="de737-115">Diese Eigenschaft ist eine Pro-Empfänger-Eigenschaft für einen Zustellungsbericht, die angibt, zu welchem Zeitpunkt die ursprüngliche Nachricht an den Messagingbenutzer übermittelt wurde, für den der Übermittlungsbericht generiert wird.</span><span class="sxs-lookup"><span data-stu-id="de737-115">This property is a per-recipient property on a delivery report that indicates the time the original message was delivered to the messaging user for which the delivery report is being generated.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="de737-116">Verwandte Ressourcen</span><span class="sxs-lookup"><span data-stu-id="de737-116">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="de737-117">Headerdateien</span><span class="sxs-lookup"><span data-stu-id="de737-117">Header files</span></span>

<span data-ttu-id="de737-118">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="de737-118">Mapidefs.h</span></span>
  
> <span data-ttu-id="de737-119">Bietet Datentypdefinitionen.</span><span class="sxs-lookup"><span data-stu-id="de737-119">Provides data type definitions.</span></span>
    
<span data-ttu-id="de737-120">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="de737-120">Mapitags.h</span></span>
  
> <span data-ttu-id="de737-121">Enthält Definitionen von Eigenschaften, die als alternative Namen aufgeführt sind.</span><span class="sxs-lookup"><span data-stu-id="de737-121">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="de737-122">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="de737-122">See also</span></span>



[<span data-ttu-id="de737-123">IMAPISupport::StatusRecips</span><span class="sxs-lookup"><span data-stu-id="de737-123">IMAPISupport::StatusRecips</span></span>](imapisupport-statusrecips.md)


[<span data-ttu-id="de737-124">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="de737-124">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="de737-125">KANONISCHE EIGENSCHAFTEN VON MAPI</span><span class="sxs-lookup"><span data-stu-id="de737-125">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="de737-126">Zuordnen kanonischer Eigenschaftsnamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="de737-126">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="de737-127">Zuordnen von MAPI-Namen zu kanonischen Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="de737-127">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

