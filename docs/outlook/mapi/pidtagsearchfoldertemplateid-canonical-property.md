---
title: Kanonische Pidtagsearchfoldertemplateid (-Eigenschaft
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
ms.openlocfilehash: bee22a7a435b99f4b94473a3f6eb4b7f32517128
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32336624"
---
# <a name="pidtagsearchfoldertemplateid-canonical-property"></a><span data-ttu-id="52890-103">Kanonische Pidtagsearchfoldertemplateid (-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="52890-103">PidTagSearchFolderTemplateId Canonical Property</span></span>

  
  
<span data-ttu-id="52890-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="52890-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="52890-105">Enthält die ID der Vorlage, die für die Suche verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="52890-105">Contains the ID of the template that is being used for the search.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="52890-106">Zugeordnete Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="52890-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="52890-107">PR_WB_SF_TEMPLATE_ID</span><span class="sxs-lookup"><span data-stu-id="52890-107">PR_WB_SF_TEMPLATE_ID</span></span>  <br/> |
|<span data-ttu-id="52890-108">Kennung:</span><span class="sxs-lookup"><span data-stu-id="52890-108">Identifier:</span></span>  <br/> |<span data-ttu-id="52890-109">0x6841</span><span class="sxs-lookup"><span data-stu-id="52890-109">0x6841</span></span>  <br/> |
|<span data-ttu-id="52890-110">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="52890-110">Data type:</span></span>  <br/> |<span data-ttu-id="52890-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="52890-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="52890-112">Bereich:</span><span class="sxs-lookup"><span data-stu-id="52890-112">Area:</span></span>  <br/> |<span data-ttu-id="52890-113">Suche</span><span class="sxs-lookup"><span data-stu-id="52890-113">Search</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="52890-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="52890-114">Remarks</span></span>

<span data-ttu-id="52890-115">Suchordnerkriterien werden durch eine Vorlage angegeben.</span><span class="sxs-lookup"><span data-stu-id="52890-115">Search folder criteria is specified by a template.</span></span> <span data-ttu-id="52890-116">Diese Eigenschaft in der Nachricht, die den Suchordner definiert, identifiziert die entsprechende Vorlage.</span><span class="sxs-lookup"><span data-stu-id="52890-116">This property on the message that defines the search folder identifies its corresponding template.</span></span> <span data-ttu-id="52890-117">Zusätzlich zum Definieren von Suchkriterien definiert eine Vorlage auch Ordner, die von der Suche ausgeschlossen werden sollen, definiert Elemente, die aus der Suche ausgeschlossen werden sollen, und gibt den Wert von **PR_WB_SF_STORAGE_TYPE** ([pidtagsearchfolderstoragetype (](pidtagsearchfolderstoragetype-canonical-property.md)) an.</span><span class="sxs-lookup"><span data-stu-id="52890-117">In addition to defining search criteria, a template also defines folders to exclude from the search, defines items to exclude from the search, and specifies the value of **PR_WB_SF_STORAGE_TYPE** ([PidTagSearchFolderStorageType](pidtagsearchfolderstoragetype-canonical-property.md)).</span></span>
  
<span data-ttu-id="52890-118">Weitere Informationen zu Suchordner Vorlagen finden Sie unter [[MS-OXOSRCH]](https://msdn.microsoft.com/library/c72e49b8-78c7-4483-ad65-e46e9133673b%28Office.15%29.aspx) .</span><span class="sxs-lookup"><span data-stu-id="52890-118">For more information about Search Folder Templates see [[MS-OXOSRCH]](https://msdn.microsoft.com/library/c72e49b8-78c7-4483-ad65-e46e9133673b%28Office.15%29.aspx) .</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="52890-119">Zugehörige Ressourcen</span><span class="sxs-lookup"><span data-stu-id="52890-119">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="52890-120">Protokollspezifikationen</span><span class="sxs-lookup"><span data-stu-id="52890-120">Protocol specifications</span></span>

<span data-ttu-id="52890-121">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="52890-121">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="52890-122">Enthält Verweise auf zugehörige Exchange Server-Protokollspezifikationen.</span><span class="sxs-lookup"><span data-stu-id="52890-122">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="52890-123">[[MS-OXOSRCH]](https://msdn.microsoft.com/library/c72e49b8-78c7-4483-ad65-e46e9133673b%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="52890-123">[[MS-OXOSRCH]](https://msdn.microsoft.com/library/c72e49b8-78c7-4483-ad65-e46e9133673b%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="52890-124">Gibt die Eigenschaften und Vorgänge zum Bearbeiten einer Suchordner Listen Konfiguration an.</span><span class="sxs-lookup"><span data-stu-id="52890-124">Specifies the properties and operations for manipulating a search folder list configuration.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="52890-125">Header Dateien</span><span class="sxs-lookup"><span data-stu-id="52890-125">Header files</span></span>

<span data-ttu-id="52890-126">Mapidefs. h</span><span class="sxs-lookup"><span data-stu-id="52890-126">Mapidefs.h</span></span>
  
> <span data-ttu-id="52890-127">Stellt Datentypdefinitionen bereit.</span><span class="sxs-lookup"><span data-stu-id="52890-127">Provides data type definitions.</span></span>
    
<span data-ttu-id="52890-128">Mapitags. h</span><span class="sxs-lookup"><span data-stu-id="52890-128">Mapitags.h</span></span>
  
> <span data-ttu-id="52890-129">Enthält Definitionen von Eigenschaften, die als Alternative Namen aufgeführt sind.</span><span class="sxs-lookup"><span data-stu-id="52890-129">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="52890-130">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="52890-130">See also</span></span>



[<span data-ttu-id="52890-131">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="52890-131">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="52890-132">Kanonische MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="52890-132">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="52890-133">Zuordnen von kanonischen Eigenschaftennamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="52890-133">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="52890-134">Zuordnen von MAPI-Namen zu kanonischen Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="52890-134">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

