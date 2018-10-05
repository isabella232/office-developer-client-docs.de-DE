---
title: PidTagSearchFolderDefinition (kanonische Eigenschaft)
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
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 3b4e5fa7228cf243c79a8ec0c9e2b73b7da21c6f
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/04/2018
ms.locfileid: "25398787"
---
# <a name="pidtagsearchfolderdefinition-canonical-property"></a><span data-ttu-id="448da-103">PidTagSearchFolderDefinition (kanonische Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="448da-103">PidTagSearchFolderDefinition Canonical Property</span></span>

  
  
<span data-ttu-id="448da-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="448da-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="448da-105">Enthält Daten, die die Suchkriterien angibt.</span><span class="sxs-lookup"><span data-stu-id="448da-105">Contains data that specifies the search criteria.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="448da-106">Zugeordnete Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="448da-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="448da-107">PR_WB_SF_DEFINITION</span><span class="sxs-lookup"><span data-stu-id="448da-107">PR_WB_SF_DEFINITION</span></span>  <br/> |
|<span data-ttu-id="448da-108">Kennung:</span><span class="sxs-lookup"><span data-stu-id="448da-108">Identifier:</span></span>  <br/> |<span data-ttu-id="448da-109">0x6845</span><span class="sxs-lookup"><span data-stu-id="448da-109">0x6845</span></span>  <br/> |
|<span data-ttu-id="448da-110">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="448da-110">Data type:</span></span>  <br/> |<span data-ttu-id="448da-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="448da-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="448da-112">Bereich:</span><span class="sxs-lookup"><span data-stu-id="448da-112">Area:</span></span>  <br/> |<span data-ttu-id="448da-113">Suche</span><span class="sxs-lookup"><span data-stu-id="448da-113">Search</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="448da-114">Hinweise</span><span class="sxs-lookup"><span data-stu-id="448da-114">Remarks</span></span>

<span data-ttu-id="448da-115">Der Inhalt der einzelnen Felder des binary large Object (BLOB) in dieser Eigenschaft enthaltenen ist abhängig von der Vorlagen-ID, die in **PidTagSearchFolderTemplateId** ([PidTagSearchFolderTemplateId](pidtagsearchfoldertemplateid-canonical-property.md))-Eigenschaft angegeben ist.</span><span class="sxs-lookup"><span data-stu-id="448da-115">The specific content of each field of the binary large object (BLOB) contained in this property is dependent upon the template ID that is specified in **PidTagSearchFolderTemplateId** ([PidTagSearchFolderTemplateId](pidtagsearchfoldertemplateid-canonical-property.md)) property.</span></span> <span data-ttu-id="448da-116">Informationen zu den BLOB-Struktur, und suchen Sie die Vorlagen finden Sie unter [[MS-OXOSRCH]](https://msdn.microsoft.com/library/c72e49b8-78c7-4483-ad65-e46e9133673b%28Office.15%29.aspx).</span><span class="sxs-lookup"><span data-stu-id="448da-116">For information about the BLOB structure and search templates, see [[MS-OXOSRCH]](https://msdn.microsoft.com/library/c72e49b8-78c7-4483-ad65-e46e9133673b%28Office.15%29.aspx).</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="448da-117">Verwandte Ressourcen</span><span class="sxs-lookup"><span data-stu-id="448da-117">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="448da-118">Protokollspezifikationen</span><span class="sxs-lookup"><span data-stu-id="448da-118">Protocol specifications</span></span>

<span data-ttu-id="448da-119">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="448da-119">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="448da-120">Bietet Verweise auf Verwandte Exchange Server-Spezifikationen.</span><span class="sxs-lookup"><span data-stu-id="448da-120">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="448da-121">[[MS-OXOSRCH]](https://msdn.microsoft.com/library/c72e49b8-78c7-4483-ad65-e46e9133673b%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="448da-121">[[MS-OXOSRCH]](https://msdn.microsoft.com/library/c72e49b8-78c7-4483-ad65-e46e9133673b%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="448da-122">Gibt die Eigenschaften und Operationen für das Bearbeiten der Liste einer Suchkonfiguration-Ordner.</span><span class="sxs-lookup"><span data-stu-id="448da-122">Specifies the properties and operations for manipulating a search folder list configuration.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="448da-123">Header-Dateien</span><span class="sxs-lookup"><span data-stu-id="448da-123">Header files</span></span>

<span data-ttu-id="448da-124">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="448da-124">Mapidefs.h</span></span>
  
> <span data-ttu-id="448da-125">Enthält die Datentypdefinitionen.</span><span class="sxs-lookup"><span data-stu-id="448da-125">Provides data type definitions.</span></span>
    
<span data-ttu-id="448da-126">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="448da-126">Mapitags.h</span></span>
  
> <span data-ttu-id="448da-127">Enthält Definitionen von Eigenschaften, die als Alternative Namen aufgelistet.</span><span class="sxs-lookup"><span data-stu-id="448da-127">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="448da-128">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="448da-128">See also</span></span>



[<span data-ttu-id="448da-129">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="448da-129">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="448da-130">Kanonische MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="448da-130">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="448da-131">Zuordnen von kanonischen Eigenschaftennamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="448da-131">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="448da-132">Zuordnen von MAPI-Namen zu kanonische Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="448da-132">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

