---
title: Kanonische Pidtagautoforwarded (-Eigenschaft
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
ms.openlocfilehash: 25d1bb121df6470f5038a2106587e3f5b37f6bb7
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32326614"
---
# <a name="pidtagautoforwarded-canonical-property"></a><span data-ttu-id="9c0d6-103">Kanonische Pidtagautoforwarded (-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="9c0d6-103">PidTagAutoForwarded Canonical Property</span></span>

  
  
<span data-ttu-id="9c0d6-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="9c0d6-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="9c0d6-105">Enthält TRUE, wenn der Client ein Kopfzeilenfeld X-MS-Exchange-Organization-autoForward anfordert.</span><span class="sxs-lookup"><span data-stu-id="9c0d6-105">Contains TRUE if the client requests an X-MS-Exchange-Organization-AutoForwarded header field.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="9c0d6-106">Zugeordnete Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="9c0d6-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="9c0d6-107">PR_AUTO_FORWARDED</span><span class="sxs-lookup"><span data-stu-id="9c0d6-107">PR_AUTO_FORWARDED</span></span>  <br/> |
|<span data-ttu-id="9c0d6-108">Kennung:</span><span class="sxs-lookup"><span data-stu-id="9c0d6-108">Identifier:</span></span>  <br/> |<span data-ttu-id="9c0d6-109">0x0005</span><span class="sxs-lookup"><span data-stu-id="9c0d6-109">0x0005</span></span>  <br/> |
|<span data-ttu-id="9c0d6-110">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="9c0d6-110">Data type:</span></span>  <br/> |<span data-ttu-id="9c0d6-111">PT_BOOLEAN</span><span class="sxs-lookup"><span data-stu-id="9c0d6-111">PT_BOOLEAN</span></span>  <br/> |
|<span data-ttu-id="9c0d6-112">Bereich:</span><span class="sxs-lookup"><span data-stu-id="9c0d6-112">Area:</span></span>  <br/> |<span data-ttu-id="9c0d6-113">Allgemeine Berichterstellung</span><span class="sxs-lookup"><span data-stu-id="9c0d6-113">General reporting</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="9c0d6-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="9c0d6-114">Remarks</span></span>

<span data-ttu-id="9c0d6-115">Wenn diese Eigenschaft auf FALSE festgelegt oder nicht verwendet wird, wird kein X-MS-Exchange-Organization-Auto forwarded-Kopfzeilenfeld erstellt.</span><span class="sxs-lookup"><span data-stu-id="9c0d6-115">If this property is set to FALSE or not used, no X-MS-Exchange-Organization-AutoForwarded header field will be created.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="9c0d6-116">Zugehörige Ressourcen</span><span class="sxs-lookup"><span data-stu-id="9c0d6-116">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="9c0d6-117">Protokollspezifikationen</span><span class="sxs-lookup"><span data-stu-id="9c0d6-117">Protocol specifications</span></span>

<span data-ttu-id="9c0d6-118">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="9c0d6-118">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="9c0d6-119">Definiert jede Eigenschaft, die in den von MS-OXO-prefixed Documents beschriebenen Objekten verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="9c0d6-119">Defines each property that is used in the objects that are described by MS-OXO-prefixed documents.</span></span>
    
<span data-ttu-id="9c0d6-120">[[MS-OXCMAIL]](https://msdn.microsoft.com/library/b60d48db-183f-4bf5-a908-f584e62cb2d4%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="9c0d6-120">[[MS-OXCMAIL]](https://msdn.microsoft.com/library/b60d48db-183f-4bf5-a908-f584e62cb2d4%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="9c0d6-121">Konvertiert von Internet Standard-e-Mail-Konventionen in Nachrichtenobjekte.</span><span class="sxs-lookup"><span data-stu-id="9c0d6-121">Converts from Internet standard email conventions to message objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="9c0d6-122">Header Dateien</span><span class="sxs-lookup"><span data-stu-id="9c0d6-122">Header files</span></span>

<span data-ttu-id="9c0d6-123">Mapidefs. h</span><span class="sxs-lookup"><span data-stu-id="9c0d6-123">Mapidefs.h</span></span>
  
> <span data-ttu-id="9c0d6-124">Stellt Datentypdefinitionen bereit.</span><span class="sxs-lookup"><span data-stu-id="9c0d6-124">Provides data type definitions.</span></span>
    
<span data-ttu-id="9c0d6-125">Mapitags. h</span><span class="sxs-lookup"><span data-stu-id="9c0d6-125">Mapitags.h</span></span>
  
> <span data-ttu-id="9c0d6-126">Enthält Definitionen von Eigenschaften, die als Alternative Namen aufgeführt sind.</span><span class="sxs-lookup"><span data-stu-id="9c0d6-126">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="9c0d6-127">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="9c0d6-127">See also</span></span>



[<span data-ttu-id="9c0d6-128">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="9c0d6-128">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="9c0d6-129">Kanonische MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="9c0d6-129">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="9c0d6-130">Zuordnen von kanonischen Eigenschaftennamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="9c0d6-130">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="9c0d6-131">Zuordnen von MAPI-Namen zu kanonischen Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="9c0d6-131">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

