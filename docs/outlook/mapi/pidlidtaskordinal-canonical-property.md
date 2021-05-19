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
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: a64008da93584529916a9303176bba0aa08d3fac
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32357960"
---
# <a name="pidlidtaskordinal-canonical-property"></a><span data-ttu-id="52489-103">PidLidTaskOrdinal (kanonische Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="52489-103">PidLidTaskOrdinal Canonical Property</span></span>

  
  
<span data-ttu-id="52489-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="52489-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="52489-105">Stellt eine Hilfe zu benutzerdefinierten Sortieraufgaben dar.</span><span class="sxs-lookup"><span data-stu-id="52489-105">Provides an aid to custom sorting tasks.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="52489-106">Zugeordnete Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="52489-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="52489-107">dispidTaskOrdinal</span><span class="sxs-lookup"><span data-stu-id="52489-107">dispidTaskOrdinal</span></span>  <br/> |
|<span data-ttu-id="52489-108">Eigenschaftensatz:</span><span class="sxs-lookup"><span data-stu-id="52489-108">Property set:</span></span>  <br/> |<span data-ttu-id="52489-109">PSETID_Task</span><span class="sxs-lookup"><span data-stu-id="52489-109">PSETID_Task</span></span>  <br/> |
|<span data-ttu-id="52489-110">Lange ID (LID):</span><span class="sxs-lookup"><span data-stu-id="52489-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="52489-111">0x00008123</span><span class="sxs-lookup"><span data-stu-id="52489-111">0x00008123</span></span>  <br/> |
|<span data-ttu-id="52489-112">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="52489-112">Data type:</span></span>  <br/> |<span data-ttu-id="52489-113">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="52489-113">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="52489-114">Bereich:</span><span class="sxs-lookup"><span data-stu-id="52489-114">Area:</span></span>  <br/> |<span data-ttu-id="52489-115">Aufgabe</span><span class="sxs-lookup"><span data-stu-id="52489-115">Task</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="52489-116">Hinweise</span><span class="sxs-lookup"><span data-stu-id="52489-116">Remarks</span></span>

<span data-ttu-id="52489-117">Diese Eigenschaft wird möglicherweise nicht mehr verwendet.</span><span class="sxs-lookup"><span data-stu-id="52489-117">This property may be left unset.</span></span> <span data-ttu-id="52489-118">Wenn festgelegt, muss der Wert größer als "0x800186A0" (-2.147.383.648) und kleiner als "0x7FFE7960" (2.147.383.648) sein und muss für Aufgaben im gleichen Ordner eindeutig sein.</span><span class="sxs-lookup"><span data-stu-id="52489-118">If set, its value must be greater than "0x800186A0" (-2,147,383,648) and less than "0x7FFE7960" (2,147,383,648) and must be unique among tasks in the same folder.</span></span>
  
<span data-ttu-id="52489-119">Wenn der Client diese Eigenschaft auf eine Zahl unter dem negativen Wert des aktuellen Werts der **PR_ORDINAL_MOST** ([PidTagOrdinalMost](pidtagordinalmost-canonical-property.md))-Eigenschaft des Ordners legt, muss der Client auch PR_ORDINAL_MOST ordner aktualisieren. </span><span class="sxs-lookup"><span data-stu-id="52489-119">Whenever the client sets this property to a number less than the negative of the current value of the **PR_ORDINAL_MOST** ([PidTagOrdinalMost](pidtagordinalmost-canonical-property.md)) property of the folder, the client must also update **PR_ORDINAL_MOST** on the folder.</span></span> 
  
<span data-ttu-id="52489-120">Die **PR_ORDINAL_MOST-Eigenschaft** des Ordners bietet eine effiziente Möglichkeit, einen eindeutigen Wert zwischen Aufgaben im gleichen Ordner zu ermitteln.</span><span class="sxs-lookup"><span data-stu-id="52489-120">The **PR_ORDINAL_MOST** property of the folder provides an efficient way to determine a unique value among tasks in the same folder.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="52489-121">Verwandte Ressourcen</span><span class="sxs-lookup"><span data-stu-id="52489-121">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="52489-122">Protokollspezifikationen</span><span class="sxs-lookup"><span data-stu-id="52489-122">Protocol specifications</span></span>

<span data-ttu-id="52489-123">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="52489-123">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="52489-124">Stellt Eigenschaftensatzdefinitionen und Verweise auf verwandte Exchange Server zur Verfügung.</span><span class="sxs-lookup"><span data-stu-id="52489-124">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="52489-125">[[MS-OXOTASK]](https://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="52489-125">[[MS-OXOTASK]](https://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="52489-126">Definiert mehrere Objekte, die das elektronische Äquivalent von Vorgängen, Vorgangszuordnungen und Vorgangsaktualisierungen modellieren.</span><span class="sxs-lookup"><span data-stu-id="52489-126">Defines several objects that model the electronic equivalent of tasks, task assignments, and task updates.</span></span> 
    
### <a name="header-files"></a><span data-ttu-id="52489-127">Headerdateien</span><span class="sxs-lookup"><span data-stu-id="52489-127">Header files</span></span>

<span data-ttu-id="52489-128">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="52489-128">Mapidefs.h</span></span>
  
> <span data-ttu-id="52489-129">Bietet Datentypdefinitionen.</span><span class="sxs-lookup"><span data-stu-id="52489-129">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="52489-130">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="52489-130">See also</span></span>



[<span data-ttu-id="52489-131">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="52489-131">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="52489-132">KANONISCHE EIGENSCHAFTEN VON MAPI</span><span class="sxs-lookup"><span data-stu-id="52489-132">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="52489-133">Zuordnen kanonischer Eigenschaftsnamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="52489-133">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="52489-134">Zuordnen von MAPI-Namen zu kanonischen Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="52489-134">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

