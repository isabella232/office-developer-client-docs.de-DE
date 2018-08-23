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
ms.openlocfilehash: bcdca783778e1a310be638ce376d408acf0b247f
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2018
ms.locfileid: "22580040"
---
# <a name="pidnamexsharingflavor-canonical-property"></a><span data-ttu-id="190bc-103">PidNameXSharingFlavor (kanonische Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="190bc-103">PidNameXSharingFlavor Canonical Property</span></span>

  
  
<span data-ttu-id="190bc-104">**Betrifft**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="190bc-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="190bc-105">Stellt den Wert der Eigenschaft **DispidSharingFlavor** ([PidLidSharingFlavor](pidlidsharingflavor-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="190bc-105">Represents the value of the **dispidSharingFlavor** ([PidLidSharingFlavor](pidlidsharingflavor-canonical-property.md)) property.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="190bc-106">Anzeigenamen:</span><span class="sxs-lookup"><span data-stu-id="190bc-106">Friendly names:</span></span>  <br/> |<span data-ttu-id="190bc-107">Keine</span><span class="sxs-lookup"><span data-stu-id="190bc-107">None</span></span>  <br/> |
|<span data-ttu-id="190bc-108">-Eigenschaft festgelegt:</span><span class="sxs-lookup"><span data-stu-id="190bc-108">Property set:</span></span>  <br/> |<span data-ttu-id="190bc-109">PS_INTERNET_HEADERS</span><span class="sxs-lookup"><span data-stu-id="190bc-109">PS_INTERNET_HEADERS</span></span>  <br/> |
|<span data-ttu-id="190bc-110">Name der Eigenschaft:</span><span class="sxs-lookup"><span data-stu-id="190bc-110">Property name:</span></span>  <br/> |<span data-ttu-id="190bc-111">X-Freigabe-Typ</span><span class="sxs-lookup"><span data-stu-id="190bc-111">X-Sharing-Flavor</span></span>  <br/> |
|<span data-ttu-id="190bc-112">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="190bc-112">Data type:</span></span>  <br/> |<span data-ttu-id="190bc-113">PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="190bc-113">PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="190bc-114">Bereich:</span><span class="sxs-lookup"><span data-stu-id="190bc-114">Area:</span></span>  <br/> |<span data-ttu-id="190bc-115">Freigabe</span><span class="sxs-lookup"><span data-stu-id="190bc-115">Sharing</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="190bc-116">HinwBemerkungeneise</span><span class="sxs-lookup"><span data-stu-id="190bc-116">Remarks</span></span>

<span data-ttu-id="190bc-117">Die **DispidSharingFlavor** -Eigenschaft muss eine der folgenden Werte sein:</span><span class="sxs-lookup"><span data-stu-id="190bc-117">The **dispidSharingFlavor** property must be one of the following values.</span></span> 
  
