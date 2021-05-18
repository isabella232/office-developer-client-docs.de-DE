---
title: PidTagBodyHtml (kanonische Eigenschaft)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagBodyHtml
api_type:
- HeaderDef
ms.assetid: 93b9215a-5900-411c-a0ae-6bba62cd5a1e
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 6ed59228ee06a1d3e362115a99bf4b859dfeb698
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32359045"
---
# <a name="pidtagbodyhtml-canonical-property"></a><span data-ttu-id="4a09e-103">PidTagBodyHtml (kanonische Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="4a09e-103">PidTagBodyHtml Canonical Property</span></span>

  
  
<span data-ttu-id="4a09e-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="4a09e-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="4a09e-105">Enthält die Hypertext Markup Language (HTML)-Version des Nachrichtentexts.</span><span class="sxs-lookup"><span data-stu-id="4a09e-105">Contains the Hypertext Markup Language (HTML) version of the message text.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="4a09e-106">Zugeordnete Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="4a09e-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="4a09e-107">PR_BODY_HTML, PR_BODY_HTML_A, PR_BODY_HTML_W</span><span class="sxs-lookup"><span data-stu-id="4a09e-107">PR_BODY_HTML, PR_BODY_HTML_A, PR_BODY_HTML_W</span></span>  <br/> |
|<span data-ttu-id="4a09e-108">Kennung:</span><span class="sxs-lookup"><span data-stu-id="4a09e-108">Identifier:</span></span>  <br/> |<span data-ttu-id="4a09e-109">0x1013</span><span class="sxs-lookup"><span data-stu-id="4a09e-109">0x1013</span></span>  <br/> |
|<span data-ttu-id="4a09e-110">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="4a09e-110">Data type:</span></span>  <br/> |<span data-ttu-id="4a09e-111">PT_UNICODE, PT_STRING8</span><span class="sxs-lookup"><span data-stu-id="4a09e-111">PT_UNICODE, PT_STRING8</span></span>  <br/> |
|<span data-ttu-id="4a09e-112">Bereich:</span><span class="sxs-lookup"><span data-stu-id="4a09e-112">Area:</span></span>  <br/> |<span data-ttu-id="4a09e-113">Allgemeines Messaging</span><span class="sxs-lookup"><span data-stu-id="4a09e-113">General messaging</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="4a09e-114">Hinweise</span><span class="sxs-lookup"><span data-stu-id="4a09e-114">Remarks</span></span>

<span data-ttu-id="4a09e-115">Diese Eigenschaften enthalten denselben Nachrichtentext wie PR_BODY_CONTENT_LOCATION **(** [PidTagBodyContentLocation](pidtagbodycontentlocation-canonical-property.md)), aber in HTML.</span><span class="sxs-lookup"><span data-stu-id="4a09e-115">These properties contain the same message text as the **PR_BODY_CONTENT_LOCATION** ([PidTagBodyContentLocation](pidtagbodycontentlocation-canonical-property.md)), but in HTML.</span></span> 
  
<span data-ttu-id="4a09e-116">Ein Nachrichtenspeicher, der HTML unterstützt, gibt dies **an,** indem STORE_HTML_OK in der PR_STORE_SUPPORT_MASK **(** [PidTagStoreSupportMask](pidtagstoresupportmask-canonical-property.md)) festlegen.</span><span class="sxs-lookup"><span data-stu-id="4a09e-116">A message store that supports HTML indicates this by setting the **STORE_HTML_OK** flag in its **PR_STORE_SUPPORT_MASK** ([PidTagStoreSupportMask](pidtagstoresupportmask-canonical-property.md)).</span></span> 
  
 <span data-ttu-id="4a09e-117">**Hinweis** **STORE_HTML_OK** ist nicht in Versionen von Mapidefs.h definiert, die in Microsoft® Exchange 2000 Server und früheren Versionen enthalten sind.</span><span class="sxs-lookup"><span data-stu-id="4a09e-117">**Note** **STORE_HTML_OK** is not defined in versions of Mapidefs.h included with Microsoft® Exchange 2000 Server and earlier.</span></span> <span data-ttu-id="4a09e-118">Wenn **STORE_HTML_OK** nicht definiert ist, verwenden Sie stattdessen den Wert 0x00010000.</span><span class="sxs-lookup"><span data-stu-id="4a09e-118">If **STORE_HTML_OK** is undefined, use the value 0x00010000 instead.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="4a09e-119">Verwandte Ressourcen</span><span class="sxs-lookup"><span data-stu-id="4a09e-119">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="4a09e-120">Protokollspezifikationen</span><span class="sxs-lookup"><span data-stu-id="4a09e-120">Protocol specifications</span></span>

<span data-ttu-id="4a09e-121">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="4a09e-121">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="4a09e-122">Enthält Verweise auf Exchange Server Protokollspezifikationen.</span><span class="sxs-lookup"><span data-stu-id="4a09e-122">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="4a09e-123">[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="4a09e-123">[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="4a09e-124">Behandelt Nachrichten- und Anlagenobjekte.</span><span class="sxs-lookup"><span data-stu-id="4a09e-124">Handles message and attachment objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="4a09e-125">Headerdateien</span><span class="sxs-lookup"><span data-stu-id="4a09e-125">Header files</span></span>

<span data-ttu-id="4a09e-126">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="4a09e-126">Mapidefs.h</span></span>
  
> <span data-ttu-id="4a09e-127">Bietet Datentypdefinitionen.</span><span class="sxs-lookup"><span data-stu-id="4a09e-127">Provides data type definitions.</span></span>
    
<span data-ttu-id="4a09e-128">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="4a09e-128">Mapitags.h</span></span>
  
> <span data-ttu-id="4a09e-129">Enthält Definitionen von Eigenschaften, die als alternative Namen aufgeführt sind.</span><span class="sxs-lookup"><span data-stu-id="4a09e-129">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="4a09e-130">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="4a09e-130">See also</span></span>



[<span data-ttu-id="4a09e-131">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="4a09e-131">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="4a09e-132">KANONISCHE EIGENSCHAFTEN VON MAPI</span><span class="sxs-lookup"><span data-stu-id="4a09e-132">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="4a09e-133">Zuordnen kanonischer Eigenschaftsnamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="4a09e-133">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="4a09e-134">Zuordnen von MAPI-Namen zu kanonischen Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="4a09e-134">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

