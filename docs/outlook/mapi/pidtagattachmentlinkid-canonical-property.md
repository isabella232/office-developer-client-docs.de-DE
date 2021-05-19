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
ms.openlocfilehash: 623b4195b7128667b9aaa6bc97d03c21d62c690a
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32345696"
---
# <a name="pidtagattachmentlinkid-canonical-property"></a><span data-ttu-id="0eadc-103">PidTagAttachmentLinkId (kanonische Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="0eadc-103">PidTagAttachmentLinkId Canonical Property</span></span>

  
  
<span data-ttu-id="0eadc-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="0eadc-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="0eadc-105">Gibt den Typ des Message-Objekts an, mit dem diese Anlage verknüpft ist.</span><span class="sxs-lookup"><span data-stu-id="0eadc-105">Indicates the type of Message object to which this attachment is linked.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="0eadc-106">Zugeordnete Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="0eadc-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="0eadc-107">PR_ATTACHMENT_LINKID</span><span class="sxs-lookup"><span data-stu-id="0eadc-107">PR_ATTACHMENT_LINKID</span></span>  <br/> |
|<span data-ttu-id="0eadc-108">Kennung:</span><span class="sxs-lookup"><span data-stu-id="0eadc-108">Identifier:</span></span>  <br/> |<span data-ttu-id="0eadc-109">0x7FFA</span><span class="sxs-lookup"><span data-stu-id="0eadc-109">0x7FFA</span></span>  <br/> |
|<span data-ttu-id="0eadc-110">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="0eadc-110">Data type:</span></span>  <br/> |<span data-ttu-id="0eadc-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="0eadc-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="0eadc-112">Bereich:</span><span class="sxs-lookup"><span data-stu-id="0eadc-112">Area:</span></span>  <br/> |<span data-ttu-id="0eadc-113">Nachrichtenanlage</span><span class="sxs-lookup"><span data-stu-id="0eadc-113">Message attachment</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="0eadc-114">Hinweise</span><span class="sxs-lookup"><span data-stu-id="0eadc-114">Remarks</span></span>

<span data-ttu-id="0eadc-115">Muss 0 sein, es sei denn, es wird durch andere Protokolle außer Kraft gesetzt, die das Message- und Attachment-Objektprotokoll erweitern, wie in [[MS-OXCMSG] angegeben.](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="0eadc-115">Must be 0, unless overridden by other protocols that extend the Message and Attachment Object Protocol as noted in [[MS-OXCMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx).</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="0eadc-116">Verwandte Ressourcen</span><span class="sxs-lookup"><span data-stu-id="0eadc-116">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="0eadc-117">Protokollspezifikationen</span><span class="sxs-lookup"><span data-stu-id="0eadc-117">Protocol specifications</span></span>

<span data-ttu-id="0eadc-118">[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="0eadc-118">[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="0eadc-119">Behandelt Nachrichten- und Anlagenobjekte.</span><span class="sxs-lookup"><span data-stu-id="0eadc-119">Handles message and attachment objects.</span></span>
    
<span data-ttu-id="0eadc-120">[[MS-OXOJRNL]](https://msdn.microsoft.com/library/2aa04fd2-0f36-4ce4-9178-c0fc70aa8d43%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="0eadc-120">[[MS-OXOJRNL]](https://msdn.microsoft.com/library/2aa04fd2-0f36-4ce4-9178-c0fc70aa8d43%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="0eadc-121">Gibt die Eigenschaften und Vorgänge an, die für Journalobjekte zulässig sind.</span><span class="sxs-lookup"><span data-stu-id="0eadc-121">Specifies the properties and operations that are permissible for journal objects.</span></span>
    
<span data-ttu-id="0eadc-122">[[MS-OXORMDR]](https://msdn.microsoft.com/library/5454ebcc-e5d1-4da8-a598-d393b101caab%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="0eadc-122">[[MS-OXORMDR]](https://msdn.microsoft.com/library/5454ebcc-e5d1-4da8-a598-d393b101caab%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="0eadc-123">Gibt die Eigenschaften und das Interaktionsmodell für E-Mail- und andere Objekterinnerungen an.</span><span class="sxs-lookup"><span data-stu-id="0eadc-123">Specifies the properties and the interaction model for email and other object reminders.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="0eadc-124">Headerdateien</span><span class="sxs-lookup"><span data-stu-id="0eadc-124">Header files</span></span>

<span data-ttu-id="0eadc-125">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="0eadc-125">Mapidefs.h</span></span>
  
> <span data-ttu-id="0eadc-126">Bietet Datentypdefinitionen.</span><span class="sxs-lookup"><span data-stu-id="0eadc-126">Provides data type definitions.</span></span>
    
<span data-ttu-id="0eadc-127">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="0eadc-127">Mapitags.h</span></span>
  
> <span data-ttu-id="0eadc-128">Enthält Definitionen von Eigenschaften, die als alternative Namen aufgeführt sind.</span><span class="sxs-lookup"><span data-stu-id="0eadc-128">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="0eadc-129">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="0eadc-129">See also</span></span>



[<span data-ttu-id="0eadc-130">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="0eadc-130">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="0eadc-131">KANONISCHE EIGENSCHAFTEN VON MAPI</span><span class="sxs-lookup"><span data-stu-id="0eadc-131">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="0eadc-132">Zuordnen kanonischer Eigenschaftsnamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="0eadc-132">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="0eadc-133">Zuordnen von MAPI-Namen zu kanonischen Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="0eadc-133">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

