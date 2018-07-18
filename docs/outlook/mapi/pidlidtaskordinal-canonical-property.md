---
title: PidLidTaskOrdinal (kanonische Eigenschaft)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidTaskOrdinal
api_type:
- COM
ms.assetid: 1021860e-4c40-4c22-aa68-b568d046aaf7
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: 033bc038988373b11f3eac863a256717624999f9
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19793848"
---
# <a name="pidlidtaskordinal-canonical-property"></a><span data-ttu-id="4f1bb-103">PidLidTaskOrdinal (kanonische Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="4f1bb-103">PidLidTaskOrdinal Canonical Property</span></span>

  
  
<span data-ttu-id="4f1bb-104">**Betrifft**: Outlook</span><span class="sxs-lookup"><span data-stu-id="4f1bb-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="4f1bb-105">Bietet Hilfe benutzerdefinierten Sortierung Aufgaben.</span><span class="sxs-lookup"><span data-stu-id="4f1bb-105">Provides an aid to custom sorting tasks.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="4f1bb-106">Zugeordneten Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="4f1bb-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="4f1bb-107">dispidTaskOrdinal</span><span class="sxs-lookup"><span data-stu-id="4f1bb-107">dispidTaskOrdinal</span></span>  <br/> |
|<span data-ttu-id="4f1bb-108">-Eigenschaft festgelegt:</span><span class="sxs-lookup"><span data-stu-id="4f1bb-108">Property set:</span></span>  <br/> |<span data-ttu-id="4f1bb-109">PSETID_Task</span><span class="sxs-lookup"><span data-stu-id="4f1bb-109">PSETID_Task</span></span>  <br/> |
|<span data-ttu-id="4f1bb-110">Long-ID (Abdeckung):</span><span class="sxs-lookup"><span data-stu-id="4f1bb-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="4f1bb-111">0x00008123</span><span class="sxs-lookup"><span data-stu-id="4f1bb-111">0x00008123</span></span>  <br/> |
|<span data-ttu-id="4f1bb-112">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="4f1bb-112">Data type:</span></span>  <br/> |<span data-ttu-id="4f1bb-113">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="4f1bb-113">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="4f1bb-114">Bereich:</span><span class="sxs-lookup"><span data-stu-id="4f1bb-114">Area:</span></span>  <br/> |<span data-ttu-id="4f1bb-115">Aufgabe</span><span class="sxs-lookup"><span data-stu-id="4f1bb-115">Task</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="4f1bb-116">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="4f1bb-116">Remarks</span></span>

<span data-ttu-id="4f1bb-117">Diese Eigenschaft kann nicht festgelegt bleiben.</span><span class="sxs-lookup"><span data-stu-id="4f1bb-117">This property may be left unset.</span></span> <span data-ttu-id="4f1bb-118">Wenn festgelegt, dessen Wert größer als "0x800186A0" (-2,147,383,648) sein muss und weniger als "0x7FFE7960" (2,147,383,648) und unter Aufgaben im selben Ordner eindeutig sein müssen.</span><span class="sxs-lookup"><span data-stu-id="4f1bb-118">If set, its value must be greater than "0x800186A0" (-2,147,383,648) and less than "0x7FFE7960" (2,147,383,648) and must be unique among tasks in the same folder.</span></span>
  
<span data-ttu-id="4f1bb-119">Wenn der Client diese Eigenschaft auf eine Zahl kleiner als den negativen Wert des aktuellen Werts der Eigenschaft **PR_ORDINAL_MOST** ([PidTagOrdinalMost](pidtagordinalmost-canonical-property.md)) des Ordners festgelegt wird, muss der Client auch **PR_ORDINAL_MOST** für den Ordner aktualisieren.</span><span class="sxs-lookup"><span data-stu-id="4f1bb-119">Whenever the client sets this property to a number less than the negative of the current value of the **PR_ORDINAL_MOST** ([PidTagOrdinalMost](pidtagordinalmost-canonical-property.md)) property of the folder, the client must also update **PR_ORDINAL_MOST** on the folder.</span></span> 
  
<span data-ttu-id="4f1bb-120">Die **PR_ORDINAL_MOST** -Eigenschaft des Ordners bietet eine effiziente Möglichkeit um einen eindeutigen Wert zwischen Aufgaben im selben Ordner zu bestimmen.</span><span class="sxs-lookup"><span data-stu-id="4f1bb-120">The **PR_ORDINAL_MOST** property of the folder provides an efficient way to determine a unique value among tasks in the same folder.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="4f1bb-121">Verwandte Ressourcen</span><span class="sxs-lookup"><span data-stu-id="4f1bb-121">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="4f1bb-122">Protokollspezifikationen</span><span class="sxs-lookup"><span data-stu-id="4f1bb-122">Protocol specifications</span></span>

<span data-ttu-id="4f1bb-123">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="4f1bb-123">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="4f1bb-124">Enthält Eigenschaftendefinitionen und Verweise auf Verwandte Exchange Server-Spezifikationen.</span><span class="sxs-lookup"><span data-stu-id="4f1bb-124">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="4f1bb-125">[[MS-OXOTASK]](http://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="4f1bb-125">[[MS-OXOTASK]](http://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="4f1bb-126">Mehrere Objekte, die das elektronische Äquivalent von Aufgaben, vorgangszuordnungen und vorgangsaktualisierungen Modell definiert.</span><span class="sxs-lookup"><span data-stu-id="4f1bb-126">Defines several objects that model the electronic equivalent of tasks, task assignments, and task updates.</span></span> 
    
### <a name="header-files"></a><span data-ttu-id="4f1bb-127">Header-Dateien</span><span class="sxs-lookup"><span data-stu-id="4f1bb-127">Header files</span></span>

<span data-ttu-id="4f1bb-128">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="4f1bb-128">Mapidefs.h</span></span>
  
> <span data-ttu-id="4f1bb-129">Enthält die Datentypdefinitionen.</span><span class="sxs-lookup"><span data-stu-id="4f1bb-129">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="4f1bb-130">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="4f1bb-130">See also</span></span>



[<span data-ttu-id="4f1bb-131">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="4f1bb-131">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="4f1bb-132">Kanonische MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="4f1bb-132">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="4f1bb-133">Zuordnen von kanonischen Eigenschaftennamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="4f1bb-133">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="4f1bb-134">Zuordnen von MAPI-Namen zu kanonische Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="4f1bb-134">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

