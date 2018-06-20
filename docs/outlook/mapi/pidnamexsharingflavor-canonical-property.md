---
title: Kanonische PidNameXSharingFlavor-Eigenschaft
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
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: 1f07a11c47c6785bc9a166f11bde8f2e5ef464a0
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19794009"
---
# <a name="pidnamexsharingflavor-canonical-property"></a><span data-ttu-id="c8be5-103">Kanonische PidNameXSharingFlavor-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="c8be5-103">PidNameXSharingFlavor Canonical Property</span></span>

  
  
<span data-ttu-id="c8be5-104">**Betrifft**: Outlook</span><span class="sxs-lookup"><span data-stu-id="c8be5-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="c8be5-105">Stellt den Wert der Eigenschaft **DispidSharingFlavor** ([PidLidSharingFlavor](pidlidsharingflavor-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="c8be5-105">Represents the value of the **dispidSharingFlavor** ([PidLidSharingFlavor](pidlidsharingflavor-canonical-property.md)) property.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="c8be5-106">Anzeigenamen:</span><span class="sxs-lookup"><span data-stu-id="c8be5-106">Friendly names:</span></span>  <br/> |<span data-ttu-id="c8be5-107">Keine</span><span class="sxs-lookup"><span data-stu-id="c8be5-107">None</span></span>  <br/> |
|<span data-ttu-id="c8be5-108">-Eigenschaft festgelegt:</span><span class="sxs-lookup"><span data-stu-id="c8be5-108">Property set:</span></span>  <br/> |<span data-ttu-id="c8be5-109">PS_INTERNET_HEADERS</span><span class="sxs-lookup"><span data-stu-id="c8be5-109">PS_INTERNET_HEADERS</span></span>  <br/> |
|<span data-ttu-id="c8be5-110">Name der Eigenschaft:</span><span class="sxs-lookup"><span data-stu-id="c8be5-110">Property name:</span></span>  <br/> |<span data-ttu-id="c8be5-111">X-Freigabe-Typ</span><span class="sxs-lookup"><span data-stu-id="c8be5-111">X-Sharing-Flavor</span></span>  <br/> |
|<span data-ttu-id="c8be5-112">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="c8be5-112">Data type:</span></span>  <br/> |<span data-ttu-id="c8be5-113">PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="c8be5-113">PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="c8be5-114">Bereich:</span><span class="sxs-lookup"><span data-stu-id="c8be5-114">Area:</span></span>  <br/> |<span data-ttu-id="c8be5-115">Freigabe</span><span class="sxs-lookup"><span data-stu-id="c8be5-115">Sharing</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="c8be5-116">Hinweise</span><span class="sxs-lookup"><span data-stu-id="c8be5-116">Remarks</span></span>

<span data-ttu-id="c8be5-117">Die **DispidSharingFlavor** -Eigenschaft muss eine der folgenden Werte sein:</span><span class="sxs-lookup"><span data-stu-id="c8be5-117">The **dispidSharingFlavor** property must be one of the following values.</span></span> 
  
