---
title: PidLidSharingInitiatorName (kanonische Eigenschaft)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidSharingInitiatorName
api_type:
- COM
ms.assetid: f2b126fc-41fa-4dc4-9f13-07bc4f621d0b
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: b9e3236affa9612356e68044d2943ea7b9276384
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32336848"
---
# <a name="pidlidsharinginitiatorname-canonical-property"></a><span data-ttu-id="93bdd-103">PidLidSharingInitiatorName (kanonische Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="93bdd-103">PidLidSharingInitiatorName Canonical Property</span></span>

  
  
<span data-ttu-id="93bdd-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="93bdd-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="93bdd-105">Wird als Eigenschaft einer Freigabenachricht bestimmt.</span><span class="sxs-lookup"><span data-stu-id="93bdd-105">Designates as a property of a sharing message.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="93bdd-106">Zugeordnete Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="93bdd-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="93bdd-107">dispidSharingInitiatorName</span><span class="sxs-lookup"><span data-stu-id="93bdd-107">dispidSharingInitiatorName</span></span>  <br/> |
|<span data-ttu-id="93bdd-108">Eigenschaftensatz:</span><span class="sxs-lookup"><span data-stu-id="93bdd-108">Property set:</span></span>  <br/> |<span data-ttu-id="93bdd-109">PSETID_Sharing</span><span class="sxs-lookup"><span data-stu-id="93bdd-109">PSETID_Sharing</span></span>  <br/> |
|<span data-ttu-id="93bdd-110">Lange ID (LID):</span><span class="sxs-lookup"><span data-stu-id="93bdd-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="93bdd-111">0x00008A07</span><span class="sxs-lookup"><span data-stu-id="93bdd-111">0x00008A07</span></span>  <br/> |
|<span data-ttu-id="93bdd-112">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="93bdd-112">Data type:</span></span>  <br/> |<span data-ttu-id="93bdd-113">PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="93bdd-113">PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="93bdd-114">Bereich:</span><span class="sxs-lookup"><span data-stu-id="93bdd-114">Area:</span></span>  <br/> |<span data-ttu-id="93bdd-115">Freigabe</span><span class="sxs-lookup"><span data-stu-id="93bdd-115">Sharing</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="93bdd-116">Hinweise</span><span class="sxs-lookup"><span data-stu-id="93bdd-116">Remarks</span></span>

<span data-ttu-id="93bdd-117">Diese Eigenschaft muss auf den Wert **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) aus dem Adressbuch festgelegt werden, das durch **dispidSharingInitiatorEid** ([PidLidSharingInitiatorEntryId](pidlidsharinginitiatorentryid-canonical-property.md)) identifiziert wurde und ignoriert werden sollte.</span><span class="sxs-lookup"><span data-stu-id="93bdd-117">This property must be set to the value of **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) from the Address Book identified by **dispidSharingInitiatorEid** ([PidLidSharingInitiatorEntryId](pidlidsharinginitiatorentryid-canonical-property.md)) and should be ignored.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="93bdd-118">Verwandte Ressourcen</span><span class="sxs-lookup"><span data-stu-id="93bdd-118">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="93bdd-119">Protokollspezifikationen</span><span class="sxs-lookup"><span data-stu-id="93bdd-119">Protocol specifications</span></span>

<span data-ttu-id="93bdd-120">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="93bdd-120">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="93bdd-121">Stellt Eigenschaftensatzdefinitionen und Verweise auf verwandte Exchange Server zur Verfügung.</span><span class="sxs-lookup"><span data-stu-id="93bdd-121">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="93bdd-122">[[MS-OXSHARE]](https://msdn.microsoft.com/library/e4e5bd27-d5e0-43f9-a6ea-550876724f3d%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="93bdd-122">[[MS-OXSHARE]](https://msdn.microsoft.com/library/e4e5bd27-d5e0-43f9-a6ea-550876724f3d%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="93bdd-123">Gibt Postfachordner zwischen Clients zurück.</span><span class="sxs-lookup"><span data-stu-id="93bdd-123">Shares mailbox folders between clients.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="93bdd-124">Headerdateien</span><span class="sxs-lookup"><span data-stu-id="93bdd-124">Header files</span></span>

<span data-ttu-id="93bdd-125">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="93bdd-125">Mapidefs.h</span></span>
  
> <span data-ttu-id="93bdd-126">Bietet Datentypdefinitionen.</span><span class="sxs-lookup"><span data-stu-id="93bdd-126">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="93bdd-127">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="93bdd-127">See also</span></span>



[<span data-ttu-id="93bdd-128">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="93bdd-128">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="93bdd-129">KANONISCHE EIGENSCHAFTEN VON MAPI</span><span class="sxs-lookup"><span data-stu-id="93bdd-129">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="93bdd-130">Zuordnen kanonischer Eigenschaftsnamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="93bdd-130">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="93bdd-131">Zuordnen von MAPI-Namen zu kanonischen Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="93bdd-131">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

