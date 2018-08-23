---
title: PidLidCategories (kanonische Eigenschaft)
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
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 6893afa11cc08b335b0ffb39b725e26478dae22f
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2018
ms.locfileid: "22574839"
---
# <a name="pidlidcategories-canonical-property"></a><span data-ttu-id="5578e-103">PidLidCategories (kanonische Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="5578e-103">PidLidCategories Canonical Property</span></span>

  
  
<span data-ttu-id="5578e-104">**Betrifft**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="5578e-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="5578e-105">Gibt eine Liste der Kategorien für ein Element.</span><span class="sxs-lookup"><span data-stu-id="5578e-105">Specifies a list of categories for an item.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="5578e-106">Zugeordnete Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="5578e-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="5578e-107">dispidCategories</span><span class="sxs-lookup"><span data-stu-id="5578e-107">dispidCategories</span></span>  <br/> |
|<span data-ttu-id="5578e-108">-Eigenschaft festgelegt:</span><span class="sxs-lookup"><span data-stu-id="5578e-108">Property set:</span></span>  <br/> |<span data-ttu-id="5578e-109">PS_PUBLIC_STRINGS</span><span class="sxs-lookup"><span data-stu-id="5578e-109">PS_PUBLIC_STRINGS</span></span>  <br/> |
|<span data-ttu-id="5578e-110">Long-ID (Abdeckung):</span><span class="sxs-lookup"><span data-stu-id="5578e-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="5578e-111">0x00002328</span><span class="sxs-lookup"><span data-stu-id="5578e-111">0x00002328</span></span>  <br/> |
|<span data-ttu-id="5578e-112">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="5578e-112">Data type:</span></span>  <br/> |<span data-ttu-id="5578e-113">PT_MV_UNICODE</span><span class="sxs-lookup"><span data-stu-id="5578e-113">PT_MV_UNICODE</span></span>  <br/> |
|<span data-ttu-id="5578e-114">Bereich:</span><span class="sxs-lookup"><span data-stu-id="5578e-114">Area:</span></span>  <br/> |<span data-ttu-id="5578e-115">Common</span><span class="sxs-lookup"><span data-stu-id="5578e-115">Common</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="5578e-116">HinwBemerkungeneise</span><span class="sxs-lookup"><span data-stu-id="5578e-116">Remarks</span></span>

<span data-ttu-id="5578e-117">Um ein Kopfzeilenfeld Schlüsselwörter generiert werden soll, müssen die Clients den Wert dieser Eigenschaft auf die gewünschten Werte festgelegt.</span><span class="sxs-lookup"><span data-stu-id="5578e-117">To generate a keywords header field, clients must set the value of this property to the desired values.</span></span> <span data-ttu-id="5578e-118">Diese Eigenschaft hat mehrere Zeichenfolgen. jeder Kategorie sollte zu einem einzelnen Stichwort zugeordnet werden.</span><span class="sxs-lookup"><span data-stu-id="5578e-118">This property has multiple strings; each category should be mapped to a single keyword.</span></span>
  
<span data-ttu-id="5578e-119">Multipurpose Internet Mail Extensions (MIME)-Autoren sollten jeder untergeordneten Wert dieser Eigenschaft zu einem separaten Stichwort in das Feld Schlüsselwörter Kopf durch ein Komma (U + 002 C) und Leerzeichen (U + 0020) trennen kopieren jedes Schlüsselwort.</span><span class="sxs-lookup"><span data-stu-id="5578e-119">Multipurpose Internet Mail Extensions (MIME) writers should copy each sub-value of this property to a separate keyword in the Keywords header field, with a comma (U+002C) and space (U+0020) separating each keyword.</span></span> <span data-ttu-id="5578e-120">MIME-Writer können diese Eigenschaft nicht kopiert werden soll, um einen Konflikt zwischen verschiedenen Sätze von Kategorien in unterschiedlichen Organisationen zu vermeiden dem Feld Stichwörter Kopfzeile löschen.</span><span class="sxs-lookup"><span data-stu-id="5578e-120">MIME writers may drop this property instead of copying it to the keywords header field, in order to avoid conflict among different sets of categories in different organizations.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="5578e-121">Verwandte Ressourcen</span><span class="sxs-lookup"><span data-stu-id="5578e-121">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="5578e-122">Protokollspezifikationen</span><span class="sxs-lookup"><span data-stu-id="5578e-122">Protocol specifications</span></span>

<span data-ttu-id="5578e-123">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="5578e-123">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="5578e-124">Enthält Set Eigenschaftendefinition und Verweise auf Verwandte Exchange Server-Spezifikationen.</span><span class="sxs-lookup"><span data-stu-id="5578e-124">Provides property set definition and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="5578e-125">[[MS-OXCMAIL]](http://msdn.microsoft.com/library/b60d48db-183f-4bf5-a908-f584e62cb2d4%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="5578e-125">[[MS-OXCMAIL]](http://msdn.microsoft.com/library/b60d48db-183f-4bf5-a908-f584e62cb2d4%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="5578e-126">Konvertiert von Internet-standard-e-Mail-Konventionen in Message-Objekten.</span><span class="sxs-lookup"><span data-stu-id="5578e-126">Converts from Internet standard email conventions to message objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="5578e-127">Header-Dateien</span><span class="sxs-lookup"><span data-stu-id="5578e-127">Header files</span></span>

<span data-ttu-id="5578e-128">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="5578e-128">Mapidefs.h</span></span>
  
> <span data-ttu-id="5578e-129">Enthält die Datentypdefinitionen.</span><span class="sxs-lookup"><span data-stu-id="5578e-129">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="5578e-130">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="5578e-130">See also</span></span>



[<span data-ttu-id="5578e-131">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="5578e-131">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="5578e-132">Kanonische MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="5578e-132">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="5578e-133">Zuordnen von kanonischen Eigenschaftennamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="5578e-133">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="5578e-134">Zuordnen von MAPI-Namen zu kanonische Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="5578e-134">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

