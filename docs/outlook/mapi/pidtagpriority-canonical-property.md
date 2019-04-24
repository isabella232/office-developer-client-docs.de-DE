---
title: Kanonische Pidtagpriority (-Eigenschaft
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
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: b9c0f5ebeae21d6d683bbb5def727d29a34bcdb6
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32339431"
---
# <a name="pidtagpriority-canonical-property"></a><span data-ttu-id="b1fbf-103">Kanonische Pidtagpriority (-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="b1fbf-103">PidTagPriority Canonical Property</span></span>

  
  
<span data-ttu-id="b1fbf-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="b1fbf-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="b1fbf-105">Enthält die relative Priorität einer Nachricht.</span><span class="sxs-lookup"><span data-stu-id="b1fbf-105">Contains the relative priority of a message.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="b1fbf-106">Zugeordnete Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="b1fbf-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="b1fbf-107">PR_PRIORITY</span><span class="sxs-lookup"><span data-stu-id="b1fbf-107">PR_PRIORITY</span></span>  <br/> |
|<span data-ttu-id="b1fbf-108">Kennung:</span><span class="sxs-lookup"><span data-stu-id="b1fbf-108">Identifier:</span></span>  <br/> |<span data-ttu-id="b1fbf-109">0x0026</span><span class="sxs-lookup"><span data-stu-id="b1fbf-109">0x0026</span></span>  <br/> |
|<span data-ttu-id="b1fbf-110">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="b1fbf-110">Data type:</span></span>  <br/> |<span data-ttu-id="b1fbf-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="b1fbf-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="b1fbf-112">Bereich:</span><span class="sxs-lookup"><span data-stu-id="b1fbf-112">Area:</span></span>  <br/> |<span data-ttu-id="b1fbf-113">E-Mail</span><span class="sxs-lookup"><span data-stu-id="b1fbf-113">Email</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="b1fbf-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="b1fbf-114">Remarks</span></span>

<span data-ttu-id="b1fbf-115">Diese Eigenschaft und die **PR_IMPORTANCE** ([PidTagImportance](pidtagimportance-canonical-property.md))-Eigenschaft sollten nicht verwechselt werden.</span><span class="sxs-lookup"><span data-stu-id="b1fbf-115">This property and the **PR_IMPORTANCE** ([PidTagImportance](pidtagimportance-canonical-property.md)) property should not be confused.</span></span> <span data-ttu-id="b1fbf-116">Wichtigkeit gibt einen Wert für Benutzer an, während Priority die Reihenfolge oder Geschwindigkeit angibt, mit der die Nachricht von der Messagingsystem Software gesendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="b1fbf-116">Importance indicates a value to users, while priority indicates the order or speed at which the message should be sent by the messaging system software.</span></span> <span data-ttu-id="b1fbf-117">Höhere Priorität weist in der Regel auf höhere Kosten hin.</span><span class="sxs-lookup"><span data-stu-id="b1fbf-117">Higher priority usually indicates a higher cost.</span></span> <span data-ttu-id="b1fbf-118">Höhere Wichtigkeit wird in der Regel einer anderen Anzeige von der Benutzeroberfläche zugeordnet.</span><span class="sxs-lookup"><span data-stu-id="b1fbf-118">Higher importance usually is associated with a different display by the user interface.</span></span>
  
<span data-ttu-id="b1fbf-119">Die Priorität einer Berichtnachricht sollte mit der Priorität der gemeldeten ursprünglichen Nachricht übereinstimmen.</span><span class="sxs-lookup"><span data-stu-id="b1fbf-119">The priority of a report message should be the same as the priority of the original message being reported.</span></span>
  
<span data-ttu-id="b1fbf-120">Diese Eigenschaft kann genau einen der folgenden Werte haben:</span><span class="sxs-lookup"><span data-stu-id="b1fbf-120">This property can have exactly one of the following values:</span></span>
  
<span data-ttu-id="b1fbf-121">PRIO_NONURGENT</span><span class="sxs-lookup"><span data-stu-id="b1fbf-121">PRIO_NONURGENT</span></span> 
  
> <span data-ttu-id="b1fbf-122">Die Nachricht ist nicht dringlich.</span><span class="sxs-lookup"><span data-stu-id="b1fbf-122">The message is not urgent.</span></span>
    
<span data-ttu-id="b1fbf-123">PRIO_NORMAL</span><span class="sxs-lookup"><span data-stu-id="b1fbf-123">PRIO_NORMAL</span></span> 
  
> <span data-ttu-id="b1fbf-124">Die Nachricht hat die normale Priorität.</span><span class="sxs-lookup"><span data-stu-id="b1fbf-124">The message has normal priority.</span></span>
    
<span data-ttu-id="b1fbf-125">PRIO_URGENT</span><span class="sxs-lookup"><span data-stu-id="b1fbf-125">PRIO_URGENT</span></span> 
  
> <span data-ttu-id="b1fbf-126">Die Nachricht ist dringend.</span><span class="sxs-lookup"><span data-stu-id="b1fbf-126">The message is urgent.</span></span>
    
## <a name="related-resources"></a><span data-ttu-id="b1fbf-127">Zugehörige Ressourcen</span><span class="sxs-lookup"><span data-stu-id="b1fbf-127">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="b1fbf-128">Protokollspezifikationen</span><span class="sxs-lookup"><span data-stu-id="b1fbf-128">Protocol specifications</span></span>

<span data-ttu-id="b1fbf-129">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="b1fbf-129">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="b1fbf-130">Enthält Verweise auf zugehörige Exchange Server-Protokollspezifikationen.</span><span class="sxs-lookup"><span data-stu-id="b1fbf-130">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="b1fbf-131">[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="b1fbf-131">[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="b1fbf-132">Gibt die Eigenschaften und Vorgänge an, die für e-Mail-Nachrichtenobjekte zulässig sind.</span><span class="sxs-lookup"><span data-stu-id="b1fbf-132">Specifies the properties and operations that are permissible on email message objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="b1fbf-133">Header Dateien</span><span class="sxs-lookup"><span data-stu-id="b1fbf-133">Header files</span></span>

<span data-ttu-id="b1fbf-134">Mapidefs. h</span><span class="sxs-lookup"><span data-stu-id="b1fbf-134">Mapidefs.h</span></span>
  
> <span data-ttu-id="b1fbf-135">Stellt Datentypdefinitionen bereit.</span><span class="sxs-lookup"><span data-stu-id="b1fbf-135">Provides data type definitions.</span></span>
    
<span data-ttu-id="b1fbf-136">Mapitags. h</span><span class="sxs-lookup"><span data-stu-id="b1fbf-136">Mapitags.h</span></span>
  
> <span data-ttu-id="b1fbf-137">Enthält Definitionen von Eigenschaften, die als Alternative Namen aufgeführt sind.</span><span class="sxs-lookup"><span data-stu-id="b1fbf-137">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="b1fbf-138">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="b1fbf-138">See also</span></span>



[<span data-ttu-id="b1fbf-139">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="b1fbf-139">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="b1fbf-140">Kanonische MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="b1fbf-140">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="b1fbf-141">Zuordnen von kanonischen Eigenschaftennamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="b1fbf-141">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="b1fbf-142">Zuordnen von MAPI-Namen zu kanonischen Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="b1fbf-142">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

