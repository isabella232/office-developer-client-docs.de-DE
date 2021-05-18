---
title: PidNameXSharingFlavor (kanonische Eigenschaft)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidNameXSharingFlavor
api_type:
- COM
ms.assetid: 7757fde1-564b-4f3a-9b9e-f80a143690ea
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: d2afa598bf9b7949f2e9142611570ebbd048f7e3
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32360886"
---
# <a name="pidnamexsharingflavor-canonical-property"></a><span data-ttu-id="7b153-103">PidNameXSharingFlavor (kanonische Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="7b153-103">PidNameXSharingFlavor Canonical Property</span></span>

  
  
<span data-ttu-id="7b153-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="7b153-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="7b153-105">Represents the value of the **dispidSharingFlavor** ([PidLidSharingFlavor](pidlidsharingflavor-canonical-property.md)) property.</span><span class="sxs-lookup"><span data-stu-id="7b153-105">Represents the value of the **dispidSharingFlavor** ([PidLidSharingFlavor](pidlidsharingflavor-canonical-property.md)) property.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="7b153-106">Anzeigenamen:</span><span class="sxs-lookup"><span data-stu-id="7b153-106">Friendly names:</span></span>  <br/> |<span data-ttu-id="7b153-107">Keine</span><span class="sxs-lookup"><span data-stu-id="7b153-107">None</span></span>  <br/> |
|<span data-ttu-id="7b153-108">Eigenschaftensatz:</span><span class="sxs-lookup"><span data-stu-id="7b153-108">Property set:</span></span>  <br/> |<span data-ttu-id="7b153-109">PS_INTERNET_HEADERS</span><span class="sxs-lookup"><span data-stu-id="7b153-109">PS_INTERNET_HEADERS</span></span>  <br/> |
|<span data-ttu-id="7b153-110">Eigenschaftsname:</span><span class="sxs-lookup"><span data-stu-id="7b153-110">Property name:</span></span>  <br/> |<span data-ttu-id="7b153-111">X-Sharing-Flavor</span><span class="sxs-lookup"><span data-stu-id="7b153-111">X-Sharing-Flavor</span></span>  <br/> |
|<span data-ttu-id="7b153-112">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="7b153-112">Data type:</span></span>  <br/> |<span data-ttu-id="7b153-113">PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="7b153-113">PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="7b153-114">Bereich:</span><span class="sxs-lookup"><span data-stu-id="7b153-114">Area:</span></span>  <br/> |<span data-ttu-id="7b153-115">Freigabe</span><span class="sxs-lookup"><span data-stu-id="7b153-115">Sharing</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="7b153-116">Hinweise</span><span class="sxs-lookup"><span data-stu-id="7b153-116">Remarks</span></span>

<span data-ttu-id="7b153-117">Die **dispidSharingFlavor-Eigenschaft** muss einer der folgenden Werte sein.</span><span class="sxs-lookup"><span data-stu-id="7b153-117">The **dispidSharingFlavor** property must be one of the following values.</span></span> 
  
