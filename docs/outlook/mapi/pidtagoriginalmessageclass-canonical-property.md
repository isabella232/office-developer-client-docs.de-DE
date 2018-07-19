---
title: PidTagOriginalMessageClass (kanonische Eigenschaft)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagOriginalMessageClass
api_type:
- COM
ms.assetid: 49deb153-03c6-4be2-a3a5-53cca01accba
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 7167b7b51698cda5610356779a8e8342b34a6082
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19794719"
---
# <a name="pidtagoriginalmessageclass-canonical-property"></a><span data-ttu-id="c3a9b-103">PidTagOriginalMessageClass (kanonische Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="c3a9b-103">PidTagOriginalMessageClass Canonical Property</span></span>

  
  
<span data-ttu-id="c3a9b-104">**Betrifft**: Outlook</span><span class="sxs-lookup"><span data-stu-id="c3a9b-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="c3a9b-105">Enthält die Klasse der ursprünglichen Nachricht für die Verwendung in einem Bericht.</span><span class="sxs-lookup"><span data-stu-id="c3a9b-105">Contains the class of the original message for use in a report.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="c3a9b-106">Zugeordneten Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="c3a9b-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="c3a9b-107">PR_ORIG_MESSAGE_CLASS, PR_ORIG_MESSAGE_CLASS_A, PR_ORIG_MESSAGE_CLASS_W</span><span class="sxs-lookup"><span data-stu-id="c3a9b-107">PR_ORIG_MESSAGE_CLASS, PR_ORIG_MESSAGE_CLASS_A, PR_ORIG_MESSAGE_CLASS_W</span></span>  <br/> |
|<span data-ttu-id="c3a9b-108">Bezeichner:</span><span class="sxs-lookup"><span data-stu-id="c3a9b-108">Identifier:</span></span>  <br/> |<span data-ttu-id="c3a9b-109">0x004B</span><span class="sxs-lookup"><span data-stu-id="c3a9b-109">0x004B</span></span>  <br/> |
|<span data-ttu-id="c3a9b-110">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="c3a9b-110">Data type:</span></span>  <br/> |<span data-ttu-id="c3a9b-111">PT_STRING8, PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="c3a9b-111">PT_STRING8, PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="c3a9b-112">Bereich:</span><span class="sxs-lookup"><span data-stu-id="c3a9b-112">Area:</span></span>  <br/> |<span data-ttu-id="c3a9b-113">Secure Messaging-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="c3a9b-113">Secure Messaging Properties</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="c3a9b-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="c3a9b-114">Remarks</span></span>

<span data-ttu-id="c3a9b-115">Diese Eigenschaften enthalten eine Kopie der Eigenschaft **PR_MESSAGE_CLASS** ([PidTagMessageClass](pidtagmessageclass-canonical-property.md)) der Nachricht für die der Bericht generiert wird.</span><span class="sxs-lookup"><span data-stu-id="c3a9b-115">These properties contain a copy of the **PR_MESSAGE_CLASS** ([PidTagMessageClass](pidtagmessageclass-canonical-property.md)) property of the message for which the report is being generated.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="c3a9b-116">Verwandte Ressourcen</span><span class="sxs-lookup"><span data-stu-id="c3a9b-116">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="c3a9b-117">Protokollspezifikationen</span><span class="sxs-lookup"><span data-stu-id="c3a9b-117">Protocol specifications</span></span>

<span data-ttu-id="c3a9b-118">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="c3a9b-118">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="c3a9b-119">Bietet Verweise auf Verwandte Exchange Server-Spezifikationen.</span><span class="sxs-lookup"><span data-stu-id="c3a9b-119">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="c3a9b-120">[[MS-OXTNEF]](http://msdn.microsoft.com/library/1f0544d7-30b7-4194-b58f-adc82f3763bb%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="c3a9b-120">[[MS-OXTNEF]](http://msdn.microsoft.com/library/1f0544d7-30b7-4194-b58f-adc82f3763bb%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="c3a9b-121">Codiert und decodiert Nachrichten- und Objekte, die auf eine effiziente Streamdarstellung.</span><span class="sxs-lookup"><span data-stu-id="c3a9b-121">Encodes and decodes message and attachment objects to an efficient stream representation.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="c3a9b-122">Header-Dateien</span><span class="sxs-lookup"><span data-stu-id="c3a9b-122">Header files</span></span>

<span data-ttu-id="c3a9b-123">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="c3a9b-123">Mapidefs.h</span></span>
  
> <span data-ttu-id="c3a9b-124">Enthält die Datentypdefinitionen.</span><span class="sxs-lookup"><span data-stu-id="c3a9b-124">Provides data type definitions.</span></span>
    
<span data-ttu-id="c3a9b-125">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="c3a9b-125">Mapitags.h</span></span>
  
> <span data-ttu-id="c3a9b-126">Enthält Definitionen von Eigenschaften, die als zugeordneten Eigenschaften aufgelistet.</span><span class="sxs-lookup"><span data-stu-id="c3a9b-126">Contains definitions of properties listed as associated properties.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="c3a9b-127">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="c3a9b-127">See also</span></span>



[<span data-ttu-id="c3a9b-128">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="c3a9b-128">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="c3a9b-129">Kanonische MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="c3a9b-129">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="c3a9b-130">Zuordnen von kanonischen Eigenschaftennamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="c3a9b-130">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="c3a9b-131">Zuordnen von MAPI-Namen zu kanonische Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="c3a9b-131">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

