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
ms.openlocfilehash: 2d6374c2fd3c277e2bb976930e9e105cc839b1e8
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32359878"
---
# <a name="pidtagdeferredsendtime-canonical-property"></a><span data-ttu-id="95a27-103">PidTagDeferredSendTime (kanonische Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="95a27-103">PidTagDeferredSendTime Canonical Property</span></span>

  
  
<span data-ttu-id="95a27-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="95a27-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="95a27-105">Gibt einen Zeitpunkt an, zu dem ein Client das Senden einer Nachricht aufschubsen möchte.</span><span class="sxs-lookup"><span data-stu-id="95a27-105">Indicates a time when a client would like to defer sending a message.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="95a27-106">Zugeordnete Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="95a27-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="95a27-107">PR_DEFERRED_SEND_TIME</span><span class="sxs-lookup"><span data-stu-id="95a27-107">PR_DEFERRED_SEND_TIME</span></span>  <br/> |
|<span data-ttu-id="95a27-108">Kennung:</span><span class="sxs-lookup"><span data-stu-id="95a27-108">Identifier:</span></span>  <br/> |<span data-ttu-id="95a27-109">0x3FEF</span><span class="sxs-lookup"><span data-stu-id="95a27-109">0x3FEF</span></span>  <br/> |
|<span data-ttu-id="95a27-110">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="95a27-110">Data type:</span></span>  <br/> |<span data-ttu-id="95a27-111">PT_SYSTIME</span><span class="sxs-lookup"><span data-stu-id="95a27-111">PT_SYSTIME</span></span>  <br/> |
|<span data-ttu-id="95a27-112">Bereich:</span><span class="sxs-lookup"><span data-stu-id="95a27-112">Area:</span></span>  <br/> |<span data-ttu-id="95a27-113">MAPI-Status</span><span class="sxs-lookup"><span data-stu-id="95a27-113">MAPI status</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="95a27-114">Hinweise</span><span class="sxs-lookup"><span data-stu-id="95a27-114">Remarks</span></span>

<span data-ttu-id="95a27-115">Wenn die **Eigenschaften PR_DEFERRED_SEND_UNITS** ([PidTagDeferredSendUnits](pidtagdeferredsendunits-canonical-property.md)) und **PR_DEFERRED_SEND_NUMBER** ([PidTagDeferredSendNumber](pidtagdeferredsendnumber-canonical-property.md)) vorhanden sind, wird der Wert dieser Eigenschaft mithilfe der folgenden Formel neu berechnet, und der alte Wert wird ignoriert.</span><span class="sxs-lookup"><span data-stu-id="95a27-115">If the **PR_DEFERRED_SEND_UNITS** ([PidTagDeferredSendUnits](pidtagdeferredsendunits-canonical-property.md)) and **PR_DEFERRED_SEND_NUMBER** ([PidTagDeferredSendNumber](pidtagdeferredsendnumber-canonical-property.md)) properties are present, the value of this property is recomputed by using the following formula and the old value is ignored.</span></span>
  
 <span data-ttu-id="95a27-116">**PR_DEFERRED_SEND_TIME**  =  **PR_CLIENT_SUBMIT_TIME** ([PidTagClientSubmitTime](pidtagclientsubmittime-canonical-property.md)) + **PR_DEFERRED_SEND_NUMBER** \* TimeOf(**PR_DEFERRED_SEND_UNITS**)</span><span class="sxs-lookup"><span data-stu-id="95a27-116">**PR_DEFERRED_SEND_TIME** = **PR_CLIENT_SUBMIT_TIME** ([PidTagClientSubmitTime](pidtagclientsubmittime-canonical-property.md)) + **PR_DEFERRED_SEND_NUMBER** \* TimeOf(**PR_DEFERRED_SEND_UNITS**)</span></span>
  
<span data-ttu-id="95a27-117">Wenn **PR_DEFERRED_SEND_TIME** wert vor der aktuellen Uhrzeit (in UTC) liegt, wird die Nachricht sofort gesendet.</span><span class="sxs-lookup"><span data-stu-id="95a27-117">If **PR_DEFERRED_SEND_TIME** value is earlier than the current time (in UTC), the message is sent immediately.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="95a27-118">Verwandte Ressourcen</span><span class="sxs-lookup"><span data-stu-id="95a27-118">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="95a27-119">Protokollspezifikationen</span><span class="sxs-lookup"><span data-stu-id="95a27-119">Protocol specifications</span></span>

<span data-ttu-id="95a27-120">[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="95a27-120">[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="95a27-121">Gibt die Eigenschaften und Vorgänge an, die für E-Mail-Nachrichtenobjekte zulässig sind.</span><span class="sxs-lookup"><span data-stu-id="95a27-121">Specifies the properties and operations that are permissible for email message objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="95a27-122">Headerdateien</span><span class="sxs-lookup"><span data-stu-id="95a27-122">Header files</span></span>

<span data-ttu-id="95a27-123">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="95a27-123">Mapidefs.h</span></span>
  
> <span data-ttu-id="95a27-124">Bietet Datentypdefinitionen.</span><span class="sxs-lookup"><span data-stu-id="95a27-124">Provides data type definitions.</span></span>
    
<span data-ttu-id="95a27-125">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="95a27-125">Mapitags.h</span></span>
  
> <span data-ttu-id="95a27-126">Enthält Definitionen von Eigenschaften, die als alternative Namen aufgeführt sind.</span><span class="sxs-lookup"><span data-stu-id="95a27-126">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="95a27-127">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="95a27-127">See also</span></span>



[<span data-ttu-id="95a27-128">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="95a27-128">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="95a27-129">KANONISCHE EIGENSCHAFTEN VON MAPI</span><span class="sxs-lookup"><span data-stu-id="95a27-129">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="95a27-130">Zuordnen kanonischer Eigenschaftsnamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="95a27-130">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="95a27-131">Zuordnen von MAPI-Namen zu kanonischen Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="95a27-131">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

