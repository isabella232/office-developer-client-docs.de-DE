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
ms.openlocfilehash: d5a1e4130deb04d18c73b2a8bd4b5fe947abe90a
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2018
ms.locfileid: "22577772"
---
# <a name="pidtagbodyhtml-canonical-property"></a><span data-ttu-id="72f7f-103">PidTagBodyHtml (kanonische Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="72f7f-103">PidTagBodyHtml Canonical Property</span></span>

  
  
<span data-ttu-id="72f7f-104">**Betrifft**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="72f7f-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="72f7f-105">Die Version Hypertext Markup Language (HTML), der den Nachrichtentext enthält.</span><span class="sxs-lookup"><span data-stu-id="72f7f-105">Contains the Hypertext Markup Language (HTML) version of the message text.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="72f7f-106">Zugeordnete Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="72f7f-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="72f7f-107">PR_BODY_HTML, PR_BODY_HTML_A, PR_BODY_HTML_W</span><span class="sxs-lookup"><span data-stu-id="72f7f-107">PR_BODY_HTML, PR_BODY_HTML_A, PR_BODY_HTML_W</span></span>  <br/> |
|<span data-ttu-id="72f7f-108">Kennung:</span><span class="sxs-lookup"><span data-stu-id="72f7f-108">Identifier:</span></span>  <br/> |<span data-ttu-id="72f7f-109">0x1013</span><span class="sxs-lookup"><span data-stu-id="72f7f-109">0x1013</span></span>  <br/> |
|<span data-ttu-id="72f7f-110">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="72f7f-110">Data type:</span></span>  <br/> |<span data-ttu-id="72f7f-111">PT_UNICODE PT_STRING8</span><span class="sxs-lookup"><span data-stu-id="72f7f-111">PT_UNICODE, PT_STRING8</span></span>  <br/> |
|<span data-ttu-id="72f7f-112">Bereich:</span><span class="sxs-lookup"><span data-stu-id="72f7f-112">Area:</span></span>  <br/> |<span data-ttu-id="72f7f-113">Allgemeine messaging</span><span class="sxs-lookup"><span data-stu-id="72f7f-113">General messaging</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="72f7f-114">HinwBemerkungeneise</span><span class="sxs-lookup"><span data-stu-id="72f7f-114">Remarks</span></span>

<span data-ttu-id="72f7f-115">Diese Eigenschaften enthalten den gleichen Nachrichtentext als **PR_BODY_CONTENT_LOCATION** ([PidTagBodyContentLocation](pidtagbodycontentlocation-canonical-property.md)), aber im HTML-Format.</span><span class="sxs-lookup"><span data-stu-id="72f7f-115">These properties contain the same message text as the **PR_BODY_CONTENT_LOCATION** ([PidTagBodyContentLocation](pidtagbodycontentlocation-canonical-property.md)), but in HTML.</span></span> 
  
<span data-ttu-id="72f7f-116">Ein Nachrichtenspeicher, der HTML unterstützt bedeutet dies, indem das **STORE_HTML_OK** Flag in seiner **PR_STORE_SUPPORT_MASK** ([PidTagStoreSupportMask](pidtagstoresupportmask-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="72f7f-116">A message store that supports HTML indicates this by setting the **STORE_HTML_OK** flag in its **PR_STORE_SUPPORT_MASK** ([PidTagStoreSupportMask](pidtagstoresupportmask-canonical-property.md)).</span></span> 
  
 <span data-ttu-id="72f7f-117">**Hinweis** **STORE_HTML_OK** ist in Versionen von Mapidefs.h mit Microsoft® Exchange 2000 Server und früheren Versionen enthalten nicht definiert.</span><span class="sxs-lookup"><span data-stu-id="72f7f-117">**Note** **STORE_HTML_OK** is not defined in versions of Mapidefs.h included with Microsoft® Exchange 2000 Server and earlier.</span></span> <span data-ttu-id="72f7f-118">Wenn **STORE_HTML_OK** nicht definiert ist, verwenden Sie stattdessen den Wert 0 x 00010000.</span><span class="sxs-lookup"><span data-stu-id="72f7f-118">If **STORE_HTML_OK** is undefined, use the value 0x00010000 instead.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="72f7f-119">Verwandte Ressourcen</span><span class="sxs-lookup"><span data-stu-id="72f7f-119">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="72f7f-120">Protokollspezifikationen</span><span class="sxs-lookup"><span data-stu-id="72f7f-120">Protocol specifications</span></span>

<span data-ttu-id="72f7f-121">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="72f7f-121">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="72f7f-122">Bietet Verweise auf Verwandte Exchange Server-Spezifikationen.</span><span class="sxs-lookup"><span data-stu-id="72f7f-122">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="72f7f-123">[[MS-OXCMSG]](http://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="72f7f-123">[[MS-OXCMSG]](http://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="72f7f-124">Nachrichten und Anlagen Objekte behandelt.</span><span class="sxs-lookup"><span data-stu-id="72f7f-124">Handles message and attachment objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="72f7f-125">Header-Dateien</span><span class="sxs-lookup"><span data-stu-id="72f7f-125">Header files</span></span>

<span data-ttu-id="72f7f-126">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="72f7f-126">Mapidefs.h</span></span>
  
> <span data-ttu-id="72f7f-127">Enthält die Datentypdefinitionen.</span><span class="sxs-lookup"><span data-stu-id="72f7f-127">Provides data type definitions.</span></span>
    
<span data-ttu-id="72f7f-128">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="72f7f-128">Mapitags.h</span></span>
  
> <span data-ttu-id="72f7f-129">Enthält Definitionen von Eigenschaften, die als Alternative Namen aufgelistet.</span><span class="sxs-lookup"><span data-stu-id="72f7f-129">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="72f7f-130">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="72f7f-130">See also</span></span>



[<span data-ttu-id="72f7f-131">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="72f7f-131">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="72f7f-132">Kanonische MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="72f7f-132">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="72f7f-133">Zuordnen von kanonischen Eigenschaftennamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="72f7f-133">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="72f7f-134">Zuordnen von MAPI-Namen zu kanonische Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="72f7f-134">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

