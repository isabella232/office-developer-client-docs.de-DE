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
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/04/2018
ms.locfileid: "25383611"
---
# <a name="pidlidsharingflavor-canonical-property"></a><span data-ttu-id="96ac7-103">PidLidSharingFlavor (kanonische Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="96ac7-103">PidLidSharingFlavor Canonical Property</span></span>

  
  
<span data-ttu-id="96ac7-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="96ac7-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="96ac7-105">Legt fest, wie eine eine Freigabenachricht-Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="96ac7-105">Designates as a property of a sharing message.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="96ac7-106">Zugeordnete Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="96ac7-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="96ac7-107">dispidSharingFlavor</span><span class="sxs-lookup"><span data-stu-id="96ac7-107">dispidSharingFlavor</span></span>  <br/> |
|<span data-ttu-id="96ac7-108">-Eigenschaft festgelegt:</span><span class="sxs-lookup"><span data-stu-id="96ac7-108">Property set:</span></span>  <br/> |<span data-ttu-id="96ac7-109">PSETID_Sharing</span><span class="sxs-lookup"><span data-stu-id="96ac7-109">PSETID_Sharing</span></span>  <br/> |
|<span data-ttu-id="96ac7-110">Long-ID (Abdeckung):</span><span class="sxs-lookup"><span data-stu-id="96ac7-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="96ac7-111">0x00008A18</span><span class="sxs-lookup"><span data-stu-id="96ac7-111">0x00008A18</span></span>  <br/> |
|<span data-ttu-id="96ac7-112">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="96ac7-112">Data type:</span></span>  <br/> |<span data-ttu-id="96ac7-113">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="96ac7-113">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="96ac7-114">Bereich:</span><span class="sxs-lookup"><span data-stu-id="96ac7-114">Area:</span></span>  <br/> |<span data-ttu-id="96ac7-115">Freigabe</span><span class="sxs-lookup"><span data-stu-id="96ac7-115">Sharing</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="96ac7-116">Hinweise</span><span class="sxs-lookup"><span data-stu-id="96ac7-116">Remarks</span></span>

<span data-ttu-id="96ac7-117">Der Wert dieser Eigenschaft muss eine der folgenden sein:</span><span class="sxs-lookup"><span data-stu-id="96ac7-117">The value of this property must be one of the following:</span></span>
  
|<span data-ttu-id="96ac7-118">**Wert**</span><span class="sxs-lookup"><span data-stu-id="96ac7-118">**Value**</span></span>|<span data-ttu-id="96ac7-119">**Art der Freigabe Message-Objekt**</span><span class="sxs-lookup"><span data-stu-id="96ac7-119">**Type of Sharing Message object**</span></span>|
|:-----|:-----|
|<span data-ttu-id="96ac7-120">0x00020310</span><span class="sxs-lookup"><span data-stu-id="96ac7-120">0x00020310</span></span>  <br/> |<span data-ttu-id="96ac7-121">Eine freigabeeinladung für einen Ordner mit Sonderfunktion.</span><span class="sxs-lookup"><span data-stu-id="96ac7-121">A sharing invitation for a special folder.</span></span>  <br/> |
|<span data-ttu-id="96ac7-122">0x00000310</span><span class="sxs-lookup"><span data-stu-id="96ac7-122">0x00000310</span></span>  <br/> |<span data-ttu-id="96ac7-123">Eine freigabeeinladung für einen Ordner, der nicht auf einen Ordner mit Sonderfunktion ist.</span><span class="sxs-lookup"><span data-stu-id="96ac7-123">A sharing invitation for a folder that is not a special folder.</span></span>  <br/> |
|<span data-ttu-id="96ac7-124">0x00020500</span><span class="sxs-lookup"><span data-stu-id="96ac7-124">0x00020500</span></span>  <br/> |<span data-ttu-id="96ac7-125">Eine Freigabeanfrage.</span><span class="sxs-lookup"><span data-stu-id="96ac7-125">A sharing request.</span></span>  <br/> |
|<span data-ttu-id="96ac7-126">0x00020710</span><span class="sxs-lookup"><span data-stu-id="96ac7-126">0x00020710</span></span>  <br/> |<span data-ttu-id="96ac7-127">Sowohl eine freigabeeinladung für einen Ordner mit Sonderfunktion und eine Freigabeanfrage für entsprechende Spezialordner des Empfängers.</span><span class="sxs-lookup"><span data-stu-id="96ac7-127">Both a sharing invitation for a special folder and a sharing request for the recipient's equivalent special folder.</span></span>  <br/> |
|<span data-ttu-id="96ac7-128">0x00025100</span><span class="sxs-lookup"><span data-stu-id="96ac7-128">0x00025100</span></span>  <br/> |<span data-ttu-id="96ac7-129">Eine Freigabeantwort eine Anforderung zu verweigern.</span><span class="sxs-lookup"><span data-stu-id="96ac7-129">A sharing response denying a request.</span></span>  <br/> |
|<span data-ttu-id="96ac7-130">0x00023310</span><span class="sxs-lookup"><span data-stu-id="96ac7-130">0x00023310</span></span>  <br/> |<span data-ttu-id="96ac7-131">Eine Freigabeantwort akzeptieren einer Anforderung (auch eine Art der Einladung zur Freigabe).</span><span class="sxs-lookup"><span data-stu-id="96ac7-131">A sharing response accepting a request (also a type of sharing invitation).</span></span>  <br/> |
   
## <a name="related-resources"></a><span data-ttu-id="96ac7-132">Verwandte Ressourcen</span><span class="sxs-lookup"><span data-stu-id="96ac7-132">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="96ac7-133">Protokollspezifikationen</span><span class="sxs-lookup"><span data-stu-id="96ac7-133">Protocol specifications</span></span>

<span data-ttu-id="96ac7-134">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="96ac7-134">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="96ac7-135">Enthält Eigenschaftendefinitionen und Verweise auf Verwandte Exchange Server-Spezifikationen.</span><span class="sxs-lookup"><span data-stu-id="96ac7-135">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="96ac7-136">[[MS-OXSHARE]](https://msdn.microsoft.com/library/e4e5bd27-d5e0-43f9-a6ea-550876724f3d%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="96ac7-136">[[MS-OXSHARE]](https://msdn.microsoft.com/library/e4e5bd27-d5e0-43f9-a6ea-550876724f3d%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="96ac7-137">Teilt Postfachordner zwischen Clients.</span><span class="sxs-lookup"><span data-stu-id="96ac7-137">Shares mailbox folders between clients.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="96ac7-138">Header-Dateien</span><span class="sxs-lookup"><span data-stu-id="96ac7-138">Header files</span></span>

<span data-ttu-id="96ac7-139">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="96ac7-139">Mapidefs.h</span></span>
  
> <span data-ttu-id="96ac7-140">Enthält die Datentypdefinitionen.</span><span class="sxs-lookup"><span data-stu-id="96ac7-140">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="96ac7-141">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="96ac7-141">See also</span></span>



[<span data-ttu-id="96ac7-142">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="96ac7-142">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="96ac7-143">Kanonische MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="96ac7-143">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="96ac7-144">Zuordnen von kanonischen Eigenschaftennamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="96ac7-144">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="96ac7-145">Zuordnen von MAPI-Namen zu kanonische Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="96ac7-145">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

