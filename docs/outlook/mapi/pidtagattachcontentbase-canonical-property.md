---
title: PidTagAttachContentBase (kanonische Eigenschaft)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagAttachContentBase
api_type:
- HeaderDef
ms.assetid: 35c10264-6998-4c46-8cef-82708c96d9c7
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: cff0e2a5ffdb3b85e73b24ec8a30b7d88637ce48
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19794082"
---
# <a name="pidtagattachcontentbase-canonical-property"></a><span data-ttu-id="310a1-103">PidTagAttachContentBase (kanonische Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="310a1-103">PidTagAttachContentBase Canonical Property</span></span>

  
  
<span data-ttu-id="310a1-104">**Betrifft**: Outlook</span><span class="sxs-lookup"><span data-stu-id="310a1-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="310a1-105">Die Inhalte base Kopfzeile der e-Mail-Anlagen Multipurpose Internet Mail Extensions (MIME) enthält.</span><span class="sxs-lookup"><span data-stu-id="310a1-105">Contains the content base header of a Multipurpose Internet Mail Extensions (MIME) message attachment.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="310a1-106">Zugeordneten Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="310a1-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="310a1-107">PR_ATTACH_CONTENT_BASE, PR_ATTACH_CONTENT_BASE_A, PR_ATTACH_CONTENT_BASE_W</span><span class="sxs-lookup"><span data-stu-id="310a1-107">PR_ATTACH_CONTENT_BASE, PR_ATTACH_CONTENT_BASE_A, PR_ATTACH_CONTENT_BASE_W</span></span>  <br/> |
|<span data-ttu-id="310a1-108">Bezeichner:</span><span class="sxs-lookup"><span data-stu-id="310a1-108">Identifier:</span></span>  <br/> |<span data-ttu-id="310a1-109">0x3711</span><span class="sxs-lookup"><span data-stu-id="310a1-109">0x3711</span></span>  <br/> |
|<span data-ttu-id="310a1-110">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="310a1-110">Data type:</span></span>  <br/> |<span data-ttu-id="310a1-111">PT_STRING8, PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="310a1-111">PT_STRING8, PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="310a1-112">Bereich:</span><span class="sxs-lookup"><span data-stu-id="310a1-112">Area:</span></span>  <br/> |<span data-ttu-id="310a1-113">E-Mail-Anlage</span><span class="sxs-lookup"><span data-stu-id="310a1-113">Message attachment</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="310a1-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="310a1-114">Remarks</span></span>

<span data-ttu-id="310a1-115">Diese Eigenschaften werden verwendet für MHTML-Unterstützung.</span><span class="sxs-lookup"><span data-stu-id="310a1-115">These properties are used for MHTML support.</span></span> <span data-ttu-id="310a1-116">Sie stellen die base Content Kopfzeile für den entsprechenden MIME Textteil dar.</span><span class="sxs-lookup"><span data-stu-id="310a1-116">They represent the content base header for the appropriate MIME body part.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="310a1-117">Verwandte Ressourcen</span><span class="sxs-lookup"><span data-stu-id="310a1-117">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="310a1-118">Protokollspezifikationen</span><span class="sxs-lookup"><span data-stu-id="310a1-118">Protocol specifications</span></span>

<span data-ttu-id="310a1-119">[[MS-OXCMSG]](http://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="310a1-119">[[MS-OXCMSG]](http://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="310a1-120">Nachrichten und Anlagen Objekte behandelt.</span><span class="sxs-lookup"><span data-stu-id="310a1-120">Handles message and attachment objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="310a1-121">Header-Dateien</span><span class="sxs-lookup"><span data-stu-id="310a1-121">Header files</span></span>

<span data-ttu-id="310a1-122">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="310a1-122">Mapidefs.h</span></span>
  
> <span data-ttu-id="310a1-123">Enthält die Datentypdefinitionen.</span><span class="sxs-lookup"><span data-stu-id="310a1-123">Provides data type definitions.</span></span>
    
<span data-ttu-id="310a1-124">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="310a1-124">Mapitags.h</span></span>
  
> <span data-ttu-id="310a1-125">Enthält Definitionen von Eigenschaften, die als Alternative Namen aufgelistet.</span><span class="sxs-lookup"><span data-stu-id="310a1-125">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="310a1-126">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="310a1-126">See also</span></span>



[<span data-ttu-id="310a1-127">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="310a1-127">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="310a1-128">Kanonische MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="310a1-128">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="310a1-129">Zuordnen von kanonischen Eigenschaftennamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="310a1-129">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="310a1-130">Zuordnen von MAPI-Namen zu kanonische Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="310a1-130">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

