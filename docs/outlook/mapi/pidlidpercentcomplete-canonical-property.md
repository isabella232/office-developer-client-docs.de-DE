---
title: PidLidPercentComplete (kanonische Eigenschaft)
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
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 870b4e0edb360ac36525f94b0605af930eee8fa3
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32357974"
---
# <a name="pidlidpercentcomplete-canonical-property"></a><span data-ttu-id="665e7-103">PidLidPercentComplete (kanonische Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="665e7-103">PidLidPercentComplete Canonical Property</span></span>

  
  
<span data-ttu-id="665e7-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="665e7-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="665e7-105">Gibt den Fortschritt an, den der Benutzer für eine Aufgabe erzielt hat.</span><span class="sxs-lookup"><span data-stu-id="665e7-105">Indicates the progress the user has made on a task.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="665e7-106">Zugeordnete Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="665e7-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="665e7-107">dispidPercentComplete</span><span class="sxs-lookup"><span data-stu-id="665e7-107">dispidPercentComplete</span></span>  <br/> |
|<span data-ttu-id="665e7-108">Eigenschaftensatz:</span><span class="sxs-lookup"><span data-stu-id="665e7-108">Property set:</span></span>  <br/> |<span data-ttu-id="665e7-109">PSETID_Task</span><span class="sxs-lookup"><span data-stu-id="665e7-109">PSETID_Task</span></span>  <br/> |
|<span data-ttu-id="665e7-110">Lange ID (LID):</span><span class="sxs-lookup"><span data-stu-id="665e7-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="665e7-111">0x00008102</span><span class="sxs-lookup"><span data-stu-id="665e7-111">0x00008102</span></span>  <br/> |
|<span data-ttu-id="665e7-112">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="665e7-112">Data type:</span></span>  <br/> |<span data-ttu-id="665e7-113">PT_R8</span><span class="sxs-lookup"><span data-stu-id="665e7-113">PT_R8</span></span>  <br/> |
|<span data-ttu-id="665e7-114">Bereich:</span><span class="sxs-lookup"><span data-stu-id="665e7-114">Area:</span></span>  <br/> |<span data-ttu-id="665e7-115">Aufgabe</span><span class="sxs-lookup"><span data-stu-id="665e7-115">Task</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="665e7-116">Hinweise</span><span class="sxs-lookup"><span data-stu-id="665e7-116">Remarks</span></span>

<span data-ttu-id="665e7-117">Der Wert dieser Eigenschaft muss eine Zahl größer oder gleich 0,0 und kleiner als oder gleich 1,0 sein, wobei 1,0 angibt, dass die Arbeit abgeschlossen ist und 0,0 angibt, dass die Arbeit noch nicht begonnen hat.</span><span class="sxs-lookup"><span data-stu-id="665e7-117">The value of this property must be a number greater than or equal to 0.0 and less than or equal to 1.0, where 1.0 indicates that work is completed and 0.0 indicates that work has not begun.</span></span>
  
<span data-ttu-id="665e7-118">Für ein Nachrichtenobjekt mit Zeitflaging muss der Wert dieser Eigenschaft auf 1,0 festgelegt werden, wenn das Objekt als abgeschlossen gekennzeichnet ist, und andernfalls auf 0,0 festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="665e7-118">For a time-flagged message object, the value of this property must be set to 1.0 if the object is flagged completed, and should be set to 0.0 otherwise.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="665e7-119">Verwandte Ressourcen</span><span class="sxs-lookup"><span data-stu-id="665e7-119">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="665e7-120">Protokollspezifikationen</span><span class="sxs-lookup"><span data-stu-id="665e7-120">Protocol specifications</span></span>

<span data-ttu-id="665e7-121">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="665e7-121">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="665e7-122">Stellt Eigenschaftensatzdefinitionen und Verweise auf verwandte Exchange Server zur Verfügung.</span><span class="sxs-lookup"><span data-stu-id="665e7-122">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="665e7-123">[[MS-OXOTASK]](https://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="665e7-123">[[MS-OXOTASK]](https://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="665e7-124">Definiert mehrere Objekte, die das elektronische Äquivalent von Vorgängen, Vorgangszuordnungen und Vorgangsaktualisierungen modellieren.</span><span class="sxs-lookup"><span data-stu-id="665e7-124">Defines several objects that model the electronic equivalent of tasks, task assignments, and task updates.</span></span>
    
<span data-ttu-id="665e7-125">[[MS-OXOFLAG]](https://msdn.microsoft.com/library/f1e50be4-ed30-4c2a-b5cb-8ff3aaaf9b91%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="665e7-125">[[MS-OXOFLAG]](https://msdn.microsoft.com/library/f1e50be4-ed30-4c2a-b5cb-8ff3aaaf9b91%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="665e7-126">Gibt die Eigenschaften und Vorgänge im Zusammenhang mit der Kennzeichnung an.</span><span class="sxs-lookup"><span data-stu-id="665e7-126">Specifies the properties and operations related to flagging.</span></span>
    
<span data-ttu-id="665e7-127">[[MS-OXCMAIL]](https://msdn.microsoft.com/library/b60d48db-183f-4bf5-a908-f584e62cb2d4%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="665e7-127">[[MS-OXCMAIL]](https://msdn.microsoft.com/library/b60d48db-183f-4bf5-a908-f584e62cb2d4%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="665e7-128">Konvertiert von Internetstandard-E-Mail-Konventionen in Nachrichtenobjekte.</span><span class="sxs-lookup"><span data-stu-id="665e7-128">Converts from Internet standard email conventions to message objects.</span></span>
    
<span data-ttu-id="665e7-129">[[MS-OXCICAL]](https://msdn.microsoft.com/library/a685a040-5b69-4c84-b084-795113fb4012%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="665e7-129">[[MS-OXCICAL]](https://msdn.microsoft.com/library/a685a040-5b69-4c84-b084-795113fb4012%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="665e7-130">Konvertiert zwischen IETF RFC2445, RFC2446 und RFC2447 sowie Termin- und Besprechungsobjekten.</span><span class="sxs-lookup"><span data-stu-id="665e7-130">Converts between IETF RFC2445, RFC2446, and RFC2447, and appointment and meeting objects.</span></span>
    
<span data-ttu-id="665e7-131">[[MS-OXCFXICS]](https://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="665e7-131">[[MS-OXCFXICS]](https://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="665e7-132">Verarbeitet die Reihenfolge und den Fluss für Datenübertragungen zwischen einem Client und einem Server.</span><span class="sxs-lookup"><span data-stu-id="665e7-132">Handles the order and flow for data transfers between a client and server.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="665e7-133">Headerdateien</span><span class="sxs-lookup"><span data-stu-id="665e7-133">Header files</span></span>

<span data-ttu-id="665e7-134">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="665e7-134">Mapidefs.h</span></span>
  
> <span data-ttu-id="665e7-135">Bietet Datentypdefinitionen.</span><span class="sxs-lookup"><span data-stu-id="665e7-135">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="665e7-136">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="665e7-136">See also</span></span>



[<span data-ttu-id="665e7-137">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="665e7-137">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="665e7-138">KANONISCHE EIGENSCHAFTEN VON MAPI</span><span class="sxs-lookup"><span data-stu-id="665e7-138">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="665e7-139">Zuordnen kanonischer Eigenschaftsnamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="665e7-139">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="665e7-140">Zuordnen von MAPI-Namen zu kanonischen Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="665e7-140">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

