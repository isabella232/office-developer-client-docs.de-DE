---
title: Kanonische PidLidPercentComplete-Eigenschaft
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidLidPercentComplete
api_type:
- COM
ms.assetid: e63792b1-9580-4702-a6d7-dd3ae5007a4a
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: f4675362de1e9efe4ef16285723cddeface9c403
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19793714"
---
# <a name="pidlidpercentcomplete-canonical-property"></a><span data-ttu-id="fd86a-103">Kanonische PidLidPercentComplete-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="fd86a-103">PidLidPercentComplete Canonical Property</span></span>

  
  
<span data-ttu-id="fd86a-104">**Betrifft**: Outlook</span><span class="sxs-lookup"><span data-stu-id="fd86a-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="fd86a-105">Gibt an, dass der Fortschritt der Benutzer für einen Vorgang vorgenommen hat.</span><span class="sxs-lookup"><span data-stu-id="fd86a-105">Indicates the progress the user has made on a task.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="fd86a-106">Zugeordneten Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="fd86a-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="fd86a-107">dispidPercentComplete</span><span class="sxs-lookup"><span data-stu-id="fd86a-107">dispidPercentComplete</span></span>  <br/> |
|<span data-ttu-id="fd86a-108">-Eigenschaft festgelegt:</span><span class="sxs-lookup"><span data-stu-id="fd86a-108">Property set:</span></span>  <br/> |<span data-ttu-id="fd86a-109">PSETID_Task</span><span class="sxs-lookup"><span data-stu-id="fd86a-109">PSETID_Task</span></span>  <br/> |
|<span data-ttu-id="fd86a-110">Long-ID (Abdeckung):</span><span class="sxs-lookup"><span data-stu-id="fd86a-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="fd86a-111">0x00008102</span><span class="sxs-lookup"><span data-stu-id="fd86a-111">0x00008102</span></span>  <br/> |
|<span data-ttu-id="fd86a-112">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="fd86a-112">Data type:</span></span>  <br/> |<span data-ttu-id="fd86a-113">PT_R8</span><span class="sxs-lookup"><span data-stu-id="fd86a-113">PT_R8</span></span>  <br/> |
|<span data-ttu-id="fd86a-114">Bereich:</span><span class="sxs-lookup"><span data-stu-id="fd86a-114">Area:</span></span>  <br/> |<span data-ttu-id="fd86a-115">Aufgabe</span><span class="sxs-lookup"><span data-stu-id="fd86a-115">Task</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="fd86a-116">Hinweise</span><span class="sxs-lookup"><span data-stu-id="fd86a-116">Remarks</span></span>

<span data-ttu-id="fd86a-117">Der Wert dieser Eigenschaft muss eine Zahl größer oder gleich 0,0 und kleiner als oder gleich 1,0, in dem 1.0 gibt an, dass Arbeit abgeschlossen ist und 0,0 gibt an, dass Arbeit nicht begonnen hat.</span><span class="sxs-lookup"><span data-stu-id="fd86a-117">The value of this property must be a number greater than or equal to 0.0 and less than or equal to 1.0, where 1.0 indicates that work is completed and 0.0 indicates that work has not begun.</span></span>
  
<span data-ttu-id="fd86a-118">Für ein Objekt Zeit gekennzeichnete Nachricht der Wert dieser Eigenschaft muss festgelegt werden auf 1.0, wenn das Objekt gekennzeichnet ist abgeschlossen, und andernfalls auf 0,0 festgelegt werden sollte.</span><span class="sxs-lookup"><span data-stu-id="fd86a-118">For a time-flagged message object, the value of this property must be set to 1.0 if the object is flagged completed, and should be set to 0.0 otherwise.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="fd86a-119">Verwandte Ressourcen</span><span class="sxs-lookup"><span data-stu-id="fd86a-119">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="fd86a-120">Protokollspezifikationen</span><span class="sxs-lookup"><span data-stu-id="fd86a-120">Protocol specifications</span></span>

