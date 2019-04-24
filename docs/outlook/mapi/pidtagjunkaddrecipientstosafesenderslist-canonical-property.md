---
title: Kanonische Pidtagjunkaddrecipientstosafesenderslist (-Eigenschaft
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagJunkAddRecipientsToSafeSendersList
api_type:
- HeaderDef
ms.assetid: 78543caa-e6ec-4ac7-bfdd-70c56f8fd955
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: 3a87beaa3873b5ccb449e5b1497262bad5bf1497
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32282368"
---
# <a name="pidtagjunkaddrecipientstosafesenderslist-canonical-property"></a><span data-ttu-id="27080-103">Kanonische Pidtagjunkaddrecipientstosafesenderslist (-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="27080-103">PidTagJunkAddRecipientsToSafeSendersList Canonical Property</span></span>

  
  
<span data-ttu-id="27080-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="27080-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="27080-105">Gibt an, ob die e-Mail-Empfänger der Liste sicherer Absender hinzugefügt werden sollen.</span><span class="sxs-lookup"><span data-stu-id="27080-105">Indicates whether or not the mail recipients are to be added to the safe senders list.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="27080-106">Zugeordnete Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="27080-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="27080-107">PR_JUNK_ADD_RECIPS_TO_SSL</span><span class="sxs-lookup"><span data-stu-id="27080-107">PR_JUNK_ADD_RECIPS_TO_SSL</span></span>  <br/> |
|<span data-ttu-id="27080-108">Kennung:</span><span class="sxs-lookup"><span data-stu-id="27080-108">Identifier:</span></span>  <br/> |<span data-ttu-id="27080-109">0x6103</span><span class="sxs-lookup"><span data-stu-id="27080-109">0x6103</span></span>  <br/> |
|<span data-ttu-id="27080-110">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="27080-110">Data type:</span></span>  <br/> |<span data-ttu-id="27080-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="27080-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="27080-112">Bereich:</span><span class="sxs-lookup"><span data-stu-id="27080-112">Area:</span></span>  <br/> |<span data-ttu-id="27080-113">Spam</span><span class="sxs-lookup"><span data-stu-id="27080-113">Spam</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="27080-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="27080-114">Remarks</span></span>

<span data-ttu-id="27080-115">Sofern vorhanden, muss diese Eigenschaft auf 0 oder 1 festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="27080-115">If present, this property must be set to 0 or 1.</span></span> <span data-ttu-id="27080-116">Der Wert 1 gibt an, dass die e-Mail-Empfänger der Liste sicherer Absender hinzugefügt werden sollen.</span><span class="sxs-lookup"><span data-stu-id="27080-116">A value of 1 indicates that the mail recipients are to be added to the safe senders list.</span></span> <span data-ttu-id="27080-117">Der Wert 0 gibt an, dass die e-Mail-Empfänger nicht der Liste der sicheren Absender hinzugefügt werden sollen.</span><span class="sxs-lookup"><span data-stu-id="27080-117">A value of 0 indicates that the mail recipients are not to be added to the safe senders list.</span></span>
  
<span data-ttu-id="27080-118">Wenn diese Eigenschaft mit dem Wert 1 vorhanden ist, müssen die SMTP-Adressen der e-Mail-Empfänger der Regelbedingung für vertrauenswürdige Absender hinzugefügt werden.</span><span class="sxs-lookup"><span data-stu-id="27080-118">If this property is present with a value of 1, the SMTP addresses of the email recipients must be added to trusted senders clause of the Junk E-Mail Rule condition.</span></span> <span data-ttu-id="27080-119">Wenn diese Eigenschaft 0 ist, ist keine Aktion erforderlich.</span><span class="sxs-lookup"><span data-stu-id="27080-119">If this property is 0, no action is required.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="27080-120">Zugehörige Ressourcen</span><span class="sxs-lookup"><span data-stu-id="27080-120">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="27080-121">Protokollspezifikationen</span><span class="sxs-lookup"><span data-stu-id="27080-121">Protocol specifications</span></span>

<span data-ttu-id="27080-122">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="27080-122">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="27080-123">Enthält Verweise auf zugehörige Exchange Server-Protokollspezifikationen.</span><span class="sxs-lookup"><span data-stu-id="27080-123">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="27080-124">[[MS-OXCSPAM]](https://msdn.microsoft.com/library/522f8587-4aed-4cd6-831b-40bd87862189%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="27080-124">[[MS-OXCSPAM]](https://msdn.microsoft.com/library/522f8587-4aed-4cd6-831b-40bd87862189%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="27080-125">Ermöglicht die Behandlung von Allow/Block-Listen und die Bestimmung von Junk-e-Mails.</span><span class="sxs-lookup"><span data-stu-id="27080-125">Enables the handling of allow/block lists and the determination of junk email messages.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="27080-126">Header Dateien</span><span class="sxs-lookup"><span data-stu-id="27080-126">Header files</span></span>

<span data-ttu-id="27080-127">Mapidefs. h</span><span class="sxs-lookup"><span data-stu-id="27080-127">Mapidefs.h</span></span>
  
> <span data-ttu-id="27080-128">Stellt Datentypdefinitionen bereit.</span><span class="sxs-lookup"><span data-stu-id="27080-128">Provides data type definitions.</span></span>
    
<span data-ttu-id="27080-129">Mapitags. h</span><span class="sxs-lookup"><span data-stu-id="27080-129">Mapitags.h</span></span>
  
> <span data-ttu-id="27080-130">Enthält Definitionen von Eigenschaften, die als Alternative Namen aufgeführt sind.</span><span class="sxs-lookup"><span data-stu-id="27080-130">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="27080-131">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="27080-131">See also</span></span>



[<span data-ttu-id="27080-132">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="27080-132">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="27080-133">Kanonische MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="27080-133">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="27080-134">Zuordnen von kanonischen Eigenschaftennamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="27080-134">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="27080-135">Zuordnen von MAPI-Namen zu kanonischen Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="27080-135">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

