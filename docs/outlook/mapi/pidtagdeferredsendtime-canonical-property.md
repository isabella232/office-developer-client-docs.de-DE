---
title: PidTagDeferredSendTime (kanonische Eigenschaft)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagDeferredSendTime
api_type:
- HeaderDef
ms.assetid: ee206c2d-8371-4d19-b42b-78f6479e13ca
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: f636c0a49d6ad96ab157d00780fa6ffc5c8f3236
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2018
ms.locfileid: "22588272"
---
# <a name="pidtagdeferredsendtime-canonical-property"></a><span data-ttu-id="f24f1-103">PidTagDeferredSendTime (kanonische Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="f24f1-103">PidTagDeferredSendTime Canonical Property</span></span>

  
  
<span data-ttu-id="f24f1-104">**Betrifft**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="f24f1-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="f24f1-105">Gibt den Zeitpunkt, wenn ein Client Senden einer Nachricht zurückstellen möchten, an.</span><span class="sxs-lookup"><span data-stu-id="f24f1-105">Indicates a time when a client would like to defer sending a message.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="f24f1-106">Zugeordnete Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="f24f1-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="f24f1-107">PR_DEFERRED_SEND_TIME</span><span class="sxs-lookup"><span data-stu-id="f24f1-107">PR_DEFERRED_SEND_TIME</span></span>  <br/> |
|<span data-ttu-id="f24f1-108">Kennung:</span><span class="sxs-lookup"><span data-stu-id="f24f1-108">Identifier:</span></span>  <br/> |<span data-ttu-id="f24f1-109">0x3FEF</span><span class="sxs-lookup"><span data-stu-id="f24f1-109">0x3FEF</span></span>  <br/> |
|<span data-ttu-id="f24f1-110">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="f24f1-110">Data type:</span></span>  <br/> |<span data-ttu-id="f24f1-111">PT_SYSTIME</span><span class="sxs-lookup"><span data-stu-id="f24f1-111">PT_SYSTIME</span></span>  <br/> |
|<span data-ttu-id="f24f1-112">Bereich:</span><span class="sxs-lookup"><span data-stu-id="f24f1-112">Area:</span></span>  <br/> |<span data-ttu-id="f24f1-113">MAPI-status</span><span class="sxs-lookup"><span data-stu-id="f24f1-113">MAPI status</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="f24f1-114">HinwBemerkungeneise</span><span class="sxs-lookup"><span data-stu-id="f24f1-114">Remarks</span></span>

<span data-ttu-id="f24f1-115">Wenn die **PR_DEFERRED_SEND_UNITS** ([PidTagDeferredSendUnits](pidtagdeferredsendunits-canonical-property.md)) und **PR_DEFERRED_SEND_NUMBER** ([PidTagDeferredSendNumber](pidtagdeferredsendnumber-canonical-property.md)) Eigenschaften vorhanden sind, der Wert dieser Eigenschaft wird neu berechnet mithilfe der folgenden Formel und der alte Wert wird ignoriert.</span><span class="sxs-lookup"><span data-stu-id="f24f1-115">If the **PR_DEFERRED_SEND_UNITS** ([PidTagDeferredSendUnits](pidtagdeferredsendunits-canonical-property.md)) and **PR_DEFERRED_SEND_NUMBER** ([PidTagDeferredSendNumber](pidtagdeferredsendnumber-canonical-property.md)) properties are present, the value of this property is recomputed by using the following formula and the old value is ignored.</span></span>
  
 <span data-ttu-id="f24f1-116">**PR_DEFERRED_SEND_TIME** = **PR_CLIENT_SUBMIT_TIME** ([PidTagClientSubmitTime](pidtagclientsubmittime-canonical-property.md)) + **PR_DEFERRED_SEND_NUMBER** \* TimeOf (**PR_DEFERRED_SEND_UNITS**)</span><span class="sxs-lookup"><span data-stu-id="f24f1-116">**PR_DEFERRED_SEND_TIME** = **PR_CLIENT_SUBMIT_TIME** ([PidTagClientSubmitTime](pidtagclientsubmittime-canonical-property.md)) + **PR_DEFERRED_SEND_NUMBER** \* TimeOf(**PR_DEFERRED_SEND_UNITS**)</span></span>
  
<span data-ttu-id="f24f1-117">Wenn **PR_DEFERRED_SEND_TIME** Wert einer älteren Version als die aktuelle Uhrzeit (in UTC) ist, wird die Nachricht sofort gesendet.</span><span class="sxs-lookup"><span data-stu-id="f24f1-117">If **PR_DEFERRED_SEND_TIME** value is earlier than the current time (in UTC), the message is sent immediately.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="f24f1-118">Verwandte Ressourcen</span><span class="sxs-lookup"><span data-stu-id="f24f1-118">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="f24f1-119">Protokollspezifikationen</span><span class="sxs-lookup"><span data-stu-id="f24f1-119">Protocol specifications</span></span>

<span data-ttu-id="f24f1-120">[[MS-OXOMSG]](http://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="f24f1-120">[[MS-OXOMSG]](http://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="f24f1-121">Gibt die Eigenschaften und Operationen, die für e-Mail-Nachrichtenobjekte zulässig sind.</span><span class="sxs-lookup"><span data-stu-id="f24f1-121">Specifies the properties and operations that are permissible for email message objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="f24f1-122">Header-Dateien</span><span class="sxs-lookup"><span data-stu-id="f24f1-122">Header files</span></span>

<span data-ttu-id="f24f1-123">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="f24f1-123">Mapidefs.h</span></span>
  
> <span data-ttu-id="f24f1-124">Enthält die Datentypdefinitionen.</span><span class="sxs-lookup"><span data-stu-id="f24f1-124">Provides data type definitions.</span></span>
    
<span data-ttu-id="f24f1-125">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="f24f1-125">Mapitags.h</span></span>
  
> <span data-ttu-id="f24f1-126">Enthält Definitionen von Eigenschaften, die als Alternative Namen aufgelistet.</span><span class="sxs-lookup"><span data-stu-id="f24f1-126">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="f24f1-127">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="f24f1-127">See also</span></span>



[<span data-ttu-id="f24f1-128">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="f24f1-128">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="f24f1-129">Kanonische MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="f24f1-129">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="f24f1-130">Zuordnen von kanonischen Eigenschaftennamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="f24f1-130">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="f24f1-131">Zuordnen von MAPI-Namen zu kanonische Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="f24f1-131">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

