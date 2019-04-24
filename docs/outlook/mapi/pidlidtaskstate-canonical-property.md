---
title: Kanonische Pidlidtaskstate (-Eigenschaft
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
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: 149f238ea53e0669f4d95c8e6c2b17a2b5a1c209
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32316534"
---
# <a name="pidlidtaskstate-canonical-property"></a><span data-ttu-id="1234f-103">Kanonische Pidlidtaskstate (-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="1234f-103">PidLidTaskState Canonical Property</span></span>

  
  
<span data-ttu-id="1234f-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="1234f-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="1234f-105">Gibt den aktuellen Zuordnungsstatus der Aufgabe an.</span><span class="sxs-lookup"><span data-stu-id="1234f-105">Indicates the current assignment state of the task.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="1234f-106">Zugeordnete Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="1234f-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="1234f-107">dispidTaskState</span><span class="sxs-lookup"><span data-stu-id="1234f-107">dispidTaskState</span></span>  <br/> |
|<span data-ttu-id="1234f-108">Eigenschaftensatz:</span><span class="sxs-lookup"><span data-stu-id="1234f-108">Property set:</span></span>  <br/> |<span data-ttu-id="1234f-109">PSETID_Task</span><span class="sxs-lookup"><span data-stu-id="1234f-109">PSETID_Task</span></span>  <br/> |
|<span data-ttu-id="1234f-110">Long-ID (Deckel):</span><span class="sxs-lookup"><span data-stu-id="1234f-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="1234f-111">0x00008113</span><span class="sxs-lookup"><span data-stu-id="1234f-111">0x00008113</span></span>  <br/> |
|<span data-ttu-id="1234f-112">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="1234f-112">Data type:</span></span>  <br/> |<span data-ttu-id="1234f-113">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="1234f-113">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="1234f-114">Bereich:</span><span class="sxs-lookup"><span data-stu-id="1234f-114">Area:</span></span>  <br/> |<span data-ttu-id="1234f-115">Aufgabe</span><span class="sxs-lookup"><span data-stu-id="1234f-115">Task</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="1234f-116">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="1234f-116">Remarks</span></span>

<span data-ttu-id="1234f-117">Der Wert dieser Eigenschaft muss einer der folgenden Werte sein:</span><span class="sxs-lookup"><span data-stu-id="1234f-117">The value of this property must be one of the following.</span></span>
  
|<span data-ttu-id="1234f-118">**Wert**</span><span class="sxs-lookup"><span data-stu-id="1234f-118">**Value**</span></span>|<span data-ttu-id="1234f-119">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="1234f-119">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="1234f-120">0x00000000</span><span class="sxs-lookup"><span data-stu-id="1234f-120">0x00000000</span></span>  <br/> |<span data-ttu-id="1234f-121">Diese Aufgabe wurde erstellt, um einer Aufgabe zu entsprechen, die in eine Aufgaben Ablehnung eingebettet wurde, aber nicht lokal gefunden werden konnte.</span><span class="sxs-lookup"><span data-stu-id="1234f-121">This task was created to correspond to a task that was embedded in a task rejection but could not be found locally.</span></span>  <br/> |
|<span data-ttu-id="1234f-122">0x00000001</span><span class="sxs-lookup"><span data-stu-id="1234f-122">0x00000001</span></span>  <br/> |<span data-ttu-id="1234f-123">Die Aufgabe wird nicht zugewiesen.</span><span class="sxs-lookup"><span data-stu-id="1234f-123">The task is not assigned.</span></span>  <br/> |
|<span data-ttu-id="1234f-124">0x00000002</span><span class="sxs-lookup"><span data-stu-id="1234f-124">0x00000002</span></span>  <br/> |<span data-ttu-id="1234f-125">Bei der Aufgabe handelt es sich um die Kopie des Aufgabenempfängers einer zugeordneten Aufgabe.</span><span class="sxs-lookup"><span data-stu-id="1234f-125">The task is the task assignee's copy of an assigned task.</span></span>  <br/> |
|<span data-ttu-id="1234f-126">0x00000003</span><span class="sxs-lookup"><span data-stu-id="1234f-126">0x00000003</span></span>  <br/> |<span data-ttu-id="1234f-127">Die Aufgabe ist die Kopie des Aufgaben beauftragten einer zugewiesenen Aufgabe.</span><span class="sxs-lookup"><span data-stu-id="1234f-127">The task is the task assigner's copy of an assigned task.</span></span>  <br/> |
|<span data-ttu-id="1234f-128">0x00000004</span><span class="sxs-lookup"><span data-stu-id="1234f-128">0x00000004</span></span>  <br/> |<span data-ttu-id="1234f-129">Die Aufgabe ist die Kopie des Aufgaben beauftragten einer abgelehnten Aufgabe.</span><span class="sxs-lookup"><span data-stu-id="1234f-129">The task is the task assigner's copy of a rejected task.</span></span>  <br/> |
   
## <a name="related-resources"></a><span data-ttu-id="1234f-130">Zugehörige Ressourcen</span><span class="sxs-lookup"><span data-stu-id="1234f-130">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="1234f-131">Protokollspezifikationen</span><span class="sxs-lookup"><span data-stu-id="1234f-131">Protocol specifications</span></span>

<span data-ttu-id="1234f-132">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="1234f-132">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="1234f-133">Stellt Eigenschaftensatz Definitionen und Verweise auf zugehörige Exchange Server-Protokollspezifikationen bereit.</span><span class="sxs-lookup"><span data-stu-id="1234f-133">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="1234f-134">[[MS-OXOTASK]](https://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="1234f-134">[[MS-OXOTASK]](https://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="1234f-135">Definiert mehrere Objekte, die das elektronische Äquivalent von Aufgaben, Vorgangszuordnungen und Vorgangsaktualisierungen modellieren.</span><span class="sxs-lookup"><span data-stu-id="1234f-135">Defines several objects that model the electronic equivalent of tasks, task assignments, and task updates.</span></span>
    
<span data-ttu-id="1234f-136">[[MS-OXOSFLD]](https://msdn.microsoft.com/library/a60e9c16-2ba8-424b-b60c-385a8a2837cb%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="1234f-136">[[MS-OXOSFLD]](https://msdn.microsoft.com/library/a60e9c16-2ba8-424b-b60c-385a8a2837cb%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="1234f-137">Gibt die Eigenschaften und Vorgänge zum Erstellen und suchen der speziellen Ordner in einem Postfach an.</span><span class="sxs-lookup"><span data-stu-id="1234f-137">Specifies the properties and operations for creating and locating the special folders in a mailbox.</span></span>
    
<span data-ttu-id="1234f-138">[[MS-OXCICAL]](https://msdn.microsoft.com/library/a685a040-5b69-4c84-b084-795113fb4012%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="1234f-138">[[MS-OXCICAL]](https://msdn.microsoft.com/library/a685a040-5b69-4c84-b084-795113fb4012%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="1234f-139">Konvertiert zwischen IETF-RFC2445, RFC2446 und RFC2447 sowie Termin-und Besprechungs Objekten.</span><span class="sxs-lookup"><span data-stu-id="1234f-139">Converts between IETF RFC2445, RFC2446, and RFC2447, and appointment and meeting objects.</span></span>
    
<span data-ttu-id="1234f-140">[[MS-OXCFXICS]](https://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="1234f-140">[[MS-OXCFXICS]](https://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="1234f-141">Verarbeitet die Reihenfolge und den Ablauf für die Datenübertragung zwischen einem Client und einem Server.</span><span class="sxs-lookup"><span data-stu-id="1234f-141">Handles the order and flow for data transfers between a client and server.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="1234f-142">Header Dateien</span><span class="sxs-lookup"><span data-stu-id="1234f-142">Header files</span></span>

<span data-ttu-id="1234f-143">Mapidefs. h</span><span class="sxs-lookup"><span data-stu-id="1234f-143">Mapidefs.h</span></span>
  
> <span data-ttu-id="1234f-144">Stellt Datentypdefinitionen bereit.</span><span class="sxs-lookup"><span data-stu-id="1234f-144">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="1234f-145">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="1234f-145">See also</span></span>



[<span data-ttu-id="1234f-146">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="1234f-146">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="1234f-147">Kanonische MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="1234f-147">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="1234f-148">Zuordnen von kanonischen Eigenschaftennamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="1234f-148">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="1234f-149">Zuordnen von MAPI-Namen zu kanonischen Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="1234f-149">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

