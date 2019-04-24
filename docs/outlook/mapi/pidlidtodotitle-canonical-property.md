---
title: Kanonische Pidlidtodotitle (-Eigenschaft
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
ms.openlocfilehash: 7ed69d9bab84a5c572026bb9480249c1212e3376
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32339942"
---
# <a name="pidlidtodotitle-canonical-property"></a><span data-ttu-id="08003-103">Kanonische Pidlidtodotitle (-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="08003-103">PidLidToDoTitle Canonical Property</span></span>

  
  
<span data-ttu-id="08003-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="08003-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="08003-105">Enthält benutzerspezifischen Text, um dieses Nachrichtenobjekt in einer konsolidierten Aufgabenliste zu identifizieren.</span><span class="sxs-lookup"><span data-stu-id="08003-105">Contains user-specifiable text to identify this message object in a consolidated to-do list.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="08003-106">Zugeordnete Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="08003-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="08003-107">dispidToDoTitle</span><span class="sxs-lookup"><span data-stu-id="08003-107">dispidToDoTitle</span></span>  <br/> |
|<span data-ttu-id="08003-108">Eigenschaftensatz:</span><span class="sxs-lookup"><span data-stu-id="08003-108">Property set:</span></span>  <br/> |<span data-ttu-id="08003-109">PSETID_Common</span><span class="sxs-lookup"><span data-stu-id="08003-109">PSETID_Common</span></span>  <br/> |
|<span data-ttu-id="08003-110">Long-ID (Deckel):</span><span class="sxs-lookup"><span data-stu-id="08003-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="08003-111">0x000085A4</span><span class="sxs-lookup"><span data-stu-id="08003-111">0x000085A4</span></span>  <br/> |
|<span data-ttu-id="08003-112">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="08003-112">Data type:</span></span>  <br/> |<span data-ttu-id="08003-113">PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="08003-113">PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="08003-114">Bereich:</span><span class="sxs-lookup"><span data-stu-id="08003-114">Area:</span></span>  <br/> |<span data-ttu-id="08003-115">Aufgabe</span><span class="sxs-lookup"><span data-stu-id="08003-115">Task</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="08003-116">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="08003-116">Remarks</span></span>

<span data-ttu-id="08003-117">Diese Eigenschaft darf für einen Vorgang nicht festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="08003-117">This property must not be set on a task.</span></span> <span data-ttu-id="08003-118">Um eine leere Eigenschaft anzugeben, legen Sie diese Eigenschaft nicht auf die Zeichenfolge der Länge 0 (null), sondern stattdessen löschen.</span><span class="sxs-lookup"><span data-stu-id="08003-118">To indicate an empty property, do not set this property to the zero-length string, but instead delete it.</span></span> 
  
<span data-ttu-id="08003-119">Wenn ein Message-Objekt gekennzeichnet wird und die Eigenschaft nicht vorhanden ist, sollte der Wert von **PR_NORMALIZED_SUBJECT** ([PidTagNormalizedSubject](pidtagnormalizedsubject-canonical-property.md)) in diese Eigenschaft geschrieben werden.</span><span class="sxs-lookup"><span data-stu-id="08003-119">When flagging a message object, and the property does not exist, a client should write the value of **PR_NORMALIZED_SUBJECT** ([PidTagNormalizedSubject](pidtagnormalizedsubject-canonical-property.md)) to this property.</span></span>
  
<span data-ttu-id="08003-120">Wenn diese Eigenschaft in einer konsolidierten Aufgabenliste nicht vorhanden ist, sollte der Wert der **PR_NORMALIZED_SUBJECT** -Eigenschaft durch einen Client ersetzt werden, wenn diese Eigenschaft in der Aufgabenliste angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="08003-120">In a consolidated to-do list, if this property does not exist, a client should substitute the value of the **PR_NORMALIZED_SUBJECT** property when displaying this property in the to-do list.</span></span> 
  
<span data-ttu-id="08003-121">Bei einem Entwurfsnachrichten Objekt sollte diese Eigenschaft auf den gleichen Wert wie **dispidRequest** ([pidlidflagrequest (](pidlidflagrequest-canonical-property.md)) festgelegt werden, wenn der Client Absender-Flags implementiert.</span><span class="sxs-lookup"><span data-stu-id="08003-121">On a draft message object, if the client implements sender flags, this property should be set to the same value as **dispidRequest** ([PidLidFlagRequest](pidlidflagrequest-canonical-property.md)).</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="08003-122">Zugehörige Ressourcen</span><span class="sxs-lookup"><span data-stu-id="08003-122">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="08003-123">Protokollspezifikationen</span><span class="sxs-lookup"><span data-stu-id="08003-123">Protocol specifications</span></span>

<span data-ttu-id="08003-124">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="08003-124">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="08003-125">Stellt Eigenschaftensatz Definitionen und Verweise auf zugehörige Exchange Server-Protokollspezifikationen bereit.</span><span class="sxs-lookup"><span data-stu-id="08003-125">Provides property set definitions and references to related Exchange Server protocol specifications</span></span>
    
<span data-ttu-id="08003-126">[[MS-OXOFLAG]](https://msdn.microsoft.com/library/f1e50be4-ed30-4c2a-b5cb-8ff3aaaf9b91%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="08003-126">[[MS-OXOFLAG]](https://msdn.microsoft.com/library/f1e50be4-ed30-4c2a-b5cb-8ff3aaaf9b91%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="08003-127">Gibt die Eigenschaften und Vorgänge im Zusammenhang mit der Markierung an.</span><span class="sxs-lookup"><span data-stu-id="08003-127">Specifies the properties and operations related to flagging.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="08003-128">Header Dateien</span><span class="sxs-lookup"><span data-stu-id="08003-128">Header files</span></span>

<span data-ttu-id="08003-129">Mapidefs. h</span><span class="sxs-lookup"><span data-stu-id="08003-129">Mapidefs.h</span></span>
  
> <span data-ttu-id="08003-130">Stellt Datentypdefinitionen bereit.</span><span class="sxs-lookup"><span data-stu-id="08003-130">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="08003-131">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="08003-131">See also</span></span>



[<span data-ttu-id="08003-132">Kanonische PidTagNormalizedSubject-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="08003-132">PidTagNormalizedSubject Canonical Property</span></span>](pidtagnormalizedsubject-canonical-property.md)
  
[<span data-ttu-id="08003-133">Kanonische PidLidFlagRequest-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="08003-133">PidLidFlagRequest Canonical Property</span></span>](pidlidflagrequest-canonical-property.md)


[<span data-ttu-id="08003-134">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="08003-134">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="08003-135">Kanonische MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="08003-135">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="08003-136">Zuordnen von kanonischen Eigenschaftennamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="08003-136">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="08003-137">Zuordnen von MAPI-Namen zu kanonischen Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="08003-137">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

