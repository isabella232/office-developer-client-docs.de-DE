---
title: PidLidTaskFCreator (kanonische Eigenschaft)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidTaskFCreator
api_type:
- COM
ms.assetid: bb88750b-4773-4241-aa38-462a2634dbcb
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: dfb49fafcc2dc368e84786b526869e0447ccaf8c
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32303080"
---
# <a name="pidlidtaskfcreator-canonical-property"></a><span data-ttu-id="c0c91-103">PidLidTaskFCreator (kanonische Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="c0c91-103">PidLidTaskFCreator Canonical Property</span></span>

  
  
<span data-ttu-id="c0c91-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="c0c91-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="c0c91-105">Gibt an, dass die Aufgabe ursprünglich vom aktuellen Benutzer- oder Benutzer-Agent erstellt wurde, anstatt eine Aufgabenanforderung zu verarbeiten.</span><span class="sxs-lookup"><span data-stu-id="c0c91-105">Indicates the task was originally created by the current user or user agent instead of by processing a task request.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="c0c91-106">Zugeordnete Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="c0c91-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="c0c91-107">dispidTaskFCreator</span><span class="sxs-lookup"><span data-stu-id="c0c91-107">dispidTaskFCreator</span></span>  <br/> |
|<span data-ttu-id="c0c91-108">Eigenschaftensatz:</span><span class="sxs-lookup"><span data-stu-id="c0c91-108">Property set:</span></span>  <br/> |<span data-ttu-id="c0c91-109">PSETID_Task</span><span class="sxs-lookup"><span data-stu-id="c0c91-109">PSETID_Task</span></span>  <br/> |
|<span data-ttu-id="c0c91-110">Lange ID (LID):</span><span class="sxs-lookup"><span data-stu-id="c0c91-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="c0c91-111">0x0000811E</span><span class="sxs-lookup"><span data-stu-id="c0c91-111">0x0000811E</span></span>  <br/> |
|<span data-ttu-id="c0c91-112">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="c0c91-112">Data type:</span></span>  <br/> |<span data-ttu-id="c0c91-113">PT_BOOLEAN</span><span class="sxs-lookup"><span data-stu-id="c0c91-113">PT_BOOLEAN</span></span>  <br/> |
|<span data-ttu-id="c0c91-114">Bereich:</span><span class="sxs-lookup"><span data-stu-id="c0c91-114">Area:</span></span>  <br/> |<span data-ttu-id="c0c91-115">Aufgabe</span><span class="sxs-lookup"><span data-stu-id="c0c91-115">Task</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="c0c91-116">Hinweise</span><span class="sxs-lookup"><span data-stu-id="c0c91-116">Remarks</span></span>

<span data-ttu-id="c0c91-117">Der Client legt diese Eigenschaft auf TRUE fest, wenn der Benutzer die Aufgabe erstellt, und auf FALSE, wenn die Aufgabe von einem anderen Benutzer zugewiesen wird.</span><span class="sxs-lookup"><span data-stu-id="c0c91-117">The client sets this property to TRUE when the user creates the task and to FALSE when the task is assigned by another user.</span></span> <span data-ttu-id="c0c91-118">Wenn diese Eigenschaft nicht mehr verwendet wird, wird der Wert TRUE angenommen.</span><span class="sxs-lookup"><span data-stu-id="c0c91-118">If this property is left unset, a value of TRUE is assumed.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="c0c91-119">Verwandte Ressourcen</span><span class="sxs-lookup"><span data-stu-id="c0c91-119">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="c0c91-120">Protokollspezifikationen</span><span class="sxs-lookup"><span data-stu-id="c0c91-120">Protocol specifications</span></span>

<span data-ttu-id="c0c91-121">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="c0c91-121">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="c0c91-122">Stellt Eigenschaftensatzdefinitionen und Verweise auf verwandte Exchange Server zur Verfügung.</span><span class="sxs-lookup"><span data-stu-id="c0c91-122">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="c0c91-123">[[MS-OXOTASK]](https://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="c0c91-123">[[MS-OXOTASK]](https://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="c0c91-124">Definiert mehrere Objekte, die das elektronische Äquivalent von Vorgängen, Vorgangszuordnungen und Vorgangsaktualisierungen modellieren.</span><span class="sxs-lookup"><span data-stu-id="c0c91-124">Defines several objects that model the electronic equivalent of tasks, task assignments, and task updates.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="c0c91-125">Headerdateien</span><span class="sxs-lookup"><span data-stu-id="c0c91-125">Header files</span></span>

<span data-ttu-id="c0c91-126">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="c0c91-126">Mapidefs.h</span></span>
  
> <span data-ttu-id="c0c91-127">Bietet Datentypdefinitionen.</span><span class="sxs-lookup"><span data-stu-id="c0c91-127">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="c0c91-128">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="c0c91-128">See also</span></span>



[<span data-ttu-id="c0c91-129">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="c0c91-129">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="c0c91-130">KANONISCHE EIGENSCHAFTEN VON MAPI</span><span class="sxs-lookup"><span data-stu-id="c0c91-130">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="c0c91-131">Zuordnen kanonischer Eigenschaftsnamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="c0c91-131">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="c0c91-132">Zuordnen von MAPI-Namen zu kanonischen Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="c0c91-132">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

