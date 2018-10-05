---
title: PidLidTaskMultipleRecipients (kanonische Eigenschaft)
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
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 3b260917e107086dee6176f73b6c82c3a1825327
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/04/2018
ms.locfileid: "25391171"
---
# <a name="pidlidtaskmultiplerecipients-canonical-property"></a><span data-ttu-id="a2915-103">PidLidTaskMultipleRecipients (kanonische Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="a2915-103">PidLidTaskMultipleRecipients Canonical Property</span></span>

  
  
<span data-ttu-id="a2915-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="a2915-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="a2915-105">Enthält Tipps zum die Empfänger eines Vorgangs Optimierung.</span><span class="sxs-lookup"><span data-stu-id="a2915-105">Provides optimization hints about the recipients of a task.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="a2915-106">Zugeordnete Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="a2915-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="a2915-107">dispidTaskMultRecips</span><span class="sxs-lookup"><span data-stu-id="a2915-107">dispidTaskMultRecips</span></span>  <br/> |
|<span data-ttu-id="a2915-108">-Eigenschaft festgelegt:</span><span class="sxs-lookup"><span data-stu-id="a2915-108">Property set:</span></span>  <br/> |<span data-ttu-id="a2915-109">PSETID_Task</span><span class="sxs-lookup"><span data-stu-id="a2915-109">PSETID_Task</span></span>  <br/> |
|<span data-ttu-id="a2915-110">Long-ID (Abdeckung):</span><span class="sxs-lookup"><span data-stu-id="a2915-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="a2915-111">0x00008120</span><span class="sxs-lookup"><span data-stu-id="a2915-111">0x00008120</span></span>  <br/> |
|<span data-ttu-id="a2915-112">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="a2915-112">Data type:</span></span>  <br/> |<span data-ttu-id="a2915-113">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="a2915-113">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="a2915-114">Bereich:</span><span class="sxs-lookup"><span data-stu-id="a2915-114">Area:</span></span>  <br/> |<span data-ttu-id="a2915-115">Aufgabe</span><span class="sxs-lookup"><span data-stu-id="a2915-115">Task</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="a2915-116">Hinweise</span><span class="sxs-lookup"><span data-stu-id="a2915-116">Remarks</span></span>

<span data-ttu-id="a2915-117">Wenn Sie festlegen möchten, muss diese Eigenschaft auf eine bitweise **OR** -Operation 0 (null) oder mehreren der folgenden Werte festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="a2915-117">If set, this property must be set to a bitwise **OR** operation of zero or more of the following values.</span></span> 
  
|<span data-ttu-id="a2915-118">**Name**</span><span class="sxs-lookup"><span data-stu-id="a2915-118">**Name**</span></span>|<span data-ttu-id="a2915-119">**Wert**</span><span class="sxs-lookup"><span data-stu-id="a2915-119">**Value**</span></span>|<span data-ttu-id="a2915-120">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="a2915-120">**Description**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="a2915-121">Gesendet</span><span class="sxs-lookup"><span data-stu-id="a2915-121">Sent</span></span>  <br/> |<span data-ttu-id="a2915-122">0x00000001</span><span class="sxs-lookup"><span data-stu-id="a2915-122">0x00000001</span></span>  <br/> |<span data-ttu-id="a2915-123">Der Vorgang hat mehrere primäre Empfänger.</span><span class="sxs-lookup"><span data-stu-id="a2915-123">The task has multiple primary recipients.</span></span>  <br/> |
|<span data-ttu-id="a2915-124">Auszahlung</span><span class="sxs-lookup"><span data-stu-id="a2915-124">Received</span></span>  <br/> |<span data-ttu-id="a2915-125">0x00000002</span><span class="sxs-lookup"><span data-stu-id="a2915-125">0x00000002</span></span>  <br/> |<span data-ttu-id="a2915-126">Obwohl die gesendete Hint nicht vorhanden war, erkannt der Client, dass der Vorgang mehrere primäre Empfänger.</span><span class="sxs-lookup"><span data-stu-id="a2915-126">Although the Sent hint was not present, the client detected that the task has multiple primary recipients.</span></span>  <br/> |
|<span data-ttu-id="a2915-127">Reserviert</span><span class="sxs-lookup"><span data-stu-id="a2915-127">Reserved</span></span>  <br/> |<span data-ttu-id="a2915-128">0 x 00000004</span><span class="sxs-lookup"><span data-stu-id="a2915-128">0x00000004</span></span>  <br/> |<span data-ttu-id="a2915-129">Dieser Wert ist reserviert.</span><span class="sxs-lookup"><span data-stu-id="a2915-129">This value is reserved.</span></span>  <br/> |
   
## <a name="related-resources"></a><span data-ttu-id="a2915-130">Verwandte Ressourcen</span><span class="sxs-lookup"><span data-stu-id="a2915-130">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="a2915-131">Protokollspezifikationen</span><span class="sxs-lookup"><span data-stu-id="a2915-131">Protocol specifications</span></span>

<span data-ttu-id="a2915-132">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="a2915-132">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="a2915-133">Enthält Eigenschaftendefinitionen und Verweise auf Verwandte Exchange Server-Spezifikationen.</span><span class="sxs-lookup"><span data-stu-id="a2915-133">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="a2915-134">[[MS-OXOTASK]](https://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="a2915-134">[[MS-OXOTASK]](https://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="a2915-135">Mehrere Objekte, die das elektronische Äquivalent von Aufgaben, vorgangszuordnungen und vorgangsaktualisierungen Modell definiert.</span><span class="sxs-lookup"><span data-stu-id="a2915-135">Defines several objects that model the electronic equivalent of tasks, task assignments, and task updates.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="a2915-136">Header-Dateien</span><span class="sxs-lookup"><span data-stu-id="a2915-136">Header files</span></span>

<span data-ttu-id="a2915-137">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="a2915-137">Mapidefs.h</span></span>
  
> <span data-ttu-id="a2915-138">Enthält die Datentypdefinitionen.</span><span class="sxs-lookup"><span data-stu-id="a2915-138">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="a2915-139">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="a2915-139">See also</span></span>



[<span data-ttu-id="a2915-140">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="a2915-140">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="a2915-141">Kanonische MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="a2915-141">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="a2915-142">Zuordnen von kanonischen Eigenschaftennamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="a2915-142">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="a2915-143">Zuordnen von MAPI-Namen zu kanonische Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="a2915-143">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

