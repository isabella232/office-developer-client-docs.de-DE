---
title: Kanonische PidTagJunkAddRecipientsToSafeSendersList-Eigenschaft
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
ms.openlocfilehash: 8c104af106a885f42f8063bcf5fb55d654f2688e
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19794530"
---
# <a name="pidtagjunkaddrecipientstosafesenderslist-canonical-property"></a><span data-ttu-id="1a624-103">Kanonische PidTagJunkAddRecipientsToSafeSendersList-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="1a624-103">PidTagJunkAddRecipientsToSafeSendersList Canonical Property</span></span>

  
  
<span data-ttu-id="1a624-104">**Betrifft**: Outlook</span><span class="sxs-lookup"><span data-stu-id="1a624-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="1a624-105">Gibt an, ob die e-Mail-Empfänger werden, die Liste sicherer Absender hinzugefügt werden soll.</span><span class="sxs-lookup"><span data-stu-id="1a624-105">Indicates whether or not the mail recipients are to be added to the safe senders list.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="1a624-106">Zugeordneten Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="1a624-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="1a624-107">PR_JUNK_ADD_RECIPS_TO_SSL</span><span class="sxs-lookup"><span data-stu-id="1a624-107">PR_JUNK_ADD_RECIPS_TO_SSL</span></span>  <br/> |
|<span data-ttu-id="1a624-108">Bezeichner:</span><span class="sxs-lookup"><span data-stu-id="1a624-108">Identifier:</span></span>  <br/> |<span data-ttu-id="1a624-109">0x6103</span><span class="sxs-lookup"><span data-stu-id="1a624-109">0x6103</span></span>  <br/> |
|<span data-ttu-id="1a624-110">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="1a624-110">Data type:</span></span>  <br/> |<span data-ttu-id="1a624-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="1a624-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="1a624-112">Bereich:</span><span class="sxs-lookup"><span data-stu-id="1a624-112">Area:</span></span>  <br/> |<span data-ttu-id="1a624-113">Spam</span><span class="sxs-lookup"><span data-stu-id="1a624-113">Spam</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="1a624-114">Hinweise</span><span class="sxs-lookup"><span data-stu-id="1a624-114">Remarks</span></span>

<span data-ttu-id="1a624-115">Wenn dieser Parameter angegeben wurde, muss diese Eigenschaft auf 0 oder 1 festgelegt.</span><span class="sxs-lookup"><span data-stu-id="1a624-115">If present, this property must be set to 0 or 1.</span></span> <span data-ttu-id="1a624-116">Der Wert 1 gibt an, dass die e-Mail-Empfänger werden, die Liste sicherer Absender hinzugefügt werden soll.</span><span class="sxs-lookup"><span data-stu-id="1a624-116">A value of 1 indicates that the mail recipients are to be added to the safe senders list.</span></span> <span data-ttu-id="1a624-117">Der Wert 0 gibt an, dass die e-Mail-Empfänger werden nicht für die Liste sicherer Absender hinzugefügt werden.</span><span class="sxs-lookup"><span data-stu-id="1a624-117">A value of 0 indicates that the mail recipients are not to be added to the safe senders list.</span></span>
  
<span data-ttu-id="1a624-118">Wenn diese Eigenschaft mit einem Wert von 1 vorhanden ist, müssen die SMTP-Adressen der e-Mail-Empfänger vertrauenswürdigen Absender-Klausel der Junk-e-Mail-Regel Bedingung hinzugefügt werden.</span><span class="sxs-lookup"><span data-stu-id="1a624-118">If this property is present with a value of 1, the SMTP addresses of the email recipients must be added to trusted senders clause of the Junk E-Mail Rule condition.</span></span> <span data-ttu-id="1a624-119">Wenn diese Eigenschaft 0 ist, ist keine Aktion erforderlich.</span><span class="sxs-lookup"><span data-stu-id="1a624-119">If this property is 0, no action is required.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="1a624-120">Verwandte Ressourcen</span><span class="sxs-lookup"><span data-stu-id="1a624-120">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="1a624-121">Protokollspezifikationen</span><span class="sxs-lookup"><span data-stu-id="1a624-121">Protocol specifications</span></span>

<span data-ttu-id="1a624-122">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="1a624-122">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="1a624-123">Bietet Verweise auf Verwandte Exchange Server-Spezifikationen.</span><span class="sxs-lookup"><span data-stu-id="1a624-123">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="1a624-124">[[MS-OXCSPAM]](http://msdn.microsoft.com/library/522f8587-4aed-4cd6-831b-40bd87862189%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="1a624-124">[[MS-OXCSPAM]](http://msdn.microsoft.com/library/522f8587-4aed-4cd6-831b-40bd87862189%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="1a624-125">Ermöglicht die Behandlung von zulassen/blockieren-Listen und die Bestimmung des junk-e-Mail-Nachrichten.</span><span class="sxs-lookup"><span data-stu-id="1a624-125">Enables the handling of allow/block lists and the determination of junk email messages.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="1a624-126">Header-Dateien</span><span class="sxs-lookup"><span data-stu-id="1a624-126">Header files</span></span>

<span data-ttu-id="1a624-127">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="1a624-127">Mapidefs.h</span></span>
  
> <span data-ttu-id="1a624-128">Enthält die Datentypdefinitionen.</span><span class="sxs-lookup"><span data-stu-id="1a624-128">Provides data type definitions.</span></span>
    
<span data-ttu-id="1a624-129">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="1a624-129">Mapitags.h</span></span>
  
> <span data-ttu-id="1a624-130">Enthält Definitionen von Eigenschaften, die als Alternative Namen aufgelistet.</span><span class="sxs-lookup"><span data-stu-id="1a624-130">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="1a624-131">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="1a624-131">See also</span></span>



[<span data-ttu-id="1a624-132">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="1a624-132">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="1a624-133">Kanonische MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="1a624-133">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="1a624-134">Zuordnen von kanonischen Eigenschaftennamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="1a624-134">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="1a624-135">Zuordnen von MAPI-Namen zu kanonische Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="1a624-135">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

