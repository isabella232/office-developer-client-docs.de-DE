---
title: Kanonische PidTagProviderSubmitTime-Eigenschaft
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
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: 162451d000c0b3da42c8fbef5f64459bc5ae23b1
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19794846"
---
# <a name="pidtagprovidersubmittime-canonical-property"></a><span data-ttu-id="c18d0-103">Kanonische PidTagProviderSubmitTime-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="c18d0-103">PidTagProviderSubmitTime Canonical Property</span></span>

  
  
<span data-ttu-id="c18d0-104">**Betrifft**: Outlook</span><span class="sxs-lookup"><span data-stu-id="c18d0-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="c18d0-105">Enthält Datum und Uhrzeit, ein Transportdienstes eine Nachricht an die zugrunde liegenden messaging-System übergeben.</span><span class="sxs-lookup"><span data-stu-id="c18d0-105">Contains the date and time a transport provider passed a message to its underlying messaging system.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="c18d0-106">Zugeordneten Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="c18d0-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="c18d0-107">PR_PROVIDER_SUBMIT_TIME</span><span class="sxs-lookup"><span data-stu-id="c18d0-107">PR_PROVIDER_SUBMIT_TIME</span></span>  <br/> |
|<span data-ttu-id="c18d0-108">Bezeichner:</span><span class="sxs-lookup"><span data-stu-id="c18d0-108">Identifier:</span></span>  <br/> |<span data-ttu-id="c18d0-109">0x0048</span><span class="sxs-lookup"><span data-stu-id="c18d0-109">0x0048</span></span>  <br/> |
|<span data-ttu-id="c18d0-110">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="c18d0-110">Data type:</span></span>  <br/> |<span data-ttu-id="c18d0-111">PT_SYSTIME</span><span class="sxs-lookup"><span data-stu-id="c18d0-111">PT_SYSTIME</span></span>  <br/> |
|<span data-ttu-id="c18d0-112">Bereich:</span><span class="sxs-lookup"><span data-stu-id="c18d0-112">Area:</span></span>  <br/> |<span data-ttu-id="c18d0-113">MAPI-Umschlag</span><span class="sxs-lookup"><span data-stu-id="c18d0-113">MAPI envelope</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="c18d0-114">Hinweise</span><span class="sxs-lookup"><span data-stu-id="c18d0-114">Remarks</span></span>

<span data-ttu-id="c18d0-115">Diese Eigenschaft wird von der ausgehenden Adressbuchhierarchie zur Zeit festgelegt, die eine Nachricht gesendet wird.</span><span class="sxs-lookup"><span data-stu-id="c18d0-115">This property is set by the outgoing transport provider at the time a message is sent.</span></span>
  
<span data-ttu-id="c18d0-116">Diese Eigenschaft entspricht einem x. 400-Übermittlung Umschlag-Message-Attribut.</span><span class="sxs-lookup"><span data-stu-id="c18d0-116">This property corresponds to an X.400 submission envelope per-message attribute.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="c18d0-117">Verwandte Ressourcen</span><span class="sxs-lookup"><span data-stu-id="c18d0-117">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="c18d0-118">Header-Dateien</span><span class="sxs-lookup"><span data-stu-id="c18d0-118">Header files</span></span>

<span data-ttu-id="c18d0-119">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="c18d0-119">Mapidefs.h</span></span>
  
> <span data-ttu-id="c18d0-120">Enthält die Datentypdefinitionen.</span><span class="sxs-lookup"><span data-stu-id="c18d0-120">Provides data type definitions.</span></span>
    
<span data-ttu-id="c18d0-121">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="c18d0-121">Mapitags.h</span></span>
  
> <span data-ttu-id="c18d0-122">Enthält Definitionen von Eigenschaften, die als Alternative Namen aufgelistet.</span><span class="sxs-lookup"><span data-stu-id="c18d0-122">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="c18d0-123">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="c18d0-123">See also</span></span>



[<span data-ttu-id="c18d0-124">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="c18d0-124">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="c18d0-125">Kanonische MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="c18d0-125">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="c18d0-126">Zuordnen von kanonischen Eigenschaftennamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="c18d0-126">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="c18d0-127">Zuordnen von MAPI-Namen zu kanonische Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="c18d0-127">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

