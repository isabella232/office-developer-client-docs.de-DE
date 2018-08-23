---
title: PidLidTaskState (kanonische Eigenschaft)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidTaskState
api_type:
- COM
ms.assetid: 06d1f8a3-53e1-4c9a-9703-75de7a11a772
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: f2cd536a2f287e880388457586f6bdfa9f67f2b4
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2018
ms.locfileid: "22590848"
---
# <a name="pidlidtaskstate-canonical-property"></a><span data-ttu-id="536f2-103">PidLidTaskState (kanonische Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="536f2-103">PidLidTaskState Canonical Property</span></span>

  
  
<span data-ttu-id="536f2-104">**Betrifft**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="536f2-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="536f2-105">Gibt den aktuellen Status der Zuordnung des Vorgangs an.</span><span class="sxs-lookup"><span data-stu-id="536f2-105">Indicates the current assignment state of the task.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="536f2-106">Zugeordnete Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="536f2-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="536f2-107">dispidTaskState</span><span class="sxs-lookup"><span data-stu-id="536f2-107">dispidTaskState</span></span>  <br/> |
|<span data-ttu-id="536f2-108">-Eigenschaft festgelegt:</span><span class="sxs-lookup"><span data-stu-id="536f2-108">Property set:</span></span>  <br/> |<span data-ttu-id="536f2-109">PSETID_Task</span><span class="sxs-lookup"><span data-stu-id="536f2-109">PSETID_Task</span></span>  <br/> |
|<span data-ttu-id="536f2-110">Long-ID (Abdeckung):</span><span class="sxs-lookup"><span data-stu-id="536f2-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="536f2-111">0x00008113</span><span class="sxs-lookup"><span data-stu-id="536f2-111">0x00008113</span></span>  <br/> |
|<span data-ttu-id="536f2-112">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="536f2-112">Data type:</span></span>  <br/> |<span data-ttu-id="536f2-113">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="536f2-113">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="536f2-114">Bereich:</span><span class="sxs-lookup"><span data-stu-id="536f2-114">Area:</span></span>  <br/> |<span data-ttu-id="536f2-115">Aufgabe</span><span class="sxs-lookup"><span data-stu-id="536f2-115">Task</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="536f2-116">HinwBemerkungeneise</span><span class="sxs-lookup"><span data-stu-id="536f2-116">Remarks</span></span>

<span data-ttu-id="536f2-117">Der Wert dieser Eigenschaft muss eine der folgenden sein:</span><span class="sxs-lookup"><span data-stu-id="536f2-117">The value of this property must be one of the following.</span></span>
  
|<span data-ttu-id="536f2-118">**Wert**</span><span class="sxs-lookup"><span data-stu-id="536f2-118">**Value**</span></span>|<span data-ttu-id="536f2-119">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="536f2-119">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="536f2-120">0x00000000</span><span class="sxs-lookup"><span data-stu-id="536f2-120">0x00000000</span></span>  <br/> |<span data-ttu-id="536f2-121">Dieser Vorgang wurde erstellt, um eine Aufgabe zu entsprechen, die in einer Aufgabe Ablehnung eingebettete wurde aber lokal nicht gefunden werden konnte.</span><span class="sxs-lookup"><span data-stu-id="536f2-121">This task was created to correspond to a task that was embedded in a task rejection but could not be found locally.</span></span>  <br/> |
|<span data-ttu-id="536f2-122">0x00000001</span><span class="sxs-lookup"><span data-stu-id="536f2-122">0x00000001</span></span>  <br/> |<span data-ttu-id="536f2-123">Die Aufgabe wird nicht zugewiesen.</span><span class="sxs-lookup"><span data-stu-id="536f2-123">The task is not assigned.</span></span>  <br/> |
|<span data-ttu-id="536f2-124">0x00000002</span><span class="sxs-lookup"><span data-stu-id="536f2-124">0x00000002</span></span>  <br/> |<span data-ttu-id="536f2-125">Der Vorgang ist der Aufgabe zugewiesenen Kopie einer zugewiesenen Aufgabe.</span><span class="sxs-lookup"><span data-stu-id="536f2-125">The task is the task assignee's copy of an assigned task.</span></span>  <br/> |
|<span data-ttu-id="536f2-126">0 x 00000003</span><span class="sxs-lookup"><span data-stu-id="536f2-126">0x00000003</span></span>  <br/> |<span data-ttu-id="536f2-127">Die Aufgabe ist die Aufgabe delegierende Person Kopie einer zugewiesenen Aufgabe.</span><span class="sxs-lookup"><span data-stu-id="536f2-127">The task is the task assigner's copy of an assigned task.</span></span>  <br/> |
|<span data-ttu-id="536f2-128">0 x 00000004</span><span class="sxs-lookup"><span data-stu-id="536f2-128">0x00000004</span></span>  <br/> |<span data-ttu-id="536f2-129">Die Aufgabe ist die Aufgabe delegierende Person Kopie einer abgelehnten Aufgabe.</span><span class="sxs-lookup"><span data-stu-id="536f2-129">The task is the task assigner's copy of a rejected task.</span></span>  <br/> |
   
