---
title: Kanonische Pidlidhaspicture (-Eigenschaft
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidHasPicture
api_type:
- COM
ms.assetid: c3bea11c-3197-4060-8672-f1b4bf352112
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: 3aef2fc1038751c9ad6fb97cf347c2dcab114fda
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32357750"
---
# <a name="pidlidhaspicture-canonical-property"></a><span data-ttu-id="94913-103">Kanonische Pidlidhaspicture (-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="94913-103">PidLidHasPicture Canonical Property</span></span>

  
  
<span data-ttu-id="94913-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="94913-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="94913-105">Gibt an, ob eine Foto Anlage für einen Kontakt vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="94913-105">Specifies whether a photo attachment exists for a contact.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="94913-106">Zugeordnete Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="94913-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="94913-107">dispidHasPicture</span><span class="sxs-lookup"><span data-stu-id="94913-107">dispidHasPicture</span></span>  <br/> |
|<span data-ttu-id="94913-108">Eigenschaftensatz:</span><span class="sxs-lookup"><span data-stu-id="94913-108">Property set:</span></span>  <br/> |<span data-ttu-id="94913-109">PSETID_Address</span><span class="sxs-lookup"><span data-stu-id="94913-109">PSETID_Address</span></span>  <br/> |
|<span data-ttu-id="94913-110">Long-ID (Deckel):</span><span class="sxs-lookup"><span data-stu-id="94913-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="94913-111">0x00008015</span><span class="sxs-lookup"><span data-stu-id="94913-111">0x00008015</span></span>  <br/> |
|<span data-ttu-id="94913-112">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="94913-112">Data type:</span></span>  <br/> |<span data-ttu-id="94913-113">PT_BOOLEAN</span><span class="sxs-lookup"><span data-stu-id="94913-113">PT_BOOLEAN</span></span>  <br/> |
|<span data-ttu-id="94913-114">Bereich:</span><span class="sxs-lookup"><span data-stu-id="94913-114">Area:</span></span>  <br/> |<span data-ttu-id="94913-115">Kontakt</span><span class="sxs-lookup"><span data-stu-id="94913-115">Contact</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="94913-116">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="94913-116">Remarks</span></span>

<span data-ttu-id="94913-117">Wenn diese Eigenschaft vorhanden ist und auf TRUE festgelegt ist, enthält die Attachment-Tabelle des Kontakts eine Anlage, wobei die **PR_ATTACHMENT_CONTACTPHOTO** ([pidtagattachmentcontactphoto (](pidtagattachmentcontactphoto-canonical-property.md))-Eigenschaft auf true festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="94913-117">If this property exists and is set to TRUE, the contact's attachment table contains an attachment with the **PR_ATTACHMENT_CONTACTPHOTO** ([PidTagAttachmentContactPhoto](pidtagattachmentcontactphoto-canonical-property.md)) property set to TRUE.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="94913-118">Zugehörige Ressourcen</span><span class="sxs-lookup"><span data-stu-id="94913-118">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="94913-119">Protokollspezifikationen</span><span class="sxs-lookup"><span data-stu-id="94913-119">Protocol specifications</span></span>

<span data-ttu-id="94913-120">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="94913-120">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="94913-121">Stellt Eigenschaftensatz Definitionen und Verweise auf zugehörige Exchange Server-Protokollspezifikationen bereit.</span><span class="sxs-lookup"><span data-stu-id="94913-121">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="94913-122">[[MS-OXOCNTC]](https://msdn.microsoft.com/library/9b636532-9150-4836-9635-9c9b756c9ccf%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="94913-122">[[MS-OXOCNTC]](https://msdn.microsoft.com/library/9b636532-9150-4836-9635-9c9b756c9ccf%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="94913-123">Gibt die Eigenschaften und Vorgänge an, die für Kontakte und persönliche Verteilerlisten zulässig sind.</span><span class="sxs-lookup"><span data-stu-id="94913-123">Specifies the properties and operations that are permissible for contacts and personal distribution lists.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="94913-124">Header Dateien</span><span class="sxs-lookup"><span data-stu-id="94913-124">Header files</span></span>

<span data-ttu-id="94913-125">Mapidefs. h</span><span class="sxs-lookup"><span data-stu-id="94913-125">Mapidefs.h</span></span>
  
> <span data-ttu-id="94913-126">Stellt Datentypdefinitionen bereit.</span><span class="sxs-lookup"><span data-stu-id="94913-126">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="94913-127">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="94913-127">See also</span></span>



[<span data-ttu-id="94913-128">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="94913-128">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="94913-129">Kanonische MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="94913-129">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="94913-130">Zuordnen von kanonischen Eigenschaftennamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="94913-130">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="94913-131">Zuordnen von MAPI-Namen zu kanonischen Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="94913-131">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

