---
title: PidTagImportance (kanonische Eigenschaft)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagImportance
api_type:
- HeaderDef
ms.assetid: 274dd444-a863-4b53-bdbc-3763c375c43c
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 6bef8b05f2fbf94b74ee126b80dfc6ae0c5e9d11
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32327923"
---
# <a name="pidtagimportance-canonical-property"></a><span data-ttu-id="5194f-103">PidTagImportance (kanonische Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="5194f-103">PidTagImportance Canonical Property</span></span>

  
  
<span data-ttu-id="5194f-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="5194f-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="5194f-105">Enthält einen Wert, der die Meinung des Nachrichtensenders zur Wichtigkeit einer Nachricht angibt.</span><span class="sxs-lookup"><span data-stu-id="5194f-105">Contains a value that indicates the message sender's opinion of the importance of a message.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="5194f-106">Zugeordnete Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="5194f-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="5194f-107">PR_IMPORTANCE</span><span class="sxs-lookup"><span data-stu-id="5194f-107">PR_IMPORTANCE</span></span>  <br/> |
|<span data-ttu-id="5194f-108">Kennung:</span><span class="sxs-lookup"><span data-stu-id="5194f-108">Identifier:</span></span>  <br/> |<span data-ttu-id="5194f-109">0x0017</span><span class="sxs-lookup"><span data-stu-id="5194f-109">0x0017</span></span>  <br/> |
|<span data-ttu-id="5194f-110">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="5194f-110">Data type:</span></span>  <br/> |<span data-ttu-id="5194f-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="5194f-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="5194f-112">Bereich:</span><span class="sxs-lookup"><span data-stu-id="5194f-112">Area:</span></span>  <br/> |<span data-ttu-id="5194f-113">Allgemeines Messaging</span><span class="sxs-lookup"><span data-stu-id="5194f-113">General messaging</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="5194f-114">Hinweise</span><span class="sxs-lookup"><span data-stu-id="5194f-114">Remarks</span></span>

<span data-ttu-id="5194f-115">Diese Eigenschaft und die **PR_PRIORITY** ([PidTagPriority](pidtagpriority-canonical-property.md)) sollten nicht verwechselt werden.</span><span class="sxs-lookup"><span data-stu-id="5194f-115">This property and the **PR_PRIORITY** ([PidTagPriority](pidtagpriority-canonical-property.md)) property should not be confused.</span></span> <span data-ttu-id="5194f-116">Importance gibt einen Wert für Benutzer an, während priorität die Reihenfolge oder Geschwindigkeit angibt, mit der die Nachricht von der Messagingsystemsoftware gesendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="5194f-116">Importance indicates a value to users, while priority indicates the order or speed at which the message should be sent by the messaging system software.</span></span> <span data-ttu-id="5194f-117">Höhere Priorität bedeutet in der Regel höhere Kosten.</span><span class="sxs-lookup"><span data-stu-id="5194f-117">Higher priority usually indicates a higher cost.</span></span> <span data-ttu-id="5194f-118">Eine höhere Wichtigkeit wird in der Regel einer anderen Anzeige durch die Benutzeroberfläche zugeordnet.</span><span class="sxs-lookup"><span data-stu-id="5194f-118">Higher importance usually is associated with a different display by the user interface.</span></span> 
  
<span data-ttu-id="5194f-119">Diese Eigenschaft kann genau einen der folgenden Werte haben:</span><span class="sxs-lookup"><span data-stu-id="5194f-119">This property can have exactly one of the following values:</span></span>
  
<span data-ttu-id="5194f-120">IMPORTANCE_LOW</span><span class="sxs-lookup"><span data-stu-id="5194f-120">IMPORTANCE_LOW</span></span> 
  
> <span data-ttu-id="5194f-121">Die Nachricht hat eine geringe Bedeutung.</span><span class="sxs-lookup"><span data-stu-id="5194f-121">The message has low importance.</span></span>
    
<span data-ttu-id="5194f-122">IMPORTANCE_HIGH</span><span class="sxs-lookup"><span data-stu-id="5194f-122">IMPORTANCE_HIGH</span></span> 
  
> <span data-ttu-id="5194f-123">Die Nachricht hat eine hohe Bedeutung.</span><span class="sxs-lookup"><span data-stu-id="5194f-123">The message has high importance.</span></span>
    
<span data-ttu-id="5194f-124">IMPORTANCE_NORMAL</span><span class="sxs-lookup"><span data-stu-id="5194f-124">IMPORTANCE_NORMAL</span></span> 
  
> <span data-ttu-id="5194f-125">Die Nachricht hat normale Bedeutung.</span><span class="sxs-lookup"><span data-stu-id="5194f-125">The message has normal importance.</span></span>
    
## <a name="related-resources"></a><span data-ttu-id="5194f-126">Verwandte Ressourcen</span><span class="sxs-lookup"><span data-stu-id="5194f-126">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="5194f-127">Protokollspezifikationen</span><span class="sxs-lookup"><span data-stu-id="5194f-127">Protocol specifications</span></span>

<span data-ttu-id="5194f-128">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="5194f-128">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="5194f-129">Enthält Verweise auf Exchange Server Protokollspezifikationen.</span><span class="sxs-lookup"><span data-stu-id="5194f-129">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="5194f-130">[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="5194f-130">[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="5194f-131">Behandelt Nachrichten- und Anlagenobjekte.</span><span class="sxs-lookup"><span data-stu-id="5194f-131">Handles message and attachment objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="5194f-132">Headerdateien</span><span class="sxs-lookup"><span data-stu-id="5194f-132">Header files</span></span>

<span data-ttu-id="5194f-133">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="5194f-133">Mapidefs.h</span></span>
  
> <span data-ttu-id="5194f-134">Bietet Datentypdefinitionen.</span><span class="sxs-lookup"><span data-stu-id="5194f-134">Provides data type definitions.</span></span>
    
<span data-ttu-id="5194f-135">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="5194f-135">Mapitags.h</span></span>
  
> <span data-ttu-id="5194f-136">Enthält Definitionen von Eigenschaften, die als alternative Namen aufgeführt sind.</span><span class="sxs-lookup"><span data-stu-id="5194f-136">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="5194f-137">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="5194f-137">See also</span></span>



[<span data-ttu-id="5194f-138">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="5194f-138">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="5194f-139">KANONISCHE EIGENSCHAFTEN VON MAPI</span><span class="sxs-lookup"><span data-stu-id="5194f-139">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="5194f-140">Zuordnen kanonischer Eigenschaftsnamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="5194f-140">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="5194f-141">Zuordnen von MAPI-Namen zu kanonischen Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="5194f-141">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

