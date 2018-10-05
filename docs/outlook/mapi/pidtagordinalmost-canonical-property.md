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
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 31f39cfbd0e993bfc28003fd64e8af97e7e76818
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/04/2018
ms.locfileid: "25392424"
---
# <a name="pidtagordinalmost-canonical-property"></a><span data-ttu-id="09bad-103">PidTagOrdinalMost (kanonische Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="09bad-103">PidTagOrdinalMost Canonical Property</span></span>

  
  
<span data-ttu-id="09bad-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="09bad-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="09bad-105">Enthält eine positive Zahl, deren negativ kleiner oder gleich dem Wert der Eigenschaft **DispidTaskOrdinal** ([PidLidTaskOrdinal](pidlidtaskordinal-canonical-property.md)) aller Aufgaben im Ordner ist.</span><span class="sxs-lookup"><span data-stu-id="09bad-105">Contains a positive number whose negative is less than or equal to the value of the **dispidTaskOrdinal** ([PidLidTaskOrdinal](pidlidtaskordinal-canonical-property.md)) property of all tasks in the folder.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="09bad-106">Zugeordnete Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="09bad-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="09bad-107">PR_ORDINAL_MOST</span><span class="sxs-lookup"><span data-stu-id="09bad-107">PR_ORDINAL_MOST</span></span>  <br/> |
|<span data-ttu-id="09bad-108">Kennung:</span><span class="sxs-lookup"><span data-stu-id="09bad-108">Identifier:</span></span>  <br/> |<span data-ttu-id="09bad-109">0x36E2</span><span class="sxs-lookup"><span data-stu-id="09bad-109">0x36E2</span></span>  <br/> |
|<span data-ttu-id="09bad-110">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="09bad-110">Data type:</span></span>  <br/> |<span data-ttu-id="09bad-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="09bad-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="09bad-112">Bereich:</span><span class="sxs-lookup"><span data-stu-id="09bad-112">Area:</span></span>  <br/> |<span data-ttu-id="09bad-113">Aufgabe</span><span class="sxs-lookup"><span data-stu-id="09bad-113">Task</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="09bad-114">Hinweise</span><span class="sxs-lookup"><span data-stu-id="09bad-114">Remarks</span></span>

<span data-ttu-id="09bad-115">Diese Eigenschaft muss aktualisiert werden, um diese Bedingung zu verwalten, wenn sich die **DispidTaskOrdinal** -Eigenschaft eines beliebigen Objekts Aufgabe im Ordner in einer Weise ändert, die die Bedingung verletzen würde.</span><span class="sxs-lookup"><span data-stu-id="09bad-115">This property must be updated to maintain this condition whenever the **dispidTaskOrdinal** property of any task object in the folder changes in a way that would violate the condition.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="09bad-116">Verwandte Ressourcen</span><span class="sxs-lookup"><span data-stu-id="09bad-116">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="09bad-117">Protokollspezifikationen</span><span class="sxs-lookup"><span data-stu-id="09bad-117">Protocol specifications</span></span>

<span data-ttu-id="09bad-118">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="09bad-118">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="09bad-119">Bietet Verweise auf Verwandte Exchange Server-Spezifikationen.</span><span class="sxs-lookup"><span data-stu-id="09bad-119">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="09bad-120">[[MS-OXOTASK]](https://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="09bad-120">[[MS-OXOTASK]](https://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="09bad-121">Gibt die Eigenschaften und Operationen, die für Kontakte und persönliche Verteilerlisten zulässig sind.</span><span class="sxs-lookup"><span data-stu-id="09bad-121">Specifies the properties and operations that are permissible for contacts and personal distribution lists.</span></span>
  
### <a name="header-files"></a><span data-ttu-id="09bad-122">Header-Dateien</span><span class="sxs-lookup"><span data-stu-id="09bad-122">Header files</span></span>

<span data-ttu-id="09bad-123">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="09bad-123">Mapidefs.h</span></span>
  
> <span data-ttu-id="09bad-124">Enthält die Datentypdefinitionen.</span><span class="sxs-lookup"><span data-stu-id="09bad-124">Provides data type definitions.</span></span>
    
<span data-ttu-id="09bad-125">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="09bad-125">Mapitags.h</span></span>
  
> <span data-ttu-id="09bad-126">Enthält Definitionen von Eigenschaften, die als Alternative Namen aufgelistet.</span><span class="sxs-lookup"><span data-stu-id="09bad-126">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="09bad-127">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="09bad-127">See also</span></span>



[<span data-ttu-id="09bad-128">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="09bad-128">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="09bad-129">Kanonische MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="09bad-129">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="09bad-130">Zuordnen von kanonischen Eigenschaftennamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="09bad-130">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="09bad-131">Zuordnen von MAPI-Namen zu kanonische Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="09bad-131">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