|<span data-ttu-id="7b153-118">**Wert**</span><span class="sxs-lookup"><span data-stu-id="7b153-118">**Value**</span></span>|<span data-ttu-id="7b153-119">**Typ der Freigabenachricht**</span><span class="sxs-lookup"><span data-stu-id="7b153-119">**Type of Sharing Message**</span></span>|
|:-----|:-----|
|<span data-ttu-id="7b153-120">0x00020310</span><span class="sxs-lookup"><span data-stu-id="7b153-120">0x00020310</span></span>  <br/> |<span data-ttu-id="7b153-121">Eine Freigabeeinladung für einen speziellen Ordner.</span><span class="sxs-lookup"><span data-stu-id="7b153-121">A sharing invitation for a special folder.</span></span>  <br/> |
|<span data-ttu-id="7b153-122">0x00000310</span><span class="sxs-lookup"><span data-stu-id="7b153-122">0x00000310</span></span>  <br/> |<span data-ttu-id="7b153-123">Eine Freigabeeinladung für einen Ordner, der kein spezieller Ordner ist.</span><span class="sxs-lookup"><span data-stu-id="7b153-123">A sharing invitation for a folder that is not a special folder.</span></span>  <br/> |
|<span data-ttu-id="7b153-124">0x00020500</span><span class="sxs-lookup"><span data-stu-id="7b153-124">0x00020500</span></span>  <br/> |<span data-ttu-id="7b153-125">Eine Freigabeanforderung.</span><span class="sxs-lookup"><span data-stu-id="7b153-125">A sharing request.</span></span>  <br/> |
|<span data-ttu-id="7b153-126">0x00020710</span><span class="sxs-lookup"><span data-stu-id="7b153-126">0x00020710</span></span>  <br/> |<span data-ttu-id="7b153-127">Sowohl eine Freigabeeinladung für einen speziellen Ordner als auch eine Freigabeanforderung für den entsprechenden speziellen Ordner des Empfängers.</span><span class="sxs-lookup"><span data-stu-id="7b153-127">Both a sharing invitation for a special folder and a sharing request for the recipient's equivalent special folder.</span></span>  <br/> |
|<span data-ttu-id="7b153-128">0x00025100</span><span class="sxs-lookup"><span data-stu-id="7b153-128">0x00025100</span></span>  <br/> |<span data-ttu-id="7b153-129">Eine Freigabeantwort, die eine Anforderung verweigert.</span><span class="sxs-lookup"><span data-stu-id="7b153-129">A sharing response that denies a request.</span></span>  <br/> |
|<span data-ttu-id="7b153-130">0x00023310</span><span class="sxs-lookup"><span data-stu-id="7b153-130">0x00023310</span></span>  <br/> |<span data-ttu-id="7b153-131">Eine Freigabeantwort, die eine Anforderung akzeptiert (auch eine Art von Freigabeeinladung).</span><span class="sxs-lookup"><span data-stu-id="7b153-131">A sharing response that accepts a request (also a type of sharing invitation).</span></span>  <br/> |
   
## <a name="related-resources"></a><span data-ttu-id="7b153-132">Verwandte Ressourcen</span><span class="sxs-lookup"><span data-stu-id="7b153-132">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="7b153-133">Protokollspezifikationen</span><span class="sxs-lookup"><span data-stu-id="7b153-133">Protocol specifications</span></span>

<span data-ttu-id="7b153-134">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="7b153-134">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="7b153-135">Stellt Eigenschaftensatzdefinitionen und Verweise auf verwandte Exchange Server zur Verfügung.</span><span class="sxs-lookup"><span data-stu-id="7b153-135">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="7b153-136">[[MS-OXSHARE]](https://msdn.microsoft.com/library/e4e5bd27-d5e0-43f9-a6ea-550876724f3d%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="7b153-136">[[MS-OXSHARE]](https://msdn.microsoft.com/library/e4e5bd27-d5e0-43f9-a6ea-550876724f3d%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="7b153-137">Gibt Postfachordner zwischen Clients zurück.</span><span class="sxs-lookup"><span data-stu-id="7b153-137">Shares mailbox folders between clients.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="7b153-138">Headerdateien</span><span class="sxs-lookup"><span data-stu-id="7b153-138">Header files</span></span>

<span data-ttu-id="7b153-139">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="7b153-139">Mapidefs.h</span></span>
  
> <span data-ttu-id="7b153-140">Bietet Datentypdefinitionen.</span><span class="sxs-lookup"><span data-stu-id="7b153-140">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="7b153-141">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="7b153-141">See also</span></span>



[<span data-ttu-id="7b153-142">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="7b153-142">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="7b153-143">KANONISCHE EIGENSCHAFTEN VON MAPI</span><span class="sxs-lookup"><span data-stu-id="7b153-143">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="7b153-144">Zuordnen kanonischer Eigenschaftsnamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="7b153-144">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="7b153-145">Zuordnen von MAPI-Namen zu kanonischen Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="7b153-145">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

