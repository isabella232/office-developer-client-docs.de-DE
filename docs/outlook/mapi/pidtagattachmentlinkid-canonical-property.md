---
title: PidTagAttachmentLinkId (kanonische Eigenschaft)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagAttachmentLinkId
api_type:
- HeaderDef
ms.assetid: 5d0daae7-248d-459f-9d96-cb949b86f590
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: cd5a6071674dce97215bbeb7027752bfcedc94ea
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2018
ms.locfileid: "22578073"
---
# <a name="pidtagattachmentlinkid-canonical-property"></a><span data-ttu-id="4f6ea-103">PidTagAttachmentLinkId (kanonische Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="4f6ea-103">PidTagAttachmentLinkId Canonical Property</span></span>

  
  
<span data-ttu-id="4f6ea-104">**Betrifft**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="4f6ea-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="4f6ea-105">Gibt den Typ des Message-Objekts mit der dieser Anlage verknüpft ist.</span><span class="sxs-lookup"><span data-stu-id="4f6ea-105">Indicates the type of Message object to which this attachment is linked.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="4f6ea-106">Zugeordnete Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="4f6ea-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="4f6ea-107">PR_ATTACHMENT_LINKID</span><span class="sxs-lookup"><span data-stu-id="4f6ea-107">PR_ATTACHMENT_LINKID</span></span>  <br/> |
|<span data-ttu-id="4f6ea-108">Kennung:</span><span class="sxs-lookup"><span data-stu-id="4f6ea-108">Identifier:</span></span>  <br/> |<span data-ttu-id="4f6ea-109">0x7FFA</span><span class="sxs-lookup"><span data-stu-id="4f6ea-109">0x7FFA</span></span>  <br/> |
|<span data-ttu-id="4f6ea-110">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="4f6ea-110">Data type:</span></span>  <br/> |<span data-ttu-id="4f6ea-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="4f6ea-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="4f6ea-112">Bereich:</span><span class="sxs-lookup"><span data-stu-id="4f6ea-112">Area:</span></span>  <br/> |<span data-ttu-id="4f6ea-113">Nachrichtenanlage</span><span class="sxs-lookup"><span data-stu-id="4f6ea-113">Message attachment</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="4f6ea-114">HinwBemerkungeneise</span><span class="sxs-lookup"><span data-stu-id="4f6ea-114">Remarks</span></span>

<span data-ttu-id="4f6ea-115">0 muss sein, es sei denn, die durch andere Protokolle, die die Nachricht erweitern und Attachment-Objektprotokoll wie bereits erwähnt in [[MS-OXCMSG]](http://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)außer Kraft gesetzt.</span><span class="sxs-lookup"><span data-stu-id="4f6ea-115">Must be 0, unless overridden by other protocols that extend the Message and Attachment Object Protocol as noted in [[MS-OXCMSG]](http://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx).</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="4f6ea-116">Verwandte Ressourcen</span><span class="sxs-lookup"><span data-stu-id="4f6ea-116">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="4f6ea-117">Protokollspezifikationen</span><span class="sxs-lookup"><span data-stu-id="4f6ea-117">Protocol specifications</span></span>

<span data-ttu-id="4f6ea-118">[[MS-OXCMSG]](http://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="4f6ea-118">[[MS-OXCMSG]](http://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="4f6ea-119">Nachrichten und Anlagen Objekte behandelt.</span><span class="sxs-lookup"><span data-stu-id="4f6ea-119">Handles message and attachment objects.</span></span>
    
<span data-ttu-id="4f6ea-120">[[MS-OXOJRNL]](http://msdn.microsoft.com/library/2aa04fd2-0f36-4ce4-9178-c0fc70aa8d43%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="4f6ea-120">[[MS-OXOJRNL]](http://msdn.microsoft.com/library/2aa04fd2-0f36-4ce4-9178-c0fc70aa8d43%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="4f6ea-121">Gibt die Eigenschaften und Operationen, die für Journal Objekte zulässig sind.</span><span class="sxs-lookup"><span data-stu-id="4f6ea-121">Specifies the properties and operations that are permissible for journal objects.</span></span>
    
<span data-ttu-id="4f6ea-122">[[MS-OXORMDR]](http://msdn.microsoft.com/library/5454ebcc-e5d1-4da8-a598-d393b101caab%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="4f6ea-122">[[MS-OXORMDR]](http://msdn.microsoft.com/library/5454ebcc-e5d1-4da8-a598-d393b101caab%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="4f6ea-123">Gibt die Eigenschaften und das Interaktionsmodell für e-Mail und anderen Objekt Erinnerungen.</span><span class="sxs-lookup"><span data-stu-id="4f6ea-123">Specifies the properties and the interaction model for email and other object reminders.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="4f6ea-124">Header-Dateien</span><span class="sxs-lookup"><span data-stu-id="4f6ea-124">Header files</span></span>

<span data-ttu-id="4f6ea-125">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="4f6ea-125">Mapidefs.h</span></span>
  
> <span data-ttu-id="4f6ea-126">Enthält die Datentypdefinitionen.</span><span class="sxs-lookup"><span data-stu-id="4f6ea-126">Provides data type definitions.</span></span>
    
<span data-ttu-id="4f6ea-127">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="4f6ea-127">Mapitags.h</span></span>
  
> <span data-ttu-id="4f6ea-128">Enthält Definitionen von Eigenschaften, die als Alternative Namen aufgelistet.</span><span class="sxs-lookup"><span data-stu-id="4f6ea-128">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="4f6ea-129">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="4f6ea-129">See also</span></span>



[<span data-ttu-id="4f6ea-130">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="4f6ea-130">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="4f6ea-131">Kanonische MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="4f6ea-131">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="4f6ea-132">Zuordnen von kanonischen Eigenschaftennamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="4f6ea-132">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="4f6ea-133">Zuordnen von MAPI-Namen zu kanonische Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="4f6ea-133">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

