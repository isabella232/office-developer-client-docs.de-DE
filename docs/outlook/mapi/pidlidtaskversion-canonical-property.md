---
title: PidLidTaskVersion (kanonische Eigenschaft)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidTaskVersion
api_type:
- COM
ms.assetid: 3ab77f25-ad11-4501-8d35-ef560c07e2f2
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 3daf8a04afc9cf47d808b46f2cee010e15a33cf9
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32356493"
---
# <a name="pidlidtaskversion-canonical-property"></a><span data-ttu-id="aed64-103">PidLidTaskVersion (kanonische Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="aed64-103">PidLidTaskVersion Canonical Property</span></span>

  
  
<span data-ttu-id="aed64-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="aed64-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="aed64-105">Gibt an, welche Kopie die neueste Aktualisierung eines Vorgangs ist.</span><span class="sxs-lookup"><span data-stu-id="aed64-105">Indicates which copy is the latest update of a task.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="aed64-106">Zugeordnete Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="aed64-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="aed64-107">dispidTaskVersion</span><span class="sxs-lookup"><span data-stu-id="aed64-107">dispidTaskVersion</span></span>  <br/> |
|<span data-ttu-id="aed64-108">Eigenschaftensatz:</span><span class="sxs-lookup"><span data-stu-id="aed64-108">Property set:</span></span>  <br/> |<span data-ttu-id="aed64-109">PSETID_Task</span><span class="sxs-lookup"><span data-stu-id="aed64-109">PSETID_Task</span></span>  <br/> |
|<span data-ttu-id="aed64-110">Lange ID (LID):</span><span class="sxs-lookup"><span data-stu-id="aed64-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="aed64-111">0x00008112</span><span class="sxs-lookup"><span data-stu-id="aed64-111">0x00008112</span></span>  <br/> |
|<span data-ttu-id="aed64-112">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="aed64-112">Data type:</span></span>  <br/> |<span data-ttu-id="aed64-113">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="aed64-113">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="aed64-114">Bereich:</span><span class="sxs-lookup"><span data-stu-id="aed64-114">Area:</span></span>  <br/> |<span data-ttu-id="aed64-115">Aufgabe</span><span class="sxs-lookup"><span data-stu-id="aed64-115">Task</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="aed64-116">Hinweise</span><span class="sxs-lookup"><span data-stu-id="aed64-116">Remarks</span></span>

<span data-ttu-id="aed64-117">Updates mit niedrigeren Versionen als die Aufgabe werden ignoriert.</span><span class="sxs-lookup"><span data-stu-id="aed64-117">Updates with lower versions than the task are ignored.</span></span> 
  
<span data-ttu-id="aed64-118">Beim Einbetten einer Aufgabe in eine Aufgabenkommunikation legt der Client auch die aktuelle Version der eingebetteten Aufgabe für die Aufgabenkommunikation fest.</span><span class="sxs-lookup"><span data-stu-id="aed64-118">When embedding a task in a task communication, the client sets the current version of the embedded task on the task communication as well.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="aed64-119">Verwandte Ressourcen</span><span class="sxs-lookup"><span data-stu-id="aed64-119">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="aed64-120">Protokollspezifikationen</span><span class="sxs-lookup"><span data-stu-id="aed64-120">Protocol specifications</span></span>

<span data-ttu-id="aed64-121">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="aed64-121">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="aed64-122">Stellt Eigenschaftensatzdefinitionen und Verweise auf verwandte Exchange Server zur Verfügung.</span><span class="sxs-lookup"><span data-stu-id="aed64-122">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="aed64-123">[[MS-OXOTASK]](https://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="aed64-123">[[MS-OXOTASK]](https://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="aed64-124">Definiert mehrere Objekte, die das elektronische Äquivalent von Vorgängen, Vorgangszuordnungen und Vorgangsaktualisierungen modellieren.</span><span class="sxs-lookup"><span data-stu-id="aed64-124">Defines several objects that model the electronic equivalent of tasks, task assignments, and task updates.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="aed64-125">Headerdateien</span><span class="sxs-lookup"><span data-stu-id="aed64-125">Header files</span></span>

<span data-ttu-id="aed64-126">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="aed64-126">Mapidefs.h</span></span>
  
> <span data-ttu-id="aed64-127">Bietet Datentypdefinitionen.</span><span class="sxs-lookup"><span data-stu-id="aed64-127">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="aed64-128">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="aed64-128">See also</span></span>



[<span data-ttu-id="aed64-129">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="aed64-129">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="aed64-130">KANONISCHE EIGENSCHAFTEN VON MAPI</span><span class="sxs-lookup"><span data-stu-id="aed64-130">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="aed64-131">Zuordnen kanonischer Eigenschaftsnamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="aed64-131">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="aed64-132">Zuordnen von MAPI-Namen zu kanonischen Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="aed64-132">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

