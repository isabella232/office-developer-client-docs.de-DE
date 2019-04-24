---
title: Kanonische PidTagSensitivity-Eigenschaft
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagSensitivity
api_type:
- COM
ms.assetid: 5b678475-f2a8-4831-ad68-11654e09c821
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: eab8ce71d28a672d7069a1c16da5cd2cc2e149f7
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32342504"
---
# <a name="pidtagsensitivity-canonical-property"></a><span data-ttu-id="7d54b-103">Kanonische PidTagSensitivity-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="7d54b-103">PidTagSensitivity Canonical Property</span></span>

  
  
<span data-ttu-id="7d54b-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="7d54b-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="7d54b-105">Enthält einen Wert, der die Meinung des Nachrichtenabsenders zur Vertraulichkeit einer Nachricht angibt.</span><span class="sxs-lookup"><span data-stu-id="7d54b-105">Contains a value that indicates the message sender's opinion of the sensitivity of a message.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="7d54b-106">Zugeordnete Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="7d54b-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="7d54b-107">PR_SENSITIVITY</span><span class="sxs-lookup"><span data-stu-id="7d54b-107">PR_SENSITIVITY</span></span>  <br/> |
|<span data-ttu-id="7d54b-108">Kennung:</span><span class="sxs-lookup"><span data-stu-id="7d54b-108">Identifier:</span></span>  <br/> |<span data-ttu-id="7d54b-109">0x0036</span><span class="sxs-lookup"><span data-stu-id="7d54b-109">0x0036</span></span>  <br/> |
|<span data-ttu-id="7d54b-110">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="7d54b-110">Data type:</span></span>  <br/> |<span data-ttu-id="7d54b-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="7d54b-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="7d54b-112">Bereich:</span><span class="sxs-lookup"><span data-stu-id="7d54b-112">Area:</span></span>  <br/> |<span data-ttu-id="7d54b-113">Allgemeine Nachrichtenübermittlung</span><span class="sxs-lookup"><span data-stu-id="7d54b-113">General messaging</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="7d54b-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="7d54b-114">Remarks</span></span>

<span data-ttu-id="7d54b-115">Es wird empfohlen, dass Nachrichtenobjekte diese Eigenschaft verfügbar machen.</span><span class="sxs-lookup"><span data-stu-id="7d54b-115">It is recommended that message objects expose this property.</span></span>
  
<span data-ttu-id="7d54b-116">Diese Eigenschaft kann genau einen der folgenden Werte haben:</span><span class="sxs-lookup"><span data-stu-id="7d54b-116">This property can have exactly one of the following values:</span></span>
  
<span data-ttu-id="7d54b-117">SENSITIVITY_NONE</span><span class="sxs-lookup"><span data-stu-id="7d54b-117">SENSITIVITY_NONE</span></span> 
  
> <span data-ttu-id="7d54b-118">Die Nachricht hat keine besondere Vertraulichkeit.</span><span class="sxs-lookup"><span data-stu-id="7d54b-118">The message has no special sensitivity.</span></span>
    
<span data-ttu-id="7d54b-119">SENSITIVITY_PERSONAL</span><span class="sxs-lookup"><span data-stu-id="7d54b-119">SENSITIVITY_PERSONAL</span></span> 
  
> <span data-ttu-id="7d54b-120">Die Nachricht ist persönlich.</span><span class="sxs-lookup"><span data-stu-id="7d54b-120">The message is personal.</span></span>
    
<span data-ttu-id="7d54b-121">SENSITIVITY_PRIVATE</span><span class="sxs-lookup"><span data-stu-id="7d54b-121">SENSITIVITY_PRIVATE</span></span> 
  
> <span data-ttu-id="7d54b-122">Die Nachricht ist privat.</span><span class="sxs-lookup"><span data-stu-id="7d54b-122">The message is private.</span></span>
    
<span data-ttu-id="7d54b-123">SENSITIVITY_COMPANY_CONFIDENTIAL</span><span class="sxs-lookup"><span data-stu-id="7d54b-123">SENSITIVITY_COMPANY_CONFIDENTIAL</span></span> 
  
> <span data-ttu-id="7d54b-124">Die Nachricht wird als "Company Confidential" festgelegt.</span><span class="sxs-lookup"><span data-stu-id="7d54b-124">The message is designated company confidential.</span></span>
    
## <a name="related-resources"></a><span data-ttu-id="7d54b-125">Zugehörige Ressourcen</span><span class="sxs-lookup"><span data-stu-id="7d54b-125">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="7d54b-126">Protokollspezifikationen</span><span class="sxs-lookup"><span data-stu-id="7d54b-126">Protocol specifications</span></span>

<span data-ttu-id="7d54b-127">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="7d54b-127">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="7d54b-128">Enthält Verweise auf zugehörige Exchange Server-Protokollspezifikationen.</span><span class="sxs-lookup"><span data-stu-id="7d54b-128">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="7d54b-129">[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="7d54b-129">[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="7d54b-130">Verarbeitet Nachrichten-und Anlagenobjekte.</span><span class="sxs-lookup"><span data-stu-id="7d54b-130">Handles message and attachment objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="7d54b-131">Header Dateien</span><span class="sxs-lookup"><span data-stu-id="7d54b-131">Header files</span></span>

<span data-ttu-id="7d54b-132">Mapidefs. h</span><span class="sxs-lookup"><span data-stu-id="7d54b-132">Mapidefs.h</span></span>
  
> <span data-ttu-id="7d54b-133">Stellt Datentypdefinitionen bereit.</span><span class="sxs-lookup"><span data-stu-id="7d54b-133">Provides data type definitions.</span></span>
    
<span data-ttu-id="7d54b-134">Mapitags. h</span><span class="sxs-lookup"><span data-stu-id="7d54b-134">Mapitags.h</span></span>
  
> <span data-ttu-id="7d54b-135">Enthält Definitionen von Eigenschaften, die als Alternative Namen aufgeführt sind.</span><span class="sxs-lookup"><span data-stu-id="7d54b-135">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="7d54b-136">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="7d54b-136">See also</span></span>



[<span data-ttu-id="7d54b-137">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="7d54b-137">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="7d54b-138">Kanonische MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="7d54b-138">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="7d54b-139">Zuordnen von kanonischen Eigenschaftennamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="7d54b-139">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="7d54b-140">Zuordnen von MAPI-Namen zu kanonischen Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="7d54b-140">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

