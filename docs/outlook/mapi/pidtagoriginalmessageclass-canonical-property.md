---
title: Kanonische Pidtagoriginalmessageclass (-Eigenschaft
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
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: 677ba61e3d812909ac4f28f3542f6a79f971ed06
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32342623"
---
# <a name="pidtagoriginalmessageclass-canonical-property"></a><span data-ttu-id="f74aa-103">Kanonische Pidtagoriginalmessageclass (-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="f74aa-103">PidTagOriginalMessageClass Canonical Property</span></span>

  
  
<span data-ttu-id="f74aa-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="f74aa-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="f74aa-105">Enthält die Klasse der ursprünglichen Nachricht für die Verwendung in einem Bericht.</span><span class="sxs-lookup"><span data-stu-id="f74aa-105">Contains the class of the original message for use in a report.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="f74aa-106">Zugeordnete Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="f74aa-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="f74aa-107">PR_ORIG_MESSAGE_CLASS, PR_ORIG_MESSAGE_CLASS_A, PR_ORIG_MESSAGE_CLASS_W</span><span class="sxs-lookup"><span data-stu-id="f74aa-107">PR_ORIG_MESSAGE_CLASS, PR_ORIG_MESSAGE_CLASS_A, PR_ORIG_MESSAGE_CLASS_W</span></span>  <br/> |
|<span data-ttu-id="f74aa-108">Kennung:</span><span class="sxs-lookup"><span data-stu-id="f74aa-108">Identifier:</span></span>  <br/> |<span data-ttu-id="f74aa-109">0x004B</span><span class="sxs-lookup"><span data-stu-id="f74aa-109">0x004B</span></span>  <br/> |
|<span data-ttu-id="f74aa-110">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="f74aa-110">Data type:</span></span>  <br/> |<span data-ttu-id="f74aa-111">PT_STRING8, PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="f74aa-111">PT_STRING8, PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="f74aa-112">Bereich:</span><span class="sxs-lookup"><span data-stu-id="f74aa-112">Area:</span></span>  <br/> |<span data-ttu-id="f74aa-113">Eigenschaften für sichere Nachrichtenübermittlung</span><span class="sxs-lookup"><span data-stu-id="f74aa-113">Secure Messaging Properties</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="f74aa-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="f74aa-114">Remarks</span></span>

<span data-ttu-id="f74aa-115">Diese Eigenschaften enthalten eine Kopie der **PR_MESSAGE_CLASS** ([PidTagMessageClass](pidtagmessageclass-canonical-property.md))-Eigenschaft der Nachricht, für die der Bericht generiert wird.</span><span class="sxs-lookup"><span data-stu-id="f74aa-115">These properties contain a copy of the **PR_MESSAGE_CLASS** ([PidTagMessageClass](pidtagmessageclass-canonical-property.md)) property of the message for which the report is being generated.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="f74aa-116">Zugehörige Ressourcen</span><span class="sxs-lookup"><span data-stu-id="f74aa-116">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="f74aa-117">Protokollspezifikationen</span><span class="sxs-lookup"><span data-stu-id="f74aa-117">Protocol specifications</span></span>

<span data-ttu-id="f74aa-118">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="f74aa-118">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="f74aa-119">Enthält Verweise auf zugehörige Exchange Server-Protokollspezifikationen.</span><span class="sxs-lookup"><span data-stu-id="f74aa-119">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="f74aa-120">[[MS-OXTNEF]](https://msdn.microsoft.com/library/1f0544d7-30b7-4194-b58f-adc82f3763bb%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="f74aa-120">[[MS-OXTNEF]](https://msdn.microsoft.com/library/1f0544d7-30b7-4194-b58f-adc82f3763bb%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="f74aa-121">Codiert und dekodiert Message-und Attachment-Objekte in einer effizienten Datenstrom Darstellung.</span><span class="sxs-lookup"><span data-stu-id="f74aa-121">Encodes and decodes message and attachment objects to an efficient stream representation.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="f74aa-122">Header Dateien</span><span class="sxs-lookup"><span data-stu-id="f74aa-122">Header files</span></span>

<span data-ttu-id="f74aa-123">Mapidefs. h</span><span class="sxs-lookup"><span data-stu-id="f74aa-123">Mapidefs.h</span></span>
  
> <span data-ttu-id="f74aa-124">Stellt Datentypdefinitionen bereit.</span><span class="sxs-lookup"><span data-stu-id="f74aa-124">Provides data type definitions.</span></span>
    
<span data-ttu-id="f74aa-125">Mapitags. h</span><span class="sxs-lookup"><span data-stu-id="f74aa-125">Mapitags.h</span></span>
  
> <span data-ttu-id="f74aa-126">Enthält Definitionen von Eigenschaften, die als zugeordnete Eigenschaften aufgelistet sind.</span><span class="sxs-lookup"><span data-stu-id="f74aa-126">Contains definitions of properties listed as associated properties.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="f74aa-127">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="f74aa-127">See also</span></span>



[<span data-ttu-id="f74aa-128">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="f74aa-128">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="f74aa-129">Kanonische MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="f74aa-129">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="f74aa-130">Zuordnen von kanonischen Eigenschaftennamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="f74aa-130">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="f74aa-131">Zuordnen von MAPI-Namen zu kanonischen Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="f74aa-131">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

