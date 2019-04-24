---
title: Kanonische Pidlidtaskmultiplerecipients (-Eigenschaft
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidTaskMultipleRecipients
api_type:
- COM
ms.assetid: 28ba9997-72dd-465f-94a7-35a317a361ef
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: 3b260917e107086dee6176f73b6c82c3a1825327
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32360067"
---
# <a name="pidlidtaskmultiplerecipients-canonical-property"></a><span data-ttu-id="3cf32-103">Kanonische Pidlidtaskmultiplerecipients (-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="3cf32-103">PidLidTaskMultipleRecipients Canonical Property</span></span>

  
  
<span data-ttu-id="3cf32-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="3cf32-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="3cf32-105">Bietet Optimierungshinweise zu den Empfängern einer Aufgabe.</span><span class="sxs-lookup"><span data-stu-id="3cf32-105">Provides optimization hints about the recipients of a task.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="3cf32-106">Zugeordnete Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="3cf32-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="3cf32-107">dispidTaskMultRecips</span><span class="sxs-lookup"><span data-stu-id="3cf32-107">dispidTaskMultRecips</span></span>  <br/> |
|<span data-ttu-id="3cf32-108">Eigenschaftensatz:</span><span class="sxs-lookup"><span data-stu-id="3cf32-108">Property set:</span></span>  <br/> |<span data-ttu-id="3cf32-109">PSETID_Task</span><span class="sxs-lookup"><span data-stu-id="3cf32-109">PSETID_Task</span></span>  <br/> |
|<span data-ttu-id="3cf32-110">Long-ID (Deckel):</span><span class="sxs-lookup"><span data-stu-id="3cf32-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="3cf32-111">0x00008120</span><span class="sxs-lookup"><span data-stu-id="3cf32-111">0x00008120</span></span>  <br/> |
|<span data-ttu-id="3cf32-112">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="3cf32-112">Data type:</span></span>  <br/> |<span data-ttu-id="3cf32-113">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="3cf32-113">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="3cf32-114">Bereich:</span><span class="sxs-lookup"><span data-stu-id="3cf32-114">Area:</span></span>  <br/> |<span data-ttu-id="3cf32-115">Aufgabe</span><span class="sxs-lookup"><span data-stu-id="3cf32-115">Task</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="3cf32-116">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="3cf32-116">Remarks</span></span>

<span data-ttu-id="3cf32-117">Wenn diese Eigenschaft festgelegt ist, muss Sie auf eine bitweise **or** -Operation mit 0 oder mehr der folgenden Werte festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="3cf32-117">If set, this property must be set to a bitwise **OR** operation of zero or more of the following values.</span></span> 
  
|<span data-ttu-id="3cf32-118">**Name**</span><span class="sxs-lookup"><span data-stu-id="3cf32-118">**Name**</span></span>|<span data-ttu-id="3cf32-119">**Wert**</span><span class="sxs-lookup"><span data-stu-id="3cf32-119">**Value**</span></span>|<span data-ttu-id="3cf32-120">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="3cf32-120">**Description**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="3cf32-121">Gesendet</span><span class="sxs-lookup"><span data-stu-id="3cf32-121">Sent</span></span>  <br/> |<span data-ttu-id="3cf32-122">0x00000001</span><span class="sxs-lookup"><span data-stu-id="3cf32-122">0x00000001</span></span>  <br/> |<span data-ttu-id="3cf32-123">Die Aufgabe hat mehrere primäre Empfänger.</span><span class="sxs-lookup"><span data-stu-id="3cf32-123">The task has multiple primary recipients.</span></span>  <br/> |
|<span data-ttu-id="3cf32-124">Auszahlung</span><span class="sxs-lookup"><span data-stu-id="3cf32-124">Received</span></span>  <br/> |<span data-ttu-id="3cf32-125">0x00000002</span><span class="sxs-lookup"><span data-stu-id="3cf32-125">0x00000002</span></span>  <br/> |<span data-ttu-id="3cf32-126">Obwohl der gesendete Hinweis nicht vorhanden war, erkannte der Client, dass die Aufgabe mehrere primäre Empfänger hat.</span><span class="sxs-lookup"><span data-stu-id="3cf32-126">Although the Sent hint was not present, the client detected that the task has multiple primary recipients.</span></span>  <br/> |
|<span data-ttu-id="3cf32-127">Reserved</span><span class="sxs-lookup"><span data-stu-id="3cf32-127">Reserved</span></span>  <br/> |<span data-ttu-id="3cf32-128">0x00000004</span><span class="sxs-lookup"><span data-stu-id="3cf32-128">0x00000004</span></span>  <br/> |<span data-ttu-id="3cf32-129">Dieser Wert ist reserviert.</span><span class="sxs-lookup"><span data-stu-id="3cf32-129">This value is reserved.</span></span>  <br/> |
   
## <a name="related-resources"></a><span data-ttu-id="3cf32-130">Zugehörige Ressourcen</span><span class="sxs-lookup"><span data-stu-id="3cf32-130">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="3cf32-131">Protokollspezifikationen</span><span class="sxs-lookup"><span data-stu-id="3cf32-131">Protocol specifications</span></span>

<span data-ttu-id="3cf32-132">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="3cf32-132">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="3cf32-133">Stellt Eigenschaftensatz Definitionen und Verweise auf zugehörige Exchange Server-Protokollspezifikationen bereit.</span><span class="sxs-lookup"><span data-stu-id="3cf32-133">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="3cf32-134">[[MS-OXOTASK]](https://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="3cf32-134">[[MS-OXOTASK]](https://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="3cf32-135">Definiert mehrere Objekte, die das elektronische Äquivalent von Aufgaben, Vorgangszuordnungen und Vorgangsaktualisierungen modellieren.</span><span class="sxs-lookup"><span data-stu-id="3cf32-135">Defines several objects that model the electronic equivalent of tasks, task assignments, and task updates.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="3cf32-136">Header Dateien</span><span class="sxs-lookup"><span data-stu-id="3cf32-136">Header files</span></span>

<span data-ttu-id="3cf32-137">Mapidefs. h</span><span class="sxs-lookup"><span data-stu-id="3cf32-137">Mapidefs.h</span></span>
  
> <span data-ttu-id="3cf32-138">Stellt Datentypdefinitionen bereit.</span><span class="sxs-lookup"><span data-stu-id="3cf32-138">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="3cf32-139">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="3cf32-139">See also</span></span>



[<span data-ttu-id="3cf32-140">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="3cf32-140">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="3cf32-141">Kanonische MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="3cf32-141">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="3cf32-142">Zuordnen von kanonischen Eigenschaftennamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="3cf32-142">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="3cf32-143">Zuordnen von MAPI-Namen zu kanonischen Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="3cf32-143">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

