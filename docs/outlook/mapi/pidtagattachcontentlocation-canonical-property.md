---
title: PidTagAttachContentLocation (kanonische Eigenschaft)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagAttachContentLocation
api_type:
- HeaderDef
ms.assetid: af2f776c-1b77-4942-827a-4363eda3924f
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: f279d8ea305c0b1e609881b15e39653c41d5828e
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32345479"
---
# <a name="pidtagattachcontentlocation-canonical-property"></a><span data-ttu-id="a377f-103">PidTagAttachContentLocation (kanonische Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="a377f-103">PidTagAttachContentLocation Canonical Property</span></span>

  
  
<span data-ttu-id="a377f-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="a377f-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="a377f-105">Enthält den Inhaltsspeicherortheader einer Mehrzweck-E-Mail-Nachrichtenanlage (Multipurpose Internet Mail Extensions, MIME).</span><span class="sxs-lookup"><span data-stu-id="a377f-105">Contains the content location header of a Multipurpose Internet Mail Extensions (MIME) message attachment.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="a377f-106">Zugeordnete Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="a377f-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="a377f-107">PR_ATTACH_CONTENT_LOCATION, PR_ATTACH_CONTENT_LOCATION_A, PR_ATTACH_CONTENT_LOCATION_W</span><span class="sxs-lookup"><span data-stu-id="a377f-107">PR_ATTACH_CONTENT_LOCATION, PR_ATTACH_CONTENT_LOCATION_A, PR_ATTACH_CONTENT_LOCATION_W</span></span>  <br/> |
|<span data-ttu-id="a377f-108">Kennung:</span><span class="sxs-lookup"><span data-stu-id="a377f-108">Identifier:</span></span>  <br/> |<span data-ttu-id="a377f-109">0x3713</span><span class="sxs-lookup"><span data-stu-id="a377f-109">0x3713</span></span>  <br/> |
|<span data-ttu-id="a377f-110">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="a377f-110">Data type:</span></span>  <br/> |<span data-ttu-id="a377f-111">PT_STRING8, PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="a377f-111">PT_STRING8, PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="a377f-112">Bereich:</span><span class="sxs-lookup"><span data-stu-id="a377f-112">Area:</span></span>  <br/> |<span data-ttu-id="a377f-113">Nachrichtenanlage</span><span class="sxs-lookup"><span data-stu-id="a377f-113">Message attachment</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="a377f-114">Hinweise</span><span class="sxs-lookup"><span data-stu-id="a377f-114">Remarks</span></span>

<span data-ttu-id="a377f-115">Diese Eigenschaften werden für die MHTML-Unterstützung verwendet.</span><span class="sxs-lookup"><span data-stu-id="a377f-115">These properties are used for MHTML support.</span></span> <span data-ttu-id="a377f-116">Sie stellen den Inhaltsspeicherortheader für den entsprechenden MIME-Textteil dar.</span><span class="sxs-lookup"><span data-stu-id="a377f-116">They represent the content location header for the appropriate MIME body part.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="a377f-117">Verwandte Ressourcen</span><span class="sxs-lookup"><span data-stu-id="a377f-117">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="a377f-118">Protokollspezifikationen</span><span class="sxs-lookup"><span data-stu-id="a377f-118">Protocol specifications</span></span>

<span data-ttu-id="a377f-119">[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="a377f-119">[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="a377f-120">Behandelt Nachrichten- und Anlagenobjekte.</span><span class="sxs-lookup"><span data-stu-id="a377f-120">Handles message and attachment objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="a377f-121">Headerdateien</span><span class="sxs-lookup"><span data-stu-id="a377f-121">Header files</span></span>

<span data-ttu-id="a377f-122">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="a377f-122">Mapidefs.h</span></span>
  
> <span data-ttu-id="a377f-123">Bietet Datentypdefinitionen.</span><span class="sxs-lookup"><span data-stu-id="a377f-123">Provides data type definitions.</span></span>
    
<span data-ttu-id="a377f-124">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="a377f-124">Mapitags.h</span></span>
  
> <span data-ttu-id="a377f-125">Enthält Definitionen von Eigenschaften, die als alternative Namen aufgeführt sind.</span><span class="sxs-lookup"><span data-stu-id="a377f-125">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="a377f-126">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="a377f-126">See also</span></span>



[<span data-ttu-id="a377f-127">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="a377f-127">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="a377f-128">KANONISCHE EIGENSCHAFTEN VON MAPI</span><span class="sxs-lookup"><span data-stu-id="a377f-128">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="a377f-129">Zuordnen kanonischer Eigenschaftsnamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="a377f-129">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="a377f-130">Zuordnen von MAPI-Namen zu kanonischen Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="a377f-130">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

