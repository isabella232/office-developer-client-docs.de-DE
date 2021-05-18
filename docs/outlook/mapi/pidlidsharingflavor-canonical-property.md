---
title: PidLidSharingFlavor (kanonische Eigenschaft)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidSharingFlavor
api_type:
- COM
ms.assetid: c91ab5c7-82ac-4895-bf54-2863ca5e2410
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 21144af15e7a36f54af3032f735c391b3038305b
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32327482"
---
# <a name="pidlidsharingflavor-canonical-property"></a><span data-ttu-id="0bc71-103">PidLidSharingFlavor (kanonische Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="0bc71-103">PidLidSharingFlavor Canonical Property</span></span>

  
  
<span data-ttu-id="0bc71-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="0bc71-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="0bc71-105">Wird als Eigenschaft einer Freigabenachricht bestimmt.</span><span class="sxs-lookup"><span data-stu-id="0bc71-105">Designates as a property of a sharing message.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="0bc71-106">Zugeordnete Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="0bc71-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="0bc71-107">dispidSharingFlavor</span><span class="sxs-lookup"><span data-stu-id="0bc71-107">dispidSharingFlavor</span></span>  <br/> |
|<span data-ttu-id="0bc71-108">Eigenschaftensatz:</span><span class="sxs-lookup"><span data-stu-id="0bc71-108">Property set:</span></span>  <br/> |<span data-ttu-id="0bc71-109">PSETID_Sharing</span><span class="sxs-lookup"><span data-stu-id="0bc71-109">PSETID_Sharing</span></span>  <br/> |
|<span data-ttu-id="0bc71-110">Lange ID (LID):</span><span class="sxs-lookup"><span data-stu-id="0bc71-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="0bc71-111">0x00008A18</span><span class="sxs-lookup"><span data-stu-id="0bc71-111">0x00008A18</span></span>  <br/> |
|<span data-ttu-id="0bc71-112">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="0bc71-112">Data type:</span></span>  <br/> |<span data-ttu-id="0bc71-113">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="0bc71-113">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="0bc71-114">Bereich:</span><span class="sxs-lookup"><span data-stu-id="0bc71-114">Area:</span></span>  <br/> |<span data-ttu-id="0bc71-115">Freigabe</span><span class="sxs-lookup"><span data-stu-id="0bc71-115">Sharing</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="0bc71-116">Hinweise</span><span class="sxs-lookup"><span data-stu-id="0bc71-116">Remarks</span></span>

<span data-ttu-id="0bc71-117">Der Wert dieser Eigenschaft muss einer der folgenden Sein:</span><span class="sxs-lookup"><span data-stu-id="0bc71-117">The value of this property must be one of the following:</span></span>
  
