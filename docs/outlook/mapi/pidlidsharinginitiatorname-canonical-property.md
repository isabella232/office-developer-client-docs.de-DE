---
title: Kanonische Pidlidsharinginitiatorname (-Eigenschaft
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
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: b9e3236affa9612356e68044d2943ea7b9276384
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32336848"
---
# <a name="pidlidsharinginitiatorname-canonical-property"></a><span data-ttu-id="40d36-103">Kanonische Pidlidsharinginitiatorname (-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="40d36-103">PidLidSharingInitiatorName Canonical Property</span></span>

  
  
<span data-ttu-id="40d36-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="40d36-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="40d36-105">Kennzeichnet als Eigenschaft einer Freigabenachricht.</span><span class="sxs-lookup"><span data-stu-id="40d36-105">Designates as a property of a sharing message.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="40d36-106">Zugeordnete Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="40d36-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="40d36-107">dispidSharingInitiatorName</span><span class="sxs-lookup"><span data-stu-id="40d36-107">dispidSharingInitiatorName</span></span>  <br/> |
|<span data-ttu-id="40d36-108">Eigenschaftensatz:</span><span class="sxs-lookup"><span data-stu-id="40d36-108">Property set:</span></span>  <br/> |<span data-ttu-id="40d36-109">PSETID_Sharing</span><span class="sxs-lookup"><span data-stu-id="40d36-109">PSETID_Sharing</span></span>  <br/> |
|<span data-ttu-id="40d36-110">Long-ID (Deckel):</span><span class="sxs-lookup"><span data-stu-id="40d36-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="40d36-111">0x00008A07</span><span class="sxs-lookup"><span data-stu-id="40d36-111">0x00008A07</span></span>  <br/> |
|<span data-ttu-id="40d36-112">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="40d36-112">Data type:</span></span>  <br/> |<span data-ttu-id="40d36-113">PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="40d36-113">PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="40d36-114">Bereich:</span><span class="sxs-lookup"><span data-stu-id="40d36-114">Area:</span></span>  <br/> |<span data-ttu-id="40d36-115">Freigabe</span><span class="sxs-lookup"><span data-stu-id="40d36-115">Sharing</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="40d36-116">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="40d36-116">Remarks</span></span>

<span data-ttu-id="40d36-117">Diese Eigenschaft muss auf den Wert von **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) aus dem von **DispidSharingInitiatorEid** ([pidlidsharinginitiatorentryid (](pidlidsharinginitiatorentryid-canonical-property.md)) angegebenen Adressbuch festgelegt werden und sollte ignoriert werden.</span><span class="sxs-lookup"><span data-stu-id="40d36-117">This property must be set to the value of **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) from the Address Book identified by **dispidSharingInitiatorEid** ([PidLidSharingInitiatorEntryId](pidlidsharinginitiatorentryid-canonical-property.md)) and should be ignored.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="40d36-118">Zugehörige Ressourcen</span><span class="sxs-lookup"><span data-stu-id="40d36-118">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="40d36-119">Protokollspezifikationen</span><span class="sxs-lookup"><span data-stu-id="40d36-119">Protocol specifications</span></span>

<span data-ttu-id="40d36-120">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="40d36-120">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="40d36-121">Stellt Eigenschaftensatz Definitionen und Verweise auf zugehörige Exchange Server-Protokollspezifikationen bereit.</span><span class="sxs-lookup"><span data-stu-id="40d36-121">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="40d36-122">[[MS-OXSHARE]](https://msdn.microsoft.com/library/e4e5bd27-d5e0-43f9-a6ea-550876724f3d%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="40d36-122">[[MS-OXSHARE]](https://msdn.microsoft.com/library/e4e5bd27-d5e0-43f9-a6ea-550876724f3d%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="40d36-123">Freigabe von Postfachordnern zwischen Clients.</span><span class="sxs-lookup"><span data-stu-id="40d36-123">Shares mailbox folders between clients.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="40d36-124">Header Dateien</span><span class="sxs-lookup"><span data-stu-id="40d36-124">Header files</span></span>

<span data-ttu-id="40d36-125">Mapidefs. h</span><span class="sxs-lookup"><span data-stu-id="40d36-125">Mapidefs.h</span></span>
  
> <span data-ttu-id="40d36-126">Stellt Datentypdefinitionen bereit.</span><span class="sxs-lookup"><span data-stu-id="40d36-126">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="40d36-127">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="40d36-127">See also</span></span>



[<span data-ttu-id="40d36-128">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="40d36-128">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="40d36-129">Kanonische MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="40d36-129">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="40d36-130">Zuordnen von kanonischen Eigenschaftennamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="40d36-130">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="40d36-131">Zuordnen von MAPI-Namen zu kanonischen Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="40d36-131">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

