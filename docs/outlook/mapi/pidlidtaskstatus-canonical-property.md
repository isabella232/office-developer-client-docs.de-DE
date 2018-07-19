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
ms.openlocfilehash: e8ca8d7a82360c1f96448b08c9eda18be502b9f7
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19793881"
---
# <a name="pidlidtaskstatus-canonical-property"></a><span data-ttu-id="332ce-103">PidLidTaskStatus (kanonische Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="332ce-103">PidLidTaskStatus Canonical Property</span></span>

  
  
<span data-ttu-id="332ce-104">**Betrifft**: Outlook</span><span class="sxs-lookup"><span data-stu-id="332ce-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="332ce-105">Gibt den Status des Benutzers Fortschritt für den Vorgang.</span><span class="sxs-lookup"><span data-stu-id="332ce-105">Specifies the status of the user's progress on the task.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="332ce-106">Zugeordneten Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="332ce-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="332ce-107">dispidTaskStatus</span><span class="sxs-lookup"><span data-stu-id="332ce-107">dispidTaskStatus</span></span>  <br/> |
|<span data-ttu-id="332ce-108">-Eigenschaft festgelegt:</span><span class="sxs-lookup"><span data-stu-id="332ce-108">Property set:</span></span>  <br/> |<span data-ttu-id="332ce-109">PSETID_Task</span><span class="sxs-lookup"><span data-stu-id="332ce-109">PSETID_Task</span></span>  <br/> |
|<span data-ttu-id="332ce-110">Long-ID (Abdeckung):</span><span class="sxs-lookup"><span data-stu-id="332ce-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="332ce-111">0x00008101</span><span class="sxs-lookup"><span data-stu-id="332ce-111">0x00008101</span></span>  <br/> |
|<span data-ttu-id="332ce-112">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="332ce-112">Data type:</span></span>  <br/> |<span data-ttu-id="332ce-113">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="332ce-113">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="332ce-114">Bereich:</span><span class="sxs-lookup"><span data-stu-id="332ce-114">Area:</span></span>  <br/> |<span data-ttu-id="332ce-115">Aufgabe</span><span class="sxs-lookup"><span data-stu-id="332ce-115">Task</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="332ce-116">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="332ce-116">Remarks</span></span>

<span data-ttu-id="332ce-117">Der Wert dieser Eigenschaft muss auf einen der folgenden festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="332ce-117">The value of this property must be set to one of the following.</span></span>
  
