---
title: Kanonische Pidtagdelivertime (-Eigenschaft
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
ms.openlocfilehash: 3e9318e396bf195ad701b92372a3136dee7fd0d8
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32357722"
---
# <a name="pidtagdelivertime-canonical-property"></a><span data-ttu-id="61b96-103">Kanonische Pidtagdelivertime (-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="61b96-103">PidTagDeliverTime Canonical Property</span></span>

  
  
<span data-ttu-id="61b96-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="61b96-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="61b96-105">Enthält das Datum und die Uhrzeit der Zustellung der ursprünglichen Nachricht.</span><span class="sxs-lookup"><span data-stu-id="61b96-105">Contains the date and time when the original message was delivered.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="61b96-106">Zugeordnete Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="61b96-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="61b96-107">PR_DELIVER_TIME</span><span class="sxs-lookup"><span data-stu-id="61b96-107">PR_DELIVER_TIME</span></span>  <br/> |
|<span data-ttu-id="61b96-108">Kennung:</span><span class="sxs-lookup"><span data-stu-id="61b96-108">Identifier:</span></span>  <br/> |<span data-ttu-id="61b96-109">0x0010</span><span class="sxs-lookup"><span data-stu-id="61b96-109">0x0010</span></span>  <br/> |
|<span data-ttu-id="61b96-110">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="61b96-110">Data type:</span></span>  <br/> |<span data-ttu-id="61b96-111">PT_SYSTIME</span><span class="sxs-lookup"><span data-stu-id="61b96-111">PT_SYSTIME</span></span>  <br/> |
|<span data-ttu-id="61b96-112">Bereich:</span><span class="sxs-lookup"><span data-stu-id="61b96-112">Area:</span></span>  <br/> |<span data-ttu-id="61b96-113">MAPI-Umschlag</span><span class="sxs-lookup"><span data-stu-id="61b96-113">MAPI envelope</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="61b96-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="61b96-114">Remarks</span></span>

<span data-ttu-id="61b96-115">Diese Eigenschaft ist eine empfängerspezifische Eigenschaft in einem Zustellungsbericht, der angibt, wie lange die ursprüngliche Nachricht an den Messagingbenutzer übermittelt wurde, für den der Zustellungsbericht generiert wird.</span><span class="sxs-lookup"><span data-stu-id="61b96-115">This property is a per-recipient property on a delivery report that indicates the time the original message was delivered to the messaging user for which the delivery report is being generated.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="61b96-116">Zugehörige Ressourcen</span><span class="sxs-lookup"><span data-stu-id="61b96-116">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="61b96-117">Header Dateien</span><span class="sxs-lookup"><span data-stu-id="61b96-117">Header files</span></span>

<span data-ttu-id="61b96-118">Mapidefs. h</span><span class="sxs-lookup"><span data-stu-id="61b96-118">Mapidefs.h</span></span>
  
> <span data-ttu-id="61b96-119">Stellt Datentypdefinitionen bereit.</span><span class="sxs-lookup"><span data-stu-id="61b96-119">Provides data type definitions.</span></span>
    
<span data-ttu-id="61b96-120">Mapitags. h</span><span class="sxs-lookup"><span data-stu-id="61b96-120">Mapitags.h</span></span>
  
> <span data-ttu-id="61b96-121">Enthält Definitionen von Eigenschaften, die als Alternative Namen aufgeführt sind.</span><span class="sxs-lookup"><span data-stu-id="61b96-121">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="61b96-122">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="61b96-122">See also</span></span>



[<span data-ttu-id="61b96-123">IMAPISupport::StatusRecips</span><span class="sxs-lookup"><span data-stu-id="61b96-123">IMAPISupport::StatusRecips</span></span>](imapisupport-statusrecips.md)


[<span data-ttu-id="61b96-124">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="61b96-124">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="61b96-125">Kanonische MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="61b96-125">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="61b96-126">Zuordnen von kanonischen Eigenschaftennamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="61b96-126">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="61b96-127">Zuordnen von MAPI-Namen zu kanonischen Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="61b96-127">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

