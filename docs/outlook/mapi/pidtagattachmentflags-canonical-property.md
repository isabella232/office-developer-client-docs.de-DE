---
title: Kanonische Pidtagattachmentflags (-Eigenschaft
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
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: d494f1f14daff75be55e910da56204ecb3dbcf83
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32345800"
---
# <a name="pidtagattachmentflags-canonical-property"></a><span data-ttu-id="744e5-103">Kanonische Pidtagattachmentflags (-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="744e5-103">PidTagAttachmentFlags Canonical Property</span></span>

  
  
<span data-ttu-id="744e5-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="744e5-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="744e5-105">Gibt eine spezielle Behandlung für dieses Attachment-Objekt an.</span><span class="sxs-lookup"><span data-stu-id="744e5-105">Indicates special handling for this Attachment object.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="744e5-106">Zugeordnete Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="744e5-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="744e5-107">PR_ATTACHMENT_FLAGS</span><span class="sxs-lookup"><span data-stu-id="744e5-107">PR_ATTACHMENT_FLAGS</span></span>  <br/> |
|<span data-ttu-id="744e5-108">Kennung:</span><span class="sxs-lookup"><span data-stu-id="744e5-108">Identifier:</span></span>  <br/> |<span data-ttu-id="744e5-109">0x7FFD</span><span class="sxs-lookup"><span data-stu-id="744e5-109">0x7FFD</span></span>  <br/> |
|<span data-ttu-id="744e5-110">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="744e5-110">Data type:</span></span>  <br/> |<span data-ttu-id="744e5-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="744e5-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="744e5-112">Bereich:</span><span class="sxs-lookup"><span data-stu-id="744e5-112">Area:</span></span>  <br/> |<span data-ttu-id="744e5-113">Nachrichtenanlage</span><span class="sxs-lookup"><span data-stu-id="744e5-113">Message attachment</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="744e5-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="744e5-114">Remarks</span></span>

<span data-ttu-id="744e5-115">Muss 0x00000000 sein, es sei denn, Sie werden von anderen Protokollen außer Kraft gesetzt, die das Protokoll der Nachricht und des Attachment-Objekts gemäß [[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx) erweitern.</span><span class="sxs-lookup"><span data-stu-id="744e5-115">Must be 0x00000000, unless overridden by other protocols that extend the Message and Attachment Object Protocol as noted in [[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="744e5-116">Zugehörige Ressourcen</span><span class="sxs-lookup"><span data-stu-id="744e5-116">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="744e5-117">Protokollspezifikationen</span><span class="sxs-lookup"><span data-stu-id="744e5-117">Protocol specifications</span></span>

<span data-ttu-id="744e5-118">[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="744e5-118">[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="744e5-119">Verarbeitet Nachrichten-und Anlagenobjekte.</span><span class="sxs-lookup"><span data-stu-id="744e5-119">Handles message and attachment objects.</span></span>
    
<span data-ttu-id="744e5-120">[[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="744e5-120">[[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="744e5-121">Gibt die Eigenschaften und Vorgänge für Termin-, Besprechungs-und Antwortnachrichten an.</span><span class="sxs-lookup"><span data-stu-id="744e5-121">Specifies the properties and operations for appointment, meeting request, and response messages.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="744e5-122">Header Dateien</span><span class="sxs-lookup"><span data-stu-id="744e5-122">Header files</span></span>

<span data-ttu-id="744e5-123">Mapidefs. h</span><span class="sxs-lookup"><span data-stu-id="744e5-123">Mapidefs.h</span></span>
  
> <span data-ttu-id="744e5-124">Stellt Datentypdefinitionen bereit.</span><span class="sxs-lookup"><span data-stu-id="744e5-124">Provides data type definitions.</span></span>
    
<span data-ttu-id="744e5-125">Mapitags. h</span><span class="sxs-lookup"><span data-stu-id="744e5-125">Mapitags.h</span></span>
  
> <span data-ttu-id="744e5-126">Enthält Definitionen von Eigenschaften, die als Alternative Namen aufgeführt sind.</span><span class="sxs-lookup"><span data-stu-id="744e5-126">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="744e5-127">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="744e5-127">See also</span></span>



[<span data-ttu-id="744e5-128">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="744e5-128">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="744e5-129">Kanonische MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="744e5-129">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="744e5-130">Zuordnen von kanonischen Eigenschaftennamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="744e5-130">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="744e5-131">Zuordnen von MAPI-Namen zu kanonischen Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="744e5-131">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

