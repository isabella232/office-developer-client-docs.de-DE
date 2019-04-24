---
title: Kanonische Pidlidcategories (-Eigenschaft
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidCategories
api_type:
- COM
ms.assetid: 6ad2aedc-405b-475e-ac76-7ecbbef28f73
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: b2047f04f3f4a8d2b3e58e07a71e7e2463eff9cf
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32344975"
---
# <a name="pidlidcategories-canonical-property"></a><span data-ttu-id="50325-103">Kanonische Pidlidcategories (-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="50325-103">PidLidCategories Canonical Property</span></span>

  
  
<span data-ttu-id="50325-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="50325-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="50325-105">Gibt eine Liste der Kategorien für ein Element an.</span><span class="sxs-lookup"><span data-stu-id="50325-105">Specifies a list of categories for an item.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="50325-106">Zugeordnete Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="50325-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="50325-107">dispidCategories</span><span class="sxs-lookup"><span data-stu-id="50325-107">dispidCategories</span></span>  <br/> |
|<span data-ttu-id="50325-108">Eigenschaftensatz:</span><span class="sxs-lookup"><span data-stu-id="50325-108">Property set:</span></span>  <br/> |<span data-ttu-id="50325-109">PS_PUBLIC_STRINGS</span><span class="sxs-lookup"><span data-stu-id="50325-109">PS_PUBLIC_STRINGS</span></span>  <br/> |
|<span data-ttu-id="50325-110">Long-ID (Deckel):</span><span class="sxs-lookup"><span data-stu-id="50325-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="50325-111">0x00002328</span><span class="sxs-lookup"><span data-stu-id="50325-111">0x00002328</span></span>  <br/> |
|<span data-ttu-id="50325-112">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="50325-112">Data type:</span></span>  <br/> |<span data-ttu-id="50325-113">PT_MV_UNICODE</span><span class="sxs-lookup"><span data-stu-id="50325-113">PT_MV_UNICODE</span></span>  <br/> |
|<span data-ttu-id="50325-114">Bereich:</span><span class="sxs-lookup"><span data-stu-id="50325-114">Area:</span></span>  <br/> |<span data-ttu-id="50325-115">Standard</span><span class="sxs-lookup"><span data-stu-id="50325-115">Common</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="50325-116">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="50325-116">Remarks</span></span>

<span data-ttu-id="50325-117">Um ein Schlüsselwort-Kopfzeilenfeld zu generieren, müssen Clients den Wert dieser Eigenschaft auf die gewünschten Werte festlegen.</span><span class="sxs-lookup"><span data-stu-id="50325-117">To generate a keywords header field, clients must set the value of this property to the desired values.</span></span> <span data-ttu-id="50325-118">Diese Eigenschaft hat mehrere Zeichenfolgen; jede Kategorie sollte einem einzelnen Schlüsselwort zugeordnet werden.</span><span class="sxs-lookup"><span data-stu-id="50325-118">This property has multiple strings; each category should be mapped to a single keyword.</span></span>
  
<span data-ttu-id="50325-119">MIME-Writer (Multipurpose Internet Mail Extensions) sollte jeden unter Wert dieser Eigenschaft in ein separates Schlüsselwort im Kopfzeilenfeld Schlüsselwörter kopieren, wobei jedes Schlüsselwort durch ein Komma (U + 002C) und Leerzeichen (U + 0020) getrennt wird.</span><span class="sxs-lookup"><span data-stu-id="50325-119">Multipurpose Internet Mail Extensions (MIME) writers should copy each sub-value of this property to a separate keyword in the Keywords header field, with a comma (U+002C) and space (U+0020) separating each keyword.</span></span> <span data-ttu-id="50325-120">MIME-Writer können diese Eigenschaft ablegen, anstatt Sie in das Schlüsselwort-Kopfzeilenfeld zu kopieren, um Konflikte zwischen verschiedenen Gruppen von Kategorien in unterschiedlichen Organisationen zu vermeiden.</span><span class="sxs-lookup"><span data-stu-id="50325-120">MIME writers may drop this property instead of copying it to the keywords header field, in order to avoid conflict among different sets of categories in different organizations.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="50325-121">Zugehörige Ressourcen</span><span class="sxs-lookup"><span data-stu-id="50325-121">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="50325-122">Protokollspezifikationen</span><span class="sxs-lookup"><span data-stu-id="50325-122">Protocol specifications</span></span>

<span data-ttu-id="50325-123">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="50325-123">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="50325-124">Stellt die Eigenschaftensatz Definition und Verweise auf zugehörige Exchange Server-Protokollspezifikationen bereit.</span><span class="sxs-lookup"><span data-stu-id="50325-124">Provides property set definition and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="50325-125">[[MS-OXCMAIL]](https://msdn.microsoft.com/library/b60d48db-183f-4bf5-a908-f584e62cb2d4%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="50325-125">[[MS-OXCMAIL]](https://msdn.microsoft.com/library/b60d48db-183f-4bf5-a908-f584e62cb2d4%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="50325-126">Konvertiert von Internet Standard-e-Mail-Konventionen in Nachrichtenobjekte.</span><span class="sxs-lookup"><span data-stu-id="50325-126">Converts from Internet standard email conventions to message objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="50325-127">Header Dateien</span><span class="sxs-lookup"><span data-stu-id="50325-127">Header files</span></span>

<span data-ttu-id="50325-128">Mapidefs. h</span><span class="sxs-lookup"><span data-stu-id="50325-128">Mapidefs.h</span></span>
  
> <span data-ttu-id="50325-129">Stellt Datentypdefinitionen bereit.</span><span class="sxs-lookup"><span data-stu-id="50325-129">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="50325-130">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="50325-130">See also</span></span>



[<span data-ttu-id="50325-131">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="50325-131">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="50325-132">Kanonische MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="50325-132">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="50325-133">Zuordnen von kanonischen Eigenschaftennamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="50325-133">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="50325-134">Zuordnen von MAPI-Namen zu kanonischen Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="50325-134">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

