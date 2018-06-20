---
title: Kanonische PidLidSharingRemoteName-Eigenschaft
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidSharingRemoteName
api_type:
- COM
ms.assetid: be975f74-4b95-45a4-bbee-959fa8e4ad45
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: fc3324cb686733f06b9cc0945c93b7df2e5980ae
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19793794"
---
# <a name="pidlidsharingremotename-canonical-property"></a><span data-ttu-id="e2120-103">Kanonische PidLidSharingRemoteName-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="e2120-103">PidLidSharingRemoteName Canonical Property</span></span>

  
  
<span data-ttu-id="e2120-104">**Betrifft**: Outlook</span><span class="sxs-lookup"><span data-stu-id="e2120-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="e2120-105">Gibt den Namen des remote-Ordners, der gemeinsam genutzt wird.</span><span class="sxs-lookup"><span data-stu-id="e2120-105">Specifies the name of the remote folder that is being shared.</span></span> <span data-ttu-id="e2120-106">Dies ist eine Eigenschaft eines eine Freigabenachricht.</span><span class="sxs-lookup"><span data-stu-id="e2120-106">This is a property of a sharing message.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="e2120-107">Zugeordneten Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="e2120-107">Associated properties:</span></span>  <br/> |<span data-ttu-id="e2120-108">dispidSharingRemoteName</span><span class="sxs-lookup"><span data-stu-id="e2120-108">dispidSharingRemoteName</span></span>  <br/> |
|<span data-ttu-id="e2120-109">-Eigenschaft festgelegt:</span><span class="sxs-lookup"><span data-stu-id="e2120-109">Property set:</span></span>  <br/> |<span data-ttu-id="e2120-110">PSETID_Sharing</span><span class="sxs-lookup"><span data-stu-id="e2120-110">PSETID_Sharing</span></span>  <br/> |
|<span data-ttu-id="e2120-111">Long-ID (Abdeckung):</span><span class="sxs-lookup"><span data-stu-id="e2120-111">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="e2120-112">0x00008A05</span><span class="sxs-lookup"><span data-stu-id="e2120-112">0x00008A05</span></span>  <br/> |
|<span data-ttu-id="e2120-113">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="e2120-113">Data type:</span></span>  <br/> |<span data-ttu-id="e2120-114">PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="e2120-114">PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="e2120-115">Bereich:</span><span class="sxs-lookup"><span data-stu-id="e2120-115">Area:</span></span>  <br/> |<span data-ttu-id="e2120-116">Freigabe</span><span class="sxs-lookup"><span data-stu-id="e2120-116">Sharing</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="e2120-117">Hinweise</span><span class="sxs-lookup"><span data-stu-id="e2120-117">Remarks</span></span>

<span data-ttu-id="e2120-118">Diese Eigenschaft muss auf den Wert der Eigenschaft **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) für den freigegebenen Ordner festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="e2120-118">This property must be set to the value of the **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) property on the folder being shared.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="e2120-119">Verwandte Ressourcen</span><span class="sxs-lookup"><span data-stu-id="e2120-119">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="e2120-120">Protokollspezifikationen</span><span class="sxs-lookup"><span data-stu-id="e2120-120">Protocol specifications</span></span>

<span data-ttu-id="e2120-121">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="e2120-121">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="e2120-122">Enthält Eigenschaftendefinitionen und Verweise auf Verwandte Exchange Server-Spezifikationen.</span><span class="sxs-lookup"><span data-stu-id="e2120-122">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="e2120-123">[[MS-OXSHARE]](http://msdn.microsoft.com/library/e4e5bd27-d5e0-43f9-a6ea-550876724f3d%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="e2120-123">[[MS-OXSHARE]](http://msdn.microsoft.com/library/e4e5bd27-d5e0-43f9-a6ea-550876724f3d%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="e2120-124">Teilt Postfachordner zwischen Clients.</span><span class="sxs-lookup"><span data-stu-id="e2120-124">Shares mailbox folders between clients.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="e2120-125">Header-Dateien</span><span class="sxs-lookup"><span data-stu-id="e2120-125">Header files</span></span>

<span data-ttu-id="e2120-126">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="e2120-126">Mapidefs.h</span></span>
  
> <span data-ttu-id="e2120-127">Enthält die Datentypdefinitionen.</span><span class="sxs-lookup"><span data-stu-id="e2120-127">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="e2120-128">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="e2120-128">See also</span></span>



[<span data-ttu-id="e2120-129">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="e2120-129">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="e2120-130">Kanonische MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="e2120-130">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="e2120-131">Zuordnen von kanonischen Eigenschaftennamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="e2120-131">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="e2120-132">Zuordnen von MAPI-Namen zu kanonische Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="e2120-132">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

