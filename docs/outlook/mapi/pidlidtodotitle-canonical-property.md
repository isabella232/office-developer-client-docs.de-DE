---
title: PidLidToDoTitle (kanonische Eigenschaft)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidToDoTitle
api_type:
- COM
ms.assetid: 94cf031f-4c78-441d-9c01-55905b4974e0
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: 66208b2d31ca379389f3249abf281dd4d040e276
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19793879"
---
# <a name="pidlidtodotitle-canonical-property"></a><span data-ttu-id="35a62-103">PidLidToDoTitle (kanonische Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="35a62-103">PidLidToDoTitle Canonical Property</span></span>

  
  
<span data-ttu-id="35a62-104">**Betrifft**: Outlook</span><span class="sxs-lookup"><span data-stu-id="35a62-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="35a62-105">Enthält Benutzer festzulegen Text, um dieses Objekt "Message" in einer konsolidierten Vorgangsliste zu ermitteln.</span><span class="sxs-lookup"><span data-stu-id="35a62-105">Contains user-specifiable text to identify this message object in a consolidated to-do list.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="35a62-106">Zugeordneten Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="35a62-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="35a62-107">dispidToDoTitle</span><span class="sxs-lookup"><span data-stu-id="35a62-107">dispidToDoTitle</span></span>  <br/> |
|<span data-ttu-id="35a62-108">-Eigenschaft festgelegt:</span><span class="sxs-lookup"><span data-stu-id="35a62-108">Property set:</span></span>  <br/> |<span data-ttu-id="35a62-109">PSETID_Common</span><span class="sxs-lookup"><span data-stu-id="35a62-109">PSETID_Common</span></span>  <br/> |
|<span data-ttu-id="35a62-110">Long-ID (Abdeckung):</span><span class="sxs-lookup"><span data-stu-id="35a62-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="35a62-111">0x000085A4</span><span class="sxs-lookup"><span data-stu-id="35a62-111">0x000085A4</span></span>  <br/> |
|<span data-ttu-id="35a62-112">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="35a62-112">Data type:</span></span>  <br/> |<span data-ttu-id="35a62-113">PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="35a62-113">PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="35a62-114">Bereich:</span><span class="sxs-lookup"><span data-stu-id="35a62-114">Area:</span></span>  <br/> |<span data-ttu-id="35a62-115">Aufgabe</span><span class="sxs-lookup"><span data-stu-id="35a62-115">Task</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="35a62-116">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="35a62-116">Remarks</span></span>

<span data-ttu-id="35a62-117">Diese Eigenschaft muss auf eine Aufgabe nicht festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="35a62-117">This property must not be set on a task.</span></span> <span data-ttu-id="35a62-118">Um eine leere Eigenschaft anzugeben, legen Sie diese Eigenschaft nicht auf die leere Zeichenfolge, aber stattdessen zu löschen.</span><span class="sxs-lookup"><span data-stu-id="35a62-118">To indicate an empty property, do not set this property to the zero-length string, but instead delete it.</span></span> 
  
<span data-ttu-id="35a62-119">Beim Kennzeichnen von einem Message-Objekt und die Eigenschaft nicht vorhanden ist, sollte den Wert der **PR_NORMALIZED_SUBJECT** ([PidTagNormalizedSubject](pidtagnormalizedsubject-canonical-property.md)) ein Client auf diese Eigenschaft geschrieben werden.</span><span class="sxs-lookup"><span data-stu-id="35a62-119">When flagging a message object, and the property does not exist, a client should write the value of **PR_NORMALIZED_SUBJECT** ([PidTagNormalizedSubject](pidtagnormalizedsubject-canonical-property.md)) to this property.</span></span>
  
<span data-ttu-id="35a62-120">In einer konsolidierten Vorgangsliste Wenn diese Eigenschaft nicht vorhanden ist, sollten ein Client den Wert der Eigenschaft **PR_NORMALIZED_SUBJECT** ersetzen, wenn diese Eigenschaft in der Vorgangsliste anzeigen.</span><span class="sxs-lookup"><span data-stu-id="35a62-120">In a consolidated to-do list, if this property does not exist, a client should substitute the value of the **PR_NORMALIZED_SUBJECT** property when displaying this property in the to-do list.</span></span> 
  
<span data-ttu-id="35a62-121">Auf ein Objekt "Message" Entwurf Wenn der Client Absender Flags, die implementiert sollte diese Eigenschaft werden auf denselben Wert als **DispidRequest** ([PidLidFlagRequest](pidlidflagrequest-canonical-property.md)) festgelegt.</span><span class="sxs-lookup"><span data-stu-id="35a62-121">On a draft message object, if the client implements sender flags, this property should be set to the same value as **dispidRequest** ([PidLidFlagRequest](pidlidflagrequest-canonical-property.md)).</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="35a62-122">Verwandte Ressourcen</span><span class="sxs-lookup"><span data-stu-id="35a62-122">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="35a62-123">Protokollspezifikationen</span><span class="sxs-lookup"><span data-stu-id="35a62-123">Protocol specifications</span></span>

<span data-ttu-id="35a62-124">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="35a62-124">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="35a62-125">Enthält Eigenschaftendefinitionen und Verweise auf Verwandte Exchange Server-Spezifikationen</span><span class="sxs-lookup"><span data-stu-id="35a62-125">Provides property set definitions and references to related Exchange Server protocol specifications</span></span>
    
<span data-ttu-id="35a62-126">[[MS-OXOFLAG]](http://msdn.microsoft.com/library/f1e50be4-ed30-4c2a-b5cb-8ff3aaaf9b91%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="35a62-126">[[MS-OXOFLAG]](http://msdn.microsoft.com/library/f1e50be4-ed30-4c2a-b5cb-8ff3aaaf9b91%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="35a62-127">Gibt die Eigenschaften und Vorgänge im Zusammenhang mit kennzeichnen.</span><span class="sxs-lookup"><span data-stu-id="35a62-127">Specifies the properties and operations related to flagging.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="35a62-128">Header-Dateien</span><span class="sxs-lookup"><span data-stu-id="35a62-128">Header files</span></span>

<span data-ttu-id="35a62-129">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="35a62-129">Mapidefs.h</span></span>
  
> <span data-ttu-id="35a62-130">Enthält die Datentypdefinitionen.</span><span class="sxs-lookup"><span data-stu-id="35a62-130">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="35a62-131">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="35a62-131">See also</span></span>



[<span data-ttu-id="35a62-132">PidTagNormalizedSubject (kanonische Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="35a62-132">PidTagNormalizedSubject Canonical Property</span></span>](pidtagnormalizedsubject-canonical-property.md)
  
[<span data-ttu-id="35a62-133">Kanonische PidLidFlagRequest-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="35a62-133">PidLidFlagRequest Canonical Property</span></span>](pidlidflagrequest-canonical-property.md)


[<span data-ttu-id="35a62-134">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="35a62-134">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="35a62-135">Kanonische MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="35a62-135">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="35a62-136">Zuordnen von kanonischen Eigenschaftennamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="35a62-136">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="35a62-137">Zuordnen von MAPI-Namen zu kanonische Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="35a62-137">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

