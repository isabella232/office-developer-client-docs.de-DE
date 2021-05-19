---
title: PidTagPriority (kanonische Eigenschaft)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagPriority
api_type:
- COM
ms.assetid: 0f3a628f-5f8e-4716-98cc-868bd3400ba9
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: b9c0f5ebeae21d6d683bbb5def727d29a34bcdb6
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32339431"
---
# <a name="pidtagpriority-canonical-property"></a><span data-ttu-id="b4ac6-103">PidTagPriority (kanonische Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="b4ac6-103">PidTagPriority Canonical Property</span></span>

  
  
<span data-ttu-id="b4ac6-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="b4ac6-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="b4ac6-105">Enthält die relative Priorität einer Nachricht.</span><span class="sxs-lookup"><span data-stu-id="b4ac6-105">Contains the relative priority of a message.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="b4ac6-106">Zugeordnete Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="b4ac6-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="b4ac6-107">PR_PRIORITY</span><span class="sxs-lookup"><span data-stu-id="b4ac6-107">PR_PRIORITY</span></span>  <br/> |
|<span data-ttu-id="b4ac6-108">Kennung:</span><span class="sxs-lookup"><span data-stu-id="b4ac6-108">Identifier:</span></span>  <br/> |<span data-ttu-id="b4ac6-109">0x0026</span><span class="sxs-lookup"><span data-stu-id="b4ac6-109">0x0026</span></span>  <br/> |
|<span data-ttu-id="b4ac6-110">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="b4ac6-110">Data type:</span></span>  <br/> |<span data-ttu-id="b4ac6-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="b4ac6-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="b4ac6-112">Bereich:</span><span class="sxs-lookup"><span data-stu-id="b4ac6-112">Area:</span></span>  <br/> |<span data-ttu-id="b4ac6-113">E-Mails</span><span class="sxs-lookup"><span data-stu-id="b4ac6-113">Email</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="b4ac6-114">Hinweise</span><span class="sxs-lookup"><span data-stu-id="b4ac6-114">Remarks</span></span>

<span data-ttu-id="b4ac6-115">Diese Eigenschaft und die **PR_IMPORTANCE** ([PidTagImportance](pidtagimportance-canonical-property.md)) -Eigenschaft sollten nicht verwechselt werden.</span><span class="sxs-lookup"><span data-stu-id="b4ac6-115">This property and the **PR_IMPORTANCE** ([PidTagImportance](pidtagimportance-canonical-property.md)) property should not be confused.</span></span> <span data-ttu-id="b4ac6-116">Importance gibt einen Wert für Benutzer an, während priorität die Reihenfolge oder Geschwindigkeit angibt, mit der die Nachricht von der Messagingsystemsoftware gesendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="b4ac6-116">Importance indicates a value to users, while priority indicates the order or speed at which the message should be sent by the messaging system software.</span></span> <span data-ttu-id="b4ac6-117">Höhere Priorität bedeutet in der Regel höhere Kosten.</span><span class="sxs-lookup"><span data-stu-id="b4ac6-117">Higher priority usually indicates a higher cost.</span></span> <span data-ttu-id="b4ac6-118">Eine höhere Wichtigkeit wird in der Regel einer anderen Anzeige durch die Benutzeroberfläche zugeordnet.</span><span class="sxs-lookup"><span data-stu-id="b4ac6-118">Higher importance usually is associated with a different display by the user interface.</span></span>
  
<span data-ttu-id="b4ac6-119">Die Priorität einer Berichtsnachricht sollte mit der Priorität der ursprünglichen gemeldeten Nachricht identisch sein.</span><span class="sxs-lookup"><span data-stu-id="b4ac6-119">The priority of a report message should be the same as the priority of the original message being reported.</span></span>
  
<span data-ttu-id="b4ac6-120">Diese Eigenschaft kann genau einen der folgenden Werte haben:</span><span class="sxs-lookup"><span data-stu-id="b4ac6-120">This property can have exactly one of the following values:</span></span>
  
<span data-ttu-id="b4ac6-121">PRIO_NONURGENT</span><span class="sxs-lookup"><span data-stu-id="b4ac6-121">PRIO_NONURGENT</span></span> 
  
> <span data-ttu-id="b4ac6-122">Die Nachricht ist nicht dringend.</span><span class="sxs-lookup"><span data-stu-id="b4ac6-122">The message is not urgent.</span></span>
    
<span data-ttu-id="b4ac6-123">PRIO_NORMAL</span><span class="sxs-lookup"><span data-stu-id="b4ac6-123">PRIO_NORMAL</span></span> 
  
> <span data-ttu-id="b4ac6-124">Die Nachricht hat normale Priorität.</span><span class="sxs-lookup"><span data-stu-id="b4ac6-124">The message has normal priority.</span></span>
    
<span data-ttu-id="b4ac6-125">PRIO_URGENT</span><span class="sxs-lookup"><span data-stu-id="b4ac6-125">PRIO_URGENT</span></span> 
  
> <span data-ttu-id="b4ac6-126">Die Nachricht ist dringend.</span><span class="sxs-lookup"><span data-stu-id="b4ac6-126">The message is urgent.</span></span>
    
## <a name="related-resources"></a><span data-ttu-id="b4ac6-127">Verwandte Ressourcen</span><span class="sxs-lookup"><span data-stu-id="b4ac6-127">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="b4ac6-128">Protokollspezifikationen</span><span class="sxs-lookup"><span data-stu-id="b4ac6-128">Protocol specifications</span></span>

<span data-ttu-id="b4ac6-129">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="b4ac6-129">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="b4ac6-130">Enthält Verweise auf Exchange Server Protokollspezifikationen.</span><span class="sxs-lookup"><span data-stu-id="b4ac6-130">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="b4ac6-131">[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="b4ac6-131">[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="b4ac6-132">Gibt die Eigenschaften und Vorgänge an, die für E-Mail-Nachrichtenobjekte zulässig sind.</span><span class="sxs-lookup"><span data-stu-id="b4ac6-132">Specifies the properties and operations that are permissible on email message objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="b4ac6-133">Headerdateien</span><span class="sxs-lookup"><span data-stu-id="b4ac6-133">Header files</span></span>

<span data-ttu-id="b4ac6-134">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="b4ac6-134">Mapidefs.h</span></span>
  
> <span data-ttu-id="b4ac6-135">Bietet Datentypdefinitionen.</span><span class="sxs-lookup"><span data-stu-id="b4ac6-135">Provides data type definitions.</span></span>
    
<span data-ttu-id="b4ac6-136">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="b4ac6-136">Mapitags.h</span></span>
  
> <span data-ttu-id="b4ac6-137">Enthält Definitionen von Eigenschaften, die als alternative Namen aufgeführt sind.</span><span class="sxs-lookup"><span data-stu-id="b4ac6-137">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="b4ac6-138">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="b4ac6-138">See also</span></span>



[<span data-ttu-id="b4ac6-139">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="b4ac6-139">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="b4ac6-140">KANONISCHE EIGENSCHAFTEN VON MAPI</span><span class="sxs-lookup"><span data-stu-id="b4ac6-140">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="b4ac6-141">Zuordnen kanonischer Eigenschaftsnamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="b4ac6-141">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="b4ac6-142">Zuordnen von MAPI-Namen zu kanonischen Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="b4ac6-142">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

