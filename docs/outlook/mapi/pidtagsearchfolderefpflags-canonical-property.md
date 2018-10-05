---
title: PidTagSearchFolderEfpFlags (kanonische Eigenschaft)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagSearchFolderEfpFlags
api_type:
- COM
ms.assetid: ef82a75f-a09f-4880-ba6a-e739b16422a3
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: d670aa91cc60c051f8464f9d83536b888b44ca9e
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/04/2018
ms.locfileid: "25400663"
---
# <a name="pidtagsearchfolderefpflags-canonical-property"></a><span data-ttu-id="45821-103">PidTagSearchFolderEfpFlags (kanonische Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="45821-103">PidTagSearchFolderEfpFlags Canonical Property</span></span>

  
  
<span data-ttu-id="45821-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="45821-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="45821-105">Enthält erweiterte Ordner Flags, die für die Suche Ordnercontainer für den Suchordner gelten.</span><span class="sxs-lookup"><span data-stu-id="45821-105">Contains extended folder flags that apply to the search folder container for the search folder.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="45821-106">Zugeordnete Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="45821-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="45821-107">PR_WB_SF_EFP_FLAGS</span><span class="sxs-lookup"><span data-stu-id="45821-107">PR_WB_SF_EFP_FLAGS</span></span>  <br/> |
|<span data-ttu-id="45821-108">Kennung:</span><span class="sxs-lookup"><span data-stu-id="45821-108">Identifier:</span></span>  <br/> |<span data-ttu-id="45821-109">0x6848</span><span class="sxs-lookup"><span data-stu-id="45821-109">0x6848</span></span>  <br/> |
|<span data-ttu-id="45821-110">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="45821-110">Data type:</span></span>  <br/> |<span data-ttu-id="45821-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="45821-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="45821-112">Bereich:</span><span class="sxs-lookup"><span data-stu-id="45821-112">Area:</span></span>  <br/> |<span data-ttu-id="45821-113">Suche</span><span class="sxs-lookup"><span data-stu-id="45821-113">Search</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="45821-114">Hinweise</span><span class="sxs-lookup"><span data-stu-id="45821-114">Remarks</span></span>

<span data-ttu-id="45821-115">Diese Eigenschaft sollten insbesondere die Kennzeichen in der **PR_EXTENDED_FOLDER_FLAGS** ([PidTagExtendedFolderFlags](pidtagextendedfolderflags-canonical-property.md))-Eigenschaft und die untergeordnete Eigenschaft **ExtendedFlags** im Feld b für den Ordner enthalten.</span><span class="sxs-lookup"><span data-stu-id="45821-115">This property should specifically contain the flags in the **PR_EXTENDED_FOLDER_FLAGS** ([PidTagExtendedFolderFlags](pidtagextendedfolderflags-canonical-property.md)) property, and the **ExtendedFlags** sub-property, in field b for the folder.</span></span> <span data-ttu-id="45821-116">Informationen zum Ordner Flags finden Sie in der [[MS-OXOCFG]](https://msdn.microsoft.com/library/7d466dd5-c156-4da9-9a01-75c78e7e1a67%28Office.15%29.aspx).</span><span class="sxs-lookup"><span data-stu-id="45821-116">For information about folder flags see the [[MS-OXOCFG]](https://msdn.microsoft.com/library/7d466dd5-c156-4da9-9a01-75c78e7e1a67%28Office.15%29.aspx).</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="45821-117">Verwandte Ressourcen</span><span class="sxs-lookup"><span data-stu-id="45821-117">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="45821-118">Protokollspezifikationen</span><span class="sxs-lookup"><span data-stu-id="45821-118">Protocol specifications</span></span>

<span data-ttu-id="45821-119">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="45821-119">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="45821-120">Bietet Verweise auf Verwandte Exchange Server-Spezifikationen.</span><span class="sxs-lookup"><span data-stu-id="45821-120">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="45821-121">[[MS-OXOSRCH]](https://msdn.microsoft.com/library/c72e49b8-78c7-4483-ad65-e46e9133673b%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="45821-121">[[MS-OXOSRCH]](https://msdn.microsoft.com/library/c72e49b8-78c7-4483-ad65-e46e9133673b%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="45821-122">Gibt die Eigenschaften und Operationen für das Bearbeiten der Liste einer Suchkonfiguration-Ordner.</span><span class="sxs-lookup"><span data-stu-id="45821-122">Specifies the properties and operations for manipulating a search folder list configuration.</span></span>
    
<span data-ttu-id="45821-123">[[MS-OXOCFG]](https://msdn.microsoft.com/library/7d466dd5-c156-4da9-9a01-75c78e7e1a67%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="45821-123">[[MS-OXOCFG]](https://msdn.microsoft.com/library/7d466dd5-c156-4da9-9a01-75c78e7e1a67%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="45821-124">Gibt den Speicherort und die Eigenschaften von Client- und Konfigurationsdaten, wie etwa freigegebene Kategorielisten und Arbeitszeiten.</span><span class="sxs-lookup"><span data-stu-id="45821-124">Specifies the location and properties of client and server configuration data, such as shared category lists and working hours.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="45821-125">Header-Dateien</span><span class="sxs-lookup"><span data-stu-id="45821-125">Header files</span></span>

<span data-ttu-id="45821-126">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="45821-126">Mapidefs.h</span></span>
  
> <span data-ttu-id="45821-127">Enthält die Datentypdefinitionen.</span><span class="sxs-lookup"><span data-stu-id="45821-127">Provides data type definitions.</span></span>
    
<span data-ttu-id="45821-128">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="45821-128">Mapitags.h</span></span>
  
> <span data-ttu-id="45821-129">Enthält Definitionen von Eigenschaften, die als Alternative Namen aufgelistet.</span><span class="sxs-lookup"><span data-stu-id="45821-129">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="45821-130">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="45821-130">See also</span></span>



[<span data-ttu-id="45821-131">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="45821-131">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="45821-132">Kanonische MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="45821-132">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="45821-133">Zuordnen von kanonischen Eigenschaftennamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="45821-133">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="45821-134">Zuordnen von MAPI-Namen zu kanonische Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="45821-134">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

