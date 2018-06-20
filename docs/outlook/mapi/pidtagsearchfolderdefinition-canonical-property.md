---
title: Kanonische PidTagSearchFolderDefinition-Eigenschaft
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagSearchFolderDefinition
api_type:
- COM
ms.assetid: a61056e7-365c-4972-abf7-26e2ab07105d
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: d19904b65b95468bd38df75aa8e05afdf0075961
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19795104"
---
# <a name="pidtagsearchfolderdefinition-canonical-property"></a><span data-ttu-id="72e36-103">Kanonische PidTagSearchFolderDefinition-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="72e36-103">PidTagSearchFolderDefinition Canonical Property</span></span>

  
  
<span data-ttu-id="72e36-104">**Betrifft**: Outlook</span><span class="sxs-lookup"><span data-stu-id="72e36-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="72e36-105">Enthält Daten, die die Suchkriterien angibt.</span><span class="sxs-lookup"><span data-stu-id="72e36-105">Contains data that specifies the search criteria.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="72e36-106">Zugeordneten Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="72e36-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="72e36-107">PR_WB_SF_DEFINITION</span><span class="sxs-lookup"><span data-stu-id="72e36-107">PR_WB_SF_DEFINITION</span></span>  <br/> |
|<span data-ttu-id="72e36-108">Bezeichner:</span><span class="sxs-lookup"><span data-stu-id="72e36-108">Identifier:</span></span>  <br/> |<span data-ttu-id="72e36-109">0x6845</span><span class="sxs-lookup"><span data-stu-id="72e36-109">0x6845</span></span>  <br/> |
|<span data-ttu-id="72e36-110">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="72e36-110">Data type:</span></span>  <br/> |<span data-ttu-id="72e36-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="72e36-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="72e36-112">Bereich:</span><span class="sxs-lookup"><span data-stu-id="72e36-112">Area:</span></span>  <br/> |<span data-ttu-id="72e36-113">Suchen</span><span class="sxs-lookup"><span data-stu-id="72e36-113">Search</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="72e36-114">Hinweise</span><span class="sxs-lookup"><span data-stu-id="72e36-114">Remarks</span></span>

<span data-ttu-id="72e36-115">Der Inhalt der einzelnen Felder des binary large Object (BLOB) in dieser Eigenschaft enthaltenen ist abhängig von der Vorlagen-ID, die in **PidTagSearchFolderTemplateId** ([PidTagSearchFolderTemplateId](pidtagsearchfoldertemplateid-canonical-property.md))-Eigenschaft angegeben ist.</span><span class="sxs-lookup"><span data-stu-id="72e36-115">The specific content of each field of the binary large object (BLOB) contained in this property is dependent upon the template ID that is specified in **PidTagSearchFolderTemplateId** ([PidTagSearchFolderTemplateId](pidtagsearchfoldertemplateid-canonical-property.md)) property.</span></span> <span data-ttu-id="72e36-116">Informationen zu den BLOB-Struktur, und suchen Sie die Vorlagen finden Sie unter [[MS-OXOSRCH]](http://msdn.microsoft.com/library/c72e49b8-78c7-4483-ad65-e46e9133673b%28Office.15%29.aspx).</span><span class="sxs-lookup"><span data-stu-id="72e36-116">For information about the BLOB structure and search templates, see [[MS-OXOSRCH]](http://msdn.microsoft.com/library/c72e49b8-78c7-4483-ad65-e46e9133673b%28Office.15%29.aspx).</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="72e36-117">Verwandte Ressourcen</span><span class="sxs-lookup"><span data-stu-id="72e36-117">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="72e36-118">Protokollspezifikationen</span><span class="sxs-lookup"><span data-stu-id="72e36-118">Protocol specifications</span></span>

<span data-ttu-id="72e36-119">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="72e36-119">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="72e36-120">Bietet Verweise auf Verwandte Exchange Server-Spezifikationen.</span><span class="sxs-lookup"><span data-stu-id="72e36-120">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="72e36-121">[[MS-OXOSRCH]](http://msdn.microsoft.com/library/c72e49b8-78c7-4483-ad65-e46e9133673b%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="72e36-121">[[MS-OXOSRCH]](http://msdn.microsoft.com/library/c72e49b8-78c7-4483-ad65-e46e9133673b%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="72e36-122">Gibt die Eigenschaften und Operationen für das Bearbeiten der Liste einer Suchkonfiguration-Ordner.</span><span class="sxs-lookup"><span data-stu-id="72e36-122">Specifies the properties and operations for manipulating a search folder list configuration.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="72e36-123">Header-Dateien</span><span class="sxs-lookup"><span data-stu-id="72e36-123">Header files</span></span>

<span data-ttu-id="72e36-124">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="72e36-124">Mapidefs.h</span></span>
  
> <span data-ttu-id="72e36-125">Enthält die Datentypdefinitionen.</span><span class="sxs-lookup"><span data-stu-id="72e36-125">Provides data type definitions.</span></span>
    
<span data-ttu-id="72e36-126">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="72e36-126">Mapitags.h</span></span>
  
> <span data-ttu-id="72e36-127">Enthält Definitionen von Eigenschaften, die als Alternative Namen aufgelistet.</span><span class="sxs-lookup"><span data-stu-id="72e36-127">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="72e36-128">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="72e36-128">See also</span></span>



[<span data-ttu-id="72e36-129">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="72e36-129">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="72e36-130">Kanonische MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="72e36-130">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="72e36-131">Zuordnen von kanonischen Eigenschaftennamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="72e36-131">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="72e36-132">Zuordnen von MAPI-Namen zu kanonische Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="72e36-132">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

