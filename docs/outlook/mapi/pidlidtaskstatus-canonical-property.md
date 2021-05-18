---
title: PidLidTaskStatus (kanonische Eigenschaft)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidTaskStatus
api_type:
- COM
ms.assetid: 809776b7-ff00-4a52-84b9-8b5fb5f5c3e3
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: d058b42ad7d1a1b8387aa5b9a1a65ea160d90b02
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32316667"
---
# <a name="pidlidtaskstatus-canonical-property"></a><span data-ttu-id="480d0-103">PidLidTaskStatus (kanonische Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="480d0-103">PidLidTaskStatus Canonical Property</span></span>

  
  
<span data-ttu-id="480d0-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="480d0-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="480d0-105">Gibt den Status des Fortschritts des Benutzers für den Vorgang an.</span><span class="sxs-lookup"><span data-stu-id="480d0-105">Specifies the status of the user's progress on the task.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="480d0-106">Zugeordnete Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="480d0-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="480d0-107">dispidTaskStatus</span><span class="sxs-lookup"><span data-stu-id="480d0-107">dispidTaskStatus</span></span>  <br/> |
|<span data-ttu-id="480d0-108">Eigenschaftensatz:</span><span class="sxs-lookup"><span data-stu-id="480d0-108">Property set:</span></span>  <br/> |<span data-ttu-id="480d0-109">PSETID_Task</span><span class="sxs-lookup"><span data-stu-id="480d0-109">PSETID_Task</span></span>  <br/> |
|<span data-ttu-id="480d0-110">Lange ID (LID):</span><span class="sxs-lookup"><span data-stu-id="480d0-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="480d0-111">0x00008101</span><span class="sxs-lookup"><span data-stu-id="480d0-111">0x00008101</span></span>  <br/> |
|<span data-ttu-id="480d0-112">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="480d0-112">Data type:</span></span>  <br/> |<span data-ttu-id="480d0-113">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="480d0-113">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="480d0-114">Bereich:</span><span class="sxs-lookup"><span data-stu-id="480d0-114">Area:</span></span>  <br/> |<span data-ttu-id="480d0-115">Aufgabe</span><span class="sxs-lookup"><span data-stu-id="480d0-115">Task</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="480d0-116">Hinweise</span><span class="sxs-lookup"><span data-stu-id="480d0-116">Remarks</span></span>

<span data-ttu-id="480d0-117">Der Wert dieser Eigenschaft muss auf einen der folgenden Werte festgelegt werden:</span><span class="sxs-lookup"><span data-stu-id="480d0-117">The value of this property must be set to one of the following.</span></span>
  
