---
title: PidTagProviderSubmitTime (kanonische Eigenschaft)
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
ms.openlocfilehash: e08b56fcfea38bf65e8628acfa481716554e2c01
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2018
ms.locfileid: "22571612"
---
# <a name="pidtagprovidersubmittime-canonical-property"></a><span data-ttu-id="3200a-103">PidTagProviderSubmitTime (kanonische Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="3200a-103">PidTagProviderSubmitTime Canonical Property</span></span>

  
  
<span data-ttu-id="3200a-104">**Betrifft**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="3200a-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="3200a-105">Enthält Datum und Uhrzeit, ein Transportdienstes eine Nachricht an die zugrunde liegenden messaging-System übergeben.</span><span class="sxs-lookup"><span data-stu-id="3200a-105">Contains the date and time a transport provider passed a message to its underlying messaging system.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="3200a-106">Zugeordnete Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="3200a-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="3200a-107">PR_PROVIDER_SUBMIT_TIME</span><span class="sxs-lookup"><span data-stu-id="3200a-107">PR_PROVIDER_SUBMIT_TIME</span></span>  <br/> |
|<span data-ttu-id="3200a-108">Kennung:</span><span class="sxs-lookup"><span data-stu-id="3200a-108">Identifier:</span></span>  <br/> |<span data-ttu-id="3200a-109">0x0048</span><span class="sxs-lookup"><span data-stu-id="3200a-109">0x0048</span></span>  <br/> |
|<span data-ttu-id="3200a-110">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="3200a-110">Data type:</span></span>  <br/> |<span data-ttu-id="3200a-111">PT_SYSTIME</span><span class="sxs-lookup"><span data-stu-id="3200a-111">PT_SYSTIME</span></span>  <br/> |
|<span data-ttu-id="3200a-112">Bereich:</span><span class="sxs-lookup"><span data-stu-id="3200a-112">Area:</span></span>  <br/> |<span data-ttu-id="3200a-113">MAPI-Umschlag</span><span class="sxs-lookup"><span data-stu-id="3200a-113">MAPI envelope</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="3200a-114">HinwBemerkungeneise</span><span class="sxs-lookup"><span data-stu-id="3200a-114">Remarks</span></span>

<span data-ttu-id="3200a-115">Diese Eigenschaft wird von der ausgehenden Adressbuchhierarchie zur Zeit festgelegt, die eine Nachricht gesendet wird.</span><span class="sxs-lookup"><span data-stu-id="3200a-115">This property is set by the outgoing transport provider at the time a message is sent.</span></span>
  
<span data-ttu-id="3200a-116">Diese Eigenschaft entspricht einem x. 400-Übermittlung Umschlag-Message-Attribut.</span><span class="sxs-lookup"><span data-stu-id="3200a-116">This property corresponds to an X.400 submission envelope per-message attribute.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="3200a-117">Verwandte Ressourcen</span><span class="sxs-lookup"><span data-stu-id="3200a-117">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="3200a-118">Header-Dateien</span><span class="sxs-lookup"><span data-stu-id="3200a-118">Header files</span></span>

<span data-ttu-id="3200a-119">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="3200a-119">Mapidefs.h</span></span>
  
> <span data-ttu-id="3200a-120">Enthält die Datentypdefinitionen.</span><span class="sxs-lookup"><span data-stu-id="3200a-120">Provides data type definitions.</span></span>
    
<span data-ttu-id="3200a-121">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="3200a-121">Mapitags.h</span></span>
  
> <span data-ttu-id="3200a-122">Enthält Definitionen von Eigenschaften, die als Alternative Namen aufgelistet.</span><span class="sxs-lookup"><span data-stu-id="3200a-122">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="3200a-123">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="3200a-123">See also</span></span>



[<span data-ttu-id="3200a-124">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="3200a-124">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="3200a-125">Kanonische MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="3200a-125">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="3200a-126">Zuordnen von kanonischen Eigenschaftennamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="3200a-126">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="3200a-127">Zuordnen von MAPI-Namen zu kanonische Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="3200a-127">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

