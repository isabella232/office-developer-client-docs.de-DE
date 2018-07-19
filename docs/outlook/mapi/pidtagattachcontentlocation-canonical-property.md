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
ms.openlocfilehash: d886bf1e30eae6b4b26512eed95988516a609c94
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19794079"
---
# <a name="pidtagattachcontentlocation-canonical-property"></a><span data-ttu-id="03ebf-103">PidTagAttachContentLocation (kanonische Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="03ebf-103">PidTagAttachContentLocation Canonical Property</span></span>

  
  
<span data-ttu-id="03ebf-104">**Betrifft**: Outlook</span><span class="sxs-lookup"><span data-stu-id="03ebf-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="03ebf-105">Die Inhaltsspeicherort Kopfzeile der e-Mail-Anlagen Multipurpose Internet Mail Extensions (MIME) enthält.</span><span class="sxs-lookup"><span data-stu-id="03ebf-105">Contains the content location header of a Multipurpose Internet Mail Extensions (MIME) message attachment.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="03ebf-106">Zugeordneten Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="03ebf-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="03ebf-107">PR_ATTACH_CONTENT_LOCATION, PR_ATTACH_CONTENT_LOCATION_A, PR_ATTACH_CONTENT_LOCATION_W</span><span class="sxs-lookup"><span data-stu-id="03ebf-107">PR_ATTACH_CONTENT_LOCATION, PR_ATTACH_CONTENT_LOCATION_A, PR_ATTACH_CONTENT_LOCATION_W</span></span>  <br/> |
|<span data-ttu-id="03ebf-108">Bezeichner:</span><span class="sxs-lookup"><span data-stu-id="03ebf-108">Identifier:</span></span>  <br/> |<span data-ttu-id="03ebf-109">0x3713</span><span class="sxs-lookup"><span data-stu-id="03ebf-109">0x3713</span></span>  <br/> |
|<span data-ttu-id="03ebf-110">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="03ebf-110">Data type:</span></span>  <br/> |<span data-ttu-id="03ebf-111">PT_STRING8, PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="03ebf-111">PT_STRING8, PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="03ebf-112">Bereich:</span><span class="sxs-lookup"><span data-stu-id="03ebf-112">Area:</span></span>  <br/> |<span data-ttu-id="03ebf-113">E-Mail-Anlage</span><span class="sxs-lookup"><span data-stu-id="03ebf-113">Message attachment</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="03ebf-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="03ebf-114">Remarks</span></span>

<span data-ttu-id="03ebf-115">Diese Eigenschaften werden verwendet für MHTML-Unterstützung.</span><span class="sxs-lookup"><span data-stu-id="03ebf-115">These properties are used for MHTML support.</span></span> <span data-ttu-id="03ebf-116">Sie stellen den Inhaltsspeicherort Hostheader für die entsprechenden MIME-Textkörper dar.</span><span class="sxs-lookup"><span data-stu-id="03ebf-116">They represent the content location header for the appropriate MIME body part.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="03ebf-117">Verwandte Ressourcen</span><span class="sxs-lookup"><span data-stu-id="03ebf-117">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="03ebf-118">Protokollspezifikationen</span><span class="sxs-lookup"><span data-stu-id="03ebf-118">Protocol specifications</span></span>

<span data-ttu-id="03ebf-119">[[MS-OXCMSG]](http://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="03ebf-119">[[MS-OXCMSG]](http://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="03ebf-120">Nachrichten und Anlagen Objekte behandelt.</span><span class="sxs-lookup"><span data-stu-id="03ebf-120">Handles message and attachment objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="03ebf-121">Header-Dateien</span><span class="sxs-lookup"><span data-stu-id="03ebf-121">Header files</span></span>

<span data-ttu-id="03ebf-122">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="03ebf-122">Mapidefs.h</span></span>
  
> <span data-ttu-id="03ebf-123">Enthält die Datentypdefinitionen.</span><span class="sxs-lookup"><span data-stu-id="03ebf-123">Provides data type definitions.</span></span>
    
<span data-ttu-id="03ebf-124">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="03ebf-124">Mapitags.h</span></span>
  
> <span data-ttu-id="03ebf-125">Enthält Definitionen von Eigenschaften, die als Alternative Namen aufgelistet.</span><span class="sxs-lookup"><span data-stu-id="03ebf-125">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="03ebf-126">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="03ebf-126">See also</span></span>



[<span data-ttu-id="03ebf-127">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="03ebf-127">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="03ebf-128">Kanonische MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="03ebf-128">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="03ebf-129">Zuordnen von kanonischen Eigenschaftennamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="03ebf-129">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="03ebf-130">Zuordnen von MAPI-Namen zu kanonische Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="03ebf-130">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