|<span data-ttu-id="0bc71-118">**Wert**</span><span class="sxs-lookup"><span data-stu-id="0bc71-118">**Value**</span></span>|<span data-ttu-id="0bc71-119">**Typ des Sharing Message-Objekts**</span><span class="sxs-lookup"><span data-stu-id="0bc71-119">**Type of Sharing Message object**</span></span>|
|:-----|:-----|
|<span data-ttu-id="0bc71-120">0x00020310</span><span class="sxs-lookup"><span data-stu-id="0bc71-120">0x00020310</span></span>  <br/> |<span data-ttu-id="0bc71-121">Eine Freigabeeinladung für einen speziellen Ordner.</span><span class="sxs-lookup"><span data-stu-id="0bc71-121">A sharing invitation for a special folder.</span></span>  <br/> |
|<span data-ttu-id="0bc71-122">0x00000310</span><span class="sxs-lookup"><span data-stu-id="0bc71-122">0x00000310</span></span>  <br/> |<span data-ttu-id="0bc71-123">Eine Freigabeeinladung für einen Ordner, der kein spezieller Ordner ist.</span><span class="sxs-lookup"><span data-stu-id="0bc71-123">A sharing invitation for a folder that is not a special folder.</span></span>  <br/> |
|<span data-ttu-id="0bc71-124">0x00020500</span><span class="sxs-lookup"><span data-stu-id="0bc71-124">0x00020500</span></span>  <br/> |<span data-ttu-id="0bc71-125">Eine Freigabeanforderung.</span><span class="sxs-lookup"><span data-stu-id="0bc71-125">A sharing request.</span></span>  <br/> |
|<span data-ttu-id="0bc71-126">0x00020710</span><span class="sxs-lookup"><span data-stu-id="0bc71-126">0x00020710</span></span>  <br/> |<span data-ttu-id="0bc71-127">Sowohl eine Freigabeeinladung für einen speziellen Ordner als auch eine Freigabeanforderung für den entsprechenden speziellen Ordner des Empfängers.</span><span class="sxs-lookup"><span data-stu-id="0bc71-127">Both a sharing invitation for a special folder and a sharing request for the recipient's equivalent special folder.</span></span>  <br/> |
|<span data-ttu-id="0bc71-128">0x00025100</span><span class="sxs-lookup"><span data-stu-id="0bc71-128">0x00025100</span></span>  <br/> |<span data-ttu-id="0bc71-129">Eine Freigabeantwort, die eine Anforderung verweigert.</span><span class="sxs-lookup"><span data-stu-id="0bc71-129">A sharing response denying a request.</span></span>  <br/> |
|<span data-ttu-id="0bc71-130">0x00023310</span><span class="sxs-lookup"><span data-stu-id="0bc71-130">0x00023310</span></span>  <br/> |<span data-ttu-id="0bc71-131">Eine Freigabeantwort, die eine Anforderung akzeptiert (auch eine Art von Freigabeeinladung).</span><span class="sxs-lookup"><span data-stu-id="0bc71-131">A sharing response accepting a request (also a type of sharing invitation).</span></span>  <br/> |
   
## <a name="related-resources"></a><span data-ttu-id="0bc71-132">Verwandte Ressourcen</span><span class="sxs-lookup"><span data-stu-id="0bc71-132">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="0bc71-133">Protokollspezifikationen</span><span class="sxs-lookup"><span data-stu-id="0bc71-133">Protocol specifications</span></span>

<span data-ttu-id="0bc71-134">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="0bc71-134">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="0bc71-135">Stellt Eigenschaftensatzdefinitionen und Verweise auf verwandte Exchange Server zur Verfügung.</span><span class="sxs-lookup"><span data-stu-id="0bc71-135">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="0bc71-136">[[MS-OXSHARE]](https://msdn.microsoft.com/library/e4e5bd27-d5e0-43f9-a6ea-550876724f3d%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="0bc71-136">[[MS-OXSHARE]](https://msdn.microsoft.com/library/e4e5bd27-d5e0-43f9-a6ea-550876724f3d%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="0bc71-137">Gibt Postfachordner zwischen Clients zurück.</span><span class="sxs-lookup"><span data-stu-id="0bc71-137">Shares mailbox folders between clients.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="0bc71-138">Headerdateien</span><span class="sxs-lookup"><span data-stu-id="0bc71-138">Header files</span></span>

<span data-ttu-id="0bc71-139">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="0bc71-139">Mapidefs.h</span></span>
  
> <span data-ttu-id="0bc71-140">Bietet Datentypdefinitionen.</span><span class="sxs-lookup"><span data-stu-id="0bc71-140">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="0bc71-141">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="0bc71-141">See also</span></span>



[<span data-ttu-id="0bc71-142">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="0bc71-142">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="0bc71-143">KANONISCHE EIGENSCHAFTEN VON MAPI</span><span class="sxs-lookup"><span data-stu-id="0bc71-143">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="0bc71-144">Zuordnen kanonischer Eigenschaftsnamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="0bc71-144">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="0bc71-145">Zuordnen von MAPI-Namen zu kanonischen Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="0bc71-145">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

