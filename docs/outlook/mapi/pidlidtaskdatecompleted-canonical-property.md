---
title: PidLidTaskDateCompleted (kanonische Eigenschaft)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidTaskDateCompleted
api_type:
- COM
ms.assetid: ae384529-55e2-4da1-9a41-acc292591a7c
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 3096e7ab2133d2984be0534cb091d61d2c7157bd
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32303213"
---
# <a name="pidlidtaskdatecompleted-canonical-property"></a><span data-ttu-id="53956-103">PidLidTaskDateCompleted (kanonische Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="53956-103">PidLidTaskDateCompleted Canonical Property</span></span>

  
  
<span data-ttu-id="53956-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="53956-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="53956-105">Gibt das Datum an, an dem der Benutzer die Aufgabe abgeschlossen hat.</span><span class="sxs-lookup"><span data-stu-id="53956-105">Specifies the date when the user completes the task.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="53956-106">Zugeordnete Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="53956-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="53956-107">dispidTaskDateCompleted</span><span class="sxs-lookup"><span data-stu-id="53956-107">dispidTaskDateCompleted</span></span>  <br/> |
|<span data-ttu-id="53956-108">Eigenschaftensatz:</span><span class="sxs-lookup"><span data-stu-id="53956-108">Property set:</span></span>  <br/> |<span data-ttu-id="53956-109">PSETID_Task</span><span class="sxs-lookup"><span data-stu-id="53956-109">PSETID_Task</span></span>  <br/> |
|<span data-ttu-id="53956-110">Lange ID (LID):</span><span class="sxs-lookup"><span data-stu-id="53956-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="53956-111">0x0000810F</span><span class="sxs-lookup"><span data-stu-id="53956-111">0x0000810F</span></span>  <br/> |
|<span data-ttu-id="53956-112">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="53956-112">Data type:</span></span>  <br/> |<span data-ttu-id="53956-113">PT_SYSTIME</span><span class="sxs-lookup"><span data-stu-id="53956-113">PT_SYSTIME</span></span>  <br/> |
|<span data-ttu-id="53956-114">Bereich:</span><span class="sxs-lookup"><span data-stu-id="53956-114">Area:</span></span>  <br/> |<span data-ttu-id="53956-115">Aufgabe</span><span class="sxs-lookup"><span data-stu-id="53956-115">Task</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="53956-116">Hinweise</span><span class="sxs-lookup"><span data-stu-id="53956-116">Remarks</span></span>

<span data-ttu-id="53956-117">Wenn diese Eigenschaft festgelegt ist, muss sie eine Zeitkomponente von Mitternacht in der lokalen Zeitzone haben, die in koordinierte Weltzeit (Coordinated Universal Time, UTC) konvertiert wird.</span><span class="sxs-lookup"><span data-stu-id="53956-117">If set, this property must have a time component of midnight in the local time zone, converted to Coordinated Universal Time (UTC).</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="53956-118">Verwandte Ressourcen</span><span class="sxs-lookup"><span data-stu-id="53956-118">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="53956-119">Protokollspezifikationen</span><span class="sxs-lookup"><span data-stu-id="53956-119">Protocol specifications</span></span>

<span data-ttu-id="53956-120">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="53956-120">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="53956-121">Stellt Eigenschaftensatzdefinitionen und Verweise auf verwandte Exchange Server zur Verfügung.</span><span class="sxs-lookup"><span data-stu-id="53956-121">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="53956-122">[[MS-OXOTASK]](https://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="53956-122">[[MS-OXOTASK]](https://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="53956-123">Definiert mehrere Objekte, die das elektronische Äquivalent von Vorgängen, Vorgangszuordnungen und Vorgangsaktualisierungen modellieren.</span><span class="sxs-lookup"><span data-stu-id="53956-123">Defines several objects that model the electronic equivalent of tasks, task assignments, and task updates.</span></span> 
    
### <a name="header-files"></a><span data-ttu-id="53956-124">Headerdateien</span><span class="sxs-lookup"><span data-stu-id="53956-124">Header files</span></span>

<span data-ttu-id="53956-125">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="53956-125">Mapidefs.h</span></span>
  
> <span data-ttu-id="53956-126">Bietet Datentypdefinitionen.</span><span class="sxs-lookup"><span data-stu-id="53956-126">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="53956-127">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="53956-127">See also</span></span>



[<span data-ttu-id="53956-128">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="53956-128">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="53956-129">KANONISCHE EIGENSCHAFTEN VON MAPI</span><span class="sxs-lookup"><span data-stu-id="53956-129">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="53956-130">Zuordnen kanonischer Eigenschaftsnamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="53956-130">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="53956-131">Zuordnen von MAPI-Namen zu kanonischen Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="53956-131">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

