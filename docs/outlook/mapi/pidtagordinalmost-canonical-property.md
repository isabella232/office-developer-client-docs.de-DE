---
title: PidTagOrdinalMost (kanonische Eigenschaft)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagOrdinalMost
api_type:
- COM
ms.assetid: c18de08b-8c28-4cdf-bd2e-b9c650cd6da6
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: 0c2cf784ff9a86c9e2a2ce1a25b3c4b8ff7d8b75
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19794663"
---
# <a name="pidtagordinalmost-canonical-property"></a><span data-ttu-id="667bd-103">PidTagOrdinalMost (kanonische Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="667bd-103">PidTagOrdinalMost Canonical Property</span></span>

  
  
<span data-ttu-id="667bd-104">**Betrifft**: Outlook</span><span class="sxs-lookup"><span data-stu-id="667bd-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="667bd-105">Enthält eine positive Zahl, deren negativ kleiner oder gleich dem Wert der Eigenschaft **DispidTaskOrdinal** ([PidLidTaskOrdinal](pidlidtaskordinal-canonical-property.md)) aller Aufgaben im Ordner ist.</span><span class="sxs-lookup"><span data-stu-id="667bd-105">Contains a positive number whose negative is less than or equal to the value of the **dispidTaskOrdinal** ([PidLidTaskOrdinal](pidlidtaskordinal-canonical-property.md)) property of all tasks in the folder.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="667bd-106">Zugeordneten Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="667bd-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="667bd-107">PR_ORDINAL_MOST</span><span class="sxs-lookup"><span data-stu-id="667bd-107">PR_ORDINAL_MOST</span></span>  <br/> |
|<span data-ttu-id="667bd-108">Bezeichner:</span><span class="sxs-lookup"><span data-stu-id="667bd-108">Identifier:</span></span>  <br/> |<span data-ttu-id="667bd-109">0x36E2</span><span class="sxs-lookup"><span data-stu-id="667bd-109">0x36E2</span></span>  <br/> |
|<span data-ttu-id="667bd-110">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="667bd-110">Data type:</span></span>  <br/> |<span data-ttu-id="667bd-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="667bd-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="667bd-112">Bereich:</span><span class="sxs-lookup"><span data-stu-id="667bd-112">Area:</span></span>  <br/> |<span data-ttu-id="667bd-113">Aufgabe</span><span class="sxs-lookup"><span data-stu-id="667bd-113">Task</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="667bd-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="667bd-114">Remarks</span></span>

<span data-ttu-id="667bd-115">Diese Eigenschaft muss aktualisiert werden, um diese Bedingung zu verwalten, wenn sich die **DispidTaskOrdinal** -Eigenschaft eines beliebigen Objekts Aufgabe im Ordner in einer Weise ändert, die die Bedingung verletzen würde.</span><span class="sxs-lookup"><span data-stu-id="667bd-115">This property must be updated to maintain this condition whenever the **dispidTaskOrdinal** property of any task object in the folder changes in a way that would violate the condition.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="667bd-116">Verwandte Ressourcen</span><span class="sxs-lookup"><span data-stu-id="667bd-116">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="667bd-117">Protokollspezifikationen</span><span class="sxs-lookup"><span data-stu-id="667bd-117">Protocol specifications</span></span>

<span data-ttu-id="667bd-118">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="667bd-118">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="667bd-119">Bietet Verweise auf Verwandte Exchange Server-Spezifikationen.</span><span class="sxs-lookup"><span data-stu-id="667bd-119">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="667bd-120">[[MS-OXOTASK]](http://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="667bd-120">[[MS-OXOTASK]](http://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="667bd-121">Gibt die Eigenschaften und Operationen, die für Kontakte und persönliche Verteilerlisten zulässig sind.</span><span class="sxs-lookup"><span data-stu-id="667bd-121">Specifies the properties and operations that are permissible for contacts and personal distribution lists.</span></span>
  
### <a name="header-files"></a><span data-ttu-id="667bd-122">Header-Dateien</span><span class="sxs-lookup"><span data-stu-id="667bd-122">Header files</span></span>

<span data-ttu-id="667bd-123">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="667bd-123">Mapidefs.h</span></span>
  
> <span data-ttu-id="667bd-124">Enthält die Datentypdefinitionen.</span><span class="sxs-lookup"><span data-stu-id="667bd-124">Provides data type definitions.</span></span>
    
<span data-ttu-id="667bd-125">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="667bd-125">Mapitags.h</span></span>
  
> <span data-ttu-id="667bd-126">Enthält Definitionen von Eigenschaften, die als Alternative Namen aufgelistet.</span><span class="sxs-lookup"><span data-stu-id="667bd-126">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="667bd-127">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="667bd-127">See also</span></span>



[<span data-ttu-id="667bd-128">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="667bd-128">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="667bd-129">Kanonische MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="667bd-129">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="667bd-130">Zuordnen von kanonischen Eigenschaftennamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="667bd-130">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="667bd-131">Zuordnen von MAPI-Namen zu kanonische Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="667bd-131">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

