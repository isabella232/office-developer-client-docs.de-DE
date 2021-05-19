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
ms.openlocfilehash: d494f1f14daff75be55e910da56204ecb3dbcf83
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32345800"
---
# <a name="pidtagattachmentflags-canonical-property"></a><span data-ttu-id="322c3-103">PidTagAttachmentFlags (kanonische Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="322c3-103">PidTagAttachmentFlags Canonical Property</span></span>

  
  
<span data-ttu-id="322c3-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="322c3-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="322c3-105">Gibt eine spezielle Behandlung für dieses Attachment-Objekt an.</span><span class="sxs-lookup"><span data-stu-id="322c3-105">Indicates special handling for this Attachment object.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="322c3-106">Zugeordnete Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="322c3-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="322c3-107">PR_ATTACHMENT_FLAGS</span><span class="sxs-lookup"><span data-stu-id="322c3-107">PR_ATTACHMENT_FLAGS</span></span>  <br/> |
|<span data-ttu-id="322c3-108">Kennung:</span><span class="sxs-lookup"><span data-stu-id="322c3-108">Identifier:</span></span>  <br/> |<span data-ttu-id="322c3-109">0x7FFD</span><span class="sxs-lookup"><span data-stu-id="322c3-109">0x7FFD</span></span>  <br/> |
|<span data-ttu-id="322c3-110">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="322c3-110">Data type:</span></span>  <br/> |<span data-ttu-id="322c3-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="322c3-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="322c3-112">Bereich:</span><span class="sxs-lookup"><span data-stu-id="322c3-112">Area:</span></span>  <br/> |<span data-ttu-id="322c3-113">Nachrichtenanlage</span><span class="sxs-lookup"><span data-stu-id="322c3-113">Message attachment</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="322c3-114">Hinweise</span><span class="sxs-lookup"><span data-stu-id="322c3-114">Remarks</span></span>

<span data-ttu-id="322c3-115">Muss 0x00000000 werden, es sei denn, es werden andere Protokolle außer Kraft gesetzt, die das Message- und Attachment-Objektprotokoll erweitern, wie in [[MS-OXCMSG] erwähnt.](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="322c3-115">Must be 0x00000000, unless overridden by other protocols that extend the Message and Attachment Object Protocol as noted in [[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="322c3-116">Verwandte Ressourcen</span><span class="sxs-lookup"><span data-stu-id="322c3-116">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="322c3-117">Protokollspezifikationen</span><span class="sxs-lookup"><span data-stu-id="322c3-117">Protocol specifications</span></span>

<span data-ttu-id="322c3-118">[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="322c3-118">[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="322c3-119">Behandelt Nachrichten- und Anlagenobjekte.</span><span class="sxs-lookup"><span data-stu-id="322c3-119">Handles message and attachment objects.</span></span>
    
<span data-ttu-id="322c3-120">[[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="322c3-120">[[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="322c3-121">Gibt die Eigenschaften und Vorgänge für Termin-, Besprechungs- und Antwortnachrichten an.</span><span class="sxs-lookup"><span data-stu-id="322c3-121">Specifies the properties and operations for appointment, meeting request, and response messages.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="322c3-122">Headerdateien</span><span class="sxs-lookup"><span data-stu-id="322c3-122">Header files</span></span>

<span data-ttu-id="322c3-123">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="322c3-123">Mapidefs.h</span></span>
  
> <span data-ttu-id="322c3-124">Bietet Datentypdefinitionen.</span><span class="sxs-lookup"><span data-stu-id="322c3-124">Provides data type definitions.</span></span>
    
<span data-ttu-id="322c3-125">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="322c3-125">Mapitags.h</span></span>
  
> <span data-ttu-id="322c3-126">Enthält Definitionen von Eigenschaften, die als alternative Namen aufgeführt sind.</span><span class="sxs-lookup"><span data-stu-id="322c3-126">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="322c3-127">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="322c3-127">See also</span></span>



[<span data-ttu-id="322c3-128">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="322c3-128">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="322c3-129">KANONISCHE EIGENSCHAFTEN VON MAPI</span><span class="sxs-lookup"><span data-stu-id="322c3-129">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="322c3-130">Zuordnen kanonischer Eigenschaftsnamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="322c3-130">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="322c3-131">Zuordnen von MAPI-Namen zu kanonischen Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="322c3-131">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

