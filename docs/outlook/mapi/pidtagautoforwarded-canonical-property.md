---
title: PidTagAutoForwarded (kanonische Eigenschaft)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagAutoForwarded
api_type:
- HeaderDef
ms.assetid: 1ba40cc2-ba27-4d75-9682-c536cf3a0d58
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: 8303a60ee0d61a56c79fadf471bc6111fcbde7d2
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19794133"
---
# <a name="pidtagautoforwarded-canonical-property"></a><span data-ttu-id="132c3-103">PidTagAutoForwarded (kanonische Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="132c3-103">PidTagAutoForwarded Canonical Property</span></span>

  
  
<span data-ttu-id="132c3-104">**Betrifft**: Outlook</span><span class="sxs-lookup"><span data-stu-id="132c3-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="132c3-105">Enthält True, wenn der Client eine X-MS-Exchange-Organisation-AutoForwarded Kopfzeilenfeld anfordert.</span><span class="sxs-lookup"><span data-stu-id="132c3-105">Contains TRUE if the client requests an X-MS-Exchange-Organization-AutoForwarded header field.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="132c3-106">Zugeordneten Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="132c3-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="132c3-107">PR_AUTO_FORWARDED</span><span class="sxs-lookup"><span data-stu-id="132c3-107">PR_AUTO_FORWARDED</span></span>  <br/> |
|<span data-ttu-id="132c3-108">Bezeichner:</span><span class="sxs-lookup"><span data-stu-id="132c3-108">Identifier:</span></span>  <br/> |<span data-ttu-id="132c3-109">0 x 0005</span><span class="sxs-lookup"><span data-stu-id="132c3-109">0x0005</span></span>  <br/> |
|<span data-ttu-id="132c3-110">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="132c3-110">Data type:</span></span>  <br/> |<span data-ttu-id="132c3-111">PT_BOOLEAN</span><span class="sxs-lookup"><span data-stu-id="132c3-111">PT_BOOLEAN</span></span>  <br/> |
|<span data-ttu-id="132c3-112">Bereich:</span><span class="sxs-lookup"><span data-stu-id="132c3-112">Area:</span></span>  <br/> |<span data-ttu-id="132c3-113">Allgemeine Berichterstattung</span><span class="sxs-lookup"><span data-stu-id="132c3-113">General reporting</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="132c3-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="132c3-114">Remarks</span></span>

<span data-ttu-id="132c3-115">Wenn diese Eigenschaft FALSE oder nicht verwendeten gesetzt ist, werden keine X-MS-Exchange-Organisation-AutoForwarded Kopfzeilenfeld erstellt.</span><span class="sxs-lookup"><span data-stu-id="132c3-115">If this property is set to FALSE or not used, no X-MS-Exchange-Organization-AutoForwarded header field will be created.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="132c3-116">Verwandte Ressourcen</span><span class="sxs-lookup"><span data-stu-id="132c3-116">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="132c3-117">Protokollspezifikationen</span><span class="sxs-lookup"><span data-stu-id="132c3-117">Protocol specifications</span></span>

<span data-ttu-id="132c3-118">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="132c3-118">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="132c3-119">Definiert jede Eigenschaft, die verwendet wird, in die Objekte, die durch MS-OXO-Präfix Dokumente beschrieben werden.</span><span class="sxs-lookup"><span data-stu-id="132c3-119">Defines each property that is used in the objects that are described by MS-OXO-prefixed documents.</span></span>
    
<span data-ttu-id="132c3-120">[[MS-OXCMAIL]](http://msdn.microsoft.com/library/b60d48db-183f-4bf5-a908-f584e62cb2d4%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="132c3-120">[[MS-OXCMAIL]](http://msdn.microsoft.com/library/b60d48db-183f-4bf5-a908-f584e62cb2d4%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="132c3-121">Konvertiert von Internet-standard-e-Mail-Konventionen in Message-Objekten.</span><span class="sxs-lookup"><span data-stu-id="132c3-121">Converts from Internet standard email conventions to message objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="132c3-122">Header-Dateien</span><span class="sxs-lookup"><span data-stu-id="132c3-122">Header files</span></span>

<span data-ttu-id="132c3-123">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="132c3-123">Mapidefs.h</span></span>
  
> <span data-ttu-id="132c3-124">Enthält die Datentypdefinitionen.</span><span class="sxs-lookup"><span data-stu-id="132c3-124">Provides data type definitions.</span></span>
    
<span data-ttu-id="132c3-125">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="132c3-125">Mapitags.h</span></span>
  
> <span data-ttu-id="132c3-126">Enthält Definitionen von Eigenschaften, die als Alternative Namen aufgelistet.</span><span class="sxs-lookup"><span data-stu-id="132c3-126">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="132c3-127">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="132c3-127">See also</span></span>



[<span data-ttu-id="132c3-128">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="132c3-128">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="132c3-129">Kanonische MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="132c3-129">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="132c3-130">Zuordnen von kanonischen Eigenschaftennamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="132c3-130">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="132c3-131">Zuordnen von MAPI-Namen zu kanonische Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="132c3-131">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

