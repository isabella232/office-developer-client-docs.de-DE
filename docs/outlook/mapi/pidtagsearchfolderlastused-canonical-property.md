---
title: PidTagSearchFolderLastUsed (kanonische Eigenschaft)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagSearchFolderLastUsed
api_type:
- COM
ms.assetid: e4071307-6205-4079-ab65-7499d14f145c
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: b90639675fa566a83dd78c6ac250f743d68480e9
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19795110"
---
# <a name="pidtagsearchfolderlastused-canonical-property"></a><span data-ttu-id="9dd82-103">PidTagSearchFolderLastUsed (kanonische Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="9dd82-103">PidTagSearchFolderLastUsed Canonical Property</span></span>

  
  
<span data-ttu-id="9dd82-104">**Betrifft**: Outlook</span><span class="sxs-lookup"><span data-stu-id="9dd82-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="9dd82-105">Der letzte Zeitpunkt des Zugriffs auf der Ordner darstellt.</span><span class="sxs-lookup"><span data-stu-id="9dd82-105">Represents the last time the folder was accessed.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="9dd82-106">Zugeordneten Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="9dd82-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="9dd82-107">PR_WB_SF_LAST_USED</span><span class="sxs-lookup"><span data-stu-id="9dd82-107">PR_WB_SF_LAST_USED</span></span>  <br/> |
|<span data-ttu-id="9dd82-108">Bezeichner:</span><span class="sxs-lookup"><span data-stu-id="9dd82-108">Identifier:</span></span>  <br/> |<span data-ttu-id="9dd82-109">0x6834</span><span class="sxs-lookup"><span data-stu-id="9dd82-109">0x6834</span></span>  <br/> |
|<span data-ttu-id="9dd82-110">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="9dd82-110">Data type:</span></span>  <br/> |<span data-ttu-id="9dd82-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="9dd82-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="9dd82-112">Bereich:</span><span class="sxs-lookup"><span data-stu-id="9dd82-112">Area:</span></span>  <br/> |<span data-ttu-id="9dd82-113">Suche</span><span class="sxs-lookup"><span data-stu-id="9dd82-113">Search</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="9dd82-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="9dd82-114">Remarks</span></span>

<span data-ttu-id="9dd82-115">Diese Eigenschaft muss als die Anzahl der Minuten seit Mitternacht (Coordinated Universal Time, UTC) 1. Januar 1601 formatiert werden.</span><span class="sxs-lookup"><span data-stu-id="9dd82-115">This property must be formatted as the number of minutes since midnight Coordinated Universal Time (UTC) January 1, 1601.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="9dd82-116">Verwandte Ressourcen</span><span class="sxs-lookup"><span data-stu-id="9dd82-116">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="9dd82-117">Protokollspezifikationen</span><span class="sxs-lookup"><span data-stu-id="9dd82-117">Protocol specifications</span></span>

<span data-ttu-id="9dd82-118">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="9dd82-118">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="9dd82-119">Bietet Verweise auf Verwandte Exchange Server-Spezifikationen.</span><span class="sxs-lookup"><span data-stu-id="9dd82-119">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="9dd82-120">[[MS-OXOSRCH]](http://msdn.microsoft.com/library/c72e49b8-78c7-4483-ad65-e46e9133673b%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="9dd82-120">[[MS-OXOSRCH]](http://msdn.microsoft.com/library/c72e49b8-78c7-4483-ad65-e46e9133673b%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="9dd82-121">Gibt die Eigenschaften und Operationen für das Bearbeiten der Liste einer Suchkonfiguration-Ordner.</span><span class="sxs-lookup"><span data-stu-id="9dd82-121">Specifies the properties and operations for manipulating a search folder list configuration.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="9dd82-122">Header-Dateien</span><span class="sxs-lookup"><span data-stu-id="9dd82-122">Header files</span></span>

<span data-ttu-id="9dd82-123">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="9dd82-123">Mapidefs.h</span></span>
  
> <span data-ttu-id="9dd82-124">Enthält die Datentypdefinitionen.</span><span class="sxs-lookup"><span data-stu-id="9dd82-124">Provides data type definitions.</span></span>
    
<span data-ttu-id="9dd82-125">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="9dd82-125">Mapitags.h</span></span>
  
> <span data-ttu-id="9dd82-126">Enthält Definitionen von Eigenschaften, die als Alternative Namen aufgelistet.</span><span class="sxs-lookup"><span data-stu-id="9dd82-126">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="9dd82-127">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="9dd82-127">See also</span></span>



[<span data-ttu-id="9dd82-128">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="9dd82-128">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="9dd82-129">Kanonische MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="9dd82-129">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="9dd82-130">Zuordnen von kanonischen Eigenschaftennamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="9dd82-130">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="9dd82-131">Zuordnen von MAPI-Namen zu kanonische Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="9dd82-131">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