## <a name="related-resources"></a><span data-ttu-id="536f2-130">Verwandte Ressourcen</span><span class="sxs-lookup"><span data-stu-id="536f2-130">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="536f2-131">Protokollspezifikationen</span><span class="sxs-lookup"><span data-stu-id="536f2-131">Protocol specifications</span></span>

<span data-ttu-id="536f2-132">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="536f2-132">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="536f2-133">Enthält Eigenschaftendefinitionen und Verweise auf Verwandte Exchange Server-Spezifikationen.</span><span class="sxs-lookup"><span data-stu-id="536f2-133">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="536f2-134">[[MS-OXOTASK]](http://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="536f2-134">[[MS-OXOTASK]](http://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="536f2-135">Mehrere Objekte, die das elektronische Äquivalent von Aufgaben, vorgangszuordnungen und vorgangsaktualisierungen Modell definiert.</span><span class="sxs-lookup"><span data-stu-id="536f2-135">Defines several objects that model the electronic equivalent of tasks, task assignments, and task updates.</span></span>
    
<span data-ttu-id="536f2-136">[[MS-OXOSFLD]](http://msdn.microsoft.com/library/a60e9c16-2ba8-424b-b60c-385a8a2837cb%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="536f2-136">[[MS-OXOSFLD]](http://msdn.microsoft.com/library/a60e9c16-2ba8-424b-b60c-385a8a2837cb%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="536f2-137">Gibt die Eigenschaften und Operationen für das Erstellen und Ordner mit Sonderfunktion in einem Postfach suchen.</span><span class="sxs-lookup"><span data-stu-id="536f2-137">Specifies the properties and operations for creating and locating the special folders in a mailbox.</span></span>
    
<span data-ttu-id="536f2-138">[[MS-OXCICAL]](http://msdn.microsoft.com/library/a685a040-5b69-4c84-b084-795113fb4012%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="536f2-138">[[MS-OXCICAL]](http://msdn.microsoft.com/library/a685a040-5b69-4c84-b084-795113fb4012%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="536f2-139">Konvertiert zwischen IETF RFC2445, RFC2446, RFC2447, und Termine und meeting-Objekte.</span><span class="sxs-lookup"><span data-stu-id="536f2-139">Converts between IETF RFC2445, RFC2446, and RFC2447, and appointment and meeting objects.</span></span>
    
<span data-ttu-id="536f2-140">[[MS-OXCFXICS]](http://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="536f2-140">[[MS-OXCFXICS]](http://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="536f2-141">Verarbeitet die Reihenfolge und den Fluss für Datenübertragungen zwischen einem Client und Server.</span><span class="sxs-lookup"><span data-stu-id="536f2-141">Handles the order and flow for data transfers between a client and server.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="536f2-142">Header-Dateien</span><span class="sxs-lookup"><span data-stu-id="536f2-142">Header files</span></span>

<span data-ttu-id="536f2-143">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="536f2-143">Mapidefs.h</span></span>
  
> <span data-ttu-id="536f2-144">Enthält die Datentypdefinitionen.</span><span class="sxs-lookup"><span data-stu-id="536f2-144">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="536f2-145">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="536f2-145">See also</span></span>



[<span data-ttu-id="536f2-146">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="536f2-146">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="536f2-147">Kanonische MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="536f2-147">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="536f2-148">Zuordnen von kanonischen Eigenschaftennamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="536f2-148">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="536f2-149">Zuordnen von MAPI-Namen zu kanonische Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="536f2-149">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