|<span data-ttu-id="190bc-118">**Wert**</span><span class="sxs-lookup"><span data-stu-id="190bc-118">**Value**</span></span>|<span data-ttu-id="190bc-119">**Freigabenachrichtentyp**</span><span class="sxs-lookup"><span data-stu-id="190bc-119">**Type of Sharing Message**</span></span>|
|:-----|:-----|
|<span data-ttu-id="190bc-120">0x00020310</span><span class="sxs-lookup"><span data-stu-id="190bc-120">0x00020310</span></span>  <br/> |<span data-ttu-id="190bc-121">Eine freigabeeinladung für einen Ordner mit Sonderfunktion.</span><span class="sxs-lookup"><span data-stu-id="190bc-121">A sharing invitation for a special folder.</span></span>  <br/> |
|<span data-ttu-id="190bc-122">0x00000310</span><span class="sxs-lookup"><span data-stu-id="190bc-122">0x00000310</span></span>  <br/> |<span data-ttu-id="190bc-123">Eine freigabeeinladung für einen Ordner, der nicht auf einen Ordner mit Sonderfunktion ist.</span><span class="sxs-lookup"><span data-stu-id="190bc-123">A sharing invitation for a folder that is not a special folder.</span></span>  <br/> |
|<span data-ttu-id="190bc-124">0x00020500</span><span class="sxs-lookup"><span data-stu-id="190bc-124">0x00020500</span></span>  <br/> |<span data-ttu-id="190bc-125">Eine Freigabeanfrage.</span><span class="sxs-lookup"><span data-stu-id="190bc-125">A sharing request.</span></span>  <br/> |
|<span data-ttu-id="190bc-126">0x00020710</span><span class="sxs-lookup"><span data-stu-id="190bc-126">0x00020710</span></span>  <br/> |<span data-ttu-id="190bc-127">Sowohl eine freigabeeinladung für einen Ordner mit Sonderfunktion und eine Freigabeanfrage für entsprechende Spezialordner des Empfängers.</span><span class="sxs-lookup"><span data-stu-id="190bc-127">Both a sharing invitation for a special folder and a sharing request for the recipient's equivalent special folder.</span></span>  <br/> |
|<span data-ttu-id="190bc-128">0x00025100</span><span class="sxs-lookup"><span data-stu-id="190bc-128">0x00025100</span></span>  <br/> |<span data-ttu-id="190bc-129">Eine Freigabeantwort, die eine Anforderung verweigert.</span><span class="sxs-lookup"><span data-stu-id="190bc-129">A sharing response that denies a request.</span></span>  <br/> |
|<span data-ttu-id="190bc-130">0x00023310</span><span class="sxs-lookup"><span data-stu-id="190bc-130">0x00023310</span></span>  <br/> |<span data-ttu-id="190bc-131">Eine Freigabeantwort, die eine Anforderung (auch eine Art der Einladung zur Freigabe) akzeptiert.</span><span class="sxs-lookup"><span data-stu-id="190bc-131">A sharing response that accepts a request (also a type of sharing invitation).</span></span>  <br/> |
   
## <a name="related-resources"></a><span data-ttu-id="190bc-132">Verwandte Ressourcen</span><span class="sxs-lookup"><span data-stu-id="190bc-132">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="190bc-133">Protokollspezifikationen</span><span class="sxs-lookup"><span data-stu-id="190bc-133">Protocol specifications</span></span>

<span data-ttu-id="190bc-134">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="190bc-134">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="190bc-135">Enthält Eigenschaftendefinitionen und Verweise auf Verwandte Exchange Server-Spezifikationen.</span><span class="sxs-lookup"><span data-stu-id="190bc-135">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="190bc-136">[[MS-OXSHARE]](http://msdn.microsoft.com/library/e4e5bd27-d5e0-43f9-a6ea-550876724f3d%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="190bc-136">[[MS-OXSHARE]](http://msdn.microsoft.com/library/e4e5bd27-d5e0-43f9-a6ea-550876724f3d%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="190bc-137">Teilt Postfachordner zwischen Clients.</span><span class="sxs-lookup"><span data-stu-id="190bc-137">Shares mailbox folders between clients.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="190bc-138">Header-Dateien</span><span class="sxs-lookup"><span data-stu-id="190bc-138">Header files</span></span>

<span data-ttu-id="190bc-139">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="190bc-139">Mapidefs.h</span></span>
  
> <span data-ttu-id="190bc-140">Enthält die Datentypdefinitionen.</span><span class="sxs-lookup"><span data-stu-id="190bc-140">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="190bc-141">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="190bc-141">See also</span></span>



[<span data-ttu-id="190bc-142">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="190bc-142">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="190bc-143">Kanonische MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="190bc-143">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="190bc-144">Zuordnen von kanonischen Eigenschaftennamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="190bc-144">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="190bc-145">Zuordnen von MAPI-Namen zu kanonische Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="190bc-145">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