|<span data-ttu-id="c8be5-118">**Wert**</span><span class="sxs-lookup"><span data-stu-id="c8be5-118">**Value**</span></span>|<span data-ttu-id="c8be5-119">**Freigabenachrichtentyp**</span><span class="sxs-lookup"><span data-stu-id="c8be5-119">**Type of Sharing Message**</span></span>|
|:-----|:-----|
|<span data-ttu-id="c8be5-120">0x00020310</span><span class="sxs-lookup"><span data-stu-id="c8be5-120">0x00020310</span></span>  <br/> |<span data-ttu-id="c8be5-121">Eine freigabeeinladung für einen Ordner mit Sonderfunktion.</span><span class="sxs-lookup"><span data-stu-id="c8be5-121">A sharing invitation for a special folder.</span></span>  <br/> |
|<span data-ttu-id="c8be5-122">0x00000310</span><span class="sxs-lookup"><span data-stu-id="c8be5-122">0x00000310</span></span>  <br/> |<span data-ttu-id="c8be5-123">Eine freigabeeinladung für einen Ordner, der nicht auf einen Ordner mit Sonderfunktion ist.</span><span class="sxs-lookup"><span data-stu-id="c8be5-123">A sharing invitation for a folder that is not a special folder.</span></span>  <br/> |
|<span data-ttu-id="c8be5-124">0x00020500</span><span class="sxs-lookup"><span data-stu-id="c8be5-124">0x00020500</span></span>  <br/> |<span data-ttu-id="c8be5-125">Eine Freigabeanfrage.</span><span class="sxs-lookup"><span data-stu-id="c8be5-125">A sharing request.</span></span>  <br/> |
|<span data-ttu-id="c8be5-126">0x00020710</span><span class="sxs-lookup"><span data-stu-id="c8be5-126">0x00020710</span></span>  <br/> |<span data-ttu-id="c8be5-127">Sowohl eine freigabeeinladung für einen Ordner mit Sonderfunktion und eine Freigabeanfrage für entsprechende Spezialordner des Empfängers.</span><span class="sxs-lookup"><span data-stu-id="c8be5-127">Both a sharing invitation for a special folder and a sharing request for the recipient's equivalent special folder.</span></span>  <br/> |
|<span data-ttu-id="c8be5-128">0x00025100</span><span class="sxs-lookup"><span data-stu-id="c8be5-128">0x00025100</span></span>  <br/> |<span data-ttu-id="c8be5-129">Eine Freigabeantwort, die eine Anforderung verweigert.</span><span class="sxs-lookup"><span data-stu-id="c8be5-129">A sharing response that denies a request.</span></span>  <br/> |
|<span data-ttu-id="c8be5-130">0x00023310</span><span class="sxs-lookup"><span data-stu-id="c8be5-130">0x00023310</span></span>  <br/> |<span data-ttu-id="c8be5-131">Eine Freigabeantwort, die eine Anforderung (auch eine Art der Einladung zur Freigabe) akzeptiert.</span><span class="sxs-lookup"><span data-stu-id="c8be5-131">A sharing response that accepts a request (also a type of sharing invitation).</span></span>  <br/> |
   
## <a name="related-resources"></a><span data-ttu-id="c8be5-132">Verwandte Ressourcen</span><span class="sxs-lookup"><span data-stu-id="c8be5-132">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="c8be5-133">Protokollspezifikationen</span><span class="sxs-lookup"><span data-stu-id="c8be5-133">Protocol specifications</span></span>

<span data-ttu-id="c8be5-134">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="c8be5-134">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="c8be5-135">Enthält Eigenschaftendefinitionen und Verweise auf Verwandte Exchange Server-Spezifikationen.</span><span class="sxs-lookup"><span data-stu-id="c8be5-135">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="c8be5-136">[[MS-OXSHARE]](http://msdn.microsoft.com/library/e4e5bd27-d5e0-43f9-a6ea-550876724f3d%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="c8be5-136">[[MS-OXSHARE]](http://msdn.microsoft.com/library/e4e5bd27-d5e0-43f9-a6ea-550876724f3d%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="c8be5-137">Teilt Postfachordner zwischen Clients.</span><span class="sxs-lookup"><span data-stu-id="c8be5-137">Shares mailbox folders between clients.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="c8be5-138">Header-Dateien</span><span class="sxs-lookup"><span data-stu-id="c8be5-138">Header files</span></span>

<span data-ttu-id="c8be5-139">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="c8be5-139">Mapidefs.h</span></span>
  
> <span data-ttu-id="c8be5-140">Enthält die Datentypdefinitionen.</span><span class="sxs-lookup"><span data-stu-id="c8be5-140">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="c8be5-141">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="c8be5-141">See also</span></span>



[<span data-ttu-id="c8be5-142">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="c8be5-142">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="c8be5-143">Kanonische MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="c8be5-143">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="c8be5-144">Zuordnen von kanonischen Eigenschaftennamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="c8be5-144">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="c8be5-145">Zuordnen von MAPI-Namen zu kanonische Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="c8be5-145">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

