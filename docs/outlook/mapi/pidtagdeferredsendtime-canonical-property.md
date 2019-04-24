---
title: Kanonische Pidtagdeferredsendtime (-Eigenschaft
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
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: 2d6374c2fd3c277e2bb976930e9e105cc839b1e8
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32359878"
---
# <a name="pidtagdeferredsendtime-canonical-property"></a><span data-ttu-id="f2716-103">Kanonische Pidtagdeferredsendtime (-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="f2716-103">PidTagDeferredSendTime Canonical Property</span></span>

  
  
<span data-ttu-id="f2716-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="f2716-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="f2716-105">Gibt einen Zeitpunkt an, zu dem ein Client das Senden einer Nachricht aufschieben möchte.</span><span class="sxs-lookup"><span data-stu-id="f2716-105">Indicates a time when a client would like to defer sending a message.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="f2716-106">Zugeordnete Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="f2716-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="f2716-107">PR_DEFERRED_SEND_TIME</span><span class="sxs-lookup"><span data-stu-id="f2716-107">PR_DEFERRED_SEND_TIME</span></span>  <br/> |
|<span data-ttu-id="f2716-108">Kennung:</span><span class="sxs-lookup"><span data-stu-id="f2716-108">Identifier:</span></span>  <br/> |<span data-ttu-id="f2716-109">0x3FEF</span><span class="sxs-lookup"><span data-stu-id="f2716-109">0x3FEF</span></span>  <br/> |
|<span data-ttu-id="f2716-110">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="f2716-110">Data type:</span></span>  <br/> |<span data-ttu-id="f2716-111">PT_SYSTIME</span><span class="sxs-lookup"><span data-stu-id="f2716-111">PT_SYSTIME</span></span>  <br/> |
|<span data-ttu-id="f2716-112">Bereich:</span><span class="sxs-lookup"><span data-stu-id="f2716-112">Area:</span></span>  <br/> |<span data-ttu-id="f2716-113">MAPI-Status</span><span class="sxs-lookup"><span data-stu-id="f2716-113">MAPI status</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="f2716-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="f2716-114">Remarks</span></span>

<span data-ttu-id="f2716-115">Wenn die Eigenschaften **PR_DEFERRED_SEND_UNITS** ([Pidtagdeferredsendunits (](pidtagdeferredsendunits-canonical-property.md)) und **PR_DEFERRED_SEND_NUMBER** ([pidtagdeferredsendnumber (](pidtagdeferredsendnumber-canonical-property.md)) vorhanden sind, wird der Wert dieser Eigenschaft mithilfe der folgenden Formel neu berechnet und der alte Wert wird ignoriert.</span><span class="sxs-lookup"><span data-stu-id="f2716-115">If the **PR_DEFERRED_SEND_UNITS** ([PidTagDeferredSendUnits](pidtagdeferredsendunits-canonical-property.md)) and **PR_DEFERRED_SEND_NUMBER** ([PidTagDeferredSendNumber](pidtagdeferredsendnumber-canonical-property.md)) properties are present, the value of this property is recomputed by using the following formula and the old value is ignored.</span></span>
  
 <span data-ttu-id="f2716-116">**PR_DEFERRED_SEND_TIME** = **PR_CLIENT_SUBMIT_TIME** ([PidTagClientSubmitTime](pidtagclientsubmittime-canonical-property.md)) + **PR_DEFERRED_SEND_NUMBER** \* TimeOf (**PR_DEFERRED_SEND_UNITS**)</span><span class="sxs-lookup"><span data-stu-id="f2716-116">**PR_DEFERRED_SEND_TIME** = **PR_CLIENT_SUBMIT_TIME** ([PidTagClientSubmitTime](pidtagclientsubmittime-canonical-property.md)) + **PR_DEFERRED_SEND_NUMBER** \* TimeOf(**PR_DEFERRED_SEND_UNITS**)</span></span>
  
<span data-ttu-id="f2716-117">Wenn der **PR_DEFERRED_SEND_TIME** -Wert vor der aktuellen Uhrzeit (in UTC) liegt, wird die Nachricht sofort gesendet.</span><span class="sxs-lookup"><span data-stu-id="f2716-117">If **PR_DEFERRED_SEND_TIME** value is earlier than the current time (in UTC), the message is sent immediately.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="f2716-118">Zugehörige Ressourcen</span><span class="sxs-lookup"><span data-stu-id="f2716-118">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="f2716-119">Protokollspezifikationen</span><span class="sxs-lookup"><span data-stu-id="f2716-119">Protocol specifications</span></span>

<span data-ttu-id="f2716-120">[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="f2716-120">[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="f2716-121">Gibt die Eigenschaften und Vorgänge an, die für e-Mail-Nachrichtenobjekte zulässig sind.</span><span class="sxs-lookup"><span data-stu-id="f2716-121">Specifies the properties and operations that are permissible for email message objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="f2716-122">Header Dateien</span><span class="sxs-lookup"><span data-stu-id="f2716-122">Header files</span></span>

<span data-ttu-id="f2716-123">Mapidefs. h</span><span class="sxs-lookup"><span data-stu-id="f2716-123">Mapidefs.h</span></span>
  
> <span data-ttu-id="f2716-124">Stellt Datentypdefinitionen bereit.</span><span class="sxs-lookup"><span data-stu-id="f2716-124">Provides data type definitions.</span></span>
    
<span data-ttu-id="f2716-125">Mapitags. h</span><span class="sxs-lookup"><span data-stu-id="f2716-125">Mapitags.h</span></span>
  
> <span data-ttu-id="f2716-126">Enthält Definitionen von Eigenschaften, die als Alternative Namen aufgeführt sind.</span><span class="sxs-lookup"><span data-stu-id="f2716-126">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="f2716-127">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="f2716-127">See also</span></span>



[<span data-ttu-id="f2716-128">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="f2716-128">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="f2716-129">Kanonische MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="f2716-129">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="f2716-130">Zuordnen von kanonischen Eigenschaftennamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="f2716-130">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="f2716-131">Zuordnen von MAPI-Namen zu kanonischen Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="f2716-131">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

