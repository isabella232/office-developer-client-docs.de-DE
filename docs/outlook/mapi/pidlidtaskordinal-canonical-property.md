---
title: Kanonische Pidlidtaskordinal (-Eigenschaft
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
ms.openlocfilehash: a64008da93584529916a9303176bba0aa08d3fac
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32357960"
---
# <a name="pidlidtaskordinal-canonical-property"></a><span data-ttu-id="b1c26-103">Kanonische Pidlidtaskordinal (-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="b1c26-103">PidLidTaskOrdinal Canonical Property</span></span>

  
  
<span data-ttu-id="b1c26-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="b1c26-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="b1c26-105">Stellt eine Hilfe für benutzerdefinierte Sortieraufgaben bereit.</span><span class="sxs-lookup"><span data-stu-id="b1c26-105">Provides an aid to custom sorting tasks.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="b1c26-106">Zugeordnete Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="b1c26-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="b1c26-107">dispidTaskOrdinal</span><span class="sxs-lookup"><span data-stu-id="b1c26-107">dispidTaskOrdinal</span></span>  <br/> |
|<span data-ttu-id="b1c26-108">Eigenschaftensatz:</span><span class="sxs-lookup"><span data-stu-id="b1c26-108">Property set:</span></span>  <br/> |<span data-ttu-id="b1c26-109">PSETID_Task</span><span class="sxs-lookup"><span data-stu-id="b1c26-109">PSETID_Task</span></span>  <br/> |
|<span data-ttu-id="b1c26-110">Long-ID (Deckel):</span><span class="sxs-lookup"><span data-stu-id="b1c26-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="b1c26-111">0x00008123</span><span class="sxs-lookup"><span data-stu-id="b1c26-111">0x00008123</span></span>  <br/> |
|<span data-ttu-id="b1c26-112">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="b1c26-112">Data type:</span></span>  <br/> |<span data-ttu-id="b1c26-113">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="b1c26-113">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="b1c26-114">Bereich:</span><span class="sxs-lookup"><span data-stu-id="b1c26-114">Area:</span></span>  <br/> |<span data-ttu-id="b1c26-115">Aufgabe</span><span class="sxs-lookup"><span data-stu-id="b1c26-115">Task</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="b1c26-116">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="b1c26-116">Remarks</span></span>

<span data-ttu-id="b1c26-117">Diese Eigenschaft kann nicht mehr als unset bleiben.</span><span class="sxs-lookup"><span data-stu-id="b1c26-117">This property may be left unset.</span></span> <span data-ttu-id="b1c26-118">Wenn dieser Wert festgelegt ist, muss er größer sein als "0x800186A0" (-2.147.383.648) und kleiner als "0x7FFE7960" (2.147.383.648) und muss Untervorgängen im gleichen Ordner eindeutig sein.</span><span class="sxs-lookup"><span data-stu-id="b1c26-118">If set, its value must be greater than "0x800186A0" (-2,147,383,648) and less than "0x7FFE7960" (2,147,383,648) and must be unique among tasks in the same folder.</span></span>
  
<span data-ttu-id="b1c26-119">Wenn der Client diese Eigenschaft auf eine Zahl kleiner als den negativen Wert der **PR_ORDINAL_MOST** ([pidtagordinalmost (](pidtagordinalmost-canonical-property.md))-Eigenschaft des Ordners festlegt, muss der Client auch **PR_ORDINAL_MOST** für den Ordner aktualisieren.</span><span class="sxs-lookup"><span data-stu-id="b1c26-119">Whenever the client sets this property to a number less than the negative of the current value of the **PR_ORDINAL_MOST** ([PidTagOrdinalMost](pidtagordinalmost-canonical-property.md)) property of the folder, the client must also update **PR_ORDINAL_MOST** on the folder.</span></span> 
  
<span data-ttu-id="b1c26-120">Die **PR_ORDINAL_MOST** -Eigenschaft des Ordners bietet eine effiziente Möglichkeit, einen eindeutigen Wert zwischen Vorgängen im gleichen Ordner zu ermitteln.</span><span class="sxs-lookup"><span data-stu-id="b1c26-120">The **PR_ORDINAL_MOST** property of the folder provides an efficient way to determine a unique value among tasks in the same folder.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="b1c26-121">Zugehörige Ressourcen</span><span class="sxs-lookup"><span data-stu-id="b1c26-121">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="b1c26-122">Protokollspezifikationen</span><span class="sxs-lookup"><span data-stu-id="b1c26-122">Protocol specifications</span></span>

<span data-ttu-id="b1c26-123">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="b1c26-123">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="b1c26-124">Stellt Eigenschaftensatz Definitionen und Verweise auf zugehörige Exchange Server-Protokollspezifikationen bereit.</span><span class="sxs-lookup"><span data-stu-id="b1c26-124">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="b1c26-125">[[MS-OXOTASK]](https://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="b1c26-125">[[MS-OXOTASK]](https://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="b1c26-126">Definiert mehrere Objekte, die das elektronische Äquivalent von Aufgaben, Vorgangszuordnungen und Vorgangsaktualisierungen modellieren.</span><span class="sxs-lookup"><span data-stu-id="b1c26-126">Defines several objects that model the electronic equivalent of tasks, task assignments, and task updates.</span></span> 
    
### <a name="header-files"></a><span data-ttu-id="b1c26-127">Header Dateien</span><span class="sxs-lookup"><span data-stu-id="b1c26-127">Header files</span></span>

<span data-ttu-id="b1c26-128">Mapidefs. h</span><span class="sxs-lookup"><span data-stu-id="b1c26-128">Mapidefs.h</span></span>
  
> <span data-ttu-id="b1c26-129">Stellt Datentypdefinitionen bereit.</span><span class="sxs-lookup"><span data-stu-id="b1c26-129">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="b1c26-130">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="b1c26-130">See also</span></span>



[<span data-ttu-id="b1c26-131">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="b1c26-131">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="b1c26-132">Kanonische MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="b1c26-132">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="b1c26-133">Zuordnen von kanonischen Eigenschaftennamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="b1c26-133">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="b1c26-134">Zuordnen von MAPI-Namen zu kanonischen Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="b1c26-134">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

