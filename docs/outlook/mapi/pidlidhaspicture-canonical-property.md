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
ms.openlocfilehash: 30046bd7982d08d99c5581c27d1616162d904dee
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2018
ms.locfileid: "22577107"
---
# <a name="pidlidhaspicture-canonical-property"></a><span data-ttu-id="ad426-103">PidLidHasPicture (kanonische Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="ad426-103">PidLidHasPicture Canonical Property</span></span>

  
  
<span data-ttu-id="ad426-104">**Betrifft**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="ad426-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="ad426-105">Gibt an, ob eine Anlage Foto für einen Kontakt vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="ad426-105">Specifies whether a photo attachment exists for a contact.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="ad426-106">Zugeordnete Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="ad426-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="ad426-107">dispidHasPicture</span><span class="sxs-lookup"><span data-stu-id="ad426-107">dispidHasPicture</span></span>  <br/> |
|<span data-ttu-id="ad426-108">-Eigenschaft festgelegt:</span><span class="sxs-lookup"><span data-stu-id="ad426-108">Property set:</span></span>  <br/> |<span data-ttu-id="ad426-109">PSETID_Address</span><span class="sxs-lookup"><span data-stu-id="ad426-109">PSETID_Address</span></span>  <br/> |
|<span data-ttu-id="ad426-110">Long-ID (Abdeckung):</span><span class="sxs-lookup"><span data-stu-id="ad426-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="ad426-111">0x00008015</span><span class="sxs-lookup"><span data-stu-id="ad426-111">0x00008015</span></span>  <br/> |
|<span data-ttu-id="ad426-112">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="ad426-112">Data type:</span></span>  <br/> |<span data-ttu-id="ad426-113">PT_BOOLEAN</span><span class="sxs-lookup"><span data-stu-id="ad426-113">PT_BOOLEAN</span></span>  <br/> |
|<span data-ttu-id="ad426-114">Bereich:</span><span class="sxs-lookup"><span data-stu-id="ad426-114">Area:</span></span>  <br/> |<span data-ttu-id="ad426-115">Kontakt</span><span class="sxs-lookup"><span data-stu-id="ad426-115">Contact</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="ad426-116">HinwBemerkungeneise</span><span class="sxs-lookup"><span data-stu-id="ad426-116">Remarks</span></span>

<span data-ttu-id="ad426-117">Wenn diese Eigenschaft vorhanden ist und auf TRUE festgelegt ist, enthält der Kontakt Anlagentabelle eine Anlage mit der **PR_ATTACHMENT_CONTACTPHOTO** ([PidTagAttachmentContactPhoto](pidtagattachmentcontactphoto-canonical-property.md))-Eigenschaft auf TRUE festgelegt.</span><span class="sxs-lookup"><span data-stu-id="ad426-117">If this property exists and is set to TRUE, the contact's attachment table contains an attachment with the **PR_ATTACHMENT_CONTACTPHOTO** ([PidTagAttachmentContactPhoto](pidtagattachmentcontactphoto-canonical-property.md)) property set to TRUE.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="ad426-118">Verwandte Ressourcen</span><span class="sxs-lookup"><span data-stu-id="ad426-118">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="ad426-119">Protokollspezifikationen</span><span class="sxs-lookup"><span data-stu-id="ad426-119">Protocol specifications</span></span>

<span data-ttu-id="ad426-120">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="ad426-120">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="ad426-121">Enthält Eigenschaftendefinitionen und Verweise auf Verwandte Exchange Server-Spezifikationen.</span><span class="sxs-lookup"><span data-stu-id="ad426-121">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="ad426-122">[[MS-OXOCNTC]](http://msdn.microsoft.com/library/9b636532-9150-4836-9635-9c9b756c9ccf%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="ad426-122">[[MS-OXOCNTC]](http://msdn.microsoft.com/library/9b636532-9150-4836-9635-9c9b756c9ccf%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="ad426-123">Gibt die Eigenschaften und Operationen, die für Kontakte und persönliche Verteilerlisten zulässig sind.</span><span class="sxs-lookup"><span data-stu-id="ad426-123">Specifies the properties and operations that are permissible for contacts and personal distribution lists.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="ad426-124">Header-Dateien</span><span class="sxs-lookup"><span data-stu-id="ad426-124">Header files</span></span>

<span data-ttu-id="ad426-125">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="ad426-125">Mapidefs.h</span></span>
  
> <span data-ttu-id="ad426-126">Enthält die Datentypdefinitionen.</span><span class="sxs-lookup"><span data-stu-id="ad426-126">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="ad426-127">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="ad426-127">See also</span></span>



[<span data-ttu-id="ad426-128">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="ad426-128">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="ad426-129">Kanonische MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="ad426-129">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="ad426-130">Zuordnen von kanonischen Eigenschaftennamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="ad426-130">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="ad426-131">Zuordnen von MAPI-Namen zu kanonische Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="ad426-131">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