|<span data-ttu-id="332ce-118">**Wert**</span><span class="sxs-lookup"><span data-stu-id="332ce-118">**Value**</span></span>|<span data-ttu-id="332ce-119">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="332ce-119">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="332ce-120">0x00000000</span><span class="sxs-lookup"><span data-stu-id="332ce-120">0x00000000</span></span>  <br/> |<span data-ttu-id="332ce-121">Der Benutzer wurde Arbeit für die Aufgabe nicht gestartet werden.</span><span class="sxs-lookup"><span data-stu-id="332ce-121">The user has not started work on the task.</span></span> <span data-ttu-id="332ce-122">Wenn dieser Wert festgelegt ist, muss **DispidPercentComplete** ([PidLidPercentComplete](pidlidpercentcomplete-canonical-property.md)) 0,0 sein.</span><span class="sxs-lookup"><span data-stu-id="332ce-122">If this value is set, **dispidPercentComplete** ([PidLidPercentComplete](pidlidpercentcomplete-canonical-property.md)) must be 0.0.</span></span>  <br/> |
|<span data-ttu-id="332ce-123">0x00000001</span><span class="sxs-lookup"><span data-stu-id="332ce-123">0x00000001</span></span>  <br/> |<span data-ttu-id="332ce-124">Der Benutzer Arbeit für diesen Vorgang wird gerade durchgeführt.</span><span class="sxs-lookup"><span data-stu-id="332ce-124">The user's work on this task is in progress.</span></span> <span data-ttu-id="332ce-125">Wenn dieser Wert festgelegt ist, muss **DispidPercentComplete** größer als 0,0 und kleiner als 1,0 sein.</span><span class="sxs-lookup"><span data-stu-id="332ce-125">If this value is set, **dispidPercentComplete** must be greater than 0.0 and less than 1.0.</span></span>  <br/> |
|<span data-ttu-id="332ce-126">0x00000002</span><span class="sxs-lookup"><span data-stu-id="332ce-126">0x00000002</span></span>  <br/> |<span data-ttu-id="332ce-127">Der Benutzer Arbeit für diesen Vorgang ist abgeschlossen.</span><span class="sxs-lookup"><span data-stu-id="332ce-127">The user's work on this task is complete.</span></span> <span data-ttu-id="332ce-128">Wenn dieser Wert festgelegt ist, **DispidPercentComplete** muss 1.0, **DispidTaskDateCompleted** ([PidLidTaskDateCompleted](pidlidtaskdatecompleted-canonical-property.md)) muss das aktuelle Datum und **DispidTaskComplete** ([PidLidTaskComplete](pidlidtaskcomplete-canonical-property.md)) muss auf TRUE festgelegt sein.</span><span class="sxs-lookup"><span data-stu-id="332ce-128">If this value is set, **dispidPercentComplete** must be 1.0, **dispidTaskDateCompleted** ([PidLidTaskDateCompleted](pidlidtaskdatecompleted-canonical-property.md)) must be the current date, and **dispidTaskComplete** ([PidLidTaskComplete](pidlidtaskcomplete-canonical-property.md)) must be TRUE.</span></span>  <br/> |
|<span data-ttu-id="332ce-129">0 x 00000003</span><span class="sxs-lookup"><span data-stu-id="332ce-129">0x00000003</span></span>  <br/> |<span data-ttu-id="332ce-130">Der Benutzer wartet auf jemand.</span><span class="sxs-lookup"><span data-stu-id="332ce-130">The user is waiting on somebody else.</span></span>  <br/> |
|<span data-ttu-id="332ce-131">0 x 00000004</span><span class="sxs-lookup"><span data-stu-id="332ce-131">0x00000004</span></span>  <br/> |<span data-ttu-id="332ce-132">Der Benutzer hat die Arbeit für den Vorgang zurückgestellt.</span><span class="sxs-lookup"><span data-stu-id="332ce-132">The user has deferred work on the task.</span></span>  <br/> |
   
## <a name="related-resources"></a><span data-ttu-id="332ce-133">Verwandte Ressourcen</span><span class="sxs-lookup"><span data-stu-id="332ce-133">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="332ce-134">Protokollspezifikationen</span><span class="sxs-lookup"><span data-stu-id="332ce-134">Protocol specifications</span></span>