|<span data-ttu-id="480d0-118">**Wert**</span><span class="sxs-lookup"><span data-stu-id="480d0-118">**Value**</span></span>|<span data-ttu-id="480d0-119">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="480d0-119">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="480d0-120">0x00000000</span><span class="sxs-lookup"><span data-stu-id="480d0-120">0x00000000</span></span>  <br/> |<span data-ttu-id="480d0-121">Der Benutzer hat nicht mit der Arbeit an der Aufgabe begonnen.</span><span class="sxs-lookup"><span data-stu-id="480d0-121">The user has not started work on the task.</span></span> <span data-ttu-id="480d0-122">Wenn dieser Wert festgelegt ist, **muss dispidPercentComplete** ([PidLidPercentComplete](pidlidpercentcomplete-canonical-property.md)) 0,0 sein.</span><span class="sxs-lookup"><span data-stu-id="480d0-122">If this value is set, **dispidPercentComplete** ([PidLidPercentComplete](pidlidpercentcomplete-canonical-property.md)) must be 0.0.</span></span>  <br/> |
|<span data-ttu-id="480d0-123">0x00000001</span><span class="sxs-lookup"><span data-stu-id="480d0-123">0x00000001</span></span>  <br/> |<span data-ttu-id="480d0-124">Die Arbeit des Benutzers an dieser Aufgabe wird ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="480d0-124">The user's work on this task is in progress.</span></span> <span data-ttu-id="480d0-125">Wenn dieser Wert festgelegt ist, **muss dispidPercentComplete** größer als 0,0 und kleiner als 1,0 sein.</span><span class="sxs-lookup"><span data-stu-id="480d0-125">If this value is set, **dispidPercentComplete** must be greater than 0.0 and less than 1.0.</span></span>  <br/> |
|<span data-ttu-id="480d0-126">0x00000002</span><span class="sxs-lookup"><span data-stu-id="480d0-126">0x00000002</span></span>  <br/> |<span data-ttu-id="480d0-127">Die Arbeit des Benutzers an dieser Aufgabe ist abgeschlossen.</span><span class="sxs-lookup"><span data-stu-id="480d0-127">The user's work on this task is complete.</span></span> <span data-ttu-id="480d0-128">Wenn dieser Wert festgelegt ist, **muss dispidPercentComplete** 1,0 sein, **dispidTaskDateCompleted** ([PidLidTaskDateCompleted](pidlidtaskdatecompleted-canonical-property.md)) muss das aktuelle Datum sein, und **dispidTaskComplete** ([PidLidTaskComplete](pidlidtaskcomplete-canonical-property.md)) muss TRUE sein.</span><span class="sxs-lookup"><span data-stu-id="480d0-128">If this value is set, **dispidPercentComplete** must be 1.0, **dispidTaskDateCompleted** ([PidLidTaskDateCompleted](pidlidtaskdatecompleted-canonical-property.md)) must be the current date, and **dispidTaskComplete** ([PidLidTaskComplete](pidlidtaskcomplete-canonical-property.md)) must be TRUE.</span></span>  <br/> |
|<span data-ttu-id="480d0-129">0x00000003</span><span class="sxs-lookup"><span data-stu-id="480d0-129">0x00000003</span></span>  <br/> |<span data-ttu-id="480d0-130">Der Benutzer wartet auf einen anderen Benutzer.</span><span class="sxs-lookup"><span data-stu-id="480d0-130">The user is waiting on somebody else.</span></span>  <br/> |
|<span data-ttu-id="480d0-131">0x00000004</span><span class="sxs-lookup"><span data-stu-id="480d0-131">0x00000004</span></span>  <br/> |<span data-ttu-id="480d0-132">Der Benutzer hat die Arbeit an der Aufgabe verzögert.</span><span class="sxs-lookup"><span data-stu-id="480d0-132">The user has deferred work on the task.</span></span>  <br/> |
   
## <a name="related-resources"></a><span data-ttu-id="480d0-133">Verwandte Ressourcen</span><span class="sxs-lookup"><span data-stu-id="480d0-133">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="480d0-134">Protokollspezifikationen</span><span class="sxs-lookup"><span data-stu-id="480d0-134">Protocol specifications</span></span>

