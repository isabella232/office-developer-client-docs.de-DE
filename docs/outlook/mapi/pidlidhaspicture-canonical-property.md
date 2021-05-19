---
title: PidLidHasPicture (kanonische Eigenschaft)
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
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 3aef2fc1038751c9ad6fb97cf347c2dcab114fda
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32357750"
---
# <a name="pidlidhaspicture-canonical-property"></a><span data-ttu-id="40e32-103">PidLidHasPicture (kanonische Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="40e32-103">PidLidHasPicture Canonical Property</span></span>

  
  
<span data-ttu-id="40e32-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="40e32-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="40e32-105">Gibt an, ob eine Fotoanlage für einen Kontakt vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="40e32-105">Specifies whether a photo attachment exists for a contact.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="40e32-106">Zugeordnete Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="40e32-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="40e32-107">dispidHasPicture</span><span class="sxs-lookup"><span data-stu-id="40e32-107">dispidHasPicture</span></span>  <br/> |
|<span data-ttu-id="40e32-108">Eigenschaftensatz:</span><span class="sxs-lookup"><span data-stu-id="40e32-108">Property set:</span></span>  <br/> |<span data-ttu-id="40e32-109">PSETID_Address</span><span class="sxs-lookup"><span data-stu-id="40e32-109">PSETID_Address</span></span>  <br/> |
|<span data-ttu-id="40e32-110">Lange ID (LID):</span><span class="sxs-lookup"><span data-stu-id="40e32-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="40e32-111">0x00008015</span><span class="sxs-lookup"><span data-stu-id="40e32-111">0x00008015</span></span>  <br/> |
|<span data-ttu-id="40e32-112">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="40e32-112">Data type:</span></span>  <br/> |<span data-ttu-id="40e32-113">PT_BOOLEAN</span><span class="sxs-lookup"><span data-stu-id="40e32-113">PT_BOOLEAN</span></span>  <br/> |
|<span data-ttu-id="40e32-114">Bereich:</span><span class="sxs-lookup"><span data-stu-id="40e32-114">Area:</span></span>  <br/> |<span data-ttu-id="40e32-115">Kontakt</span><span class="sxs-lookup"><span data-stu-id="40e32-115">Contact</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="40e32-116">Hinweise</span><span class="sxs-lookup"><span data-stu-id="40e32-116">Remarks</span></span>

<span data-ttu-id="40e32-117">Wenn diese Eigenschaft vorhanden ist und auf TRUE festgelegt ist, enthält die Anlagentabelle des Kontakts eine Anlage, bei der **die eigenschaft PR_ATTACHMENT_CONTACTPHOTO** ([PidTagAttachmentContactPhoto](pidtagattachmentcontactphoto-canonical-property.md)) auf TRUE festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="40e32-117">If this property exists and is set to TRUE, the contact's attachment table contains an attachment with the **PR_ATTACHMENT_CONTACTPHOTO** ([PidTagAttachmentContactPhoto](pidtagattachmentcontactphoto-canonical-property.md)) property set to TRUE.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="40e32-118">Verwandte Ressourcen</span><span class="sxs-lookup"><span data-stu-id="40e32-118">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="40e32-119">Protokollspezifikationen</span><span class="sxs-lookup"><span data-stu-id="40e32-119">Protocol specifications</span></span>

<span data-ttu-id="40e32-120">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="40e32-120">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="40e32-121">Stellt Eigenschaftensatzdefinitionen und Verweise auf verwandte Exchange Server zur Verfügung.</span><span class="sxs-lookup"><span data-stu-id="40e32-121">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="40e32-122">[[MS-OXOCNTC]](https://msdn.microsoft.com/library/9b636532-9150-4836-9635-9c9b756c9ccf%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="40e32-122">[[MS-OXOCNTC]](https://msdn.microsoft.com/library/9b636532-9150-4836-9635-9c9b756c9ccf%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="40e32-123">Gibt die Eigenschaften und Vorgänge an, die für Kontakte und persönliche Verteilerlisten zulässig sind.</span><span class="sxs-lookup"><span data-stu-id="40e32-123">Specifies the properties and operations that are permissible for contacts and personal distribution lists.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="40e32-124">Headerdateien</span><span class="sxs-lookup"><span data-stu-id="40e32-124">Header files</span></span>

<span data-ttu-id="40e32-125">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="40e32-125">Mapidefs.h</span></span>
  
> <span data-ttu-id="40e32-126">Bietet Datentypdefinitionen.</span><span class="sxs-lookup"><span data-stu-id="40e32-126">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="40e32-127">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="40e32-127">See also</span></span>



[<span data-ttu-id="40e32-128">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="40e32-128">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="40e32-129">KANONISCHE EIGENSCHAFTEN VON MAPI</span><span class="sxs-lookup"><span data-stu-id="40e32-129">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="40e32-130">Zuordnen kanonischer Eigenschaftsnamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="40e32-130">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="40e32-131">Zuordnen von MAPI-Namen zu kanonischen Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="40e32-131">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

