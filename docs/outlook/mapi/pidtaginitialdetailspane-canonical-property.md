---
title: PidTagInitialDetailsPane (kanonische Eigenschaft)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagInitialDetailsPane
api_type:
- HeaderDef
ms.assetid: c4712133-6fbd-4c50-a258-5f4317120476
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 0ea7d0a17fdb6dba047cb97290d991ce384d4750
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2018
ms.locfileid: "22573936"
---
# <a name="pidtaginitialdetailspane-canonical-property"></a><span data-ttu-id="5c0b0-103">PidTagInitialDetailsPane (kanonische Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="5c0b0-103">PidTagInitialDetailsPane Canonical Property</span></span>

  
  
<span data-ttu-id="5c0b0-104">**Betrifft**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="5c0b0-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="5c0b0-105">Gibt eine Anzeigevorlage zum ersten Anzeigen der Seite an.</span><span class="sxs-lookup"><span data-stu-id="5c0b0-105">Indicates the page of a display template to display first.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="5c0b0-106">Zugeordnete Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="5c0b0-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="5c0b0-107">PR_INITIAL_DETAILS_PANE</span><span class="sxs-lookup"><span data-stu-id="5c0b0-107">PR_INITIAL_DETAILS_PANE</span></span>  <br/> |
|<span data-ttu-id="5c0b0-108">Kennung:</span><span class="sxs-lookup"><span data-stu-id="5c0b0-108">Identifier:</span></span>  <br/> |<span data-ttu-id="5c0b0-109">0x3F08</span><span class="sxs-lookup"><span data-stu-id="5c0b0-109">0x3F08</span></span>  <br/> |
|<span data-ttu-id="5c0b0-110">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="5c0b0-110">Data type:</span></span>  <br/> |<span data-ttu-id="5c0b0-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="5c0b0-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="5c0b0-112">Bereich:</span><span class="sxs-lookup"><span data-stu-id="5c0b0-112">Area:</span></span>  <br/> |<span data-ttu-id="5c0b0-113">MAPI-Anzeige Tabellen</span><span class="sxs-lookup"><span data-stu-id="5c0b0-113">MAPI Display Tables</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="5c0b0-114">HinwBemerkungeneise</span><span class="sxs-lookup"><span data-stu-id="5c0b0-114">Remarks</span></span>

<span data-ttu-id="5c0b0-115">Es muss auf allen Address Book-Objekten auf einem Server (NSPI = Name Service Provider Interface) vorhanden sein und muss den Wert NULL (0) sein.</span><span class="sxs-lookup"><span data-stu-id="5c0b0-115">It must be present on all address book objects on an Name Service Provider Interface (NSPI) server, and must have the value zero (0).</span></span> <span data-ttu-id="5c0b0-116">Sie müssen nicht für alle Objekte in einem Offline-Adressbuch definiert werden.</span><span class="sxs-lookup"><span data-stu-id="5c0b0-116">It must not be defined for any objects in an Offline Address Book.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="5c0b0-117">Verwandte Ressourcen</span><span class="sxs-lookup"><span data-stu-id="5c0b0-117">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="5c0b0-118">Protokollspezifikationen</span><span class="sxs-lookup"><span data-stu-id="5c0b0-118">Protocol specifications</span></span>

<span data-ttu-id="5c0b0-119">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="5c0b0-119">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="5c0b0-120">Bietet Verweise auf Verwandte Exchange Server-Spezifikationen.</span><span class="sxs-lookup"><span data-stu-id="5c0b0-120">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="5c0b0-121">[[MS-OXOABK]](http://msdn.microsoft.com/library/f4cf9b4c-9232-4506-9e71-2270de217614%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="5c0b0-121">[[MS-OXOABK]](http://msdn.microsoft.com/library/f4cf9b4c-9232-4506-9e71-2270de217614%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="5c0b0-122">Gibt die Eigenschaften und Operationen für Listen der Benutzer, Kontakte, Gruppen und Ressourcen.</span><span class="sxs-lookup"><span data-stu-id="5c0b0-122">Specifies the properties and operations for lists of users, contacts, groups, and resources.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="5c0b0-123">Header-Dateien</span><span class="sxs-lookup"><span data-stu-id="5c0b0-123">Header files</span></span>

<span data-ttu-id="5c0b0-124">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="5c0b0-124">Mapidefs.h</span></span>
  
> <span data-ttu-id="5c0b0-125">Enthält die Datentypdefinitionen.</span><span class="sxs-lookup"><span data-stu-id="5c0b0-125">Provides data type definitions.</span></span>
    
<span data-ttu-id="5c0b0-126">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="5c0b0-126">Mapitags.h</span></span>
  
> <span data-ttu-id="5c0b0-127">Enthält Definitionen von Eigenschaften, die als zugeordneten Eigenschaften aufgelistet.</span><span class="sxs-lookup"><span data-stu-id="5c0b0-127">Contains definitions of properties listed as associated properties.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="5c0b0-128">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="5c0b0-128">See also</span></span>



[<span data-ttu-id="5c0b0-129">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="5c0b0-129">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="5c0b0-130">Kanonische MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="5c0b0-130">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="5c0b0-131">Zuordnen von kanonischen Eigenschaftennamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="5c0b0-131">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="5c0b0-132">Zuordnen von MAPI-Namen zu kanonische Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="5c0b0-132">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