<span data-ttu-id="fd86a-121">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="fd86a-121">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="fd86a-122">Enthält Eigenschaftendefinitionen und Verweise auf Verwandte Exchange Server-Spezifikationen.</span><span class="sxs-lookup"><span data-stu-id="fd86a-122">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="fd86a-123">[[MS-OXOTASK]](http://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="fd86a-123">[[MS-OXOTASK]](http://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="fd86a-124">Mehrere Objekte, die das elektronische Äquivalent von Aufgaben, vorgangszuordnungen und vorgangsaktualisierungen Modell definiert.</span><span class="sxs-lookup"><span data-stu-id="fd86a-124">Defines several objects that model the electronic equivalent of tasks, task assignments, and task updates.</span></span>
    
<span data-ttu-id="fd86a-125">[[MS-OXOFLAG]](http://msdn.microsoft.com/library/f1e50be4-ed30-4c2a-b5cb-8ff3aaaf9b91%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="fd86a-125">[[MS-OXOFLAG]](http://msdn.microsoft.com/library/f1e50be4-ed30-4c2a-b5cb-8ff3aaaf9b91%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="fd86a-126">Gibt die Eigenschaften und Vorgänge im Zusammenhang mit kennzeichnen.</span><span class="sxs-lookup"><span data-stu-id="fd86a-126">Specifies the properties and operations related to flagging.</span></span>
    
<span data-ttu-id="fd86a-127">[[MS-OXCMAIL]](http://msdn.microsoft.com/library/b60d48db-183f-4bf5-a908-f584e62cb2d4%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="fd86a-127">[[MS-OXCMAIL]](http://msdn.microsoft.com/library/b60d48db-183f-4bf5-a908-f584e62cb2d4%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="fd86a-128">Konvertiert von Internet-standard-e-Mail-Konventionen in Message-Objekten.</span><span class="sxs-lookup"><span data-stu-id="fd86a-128">Converts from Internet standard email conventions to message objects.</span></span>
    
<span data-ttu-id="fd86a-129">[[MS-OXCICAL]](http://msdn.microsoft.com/library/a685a040-5b69-4c84-b084-795113fb4012%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="fd86a-129">[[MS-OXCICAL]](http://msdn.microsoft.com/library/a685a040-5b69-4c84-b084-795113fb4012%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="fd86a-130">Konvertiert zwischen IETF RFC2445, RFC2446, RFC2447, und Termine und meeting-Objekte.</span><span class="sxs-lookup"><span data-stu-id="fd86a-130">Converts between IETF RFC2445, RFC2446, and RFC2447, and appointment and meeting objects.</span></span>
    
<span data-ttu-id="fd86a-131">[[MS-OXCFXICS]](http://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="fd86a-131">[[MS-OXCFXICS]](http://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="fd86a-132">Verarbeitet die Reihenfolge und den Fluss für Datenübertragungen zwischen einem Client und Server.</span><span class="sxs-lookup"><span data-stu-id="fd86a-132">Handles the order and flow for data transfers between a client and server.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="fd86a-133">Header-Dateien</span><span class="sxs-lookup"><span data-stu-id="fd86a-133">Header files</span></span>

<span data-ttu-id="fd86a-134">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="fd86a-134">Mapidefs.h</span></span>
  
> <span data-ttu-id="fd86a-135">Enthält die Datentypdefinitionen.</span><span class="sxs-lookup"><span data-stu-id="fd86a-135">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="fd86a-136">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="fd86a-136">See also</span></span>



[<span data-ttu-id="fd86a-137">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="fd86a-137">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="fd86a-138">Kanonische MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="fd86a-138">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="fd86a-139">Zuordnen von kanonischen Eigenschaftennamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="fd86a-139">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="fd86a-140">Zuordnen von MAPI-Namen zu kanonische Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="fd86a-140">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

