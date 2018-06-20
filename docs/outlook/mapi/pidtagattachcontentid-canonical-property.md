---
title: Kanonische PidTagAttachContentId-Eigenschaft
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagAttachContentId
api_type:
- HeaderDef
ms.assetid: 46f31089-3b66-41a2-8094-e3db52464b9f
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: edd0df690df6af47ed6db34dc4a658b24136077c
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19794095"
---
# <a name="pidtagattachcontentid-canonical-property"></a><span data-ttu-id="8ed91-103">Kanonische PidTagAttachContentId-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="8ed91-103">PidTagAttachContentId Canonical Property</span></span>

  
  
<span data-ttu-id="8ed91-104">**Betrifft**: Outlook</span><span class="sxs-lookup"><span data-stu-id="8ed91-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="8ed91-105">Header Content Identification Multipurpose Internet Mail Extensions (MIME) e-Mail-Anlagen enthält.</span><span class="sxs-lookup"><span data-stu-id="8ed91-105">Contains the content identification header of a Multipurpose Internet Mail Extensions (MIME) message attachment.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="8ed91-106">Zugeordneten Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="8ed91-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="8ed91-107">PR_ATTACH_CONTENT_ID, PR_ATTACH_CONTENT_ID_A, PR_ATTACH_CONTENT_ID_W</span><span class="sxs-lookup"><span data-stu-id="8ed91-107">PR_ATTACH_CONTENT_ID, PR_ATTACH_CONTENT_ID_A, PR_ATTACH_CONTENT_ID_W</span></span>  <br/> |
|<span data-ttu-id="8ed91-108">Bezeichner:</span><span class="sxs-lookup"><span data-stu-id="8ed91-108">Identifier:</span></span>  <br/> |<span data-ttu-id="8ed91-109">0x3712</span><span class="sxs-lookup"><span data-stu-id="8ed91-109">0x3712</span></span>  <br/> |
|<span data-ttu-id="8ed91-110">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="8ed91-110">Data type:</span></span>  <br/> |<span data-ttu-id="8ed91-111">PT_STRING8, PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="8ed91-111">PT_STRING8, PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="8ed91-112">Bereich:</span><span class="sxs-lookup"><span data-stu-id="8ed91-112">Area:</span></span>  <br/> |<span data-ttu-id="8ed91-113">E-Mail-Anlage</span><span class="sxs-lookup"><span data-stu-id="8ed91-113">Message attachment</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="8ed91-114">Hinweise</span><span class="sxs-lookup"><span data-stu-id="8ed91-114">Remarks</span></span>

<span data-ttu-id="8ed91-115">Diese Eigenschaften werden verwendet für MHTML-Unterstützung.</span><span class="sxs-lookup"><span data-stu-id="8ed91-115">These properties are used for MHTML support.</span></span> <span data-ttu-id="8ed91-116">Sie stellen die Kopfzeile Content Kennung für die entsprechenden MIME-Textkörper dar.</span><span class="sxs-lookup"><span data-stu-id="8ed91-116">They represent the content identification header for the appropriate MIME body part.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="8ed91-117">Verwandte Ressourcen</span><span class="sxs-lookup"><span data-stu-id="8ed91-117">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="8ed91-118">Protokollspezifikationen</span><span class="sxs-lookup"><span data-stu-id="8ed91-118">Protocol specifications</span></span>

<span data-ttu-id="8ed91-119">[[MS-OXCMSG]](http://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="8ed91-119">[[MS-OXCMSG]](http://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="8ed91-120">Nachrichten und Anlagen Objekte behandelt.</span><span class="sxs-lookup"><span data-stu-id="8ed91-120">Handles message and attachment objects.</span></span>
    
## <a name="header-files"></a><span data-ttu-id="8ed91-121">Header-Dateien</span><span class="sxs-lookup"><span data-stu-id="8ed91-121">Header Files</span></span>

<span data-ttu-id="8ed91-122">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="8ed91-122">Mapidefs.h</span></span>
  
> <span data-ttu-id="8ed91-123">Enthält die Datentypdefinitionen.</span><span class="sxs-lookup"><span data-stu-id="8ed91-123">Provides data type definitions.</span></span>
    
<span data-ttu-id="8ed91-124">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="8ed91-124">Mapitags.h</span></span>
  
> <span data-ttu-id="8ed91-125">Enthält Definitionen von Eigenschaften, die als Alternative Namen aufgelistet.</span><span class="sxs-lookup"><span data-stu-id="8ed91-125">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="8ed91-126">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="8ed91-126">See also</span></span>



[<span data-ttu-id="8ed91-127">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="8ed91-127">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="8ed91-128">Kanonische MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="8ed91-128">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="8ed91-129">Zuordnen von kanonischen Eigenschaftennamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="8ed91-129">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="8ed91-130">Zuordnen von MAPI-Namen zu kanonische Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="8ed91-130">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

