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
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/04/2018
ms.locfileid: "25400831"
---
# <a name="pidtagimportance-canonical-property"></a><span data-ttu-id="18758-103">PidTagImportance (kanonische Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="18758-103">PidTagImportance Canonical Property</span></span>

  
  
<span data-ttu-id="18758-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="18758-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="18758-105">Enthält einen Wert, der den Nachrichtenabsender Opinion die Wichtigkeitsstufe einer Nachricht angibt.</span><span class="sxs-lookup"><span data-stu-id="18758-105">Contains a value that indicates the message sender's opinion of the importance of a message.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="18758-106">Zugeordnete Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="18758-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="18758-107">PR_IMPORTANCE</span><span class="sxs-lookup"><span data-stu-id="18758-107">PR_IMPORTANCE</span></span>  <br/> |
|<span data-ttu-id="18758-108">Kennung:</span><span class="sxs-lookup"><span data-stu-id="18758-108">Identifier:</span></span>  <br/> |<span data-ttu-id="18758-109">0x0017</span><span class="sxs-lookup"><span data-stu-id="18758-109">0x0017</span></span>  <br/> |
|<span data-ttu-id="18758-110">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="18758-110">Data type:</span></span>  <br/> |<span data-ttu-id="18758-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="18758-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="18758-112">Bereich:</span><span class="sxs-lookup"><span data-stu-id="18758-112">Area:</span></span>  <br/> |<span data-ttu-id="18758-113">Allgemeine messaging</span><span class="sxs-lookup"><span data-stu-id="18758-113">General messaging</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="18758-114">Hinweise</span><span class="sxs-lookup"><span data-stu-id="18758-114">Remarks</span></span>

<span data-ttu-id="18758-115">Diese Eigenschaft und die **PR_PRIORITY** ([PidTagPriority](pidtagpriority-canonical-property.md))-Eigenschaft darf nicht verwechselt werden.</span><span class="sxs-lookup"><span data-stu-id="18758-115">This property and the **PR_PRIORITY** ([PidTagPriority](pidtagpriority-canonical-property.md)) property should not be confused.</span></span> <span data-ttu-id="18758-116">Bedeutung der Wert für Benutzer, während der Priorität angibt, die Reihenfolge oder Geschwindigkeit, an dem die Nachricht soll, von der messaging-Systemsoftware gesendet werden, an.</span><span class="sxs-lookup"><span data-stu-id="18758-116">Importance indicates a value to users, while priority indicates the order or speed at which the message should be sent by the messaging system software.</span></span> <span data-ttu-id="18758-117">Höherer Priorität Gibt in der Regel höhere Kosten.</span><span class="sxs-lookup"><span data-stu-id="18758-117">Higher priority usually indicates a higher cost.</span></span> <span data-ttu-id="18758-118">Höhere Priorität ist in der Regel eine andere Darstellung von der Benutzeroberfläche zugeordnet.</span><span class="sxs-lookup"><span data-stu-id="18758-118">Higher importance usually is associated with a different display by the user interface.</span></span> 
  
<span data-ttu-id="18758-119">Diese Eigenschaft kann genau einen der folgenden Werte aufweisen:</span><span class="sxs-lookup"><span data-stu-id="18758-119">This property can have exactly one of the following values:</span></span>
  
<span data-ttu-id="18758-120">IMPORTANCE_LOW</span><span class="sxs-lookup"><span data-stu-id="18758-120">IMPORTANCE_LOW</span></span> 
  
> <span data-ttu-id="18758-121">Die Nachricht weist Wichtigkeit ' Niedrig '.</span><span class="sxs-lookup"><span data-stu-id="18758-121">The message has low importance.</span></span>
    
<span data-ttu-id="18758-122">IMPORTANCE_HIGH</span><span class="sxs-lookup"><span data-stu-id="18758-122">IMPORTANCE_HIGH</span></span> 
  
> <span data-ttu-id="18758-123">Die Nachricht weist hohen Priorität.</span><span class="sxs-lookup"><span data-stu-id="18758-123">The message has high importance.</span></span>
    
<span data-ttu-id="18758-124">IMPORTANCE_NORMAL</span><span class="sxs-lookup"><span data-stu-id="18758-124">IMPORTANCE_NORMAL</span></span> 
  
> <span data-ttu-id="18758-125">Die Nachricht weist die normale Bedeutung.</span><span class="sxs-lookup"><span data-stu-id="18758-125">The message has normal importance.</span></span>
    
## <a name="related-resources"></a><span data-ttu-id="18758-126">Verwandte Ressourcen</span><span class="sxs-lookup"><span data-stu-id="18758-126">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="18758-127">Protokollspezifikationen</span><span class="sxs-lookup"><span data-stu-id="18758-127">Protocol specifications</span></span>

<span data-ttu-id="18758-128">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="18758-128">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="18758-129">Bietet Verweise auf Verwandte Exchange Server-Spezifikationen.</span><span class="sxs-lookup"><span data-stu-id="18758-129">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="18758-130">[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="18758-130">[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="18758-131">Nachrichten und Anlagen Objekte behandelt.</span><span class="sxs-lookup"><span data-stu-id="18758-131">Handles message and attachment objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="18758-132">Header-Dateien</span><span class="sxs-lookup"><span data-stu-id="18758-132">Header files</span></span>

<span data-ttu-id="18758-133">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="18758-133">Mapidefs.h</span></span>
  
> <span data-ttu-id="18758-134">Enthält die Datentypdefinitionen.</span><span class="sxs-lookup"><span data-stu-id="18758-134">Provides data type definitions.</span></span>
    
<span data-ttu-id="18758-135">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="18758-135">Mapitags.h</span></span>
  
> <span data-ttu-id="18758-136">Enthält Definitionen von Eigenschaften, die als Alternative Namen aufgelistet.</span><span class="sxs-lookup"><span data-stu-id="18758-136">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="18758-137">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="18758-137">See also</span></span>



[<span data-ttu-id="18758-138">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="18758-138">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="18758-139">Kanonische MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="18758-139">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="18758-140">Zuordnen von kanonischen Eigenschaftennamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="18758-140">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="18758-141">Zuordnen von MAPI-Namen zu kanonische Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="18758-141">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