<span data-ttu-id="332ce-135">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="332ce-135">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="332ce-136">Enthält Eigenschaftendefinitionen und Verweise auf Verwandte Exchange Server-Spezifikationen.</span><span class="sxs-lookup"><span data-stu-id="332ce-136">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="332ce-137">[[MS-OXOTASK]](http://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="332ce-137">[[MS-OXOTASK]](http://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="332ce-138">Mehrere Objekte, die das elektronische Äquivalent von Aufgaben, vorgangszuordnungen und vorgangsaktualisierungen Modell definiert.</span><span class="sxs-lookup"><span data-stu-id="332ce-138">Defines several objects that model the electronic equivalent of tasks, task assignments, and task updates.</span></span>
    
<span data-ttu-id="332ce-139">[[MS-OXOFLAG]](http://msdn.microsoft.com/library/f1e50be4-ed30-4c2a-b5cb-8ff3aaaf9b91%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="332ce-139">[[MS-OXOFLAG]](http://msdn.microsoft.com/library/f1e50be4-ed30-4c2a-b5cb-8ff3aaaf9b91%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="332ce-140">Gibt die Eigenschaften und Vorgänge im Zusammenhang mit kennzeichnen.</span><span class="sxs-lookup"><span data-stu-id="332ce-140">Specifies the properties and operations related to flagging.</span></span>
    
<span data-ttu-id="332ce-141">[[MS-OXOSFLD]](http://msdn.microsoft.com/library/a60e9c16-2ba8-424b-b60c-385a8a2837cb%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="332ce-141">[[MS-OXOSFLD]](http://msdn.microsoft.com/library/a60e9c16-2ba8-424b-b60c-385a8a2837cb%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="332ce-142">Gibt die Eigenschaften und Operationen für das Erstellen und Ordner mit Sonderfunktion in einem Postfach suchen.</span><span class="sxs-lookup"><span data-stu-id="332ce-142">Specifies the properties and operations for creating and locating the special folders in a mailbox.</span></span>
    
<span data-ttu-id="332ce-143">[[MS-OXCMAIL]](http://msdn.microsoft.com/library/b60d48db-183f-4bf5-a908-f584e62cb2d4%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="332ce-143">[[MS-OXCMAIL]](http://msdn.microsoft.com/library/b60d48db-183f-4bf5-a908-f584e62cb2d4%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="332ce-144">Konvertiert von Internet-standard-e-Mail-Konventionen in Message-Objekten.</span><span class="sxs-lookup"><span data-stu-id="332ce-144">Converts from Internet standard email conventions to message objects.</span></span>
    
<span data-ttu-id="332ce-145">[[MS-OXCICAL]](http://msdn.microsoft.com/library/a685a040-5b69-4c84-b084-795113fb4012%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="332ce-145">[[MS-OXCICAL]](http://msdn.microsoft.com/library/a685a040-5b69-4c84-b084-795113fb4012%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="332ce-146">Konvertiert zwischen IETF RFC2445, RFC2446, RFC2447, und Termine und meeting-Objekte.</span><span class="sxs-lookup"><span data-stu-id="332ce-146">Converts between IETF RFC2445, RFC2446, and RFC2447, and appointment and meeting objects.</span></span>
    
<span data-ttu-id="332ce-147">[[MS-OXCFXICS]](http://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="332ce-147">[[MS-OXCFXICS]](http://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="332ce-148">Verarbeitet die Reihenfolge und den Fluss für Datenübertragungen zwischen einem Client und Server.</span><span class="sxs-lookup"><span data-stu-id="332ce-148">Handles the order and flow for data transfers between a client and server.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="332ce-149">Header-Dateien</span><span class="sxs-lookup"><span data-stu-id="332ce-149">Header files</span></span>

<span data-ttu-id="332ce-150">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="332ce-150">Mapidefs.h</span></span>
  
> <span data-ttu-id="332ce-151">Enthält die Datentypdefinitionen.</span><span class="sxs-lookup"><span data-stu-id="332ce-151">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="332ce-152">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="332ce-152">See also</span></span>



[<span data-ttu-id="332ce-153">PidLidPercentComplete (kanonische Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="332ce-153">PidLidPercentComplete Canonical Property</span></span>](pidlidpercentcomplete-canonical-property.md)
  
[<span data-ttu-id="332ce-154">PidLidTaskDateCompleted (kanonische Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="332ce-154">PidLidTaskDateCompleted Canonical Property</span></span>](pidlidtaskdatecompleted-canonical-property.md)
  
[<span data-ttu-id="332ce-155">PidLidTaskComplete (kanonische Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="332ce-155">PidLidTaskComplete Canonical Property</span></span>](pidlidtaskcomplete-canonical-property.md)


[<span data-ttu-id="332ce-156">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="332ce-156">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="332ce-157">Kanonische MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="332ce-157">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="332ce-158">Zuordnen von kanonischen Eigenschaftennamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="332ce-158">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="332ce-159">Zuordnen von MAPI-Namen zu kanonische Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="332ce-159">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

