---
title: PidLidSharingRemoteUid (kanonische Eigenschaft)
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
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: cd42711fc5647f16b33677a330e71d141f1962d7
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2018
ms.locfileid: "22566866"
---
# <a name="pidlidsharingremoteuid-canonical-property"></a><span data-ttu-id="35621-103">PidLidSharingRemoteUid (kanonische Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="35621-103">PidLidSharingRemoteUid Canonical Property</span></span>

  
  
<span data-ttu-id="35621-104">**Betrifft**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="35621-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="35621-105">Gibt die Eintrags-ID des remote-Ordners freigegeben.</span><span class="sxs-lookup"><span data-stu-id="35621-105">Specifies the entry ID of the remote folder being shared.</span></span> <span data-ttu-id="35621-106">Dies ist eine Eigenschaft eines eine Freigabenachricht.</span><span class="sxs-lookup"><span data-stu-id="35621-106">This is a property of a sharing message.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="35621-107">Zugeordnete Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="35621-107">Associated properties:</span></span>  <br/> |<span data-ttu-id="35621-108">dispidSharingRemoteUid</span><span class="sxs-lookup"><span data-stu-id="35621-108">dispidSharingRemoteUid</span></span>  <br/> |
|<span data-ttu-id="35621-109">-Eigenschaft festgelegt:</span><span class="sxs-lookup"><span data-stu-id="35621-109">Property set:</span></span>  <br/> |<span data-ttu-id="35621-110">PSETID_Sharing</span><span class="sxs-lookup"><span data-stu-id="35621-110">PSETID_Sharing</span></span>  <br/> |
|<span data-ttu-id="35621-111">Long-ID (Abdeckung):</span><span class="sxs-lookup"><span data-stu-id="35621-111">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="35621-112">0x00008A06</span><span class="sxs-lookup"><span data-stu-id="35621-112">0x00008A06</span></span>  <br/> |
|<span data-ttu-id="35621-113">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="35621-113">Data type:</span></span>  <br/> |<span data-ttu-id="35621-114">PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="35621-114">PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="35621-115">Bereich:</span><span class="sxs-lookup"><span data-stu-id="35621-115">Area:</span></span>  <br/> |<span data-ttu-id="35621-116">Freigabe</span><span class="sxs-lookup"><span data-stu-id="35621-116">Sharing</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="35621-117">HinwBemerkungeneise</span><span class="sxs-lookup"><span data-stu-id="35621-117">Remarks</span></span>

<span data-ttu-id="35621-118">Diese Eigenschaft muss auf die hexadezimale Zeichenfolgendarstellung des Werts der Eigenschaft PR_ENTRYID ([PidTagEntryId](pidtagentryid-canonical-property.md)) für den freigegebenen Ordner festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="35621-118">This property must be set to the hexadecimal string representation of the value of the PR_ENTRYID ([PidTagEntryId](pidtagentryid-canonical-property.md)) property on the folder being shared.</span></span> <span data-ttu-id="35621-119">Dies ist eine Eigenschaft eines eine Freigabenachricht.</span><span class="sxs-lookup"><span data-stu-id="35621-119">This is a property of a sharing message.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="35621-120">Verwandte Ressourcen</span><span class="sxs-lookup"><span data-stu-id="35621-120">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="35621-121">Protokollspezifikationen</span><span class="sxs-lookup"><span data-stu-id="35621-121">Protocol specifications</span></span>

<span data-ttu-id="35621-122">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="35621-122">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="35621-123">Enthält Eigenschaftendefinitionen und Verweise auf Verwandte Exchange Server-Spezifikationen.</span><span class="sxs-lookup"><span data-stu-id="35621-123">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="35621-124">[[MS-OXSHARE]](http://msdn.microsoft.com/library/e4e5bd27-d5e0-43f9-a6ea-550876724f3d%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="35621-124">[[MS-OXSHARE]](http://msdn.microsoft.com/library/e4e5bd27-d5e0-43f9-a6ea-550876724f3d%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="35621-125">Teilt Postfachordner zwischen Clients.</span><span class="sxs-lookup"><span data-stu-id="35621-125">Shares mailbox folders between clients.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="35621-126">Header-Dateien</span><span class="sxs-lookup"><span data-stu-id="35621-126">Header files</span></span>

<span data-ttu-id="35621-127">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="35621-127">Mapidefs.h</span></span>
  
> <span data-ttu-id="35621-128">Enthält die Datentypdefinitionen.</span><span class="sxs-lookup"><span data-stu-id="35621-128">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="35621-129">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="35621-129">See also</span></span>



[<span data-ttu-id="35621-130">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="35621-130">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="35621-131">Kanonische MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="35621-131">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="35621-132">Zuordnen von kanonischen Eigenschaftennamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="35621-132">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="35621-133">Zuordnen von MAPI-Namen zu kanonische Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="35621-133">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

