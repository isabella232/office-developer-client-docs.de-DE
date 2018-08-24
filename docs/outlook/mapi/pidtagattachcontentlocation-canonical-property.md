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
ms.openlocfilehash: 1d654c2a14728979146ef09618bfc4e9e618f9d8
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2018
ms.locfileid: "22594768"
---
# <a name="pidtagattachcontentlocation-canonical-property"></a><span data-ttu-id="6a453-103">PidTagAttachContentLocation (kanonische Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="6a453-103">PidTagAttachContentLocation Canonical Property</span></span>

  
  
<span data-ttu-id="6a453-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="6a453-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="6a453-105">Die Inhaltsspeicherort Kopfzeile der e-Mail-Anlagen Multipurpose Internet Mail Extensions (MIME) enthält.</span><span class="sxs-lookup"><span data-stu-id="6a453-105">Contains the content location header of a Multipurpose Internet Mail Extensions (MIME) message attachment.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="6a453-106">Zugeordnete Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="6a453-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="6a453-107">PR_ATTACH_CONTENT_LOCATION, PR_ATTACH_CONTENT_LOCATION_A, PR_ATTACH_CONTENT_LOCATION_W</span><span class="sxs-lookup"><span data-stu-id="6a453-107">PR_ATTACH_CONTENT_LOCATION, PR_ATTACH_CONTENT_LOCATION_A, PR_ATTACH_CONTENT_LOCATION_W</span></span>  <br/> |
|<span data-ttu-id="6a453-108">Kennung:</span><span class="sxs-lookup"><span data-stu-id="6a453-108">Identifier:</span></span>  <br/> |<span data-ttu-id="6a453-109">0x3713</span><span class="sxs-lookup"><span data-stu-id="6a453-109">0x3713</span></span>  <br/> |
|<span data-ttu-id="6a453-110">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="6a453-110">Data type:</span></span>  <br/> |<span data-ttu-id="6a453-111">PT_STRING8, PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="6a453-111">PT_STRING8, PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="6a453-112">Bereich:</span><span class="sxs-lookup"><span data-stu-id="6a453-112">Area:</span></span>  <br/> |<span data-ttu-id="6a453-113">Nachrichtenanlage</span><span class="sxs-lookup"><span data-stu-id="6a453-113">Message attachment</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="6a453-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="6a453-114">Remarks</span></span>

<span data-ttu-id="6a453-115">Diese Eigenschaften werden verwendet für MHTML-Unterstützung.</span><span class="sxs-lookup"><span data-stu-id="6a453-115">These properties are used for MHTML support.</span></span> <span data-ttu-id="6a453-116">Sie stellen den Inhaltsspeicherort Hostheader für die entsprechenden MIME-Textkörper dar.</span><span class="sxs-lookup"><span data-stu-id="6a453-116">They represent the content location header for the appropriate MIME body part.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="6a453-117">Verwandte Ressourcen</span><span class="sxs-lookup"><span data-stu-id="6a453-117">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="6a453-118">Protokollspezifikationen</span><span class="sxs-lookup"><span data-stu-id="6a453-118">Protocol specifications</span></span>

<span data-ttu-id="6a453-119">[[MS-OXCMSG]](http://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="6a453-119">[[MS-OXCMSG]](http://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="6a453-120">Nachrichten und Anlagen Objekte behandelt.</span><span class="sxs-lookup"><span data-stu-id="6a453-120">Handles message and attachment objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="6a453-121">Header-Dateien</span><span class="sxs-lookup"><span data-stu-id="6a453-121">Header files</span></span>

<span data-ttu-id="6a453-122">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="6a453-122">Mapidefs.h</span></span>
  
> <span data-ttu-id="6a453-123">Enthält die Datentypdefinitionen.</span><span class="sxs-lookup"><span data-stu-id="6a453-123">Provides data type definitions.</span></span>
    
<span data-ttu-id="6a453-124">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="6a453-124">Mapitags.h</span></span>
  
> <span data-ttu-id="6a453-125">Enthält Definitionen von Eigenschaften, die als Alternative Namen aufgelistet.</span><span class="sxs-lookup"><span data-stu-id="6a453-125">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="6a453-126">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="6a453-126">See also</span></span>



[<span data-ttu-id="6a453-127">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="6a453-127">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="6a453-128">Kanonische MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="6a453-128">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="6a453-129">Zuordnen von kanonischen Eigenschaftennamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="6a453-129">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="6a453-130">Zuordnen von MAPI-Namen zu kanonische Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="6a453-130">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

