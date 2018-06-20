---
title: Kanonische PidLidSharingRemoteType-Eigenschaft
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidSharingRemoteType
api_type:
- COM
ms.assetid: e9bc7c7c-86df-45d8-922b-76e3b076144a
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: 8a9975090a8b90946482fa77fd2dafdb503c1f68
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19793795"
---
# <a name="pidlidsharingremotetype-canonical-property"></a><span data-ttu-id="28cda-103">Kanonische PidLidSharingRemoteType-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="28cda-103">PidLidSharingRemoteType Canonical Property</span></span>

  
  
<span data-ttu-id="28cda-104">**Betrifft**: Outlook</span><span class="sxs-lookup"><span data-stu-id="28cda-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="28cda-105">Gibt den Typ des freigegebenen Ordners remote.</span><span class="sxs-lookup"><span data-stu-id="28cda-105">Specifies the type of the remote shared folder.</span></span> <span data-ttu-id="28cda-106">Dies ist eine Eigenschaft eines eine Freigabenachricht.</span><span class="sxs-lookup"><span data-stu-id="28cda-106">This is a property of a sharing message.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="28cda-107">Zugeordneten Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="28cda-107">Associated properties:</span></span>  <br/> |<span data-ttu-id="28cda-108">dispidSharingRemoteType</span><span class="sxs-lookup"><span data-stu-id="28cda-108">dispidSharingRemoteType</span></span>  <br/> |
|<span data-ttu-id="28cda-109">-Eigenschaft festgelegt:</span><span class="sxs-lookup"><span data-stu-id="28cda-109">Property set:</span></span>  <br/> |<span data-ttu-id="28cda-110">PSETID_Sharing</span><span class="sxs-lookup"><span data-stu-id="28cda-110">PSETID_Sharing</span></span>  <br/> |
|<span data-ttu-id="28cda-111">Long-ID (Abdeckung):</span><span class="sxs-lookup"><span data-stu-id="28cda-111">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="28cda-112">0x00008A1D</span><span class="sxs-lookup"><span data-stu-id="28cda-112">0x00008A1D</span></span>  <br/> |
|<span data-ttu-id="28cda-113">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="28cda-113">Data type:</span></span>  <br/> |<span data-ttu-id="28cda-114">PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="28cda-114">PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="28cda-115">Bereich:</span><span class="sxs-lookup"><span data-stu-id="28cda-115">Area:</span></span>  <br/> |<span data-ttu-id="28cda-116">Freigabe</span><span class="sxs-lookup"><span data-stu-id="28cda-116">Sharing</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="28cda-117">Hinweise</span><span class="sxs-lookup"><span data-stu-id="28cda-117">Remarks</span></span>

<span data-ttu-id="28cda-118">Diese Eigenschaft muss festgelegt werden, auf den gleichen Wert wie die Eigenschaft **DispidSharingLocalType** ([PidLidSharingLocalType](pidlidsharinglocaltype-canonical-property.md)) und sollte ignoriert werden.</span><span class="sxs-lookup"><span data-stu-id="28cda-118">This property must be set to the same value as the **dispidSharingLocalType** ([PidLidSharingLocalType](pidlidsharinglocaltype-canonical-property.md)) property and should be ignored.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="28cda-119">Verwandte Ressourcen</span><span class="sxs-lookup"><span data-stu-id="28cda-119">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="28cda-120">Protokollspezifikationen</span><span class="sxs-lookup"><span data-stu-id="28cda-120">Protocol specifications</span></span>

<span data-ttu-id="28cda-121">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="28cda-121">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="28cda-122">Enthält Eigenschaftendefinitionen und Verweise auf Verwandte Exchange Server-Spezifikationen.</span><span class="sxs-lookup"><span data-stu-id="28cda-122">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="28cda-123">[[MS-OXSHARE]](http://msdn.microsoft.com/library/e4e5bd27-d5e0-43f9-a6ea-550876724f3d%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="28cda-123">[[MS-OXSHARE]](http://msdn.microsoft.com/library/e4e5bd27-d5e0-43f9-a6ea-550876724f3d%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="28cda-124">Teilt Postfachordner zwischen Clients.</span><span class="sxs-lookup"><span data-stu-id="28cda-124">Shares mailbox folders between clients.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="28cda-125">Header-Dateien</span><span class="sxs-lookup"><span data-stu-id="28cda-125">Header files</span></span>

<span data-ttu-id="28cda-126">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="28cda-126">Mapidefs.h</span></span>
  
> <span data-ttu-id="28cda-127">Enthält die Datentypdefinitionen.</span><span class="sxs-lookup"><span data-stu-id="28cda-127">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="28cda-128">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="28cda-128">See also</span></span>



[<span data-ttu-id="28cda-129">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="28cda-129">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="28cda-130">Kanonische MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="28cda-130">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="28cda-131">Zuordnen von kanonischen Eigenschaftennamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="28cda-131">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="28cda-132">Zuordnen von MAPI-Namen zu kanonische Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="28cda-132">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

