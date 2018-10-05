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
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/04/2018
ms.locfileid: "25394380"
---
# <a name="pidlidsharinginitiatorname-canonical-property"></a><span data-ttu-id="da5f9-103">PidLidSharingInitiatorName (kanonische Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="da5f9-103">PidLidSharingInitiatorName Canonical Property</span></span>

  
  
<span data-ttu-id="da5f9-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="da5f9-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="da5f9-105">Legt fest, wie eine eine Freigabenachricht-Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="da5f9-105">Designates as a property of a sharing message.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="da5f9-106">Zugeordnete Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="da5f9-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="da5f9-107">dispidSharingInitiatorName</span><span class="sxs-lookup"><span data-stu-id="da5f9-107">dispidSharingInitiatorName</span></span>  <br/> |
|<span data-ttu-id="da5f9-108">-Eigenschaft festgelegt:</span><span class="sxs-lookup"><span data-stu-id="da5f9-108">Property set:</span></span>  <br/> |<span data-ttu-id="da5f9-109">PSETID_Sharing</span><span class="sxs-lookup"><span data-stu-id="da5f9-109">PSETID_Sharing</span></span>  <br/> |
|<span data-ttu-id="da5f9-110">Long-ID (Abdeckung):</span><span class="sxs-lookup"><span data-stu-id="da5f9-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="da5f9-111">0x00008A07</span><span class="sxs-lookup"><span data-stu-id="da5f9-111">0x00008A07</span></span>  <br/> |
|<span data-ttu-id="da5f9-112">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="da5f9-112">Data type:</span></span>  <br/> |<span data-ttu-id="da5f9-113">PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="da5f9-113">PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="da5f9-114">Bereich:</span><span class="sxs-lookup"><span data-stu-id="da5f9-114">Area:</span></span>  <br/> |<span data-ttu-id="da5f9-115">Freigabe</span><span class="sxs-lookup"><span data-stu-id="da5f9-115">Sharing</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="da5f9-116">Hinweise</span><span class="sxs-lookup"><span data-stu-id="da5f9-116">Remarks</span></span>

<span data-ttu-id="da5f9-117">Diese Eigenschaft muss auf den Wert der **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) aus dem Adressbuch identifizierten **DispidSharingInitiatorEid** ([PidLidSharingInitiatorEntryId](pidlidsharinginitiatorentryid-canonical-property.md)) festgelegt und sollte ignoriert werden.</span><span class="sxs-lookup"><span data-stu-id="da5f9-117">This property must be set to the value of **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) from the Address Book identified by **dispidSharingInitiatorEid** ([PidLidSharingInitiatorEntryId](pidlidsharinginitiatorentryid-canonical-property.md)) and should be ignored.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="da5f9-118">Verwandte Ressourcen</span><span class="sxs-lookup"><span data-stu-id="da5f9-118">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="da5f9-119">Protokollspezifikationen</span><span class="sxs-lookup"><span data-stu-id="da5f9-119">Protocol specifications</span></span>

<span data-ttu-id="da5f9-120">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="da5f9-120">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="da5f9-121">Enthält Eigenschaftendefinitionen und Verweise auf Verwandte Exchange Server-Spezifikationen.</span><span class="sxs-lookup"><span data-stu-id="da5f9-121">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="da5f9-122">[[MS-OXSHARE]](https://msdn.microsoft.com/library/e4e5bd27-d5e0-43f9-a6ea-550876724f3d%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="da5f9-122">[[MS-OXSHARE]](https://msdn.microsoft.com/library/e4e5bd27-d5e0-43f9-a6ea-550876724f3d%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="da5f9-123">Teilt Postfachordner zwischen Clients.</span><span class="sxs-lookup"><span data-stu-id="da5f9-123">Shares mailbox folders between clients.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="da5f9-124">Header-Dateien</span><span class="sxs-lookup"><span data-stu-id="da5f9-124">Header files</span></span>

<span data-ttu-id="da5f9-125">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="da5f9-125">Mapidefs.h</span></span>
  
> <span data-ttu-id="da5f9-126">Enthält die Datentypdefinitionen.</span><span class="sxs-lookup"><span data-stu-id="da5f9-126">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="da5f9-127">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="da5f9-127">See also</span></span>



[<span data-ttu-id="da5f9-128">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="da5f9-128">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="da5f9-129">Kanonische MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="da5f9-129">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="da5f9-130">Zuordnen von kanonischen Eigenschaftennamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="da5f9-130">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="da5f9-131">Zuordnen von MAPI-Namen zu kanonische Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="da5f9-131">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

