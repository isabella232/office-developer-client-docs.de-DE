---
title: PidTagBodyContentLocation (kanonische Eigenschaft)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagBodyContentLocation
api_type:
- HeaderDef
ms.assetid: a66d1c64-5c5a-4980-9acd-72448108fd2c
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 4b10daf3bdc11d406b6f7248fd6aaa9e3c6c2a68
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2018
ms.locfileid: "22584716"
---
# <a name="pidtagbodycontentlocation-canonical-property"></a><span data-ttu-id="0f4ce-103">PidTagBodyContentLocation (kanonische Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="0f4ce-103">PidTagBodyContentLocation Canonical Property</span></span>

  
  
<span data-ttu-id="0f4ce-104">**Betrifft**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="0f4ce-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="0f4ce-105">Enthält den Wert eines Felds der MIME-Content-Location-Header.</span><span class="sxs-lookup"><span data-stu-id="0f4ce-105">Contains the value of a MIME Content-Location header field.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="0f4ce-106">Zugeordnete Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="0f4ce-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="0f4ce-107">PR_BODY_CONTENT_LOCATION, PR_BODY_CONTENT_LOCATION_A, PR_BODY_CONTENT_LOCATION_W</span><span class="sxs-lookup"><span data-stu-id="0f4ce-107">PR_BODY_CONTENT_LOCATION, PR_BODY_CONTENT_LOCATION_A, PR_BODY_CONTENT_LOCATION_W</span></span>  <br/> |
|<span data-ttu-id="0f4ce-108">Kennung:</span><span class="sxs-lookup"><span data-stu-id="0f4ce-108">Identifier:</span></span>  <br/> |<span data-ttu-id="0f4ce-109">0x1014</span><span class="sxs-lookup"><span data-stu-id="0f4ce-109">0x1014</span></span>  <br/> |
|<span data-ttu-id="0f4ce-110">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="0f4ce-110">Data type:</span></span>  <br/> |<span data-ttu-id="0f4ce-111">PT_STRING8, PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="0f4ce-111">PT_STRING8, PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="0f4ce-112">Bereich:</span><span class="sxs-lookup"><span data-stu-id="0f4ce-112">Area:</span></span>  <br/> |<span data-ttu-id="0f4ce-113">MIME</span><span class="sxs-lookup"><span data-stu-id="0f4ce-113">MIME</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="0f4ce-114">HinwBemerkungeneise</span><span class="sxs-lookup"><span data-stu-id="0f4ce-114">Remarks</span></span>

<span data-ttu-id="0f4ce-115">Wenn den Wert dieser Eigenschaften festlegen möchten, sollte MIME-Clients den gewünschten Wert in ein Kopfzeilenfeld Content-Location auf eine Entität MIME-geschrieben werden, die Textkörper einer Nachricht zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="0f4ce-115">To set the value of these properties, MIME clients should write the desired value to a Content-Location header field on a MIME entity that maps to a message body.</span></span>
  
<span data-ttu-id="0f4ce-116">MIME-Leser sollten auf den Wert dieser Eigenschaften den Wert eines Felds Header Content-Location auf solchen eine MIME-Entität kopieren.</span><span class="sxs-lookup"><span data-stu-id="0f4ce-116">MIME readers should copy the value of a Content-Location header field on such a MIME entity to the value of these properties.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="0f4ce-117">Verwandte Ressourcen</span><span class="sxs-lookup"><span data-stu-id="0f4ce-117">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="0f4ce-118">Protokollspezifikationen</span><span class="sxs-lookup"><span data-stu-id="0f4ce-118">Protocol specifications</span></span>

<span data-ttu-id="0f4ce-119">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="0f4ce-119">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="0f4ce-120">Bietet Verweise auf Verwandte Exchange Server-Spezifikationen.</span><span class="sxs-lookup"><span data-stu-id="0f4ce-120">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="0f4ce-121">[[MS-OXCMAIL]](http://msdn.microsoft.com/library/b60d48db-183f-4bf5-a908-f584e62cb2d4%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="0f4ce-121">[[MS-OXCMAIL]](http://msdn.microsoft.com/library/b60d48db-183f-4bf5-a908-f584e62cb2d4%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="0f4ce-122">Konvertiert von Internet-standard-e-Mail-Konventionen in Message-Objekten.</span><span class="sxs-lookup"><span data-stu-id="0f4ce-122">Converts from Internet standard email conventions to message objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="0f4ce-123">Header-Dateien</span><span class="sxs-lookup"><span data-stu-id="0f4ce-123">Header files</span></span>

<span data-ttu-id="0f4ce-124">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="0f4ce-124">Mapidefs.h</span></span>
  
> <span data-ttu-id="0f4ce-125">Enthält die Datentypdefinitionen.</span><span class="sxs-lookup"><span data-stu-id="0f4ce-125">Provides data type definitions.</span></span>
    
<span data-ttu-id="0f4ce-126">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="0f4ce-126">Mapitags.h</span></span>
  
> <span data-ttu-id="0f4ce-127">Enthält Definitionen von Eigenschaften, die als Alternative Namen aufgelistet.</span><span class="sxs-lookup"><span data-stu-id="0f4ce-127">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="0f4ce-128">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="0f4ce-128">See also</span></span>



[<span data-ttu-id="0f4ce-129">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="0f4ce-129">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="0f4ce-130">Kanonische MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="0f4ce-130">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="0f4ce-131">Zuordnen von kanonischen Eigenschaftennamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="0f4ce-131">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="0f4ce-132">Zuordnen von MAPI-Namen zu kanonische Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="0f4ce-132">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