<span data-ttu-id="480d0-135">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="480d0-135">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="480d0-136">Stellt Eigenschaftensatzdefinitionen und Verweise auf verwandte Exchange Server zur Verfügung.</span><span class="sxs-lookup"><span data-stu-id="480d0-136">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="480d0-137">[[MS-OXOTASK]](https://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="480d0-137">[[MS-OXOTASK]](https://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="480d0-138">Definiert mehrere Objekte, die das elektronische Äquivalent von Vorgängen, Vorgangszuordnungen und Vorgangsaktualisierungen modellieren.</span><span class="sxs-lookup"><span data-stu-id="480d0-138">Defines several objects that model the electronic equivalent of tasks, task assignments, and task updates.</span></span>
    
<span data-ttu-id="480d0-139">[[MS-OXOFLAG]](https://msdn.microsoft.com/library/f1e50be4-ed30-4c2a-b5cb-8ff3aaaf9b91%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="480d0-139">[[MS-OXOFLAG]](https://msdn.microsoft.com/library/f1e50be4-ed30-4c2a-b5cb-8ff3aaaf9b91%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="480d0-140">Gibt die Eigenschaften und Vorgänge im Zusammenhang mit der Kennzeichnung an.</span><span class="sxs-lookup"><span data-stu-id="480d0-140">Specifies the properties and operations related to flagging.</span></span>
    
<span data-ttu-id="480d0-141">[[MS-OXOSFLD]](https://msdn.microsoft.com/library/a60e9c16-2ba8-424b-b60c-385a8a2837cb%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="480d0-141">[[MS-OXOSFLD]](https://msdn.microsoft.com/library/a60e9c16-2ba8-424b-b60c-385a8a2837cb%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="480d0-142">Gibt die Eigenschaften und Vorgänge zum Erstellen und Suchen der speziellen Ordner in einem Postfach an.</span><span class="sxs-lookup"><span data-stu-id="480d0-142">Specifies the properties and operations for creating and locating the special folders in a mailbox.</span></span>
    
<span data-ttu-id="480d0-143">[[MS-OXCMAIL]](https://msdn.microsoft.com/library/b60d48db-183f-4bf5-a908-f584e62cb2d4%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="480d0-143">[[MS-OXCMAIL]](https://msdn.microsoft.com/library/b60d48db-183f-4bf5-a908-f584e62cb2d4%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="480d0-144">Konvertiert von Internetstandard-E-Mail-Konventionen in Nachrichtenobjekte.</span><span class="sxs-lookup"><span data-stu-id="480d0-144">Converts from Internet standard email conventions to message objects.</span></span>
    
<span data-ttu-id="480d0-145">[[MS-OXCICAL]](https://msdn.microsoft.com/library/a685a040-5b69-4c84-b084-795113fb4012%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="480d0-145">[[MS-OXCICAL]](https://msdn.microsoft.com/library/a685a040-5b69-4c84-b084-795113fb4012%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="480d0-146">Konvertiert zwischen IETF RFC2445, RFC2446 und RFC2447 sowie Termin- und Besprechungsobjekten.</span><span class="sxs-lookup"><span data-stu-id="480d0-146">Converts between IETF RFC2445, RFC2446, and RFC2447, and appointment and meeting objects.</span></span>
    
<span data-ttu-id="480d0-147">[[MS-OXCFXICS]](https://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="480d0-147">[[MS-OXCFXICS]](https://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="480d0-148">Verarbeitet die Reihenfolge und den Fluss für Datenübertragungen zwischen einem Client und einem Server.</span><span class="sxs-lookup"><span data-stu-id="480d0-148">Handles the order and flow for data transfers between a client and server.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="480d0-149">Headerdateien</span><span class="sxs-lookup"><span data-stu-id="480d0-149">Header files</span></span>

<span data-ttu-id="480d0-150">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="480d0-150">Mapidefs.h</span></span>
  
> <span data-ttu-id="480d0-151">Bietet Datentypdefinitionen.</span><span class="sxs-lookup"><span data-stu-id="480d0-151">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="480d0-152">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="480d0-152">See also</span></span>



[<span data-ttu-id="480d0-153">PidLidPercentComplete (kanonische Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="480d0-153">PidLidPercentComplete Canonical Property</span></span>](pidlidpercentcomplete-canonical-property.md)
  
[<span data-ttu-id="480d0-154">PidLidTaskDateCompleted (kanonische Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="480d0-154">PidLidTaskDateCompleted Canonical Property</span></span>](pidlidtaskdatecompleted-canonical-property.md)
  
[<span data-ttu-id="480d0-155">PidLidTaskComplete (kanonische Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="480d0-155">PidLidTaskComplete Canonical Property</span></span>](pidlidtaskcomplete-canonical-property.md)


[<span data-ttu-id="480d0-156">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="480d0-156">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="480d0-157">KANONISCHE EIGENSCHAFTEN VON MAPI</span><span class="sxs-lookup"><span data-stu-id="480d0-157">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="480d0-158">Zuordnen kanonischer Eigenschaftsnamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="480d0-158">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="480d0-159">Zuordnen von MAPI-Namen zu kanonischen Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="480d0-159">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

