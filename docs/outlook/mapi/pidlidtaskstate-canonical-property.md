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
ms.openlocfilehash: 149f238ea53e0669f4d95c8e6c2b17a2b5a1c209
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/04/2018
ms.locfileid: "25400985"
---
# <a name="pidlidtaskstate-canonical-property"></a><span data-ttu-id="87d40-103">PidLidTaskState (kanonische Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="87d40-103">PidLidTaskState Canonical Property</span></span>

  
  
<span data-ttu-id="87d40-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="87d40-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="87d40-105">Gibt den aktuellen Status der Zuordnung des Vorgangs an.</span><span class="sxs-lookup"><span data-stu-id="87d40-105">Indicates the current assignment state of the task.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="87d40-106">Zugeordnete Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="87d40-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="87d40-107">dispidTaskState</span><span class="sxs-lookup"><span data-stu-id="87d40-107">dispidTaskState</span></span>  <br/> |
|<span data-ttu-id="87d40-108">-Eigenschaft festgelegt:</span><span class="sxs-lookup"><span data-stu-id="87d40-108">Property set:</span></span>  <br/> |<span data-ttu-id="87d40-109">PSETID_Task</span><span class="sxs-lookup"><span data-stu-id="87d40-109">PSETID_Task</span></span>  <br/> |
|<span data-ttu-id="87d40-110">Long-ID (Abdeckung):</span><span class="sxs-lookup"><span data-stu-id="87d40-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="87d40-111">0x00008113</span><span class="sxs-lookup"><span data-stu-id="87d40-111">0x00008113</span></span>  <br/> |
|<span data-ttu-id="87d40-112">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="87d40-112">Data type:</span></span>  <br/> |<span data-ttu-id="87d40-113">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="87d40-113">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="87d40-114">Bereich:</span><span class="sxs-lookup"><span data-stu-id="87d40-114">Area:</span></span>  <br/> |<span data-ttu-id="87d40-115">Aufgabe</span><span class="sxs-lookup"><span data-stu-id="87d40-115">Task</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="87d40-116">Hinweise</span><span class="sxs-lookup"><span data-stu-id="87d40-116">Remarks</span></span>

<span data-ttu-id="87d40-117">Der Wert dieser Eigenschaft muss eine der folgenden sein:</span><span class="sxs-lookup"><span data-stu-id="87d40-117">The value of this property must be one of the following.</span></span>
  
|<span data-ttu-id="87d40-118">**Wert**</span><span class="sxs-lookup"><span data-stu-id="87d40-118">**Value**</span></span>|<span data-ttu-id="87d40-119">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="87d40-119">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="87d40-120">0x00000000</span><span class="sxs-lookup"><span data-stu-id="87d40-120">0x00000000</span></span>  <br/> |<span data-ttu-id="87d40-121">Dieser Vorgang wurde erstellt, um eine Aufgabe zu entsprechen, die in einer Aufgabe Ablehnung eingebettete wurde aber lokal nicht gefunden werden konnte.</span><span class="sxs-lookup"><span data-stu-id="87d40-121">This task was created to correspond to a task that was embedded in a task rejection but could not be found locally.</span></span>  <br/> |
|<span data-ttu-id="87d40-122">0x00000001</span><span class="sxs-lookup"><span data-stu-id="87d40-122">0x00000001</span></span>  <br/> |<span data-ttu-id="87d40-123">Die Aufgabe wird nicht zugewiesen.</span><span class="sxs-lookup"><span data-stu-id="87d40-123">The task is not assigned.</span></span>  <br/> |
|<span data-ttu-id="87d40-124">0x00000002</span><span class="sxs-lookup"><span data-stu-id="87d40-124">0x00000002</span></span>  <br/> |<span data-ttu-id="87d40-125">Der Vorgang ist der Aufgabe zugewiesenen Kopie einer zugewiesenen Aufgabe.</span><span class="sxs-lookup"><span data-stu-id="87d40-125">The task is the task assignee's copy of an assigned task.</span></span>  <br/> |
|<span data-ttu-id="87d40-126">0 x 00000003</span><span class="sxs-lookup"><span data-stu-id="87d40-126">0x00000003</span></span>  <br/> |<span data-ttu-id="87d40-127">Die Aufgabe ist die Aufgabe delegierende Person Kopie einer zugewiesenen Aufgabe.</span><span class="sxs-lookup"><span data-stu-id="87d40-127">The task is the task assigner's copy of an assigned task.</span></span>  <br/> |
|<span data-ttu-id="87d40-128">0 x 00000004</span><span class="sxs-lookup"><span data-stu-id="87d40-128">0x00000004</span></span>  <br/> |<span data-ttu-id="87d40-129">Die Aufgabe ist die Aufgabe delegierende Person Kopie einer abgelehnten Aufgabe.</span><span class="sxs-lookup"><span data-stu-id="87d40-129">The task is the task assigner's copy of a rejected task.</span></span>  <br/> |
   
