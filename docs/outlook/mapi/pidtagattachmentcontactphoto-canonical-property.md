---
title: PidTagAttachmentContactPhoto (kanonische Eigenschaft)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagAttachmentContactPhoto
api_type:
- HeaderDef
ms.assetid: ea5b77b7-8440-4e54-abd2-c475138c8f63
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 332b6b857921c8f72837dc115805084efd8c5a19
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2018
ms.locfileid: "22574748"
---
# <a name="pidtagattachmentcontactphoto-canonical-property"></a><span data-ttu-id="a8fb2-103">PidTagAttachmentContactPhoto (kanonische Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="a8fb2-103">PidTagAttachmentContactPhoto Canonical Property</span></span>

  
  
<span data-ttu-id="a8fb2-104">**Betrifft**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="a8fb2-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="a8fb2-105">Gibt das Vorhandensein einer Anlage Foto für einen Kontakt an.</span><span class="sxs-lookup"><span data-stu-id="a8fb2-105">Indicates the existence of a photo attachment for a contact.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="a8fb2-106">Zugeordnete Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="a8fb2-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="a8fb2-107">PR_ATTACHMENT_CONTACTPHOTO</span><span class="sxs-lookup"><span data-stu-id="a8fb2-107">PR_ATTACHMENT_CONTACTPHOTO</span></span>  <br/> |
|<span data-ttu-id="a8fb2-108">Kennung:</span><span class="sxs-lookup"><span data-stu-id="a8fb2-108">Identifier:</span></span>  <br/> |<span data-ttu-id="a8fb2-109">0x7FFF</span><span class="sxs-lookup"><span data-stu-id="a8fb2-109">0x7FFF</span></span>  <br/> |
|<span data-ttu-id="a8fb2-110">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="a8fb2-110">Data type:</span></span>  <br/> |<span data-ttu-id="a8fb2-111">PT_BOOLEAN</span><span class="sxs-lookup"><span data-stu-id="a8fb2-111">PT_BOOLEAN</span></span>  <br/> |
|<span data-ttu-id="a8fb2-112">Bereich:</span><span class="sxs-lookup"><span data-stu-id="a8fb2-112">Area:</span></span>  <br/> |<span data-ttu-id="a8fb2-113">Nachrichtenanlage</span><span class="sxs-lookup"><span data-stu-id="a8fb2-113">Message attachment</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="a8fb2-114">HinwBemerkungeneise</span><span class="sxs-lookup"><span data-stu-id="a8fb2-114">Remarks</span></span>

<span data-ttu-id="a8fb2-115">Der Wert dieser Eigenschaft muss auf TRUE festgelegt sein, und es sollte nur eine Anlage in einem bestimmten Kontaktobjekt vorhanden sein.</span><span class="sxs-lookup"><span data-stu-id="a8fb2-115">This property's value must be set to TRUE, and there should only be one attachment on a given Contact object.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="a8fb2-116">Verwandte Ressourcen</span><span class="sxs-lookup"><span data-stu-id="a8fb2-116">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="a8fb2-117">Protokollspezifikationen</span><span class="sxs-lookup"><span data-stu-id="a8fb2-117">Protocol specifications</span></span>

<span data-ttu-id="a8fb2-118">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="a8fb2-118">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="a8fb2-119">Enthält Eigenschaftendefinitionen und Verweise auf Verwandte Exchange Server-Spezifikationen.</span><span class="sxs-lookup"><span data-stu-id="a8fb2-119">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="a8fb2-120">[[MS-OXOCNTC]](http://msdn.microsoft.com/library/9b636532-9150-4836-9635-9c9b756c9ccf%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="a8fb2-120">[[MS-OXOCNTC]](http://msdn.microsoft.com/library/9b636532-9150-4836-9635-9c9b756c9ccf%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="a8fb2-121">Gibt die Eigenschaften und Operationen, die für Kontakte und persönliche Verteilerlisten zulässig sind.</span><span class="sxs-lookup"><span data-stu-id="a8fb2-121">Specifies the properties and operations that are permissible for contacts and personal distribution lists.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="a8fb2-122">Header-Dateien</span><span class="sxs-lookup"><span data-stu-id="a8fb2-122">Header files</span></span>

<span data-ttu-id="a8fb2-123">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="a8fb2-123">Mapidefs.h</span></span>
  
> <span data-ttu-id="a8fb2-124">Enthält die Datentypdefinitionen.</span><span class="sxs-lookup"><span data-stu-id="a8fb2-124">Provides data type definitions.</span></span>
    
<span data-ttu-id="a8fb2-125">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="a8fb2-125">Mapitags.h</span></span>
  
> <span data-ttu-id="a8fb2-126">Enthält Definitionen von Eigenschaften, die als Alternative Namen aufgelistet.</span><span class="sxs-lookup"><span data-stu-id="a8fb2-126">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="a8fb2-127">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="a8fb2-127">See also</span></span>



[<span data-ttu-id="a8fb2-128">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="a8fb2-128">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="a8fb2-129">Kanonische MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="a8fb2-129">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="a8fb2-130">Zuordnen von kanonischen Eigenschaftennamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="a8fb2-130">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="a8fb2-131">Zuordnen von MAPI-Namen zu kanonische Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="a8fb2-131">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

