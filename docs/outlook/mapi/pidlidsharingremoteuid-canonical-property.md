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
ms.openlocfilehash: c3e783934367ad7c5c1a9a760aa8a24525901832
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/04/2018
ms.locfileid: "25394734"
---
# <a name="pidlidsharingremoteuid-canonical-property"></a><span data-ttu-id="3b1b9-103">PidLidSharingRemoteUid (kanonische Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="3b1b9-103">PidLidSharingRemoteUid Canonical Property</span></span>

  
  
<span data-ttu-id="3b1b9-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="3b1b9-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="3b1b9-105">Gibt die Eintrags-ID des remote-Ordners freigegeben.</span><span class="sxs-lookup"><span data-stu-id="3b1b9-105">Specifies the entry ID of the remote folder being shared.</span></span> <span data-ttu-id="3b1b9-106">Dies ist eine Eigenschaft eines eine Freigabenachricht.</span><span class="sxs-lookup"><span data-stu-id="3b1b9-106">This is a property of a sharing message.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="3b1b9-107">Zugeordnete Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="3b1b9-107">Associated properties:</span></span>  <br/> |<span data-ttu-id="3b1b9-108">dispidSharingRemoteUid</span><span class="sxs-lookup"><span data-stu-id="3b1b9-108">dispidSharingRemoteUid</span></span>  <br/> |
|<span data-ttu-id="3b1b9-109">-Eigenschaft festgelegt:</span><span class="sxs-lookup"><span data-stu-id="3b1b9-109">Property set:</span></span>  <br/> |<span data-ttu-id="3b1b9-110">PSETID_Sharing</span><span class="sxs-lookup"><span data-stu-id="3b1b9-110">PSETID_Sharing</span></span>  <br/> |
|<span data-ttu-id="3b1b9-111">Long-ID (Abdeckung):</span><span class="sxs-lookup"><span data-stu-id="3b1b9-111">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="3b1b9-112">0x00008A06</span><span class="sxs-lookup"><span data-stu-id="3b1b9-112">0x00008A06</span></span>  <br/> |
|<span data-ttu-id="3b1b9-113">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="3b1b9-113">Data type:</span></span>  <br/> |<span data-ttu-id="3b1b9-114">PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="3b1b9-114">PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="3b1b9-115">Bereich:</span><span class="sxs-lookup"><span data-stu-id="3b1b9-115">Area:</span></span>  <br/> |<span data-ttu-id="3b1b9-116">Freigabe</span><span class="sxs-lookup"><span data-stu-id="3b1b9-116">Sharing</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="3b1b9-117">Hinweise</span><span class="sxs-lookup"><span data-stu-id="3b1b9-117">Remarks</span></span>

<span data-ttu-id="3b1b9-118">Diese Eigenschaft muss auf die hexadezimale Zeichenfolgendarstellung des Werts der Eigenschaft PR_ENTRYID ([PidTagEntryId](pidtagentryid-canonical-property.md)) für den freigegebenen Ordner festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="3b1b9-118">This property must be set to the hexadecimal string representation of the value of the PR_ENTRYID ([PidTagEntryId](pidtagentryid-canonical-property.md)) property on the folder being shared.</span></span> <span data-ttu-id="3b1b9-119">Dies ist eine Eigenschaft eines eine Freigabenachricht.</span><span class="sxs-lookup"><span data-stu-id="3b1b9-119">This is a property of a sharing message.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="3b1b9-120">Verwandte Ressourcen</span><span class="sxs-lookup"><span data-stu-id="3b1b9-120">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="3b1b9-121">Protokollspezifikationen</span><span class="sxs-lookup"><span data-stu-id="3b1b9-121">Protocol specifications</span></span>

<span data-ttu-id="3b1b9-122">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="3b1b9-122">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="3b1b9-123">Enthält Eigenschaftendefinitionen und Verweise auf Verwandte Exchange Server-Spezifikationen.</span><span class="sxs-lookup"><span data-stu-id="3b1b9-123">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="3b1b9-124">[[MS-OXSHARE]](https://msdn.microsoft.com/library/e4e5bd27-d5e0-43f9-a6ea-550876724f3d%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="3b1b9-124">[[MS-OXSHARE]](https://msdn.microsoft.com/library/e4e5bd27-d5e0-43f9-a6ea-550876724f3d%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="3b1b9-125">Teilt Postfachordner zwischen Clients.</span><span class="sxs-lookup"><span data-stu-id="3b1b9-125">Shares mailbox folders between clients.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="3b1b9-126">Header-Dateien</span><span class="sxs-lookup"><span data-stu-id="3b1b9-126">Header files</span></span>

<span data-ttu-id="3b1b9-127">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="3b1b9-127">Mapidefs.h</span></span>
  
> <span data-ttu-id="3b1b9-128">Enthält die Datentypdefinitionen.</span><span class="sxs-lookup"><span data-stu-id="3b1b9-128">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="3b1b9-129">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="3b1b9-129">See also</span></span>



[<span data-ttu-id="3b1b9-130">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="3b1b9-130">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="3b1b9-131">Kanonische MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="3b1b9-131">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="3b1b9-132">Zuordnen von kanonischen Eigenschaftennamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="3b1b9-132">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="3b1b9-133">Zuordnen von MAPI-Namen zu kanonische Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="3b1b9-133">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

