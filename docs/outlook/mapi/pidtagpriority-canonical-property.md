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
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/04/2018
ms.locfileid: "25385452"
---
# <a name="pidtagpriority-canonical-property"></a><span data-ttu-id="6adfb-103">PidTagPriority (kanonische Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="6adfb-103">PidTagPriority Canonical Property</span></span>

  
  
<span data-ttu-id="6adfb-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="6adfb-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="6adfb-105">Die relative Priorität der Nachricht enthält.</span><span class="sxs-lookup"><span data-stu-id="6adfb-105">Contains the relative priority of a message.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="6adfb-106">Zugeordnete Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="6adfb-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="6adfb-107">PR_PRIORITY</span><span class="sxs-lookup"><span data-stu-id="6adfb-107">PR_PRIORITY</span></span>  <br/> |
|<span data-ttu-id="6adfb-108">Kennung:</span><span class="sxs-lookup"><span data-stu-id="6adfb-108">Identifier:</span></span>  <br/> |<span data-ttu-id="6adfb-109">0x0026</span><span class="sxs-lookup"><span data-stu-id="6adfb-109">0x0026</span></span>  <br/> |
|<span data-ttu-id="6adfb-110">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="6adfb-110">Data type:</span></span>  <br/> |<span data-ttu-id="6adfb-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="6adfb-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="6adfb-112">Bereich:</span><span class="sxs-lookup"><span data-stu-id="6adfb-112">Area:</span></span>  <br/> |<span data-ttu-id="6adfb-113">E-Mail</span><span class="sxs-lookup"><span data-stu-id="6adfb-113">Email</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="6adfb-114">Hinweise</span><span class="sxs-lookup"><span data-stu-id="6adfb-114">Remarks</span></span>

<span data-ttu-id="6adfb-115">Diese Eigenschaft und die Eigenschaft **PR_IMPORTANCE** ([PidTagImportance](pidtagimportance-canonical-property.md)) darf nicht verwechselt werden.</span><span class="sxs-lookup"><span data-stu-id="6adfb-115">This property and the **PR_IMPORTANCE** ([PidTagImportance](pidtagimportance-canonical-property.md)) property should not be confused.</span></span> <span data-ttu-id="6adfb-116">Bedeutung der Wert für Benutzer, während der Priorität angibt, die Reihenfolge oder Geschwindigkeit, an dem die Nachricht soll, von der messaging-Systemsoftware gesendet werden, an.</span><span class="sxs-lookup"><span data-stu-id="6adfb-116">Importance indicates a value to users, while priority indicates the order or speed at which the message should be sent by the messaging system software.</span></span> <span data-ttu-id="6adfb-117">Höherer Priorität Gibt in der Regel höhere Kosten.</span><span class="sxs-lookup"><span data-stu-id="6adfb-117">Higher priority usually indicates a higher cost.</span></span> <span data-ttu-id="6adfb-118">Höhere Priorität ist in der Regel eine andere Darstellung von der Benutzeroberfläche zugeordnet.</span><span class="sxs-lookup"><span data-stu-id="6adfb-118">Higher importance usually is associated with a different display by the user interface.</span></span>
  
<span data-ttu-id="6adfb-119">Die Priorität einer Nachricht Bericht sollte dieselbe wie die Priorität der ursprünglichen Nachricht gemeldet wird.</span><span class="sxs-lookup"><span data-stu-id="6adfb-119">The priority of a report message should be the same as the priority of the original message being reported.</span></span>
  
<span data-ttu-id="6adfb-120">Diese Eigenschaft kann genau einen der folgenden Werte aufweisen:</span><span class="sxs-lookup"><span data-stu-id="6adfb-120">This property can have exactly one of the following values:</span></span>
  
<span data-ttu-id="6adfb-121">PRIO_NONURGENT</span><span class="sxs-lookup"><span data-stu-id="6adfb-121">PRIO_NONURGENT</span></span> 
  
> <span data-ttu-id="6adfb-122">Die Nachricht ist nicht dringend.</span><span class="sxs-lookup"><span data-stu-id="6adfb-122">The message is not urgent.</span></span>
    
<span data-ttu-id="6adfb-123">PRIO_NORMAL</span><span class="sxs-lookup"><span data-stu-id="6adfb-123">PRIO_NORMAL</span></span> 
  
> <span data-ttu-id="6adfb-124">Die Nachricht weist normalen Priorität.</span><span class="sxs-lookup"><span data-stu-id="6adfb-124">The message has normal priority.</span></span>
    
<span data-ttu-id="6adfb-125">PRIO_URGENT</span><span class="sxs-lookup"><span data-stu-id="6adfb-125">PRIO_URGENT</span></span> 
  
> <span data-ttu-id="6adfb-126">Die Nachricht ist dringend.</span><span class="sxs-lookup"><span data-stu-id="6adfb-126">The message is urgent.</span></span>
    
## <a name="related-resources"></a><span data-ttu-id="6adfb-127">Verwandte Ressourcen</span><span class="sxs-lookup"><span data-stu-id="6adfb-127">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="6adfb-128">Protokollspezifikationen</span><span class="sxs-lookup"><span data-stu-id="6adfb-128">Protocol specifications</span></span>

<span data-ttu-id="6adfb-129">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="6adfb-129">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="6adfb-130">Bietet Verweise auf Verwandte Exchange Server-Spezifikationen.</span><span class="sxs-lookup"><span data-stu-id="6adfb-130">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="6adfb-131">[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="6adfb-131">[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="6adfb-132">Gibt die Eigenschaften und Operationen, die für Objekte, die e-Mail-Nachricht zulässig sind.</span><span class="sxs-lookup"><span data-stu-id="6adfb-132">Specifies the properties and operations that are permissible on email message objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="6adfb-133">Header-Dateien</span><span class="sxs-lookup"><span data-stu-id="6adfb-133">Header files</span></span>

<span data-ttu-id="6adfb-134">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="6adfb-134">Mapidefs.h</span></span>
  
> <span data-ttu-id="6adfb-135">Enthält die Datentypdefinitionen.</span><span class="sxs-lookup"><span data-stu-id="6adfb-135">Provides data type definitions.</span></span>
    
<span data-ttu-id="6adfb-136">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="6adfb-136">Mapitags.h</span></span>
  
> <span data-ttu-id="6adfb-137">Enthält Definitionen von Eigenschaften, die als Alternative Namen aufgelistet.</span><span class="sxs-lookup"><span data-stu-id="6adfb-137">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="6adfb-138">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="6adfb-138">See also</span></span>



[<span data-ttu-id="6adfb-139">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="6adfb-139">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="6adfb-140">Kanonische MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="6adfb-140">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="6adfb-141">Zuordnen von kanonischen Eigenschaftennamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="6adfb-141">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="6adfb-142">Zuordnen von MAPI-Namen zu kanonische Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="6adfb-142">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

