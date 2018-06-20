---
title: Kanonische PidLidCategories-Eigenschaft
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
ms.openlocfilehash: 01d4391850067d00645b5c0248e1bf858c2a9049
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19793463"
---
# <a name="pidlidcategories-canonical-property"></a><span data-ttu-id="7a8a8-103">Kanonische PidLidCategories-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="7a8a8-103">PidLidCategories Canonical Property</span></span>

  
  
<span data-ttu-id="7a8a8-104">**Betrifft**: Outlook</span><span class="sxs-lookup"><span data-stu-id="7a8a8-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="7a8a8-105">Gibt eine Liste der Kategorien für ein Element.</span><span class="sxs-lookup"><span data-stu-id="7a8a8-105">Specifies a list of categories for an item.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="7a8a8-106">Zugeordneten Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="7a8a8-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="7a8a8-107">dispidCategories</span><span class="sxs-lookup"><span data-stu-id="7a8a8-107">dispidCategories</span></span>  <br/> |
|<span data-ttu-id="7a8a8-108">-Eigenschaft festgelegt:</span><span class="sxs-lookup"><span data-stu-id="7a8a8-108">Property set:</span></span>  <br/> |<span data-ttu-id="7a8a8-109">PS_PUBLIC_STRINGS</span><span class="sxs-lookup"><span data-stu-id="7a8a8-109">PS_PUBLIC_STRINGS</span></span>  <br/> |
|<span data-ttu-id="7a8a8-110">Long-ID (Abdeckung):</span><span class="sxs-lookup"><span data-stu-id="7a8a8-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="7a8a8-111">0x00002328</span><span class="sxs-lookup"><span data-stu-id="7a8a8-111">0x00002328</span></span>  <br/> |
|<span data-ttu-id="7a8a8-112">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="7a8a8-112">Data type:</span></span>  <br/> |<span data-ttu-id="7a8a8-113">PT_MV_UNICODE</span><span class="sxs-lookup"><span data-stu-id="7a8a8-113">PT_MV_UNICODE</span></span>  <br/> |
|<span data-ttu-id="7a8a8-114">Bereich:</span><span class="sxs-lookup"><span data-stu-id="7a8a8-114">Area:</span></span>  <br/> |<span data-ttu-id="7a8a8-115">Common</span><span class="sxs-lookup"><span data-stu-id="7a8a8-115">Common</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="7a8a8-116">Hinweise</span><span class="sxs-lookup"><span data-stu-id="7a8a8-116">Remarks</span></span>

<span data-ttu-id="7a8a8-117">Um ein Kopfzeilenfeld Schlüsselwörter generiert werden soll, müssen die Clients den Wert dieser Eigenschaft auf die gewünschten Werte festgelegt.</span><span class="sxs-lookup"><span data-stu-id="7a8a8-117">To generate a keywords header field, clients must set the value of this property to the desired values.</span></span> <span data-ttu-id="7a8a8-118">Diese Eigenschaft hat mehrere Zeichenfolgen. jeder Kategorie sollte zu einem einzelnen Stichwort zugeordnet werden.</span><span class="sxs-lookup"><span data-stu-id="7a8a8-118">This property has multiple strings; each category should be mapped to a single keyword.</span></span>
  
<span data-ttu-id="7a8a8-119">Multipurpose Internet Mail Extensions (MIME)-Autoren sollten jeder untergeordneten Wert dieser Eigenschaft zu einem separaten Stichwort in das Feld Schlüsselwörter Kopf durch ein Komma (U + 002 C) und Leerzeichen (U + 0020) trennen kopieren jedes Schlüsselwort.</span><span class="sxs-lookup"><span data-stu-id="7a8a8-119">Multipurpose Internet Mail Extensions (MIME) writers should copy each sub-value of this property to a separate keyword in the Keywords header field, with a comma (U+002C) and space (U+0020) separating each keyword.</span></span> <span data-ttu-id="7a8a8-120">MIME-Writer können diese Eigenschaft nicht kopiert werden soll, um einen Konflikt zwischen verschiedenen Sätze von Kategorien in unterschiedlichen Organisationen zu vermeiden dem Feld Stichwörter Kopfzeile löschen.</span><span class="sxs-lookup"><span data-stu-id="7a8a8-120">MIME writers may drop this property instead of copying it to the keywords header field, in order to avoid conflict among different sets of categories in different organizations.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="7a8a8-121">Verwandte Ressourcen</span><span class="sxs-lookup"><span data-stu-id="7a8a8-121">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="7a8a8-122">Protokollspezifikationen</span><span class="sxs-lookup"><span data-stu-id="7a8a8-122">Protocol specifications</span></span>

<span data-ttu-id="7a8a8-123">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="7a8a8-123">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="7a8a8-124">Enthält Set Eigenschaftendefinition und Verweise auf Verwandte Exchange Server-Spezifikationen.</span><span class="sxs-lookup"><span data-stu-id="7a8a8-124">Provides property set definition and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="7a8a8-125">[[MS-OXCMAIL]](http://msdn.microsoft.com/library/b60d48db-183f-4bf5-a908-f584e62cb2d4%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="7a8a8-125">[[MS-OXCMAIL]](http://msdn.microsoft.com/library/b60d48db-183f-4bf5-a908-f584e62cb2d4%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="7a8a8-126">Konvertiert von Internet-standard-e-Mail-Konventionen in Message-Objekten.</span><span class="sxs-lookup"><span data-stu-id="7a8a8-126">Converts from Internet standard email conventions to message objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="7a8a8-127">Header-Dateien</span><span class="sxs-lookup"><span data-stu-id="7a8a8-127">Header files</span></span>

<span data-ttu-id="7a8a8-128">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="7a8a8-128">Mapidefs.h</span></span>
  
> <span data-ttu-id="7a8a8-129">Enthält die Datentypdefinitionen.</span><span class="sxs-lookup"><span data-stu-id="7a8a8-129">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="7a8a8-130">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="7a8a8-130">See also</span></span>



[<span data-ttu-id="7a8a8-131">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="7a8a8-131">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="7a8a8-132">Kanonische MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="7a8a8-132">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="7a8a8-133">Zuordnen von kanonischen Eigenschaftennamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="7a8a8-133">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="7a8a8-134">Zuordnen von MAPI-Namen zu kanonische Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="7a8a8-134">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

