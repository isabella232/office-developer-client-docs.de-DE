---
title: PidLidSharingRemoteName (kanonische Eigenschaft)
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
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 3be288b606e197b350c1b053303077c1cb984e9c
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/04/2018
ms.locfileid: "25398290"
---
# <a name="pidlidsharingremotename-canonical-property"></a><span data-ttu-id="1158c-103">PidLidSharingRemoteName (kanonische Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="1158c-103">PidLidSharingRemoteName Canonical Property</span></span>

  
  
<span data-ttu-id="1158c-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="1158c-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="1158c-105">Gibt den Namen des remote-Ordners, der gemeinsam genutzt wird.</span><span class="sxs-lookup"><span data-stu-id="1158c-105">Specifies the name of the remote folder that is being shared.</span></span> <span data-ttu-id="1158c-106">Dies ist eine Eigenschaft eines eine Freigabenachricht.</span><span class="sxs-lookup"><span data-stu-id="1158c-106">This is a property of a sharing message.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="1158c-107">Zugeordnete Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="1158c-107">Associated properties:</span></span>  <br/> |<span data-ttu-id="1158c-108">dispidSharingRemoteName</span><span class="sxs-lookup"><span data-stu-id="1158c-108">dispidSharingRemoteName</span></span>  <br/> |
|<span data-ttu-id="1158c-109">-Eigenschaft festgelegt:</span><span class="sxs-lookup"><span data-stu-id="1158c-109">Property set:</span></span>  <br/> |<span data-ttu-id="1158c-110">PSETID_Sharing</span><span class="sxs-lookup"><span data-stu-id="1158c-110">PSETID_Sharing</span></span>  <br/> |
|<span data-ttu-id="1158c-111">Long-ID (Abdeckung):</span><span class="sxs-lookup"><span data-stu-id="1158c-111">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="1158c-112">0x00008A05</span><span class="sxs-lookup"><span data-stu-id="1158c-112">0x00008A05</span></span>  <br/> |
|<span data-ttu-id="1158c-113">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="1158c-113">Data type:</span></span>  <br/> |<span data-ttu-id="1158c-114">PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="1158c-114">PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="1158c-115">Bereich:</span><span class="sxs-lookup"><span data-stu-id="1158c-115">Area:</span></span>  <br/> |<span data-ttu-id="1158c-116">Freigabe</span><span class="sxs-lookup"><span data-stu-id="1158c-116">Sharing</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="1158c-117">Hinweise</span><span class="sxs-lookup"><span data-stu-id="1158c-117">Remarks</span></span>

<span data-ttu-id="1158c-118">Diese Eigenschaft muss auf den Wert der Eigenschaft **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) für den freigegebenen Ordner festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="1158c-118">This property must be set to the value of the **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) property on the folder being shared.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="1158c-119">Verwandte Ressourcen</span><span class="sxs-lookup"><span data-stu-id="1158c-119">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="1158c-120">Protokollspezifikationen</span><span class="sxs-lookup"><span data-stu-id="1158c-120">Protocol specifications</span></span>

<span data-ttu-id="1158c-121">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="1158c-121">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="1158c-122">Enthält Eigenschaftendefinitionen und Verweise auf Verwandte Exchange Server-Spezifikationen.</span><span class="sxs-lookup"><span data-stu-id="1158c-122">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="1158c-123">[[MS-OXSHARE]](https://msdn.microsoft.com/library/e4e5bd27-d5e0-43f9-a6ea-550876724f3d%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="1158c-123">[[MS-OXSHARE]](https://msdn.microsoft.com/library/e4e5bd27-d5e0-43f9-a6ea-550876724f3d%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="1158c-124">Teilt Postfachordner zwischen Clients.</span><span class="sxs-lookup"><span data-stu-id="1158c-124">Shares mailbox folders between clients.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="1158c-125">Header-Dateien</span><span class="sxs-lookup"><span data-stu-id="1158c-125">Header files</span></span>

<span data-ttu-id="1158c-126">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="1158c-126">Mapidefs.h</span></span>
  
> <span data-ttu-id="1158c-127">Enthält die Datentypdefinitionen.</span><span class="sxs-lookup"><span data-stu-id="1158c-127">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="1158c-128">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="1158c-128">See also</span></span>



[<span data-ttu-id="1158c-129">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="1158c-129">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="1158c-130">Kanonische MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="1158c-130">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="1158c-131">Zuordnen von kanonischen Eigenschaftennamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="1158c-131">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="1158c-132">Zuordnen von MAPI-Namen zu kanonische Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="1158c-132">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

