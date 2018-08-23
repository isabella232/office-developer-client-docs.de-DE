---
title: PidTagAttachmentFlags (kanonische Eigenschaft)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagAttachmentFlags
api_type:
- HeaderDef
ms.assetid: 42981aac-f9e7-45dd-91a2-15d9784f30aa
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 0701bb2cf08c79a69c9cd21e9acf1ce4e8ac4ee1
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2018
ms.locfileid: "22593074"
---
# <a name="pidtagattachmentflags-canonical-property"></a><span data-ttu-id="939d3-103">PidTagAttachmentFlags (kanonische Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="939d3-103">PidTagAttachmentFlags Canonical Property</span></span>

  
  
<span data-ttu-id="939d3-104">**Betrifft**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="939d3-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="939d3-105">Besondere Behandlung für diese Attachment-Objekt angibt.</span><span class="sxs-lookup"><span data-stu-id="939d3-105">Indicates special handling for this Attachment object.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="939d3-106">Zugeordnete Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="939d3-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="939d3-107">PR_ATTACHMENT_FLAGS</span><span class="sxs-lookup"><span data-stu-id="939d3-107">PR_ATTACHMENT_FLAGS</span></span>  <br/> |
|<span data-ttu-id="939d3-108">Kennung:</span><span class="sxs-lookup"><span data-stu-id="939d3-108">Identifier:</span></span>  <br/> |<span data-ttu-id="939d3-109">0x7FFD</span><span class="sxs-lookup"><span data-stu-id="939d3-109">0x7FFD</span></span>  <br/> |
|<span data-ttu-id="939d3-110">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="939d3-110">Data type:</span></span>  <br/> |<span data-ttu-id="939d3-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="939d3-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="939d3-112">Bereich:</span><span class="sxs-lookup"><span data-stu-id="939d3-112">Area:</span></span>  <br/> |<span data-ttu-id="939d3-113">Nachrichtenanlage</span><span class="sxs-lookup"><span data-stu-id="939d3-113">Message attachment</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="939d3-114">HinwBemerkungeneise</span><span class="sxs-lookup"><span data-stu-id="939d3-114">Remarks</span></span>

<span data-ttu-id="939d3-115">0 x 00000000, muss es sei denn, die durch andere Protokolle, die die Nachricht erweitern und Attachment-Objektprotokoll wie bereits erwähnt in [[MS-OXCMSG]](http://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx) außer Kraft gesetzt</span><span class="sxs-lookup"><span data-stu-id="939d3-115">Must be 0x00000000, unless overridden by other protocols that extend the Message and Attachment Object Protocol as noted in [[MS-OXCMSG]](http://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="939d3-116">Verwandte Ressourcen</span><span class="sxs-lookup"><span data-stu-id="939d3-116">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="939d3-117">Protokollspezifikationen</span><span class="sxs-lookup"><span data-stu-id="939d3-117">Protocol specifications</span></span>

<span data-ttu-id="939d3-118">[[MS-OXCMSG]](http://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="939d3-118">[[MS-OXCMSG]](http://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="939d3-119">Nachrichten und Anlagen Objekte behandelt.</span><span class="sxs-lookup"><span data-stu-id="939d3-119">Handles message and attachment objects.</span></span>
    
<span data-ttu-id="939d3-120">[[MS-OXOCAL]](http://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="939d3-120">[[MS-OXOCAL]](http://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="939d3-121">Gibt die Eigenschaften und Vorgänge für den Termin, einer Besprechungsanfrage und Antwortnachrichten.</span><span class="sxs-lookup"><span data-stu-id="939d3-121">Specifies the properties and operations for appointment, meeting request, and response messages.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="939d3-122">Header-Dateien</span><span class="sxs-lookup"><span data-stu-id="939d3-122">Header files</span></span>

<span data-ttu-id="939d3-123">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="939d3-123">Mapidefs.h</span></span>
  
> <span data-ttu-id="939d3-124">Enthält die Datentypdefinitionen.</span><span class="sxs-lookup"><span data-stu-id="939d3-124">Provides data type definitions.</span></span>
    
<span data-ttu-id="939d3-125">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="939d3-125">Mapitags.h</span></span>
  
> <span data-ttu-id="939d3-126">Enthält Definitionen von Eigenschaften, die als Alternative Namen aufgelistet.</span><span class="sxs-lookup"><span data-stu-id="939d3-126">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="939d3-127">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="939d3-127">See also</span></span>



[<span data-ttu-id="939d3-128">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="939d3-128">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="939d3-129">Kanonische MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="939d3-129">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="939d3-130">Zuordnen von kanonischen Eigenschaftennamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="939d3-130">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="939d3-131">Zuordnen von MAPI-Namen zu kanonische Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="939d3-131">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

