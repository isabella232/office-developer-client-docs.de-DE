---
title: PidLidSharingCapabilities (kanonische Eigenschaft)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidSharingCapabilities
api_type:
- COM
ms.assetid: 86b3eab2-2594-4204-aedf-8ce2ee3b81ce
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: d44851e1c863cb117eed3462eb98de87f8d1f0be
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/04/2018
ms.locfileid: "25388322"
---
# <a name="pidlidsharingcapabilities-canonical-property"></a><span data-ttu-id="00141-103">PidLidSharingCapabilities (kanonische Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="00141-103">PidLidSharingCapabilities Canonical Property</span></span>

  
  
<span data-ttu-id="00141-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="00141-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="00141-105">Legt fest, wie eine eine Freigabenachricht-Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="00141-105">Designates as a property of a sharing message.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="00141-106">Zugeordnete Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="00141-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="00141-107">dispidSharingCaps</span><span class="sxs-lookup"><span data-stu-id="00141-107">dispidSharingCaps</span></span>  <br/> |
|<span data-ttu-id="00141-108">-Eigenschaft festgelegt:</span><span class="sxs-lookup"><span data-stu-id="00141-108">Property set:</span></span>  <br/> |<span data-ttu-id="00141-109">PSETID_Sharing</span><span class="sxs-lookup"><span data-stu-id="00141-109">PSETID_Sharing</span></span>  <br/> |
|<span data-ttu-id="00141-110">Long-ID (Abdeckung):</span><span class="sxs-lookup"><span data-stu-id="00141-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="00141-111">0x00008A17</span><span class="sxs-lookup"><span data-stu-id="00141-111">0x00008A17</span></span>  <br/> |
|<span data-ttu-id="00141-112">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="00141-112">Data type:</span></span>  <br/> |<span data-ttu-id="00141-113">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="00141-113">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="00141-114">Bereich:</span><span class="sxs-lookup"><span data-stu-id="00141-114">Area:</span></span>  <br/> |<span data-ttu-id="00141-115">Freigabe</span><span class="sxs-lookup"><span data-stu-id="00141-115">Sharing</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="00141-116">Hinweise</span><span class="sxs-lookup"><span data-stu-id="00141-116">Remarks</span></span>

<span data-ttu-id="00141-117">Diese Eigenschaft muss auf einen der folgenden Werte festgelegt werden:</span><span class="sxs-lookup"><span data-stu-id="00141-117">This property must be set to one of the following values:</span></span>
  
|<span data-ttu-id="00141-118">**Wert**</span><span class="sxs-lookup"><span data-stu-id="00141-118">**Value**</span></span>|<span data-ttu-id="00141-119">**Szenario**</span><span class="sxs-lookup"><span data-stu-id="00141-119">**Scenario**</span></span>|
|:-----|:-----|
|<span data-ttu-id="00141-120">0x00040290</span><span class="sxs-lookup"><span data-stu-id="00141-120">0x00040290</span></span>  <br/> |<span data-ttu-id="00141-121">Dieses Objekt Freigabenachricht bezieht sich auf einen Ordner mit Sonderfunktion.</span><span class="sxs-lookup"><span data-stu-id="00141-121">This Sharing Message object relates to a special folder.</span></span>  <br/> |
|<span data-ttu-id="00141-122">0x000402B0</span><span class="sxs-lookup"><span data-stu-id="00141-122">0x000402B0</span></span>  <br/> |<span data-ttu-id="00141-123">Dieses Objekt Freigabenachricht bezieht sich nicht auf einen Ordner mit Sonderfunktion.</span><span class="sxs-lookup"><span data-stu-id="00141-123">This Sharing Message object does not relate to a special folder.</span></span>  <br/> |
   
## <a name="related-resources"></a><span data-ttu-id="00141-124">Verwandte Ressourcen</span><span class="sxs-lookup"><span data-stu-id="00141-124">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="00141-125">Protokollspezifikationen</span><span class="sxs-lookup"><span data-stu-id="00141-125">Protocol specifications</span></span>

<span data-ttu-id="00141-126">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="00141-126">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="00141-127">Enthält Eigenschaftendefinitionen und Verweise auf Verwandte Exchange Server-Spezifikationen.</span><span class="sxs-lookup"><span data-stu-id="00141-127">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="00141-128">[[MS-OXSHARE]](https://msdn.microsoft.com/library/e4e5bd27-d5e0-43f9-a6ea-550876724f3d%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="00141-128">[[MS-OXSHARE]](https://msdn.microsoft.com/library/e4e5bd27-d5e0-43f9-a6ea-550876724f3d%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="00141-129">Teilt Postfachordner zwischen Clients.</span><span class="sxs-lookup"><span data-stu-id="00141-129">Shares mailbox folders between clients.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="00141-130">Header-Dateien</span><span class="sxs-lookup"><span data-stu-id="00141-130">Header files</span></span>

<span data-ttu-id="00141-131">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="00141-131">Mapidefs.h</span></span>
  
> <span data-ttu-id="00141-132">Enthält die Datentypdefinitionen.</span><span class="sxs-lookup"><span data-stu-id="00141-132">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="00141-133">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="00141-133">See also</span></span>



[<span data-ttu-id="00141-134">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="00141-134">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="00141-135">Kanonische MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="00141-135">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="00141-136">Zuordnen von kanonischen Eigenschaftennamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="00141-136">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="00141-137">Zuordnen von MAPI-Namen zu kanonische Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="00141-137">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

