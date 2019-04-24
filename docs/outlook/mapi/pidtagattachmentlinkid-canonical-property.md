---
title: Kanonische Pidtagattachmentlinkid (-Eigenschaft
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
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: 623b4195b7128667b9aaa6bc97d03c21d62c690a
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32345696"
---
# <a name="pidtagattachmentlinkid-canonical-property"></a><span data-ttu-id="e1274-103">Kanonische Pidtagattachmentlinkid (-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="e1274-103">PidTagAttachmentLinkId Canonical Property</span></span>

  
  
<span data-ttu-id="e1274-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="e1274-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="e1274-105">Gibt den Typ des Nachrichtenobjekts an, mit dem diese Anlage verknüpft ist.</span><span class="sxs-lookup"><span data-stu-id="e1274-105">Indicates the type of Message object to which this attachment is linked.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="e1274-106">Zugeordnete Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="e1274-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="e1274-107">PR_ATTACHMENT_LINKID</span><span class="sxs-lookup"><span data-stu-id="e1274-107">PR_ATTACHMENT_LINKID</span></span>  <br/> |
|<span data-ttu-id="e1274-108">Kennung:</span><span class="sxs-lookup"><span data-stu-id="e1274-108">Identifier:</span></span>  <br/> |<span data-ttu-id="e1274-109">0x7FFA</span><span class="sxs-lookup"><span data-stu-id="e1274-109">0x7FFA</span></span>  <br/> |
|<span data-ttu-id="e1274-110">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="e1274-110">Data type:</span></span>  <br/> |<span data-ttu-id="e1274-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="e1274-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="e1274-112">Bereich:</span><span class="sxs-lookup"><span data-stu-id="e1274-112">Area:</span></span>  <br/> |<span data-ttu-id="e1274-113">Nachrichtenanlage</span><span class="sxs-lookup"><span data-stu-id="e1274-113">Message attachment</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="e1274-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="e1274-114">Remarks</span></span>

<span data-ttu-id="e1274-115">Muss 0 sein, es sei denn, Sie wird von anderen Protokollen außer Kraft gesetzt, die das Protokoll der Nachricht und des Attachment-Objekts gemäß [[MS-OXCMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)erweitern.</span><span class="sxs-lookup"><span data-stu-id="e1274-115">Must be 0, unless overridden by other protocols that extend the Message and Attachment Object Protocol as noted in [[MS-OXCMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx).</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="e1274-116">Zugehörige Ressourcen</span><span class="sxs-lookup"><span data-stu-id="e1274-116">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="e1274-117">Protokollspezifikationen</span><span class="sxs-lookup"><span data-stu-id="e1274-117">Protocol specifications</span></span>

<span data-ttu-id="e1274-118">[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="e1274-118">[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="e1274-119">Verarbeitet Nachrichten-und Anlagenobjekte.</span><span class="sxs-lookup"><span data-stu-id="e1274-119">Handles message and attachment objects.</span></span>
    
<span data-ttu-id="e1274-120">[[MS-OXOJRNL]](https://msdn.microsoft.com/library/2aa04fd2-0f36-4ce4-9178-c0fc70aa8d43%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="e1274-120">[[MS-OXOJRNL]](https://msdn.microsoft.com/library/2aa04fd2-0f36-4ce4-9178-c0fc70aa8d43%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="e1274-121">Gibt die Eigenschaften und Vorgänge an, die für Journal Objekte zulässig sind.</span><span class="sxs-lookup"><span data-stu-id="e1274-121">Specifies the properties and operations that are permissible for journal objects.</span></span>
    
<span data-ttu-id="e1274-122">[[MS-OXORMDR]](https://msdn.microsoft.com/library/5454ebcc-e5d1-4da8-a598-d393b101caab%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="e1274-122">[[MS-OXORMDR]](https://msdn.microsoft.com/library/5454ebcc-e5d1-4da8-a598-d393b101caab%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="e1274-123">Gibt die Eigenschaften und das Interaktionsmodell für e-Mails und andere Objekt Erinnerungen an.</span><span class="sxs-lookup"><span data-stu-id="e1274-123">Specifies the properties and the interaction model for email and other object reminders.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="e1274-124">Header Dateien</span><span class="sxs-lookup"><span data-stu-id="e1274-124">Header files</span></span>

<span data-ttu-id="e1274-125">Mapidefs. h</span><span class="sxs-lookup"><span data-stu-id="e1274-125">Mapidefs.h</span></span>
  
> <span data-ttu-id="e1274-126">Stellt Datentypdefinitionen bereit.</span><span class="sxs-lookup"><span data-stu-id="e1274-126">Provides data type definitions.</span></span>
    
<span data-ttu-id="e1274-127">Mapitags. h</span><span class="sxs-lookup"><span data-stu-id="e1274-127">Mapitags.h</span></span>
  
> <span data-ttu-id="e1274-128">Enthält Definitionen von Eigenschaften, die als Alternative Namen aufgeführt sind.</span><span class="sxs-lookup"><span data-stu-id="e1274-128">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="e1274-129">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="e1274-129">See also</span></span>



[<span data-ttu-id="e1274-130">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="e1274-130">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="e1274-131">Kanonische MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="e1274-131">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="e1274-132">Zuordnen von kanonischen Eigenschaftennamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="e1274-132">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="e1274-133">Zuordnen von MAPI-Namen zu kanonischen Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="e1274-133">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

