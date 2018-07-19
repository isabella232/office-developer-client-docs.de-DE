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
ms.openlocfilehash: 825f6f1eff94635ca2d0f5226cfc3f421d41bcce
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19794118"
---
# <a name="pidtagattachmentflags-canonical-property"></a><span data-ttu-id="088b1-103">PidTagAttachmentFlags (kanonische Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="088b1-103">PidTagAttachmentFlags Canonical Property</span></span>

  
  
<span data-ttu-id="088b1-104">**Betrifft**: Outlook</span><span class="sxs-lookup"><span data-stu-id="088b1-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="088b1-105">Besondere Behandlung für diese Attachment-Objekt angibt.</span><span class="sxs-lookup"><span data-stu-id="088b1-105">Indicates special handling for this Attachment object.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="088b1-106">Zugeordneten Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="088b1-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="088b1-107">PR_ATTACHMENT_FLAGS</span><span class="sxs-lookup"><span data-stu-id="088b1-107">PR_ATTACHMENT_FLAGS</span></span>  <br/> |
|<span data-ttu-id="088b1-108">Bezeichner:</span><span class="sxs-lookup"><span data-stu-id="088b1-108">Identifier:</span></span>  <br/> |<span data-ttu-id="088b1-109">0x7FFD</span><span class="sxs-lookup"><span data-stu-id="088b1-109">0x7FFD</span></span>  <br/> |
|<span data-ttu-id="088b1-110">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="088b1-110">Data type:</span></span>  <br/> |<span data-ttu-id="088b1-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="088b1-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="088b1-112">Bereich:</span><span class="sxs-lookup"><span data-stu-id="088b1-112">Area:</span></span>  <br/> |<span data-ttu-id="088b1-113">E-Mail-Anlage</span><span class="sxs-lookup"><span data-stu-id="088b1-113">Message attachment</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="088b1-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="088b1-114">Remarks</span></span>

<span data-ttu-id="088b1-115">0 x 00000000, muss es sei denn, die durch andere Protokolle, die die Nachricht erweitern und Attachment-Objektprotokoll wie bereits erwähnt in [[MS-OXCMSG]](http://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx) außer Kraft gesetzt</span><span class="sxs-lookup"><span data-stu-id="088b1-115">Must be 0x00000000, unless overridden by other protocols that extend the Message and Attachment Object Protocol as noted in [[MS-OXCMSG]](http://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="088b1-116">Verwandte Ressourcen</span><span class="sxs-lookup"><span data-stu-id="088b1-116">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="088b1-117">Protokollspezifikationen</span><span class="sxs-lookup"><span data-stu-id="088b1-117">Protocol specifications</span></span>

<span data-ttu-id="088b1-118">[[MS-OXCMSG]](http://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="088b1-118">[[MS-OXCMSG]](http://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="088b1-119">Nachrichten und Anlagen Objekte behandelt.</span><span class="sxs-lookup"><span data-stu-id="088b1-119">Handles message and attachment objects.</span></span>
    
<span data-ttu-id="088b1-120">[[MS-OXOCAL]](http://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="088b1-120">[[MS-OXOCAL]](http://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="088b1-121">Gibt die Eigenschaften und Vorgänge für den Termin, einer Besprechungsanfrage und Antwortnachrichten.</span><span class="sxs-lookup"><span data-stu-id="088b1-121">Specifies the properties and operations for appointment, meeting request, and response messages.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="088b1-122">Header-Dateien</span><span class="sxs-lookup"><span data-stu-id="088b1-122">Header files</span></span>

<span data-ttu-id="088b1-123">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="088b1-123">Mapidefs.h</span></span>
  
> <span data-ttu-id="088b1-124">Enthält die Datentypdefinitionen.</span><span class="sxs-lookup"><span data-stu-id="088b1-124">Provides data type definitions.</span></span>
    
<span data-ttu-id="088b1-125">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="088b1-125">Mapitags.h</span></span>
  
> <span data-ttu-id="088b1-126">Enthält Definitionen von Eigenschaften, die als Alternative Namen aufgelistet.</span><span class="sxs-lookup"><span data-stu-id="088b1-126">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="088b1-127">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="088b1-127">See also</span></span>



[<span data-ttu-id="088b1-128">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="088b1-128">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="088b1-129">Kanonische MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="088b1-129">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="088b1-130">Zuordnen von kanonischen Eigenschaftennamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="088b1-130">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="088b1-131">Zuordnen von MAPI-Namen zu kanonische Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="088b1-131">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

