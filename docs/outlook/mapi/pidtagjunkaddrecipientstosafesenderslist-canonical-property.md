---
title: PidTagJunkAddRecipientsToSafeSendersList (kanonische Eigenschaft)
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
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: dc31d26ba1aa695ad0b64114ac7992e10bb548ba
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2018
ms.locfileid: "22595409"
---
# <a name="pidtagjunkaddrecipientstosafesenderslist-canonical-property"></a><span data-ttu-id="82b18-103">PidTagJunkAddRecipientsToSafeSendersList (kanonische Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="82b18-103">PidTagJunkAddRecipientsToSafeSendersList Canonical Property</span></span>

  
  
<span data-ttu-id="82b18-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="82b18-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="82b18-105">Gibt an, ob die e-Mail-Empfänger werden, die Liste sicherer Absender hinzugefügt werden soll.</span><span class="sxs-lookup"><span data-stu-id="82b18-105">Indicates whether or not the mail recipients are to be added to the safe senders list.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="82b18-106">Zugeordnete Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="82b18-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="82b18-107">PR_JUNK_ADD_RECIPS_TO_SSL</span><span class="sxs-lookup"><span data-stu-id="82b18-107">PR_JUNK_ADD_RECIPS_TO_SSL</span></span>  <br/> |
|<span data-ttu-id="82b18-108">Kennung:</span><span class="sxs-lookup"><span data-stu-id="82b18-108">Identifier:</span></span>  <br/> |<span data-ttu-id="82b18-109">0x6103</span><span class="sxs-lookup"><span data-stu-id="82b18-109">0x6103</span></span>  <br/> |
|<span data-ttu-id="82b18-110">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="82b18-110">Data type:</span></span>  <br/> |<span data-ttu-id="82b18-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="82b18-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="82b18-112">Bereich:</span><span class="sxs-lookup"><span data-stu-id="82b18-112">Area:</span></span>  <br/> |<span data-ttu-id="82b18-113">Spam</span><span class="sxs-lookup"><span data-stu-id="82b18-113">Spam</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="82b18-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="82b18-114">Remarks</span></span>

<span data-ttu-id="82b18-115">Wenn dieser Parameter angegeben wurde, muss diese Eigenschaft auf 0 oder 1 festgelegt.</span><span class="sxs-lookup"><span data-stu-id="82b18-115">If present, this property must be set to 0 or 1.</span></span> <span data-ttu-id="82b18-116">Der Wert 1 gibt an, dass die e-Mail-Empfänger werden, die Liste sicherer Absender hinzugefügt werden soll.</span><span class="sxs-lookup"><span data-stu-id="82b18-116">A value of 1 indicates that the mail recipients are to be added to the safe senders list.</span></span> <span data-ttu-id="82b18-117">Der Wert 0 gibt an, dass die e-Mail-Empfänger werden nicht für die Liste sicherer Absender hinzugefügt werden.</span><span class="sxs-lookup"><span data-stu-id="82b18-117">A value of 0 indicates that the mail recipients are not to be added to the safe senders list.</span></span>
  
<span data-ttu-id="82b18-118">Wenn diese Eigenschaft mit einem Wert von 1 vorhanden ist, müssen die SMTP-Adressen der e-Mail-Empfänger vertrauenswürdigen Absender-Klausel der Junk-e-Mail-Regel Bedingung hinzugefügt werden.</span><span class="sxs-lookup"><span data-stu-id="82b18-118">If this property is present with a value of 1, the SMTP addresses of the email recipients must be added to trusted senders clause of the Junk E-Mail Rule condition.</span></span> <span data-ttu-id="82b18-119">Wenn diese Eigenschaft 0 ist, ist keine Aktion erforderlich.</span><span class="sxs-lookup"><span data-stu-id="82b18-119">If this property is 0, no action is required.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="82b18-120">Verwandte Ressourcen</span><span class="sxs-lookup"><span data-stu-id="82b18-120">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="82b18-121">Protokollspezifikationen</span><span class="sxs-lookup"><span data-stu-id="82b18-121">Protocol specifications</span></span>

<span data-ttu-id="82b18-122">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="82b18-122">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="82b18-123">Bietet Verweise auf Verwandte Exchange Server-Spezifikationen.</span><span class="sxs-lookup"><span data-stu-id="82b18-123">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="82b18-124">[[MS-OXCSPAM]](http://msdn.microsoft.com/library/522f8587-4aed-4cd6-831b-40bd87862189%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="82b18-124">[[MS-OXCSPAM]](http://msdn.microsoft.com/library/522f8587-4aed-4cd6-831b-40bd87862189%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="82b18-125">Ermöglicht die Behandlung von zulassen/blockieren-Listen und die Bestimmung des junk-e-Mail-Nachrichten.</span><span class="sxs-lookup"><span data-stu-id="82b18-125">Enables the handling of allow/block lists and the determination of junk email messages.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="82b18-126">Header-Dateien</span><span class="sxs-lookup"><span data-stu-id="82b18-126">Header files</span></span>

<span data-ttu-id="82b18-127">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="82b18-127">Mapidefs.h</span></span>
  
> <span data-ttu-id="82b18-128">Enthält die Datentypdefinitionen.</span><span class="sxs-lookup"><span data-stu-id="82b18-128">Provides data type definitions.</span></span>
    
<span data-ttu-id="82b18-129">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="82b18-129">Mapitags.h</span></span>
  
> <span data-ttu-id="82b18-130">Enthält Definitionen von Eigenschaften, die als Alternative Namen aufgelistet.</span><span class="sxs-lookup"><span data-stu-id="82b18-130">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="82b18-131">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="82b18-131">See also</span></span>



[<span data-ttu-id="82b18-132">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="82b18-132">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="82b18-133">Kanonische MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="82b18-133">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="82b18-134">Zuordnen von kanonischen Eigenschaftennamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="82b18-134">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="82b18-135">Zuordnen von MAPI-Namen zu kanonische Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="82b18-135">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

