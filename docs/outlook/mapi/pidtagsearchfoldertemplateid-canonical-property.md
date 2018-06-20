---
title: Kanonische PidTagSearchFolderTemplateId-Eigenschaft
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagSearchFolderTemplateId
api_type:
- COM
ms.assetid: 56288f55-b3ba-42df-9c90-f9b5857f19a1
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: 4e752d3264a64ad7b467947c44d01eb7c47ec863
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19795126"
---
# <a name="pidtagsearchfoldertemplateid-canonical-property"></a><span data-ttu-id="13dd4-103">Kanonische PidTagSearchFolderTemplateId-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="13dd4-103">PidTagSearchFolderTemplateId Canonical Property</span></span>

  
  
<span data-ttu-id="13dd4-104">**Betrifft**: Outlook</span><span class="sxs-lookup"><span data-stu-id="13dd4-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="13dd4-105">Enthält die ID der Vorlage, die für die Suche verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="13dd4-105">Contains the ID of the template that is being used for the search.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="13dd4-106">Zugeordneten Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="13dd4-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="13dd4-107">PR_WB_SF_TEMPLATE_ID</span><span class="sxs-lookup"><span data-stu-id="13dd4-107">PR_WB_SF_TEMPLATE_ID</span></span>  <br/> |
|<span data-ttu-id="13dd4-108">Bezeichner:</span><span class="sxs-lookup"><span data-stu-id="13dd4-108">Identifier:</span></span>  <br/> |<span data-ttu-id="13dd4-109">0x6841</span><span class="sxs-lookup"><span data-stu-id="13dd4-109">0x6841</span></span>  <br/> |
|<span data-ttu-id="13dd4-110">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="13dd4-110">Data type:</span></span>  <br/> |<span data-ttu-id="13dd4-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="13dd4-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="13dd4-112">Bereich:</span><span class="sxs-lookup"><span data-stu-id="13dd4-112">Area:</span></span>  <br/> |<span data-ttu-id="13dd4-113">Suchen</span><span class="sxs-lookup"><span data-stu-id="13dd4-113">Search</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="13dd4-114">Hinweise</span><span class="sxs-lookup"><span data-stu-id="13dd4-114">Remarks</span></span>

<span data-ttu-id="13dd4-115">Ordner Suchkriterien wird durch eine Vorlage angegeben.</span><span class="sxs-lookup"><span data-stu-id="13dd4-115">Search folder criteria is specified by a template.</span></span> <span data-ttu-id="13dd4-116">Diese Eigenschaft für die Nachricht, die den Suchordner definiert identifiziert die zugehörige Vorlage.</span><span class="sxs-lookup"><span data-stu-id="13dd4-116">This property on the message that defines the search folder identifies its corresponding template.</span></span> <span data-ttu-id="13dd4-117">Zusätzlich zu den Suchkriterien definieren, eine Vorlage auch Ordner, die von der Suche ausschließen definiert, Elemente aus der Suche ausschließen definiert und gibt den Wert des **PR_WB_SF_STORAGE_TYPE** ([PidTagSearchFolderStorageType](pidtagsearchfolderstoragetype-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="13dd4-117">In addition to defining search criteria, a template also defines folders to exclude from the search, defines items to exclude from the search, and specifies the value of **PR_WB_SF_STORAGE_TYPE** ([PidTagSearchFolderStorageType](pidtagsearchfolderstoragetype-canonical-property.md)).</span></span>
  
<span data-ttu-id="13dd4-118">Weitere Informationen zu Search Ordnervorlagen finden Sie unter [[MS-OXOSRCH]](http://msdn.microsoft.com/library/c72e49b8-78c7-4483-ad65-e46e9133673b%28Office.15%29.aspx) .</span><span class="sxs-lookup"><span data-stu-id="13dd4-118">For more information about Search Folder Templates see [[MS-OXOSRCH]](http://msdn.microsoft.com/library/c72e49b8-78c7-4483-ad65-e46e9133673b%28Office.15%29.aspx) .</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="13dd4-119">Verwandte Ressourcen</span><span class="sxs-lookup"><span data-stu-id="13dd4-119">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="13dd4-120">Protokollspezifikationen</span><span class="sxs-lookup"><span data-stu-id="13dd4-120">Protocol specifications</span></span>

<span data-ttu-id="13dd4-121">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="13dd4-121">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="13dd4-122">Bietet Verweise auf Verwandte Exchange Server-Spezifikationen.</span><span class="sxs-lookup"><span data-stu-id="13dd4-122">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="13dd4-123">[[MS-OXOSRCH]](http://msdn.microsoft.com/library/c72e49b8-78c7-4483-ad65-e46e9133673b%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="13dd4-123">[[MS-OXOSRCH]](http://msdn.microsoft.com/library/c72e49b8-78c7-4483-ad65-e46e9133673b%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="13dd4-124">Gibt die Eigenschaften und Operationen für das Bearbeiten der Liste einer Suchkonfiguration-Ordner.</span><span class="sxs-lookup"><span data-stu-id="13dd4-124">Specifies the properties and operations for manipulating a search folder list configuration.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="13dd4-125">Header-Dateien</span><span class="sxs-lookup"><span data-stu-id="13dd4-125">Header files</span></span>

<span data-ttu-id="13dd4-126">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="13dd4-126">Mapidefs.h</span></span>
  
> <span data-ttu-id="13dd4-127">Enthält die Datentypdefinitionen.</span><span class="sxs-lookup"><span data-stu-id="13dd4-127">Provides data type definitions.</span></span>
    
<span data-ttu-id="13dd4-128">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="13dd4-128">Mapitags.h</span></span>
  
> <span data-ttu-id="13dd4-129">Enthält Definitionen von Eigenschaften, die als Alternative Namen aufgelistet.</span><span class="sxs-lookup"><span data-stu-id="13dd4-129">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="13dd4-130">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="13dd4-130">See also</span></span>



[<span data-ttu-id="13dd4-131">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="13dd4-131">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="13dd4-132">Kanonische MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="13dd4-132">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="13dd4-133">Zuordnen von kanonischen Eigenschaftennamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="13dd4-133">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="13dd4-134">Zuordnen von MAPI-Namen zu kanonische Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="13dd4-134">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

