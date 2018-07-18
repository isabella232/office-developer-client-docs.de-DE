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
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: 1b20c2171f77451d9b7e85573260acff3243238f
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19793783"
---
# <a name="pidlidsharinginitiatorname-canonical-property"></a><span data-ttu-id="919e0-103">PidLidSharingInitiatorName (kanonische Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="919e0-103">PidLidSharingInitiatorName Canonical Property</span></span>

  
  
<span data-ttu-id="919e0-104">**Betrifft**: Outlook</span><span class="sxs-lookup"><span data-stu-id="919e0-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="919e0-105">Legt fest, wie eine eine Freigabenachricht-Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="919e0-105">Designates as a property of a sharing message.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="919e0-106">Zugeordneten Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="919e0-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="919e0-107">dispidSharingInitiatorName</span><span class="sxs-lookup"><span data-stu-id="919e0-107">dispidSharingInitiatorName</span></span>  <br/> |
|<span data-ttu-id="919e0-108">-Eigenschaft festgelegt:</span><span class="sxs-lookup"><span data-stu-id="919e0-108">Property set:</span></span>  <br/> |<span data-ttu-id="919e0-109">PSETID_Sharing</span><span class="sxs-lookup"><span data-stu-id="919e0-109">PSETID_Sharing</span></span>  <br/> |
|<span data-ttu-id="919e0-110">Long-ID (Abdeckung):</span><span class="sxs-lookup"><span data-stu-id="919e0-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="919e0-111">0x00008A07</span><span class="sxs-lookup"><span data-stu-id="919e0-111">0x00008A07</span></span>  <br/> |
|<span data-ttu-id="919e0-112">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="919e0-112">Data type:</span></span>  <br/> |<span data-ttu-id="919e0-113">PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="919e0-113">PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="919e0-114">Bereich:</span><span class="sxs-lookup"><span data-stu-id="919e0-114">Area:</span></span>  <br/> |<span data-ttu-id="919e0-115">Freigabe</span><span class="sxs-lookup"><span data-stu-id="919e0-115">Sharing</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="919e0-116">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="919e0-116">Remarks</span></span>

<span data-ttu-id="919e0-117">Diese Eigenschaft muss auf den Wert der **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) aus dem Adressbuch identifizierten **DispidSharingInitiatorEid** ([PidLidSharingInitiatorEntryId](pidlidsharinginitiatorentryid-canonical-property.md)) festgelegt und sollte ignoriert werden.</span><span class="sxs-lookup"><span data-stu-id="919e0-117">This property must be set to the value of **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) from the Address Book identified by **dispidSharingInitiatorEid** ([PidLidSharingInitiatorEntryId](pidlidsharinginitiatorentryid-canonical-property.md)) and should be ignored.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="919e0-118">Verwandte Ressourcen</span><span class="sxs-lookup"><span data-stu-id="919e0-118">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="919e0-119">Protokollspezifikationen</span><span class="sxs-lookup"><span data-stu-id="919e0-119">Protocol specifications</span></span>

<span data-ttu-id="919e0-120">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="919e0-120">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="919e0-121">Enthält Eigenschaftendefinitionen und Verweise auf Verwandte Exchange Server-Spezifikationen.</span><span class="sxs-lookup"><span data-stu-id="919e0-121">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="919e0-122">[[MS-OXSHARE]](http://msdn.microsoft.com/library/e4e5bd27-d5e0-43f9-a6ea-550876724f3d%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="919e0-122">[[MS-OXSHARE]](http://msdn.microsoft.com/library/e4e5bd27-d5e0-43f9-a6ea-550876724f3d%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="919e0-123">Teilt Postfachordner zwischen Clients.</span><span class="sxs-lookup"><span data-stu-id="919e0-123">Shares mailbox folders between clients.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="919e0-124">Header-Dateien</span><span class="sxs-lookup"><span data-stu-id="919e0-124">Header files</span></span>

<span data-ttu-id="919e0-125">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="919e0-125">Mapidefs.h</span></span>
  
> <span data-ttu-id="919e0-126">Enthält die Datentypdefinitionen.</span><span class="sxs-lookup"><span data-stu-id="919e0-126">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="919e0-127">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="919e0-127">See also</span></span>



[<span data-ttu-id="919e0-128">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="919e0-128">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="919e0-129">Kanonische MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="919e0-129">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="919e0-130">Zuordnen von kanonischen Eigenschaftennamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="919e0-130">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="919e0-131">Zuordnen von MAPI-Namen zu kanonische Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="919e0-131">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

