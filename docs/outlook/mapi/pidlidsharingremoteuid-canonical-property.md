---
title: Kanonische Pidlidsharingremoteuid (-Eigenschaft
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidSharingRemoteUid
api_type:
- COM
ms.assetid: cfe3b728-317b-4871-adea-e2fdf8441da7
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: c3e783934367ad7c5c1a9a760aa8a24525901832
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32331262"
---
# <a name="pidlidsharingremoteuid-canonical-property"></a><span data-ttu-id="e291c-103">Kanonische Pidlidsharingremoteuid (-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="e291c-103">PidLidSharingRemoteUid Canonical Property</span></span>

  
  
<span data-ttu-id="e291c-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="e291c-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="e291c-105">Gibt die Eintrags-ID des freigegebenen Remote Ordners an.</span><span class="sxs-lookup"><span data-stu-id="e291c-105">Specifies the entry ID of the remote folder being shared.</span></span> <span data-ttu-id="e291c-106">Dies ist eine Eigenschaft einer Freigabenachricht.</span><span class="sxs-lookup"><span data-stu-id="e291c-106">This is a property of a sharing message.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="e291c-107">Zugeordnete Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="e291c-107">Associated properties:</span></span>  <br/> |<span data-ttu-id="e291c-108">dispidSharingRemoteUid</span><span class="sxs-lookup"><span data-stu-id="e291c-108">dispidSharingRemoteUid</span></span>  <br/> |
|<span data-ttu-id="e291c-109">Eigenschaftensatz:</span><span class="sxs-lookup"><span data-stu-id="e291c-109">Property set:</span></span>  <br/> |<span data-ttu-id="e291c-110">PSETID_Sharing</span><span class="sxs-lookup"><span data-stu-id="e291c-110">PSETID_Sharing</span></span>  <br/> |
|<span data-ttu-id="e291c-111">Long-ID (Deckel):</span><span class="sxs-lookup"><span data-stu-id="e291c-111">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="e291c-112">0x00008A06</span><span class="sxs-lookup"><span data-stu-id="e291c-112">0x00008A06</span></span>  <br/> |
|<span data-ttu-id="e291c-113">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="e291c-113">Data type:</span></span>  <br/> |<span data-ttu-id="e291c-114">PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="e291c-114">PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="e291c-115">Bereich:</span><span class="sxs-lookup"><span data-stu-id="e291c-115">Area:</span></span>  <br/> |<span data-ttu-id="e291c-116">Freigabe</span><span class="sxs-lookup"><span data-stu-id="e291c-116">Sharing</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="e291c-117">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="e291c-117">Remarks</span></span>

<span data-ttu-id="e291c-118">Diese Eigenschaft muss auf die hexadezimale Zeichenfolgendarstellung des Werts der PR_ENTRYID ([PidTagEntryId](pidtagentryid-canonical-property.md))-Eigenschaft für den freigegebenen Ordner festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="e291c-118">This property must be set to the hexadecimal string representation of the value of the PR_ENTRYID ([PidTagEntryId](pidtagentryid-canonical-property.md)) property on the folder being shared.</span></span> <span data-ttu-id="e291c-119">Dies ist eine Eigenschaft einer Freigabenachricht.</span><span class="sxs-lookup"><span data-stu-id="e291c-119">This is a property of a sharing message.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="e291c-120">Zugehörige Ressourcen</span><span class="sxs-lookup"><span data-stu-id="e291c-120">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="e291c-121">Protokollspezifikationen</span><span class="sxs-lookup"><span data-stu-id="e291c-121">Protocol specifications</span></span>

<span data-ttu-id="e291c-122">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="e291c-122">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="e291c-123">Stellt Eigenschaftensatz Definitionen und Verweise auf zugehörige Exchange Server-Protokollspezifikationen bereit.</span><span class="sxs-lookup"><span data-stu-id="e291c-123">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="e291c-124">[[MS-OXSHARE]](https://msdn.microsoft.com/library/e4e5bd27-d5e0-43f9-a6ea-550876724f3d%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="e291c-124">[[MS-OXSHARE]](https://msdn.microsoft.com/library/e4e5bd27-d5e0-43f9-a6ea-550876724f3d%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="e291c-125">Freigabe von Postfachordnern zwischen Clients.</span><span class="sxs-lookup"><span data-stu-id="e291c-125">Shares mailbox folders between clients.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="e291c-126">Header Dateien</span><span class="sxs-lookup"><span data-stu-id="e291c-126">Header files</span></span>

<span data-ttu-id="e291c-127">Mapidefs. h</span><span class="sxs-lookup"><span data-stu-id="e291c-127">Mapidefs.h</span></span>
  
> <span data-ttu-id="e291c-128">Stellt Datentypdefinitionen bereit.</span><span class="sxs-lookup"><span data-stu-id="e291c-128">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="e291c-129">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="e291c-129">See also</span></span>



[<span data-ttu-id="e291c-130">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="e291c-130">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="e291c-131">Kanonische MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="e291c-131">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="e291c-132">Zuordnen von kanonischen Eigenschaftennamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="e291c-132">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="e291c-133">Zuordnen von MAPI-Namen zu kanonischen Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="e291c-133">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

