---
title: Kanonische Pidtagbodycontentlocation (-Eigenschaft
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
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: 90a873174b5b990f165d0b2173efa38fc7df2d9d
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32350939"
---
# <a name="pidtagbodycontentlocation-canonical-property"></a><span data-ttu-id="5552c-103">Kanonische Pidtagbodycontentlocation (-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="5552c-103">PidTagBodyContentLocation Canonical Property</span></span>

  
  
<span data-ttu-id="5552c-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="5552c-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="5552c-105">Enthält den Wert eines MIME-Inhalts-Location-Kopfzeilenfelds.</span><span class="sxs-lookup"><span data-stu-id="5552c-105">Contains the value of a MIME Content-Location header field.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="5552c-106">Zugeordnete Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="5552c-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="5552c-107">PR_BODY_CONTENT_LOCATION, PR_BODY_CONTENT_LOCATION_A, PR_BODY_CONTENT_LOCATION_W</span><span class="sxs-lookup"><span data-stu-id="5552c-107">PR_BODY_CONTENT_LOCATION, PR_BODY_CONTENT_LOCATION_A, PR_BODY_CONTENT_LOCATION_W</span></span>  <br/> |
|<span data-ttu-id="5552c-108">Kennung:</span><span class="sxs-lookup"><span data-stu-id="5552c-108">Identifier:</span></span>  <br/> |<span data-ttu-id="5552c-109">0x1014</span><span class="sxs-lookup"><span data-stu-id="5552c-109">0x1014</span></span>  <br/> |
|<span data-ttu-id="5552c-110">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="5552c-110">Data type:</span></span>  <br/> |<span data-ttu-id="5552c-111">PT_STRING8, PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="5552c-111">PT_STRING8, PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="5552c-112">Bereich:</span><span class="sxs-lookup"><span data-stu-id="5552c-112">Area:</span></span>  <br/> |<span data-ttu-id="5552c-113">MIME</span><span class="sxs-lookup"><span data-stu-id="5552c-113">MIME</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="5552c-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="5552c-114">Remarks</span></span>

<span data-ttu-id="5552c-115">Um den Wert dieser Eigenschaften festzulegen, sollten MIME-Clients den gewünschten Wert in ein Content-Location-Kopfzeilenfeld einer MIME-Entität schreiben, die einem Nachrichtentext zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="5552c-115">To set the value of these properties, MIME clients should write the desired value to a Content-Location header field on a MIME entity that maps to a message body.</span></span>
  
<span data-ttu-id="5552c-116">MIME-Leser sollten den Wert eines Content-Location-Kopfzeilenfelds für eine solche MIME-Entität in den Wert dieser Eigenschaften kopieren.</span><span class="sxs-lookup"><span data-stu-id="5552c-116">MIME readers should copy the value of a Content-Location header field on such a MIME entity to the value of these properties.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="5552c-117">Zugehörige Ressourcen</span><span class="sxs-lookup"><span data-stu-id="5552c-117">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="5552c-118">Protokollspezifikationen</span><span class="sxs-lookup"><span data-stu-id="5552c-118">Protocol specifications</span></span>

<span data-ttu-id="5552c-119">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="5552c-119">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="5552c-120">Enthält Verweise auf zugehörige Exchange Server-Protokollspezifikationen.</span><span class="sxs-lookup"><span data-stu-id="5552c-120">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="5552c-121">[[MS-OXCMAIL]](https://msdn.microsoft.com/library/b60d48db-183f-4bf5-a908-f584e62cb2d4%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="5552c-121">[[MS-OXCMAIL]](https://msdn.microsoft.com/library/b60d48db-183f-4bf5-a908-f584e62cb2d4%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="5552c-122">Konvertiert von Internet Standard-e-Mail-Konventionen in Nachrichtenobjekte.</span><span class="sxs-lookup"><span data-stu-id="5552c-122">Converts from Internet standard email conventions to message objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="5552c-123">Header Dateien</span><span class="sxs-lookup"><span data-stu-id="5552c-123">Header files</span></span>

<span data-ttu-id="5552c-124">Mapidefs. h</span><span class="sxs-lookup"><span data-stu-id="5552c-124">Mapidefs.h</span></span>
  
> <span data-ttu-id="5552c-125">Stellt Datentypdefinitionen bereit.</span><span class="sxs-lookup"><span data-stu-id="5552c-125">Provides data type definitions.</span></span>
    
<span data-ttu-id="5552c-126">Mapitags. h</span><span class="sxs-lookup"><span data-stu-id="5552c-126">Mapitags.h</span></span>
  
> <span data-ttu-id="5552c-127">Enthält Definitionen von Eigenschaften, die als Alternative Namen aufgeführt sind.</span><span class="sxs-lookup"><span data-stu-id="5552c-127">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="5552c-128">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="5552c-128">See also</span></span>



[<span data-ttu-id="5552c-129">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="5552c-129">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="5552c-130">Kanonische MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="5552c-130">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="5552c-131">Zuordnen von kanonischen Eigenschaftennamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="5552c-131">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="5552c-132">Zuordnen von MAPI-Namen zu kanonischen Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="5552c-132">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