## <a name="related-resources"></a><span data-ttu-id="87d40-130">Verwandte Ressourcen</span><span class="sxs-lookup"><span data-stu-id="87d40-130">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="87d40-131">Protokollspezifikationen</span><span class="sxs-lookup"><span data-stu-id="87d40-131">Protocol specifications</span></span>

<span data-ttu-id="87d40-132">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="87d40-132">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="87d40-133">Enthält Eigenschaftendefinitionen und Verweise auf Verwandte Exchange Server-Spezifikationen.</span><span class="sxs-lookup"><span data-stu-id="87d40-133">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="87d40-134">[[MS-OXOTASK]](https://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="87d40-134">[[MS-OXOTASK]](https://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="87d40-135">Mehrere Objekte, die das elektronische Äquivalent von Aufgaben, vorgangszuordnungen und vorgangsaktualisierungen Modell definiert.</span><span class="sxs-lookup"><span data-stu-id="87d40-135">Defines several objects that model the electronic equivalent of tasks, task assignments, and task updates.</span></span>
    
<span data-ttu-id="87d40-136">[[MS-OXOSFLD]](https://msdn.microsoft.com/library/a60e9c16-2ba8-424b-b60c-385a8a2837cb%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="87d40-136">[[MS-OXOSFLD]](https://msdn.microsoft.com/library/a60e9c16-2ba8-424b-b60c-385a8a2837cb%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="87d40-137">Gibt die Eigenschaften und Operationen für das Erstellen und Ordner mit Sonderfunktion in einem Postfach suchen.</span><span class="sxs-lookup"><span data-stu-id="87d40-137">Specifies the properties and operations for creating and locating the special folders in a mailbox.</span></span>
    
<span data-ttu-id="87d40-138">[[MS-OXCICAL]](https://msdn.microsoft.com/library/a685a040-5b69-4c84-b084-795113fb4012%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="87d40-138">[[MS-OXCICAL]](https://msdn.microsoft.com/library/a685a040-5b69-4c84-b084-795113fb4012%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="87d40-139">Konvertiert zwischen IETF RFC2445, RFC2446, RFC2447, und Termine und meeting-Objekte.</span><span class="sxs-lookup"><span data-stu-id="87d40-139">Converts between IETF RFC2445, RFC2446, and RFC2447, and appointment and meeting objects.</span></span>
    
<span data-ttu-id="87d40-140">[[MS-OXCFXICS]](https://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="87d40-140">[[MS-OXCFXICS]](https://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="87d40-141">Verarbeitet die Reihenfolge und den Fluss für Datenübertragungen zwischen einem Client und Server.</span><span class="sxs-lookup"><span data-stu-id="87d40-141">Handles the order and flow for data transfers between a client and server.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="87d40-142">Header-Dateien</span><span class="sxs-lookup"><span data-stu-id="87d40-142">Header files</span></span>

<span data-ttu-id="87d40-143">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="87d40-143">Mapidefs.h</span></span>
  
> <span data-ttu-id="87d40-144">Enthält die Datentypdefinitionen.</span><span class="sxs-lookup"><span data-stu-id="87d40-144">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="87d40-145">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="87d40-145">See also</span></span>



[<span data-ttu-id="87d40-146">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="87d40-146">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="87d40-147">Kanonische MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="87d40-147">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="87d40-148">Zuordnen von kanonischen Eigenschaftennamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="87d40-148">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="87d40-149">Zuordnen von MAPI-Namen zu kanonische Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="87d40-149">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

