---
title: PidTagAttachContentId (kanonische Eigenschaft)
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
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 5fc7360e3070ed4d20be7ac0155ebdcb04cf2048
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/04/2018
ms.locfileid: "25396953"
---
# <a name="pidtagattachcontentid-canonical-property"></a><span data-ttu-id="0a305-103">PidTagAttachContentId (kanonische Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="0a305-103">PidTagAttachContentId Canonical Property</span></span>

  
  
<span data-ttu-id="0a305-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="0a305-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="0a305-105">Header Content Identification Multipurpose Internet Mail Extensions (MIME) e-Mail-Anlagen enthält.</span><span class="sxs-lookup"><span data-stu-id="0a305-105">Contains the content identification header of a Multipurpose Internet Mail Extensions (MIME) message attachment.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="0a305-106">Zugeordnete Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="0a305-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="0a305-107">PR_ATTACH_CONTENT_ID, PR_ATTACH_CONTENT_ID_A, PR_ATTACH_CONTENT_ID_W</span><span class="sxs-lookup"><span data-stu-id="0a305-107">PR_ATTACH_CONTENT_ID, PR_ATTACH_CONTENT_ID_A, PR_ATTACH_CONTENT_ID_W</span></span>  <br/> |
|<span data-ttu-id="0a305-108">Kennung:</span><span class="sxs-lookup"><span data-stu-id="0a305-108">Identifier:</span></span>  <br/> |<span data-ttu-id="0a305-109">0x3712</span><span class="sxs-lookup"><span data-stu-id="0a305-109">0x3712</span></span>  <br/> |
|<span data-ttu-id="0a305-110">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="0a305-110">Data type:</span></span>  <br/> |<span data-ttu-id="0a305-111">PT_STRING8, PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="0a305-111">PT_STRING8, PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="0a305-112">Bereich:</span><span class="sxs-lookup"><span data-stu-id="0a305-112">Area:</span></span>  <br/> |<span data-ttu-id="0a305-113">Nachrichtenanlage</span><span class="sxs-lookup"><span data-stu-id="0a305-113">Message attachment</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="0a305-114">Hinweise</span><span class="sxs-lookup"><span data-stu-id="0a305-114">Remarks</span></span>

<span data-ttu-id="0a305-115">Diese Eigenschaften werden verwendet für MHTML-Unterstützung.</span><span class="sxs-lookup"><span data-stu-id="0a305-115">These properties are used for MHTML support.</span></span> <span data-ttu-id="0a305-116">Sie stellen die Kopfzeile Content Kennung für die entsprechenden MIME-Textkörper dar.</span><span class="sxs-lookup"><span data-stu-id="0a305-116">They represent the content identification header for the appropriate MIME body part.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="0a305-117">Verwandte Ressourcen</span><span class="sxs-lookup"><span data-stu-id="0a305-117">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="0a305-118">Protokollspezifikationen</span><span class="sxs-lookup"><span data-stu-id="0a305-118">Protocol specifications</span></span>

<span data-ttu-id="0a305-119">[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="0a305-119">[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="0a305-120">Nachrichten und Anlagen Objekte behandelt.</span><span class="sxs-lookup"><span data-stu-id="0a305-120">Handles message and attachment objects.</span></span>
    
## <a name="header-files"></a><span data-ttu-id="0a305-121">Header-Dateien</span><span class="sxs-lookup"><span data-stu-id="0a305-121">Header Files</span></span>

<span data-ttu-id="0a305-122">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="0a305-122">Mapidefs.h</span></span>
  
> <span data-ttu-id="0a305-123">Enthält die Datentypdefinitionen.</span><span class="sxs-lookup"><span data-stu-id="0a305-123">Provides data type definitions.</span></span>
    
<span data-ttu-id="0a305-124">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="0a305-124">Mapitags.h</span></span>
  
> <span data-ttu-id="0a305-125">Enthält Definitionen von Eigenschaften, die als Alternative Namen aufgelistet.</span><span class="sxs-lookup"><span data-stu-id="0a305-125">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="0a305-126">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="0a305-126">See also</span></span>



[<span data-ttu-id="0a305-127">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="0a305-127">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="0a305-128">Kanonische MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="0a305-128">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="0a305-129">Zuordnen von kanonischen Eigenschaftennamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="0a305-129">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="0a305-130">Zuordnen von MAPI-Namen zu kanonische Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="0a305-130">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

