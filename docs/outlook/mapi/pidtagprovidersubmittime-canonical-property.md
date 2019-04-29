---
title: Kanonische Pidtagprovidersubmittime (-Eigenschaft
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagProviderSubmitTime
api_type:
- COM
ms.assetid: 9e5161d9-fefe-4a12-b7f7-5600f1d2e95b
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: c5e840250da7ba3b95150f2e83e1eb08b0c61ab5
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33409020"
---
# <a name="pidtagprovidersubmittime-canonical-property"></a><span data-ttu-id="653c9-103">Kanonische Pidtagprovidersubmittime (-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="653c9-103">PidTagProviderSubmitTime Canonical Property</span></span>

  
  
<span data-ttu-id="653c9-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="653c9-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="653c9-105">Enthält das Datum und die Uhrzeit, zu denen ein Transportanbieter eine Nachricht an das zugrunde liegende Messagingsystem übergeben hat.</span><span class="sxs-lookup"><span data-stu-id="653c9-105">Contains the date and time a transport provider passed a message to its underlying messaging system.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="653c9-106">Zugeordnete Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="653c9-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="653c9-107">PR_PROVIDER_SUBMIT_TIME</span><span class="sxs-lookup"><span data-stu-id="653c9-107">PR_PROVIDER_SUBMIT_TIME</span></span>  <br/> |
|<span data-ttu-id="653c9-108">Kennung:</span><span class="sxs-lookup"><span data-stu-id="653c9-108">Identifier:</span></span>  <br/> |<span data-ttu-id="653c9-109">0x0048</span><span class="sxs-lookup"><span data-stu-id="653c9-109">0x0048</span></span>  <br/> |
|<span data-ttu-id="653c9-110">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="653c9-110">Data type:</span></span>  <br/> |<span data-ttu-id="653c9-111">PT_SYSTIME</span><span class="sxs-lookup"><span data-stu-id="653c9-111">PT_SYSTIME</span></span>  <br/> |
|<span data-ttu-id="653c9-112">Bereich:</span><span class="sxs-lookup"><span data-stu-id="653c9-112">Area:</span></span>  <br/> |<span data-ttu-id="653c9-113">MAPI-Umschlag</span><span class="sxs-lookup"><span data-stu-id="653c9-113">MAPI envelope</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="653c9-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="653c9-114">Remarks</span></span>

<span data-ttu-id="653c9-115">Diese Eigenschaft wird vom ausgehenden Transportanbieter festgelegt, wenn eine Nachricht gesendet wird.</span><span class="sxs-lookup"><span data-stu-id="653c9-115">This property is set by the outgoing transport provider at the time a message is sent.</span></span>
  
<span data-ttu-id="653c9-116">Diese Eigenschaft entspricht einem X. 400-Übermittlungs Umschlag pro Nachrichtenattribut.</span><span class="sxs-lookup"><span data-stu-id="653c9-116">This property corresponds to an X.400 submission envelope per-message attribute.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="653c9-117">Verwandte Ressourcen</span><span class="sxs-lookup"><span data-stu-id="653c9-117">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="653c9-118">Header Dateien</span><span class="sxs-lookup"><span data-stu-id="653c9-118">Header files</span></span>

<span data-ttu-id="653c9-119">Mapidefs. h</span><span class="sxs-lookup"><span data-stu-id="653c9-119">Mapidefs.h</span></span>
  
> <span data-ttu-id="653c9-120">Stellt Datentypdefinitionen bereit.</span><span class="sxs-lookup"><span data-stu-id="653c9-120">Provides data type definitions.</span></span>
    
<span data-ttu-id="653c9-121">Mapitags. h</span><span class="sxs-lookup"><span data-stu-id="653c9-121">Mapitags.h</span></span>
  
> <span data-ttu-id="653c9-122">Enthält Definitionen von Eigenschaften, die als Alternative Namen aufgeführt sind.</span><span class="sxs-lookup"><span data-stu-id="653c9-122">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="653c9-123">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="653c9-123">See also</span></span>



[<span data-ttu-id="653c9-124">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="653c9-124">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="653c9-125">Kanonische MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="653c9-125">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="653c9-126">Zuordnen von kanonischen Eigenschaftennamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="653c9-126">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="653c9-127">Zuordnen von MAPI-Namen zu kanonischen Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="653c9-127">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

