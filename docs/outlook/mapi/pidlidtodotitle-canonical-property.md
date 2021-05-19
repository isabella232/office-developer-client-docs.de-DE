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
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 7ed69d9bab84a5c572026bb9480249c1212e3376
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32339942"
---
# <a name="pidlidtodotitle-canonical-property"></a><span data-ttu-id="adc92-103">PidLidToDoTitle (kanonische Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="adc92-103">PidLidToDoTitle Canonical Property</span></span>

  
  
<span data-ttu-id="adc92-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="adc92-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="adc92-105">Enthält benutzerspezifikationsfähigen Text, um dieses Nachrichtenobjekt in einer konsolidierten To-Do-Liste zu identifizieren.</span><span class="sxs-lookup"><span data-stu-id="adc92-105">Contains user-specifiable text to identify this message object in a consolidated to-do list.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="adc92-106">Zugeordnete Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="adc92-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="adc92-107">dispidToDoTitle</span><span class="sxs-lookup"><span data-stu-id="adc92-107">dispidToDoTitle</span></span>  <br/> |
|<span data-ttu-id="adc92-108">Eigenschaftensatz:</span><span class="sxs-lookup"><span data-stu-id="adc92-108">Property set:</span></span>  <br/> |<span data-ttu-id="adc92-109">PSETID_Common</span><span class="sxs-lookup"><span data-stu-id="adc92-109">PSETID_Common</span></span>  <br/> |
|<span data-ttu-id="adc92-110">Lange ID (LID):</span><span class="sxs-lookup"><span data-stu-id="adc92-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="adc92-111">0x000085A4</span><span class="sxs-lookup"><span data-stu-id="adc92-111">0x000085A4</span></span>  <br/> |
|<span data-ttu-id="adc92-112">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="adc92-112">Data type:</span></span>  <br/> |<span data-ttu-id="adc92-113">PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="adc92-113">PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="adc92-114">Bereich:</span><span class="sxs-lookup"><span data-stu-id="adc92-114">Area:</span></span>  <br/> |<span data-ttu-id="adc92-115">Aufgabe</span><span class="sxs-lookup"><span data-stu-id="adc92-115">Task</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="adc92-116">Hinweise</span><span class="sxs-lookup"><span data-stu-id="adc92-116">Remarks</span></span>

<span data-ttu-id="adc92-117">Diese Eigenschaft darf nicht für einen Vorgang festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="adc92-117">This property must not be set on a task.</span></span> <span data-ttu-id="adc92-118">Wenn Sie eine leere Eigenschaft angeben möchten, legen Sie diese Eigenschaft nicht auf die leere Zeichenfolge, sondern löschen Sie sie.</span><span class="sxs-lookup"><span data-stu-id="adc92-118">To indicate an empty property, do not set this property to the zero-length string, but instead delete it.</span></span> 
  
<span data-ttu-id="adc92-119">Wenn ein Nachrichtenobjekt kennzeichnend ist und die Eigenschaft nicht vorhanden ist, sollte ein Client den Wert **von PR_NORMALIZED_SUBJECT** ([PidTagNormalizedSubject](pidtagnormalizedsubject-canonical-property.md)) in diese Eigenschaft schreiben.</span><span class="sxs-lookup"><span data-stu-id="adc92-119">When flagging a message object, and the property does not exist, a client should write the value of **PR_NORMALIZED_SUBJECT** ([PidTagNormalizedSubject](pidtagnormalizedsubject-canonical-property.md)) to this property.</span></span>
  
<span data-ttu-id="adc92-120">Wenn diese Eigenschaft nicht vorhanden ist, sollte ein Client in einer konsolidierten To-Do-Liste den Wert der **PR_NORMALIZED_SUBJECT-Eigenschaft** ersetzen, wenn diese Eigenschaft in der To-Do-Liste angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="adc92-120">In a consolidated to-do list, if this property does not exist, a client should substitute the value of the **PR_NORMALIZED_SUBJECT** property when displaying this property in the to-do list.</span></span> 
  
<span data-ttu-id="adc92-121">Wenn der Client Absenderflags implementiert, sollte diese Eigenschaft bei einem Nachrichtenentwurfsobjekt auf denselben Wert wie **dispidRequest** ([PidLidFlagRequest](pidlidflagrequest-canonical-property.md)) festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="adc92-121">On a draft message object, if the client implements sender flags, this property should be set to the same value as **dispidRequest** ([PidLidFlagRequest](pidlidflagrequest-canonical-property.md)).</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="adc92-122">Verwandte Ressourcen</span><span class="sxs-lookup"><span data-stu-id="adc92-122">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="adc92-123">Protokollspezifikationen</span><span class="sxs-lookup"><span data-stu-id="adc92-123">Protocol specifications</span></span>

<span data-ttu-id="adc92-124">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="adc92-124">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="adc92-125">Stellt Eigenschaftensatzdefinitionen und Verweise auf verwandte Exchange Server zur Verfügung.</span><span class="sxs-lookup"><span data-stu-id="adc92-125">Provides property set definitions and references to related Exchange Server protocol specifications</span></span>
    
<span data-ttu-id="adc92-126">[[MS-OXOFLAG]](https://msdn.microsoft.com/library/f1e50be4-ed30-4c2a-b5cb-8ff3aaaf9b91%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="adc92-126">[[MS-OXOFLAG]](https://msdn.microsoft.com/library/f1e50be4-ed30-4c2a-b5cb-8ff3aaaf9b91%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="adc92-127">Gibt die Eigenschaften und Vorgänge im Zusammenhang mit der Kennzeichnung an.</span><span class="sxs-lookup"><span data-stu-id="adc92-127">Specifies the properties and operations related to flagging.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="adc92-128">Headerdateien</span><span class="sxs-lookup"><span data-stu-id="adc92-128">Header files</span></span>

<span data-ttu-id="adc92-129">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="adc92-129">Mapidefs.h</span></span>
  
> <span data-ttu-id="adc92-130">Bietet Datentypdefinitionen.</span><span class="sxs-lookup"><span data-stu-id="adc92-130">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="adc92-131">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="adc92-131">See also</span></span>



[<span data-ttu-id="adc92-132">PidTagNormalizedSubject (kanonische Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="adc92-132">PidTagNormalizedSubject Canonical Property</span></span>](pidtagnormalizedsubject-canonical-property.md)
  
[<span data-ttu-id="adc92-133">Kanonische PidLidFlagRequest-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="adc92-133">PidLidFlagRequest Canonical Property</span></span>](pidlidflagrequest-canonical-property.md)


[<span data-ttu-id="adc92-134">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="adc92-134">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="adc92-135">KANONISCHE EIGENSCHAFTEN VON MAPI</span><span class="sxs-lookup"><span data-stu-id="adc92-135">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="adc92-136">Zuordnen kanonischer Eigenschaftsnamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="adc92-136">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="adc92-137">Zuordnen von MAPI-Namen zu kanonischen Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="adc92-137">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

