---
title: PidLidLogDuration (kanonische Eigenschaft)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidLogDocumentSaved
api_type:
- COM
ms.assetid: 012a3f6e-fd16-4dc9-845d-2bf4cebeaa42
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 6f25c1a72882f9236d56532b7259f51512734945
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32336918"
---
# <a name="pidlidlogduration-canonical-property"></a><span data-ttu-id="51b67-103">PidLidLogDuration (kanonische Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="51b67-103">PidLidLogDuration Canonical Property</span></span>

  
  
<span data-ttu-id="51b67-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="51b67-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="51b67-105">Stellt die Dauer einer Journalnachricht in Minuten dar.</span><span class="sxs-lookup"><span data-stu-id="51b67-105">Represents the duration, in minutes, of a journal message.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="51b67-106">Zugeordnete Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="51b67-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="51b67-107">dispidLogDuration</span><span class="sxs-lookup"><span data-stu-id="51b67-107">dispidLogDuration</span></span>  <br/> |
|<span data-ttu-id="51b67-108">Eigenschaftensatz:</span><span class="sxs-lookup"><span data-stu-id="51b67-108">Property set:</span></span>  <br/> |<span data-ttu-id="51b67-109">PSETID_Log</span><span class="sxs-lookup"><span data-stu-id="51b67-109">PSETID_Log</span></span>  <br/> |
|<span data-ttu-id="51b67-110">Lange ID (LID):</span><span class="sxs-lookup"><span data-stu-id="51b67-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="51b67-111">0x00008707</span><span class="sxs-lookup"><span data-stu-id="51b67-111">0x00008707</span></span>  <br/> |
|<span data-ttu-id="51b67-112">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="51b67-112">Data type:</span></span>  <br/> |<span data-ttu-id="51b67-113">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="51b67-113">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="51b67-114">Bereich:</span><span class="sxs-lookup"><span data-stu-id="51b67-114">Area:</span></span>  <br/> |<span data-ttu-id="51b67-115">Journal</span><span class="sxs-lookup"><span data-stu-id="51b67-115">Journal</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="51b67-116">Hinweise</span><span class="sxs-lookup"><span data-stu-id="51b67-116">Remarks</span></span>

<span data-ttu-id="51b67-117">Die Dauer der Aktivität in Minuten, die der Unterschied zwischen den **Eigenschaften dispidLogEnd** ([PidLidLogEnd](pidlidlogend-canonical-property.md)) und **dispidLogStart** ([PidLidLogStart](pidlidlogstart-canonical-property.md)) sein muss.</span><span class="sxs-lookup"><span data-stu-id="51b67-117">The duration, in minutes, of the activity that must be the difference between the **dispidLogEnd** ([PidLidLogEnd](pidlidlogend-canonical-property.md)) and **dispidLogStart** ([PidLidLogStart](pidlidlogstart-canonical-property.md)) properties.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="51b67-118">Verwandte Ressourcen</span><span class="sxs-lookup"><span data-stu-id="51b67-118">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="51b67-119">Protokollspezifikationen</span><span class="sxs-lookup"><span data-stu-id="51b67-119">Protocol specifications</span></span>

<span data-ttu-id="51b67-120">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="51b67-120">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="51b67-121">Stellt Eigenschaftensatzdefinitionen und Verweise auf verwandte Exchange Server zur Verfügung.</span><span class="sxs-lookup"><span data-stu-id="51b67-121">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="51b67-122">[[MS-OXOJRNL]](https://msdn.microsoft.com/library/2aa04fd2-0f36-4ce4-9178-c0fc70aa8d43%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="51b67-122">[[MS-OXOJRNL]](https://msdn.microsoft.com/library/2aa04fd2-0f36-4ce4-9178-c0fc70aa8d43%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="51b67-123">Gibt die Eigenschaften und Vorgänge an, die für Journale zulässig sind.</span><span class="sxs-lookup"><span data-stu-id="51b67-123">Specifies the properties and operations that are permissible for journals.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="51b67-124">Headerdateien</span><span class="sxs-lookup"><span data-stu-id="51b67-124">Header files</span></span>

<span data-ttu-id="51b67-125">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="51b67-125">Mapidefs.h</span></span>
  
> <span data-ttu-id="51b67-126">Bietet Datentypdefinitionen.</span><span class="sxs-lookup"><span data-stu-id="51b67-126">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="51b67-127">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="51b67-127">See also</span></span>



[<span data-ttu-id="51b67-128">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="51b67-128">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="51b67-129">KANONISCHE EIGENSCHAFTEN VON MAPI</span><span class="sxs-lookup"><span data-stu-id="51b67-129">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="51b67-130">Zuordnen kanonischer Eigenschaftsnamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="51b67-130">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="51b67-131">Zuordnen von MAPI-Namen zu kanonischen Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="51b67-131">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

